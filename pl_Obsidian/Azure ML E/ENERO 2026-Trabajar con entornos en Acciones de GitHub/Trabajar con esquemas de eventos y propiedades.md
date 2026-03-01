

La estructura de los eventos determina cómo Event Grid enruta, filtra y entrega a los suscriptores. En esta unidad se explica cómo diseñar eventos mediante el esquema CloudEvents para las operaciones de IA, definir tipos de eventos personalizados que representan cambios de estado significativos y configurar filtros de suscripción de eventos para enrutar eventos en función del tipo, asunto o atributos de datos.

 Nota:

Todos los ejemplos de código de este módulo se basan en la versión más reciente de la `azure-eventgrid` biblioteca en el momento de escribir. La biblioteca se actualiza a menudo y la recomendación es visitar el sitio del [SDK de Azure Event Grid para Python](https://github.com/Azure/azure-sdk-for-python/tree/main/sdk/eventgrid/azure-eventgrid) para obtener la información más actualizada.

## Elección entre el esquema de Event Grid y el esquema de CloudEvents

Event Grid admite dos esquemas de eventos: el esquema propietario de Event Grid y el [esquema open CloudEvents v1.0](https://learn.microsoft.com/es-es/azure/event-grid/cloud-event-schema). CloudEvents es el formato recomendado para las nuevas implementaciones porque proporciona una estructura de eventos independiente del protocolo estandarizada respaldada por Cloud Native Computing Foundation (CNCF). La estandarización significa que los eventos generados por los servicios de IA pueden interoperar con cualquier sistema que admita CloudEvents, no solo Azure Event Grid.

CloudEvents simplifica la integración multiplataforma con un conjunto mínimo de atributos necesarios y un mecanismo de extensión bien definido. Si la canalización de IA implica componentes fuera de Azure, CloudEvents garantiza la coherencia entre los límites. Event Grid admite de forma nativa el formato JSON de CloudEvents y el enlace de protocolo HTTP, por lo que no es necesario transformar eventos antes de publicarlos o consumirlos.

El esquema propietario de Event Grid permanece disponible para la compatibilidad con versiones anteriores. Los [eventos del sistema](https://learn.microsoft.com/es-es/azure/event-grid/system-topics) de Azure existentes se pueden entregar en formato CloudEvents configurando el esquema de salida en la suscripción de eventos. Sin embargo, no se admite la conversión de esquemas de CloudEvents a Event Grid porque CloudEvents admite atributos de extensión que el esquema de Event Grid no admite.

## Descripción de la estructura del esquema de CloudEvents

Un evento CloudEvents contiene atributos necesarios que identifican el evento y los atributos opcionales que proporcionan contexto adicional. Para las operaciones de inteligencia artificial, cada atributo desempeña un papel específico en las decisiones de enrutamiento y filtrado.

En el ejemplo siguiente se muestra un evento JSON de CloudEvents para una operación de inferencia completada en una canalización de moderación de contenido:

JSON

```
{
    "specversion": "1.0",
    "type": "com.contoso.ai.InferenceCompleted",
    "source": "/services/content-moderation",
    "id": "a1b2c3d4-e5f6-7890-abcd-ef1234567890",
    "time": "2025-09-15T14:30:00Z",
    "subject": "/pipelines/moderation/batch-42",
    "datacontenttype": "application/json",
    "data": {
        "modelName": "content-classifier-v3",
        "requestId": "req-78901",
        "resultLocation": "https://storage.blob.core.windows.net/results/batch-42.json",
        "processingDurationMs": 1250,
        "status": "success",
        "itemsProcessed": 150
    }
}
```

Los atributos necesarios sirven para los siguientes propósitos:

- **`specversion`:** identifica la versión de especificación de CloudEvents. Establézcalo siempre en `"1.0"`.
- **`type`:** clasifica el evento. Este campo controla el filtrado del tipo de evento. Use una convención de nomenclatura de DNS inverso para evitar colisiones entre organizaciones y servicios.
- **`source`:** identifica el sistema o componente de origen. Combine con `type` para identificar de forma única el contexto en el que se produjo el evento.
- **`id`:** proporciona un identificador único para este evento específico. Los suscriptores usan este campo para detectar y desduplicar entregas repetidas.

Los atributos opcionales agregan contexto que habilita el enrutamiento más granular:

- **`subject`:** proporciona una ruta de acceso para el filtrado. Establézcalo en un valor jerárquico que refleje el contexto del evento, lo que permite el filtrado de prefijo y sufijo en las suscripciones.
- **`time`:** registra cuándo se produjo el evento en UTC. Útil para la supervisión y depuración.
- **`datacontenttype`:** describe el formato de la carga de datos, normalmente `"application/json"`.
- **`data`:** lleva la carga del evento con detalles específicos de la operación.

## Diseño de tipos de eventos personalizados para flujos de trabajo de IA

Los tipos de eventos bien diseñados facilitan el filtrado, la supervisión y la extensión de la canalización de IA controlada por eventos. Cada tipo de evento debe representar un cambio de estado significativo que al menos un suscriptor debe conocer. Defina tipos mediante una convención de nomenclatura de DNS inverso para evitar colisiones con eventos de otros equipos o servicios.

Entre los tipos de eventos comunes para las aplicaciones de IA se incluyen:

- **`com.contoso.ai.InferenceCompleted`:** se publica cuando una solicitud de inferencia finaliza el procesamiento.
- **`com.contoso.ai.EmbeddingsRefreshed`:** se publica cuando se actualiza un índice de inserción de vectores.
- **`com.contoso.ai.BatchProcessingStarted`:** se publica cuando comienza un trabajo de procesamiento por lotes.
- **`com.contoso.ai.AnomalyDetected`:** se publica cuando el sistema identifica una anomalía en los datos entrantes.
- **`com.contoso.ai.ModelRetrained`:** se publica cuando un modelo completa un ciclo de reentrenamiento.
- **`com.contoso.ai.ContentClassified`:** se publica cuando finaliza una clasificación de moderación de contenido.

Mantenga la carga del evento pequeña y centrada. Incluya suficiente contexto para que el suscriptor empiece a procesar, como un URI de recurso, el nombre del modelo, la duración del procesamiento y un resumen de los resultados. No insertar los resultados completos de la inferencia en los datos del evento. En su lugar, incluya una referencia (como una dirección URL de almacenamiento) que el suscriptor usa para recuperar resultados detallados de un almacén de datos.

## Configuración del filtrado de tipos de evento

Las suscripciones de eventos pueden filtrar eventos por tipo para asegurarse de que cada controlador recibe solo los eventos que necesita. Este enfoque mantiene los controladores centrados y evita invocaciones innecesarias. En el caso de los flujos de trabajo de IA en los que diferentes servicios procesan diferentes tipos de eventos, el filtrado de tipos enruta cada evento al controlador correcto sin una lógica de enrutamiento personalizada en el código.

Puede configurar el filtrado de tipos de evento al crear una suscripción de eventos. El `--included-event-types` parámetro acepta una lista de tipos de eventos que entrega la suscripción. Los eventos con tipos que no están en la lista se filtran antes de la entrega. En el ejemplo siguiente se crea una suscripción de eventos que solo recibe eventos de finalización de inferencia:

Azure CLI

```
az eventgrid event-subscription create \
    --name inference-handler-sub \
    --source-resource-id /subscriptions/{sub-id}/resourceGroups/{rg}/providers/Microsoft.EventGrid/topics/ai-events \
    --endpoint https://inference-handler.azurewebsites.net/api/events \
    --included-event-types com.contoso.ai.InferenceCompleted
```

Puede incluir varios tipos de eventos en una sola suscripción al enumerarlos separados por espacios. Un servicio de supervisión que realiza un seguimiento de las finalizaciones de inferencia y las detecciones de anomalías incluiría ambos tipos en su filtro de suscripción.

## Aplicar el filtrado de asunto para el enrutamiento pormenorizado

El `subject` campo habilita el filtrado basado en ruta mediante coincidencias de prefijos y sufijos. En el caso de las aplicaciones de IA, configure el tema en una ruta de acceso jerárquica que refleje el contexto del evento, como `/pipelines/embeddings/batch-42` o `/models/classification/v3`. Después, los suscriptores pueden filtrar eventos en función de dónde se originó el evento en la jerarquía.

El filtrado de asunto usa dos parámetros en la suscripción de eventos:

- **`subjectBeginsWith`:** Coincide con eventos cuyo asunto comienza con el prefijo especificado. Úselo para enrutar eventos desde una canalización o categoría de servicio específica.
- **`subjectEndsWith`:** Coincide con eventos cuyo asunto termina con el sufijo especificado. Úselo para filtrar por tipo de archivo, versión o estado.

En el ejemplo siguiente se crea una suscripción que recibe solo eventos de la canalización de inserción:

Azure CLI

```
az eventgrid event-subscription create \
    --name embeddings-sub \
    --source-resource-id /subscriptions/{sub-id}/resourceGroups/{rg}/providers/Microsoft.EventGrid/topics/ai-events \
    --endpoint https://embeddings-handler.azurewebsites.net/api/events \
    --subject-begins-with /pipelines/embeddings
```

Puede combinar el filtrado de asunto con el filtrado de tipo de evento en la misma suscripción. Una suscripción de eventos que filtra por el tipo y el prefijo del firmante solo recibe eventos que coinciden con todos los criterios especificados.

## Uso del filtrado avanzado en atributos de datos

Event Grid admite [filtros avanzados](https://learn.microsoft.com/es-es/azure/event-grid/event-filtering#advanced-filtering) que coinciden con valores dentro del cuerpo del evento o los atributos de extensión. Los filtros avanzados permiten tomar decisiones de enrutamiento basadas en el contenido de los datos del evento, como puntuaciones de confianza, nombres de modelo o estados de procesamiento. Esta funcionalidad es especialmente útil para los eventos de inteligencia artificial en los que la decisión de enrutamiento depende de la carga del evento.

Los filtros avanzados usan operadores como `StringContains`, `NumberGreaterThan`, `StringBeginsWith`, , `BoolEquals`y `IsNotNull`. Puede definir hasta 25 condiciones de filtro por suscripción. Varias condiciones usan lógica AND entre condiciones y lógica OR dentro de los valores de cada condición.

En el ejemplo siguiente se crea una suscripción que recibe solo eventos en los que el `data.status` campo es igual a `"flagged"`. Un servicio de revisión de moderación usaría este filtro para recibir solo el contenido que necesita revisión humana:

Azure CLI

```
az eventgrid event-subscription create \
    --name flagged-content-sub \
    --source-resource-id /subscriptions/{sub-id}/resourceGroups/{rg}/providers/Microsoft.EventGrid/topics/ai-events \
    --endpoint https://review-service.azurewebsites.net/api/events \
    --advanced-filter data.status StringIn flagged
```

En el caso de los eventos de IA, los filtros avanzados permiten escenarios de enrutamiento dirigidos, como:

- **Enrutamiento basado en confianza:** Enrutar eventos a diferentes controladores en función de un umbral de puntuación de confianza, como `data.confidence NumberGreaterThan 0.9` para los resultados de confianza alta y una suscripción independiente para puntuaciones inferiores
- **Suscripciones específicas del modelo:** Filtra por `data.modelName` para suscribirte a eventos de una versión determinada del modelo.
- **Flujos de trabajo basados en estado:** se enrutan solo eventos con errores o marcados a una cola de revisión, mientras que los eventos completados fluyen a un servicio de panel.

## Configuración del esquema de entrada y salida

Al crear un tema personalizado, el `input-schema` parámetro controla qué esquema acepta el tema. Establézcalo en `cloudeventschemav1_0` para aceptar eventos en formato CloudEvents:

Azure CLI

```
az eventgrid topic create \
    --name ai-events \
    --resource-group ai-platform-rg \
    --location eastus \
    --input-schema cloudeventschemav1_0
```

Al crear una suscripción de eventos, el `event-delivery-schema` parámetro controla el formato entregado al controlador. Event Grid puede convertir entre el esquema de Event Grid y el esquema de CloudEvents durante la entrega. Si el tema usa el esquema de Event Grid, pero el controlador espera CloudEvents, puede establecer el esquema de salida en consecuencia. Sin embargo, no se admite la conversión de CloudEvents a Event Grid porque CloudEvents admite atributos de extensión que el esquema de Event Grid no puede representar. En el caso de las nuevas implementaciones que usan CloudEvents a lo largo de todo, puede omitir este parámetro y los eventos se entregan en el mismo formato que se publicaron.

# Configuración de directivas de entrega y reintento para el procesamiento fiable de eventos



Los puntos de conexión de la canalización de IA no siempre responden bien al primer intento. Los servicios de modelo se reinician, las funciones sin servidor experimentan arranques en frío y las dependencias posteriores se desconectan temporalmente. En esta unidad se explica cómo Event Grid controla los errores de entrega a través de su mecanismo de reintento, cómo personalizar las directivas de reintento para diferentes patrones de carga de trabajo de IA, cómo configurar destinos de mensajes fallidos para eventos que no se pueden entregar y cómo supervisar los resultados de entrega.

## Descripción de cómo Event Grid entrega eventos

Event Grid entrega eventos mediante el envío de una solicitud HTTP POST al punto de conexión del suscriptor. El suscriptor debe responder con un código de estado correcto (200, 201, 202, 203 o 204) para confirmar la recepción. Cualquier otro código de respuesta, o ninguna respuesta dentro del período de tiempo de espera, desencadena un reintento. Event Grid espera 30 segundos para obtener una respuesta después de entregar un mensaje. Si el punto de conexión no ha respondido dentro de esa ventana, Event Grid pone en cola el mensaje para reintentarlo.

Event Grid entrega un evento cada vez de forma predeterminada, con la carga como una matriz que contiene un único evento. El comportamiento predeterminado garantiza que cada evento se confirme de forma independiente y se vuelva a intentar. Para cargas de trabajo de inteligencia artificial de alto rendimiento, puede habilitar el procesamiento por lotes de salida para agrupar varios eventos por solicitud de entrega, lo que reduce la sobrecarga HTTP y mejora el rendimiento.

Event Grid proporciona al menos una entrega una vez, lo que significa que los suscriptores pueden recibir el mismo evento más de una vez. Esta garantía es importante para las canalizaciones de IA porque significa que los puntos de conexión del controlador deben ser [idempotentes](https://learn.microsoft.com/es-es/azure/architecture/building-blocks/idempotency). Use el campo de evento `id` para detectar y desduplicar entregas repetidas. Por ejemplo, si el servicio de inferencia recibe el mismo evento dos veces, debe comprobar si ya procesó un resultado para ese identificador de evento antes de iniciar una nueva ejecución de inferencia.

## Examen de la programación de reintento y el control de errores

Cuando Event Grid recibe una respuesta de error, evalúa el tipo de error para decidir si se reintenta. Los errores relacionados con la configuración que no se pueden corregir con reintentos se controlan de forma diferente a los errores transitorios.

Los errores siguientes no se reintentan porque indican problemas permanentes:

- **400 Solicitud incorrecta:** La carga del evento tiene un formato incorrecto o el punto de conexión no puede procesarla.
- **413 Entidad de solicitud demasiado grande:** El evento supera el límite de tamaño del punto de conexión.
- **403 Prohibido:** El punto de conexión rechaza explícitamente la entrega.

En el caso de los puntos de conexión de webhook, tampoco se reintenta una respuesta 401 no autorizada. En el caso de los puntos de conexión de recursos de Azure, las respuestas 401 y 404 desencadenan un reintento después de cinco minutos o más, ya que estos errores pueden resolverse a medida que el recurso finaliza el aprovisionamiento.

Para todos los demás errores, Event Grid aplica una programación de reintentos de retroceso exponencial:

1. 10 segundos
2. 30 segundos
3. Un momento
4. Cinco minutos
5. 10 minutos
6. 30 minutos
7. Una hora
8. Tres horas
9. Seis horas
10. Cada 12 horas hasta 24 horas

Event Grid agrega aleatorización a los intervalos de reintentos para distribuir la carga y podría omitir reintentos si un punto de conexión aparece constantemente como incorrecto. Si el punto de conexión responde en tres minutos, Event Grid intenta eliminar el evento de la cola de reintentos en el mejor momento posible, pero aún se podrían recibir duplicados.

## Personalizar configuraciones de la política de reintento

Puede ajustar dos parámetros al crear una suscripción de eventos para controlar el comportamiento de reintento. Event Grid usa el límite que se alcance primero para detener el reintento y quitar o procesar el evento como correo devuelto.

- **Número máximo de intentos:** Entero entre uno y 30 (valor predeterminado: 30). Event Grid deja de reintentarlo después de este número de intentos de entrega.
- **Período de vida del evento (TTL):** Entero entre uno y 1440 minutos (valor predeterminado: 1440 minutos o 24 horas). Event Grid deja de intentarlo una vez transcurrido este tiempo desde la hora de publicación original del evento.

La configuración correcta depende de la tolerancia a la latencia de la carga de trabajo de IA. En el caso de las operaciones que distinguen el tiempo, como la clasificación de contenido en tiempo real, establezca un TTL más corto para que los eventos obsoletos no consuman recursos de controlador cuando se haya pasado la ventana para un procesamiento útil. En el caso de las canalizaciones de procesamiento por lotes que pueden tolerar retrasos, use valores de TTL más largos con más intentos de reintento para maximizar la posibilidad de una entrega correcta.

En el ejemplo siguiente se crea una suscripción de eventos con un TTL de 30 minutos y un máximo de cinco intentos de entrega:

Azure CLI

```
az eventgrid event-subscription create \
    --name moderation-sub \
    --source-resource-id /subscriptions/{sub-id}/resourceGroups/{rg}/providers/Microsoft.EventGrid/topics/ai-events \
    --endpoint https://moderation-service.azurewebsites.net/api/events \
    --max-delivery-attempts 5 \
    --event-ttl 30
```

Tenga en cuenta que la programación de retroceso exponencial interactúa con la configuración de TTL. Con la programación de reintento predeterminada, solo se completan aproximadamente seis intentos de entrega en los primeros 30 minutos. Establecer el número máximo de intentos de entrega en 10 con un TTL de 30 minutos no tiene ningún efecto adicional porque el TTL expira primero.

## Configuración de destinos de mensajes fallidos para eventos que no se pueden entregar

Si Event Grid agota todos los intentos de reintento o el TTL del evento expira, puede enviar el evento no entregado a un [destino de mensajes muertos](https://learn.microsoft.com/es-es/azure/event-grid/manage-event-delivery). La opción de procesar como correo devuelto está deshabilitada de forma predeterminada. Para habilitarla, especifique un contenedor de Azure Blob Storage como punto de conexión de mensajes fallidos al crear la suscripción de eventos. Debe crear la cuenta de almacenamiento y el contenedor antes de configurar la opción de procesar como correo devuelto.

Azure CLI

```
az eventgrid event-subscription create \
    --name moderation-sub \
    --source-resource-id /subscriptions/{sub-id}/resourceGroups/{rg}/providers/Microsoft.EventGrid/topics/ai-events \
    --endpoint https://moderation-service.azurewebsites.net/api/events \
    --max-delivery-attempts 5 \
    --event-ttl 30 \
    --deadletter-endpoint /subscriptions/{sub-id}/resourceGroups/{rg}/providers/Microsoft.Storage/storageAccounts/{storage-account}/blobServices/default/containers/dead-letters
```

Cada evento con mensajes fallidos incluye propiedades de diagnóstico que le ayudarán a comprender por qué se produjo un error en la entrega. Estas propiedades aparecen junto con los datos de eventos originales en el blob de mensajes fallidos:

- **`deadLetterReason`:** el motivo por el que el evento se marcó como fallido (por ejemplo, `MaxDeliveryAttemptsExceeded` o `MaxRetryDurationExceeded`)
- **`deliveryAttempts`:** el número de intentos de entrega antes de que el evento se haya procesado como correo devuelto.
- **`lastDeliveryOutcome`:** el resultado del último intento de entrega (por ejemplo, `NotFound`, `TimedOut`, `Busy`o `Forbidden`)
- **`publishTime`:** hora UTC en la que Event Grid aceptó el evento.
- **`lastDeliveryAttemptTime`:** hora UTC del último intento de entrega.

Para canalizaciones de IA, los eventos de mensajes fallidos suelen indicar problemas sistémicos que necesitan investigación. Un lote de eventos con mensajes fallidos con `lastDeliveryOutcome` de `NotFound` puede significar que la dirección URL del punto de conexión del controlador ha cambiado. Un clúster de `TimedOut` resultados puede indicar que el servicio de inferencia está sobrecargado y necesita ajustes de escalado.

También puede configurar una suscripción de eventos en el propio contenedor de Blob Storage de mensajes fallidos. Este enfoque notifica a un servicio de supervisión cada vez que llega un nuevo evento procesado como correo devuelto, lo que permite alertas automatizadas o flujos de trabajo de reprocesamiento.

## Control de fallos transitorios en canalizaciones de IA

Los puntos de conexión del controlador de IA experimentan varias categorías de errores transitorios que controla automáticamente el mecanismo de reintento de Event Grid. Los reinicios del servicio de modelo provocan breves períodos de falta de disponibilidad. Las funciones sin servidor en los planes de consumo experimentan [latencia de arranque en frío](https://learn.microsoft.com/es-es/azure/azure-functions/event-driven-scaling#cold-start) que puede superar el tiempo de espera de respuesta de 30 segundos de Event Grid. La presión de memoria de GPU durante las cargas de inferencia máximas puede provocar errores de solicitud temporales. Las interrupciones de dependencias descendentes, como una base de datos vectorial que se encuentra temporalmente no disponible, hacen que el manejador devuelva códigos de error.

El backoff exponencial y el comportamiento de reintento de Event Grid abordan estos errores transitorios sin que sea necesario implementar lógica de reintento personalizada. Sin embargo, debe diseñar los puntos de conexión del controlador para admitir este patrón:

- **Devuelve los códigos de estado adecuados:** Devuelve el 200-204 para su procesamiento correcto. Devuelve 503 si el servicio está sobrecargado temporalmente. No devuelva 400 para problemas transitorios porque Event Grid no reintentará 400 respuestas.
- **Implemente el procesamiento idempotent:** realice un seguimiento de los identificadores de eventos que ya ha procesado. La garantía de "al menos una vez" de Event Grid implica que el controlador podría recibir el mismo evento más de una vez.
- **Procesar rápidamente o confirmar lo antes posible:** Si la operación de inferencia tarda más de 30 segundos, devuelva 202 (aceptado) inmediatamente y procese el evento de forma asincrónica. Event Grid interpreta una respuesta 202 como entrega correcta.

## Habilitación del procesamiento por lotes de salida para cargas de trabajo de inteligencia artificial de alto rendimiento

En el caso de los sistemas de inteligencia artificial que generan o consumen eventos en gran volumen, como el procesamiento de miles de cargas de documentos o clasificaciones de imágenes, el procesamiento por lotes de salida reduce el número de solicitudes HTTP al controlador. Configure el procesamiento por lotes en la suscripción de eventos con dos parámetros:

- **Eventos máximos por lote:** Entero entre uno y 5.000. Event Grid no superará este número, pero podría entregar menos eventos si están disponibles menos.
- **Tamaño de lote preferido en kilobytes:** Entero entre uno y 1024. Event Grid tiene como objetivo este tamaño de lote, pero un único evento mayor que el tamaño preferido sigue entregándose en su propio lote.

Azure CLI

```
az eventgrid event-subscription create \
    --name batch-processor-sub \
    --source-resource-id /subscriptions/{sub-id}/resourceGroups/{rg}/providers/Microsoft.EventGrid/topics/ai-events \
    --endpoint https://batch-processor.azurewebsites.net/api/events \
    --max-events-per-batch 100 \
    --preferred-batch-size-in-kilobytes 512
```

El procesamiento por lotes utiliza la semántica de entrega de todo o nada. El controlador debe devolver un código de éxito para toda la tarea. Si se produce un error en cualquier evento del lote, se reintenta todo el lote. Diseñe el controlador para procesar todos los eventos de un lote o rechace todo el lote devolviendo un código de error adecuado. No establezca el tamaño del lote más grande de lo que su controlador puede procesar de forma confiable dentro del tiempo límite de respuesta de 30 segundos.

## Supervisión de los resultados de entrega

Event Grid publica métricas de entrega a través de [Azure Monitor](https://learn.microsoft.com/es-es/azure/event-grid/monitor-event-delivery) que proporcionan visibilidad sobre cómo fluyen los eventos a través de la canalización de IA. Entre las métricas clave se incluyen las siguientes:

- **Recuento de éxitos de entrega:** Eventos entregados correctamente a los puntos de conexión del controlador
- **Recuento de errores de entrega:** Eventos que no se pudieron entregar (errores individuales de intentos, no errores finales)
- **Eventos coincidentes:** Eventos que coinciden con al menos un filtro de suscripción
- **Eventos descartados:** eventos que coincidieron con una suscripción pero superaron los límites de reintento sin mensajes fallidos
- **Eventos con mensajes fallidos:** eventos enviados al destino de mensajes fallidos después de agotar los reintentos

Puede establecer alertas en estas métricas para detectar problemas sistémicos en la canalización. Un aumento repentino de los eventos fallidos podría indicar que un servicio de modelo está inactivo, una dirección URL del punto de conexión del controlador ha cambiado o que una implementación introdujo un error. Una eliminación de eventos coincidentes puede significar que el origen del evento dejó de publicarse o que una configuración de filtro cambió inesperadamente. La supervisión de estas métricas junto con los registros de la aplicación proporciona una imagen completa del estado del flujo de eventos en toda la solución de inteligencia artificial.