# Capítulo 5: Integrales Múltiples - Desarrollo Extensivo y Completo

Este capítulo desarrolla las herramientas fundamentales del cálculo integral para funciones de varias variables, centrándose en las integrales dobles y triples. Las integrales múltiples son esenciales para calcular cantidades físicas como áreas, volúmenes, masas, centros de masa y momentos de inercia de objetos bidimensionales y tridimensionales. El capítulo comienza con la definición formal de la integral doble, continúa con su evaluación mediante integrales iteradas, explora diversas aplicaciones físicas y culmina con el cambio de variables y el uso del jacobiano, una técnica poderosa para simplificar integrales complejas al transformarlas a coordenadas más adecuadas.

## 1. Introducción

La integración es una herramienta fundamental en matemáticas aplicadas, utilizada para calcular cantidades como área, volumen, masa, momento de inercia, entre otras. Mientras que una integral simple $\int_a^b f(x)  dx$ se utiliza para encontrar el área bajo una curva $y = f(x)$ en un intervalo $[a, b]$, una integral doble $\iint_A f(x, y)  dx  dy$ extiende este concepto para encontrar el volumen bajo una superficie $z = f(x, y)$ sobre una región $A$ en el plano $xy$. De manera análoga, una integral triple $\iiint_V f(x, y, z)  dx  dy  dz$ se utiliza para calcular cantidades en volúmenes tridimensionales, como la masa total de un sólido con densidad variable.

El proceso de definir una integral doble es una extensión directa del proceso para integrales simples. Se divide la región $A$ en $N$ subregiones pequeñas (por ejemplo, rectángulos) de área $\Delta A_i$. Se elige un punto $(x_i, y_i)$ dentro de cada subregión y se forma la suma de Riemann:
$$
S_N = \sum_{i=1}^N f(x_i, y_i) \Delta A_i.
$$
La integral doble es el límite de esta suma cuando el tamaño de las subregiones tiende a cero (y $N \to \infty$):
$$
\iint_A f(x, y)  dx  dy = \lim_{\max(\Delta A_i) \to 0} S_N.
$$
Este límite, si existe, representa el volumen del sólido que se extiende desde la superficie $z = f(x, y)$ hasta el plano $xy$ sobre la región $A$. El capítulo explora cómo evaluar estas integrales de manera práctica mediante el concepto de integrales iteradas.

## 2. Integrales Dobles y Triples

La evaluación práctica de integrales múltiples se realiza mediante integrales iteradas (o repetidas). Una integral iterada consiste en evaluar dos o más integrales simples una dentro de la otra, siguiendo un orden específico de integración.

**Integrales Dobles:** Considere una región $A$ en el plano $xy$ acotada por $x = a$, $x = b$, $y = g_1(x)$, e $y = g_2(x)$, donde $g_1(x) \leq g_2(x)$ para $a \leq x \leq b$. La integral doble sobre $A$ se puede evaluar como una integral iterada integrando primero con respecto a $y$ y luego con respecto a $x$:
$$
\iint_A f(x, y)  dx  dy = \int_{x=a}^{x=b} \left( \int_{y=g_1(x)}^{y=g_2(x)} f(x, y)  dy \right) dx.
$$
Alternativamente, si la región se puede describir como $y = c$, $y = d$, $x = h_1(y)$, $x = h_2(y)$, con $h_1(y) \leq h_2(y)$, se puede integrar primero con respecto a $x$:
$$
\iint_A f(x, y)  dx  dy = \int_{y=c}^{y=d} \left( \int_{x=h_1(y)}^{x=h_2(y)} f(x, y)  dx \right) dy.
$$
El teorema de Fubini garantiza que si $f(x, y)$ es continua en $A$, ambos órdenes de integración producirán el mismo resultado.

**Ejemplo 1 (Volumen de un sólido):** Encuentre el volumen del sólido limitado por el cilindro $y = x^2$, los planos $y = 0$, $z = 0$ y $x + z = 1$. La región $A$ en el plano $xy$ está acotada por $y = 0$, $y = x^2$, $x = 0$, y $x = 1$. La superficie superior es $z = 1 - x$. El volumen $V$ es:
$$
V = \iint_A (1 - x)  dx  dy.
$$
Integrando primero con respecto a $y$ (de $0$ a $x^2$) y luego con respecto a $x$ (de $0$ a $1$):
$$
V = \int_{x=0}^{1} \int_{y=0}^{x^2} (1 - x)  dy  dx = \int_{0}^{1} (1 - x) \left[ y \right]_{0}^{x^2}  dx = \int_{0}^{1} (1 - x)x^2  dx = \int_{0}^{1} (x^2 - x^3)  dx = \left[ \frac{x^3}{3} - \frac{x^4}{4} \right]_{0}^{1} = \frac{1}{3} - \frac{1}{4} = \frac{1}{12}.
$$

**Integrales Triples:** Una integral triple se evalúa como una integral iterada de tres integrales simples. La región de integración $V$ en el espacio tridimensional se describe mediante límites para $x$, $y$, y $z$. Por ejemplo, si $V$ está acotado por $a \leq x \leq b$, $g_1(x) \leq y \leq g_2(x)$, y $h_1(x,y) \leq z \leq h_2(x,y)$, entonces:
$$
\iiint_V f(x, y, z)  dx  dy  dz = \int_{x=a}^{b} \int_{y=g_1(x)}^{g_2(x)} \int_{z=h_1(x,y)}^{h_2(x,y)} f(x, y, z)  dz  dy  dx.
$$

**Ejemplo 2 (Volumen de un sólido):** Encuentre el volumen del sólido $V$ limitado por el paraboloide $z = x^2 + y^2$ y el plano $z = 4$. La proyección de $V$ sobre el plano $xy$ es el círculo $x^2 + y^2 = 4$. Para un punto $(x, y)$ dentro de este círculo, $z$ varía desde $x^2 + y^2$ hasta $4$. El volumen $V$ es:
$$
V = \iiint_V 1  dx  dy  dz = \iint_A \left( \int_{z=x^2+y^2}^{4} dz \right) dx  dy = \iint_A (4 - x^2 - y^2)  dx  dy,
$$
donde $A$ es el disco $x^2 + y^2 \leq 4$. Esta integral doble se evalúa más fácilmente usando coordenadas polares (ver Sección 4).

## 3. Aplicaciones de la Integración: Integrales Simples y Múltiples

Las integrales múltiples se utilizan para calcular una amplia gama de cantidades físicas. El capítulo enfatiza que el proceso de "configurar" la integral es tan importante como su evaluación.

**Área y Volumen:** La integral doble de $1$ sobre una región $A$ da su área: $\text{Área}(A) = \iint_A dx  dy$. La integral triple de $1$ sobre un sólido $V$ da su volumen: $\text{Volumen}(V) = \iiint_V dx  dy  dz$.

**Masa:** Si una lámina (hoja delgada) en el plano $xy$ tiene una densidad de área $\rho(x, y)$ (masa por unidad de área), su masa total es:
$$
M = \iint_A \rho(x, y)  dx  dy.
$$
Si un sólido $V$ tiene una densidad de volumen $\rho(x, y, z)$ (masa por unidad de volumen), su masa total es:
$$
M = \iiint_V \rho(x, y, z)  dx  dy  dz.
$$

**Centro de Masa (Centroide):** Las coordenadas $(\bar{x}, \bar{y})$ del centro de masa de una lámina con densidad $\rho(x, y)$ son:
$$
\bar{x} = \frac{1}{M} \iint_A x \rho(x, y)  dx  dy, \quad \bar{y} = \frac{1}{M} \iint_A y \rho(x, y)  dx  dy.
$$
Para un sólido, las coordenadas $(\bar{x}, \bar{y}, \bar{z})$ son:
$$
\bar{x} = \frac{1}{M} \iiint_V x \rho(x, y, z)  dx  dy  dz, \quad \bar{y} = \frac{1}{M} \iiint_V y \rho(x, y, z)  dx  dy  dz, \quad \bar{z} = \frac{1}{M} \iiint_V z \rho(x, y, z)  dx  dy  dz.
$$
Si la densidad es constante, el centro de masa se llama centroide.

**Momentos de Inercia:** El momento de inercia mide la resistencia de un objeto a la rotación. Para una lámina, el momento de inercia respecto al eje $x$ es:
$$
I_x = \iint_A y^2 \rho(x, y)  dx  dy.
$$
Respecto al eje $y$:
$$
I_y = \iint_A x^2 \rho(x, y)  dx  dy.
$$
El momento de inercia respecto al origen (o al eje $z$ perpendicular al plano) es:
$$
I_0 = I_x + I_y = \iint_A (x^2 + y^2) \rho(x, y)  dx  dy.
$$
Para un sólido, el momento de inercia respecto al eje $z$ es:
$$
I_z = \iiint_V (x^2 + y^2) \rho(x, y, z)  dx  dy  dz.
$$

**Ejemplo 3 (Masa y centroide de una lámina):** Encuentre la masa y el centroide de la lámina que cubre el cuarto de disco $x^2 + y^2 \leq 4$, $x > 0$, $y > 0$, con densidad $\rho(x, y) = x + y$. Primero, calcule la masa:
$$
M = \iint_A (x + y)  dx  dy.
$$
Usando coordenadas polares ($x = r\cos\theta$, $y = r\sin\theta$, $dx  dy = r  dr  d\theta$), los límites son $0 \leq r \leq 2$, $0 \leq \theta \leq \pi/2$:
$$
M = \int_{\theta=0}^{\pi/2} \int_{r=0}^{2} (r\cos\theta + r\sin\theta) r  dr  d\theta = \int_{0}^{\pi/2} (\cos\theta + \sin\theta)  d\theta \int_{0}^{2} r^2  dr = [\sin\theta - \cos\theta]_{0}^{\pi/2} \cdot \left[\frac{r^3}{3}\right]_{0}^{2} = (1 - 0 - (0 - 1)) \cdot \frac{8}{3} = 2 \cdot \frac{8}{3} = \frac{16}{3}.
$$
Por simetría, $\bar{x} = \bar{y}$. Calcule $\bar{x}$:
$$
\bar{x} = \frac{1}{M} \iint_A x(x + y)  dx  dy = \frac{3}{16} \int_{0}^{\pi/2} \int_{0}^{2} (r\cos\theta)(r\cos\theta + r\sin\theta) r  dr  d\theta = \frac{3}{16} \int_{0}^{\pi/2} (\cos^2\theta + \cos\theta\sin\theta)  d\theta \int_{0}^{2} r^3  dr.
$$
$$
= \frac{3}{16} \left[ \frac{\theta}{2} + \frac{\sin 2\theta}{4} + \frac{\sin^2\theta}{2} \right]_{0}^{\pi/2} \cdot \left[\frac{r^4}{4}\right]_{0}^{2} = \frac{3}{16} \left( \frac{\pi}{4} + 0 + \frac{1}{2} - 0 \right) \cdot 4 = \frac{3}{16} \cdot \left( \frac{\pi}{4} + \frac{1}{2} \right) \cdot 4 = \frac{3}{4} \left( \frac{\pi}{4} + \frac{1}{2} \right) = \frac{3\pi}{16} + \frac{3}{8}.
$$
Por lo tanto, $\bar{x} = \bar{y} = \frac{3\pi}{16} + \frac{3}{8}$.

## 4. Cambio de Variables en Integrales; Jacobianos

Evaluar integrales múltiples puede simplificarse enormemente mediante un cambio de variables. Por ejemplo, una integral sobre un disco es mucho más fácil en coordenadas polares que en cartesianas. La herramienta matemática que permite este cambio es el jacobiano.

Suponga que se desea cambiar de variables $(x, y)$ a nuevas variables $(u, v)$ mediante las transformaciones:
$$
x = x(u, v), \quad y = y(u, v).
$$
El jacobiano de esta transformación, denotado por $\frac{\partial(x, y)}{\partial(u, v)}$, es el determinante de la matriz de derivadas parciales:
$$
\frac{\partial(x, y)}{\partial(u, v)} = \begin{vmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{vmatrix} = \frac{\partial x}{\partial u} \frac{\partial y}{\partial v} - \frac{\partial x}{\partial v} \frac{\partial y}{\partial u}.
$$
La fórmula para el cambio de variables en una integral doble es:
$$
\iint_A f(x, y)  dx  dy = \iint_{A'} f(x(u, v), y(u, v)) \left| \frac{\partial(x, y)}{\partial(u, v)} \right|  du  dv,
$$
donde $A'$ es la región en el plano $uv$ que corresponde a $A$ en el plano $xy$. El valor absoluto del jacobiano actúa como un factor de escala que ajusta el área del elemento diferencial al nuevo sistema de coordenadas.

**Coordenadas Polares:** El cambio más común es de cartesianas a polares: $x = r\cos\theta$, $y = r\sin\theta$. El jacobiano es:
$$
\frac{\partial(x, y)}{\partial(r, \theta)} = \begin{vmatrix}
\cos\theta & -r\sin\theta \\
\sin\theta & r\cos\theta
\end{vmatrix} = (\cos\theta)(r\cos\theta) - (-r\sin\theta)(\sin\theta) = r\cos^2\theta + r\sin^2\theta = r.
$$
Por lo tanto, $dx  dy = |r|  dr  d\theta = r  dr  d\theta$ (dado que $r \geq 0$). Esta fórmula es fundamental para evaluar integrales sobre regiones circulares o anulares.

**Ejemplo 4 (Integral en coordenadas polares):** Evalúe $\iint_A e^{-x^2-y^2}  dx  dy$ donde $A$ es el primer cuadrante ($x \geq 0$, $y \geq 0$). En coordenadas polares, $x^2 + y^2 = r^2$ y $dx  dy = r  dr  d\theta$. Los límites son $0 \leq r < \infty$, $0 \leq \theta \leq \pi/2$. La integral se convierte en:
$$
\int_{\theta=0}^{\pi/2} \int_{r=0}^{\infty} e^{-r^2} r  dr  d\theta.
$$
La integral interna se resuelve con la sustitución $u = r^2$, $du = 2r  dr$:
$$
\int_{0}^{\infty} e^{-r^2} r  dr = \frac{1}{2} \int_{0}^{\infty} e^{-u}  du = \frac{1}{2} [-e^{-u}]_{0}^{\infty} = \frac{1}{2}.
$$
Entonces:
$$
\int_{0}^{\pi/2} \frac{1}{2}  d\theta = \frac{1}{2} \cdot \frac{\pi}{2} = \frac{\pi}{4}.
$$

**Integrales Triples y Coordenadas Esféricas/Cilíndricas:** El concepto se extiende a tres dimensiones. Para coordenadas cilíndricas ($x = r\cos\theta$, $y = r\sin\theta$, $z = z$), el jacobiano es $r$, por lo que $dx  dy  dz = r  dr  d\theta  dz$. Para coordenadas esféricas ($x = \rho\sin\phi\cos\theta$, $y = \rho\sin\phi\sin\theta$, $z = \rho\cos\phi$), el jacobiano es $\rho^2 \sin\phi$, por lo que $dx  dy  dz = \rho^2 \sin\phi  d\rho  d\phi  d\theta$. Estos jacobianos representan los elementos de volumen en sus respectivos sistemas de coordenadas.

**Ejemplo 5 (Volumen de una esfera):** Use coordenadas esféricas para encontrar el volumen de una esfera de radio $a$. El volumen es:
$$
V = \iiint_V 1  dx  dy  dz = \int_{\theta=0}^{2\pi} \int_{\phi=0}^{\pi} \int_{\rho=0}^{a} \rho^2 \sin\phi  d\rho  d\phi  d\theta.
$$
$$
= \int_{0}^{2\pi} d\theta \int_{0}^{\pi} \sin\phi  d\phi \int_{0}^{a} \rho^2  d\rho = (2\pi) [-\cos\phi]_{0}^{\pi} \left[\frac{\rho^3}{3}\right]_{0}^{a} = 2\pi ( -(-1) + 1 ) \cdot \frac{a^3}{3} = 2\pi \cdot 2 \cdot \frac{a^3}{3} = \frac{4}{3}\pi a^3.
$$

## 5. Integrales de Superficie

Aunque el texto principal del archivo proporcionado no desarrolla extensamente esta sección, las integrales de superficie son una extensión natural del capítulo. Una integral de superficie se utiliza para integrar una función sobre una superficie $S$ en el espacio tridimensional. Si la superficie $S$ está definida por $z = g(x, y)$, el elemento de área de superficie $dS$ está dado por:
$$
dS = \sqrt{1 + \left( \frac{\partial g}{\partial x} \right)^2 + \left( \frac{\partial g}{\partial y} \right)^2}  dx  dy.
$$
Entonces, la integral de una función $f(x, y, z)$ sobre $S$ es:
$$
\iint_S f(x, y, z)  dS = \iint_A f(x, y, g(x, y)) \sqrt{1 + \left( \frac{\partial g}{\partial x} \right)^2 + \left( \frac{\partial g}{\partial y} \right)^2}  dx  dy,
$$
donde $A$ es la proyección de $S$ sobre el plano $xy$. Las integrales de superficie son cruciales para definir integrales de flujo, como $\iint_S \vec{F} \cdot \vec{n}  dS$, que mide el flujo de un campo vectorial $\vec{F}$ a través de la superficie $S$.

## 6. Problemas Diversos

Esta sección del capítulo contiene problemas que integran y aplican todas las técnicas aprendidas. Incluye ejercicios para practicar la configuración y evaluación de integrales dobles y triples en diferentes órdenes de integración, el cambio de orden de integración para facilitar el cálculo (especialmente cuando la integral interna no se puede evaluar directamente), y el uso del jacobiano para transformaciones más generales. También abarca aplicaciones adicionales de la física y la geometría, reforzando la idea central de que la habilidad para "configurar" correctamente una integral es fundamental para resolver problemas del mundo real. El capítulo enfatiza constantemente la importancia de esbozar la región de integración para determinar correctamente los límites y verificar los resultados mediante computadora.

# EJEMPLOS

Sí, basado en el contenido del capítulo 5 del libro de Mary Boas, aquí hay varios ejemplos resueltos que ilustran los principales conceptos y técnicas.

### Ejemplo 1: Evaluación de una Integral Doble (Problema resuelto implícito en la Sección 2)

**Problema:** Evalúe la integral doble $\int_{x=0}^{1} \int_{y=0}^{x^2} (1 - x)  dy  dx$.

**Solución:**
Este ejemplo corresponde a la Sección 2 del capítulo, donde se introducen las integrales iteradas. El problema es similar al que se usa para calcular el volumen en el texto.
1.  **Integre con respecto a $y$ primero:** La función $(1 - x)$ es constante con respecto a $y$, por lo que:
    $$
    \int_{y=0}^{x^2} (1 - x)  dy = (1 - x) \cdot [y]_{0}^{x^2} = (1 - x) \cdot (x^2 - 0) = x^2(1 - x) = x^2 - x^3.
    $$
2.  **Integre con respecto a $x$:** Ahora sustituimos el resultado anterior en la integral externa:
    $$
    \int_{x=0}^{1} (x^2 - x^3)  dx = \left[ \frac{x^3}{3} - \frac{x^4}{4} \right]_{0}^{1} = \left( \frac{1}{3} - \frac{1}{4} \right) - (0) = \frac{4}{12} - \frac{3}{12} = \frac{1}{12}.
    $$
**Respuesta:** $\int_{x=0}^{1} \int_{y=0}^{x^2} (1 - x)  dy  dx = \frac{1}{12}$.

---

### Ejemplo 2: Cambio de Orden de Integración (Problema 25)

**Problema:** Esboce el área de integración y escriba una integral equivalente con el orden de integración invertido para $\int_{x=0}^{1} \int_{y=0}^{3-3x} dy  dx$. Verifique que ambas integrales den el mismo resultado.

**Solución:**
Este problema es un ejemplo típico de la Sección 2, donde se discute cómo cambiar el orden de integración.
1.  **Esbozar el área:** Los límites originales son $0 \leq x \leq 1$ y $0 \leq y \leq 3-3x$. La línea $y = 3-3x$ cruza el eje $y$ en $y=3$ (cuando $x=0$) y el eje $x$ en $x=1$ (cuando $y=0$). El área es un triángulo con vértices en $(0,0)$, $(1,0)$, y $(0,3)$.
2.  **Cambiar el orden:** Para integrar primero con respecto a $x$, observamos que $y$ varía desde $0$ hasta $3$. Para un valor fijo de $y$, la variable $x$ varía desde la línea $x=0$ hasta la línea $y = 3-3x$, que se reescribe como $x = 1 - y/3$. Por lo tanto, los nuevos límites son $0 \leq y \leq 3$ y $0 \leq x \leq 1 - y/3$. La integral equivalente es:
    $$
    \int_{y=0}^{3} \int_{x=0}^{1-y/3} dx  dy.
    $$
3.  **Verificar el resultado:**
    *   **Orden original:** $\int_{x=0}^{1} \int_{y=0}^{3-3x} dy  dx = \int_{0}^{1} [y]_{0}^{3-3x} dx = \int_{0}^{1} (3-3x)  dx = \left[ 3x - \frac{3x^2}{2} \right]_{0}^{1} = 3 - \frac{3}{2} = \frac{3}{2}$.
    *   **Orden invertido:** $\int_{y=0}^{3} \int_{x=0}^{1-y/3} dx  dy = \int_{0}^{3} [x]_{0}^{1-y/3} dy = \int_{0}^{3} \left(1 - \frac{y}{3}\right)  dy = \left[ y - \frac{y^2}{6} \right]_{0}^{3} = \left(3 - \frac{9}{6}\right) - 0 = 3 - 1.5 = \frac{3}{2}$.
**Respuesta:** Ambas integrales valen $\frac{3}{2}$, lo que confirma que el cambio de orden es correcto.

---

### Ejemplo 3: Aplicación - Masa de una Lámina (Ejemplo 1, Sección 3)

**Problema:** Encuentre la masa de una lámina que tiene la forma de un cuarto de disco $x^2 + y^2 \leq 4$, $x > 0$, $y > 0$, si su densidad es $\rho(x, y) = x + y$.

**Solución:**
Este ejemplo ilustra las aplicaciones de las integrales múltiples, específicamente el cálculo de la masa.
1.  **Configurar la integral:** La masa $M$ es la integral de la densidad sobre el área $A$:
    $$
    M = \iint_A (x + y)  dx  dy.
    $$
2.  **Cambiar a coordenadas polares:** Dado que la región es un cuarto de disco, es mucho más fácil usar coordenadas polares: $x = r\cos\theta$, $y = r\sin\theta$, y $dx  dy = r  dr  d\theta$. La densidad se convierte en $x + y = r\cos\theta + r\sin\theta = r(\cos\theta + \sin\theta)$. Los límites son $0 \leq r \leq 2$ y $0 \leq \theta \leq \pi/2$.
3.  **Evaluar la integral:**
    $$
    M = \int_{\theta=0}^{\pi/2} \int_{r=0}^{2} r(\cos\theta + \sin\theta) \cdot r  dr  d\theta = \int_{0}^{\pi/2} (\cos\theta + \sin\theta)  d\theta \int_{0}^{2} r^2  dr.
    $$
    Resolvemos cada integral por separado:
    *   $\int_{0}^{2} r^2  dr = \left[ \frac{r^3}{3} \right]_{0}^{2} = \frac{8}{3}$.
    *   $\int_{0}^{\pi/2} (\cos\theta + \sin\theta)  d\theta = \left[ \sin\theta - \cos\theta \right]_{0}^{\pi/2} = (\sin(\pi/2) - \cos(\pi/2)) - (\sin(0) - \cos(0)) = (1 - 0) - (0 - 1) = 1 + 1 = 2$.
    Multiplicando los resultados: $M = 2 \cdot \frac{8}{3} = \frac{16}{3}$.
**Respuesta:** La masa de la lámina es $\frac{16}{3}$ unidades de masa.

---

### Ejemplo 4: Cambio de Variables - Coordenadas Polares (Ejemplo implícito en Sección 4)

**Problema:** Evalúe la integral $\iint_A e^{-x^2-y^2}  dx  dy$ donde $A$ es el primer cuadrante del plano ($x \geq 0$, $y \geq 0$).

**Solución:**
Este es un ejemplo clásico del uso del jacobiano para cambiar a coordenadas polares.
1.  **Cambiar a coordenadas polares:** Como en el ejemplo anterior, $x^2 + y^2 = r^2$ y $dx  dy = r  dr  d\theta$. La región $A$ en coordenadas polares es $0 \leq r < \infty$, $0 \leq \theta \leq \pi/2$.
2.  **Configurar la integral:**
    $$
    \iint_A e^{-x^2-y^2}  dx  dy = \int_{\theta=0}^{\pi/2} \int_{r=0}^{\infty} e^{-r^2} r  dr  d\theta.
    $$
3.  **Evaluar la integral interna:** Usamos la sustitución $u = r^2$, $du = 2r  dr$:
    $$
    \int_{0}^{\infty} e^{-r^2} r  dr = \frac{1}{2} \int_{0}^{\infty} e^{-u}  du = \frac{1}{2} \left[ -e^{-u} \right]_{0}^{\infty} = \frac{1}{2} (0 - (-1)) = \frac{1}{2}.
    $$
4.  **Evaluar la integral externa:**
    $$
    \int_{0}^{\pi/2} \frac{1}{2}  d\theta = \frac{1}{2} \cdot \left[ \theta \right]_{0}^{\pi/2} = \frac{1}{2} \cdot \frac{\pi}{2} = \frac{\pi}{4}.
    $$
**Respuesta:** $\iint_A e^{-x^2-y^2}  dx  dy = \frac{\pi}{4}$.