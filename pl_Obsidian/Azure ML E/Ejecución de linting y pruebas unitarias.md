
Acciones de GitHub se puede usar para automatizar las tareas desencadenadas por eventos. Para desencadenar comprobaciones de calidad del código cuando se crea una solicitud de incorporación de cambios, deberá hacer lo siguiente:

- Comprobar el código con linters y pruebas unitarias.
- Integrar comprobaciones de código con solicitudes de incorporación de cambios.

## Comprobación del código

Hay dos tipos comunes de comprobaciones que deberá realizar en el código: **linters** y **pruebas unitarias**.

Puede usar **linters** para comprobar si el código cumple las directrices de calidad que ha establecido su organización. Por ejemplo, para analizar tu código con Flake8, crearás un archivo de configuración `.flake8` que contenga las reglas que debe cumplir el código.

Para comprobar si el código funciona según lo previsto, puede crear **pruebas unitarias**. Para probar fácilmente partes específicas del código, los scripts deben contener **funciones**. Puede probar funciones en los scripts mediante la creación de archivos de prueba. Una herramienta popular para probar el código de Python es **Pytest**.

 Sugerencia

Obtenga más información sobre [cómo ejecutar pruebas unitarias con Pytest](https://learn.microsoft.com/es-es/training/modules/test-python-with-pytest/).

Para comprobar el código mediante Acciones de GitHub deberá:

- Instalar la herramienta (Flake8 o Pytest).
- Ejecutar las pruebas especificando las carpetas dentro del repositorio que deben comprobarse.

 Sugerencia

Puede comprobar el código automáticamente con Acciones de GitHub, o manualmente en Visual Studio Code. Obtenga más información sobre [cómo comprobar el código localmente](https://learn.microsoft.com/es-es/training/modules/source-control-for-machine-learning-projects/5-verify-your-code-locally).

## Integrar comprobaciones de código con solicitudes de incorporación de cambios.

Para desencadenar un flujo de trabajo de GitHub Actions cuando se crea un pull request, puede usar `on: pull_request`.

Quiere asegurarse de que una solicitud de incorporación de cambios solo se pueda combinar cuando se hayan superado todas las comprobaciones de calidad.

Para integrar las comprobaciones de código con las pull requests destinadas a la rama principal, deberá hacer lo siguiente:

1. Ir a la pestaña **Configuración** del repositorio.
2. Seleccionar **Ramas**.
3. Habilite **Requiera comprobaciones de estado para pasar antes de combinar** dentro de la regla de protección de rama para la rama principal.

![Captura de pantalla de la opción para requerir comprobaciones de estado antes de combinar.](https://learn.microsoft.com/es-es/training/wwl-data-ai/work-linting-unit-test-github-actions/media/05-01-check.png)

Aquí puede buscar y seleccionar los linters y las pruebas unitarias para establecerlos según sea necesario. Cada vez que cree una solicitud de incorporación de cambios, observará que desencadenará Acciones de GitHub, y solo cuando los flujos de trabajo pasen correctamente, podrá combinar la solicitud de incorporación de cambios.

 Nota:

Para configurar las comprobaciones de código que se van a requerir antes de combinar una solicitud de incorporación de cambios, el trabajo debe tener un nombre en el flujo de trabajo de Acciones de GitHub. A continuación, puede encontrar las comprobaciones buscando los nombres de las tareas.