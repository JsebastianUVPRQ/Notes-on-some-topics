## Objetivos

En este módulo aprenderá a:

- Cree entornos en GitHub.
- Use entornos en Acciones de GitHub.
- Agregue aprobaciones para asignar revisores necesarios antes de mover el modelo al siguiente entorno
---
# Objetivos - Descripción del problema empresarial

Imagine que es un ingeniero de aprendizaje automático en Proseware, una joven start-up que trabaja en una nueva aplicación de atención sanitaria. El modelo de clasificación de diabetes, creado por los científicos de datos, es el primer modelo que se va a integrar en la aplicación. Después de hablar con el equipo más grande, resulta que el objetivo es tener varios modelos integrados en la aplicación web.

Cuando el modelo de clasificación de diabetes resulte correcto, Proseware querrá agregar más modelos de aprendizaje automático, de modo que los médicos puedan diagnosticar más rápidamente a los pacientes para diversas enfermedades. Para cada modelo nuevo, el equipo de ciencia de datos deberá poder experimentar en un entorno seguro. Una vez que el nuevo modelo sea lo suficientemente preciso como para integrarse en la aplicación web, se deberá probar antes de implementarlo en un punto de conexión al que se llamará desde la aplicación web.

Junto con el equipo, decide que es mejor usar distintos entornos:

- **Desarrollo**, para la experimentación.
- **Ensayo**, para pruebas.
- **Producción**, para implementar el modelo en el punto de conexión de producción.

Para cada entorno, creará un área de trabajo de Azure Machine Learning independiente. Al mantener las áreas de trabajo independientes para cada entorno, podrá proteger los datos y los recursos. Por ejemplo, el área de trabajo de desarrollo no contendrá ningún dato personal de los pacientes. Y los científicos de datos solo tendrán acceso al área de trabajo de desarrollo, ya que solo necesitan un entorno para la experimentación y no necesitan acceso a ninguno de los recursos ni al código de producción.

Como ingeniero de aprendizaje automático, debe asegurarse de que los datos que compilen los científicos de datos se moverán fácilmente entre entornos. Una vez que un modelo nuevo esté listo para su implementación, quiere que el modelo se entrene y se pruebe en el entorno de ensayo. Después de probar el código, el modelo y la implementación, quiere implementar el modelo en el entorno de producción. Las partes de este proceso se pueden automatizar para acelerar el proceso.

Para trabajar con entornos, querrá:

- Crear **entornos** en el repositorio de GitHub.
- Almacenar las credenciales en cada área de trabajo de Azure Machine Learning como **secreto** de entorno en GitHub.
- Agregar **revisores necesarios** a entornos para la **aprobación controlada**.
- Usar entornos en los flujos de trabajo de Acciones de GitHub.