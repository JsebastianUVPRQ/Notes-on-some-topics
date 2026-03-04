Aquí tienes la traducción al español del fragmento del libro de Nielsen y Chuang:

===== Página 1 =====

**2.1 Álgebra lineal**

"Este libro está escrito tanto para perturbar y molestar como para instruir". La primera línea de *Sobre vectores*, de Banesh Hoffmann.

"La vida es compleja: tiene partes reales e imaginarias". - Anónimo.

El álgebra lineal es el estudio de los espacios vectoriales y de las operaciones lineales sobre esos espacios vectoriales. Una buena comprensión de la mecánica cuántica se basa en un sólido dominio del álgebra lineal elemental. En esta sección repasamos algunos conceptos básicos del álgebra lineal y describimos las notaciones estándar que se utilizan para estos conceptos en el estudio de la mecánica cuántica. Estas notaciones se resumen en la Figura 2.1 en la página 62, con la notación cuántica en la columna izquierda y la descripción algebraico-lineal en la columna derecha. Quizá quieras echar un vistazo a la tabla y ver cuántos de los conceptos de la columna derecha reconoces.

En nuestra opinión, el principal obstáculo para asimilar los postulados de la mecánica cuántica no son los postulados en sí, sino más bien el gran conjunto de nociones de álgebra lineal necesarias para entenderlos. Sumado a la inusual notación de Dirac adoptada por los físicos para la mecánica cuántica, puede parecer (falsamente) bastante temible. Por estas razones, aconsejamos al lector no familiarizado con la mecánica cuántica que lea rápidamente el material que sigue, deteniéndose principalmente para concentrarse en entender lo absolutamente básico de la notación que se está usando. Luego proceda a un estudio cuidadoso del tema principal del capítulo -los postulados de la mecánica cuántica- volviendo a estudiar las nociones y notaciones algebraico-lineales necesarias con más profundidad, según sea necesario.

Los objetos básicos del álgebra lineal son los espacios vectoriales. El espacio vectorial que más nos interesa es $\mathbf{C}^{n}$, el espacio de todas las $n$-tuplas de números complejos, $(z_{1},\ldots ,z_{n})$. Los elementos de un espacio vectorial se llaman vectores, y a veces usaremos la notación de matriz columna

$\left[ \begin{array}{c}z_{1} \\ \vdots \\ z_{n} \end{array} \right] \quad (2.1)$

para indicar un vector. Hay una operación de suma definida que lleva pares de vectores a otros vectores. En $\mathbf{C}^{n}$ la operación de suma para vectores se define por

$\left[ \begin{array}{c}z_{1} \\ \vdots \\ z_{n} \end{array} \right] + \left[ \begin{array}{c}z_{1}' \\ \vdots \\ z_{n}' \end{array} \right] \equiv \left[ \begin{array}{c}z_{1} + z_{1}' \\ \vdots \\ z_{n} + z_{n}' \end{array} \right], \quad (2.2)$

donde las operaciones de suma a la derecha son simplemente sumas ordinarias de números complejos. Además, en un espacio vectorial hay una multiplicación por un escalar. En $\mathbf{C}^{n}$ esta operación se define por

$z\left[ \begin{array}{c}z_{1} \\ \vdots \\ z_{n} \end{array} \right] \equiv \left[ \begin{array}{c}z z_{1} \\ \vdots \\ z z_{n} \end{array} \right], \quad (2.3)$

===== Página 2 =====

**62 Introducción a la mecánica cuántica**

donde $z$ es un escalar, es decir, un número complejo, y las multiplicaciones a la derecha son multiplicaciones ordinarias de números complejos. Los físicos a veces se refieren a los números complejos como *c-números*.

La mecánica cuántica es nuestra principal motivación para estudiar álgebra lineal, por lo que usaremos la notación estándar de la mecánica cuántica para conceptos algebraico-lineales. La notación cuántica estándar para un vector en un espacio vectorial es la siguiente:

$|\psi \rangle . \quad (2.4)$

$\psi$ es una etiqueta para el vector (cualquier etiqueta es válida, aunque preferimos usar etiquetas simples como $\psi$ y $\phi$). La notación $|\cdot \rangle$ se usa para indicar que el objeto es un vector. El objeto completo $|\psi \rangle$ a veces se llama *ket*, aunque no usaremos esa terminología a menudo.

Un espacio vectorial también contiene un vector cero especial, que denotamos por 0. Satisface la propiedad de que para cualquier otro vector $|v\rangle ,|v\rangle +0 = |v\rangle$. Nótese que no usamos la notación de ket para el vector cero: es la única excepción que haremos. La razón de hacer la excepción es que es convencional usar la notación 'obvia' para el vector cero, $|0\rangle$, para significar algo completamente distinto. La operación de multiplicación por escalar es tal que $z0 = 0$ para cualquier número complejo $z$. Por conveniencia, usamos la notación $(z_{1},\ldots ,z_{n})$ para denotar una matriz columna con entradas $z_{1},\ldots ,z_{n}$. En $\mathbf{C}^{n}$ el elemento cero es $(0,0,\ldots ,0)$. Un subespacio vectorial de un espacio vectorial $V$ es un subconjunto $W$ de $V$ tal que $W$ también es un espacio vectorial, es decir, $W$ debe ser cerrado bajo multiplicación por escalar y suma.

<table>
<thead>
<tr><th>Notación</th><th>Descripción</th></tr>
</thead>
<tbody>
<tr><td>z*</td><td>Conjugado complejo del número complejo z.<br>(1 + i)* = 1 - i</td></tr>
<tr><td>|ψ⟩</td><td>Vector. También conocido como ket.</td></tr>
<tr><td>⟨ψ|</td><td>Vector dual a |ψ⟩. También conocido como bra.</td></tr>
<tr><td>⟨φ|ψ⟩</td><td>Producto interno entre los vectores |φ⟩ y |ψ⟩.</td></tr>
<tr><td>|φ⟩ ⊗ |ψ⟩</td><td>Producto tensorial de |φ⟩ y |ψ⟩.</td></tr>
<tr><td>|φ⟩|ψ⟩</td><td>Notación abreviada para el producto tensorial de |φ⟩ y |ψ⟩.</td></tr>
<tr><td>A*</td><td>Conjugado complejo de la matriz A.</td></tr>
<tr><td>A*T</td><td>Transpuesta de la matriz A.</td></tr>
<tr><td>A†</td><td>Conjugado hermitiano o adjunto de la matriz A, A† = (A*T)*.</td></tr>
<tr><td>⟨φ|A|ψ⟩</td><td>Producto interno entre |φ⟩ y A|ψ⟩.<br>Equivalentemente, producto interno entre A†|φ⟩ y |ψ⟩.</td></tr>
</tbody>
</table>

Figura 2.1. Resumen de algunas notaciones cuánticas estándar para nociones del álgebra lineal. Este estilo de notación se conoce como notación de Dirac.

#### 2.1.1 Bases e independencia lineal

Un conjunto generador (spanning set) para un espacio vectorial es un conjunto de vectores $|v_{1}\rangle ,\ldots ,|v_{n}\rangle$ tal que cualquier vector $|v\rangle$ en el espacio vectorial puede escribirse como una combinación lineal $|v\rangle = \sum_{i}a_{i}|v_{i}\rangle$ de vectores

===== Página 3 =====

en ese conjunto. Por ejemplo, un conjunto generador para el espacio vectorial $\mathbf{C}^2$ es el conjunto

$|v_1\rangle \equiv \left[ \begin{array}{c}1\\ 0 \end{array} \right]; |v_2\rangle \equiv \left[ \begin{array}{c}0\\ 1 \end{array} \right], \quad (2.5)$

ya que cualquier vector

$|v\rangle = \left[ \begin{array}{c}a_1\\ a_2 \end{array} \right] \quad (2.6)$

en $\mathbf{C}^2$ puede escribirse como una combinación lineal $|v\rangle = a_1|v_1\rangle +a_2|v_2\rangle$ de los vectores $|v_1\rangle$ y $|v_2\rangle$. Decimos que los vectores $|v_1\rangle$ y $|v_2\rangle$ generan el espacio vectorial $\mathbf{C}^2$.

En general, un espacio vectorial puede tener muchos conjuntos generadores diferentes. Un segundo conjunto generador para el espacio vectorial $\mathbf{C}^2$ es el conjunto

$|v_1\rangle \equiv \frac{1}{\sqrt{2}}\left[ \begin{array}{c}1\\ 1 \end{array} \right]; |v_2\rangle \equiv \frac{1}{\sqrt{2}}\left[ \begin{array}{c}1\\ -1 \end{array} \right], \quad (2.7)$

ya que un vector arbitrario $|v\rangle = (a_1,a_2)$ puede escribirse como una combinación lineal de $|v_1\rangle$ y $|v_2\rangle$

$|v\rangle = \frac{a_1 + a_2}{\sqrt{2}} |v_1\rangle +\frac{a_1 - a_2}{\sqrt{2}} |v_2\rangle . \quad (2.8)$

Un conjunto de vectores no nulos $|v_1\rangle ,\ldots ,|v_n\rangle$ es linealmente dependiente si existe un conjunto de números complejos $a_1,\ldots ,a_n$ con $a_i\neq 0$ para al menos un valor de $i$, tal que

$a_1|v_1\rangle +a_2|v_2\rangle +\dots +a_n|v_n\rangle = 0. \quad (2.9)$

Un conjunto de vectores es linealmente independiente si no es linealmente dependiente. Puede demostrarse que dos conjuntos cualesquiera de vectores linealmente independientes que generan un espacio vectorial $V$ contienen el mismo número de elementos. Llamamos a tal conjunto una base para $V$. Además, tal conjunto base siempre existe. El número de elementos en la base se define como la dimensión de $V$. En este libro solo nos interesaremos en espacios vectoriales de dimensión finita. Hay muchas preguntas interesantes y a menudo difíciles asociadas con espacios vectoriales de dimensión infinita. No necesitaremos preocuparnos por estas preguntas.

Ejercicio 2.1: (Dependencia lineal: ejemplo) Muestra que $(1, - 1), (1,2)$ y $(2,1)$ son linealmente dependientes.

#### 2.1.2 Operadores lineales y matrices

Un operador lineal entre espacios vectoriales $V$ y $W$ se define como cualquier función $A:V\to W$ que es lineal en sus entradas,

$A\left(\sum_{i}a_{i}|v_{i}\rangle\right) = \sum_{i}a_{i}A\left(|v_{i}\rangle\right). \quad (2.10)$

Normalmente solo escribimos $A|v\rangle$ para denotar $A(|v\rangle)$. Cuando decimos que un operador lineal $A$ está definido sobre un espacio vectorial, $V$, queremos decir que $A$ es un operador lineal de $V$ a $V$. Un operador lineal importante en cualquier espacio vectorial $V$ es el operador identidad, $I_V$, definido por la ecuación $I_V|v\rangle \equiv |v\rangle$ para todos los vectores $|v\rangle$. Donde no haya riesgo de confusión, omitiremos el subíndice $V$ y solo escribiremos $I$ para denotar el operador identidad. Otro operador lineal importante es el operador cero, que denotamos 0. El operador cero mapea todos los vectores al

===== Página 4 =====

**64 Introducción a la mecánica cuántica**

vector cero, $0|v\rangle \equiv 0$. Está claro a partir de (2.10) que una vez que se especifica la acción de un operador lineal $A$ sobre una base, la acción de $A$ está completamente determinada para todas las entradas.

Supongamos que $V,W$ y $X$ son espacios vectoriales, y $A:V\to W$ y $B:W\to X$ son operadores lineales. Entonces usamos la notación $BA$ para denotar la composición de $B$ con $A$ definida por $(BA)(|v\rangle)\equiv B(A(|v\rangle))$. Nuevamente, escribimos $BA|v\rangle$ como una abreviatura de $(BA)(|v\rangle)$.

La forma más conveniente de entender los operadores lineales es en términos de sus representaciones matriciales. De hecho, los puntos de vista de operador lineal y matriz resultan ser completamente equivalentes. Sin embargo, el punto de vista matricial puede serte más familiar. Para ver la conexión, ayuda primero entender que una matriz compleja $A$ de $m$ por $n$ con entradas $A_{ij}$ es en realidad un operador lineal que envía vectores en el espacio vectorial $\mathbf{C}^n$ al espacio vectorial $\mathbf{C}^m$, bajo la multiplicación de la matriz $A$ por un vector en $\mathbf{C}^n$. Más precisamente, la afirmación de que la matriz $A$ es un operador lineal simplemente significa que

$A\left(\sum_{i}a_{i}|v_{i}\rangle\right) = \sum_{i}a_{i}A|v_{i}\rangle \quad (2.11)$

es cierta como una ecuación donde la operación es la multiplicación matricial de $A$ por vectores columna. ¡Claramente, esto es cierto!

Hemos visto que las matrices pueden considerarse como operadores lineales. ¿Se puede dar una representación matricial a los operadores lineales? De hecho sí se puede, como explicamos ahora. Esta equivalencia entre los dos puntos de vista justifica que intercambiemos términos de la teoría de matrices y la teoría de operadores a lo largo del libro. Supongamos que $A:V\to W$ es un operador lineal entre los espacios vectoriales $V$ y $W$. Supongamos que $|v_{1}\rangle ,\ldots ,|v_{m}\rangle$ es una base para $V$ y $|w_{1}\rangle ,\ldots ,|w_{n}\rangle$ es una base para $W$. Entonces para cada $j$ en el rango $1,\ldots ,m$, existen números complejos $A_{1j}$ hasta $A_{nj}$ tales que

$A|v_{j}\rangle = \sum_{i}A_{ij}|w_{i}\rangle . \quad (2.12)$

Se dice que la matriz cuyas entradas son los valores $A_{ij}$ forma una representación matricial del operador $A$. Esta representación matricial de $A$ es completamente equivalente al operador $A$ y usaremos indistintamente el punto de vista de la representación matricial y el del operador abstracto. Nótese que para establecer la conexión entre matrices y operadores lineales debemos especificar un conjunto de estados base de entrada y salida para los espacios vectoriales de entrada y salida del operador lineal.

Ejercicio 2.2: (Representaciones matriciales: ejemplo) Supón que $V$ es un espacio vectorial con vectores base $|0\rangle$ y $|1\rangle$, y $A$ es un operador lineal de $V$ a $V$ tal que $A|0\rangle = |1\rangle$ y $A|1\rangle = |0\rangle$. Da una representación matricial para $A$, con respecto a la base de entrada $|0\rangle ,|1\rangle$, y la base de salida $|0\rangle ,|1\rangle$. Encuentra bases de entrada y salida que den lugar a una representación matricial diferente de $A$.

Ejercicio 2.3: (Representación matricial para productos de operadores) Supón que $A$ es un operador lineal del espacio vectorial $V$ al espacio vectorial $W$, y $B$ es un operador lineal del espacio vectorial $W$ al espacio vectorial $X$. Sean $|v_{i}\rangle ,|w_{j}\rangle$ y $|x_{k}\rangle$ bases para los espacios vectoriales $V,W$ y $X$, respectivamente. Muestra que la representación matricial para la transformación lineal $BA$ es el producto matricial de las representaciones matriciales para $B$ y $A$, con respecto a las bases apropiadas.

===== Página 5 =====

#### 2.1.3 Las matrices de Pauli

Cuatro matrices extremadamente útiles que a menudo tendremos ocasión de usar son las matrices de Pauli. Estas son matrices de 2 por 2, que se denotan de varias formas. Las matrices y sus correspondientes notaciones se muestran en la Figura 2.2. Las matrices de Pauli son tan útiles en el estudio de la computación cuántica y la información cuántica que te animamos a memorizarlas trabajando en detalle los muchos ejemplos y ejercicios basados en ellas en las secciones posteriores.

ecuación[[223, 277, 623, 313]]

ecuación[[178, 323, 623, 359]]

Figura 2.2. Las matrices de Pauli. A veces $I$ se omite de la lista y solo $X,Y$ y $Z$ se conocen como matrices de Pauli.

#### 2.1.4 Productos internos

Un producto interno es una función que toma como entrada dos vectores $|v\rangle$ y $|w\rangle$ de un espacio vectorial y produce un número complejo como salida. Por el momento, será conveniente escribir el producto interno de $|v\rangle$ y $|w\rangle$ como $(|v\rangle ,|w\rangle)$. Esta no es la notación mecánico-cuántica estándar; para claridad pedagógica, la notación $(\cdot ,\cdot)$ será útil ocasionalmente en este capítulo. La notación mecánico-cuántica estándar para el producto interno $(|v\rangle ,|w\rangle)$ es $\langle v|w\rangle$, donde $|v\rangle$ y $|w\rangle$ son vectores en el espacio con producto interno, y la notación $\langle v|$ se usa para el vector dual al vector $|v\rangle$; el dual es un operador lineal desde el espacio con producto interno $V$ a los números complejos $\mathbf{C}$, definido por $\langle v|(|w\rangle)\equiv \langle v|w\rangle \equiv (|v\rangle ,|w\rangle)$. Veremos pronto que la representación matricial de los vectores duales es solo un vector fila.

Una función $(\cdot ,\cdot)$ de $V\times V$ a $\mathbf{C}$ es un producto interno si satisface los requisitos de que:

(1) $(\cdot ,\cdot)$ es lineal en el segundo argumento,

$\left(|v\rangle ,\sum_{i}\lambda_{i}|w_{i}\rangle\right) = \sum_{i}\lambda_{i}\left(|v\rangle ,|w_{i}\rangle\right). \quad (2.13)$

(2) $(|v\rangle ,|w\rangle) = (|w\rangle ,|v\rangle)^{*}$

(3) $(|v\rangle ,|v\rangle)\geq 0$ con igualdad si y solo si $|v\rangle = 0$

Por ejemplo, $\mathbf{C}^{n}$ tiene un producto interno definido por

$((y_{1},\ldots ,y_{n}),(z_{1},\ldots ,z_{n}))\equiv \sum_{i}y_{i}^{*}z_{i} = [y_{1}^{*}\ldots y_{n}^{*}]\left[ \begin{array}{c}z_{1}\\ \vdots \\ z_{n} \end{array} \right]. \quad (2.14)$

===== Página 6 =====

**66 Introducción a la mecánica cuántica**

Llamamos espacio con producto interno a un espacio vectorial equipado con un producto interno.

Ejercicio 2.5: Verifica que $(\cdot ,\cdot)$ recién definido es un producto interno en $\mathbf{C}^{n}$.

Ejercicio 2.6: Muestra que cualquier producto interno $(\cdot ,\cdot)$ es conjugado-lineal en el primer argumento,

$\left(\sum_{i}\lambda_{i}|w_{i}\rangle ,|v\rangle\right) = \sum_{i}\lambda_{i}^{*}(|w_{i}\rangle ,|v\rangle). \quad (2.15)$

Las discusiones sobre mecánica cuántica a menudo se refieren al espacio de Hilbert. En los espacios vectoriales complejos de dimensión finita que surgen en computación cuántica e información cuántica, un espacio de Hilbert es exactamente lo mismo que un espacio con producto interno. De ahora en adelante usaremos los dos términos indistintamente, prefiriendo el término espacio de Hilbert. En dimensiones infinitas, los espacios de Hilbert satisfacen restricciones técnicas adicionales más allá de los espacios con producto interno, de las cuales no necesitaremos preocuparnos.

Los vectores $|w\rangle$ y $|v\rangle$ son ortogonales si su producto interno es cero. Por ejemplo, $|w\rangle \equiv$ $(1,0)$ y $|v\rangle \equiv (0,1)$ son ortogonales con respecto al producto interno definido por (2.14). Definimos la norma de un vector $|v\rangle$ por

$\| |v\rangle \| \equiv \sqrt{\langle v|v\rangle}. \quad (2.16)$

Un vector unitario es un vector $|v\rangle$ tal que $\| |v\rangle \| = 1$. También decimos que $|v\rangle$ está normalizado si $\| |v\rangle \| = 1$. Es conveniente hablar de normalizar un vector dividiendo por su norma; así $|v\rangle /\| |v\rangle \|$ es la forma normalizada de $|v\rangle$, para cualquier vector no nulo $|v\rangle$. Un conjunto $|i\rangle$ de vectores con índice $i$ es ortonormal si cada vector es un vector unitario, y vectores distintos en el conjunto son ortogonales, es decir, $\langle i|j\rangle = \delta_{ij}$, donde $i$ y $j$ se eligen ambos del conjunto de índices.

Ejercicio 2.7: Verifica que $|w\rangle \equiv (1,1)$ y $|v\rangle \equiv (1, - 1)$ son ortogonales. ¿Cuáles son las formas normalizadas de estos vectores?

Supongamos que $|w_{1}\rangle ,\ldots ,|w_{d}\rangle$ es un conjunto base para algún espacio vectorial $V$ con un producto interno. Hay un método útil, el procedimiento de Gram-Schmidt, que puede usarse para producir un conjunto base ortonormal $|v_{1}\rangle ,\ldots ,|v_{d}\rangle$ para el espacio vectorial $V$. Define $|v_{1}\rangle \equiv |w_{1}\rangle /\| |w_{1}\rangle \|$ y para $1\leq k\leq d - 1$ define $|v_{k + 1}\rangle$ inductivamente por

$|v_{k + 1}\rangle \equiv \frac{|w_{k + 1}\rangle - \sum_{i = 1}^{k}\langle v_{i}|w_{k + 1}\rangle|v_{i}\rangle}{\| |w_{k + 1}\rangle - \sum_{i = 1}^{k}\langle v_{i}|w_{k + 1}\rangle|v_{i}\rangle\|}. \quad (2.17)$

No es difícil verificar que los vectores $|v_{1}\rangle ,\ldots ,|v_{d}\rangle$ forman un conjunto ortonormal que también es una base para $V$. Por lo tanto, cualquier espacio vectorial de dimensión finita $d$ tiene una base ortonormal, $|v_{1}\rangle ,\ldots ,|v_{d}\rangle$.

Ejercicio 2.8: Demuestra que el procedimiento de Gram-Schmidt produce una base ortonormal para $V$.

De ahora en adelante, cuando hablemos de una representación matricial para un operador lineal, nos referiremos a una representación matricial con respecto a bases de entrada y salida ortonormales. También usamos la convención de que si los espacios de entrada y salida para un operador lineal son los mismos, entonces las bases de entrada y salida son las mismas, a menos que se indique lo contrario.

===== Página 7 =====

Con estas convenciones, el producto interno en un espacio de Hilbert puede tener una representación matricial conveniente. Sean $|w\rangle = \sum_{i}w_{i}|i\rangle$ y $|v\rangle = \sum_{j}v_{j}|j\rangle$ representaciones de los vectores $|w\rangle$ y $|v\rangle$ con respecto a alguna base ortonormal $|i\rangle$. Entonces, dado que $\langle i|j\rangle = \delta_{ij}$,

$\begin{array}{l}{\langle v|w\rangle = \left(\sum_{i}v_{i}|i\rangle ,\sum_{j}w_{j}|j\rangle\right) = \sum_{ij}v_{i}^{*}w_{j}\delta_{ij} = \sum_{i}v_{i}^{*}w_{i}}\\ {= [v_{1}^{*}\dots v_{n}^{*}]\left[ \begin{array}{c}w_{1}\\ \vdots \\ w_{n} \end{array} \right].} \end{array} \quad (2.18)$

Es decir, el producto interno de dos vectores es igual al producto interno vectorial entre dos representaciones matriciales de esos vectores, siempre que las representaciones estén escritas con respecto a la misma base ortonormal. También vemos que el vector dual $\langle v|$ tiene una buena interpretación como el vector fila cuyas componentes son los conjugados complejos de las componentes correspondientes de la representación de vector columna de $|v\rangle$.

Hay una forma útil de representar operadores lineales que hace uso del producto interno, conocida como representación de producto externo. Supongamos que $|v\rangle$ es un vector en un espacio con producto interno $V$, y $|w\rangle$ es un vector en un espacio con producto interno $W$. Define $|w\rangle \langle v|$ como el operador lineal de $V$ a $W$ cuya acción se define por

$(|w\rangle \langle v|)(|v^{\prime}\rangle)\equiv |w\rangle \langle v|v^{\prime}\rangle = \langle v|v^{\prime}\rangle |w\rangle . \quad (2.20)$

Esta ecuación encaja perfectamente en nuestras convenciones notacionales, según las cuales la expresión $|w\rangle \langle v|v^{\prime}\rangle$ podría tener potencialmente uno de dos significados: la usaremos para denotar el resultado cuando el operador $|w\rangle \langle v|$ actúa sobre $|v^{\prime}\rangle$, y tiene una interpretación existente como el resultado de multiplicar $|w\rangle$ por el número complejo $\langle v|v^{\prime}\rangle$. Nuestras definiciones se eligen de modo que estos dos significados potenciales coincidan. ¡De hecho, definimos el primero en términos del segundo!

Podemos tomar combinaciones lineales de operadores de producto externo $|w\rangle \langle v|$ de la manera obvia. Por definición, $\sum_{i}a_{i}|w_{i}\rangle \langle v_{i}|$ es el operador lineal que, al actuar sobre $|v^{\prime}\rangle$, produce $\sum_{i}a_{i}|w_{i}\rangle \langle v_{i}|v^{\prime}\rangle$ como salida.

La utilidad de la notación de producto externo puede discernirse a partir de un resultado importante conocido como la relación de completitud para vectores ortonormales. Sea $|i\rangle$ cualquier base ortonormal para el espacio vectorial $V$, de modo que un vector arbitrario $|v\rangle$ puede escribirse $|v\rangle = \sum_{i}v_{i}|i\rangle$ para algún conjunto de números complejos $v_{i}$. Nótese que $\langle i|v\rangle = v_{i}$ y por lo tanto

$\left(\sum_{i}|i\rangle \langle i|\right)|v\rangle = \sum_{i}|i\rangle \langle i|v\rangle = \sum_{i}v_{i}|i\rangle = |v\rangle . \quad (2.21)$

Dado que la última ecuación es cierta para todo $|v\rangle$, se sigue que

$\sum_{i}|i\rangle \langle i| = I. \quad (2.22)$

Esta ecuación se conoce como la relación de completitud. Una aplicación de la relación de completitud es dar un medio para representar cualquier operador en la notación de producto externo. Supongamos que $A:V\to W$ es un operador lineal, $|v_{i}\rangle$ es una base ortonormal para $V$, y $|w_{j}\rangle$ una base ortonormal para $W$. Usando la relación de completitud dos veces obtenemos

$A = I_{W}A I_{V} \quad (2.23)$

===== Página 8 =====

#### 2.1.5 Vectores propios y valores propios

Un vector propio de un operador lineal $A$ en un espacio vectorial es un vector no nulo $|v\rangle$ tal que $A|v\rangle = v|v\rangle$, donde $v$ es un número complejo conocido como el valor propio de $A$ correspondiente a $|v\rangle$. A menudo será conveniente usar la notación $v$ tanto como una etiqueta para el vector propio, como para representar el valor propio. Suponemos que estás familiarizado con las propiedades elementales de los valores propios y vectores propios; en particular, cómo encontrarlos, mediante la ecuación característica. La función característica se define como $c(\lambda) \equiv \det |A - \lambda I|$.

$= \sum_{ij}|w_j\rangle \langle w_j|A|v_i\rangle \langle v_i| \quad (2.24)$ $= \sum_{ij}\langle w_j|A|v_i\rangle |w_j\rangle \langle v_i|, \quad (2.25)$

que es la representación de producto externo para $A$. También vemos a partir de esta ecuación que $A$ tiene el elemento de matriz $\langle w_j|A|v_i\rangle$ en la columna $i$ y la fila $j$, con respecto a la base de entrada $|v_i\rangle$ y la base de salida $|w_j\rangle$.

Una segunda aplicación que ilustra la utilidad de la relación de completitud es la desigualdad de Cauchy-Schwarz. Este importante resultado se discute en el Recuadro 2.1, en esta página.

Ejercicio 2.9: (Operadores de Pauli y el producto externo) Las matrices de Pauli (Figura 2.2 en la página 65) pueden considerarse como operadores con respecto a una base ortonormal $|0\rangle$ , $|1\rangle$ para un espacio de Hilbert bidimensional. Expresa cada uno de los operadores de Pauli en la notación de producto externo.

Ejercicio 2.10: Supón que $|v_i\rangle$ es una base ortonormal para un espacio con producto interno $V$. ¿Cuál es la representación matricial para el operador $|v_j\rangle \langle v_k|$, con respecto a la base $|v_i\rangle$?

## Recuadro 2.1: La desigualdad de Cauchy-Schwarz

La desigualdad de Cauchy-Schwarz es un hecho geométrico importante sobre espacios de Hilbert. Establece que para dos vectores cualesquiera $|v\rangle$ y $|w\rangle$, $|\langle v|w\rangle |^2 \leq \langle v|v\rangle \langle w|w\rangle$. Para ver esto, usa el procedimiento de Gram-Schmidt para construir una base ortonormal $|i\rangle$ para el espacio vectorial tal que el primer miembro de la base $|i\rangle$ sea $|w\rangle /\sqrt{\langle w|w\rangle}$. Usando la relación de completitud $\sum_i |i\rangle \langle i| = I$, y descartando algunos términos no negativos se obtiene

$\begin{array}{r l} & {\langle v|v\rangle \langle w|w\rangle = \sum_{i}\langle v|i\rangle \langle i|v\rangle \langle w|w\rangle}\\ & {\qquad \geq \frac{\langle v|w\rangle\langle w|v\rangle}{\langle w|w\rangle}\langle w|w\rangle}\\ & {\qquad = \langle v|w\rangle \langle w|v\rangle = |\langle v|w\rangle |^{2},} \end{array} \quad (2.28)$

como se requería. Un poco de reflexión muestra que la igualdad ocurre si y solo si $|v\rangle$ y $|w\rangle$ están linealmente relacionados, $|v\rangle = z|w\rangle$ o $|w\rangle = z|v\rangle$, para algún escalar $z$.

#### 2.1.5 Vectores propios y valores propios

Un vector propio de un operador lineal $A$ en un espacio vectorial es un vector no nulo $|v\rangle$ tal que $A|v\rangle = v|v\rangle$, donde $v$ es un número complejo conocido como el valor propio de $A$ correspondiente a $|v\rangle$. A menudo será conveniente usar la notación $v$ tanto como una etiqueta para el vector propio, como para representar el valor propio. Suponemos que estás familiarizado con las propiedades elementales de los valores propios y vectores propios; en particular, cómo encontrarlos, mediante la ecuación característica. La función característica se define como $c(\lambda) \equiv \det |A - \lambda I|$,

===== Página 9 =====

donde det es la función determinante para matrices; puede demostrarse que la función característica depende solo del operador $A$, y no de la representación matricial específica usada para $A$. Las soluciones de la ecuación característica $c(\lambda) = 0$ son los valores propios del operador $A$. Por el teorema fundamental del álgebra, todo polinomio tiene al menos una raíz compleja, por lo que todo operador $A$ tiene al menos un valor propio, y un vector propio correspondiente. El espacio propio correspondiente a un valor propio $v$ es el conjunto de vectores que tienen valor propio $v$. Es un subespacio vectorial del espacio vectorial sobre el que actúa $A$.

Una representación diagonal para un operador $A$ sobre un espacio vectorial $V$ es una representación $A = \sum_{i}\lambda_{i}|i\rangle \langle i|$, donde los vectores $|i\rangle$ forman un conjunto ortonormal de vectores propios para $A$ con valores propios correspondientes $\lambda_{i}$. Se dice que un operador es diagonalizable si tiene una representación diagonal. En la siguiente sección encontraremos un conjunto simple de condiciones necesarias y suficientes para que un operador en un espacio de Hilbert sea diagonalizable. Como ejemplo de una representación diagonal, nótese que la matriz de Pauli $Z$ puede escribirse

$Z = \left[ \begin{array}{cc}1 & 0\\ 0 & -1 \end{array} \right] = |0\rangle \langle 0| - |1\rangle \langle 1|, \quad (2.29)$

donde la representación matricial es con respecto a los vectores ortonormales $|0\rangle$ y $|1\rangle$, respectivamente. Las representaciones diagonales a veces también se conocen como descomposiciones ortonormales.

Cuando un espacio propio tiene más de una dimensión decimos que es degenerado. Por ejemplo, la matriz $A$ definida por

$A\equiv \left[ \begin{array}{ccc}2 & 0 & 0\\ 0 & 2 & 0\\ 0 & 0 & 0 \end{array} \right] \quad (2.30)$

tiene un espacio propio bidimensional correspondiente al valor propio 2. Los vectores propios $(1,0,0)$ y $(0,1,0)$ se dice que son degenerados porque son vectores propios linealmente independientes de $A$ con el mismo valor propio.

Ejercicio 2.11: (Descomposición en valores propios de las matrices de Pauli) Encuentra los vectores propios, valores propios y representaciones diagonales de las matrices de Pauli $X, Y$ y $Z$.

Ejercicio 2.12: Demuestra que la matriz

$\left[ \begin{array}{cc}1 & 0\\ 1 & 1 \end{array} \right] \quad (2.31)$

no es diagonalizable.

#### 2.1.6 Adjuntos y operadores hermíticos

Supongamos que $A$ es cualquier operador lineal en un espacio de Hilbert, $V$. Resulta que existe un operador lineal único $A^{\dagger}$ en $V$ tal que para todos los vectores $|v\rangle ,|w\rangle \in V$

$(|v\rangle ,A|w\rangle) = (A^{\dagger}|v\rangle ,|w\rangle). \quad (2.32)$

Este operador lineal se conoce como el adjunto o conjugado hermitiano del operador $A$. A partir de la definición es fácil ver que $(AB)^{\dagger} = B^{\dagger}A^{\dagger}$. Por convención, si $|v\rangle$ es un vector, entonces definimos $|v\rangle^{\dagger} \equiv \langle v|$. Con esta definición no es difícil ver que $(A|v\rangle)^{\dagger} = \langle v|A^{\dagger}$.

===== Página 10 =====

Ejercicio 2.13: Si $|w\rangle$ y $|v\rangle$ son dos vectores cualesquiera, muestra que $(|w\rangle \langle v|)^{\dagger} = |v\rangle \langle w|$.

Ejercicio 2.14: (Antilinealidad del adjunto) Muestra que la operación adjunta es antilineal,

$\left(\sum_{i}a_{i}A_{i}\right)^{\dagger} = \sum_{i}a_{i}^{*}A_{i}^{\dagger}. \quad (2.33)$

Ejercicio 2.15: Muestra que $(A^{\dagger})^{\dagger} = A$.

En una representación matricial de un operador $A$, la acción de la operación de conjugación hermitiana es llevar la matriz de $A$ a la matriz conjugada-transpuesta, $A^{\dagger} \equiv (A^{*})^{T}$, donde el $*$ indica conjugación compleja, y $T$ indica la operación de transposición. Por ejemplo, tenemos

$\left[ \begin{array}{cc}1 + 3i & 2i\\ 1 + i & 1 - 4i \end{array} \right]^{\dagger} = \left[ \begin{array}{cc}1 - 3i & 1 - i\\ -2i & 1 + 4i \end{array} \right]. \quad (2.34)$

Un operador $A$ cuyo adjunto es $A$ se conoce como operador hermítico o autoadjunto. Una clase importante de operadores hermíticos son los proyectores. Supongamos que $W$ es un subespacio vectorial de dimensión $k$ del espacio vectorial de dimensión $d$ $V$. Usando el procedimiento de Gram-Schmidt es posible construir una base ortonormal $|1\rangle , \ldots , |d\rangle$ para $V$ tal que $|1\rangle , \ldots , |k\rangle$ es una base ortonormal para $W$. Por definición,

$P\equiv \sum_{i = 1}^{k}|i\rangle \langle i| \quad (2.35)$

es el proyector sobre el subespacio $W$. Es fácil verificar que esta definición es independiente de la base ortonormal $|1\rangle , \ldots , |k\rangle$ usada para $W$. A partir de la definición se puede demostrar que $|v\rangle \langle v|$ es hermítico para cualquier vector $|v\rangle$, por lo que $P$ es hermítico, $P^{\dagger} = P$. A menudo nos referiremos al 'espacio vectorial' $P$, como abreviatura del espacio vectorial sobre el que $P$ es un proyector. El complemento ortogonal de $P$ es el operador $Q \equiv I - P$. Es fácil ver que $Q$ es un proyector sobre el espacio vectorial generado por $|k + 1\rangle , \ldots , |d\rangle$, al que también nos referimos como el complemento ortogonal de $P$, y podemos denotar por $Q$.

Ejercicio 2.16: Muestra que cualquier proyector $P$ satisface la ecuación $P^{2} = P$.

Se dice que un operador $A$ es normal si $A A^{\dagger} = A^{\dagger}A$. Claramente, un operador que es hermítico también es normal. Hay un notable teorema de representación para operadores normales conocido como la descomposición espectral, que establece que un operador es un operador normal si y solo si es diagonalizable. Este resultado se demuestra en el Recuadro 2.2 en la página 72, que deberías leer detenidamente.

Ejercicio 2.17: Muestra que una matriz normal es hermítica si y solo si tiene valores propios reales.

Se dice que una matriz $U$ es unitaria si $U^{\dagger}U = I$. Similarmente, un operador $U$ es unitario si $U^{\dagger}U = I$. Se verifica fácilmente que un operador es unitario si y solo si cada una de sus representaciones matriciales es unitaria. Un operador unitario también satisface $U U^{\dagger} = I$, y por lo tanto $U$ es normal y tiene una descomposición espectral. Geométricamente, los operadores unitarios son importantes porque preservan los productos internos entre vectores. Para ver esto, sean $|v\rangle$ y $|w\rangle$ cualesquiera

===== Página 11 =====

dos vectores. Entonces el producto interno de $U|v\rangle$ y $U|w\rangle$ es el mismo que el producto interno de $|v\rangle$ y $|w\rangle$

$(U|v\rangle ,U|w\rangle) = \langle v|U^{\dagger}U|w\rangle = \langle v|I|w\rangle = \langle v|w\rangle . \quad (2.36)$

Este resultado sugiere la siguiente elegante representación de producto externo de cualquier unitario $U$. Sea $|v_{i}\rangle$ cualquier conjunto base ortonormal. Define $|w_{i}\rangle \equiv U|v_{i}\rangle$, así $|w_{i}\rangle$ también es un conjunto base ortonormal, ya que los operadores unitarios preservan productos internos. Nótese que $U = \sum_{i}|w_{i}\rangle \langle v_{i}|$. Recíprocamente, si $|v_{i}\rangle$ y $|w_{i}\rangle$ son dos bases ortonormales cualesquiera, entonces es fácil verificar que el operador $U$ definido por $U\equiv \sum_{i}|w_{i}\rangle \langle v_{i}|$ es un operador unitario.

Ejercicio 2.18: Muestra que todos los valores propios de una matriz unitaria tienen módulo 1, es decir, pueden escribirse en la forma $e^{i\theta}$ para algún $\theta$ real.

Ejercicio 2.19: (Matrices de Pauli: hermíticas y unitarias) Muestra que las matrices de Pauli son hermíticas y unitarias.

Ejercicio 2.20: (Cambios de base) Supón que $A^{\prime}$ y $A^{\prime \prime}$ son representaciones matriciales de un operador $A$ en un espacio vectorial $V$ con respecto a dos bases ortonormales diferentes, $|v_{i}\rangle$ y $|w_{i}\rangle$. Entonces los elementos de $A^{\prime}$ y $A^{\prime \prime}$ son $A_{ij}^{\prime} = \langle v_{i}|A|v_{j}\rangle$ y $A_{ij}^{\prime \prime} = \langle w_{i}|A|w_{j}\rangle$. Caracteriza la relación entre $A^{\prime}$ y $A^{\prime \prime}$.

Una subclase especial de operadores hermíticos es extremadamente importante. Estos son los operadores positivos. Un operador positivo $A$ se define como un operador tal que para cualquier vector $|v\rangle$, $(|v\rangle ,A|v\rangle)$ es un número real, no negativo. Si $(|v\rangle ,A|v\rangle)$ es estrictamente mayor que cero para todo $|v\rangle \neq 0$ entonces decimos que $A$ es definido positivo. En el Ejercicio 2.24 en esta página mostrarás que cualquier operador positivo es automáticamente hermítico, y por lo tanto, por la descomposición espectral, tiene representación diagonal $\sum_{i}\lambda_{i}|i\rangle \langle i|$, con valores propios no negativos $\lambda_{i}$.

Ejercicio 2.21: Repite la prueba de la descomposición espectral en el Recuadro 2.2 para el caso en que $M$ es hermítico, simplificando la prueba siempre que sea posible.

Ejercicio 2.22: Demuestra que dos vectores propios de un operador hermítico con diferentes valores propios son necesariamente ortogonales.

Ejercicio 2.23: Muestra que los valores propios de un proyector $P$ son todos 0 o 1.

Ejercicio 2.24: (Hermiticidad de operadores positivos) Muestra que un operador positivo es necesariamente hermítico. (Pista: Muestra que un operador arbitrario $A$ puede escribirse $A = B + iC$ donde $B$ y $C$ son hermíticos.)

Ejercicio 2.25: Muestra que para cualquier operador $A$, $A^{\dagger}A$ es positivo.

#### 2.1.7 Productos tensoriales

El producto tensorial es una forma de unir espacios vectoriales para formar espacios vectoriales más grandes. Esta construcción es crucial para entender la mecánica cuántica de sistemas multipartícula. La siguiente discusión es un poco abstracta, y puede ser difícil de seguir si aún no estás familiarizado con el producto tensorial, así que siéntete libre de saltarla por ahora y volver más tarde cuando llegues a la discusión de productos tensoriales en mecánica cuántica.

Supongamos que $V$ y $W$ son espacios vectoriales de dimensión $m$ y $n$ respectivamente. Por conveniencia también suponemos que $V$ y $W$ son espacios de Hilbert. Entonces $V \otimes W$ (léase '$V$ tensor

===== Página 12 =====

#### 2.2: La descomposición espectral - ¡importante! La descomposición espectral es un teorema de representación extremadamente útil para operadores normales.

Teorema 2.1: (Descomposición espectral) Cualquier operador normal $M$ sobre un espacio vectorial $V$ es diagonal con respecto a alguna base ortonormal para $V$. Recíprocamente, cualquier operador diagonalizable es normal.

## Prueba

El recíproco es un ejercicio simple, así que probamos solo la implicación directa, por inducción sobre la dimensión $d$ de $V$. El caso $d = 1$ es trivial. Sea $\lambda$ un valor propio de $M$, $P$ el proyector sobre el espacio propio de $\lambda$, y $Q$ el proyector sobre el complemento ortogonal. Entonces $M = (P + Q)M(P + Q) = PMP + QMP + PMQ + QMQ$. Obviamente $PMP = \lambda P$. Además, $QMP = 0$, ya que $M$ lleva el subespacio $P$ en sí mismo. Afirmamos que $PMQ = 0$ también. Para ver esto, sea $|v\rangle$ un elemento del subespacio $P$. Entonces $MM^{\dagger}|v\rangle = M^{\dagger}M|v\rangle = \lambda M^{\dagger}|v\rangle$. Así, $M^{\dagger}|v\rangle$ tiene valor propio $\lambda$ y por lo tanto es un elemento del subespacio $P$. Se sigue que $QM^{\dagger}P = 0$. Tomando el adjunto de esta ecuación se obtiene $PMQ = 0$. Así $M = PMP + QMQ$. A continuación, probamos que $QMQ$ es normal. Para ver esto, nótese que $QM = QM(P + Q) = QMQ$, y $QM^{\dagger} = QM^{\dagger}(P + Q) = QM^{\dagger}Q$. Por lo tanto, por la normalidad de $M$, y la observación de que $Q^{2} = Q$,

$\begin{array}{r l} & {Q M Q Q M^{\dagger}Q = Q M Q M^{\dagger}Q}\\ & {\qquad = Q M M^{\dagger}Q}\\ & {\qquad = Q M^{\dagger}M Q}\\ & {\qquad = Q M^{\dagger}Q M Q}\\ & {\qquad = Q M^{\dagger}Q Q M Q,} \end{array} \quad (2.37)$

así que $QMQ$ es normal. Por inducción, $QMQ$ es diagonal con respecto a alguna base ortonormal para el subespacio $Q$, y $PMP$ ya es diagonal con respecto a alguna base ortonormal para $P$. Se sigue que $M = PMP + QMQ$ es diagonal con respecto a alguna base ortonormal para el espacio vectorial total.

En términos de la representación de producto externo, esto significa que $M$ puede escribirse como $M = \sum_{i}\lambda_{i}|i\rangle \langle i|$, donde $\lambda_{i}$ son los valores propios de $M$, $|i\rangle$ es una base ortonormal para $V$, y cada $|i\rangle$ es un vector propio de $M$ con valor propio $\lambda_{i}$. En términos de proyectores, $M = \sum_{i}\lambda_{i}P_{i}$, donde $\lambda_{i}$ son nuevamente los valores propios de $M$, y $P_{i}$ es el proyector sobre el espacio propio $\lambda_{i}$ de $M$. Estos proyectores satisfacen la relación de completitud $\sum_{i}P_{i} = I$, y la relación de ortonormalidad $P_{i}P_{j} = \delta_{ij}P_{i}$.

$W$') es un espacio vectorial de dimensión $mn$. Los elementos de $V\otimes W$ son combinaciones lineales de 'productos tensoriales' $|v\rangle \otimes |w\rangle$ de elementos $|v\rangle$ de $V$ y $|w\rangle$ de $W$. En particular, si $|i\rangle$ y $|j\rangle$ son bases ortonormales para los espacios $V$ y $W$ entonces $|i\rangle \otimes |j\rangle$ es una base para $V\otimes W$. A menudo usamos las notaciones abreviadas $|v\rangle |w\rangle$, $|v,w\rangle$ o incluso $|vw\rangle$ para el producto tensorial

===== Página 13 =====

$|v\rangle \otimes |w\rangle$. Por ejemplo, si $V$ es un espacio vectorial bidimensional con base ortonormal $|0\rangle ,|1\rangle$ (a menudo llamados estados de un *qubit* o *cúbit*), entonces $|0\rangle \otimes |0\rangle +|1\rangle \otimes |1\rangle$ es un elemento de $V\otimes V$.

Por definición, el producto tensorial satisface las siguientes propiedades básicas:

(1) Para un escalar arbitrario $z$ y elementos $|v\rangle$ de $V$ y $|w\rangle$ de $W$

$z\left(|v\rangle \otimes |w\rangle\right) = \left(z|v\rangle\right)\otimes |w\rangle = |v\rangle \otimes \left(z|w\rangle\right). \quad (2.42)$

(2) Para $|v_{1}\rangle$ y $|v_{2}\rangle$ arbitrarios en $V$ y $|w\rangle$ en $W$

$\left(|v_{1}\rangle +|v_{2}\rangle\right)\otimes |w\rangle = |v_{1}\rangle \otimes |w\rangle +|v_{2}\rangle \otimes |w\rangle . \quad (2.43)$

(3) Para $|v\rangle$ arbitrario en $V$ y $|w_{1}\rangle$ y $|w_{2}\rangle$ en $W$

$|v\rangle \otimes \left(|w_{1}\rangle +|w_{2}\rangle\right) = |v\rangle \otimes |w_{1}\rangle +|v\rangle \otimes |w_{2}\rangle . \quad (2.44)$

¿Qué tipo de operadores lineales actúan sobre el espacio $V\otimes W$? Supongamos que $|v\rangle$ y $|w\rangle$ son vectores en $V$ y $W$, y $A$ y $B$ son operadores lineales sobre $V$ y $W$, respectivamente. Entonces podemos definir un operador lineal $A\otimes B$ sobre $V\otimes W$ mediante la ecuación

$(A\otimes B)(|v\rangle \otimes |w\rangle)\equiv A|v\rangle \otimes B|w\rangle . \quad (2.45)$

La definición de $A\otimes B$ se extiende entonces a todos los elementos de $V\otimes W$ de la manera natural para asegurar la linealidad de $A\otimes B$, es decir,

$(A\otimes B)\left(\sum_{i}a_{i}|v_{i}\rangle \otimes |w_{i}\rangle\right)\equiv \sum_{i}a_{i}A|v_{i}\rangle \otimes B|w_{i}\rangle . \quad (2.46)$

Puede demostrarse que $A\otimes B$ definido de esta manera es un operador lineal bien definido sobre $V\otimes W$. Esta noción del producto tensorial de dos operadores se extiende de manera obvia al caso donde $A:V\to V^{\prime}$ y $B:W\to W^{\prime}$ mapean entre espacios vectoriales diferentes. De hecho, un operador lineal arbitrario $C$ que mapea $V\otimes W$ a $V^{\prime}\otimes W^{\prime}$ puede representarse como una combinación lineal de productos tensoriales de operadores que mapean $V$ a $V^{\prime}$ y $W$ a $W^{\prime}$,

$C = \sum_{i}c_{i}A_{i}\otimes B_{i}, \quad (2.47)$

donde por definición

$\left(\sum_{i}c_{i}A_{i}\otimes B_{i}\right)|v\rangle \otimes |w\rangle \equiv \sum_{i}c_{i}A_{i}|v\rangle \otimes B_{i}|w\rangle . \quad (2.48)$

Los productos internos en los espacios $V$ y $W$ pueden usarse para definir un producto interno natural en $V\otimes W$. Define

$\left(\sum_{i}a_{i}|v_{i}\rangle \otimes |w_{i}\rangle ,\sum_{j}b_{j}|v_{j}^{\prime}\rangle \otimes |w_{j}^{\prime}\rangle\right)\equiv \sum_{ij}a_{i}^{*}b_{j}\langle v_{i}|v_{j}^{\prime}\rangle \langle w_{i}|w_{j}^{\prime}\rangle . \quad (2.49)$

Puede demostrarse que la función así definida es un producto interno bien definido. A partir de este producto interno, el espacio con producto interno $V\otimes W$ hereda la otra estructura que conocemos, como nociones de adjunto, unitariedad, normalidad y hermiticidad.

Toda esta discusión es bastante abstracta. Puede hacerse mucho más concreta al pasar

===== Página 14 =====

**74 Introducción a la mecánica cuántica**

a una representación matricial conveniente conocida como producto de Kronecker. Supongamos que $A$ es una matriz de $m$ por $n$, y $B$ es una matriz de $p$ por $q$. Entonces tenemos la representación matricial:

$A\otimes B\equiv \left[ \begin{array}{cccc}{A_{11}B} & {A_{12}B} & \ldots & {A_{1n}B}\\ {A_{21}B} & {A_{22}B} & \ldots & {A_{2n}B}\\ \vdots & \vdots & \ddots & \vdots \\ {A_{m1}B} & {A_{m2}B} & \ldots & {A_{mn}B} \end{array} \right]_{mp \times nq}. \quad (2.50)$

En esta representación, términos como $A_{11}B$ denotan submatrices de $p$ por $q$ cuyas entradas son proporcionales a $B$, con constante de proporcionalidad general $A_{11}$. Por ejemplo, el producto tensorial de los vectores $(1,2)$ y $(2,3)$ es el vector

$\left[ \begin{array}{c}1\\ 2 \end{array} \right]\otimes \left[ \begin{array}{c}2\\ 3 \end{array} \right] = \left[ \begin{array}{c}1\times 2\\ 1\times 3\\ 2\times 2\\ 2\times 3 \end{array} \right] = \left[ \begin{array}{c}2\\ 3\\ 4\\ 6 \end{array} \right]. \quad (2.51)$

El producto tensorial de las matrices de Pauli $X$ y $Y$ es

$X\otimes Y = \left[ \begin{array}{ll}0\cdot Y & 1\cdot Y\\ 1\cdot Y & 0\cdot Y \end{array} \right] = \left[ \begin{array}{llll}0 & 0 & 0 & -i\\ 0 & 0 & i & 0\\ 0 & -i & 0 & 0\\ i & 0 & 0 & 0 \end{array} \right]. \quad (2.52)$

Finalmente, mencionamos la notación útil $|\psi \rangle^{\otimes k}$, que significa $|\psi \rangle$ tensado consigo mismo $k$ veces. Por ejemplo $|\psi \rangle^{\otimes 2} = |\psi \rangle \otimes |\psi \rangle$. Se usa una notación análoga también para operadores sobre espacios de producto tensorial.

Ejercicio 2.26: Sea $|\psi \rangle = (|0\rangle +|1\rangle) / \sqrt{2}$. Escribe explícitamente $|\psi \rangle^{\otimes 2}$ y $|\psi \rangle^{\otimes 3}$, tanto en términos de productos tensoriales como $|0\rangle |1\rangle$, como usando el producto de Kronecker.

Ejercicio 2.27: Calcula la representación matricial del producto tensorial de los operadores de Pauli (a) $X$ y $Z$; (b) $I$ y $X$; (c) $X$ y $I$. ¿Es conmutativo el producto tensorial?

Ejercicio 2.28: Muestra que las operaciones de transposición, conjugación compleja y adjunto se distribuyen sobre el producto tensorial,

$(A\otimes B)^{*} = A^{*}\otimes B^{*};(A\otimes B)^{T} = A^{T}\otimes B^{T};(A\otimes B)^{\dagger} = A^{\dagger}\otimes B^{\dagger}. \quad (2.53)$

Ejercicio 2.29: Muestra que el producto tensorial de dos operadores unitarios es unitario.

Ejercicio 2.30: Muestra que el producto tensorial de dos operadores hermíticos es hermítico.

Ejercicio 2.31: Muestra que el producto tensorial de dos operadores positivos es positivo.

Ejercicio 2.32: Muestra que el producto tensorial de dos proyectores es un proyector.

Ejercicio 2.33: El operador de Hadamard en un cúbit puede escribirse como

$H = \frac{1}{\sqrt{2}}\left[(|0\rangle +|1\rangle)\langle 0| + (|0\rangle -|1\rangle)\langle 1| \right]. \quad (2.54)$

===== Página 15 =====

Muestra explícitamente que la transformada de Hadamard en $n$ cúbits, $H^{\otimes n}$, puede escribirse como

$H^{\otimes n} = \frac{1}{\sqrt{2^n}}\sum_{x,y}(-1)^{x\cdot y}|x\rangle \langle y|. \quad (2.55)$

Escribe una representación matricial explícita para $H^{\otimes 2}$.

#### 2.1.8 Funciones de operadores

Hay muchas funciones importantes que pueden definirse para operadores y matrices. En general, dada una función $f$ de los números complejos a los números complejos, es posible definir una función matricial correspondiente en matrices normales (o alguna subclase, como las matrices hermíticas) mediante la siguiente construcción. Sea $A = \sum_{a}a|a\rangle \langle a|$ una descomposición espectral para un operador normal $A$. Define $f(A)\equiv \sum_{a}f(a)|a\rangle \langle a|$. Un poco de reflexión muestra que $f(A)$ está definido de forma única. Este procedimiento puede usarse, por ejemplo, para definir la raíz cuadrada de un operador positivo, el logaritmo de un operador definido positivo, o la exponencial de un operador normal. Como ejemplo,

$\exp (\theta Z) = \left[ \begin{array}{cc}e^{\theta} & 0\\ 0 & e^{-\theta} \end{array} \right], \quad (2.56)$

ya que $Z$ tiene vectores propios $|0\rangle$ y $|1\rangle$.

Ejercicio 2.34: Encuentra la raíz cuadrada y el logaritmo de la matriz

$\left[ \begin{array}{cc}4 & 3\\ 3 & 4 \end{array} \right]. \quad (2.57)$

Ejercicio 2.35: (Exponencial de las matrices de Pauli) Sea $\vec{v}$ cualquier vector unitario real tridimensional y $\theta$ un número real. Demuestra que

$\exp (i\theta \vec{v}\cdot \vec{\sigma}) = \cos (\theta)I + i\sin (\theta)\vec{v}\cdot \vec{\sigma}, \quad (2.58)$

donde $\vec{v}\cdot \vec{\sigma}\equiv \sum_{i = 1}^{3}v_{i}\sigma_{i}$. Este ejercicio se generaliza en el Problema 2.1 en la página 117.

Otra función matricial importante es la traza de una matriz. La traza de $A$ se define como la suma de sus elementos diagonales,

$\operatorname {tr}(A)\equiv \sum_{i}A_{ii}. \quad (2.59)$

Se ve fácilmente que la traza es cíclica, $\operatorname {tr}(AB) = \operatorname {tr}(BA)$, y lineal, $\operatorname {tr}(A + B) = \operatorname {tr}(A) + \operatorname {tr}(B)$, $\operatorname {tr}(zA) = z\operatorname {tr}(A)$, donde $A$ y $B$ son matrices arbitrarias, y $z$ es un número complejo. Además, de la propiedad cíclica se sigue que la traza de una matriz es invariante bajo la transformación de similitud unitaria $A\to UAU^{\dagger}$, ya que $\operatorname {tr}(UAU^{\dagger}) = \operatorname {tr}(U^{\dagger}UA) = \operatorname {tr}(A)$. A la luz de este resultado, tiene sentido definir la traza de un operador $A$ como la traza de cualquier representación matricial de $A$. La invariancia de la traza bajo transformaciones de similitud unitarias asegura que la traza de un operador está bien definida.

Como ejemplo de la traza, supongamos que $|\psi \rangle$ es un vector unitario y $A$ es un operador arbitrario. Para evaluar $\operatorname {tr}(A|\psi \rangle \langle \psi |)$ usa el procedimiento de Gram-Schmidt para extender $|\psi \rangle$ a una

===== Página 16 =====

base ortogonal $|i\rangle$ que incluya $|\psi \rangle$ como primer elemento. Entonces tenemos

$\mathrm{tr}(A|\psi \rangle \langle \psi |) = \sum_{i}\langle i|A|\psi \rangle \langle \psi |i\rangle$ $= \langle \psi |A|\psi \rangle .$

Este resultado, que $\mathrm{tr}(A|\psi \rangle \langle \psi |) = \langle \psi |A|\psi \rangle$ es extremadamente útil para evaluar la traza de un operador.

Ejercicio 2.36: Muestra que las matrices de Pauli, excepto $I$, tienen traza cero.

Ejercicio 2.37: (Propiedad cíclica de la traza) Si $A$ y $B$ son dos operadores lineales, muestra que

$\mathrm{tr}(AB) = \mathrm{tr}(BA). \quad (2.62)$

Ejercicio 2.38: (Linealidad de la traza) Si $A$ y $B$ son dos operadores lineales, muestra que

$\mathrm{tr}(A + B) = \mathrm{tr}(A) + \mathrm{tr}(B) \quad (2.63)$

y si $z$ es un número complejo arbitrario, muestra que

$\mathrm{tr}(zA) = z\mathrm{tr}(A). \quad (2.64)$

Ejercicio 2.39: (El producto interno de Hilbert-Schmidt sobre operadores) El conjunto $L_{V}$ de operadores lineales sobre un espacio de Hilbert $V$ es obviamente un espacio vectorial: la suma de dos operadores lineales es un operador lineal, $zA$ es un operador lineal si $A$ es un operador lineal y $z$ es un número complejo, y hay un elemento cero 0. Un resultado adicional importante es que al espacio vectorial $L_{V}$ puede dársele una estructura natural de producto interno, convirtiéndolo en un espacio de Hilbert.

(1) Muestra que la función $(\cdot ,\cdot)$ sobre $L_{V}\times L_{V}$ definida por

$(A,B)\equiv \mathrm{tr}(A^{\dagger}B) \quad (2.65)$

es una función producto interno. Este producto interno se conoce como producto interno de Hilbert-Schmidt o de traza.

(2) Si $V$ tiene $d$ dimensiones, muestra que $L_{V}$ tiene dimensión $d^{2}$.

(3) Encuentra una base ortonormal de matrices hermíticas para el espacio de Hilbert $L_{V}$.

#### 2.1.9 El conmutador y el anticonmutador

El conmutador entre dos operadores $A$ y $B$ se define como

$[A,B]\equiv AB - BA. \quad (2.66)$

Si $[A,B] = 0$, es decir, $AB = BA$, entonces decimos que $A$ conmuta con $B$. Similarmente, el anticonmutador de dos operadores $A$ y $B$ se define por

$\{A,B\} \equiv AB + BA; \quad (2.67)$

decimos que $A$ anticonmuta con $B$ si $\{A,B\} = 0$. Resulta que muchas propiedades importantes de pares de operadores pueden deducirse de su conmutador y anticonmutador. Quizás la relación más útil es la siguiente conexión entre el conmutador y la propiedad de poder diagonalizar simultáneamente los operadores hermíticos $A$ y $B$,

===== Página 17 =====

que se establece en el siguiente teorema, y cuya prueba se deja como ejercicio.

Teorema 2.2: (Conmutación y diagonalización simultánea) Supongamos que $A$ y $B$ son operadores hermíticos. Entonces $[A,B] = 0$ si y solo si existe una base ortonormal tal que tanto $A$ como $B$ son diagonales con respecto a esa base. Decimos que $A$ y $B$ son simultáneamente diagonalizables en este caso.

Esta conexión entre conmutación y diagonalización simultánea es muy poderosa. Es sencillo probar el teorema en una dirección: si $A$ y $B$ son diagonalizables en la misma base, entonces ciertamente conmutan. Para probar la otra dirección, uno puede construir una base ortonormal de vectores propios comunes, lo que requiere un poco más de trabajo.

Ejercicio 2.40: (Relaciones de conmutación para las matrices de Pauli) Verifica las relaciones de conmutación para las matrices de Pauli. Estas relaciones pueden resumirse de manera compacta como

$[\sigma_{j},\sigma_{k}] = 2i\epsilon_{jkl}\sigma_{l} \quad (2.73)$

o, escribiendo explícitamente la suma sobre el índice $l$,

$[\sigma_{j},\sigma_{k}] = 2i\sum_{l = 1}^{3}\epsilon_{jkl}\sigma_{l}. \quad (2.74)$

Aquí, $\epsilon_{jkl}$ es el símbolo de Levi-Civita, totalmente antisimétrico en sus tres índices, para el cual $\epsilon_{jkl} = 0$ excepto para $\epsilon_{123} = \epsilon_{231} = \epsilon_{312} = 1$, y $\epsilon_{321} = \epsilon_{213} = \epsilon_{132} = -1$.

Ejercicio 2.41: (Relaciones de anticonmutación para las matrices de Pauli) Verifica las relaciones de anticonmutación

$\{\sigma_{i},\sigma_{j}\} = 0 \quad (2.75)$

donde $i\neq j$ se eligen ambos del conjunto 1, 2, 3. También verifica que (para $i = 0,1,2,3$)

$\sigma_{i}^{2} = I. \quad (2.76)$

Ejercicio 2.42: Verifica que

$A B = \frac{[A,B] + \{A,B\}}{2}. \quad (2.77)$

Ejercicio 2.43: Muestra que para $j,k = 1,2,3$

$\sigma_{j}\sigma_{k} = \delta_{jk}I + i\sum_{l = 1}^{3}\epsilon_{jkl}\sigma_{l}. \quad (2.78)$

Ejercicio 2.44: Supón que $[A,B] = 0,\{A,B\} = 0$, y $A$ es invertible. Muestra que $B$ debe ser 0.

Ejercicio 2.45: Muestra que $[A,B]^{\dagger} = [B^{\dagger},A^{\dagger}]$.

Ejercicio 2.46: Muestra que $[A,B] = - [B,A]$.

Ejercicio 2.47: Supón que $A$ y $B$ son hermíticos. Muestra que $i[A,B]$ es hermítico.

#### 2.1.10 Las descomposiciones polar y de valores singulares

Las descomposiciones polar y de valores singulares son formas útiles de descomponer operadores lineales en partes más simples. En particular, estas descomposiciones nos permiten descomponer operadores lineales generales en productos de operadores unitarios y operadores positivos. Si bien no entendemos terriblemente bien la estructura de los operadores lineales generales, sí entendemos los operadores unitarios y positivos con bastante detalle. Las descomposiciones polar y de valores singulares nos permiten aplicar este entendimiento para comprender mejor los operadores lineales generales.

Teorema 2.3: (Descomposición polar) Sea $A$ un operador lineal sobre un espacio vectorial $V$. Entonces existen un operador unitario $U$ y operadores positivos $J$ y $K$ tales que

$A = UJ = KU, \quad (2.79)$

donde los operadores positivos únicos $J$ y $K$ que satisfacen estas ecuaciones están definidos por $J\equiv \sqrt{A^{\dagger}A}$ y $K\equiv \sqrt{A A^{\dagger}}$. Además, si $A$ es invertible, entonces $U$ es único.


Llamamos a la expresión $A = UJ$ la descomposición polar izquierda de $A$, y a $A = KU$ la descomposición polar derecha de $A$. La mayoría de las veces, omitiremos la nomenclatura 'derecha' o 'izquierda', y usaremos el término 'descomposición polar' para ambas expresiones, indicando el contexto cuál se quiere decir.

**Prueba**

$J\equiv \sqrt{A^{\dagger}A}$ es un operador positivo, por lo que puede dársele una descomposición espectral, $J =$ $\sum_{i}\lambda_{i}|i\rangle \langle i|(\lambda_{i}\geq 0)$. Define $|\psi_{i}\rangle \equiv A|i\rangle$. De la definición, vemos que $\langle \psi_{i}|\psi_{i}\rangle = \lambda_{i}^{2}$. Consideremos por ahora solo aquellos $i$ para los cuales $\lambda_{i}\neq 0$. Para esos $i$, define $|e_{i}\rangle \equiv |\psi_{i}\rangle /\lambda_{i}$, así los $|e_{i}\rangle$ están normalizados. Además, son ortogonales, ya que si $i\neq j$ entonces $\langle e_{i}|e_{j}\rangle =$ $\langle i|A^{\dagger}A|j\rangle /\lambda_{i}\lambda_{j} = \langle i|J^{2}|j\rangle /\lambda_{i}\lambda_{j} = 0$.

Hemos estado considerando $i$ tal que $\lambda_{i}\neq 0$. Ahora usa el procedimiento de Gram-Schmidt para extender el conjunto ortonormal $|e_{i}\rangle$ de modo que forme una base ortonormal, que también etiquetamos $|e_{i}\rangle$. Define un operador unitario $U\equiv \sum_{i}|e_{i}\rangle \langle i|$. Cuando $\lambda_{i}\neq 0$ tenemos $UJ|i\rangle = \lambda_{i}|e_{i}\rangle =$ $|\psi_{i}\rangle = A|i\rangle$. Cuando $\lambda_{i} = 0$ tenemos $UJ|i\rangle = 0 = |\psi_{i}\rangle$. Hemos probado que la acción de $A$ y $UJ$ coinciden en la base $|i\rangle$, y por lo tanto que $A = UJ$.

$J$ es único, ya que multiplicando $A = UJ$ a la izquierda por la ecuación adjunta $A^{\dagger} = JU^{\dagger}$ da $J^{2} = A^{\dagger}A$, de lo cual vemos que $J = \sqrt{A^{\dagger}A}$, de forma única. Un poco de reflexión muestra que si $A$ es invertible, entonces también lo es $J$, así que $U$ está determinado de manera única por la ecuación $U = AJ^{- 1}$. La prueba de la descomposición polar derecha se sigue, ya que $A = UJ = UJ U^{\dagger}U = KU$, donde $K\equiv UJ U^{\dagger}$ es un operador positivo. Dado que $AA^{\dagger} = KU U^{\dagger}K = K^{2}$ debemos tener $K = \sqrt{AA^{\dagger}}$, como se afirmó. $\square$

La descomposición de valores singulares combina la descomposición polar y el teorema espectral.

Corolario 2.4: (Descomposición de valores singulares) Sea $A$ una matriz cuadrada. Entonces existen matrices unitarias $U$ y $V$, y una matriz diagonal $D$ con entradas no negativas tales que

$A = UDV. \quad (2.80)$

Los elementos diagonales de $D$ se llaman los valores singulares de $A$.

**Prueba**

Por la descomposición polar, $A = SJ$, para $S$ unitaria, y $J$ positiva. Por el teorema espectral, $J = TDT^{\dagger}$, para $T$ unitaria y $D$ diagonal con entradas no negativas. Haciendo $U\equiv ST$ y $V\equiv T^{\dagger}$ se co$leta la prueba. $\square$

Ejercicio 2.48: ¿Cuál es la descomposición polar de una matriz positiva $P$? ¿De una matriz unitaria $U$? ¿De una matriz hermítica $H$?

Ejercicio 2.49: Expresa la descomposición polar de una matriz normal en la representación de producto externo.

Ejercicio 2.50: Encuentra las descomposiciones polares izquierda y derecha de la matriz

---
---
# Soluciones 

Aquí tienes las soluciones detalladas, paso a paso y utilizando el formalismo del álgebra lineal avanzada (notación de Dirac y descomposición espectral cuando es pertinente), basadas en los teoremas proporcionados.

---

### Ejercicio 2.48: Casos Especiales de Descomposición Polar

**Objetivo:** Encontrar $U$ y $J$ (para la izquierda $A=UJ$) en casos específicos. Según el Teorema 2.3, $J \equiv \sqrt{A^\dagger A}$.

#### 1. Descomposición de una Matriz Positiva $P$

Sea $A = P$, donde $P$ es un operador positivo (por definición, hermítico $P=P^\dagger$ y con valores propios no negativos).

- **Paso 1: Calcular $J$.**
    
    Utilizamos la definición dada:
    
    $$J = \sqrt{A^\dagger A} = \sqrt{P^\dagger P}$$
    
    Como $P$ es hermítica, $P^\dagger = P$, entonces:
    
    $$J = \sqrt{P^2}$$
    
    Dado que $P$ es positivo, la raíz cuadrada única positiva de $P^2$ es simplemente $P$.
    
    $$\Rightarrow J = P$$
    
- **Paso 2: Determinar $U$.**
    
    Sustituimos en la ecuación $A = UJ$:
    
    $$P = U P$$
    
    Si $P$ es invertible, multiplicamos por $P^{-1}$ por la derecha: $I = U$.
    
    Si $P$ no es invertible, $U$ puede ser cualquier operador que actúe como la identidad en el rango de $P$. La elección canónica más simple es la identidad.
    
    $$\Rightarrow U = I$$
    
- **Resultado:** $P = I \cdot P$ (donde $U=I, J=P$).
    

#### 2. Descomposición de una Matriz Unitaria $V$

Sea $A = V$, donde $V$ es unitaria ($V^\dagger V = I$).

- **Paso 1: Calcular $J$.**
    
    $$J = \sqrt{V^\dagger V} = \sqrt{I} = I$$
    
    El operador positivo asociado es la Identidad.
    
- **Paso 2: Determinar $U$.**
    
    Sustituimos en $A = UJ$:
    
    $$V = U \cdot I \implies U = V$$
    
- **Resultado:** $V = V \cdot I$ (donde la parte unitaria es la misma matriz y la parte positiva es la identidad).
    

#### 3. Descomposición de una Matriz Hermítica $H$

Sea $A = H$, donde $H$ es hermítica ($H = H^\dagger$). Nota: $H$ puede tener valores propios negativos.

- **Paso 1: Descomposición Espectral de $H$.**
    
    $$H = \sum_k \lambda_k |k\rangle\langle k|$$
    
    Donde $\lambda_k \in \mathbb{R}$ son los valores propios y $|k\rangle$ los vectores propios ortonormales.
    
- **Paso 2: Calcular $J = \sqrt{H^\dagger H}$.**
    
    $$H^\dagger H = H^2 = \sum_k \lambda_k^2 |k\rangle\langle k|$$
    
    Tomando la raíz cuadrada positiva:
    
    $$J = \sqrt{H^2} = \sum_k |\lambda_k| |k\rangle\langle k|$$
    
    Es decir, $J$ es la matriz que contiene los valores absolutos de los valores propios de $H$.
    
- **Paso 3: Determinar $U$.**
    
    Queremos $H = UJ$. Proyectando sobre la base propia:
    
    $$\lambda_k |k\rangle = U (|\lambda_k| |k\rangle) = |\lambda_k| U |k\rangle$$
    
    - Si $\lambda_k > 0$, entonces $|\lambda_k| = \lambda_k$, lo que implica $U|k\rangle = |k\rangle$.
        
    - Si $\lambda_k < 0$, entonces $|\lambda_k| = -\lambda_k$, lo que implica $U|k\rangle = -|k\rangle$.
        
    - Si $\lambda_k = 0$, $U$ es arbitrario en ese subespacio (podemos elegir 1).
        
    
    Por lo tanto, $U$ es una matriz diagonal de signos:
    
    $$U = \sum_k \text{sgn}(\lambda_k) |k\rangle\langle k|$$
    
    Donde $\text{sgn}(x) = 1$ si $x \ge 0$ y $-1$ si $x < 0$.
    

---

### Ejercicio 2.49: Descomposición Polar de una Matriz Normal

**Contexto:** Una matriz $A$ es normal si $[A, A^\dagger] = 0$. Por el Teorema Espectral para matrices normales, $A$ puede ser diagonalizada por una matriz unitaria.

**Representación de Producto Externo:**

Sea la descomposición espectral de $A$:

$$A = \sum_k \lambda_k |k\rangle\langle k|$$

Donde $\lambda_k \in \mathbb{C}$ son los valores propios complejos.

**Solución Paso a Paso:**

1. **Forma Polar de los Valores Propios:**
    
    Expresamos cada valor propio complejo $\lambda_k$ en su forma polar escalar:
    
    $$\lambda_k = r_k e^{i\theta_k}$$
    
    Donde $r_k = |\lambda_k| \ge 0$ (magnitud) y $\theta_k \in [0, 2\pi)$ (fase).
    
2. **Construcción de $J$ (Parte Positiva):**
    
    $$J = \sqrt{A^\dagger A} = \sqrt{\left(\sum_k \bar{\lambda}_k |k\rangle\langle k|\right)\left(\sum_j \lambda_j |j\rangle\langle j|\right)}$$
    
    Por ortonormalidad $\langle k|j \rangle = \delta_{kj}$:
    
    $$J = \sqrt{\sum_k |\lambda_k|^2 |k\rangle\langle k|} = \sum_k |\lambda_k| |k\rangle\langle k| = \sum_k r_k |k\rangle\langle k|$$
    
3. **Construcción de $U$ (Parte Unitaria):**
    
    Necesitamos $A = UJ$. Observando la estructura de $A$:
    
    $$A = \sum_k (r_k e^{i\theta_k}) |k\rangle\langle k| = \left( \sum_k e^{i\theta_k} |k\rangle\langle k| \right) \left( \sum_k r_k |k\rangle\langle k| \right)$$
    
    Identificamos el primer factor como $U$:
    
    $$U = \sum_k e^{i\theta_k} |k\rangle\langle k|$$
    

**Resultado Final:**

La descomposición polar de una matriz normal $A$ es:

$$J = \sum_k |\lambda_k| |k\rangle\langle k|, \quad U = \sum_k e^{i\arg(\lambda_k)} |k\rangle\langle k|$$

_(Nota: Para matrices normales, las descomposiciones izquierda y derecha son idénticas porque $U$ y $J$ conmutan)._

---

### Ejercicio 2.50: Descomposición Polar de una Matriz $A$

**Nota Importante:** En tu solicitud, el texto del Ejercicio 2.50 se cortó y no incluiste la matriz específica. Sin embargo, para cumplir con la instrucción de resolverlo de forma "AVANZADA", presentaré el **Algoritmo General Riguroso** para encontrar dicha descomposición para cualquier matriz cuadrada invertible $A$.

Supongamos que la matriz es $A$. Buscamos $A = UJ$ (izquierda) y $A = KU$ (derecha).

#### Procedimiento Paso a Paso

1. **Calcular $J$ (Matriz Positiva Derecha):**
    
    - Calcula la matriz hermítica: $M = A^\dagger A$.
        
    - Diagonaliza $M$ para encontrar sus valores propios ($\sigma_i^2$) y vectores propios ($|v_i\rangle$). Como $M$ es positiva definida, $\sigma_i^2 \ge 0$.
        
    - Calcula la raíz cuadrada tomando la raíz de los valores propios:
        
        $$J = \sqrt{A^\dagger A} = \sum_i \sigma_i |v_i\rangle\langle v_i|$$
        
        (Donde $\sigma_i$ son los **valores singulares** de $A$).
        
2. **Calcular $U$ (Matriz Unitaria):**
    
    - Del teorema $A = UJ$, si $A$ es invertible, entonces $J$ es invertible.
        
    - Despejamos $U$:
        
        $$U = A J^{-1}$$
        
    - Si $A$ no fuera invertible, se utiliza la Descomposición en Valores Singulares (SVD). Si $A = V D W^\dagger$, entonces $U = V W^\dagger$.
        
3. **Calcular $K$ (Matriz Positiva Izquierda):**
    
    - Podemos calcularla directamente como $K = \sqrt{A A^\dagger}$.
        
    - O, más sencillamente, usando la relación de similitud con $J$ a través de $U$:
        
        $$A = KU \quad \text{y} \quad A = UJ$$
        
        $$UJ = KU \implies K = U J U^\dagger$$
        
    - Esto significa que $K$ tiene los mismos valores propios que $J$ (los valores singulares de $A$), pero sus vectores propios están rotados por $U$.
        

---

**¿Deseas que resuelva el Ejercicio 2.50 para una matriz específica (como la matriz de cizalla $\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$ o la matriz de Pauli)? Si me proporcionas la matriz, aplicaré este algoritmo numéricamente.**

**Problema 3.1:** El siguiente problema esboza una construcción más elaborada que logra una cota superior de $O(\log^2(1/\epsilon) \log^c (\log(1/\epsilon)))$ en el número de compuertas requeridas para aproximar con error $\epsilon$ una compuerta objetivo deseada, para cualquier $c > 2$.

1.  Supón que $\mathcal{N}$ es una $\delta$-red en $S_\epsilon$, para $0 < \delta < \epsilon \leq \epsilon_0$, con $\epsilon_0$ suficientemente pequeño. Demuestra que $[\mathcal{N}, \mathcal{N}]_{\text{gp}}$ es una $d\delta \epsilon$-red en $S_{\epsilon^2}$, para alguna constante $d$.

2.  Supón que $\mathcal{G}_l$ es una $\delta$-red en $S_\epsilon$, para $0 < \delta < \epsilon \leq \epsilon_0$. Demuestra que $\mathcal{G}_{4^k l}$ es una $d^k \delta \epsilon^{2^k - 1}$-red en $S_{\epsilon^{2^k}}$.

3.  Supón que definimos $k$ como
    $$k \equiv \left\lceil \log \left( \frac{\log(1/\epsilon)}{\log(1/\epsilon_0)} \right) \right\rceil,$$
    y supón que podemos encontrar un $l$ tal que $\mathcal{G}_l$ es una $\delta_0$-red para $S_{\epsilon_0}$, donde
    $$d^k \delta_0 = \epsilon_0. \tag{A3.24}$$
    Demuestra que $\mathcal{G}_{4^k l}$s una $\epsilon$-red para $S_{\epsilon_0^{2^k}}$.

4.  Usa la versión ya demostrada del teorema de Solovay–Kitaev para mostrar que elegir $l = O(k^c)$ es suficiente en la parte anterior de este problema, donde $c = \log(5)/\log(3/2)$ es la constante que aparece en el exponente en la versión ya demostrada del teorema de Solovay–Kitaev.

5.  Combina los resultados anteriores para probar que se pueden usar $O(\log^2(1/\epsilon) \log^c (\log(1/\epsilon)))$ compuertas para $\epsilon$-aproximar una compuerta arbitraria en $SU(2)$.

6.  Demuestra que cualquier $c > 2$ puede aparecer en la conclusión del resultado anterior.

# SOLUCION



