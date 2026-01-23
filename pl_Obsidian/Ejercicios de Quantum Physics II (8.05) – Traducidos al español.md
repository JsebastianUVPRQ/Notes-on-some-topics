
## Assignment 1 (ps1)

**1. Propiedades de una función de onda. [10 puntos]**  
Una partícula de masa $m$ en un potencial unidimensional $V(x)$ tiene la función de onda  
$$
\psi (x) = Nx\exp \left(-\frac{1}{2}\alpha x^2\right),\quad \alpha >0.
$$  
(a) Normalice $\psi (x)$ para determinar $N$. ¿Cuánto vale $\langle \hat{x} \rangle$? ¿Y $\langle \hat{x}^2 \rangle$?  
(b) ¿Cuánto vale $\langle \hat{p} \rangle$? ¿Y $\langle \hat{p}^2 \rangle$?  
(c) ¿Es $\psi (x)$ un estado propio de posición? ¿Es $\psi (x)$ un estado propio de momento? Explique.  
(d) Suponga que $V(x) = 0$. ¿Cuánto vale $\langle \hat{H} \rangle$?  
(e) Suponga que no se conoce $V(x)$, pero $\psi (x)$ es un estado propio de energía. Encuentre el potencial $V(x)$ y el valor propio de energía $E$, asumiendo $V(0) = 0$. ¿Podría $\psi (x)$ ser la función de onda del estado fundamental para la partícula?

**2. La energía debe superar el valor mínimo del potencial. [5 puntos]**  
Considere la ecuación de Schrödinger independiente del tiempo para una partícula de energía $E$ en un potencial $V(x)$, con $x \in (-\infty , \infty)$:  
$$
\frac{d^2\psi}{dx^2} = \frac{2m}{\hbar^2} [V(x) - E]\psi (x). \quad (1)
$$  
Sin pérdida de generalidad se puede asumir que $\psi (x)$ es real. Suponga que el potencial está acotado inferiormente,  
$$
V(x)\geq V_{\mathrm{min}},\ \text{para toda } x,
$$  
donde $V_{\mathrm{min}}$ es el valor mínimo del potencial.  
Demuestre que $E > V_{\mathrm{min}}$ para que existan soluciones normalizables. Para ello, suponga $E\leq V_{\mathrm{min}}$ e intente usar la ecuación (1) e integración para llegar a una contradicción clara.

**3. Tres funciones delta [15 puntos]**  
Una partícula de masa $m$ se mueve en una dimensión, sujeta a una función de energía potencial $V(x)$ que es la suma de tres funciones delta atractivas equiespaciadas:  
$$
V(x) = -V_0a\sum_{n = -1}^{1}\delta (x - na),\ \text{donde } V_0 > 0,\ a > 0 \text{ son constantes.}
$$  
(a) Calcule la discontinuidad en la primera derivada de la función de onda en $x = -a$, 0 y $a$.  
(b) Considere el posible número y ubicación de nodos en las funciones de onda de estados ligados para este sistema.  
(i) ¿Cuántos nodos son posibles en la región $x > a$?  
(ii) ¿Cuántos nodos son posibles en la región $0 < x < a$?  
(iii) ¿Puede haber un nodo en $x = a$?  
(iv) ¿Puede haber un nodo en $x = 0$?  
(c) Para $V_0$ arbitrariamente grande, ¿cuántos estados ligados hay? Dibújelos cualitativamente.  
(d) Derive la ecuación que determina la energía para el estado ligado antisimétrico de menor energía. Encuentre el valor mínimo de $V_0$ para que exista el estado ligado.

**4. Estimaciones para el pozo cuadrado finito [10 puntos]**  
Considere el potencial de pozo cuadrado finito de la sección 2.6 de Griffiths:  
$$
V(x) = -V_{0}\ \text{para } - a\leq x\leq a,\ \text{y } V(x) = 0\ \text{para } |x| > a.
$$  
(a) Número de estados ligados para un pozo profundo. Suponga que el pozo es suficientemente profundo y/o ancho de modo que $z_{0}$, definido como  
$$
z_{0}\equiv \frac{a}{\hbar}\sqrt{2mV_{0}},
$$  
es un número grande. Encuentre una estimación para el número de estados ligados en este pozo usando el resultado de que el $k$-ésimo estado ligado tiene $k - 1$ nodos. Confirme que su resultado es una buena aproximación comparando con la Figura 2.18 del libro.  
(b) Energía del estado ligado para un pozo somero. Suponga ahora que el potencial es muy somero y/o estrecho de modo que $z_{0}$ es muy pequeño y como resultado hay solo un estado ligado. Use las ecuaciones relevantes del problema (ver Griffiths) para estimar la energía $E$ de este estado en términos de $V_{0}$ y $z_{0}$ (es decir, encuentre el término principal de la energía en la expansión en términos de $z_{0}$, cuando $z_{0} \to 0$).

**5. Valor esperado $\langle \hat{p} \rangle$ del momento. [5 puntos]**  
(a) La función de onda en el espacio de coordenadas de una partícula es real y de cuadrado integrable salvo por una fase multiplicativa arbitraria:  
$$
\psi (x) = e^{i\alpha}\phi (x),
$$  
con $\alpha$ real y constante, y $\phi (x)$ real. Demuestre que el valor esperado del momento es cero.  
(b) Considere ahora la función de onda  
$$
\psi (x) = \phi_{1}(x) + e^{i\alpha}\phi_{2}(x),
$$  
donde $\phi_{1}(x)$ y $\phi_{2}(x)$ son cada una real y de cuadrado integrable. ¿Cuánto vale $\langle \hat{p} \rangle$? La respuesta puede expresarse como una función de $\alpha$ multiplicada por una integral que involucra las funciones $\phi_{2}$ y $d\phi_{1} / dx$ (o $\phi_{1}$ y $d\phi_{2} / dx$). ¿Para qué valores de $\alpha$ podemos estar seguros de que $\langle \hat{p} \rangle$ es cero sin tener más información sobre $\phi_{1}$ y $\phi_{2}$?  
(c) Considere esta vez la función de onda  
$$
\psi (x) = e^{ikx}\phi (x),
$$  
con $k$ real y constante, y $\phi (x)$ real. Calcule $\langle \hat{p} \rangle$.

**6. Corriente de probabilidad conservada. [10 puntos]**  
Suponga que $\Psi (x,t)$ obedece la ecuación de Schrödinger unidimensional,  
$$
-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2}\Psi (x,t) + V(x)\Psi (x,t) = i\hbar \frac{\partial}{\partial t}\Psi (x,t). \quad (2)
$$  
(a) Derive la ley de conservación para la probabilidad,  
$$
\frac{\partial\rho}{\partial t} +\frac{\partial J}{\partial x} = 0, \quad (3)
$$  
donde $\rho (x,t)$ es la densidad de probabilidad y $J(x,t)$ es la densidad de corriente de probabilidad  
$$
\rho (x,t) = \Psi^{*}\Psi ,\quad J(x,t) = \frac{\hbar}{m}\mathrm{Im}\left(\Psi^{*}\frac{\partial\Psi}{\partial x}\right). \quad (4)
$$  
¿Cuáles son las unidades de $\rho$ y $J$?  
(b) Explique por qué (3) es una ley de conservación para la probabilidad. Para ello, defina  
$$
P_{ab}(t)\equiv \int_a^b dx\rho (x,t),
$$  
evalúe $\frac{dP_{ab}}{dt}$ en términos de las corrientes e interprete su respuesta. Demuestre luego que una función de onda $\Psi (x,t)$ normalizada en el tiempo $t$ permanece normalizada en tiempos posteriores.  
(c) En lo siguiente consideramos estados estacionarios con funciones de onda espaciales $\psi (x)$. Calcule la corriente de probabilidad $J$ para $\psi (x) = e^{i\alpha (x)}\phi (x)$ donde $\alpha (x)$ y $\phi (x)$ son reales. Demuestre que  
$$
\frac{J(x)}{\rho(x)} = \frac{\hbar}{m}\alpha '(x).
$$  
Explique por qué la razón $J / \rho$ puede verse como la velocidad local de la partícula cuántica descrita por $\psi (x)$.  
(d) Considere $\psi (x) = Ae^{ipx / \hbar} + Be^{-ipx / \hbar}$, con $A$ y $B$ constantes complejas. Calcule $J(x)$. ¿Hay términos cruzados en $J$ entre las partes de izquierda y derecha de $\psi$?

**7. Griffiths Problema 2.38, p.85 [10 puntos]**

---

## Assignment 2 (ps2)

**1. Pozo cuadrado con función delta [10 puntos]**  
Considere el pozo infinito unidimensional $0\leq x\leq a$. Añadimos una función delta en el centro del pozo  
$$
V(x) = V_0a\delta \Big(x - \frac{a}{2}\Big),V_0 > 0, \quad (1)
$$  
con $V_{0}$ un valor grande con unidades de energía. De hecho, $V_{0}$ es grande comparado con la escala natural de energía del pozo:  
$$
\frac{V_0}{(\frac{a}{ma^2})}\equiv \gamma \gg 1. \quad (2)
$$  
El número adimensional $\gamma$ se toma grande. La función delta crea una barrera entre el lado izquierdo y el derecho del pozo. A medida que la intensidad de la función delta $V_{0}$ tiende a infinito podemos obtener una situación singular.  
Calcule la energía del estado fundamental, incluyendo correcciones de orden $1 / \gamma$ pero ignorando órdenes superiores. Compare con la energía del primer estado excitado. ¿Qué sucede con la diferencia de energía entre estos dos niveles?

**2. Nodos en funciones de onda [10 puntos]**  
Hemos escrito la ecuación de Schrödinger en la forma  
$$
\psi^{\prime \prime} + (\mathcal{E} - U(x))\psi = 0.
$$  
Sea $\psi_{k}$ el estado propio de energía con energía $\mathcal{E}_{k}$ y $\psi_{k + 1}$ el estado propio de energía con energía $\mathcal{E}_{k + 1}$ mayor que $\mathcal{E}_{k}$.  
(a) Demuestre que  
$$
\left(\psi_{k + 1}\psi_{k}^{\prime} - \psi_{k}\psi_{k + 1}^{\prime}\right)\bigg|_{a}^{b} = (\mathcal{E}_{k + 1} - \mathcal{E}_{k})\int_{a}^{b}dx\psi_{k}\psi_{k + 1}. \quad (1)
$$  
(b) Sean ahora $a,b$ con $a< b$ dos ceros sucesivos de $\psi_{k}(x)$ y asuma, por conveniencia, que $\psi_{k}(x) > 0$ para $a< x< b$. Usando (1) demuestre que $\psi_{k + 1}$ debe cambiar de signo en el intervalo $(a,b)$. Es decir, $\psi_{k + 1}$ debe tener al menos un cero entre cada par de ceros de $\psi_{k}$. Sugerencia: considere el signo de cada lado de la ecuación (1) bajo la suposición de que $\psi_{k + 1}$ no cambia de signo en $(a,b)$.

**3. Desarrollo del principio variacional [10 puntos]**  
(a) Considere funciones de onda de prueba normalizadas $\psi (x)$ que son ortogonales a la función de onda del estado fundamental $\psi_{1}$: $\int dx\psi_{1}^{*}(x)\psi (x) = 0$. Demuestre que la energía del primer excitado $E_{2}$ está acotada como:  
$$
E_{2}\leq \int dx\psi^{*}(x)H\psi (x).
$$  
Este resultado tiene una generalización clara (que no necesita probar): funciones de onda de prueba ortogonales a los $n$ estados propios de menor energía dan una cota superior para la energía del estado $(n + 1)$-ésimo.  
(b) Asuma que podemos usar funciones de onda reales y considere el funcional  
$$
\mathcal{F}(\psi) = \frac{\int dx\psi(x)H\psi(x)}{\int dx\psi(x)\psi(x)}.
$$  
Este funcional tiene una propiedad notable: ¡es estacionario en los estados propios de energía! Hará un cálculo que confirma esto para un caso especial, dándole intuición sobre la naturaleza del punto crítico. Tomemos  
$$
\psi (x) = \psi_{2}(x) + \sum_{n = 1}\epsilon_{n}\psi_{n}(x), \quad (3)
$$  
Este es el primer estado excitado perturbado por pequeñas adiciones de los otros estados propios de energía: todas las $\epsilon$ se toman pequeñas. Evalúe el funcional $\mathcal{F}$ para esta función de onda incluyendo términos cuadráticos en las $\epsilon$ pero ignorando términos cúbicos o de orden superior. Confirme que todos los términos lineales en $\epsilon$ se cancelan, mostrando que el funcional es efectivamente estacionario en $\psi_{2}(x)$. ¿Alguna $\epsilon$ desaparece a orden cuadrático? Discuta la naturaleza del punto crítico (máximo, mínimo, direcciones planas, punto silla).

**4. Potenciales atractivos unidimensionales tienen un estado ligado [10 puntos]**  
(Basado en el Ejercicio 5.2.2 de Shankar (p.163) parte (b).) Use el principio variacional para probar que cualquier potencial atractivo en una dimensión debe tener al menos un estado ligado. Tomamos un potencial atractivo como uno donde el potencial tiende a cero en más y menos infinito: $\lim_{x\to \pm \infty}|V(x)| = 0$, es continuo a trozos, nunca positivo, y no idénticamente cero. Note que se sigue que $V(x) = - |V(x)|$.  
Para hacer esto, considere la función de onda de prueba  
$$
\psi_{\alpha}(x) = \left(\frac{\alpha}{\pi}\right)^{1 / 4}e^{-\alpha x^{2} / 2},
$$  
e intente demostrar que el valor esperado $E(\alpha)$ de $\hat{H}$ en este estado  
$$
E(\alpha) = \int dx\psi_{\alpha}(x)\hat{H}\psi_{\alpha}(x),\quad \hat{H} = -\frac{\hbar^2}{2m}\frac{d^2}{dx^2} -|V(x)|.
$$  
puede hacerse negativo para una elección adecuada de $\alpha$. Encontrar la contribución del término potencial a $E(\alpha)$ es desafiante. Para un $V(x)$ atractivo arbitrario no puede calcularse explícitamente, pero basta con encontrar una cota.  
Se puede obtener una cota encontrando un punto $x_0$ donde el potencial es continuo y toma un valor negativo (tal punto debe existir). Suponga  
$$
|V(x_0)| = 2v_0 > 0.
$$  
Dado que el potencial tiende a cero en más y menos infinito, hay un intervalo finito $[x_{1},x_{2}]$ alrededor de $x_{0}$ (con $x_{1}< x_{0}< x_{2}$, $\Delta \equiv x_{2} - x_{1}$) para el cual  
$$
|V(x)|\geq v_0.
$$  
Explique cómo el término potencial puede acotarse reemplazando $V(x)$ por un potencial $\bar{V}$ que satisface $\bar{V} (x) = - v_{0}$ para $x\in [x_{1},x_{2}]$ y cero en otro lugar.

**5. Análisis variacional del potencial $V(x) = \alpha x^{4}$ [20 puntos]**  
Estamos considerando la ecuación de Schrödinger  
$$
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} +\alpha x^4\psi = E\psi .
$$  
(a) Realice un cambio de coordenadas, definiendo $x = \beta u$ y determine la constante $\beta$ de modo que la ecuación diferencial tome la forma  
$$
-\frac{1}{2}\frac{d^2\psi}{du^2} +(u^4 -e)\psi = 0.
$$  
¿Cómo se expresa $E$ en términos de la constante adimensional $e$?  
(b) Use un manipulador algebraico que pueda manejar ecuaciones diferenciales para determinar el valor de la constante $e$ para la energía del estado fundamental con una precisión de seis dígitos $e\simeq 0.67$. Para esto intente integrar la ecuación numéricamente comenzando en $u = 0$ definiendo $\psi (0) = 1$ y $\psi^{\prime}(0) = 0$ (¿por qué esta derivada es cero?). Solo para valores discretos de $e$ la solución no explota cuando $u$ se hace grande. El menor de tales valores de $e$ es el que busca.  
(c) Escriba una función de onda candidata para el principio variacional y determine una cota superior para la energía del primer excitado.  
(d) Use el manipulador algebraico para determinar el siguiente valor más bajo de $e$ (con precisión de tres dígitos) y compare con su estimación variacional.

**6. Una propiedad de matrices [5 puntos]**  
Podemos definir una función de una matriz $\mathbf{M}$ mediante una serie de potencias. Si $f(z)$ es una función con una expansión en serie de Taylor $f(z) = \sum_{n = 0}^{\infty}f_{n}z^{n}$, entonces definimos $f(\mathbf{M})\equiv \sum_{n = 0}^{\infty}f_{n}\mathbf{M}^{n}$. Sea $\mathbf{M}$ la matriz  
$$
\mathbf{M} = \begin{pmatrix} 0 & -i\\ i & 0 \end{pmatrix}
$$  
Demuestre que $e^{i\mathbf{M}\theta}$ toma la forma  
$$
e^{i\mathbf{M}\theta} = A(\theta)\mathbf{1} + B(\theta)\mathbf{M}, \quad (4)
$$  
donde 1 es la matriz identidad $2\times 2$ y $A$ y $B$ son funciones que debe determinar. ¿Cuál es la propiedad algebraica de una matriz $\mathbf{M}$ de tamaño arbitrario que llevaría a este resultado?

---

## Assignment 3 (ps3)

**1. Estados de espín un medio a lo largo de un eje arbitrario. [10 puntos]**  
(a) Un estado de espín (no normalizado) está dado por  
$$
(1 + i)| + \rangle -(1 + i\sqrt{3})| - \rangle .
$$  
¿En qué dirección apunta este estado de espín?  
(b) Considere la siguiente secuencia de experimentos:  
i. Primero, prepare un haz de átomos de espín-1/2 todos en el estado $| + \rangle$ pasando un haz por un dispositivo Stern-Gerlach orientado en la dirección $\hat{z}$, y conservando solo aquellos átomos medidos con valor propio $+h / 2$.  
ii. Luego, pase estos átomos por un segundo dispositivo Stern-Gerlach diseñado para medir $\hat{S}_{\vec{n}}$, para algún $\vec{n}$ en el plano $(x,z)$. Es decir, $\phi = 0$; $\theta \neq 0$. Conserve solo aquellos átomos que tengan valor propio $h / 2$.  
iii. Finalmente, pase los átomos que quedan por un tercer experimento Stern-Gerlach, orientado en la misma dirección $(z)$ que el primero.  
De todos los átomos que entraron al segundo imán, ¿qué fracción son encontrados por el tercer imán en el estado $| + \rangle$? ¿Qué fracción son encontrados en el estado $| - \rangle$? ¿Qué fracción nunca llegó al tercer imán? Sus respuestas serán, por supuesto, funciones del ángulo $\theta$. Argumente que sus respuestas tienen sentido para $\theta = 0$ ($\vec{n}$ en la dirección $z$), $\theta = \pi /2$ ($\vec{n}$ en la dirección $x$) y $\theta = \pi$ ($\vec{n}$ en la dirección $- z$).

**2. Solapamiento de dos estados de espín un medio. [10 puntos]**  
Considere un estado de espín $|\mathbf{n}; + \rangle$ donde $\mathbf{n}$ es el vector unitario definido por los ángulos polares $\theta$ y $\phi$ y el estado de espín $|\mathbf{n}^{\prime}; + \rangle$ donde $\mathbf{n}^{\prime}$ es el vector unitario definido por los ángulos polares $\theta^{\prime}$ y $\phi^{\prime}$. Sea $\gamma$ el ángulo entre los vectores $\mathbf{n}$ y $\mathbf{n}^{\prime}$:  
$$
\mathbf{n}\cdot \mathbf{n}^{\prime} = \cos \gamma .
$$  
Demuestre mediante cálculo directo que el solapamiento de los estados de espín asociados está controlado por la mitad del ángulo entre los vectores unitarios:  
$$
\left|\langle \mathbf{n}^{\prime}; + |\mathbf{n}; + \rangle \right|^{2} = \cos^{2}\frac{\gamma}{2}.
$$

**3. Rotación de estados de espín. [10 puntos]**  
Definimos el operador $\hat{R}_{\mathbf{n}}(\alpha)$, con $\alpha$ real y $\mathbf{n}$ un vector unitario, por  
$$
\hat{R}_{\mathbf{n}}(\alpha)\equiv \exp \Bigl (-\frac{i\alpha\hat{S}_{\mathbf{n}}}{\hbar}\Bigr) = \exp \Bigl (-i\frac{\alpha}{2}\mathbf{n}\cdot \pmb {\sigma}\Bigr),
$$  
donde notamos que $\hat{S}_{\mathbf{n}} = \frac{\hbar}{2}\mathbf{n}\cdot \pmb {\sigma}$.  
(a) Usando la definición de la función exponencial y propiedades de las matrices $\sigma$, demuestre que  
$$
\hat{R}_{\mathbf{n}}(\alpha) = I\cos \frac{\alpha}{2} -i\pmb {\sigma}\cdot \mathbf{n}\sin \frac{\alpha}{2}.
$$  
Verifique por cálculo directo que $\hat{R}_{\mathbf{n}}(\alpha)$ es unitario.  
(b) Por brevedad escribimos $\hat{R}_{y}(\alpha)$ para $\hat{R}_{\hat{\epsilon}_{y}}(\alpha)$. Evalúe el operador  
$$
\hat{R}_{y}(\alpha)\hat{S}_{z}\hat{R}_{y}(\alpha)^{\dagger}
$$  
en términos de $\hat{S}_{x},\hat{S}_{y}$ y $\hat{S}_{z}$.  
(c) Encuentre el estado obtenido al actuar con $\hat{R}_{y}(\alpha)$ sobre $| + \rangle$. ¿Para qué operador es el estado resultante un estado propio con valor propio $\hbar /2$? Explique por qué podemos pensar en $\hat{R}_{y}(\alpha)$ como un operador de rotación. (Similarmente, se puede mostrar que $\hat{R}_{\mathbf{n}}(\alpha)$ es un operador de rotación alrededor de un eje apuntando a lo largo de $\mathbf{n}$.)

**4. Desigualdad de Schwarz y desigualdad del triángulo [15 puntos]**  
(a) Para espacios vectoriales reales el producto punto familiar satisface la desigualdad de Schwarz  
$$
(\vec{a}\cdot \vec{b})^2\leq (\vec{a}\cdot \vec{a})(\vec{b}\cdot \vec{b}),\ \text{o }|\vec{a}\cdot \vec{b}|\leq |\vec{a} ||\vec{b} |. \quad (1)
$$  
Note que en la última desigualdad, las barras verticales en el lado izquierdo denotan valor absoluto, pero en el lado derecho denotan longitud del vector. Demuestre esta desigualdad como sigue. Considere el vector $\vec{a} - \lambda \vec{b}$, con $\lambda$ una constante real. Note que  
$$
f(\lambda)\equiv (\vec{a} -\lambda \vec{b})\cdot (\vec{a} -\lambda \vec{b})\geq 0,
$$  
para todo $\lambda$ y por tanto el mínimo sobre $\lambda$ sigue siendo no negativo  
$$
\min_{\lambda}f(\lambda)\geq 0.
$$  
¿Cuándo se satura la desigualdad de Schwarz?  
(b) Para un espacio vectorial complejo la desigualdad de Schwarz dice  
$$
|\langle a|b\rangle |^2\leq \langle a|a\rangle \langle b|b\rangle ,\ \text{o }|\langle a|b\rangle |\leq |a||b|. \quad (2)
$$  
Aquí la norma se define por $|a|^{2} = \langle a|a\rangle$. Demuestre esta desigualdad usando el vector $|v(\lambda)\rangle \equiv |a\rangle - \lambda |b\rangle$, con $\lambda$ una constante compleja y notando que  
$$
f(\lambda)\equiv \langle v(\lambda)|v(\lambda)\rangle \geq 0
$$  
para todo $\lambda$ de modo que su mínimo sobre $\lambda$ es no negativo. ¿Cuándo se satura la desigualdad de Schwarz?  
(c) Para un espacio vectorial complejo se tiene la desigualdad del triángulo  
$$
|a + b|\leq |a| + |b|, \quad (3)
$$  
donde la norma se define por $|a|^{2} = \langle a|a\rangle$. Demuestre esta desigualdad partiendo de la expansión de $|a + b|^{2}$. Tendrá que usar la propiedad $|\mathrm{Re}(z)|\leq |z|$, que vale para cualquier número complejo $z$, así como la desigualdad de Schwarz. Demuestre que la igualdad en (3) se da si y solo si $a = cb$ para $c$ una constante real positiva.

**5. Ejercicios de álgebra lineal. [10 puntos]**  
(a) (del libro de Axler) Considere el siguiente enunciado: $U_{1},U_{2}$ y $W$ son subespacios de $V$ y se cumple  
$$
V = U_{1}\oplus W\quad \mathrm{y}\quad V = U_{2}\oplus W.
$$  
¿Puede concluir que $U_{1} = U_{2}$? Es decir, ¿son el mismo subespacio? Si sí, demuéstrelo. Si no, dé un contraejemplo.  
(b) Demuestre que $\mathbb{F}^{\infty}$ (como se define en la ecuación (1.4)) es un espacio vectorial de dimensión infinita. (Comentario: Puede haber varias formas de mostrar esto. Me resultó útil usar el resultado (enunciado en las notas) de que en un espacio vectorial de dimensión finita la longitud de cualquier lista generadora debe ser mayor o igual que la longitud de cualquier lista de vectores linealmente independientes.)  
(c) Demuestre que $T$ es inyectivo si y solo si $\text{null } T = \{0\}$.

**6. Cantidades independientes de la base. [10 puntos]**  
Considere un espacio vectorial $V$ y un cambio de base de $(v_{1},\ldots v_{n})$ a $(u_{1},\ldots u_{n})$ definido por el operador lineal $A:v_{k}\to u_{k}$, para $k = 1,\ldots ,n$. El operador es claramente invertible porque, definiendo $B:u_{k}\to v_{k}$, tenemos $BA:v_{k}\to v_{k}$, mostrando que $BA = I$ y $AB:u_{k}\to u_{k}$, mostrando que $AB = I$. Así, $B$ es la inversa de $A$.  
(a) Considere las ecuaciones de mapeo  
$$
u_{k} = Av_{k},\qquad \mathrm{y}\qquad v_{k} = B u_{k},
$$  
y escríbalas explícitamente usando la representación matricial de $A$ en la base $v$ y la representación matricial de $B$ en la base $u$. Demuestre que estas dos matrices son inversas una de la otra.  
Considere ahora el operador lineal $T$ en $V$. Sea $T_{ij}(\{v\})$ su representación matricial en la base $v$ y $T_{ij}(\{u\})$ su representación matricial en la base $u$.  
(b) Encuentre una relación matricial entre $T_{ij}(\{v\})$ y $T_{ij}(\{u\})$, escrita en términos de la matriz representante de $A$ y su inversa.  
(c) Demuestre que la traza de la representación matricial de $T$ es independiente de la base.  
(d) Demuestre que el determinante de la representación matricial de $T$ es independiente de la base.

---

## Assignment 4 (ps4)

**1. Identidades para conmutadores (Basado en Griffiths Prob.3.13) [10 puntos]**  
En el siguiente problema $A$, $B$ y $C$ son operadores lineales. También lo son $q$ y $p$.  
(a) Demuestre la siguiente identidad de conmutador:  
$$
[A,BC] = [A,B]C + B[A,C].
$$  
Esta es la propiedad de derivación del conmutador: el conmutador con $A$, es decir el objeto $[A, \cdot ]$, actúa como una derivada sobre el producto $BC$. En el resultado el conmutador se toma primero con $B$ y luego con $C$ mientras el operador que queda intacto se posiciona en el lugar esperado.  
(b) Demuestre la identidad de Jacobi:  
$$
[[A,B],C] + [[B,C],A] + [[C,A],B] = 0.
$$  
(c) Usando $[q, p] = i\hbar$ y el resultado de (a), demuestre que  
$$
[q^n,p] = i\hbar nq^{n - 1}.
$$  
(d) Para cualquier función $f(q)$ que pueda expandirse en una serie de potencias en $q$, use (c) para mostrar  
$$
[f(q),p] = i\hbar f'(q).
$$  
(e) En el espacio de funciones dependientes de la posición, el operador $f(x)$ actúa multiplicativamente y $p$ actúa como $\frac{\hbar}{i}\frac{\partial}{\partial x}$. Calcule $[f(x), p]$ dejando que este operador actúe sobre una función de onda arbitraria.

**2. Identidades de operadores útiles y traslaciones [10 puntos]**  
Suponga que $A$ y $B$ son dos operadores que no conmutan, $[A, B] \neq 0$.  
(a) Sea $t$ una variable formal. Demuestre que  
$$
\frac{d}{dt} e^{t(A + B)} = (A + B)e^{t(A + B)} = e^{t(A + B)}(A + B).
$$  
(b) Ahora suponga $[A,B] = c$, donde $c$ es un $c$-número (un número complejo por el operador identidad). Demuestre que  
$$
e^{A}Be^{-A} = B + c. \quad (1)
$$  
[Sugerencia: Defina una función con valor de operador $F(t)\equiv e^{tA}Be^{- tA}$. ¿Cuánto vale $F(0)$? Derive una ecuación diferencial para $F(t)$ e intégrela.]  
Comentario: La ecuación (1) es un caso especial del lema de Hadamard, que se considerará más abajo.  
(c) Sea $a$ un número real y $\hat{p}$ el operador momento. Demuestre que el operador unitario de traslación  
$$
\hat{T} (a)\equiv e^{-ia\hat{p} /\hbar}
$$  
traslada el operador posición:  
$$
\hat{T}^{\dagger}(a)\hat{x}\hat{T} (a) = \hat{x} +a.
$$  
Si un estado $|\psi \rangle$ se describe por la función de onda $\langle x|\psi \rangle = \psi (x)$, demuestre que el estado $\hat{T} (a)|\psi \rangle$ se describe por la función de onda $\psi (x - a)$.

**3. Demostración del lema de Hadamard [10 puntos]**  
Demuestre que para dos operadores $A$ y $B$, tenemos  
$$
e^{A}Be^{-A} = B + [A,B] + \frac{1}{2!} [A,[A,B]] + \frac{1}{3!} [A,[A,[A,B]]] + \dots . \quad (1)
$$  
Defina $f(t)\equiv e^{tA}Be^{- tA}$ y calcule las primeras derivadas de $f(t)$ evaluadas en $t = 0$. Luego use expansiones de Taylor. Calcular explícitamente las primeras tres derivadas basta para obtener (1).  
Haga las cosas a todo orden encontrando la forma del término $(n + 1)$-ésimo en el lado derecho de (1). Para escribir la respuesta de forma ordenada definimos el operador $\operatorname {ad}A$ que actúa sobre operadores $X$ para dar operadores mediante el conmutador  
$$
\operatorname {ad}A(X)\equiv [A,X].
$$  
Confirme que con esta notación, la versión completa de la ecuación (1) se vuelve  
$$
e^{A}Be^{-A} = e^{\mathrm{ad}A}(B).
$$

**4. Caso especial del Teorema de Baker-Haussdorf [10 puntos]**  
Considere dos operadores $A$ y $B$, tales que $[A,B] = cI$, donde $c$ es un número complejo e $I$ es el operador identidad. Demostrará aquí la siguiente identidad  
$$
e^{A + B} = e^{B}e^{A}e^{c / 2} = e^{A}e^{B}e^{-c / 2}. \quad (2)
$$  
Para este propósito considere la función con valor de operador  
$$
G(t)\equiv e^{t(A + B)}e^{-tA}.
$$  
(a) Usando propiedades de operadores e identidades que derivó previamente, demuestre que  
$$
G^{-1}\frac{d}{dt} G(t) = B + ct. \quad (3)
$$  
(b) Note que (3) es equivalente a $\frac{d}{dt} G(t) = G(t)(B + ct)$. Verifique que la solución a esta ecuación es  
$$
G(t) = G(0)e^{tB}e^{\frac{1}{2} ct^2}. \quad (4)
$$  
(c) Considere $G(1)$ para probar la primera igualdad en (2). Renombre los operadores para obtener la otra igualdad.  
Comentario: La fórmula completa de Baker-Hausdorff es de la forma  
$$
e^{X}e^{Y} = e^{X + Y + \frac{1}{2} [X,Y] + \frac{1}{12} ([X,[X,Y]] - [Y,[X,Y]]) + \dots}
$$  
y no hay una forma cerrada simple para $X$ e $Y$ generales.

**5. Bras y kets. [5 puntos]**  
Considere un espacio de Hilbert tridimensional con una base ortonormal $|1\rangle$, $|2\rangle$, $|3\rangle$. Usando constantes complejas $a$ y $b$ defina los kets  
$$
|\psi \rangle = a|1\rangle -b|2\rangle +a|3\rangle ;\quad |\phi \rangle = b|1\rangle +a|2\rangle .
$$  
(a) Escriba $\langle \psi |$ y $\langle \phi |$. Calcule $\langle \phi |\psi \rangle$ y $\langle \psi |\phi \rangle$. Verifique que $\langle \phi |\psi \rangle = \langle \psi |\phi \rangle^*$.  
(b) Exprese $|\psi \rangle$ y $|\phi \rangle$ como vectores columna en la base $|1\rangle$, $|2\rangle$, $|3\rangle$ y repita (a).  
(c) Sea $A = |\phi \rangle \langle \psi |$. Encuentre la matriz $3 \times 3$ que representa a $A$ en la base dada.  
(d) Sea $Q = |\psi \rangle \langle \psi | + |\phi \rangle \langle \phi |$. ¿Es $Q$ hermítica? Dé un argumento simple (sin cálculo) para mostrar que $Q$ tiene un valor propio cero.


**7. Proyecciones ortogonales y aproximaciones (basado en Axler) [15 puntos]**  
Considere un espacio vectorial $V$ con un producto interno y un subespacio $U$ de $V$ generado por vectores bastante simples. (Puede imaginar esto tomando $V$ como espacio tridimensional y $U$ algún plano que pasa por el origen). La pregunta es: Dado un vector $v \in V$ que no está en $U$, ¿cuál es el vector en $U$ que mejor aproxima $v$? Como también tenemos una norma, podemos preguntar con más precisión: ¿Cuál es el vector $u \in U$ para el cual $|v - u|$ es mínimo? La respuesta es sorprendentemente simple: el vector $u$ está dado por $P_U v$, la proyección ortogonal de $v$ sobre $U$.  
(a) Demuestre la afirmación anterior mostrando que para cualquier $u \in U$ se tiene  
$$
|v - u|\geq |v - P_U v|.
$$  
Como aplicación considere el espacio vectorial infinito-dimensional de funciones reales en el intervalo $x \in [-\pi , \pi ]$. El producto interno de dos funciones $f$ y $g$ en este intervalo se toma como:  
$$
\langle f,g\rangle = \int_{-\pi}^{\pi}f(x)g(x)dx.
$$  
Tomaremos $U$ como el subespacio de seis dimensiones de funciones con una base dada por $(1, x, x^2, x^3, x^4, x^5)$. En este problema use un manipulador algebraico que haga integrales.  
(b) Use el algoritmo de Gram-Schmidt para encontrar una base ortonormal $(e_1, \ldots , e_6)$ para $U$.  
(c) Considere aproximar las funciones $\sin x$ y $\cos x$ con los mejores representantes posibles de $U$. Calcule exactamente estos dos representantes y escríbalos como polinomios en $x$ con coeficientes que dependen de potencias de $\pi$ y otras constantes. También escriba los polinomios usando coeficientes numéricos con seis dígitos significativos.  
(d) Haga una gráfica para cada una de las funciones ($\sin x$ y $\cos x$) donde muestre la función original, su mejor aproximación en $U$ calculada arriba, y la aproximación en $U$ que corresponde a la expansión de Taylor truncada alrededor de $x = 0$.

---