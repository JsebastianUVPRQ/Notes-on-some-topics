# Enunciados de Ejercicios - Quiz de Métodos Matemáticos

## Ejercicio 1
La trayectoria de un cuerpo celeste alrededor de otra estrella está descrita por:
$$r(\theta) = \frac{r_0}{1+\varepsilon \cos \theta}$$
donde $r_0$ es una constante que depende de los parámetros de la órbita, y $\varepsilon$ es la excentricidad.

En coordenadas polares, el área de una sección circular entre ángulos $\theta_1$ y $\theta_2$ viene dada por:
$$A = \frac{1}{2} \int_{\theta_1}^{\theta_2} r^2(\theta)d\theta$$

a) Deduzca una expresión general para hallar el área de la órbita entre $\theta_1$ y $\theta_2$ en términos de una integral. Para una órbita completa, indique cómo se puede utilizar el teorema del residuo para calcular el área indicando la sustitución apropiada, el contorno y la nueva integral.

b) Encuentre, en términos de los parámetros dados, el área de una trayectoria circular entre ángulos $\theta_1$ y $\theta_2$ y el área de una trayectoria circular completa.

c) Explique por qué para las trayectorias parabólicas e hiperbólicas el área no se puede calcular usando el teorema del residuo. ¿Podría ser calculada usando algún otro método? De una interpretación física a su resultado.

d) Evaluar el área de una trayectoria elíptica utilizando el teorema del residuo.

e) Si la excentricidad de una elipse es $\varepsilon = \sqrt{a^2-b^2}/a$, donde $a$ es el eje mayor y $b$ el eje menor, usar el resultado anterior para hallar $r_0$ para una elipse.

## Ejercicio 2
Cuando se analizan colisiones en mecánica cuántica encontramos la integral:
$$I = \int_{-\infty}^{\infty} \frac{\sin t}{t} e^{ipt}dt$$

a) Descomponer el $\sin t$ como una suma de exponenciales complejas para escribir $I$ como la suma de dos integrales. Exprésela como $I = I_+ + I_-$.

b) Para los casos $p < -1$, $-1 < p < 0$, $0 < p < 1$ y $p > 1$, describir el contorno que debe ser usado para calcular cada integral ($I_+$ e $I_-$).

c) Evaluar cada integral para los casos mencionados.

d) Juntar los resultados anteriores y decir el valor de $I$ cuando $|p| > 1$ y cuando $|p| < 1$.

e) Explicar qué sucede con $I$ cuando $p = \pm 1$.

## Ejercicio 3
Al analizar el problema de dispersión en mecánica cuántica:
$$I(\sigma) = \int_{-\infty}^{\infty} \frac{x \sin x}{x^2 - \sigma^2} dx$$
donde $\sigma > 0$.

a) Escriba $\sin x$ como suma de exponenciales complejas para escribir $I(\sigma)$ como $I(\sigma) = I_1(\sigma) + I_2(\sigma)$.

b) Encuentre los polos de cada integral y escoja el contorno apropiado para evaluar cada una. Ubique los polos en los contornos y explique por qué el valor de la integral no depende si encerramos o no las singularidades.

c) Evaluar cada integral utilizando el teorema del residuo y obtener la integral total.

d) Para encontrar la solución esperada (onda viajera), considere $\pm\sigma \to \pm\sigma \pm i\varepsilon$ con $\varepsilon > 0$. Realice de nuevo las integrales, tome el límite $\varepsilon \to 0$ y explique por qué esta integral es compleja.

## Ejercicio 4
a) Resolver la integral:
$$f(t) = -\frac{1}{2\pi} \int_{-\infty}^{\infty} \frac{e^{i\omega t} d\omega}{(b+i\omega)(\omega^2+a^2)}$$
donde $a > 0$ y $b > 0$.

b) Mostrar que cuando $b = a$:
$$f(t) = -\frac{e^{-a|t|}}{4a^2} - \frac{t}{2a}H(t)e^{-at}$$
donde $H(t)$ es la función Heaviside.

## Ejercicio 5
Evaluar la siguiente integral:
$$\int_{0}^{\infty} \frac{x^2 dx}{x^6 + a^6}, \quad a > 0$$

## Ejercicio 6
Sea $P(x) = ax^2 + bx + c$ un polinomio de grado 2 tal que $b^2 < 4ac$. Evaluar la integral:
$$\int_{-\infty}^{\infty} \frac{x dx}{P(x)^2}$$
Explicar por qué se requiere la condición $b^2 < 4ac$.