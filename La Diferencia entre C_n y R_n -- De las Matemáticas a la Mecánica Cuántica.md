# La Diferencia entre $C^n$ y $R^n$

## 1. Diferencia Matemática Fundamental

La diferencia radical reside en el **campo escalar** sobre el cual se construye el espacio vectorial:
- $R^n$ es un espacio vectorial sobre el **campo de los números reales** ($\mathbb{R}$).
- $C^n$ es un espacio vectorial sobre el **campo de los números complejos** ($\mathbb{C}$).

Esta distinción algebraica determina completamente su estructura geométrica y operacional.

### 1.1. Estructura Algebraica y Geométrica

#### a) Producto Interno y Norma
- **En $R^n$**: El producto interno estándar (producto punto) es simétrico y siempre real:
  $$ \langle \mathbf{u}, \mathbf{v} \rangle_{\mathbb{R}} = u_1 v_1 + u_2 v_2 + \cdots + u_n v_n \in \mathbb{R} $$
  La norma (longitud) se define como $||\mathbf{u}|| = \sqrt{\langle \mathbf{u}, \mathbf{u} \rangle}$, siempre real y no negativa.

- **En $C^n$**: El producto interno estándar es **hermítico** (sesquilineal), requiriendo conjugación compleja para garantizar una norma real positiva:
  $$ \langle \mathbf{u}, \mathbf{v} \rangle_{\mathbb{C}} = u_1 \bar{v}_1 + u_2 \bar{v}_2 + \cdots + u_n \bar{v}_n \in \mathbb{C} $$
  donde $\bar{v}$ denota el complejo conjugado. La norma es:
  $$ ||\mathbf{u}|| = \sqrt{\langle \mathbf{u}, \mathbf{u} \rangle} = \sqrt{|u_1|^2 + \cdots + |u_n|^2} $$

**Consecuencia crucial**: En $C^n$, el producto interno de dos vectores diferentes puede ser un número complejo, codificando información sobre la **fase relativa** entre ellos, un concepto inexistente en $R^n$.

#### b) Operadores Lineales y Teoría Espectral
- **En $R^n$**: Una matriz simétrica ($A = A^T$) tiene valores propios reales y se diagonaliza en una base ortonormal. Las matrices ortogonales ($A^T A = I$) representan rotaciones/reflexiones.
  
- **En $C^n$**: La matriz análoga a la simétrica es la **hermítica** ($A = A^\dagger$, donde $\dagger$ es traspuesta conjugada). Toda matriz hermítica tiene **valores propios reales**. La análoga a la ortogonal es la **unitaria** ($U^\dagger U = I$).

**Diferencia profunda**: El campo $\mathbb{C}$ es algebraicamente cerrado (todo polinomio tiene raíces en $\mathbb{C}$), mientras que $\mathbb{R}$ no lo es. Esto significa que:
- En $C^n$, **toda** matriz tiene valores propios en $\mathbb{C}$.
- En $R^n$, muchas matrices simples (como rotaciones de 90°) no tienen valores propios reales.

#### c) Dimensión y Conjugación Compleja
- $R^n$ tiene dimensión $n$ sobre $\mathbb{R}$.
- $C^n$ tiene:
  - Dimensión $n$ sobre $\mathbb{C}$
  - Dimensión $2n$ sobre $\mathbb{R}$ (cada componente $a+bi$ requiere dos coordenadas reales)
  
La **conjugación compleja** ($\mathbf{v} \to \bar{\mathbf{v}}$) es una transformación antilineal sin análogo en $R^n$.

---

## 2. Diferencia en el Contexto de la Mecánica Cuántica

La mecánica cuántica **no podría formularse** correctamente sobre $R^n$. Requiere esencialmente la estructura de $C^n$ (o espacios de Hilbert complejos).

### 2.1. El Espacio de Estados es Complejo
El estado de un sistema cuántico es un vector en un espacio de Hilbert complejo. Para un sistema de 2 niveles (qubit):
$$ |\psi\rangle = \alpha|0\rangle + \beta|1\rangle, \quad \alpha, \beta \in \mathbb{C} $$
En $R^2$, los coeficientes serían reales, restringiendo severamente la física posible.

### 2.2. Superposición e Interferencia Cuántica
La naturaleza compleja permite **interferencia**:
- Probabilidad: $P(0) = |\alpha|^2 = \alpha\bar{\alpha}$
- Interferencia: $|\alpha + \beta|^2 \neq |\alpha|^2 + |\beta|^2$

El término de interferencia $2\operatorname{Re}(\alpha\bar{\beta})$ depende de la **fase relativa** $\arg(\alpha) - \arg(\beta)$, información puramente compleja. En $R^n$, la interferencia destructiva total ($\alpha + \beta = 0$ con $\alpha, \beta \neq 0$) es mucho más restringida.

### 2.3. Observables como Operadores Hermíticos
Las cantidades medibles (posición, momento, energía) son operadores hermíticos $A = A^\dagger$. En $C^n$:
1. **Valores propios reales**: Los resultados de medición son siempre números reales.
2. **Autoestados ortogonales**: Según el producto interno hermítico, esencial para el postulado de proyección.

### 2.4. Evolución Temporal Unitaria
La evolución viene dada por el operador unitario:
$$ U(t) = \exp\left(-\frac{i H t}{\hbar}\right) $$
derivado de la ecuación de Schrödinger:
$$ i\hbar \frac{d}{dt}|\psi(t)\rangle = H|\psi(t)\rangle $$

**La unidad proviene de la $i$ en la ecuación**. Un operador unitario ($U^\dagger U = I$) preserva el producto interno hermítico y la norma (probabilidad total = 1). En $R^n$, la evolución vendría dada por operadores ortogonales, una clase demasiado restrictiva.

### 2.5. Relaciones de Conmutación Canónicas
La relación fundamental entre posición ($\hat{x}$) y momento ($\hat{p}$):
$$ [\hat{x}, \hat{p}] = \hat{x}\hat{p} - \hat{p}\hat{x} = i\hbar I $$
**¡Requiere la $i$!** Esta relación no puede satisfacerse por operadores en un espacio real de dimensión finita si exigen ser hermíticos. Es el origen del principio de incertidumbre y demanda absolutamente el campo complejo.

---

## Resumen Comparativo

| Aspecto | $R^n$ (Real) | $C^n$ (Complejo) | Relevancia en Mecánica Cuántica |
|---------|--------------|------------------|--------------------------------|
| **Campo Escalar** | $\mathbb{R}$ | $\mathbb{C}$ | **Fundamental**: coeficientes complejos de superposición |
| **Producto Interno** | Simétrico, bilineal $\langle u,v\rangle \in \mathbb{R}$ | Hermítico, sesquilineal $\langle u,v\rangle \in \mathbb{C}$ | Define amplitudes de probabilidad; la fase relativa es física |
| **Valores Propios** | Matrices simétricas: reales | Matrices hermíticas: **reales** | **Observables son hermíticos, sus medidas son reales** |
| **Evolución** | Operadores ortogonales | **Operadores unitarios** ($U^\dagger U = I$) | Evolución temporal unitaria conserva probabilidad; requiere $i$ en Schrödinger |
| **Relaciones de Conmutación** | No admiten $[x,p]=i\hbar$ naturalmente | **Admiten y requieren** la $i$ en $[x,p]=i\hbar$ | Origen del principio de incertidumbre |
| **Información Codificada** | Magnitud | **Magnitud y Fase** | La fase es clave para interferencia, enredamiento y coherencia cuántica |

---

## Conclusión Epistemológica

Matemáticamente, $C^n$ es una estructura más rica que $R^n$ gracias a:
1. La clausura algebraica de $\mathbb{C}$
2. El producto interno hermítico
3. Una teoría espectral completa y natural

Físicamente, **la mecánica cuántica es intrínsecamente compleja**. La necesidad de codificar **fases relativas**, la estructura de **observables como operadores hermíticos**, la **unitaridad de la evolución temporal** y la forma misma de las **relaciones de conmutación fundamentales** hacen de $C^n$ (y sus generalizaciones a espacios de Hilbert) el lenguaje natural y necesario para describir la realidad cuántica.

La complejidad no es un mero artefacto matemático, sino una característica esencial de la trama de la realidad física a escalas fundamentales.

---
---
---
## **2.1.4 Productos Internos**

Un **producto interno** es una función que toma como entrada dos vectores $|v\rangle$ y $|w\rangle$ de un espacio vectorial y produce un número complejo como salida. Por el momento, será conveniente escribir el producto interno de $|v\rangle$ y $|w\rangle$ como $(|v\rangle, |w\rangle)$. Esta no es la notación estándar de la mecánica cuántica; por claridad pedagógica, la notación $(\cdot, \cdot)$ será útil ocasionalmente en este capítulo. La notación estándar en mecánica cuántica para el producto interno $(|v\rangle, |w\rangle)$ es $\langle v|w\rangle$, donde $|v\rangle$ y $|w\rangle$ son vectores en el espacio con producto interno, y la notación $\langle v|$ se usa para el **vector dual** al vector $|v\rangle$; el dual es un operador lineal desde el espacio de producto interno $V$ hasta los números complejos $\mathbb{C}$, definido por $\langle v|(|w\rangle) \equiv \langle v|w\rangle \equiv (|v\rangle, |w\rangle)$. Veremos pronto que la representación matricial de los vectores duales es simplemente un vector fila.

Una función $(\cdot, \cdot)$ de $V \times V$ a $\mathbb{C}$ es un producto interno si satisface los requisitos de que:

1. $(\cdot, \cdot)$ es lineal en el segundo argumento,
   $$
   \left( |v\rangle, \sum_i \lambda_i |w_i\rangle \right) = \sum_i \lambda_i \left( |v\rangle, |w_i\rangle \right).
   $$
2. $(|v\rangle, |w\rangle) = (|w\rangle, |v\rangle)^*$.
3. $(|v\rangle, |v\rangle) \geq 0$ con igualdad si y solo si $|v\rangle = 0$.

Por ejemplo, $\mathbb{C}^n$ tiene un producto interno definido por
$$
((y_1, \ldots, y_n), (z_1, \ldots, z_n)) \equiv \sum_i y_i^* z_i = [y_1^* \cdots y_n^*] \begin{bmatrix} z_1 \\ \vdots \\ z_n \end{bmatrix}.
$$

---

**Explicación Intuitiva**

El producto interno es una herramienta fundamental que generaliza el concepto de "ángulo" y "longitud" en espacios vectoriales complejos. En esencia, nos permite medir la "similitud" o "proyección" entre dos vectores, teniendo en cuenta no solo sus magnitudes sino también su orientación relativa en un espacio complejo.

- **Linealidad en el segundo argumento**: Esto significa que si tenemos un vector fijo $|v\rangle$, el producto interno con una combinación lineal de otros vectores se distribuye como una suma ponderada. Es análogo a la propiedad distributiva del producto punto en geometría euclidiana.
  
- **Conjugación hermítica (simetría conjugada)**: $(|v\rangle, |w\rangle) = (|w\rangle, |v\rangle)^*$. Esta propiedad asegura que cuando medimos el producto interno de un vector consigo mismo, el resultado es real. En efecto, $(|v\rangle, |v\rangle) = (|v\rangle, |v\rangle)^*$, por lo que debe ser un número real. Además, esta propiedad captura la idea de que el producto interno no es simétrico en el sentido real ordinario, sino que intercambiar los vectores conjuga el resultado. Esto es crucial para mantener consistencia con la noción de "ángulo" en espacios complejos.

- **Positividad definida**: $(|v\rangle, |v\rangle) \geq 0$, y es cero solo para el vector cero. Esto nos permite definir una **norma** (longitud) a partir del producto interno: $\||v\rangle\| = \sqrt{\langle v|v\rangle}$. La positividad garantiza que la longitud sea un número real no negativo, y que solo el vector cero tenga longitud cero.

El ejemplo en $\mathbb{C}^n$ muestra la forma más común de producto interno en espacios complejos finito-dimensionales: se multiplica cada componente del primer vector por el conjugado complejo del componente correspondiente del segundo vector, y se suman. Esto se puede escribir como el producto de un vector fila (el conjugado hermítico del primer vector) por un vector columna (el segundo vector). Esta estructura es la base de la notación bra-ket de Dirac, donde $\langle v|$ es el vector fila (bra) y $|w\rangle$ es el vector columna (ket).

---

### **Ejercicio 2.5**
Verifica que $(\cdot, \cdot)$ recién definido es un producto interno en $\mathbb{C}^n$.

**Solución/Guía**:
Para verificarlo, debemos comprobar las tres propiedades:

1. **Linealidad en el segundo argumento**:
   Sean $|v\rangle = (v_1, \ldots, v_n)$, $|w\rangle = (w_1, \ldots, w_n)$, y $|u\rangle = (u_1, \ldots, u_n)$ vectores en $\mathbb{C}^n$, y sean $\alpha, \beta \in \mathbb{C}$. Entonces:
   $$
   (|v\rangle, \alpha|w\rangle + \beta|u\rangle) = \sum_{i=1}^n v_i^* (\alpha w_i + \beta u_i) = \alpha \sum_{i=1}^n v_i^* w_i + \beta \sum_{i=1}^n v_i^* u_i = \alpha(|v\rangle, |w\rangle) + \beta(|v\rangle, |u\rangle).
   $$

2. **Simetría conjugada**:
   $$
   (|v\rangle, |w\rangle) = \sum_{i=1}^n v_i^* w_i = \left( \sum_{i=1}^n w_i^* v_i \right)^* = (|w\rangle, |v\rangle)^*.
   $$

3. **Positividad definida**:
   $$
   (|v\rangle, |v\rangle) = \sum_{i=1}^n v_i^* v_i = \sum_{i=1}^n |v_i|^2 \geq 0,
   $$
   y es igual a cero si y solo si cada $|v_i|^2 = 0$, es decir, $v_i = 0$ para todo $i$, por lo que $|v\rangle = 0$.

Por lo tanto, cumple todas las propiedades.

---

### **Ejercicio 2.6**
Muestra que cualquier producto interno $(\cdot, \cdot)$ es conjugado-lineal en el primer argumento,
$$
\left( \sum_i \lambda_i |w_i\rangle, |v\rangle \right) = \sum_i \lambda_i^* (|w_i\rangle, |v\rangle). \tag{2.15}
$$

**Solución/Guía**:
Usando la propiedad de simetría conjugada y la linealidad en el segundo argumento:
$$
\left( \sum_i \lambda_i |w_i\rangle, |v\rangle \right) = \left( |v\rangle, \sum_i \lambda_i |w_i\rangle \right)^* = \left( \sum_i \lambda_i \left( |v\rangle, |w_i\rangle \right) \right)^* = \sum_i \lambda_i^* \left( |v\rangle, |w_i\rangle \right)^* = \sum_i \lambda_i^* \left( |w_i\rangle, |v\rangle \right).
$$
La última igualdad usa nuevamente la simetría conjugada: $(|v\rangle, |w_i\rangle)^* = (|w_i\rangle, |v\rangle)$.

Esto demuestra que el producto interno es **conjugado-lineal** en el primer argumento: los escalares salen como conjugados. Combinado con la linealidad en el segundo argumento, decimos que el producto interno es **sesquilineal** (una vez y media lineal).

---

**Explicación Intuitiva de la Conjugado-linealidad**:

La conjugado-linealidad en el primer argumento es una consecuencia natural de querer que la norma $\langle v|v\rangle$ sea real y positiva. Si no conjugáramos en el primer argumento, al calcular $\langle \lambda v|\lambda v\rangle$ obtendríamos $|\lambda|^2 \langle v|v\rangle$ solo si conjugamos uno de los $\lambda$. Matemáticamente, esto asegura que la longitud de un vector escalado sea $|\lambda|$ veces la longitud original, lo cual es deseable. Físicamente, en mecánica cuántica, los estados se representan por vectores unitarios (norma 1), y la multiplicación por un factor de fase global $e^{i\theta}$ no cambia el estado físico. La conjugado-linealidad garantiza que $\langle e^{i\theta} v | e^{i\theta} v \rangle = \langle v|v\rangle$, preservando la norma bajo cambios de fase global.

---

Llamamos a un espacio vectorial equipado con un producto interno un **espacio con producto interno**.

**Ejercicio 2.5** (ya resuelto arriba).

**Ejercicio 2.6** (ya resuelto arriba).

Las discusiones sobre mecánica cuántica a menudo se refieren al *espacio de Hilbert*. En los espacios vectoriales complejos de dimensión finita que surgen en computación cuántica e información cuántica, un espacio de Hilbert es *exactamente lo mismo* que un espacio con producto interno. De ahora en adelante usamos los dos términos indistintamente, prefiriendo el término espacio de Hilbert. En dimensiones infinitas, los espacios de Hilbert satisfacen restricciones técnicas adicionales más allá de los espacios con producto interno, que no necesitaremos preocuparnos.

Los vectores $|w\rangle$ y $|v\rangle$ son **ortogonales** si su producto interno es cero. Por ejemplo, $|w\rangle \equiv (1, 0)$ y $|v\rangle \equiv (0, 1)$ son ortogonales con respecto al producto interno definido por (2.14) (el ejemplo estándar en $\mathbb{C}^2$). Definimos la **norma** de un vector $|v\rangle$ por
$$
\||v\rangle\| \equiv \sqrt{\langle v | v \rangle}. \tag{2.16}
$$

Un **vector unitario** es un vector $|v\rangle$ tal que $\||v\rangle\| = 1$. También decimos que $|v\rangle$ está **normalizado** si $\||v\rangle\| = 1$. Es conveniente hablar de **normalizar** un vector dividiendo por su norma; así, $|v\rangle / \||v\rangle\|$ es la **forma normalizada** de $|v\rangle$, para cualquier vector no cero $|v\rangle$. Un conjunto $|i\rangle$ de vectores indexados por $i$ es **ortonormal** si cada vector es un vector unitario, y vectores distintos en el conjunto son ortogonales, es decir, $\langle i | j \rangle = \delta_{ij}$, donde $i$ y $j$ se eligen del conjunto de índices.

---

**Explicación Intuitiva**

- **Ortogonalidad**: Dos vectores son ortogonales si su producto interno es cero. En geometría, esto corresponde a perpendicularidad. En mecánica cuántica, los estados ortogonales representan estados distinguibles con certeza; por ejemplo, los estados de espín arriba y abajo a lo largo del eje z son ortogonales.

- **Norma**: La norma mide la "longitud" o "magnitud" del vector. En el contexto cuántico, la norma al cuadrado de un vector de estado está asociada a la probabilidad total, que debe ser 1. Por eso es crucial trabajar con vectores normalizados.

- **Conjuntos ortonormales**: Un conjunto ortonormal es una base donde todos los vectores son mutuamente perpendiculares y tienen longitud 1. Esto simplifica enormemente los cálculos, porque los coeficientes de un vector en esa base se obtienen simplemente tomando productos internos: si $\{|e_i\rangle\}$ es ortonormal, entonces cualquier vector $|v\rangle$ se expresa como $|v\rangle = \sum_i \langle e_i|v\rangle |e_i\rangle$. Los coeficientes $\langle e_i|v\rangle$ se llaman **amplitudes de probabilidad** en mecánica cuántica.

---

### **Ejercicio 2.7:**
Verifica que $|w\rangle \equiv (1, 1)$ y $|v\rangle \equiv (1, -1)$ son ortogonales. ¿Cuáles son las formas normalizadas de estos vectores?

**Solución**:
Usando el producto interno estándar en $\mathbb{C}^2$:
$$
\langle w|v \rangle = (1^*, 1^*) \begin{pmatrix} 1 \\ -1 \end{pmatrix} = 1 \cdot 1 + 1 \cdot (-1) = 1 - 1 = 0.
$$
Por lo tanto, son ortogonales.

Las normas:
$$
\||w\rangle\| = \sqrt{|1|^2 + |1|^2} = \sqrt{2}, \quad \||v\rangle\| = \sqrt{|1|^2 + |-1|^2} = \sqrt{2}.
$$
Las formas normalizadas son:
$$
\frac{|w\rangle}{\||w\rangle\|} = \frac{1}{\sqrt{2}} (1, 1), \quad \frac{|v\rangle}{\||v\rangle\|} = \frac{1}{\sqrt{2}} (1, -1).
$$

---

Supongamos que $|w_1\rangle, \ldots, |w_d\rangle$ es un conjunto de base para algún espacio vectorial $V$ con un producto interno. Existe un método útil, el procedimiento de *Gram–Schmidt*, que puede usarse para producir un conjunto de base ortonormal $|v_1\rangle, \ldots, |v_d\rangle$ para el espacio vectorial $V$. Definimos $|v_1\rangle \equiv |w_1\rangle / \| |w_1\rangle \|$, y para $1 \leq k \leq d-1$ definimos $|v_{k+1}\rangle$ inductivamente por
$$
|v_{k+1}\rangle \equiv \frac{|w_{k+1}\rangle - \sum_{i=1}^k \langle v_i | w_{k+1} \rangle |v_i\rangle}{\| |w_{k+1}\rangle - \sum_{i=1}^k \langle v_i | w_{k+1} \rangle |v_i\rangle\|}. \tag{2.17}
$$

No es difícil verificar que los vectores $|v_1\rangle, \ldots, |v_d\rangle$ forman un conjunto ortonormal que también es una base para $V$. Por lo tanto, cualquier espacio vectorial de dimensión finita $d$ tiene una base ortonormal, $|v_1\rangle, \ldots, |v_d\rangle$.

---

**Explicación Intuitiva del Procedimiento de Gram-Schmidt**

Gram-Schmidt es una forma sistemática de tomar un conjunto de vectores linealmente independientes (una base) y "ortogonalizarlos" sin cambiar el espacio que generan. La idea es construir los nuevos vectores ortonormales uno por uno, asegurando que cada nuevo vector sea ortogonal a todos los anteriores.

**Paso a paso**:

1. Tomamos el primer vector de la base original y simplemente lo normalizamos para obtener el primer vector ortonormal $|v_1\rangle$. Este define la dirección inicial.

2. Para el segundo vector $|w_2\rangle$, queremos construir un vector que sea ortogonal a $|v_1\rangle$. Para ello, restamos de $|w_2\rangle$ su proyección sobre $|v_1\rangle$. La proyección es $\langle v_1|w_2\rangle |v_1\rangle$ (ya que $|v_1\rangle$ es unitario). El resultado, $|w_2'\rangle = |w_2\rangle - \langle v_1|w_2\rangle |v_1\rangle$, es ortogonal a $|v_1\rangle$ (puedes verificarlo tomando el producto interno con $|v_1\rangle$). Luego normalizamos $|w_2'\rangle$ para obtener $|v_2\rangle$.

3. Para el tercer vector $|w_3\rangle$, restamos sus proyecciones sobre $|v_1\rangle$ y $|v_2\rangle$: $|w_3'\rangle = |w_3\rangle - \langle v_1|w_3\rangle |v_1\rangle - \langle v_2|w_3\rangle |v_2\rangle$. Este vector es ortogonal a ambos. Luego normalizamos.

4. Continuamos así hasta agotar todos los vectores.

La razón por la que esto funciona es que en cada paso eliminamos la componente del nuevo vector que está en el subespacio ya cubierto por los vectores ortonormales anteriores, dejando solo la componente perpendicular. La normalización asegura longitud unitaria.

**Importancia en mecánica cuántica**: Dado que los espacios de estados cuánticos son espacios de Hilbert, siempre podemos elegir una base ortonormal para trabajar. Esto simplifica muchos cálculos, como el cálculo de probabilidades y valores esperados. Además, en algoritmos cuánticos, a menudo se requiere preparar estados en una base ortonormal.

---

### **Ejercicio 2.8:**
Demuestra que el procedimiento de Gram–Schmidt produce una base ortonormal para $V$.

**Esbozo de prueba**:
Por inducción. Supongamos que después de $k$ pasos hemos construido un conjunto ortonormal $\{|v_1\rangle, \ldots, |v_k\rangle\}$ que genera el mismo subespacio que $\{|w_1\rangle, \ldots, |w_k\rangle\}$. Para $k+1$, definimos $|w_{k+1}'\rangle = |w_{k+1}\rangle - \sum_{i=1}^k \langle v_i|w_{k+1}\rangle |v_i\rangle$. Nota que $|w_{k+1}'\rangle \neq 0$ porque de lo contrario $|w_{k+1}\rangle$ sería combinación lineal de los $|v_i\rangle$ (y por tanto de los $|w_1\rangle, \ldots, |w_k\rangle$), contradiciendo la independencia lineal de la base original. Luego, para cualquier $j \leq k$:
$$
\langle v_j|w_{k+1}'\rangle = \langle v_j|w_{k+1}\rangle - \sum_{i=1}^k \langle v_i|w_{k+1}\rangle \langle v_j|v_i\rangle = \langle v_j|w_{k+1}\rangle - \langle v_j|w_{k+1}\rangle = 0,
$$
debido a que $\langle v_j|v_i\rangle = \delta_{ji}$ Así, $|w_{k+1}'\rangle$ es ortogonal a todos los $|v_j\rangle$ anteriores. Luego, definimos $|v_{k+1}\rangle = |w_{k+1}'\rangle / \||w_{k+1}'\rangle\|$, que tiene norma 1 y sigue siendo ortogonal a los anteriores. Además, $|w_{k+1}\rangle$ está en el espacio generado por $\{|v_1\rangle, \ldots, |v_{k+1}\rangle\}$, por construcción. Por inducción, al final obtenemos un conjunto ortonormal de $d$ vectores, que es una base porque son linealmente independientes y hay $d$ de ellos.

---

De ahora en adelante, cuando hablamos de una representación matricial para un operador lineal, nos referimos a una representación matricial con respecto a bases ortonormales de entrada y salida. También usamos la convención de que si los espacios de entrada y salida para un operador lineal son los mismos, entonces las bases de entrada y salida son las mismas, a menos que se indique lo contrario.

**Explicación Intuitiva**:

Cuando representamos un operador lineal como una matriz, la elección de bases afecta los elementos de la matriz. Si elegimos bases ortonormales, la matriz tiene una forma particularmente simple: el elemento $A_{ij}$ de la matriz del operador $A$ es simplemente $\langle i|A|j\rangle$, donde $|i\rangle$ y $|j\rangle$ son los vectores de la base ortonormal de salida y entrada, respectivamente. Esto facilita el cálculo de la acción del operador sobre vectores: si $|v\rangle = \sum_j v_j |j\rangle$, entonces la componente $i$-ésima de $A|v\rangle$ es $\sum_j A_{ij} v_j$.

Además, en mecánica cuántica, los operadores que representan observables (hermíticos) tienen matrices hermíticas cuando se usan bases ortonormales, y los operadores unitarios tienen matrices unitarias. Esta correspondencia es natural y poderosa.

La convención de usar la misma base para entrada y salida cuando el espacio es el mismo es estándar, pero a veces se usan bases diferentes, por ejemplo, cuando se cambia de base. En tales casos, se necesita una matriz de cambio de base, que es unitaria si ambas bases son ortonormales.