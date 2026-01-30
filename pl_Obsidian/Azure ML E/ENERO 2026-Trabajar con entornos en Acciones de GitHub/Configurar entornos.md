Para implementar entornos al trabajar con modelos de Machine Learning, puede usar una plataforma como GitHub. Para automatizar las tareas que necesitan ejecutarse en entornos independientes, deberá hacer lo siguiente:

- Configurar los entornos en GitHub.
- Usar los entornos de Acciones de GitHub.
- Agregar aprobaciones para asignar los revisores necesarios.

## Configuración de los entornos en GitHub

Para crear un entorno en el repositorio de GitHub:

1. Vaya a la pestaña **Configuración** del repositorio.
2. Seleccione **Entornos**.
3. Cree un **entorno nuevo**.
4. Escriba un nombre.
5. Seleccione **Configure environment** (Configurar el entorno).

Para asociar un entorno a un área de trabajo de Azure Machine Learning específica, puede crear un **secreto de entorno** para proporcionar acceso al entorno únicamente a un área de trabajo de Azure Machine Learning.

 Nota:

Para conceder a GitHub acceso a cualquier área de trabajo de Azure Machine Learning, debe crear una entidad de servicio en Azure. Después, debe proporcionar acceso al área de trabajo de Azure Machine Learning en Azure a la entidad de servicio. Aprenda la [Integración de Azure Machine Learning con herramientas de DevOps como GitHub](https://learn.microsoft.com/es-es/training/modules/introduction-development-operations-principles-for-machine-learn/4-integrate-azure-development-operations-tools).

Puede crear un secreto en el repositorio para almacenar las credenciales de la entidad de servicio. Al trabajar con entornos, querrá crear un secreto de entorno en su lugar para definir qué entorno específico de GitHub debe tener acceso al área de trabajo de Azure Machine Learning.

Para crear un secreto de entorno, vaya a la pestaña **Entornos** de la pestaña **Configuración**.

1. Vaya al nuevo entorno.
2. Vaya a la sección **Environment secrets** (Secretos de entorno).

![Captura de pantalla de la configuración de un entorno en GitHub.](https://learn.microsoft.com/es-es/training/wwl-data-ai/work-environments-github-actions/media/04-01-settings.png)

3. Agregue un nuevo secreto.
4. Escriba `AZURE_CREDENTIALS` para el nombre.
5. Escriba las credenciales de la entidad de servicio en el campo de valor.

## Uso de entornos en Acciones de GitHub y adición de aprobaciones

Después de crear entornos en el repositorio de GitHub, puede hacer referencia al entorno desde los flujos de trabajo de Acciones de GitHub. Siempre que quiera agregar una comprobación manual entre entornos, puede agregar **aprobaciones**.

Por ejemplo, siempre que desencadene un trabajo de Azure Machine Learning en el flujo de trabajo de Acciones de GitHub, la tarea se puede ejecutar correctamente en el flujo de trabajo. Pero, puede ser que durante el entrenamiento del modelo en el área de trabajo de Azure Machine Learning, se produzca un error debido a un problema con el script de entrenamiento. O después del entrenamiento del modelo, al evaluar las métricas del modelo, puede decidir que necesita volver a entrenar el modelo en lugar de implementarlo.

Para darle la oportunidad de revisar el resultado del entrenamiento del modelo en el área de trabajo de Azure Machine Learning, puede agregar una aprobación para un entorno. Siempre que un flujo de trabajo de Acciones de GitHub quiera ejecutar una tarea en un entorno específico, se notificará a los revisores necesarios y deberá aprobar las tareas antes de que se ejecuten.

 Sugerencia

Obtenga más información sobre [cómo usar entornos en Acciones de GitHub y cómo agregar aprobaciones](https://learn.microsoft.com/es-es/training/modules/continuous-deployment-for-machine-learning/).

---
---
# Siga estas instrucciones para completar el desafío:

- Vea el [repositorio de desafíos en GitHub](https://microsoftlearning.github.io/mslearn-mlops/).
- Complete el desafío 5: trabajar con entornos.