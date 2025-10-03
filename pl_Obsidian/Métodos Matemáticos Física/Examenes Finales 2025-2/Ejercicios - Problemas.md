### Ejercicio 1

La función $u(x, y) = \dfrac{x}{x^2 + y^2}$ es armónica porque satisface la ecuación de Laplace $\nabla^2 u = 0$. Esto se verificacion:
a calculando las derivadas parciales segundas y mostrando que su suma es cero.

La conjugada armónica $v(x, y)$e encuentra mediante las ecuaciones de Cauchy-Riemann:
$$
\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \quad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}.
$$
Con $\dfrac{\partial u}{\partial x} = \dfrac{y^2 - x^2}{(x^2 + y^2)^2}$ y $c\dfrac{\partial u}{\partial y} = \dfrac{-2xy}{(x^2 + y^2)^2}$, se integra para obtener:
$$
v(x, y) = \frac{-y}{x^2 + y^2} + C,
$$
donde $C$ es una constante. Tomando $C = 0$, la conjugada armónica es:
$$
v(x, y) = \frac{-y}{x^2 + y^2}.
$$

### Ejercicio 2

La integral 
$$
I = \int_{|z|=5} \frac{z \, dz}{(\sec z)(1 - \cos z)}
$$
se simplifica a 
$$
I = \oint_{|z|=5} \frac{z \cos z}{1 - \cos z} \, dz.
$$
Las singularidades ocurren cuando $1 - \cos z = 0$, es decir, $z = 2\pi k$ para $k \in \mathbb{Z}$. Dentro de $|z| = 5$, el único punto es $z = 0$. Se expande en series de Laurent alrededor de $z = 0$:
$$
\cos z = 1 - \frac{z^2}{2!} + \frac{z^4}{4!} - \cdots, \quad 1 - \cos z = \frac{z^2}{2} - \frac{z^4}{24} + \cdots,
$$
$$
\frac{1}{1 - \cos z} = \frac{2}{z^2} \left(1 + \frac{z^2}{12} + \cdots \right), \quad \frac{z \cos z}{1 - \cos z} = \frac{2}{z} \left(1 - \frac{5}{12} z^2 + \cdots \right).
$$
El residuo en $z = 0$ es 2. Por el teorema de los residuos:
$$
I = 2\pi i \cdot 2 = 4\pi i.
$$

### Ejercicio 3

#### (a) Representación matricial
En la base ortonormal $\{|1\rangle, |2\rangle\}$:
- $\sigma_x = |1\rangle \langle 2| + |2\rangle \langle 1| = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$
- $\sigma_y = -i|1\rangle \langle 2| + i|2\rangle \langle 1| = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}$
- $\sigma_z = |1\rangle \langle 1| - |2\rangle \langle 2| = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$

#### (b) Valores y vectores propios
- $\sigma_x$: Valores propios $\lambda = \pm 1$. Vectores propios: $\frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix}$ para $\lambda = 1$, $\frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -1 \end{pmatrix}$ para $\lambda = -1$.
- $\sigma_y$: Valores propios $\lambda = \pm 1$. Vectores propios: $\frac{1}{\sqrt{2}} \begin{pmatrix} -i \\ 1 \end{pmatrix}$ para $\lambda = 1$, $\frac{1}{\sqrt{2}} \begin{pmatrix} i \\ 1 \end{pmatrix}$ para $\lambda = -1$.
- $\sigma_z$: Valores propios $\lambda = \pm 1$. Vectores propios: $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$ para $\lambda = 1$, $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$ para $\lambda = -1$.

#### (c) Representación de $\sigma_z$ en base de $\sigma_x$
La base de estados propios de $\sigma_x$ es $|+\rangle = \frac{1}{\sqrt{2}} (|1\rangle + |2\rangle)$, $|-\rangle = \frac{1}{\sqrt{2}} (|1\rangle - |2\rangle)$. La matriz de $\sigma_z$ en esta base es:
$$
\langle + | \sigma_z | + \rangle = 0, \quad \langle + | \sigma_z | - \rangle = 1, \quad \langle - | \sigma_z | + \rangle = 1, \quad \langle - | \sigma_z | - \rangle = 0,
$$
es decir,
$$
\sigma_z = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}.
$$

#### (d) Conmutadores
El conmutador se define como $[A, B] = AB - BA$. Se verifica:
- $[\sigma_x, \sigma_y] = 2i \sigma_z$
- $[\sigma_y, \sigma_z] = 2i \sigma_x$
- $[\sigma_z, \sigma_x] = 2i \sigma_y$
Thus, el conmutador de dos matrices de Pauli es $2i$ veces la tercera.

### Ejercicio 4

#### (a) Funciones de Green
El operador es $L = \frac{d^2}{dt^2} + q^2$. La función de Green $G(t, s)$ satisface $L G(t, s) = \delta(t - s)$. Para $t \neq s$, la solución es $G(t,s) = A(s) \cos(q t) + B(s) \sin(q t)$. Imponiendo continuidad en $t = s$ y un salto unitario en la derivada, se obtiene la función de Green causal:
$$
G(t,s) = \frac{1}{q} \sin(q(t-s)) \Theta(t-s),
$$
donde $\Theta$ es la función escalón. La función de Green no es única porque se puede agregar cualquier solución de la ecuación homogénea $L x = 0$.

#### (b) Solución para $F(x) = x(t)^2$
La ecuación es $\frac{d^2 x}{dt^2} + q^2 x = x(t)^2$. Usando la función de Green, la solución se escribe como:
$$
x(t) = x_h(t) + \int_{-\infty}^{\infty} G(t,s) x(s)^2 \, ds,
$$
donde $x_h(t)$ es la solución homogénea de $L x_h = 0$. Para la función de Green causal, esto se reduce a:
$$
x(t) = x_h(t) + \int_{-\infty}^{t} \frac{1}{q} \sin(q(t-s)) x(s)^2 \, ds.
$$
Esta es una ecuación integral no lineal para $x(t)$.

# Final 2

## 1.  
Considere el operador diferencial asociado a un problema de oscilador armónico forzado con masa $(m = 1)$:  
$$\frac{d^2}{dt^2}x(t) + \alpha^2 x(t) = F(t).$$

**(a)** Encuentre las soluciones a la ecuación diferencial homogénea.

**(b)** Escriba la ecuación de Green asociada a ese operador.

**(c)** Use la transformada de Fourier  
$$g(t) = \frac{1}{\sqrt{2\pi}} \int dw  e^{-iwt} \tilde{g}(w), \quad \tilde{g}(w) = \frac{1}{\sqrt{2\pi}} \int dt  e^{iwt} g(t),$$  
para escribir la transformada de la función de Green.

**(d)** Use la ecuación diferencial de Green y la expresión de la función Delta de Dirac en Fourier  
$$\delta(t) = \frac{1}{2\pi} \int dw  e^{-iwt}$$  
para obtener los coeficientes de Fourier $\tilde{g}(w)$.

**(e)** Escriba la función de Green y obtenga las diferentes aproximaciones integrando por el método de residuos.

**(f)** Escriba la expresión para la solución de la ecuación diferencial propuesta, si $F(t) = e^{i\beta t}$.

---

## 2.  
Para un espacio de Hilbert $\mathcal{H}$ de las funciones de valor complejo, cuadrado integrables, sobre $\mathbb{R}$, con producto escalar:  
$$\langle f, g \rangle = \int f^*(x) g(x)  dx,$$  
se pide:

**(a)** Muestre que el operador $P = -i \frac{d}{dx}$ es un operador autoadjunto.

**(b)** Muestre que los vectores propios para un operador autoadjunto, con diferente valor propio, son ortogonales.

**(c)** Encuentre las funciones que son vectores propios de este operador.

**(d)** Dado un conjunto de funciones ortogonales con norma finita. Escriba la descomposición de la función $f \in L^2(\mathbb{R})$ en una base.

**(e)** Muestre que el operador $P = -i \frac{d}{dx}$ es un operador autoadjunto.

**(f)** ¿El conjunto de funciones propias del operador $P$ es completo?

**(g)** Escriba la expresión del operador proyección sobre un subespacio invariante.

**(h)** Si cambiamos de espacio de Hilbert a $L^2([a,b])$, con producto interno  
$$\langle f, g \rangle = \int_a^b f^*(x) g(x)  dx,$$  
¿qué condición o condiciones se requieren para que $P$ sea autoadjunto?

# Final 3

### Métodos Matemáticos – Segundo Examen Parcial

## 1. (50%)
Calcule, por método de residuos, la integral

$$
f(t) = \int_{-\infty}^{\infty} \frac{e^{-iqt}}{q^2 - a^2}  dq
$$

donde $a$ es una constante positiva.

---

## 2. (25%)
Calcule, por el método de residuos, la integral

$$
\int_{0}^{2\pi} \frac{\sin ^2 x}{5 + 4\cos x}  dx
$$

---

## 3. (25%) 
Para la esfera $S^2 \simeq \mathbb{C} \cup \{\infty\}$, encuentre:

### (a) Transformación fraccionaria lineal
Encuentre la transformación fraccionaria lineal

$$
w = \frac{az+b}{cz+d}, \quad ad - bc \neq 0
$$

que lleva los puntos:
- $1 \mapsto 0$
- $0 \mapsto -1$
- $-1 \mapsto \infty$

### (b) Puntos fijos
Encuentre los puntos fijos de esta transformación.

### (c) Transformación de semiplano a círculo
Argumente por qué esta transformación lleva el semiplano de los reales positivos

$$
\{(x,y): x>0\}
$$

al círculo de radio 1 en el plano complejo.