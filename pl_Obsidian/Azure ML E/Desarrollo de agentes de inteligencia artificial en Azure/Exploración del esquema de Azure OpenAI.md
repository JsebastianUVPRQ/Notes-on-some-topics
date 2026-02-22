Al incorporar Azure OpenAI en la base de datos postgreSQL, puede crear aplicaciones con tecnología de inteligencia artificial altamente escalables. Esta integración le permite usar el lenguaje SQL conocido y la flexibilidad de PostgreSQL para crear soluciones inteligentes dentro de la capa de base de datos. Ya sea en el procesamiento de lenguaje natural, los sistemas de recomendación o la generación de contenido, Azure OpenAI potencia tus aplicaciones.

El `azure_openai` esquema instalado por la `azure_ai` extensión le permite conectarse e interactuar con una instancia del servicio Azure OpenAI. Este esquema permite una integración perfecta con el servicio Azure OpenAI, lo que le permite crear eficaces aplicaciones de IA generativas directamente desde la base de datos postgreSQL.

## Creación de incrustaciones

Con el `azure_openai` esquema, puede llamar a la `create_embeddings()` función , que genera incrustaciones de vectores desde dentro de la capa de base de datos. Estas incrustaciones permiten un almacenamiento, una indexación y una consulta eficaces de vectores de alta dimensión. La función puede tomar una entrada de texto o una matriz de valores de texto, en función del número de elementos que desee insertar a la vez.

La función requiere que:

- Especifique el nombre de la implementación de embedding.
- Proporcione el texto de entrada o la matriz de texto.
- Deje que la función devuelva el vector de inserción como `vector` o `vector[]`.

Ejemplo:


```sql
SELECT azure_openai.create_embeddings(
'{your-deployment-name}',
'Sample text to embed'
);
```


Al pasar varios valores de entrada, la función devuelve una matriz de vectores:


```sql
SELECT azure_openai.create_embeddings(
'{your-deployment-name}',
ARRAY['First text', 'Second text']
);
```


La función controla el procesamiento por lotes internamente en función del número de elementos proporcionados.

## Configuración de una conexión a Azure OpenAI

Antes de usar las `azure_openai` funciones, configure la extensión con el punto de conexión y la clave del servicio Azure OpenAI. El siguiente comando representa las consultas que usaría para establecer el punto de conexión y la clave necesarios para conectarse a la instancia de Azure OpenAI:

SQL

```sql
SELECT azure_ai.set_setting('azure_openai.endpoint', '{endpoint}');
SELECT azure_ai.set_setting('azure_openai.subscription_key', '{api-key}');
```

Después, puede usar la `get_setting()` función para comprobar la configuración escrita en la `azure_ai.settings` tabla de configuración:

SQL

```sql
SELECT azure_ai.get_setting('azure_openai.endpoint');
SELECT azure_ai.get_setting('azure_openai.subscription_key');
```

## Habilitar soporte para vectores con la extensión vectorial

La `azure_openai.create_embeddings()` función de la `azure_ai` extensión permite generar incrustaciones para texto de entrada. Para permitir que los vectores generados se almacenen junto con el resto de sus datos en la base de datos, también debe instalar la `vector` extensión siguiendo la guía para [habilitar el soporte de vectores en su base de datos](https://learn.microsoft.com/es-es/azure/postgresql/flexible-server/how-to-use-pgvector#enable-extension) en la documentación de la base de datos.

Puede instalar la `vector` extensión mediante el comando [CREATE EXTENSION](https://www.postgresql.org/docs/current/sql-createextension.html) .

SQL

```sql
CREATE EXTENSION IF NOT EXISTS vector;
```

### Generar y almacenar vectores

En la aplicación de recomendación de propiedades de alquiler con tecnología de IA que está desarrollando para Margie's Travel, debe agregar una nueva columna a la tabla de destino mediante el `vector` tipo de datos para almacenar incrustaciones dentro de esa tabla después de agregar compatibilidad con vectores a la base de datos. Los vectores están habilitados en la `listings` tabla para permitir funcionalidades de búsqueda semántica al ejecutar consultas para buscar propiedades disponibles. El `text-embedding-ada-002` modelo genera vectores con 1536 dimensiones, por lo que debe especificar `1536` como el tamaño del vector.

SQL

```SQL
ALTER TABLE listings
ADD COLUMN description_vector vector(1536);
```

La `listings` tabla ya está lista para almacenar incrustaciones. Con la función `azure_openai.create_embeddings()`, se crean vectores para el campo `description` y se insertan en la columna recién creada `description_vector` de la tabla `listings`.

SQL

```SQL
UPDATE listings
SET description_vector = azure_openai.create_embeddings('{your-deployment-name}', description);
```

Cada inserción es un vector de números de punto flotante, por lo que la distancia entre dos incrustaciones en el espacio vectorial se correlaciona con la similitud semántica entre dos entradas en el formato original.