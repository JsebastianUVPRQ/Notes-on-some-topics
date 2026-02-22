La `azure_ai` extensión incluye un pequeño conjunto de operadores semánticos que permiten trabajar con modelos de IA generativos directamente en SQL. Estos operadores le ayudan a generar texto, evaluar instrucciones, extraer información estructurada y clasificar documentos. Cada operador llama a un modelo que configuró en la `azure_ai.settings` tabla.

Los operadores semánticos son:

- *`azure_ai.generate`* genera texto y puede devolver JSON estructurado cuando se proporciona un esquema.
- ```azure_ai.is_true``` : evalúa una declaración y devuelve si es probable que sea verdadero.
- `azure_ai.extract` : extrae campos o valores específicos del texto no estructurado.
- `azure_ai.rank` : devuelve una lista clasificada por relevancia de los documentos de una consulta determinada.

## El operador `generate`

`azure_ai.generate` envía un mensaje a un modelo y devuelve el texto generado. Si proporciona un esquema JSON, el modelo intenta devolver datos estructurados que se ajustan a ese esquema. Este método es útil cuando se necesita una salida que es consumida por la lógica SQL posterior.

Ejemplo:

```SQL
SELECT azure_ai.generate(
  prompt => 'Summarize the following review: ' || review_text
)
FROM product_reviews;
```

Si se proporciona un esquema, el resultado se devuelve como `jsonb`.

## El operador `is_true`

`azure_ai.is_true` evalúa una instrucción y devuelve `true`, `false`o `NULL` si el modelo no puede determinar la respuesta. Este operador es útil cuando necesita comprobar si un fragmento de texto satisface una condición o hace referencia a un concepto específico.

Ejemplo:
```SQL
SELECT azure_ai.is_true(
  'This review describes the product as durable: ' || review_text
) AS durability_claim
FROM product_reviews;
```

## El operador `extract`

`azure_ai.extract` identifica campos específicos dentro de un documento. Especifique una matriz de etiquetas y el modelo devuelve un `jsonb` objeto que contiene los valores extraídos. Este operador es adecuado para extraer detalles estructurados del texto más largo.

Ejemplo:
```SQL
SELECT azure_ai.extract(
  'The headphones have clear sound but the battery life is short.',
  ARRAY['sound_quality', 'battery_life']
);
```

El resultado es un documento JSON que contiene los campos solicitados.

## El operador `rank`

`azure_ai.rank` devuelve documentos ordenados por relevancia para una consulta. Proporcione el texto de la consulta y una matriz de documentos. El operador devuelve un conjunto de filas que incluye cada documento, su clasificación y una puntuación. Este conjunto de filas es útil cuando desea que el modelo ayude a determinar qué elementos son más relevantes para la búsqueda de un usuario.

Ejemplo:

```SQL
SELECT *
FROM azure_ai.rank(
  'Lightweight travel headphones',
  ARRAY[
    'These foldable headphones are easy to pack.',
    'Battery life is average.',
    'Sound quality is very detailed.'
  ]
);
```

El operador devuelve una fila por documento con información de clasificación.

## Configuración

Todos los operadores semánticos dependen de la configuración del modelo almacenada en `azure_ai.settings`. Antes de llamar a los operadores, asegúrese de establecer el punto de conexión y la clave para el modelo que quiere usar.

Ejemplo:

```SQL
SELECT azure_ai.set_setting('azure_openai.endpoint', '{endpoint}');
SELECT azure_ai.set_setting('azure_openai.api_key', '{api_key}');
```

Una vez que se ha implementado la configuración, los operadores semánticos se pueden usar en consultas, vistas o procedimientos almacenados estándar de SQL.

## Takeaways

Los operadores semánticos de la `azure_ai` extensión proporcionan funcionalidades eficaces para integrar inteligencia artificial generativa directamente en los flujos de trabajo de SQL. Con estos operadores, puede mejorar las aplicaciones con generación de texto, evaluación de verdad, extracción de información y clasificación de documentos, todo ello dentro del contexto familiar de una base de datos postgreSQL.