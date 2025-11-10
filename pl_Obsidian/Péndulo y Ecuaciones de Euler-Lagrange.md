
## pendulum 4. Péndulo y Ecuaciones de Euler-Lagrange

### a) Derivación de la Ecuación de Movimiento

El objetivo es encontrar el Lagrangiano $L = T - V$ y aplicar la ecuación de Euler-Lagrange: $\frac{\partial L}{\partial \phi} - \frac{d}{dt} \left( \frac{\partial L}{\partial \dot{\phi}} \right) = 0$.

1. Energía Cinética ($T$):
    
    Usamos las coordenadas dadas: $x = l \sin \phi$ y $y = l \cos \phi$.
    
    Derivamos respecto al tiempo para encontrar las velocidades:
    
    - $\dot{x} = l \dot{\phi} \cos \phi$
        
    - $\dot{y} = -l \dot{\phi} \sin \phi$
        
    
    La energía cinética es $T = \frac{1}{2} m v^2 = \frac{1}{2} m (\dot{x}^2 + \dot{y}^2)$.
    
    $$T = \frac{1}{2} m \left( (l \dot{\phi} \cos \phi)^2 + (-l \dot{\phi} \sin \phi)^2 \right)$$
    
    $$T = \frac{1}{2} m \left( l^2 \dot{\phi}^2 \cos^2 \phi + l^2 \dot{\phi}^2 \sin^2 \phi \right)$$
    
    Usando la identidad $\sin^2 \phi + \cos^2 \phi = 1$:
    
    $T = \frac{1}{2} m l^2 \dot{\phi}^2$
    
2. Energía Potencial ($V$):
    
    El problema indica que el eje $y$ es paralelo a la gravedad. Asumiremos que la gravedad $\vec{g}$ apunta en la dirección negativa de $y$ (configuración estándar) y que el pivote está en $y=0$.
    
    La energía potencial gravitatoria es $V = mgy$.
    
    Sustituyendo $y = l \cos \phi$:
    
    $V = mgl \cos \phi$
    
    (Nota: La ecuación final dada en el problema, $ml^2 \ddot{\phi} = -mgl \sin \phi$, sugiere que $V = -mgl \cos \phi$. Esto ocurre si $\phi=0$ se mide desde la vertical hacia abajo. Si seguimos estrictamente $V = mgl \cos \phi$, la ecuación resultante tendrá un signo positivo: $ml^2 \ddot{\phi} = mgl \sin \phi$, que describe un péndulo invertido. Para obtener la ecuación del problema, usaremos $V = -mgl \cos \phi$, asumiendo que $\phi=0$ es el punto más bajo.)
    
    **Usemos $V = -mgl \cos \phi$** (para coincidir con la ecuación del problema).
    
3. Lagrangiano ($L$):
    
    $$L = T - V = \frac{1}{2} m l^2 \dot{\phi}^2 - (-mgl \cos \phi) = \frac{1}{2} m l^2 \dot{\phi}^2 + mgl \cos \phi$$
    
4. **Ecuación de Euler-Lagrange:**
    
    - $\frac{\partial L}{\partial \phi} = \frac{\partial}{\partial \phi} (mgl \cos \phi) = -mgl \sin \phi$
        
    - $\frac{\partial L}{\partial \dot{\phi}} = \frac{\partial}{\partial \dot{\phi}} (\frac{1}{2} m l^2 \dot{\phi}^2) = m l^2 \dot{\phi}$
        
    - $\frac{d}{dt} \left( \frac{\partial L}{\partial \dot{\phi}} \right) = \frac{d}{dt} (m l^2 \dot{\phi}) = m l^2 \ddot{\phi}$
        
    
    Sustituyendo en la ecuación de E-L:
    
    $(-mgl \sin \phi) - (m l^2 \ddot{\phi}) = 0$
    
    $ml^2 \ddot{\phi} = -mgl \sin \phi$
    

---

### b) Justificación de $\sin \phi \approx \phi$

Esta es la **aproximación de ángulo pequeño**. Se justifica usando la expansión en serie de Taylor de $\sin \phi$ alrededor de $\phi = 0$:

$$\sin \phi = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)!} \phi^{2n+1} = \phi - \frac{\phi^3}{3!} + \frac{\phi^5}{5!} - \dots$$

Para oscilaciones **pequeñas**, $\phi$ es un valor muy cercano a cero (en radianes).

- El término $\phi^3$ es mucho más pequeño que $\phi$.
    
- El término $\phi^5$ es aún más pequeño.
    

Por lo tanto, para $\phi \ll 1$, podemos despreciar todos los términos de orden superior ($\phi^3$ y mayores), dejando únicamente el primer término:

$\sin \phi \approx \phi$

---

### c) Solución de la Ecuación Simplificada

Sustituimos $\sin \phi \approx \phi$ en la ecuación de movimiento:

$ml^2 \ddot{\phi} = -mgl \phi$

Dividimos por $ml^2$:

$\ddot{\phi} = -\frac{g}{l} \phi$

Reescribimos como:

$\ddot{\phi} + \frac{g}{l} \phi = 0$

Esta es la ecuación diferencial canónica de un Oscilador Armónico Simple (OAS). La forma general es $\ddot{x} + \omega^2 x = 0$.

Identificamos la frecuencia angular $\omega$:

$\omega = \sqrt{\frac{g}{l}}$

La solución general para $\phi(t)$ es una superposición de seno y coseno:

$\phi(t) = A \cos(\omega t) + B \sin(\omega t)$

donde $\omega = \sqrt{g/l}$, y $A$ y $B$ son constantes que se determinan a partir de las condiciones iniciales (posición inicial $\phi(0)$ y velocidad inicial $\dot{\phi}(0)$).

---

## 🏛️ 5. Principio de Mínima Acción

Esto requiere mostrar cómo el principio variacional $\delta S = 0$ conduce a las $N$ ecuaciones de Euler-Lagrange.

1. Acción ($S$) y su Variación ($\delta S$):
    
    La acción es la integral del Lagrangiano: $S = \int_{t_1}^{t_2} L(q_i, \dot{q}_i, t) dt$.
    
    El principio de mínima acción establece que la variación de la acción $\delta S$ es cero para la trayectoria física:
    
    $$\delta S = \delta \int L dt = \int \delta L dt = 0$$
    
2. Variación del Lagrangiano ($\delta L$):
    
    Usamos la regla de la cadena para la variación $\delta L$, que depende de $N$ coordenadas $q_i$ y $N$ velocidades $\dot{q}_i$:
    
    $$\delta L = \sum_{i=1}^{N} \left( \frac{\partial L}{\partial q_i} \delta q_i + \frac{\partial L}{\partial \dot{q}_i} \delta \dot{q}_i \right)$$
    
3. Integración por Partes:
    
    Sustituimos $\delta L$ en la integral de la acción:
    
    $$\delta S = \int_{t_1}^{t_2} \sum_{i=1}^{N} \left( \frac{\partial L}{\partial q_i} \delta q_i + \frac{\partial L}{\partial \dot{q}_i} \delta \dot{q}_i \right) dt = 0$$
    
    Nos centramos en el segundo término. Usamos $\delta \dot{q}_i = \frac{d}{dt}(\delta q_i)$ y aplicamos integración por partes: $\int u dv = uv - \int v du$.
    
    - Sea $u = \frac{\partial L}{\partial \dot{q}_i}$ y $dv = \delta \dot{q}_i dt = d(\delta q_i)$.
        
    - Entonces $du = \frac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}_i} \right) dt$ y $v = \delta q_i$.
        
    
    $$\int_{t_1}^{t_2} \frac{\partial L}{\partial \dot{q}_i} \delta \dot{q}_i dt = \left[ \frac{\partial L}{\partial \dot{q}_i} \delta q_i \right]_{t_1}^{t_2} - \int_{t_1}^{t_2} \left( \frac{d}{dt} \frac{\partial L}{\partial \dot{q}_i} \right) \delta q_i dt$$
    
4. Términos de Frontera:
    
    El principio variacional asume que la trayectoria está fija en los puntos finales $t_1$ y $t_2$. Esto significa que cualquier variación $\delta q_i$ debe ser cero en esos puntos: $\delta q_i(t_1) = 0$ y $\delta q_i(t_2) = 0$.
    
    Por lo tanto, el término de frontera $\left[ \frac{\partial L}{\partial \dot{q}_i} \delta q_i \right]_{t_1}^{t_2}$ es cero.
    
5. Obtención de las Ecuaciones:
    
    Sustituimos el resultado de la integración por partes (sin el término de frontera) de nuevo en la expresión de $\delta S$:
    
    $$\delta S = \int_{t_1}^{t_2} \sum_{i=1}^{N} \left( \frac{\partial L}{\partial q_i} \delta q_i - \frac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}_i} \right) \delta q_i \right) dt = 0$$
    
    Factorizamos el $\delta q_i$:
    
    $$\delta S = \int_{t_1}^{t_2} \sum_{i=1}^{N} \left( \frac{\partial L}{\partial q_i} - \frac{d}{dt} \frac{\partial L}{\partial \dot{q}_i} \right) \delta q_i dt = 0$$
    
    Dado que las $N$ variaciones $\delta q_i$ son independientes y arbitrarias (pueden tomar cualquier valor pequeño), la única forma en que la integral puede ser cero para _todas_ las posibles $\delta q_i$ es si el término entre paréntesis es cero para **cada $i$**:
    
    $\frac{\partial L}{\partial q_i} - \frac{d}{dt} \frac{\partial L}{\partial \dot{q}_i} = 0 \quad \text{para } i = 1, \dots, N$
    
    Esto nos da las $N$ ecuaciones de Euler-Lagrange.
    

---

## 🔀 6. Derivadas Temporales Totales

### a) Por qué $S$ y $S'$ dan la misma variación

Supongamos que tenemos dos Lagrangianos $L$ y $L'$ relacionados por una derivada temporal total de una función arbitraria $F(q, t)$:

$L'(q, \dot{q}, t) = L(q, \dot{q}, t) + \frac{dF(q, t)}{dt}$

Ahora, calculemos la acción $S'$ correspondiente a $L'$:

$$S' = \int_{t_1}^{t_2} L' dt = \int_{t_1}^{t_2} \left( L + \frac{dF}{dt} \right) dt$$

$$S' = \int_{t_1}^{t_2} L dt + \int_{t_1}^{t_2} \frac{dF}{dt} dt$$

La primera integral es la acción original $S$. La segunda integral es la integral de una derivada total, que por el Teorema Fundamental del Cálculo es simplemente la función $F$ evaluada en los límites:

$\int_{t_1}^{t_2} \frac{dF}{dt} dt = F(q(t_2), t_2) - F(q(t_1), t_1) = [F]_{t_1}^{t_2}$

Por lo tanto, las dos acciones $S$ y $S'$ difieren por:

$S' = S + [F(q, t)]_{t_1}^{t_2}$

La clave es que $S$ y $S'$ "difieren por una cantidad que da cero en la variación" (como dice el problema). Para encontrar las ecuaciones de movimiento, aplicamos el principio variacional $\delta S' = 0$.

$$\delta S' = \delta \left( S + [F]_{t_1}^{t_2} \right) = \delta S + \delta [F]_{t_1}^{t_2}$$

La variación $\delta [F]_{t_1}^{t_2}$ es $\delta F(q(t_2), t_2) - \delta F(q(t_1), t_1)$.

Como $F$ depende de $q$ y $t$, su variación es $\delta F = \frac{\partial F}{\partial q} \delta q$.

Así, $\delta [F]_{t_1}^{t_2} = \left[ \frac{\partial F}{\partial q} \delta q \right]_{t_1}^{t_2}$.

Como vimos en el problema 5, la variación $\delta q$ es cero en los puntos finales $t_1$ y $t_2$.

Por lo tanto, $\delta [F]_{t_1}^{t_2} = 0$.

Esto nos deja con:

$\delta S' = \delta S$

Si el principio de mínima acción $\delta S = 0$ da las ecuaciones de movimiento correctas para $L$, entonces $\delta S' = 0$ se cumple exactamente por las mismas ecuaciones de movimiento. Agregar una derivada temporal total al Lagrangiano **no cambia las ecuaciones de movimiento**.

---

### b) 2 ejemplos que SON una derivada total

Buscamos $g(q, \dot{q}, t) = \frac{dF(q, t)}{dt}$.

Recordamos que $\frac{dF(q, t)}{dt} = \frac{\partial F}{\partial q} \dot{q} + \frac{\partial F}{\partial t}$.

1. Ejemplo 1: $F(q, t) = q$
    
    $g(q, \dot{q}, t) = \frac{d}{dt}(q) = \dot{q}$
    
2. Ejemplo 2: $F(q, t) = \frac{1}{2} q^2$
    
    $g(q, \dot{q}, t) = \frac{d}{dt} (\frac{1}{2} q^2) = \frac{\partial F}{\partial q} \dot{q} = q \dot{q}$
    

_(Estos dos ejemplos, $g_1 = \dot{q}$ y $g_2 = q \dot{q}$, son linealmente independientes)._

---

### c) 2 ejemplos que NO SON una derivada total

Buscamos funciones $g(q, \dot{q}, t)$ para las cuales no existe ninguna $F(q, t)$ tal que $\frac{\partial F}{\partial q} \dot{q} + \frac{\partial F}{\partial t} = g$.

La clave es que $F$ no puede depender de $\dot{q}$. Por lo tanto, cualquier $g$ que tenga una dependencia en $\dot{q}$ que no sea lineal (como $\dot{q}^2$, $\sqrt{\dot{q}}$, etc.) no puede ser una derivada temporal total.

1. Ejemplo 1: $g(q, \dot{q}, t) = \dot{q}^2$ (o $\frac{1}{2} m \dot{q}^2$, la energía cinética)
    
    Justificación: Para obtener $\dot{q}^2$, necesitaríamos que $\frac{\partial F}{\partial q}$ dependiera de $\dot{q}$ (específicamente, $\frac{\partial F}{\partial q} \propto \dot{q}$), pero $F$ solo puede depender de $q$ y $t$. Por lo tanto, no existe tal $F(q, t)$.
    
2. Ejemplo 2: $g(q, \dot{q}, t) = q^2$ (o $V(q)$, una energía potencial)
    
    Justificación: Si $g = q^2$, necesitamos $\frac{\partial F}{\partial q} \dot{q} + \frac{\partial F}{\partial t} = q^2$.
    
    Como $\dot{q}$ es independiente, la única forma de que esto funcione es si $\frac{\partial F}{\partial q} = 0$, lo que implica $F = F(t)$.
    
    Pero si $F=F(t)$, la ecuación se convierte en $\frac{dF(t)}{dt} = q^2$. El lado izquierdo depende solo de $t$ y el derecho solo de $q$. Esto es una contradicción, por lo que no existe tal $F(q, t)$.
    

_(Estos dos ejemplos, $g_1 = \dot{q}^2$ y $g_2 = q^2$, son linealmente independientes)._
