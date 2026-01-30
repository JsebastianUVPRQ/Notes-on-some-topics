
Acciones de GitHub es una plataforma que permite automatizar las tareas desencadenadas por eventos que se producen en un repositorio de GitHub. Un flujo de trabajo de GitHub Actions consta de **tareas**. Un trabajo agrupa un **conjunto de pasos** que puede definir. Uno de estos pasos puede usar la CLI (v2) para ejecutar un **trabajo de Azure Machine Learning** para entrenar un modelo.

Para automatizar el entrenamiento de modelos con Acciones de GitHub, deberá hacer lo siguiente:

- Crear una entidad de servicio con la CLI de Azure.
- Almacenar las credenciales de Azure en un secreto de GitHub.
- Definir una Acción de GitHub en YAML.

## Creación de una entidad de servicio

Cuando emplee Acciones de GitHub para automatizar trabajos de Azure Machine Learning, deberá usar una entidad de servicio a fin de autenticar GitHub para administrar el área de trabajo de Azure Machine Learning. Por ejemplo, para entrenar un modelo mediante el proceso de Azure Machine Learning, usted o la herramienta que emplee deberán estar autorizados para usar ese proceso.

Sugerencia

Más información sobre cómo [usar Acciones de GitHub para conectarse a Azure](https://learn.microsoft.com/es-es/azure/developer/github/connect-from-azure)

## Almacenamiento de las credenciales de Azure

Las credenciales de Azure que necesita para autenticarse no deben estar almacenadas en el código ni en texto sin formato, sino que deben almacenarse en un secreto de GitHub.

Para agregar un secreto al repositorio de GitHub:

1. Vaya a la pestaña **Configuración** .
    
    ![Captura de pantalla de la pestaña de configuración en el repositorio de GitHub.](https://learn.microsoft.com/es-es/training/wwl-data-ai/trigger-azure-machine-learn-jobs-github-actions/media/04-01-settings.png)
    
2. En la pestaña **Configuración** , en **Seguridad**, expanda la opción **Secretos** y seleccione **Acciones**.
    
    ![Captura de pantalla de la opción secretos en la sección seguridad.](https://learn.microsoft.com/es-es/training/wwl-data-ai/trigger-azure-machine-learn-jobs-github-actions/media/04-02-secrets.png)
    
3. Escriba las credenciales de Azure como un secreto y asigne al secreto el nombre `AZURE_CREDENTIALS`.
    
4. Para usar un secreto que contenga credenciales de Azure en una Acción de GitHub, consulte el secreto en el archivo YAML.
    
    ```yml
    on: [push]
    
    name: Azure Login Sample
    
    jobs:
      build-and-deploy:
        runs-on: ubuntu-latest
        steps:
          - name: Log in with Azure
            uses: azure/login@v1
            with:
              creds: '${{secrets.AZURE_CREDENTIALS}}'
    ```
    

## Definición de la Acción de GitHub

Para definir un flujo de trabajo, deberá crear un archivo YAML. Puede desencadenar el flujo de trabajo para entrenar un modelo manualmente o con un evento de inserción. El desencadenamiento manual del flujo de trabajo es ideal para las pruebas, mientras que la automatización con un evento es mejor para la automatización.

Para configurar un flujo de trabajo de Acciones de GitHub de modo que pueda desencadenarlo manualmente, use `on: workflow_dispatch`. Para desencadenar un flujo de trabajo con un evento de inserción, use `on: [push]`.

Una vez que se ha desencadenado el flujo de trabajo de Acciones de GitHub, puede agregar varios pasos a un trabajo. Por ejemplo, puede usar un paso para ejecutar un trabajo de Azure Machine Learning:



```yml
name: Manually trigger an Azure Machine Learning job

on:
  workflow_dispatch:

jobs:
  train-model:
    runs-on: ubuntu-latest
    steps:
    - name: Trigger Azure Machine Learning job
      run: |
        az ml job create --file src/job.yml
```

Sugerencia

Obtenga más información sobre [Acciones de GitHub, incluidos los conceptos básicos y la terminología esencial.](https://docs.github.com/actions/learn-github-actions/understanding-github-actions)