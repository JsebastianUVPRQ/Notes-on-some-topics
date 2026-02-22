La integridad de datos en Delta Lake es un aspecto crítico que garantiza la precisión, la coherencia y la confiabilidad de los datos a lo largo de su ciclo de vida. Delta Lake proporciona varios mecanismos para mantener la integridad de datos, especialmente en entornos con canalizaciones de datos complejas y varios usuarios simultáneos. Ya hemos tratado las transacciones ACID, el cumplimiento de esquemas, la evolución, el viaje en el tiempo, etc.

## Aplicar restricciones

**Las restricciones clave principal** (PK) y clave **externa** (FK) en Databricks definen la estructura relacional y la unicidad prevista y las relaciones referenciales entre tablas. Una restricción de clave principal indica que una columna (o conjunto de columnas) _debe_ identificar de forma única cada fila de la tabla (y normalmente que ninguna de esas columnas sea nula). Una restricción de clave externa significa que una columna o un conjunto de columnas de una tabla debe coincidir con los valores de una clave principal o candidata en otra tabla, estableciendo la integridad referencial. Sin embargo, es importante tener en cuenta que estas restricciones son **informativas**, **no aplicadas** por el propio motor de Databricks. Sirven para documentar las relaciones deseadas y permiten optimizaciones (especialmente si las marca con la opción RELY), pero no garantizan que los datos realmente los satisfagan a menos que se apliquen de forma ascendente o validada manualmente.

Vamos a explorar un ejemplo en SQL donde creamos una tabla de clientes (PK compuesta) y una tabla de pedidos (PK único + FK compuesto):

SQL

```
-- Dimension: customers (composite primary key)
CREATE TABLE customers (
  customer_id INT    NOT NULL,
  region_id   INT    NOT NULL,
  name        STRING NOT NULL,
  email       STRING,
  CONSTRAINT customers_pk PRIMARY KEY (customer_id, region_id)
);

-- Fact: orders (single-column primary key, plus a composite FK to customers)
CREATE TABLE orders (
  order_id    INT      NOT NULL PRIMARY KEY,
  customer_id INT,
  region_id   INT,
  order_date  DATE     NOT NULL,
  amount      DECIMAL(12,2) NOT NULL,
  CONSTRAINT orders_customer_fk
    FOREIGN KEY (customer_id, region_id) REFERENCES customers
);
```

 Nota:

- Las restricciones de clave principal y clave externa están disponibles en Databricks Runtime 11.3 LTS y versiones posteriores, y están totalmente disponibles en Databricks Runtime 15.2 y versiones posteriores.
- Las restricciones de clave principal y clave externa requieren Unity Catalog y Delta Lake.

Delta también admite **restricciones**, como `NOT NULL`, `CHECK`y columnas generadas. Estas restricciones se validan en tiempo de escritura para asegurarse de que solo los datos válidos entran en la tabla. En el ejemplo siguiente se crea una tabla de empleados con restricciones de clave principal, `NOT NULL`, y `CHECK` para aplicar edades y fechas válidas y, a continuación, se agrega otra `CHECK` restricción que garantiza que `employee_id` los valores permanezcan dentro del intervalo entre 1 y 999,999,999. Se rechazan los registros infractores y se mantiene la coherencia de la tabla con las reglas de negocio.

SQL

```
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    first_name  STRING,
    last_name   STRING NOT NULL,
    age         INT,
    start_date  DATE,
    end_date    DATE,
    CONSTRAINT age_non_negative CHECK (age >= 0),
    CONSTRAINT valid_dates      CHECK (end_date > start_date)
);

ALTER TABLE employees ADD CONSTRAINT validIds CHECK (employee_id >= 1 and employee_id <= 99999999);
```

## Controlar la concurrencia

La simultaneidad es otro desafío de integridad de datos, más que nada cuando varios usuarios o procesos escriben en la misma tabla. Delta lo controla con el control de simultaneidad optimista (OCC). Cada transacción lee la instantánea actual y propone cambios; antes de confirmar, Delta comprueba si otras confirmaciones han modificado los mismos archivos de datos. Si se detecta un conflicto (por ejemplo, dos procesos actualizan la misma fila), una transacción falla con un error de conflicto en lugar de sobrescribir silenciosamente los cambios del otro. Esto garantiza la coherencia sin bloquear toda la tabla.

Veamos un ejemplo. Tenemos una tabla de empleados:

SQL

```
CREATE TABLE employees (
  id INT,
  name STRING,
  age INT
);

INSERT INTO employees VALUES (1, 'Alice', 30), (2, 'Bob', 25);
```

Imagina que la transacción A y la transacción B se inician al mismo tiempo, cada una leyendo la misma instantánea de la tabla (versión 1).

**Transacción A (sesión 1):**

SQL

```
-- Session 1: Try to update Bob
UPDATE employees
SET age = 26
WHERE id = 2;
```

**Transacción B (sesión 2):**

SQL

```
-- Session 2: Try to update Bob differently
UPDATE employees
SET age = 27
WHERE id = 2;
```

La sesión 1 finaliza y se confirma correctamente, lo que genera la versión 2 de la tabla en la que la edad de Bob se actualiza a 26. Cuando la sesión 2 intenta confirmar, Delta compara el estado actual de la tabla con los archivos que planea modificar. Encuentra que esos archivos ya se han cambiado en la versión 2, por lo que la confirmación se bloquea y se produce un error de conflicto en la sesión 2.

## Definir expectativas

Por último, Delta proporciona herramientas de calidad de datos, como las expectativas de las canalizaciones declarativas de Lakeflow, que permiten definir reglas de calidad de datos mediante declaración y realizar un seguimiento de las infracciones.

Permiten declarar condiciones booleanas en los registros a medida que fluyen datos a través de canalizaciones de streaming o ETL (vistas materializadas o tablas de streaming) para validar que los datos cumplen las restricciones especificadas. Por ejemplo, puede exigir que una columna "age" esté entre 0 y 120, o que determinados campos no sean NULL. Las condiciones se expresan en SQL (o a través de decoradores de Python) y se ejecutan por registro. Cuando un registro viola la expectativa, lo que sucede a continuación depende de la configuración de la expectativa ("acción ante violación"): se puede advertir y registrar, eliminar el registro o provocar el fallo de la actualización.

Hay tres partes principales de una expectativa:

- **Nombre de la expectativa** : una etiqueta que identifica la regla (debe ser única por conjunto de datos). Se usa para la supervisión, las métricas y la comprensión de qué regla falló.
    
- **Constraint /Condition** : una condición booleana de SQL que debe cumplir cada registro.
    
- **Acción en caso de infracción** : qué hacer cuando un registro infringe la restricción. Las opciones son:
    
    - _advertir (valor predeterminado):_ conservar registros no válidos, pero registrar métricas.
    - _drop_: elimina los registros no válidos antes de escribirlos en la tabla de destino, registrando cuántos se eliminaron.
    - _fail_: anule la actualización o el flujo si algún registro infringe la expectativa.