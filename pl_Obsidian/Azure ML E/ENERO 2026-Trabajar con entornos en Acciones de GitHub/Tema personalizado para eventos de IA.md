## Creación de un tema personalizado para eventos de IA

Un tema personalizado proporciona un punto de conexión definido por el usuario en el que la aplicación publica eventos. Para que la aplicación de IA pueda publicar eventos, debe crear el tema y configurarlo para aceptar el esquema que usan los eventos. Establezca el esquema de entrada en `cloudeventschemav1_0` al crear el tema para que los eventos sigan el formato estándar de CloudEvents.

Azure CLI

```
az eventgrid topic create \
    --name ai-pipeline-events \
    --resource-group ai-platform-rg \
    --location eastus \
    --input-schema cloudeventschemav1_0
```

Después de crear el tema, necesita credenciales para publicar eventos. Puede recuperar el punto de conexión del tema y la clave de acceso mediante la CLI de Azure:

Azure CLI

```
az eventgrid topic show \
    --name ai-pipeline-events \
    --resource-group ai-platform-rg \
    --query "endpoint" \
    --output tsv

az eventgrid topic key list \
    --name ai-pipeline-events \
    --resource-group ai-platform-rg \
    --query "key1" \
    --output tsv
```

Event Grid admite tres métodos de autenticación: autenticación de clave de acceso (mediante el `aeg-sas-key` encabezado), autenticación de token de SAS e id. de Microsoft Entra. En el caso de las aplicaciones de IA de Producción, la [autenticación de ID de Microsoft Entra](https://learn.microsoft.com/es-es/azure/event-grid/authenticate-with-microsoft-entra-id) es el enfoque recomendado. Elimina la necesidad de administrar y rotar secretos compartidos, admite identidades administradas y ventajas de características como directivas de acceso condicional. Cuando la aplicación se ejecuta en servicios de Azure como Azure Functions, Azure Container Apps o Azure Kubernetes Service, puede asignar una identidad administrada al servicio de hospedaje y concederle el rol **Remitente de datos de Event Grid** en el tema personalizado.

## Creación de eventos para operaciones de IA

Cada evento personalizado describe un cambio de estado significativo en el sistema de IA. Un evento bien construido incluye suficiente contexto para que el suscriptor empiece a procesar sin insertar los resultados de la operación completa. Los suscriptores recuperan los resultados detallados de un almacén de datos gracias a los identificadores presentes en los datos del evento.

En la estructura siguiente se muestra un evento CloudEvents para una finalización de inferencia. El `type` campo clasifica la operación, `source` identifica el servicio de origen y `subject` proporciona una ruta de acceso filtrable. La `data` carga incluye metadatos sobre la operación y una referencia a donde el suscriptor puede encontrar los resultados detallados:

JSON

```
{
    "specversion": "1.0",
    "type": "com.contoso.ai.InferenceCompleted",
    "source": "/services/content-moderation",
    "id": "evt-20250915-143000-001",
    "time": "2025-09-15T14:30:00Z",
    "subject": "/pipelines/moderation/image-classifier",
    "datacontenttype": "application/json",
    "data": {
        "requestId": "req-78901",
        "modelName": "content-classifier-v3",
        "modelVersion": "3.2.1",
        "processingDurationMs": 1250,
        "resultLocation": "https://results.blob.core.windows.net/output/req-78901.json",
        "status": "completed",
        "itemsProcessed": 1,
        "summary": {
            "classification": "safe",
            "confidence": 0.97
        }
    }
}
```

Al diseñar la carga de datos, tenga en cuenta los siguientes principios:

- **Incluya identificadores para la correlación:** el `requestId` o el identificador de ejecución de la canalización permite a los suscriptores realizar un seguimiento del evento hasta la solicitud original en los servicios distribuidos.
- **Resultados de referencia en lugar de insertarlos:** Almacene salidas detalladas (resultados de inferencia, incrustaciones, texto generado) en Blob Storage o una base de datos. Incluya la ubicación en el evento para que los suscriptores puedan recuperarlos cuando sea necesario.
- **Agregar metadatos operativos:** Campos como `processingDurationMs` y `modelVersion` ayudan a supervisar los servicios de seguimiento de las tendencias de rendimiento y el uso del modelo sin consultar los registros de aplicaciones.
- **Proporcione un resumen para tomar decisiones rápidas:** Incluya un breve resumen del resultado para que los suscriptores puedan tomar decisiones de enrutamiento (marca para su revisión, continuar a la siguiente fase) sin descargar la salida completa.

## Publicación de eventos mediante el SDK de Event Grid

El `EventGridPublisherClient` de la biblioteca `azure-eventgrid` maneja la serialización de eventos, la autenticación y los reintentos. Puede autenticarse con una clave de acceso mediante `AzureKeyCredential` o con el identificador de Entra de Microsoft mediante `DefaultAzureCredential`. En el ejemplo siguiente se muestra cómo crear un cliente y publicar un cloudEvent en un tema personalizado:

Python

```
# Code fragment - focus on creating and sending a CloudEvent
from azure.core.credentials import AzureKeyCredential
from azure.core.messaging import CloudEvent
from azure.eventgrid import EventGridPublisherClient

endpoint = os.environ["EVENTGRID_TOPIC_ENDPOINT"]
key = os.environ["EVENTGRID_TOPIC_KEY"]

credential = AzureKeyCredential(key)
client = EventGridPublisherClient(endpoint, credential)

event = CloudEvent(
    type="com.contoso.ai.InferenceCompleted",
    source="/services/content-moderation",
    data={
        "requestId": "req-78901",
        "modelName": "content-classifier-v3",
        "processingDurationMs": 1250,
        "resultLocation": "https://results.blob.core.windows.net/output/req-78901.json",
        "status": "completed"
    },
    subject="/pipelines/moderation/image-classifier"
)

client.send(event)
```

Para las implementaciones de producción, use `DefaultAzureCredential` para autenticarse con una identidad administrada en lugar de claves de acceso:

Python

```
# Code fragment - focus on managed identity authentication
from azure.identity import DefaultAzureCredential
from azure.core.messaging import CloudEvent
from azure.eventgrid import EventGridPublisherClient

endpoint = os.environ["EVENTGRID_TOPIC_ENDPOINT"]

credential = DefaultAzureCredential()
client = EventGridPublisherClient(endpoint, credential)
```

Puede publicar eventos en lotes para mejorar el rendimiento. Al publicar una lista de eventos, el SDK los envía en una única solicitud HTTP. Este enfoque reduce la sobrecarga de red para las aplicaciones de inteligencia artificial que emiten varios eventos durante una ejecución de procesamiento, como publicar eventos de transición de fase para cada paso de una canalización:

Python

```
# Code fragment - focus on batch publishing
events = [
    CloudEvent(
        type="com.contoso.ai.StageCompleted",
        source="/services/embeddings",
        data={"pipelineRunId": "run-42", "stage": "embeddings", "status": "completed"},
        subject="/pipelines/rag/run-42"
    ),
    CloudEvent(
        type="com.contoso.ai.StageCompleted",
        source="/services/indexing",
        data={"pipelineRunId": "run-42", "stage": "indexing", "status": "completed"},
        subject="/pipelines/rag/run-42"
    )
]

client.send(events)
```

Publique eventos en límites naturales de punto de control en su flujo de trabajo de IA. Entre los buenos puntos de publicación se incluyen la finalización de una inferencia, la transición de una etapa de la canalización, la detección de una anomalía o la finalización de la validación de un modelo. No publique eventos para cambios de estado internos que no necesite conocer ningún suscriptor externo.

## Publicación de eventos mediante la API REST

También puede publicar eventos enviando una solicitud HTTP POST directamente al punto de conexión de tema personalizado. Este enfoque es útil al publicar desde lenguajes sin un SDK oficial de Event Grid, desde servicios ligeros que no necesitan la dependencia completa del SDK o desde sistemas que no son de aplicación, como canalizaciones de CI/CD.

Para un tema personalizado configurado con el esquema de entrada de CloudEvents, envíe un solo CloudEvent como un objeto JSON con el encabezado `content-type` establecido en `application/cloudevents+json; charset=utf-8`. Autentíquese mediante el `aeg-sas-key` encabezado :

Bash

```
curl -X POST \
    -H "Content-Type: application/cloudevents+json; charset=utf-8" \
    -H "aeg-sas-key: $EVENTGRID_TOPIC_KEY" \
    -d '{
        "specversion": "1.0",
        "type": "com.contoso.ai.ModelRetrained",
        "source": "/services/training",
        "id": "evt-20250915-160000-001",
        "time": "2025-09-15T16:00:00Z",
        "subject": "/models/sentiment-v2",
        "datacontenttype": "application/json",
        "data": {
            "modelName": "sentiment-v2",
            "modelVersion": "2.1.0",
            "accuracy": 0.94,
            "trainingDurationMinutes": 45,
            "artifactLocation": "https://models.blob.core.windows.net/trained/sentiment-v2.1.0.tar.gz"
        }
    }' \
    "$EVENTGRID_TOPIC_ENDPOINT"
```

La API REST devuelve 200 Ok cuando se acepta el evento para el enrutamiento. Una respuesta no 200 indica un error en la solicitud, como un evento con formato incorrecto, una clave no válida o un error de coincidencia de esquema.

## Aplicación de patrones de diseño de eventos para aplicaciones de IA

Las distintas operaciones de IA llaman a diferentes estructuras de eventos. Los patrones siguientes abarcan escenarios comunes en sistemas con tecnología de inteligencia artificial.

### Eventos de finalización de inferencia

Publique una vez completada cada solicitud de inferencia. Incluya el identificador de correlación de solicitudes, el nombre del modelo, la duración del procesamiento, la ubicación del resultado y un estado de resumen. Los suscriptores posteriores pueden desencadenar flujos de trabajo de notificación, actualizar dashboards o iniciar pasos de procesamiento de seguimiento.

### Eventos de actualización de modelos

Publicar cuando un modelo es reentrenado, validado o promocionado a producción. Incluya la versión del modelo, las métricas de entrenamiento clave y el destino de implementación. Los suscriptores pueden actualizar las memorias caché del modelo en los puntos de conexión de servicio, actualizar las tablas de enrutamiento para dirigir el tráfico al nuevo modelo o desencadenar pruebas de integración en la versión actualizada.

### Eventos de transición de fase de canalización

Publique en el límite de cada etapa en una canalización de varias etapas. Incluya el identificador de ejecución de canalización, el nombre de la etapa, el estado de la etapa y las referencias de entrada y salida. Un servicio de supervisión se suscribe a estos eventos para crear una vista en tiempo real del progreso de la canalización y detectar cuellos de botella. Un servicio de orquestación los usa para desencadenar la siguiente fase cuando se completa la anterior.

Cada uno de estos patrones sigue el mismo principio básico: el evento describe lo que ha ocurrido y proporciona suficiente contexto para que los suscriptores actúen. El productor de eventos no necesita saber quién se suscribe o qué hacen con la información. Este desacoplamiento es lo que hace que las arquitecturas de IA controladas por eventos sean extensibles. Agregar un nuevo consumidor es cuestión de crear una nueva suscripción de eventos, no modificar el productor.