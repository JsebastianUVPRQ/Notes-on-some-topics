## Tratamiento Completo de Electrodiámica: Radiación y Covariancia

### Unidad No. 7: RADIACIÓN DE ONDAS ELECTROMAGNÉTICAS

#### 7.1 Potenciales de un sistema de cargas
En electrodinámica, los campos electromagnéticos se derivan de potenciales escalares ($\phi$) y vectoriales ($\vec{A}$). Para sistemas con fuentes dependientes del tiempo ($\rho(\vec{r}, t)$, $\vec{J}(\vec{r}, t)$), es crucial usar los **potenciales retardados**. Estos incorporan el retardo debido a la velocidad finita de la luz ($c$), asegurando causalidad. La solución a las ecuaciones de onda inhomogéneas para los potenciales en el gauge de Lorenz ($\nabla \cdot \vec{A} + \frac{1}{c^2} \frac{\partial \phi}{\partial t} = 0$) es:

$$
\phi(\vec{r}, t) = \frac{1}{4\pi\epsilon_0} \int \frac{\rho(\vec{r}', t_r)}{|\vec{r} - \vec{r}'|}  d^3r'
$$
$$
\vec{A}(\vec{r}, t) = \frac{\mu_0}{4\pi} \int \frac{\vec{J}(\vec{r}', t_r)}{|\vec{r} - \vec{r}'|}  d^3r'
$$

donde $t_r = t - \frac{|\vec{r} - \vec{r}'|}{c}$ es el **tiempo retardado**. La densidad de carga y corriente se evalúan en el momento en que la "señal" salió de la fuente para llegar al punto de observación $\vec{r}$ en el tiempo $t$. Los campos se obtienen luego como:
$$
\vec{E} = -\nabla \phi - \frac{\partial \vec{A}}{\partial t}, \quad \vec{B} = \nabla \times \vec{A}.
$$

Estos potenciales son fundamentales para calcular la radiación generada por distribuciones arbitrarias de carga y corriente.

#### 7.2 Radiación dipolar
La radiación dipolar eléctrica domina cuando la distribución de carga tiene un momento dipolar eléctrico $\vec{p}(t)$ variable en el tiempo y la longitud de onda de la radiación es mucho mayor que el tamaño de la fuente ($\lambda \gg d$). Expandiendo el potencial vectorial retardado en potencias de $kd$ (donde $k = \omega/c$ es el número de onda), el término líder es:

$$
\vec{A}_{dip}(\vec{r}, t) = \frac{\mu_0}{4\pi r} \dot{\vec{p}}(t_r)
$$

donde $\dot{\vec{p}} = \frac{d\vec{p}}{dt}$ es la derivada temporal del momento dipolar eléctrico evaluada en el tiempo retardado. Los campos de radiación (campos lejanos, dependientes de $1/r$) se calculan como:
$$
\vec{E}_{rad} = \frac{\mu_0}{4\pi r} \left[ (\hat{r} \times \ddot{\vec{p}}) \times \hat{r} \right] = -\frac{\mu_0}{4\pi r} \ddot{\vec{p}}_{\perp}
$$
$$
\vec{B}_{rad} = \frac{\mu_0}{4\pi c r} (\hat{r} \times \ddot{\vec{p}})
$$

donde $\ddot{\vec{p}}$ es la segunda derivada de $\vec{p}$ y $\ddot{\vec{p}}_{\perp}$ es su componente perpendicular a $\hat{r}$. La potencia radiada total se obtiene integrando el vector de Poynting $\langle \vec{S} \rangle$ sobre una esfera:

$$
\langle P \rangle = \frac{\mu_0}{6\pi c} \langle |\ddot{\vec{p}}|^2 \rangle \quad \text{(Fórmula de Larmor)}
$$

El patrón de radiación es dipolar: máximo en el plano ecuatorial perpendicular a $\ddot{\vec{p}}$ y nulo a lo largo de su eje.

#### 7.3 Radiación cuadrupolar y magnetodipolar
Cuando el momento dipolar eléctrico es estático o cero (e.g., dipolos puramente magnéticos o distribuciones de carga simétricas), los términos de orden superior en la expansión multipolar se vuelven dominantes.

*   **Radiación Magnetodipolar:** Originada por la variación temporal del momento dipolar magnético $\vec{m}(t)$. El potencial vectorial dipolar magnético es:
    $$
    \vec{A}_{md}(\vec{r}, t) = \frac{\mu_0}{4\pi} \frac{\dot{\vec{m}}(t_r) \times \hat{r}}{r}
    $$
    Los campos de radiación son:
    $$
    \vec{E}_{rad}^{md} = -\frac{\mu_0}{4\pi c r} (\hat{r} \times \ddot{\vec{m}})
    $$
    $$
    \vec{B}_{rad}^{md} = \frac{\mu_0}{4\pi c^2 r} \left[ (\hat{r} \times \ddot{\vec{m}}) \times \hat{r} \right]
    $$
    La potencia radiada total es análoga a Larmor:
    $$
    \langle P_{md} \rangle = \frac{\mu_0}{6\pi c^3} \langle |\ddot{\vec{m}}|^2 \rangle
    $$
    El patrón de radiación es idéntico al dipolar eléctrico pero con $\vec{E}$ y $\vec{B}$ intercambiados.

*   **Radiación Cuadrupolar Eléctrica:** Originada por la variación temporal del tensor momento cuadrupolar eléctrico $Q_{\alpha\beta}(t) = \int \rho (3r'_\alpha r'_\beta - r'^2 \delta_{\alpha\beta}) d^3r'$. El potencial vectorial cuadrupolar es más complejo. El campo eléctrico de radiación es:
    $$
    \vec{E}_{rad}^{Q}(\vec{r}, t) = -\frac{\mu_0}{24\pi c r} \sum_{\alpha,\beta} \dddot{Q}_{\alpha\beta}(t_r) \hat{r}_{\beta} \hat{e}_{\alpha}
    $$
    La potencia radiada total depende de la traza del tensor $\dddot{Q}_{\alpha\beta}$:
    $$
    \langle P_Q \rangle = \frac{\mu_0}{1440\pi c^5} \langle \sum_{\alpha,\beta} |\dddot{Q}_{\alpha\beta}|^2 \rangle
    $$
    El patrón de radiación es más complejo (típicamente de 4 lóbulos) que el dipolar.

La potencia total radiada por una distribución arbitraria es la suma $P = P_{ed} + P_{md} + P_Q + ...$. Generalmente $P_{ed} \gg P_{md} \sim (v/c)^2 P_{ed} \gg P_Q \sim (v/c)^2 P_{md}$ para fuentes no relativistas ($v \ll c$).

#### 7.4 Radiación de una antena de media onda
Una antena lineal delgada de longitud $L = \lambda/2$, alimentada en su centro, es un ejemplo clásico de radiador dipolar. Asumiendo una corriente sinusoidal estacionaria $I(z, t) = I_0 \cos(kz) e^{-i\omega t}$ (con $k=2\pi/\lambda$), donde $z$ va desde $-\lambda/4$ hasta $+\lambda/4$.

*   **Potencial Vectorial y Campos:** El potencial vectorial en la zona de radiación ($r \gg \lambda$) es:
    $$
    \vec{A}(\vec{r}, t) \approx \hat{z} \frac{\mu_0}{4\pi} \frac{e^{i(kr - \omega t)}}{r} I_0 \int_{-\lambda/4}^{\lambda/4} \cos(kz') e^{-ikz'\cos\theta} dz'
    $$
    Resolviendo la integral se obtiene:
    $$
    \vec{A}(\vec{r}, t) \approx \hat{z} \frac{\mu_0 I_0}{2\pi} \frac{e^{i(kr - \omega t)}}{kr} \left[ \frac{\cos\left(\frac{\pi}{2}\cos\theta\right)}{\sin^2\theta} \right]
    $$
    Los campos de radiación son:
    $$
    \vec{E}_{rad} \approx i \frac{\mu_0 c I_0}{2\pi} \frac{e^{i(kr - \omega t)}}{r} \left[ \frac{\cos\left(\frac{\pi}{2}\cos\theta\right)}{\sin\theta} \right] \hat{\theta}
    $$
    $$
    \vec{B}_{rad} \approx \frac{1}{c} \hat{r} \times \vec{E}_{rad}
    $$

*   **Patrón de Radiación:** La intensidad angular normalizada es:
    $$
    \frac{dP}{d\Omega} \propto |\vec{E}_{rad}|^2 \propto \left[ \frac{\cos^2\left(\frac{\pi}{2}\cos\theta\right)}{\sin^2\theta} \right]
    $$
    Tiene un lóbulo principal máximo en $\theta = \pi/2$ (plano ecuatorial) y nulos a lo largo del eje de la antena ($\theta=0, \pi$). Es similar pero no idéntico al dipolo puro.

*   **Resistencia de Radiación:** La potencia total radiada se integra del patrón angular:
    $$
    \langle P \rangle = \frac{1}{2} \int \frac{dP}{d\Omega} d\Omega = \frac{1}{2} R_{rad} I_0^2
    $$
    Para la antena $\lambda/2$, $R_{rad} \approx 73.1 \Omega$. Esta resistencia determina la eficiencia de radiación y la impedancia de entrada.

---

### Unidad No. 8: COVARIANCIA DE LA ELECTRODINÁMICA

#### 8.1 Dinámica de una partícula relativista
La mecánica de Newton falla a velocidades cercanas a $c$. La dinámica relativista se formula en el **espacio-tiempo de Minkowski** de 4 dimensiones. Los eventos se describen por **cuadrivectores posición**:
$$
x^\mu = (ct, x, y, z) \quad (\mu = 0, 1, 2, 3).
$$
El intervalo invariante es $ds^2 = c^2 dt^2 - dx^2 - dy^2 - dz^2 = \eta_{\mu\nu} dx^\mu dx^\nu$, con $\eta_{\mu\nu} = \text{diag}(1, -1, -1, -1)$ la métrica de Minkowski.

*   **Cuadrivelocidad:** Derivada de la posición respecto al tiempo propio invariante $\tau$ ($d\tau = dt / \gamma$):
    $$
    u^\mu = \frac{dx^\mu}{d\tau} = \gamma (c, \vec{v}), \quad \gamma = \frac{1}{\sqrt{1 - v^2/c^2}}
    $$
    Satisface $u^\mu u_\mu = c^2$.

*   **Cuadrimomento:** Combina energía y momento:
    $$
    p^\mu = m u^\mu = \left( \frac{E}{c}, \vec{p} \right)
    $$
    donde $E = \gamma m c^2$ y $\vec{p} = \gamma m \vec{v}$. La norma es $p^\mu p_\mu = m^2 c^2$.

*   **Ecuación de Movimiento:** La fuerza de Minkowski $K^\mu$ generaliza la segunda ley de Newton:
    $$
    K^\mu = \frac{dp^\mu}{d\tau}
    $$
    $K^\mu$ debe satisfacer $K^\mu u_\mu = 0$ para conservar $p^\mu p_\mu$.

#### 8.2 Partícula en un campo electromagnético
La fuerza de Lorentz $\vec{F} = q(\vec{E} + \vec{v} \times \vec{B})$ se generaliza covariante usando el **tensor campo electromagnético** $F^{\mu\nu}$:
$$
F^{\mu\nu} = \begin{pmatrix}
0 & -E_x/c & -E_y/c & -E_z/c \\
E_x/c & 0 & -B_z & B_y \\
E_y/c & B_z & 0 & -B_x \\
E_z/c & -B_y & B_x & 0
\end{pmatrix}
$$

La **fuerza de Minkowski** para una carga $q$ es:
$$
K^\mu = \frac{q}{c} F^{\mu\nu} u_\nu
$$

Explícitamente, la componente temporal ($\mu=0$) da la potencia transferida $\frac{dE}{dt} = q\vec{v}\cdot\vec{E}$, y las componentes espaciales ($\mu=1,2,3$) dan la fuerza de Lorentz $\frac{d\vec{p}}{dt} = q(\vec{E} + \vec{v} \times \vec{B})$. La ecuación de movimiento covariante es:
$$
\frac{dp^\mu}{d\tau} = \frac{q}{c} F^{\mu\nu} u_\nu
$$

#### 8.3 4-corriente y 4-potencial
Las fuentes del campo EM y los potenciales se unifican en cuadrivectores.

*   **Cuadricorriente:** Combina densidad de carga y corriente:
    $$
    J^\mu = (c\rho, \vec{J})
    $$
    Satisface la **ecuación de continuidad covariante** (conservación de carga):
    $$
    \partial_\mu J^\mu = 0 \quad \text{(equivale a } \frac{\partial \rho}{\partial t} + \nabla \cdot \vec{J} = 0\text{)}
    $$

*   **Cuadripotencial:** Combina los potenciales escalar y vectorial:
    $$
    A^\mu = \left( \frac{\phi}{c}, \vec{A} \right)
    $$
    El tensor campo electromagnético se expresa en términos de $A^\mu$:
    $$
    F^{\mu\nu} = \partial^\mu A^\nu - \partial^\nu A^\mu
    $$
    donde $\partial^\mu = (\frac{1}{c}\frac{\partial}{\partial t}, -\nabla)$. Esta definición satisface automáticamente las identidades de Maxwell $\partial^\lambda F^{\mu\nu} + \partial^\mu F^{\nu\lambda} + \partial^\nu F^{\lambda\mu} = 0$ (homogéneas).

#### 8.4 Ecuaciones de Maxwell en notación covariante
Las ecuaciones de Maxwell se condensan en dos ecuaciones tensoriales covariantes bajo transformaciones de Lorentz.

1.  **Ecuaciones Inhomogéneas (Fuentes):**
    $$
    \partial_\mu F^{\mu\nu} = \mu_0 J^\nu
    $$
    *   $\nu = 0$: $\partial_\mu F^{\mu 0} = \partial_i F^{i0} = \nabla \cdot (-\vec{E}/c) = \mu_0 c\rho \implies \nabla \cdot \vec{E} = \rho / \epsilon_0$
    *   $\nu = j$: $\partial_\mu F^{\mu j} = \partial_0 F^{0j} + \partial_i F^{ij} = -\frac{1}{c^2}\frac{\partial E_j}{\partial t} + \nabla \times \vec{B}|_j = \mu_0 J_j \implies \nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial \vec{E}}{\partial t}$

2.  **Ecuaciones Homogéneas (Libres de Fuentes):**
    $$
    \partial^\lambda F^{\mu\nu} + \partial^\mu F^{\nu\lambda} + \partial^\nu F^{\lambda\mu} = 0 \quad \text{(o equivalentemente } \epsilon^{\alpha\beta\mu\nu} \partial_\beta F_{\mu\nu} = 0\text{)}
    $$
    *   Con $\lambda, \mu, \nu$ cíclicos y distintos, se obtienen $\nabla \cdot \vec{B} = 0$ y $\nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}$.

La elegancia y poder de esta formulación radica en su manifiesta covariancia Lorentz.

#### 8.5 Transformación de los campos
Los campos $\vec{E}$ y $\vec{B}$ no son invariantes Lorentz, sino componentes del tensor $F^{\mu\nu}$. Bajo un boost de Lorentz en la dirección $x$ con velocidad $v$:
$$
F'^{\mu\nu} = \Lambda^\mu_{\ \alpha} \Lambda^\nu_{\ \beta} F^{\alpha\beta}
$$
donde $\Lambda$ es la matriz de transformación. Esto conduce a las **transformaciones de los campos**:
$$
\begin{aligned}
E'_x &= E_x \\
E'_y &= \gamma (E_y - v B_z) \\
E'_z &= \gamma (E_z + v B_y) \\
B'_x &= B_x \\
B'_y &= \gamma \left(B_y + \frac{v}{c^2} E_z\right) \\
B'_z &= \gamma \left(B_z - \frac{v}{c^2} E_y\right)
\end{aligned}
$$

*   **Implicaciones:**
    *   $\vec{E}$ y $\vec{B}$ se mezclan. Un campo puramente eléctrico en un sistema puede tener componente magnética en otro.
    *   Las cantidades invariantes son $|\vec{E}|^2 - c^2 |\vec{B}|^2$ y $\vec{E} \cdot \vec{B}$.
    *   Si $\vec{E} \cdot \vec{B} = 0$ y $|\vec{E}| = c |\vec{B}|$ en un sistema, existe un sistema de referencia donde $\vec{E}=0$ o $\vec{B}=0$.

Esta unidad demuestra que el electromagnetismo es inherentemente una teoría relativista, con la covariancia Lorentz como principio fundamental unificador.