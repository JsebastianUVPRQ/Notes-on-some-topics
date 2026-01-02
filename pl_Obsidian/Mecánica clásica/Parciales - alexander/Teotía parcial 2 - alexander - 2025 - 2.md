
---


---

## 1. Teoría de Dispersión (Scattering) y Fuerzas Centrales

_Relevante para el Ejercicio 1 (Rutherford)_

Este tema conecta la geometría de una trayectoria con las leyes de conservación.

#### A. Conceptos Físicos Clave

1. **Potencial Central:** Un campo de fuerza que solo depende de la distancia al origen, $V(r)$. Esto implica que el torque es cero y, por tanto, el **Momento Angular ($L$) se conserva**. El movimiento siempre ocurre en un plano.
    
2. **Ecuación de la Órbita:** En lugar de buscar $r(t)$, buscamos la forma geométrica de la trayectoria $r(\phi)$. Para potenciales tipo $1/r$ (gravitatorio o eléctrico), la solución siempre es una **sección cónica** (elipse, parábola o hipérbola).
    
    - _Eccentricidad ($e$):_ Determina la forma. Si $e > 1$, es una hipérbola (dispersión/trayectoria abierta). Si $0 \le e < 1$, es una elipse (órbita cerrada).
        
3. **Parámetro de Impacto ($b$):** Es la distancia perpendicular entre la velocidad inicial de la partícula (en el infinito) y el centro de fuerza. Es la "puntería" del disparo.
    
4. **Sección Eficaz Diferencial ($d\sigma/d\Omega$):** Es el concepto más importante. Representa la probabilidad de que una partícula sea desviada en un ángulo sólido específico. Físicamente, relaciona el área geométrica del "blanco" con el ángulo de salida.
    

#### B. Herramientas Matemáticas

1. **Geometría de Hipérbolas:** Debes saber relacionar la ecuación polar $r = \frac{l^2/mk}{1+e\cos\phi}$ con sus asíntotas. El ángulo de la asíntota define el ángulo de salida.
    
2. Cálculo Diferencial (Derivada de la Cadena):
    
    La fórmula maestra para la sección eficaz clásica es:
    
    $$\frac{d\sigma}{d\Omega} = \frac{b}{\sin \theta} \left| \frac{db}{d\theta} \right|$$
    
    Necesitas expresar $b$ en función de $\theta$, derivar y sustituir.
    
3. **Identidades Trigonométricas:** Fundamental. En el ejercicio 1, el truco matemático clave fue convertir $\cot(\theta/2)$ y $\csc(\theta/2)$ para simplificar la expresión final.
    

---

## 2. Osciladores Acoplados y Formalismo Lagrangiano

Aquí pasamos de estudiar una partícula a estudiar sistemas de múltiples cuerpos conectados.

#### A. Conceptos Físicos Clave

1. **Coordenadas Generalizadas ($q_i$):** El número mínimo de variables necesarias para describir el sistema (grados de libertad).
    
2. **El Lagrangiano ($L = T - V$):** La función que resume la dinámica del sistema.
    
3. Aproximación de Pequeñas Oscilaciones:
    
    Cualquier potencial $V(q)$ que tenga un mínimo estable (equilibrio) se comporta como una parábola cerca de ese mínimo (Serie de Taylor).
    
    $$V(q) \approx V(0) + \frac{1}{2} k q^2$$
    
    Esto linealiza las ecuaciones diferenciales, convirtiéndolas en osciladores armónicos.
    
4. **Modos Normales:** En un sistema acoplado, las masas no oscilan caóticamente. Existen frecuencias especiales ("eigenfrecuencias") donde todas las partes del sistema se mueven sinusoidalmente con la misma frecuencia y fase.
    

#### B. Herramientas Matemáticas

1. Matrices y Álgebra Lineal:
    
    El problema físico se traduce en resolver la ecuación secular:
    
    $$\det(\mathbf{K} - \omega^2 \mathbf{M}) = 0$$
    
    - $\mathbf{M}$: Matriz de masas (o cinética).
        
    - $\mathbf{K}$: Matriz de rigidez (o potencial, segundas derivadas de V).
        
2. **Diagonalización:** Encontrar las frecuencias normales es equivalente a encontrar los **eigenvalores** (valores propios) de la matriz del sistema.
    
3. **Ansatz Complejo:** Suponer soluciones de la forma $q(t) = A e^{i\omega t}$ convierte ecuaciones diferenciales en ecuaciones algebraicas.
    

---

## 3. Mecánica Hamiltoniana y Transformaciones Canónicas

_Relevante para el Ejercicio 3_

Este es el nivel más abstracto, fundamental para la mecánica cuántica y la física estadística.

#### A. Conceptos Físicos Clave

1. **Espacio de Fase:** Un espacio de 2n dimensiones donde viven las coordenadas ($q$) y los momentos ($p$). El estado del sistema es un punto en este espacio.
    
2. **Transformación Canónica:** Un cambio de coordenadas $(q, p) \to (Q, P)$ que conserva la "estructura" de las ecuaciones de Hamilton. Es decir, la física no cambia, solo el punto de vista.
    
3. **Corchetes de Poisson $\{ \cdot, \cdot \}$:** Son una operación matemática que mide la "no conmutatividad" clásica. Son el test de oro:
    
    - Si $\{Q, P\}_{q,p} = 1$, la transformación es canónica.
        
4. **Función Generatriz ($F$):** Es una función puente que conecta las variables viejas con las nuevas. Actúa como un potencial del cual se derivan las ecuaciones de transformación. Hay 4 tipos básicos ($F_1, F_2, F_3, F_4$) dependiendo de qué variables mezcles (ej. $F_3(p, Q)$ mezcla momento viejo y coordenada nueva).
    

#### B. Herramientas Matemáticas

1. **Derivadas Parciales:** Todo el ejercicio 3 se basa en calcular derivadas parciales con precisión quirúrgica. Un error de signo aquí destruye el resultado.
    
2. **Propiedades de Logaritmos y Exponenciales:** Como viste en el ejercicio, transformar $Q = \ln(\dots)$ requiere saber derivar funciones compuestas y manipular inversas ($e^Q$).
    
3. Cálculo del Corchete de Poisson:
    
    $$\{f, g\} = \sum \left( \frac{\partial f}{\partial q} \frac{\partial g}{\partial p} - \frac{\partial f}{\partial p} \frac{\partial g}{\partial q} \right)$$
    
    Debes dominar este algoritmo de cálculo.
    

---
---
## ejercicio 4
El objetivo es entender **por qué** escribimos el Lagrangiano de esa forma y qué significan esos símbolos ($u^\mu$, $\tau$, etc.).

---
### Nivel 1: La Crisis y los Postulados (El "Por qué")

En la mecánica clásica (Newton), el tiempo es absoluto. Un segundo es un segundo para todos. Pero el electromagnetismo (Maxwell) decía que la luz viaja a velocidad $c$ sin importar quién la mire. Esto generaba una contradicción.

Einstein lo resolvió con dos postulados:

1. **Las leyes de la física son iguales** en todos los sistemas inerciales.
    
2. **La velocidad de la luz ($c$) es constante** para todos.
    

**Consecuencia:** Para que $c$ sea constante, el tiempo ($t$) y el espacio ($x$) deben estirarse o encogerse. Ya no son entidades separadas; forman un tejido de 4 dimensiones: el **Espacio-Tiempo**.

---

### Nivel 2: La Geometría y el Tiempo Propio (La Herramienta)

Si el tiempo y el espacio cambian según quién mire, ¿hay algo en lo que todos estemos de acuerdo? Sí: el **Intervalo Invariante ($ds^2$)**.

Imagina una partícula moviéndose. Para ella, su propio reloj marca el tiempo "real". A esto le llamamos Tiempo Propio ($\tau$).

La relación fundamental es:

$$ds^2 = c^2 d\tau^2 = c^2 dt^2 - dx^2 - dy^2 - dz^2$$

- $t$: Tiempo medido por un observador externo (coordenada).
    
- $\tau$: Tiempo medido por la partícula (invariante).
    

> **Nota clave:** En relatividad, preferimos derivar respecto a $\tau$ (que es universal para la partícula) y no respecto a $t$ (que depende del observador).

---

### Nivel 3: Cinemática con 4-Vectores (El Lenguaje)

Para hacer física que funcione en el espacio-tiempo, cambiamos nuestros vectores de 3 componentes ($\vec{v}$) por "4-vectores" ($\mu = 0, 1, 2, 3$).

1. La 4-Posición ($x^\mu$):

$$x^\mu = (ct, x, y, z)$$

2. La 4-Velocidad ($u^\mu$):

Aquí está el truco. No definimos la velocidad como $dx/dt$, sino como el cambio de posición respecto al tiempo propio $\tau$:

$$u^\mu = \frac{dx^\mu}{d\tau}$$

¿Cuánto vale la magnitud de esta velocidad?

Debido a la geometría del espacio-tiempo, la "longitud" de este vector 4D es siempre constante:

$$u_\mu u^\mu = c^2$$

(Esta es la restricción que usamos en tu problema anterior).

---

### Nivel 4: Dinámica Lagrangiana (El Problema que resolviste)

Aquí es donde entra el ejercicio. En mecánica clásica, usamos el Principio de Mínima Acción: la naturaleza "elige" el camino que minimiza la acción $S = \int L \, dt$.

En relatividad, queremos que la Acción sea un **escalar de Lorentz** (un número que no cambia si cambiamos de sistema de referencia).

#### A. La Partícula Libre

La cantidad más simple que es invariante para una partícula es su tiempo propio. Así que la Acción es proporcional a la suma de "tics" de su reloj:

$$S = -mc \int d\tau$$

Como $d\tau = \frac{1}{\gamma} dt$, el Lagrangiano libre resulta ser:

$$L_{libre} = -mc^2 \sqrt{1 - v^2/c^2}$$

#### B. Generalizando a 4-vectores (Tu ejercicio)

A veces, es más elegante escribir el Lagrangiano usando la 4-velocidad $u^\mu$ explícitamente para mantener la simetría relativista visible.

El término cinético libre se suele escribir como:

$$L = \frac{1}{2} m u_\mu u^\mu$$

(Técnicamente, esto requiere un truco matemático de "multiplicadores" o fijación de gauge, porque sabemos que $u_\mu u^\mu$ es constante, pero al derivar lo tratamos como variable).

#### C. Añadiendo Interacciones (El Campo Escalar $\phi$)

En tu problema, la partícula ya no es libre. Se mueve a través de un "campo escalar" $\phi(x)$.

- Un campo escalar es como una temperatura en el espacio; es solo un número en cada punto, no empuja en una dirección específica (vector), sino que modifica las propiedades locales.
    

El Lagrangiano del problema era:

$$L = \underbrace{\frac{1}{2} m u_\mu u^\mu}_{\text{Cinética}} + \underbrace{\lambda \phi(x) f(u^2)}_{\text{Interacción}}$$

Lo que descubriste en el ejercicio (que $n=1/2$) implica que la interacción se acopla a la **norma** de la velocidad. Físicamente, este tipo de acoplamiento (donde $n=1/2$) tiene un efecto fascinante: **hace que la masa de la partícula dependa de dónde está**.

Al final, obtuviste un momento:

$$p^\mu = u^\mu (m + \text{algo que depende de } \phi)$$

Esto significa que el campo $\phi$ está actuando como una masa variable. Es el mismo mecanismo (simplificado) por el cual el Campo de Higgs da masa a las partículas en el Modelo Estándar.

### Resumen del camino

1. **Einstein:** El tiempo es relativo ($t$ vs $\tau$).
    
2. **Geometría:** Usamos 4-vectores ($u^\mu$) derivados respecto a $\tau$.
    
3. **Lagrangiano:** Buscamos funciones invariantes para construir la acción.
    
4. **Tu problema:** Un Lagrangiano donde un campo externo modifica la "inercia" (masa) de la partícula.
    

¿Hay algún paso en esta cadena (por ejemplo, la definición de tiempo propio o cómo se deriva Euler-Lagrange en relatividad) que quieras ver con más detalle matemático?