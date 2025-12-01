Esta es una solución detallada paso a paso para el problema de mecánica clásica planteado.

---

### 1. Definición de Variables y Coordenadas

Antes de comenzar, definamos las masas y coordenadas transformadas:

- **Coordenadas individuales:** $\vec{r}_1, \vec{r}_2$
    
- **Masa Total:** $M = m_1 + m_2$
    
- **Masa Reducida:** $\mu = \frac{m_1 m_2}{M}$
    
- **Coordenada del Centro de Masa (CM):** $\vec{R} = \frac{m_1 \vec{r}_1 + m_2 \vec{r}_2}{M}$
    
- **Vector de distancia relativa:** $\vec{r} = \vec{r}_1 - \vec{r}_2$
    

La relación inversa de las coordenadas es:

$$\vec{r}_1 = \vec{R} + \frac{m_2}{M}\vec{r} \quad ; \quad \vec{r}_2 = \vec{R} - \frac{m_1}{M}\vec{r}$$

---

### (a) El Lagrangiano

El Lagrangiano se define como $L = T - V$, donde $T$ es la energía cinética y $V$ es la energía potencial.

1. Energía Cinética ($T$):

En términos de $\vec{R}$ y $\vec{r}$, la energía cinética total de un sistema de dos cuerpos se descompone en la energía del CM y la energía del movimiento relativo:

$$T = \frac{1}{2}M|\dot{\vec{R}}|^2 + \frac{1}{2}\mu|\dot{\vec{r}}|^2$$

2. Energía Potencial ($V$):

La energía potencial total es la suma de la interacción mutua y el potencial externo.

- **Interacción Mutua:** $V_{int} = - \frac{G m_1 m_2}{|\vec{r}|} = - \frac{G m_1 m_2}{r}$
    
- Campo Externo: El campo es uniforme con aceleración $-g\hat{z}$. El potencial para una masa $m$ a altura $z$ es $mgz$.
    
    $$V_{ext} = m_1 g z_1 + m_2 g z_2$$
    

Sustituimos las coordenadas $z_1$ y $z_2$ usando la transformación al CM (donde $Z$ es la componente z de $\vec{R}$ y $z$ es la componente z de $\vec{r}$):

$$V_{ext} = m_1 g \left(Z + \frac{m_2}{M}z\right) + m_2 g \left(Z - \frac{m_1}{M}z\right)$$

$$V_{ext} = (m_1 + m_2)gZ + g z \left( \frac{m_1 m_2}{M} - \frac{m_2 m_1}{M} \right)$$

Los términos que dependen de $z$ se cancelan.

$$V_{ext} = MgZ$$

3. Lagrangiano Total:

$$L = \left[ \frac{1}{2}M|\dot{\vec{R}}|^2 - MgZ \right] + \left[ \frac{1}{2}\mu|\dot{\vec{r}}|^2 + \frac{G m_1 m_2}{r} \right]$$

Podemos escribir esto como $L = L_{CM} + L_{rel}$.

Explicación Física:

La separación tiene sentido porque el campo gravitacional externo es uniforme. Debido a esto, la fuerza externa actúa efectivamente sobre el centro de masa del sistema como si toda la masa estuviera concentrada allí. El movimiento interno (relativo) de las partículas no se ve afectado por la aceleración uniforme del "laboratorio", ya que ambas partículas caen con la misma aceleración externa.

- $L_{CM}$ describe una partícula libre de masa $M$ en un campo gravitacional (tiro parabólico).
    
- $L_{rel}$ describe el problema de Kepler: una partícula de masa $\mu$ en un potencial central.
    

---

### (b) Ecuaciones de Euler-Lagrange (Parte Relativa)

Nos enfocamos solo en la parte relativa:

$$L_{rel} = \frac{1}{2}\mu \dot{\vec{r}}^2 + \frac{k}{r}$$

Donde definimos $k = G m_1 m_2$ para simplificar la notación.

1. Coordenadas Esféricas:

En coordenadas esféricas $(r, \theta, \phi)$, el cuadrado de la velocidad es:

$$\dot{\vec{r}}^2 = \dot{r}^2 + r^2 \dot{\theta}^2 + r^2 \sin^2\theta \, \dot{\phi}^2$$

El Lagrangiano relativo es:

$$L_{rel} = \frac{1}{2}\mu (\dot{r}^2 + r^2 \dot{\theta}^2 + r^2 \sin^2\theta \, \dot{\phi}^2) + \frac{k}{r}$$

2. Ecuaciones de Movimiento:

Usamos la ecuación de Euler-Lagrange: $\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}_i}\right) - \frac{\partial L}{\partial q_i} = 0$.

- Para la coordenada radial ($r$):
    
    $$\frac{\partial L}{\partial \dot{r}} = \mu \dot{r} \implies \frac{d}{dt}(\mu \dot{r}) = \mu \ddot{r}$$
    
    $$\frac{\partial L}{\partial r} = \mu r \dot{\theta}^2 + \mu r \sin^2\theta \dot{\phi}^2 - \frac{k}{r^2}$$
    
    > Ecuación radial:
    > 
    > $$\mu \ddot{r} - \mu r (\dot{\theta}^2 + \sin^2\theta \dot{\phi}^2) + \frac{G m_1 m_2}{r^2} = 0$$
    
- Para la coordenada polar ($\theta$):
    
    $$\frac{\partial L}{\partial \dot{\theta}} = \mu r^2 \dot{\theta} \implies \frac{d}{dt}(\mu r^2 \dot{\theta})$$
    
    $$\frac{\partial L}{\partial \theta} = \mu r^2 \sin\theta \cos\theta \dot{\phi}^2$$
    
    > Ecuación polar:
    > 
    > $$\frac{d}{dt}(\mu r^2 \dot{\theta}) - \mu r^2 \sin\theta \cos\theta \dot{\phi}^2 = 0$$
    
- Para la coordenada azimutal ($\phi$):
    
    $$\frac{\partial L}{\partial \dot{\phi}} = \mu r^2 \sin^2\theta \dot{\phi} \implies \frac{d}{dt}(\mu r^2 \sin^2\theta \dot{\phi})$$
    
    $$\frac{\partial L}{\partial \phi} = 0$$
    
    > Ecuación azimutal:
    > 
    > $$\frac{d}{dt}(\mu r^2 \sin^2\theta \dot{\phi}) = 0$$
    > 
    > (Nota: Esto implica que el momento angular conjugado $p_\phi$ se conserva).
    

---

### (c) El Hamiltoniano y Ecuaciones de Hamilton

A partir del Lagrangiano $L_{rel}$ del inciso (b), primero encontramos los momentos canónicos conjugados ($p_i = \frac{\partial L}{\partial \dot{q}_i}$):

1. $p_r = \mu \dot{r} \implies \dot{r} = \frac{p_r}{\mu}$
    
2. $p_\theta = \mu r^2 \dot{\theta} \implies \dot{\theta} = \frac{p_\theta}{\mu r^2}$
    
3. $p_\phi = \mu r^2 \sin^2\theta \dot{\phi} \implies \dot{\phi} = \frac{p_\phi}{\mu r^2 \sin^2\theta}$
    

4. El Hamiltoniano ($H$):

Dado que el sistema es "natural" (la energía cinética es cuadrática en velocidades y el potencial no depende de la velocidad), el Hamiltoniano es la energía total $T + V$, pero expresada en términos de los momentos.

$$H = T + V = \frac{1}{2}\mu (\dot{r}^2 + r^2 \dot{\theta}^2 + r^2 \sin^2\theta \, \dot{\phi}^2) - \frac{k}{r}$$

Sustituyendo las velocidades por los momentos:

$$H(r, \theta, \phi, p_r, p_\theta, p_\phi) = \frac{p_r^2}{2\mu} + \frac{p_\theta^2}{2\mu r^2} + \frac{p_\phi^2}{2\mu r^2 \sin^2\theta} - \frac{G m_1 m_2}{r}$$

2. Ecuaciones de Movimiento de Hamilton:

Las ecuaciones son $\dot{q}_i = \frac{\partial H}{\partial p_i}$ y $\dot{p}_i = - \frac{\partial H}{\partial q_i}$.

- Derivadas de las coordenadas ($\dot{q}$): (Simplemente recuperan las definiciones de velocidad)
    
    $$\dot{r} = \frac{p_r}{\mu}$$
    
    $$\dot{\theta} = \frac{p_\theta}{\mu r^2}$$
    
    $$\dot{\phi} = \frac{p_\phi}{\mu r^2 \sin^2\theta}$$
    
- Derivadas de los momentos ($\dot{p}$):
    
    $$\dot{p}_r = -\frac{\partial H}{\partial r} = - \left[ \frac{-2 p_\theta^2}{2\mu r^3} + \frac{-2 p_\phi^2}{2\mu r^3 \sin^2\theta} + \frac{G m_1 m_2}{r^2} \right]$$
    
    > $$\dot{p}_r = \frac{p_\theta^2}{\mu r^3} + \frac{p_\phi^2}{\mu r^3 \sin^2\theta} - \frac{G m_1 m_2}{r^2}$$
    
    $$\dot{p}_\theta = -\frac{\partial H}{\partial \theta} = - \left[ \frac{p_\phi^2}{2\mu r^2} \cdot \frac{\partial}{\partial \theta}(\sin^{-2}\theta) \right]$$
    
    > $$\dot{p}_\theta = \frac{p_\phi^2 \cos\theta}{\mu r^2 \sin^3\theta}$$
    
    $$\dot{p}_\phi = -\frac{\partial H}{\partial \phi}$$
    
    > $$\dot{p}_\phi = 0$$
    

---
# Pendulo doble
¡Claro que sí! Este es un problema clásico de mecánica analítica. Resolveremos el problema paso a paso, derivando el Lagrangiano para la parte (a) y luego el Hamiltoniano para la parte (b).

---

### Parte a) El Lagrangiano y las Ecuaciones de Movimiento

Primero, definimos las coordenadas y las energías del sistema.

**1. Coordenadas y Velocidades**

Tomamos el origen $(0,0)$ en el punto fijo superior. El eje $y$ apunta hacia arriba (por lo tanto, la gravedad actúa en la dirección negativa de $y$).

Las posiciones de las masas $m_1$ y $m_2$ son:

Para $m_1$:

$$x_1 = \ell_1 \sin\theta_1$$

$$y_1 = -\ell_1 \cos\theta_1$$

Para $m_2$:

$$x_2 = x_1 + \ell_2 \sin\theta_2 = \ell_1 \sin\theta_1 + \ell_2 \sin\theta_2$$

$$y_2 = y_1 - \ell_2 \cos\theta_2 = -\ell_1 \cos\theta_1 - \ell_2 \cos\theta_2$$

Las velocidades al cuadrado son necesarias para la energía cinética ($v^2 = \dot{x}^2 + \dot{y}^2$).

$$v_1^2 = \ell_1^2 \dot{\theta}_1^2$$

Para $v_2$, derivamos las posiciones de $m_2$ respecto al tiempo:

$$\dot{x}_2 = \ell_1 \dot{\theta}_1 \cos\theta_1 + \ell_2 \dot{\theta}_2 \cos\theta_2$$

$$\dot{y}_2 = \ell_1 \dot{\theta}_1 \sin\theta_1 + \ell_2 \dot{\theta}_2 \sin\theta_2$$

Calculando $v_2^2 = \dot{x}_2^2 + \dot{y}_2^2$ y usando la identidad trigonométrica $\cos(A-B) = \cos A \cos B + \sin A \sin B$:

$$v_2^2 = \ell_1^2 \dot{\theta}_1^2 + \ell_2^2 \dot{\theta}_2^2 + 2\ell_1 \ell_2 \dot{\theta}_1 \dot{\theta}_2 \cos(\theta_1 - \theta_2)$$

**2. Energía Cinética ($T$) y Potencial ($V$)**

$$T = \frac{1}{2}m_1 v_1^2 + \frac{1}{2}m_2 v_2^2$$

Sustituyendo las velocidades:

$$T = \frac{1}{2}(m_1 + m_2)\ell_1^2 \dot{\theta}_1^2 + \frac{1}{2}m_2 \ell_2^2 \dot{\theta}_2^2 + m_2 \ell_1 \ell_2 \dot{\theta}_1 \dot{\theta}_2 \cos(\theta_1 - \theta_2)$$

La energía potencial (referencia $y=0$ en el pivote):

$$V = m_1 g y_1 + m_2 g y_2$$

$$V = -(m_1 + m_2)g\ell_1 \cos\theta_1 - m_2 g \ell_2 \cos\theta_2$$

**3. El Lagrangiano ($L = T - V$)**

$$L = \frac{1}{2}(m_1 + m_2)\ell_1^2 \dot{\theta}_1^2 + \frac{1}{2}m_2 \ell_2^2 \dot{\theta}_2^2 + m_2 \ell_1 \ell_2 \dot{\theta}_1 \dot{\theta}_2 \cos(\theta_1 - \theta_2) + (m_1 + m_2)g\ell_1 \cos\theta_1 + m_2 g \ell_2 \cos\theta_2$$

4. Ecuaciones de Movimiento de Euler-Lagrange

La ecuación es: $\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{\theta}_i}\right) - \frac{\partial L}{\partial \theta_i} = 0$

Para $\theta_1$:

$$\frac{\partial L}{\partial \dot{\theta}_1} = (m_1+m_2)\ell_1^2 \dot{\theta}_1 + m_2\ell_1\ell_2 \dot{\theta}_2 \cos(\theta_1-\theta_2)$$

$$\frac{\partial L}{\partial \theta_1} = -m_2\ell_1\ell_2 \dot{\theta}_1 \dot{\theta}_2 \sin(\theta_1-\theta_2) - (m_1+m_2)g\ell_1 \sin\theta_1$$

Derivando respecto al tiempo $\frac{d}{dt}(\frac{\partial L}{\partial \dot{\theta}_1})$ e igualando, obtenemos la primera ecuación de movimiento:

$$(m_1+m_2)\ell_1 \ddot{\theta}_1 + m_2\ell_2 \ddot{\theta}_2 \cos(\theta_1-\theta_2) + m_2\ell_2 \dot{\theta}_2^2 \sin(\theta_1-\theta_2) + (m_1+m_2)g \sin\theta_1 = 0$$

Para $\theta_2$:

Haciendo el mismo proceso para $\theta_2$:

$$m_2\ell_2 \ddot{\theta}_2 + m_2\ell_1 \ddot{\theta}_1 \cos(\theta_1-\theta_2) - m_2\ell_1 \dot{\theta}_1^2 \sin(\theta_1-\theta_2) + m_2g \sin\theta_2 = 0$$

---

### Parte b) El Hamiltoniano

Asumimos $m_1 = m_2 = m$.

1. Lagrangiano Simplificado

$$L = m\ell_1^2 \dot{\theta}_1^2 + \frac{1}{2}m \ell_2^2 \dot{\theta}_2^2 + m \ell_1 \ell_2 \dot{\theta}_1 \dot{\theta}_2 \cos(\theta_1 - \theta_2) + 2mg\ell_1 \cos\theta_1 + mg \ell_2 \cos\theta_2$$

(Nota: el término cinético de $\theta_1$ tiene un factor 2 implícito porque $m_1+m_2=2m$, por eso $\frac{1}{2}(2m) = m$).

**2. Momentos Conjugados ($p_i = \partial L / \partial \dot{\theta}_i$)**

$$p_{\theta_1} = 2m\ell_1^2 \dot{\theta}_1 + m\ell_1\ell_2 \cos(\theta_1-\theta_2) \dot{\theta}_2$$

$$p_{\theta_2} = m\ell_1\ell_2 \cos(\theta_1-\theta_2) \dot{\theta}_1 + m\ell_2^2 \dot{\theta}_2$$

3. Despejar las velocidades ($\dot{\theta}_1, \dot{\theta}_2$)

Este es un sistema lineal. Para simplificar la notación, sea $\Delta = \theta_1 - \theta_2$.

Escribimos en forma matricial:

$$\begin{pmatrix} p_{\theta_1} \\ p_{\theta_2} \end{pmatrix} = \begin{pmatrix} 2m\ell_1^2 & m\ell_1\ell_2 \cos\Delta \\ m\ell_1\ell_2 \cos\Delta & m\ell_2^2 \end{pmatrix} \begin{pmatrix} \dot{\theta}_1 \\ \dot{\theta}_2 \end{pmatrix}$$

Calculamos el determinante ($D$) de la matriz de masas:

$$D = (2m\ell_1^2)(m\ell_2^2) - (m\ell_1\ell_2 \cos\Delta)^2 = m^2\ell_1^2\ell_2^2 (2 - \cos^2\Delta)$$

Invertimos la matriz para encontrar $\dot{\theta}$:

$$\begin{pmatrix} \dot{\theta}_1 \\ \dot{\theta}_2 \end{pmatrix} = \frac{1}{D} \begin{pmatrix} m\ell_2^2 & -m\ell_1\ell_2 \cos\Delta \\ -m\ell_1\ell_2 \cos\Delta & 2m\ell_1^2 \end{pmatrix} \begin{pmatrix} p_{\theta_1} \\ p_{\theta_2} \end{pmatrix}$$

De aquí obtenemos las velocidades en función de los momentos:

$$\dot{\theta}_1 = \frac{m\ell_2^2 p_{\theta_1} - m\ell_1\ell_2 \cos\Delta p_{\theta_2}}{m^2\ell_1^2\ell_2^2 (2 - \cos^2\Delta)}$$

$$\dot{\theta}_2 = \frac{-m\ell_1\ell_2 \cos\Delta p_{\theta_1} + 2m\ell_1^2 p_{\theta_2}}{m^2\ell_1^2\ell_2^2 (2 - \cos^2\Delta)}$$

4. El Hamiltoniano ($H = T + V$)

Como el sistema es conservativo y las coordenadas no dependen explícitamente del tiempo, $H$ es la energía total expresada en términos de momentos y posiciones.

$$H = T(p, q) + V(q)$$

La energía cinética en forma matricial es $T = \frac{1}{2} \mathbf{p}^T M^{-1} \mathbf{p}$.

Desarrollando la multiplicación con la matriz inversa hallada arriba:

$$T = \frac{1}{2m^2\ell_1^2\ell_2^2 (2 - \cos^2(\theta_1-\theta_2))} \left[ m\ell_2^2 p_{\theta_1}^2 - 2m\ell_1\ell_2 \cos(\theta_1-\theta_2) p_{\theta_1} p_{\theta_2} + 2m\ell_1^2 p_{\theta_2}^2 \right]$$

Simplificando masas:

$$H = \frac{ \ell_2^2 p_{\theta_1}^2 - 2\ell_1\ell_2 p_{\theta_1} p_{\theta_2} \cos(\theta_1-\theta_2) + 2\ell_1^2 p_{\theta_2}^2 }{ 2m\ell_1^2\ell_2^2 (2 - \cos^2(\theta_1-\theta_2)) } - 2mg\ell_1 \cos\theta_1 - mg\ell_2 \cos\theta_2$$

5. Ecuaciones de Hamilton

Las ecuaciones son:

$$\dot{\theta}_i = \frac{\partial H}{\partial p_{\theta_i}} \quad , \quad \dot{p}_{\theta_i} = -\frac{\partial H}{\partial \theta_i}$$

Las ecuaciones $\dot{\theta}_i$ son simplemente las expresiones de velocidad que hallamos en el paso 3.

Las ecuaciones para $\dot{p}_{\theta_i}$ requieren derivar todo el Hamiltoniano respecto a $\theta_1$ y $\theta_2$. Dado que esto resulta en expresiones algebraicas muy extensas, se suele dejar indicado de la siguiente forma general:

$$\dot{p}_{\theta_1} = -\frac{\partial H}{\partial \theta_1} = -\frac{\partial T}{\partial \theta_1} - 2mg\ell_1 \sin\theta_1$$

$$\dot{p}_{\theta_2} = -\frac{\partial H}{\partial \theta_2} = -\frac{\partial T}{\partial \theta_2} - mg\ell_2 \sin\theta_2$$

¿Te gustaría que desarrolle explícitamente las derivadas parciales para las ecuaciones de momento $\dot{p}$?

# jerky mechanics

Aquí tienes la solución detallada para los dos problemas de la imagen. Continuaré en español para mantener la consistencia con nuestra conversación anterior.

---

### 5. Jerky Mechanics (Mecánica de Derivadas Superiores)

**Objetivo:** Derivar la ecuación de Euler-Lagrange generalizada para un Lagrangiano que depende de la aceleración: $L(q_i, \dot{q}_i, \ddot{q}_i, t)$.

Paso 1: Principio de Hamilton

El principio de Hamilton establece que la acción $S$ es estacionaria para la trayectoria real ($\delta S = 0$).

$$S = \int_{t_1}^{t_2} L(q_i, \dot{q}_i, \ddot{q}_i, t) \, dt$$

Calculamos la variación de la acción $\delta S$:

$$\delta S = \int_{t_1}^{t_2} \sum_i \left( \frac{\partial L}{\partial q_i}\delta q_i + \frac{\partial L}{\partial \dot{q}_i}\delta \dot{q}_i + \frac{\partial L}{\partial \ddot{q}_i}\delta \ddot{q}_i \right) dt = 0$$

Ten en cuenta que las variaciones son conmutativas con la derivada temporal, es decir:

$\delta \dot{q}_i = \frac{d}{dt}(\delta q_i)$ y $\delta \ddot{q}_i = \frac{d^2}{dt^2}(\delta q_i)$.

Paso 2: Integración por partes

Debemos mover las derivadas temporales fuera de las variaciones $\delta \dot{q}$ y $\delta \ddot{q}$ para factorizar $\delta q_i$.

- Para el segundo término ($\dot{q}_i$):
    
    Hacemos integración por partes una vez:
    
    $$\int_{t_1}^{t_2} \frac{\partial L}{\partial \dot{q}_i} \frac{d}{dt}(\delta q_i) dt = \left[ \frac{\partial L}{\partial \dot{q}_i} \delta q_i \right]_{t_1}^{t_2} - \int_{t_1}^{t_2} \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}_i}\right) \delta q_i dt$$
    
    El término de frontera (corchetes) es cero porque el enunciado dice que la variación de $q_i$ es cero en los extremos ($\delta q_i(t_1) = \delta q_i(t_2) = 0$).
    
- Para el tercer término ($\ddot{q}_i$):
    
    Necesitamos integrar por partes dos veces.
    
    1. Primera integración:
        
        $$\int_{t_1}^{t_2} \frac{\partial L}{\partial \ddot{q}_i} \frac{d}{dt}(\delta \dot{q}_i) dt = \left[ \frac{\partial L}{\partial \ddot{q}_i} \delta \dot{q}_i \right]_{t_1}^{t_2} - \int_{t_1}^{t_2} \frac{d}{dt}\left(\frac{\partial L}{\partial \ddot{q}_i}\right) \delta \dot{q}_i dt$$
        
        El término de frontera es cero porque el enunciado especifica que la variación de $\dot{q}_i$ también es cero en los extremos.
        
    2. Segunda integración (sobre la integral resultante):
        
        $$-\int_{t_1}^{t_2} \underbrace{\frac{d}{dt}\left(\frac{\partial L}{\partial \ddot{q}_i}\right)}_{u} \underbrace{\frac{d}{dt}(\delta q_i) dt}_{dv} = -\left[ \frac{d}{dt}\left(\frac{\partial L}{\partial \ddot{q}_i}\right) \delta q_i \right]_{t_1}^{t_2} + \int_{t_1}^{t_2} \frac{d^2}{dt^2}\left(\frac{\partial L}{\partial \ddot{q}_i}\right) \delta q_i dt$$
        
        Nuevamente, el término de frontera es cero por $\delta q_i = 0$.
        

Paso 3: Agrupar términos

Sustituyendo todo de vuelta en la integral de $\delta S$:

$$\delta S = \int_{t_1}^{t_2} \sum_i \left[ \frac{\partial L}{\partial q_i} - \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}_i}\right) + \frac{d^2}{dt^2}\left(\frac{\partial L}{\partial \ddot{q}_i}\right) \right] \delta q_i \, dt = 0$$

Conclusión

Dado que las variaciones $\delta q_i$ son arbitrarias dentro del intervalo, el término entre corchetes debe ser cero para cada $i$.

$$\frac{d^2}{dt^2}\left(\frac{\partial L}{\partial \ddot{q}_i}\right) - \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}_i}\right) + \frac{\partial L}{\partial q_i} = 0$$

(Q.E.D)

---

### 6. Extra Problem: Equivalent Lagrangians

**Objetivo:** Demostrar que $L' = L + \frac{dF(q,t)}{dt}$ satisface las mismas ecuaciones de Euler-Lagrange que $L$.

Lo demostraremos algebraicamente verificando que la ecuación de Euler-Lagrange para $L'$ es idéntica a la de $L$.

Paso 1: Expandir la derivada total

La derivada total de $F(q, t)$ es:

$$\frac{dF(q,t)}{dt} = \frac{\partial F}{\partial q}\dot{q} + \frac{\partial F}{\partial t}$$

Entonces:

$$L'(q, \dot{q}, t) = L(q, \dot{q}, t) + \frac{\partial F}{\partial q}\dot{q} + \frac{\partial F}{\partial t}$$

Paso 2: Calcular los términos de la ecuación de Euler-Lagrange para $L'$

La ecuación es $\frac{d}{dt}(\frac{\partial L'}{\partial \dot{q}}) - \frac{\partial L'}{\partial q} = 0$.

- Derivada respecto a $\dot{q}$:
    
    $$\frac{\partial L'}{\partial \dot{q}} = \frac{\partial L}{\partial \dot{q}} + \frac{\partial}{\partial \dot{q}}\left( \frac{\partial F}{\partial q}\dot{q} + \frac{\partial F}{\partial t} \right)$$
    
    Como $F$ solo depende de $q$ y $t$, el término $\frac{\partial F}{\partial t}$ se anula y $\frac{\partial F}{\partial q}$ es constante respecto a $\dot{q}$.
    
    $$\frac{\partial L'}{\partial \dot{q}} = \frac{\partial L}{\partial \dot{q}} + \frac{\partial F}{\partial q}$$
    
    Ahora aplicamos la derivada temporal $\frac{d}{dt}$:
    
    $$\frac{d}{dt}\left(\frac{\partial L'}{\partial \dot{q}}\right) = \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}}\right) + \frac{d}{dt}\left(\frac{\partial F}{\partial q}\right)$$
    
    Expandiendo el segundo término usando regla de la cadena:
    
    $$\frac{d}{dt}\left(\frac{\partial L'}{\partial \dot{q}}\right) = \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}}\right) + \frac{\partial^2 F}{\partial q^2}\dot{q} + \frac{\partial^2 F}{\partial t \partial q}$$
    
- Derivada respecto a $q$:
    
    $$\frac{\partial L'}{\partial q} = \frac{\partial L}{\partial q} + \frac{\partial}{\partial q}\left( \frac{\partial F}{\partial q}\dot{q} + \frac{\partial F}{\partial t} \right)$$
    
    $$\frac{\partial L'}{\partial q} = \frac{\partial L}{\partial q} + \frac{\partial^2 F}{\partial q^2}\dot{q} + \frac{\partial^2 F}{\partial q \partial t}$$
    

Paso 3: Restar los términos

$$\frac{d}{dt}\left(\frac{\partial L'}{\partial \dot{q}}\right) - \frac{\partial L'}{\partial q} = \left[ \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}}\right) + \frac{\partial^2 F}{\partial q^2}\dot{q} + \frac{\partial^2 F}{\partial t \partial q} \right] - \left[ \frac{\partial L}{\partial q} + \frac{\partial^2 F}{\partial q^2}\dot{q} + \frac{\partial^2 F}{\partial q \partial t} \right]$$

Observamos que:

1. Los términos $\frac{\partial^2 F}{\partial q^2}\dot{q}$ se cancelan.
    
2. Las derivadas parciales mixtas son iguales (Teorema de Schwarz): $\frac{\partial^2 F}{\partial t \partial q} = \frac{\partial^2 F}{\partial q \partial t}$, por lo que también se cancelan.
    

Conclusión

$$\frac{d}{dt}\left(\frac{\partial L'}{\partial \dot{q}}\right) - \frac{\partial L'}{\partial q} = \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}}\right) - \frac{\partial L}{\partial q}$$

La ecuación de movimiento para $L'$ es exactamente la misma que para $L$.

¿Te gustaría que te ayude a resolver algún otro problema de la hoja?