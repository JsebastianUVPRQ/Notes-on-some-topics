Mientras que el linting comprueba cómo escribió el código, las pruebas unitarias comprueban cómo funciona. Las unidades hacen referencia al código que crea. Por lo tanto, las pruebas unitarias también se conocen como pruebas de código.

Como procedimiento recomendado, el código debe existir principalmente fuera de las funciones. No importa si ha creado funciones para preparar los datos o para entrenar un modelo. Puede aplicar pruebas unitarias para, por ejemplo:

- Comprobar que los nombres de columna son correctos.
- Comprobar el nivel de predicción del modelo en nuevos conjuntos de datos.
- Compruebe la distribución de los niveles de predicción.

Al trabajar con Python, puede usar **Pytest** y **Numpy** (que usa el marco Pytest) para probar el código. Para más información sobre cómo trabajar con Pytest, [aprenda a escribir pruebas con Pytest](https://learn.microsoft.com/es-es/training/modules/test-python-with-pytest/).

 Sugerencia

Revise un tutorial más detallado de [las pruebas de Python en Visual Studio Code](https://code.visualstudio.com/docs/python/testing).

Imagine que ha creado un script de entrenamiento `train.py`, que contiene la siguiente función:


```Python
# Train the model, return the model
def train_model(data, ridge_args):
    reg_model = Ridge(**ridge_args)
    reg_model.fit(data["train"]["X"], data["train"]["y"])
    return reg_model
```

Supongamos que ha almacenado el script de entrenamiento en el directorio `src/model/train.py` del repositorio. Para probar la función `train_model`, debe importar la función desde `src.model.train`.

El archivo `test_train.py` se crea en la carpeta `tests`. Una manera de probar el código de Python es usar `numpy`. Numpy ofrece varias funciones `assert` para comparar matrices, cadenas, objetos o elementos.

 Sugerencia

Obtenga más información sobre [las directrices de pruebas al usar las pruebas de Numpy](https://numpy.org/doc/stable/reference/testing.html) y [la compatibilidad con pruebas de Numpy](https://numpy.org/doc/stable/reference/routines.testing.html).

Por ejemplo, para probar la `train_model` función, puede usar un pequeño conjunto de datos de entrenamiento y usar `assert` para comprobar si las predicciones son _casi iguales_ a las métricas de rendimiento predefinidas.

```Python
import numpy as np
from src.model.train import train_model

def test_train_model():
    X_train = np.array([1, 2, 3, 4, 5, 6]).reshape(-1, 1)
    y_train = np.array([10, 9, 8, 8, 6, 5])
    data = {"train": {"X": X_train, "y": y_train}}

    reg_model = train_model(data, {"alpha": 1.2})

    preds = reg_model.predict([[1], [2]])
    np.testing.assert_almost_equal(preds, [9.93939393939394, 9.03030303030303])
```

Para probar el código en Visual Studio Code mediante la interfaz de usuario:

1. Instale todas las bibliotecas necesarias para ejecutar el script de entrenamiento.
2. Asegúrese de que `pytest` está instalado y habilitado en Visual Studio Code.
3. Instale la extensión de **Python** para Visual Studio Code.
4. Seleccione el script `train.py` que quiere probar.
5. Seleccione la pestaña **Pruebas** en el menú de la izquierda.
6. Configure las pruebas de Python seleccionando **pytest** y estableciendo el directorio de pruebas en la `tests/` carpeta.
7. Para ejecutar todas las pruebas, seleccione el botón Reproducir y revise los resultados.

![Captura de pantalla de resultados de pruebas unitarias correctas en Visual Studio Code.](https://learn.microsoft.com/es-es/training/wwl-azure/source-control-for-machine-learning-projects/media/04-05-test-results.png)

Para ejecutar la prueba en una canalización de Azure DevOps o Acción de GitHub:

1. Asegúrese de que todas las bibliotecas necesarias están instaladas para ejecutar el script de entrenamiento. Idealmente, use un `requirements.txt` con una lista de todas las bibliotecas con `pip install -r requirements.txt`
2. Instalación de `pytest` con `pip install pytest`
3. Ejecute las pruebas con `pytest tests/`

Los resultados de las pruebas se mostrarán en la salida de la canalización o flujo de trabajo que ejecute.

## Nota
Si durante el linting o las pruebas unitarias se devuelve un error, es posible que falle la canalización de CI. Por lo tanto, es mejor comprobar el código localmente en primer lugar antes de desencadenar la canalización de CI.