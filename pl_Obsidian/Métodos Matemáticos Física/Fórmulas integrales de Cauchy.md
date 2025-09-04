
---

Las fórmulas de representación, y en particular las fórmulas de representación integral, juegan un papel importante en matemáticas, ya que nos permiten recuperar una función en un conjunto grande a partir de su comportamiento en un conjunto más pequeño. Por ejemplo, vimos en el Libro I que una solución de la ecuación del calor en estado estacionario en el disco estaba completamente determinada por sus valores en la frontera sobre el círculo mediante una convolución con el núcleo de Poisson

$$
u(r, \theta) = \frac{1}{2\pi} \int_0^{2\pi} P_r(\theta - \varphi) u(1, \varphi)  d\varphi.
$$

En el caso de las funciones holomorfas, la situación es análoga, lo cual no es sorprendente ya que las partes real e imaginaria de una función holomorfa son armónicas. Aquí, probaremos una fórmula de representación integral de una manera que es independiente de la teoría de funciones armónicas. De hecho, también es posible recuperar la fórmula integral de Poisson como consecuencia del próximo teorema.

**Teorema 4.1** Supongamos que $f$ es holomorfa en un conjunto abierto que contiene la clausura de un disco $D$. Si $C$ denota el círculo frontera de este disco con la orientación positiva, entonces

$$
f(z) = \frac{1}{2\pi i} \int_C \frac{f(\zeta)}{\zeta - z}  d\zeta \quad \text{para cualquier punto } z \in D.
$$

*Demostración omitida.*

**Observaciones.** Nuestra discusión anterior sobre contornos simples proporciona extensiones sencillas de la fórmula integral de Cauchy; por ejemplo, si $f$ es holomorfa en un conjunto abierto que contiene un rectángulo (con orientación positiva) $R$ y su interior, entonces

$$
f(z) = \frac{1}{2\pi i} \int_{R} \frac{f(\zeta)}{\zeta - z}  d\zeta,
$$

siempre que $z$ pertenezca al interior de $R$. También debe notarse que la integral anterior se anula cuando $z$ está fuera de $R$, ya que en este caso $F(\zeta) = f(\zeta)/(\zeta - z)$ es holomorfa dentro de $R$. Por supuesto, un resultado similar también es válido para el círculo o cualquier otro contorno simple.

Como corolario de la fórmula integral de Cauchy, llegamos a un segundo hecho notable sobre las funciones holomorfas, a saber, su regularidad. También obtenemos más fórmulas integrales que expresan las derivadas de $f$ dentro del disco en términos de los valores de $f$ en la frontera.

**Corolario 4.2** Si $f$ es holomorfa en un conjunto abierto $\Omega$, entonces $f$ tiene infinitas derivadas complejas en $\Omega$. Además, si $C \subset \Omega$ es un círculo cuyo interior también está contenido en $\Omega$, entonces

$$
f^{(n)}(z) = \frac{n!}{2\pi i} \int_C \frac{f(\zeta)}{(\zeta - z)^{n+1}}  d\zeta
$$

para todo $z$ en el interior de $C$.

Recordamos que, como en el teorema anterior, tomamos el círculo $C$ con orientación positiva.

*Demostración omitida.*

De ahora en adelante, llamaremos a las fórmulas del Teorema 4.1 y del Corolario 4.2 las **fórmulas integrales de Cauchy**.

**Corolario 4.3 (Desigualdades de Cauchy)** Si $f$ es holomorfa en un conjunto abierto que contiene la clausura de un disco $D$ centrado en $z_0$ y de radio $R$, entonces

$$
|f^{(n)}(z_0)| \leq \frac{n! \|f\|_C}{R^n},
$$

donde $\|f\|_C = \sup_{z \in C} |f(z)|$ denota el supremo de $|f|$ en el círculo frontera $C$.

*Demostración omitida.*

Otra consecuencia sorprendente de la fórmula integral de Cauchy es su conexión con las series de potencias. En el Capítulo 1, probamos que una serie de potencias es holomorfa en el interior de su disco de convergencia, y prometimos una prueba de un recíproco, que es el contenido del próximo teorema.

**Teorema 4.4** Supongamos que $f$ es holomorfa en un conjunto abierto $\Omega$. Si $D$ es un disco centrado en $z_0$ y cuya clausura está contenida en $\Omega$, entonces $f$ tiene un desarrollo en serie de potencias en $z_0$

$$
f(z) = \sum_{n=0}^{\infty} a_n (z - z_0)^n
$$

para todo $z \in D$, y los coeficientes vienen dados por

$$
a_n = \frac{f^{(n)}(z_0)}{n!} \quad \text{para todo } n \geq 0.
$$

*Demostración omitida.*

Obsérvese que, dado que las series de potencias definen funciones indefinidamente diferenciables (en el sentido complejo), el teorema da otra prueba de que una función holomorfa es automáticamente indefinidamente diferenciable.

Otra observación importante es que el desarrollo en serie de potencias de $f$ centrado en $z_0$ converge en cualquier disco, sin importar cuán grande sea, siempre que su clausura esté contenida en $\Omega$. En particular, si $f$ es entera (es decir, holomorfa en todo $\mathbb{C}$), el teorema implica que $f$ tiene un desarrollo en serie de potencias alrededor de 0, digamos $f(z) = \sum_{n=0}^{\infty} a_n z^n$, que converge en todo $\mathbb{C}$.

**Corolario 4.5 (Teorema de Liouville)** Si $f$ es entera y acotada, entonces $f$ es constante.

*Demostración omitida.*

Como aplicación de nuestro trabajo hasta ahora, podemos dar una prueba elegante del teorema fundamental del álgebra.

**Corolario 4.6** Todo polinomio no constante $P(z) = a_n z^n + \cdots + a_0$ con coeficientes complejos tiene una raíz en $\mathbb{C}$.

*Demostración omitida.*

**Corolario 4.7** Todo polinomio $P(z) = a_n z^n + \cdots + a_0$ de grado $n \geq 1$ tiene precisamente $n$ raíces en $\mathbb{C}$. Si estas raíces se denotan por $w_1, \ldots, w_n$, entonces $P$ puede factorizarse como

$$
P(z) = a_n(z - w_1)(z - w_2) \cdots (z - w_n).
$$

*Demostración omitida.*

Finalmente, terminamos esta sección con una discusión sobre la prolongación analítica (el tercero de los "milagros" que mencionamos en la introducción). Esta establece que el "código genético" de una función holomorfa está determinado (es decir, la función queda fijada) si conocemos sus valores en subconjuntos arbitrariamente pequeños apropiados. Nótese que en el teorema siguiente, se asume que $\Omega$ es conexo.

**Teorema 4.8** Supongamos que $f$ es una función holomorfa en una región $\Omega$ que se anula en una sucesión de puntos distintos con un punto límite en $\Omega$. Entonces $f$ es idénticamente 0.

En otras palabras, si los ceros de una función holomorfa $f$ en el conjunto abierto conexo $\Omega$ se acumulan en $\Omega$, entonces $f = 0$.

*Demostración omitida.*

Una consecuencia inmediata del teorema es la siguiente.

**Corolario 4.9** Supongamos que $f$ y $g$ son holomorfas en una región $\Omega$ y $f(z) = g(z)$ para todo $z$ en algún subconjunto abierto no vacío de $\Omega$ (o más generalmente para $z$ en alguna sucesión de puntos distintos con punto límite en $\Omega$). Entonces $f(z) = g(z)$ en todo $\Omega$.

Supongamos que se nos da un par de funciones $f$ y $F$ analíticas en regiones $\Omega$ y $\Omega'$, respectivamente, con $\Omega \subset \Omega'$. Si las dos funciones coinciden en el conjunto más pequeño $\Omega$, decimos que $F$ es una **prolongación analítica** de $f$ en la región $\Omega'$. El corolario entonces garantiza que sólo puede haber una única prolongación analítica de este tipo, ya que $F$ está determinada de manera única por $f$.

---