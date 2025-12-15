
**1.** Considere una varilla de peso despreciable suspendida por un extremo fijo, de modo que puede oscilar en un plano vertical. Una partícula de masa $m$ se mueve sin fricción a lo largo de la varilla.

- **a)** Obtenga las ecuaciones de movimiento en la formulación Hamiltoniana.
    
- **b)** Indique si hay alguna cantidad conservada.
    

---

**2.** El Lagrangiano de un sistema se puede expresar:

$$L = \dot{q}_1^2 + \frac{\dot{q}_2^2}{a + bq_1} + k_1 q_1^2 + k_2 \dot{q}_1 \dot{q}_2$$

donde $a, b, k_1, k_2$ son constantes. Encuentre las ecuaciones de movimiento en la formulación Hamiltoniana.

---

**3.** El Hamiltoniano de una partícula es:

$$H = \frac{p^2}{2m} - \mathbf{a} \cdot \mathbf{p} - \mathbf{b} \cdot \mathbf{r}$$

donde $\mathbf{a}$ y $\mathbf{b}$ son vectores constantes.

- **a)** Encuentre las ecuaciones de movimiento.
    
- **b)** Si inicialmente la partícula se encuentra en reposo en la posición $\mathbf{r}_o$, encuentre su posición en función del tiempo.
    
- **c)** Determine el Lagrangiano del sistema.
    

---

4.El Lagrangiano de un sistema es
$$L = a\dot{x}^2 + b\frac{\dot{y}}{x} + c\dot{x}\dot{y} + f y^2 \dot{x} \dot{z} + g \dot{y} - k \sqrt{x^2 + y^2},$$
donde $a, b, c, f, g$ y $k$ son constantes.
a) Encuentre el Hamiltoniano del sistema.
b) Encuentre las cantidades conservadas en el sistema.


5.El modelo de Lotka-Volterra para la dinámica de predadores $z$ y presas $c$ se describe mediante las ecuaciones

$$\begin{aligned} \dot{c} &= \alpha c - \beta cz \\ \dot{z} &= -\gamma z + \delta cz, \end{aligned}$$

donde $\alpha, \beta, \gamma, \delta$ son parámetros positivos.

- **a)** Encuentre las condiciones para que este sistema sea conservativo.
    
- b) Encuentre las transformaciones de variables que permiten expresar estas ecuaciones en la forma adimensional
    
    $$\begin{aligned} \dot{x} &= x(1 - y) \\ \dot{y} &= \mu y(x - 1). \end{aligned}$$
    
- **c)** Encuentre una cantidad conservada en términos de las variables adimensionales.
    


7. El elemento de volumen de un ensemble en el espacio de fase $n$-dimensional para el sistema dinámico $\frac{d\mathbf{x}}{dt} = \mathbf{f}(\mathbf{x})$ es

$$\Delta \Gamma = \prod_{i=1}^n dx_i.$$

Demuestre que

$$\frac{d(\Delta \Gamma)}{dt} = \nabla \cdot \mathbf{f} \, \Delta \Gamma.$$

8. La ecuación de movimiento unidimensional amortiguado y forzado de una partícula de masa $m$ sujeta a un resorte de constante $k$ es

$$\ddot{x} + 2\lambda \dot{x} + \omega^2 x = A \cos \nu t,$$

donde $\omega^2 = k/m$, $\lambda > 0$ es el coeficiente de fricción del medio, $A$ es la amplitud de la fuerza externa que actúa sobre la partícula y $\nu$ es la frecuencia de esa fuerza. Demuestre que este sistema es disipativo.

9. El atractor de Rössler se genera con el siguiente sistema:

$$\begin{aligned} \dot{x} &= -y - z \\ \dot{y} &= x + ay \\ \dot{z} &= b + xz - cz \end{aligned}$$

donde $a, b, c$ son parámetros.

- **a)** Encuentre la condición para que este sistema sea disipativo.
    
- **b)** Calcule los puntos fijos de este sistema en función de los parámetros.
    

### Integrabilidad y Simetrías

13. El Hamiltoniano de una partícula que se mueve en dos dimensiones es:

$$H = |\mathbf{p}|^n - a|\mathbf{r}|^{-n}, \quad a = \text{cte.}$$

- **a)** Encuentre las ecuaciones de Hamilton para el movimiento.
    
- **b)** Determine el Lagrangiano del sistema.
    
- c) ¿Cuál de las siguientes funciones es una integral de movimiento para este sistema?
    
    $$f = \frac{\mathbf{r} \cdot \mathbf{p}}{n} - Ht, \qquad g = |\mathbf{p}|.$$
    

14. El siguiente Hamiltoniano bidimensional

$$H = \frac{1}{2}(p_x^2 + p_y^2) + \frac{1}{24}\left[e^{(2y+2\sqrt{3}x)} + e^{(2y-2\sqrt{3}x)} + e^{-4y}\right] - \frac{1}{8},$$

aparece asociado a una red de Toda, un sistema de gran interés en Física No Lineal.

- **a)** Encuentre las ecuaciones de movimiento para este sistema.
    
- b) Demuestre que este sistema posee la siguiente cantidad conservada,
    
    $$I = 8p_x(p_x^2 - 3p_y^2) + (p_x + \sqrt{3}p_y)e^{(2y-2\sqrt{3}x)} + (p_x - \sqrt{3}p_y)e^{(2y+2\sqrt{3}x)} - 2p_x e^{-4y}.$$
    
    La existencia de las constantes de movimiento $H$ e $I$ hace que este sistema sea integrable. Sin embargo, la cantidad $I$ no está relacionada con ninguna simetría evidente del sistema.
    
- **c)** Calcule $I$ en el límite de $x$ y $y$ pequeños.
    

### Paréntesis de Poisson y Transformaciones Canónicas

**16.** El vector de Laplace-Runge-Lenz para el problema de Kepler se define como $\mathbf{A} = \mathbf{p} \times \mathbf{l} - mk\hat{\mathbf{r}}$. Calcule $[A_i, l_j]$.

**17.** Evalúe los siguientes paréntesis de Poisson:

- **a)** $[\mathbf{l}, (\mathbf{r} \cdot \mathbf{p})]$;
    
- **b)** $[\mathbf{p}, \mathbf{r}^n]$;
    
- c) $[\mathbf{p}, (\mathbf{a} \cdot \mathbf{r})^n]$;
    
    donde $\mathbf{a}$ es un vector constante.
    

18. Considere la transformación de coordenadas

$$q^{2m} = Q^2 + P^2, \qquad P = Q \tan np;$$

donde $m$ y $n$ son constantes.

- **a)** Determine los valores de $m$ y $n$ para los cuales esta transformación es canónica.
    
- **b)** Encuentre una función generadora de tipo $F_3(p, Q)$ para esta transformación canónica.
    

**19.** Una partícula de masa $m = 1$ se mueve sin fricción a lo largo de una varilla que gira extendida sobre una superficie horizontal con velocidad angular constante $\omega$.

- a) Demuestre que las soluciones de las ecuaciones de Hamilton para este sistema son
    
    $$\begin{aligned} q &= i\lambda [P e^{-\omega t} + Q e^{\omega t}], \\ p &= -i\lambda \omega [P e^{-\omega t} - Q e^{\omega t}]; \end{aligned}$$
    
    donde $q$ es la coordenada que describe la posición de la partícula sobre la varilla, $p$ es el momento, y $P, Q$ y $\lambda$ son constantes.
    
- **b)** Calcule el valor de $\lambda$ para que una transformación de variables $(q, p)$ a $(Q, P)$ sea canónica.
    

---
### Teoría de Hamilton-Jacobi (Nuevos)

**26.** Una partícula de masa $m$ se suelta en reposo desde una altura $h$ a lo largo de un plano inclinado sin fricción, el cual forma un ángulo $\alpha$ con el suelo.

- **a)** Encuentre la posición de la partícula sobre el plano en función del tiempo, a partir de la correspondiente ecuación de Hamilton-Jacobi para este sistema.
    
- **b)** Encuentre el momento de la partícula en función del tiempo.
    

27. La energía cinética relativista de una partícula de masa $m$ es

$$T = \sqrt{(cp)^2 + (mc^2)^2},$$

donde $c$ es la velocidad de la luz. Considere una partícula relativista sujeta a la fuerza gravitacional terrestre $\mathbf{F} = -mg\hat{y}$, tal que inicialmente se suelta del reposo en $y=0$. Determine la trayectoria de la partícula en función del tiempo a partir de la correspondiente ecuación de Hamilton-Jacobi para este sistema.

**28.** Encuentre la expresión de la acción correspondiente a un péndulo simple a partir de la ecuación de Hamilton-Jacobi para este sistema.

**29.**

- **a)** Empleando la correspondiente ecuación de Hamilton-Jacobi, calcule la posición en función del tiempo para una partícula libre con masa $m$ y energía $E$ que se encuentra en el origen en $t = 0$.
    
- **b)** Encuentre la acción en función del tiempo.
    

**30.** Una partícula de masa $m$ y energía $E$ se mueve en el potencial unidimensional $V(q) = k/q^2$, donde $k$ es constante.

- **a)** Encuentre la acción $S(q,t)$ asociada a esta partícula.
    
- **b)** Encuentre la posición de la partícula en función del tiempo.
    

---

### Variables de Acción-Ángulo y Pequeñas Oscilaciones

36. Una partícula de masa $m$ se encuentra inicialmente en $x=0$ con velocidad $v_o\hat{\mathbf{x}}$ y se mueve en el potencial unidimensional

$$V(x) = k \sin^2 \left(\frac{x}{a}\right), \quad \frac{x}{a} \in [-\pi/2, \pi/2],$$

y $V(x) = \infty$, para $\frac{x}{a} \notin [-\pi/2, \pi/2]$, con $k, a$ constantes. Utilizando la ecuación de Hamilton-Jacobi, encuentre el período de oscilación de la partícula en este potencial si $x \ll a$.

**37.** Una partícula con masa $m$ y energía $E$ se mueve periódicamente en el potencial unidimensional $V = k|x|$, $k = \text{cte}$. Usando variables de acción-ángulo, encuentre el período del movimiento de la partícula.

**38.** Una partícula de masa $m$ se mueve en una dimensión sujeta al potencial $V(x) = k \sec^2(x/a)$.

- **a)** Encuentre una expresión para la acción $S$ utilizando la ecuación de Hamilton-Jacobi para este sistema.
    
- **b)** Encuentre la frecuencia de las oscilaciones de la partícula usando variables de acción-ángulo. Calcule esta frecuencia en el límite de pequeñas amplitudes.
    

---


### Variables de Acción-Ángulo e Integrabilidad

**40.** Considere un oscilador armónico con masa $m$ y constante de resorte $k$ que puede moverse en un plano.

- **a)** Encuentre el Hamiltoniano del sistema en coordenadas polares.
    
- **b)** Calcule las frecuencias del movimiento usando variables de acción-ángulo.
    

41. Utilizando el método de las variables de acción-ángulo, demuestre que el período de libración de un péndulo simple, de masa $m$ y longitud $l$, y cuya amplitud inicial es $\theta_0$, se puede expresar como

$$T = 2\sqrt{\frac{l}{g}} \int_0^{\theta_0} \frac{d\theta}{\sqrt{\cos \theta - \cos \theta_0}}.$$

**42.** Considere una partícula de masa $m$ sujeta a moverse sin fricción sobre un cono invertido, con ángulo de vertice $\beta$, en el campo gravitacional terrestre. Calcule las frecuencias del movimiento mediante el uso de variables de acción-ángulo para este sistema.

43. Considere el Hamiltoniano

$$H(q_i, p_i) = \sum_{k=1}^s \beta_k G_k(q_i, p_i),$$

donde los coeficientes $\beta_k$ son constantes y

$$G_k(q_i, p_i) = ap_k^2 + (b+c)p_k q_k + dq_k^2 - (ad-bd) \sum_{i \neq k} \frac{(p_i q_k - q_i p_k)^2}{\alpha_k - \alpha_i}, \quad k = 1, \dots, s,$$

con $a, b, c, d$ y $\alpha_k$ distintas constantes. Demuestre que las funciones $G_k(q_i, p_i)$ son constantes del movimiento y, por lo tanto, este sistema es integrable.

(Nota: En la transcripción del problema 43 he asumido la forma estándar del momento angular $p_i q_k - q_i p_k$ en el término de interacción, ya que la notación de la imagen contiene lo que parece ser un error tipográfico en los índices).

---
