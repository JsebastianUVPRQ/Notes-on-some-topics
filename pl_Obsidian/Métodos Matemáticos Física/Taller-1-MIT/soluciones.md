# Solución a los Ejercicios 1 y 2

## Ejercicio 1

Para demostrar que el espacio de matrices $2 \times 2$ es un espacio vectorial lineal, debemos verificar que satisface los axiomas de un espacio vectorial:

1. **Cerradura bajo suma**: Si $A$ y $B$ son matrices $2 \times 2$, entonces $A+B$ también es una matriz $2 \times 2$
2. **Cerradura bajo multiplicación por escalar**: Si $A$ es una matriz $2 \times 2$ y $c$ es un escalar, entonces $cA$ también es una matriz $2 \times 2$.
3. **Existencia del elemento neutro**: La matriz cero $O = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$ es el elemento neutro para la suma.
4. **Existencia de inversos aditivos**: Para cualquier matriz $A$, $-A$ es también una matriz $2 \times 2$ que satisface $A + (-A) = O$.
5. **Propiedades asociativas y conmutativas**: La suma de matrices es asociativa y conmutativa.
6. **Propiedades distributivas**: La multiplicación por escalar distribuye sobre la suma de matrices y de escalares.

Todos estos axiomas se cumplen para el conjunto de matrices $2 \times 2$, por lo tanto, el espacio de matrices $2 \times 2$ es un espacio vectorial lineal.

La dimensión del espacio de matrices $2 \times 2$ es $4$, ya que se necesitan $4$ parámetros independientes para especificar cualquier matriz $2 \times 2$.

Una base para este espacio es:
$$
\left\{
\begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix},
\begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix},
\begin{pmatrix} 0 & 0 \\ 1 & 0 \end{pmatrix},
\begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}
\right\}
$$

Cualquier matriz $2 \times 2$ $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ se puede expresar como combinación lineal de estos elementos base:
$$
\begin{pmatrix} a & b \\ c & d \end{pmatrix} = a\begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix} + b\begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix} + c\begin{pmatrix} 0 & 0 \\ 1 & 0 \end{pmatrix} + d\begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}
$$

## Ejercicio 2

La dimensión del espacio de matrices $n \times n$ es $n^2$.

Esto se debe a que una matriz $n \times n$ tiene $n^2$ elementos, y cada elemento puede variar independientemente. Para especificar completamente una matriz $n \times n$, necesitamos $n^2$ parámetros.

Una base para este espacio es el conjunto de matrices $\{E_{ij} \mid 1 \leq i,j \leq n\}$, donde $E_{ij}$ es la matriz con $1$ en la posición $(i,j)$ y $0$ en todas las demás posiciones:

$$
E_{ij} = \begin{pmatrix}
0 & \cdots & 0 & \cdots & 0 \\
\vdots & \ddots & \vdots & & \vdots \\
0 & \cdots & 1 & \cdots & 0 \\
\vdots & & \vdots & \ddots & \vdots \\
0 & \cdots & 0 & \cdots & 0
\end{pmatrix}
$$

donde el $1$ está en la posición $(i,j)$.

Cualquier matriz $A = (a_{ij})$ de tamaño $n \times n$ se puede expresar como:
$$
A = \sum_{i=1}^{n} \sum_{j=1}^{n} a_{ij} E_{ij}
$$

Esta base tiene exactamente $n^2$ elementos, lo que confirma que la dimensión del espacio de matrices $n \times n$ es $n^2$.
# 3
# Solución a los Problemas 3, 4, 5, 6 y 7


**¿Cuál es la dimensión del espacio de matrices $n \times n$ cuyos componentes son todos cero excepto posiblemente los componentes diagonales?**

Este es el espacio de matrices diagonales. Una matriz diagonal $n \times n$ tiene la forma:
$$
\begin{pmatrix}
a_1 & 0 & \cdots & 0 \\
0 & a_2 & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & a_n
\end{pmatrix}
$$

Para especificar una matriz diagonal $n \times n$, necesitamos especificar $n$ elementos (los elementos diagonales). Esto significa que el espacio de matrices diagonales $n \times n$ es isomorfo a $\mathbb{R}^n$, y por lo tanto tiene dimensión $n$.

Una base para este espacio sería:
$$
\left\{
\begin{pmatrix} 1 & 0 & \cdots & 0 \\ 0 & 0 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & 0 \end{pmatrix},
\begin{pmatrix} 0 & 0 & \cdots & 0 \\ 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & 0 \end{pmatrix},
\ldots,
\begin{pmatrix} 0 & 0 & \cdots & 0 \\ 0 & 0 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & 1 \end{pmatrix}
\right\}
$$

Esta base tiene $n$ elementos, lo que confirma que la dimensión es $n$.

## Problema 4

**¿Cuál es la dimensión del espacio de matrices simétricas $2 \times 2$, es decir, matrices $2 \times 2$ tales que $A = A^T$? Exhiba una base para este espacio.**

Una matriz simétrica $2 \times 2$ tiene la forma:
$$
\begin{pmatrix}
a & b \\
b & c
\end{pmatrix}
$$

Para especificar una matriz simétrica $2 \times 2$, necesitamos especificar $3$ elementos ($a, b, c$). Esto significa que el espacio de matrices simétricas $2 \times 2$ es isomorfo a $\mathbb{R}^3$, y por lo tanto tiene dimensión $3$.

Una base para este espacio sería:
$$
\left\{
\begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix},
\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix},
\begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}
\right\}
$$

Esta base tiene $3$ elementos, lo que confirma que la dimensión es $3$.

## Problema 5

**Considere el espacio vectorial de todas las funciones de una variable $t$. Muestre que los siguientes pares de funciones son linealmente independientes:**

Para demostrar que dos funciones son linealmente independientes, debemos mostrar que si $af(t) + bg(t) = 0$ para todo $t$, entonces $a = b = 0$.

**(a) $1$, $t$**

Supongamos que $a \cdot 1 + b \cdot t = 0$ para todo $t$. Esto significa que $a + bt = 0$ para todo $t$. Evaluando en $t = 0$, obtenemos $a = 0$. Luego, con $a = 0$, la ecuación se reduce a $bt = 0$ para todo $t$, lo que implica que $b = 0$. Por lo tanto, $1$ y $t$ son linealmente independientes.

**(b) $t$, $t^2$**

Supongamos que $a \cdot t + b \cdot t^2 = 0$ para todo $t$. Esto significa que $at + bt^2 = 0$ para todo $t$. Evaluando en $t = 1$, obtenemos $a + b = 0$. Evaluando en $t = 2$, obtenemos $2a + 4b = 0$. Resolviendo este sistema de ecuaciones, obtenemos $a = b = 0$. Por lo tanto, $t$ y $t^2$ son linealmente independientes.

**(c) $e^t$, $t$**

Supongamos que $a \cdot e^t + b \cdot t = 0$ para todo $t$. Esto significa que $ae^t + bt = 0$ para todo $t$. Evaluando en $t = 0$, obtenemos $a = 0$. Luego, con $a = 0$, la ecuación se reduce a $bt = 0$ para todo $t$, lo que implica que $b = 0$. Por lo tanto, $e^t$ y $t$ son linealmente independientes.

**(d) $\sin(t)$, $\cos(t)$**

Supongamos que $a \cdot \sin(t) + b \cdot \cos(t) = 0$ para todo $t$. Evaluando en $t = 0$, obtenemos $b = 0$. Evaluando en $t = \pi/2$, obtenemos $a = 0$. Por lo tanto, $\sin(t)$ y $\cos(t)$ son linealmente independientes.

## Problema 6

**¿Cuáles son las coordenadas de la función $f(t) = 3\sin(t) + 5\cos(t)$ con respecto a la base $\{\sin(t), \cos(t)\}$?**

La función $f(t)$ ya está expresada como una combinación lineal de los elementos de la base:
$$f(t) = 3\sin(t) + 5\cos(t)$$

Por lo tanto, las coordenadas de $f(t)$ con respecto a la base $\{\sin(t), \cos(t)\}$ son $(3, 5)$.

## Problema 7

**¿Cuáles son las dimensiones de los espacios vectoriales generados por los siguientes conjuntos de vectores?**

**(a) $\{(1, 1)^T, (1, 2)^T\}$**

Para determinar la dimensión, verificamos si los vectores son linealmente independientes. Supongamos que $a(1, 1)^T + b(1, 2)^T = (0, 0)^T$. Esto da el sistema:
$$
\begin{cases}
a + b = 0 \\
a + 2b = 0
\end{cases}
$$

Restando la primera ecuación de la segunda, obtenemos $b = 0$, y luego $a = 0$. Los vectores son linealmente independientes, por lo que la dimensión es 2.

**(b) $\{(1, 0)^T, (1, 0)^T\}$**

Estos son dos vectores idénticos. El espacio generado es el mismo que el generado por $\{(1, 0)^T\}$, que es una línea en $\mathbb{R}^2$. Por lo tanto, la dimensión es 1.

**(c) $\{(1, 1, 2)^T, (-2, 0, 1)^T, (-1, 1, 3)^T\}$**

Formamos una matriz con estos vectores como columnas y calculamos su rango:
$$
\begin{pmatrix}
1 & -2 & -1 \\
1 & 0 & 1 \\
2 & 1 & 3
\end{pmatrix}
$$

Reduciendo a forma escalonada:
$$
\begin{pmatrix}
1 & -2 & -1 \\
0 & 1 & 1 \\
0 & 0 & 0
\end{pmatrix}
$$

La matriz tiene 2 filas no nulas, por lo tanto, el rango es 2. La dimensión del espacio generado es 2.

Podemos tomar $\{(1, 1, 2)^T, (-2, 0, 1)^T\}$ como base. El tercer vector se expresa como:
$$(-1, 1, 3)^T = (1, 1, 2)^T + (-2, 0, 1)^T$$

**(d) $\{(1, 1, 1, 1)^T, (1, -1, 1, -1)^T, (1, 1, -1, -1)^T, (1, -1, -1, 1)^T\}$**

Formamos la matriz:
$$
\begin{pmatrix}
1 & 1 & 1 & 1 \\
1 & -1 & 1 & -1 \\
1 & 1 & -1 & -1 \\
1 & -1 & -1 & 1
\end{pmatrix}
$$

Esta es una matriz de Hadamard, y su producto consigo misma transpuesta es $4I$, lo que significa que es invertible. Por lo tanto, los 4 vectores son linealmente independientes, y la dimensión del espacio generado es 4.

**(e) $\{(1, 2, 3)^T, (1, -2, 1)^T, (3, 0, 2)^T, (4, 5, 6)^T\}$**

Formamos la matriz:
$$
\begin{pmatrix}
1 & 1 & 3 & 4 \\
2 & -2 & 0 & 5 \\
3 & 1 & 2 & 6
\end{pmatrix}
$$

Reduciendo a forma escalonada:
$$
\begin{pmatrix}
1 & 1 & 3 & 4 \\
0 & 1 & 3/2 & 3/4 \\
0 & 0 & 1 & 9/8
\end{pmatrix}
$$

La matriz tiene 3 filas no nulas, por lo tanto, el rango es 3. La dimensión del espacio generado es 3.

Podemos tomar $\{(1, 2, 3)^T, (1, -2, 1)^T, (3, 0, 2)^T\}$ como base. El cuarto vector se expresa como:
$$(4, 5, 6)^T = \frac{25}{16}(1, 2, 3)^T - \frac{15}{16}(1, -2, 1)^T + \frac{9}{8}(3, 0, 2)^T$$

**Bases ortogonales:**

- (a): $(1, 1)^T \cdot (1, 2)^T = 3 \neq 0$, no es ortogonal.
- (b): Trivialmente ortogonal (solo un vector).
- (c): $(1, 1, 2)^T \cdot (-2, 0, 1)^T = 0$, es ortogonal.
- (d): Todos los productos punto entre vectores distintos son 0, es ortogonal.
- (e): $(1, 2, 3)^T \cdot (3, 0, 2)^T = 9 \neq 0$, no es ortogonal.

# parte 2
# Solución a los Problemas 8, 9, 10, 11, 12, 13 y 14

## Problema 8: Desigualdad del Triángulo

Para demostrar la desigualdad del triángulo:

$$\|\mathbf{v}\rangle + \mathbf{w}\rangle\| \leq \|\mathbf{v}\rangle\| + \|\mathbf{w}\rangle\|$$

Elevamos al cuadrado ambos lados:

$$\|\mathbf{v}\rangle + \mathbf{w}\rangle\|^2 \leq (\|\mathbf{v}\rangle\| + \|\mathbf{w}\rangle\|)^2$$

Desarrollando el lado izquierdo:

$$\|\mathbf{v}\rangle + \mathbf{w}\rangle\|^2 = \langle\mathbf{v} + \mathbf{w}|\mathbf{v} + \mathbf{w}\rangle = \|\mathbf{v}\rangle\|^2 + \langle\mathbf{v}|\mathbf{w}\rangle + \langle\mathbf{w}|\mathbf{v}\rangle + \|\mathbf{w}\rangle\|^2$$

Para espacios complejos, $\langle\mathbf{w}|\mathbf{v}\rangle = \langle\mathbf{v}|\mathbf{w}\rangle^*$, por lo que:

$$\langle\mathbf{v}|\mathbf{w}\rangle + \langle\mathbf{w}|\mathbf{v}\rangle = 2\text{Re}(\langle\mathbf{v}|\mathbf{w}\rangle)$$

El lado derecho es:

$$(\|\mathbf{v}\rangle\| + \|\mathbf{w}\rangle\|)^2 = \|\mathbf{v}\rangle\|^2 + 2\|\mathbf{v}\rangle\|\|\mathbf{w}\rangle\| + \|\mathbf{w}\rangle\|^2$$

Por la desigualdad de Cauchy-Schwarz:

$$|\langle\mathbf{v}|\mathbf{w}\rangle| \leq \|\mathbf{v}\rangle\|\|\mathbf{w}\rangle\|$$

Por lo tanto:

$$\text{Re}(\langle\mathbf{v}|\mathbf{w}\rangle) \leq |\langle\mathbf{v}|\mathbf{w}\rangle| \leq \|\mathbf{v}\rangle\|\|\mathbf{w}\rangle\|$$

Entonces:

$$\|\mathbf{v}\rangle + \mathbf{w}\rangle\|^2 = \|\mathbf{v}\rangle\|^2 + 2\text{Re}(\langle\mathbf{v}|\mathbf{w}\rangle) + \|\mathbf{w}\rangle\|^2 \leq \|\mathbf{v}\rangle\|^2 + 2\|\mathbf{v}\rangle\|\|\mathbf{w}\rangle\| + \|\mathbf{w}\rangle\|^2$$

Tomando la raíz cuadrada de ambos lados (función monótona creciente):

$$\|\mathbf{v}\rangle + \mathbf{w}\rangle\| \leq \|\mathbf{v}\rangle\| + \|\mathbf{w}\rangle\|$$

## Problema 9: Vectores mutuamente perpendiculares

Sean $\tilde{\mathbf{a}}_1, \ldots, \tilde{\mathbf{a}}_n$ vectores en $\mathbb{R}^n$ mutuamente perpendiculares (i.e., $\tilde{\mathbf{a}}_i \cdot \tilde{\mathbf{a}}_j = 0$ para $i \neq j$) y ninguno igual a $\mathbf{0}$.

Supongamos que:

$$c_1\tilde{\mathbf{a}}_1 + c_2\tilde{\mathbf{a}}_2 + \ldots + c_n\tilde{\mathbf{a}}_n = \mathbf{0}$$

Tomando el producto punto con $\tilde{\mathbf{a}}_i$:

$$(c_1\tilde{\mathbf{a}}_1 + c_2\tilde{\mathbf{a}}_2 + \ldots + c_n\tilde{\mathbf{a}}_n) \cdot \tilde{\mathbf{a}}_i = \mathbf{0} \cdot \tilde{\mathbf{a}}_i$$

Por perpendicularidad:

$$c_i(\tilde{\mathbf{a}}_i \cdot \tilde{\mathbf{a}}_i) = 0$$

Como $\tilde{\mathbf{a}}_i \neq \mathbf{0}$, entonces $\tilde{\mathbf{a}}_i \cdot \tilde{\mathbf{a}}_i > 0$, por lo que $c_i = 0$.

Esto es válido para todo $i$, por lo que $c_1 = c_2 = \ldots = c_n = 0$. Los vectores son linealmente independientes.

## Problema 10: Vectores complejos normalizados

Tenemos:
$$\mathbf{u} = \alpha\begin{pmatrix} 1+i \\ 1-i \end{pmatrix}, \quad \mathbf{v} = \beta\begin{pmatrix} 1-i \\ 1+i \end{pmatrix}$$

Para que $\mathbf{u}$ esté normalizado:
$$\mathbf{u}^\dagger \mathbf{u} = 1$$

Calculamos:
$$\mathbf{u}^\dagger \mathbf{u} = \alpha^2\begin{pmatrix} 1-i & 1+i \end{pmatrix}\begin{pmatrix} 1+i \\ 1-i \end{pmatrix} = \alpha^2[2+2] = 4\alpha^2$$

Para normalización: $4\alpha^2 = 1 \implies \alpha = \frac{1}{2}$

Similarmente para $\mathbf{v}$:
$$\mathbf{v}^\dagger \mathbf{v} = \beta^2[2+2] = 4\beta^2$$

Para normalización: $4\beta^2 = 1 \implies \beta = \frac{1}{2}$

El producto escalar es:
$$\mathbf{u}^\dagger \mathbf{v} = \frac{1}{4}\begin{pmatrix} 1-i & 1+i \end{pmatrix}\begin{pmatrix} 1-i \\ 1+i \end{pmatrix} = \frac{1}{4}[-2i+2i] = 0$$

Para probar independencia lineal, supongamos $a\mathbf{u} + b\mathbf{v} = \mathbf{0}$:
- Tomando producto punto con $\mathbf{u}^\dagger$: $a = 0$
- Tomando producto punto con $\mathbf{v}^\dagger$: $b = 0$

Por lo tanto, $\mathbf{u}$ y $\mathbf{v}$ son linealmente independientes.

El espacio vectorial complejo bidimensional tiene dimensión 2, por lo que $\mathbf{u}$ y $\mathbf{v}$ forman una base. Como $\mathbf{u}^\dagger \mathbf{v} = 0$ y ambos están normalizados, es una base ortonormal.

Para expresar $\begin{pmatrix} 1 \\ i \end{pmatrix}$:
- $c_1 = \mathbf{u}^\dagger\begin{pmatrix} 1 \\ i \end{pmatrix} = 0$
- $c_2 = \mathbf{v}^\dagger\begin{pmatrix} 1 \\ i \end{pmatrix} = 1+i$

Por lo tanto:
$$\begin{pmatrix} 1 \\ i \end{pmatrix} = (1+i)\mathbf{v}$$

## Problema 11: Vectores ortogonales

### (a) $\begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$, $\begin{pmatrix} -1 \\ -1 \\ 1 \end{pmatrix}$

Buscamos $\mathbf{w} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$ tal que:
$$x + 2y + 3z = 0$$
$$-x - y + z = 0$$

Resolviendo:
$$y = -4z, \quad x = 5z$$

Tomamos $z = 1$: $\mathbf{w} = \begin{pmatrix} 5 \\ -4 \\ 1 \end{pmatrix}$

Normalización:
- $\hat{\mathbf{v}}_1 = \frac{1}{\sqrt{14}}\begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$
- $\hat{\mathbf{v}}_2 = \frac{1}{\sqrt{3}}\begin{pmatrix} -1 \\ -1 \\ 1 \end{pmatrix}$
- $\hat{\mathbf{w}} = \frac{1}{\sqrt{42}}\begin{pmatrix} 5 \\ -4 \\ 1 \end{pmatrix}$

### (b) $\begin{pmatrix} 1+i\sqrt{3} \\ 2 \\ 1-i\sqrt{3} \end{pmatrix}$, $\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}$

Para vectores complejos, el producto escalar es:
$$\mathbf{a} \cdot \mathbf{b} = a_1^*b_1 + a_2^*b_2 + a_3^*b_3$$

Resolviendo el sistema:
$$x^*(1+i\sqrt{3}) + 2y^* + z^*(1-i\sqrt{3}) = 0$$
$$x^* - y^* + z^* = 0$$

Obtenemos:
$$\mathbf{w} = \begin{pmatrix} -\frac{21}{2}-4i\sqrt{3} \\ -7-8i\sqrt{3} \\ 14 \end{pmatrix}$$

Normalización:
- $\hat{\mathbf{v}}_1 = \frac{1}{2\sqrt{3}}\begin{pmatrix} 1+i\sqrt{3} \\ 2 \\ 1-i\sqrt{3} \end{pmatrix}$
- $\hat{\mathbf{v}}_2 = \frac{1}{\sqrt{3}}\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}$
- $\hat{\mathbf{w}}$ se obtiene normalizando $\mathbf{w}$

### (c) $\begin{pmatrix} 1-i \\ 1 \\ 3i \end{pmatrix}$, $\begin{pmatrix} 1+2i \\ 2 \\ 1 \end{pmatrix}$

Resolviendo:
$$x^*(1-i) + y^* + z^*(-3i) = 0$$
$$x^*(1+2i) + 2y^* + z^* = 0$$

Obtenemos un vector $\mathbf{w}$ que se normaliza junto con los otros dos.

## Problema 12: Proceso de Gram-Schmidt

Vectores dados:
$$\tilde{\mathbf{x}}_1 = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 1 \end{pmatrix}, \tilde{\mathbf{x}}_2 = \begin{pmatrix} 1 \\ 0 \\ -1 \\ 0 \end{pmatrix}, \tilde{\mathbf{x}}_3 = \begin{pmatrix} 1 \\ 2 \\ 0 \\ 2 \end{pmatrix}, \tilde{\mathbf{x}}_4 = \begin{pmatrix} 2 \\ 1 \\ 1 \\ 1 \end{pmatrix}$$

Aplicando Gram-Schmidt:

1. $\mathbf{u}_1 = \tilde{\mathbf{x}}_1 = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 1 \end{pmatrix}$

   $\|\mathbf{u}_1\| = \sqrt{2}$

   $\mathbf{e}_1 = \frac{1}{\sqrt{2}}\begin{pmatrix} 0 \\ 0 \\ 1 \\ 1 \end{pmatrix}$

2. $\mathbf{u}_2 = \tilde{\mathbf{x}}_2 - \langle \mathbf{e}_1, \tilde{\mathbf{x}}_2 \rangle \mathbf{e}_1 = \begin{pmatrix} 1 \\ 0 \\ -\frac{1}{2} \\ \frac{1}{2} \end{pmatrix}$

   $\|\mathbf{u}_2| = \sqrt{\frac{3}{2}}$

   $\mathbf{e}_2 = \begin{pmatrix} \sqrt{\frac{2}{3}} \\ 0 \\ -\frac{1}{\sqrt{6}} \\ \frac{1}{\sqrt{6}} \end{pmatrix}$

3. $\mathbf{u}_3 = \tilde{\mathbf{x}}_3 - \langle \mathbf{e}_1, \tilde{\mathbf{x}}_3 \rangle \mathbf{e}_1 - \langle \mathbf{e}_2, \tilde{\mathbf{x}}_3 \rangle \mathbf{e}_2 = \begin{pmatrix} -\frac{1}{3} \\ 2 \\ -\frac{1}{3} \\ \frac{1}{3} \end{pmatrix}$

   $\|\mathbf{u}_3| = \sqrt{\frac{13}{3}}$

   $\mathbf{e}_3 = \begin{pmatrix} -\frac{1}{\sqrt{39}} \\ \frac{2\sqrt{3}}{\sqrt{13}} \\ -\frac{1}{\sqrt{39}} \\ \frac{1}{\sqrt{39}} \end{pmatrix}$

4. $\mathbf{u}_4 = \tilde{\mathbf{x}}_4 - \langle \mathbf{e}_1, \tilde{\mathbf{x}}_4 \rangle \mathbf{e}_1 - \langle \mathbf{e}_2, \tilde{\mathbf{x}}_4 \rangle \mathbf{e}_2 - \langle \mathbf{e}_3, \tilde{\mathbf{x}}_4 \rangle \mathbf{e}_3$

   (Se calcula de manera similar)

## Problema 13: Producto escalar en espacio de funciones

### Demostración de que $\langle f|g \rangle = \int_{-\pi}^{\pi} dt f^*(t) g(t)$ define un producto escalar

Verificamos las propiedades:

1. **Linealidad en el segundo argumento**: $\langle f|ag + bh \rangle = a\langle f|g \rangle + b\langle f|h \rangle$
   - Se cumple por linealidad de la integral

2. **Antilinealidad en el primer argumento**: $\langle af + bh|g \rangle = a^*\langle f|g \rangle + b^*\langle h|g \rangle$
   - Se cumple por $(af + bh)^* = a^*f^* + b^*h^*$

3. **Hermiticidad**: $\langle f|g \rangle = \langle g|f \rangle^*$
   - $\langle g|f \rangle^* = \int_{-\pi}^{\pi} dt g(t) f^*(t) = \langle f|g \rangle$

4. **Positividad definida**: $\langle f|f \rangle \geq 0$ y $\langle f|f \rangle = 0$ si y solo si $f = 0$
   - $\langle f|f \rangle = \int_{-\pi}^{\pi} dt |f(t)|^2 \geq 0$
   - $\langle f|f \rangle = 0$ implica $f = 0$ (por continuidad)

### Ortogonalidad de funciones

**(a) $\sin(t)$, $\cos(t)$**

$$\langle \sin(t)|\cos(t) \rangle = \int_{-\pi}^{\pi} dt \sin(t)\cos(t) = \int_{-\pi}^{\pi} dt \frac{1}{2}\sin(2t) = 0$$

Son ortogonales.

**(b) $\exp(int)$, $\exp(ikt)$ con $n,k$ enteros**

$$\langle \exp(int)|\exp(ikt) \rangle = \int_{-\pi}^{\pi} dt \exp(i(k-n)t)$$

- Si $k = n$: $2\pi$
- Si $k \neq n$: $\frac{2\sin((k-n)\pi)}{k-n} = 0$

Son ortogonales si $k \neq n$.

**(c) $t^2$, $t^4$**

$$\langle t^2|t^4 \rangle = \int_{-\pi}^{\pi} dt t^6 = \frac{2\pi^7}{7} \neq 0$$

No son ortogonales.

## Problema 14: Producto escalar en espacio de matrices simétricas

### Demostración de que $\langle A|B \rangle = \text{Tr}(AB)$ define un producto escalar

Verificamos las propiedades:

1. **Linealidad en el segundo argumento**: $\langle A|cB + dC \rangle = c\langle A|B \rangle + d\langle A|C \rangle$
   - $\text{Tr}(A(cB + dC)) = c\text{Tr}(AB) + d\text{Tr}(AC)$

2. **Simetría**: $\langle A|B \rangle = \langle B|A \rangle$
   - $\text{Tr}(AB) = \text{Tr}(BA)$

3. **Positividad definida**: $\langle A|A \rangle \geq 0$ y $\langle A|A \rangle = 0$ si y solo si $A = 0$
   - Como $A$ es simétrica, $A = PDP^{-1}$ con $D$ diagonal
   - $\text{Tr}(A^2) = \text{Tr}(D^2) = \sum \lambda_i^2 \geq 0$
   - $\text{Tr}(A^2) = 0$ si y solo si $A = 0$

Por lo tanto, $\langle A|B \rangle = \text{Tr}(AB)$ define un producto escalar válido.