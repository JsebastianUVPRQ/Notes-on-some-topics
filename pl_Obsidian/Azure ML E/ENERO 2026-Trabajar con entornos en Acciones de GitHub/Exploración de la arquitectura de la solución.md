
Al trabajar en proyectos más pequeños con equipos más pequeños, puede tener sentido tener un área de trabajo de Azure Machine Learning. El área de trabajo se puede usar para todo: para entrenar, probar e implementar el modelo. Pero, en Proseware, quiere tener una solución sólida y de prueba de futuro que pueda escalar con facilidad al compilar y mantener varios modelos que desea integrar con nuestra aplicación web para profesionales.

Para trasladar un modelo rápidamente pero de forma segura desde el desarrollo hasta la producción, has acordado una arquitectura de operaciones de **aprendizaje automático** (**MLOps**) de alto nivel.

![Diagrama de la arquitectura de operaciones de aprendizaje automático.](https://learn.microsoft.com/es-es/training/wwl-data-ai/work-environments-github-actions/media/01-01-architecture.png)

 Nota:

El diagrama es una representación simplificada de una arquitectura de MLOps. Para ver una arquitectura más detallada, explore los distintos casos de uso en el acelerador de soluciones [de MLOps (v2).](https://github.com/Azure/mlops-v2)

La arquitectura incluye:

1. **Configuración**: cree todos los recursos necesarios de Azure para la solución.
2. **Desarrollo de modelos (bucle interno):** explore y procese los datos para entrenar y evaluar el modelo.
3. **Integración continua**: empaquetar y registrar el modelo.
4. **Implementación de modelos (bucle externo):** implemente el modelo.
5. **Implementación continua**: pruebe el modelo y promueva al entorno de producción.
6. **Supervisión**: supervise el rendimiento del modelo y del punto de conexión.

Para trabajar con modelos de Machine Learning a gran escala, Proseware quiere usar entornos independientes para diferentes fases. Tener entornos independientes facilitará el control del acceso a los recursos. A continuación, cada entorno se puede asociar a un área de trabajo de Azure Machine Learning independiente.

 Nota:

En este módulo, se hace referencia a la interpretación de entornos de DevOps. Tenga en cuenta que Azure Machine Learning también usa el término "entornos" para describir una colección de paquetes de Python necesarios para ejecutar un script. Estos dos conceptos de entornos son independientes entre sí. Obtenga más información sobre [los entornos de Azure Machine Learning](https://learn.microsoft.com/es-es/azure/machine-learning/concept-environments).

Para permitir que los modelos se prueben antes de implementarse, quiere trabajar con tres entornos:

![Diagrama del entorno de desarrollo, ensayo y producción.](https://learn.microsoft.com/es-es/training/wwl-data-ai/work-environments-github-actions/media/03-02-environments.png)

El entorno de **desarrollo** se usa para el bucle interno:

1. Los científicos de datos entrenan el modelo.
2. El modelo se empaqueta y registra.

El entorno **de ensayo** se usa para parte del bucle externo:

3. Pruebe el código y el modelo con linting y pruebas unitarias.
4. Implemente el modelo para probar el punto de conexión.

El entorno de **producción** se usa para otra parte del bucle externo:

5. Implemente el modelo en el punto de conexión de producción. El punto de conexión de producción se integra con la aplicación web.
6. Supervise el rendimiento del modelo y del punto de conexión para desencadenar el reentrenamiento cuando sea necesario.

Aunque muchas tareas de aprendizaje automático pueden y deben automatizarse, también querrá planear puntos en los que desee la aprobación controlada. Cuando se ha entrenado y empaquetado un modelo, quiere notificar al científico de datos principal para que valide el modelo antes de pasar al entorno de ensayo.

De forma similar, después de probar el modelo con vigor en el entorno de ensayo, quiere agregar la aprobación cerrada para asegurarse de que alguien del equipo de desarrollo de software comprueba que todas las pruebas se han realizado correctamente antes de implementar el modelo en producción.

Al trabajar con entornos, la aprobación cerrada le permite controlar las implementaciones de un entorno a otro.