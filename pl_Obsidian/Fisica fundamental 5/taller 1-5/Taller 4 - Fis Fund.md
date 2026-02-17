Resuelve PASO-A-PASO explicando los prerrequisitos, conceptos necesarios, tus argumentos de uso de los conceptos y la matemática, etc. debes ser minucioso

---

## Problema 19: Pozo Cuadrado Infinito

**Prerrequisitos y Conceptos:**

- **Ecuación de Schrödinger Independiente del Tiempo (ESIT):** $\hat{H}\psi = E\psi$.
    
- **Condiciones de Frontera:** La función de onda debe anularse donde el potencial es infinito.
    
- **Ortogonalidad:** $\int \psi_m^* \psi_n dx = \delta_{mn}$.
    
- **Evolución Temporal:** Un estado estacionario evoluciona con una fase $e^{-iE_nt/\hbar}$.
    

#### (a) Funciones propias y valores propios

**1. Planteamiento de la Ecuación Diferencial:**

Dentro del pozo ($0 \le x \le L$), $V(x)=0$. La ESIT es:

$$-\frac{\hbar^2}{2m} \frac{d^2\psi(x)}{dx^2} = E\psi(x)$$

Reescribiendo como $\frac{d^2\psi}{dx^2} + k^2\psi = 0$, donde definimos el número de onda $k \equiv \frac{\sqrt{2mE}}{\hbar}$.

**2. Solución General y Condiciones de Frontera:**

La solución general es $\psi(x) = A \sin(kx) + B \cos(kx)$.

- Condición en $x=0$: $\psi(0) = B = 0$. Entonces $\psi(x) = A \sin(kx)$.
    
- Condición en $x=L$: $\psi(L) = A \sin(kL) = 0$.
    
    Para que la solución sea no trivial ($A \neq 0$), debemos tener $\sin(kL) = 0$, lo que implica:
    
    $$k_n L = n\pi \implies k_n = \frac{n\pi}{L}, \quad n=1, 2, 3...$$
    
    _(Nota: $n=0$ anula la función y $n$ negativos no son linealmente independientes)._
    

**3. Valores de Energía ($E_n$):**

Despejando $E$ de la definición de $k$:

$$E_n = \frac{\hbar^2 k_n^2}{2m} = \frac{\hbar^2 \pi^2 n^2}{2mL^2}$$

**4. Normalización:**

Exigimos $\int_0^L |\psi_n(x)|^2 dx = 1$.

$$|A|^2 \int_0^L \sin^2\left(\frac{n\pi x}{L}\right) dx = |A|^2 \left(\frac{L}{2}\right) = 1 \implies A = \sqrt{\frac{2}{L}}$$

Por lo tanto, las funciones propias son:

$$\psi_n(x) = \sqrt{\frac{2}{L}} \sin\left(\frac{n\pi x}{L}\right)$$

---

#### (b) Paquete de ondas inicial $\psi(x,0) = Nx(L-x)$

**i. Constante de normalización $N$**

Calculamos $\int_0^L |\psi(x,0)|^2 dx = 1$.

$$N^2 \int_0^L x^2 (L-x)^2 dx = N^2 \int_0^L (L^2 x^2 - 2L x^3 + x^4) dx = 1$$

Integrando término a término:

$$N^2 \left[ L^2\frac{L^3}{3} - 2L\frac{L^4}{4} + \frac{L^5}{5} \right] = N^2 L^5 \left( \frac{1}{3} - \frac{1}{2} + \frac{1}{5} \right) = N^2 L^5 \left( \frac{10 - 15 + 6}{30} \right) = N^2 \frac{L^5}{30}$$

Igualando a 1 y despejando $N$:

$$N = \sqrt{\frac{30}{L^5}}$$

**ii. Coeficientes de expansión $a_n$**

La teoría de Sturm-Liouville nos dice que podemos expandir la función en la base $\psi_n$:

$$a_n = \langle \psi_n | \psi(0) \rangle = \int_0^L \sqrt{\frac{2}{L}} \sin\left(\frac{n\pi x}{L}\right) \cdot N x(L-x) \, dx$$

Sustituyendo $N$:

$$a_n = \sqrt{\frac{2}{L}} \sqrt{\frac{30}{L^5}} \int_0^L (Lx - x^2) \sin\left(\frac{n\pi x}{L}\right) dx = \frac{\sqrt{60}}{L^3} \underbrace{\int_0^L (Lx - x^2) \sin\left(\frac{n\pi x}{L}\right) dx}_{I}$$

Esta integral se resuelve por partes dos veces o usando tablas. El resultado es:

- Si $n$ es par, la integral se anula (por la simetría de la función inicial respecto a $L/2$).
    
- Si $n$ es impar:
    
    $$I = \frac{4L^3}{(n\pi)^3}$$
    
    Sustituyendo $I$ en la expresión de $a_n$:
    
    $$a_n = \frac{2\sqrt{15}}{L^3} \left[ \frac{2L^3 (1 - (-1)^n)}{(n\pi)^3} \right]$$
    
    Simplificando:
    
    $$a_n = \begin{cases} 0 & \text{si } n \text{ es par} \\ \frac{8\sqrt{15}}{(n\pi)^3} & \text{si } n \text{ es impar} \end{cases}$$
    

---

#### (c) Evolución Temporal y Graficación

**Serie Temporal:**

La función de onda completa es:

$$\psi(x,t) = \sum_{n \text{ impar}} \frac{8\sqrt{15}}{(n\pi)^3} \sqrt{\frac{2}{L}} \sin\left(\frac{n\pi x}{L}\right) e^{-i E_n t / \hbar}$$

Donde $E_n = n^2 E_1$.

**Análisis de tiempos especiales:**

Nos piden evaluar en $t = \nu T$, con $T = \frac{\pi\hbar}{E_1}$.

El factor de fase temporal es:

$$\exp\left( -i \frac{E_n (\nu T)}{\hbar} \right) = \exp\left( -i \frac{n^2 E_1 \nu \pi \hbar}{\hbar E_1} \right) = \exp(-i \pi \nu n^2)$$

Dado que $n$ es impar (digamos $n=2k+1$), entonces $n^2$ también es impar.

$$n^2 = (2k+1)^2 = 4k^2 + 4k + 1 = 2(2k^2+2k) + 1 \quad (\text{Impar})$$

Entonces la fase es $(-1)^{\nu \cdot (\text{impar})} = (-1)^\nu$.

**Casos para $\nu$:**

1. **$\nu$ es par:** $(-1)^\nu = 1$.
    
    $$\psi(x, \nu T) = \sum a_n \psi_n(x) (1) = \psi(x, 0)$$
    
    **Resultado:** La función de onda vuelve a su forma original exacta.
    
2. **$\nu$ es impar:** $(-1)^\nu = -1$.
    
    $$\psi(x, \nu T) = \sum a_n \psi_n(x) (-1) = -\psi(x, 0)$$
    
    **Resultado:** La función de onda es la original invertida (signo negativo global), lo cual físicamente representa la misma densidad de probabilidad $|\psi|^2$.
    

**Gráfica:**

Es una parábola invertida (forma de $x(L-x)$) que oscila entre positiva y negativa ("respirando" fase) pero manteniendo su forma de densidad de probabilidad estática en estos instantes precisos.

---

## Problema 20: Potencial Delta de Dirac

**Prerrequisitos:**

- **Propiedad de filtrado de la Delta:** $\int f(x)\delta(x)dx = f(0)$.
    
- **Discontinuidad de la derivada:** En presencia de un potencial delta, la derivada de la función de onda tiene un salto.
    

#### (a) Estado ligado y Energía

El potencial es $V(x) = -g\delta(x)$. Buscamos estados ligados ($E < 0$). Definimos la energía como $E = -\frac{\hbar^2 \kappa^2}{2m}$, donde $\kappa > 0$.

**1. Regiones fuera del origen ($x \neq 0$):**

La ecuación es $-\frac{\hbar^2}{2m}\psi'' = E\psi$, o $\psi'' - \kappa^2 \psi = 0$.

- Para $x < 0$: $\psi(x) = A e^{\kappa x}$ (descartamos $e^{-\kappa x}$ porque diverge en $-\infty$).
    
- Para $x > 0$: $\psi(x) = B e^{-\kappa x}$ (descartamos $e^{\kappa x}$ porque diverge en $+\infty$).
    

**2. Continuidad en $x=0$:**

$\psi(0^-) = \psi(0^+) \implies A = B$.

Por lo tanto, $\psi(x) = A e^{-\kappa|x|}$.

**3. Condición de la Derivada (Salto):**

Integramos la ecuación de Schrödinger de $-\epsilon$ a $\epsilon$ (como indica la ayuda del problema):

$$-\frac{\hbar^2}{2m} \left( \psi'(\epsilon) - \psi'(-\epsilon) \right) - g\psi(0) = 0$$

$$\Delta \psi' = -\frac{2mg}{\hbar^2} \psi(0)$$

Calculamos las derivadas:

- $x > 0 \implies \psi' = -\kappa A e^{-\kappa x} \implies \psi'(0^+) = -\kappa A$
    
- $x < 0 \implies \psi' = \kappa A e^{\kappa x} \implies \psi'(0^-) = \kappa A$
    
    Restamos:
    
    $$(-\kappa A) - (\kappa A) = -\frac{2mg}{\hbar^2} A$$
    
    $$-2\kappa = -\frac{2mg}{\hbar^2} \implies \kappa = \frac{mg}{\hbar^2}$$
    
    +1
    

**4. Resultados:**

- **Energía:** $E = -\frac{\hbar^2 \kappa^2}{2m} = -\frac{mg^2}{2\hbar^2}$.
    
- **Función de onda:** Normalizamos $\int_{-\infty}^\infty |A|^2 e^{-2\kappa|x|} dx = 1$.
    
    $$2|A|^2 \int_0^\infty e^{-2\kappa x} dx = 2|A|^2 \frac{1}{2\kappa} = \frac{|A|^2}{\kappa} = 1 \implies A = \sqrt{\kappa}$$
    
    $$\psi(x) = \sqrt{\kappa} e^{-\kappa|x|} = \frac{\sqrt{mg}}{\hbar} e^{-\frac{mg}{\hbar^2}|x|}$$
    

---

#### (b)

Incertidumbres $\Delta x$ y $\Delta p$

**Posición:**

Por simetría (función par $|\psi|^2$), $\langle x \rangle = 0$.

Calculamos $\langle x^2 \rangle$:

$$\langle x^2 \rangle = \int_{-\infty}^\infty x^2 (\kappa e^{-2\kappa|x|}) dx = 2\kappa \int_0^\infty x^2 e^{-2\kappa x} dx$$

Usando $\int_0^\infty x^n e^{-ax} dx = n!/a^{n+1}$:

$$\langle x^2 \rangle = 2\kappa \frac{2!}{(2\kappa)^3} = \frac{4\kappa}{8\kappa^3} = \frac{1}{2\kappa^2}$$

$$\Delta x = \sqrt{\langle x^2 \rangle - \langle x \rangle^2} = \frac{1}{\sqrt{2}\kappa}$$

**Momento:**

El valor esperado $\langle p \rangle = 0$ (la función de onda es real y es un estado ligado estático).

Calculamos $\langle p^2 \rangle$. Podemos usar integración directa o el Teorema del Virial, pero integremos:

$$\langle p^2 \rangle = \int_{-\infty}^\infty \psi^* (-\hbar^2 \frac{d^2}{dx^2}) \psi dx = \hbar^2 \int_{-\infty}^\infty |\frac{d\psi}{dx}|^2 dx$$

(Usamos la forma de la energía cinética. Ojo: $\frac{d^2}{dx^2}$ introduce una delta, es más seguro integrar el cuadrado de la primera derivada).

La derivada es $\psi'(x) = -\kappa \sqrt{\kappa} e^{-\kappa x}$ para $x>0$ (y signo opuesto para $x<0$).

$$|\psi'(x)|^2 = \kappa^3 e^{-2\kappa|x|}$$

$$\langle p^2 \rangle = \hbar^2 \int_{-\infty}^\infty \kappa^3 e^{-2\kappa|x|} dx = \hbar^2 \kappa^2 \underbrace{\int_{-\infty}^\infty \kappa e^{-2\kappa|x|} dx}_{1} = \hbar^2 \kappa^2$$

$$\Delta p = \sqrt{\hbar^2 \kappa^2} = \hbar \kappa$$

**Verificación:** $\Delta x \Delta p = \frac{1}{\sqrt{2}\kappa} (\hbar \kappa) = \frac{\hbar}{\sqrt{2}} \approx 0.707 \hbar > 0.5 \hbar$. Cumple Heisenberg.

---

#### (c)

Espacio de Momento

+1

Calculamos la Transformada de Fourier:

$$\phi(p) = \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^\infty \psi(x) e^{-ipx/\hbar} dx$$

$$\phi(p) = \sqrt{\frac{\kappa}{2\pi\hbar}} \int_{-\infty}^\infty e^{-\kappa|x|} e^{-ipx/\hbar} dx$$

Separamos la integral:

$$\int_{-\infty}^0 e^{(\kappa - ip/\hbar)x} dx + \int_0^\infty e^{(-\kappa - ip/\hbar)x} dx$$

1. $\left[ \frac{e^{(\kappa - ip/\hbar)x}}{\kappa - ip/\hbar} \right]_{-\infty}^0 = \frac{1}{\kappa - ip/\hbar}$
    
2. $\left[ \frac{e^{-(\kappa + ip/\hbar)x}}{-(\kappa + ip/\hbar)} \right]_0^\infty = \frac{1}{\kappa + ip/\hbar}$
    

Sumamos:

$$\frac{1}{\kappa - \frac{ip}{\hbar}} + \frac{1}{\kappa + \frac{ip}{\hbar}} = \frac{\kappa + \frac{ip}{\hbar} + \kappa - \frac{ip}{\hbar}}{\kappa^2 + \frac{p^2}{\hbar^2}} = \frac{2\kappa}{\kappa^2 + (p/\hbar)^2} = \frac{2\hbar^2\kappa}{\hbar^2\kappa^2 + p^2}$$

Función de onda en momento:

$$\phi(p) = \sqrt{\frac{\kappa}{2\pi\hbar}} \frac{2\kappa}{ (\kappa^2 + p^2/\hbar^2) } = \sqrt{\frac{2}{\pi}} \frac{(\hbar \kappa)^{3/2}}{(\hbar\kappa)^2 + p^2}$$

Esta es una distribución Lorentziana (o de Cauchy).

**Máximo de la distribución:**

La función $\phi(p)$ (y la probabilidad $|\phi(p)|^2$) tiene su máximo donde el denominador es mínimo. Dado que $p^2 \ge 0$, el mínimo denominador ocurre en **$p=0$**.

Por lo tanto, la partícula tiene mayor probabilidad de tener momento cero, lo cual es consistente con $\langle p \rangle = 0$.

---
Hola, **Sebastián**. Es un gusto saludarte de nuevo.

Estos dos problemas son fundamentales en mecánica cuántica porque rompen con la intuición clásica: el **Problema 21** trata sobre la dispersión (scattering) y cómo una partícula "siente" un cambio de potencial incluso si tiene energía suficiente para pasar, y el **Problema 22** es la demostración matemática del **Efecto Túnel**, base de fenómenos como la desintegración alfa o los microscopios de efecto túnel (STM).

A continuación, presento la solución rigurosa, paso a paso, utilizando el formalismo de la Ecuación de Schrödinger.

---

### **Prerrequisitos y Conceptos Clave**

1. **Ecuación de Schrödinger Independiente del Tiempo (EES):**
    
    $$ -\frac{\hbar^2}{2m} \frac{d^2\psi}{dx^2} + V(x)\psi = E\psi $$
    
    La reescribimos siempre como $\psi'' + k^2 \psi = 0$ (región oscilatoria) o $\psi'' - \kappa^2 \psi = 0$ (región exponencial).
    
2. **Continuidad de la Función de Onda:**
    
    Para potenciales finitos (como escalones y barreras), tanto $\psi(x)$ como su derivada $\psi'(x)$ deben ser continuas en las fronteras donde cambia el potencial. Esto garantiza la conservación de la probabilidad y del flujo de probabilidad.
    
3. **Espectro Continuo vs. Discreto:**
    
    - **Discreto:** Cuando la partícula está confinada (pozo infinito).
        
    - **Continuo:** Cuando la partícula es libre de moverse hacia el infinito en al menos una dirección (scattering).
        

---

## **Solución Problema 21: Potencial de Paso (Reflexión Cuántica)**

El potencial es un escalón que cae hacia la izquierda:

- Región I ($x < 0$): $V(x) = -\frac{\hbar^2 k_0^2}{2m}$ (Pozo/Valle).
    
- Región II ($x \ge 0$): $V(x) = 0$ (Meseta).
    

#### **(a) Soluciones independientes y Espectro**

**Caso 1: Energía Positiva ($E > 0$)**

Definimos $E = \frac{\hbar^2 k^2}{2m}$.

- **Región II ($x > 0$):** $V=0$.
    
    $$ \frac{d^2\psi}{dx^2} + k^2\psi = 0 $$
    
    Dos soluciones linealmente independientes (ondas planas): $\psi_R(x) = e^{ikx}$ (viaja a derecha) y $\psi_L(x) = e^{-ikx}$ (viaja a izquierda).
    
- **Región I ($x < 0$):** $V = -|V_0|$.
    
    La energía cinética efectiva es $E - V = E + |V_0|$.
    
    $$ \frac{d^2\psi}{dx^2} + \frac{2m(E+|V_0|)}{\hbar^2}\psi = 0 $$
    
    Definimos el número de onda $q$:
    
    $$ q^2 = \frac{2mE}{\hbar^2} + \frac{2m|V_0|}{\hbar^2} = k^2 + k_0^2 $$
    
    Soluciones independientes: $e^{iqx}$ y $e^{-iqx}$.
    

**Caso 2: Energía Negativa ($E < 0$) pero $E > -|V_0|$**

Supongamos $E = -\frac{\hbar^2 \kappa^2}{2m}$.

- **Región II ($x > 0$):**
    
    $$ \psi'' - \kappa^2 \psi = 0 $$
    
    Soluciones: $e^{-\kappa x}$ (decaimiento físico) y $e^{\kappa x}$ (divergencia no física si $x \to \infty$).
    
- **Región I ($x < 0$):**
    
    Si la energía es mayor que el fondo del pozo, la partícula aún tiene energía cinética local positiva.
    
    Soluciones oscilatorias: $e^{iq'x}$ y $e^{-iq'x}$.
    

**¿Por qué el espectro es continuo?**

El espectro de energías es continuo porque el sistema no está confinado espacialmente. En la región $x < 0$ (o en $x>0$ si $E>0$), la partícula se comporta como una onda libre. No hay condiciones de frontera en $\pm \infty$ que fuercen a la onda a anularse en ambos extremos simultáneamente (como ocurre en el pozo infinito). Para cualquier valor de $E > -|V_0|$, podemos encontrar una solución válida y normalizable en el sentido de ondas planas (función delta de Dirac).

---

#### **(b) Dispersión desde $+\infty$ (Incidencia desde la derecha)**

**Argumento Físico de la Forma de la Solución:**

La partícula viene desde $+\infty$ viajando hacia la izquierda.

1. **Región II ($x > 0$):**
    
    - **Incidente:** Debe viajar hacia $-x$. Forma: $e^{-ikx}$.
        
    - **Reflejada:** Al chocar con el cambio de potencial en $x=0$, parte de la onda rebota hacia $+x$. Forma: $R e^{ikx}$.
        
    - Total: $\psi_{II}(x) = e^{-ikx} + R e^{ikx}$.
        
2. **Región I ($x < 0$):**
    
    - **Transmitida:** La onda pasa al pozo y sigue viajando hacia $-\infty$. No hay nada en $-\infty$ que la haga rebotar, por lo que solo existe la onda viajera hacia la izquierda.
        
    - Momento en esta región: $\hbar q$.
        
    - Forma: $T e^{-iqx}$ (el signo menos en el exponente indica dirección $-x$).
        
    - Total: $\psi_{I}(x) = T e^{-iqx}$.
        

**Cálculo de $R$ y $T$:**

Aplicamos condiciones de continuidad en $x=0$:

1. **Continuidad de $\psi$:**
    
    $$ \psi_I(0) = \psi_{II}(0) \implies T e^0 = e^0 + R e^0 $$
    
    $$ T = 1 + R \quad \text{(Ec. 1)} $$
    
2. **Continuidad de $\psi'$:**
    
    Derivadas: $\psi'_I = -iq T e^{-iqx}$ y $\psi'_{II} = -ik e^{-ikx} + ik R e^{ikx}$.
    
    Evaluando en $x=0$:
    
    $$ -iq T = -ik + ik R $$
    
    Dividimos por $-i$:
    
    $$ qT = k(1 - R) \quad \text{(Ec. 2)} $$
    

**Resolviendo el sistema:**

Sustituimos (Ec. 1) en (Ec. 2):

$$ q(1+R) = k(1-R) $$

$$ q + qR = k - kR $$

$$ R(q + k) = k - q $$

$$ R = \frac{k - q}{k + q} $$

Para encontrar $T$, usamos $T = 1 + R$:

$$ T = 1 + \frac{k - q}{k + q} = \frac{k + q + k - q}{k + q} = \frac{2k}{k + q} $$

**Resultados:**

$$ R(k) = \frac{k - \sqrt{k^2 + k_0^2}}{k + \sqrt{k^2 + k_0^2}}, \quad T(k) = \frac{2k}{k + \sqrt{k^2 + k_0^2}} $$

---

#### **(c) Análisis de Límites**

**Límite de baja energía ($k \to 0$):**

Aquí, la energía cinética incidente es muy pequeña comparada con la profundidad del pozo.

Sabemos que $q = \sqrt{k^2 + k_0^2}$.

Si $k \to 0$, podemos hacer una expansión de Taylor alrededor de $k=0$.

$$ q = (k_0^2 + k^2)^{1/2} = k_0 (1 + \frac{k^2}{k_0^2})^{1/2} \approx k_0 (1 + \frac{k^2}{2k_0^2}) \approx k_0 $$

(A primer orden, $q \approx k_0$).

Retomamos $R$:

$$ R = \frac{k - q}{k + q} $$

Reescribimos sacando factor común en el denominador para ver la estructura $1/(1+x) \approx 1-x$:

$$ R = \frac{k - q}{q(1 + k/q)} \approx \frac{k - k_0}{k_0(1 + k/k_0)} \approx \frac{k-k_0}{k_0} (1 - \frac{k}{k_0}) $$

Sin embargo, el problema sugiere una forma específica $-1 + 2bk$. Vamos a manipular algebraicamente para llegar ahí directamente:

$$ R = \frac{k-q}{k+q} = \frac{-(q-k)}{q+k} = - \frac{q-k}{q+k} $$

Multiplicamos y dividimos por el conjugado o simplemente evaluamos el límite principal.

Cuando $k \to 0$, $q \to k_0$.

$$ R \to \frac{-k_0}{k_0} = -1 $$

Para ver el siguiente término, escribimos:

$$ R = \frac{k - (k_0 + O(k^2))}{k + k_0 + O(k^2)} \approx \frac{k - k_0}{k + k_0} = \frac{-k_0(1 - k/k_0)}{k_0(1 + k/k_0)} = -(1 - \frac{k}{k_0})(1 - \frac{k}{k_0}) $$

(Usando la serie geométrica $\frac{1}{1+x} \approx 1-x$).

$$ R \approx -(1 - \frac{2k}{k_0}) = -1 + \frac{2k}{k_0} $$

Definiendo $b = 1/k_0$, obtenemos:

$$ R \approx -1 + 2bk $$

**Probabilidad de Reflexión $P_R$ (o Coeficiente de Reflexión $\mathcal{R}$):**

$$ P_R = |R|^2 \approx |-1 + 2bk|^2 = (1 - 2bk)^2 \approx 1 - 4bk + \mathcal{O}(k^2) $$

**Límite de alta energía ($E \to \infty \implies k \to \infty$):**

Si $E$ es muy grande, el pozo "se siente" menos.

$$ q = \sqrt{k^2 + k_0^2} = k \sqrt{1 + k_0^2/k^2} \approx k $$

$$ R = \frac{k - q}{k + q} \approx \frac{k - k}{2k} = 0 $$

**Interpretación:** A energías infinitas, la partícula no ve el cambio de potencial y pasa sin reflejarse ($P_R \to 0$, $T \to 1$).

---

## **Solución Problema 22: Efecto Túnel en Barrera**

![quantum barrier tunneling, generada por IA](https://encrypted-tbn0.gstatic.com/licensed-image?q=tbn:ANd9GcS96ian3kYy_tOg9jiSTk6g8Akol6XOdFSK0q_ZbGPD36U3pwSOzl-0BsAZKuLRpsNBusnCO-deNN8K6HRMlZ6JL6ts1GTeqIaSpTfifGo1ZVt2yno)

Shutterstock

Explorar

Aquí tenemos una barrera rectangular de ancho $2a$ y altura $V_0$.

$E < V_0$, por lo que clásicamente la partícula rebotaría. Cuánticamente, tunela.

#### **Definición de Regiones y Funciones**

- **Región I ($x < -a$):** $V=0$. Incidencia y reflexión.
    
    $$ \phi_I(x) = A e^{ikx} + B e^{-ikx} $$
    
- **Región II ($-a \le x \le a$):** $V=V_0$.
    
    Como $E < V_0$, el número de onda es imaginario. Definimos $q = \sqrt{2m(V_0 - E)}/\hbar = \sqrt{k_0^2 - k^2}$.
    
    $$ \phi_{II}(x) = D e^{-qx} + F e^{qx} $$
    
    _(Nota: El problema usa $q$ para la región de barrera, cuidado de no confundir con el problema anterior)._
    
    _(Nota 2: El problema sugiere usar funciones hiperbólicas al final, pero partiremos de exponenciales para el álgebra)._
    
- **Región III ($x > a$):** $V=0$. Transmisión.
    
    $$ \phi_{III}(x) = C e^{ikx} $$
    

#### **Estrategia Matemática (Cálculo de Transmisión)**

Queremos $P(E) = |C/A|^2$. Debemos relacionar $A$ con $C$ usando las 4 condiciones de frontera (continuidad de $\phi$ y $\phi'$ en $x=-a$ y $x=a$).

**Paso 1: Frontera en $x=a$ (Interfaz II-III)**

$$ \phi_{II}(a) = \phi_{III}(a) \implies D e^{-qa} + F e^{qa} = C e^{ika} $$

$$ \phi'_{II}(a) = \phi'_{III}(a) \implies -q D e^{-qa} + q F e^{qa} = ik C e^{ika} $$

Este es un sistema 2x2 para despejar $D$ y $F$ en función de $C$.

Multiplicando la primera ecuación por $q$ y sumando/restando con la segunda:

1. $2q F e^{qa} = (q + ik) C e^{ika} \implies F = \frac{q+ik}{2q} e^{(ik-q)a} C$
    
2. $2q D e^{-qa} = (q - ik) C e^{ika} \implies D = \frac{q-ik}{2q} e^{(ik+q)a} C$
    

**Paso 2: Frontera en $x=-a$ (Interfaz I-II)**

$$ \phi_I(-a) = \phi_{II}(-a) \implies A e^{-ika} + B e^{ika} = D e^{qa} + F e^{-qa} $$

$$ \phi'_I(-a) = \phi'_{II}(-a) \implies ik A e^{-ika} - ik B e^{ika} = -q D e^{qa} + q F e^{-qa} $$

Para eliminar $B$ y quedarnos solo con $A$, multiplicamos la primera por $ik$ y sumamos la segunda:

$$ 2ik A e^{-ika} = D e^{qa} (ik - q) + F e^{-qa} (ik + q) $$

$$ A = \frac{e^{ika}}{2ik} \left[ D e^{qa} (ik - q) + F e^{-qa} (ik + q) \right] $$

**Paso 3: Sustitución y Álgebra (El paso crucial)**

Sustituimos las expresiones de $D$ y $F$ (del Paso 1) en la ecuación de $A$:

$$ A = \frac{e^{ika}}{2ik} \left[ \left(\frac{q-ik}{2q} e^{(ik+q)a} C\right) e^{qa} (ik - q) + \left(\frac{q+ik}{2q} e^{(ik-q)a} C\right) e^{-qa} (ik + q) \right] $$

Factorizamos $C e^{ika}$ (que viene de $D$ y $F$):

$$ \frac{A}{C} = \frac{e^{2ika}}{4ikq} \left[ (q-ik)(ik-q) e^{2qa} + (q+ik)(ik+q) e^{-2qa} \right] $$

Observa los términos:

- $(q-ik)(ik-q) = -(q-ik)^2 = -(q^2 - 2iqk - k^2)$
    
- $(q+ik)(ik+q) = (q+ik)^2 = q^2 + 2iqk - k^2$
    

Reagrupando términos:

$$ \frac{A}{C} e^{-2ika} = \frac{1}{4ikq} \left[ -(q^2 - k^2 - 2iqk)e^{2qa} + (q^2 - k^2 + 2iqk)e^{-2qa} \right] $$

Usamos $e^{2qa} = \cosh(2qa) + \sinh(2qa)$ y $e^{-2qa} = \cosh(2qa) - \sinh(2qa)$.

Al hacer el álgebra con cuidado, los términos se agrupan:

$$ \frac{A}{C} e^{-2ika} = \cosh(2qa) + i \frac{k^2 - q^2}{2kq} \sinh(2qa) $$

_(Verifica el signo: $ikq$ en el denominador sube como $-i$. El término real viene de los senos hiperbólicos cruzados con $i$, y el imaginario de los cosenos)._

En realidad, la forma estándar simplificada es:

$$ \frac{A}{C} \sim \cosh(2qa) + i \frac{q^2-k^2}{2kq} \sinh(2qa) $$

(Dependiendo de la convención de signos, pero el módulo cuadrado es lo que importa).

**Paso 4: El coeficiente de transmisión**

Calculamos $P(E) = |C/A|^2 = |A/C|^{-2}$.

$$ \left| \frac{A}{C} \right|^2 = \cosh^2(2qa) + \left( \frac{k^2 - q^2}{2kq} \right)^2 \sinh^2(2qa) $$

Usamos la identidad $\cosh^2 x = 1 + \sinh^2 x$:

$$ \left| \frac{A}{C} \right|^2 = 1 + \sinh^2(2qa) + \frac{(k^2 - q^2)^2}{4k^2q^2} \sinh^2(2qa) $$

Factorizamos $\sinh^2$:

$$ \left| \frac{A}{C} \right|^2 = 1 + \left( 1 + \frac{(k^2 - q^2)^2}{4k^2q^2} \right) \sinh^2(2qa) $$

El término entre paréntesis es:

$$ \frac{4k^2q^2 + k^4 - 2k^2q^2 + q^4}{4k^2q^2} = \frac{(k^2+q^2)^2}{4k^2q^2} $$

El problema define $\epsilon = \frac{q}{k} - \frac{k}{q} = \frac{q^2-k^2}{kq}$. Si elevamos al cuadrado $\epsilon^2 = \frac{q^4 - 2q^2k^2 + k^4}{k^2q^2}$.

La fórmula del enunciado pide:

$$ 1 + \frac{\epsilon^2}{4} = 1 + \frac{(q/k - k/q)^2}{4} $$

Que al operar coincide con nuestro término multiplicativo.

Sustituyendo las energías ($q^2 \propto V_0 - E$, $k^2 \propto E$):

$$ \frac{(k^2+q^2)^2}{4k^2q^2} = \frac{(V_0)^2}{4 E (V_0 - E)} $$

(Ya que $k^2+q^2 \propto E + (V_0-E) = V_0$).

Finalmente:

$$ P(E) = \frac{1}{1 + \frac{V_0^2}{4E(V_0-E)} \sinh^2(2qa)} $$

Dividiendo numerador y denominador por $V_0^2$ llegas a la forma dada en el enunciado:

$$ P(E) = \frac{1 - E/V_0}{(1 - E/V_0) + \frac{V_0}{4E} \sinh^2(2qa)} $$

---

#### **Límite de Barrera Gruesa ($aq \gg 1$)**

Si la barrera es muy ancha o muy alta ($aq \gg 1$), entonces $\sinh(2qa) \approx \frac{e^{2qa}}{2}$.

$$ \sinh^2(2qa) \approx \frac{e^{4qa}}{4} $$

Sustituimos en la ecuación inversa de transmisión:

$$ \frac{1}{P(E)} \approx \frac{V_0^2}{4E(V_0-E)} \frac{e^{4qa}}{4} = \frac{V_0^2}{16E(V_0-E)} e^{4qa} $$

Invirtiendo:

$$ P(E) \approx \frac{16E(V_0-E)}{V_0^2} e^{-4qa} $$

Esta es exactamente la **Ecuación (2)** pedida. Este factor exponencial $e^{-4qa}$ es el sello distintivo del efecto túnel y es lo que gobierna, por ejemplo, las vidas medias enormemente variadas en la desintegración alfa.