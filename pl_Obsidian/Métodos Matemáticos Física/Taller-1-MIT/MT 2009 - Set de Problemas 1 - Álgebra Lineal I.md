# Métodos Matemáticos (Segundo Año) 

## A. Espacios Vectoriales Lineales, Independencia Lineal, Dimensión, Bases

1. Muestre que el espacio de matrices $2 \times 2$ es un espacio vectorial lineal. ¿Cuál es su dimensión? Dé una base para este espacio.

2. ¿Cuál es la dimensión del espacio de matrices $n \times n$? Dé una base para este espacio.

3. ¿Cuál es la dimensión del espacio de matrices $n \times n$ cuyos componentes son todos cero excepto posiblemente los componentes diagonales?

4. ¿Cuál es la dimensión del espacio de matrices simétricas $2 \times 2$, es decir, matrices $2 \times 2$ tales que $A = A^T$ (recuerde que la matriz transpuesta se define por $(A^T)_{ij} = A_{ji}$)? Exhiba una base para este espacio.

5. Considere el espacio vectorial de todas las funciones de una variable $t$. Muestre que los siguientes pares de funciones son linealmente independientes:
   (a) $1$, $t$  
   (b) $t$, $t^2$  
   (c) $e^t$, $t$  
   (d) $\sin(t)$, $\cos(t)$

6. ¿Cuáles son las coordenadas de la función $f(t) = 3\sin(t) + 5\cos(t)$ con respecto a la base $\{\sin(t), \cos(t)\}$?

7. ¿Cuáles son las dimensiones de los espacios vectoriales generados por los siguientes conjuntos de vectores (se dan en forma cartesiana)?
   (a) $\{(1, 1)^T, (1, 2)^T\}$  
   (b) $\{(1, 0)^T, (1, 0)^T\}$  
   (c) $\{(1, 1, 2)^T, (-2, 0, 1)^T, (-1, 1, 3)^T\}$  
   (d) $\{(1, 1, 1, 1)^T, (1, -1, 1, -1)^T, (1, 1, -1, -1)^T, (1, -1, -1, 1)^T\}$  
   (e) $\{(1, 2, 3)^T, (1, -2, 1)^T, (3, 0, 2)^T, (4, 5, 6)^T\}$  
   
   Si el número de vectores es mayor que la dimensión, elija algunos de ellos para formar un conjunto de vectores base y exprese los vectores restantes como combinaciones lineales de ellos. ¿Cuáles de las bases son ortogonales?

## B. Producto Escalar, Ortogonalidad

8. Pruebe la Desigualdad del Triángulo: dada una norma $\|\mathbf{a}\rangle\| = \sqrt{\langle\mathbf{a}|\mathbf{a}\rangle}$ definida a través del producto escalar $\langle\cdot|\cdot\rangle$, tenemos para cualesquiera dos vectores $\|\mathbf{v}\rangle$ y $\|\mathbf{w}\rangle$ en un espacio vectorial lineal:
   $$
   \|\mathbf{v}\rangle + \mathbf{w}\rangle\| \leq \|\mathbf{v}\rangle\| + \|\mathbf{w}\rangle\|
   $$

9. Sean $\tilde{\mathbf{a}}_1, \ldots, \tilde{\mathbf{a}}_n$ vectores en $\mathbb{R}^n$ y suponga que son mutuamente perpendiculares (es decir, cualesquiera dos de ellos son perpendiculares) y ninguno de ellos es igual a $\mathbf{0}$. Pruebe que son linealmente independientes.

10. Encuentre valores reales $\alpha$ y $\beta$ tales que los vectores complejos $\mathbf{u} = \alpha\begin{pmatrix} 1+i \\ 1-i \end{pmatrix}$ y $\mathbf{v} = \beta\begin{pmatrix} 1-i \\ 1+i \end{pmatrix}$ estén normalizados. ¿Cuál es el valor del producto escalar $\mathbf{u}^\dagger \cdot \mathbf{v}$? Pruebe que $\mathbf{u}$ y $\mathbf{v}$ son linealmente independientes. ¿Hay otros vectores complejos bidimensionales linealmente independientes? Si es así, encuentre los vectores necesarios para hacer una base ortogonal. Exprese el vector $\begin{pmatrix} 1 \\ i \end{pmatrix}$ como combinación lineal de los vectores base.

11. Construya un tercer vector que sea ortogonal a los siguientes pares y normalice los tres vectores:
    (a) $\begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$, $\begin{pmatrix} -1 \\ -1 \\ 1 \end{pmatrix}$  
    (b) $\begin{pmatrix} 1+i\sqrt{3} \\ 2 \\ 1-i\sqrt{3} \end{pmatrix}$, $\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}$  
    (c)* $\begin{pmatrix} 1-i \\ 1 \\ 3i \end{pmatrix}$, $\begin{pmatrix} 1+2i \\ 2 \\ 1 \end{pmatrix}$

12. Usando el procedimiento de Schmidt construya un conjunto ortonormal de vectores a partir de los siguientes:
    $$
    \tilde{\mathbf{x}}_1 = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 1 \end{pmatrix}, \tilde{\mathbf{x}}_2 = \begin{pmatrix} 1 \\ 0 \\ -1 \\ 0 \end{pmatrix}, \tilde{\mathbf{x}}_3 = \begin{pmatrix} 1 \\ 2 \\ 0 \\ 2 \end{pmatrix}, \tilde{\mathbf{x}}_4 = \begin{pmatrix} 2 \\ 1 \\ 1 \\ 1 \end{pmatrix}
    $$

13. Considere el espacio vectorial de funciones continuas, con valores complejos en el intervalo $[-\pi, \pi]$. Muestre que
    $$
    \langle f|g \rangle = \int_{-\pi}^{\pi} dt \, f^*(t) g(t)
    $$
    define un producto escalar en este espacio. ¿Son las siguientes funciones ortogonales con respecto a este producto escalar?
    (a) $\sin(t)$, $\cos(t)$  
    (b) $\exp(int)$, $\exp(ikt)$ con $n,k$ enteros  
    (c) $t^2$, $t^4$

14. Sea $V$ el espacio vectorial real de todas las matrices simétricas $n \times n$ reales y defina el producto escalar de dos matrices $A, B$ por (Tr($A$) denota la traza de $A$)
    $$
    \langle A|B \rangle = \text{Tr}(AB)
    $$
    Muestre que esto efectivamente cumple los requisitos de un producto escalar.

## C. Matrices, Rotaciones

15. Encuentre el rango de las siguientes matrices reduciendo sus determinantes a forma triangular superior:
    $$
    \begin{pmatrix} 1 & 0 & 1 \\ 0 & 3 & 0 \\ 1 & 2 & -1 \end{pmatrix}, \begin{pmatrix} 1 & 1 & 1 \\ 1 & -2 & 1 \\ 1 & 0 & -1 \end{pmatrix}, \begin{pmatrix} 1 & 2 & 3 \\ 1 & -1 & -1 \\ 5 & -2 & -1 \end{pmatrix}, \begin{pmatrix} 1 & x & y \\ 3x & 2y & 1 \\ x & y & 1 \end{pmatrix}
    $$

16. Considerando las matrices $A = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$, $B = \begin{pmatrix} 0 & 0 \\ 3 & 4 \end{pmatrix}$ muestre que $AB = 0$ no implica que ninguna de las matrices $A$ o $B$ sea la matriz cero. Permitiendo que $A, B$ sean cualesquiera matrices cuadradas, muestre que $AB = 0$ implica que al menos una de ellas es singular, es decir, tiene determinante cero.

17. Considere las tres matrices $\sigma_x = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$, $\sigma_y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}$, $\sigma_z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$. ¿Cuáles de las matrices son simétricas, cuáles son hermíticas? Calculando los conmutadores de estas matrices, muestre que pueden escribirse como $[\sigma_a, \sigma_b] = 2i\varepsilon_{abc}\sigma_c$, donde $\varepsilon_{abc}$ es el tensor epsilon y en el lado derecho se emplea la convención de suma (es decir, el índice $c$ se suma). Escriba $\exp(i\alpha\sigma_y)$ ($\alpha$ es un número real) como una matriz $2 \times 2$. ¿Qué representa? Muestre que $\exp(i\alpha\sigma_y)$ es unitaria sin escribirla explícitamente como una matriz $2 \times 2$.

18. Considere el espacio vectorial $V$ de flechas en el plano. Sea $A$ el operador lineal que rota todos los vectores 45 grados y luego los refleja con respecto a la horizontal. Sea $B_1 = \{\tilde{\mathbf{e}}_1, \tilde{\mathbf{e}}_2\}$ la base cartesiana estándar y $B_2 = \{\tilde{\mathbf{e}}_1', \tilde{\mathbf{e}}_2'\}$ otra base ortonormal de $V$, que se obtiene de $\{\tilde{\mathbf{e}}_1, \tilde{\mathbf{e}}_2\}$ mediante una rotación por un ángulo $\alpha$, ver Fig. 1. Escriba la transformación que lleva $\tilde{\mathbf{e}}_{1,2}$ a $\tilde{\mathbf{e}}_{1,2}'$ en forma matricial.
    ¿Cuáles son las representaciones coordenadas de $A$ con respecto a las bases $B_1$ y $B_2$ respectivamente? ¿Cuál es la ecuación matricial que relaciona estas dos representaciones coordenadas?

19. (i) Muestre que $(AB)^T = B^T A^T$.  
    (ii) La traza de una matriz $A$ se define como $\text{Tr} A = \sum_n A_{nn}$ es decir la suma de los elementos diagonales. Muestre que $\text{Tr} AB = \text{Tr} BA$ para cualesquiera dos matrices $B, A$ y por lo tanto que la traza de cualquier producto de matrices $AB\ldots Z$ no cambia bajo una permutación cíclica de las entradas.  
    (iii) Muestre que si $R$ es una matriz ortogonal, entonces $\text{Tr} R^TAR = \text{Tr} A$ es decir la traza es invariante bajo cambio de base ortonormal.