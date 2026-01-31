
Puedes ejecutar muchos tipos diferentes de aplicaciones en Spark, incluido el código en scripts de Python o Scala, el código de Java compilado como un archivo Java (JAR) y otros. Spark se usa normalmente en dos tipos de cargas de trabajo:

- Trabajos de procesamiento por lotes o flujos para ingerir, limpiar y transformar datos, que a menudo se ejecutan como parte de una canalización automatizada.
- Sesiones de análisis interactivas para explorar, analizar y visualizar datos.

## Conceptos básicos de edición y código de cuadernos

Los cuadernos de Databricks son el área de trabajo principal para la ciencia de datos, la ingeniería y el análisis. Se compilan alrededor de celdas, que pueden contener código o texto con formato (Markdown). Este enfoque basado en celdas facilita la experimentación, la prueba y la explicación del trabajo en un solo lugar. Puede ejecutar una sola celda, un grupo de celdas o todo el cuaderno, con salidas como tablas, gráficos o texto sin formato que aparecen directamente debajo de la celda ejecutada. Las celdas se pueden reordenar, contraer o borrar para mantener el cuaderno organizado y legible.

![Captura de pantalla de un cuaderno en Azure Databricks.](https://learn.microsoft.com/es-es/training/wwl-data-ai/use-apache-spark-azure-databricks/media/azure-databricks-notebook.png)

Una fuerza importante de los cuadernos de Databricks es la compatibilidad con varios idiomas. Aunque el valor predeterminado suele ser Python, puede cambiar a SQL, Scala o R en el mismo cuaderno mediante comandos mágicos como %sql o %scala. Esta flexibilidad significa que puede escribir lógica de ETL en SQL, código de aprendizaje automático en Python y, a continuación, visualizar los resultados con R, todo en un solo flujo de trabajo. Databricks también brinda resaltado de sintaxis y autocompletar para facilitar la detección de errores y acelerar la codificación.

Antes de ejecutar cualquier código, se debe adjuntar un cuaderno a un clúster. Sin un clúster asociado, no se pueden ejecutar celdas de código. Puede seleccionar un clúster existente en la barra de herramientas del cuaderno o crear uno nuevo, y puede desasociar y volver a adjuntar cuadernos según sea necesario. Esta conexión es lo que permite que el cuaderno aproveche la potencia de procesamiento distribuida en Azure Databricks.

## Uso de Databricks Assistant

**Databricks Assistant** es un complemento de codificación con tecnología de inteligencia artificial integrado directamente en cuadernos. Su objetivo es ayudarle a escribir, comprender y mejorar el código de forma más eficaz aprovechando el contexto del cuaderno y el área de trabajo. Puede generar código nuevo a partir de mensajes de lenguaje natural, explicar lógica compleja, sugerir correcciones para errores, optimizar el rendimiento e incluso refactorizar o dar formato al código para mejorar la legibilidad. Esto hace que sea útil no solo para principiantes aprendiendo Spark o SQL, sino también para los usuarios experimentados que desean acelerar el desarrollo y reducir el trabajo repetitivo.

El asistente tiene **en cuenta el contexto**, lo que significa que puede usar información sobre el cuaderno, el clúster y el entorno de datos para proporcionar sugerencias personalizadas. Por ejemplo, si el área de trabajo tiene habilitado el catálogo de Unity, puede extraer metadatos como nombres de tabla, nombres de columna y esquemas al escribir consultas SQL. Esto le permite preguntar algo parecido a "Seleccionar el importe medio de ventas por región de la tabla de ventas" y obtener código SQL en funcionamiento que se adapte al modelo de datos real. Del mismo modo, en Python, puede pedirle que cree transformaciones de datos o trabajos de Spark sin tener que recuperar todas las firmas de función de la memoria.

Interactúa con el asistente de dos maneras principales:

1. **Mensajes de lenguaje natural**: puede escribir instrucciones en inglés sin formato en la interfaz similar al chat y insertará código en el cuaderno.
    
2. **Comandos de barra**: comandos rápidos como `/explain`, `/fix` o `/optimize` que permiten actuar en el código seleccionado. Por ejemplo, `/explain` desglosa una función compleja en pasos más sencillos, `/fix` puede intentar resolver errores de sintaxis o tiempo de ejecución, y `/optimize` sugiere mejoras de rendimiento, como la repartición o el uso de funciones eficaces de Spark.
    

![Captura de pantalla de AI Assistant en un cuaderno de Azure Databricks.](https://learn.microsoft.com/es-es/training/wwl-data-ai/use-apache-spark-azure-databricks/media/ai-assistant.png)

Una característica eficaz es el modo de edición, donde el asistente puede proponer cambios estructurales más grandes en varias celdas. Por ejemplo, podría refactorizar la lógica repetida en una sola función reutilizable o reestructurar un flujo de trabajo para mejorar la legibilidad. Siempre tiene control: las sugerencias no son destructivas, lo que significa que puede revisarlas y aceptarlas o rechazarlas antes de aplicar cambios en el cuaderno.

## Uso compartido y modularización de código

Para evitar la duplicación y mejorar la capacidad de mantenimiento, Databricks admite la colocación de código reutilizable en archivos (por ejemplo, módulos .py) en el área de trabajo, que los cuadernos pueden importar. Hay mecanismos para organizar cuadernos (es decir, ejecutar cuadernos de otros cuadernos o trabajos con varias tareas), por lo que puede crear flujos de trabajo que usen funciones o módulos compartidos. El uso `%run` es una manera más sencilla de incluir otro cuaderno, aunque con algunas limitaciones.

## Depuración, historial de versiones y corrección de errores

Databricks ofrece un **depurador interactivo** integrado para cuadernos de Python: puede establecer puntos de interrupción, pasar por la ejecución, inspeccionar variables y navegar por la ejecución de código paso a paso. Esto ayuda a aislar los errores de forma más eficaz que la depuración mediante impresión o registro.

![Captura de pantalla anotada de la barra de herramientas del depurador en el cuaderno de Azure Databricks.](https://learn.microsoft.com/es-es/training/wwl-data-ai/use-apache-spark-azure-databricks/media/debugger-toolbar.png)

Los cuadernos también mantienen automáticamente el historial de versiones: puede ver instantáneas anteriores, proporcionar descripciones de versiones, restaurar versiones anteriores o eliminar o borrar el historial. Si usa la integración de Git, puede sincronizar y versionar cuadernos o archivos en el repositorio.

![Captura de pantalla del historial de versiones de restauración en el cuaderno de Azure Databricks.](https://learn.microsoft.com/es-es/training/wwl-data-ai/use-apache-spark-azure-databricks/media/restore-version.png)