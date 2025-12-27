
## **MECÁNICA CUÁNTICA 1: FUNDAMENTOS Y APLICACIONES**

### **3. CONDICIONES DE CUANTIZACIÓN Y FORMALISMO MATEMÁTICO**

#### **3.1. Homomorfismo entre Álgebra de Poisson y Álgebra de Observables**
La transición de la mecánica clásica a la cuántica representa uno de los cambios paradigmáticos más profundos en la física. El puente matemático entre ambas teorías se establece mediante la **correspondencia de Dirac**, que relaciona las estructuras algebraicas subyacentes.

En mecánica clásica, las variables dinámicas (posición, momento, energía) son funciones sobre el espacio de fases que obedecen el **álgebra de Poisson**. Para dos funciones $f(q,p)$ y $g(q,p)$, el corchete de Poisson se define como:

$$
\{f, g\} = \sum_i \left( \frac{\partial f}{\partial q_i} \frac{\partial g}{\partial p_i} - \frac{\partial f}{\partial p_i} \frac{\partial g}{\partial q_i} \right)
$$

Este objeto matemático codifica la evolución temporal y las simetrías del sistema. Particularmente importante es la relación fundamental: $\{q_i, p_j\} = \delta_{ij}$.

Dirac postuló que en la teoría cuántica, a cada observable clásico le corresponde un **operador hermítico** actuando sobre un espacio de Hilbert, y que los corchetes de Poisson se traducen en **conmutadores** según:

$$
\{f, g\} \longrightarrow \frac{1}{i\hbar} [\hat{f}, \hat{g}]
$$

donde $[\hat{A}, \hat{B}] = \hat{A}\hat{B} - \hat{B}\hat{A}$. Esta correspondencia no es un isomorfismo perfecto (hay obstruciones matemáticas conocidas como problemas de ordenamiento), pero sí un **homomorfismo** que preserva la estructura algebraica esencial.

La relación fundamental de cuantización se convierte entonces en:

$$
[\hat{x}_i, \hat{p}_j] = i\hbar \delta_{ij} \hat{I}
$$

Esta ecuación contiene la **esencia de la no conmutatividad** cuántica y es el origen del principio de incertidumbre. Matemáticamente, implica que los operadores de posición y momento no pueden ser representados simultáneamente como matrices diagonales en el mismo espacio de Hilbert, lo que lleva naturalmente a la necesidad de diferentes representaciones.

#### **3.2. Representación de Schrödinger**
La representación de Schrödinger es la formulación más intuitiva de la mecánica cuántica, donde la **dinámica temporal** reside completamente en los vectores de estado. El postulado fundamental establece que la evolución de un estado cuántico $|\psi(t)\rangle$ está gobernada por la **ecuación de Schrödinger dependiente del tiempo**:

$$
i\hbar \frac{d}{dt} |\psi(t)\rangle = \hat{H} |\psi(t)\rangle
$$

Aquí, $\hat{H}$ es el operador hamiltoniano, que corresponde a la energía total del sistema. Para un sistema conservativo, $\hat{H}$ no depende explícitamente del tiempo, y la ecuación admite soluciones por separación de variables.

La solución formal puede escribirse en términos del **operador de evolución temporal** $\hat{U}(t, t_0)$:

$$
|\psi(t)\rangle = \hat{U}(t, t_0) |\psi(t_0)\rangle
$$

Para un hamiltoniano independiente del tiempo, este operador toma la forma exponencial:

$$
\hat{U}(t, t_0) = e^{-i\hat{H}(t-t_0)/\hbar}
$$

La representación de Schrödinger es particularmente útil para problemas de valor inicial y para calcular probabilidades de transición entre estados.

#### **3.3. Operador Evolución y Representación de Heisenberg**
Mientras que en la imagen de Schrödinger los operadores son estáticos (salvo dependencia explícita) y los estados evolucionan, en la **imagen de Heisenberg** ocurre lo contrario: los estados son constantes en el tiempo y los operadores evolucionan.

La conexión entre ambas imágenes se realiza mediante el operador de evolución:

$$
\hat{A}_H(t) = \hat{U}^\dagger(t, t_0) \hat{A}_S \hat{U}(t, t_0)
$$

donde $\hat{A}_S$ es el operador en la imagen de Schrödinger. La dinámica de los operadores en la imagen de Heisenberg está gobernada por la **ecuación de Heisenberg**:

$$
\frac{d\hat{A}_H(t)}{dt} = \frac{1}{i\hbar} [\hat{A}_H(t), \hat{H}_H] + \left( \frac{\partial \hat{A}_S}{\partial t} \right)_H
$$

Esta ecuación es formalmente análoga a la ecuación clásica de movimiento en términos de corchetes de Poisson, manifestando claramente el **principio de correspondencia**.

La imagen de Heisenberg es especialmente útil para:
1. Estudiar sistemas con simetrías, ya que las ecuaciones de movimiento toman formas similares a las clásicas
2. Analizar problemas de teoría cuántica de campos
3. Conexión directa con la mecánica clásica a través del límite $\hbar \to 0$

#### **3.4. Representación de Estados en Base de Posición y Momento**
La dualidad onda-partícula encuentra su expresión matemática en la posibilidad de representar un mismo estado cuántico en diferentes bases. Consideremos un espacio de Hilbert genérico donde los operadores de posición $\hat{x}$ y momento $\hat{p}$ actúan.

En la **base de posición**, los autoestados $|x\rangle$ satisfacen:
$$
\hat{x} |x\rangle = x |x\rangle
$$
Estos estados forman un continuo y son ortogonales en el sentido distribucional:
$$
\langle x | x' \rangle = \delta(x - x')
$$
Un estado general $|\psi\rangle$ se representa mediante su **función de onda**:
$$
\psi(x) = \langle x | \psi \rangle
$$

En la **base de momento**, los autoestados $|p\rangle$ satisfacen:
$$
\hat{p} |p\rangle = p |p\rangle
$$
con ortogonalidad:
$$
\langle p | p' \rangle = \delta(p - p')
$$
La representación en esta base es:
$$
\phi(p) = \langle p | \psi \rangle
$$

La relación entre ambas bases está determinada por los elementos de matriz $\langle x | p \rangle$, que deben satisfacer:
$$
\langle x | \hat{p} | p \rangle = p \langle x | p \rangle = -i\hbar \frac{\partial}{\partial x} \langle x | p \rangle
$$
Esta ecuación diferencial tiene como solución:
$$
\langle x | p \rangle = \frac{1}{\sqrt{2\pi\hbar}} e^{ipx/\hbar}
$$

#### **3.5. Transformación de Fourier**
La relación entre las representaciones de posición y momento es precisamente una **transformada de Fourier**, que emerge naturalmente de la relación de conmutación canónica:

$$
\phi(p) = \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^{\infty} \psi(x) e^{-ipx/\hbar} dx
$$
$$
\psi(x) = \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^{\infty} \phi(p) e^{ipx/\hbar} dp
$$

Esta transformación tiene profundas implicaciones:
1. **Principio de incertidumbre**: Una función localizada en el espacio $x$ tiene una transformada de Fourier extendida en el espacio $p$, y viceversa
2. **Relación de completez**: Las bases de posición y momento satisfacen relaciones de completez:
   $$
   \int dx |x\rangle\langle x| = \hat{I}, \quad \int dp |p\rangle\langle p| = \hat{I}
   $$
3. **Unitaridad**: La transformada de Fourier es un operador unitario que conecta ambas representaciones

La transformada de Fourier es la herramienta matemática que implementa el cambio entre las descripciones en términos de posición y momento, encapsulando la naturaleza complementaria de estas variables en la teoría cuántica.

### **4. ECUACIONES DE MOVIMIENTO**

#### **4.1. Ecuación de Movimiento en Representación de Schrödinger**
La ecuación de Schrödinger dependiente del tiempo es la piedra angular de la dinámica cuántica en esta representación. Para una partícula en un potencial $V(\hat{x})$, el hamiltoniano es:

$$
\hat{H} = \frac{\hat{p}^2}{2m} + V(\hat{x})
$$

En la base de posición, esta ecuación toma la forma de una ecuación diferencial parcial:

$$
i\hbar \frac{\partial \psi(x,t)}{\partial t} = \left[ -\frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2} + V(x) \right] \psi(x,t)
$$

Esta es una ecuación de tipo **parabólico** que gobierna la evolución de la función de onda. Sus propiedades matemáticas clave incluyen:
1. **Linealidad**: Si $\psi_1$ y $\psi_2$ son soluciones, cualquier combinación lineal también lo es
2. **Unitaridad**: La norma $\int |\psi(x,t)|^2 dx$ se conserva en el tiempo
3. **Reversibilidad temporal**: Para potenciales reales, si $\psi(x,t)$ es solución, entonces $\psi^*(x,-t)$ también lo es

#### **4.2. Ecuación de Movimiento en Representación de Heisenberg**
En contraste, la imagen de Heisenberg enfatiza la evolución de los observables físicos. Para un operador $\hat{A}_H(t)$ sin dependencia explícita en el tiempo, la ecuación de movimiento es:

$$
\frac{d\hat{A}_H}{dt} = \frac{1}{i\hbar} [\hat{A}_H, \hat{H}_H]
$$

Esta ecuación es notable por varias razones:
1. **Analogía clásica**: Tiene la misma estructura que la ecuación de movimiento clásica en términos de corchetes de Poisson
2. **Constantes de movimiento**: Si $[\hat{A}, \hat{H}] = 0$, entonces $\hat{A}$ es una constante del movimiento
3. **Teorema de Ehrenfest**: Para los operadores de posición y momento:
   $$
   \frac{d\langle \hat{x} \rangle}{dt} = \frac{\langle \hat{p} \rangle}{m}, \quad \frac{d\langle \hat{p} \rangle}{dt} = -\langle \frac{\partial V}{\partial x} \rangle
   $$
   Estas ecuaciones son similares a las ecuaciones de Newton, pero con valores esperados

#### **4.3. Estados Estacionarios**
Los estados estacionarios son soluciones especiales de la ecuación de Schrödinger que tienen una dependencia temporal particularmente simple. Se obtienen mediante el método de separación de variables:

$$
\psi(x,t) = \phi(x) e^{-iEt/\hbar}
$$

Sustituyendo en la ecuación de Schrödinger dependiente del tiempo se obtiene la **ecuación de Schrödinger independiente del tiempo**:

$$
\hat{H} \phi(x) = E \phi(x)
$$

Esta es una **ecuación de autovalores** donde $E$ es la energía y $\phi(x)$ la autofunción correspondiente. Las propiedades importantes de los estados estacionarios son:
1. **Densidad de probabilidad independiente del tiempo**: $|\psi(x,t)|^2 = |\phi(x)|^2$
2. **Valores esperados independientes del tiempo**: Para operadores sin dependencia temporal explícita
3. **Base del espacio de Hilbert**: El conjunto de autofunciones forma una base completa (con posibles generalizaciones para espectro continuo)

La ecuación de autovalores energéticos es el problema central de la mecánica cuántica para sistemas conservativos.

#### **4.4. Partícula Libre**
La partícula libre es el sistema más simple en mecánica cuántica, con hamiltoniano $\hat{H} = \frac{\hat{p}^2}{2m}$. La ecuación de Schrödinger independiente del tiempo es:

$$
-\frac{\hbar^2}{2m} \frac{d^2 \phi(x)}{dx^2} = E \phi(x)
$$

Para $E > 0$, las soluciones son ondas planas:
$$
\phi_k(x) = \frac{1}{\sqrt{2\pi}} e^{ikx}, \quad E_k = \frac{\hbar^2 k^2}{2m}
$$

Estas funciones tienen varias peculiaridades:
1. **No normalizabilidad**: $\int_{-\infty}^{\infty} |\phi_k(x)|^2 dx = \infty$
2. **Ortogonalidad**: $\langle \phi_k | \phi_{k'} \rangle = \delta(k - k')$
3. **Completez**: Cualquier función de onda puede expandirse como superposición de ondas planas

Para $E < 0$, no hay soluciones físicamente aceptables (que no diverjan en el infinito). La solución general de la ecuación dependiente del tiempo es un paquete de ondas:

$$
\psi(x,t) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} \phi(k) e^{i(kx - \omega(k)t)} dk
$$
con $\omega(k) = \frac{\hbar k^2}{2m}$.

### **5. APLICACIONES EN UNA DIMENSIÓN**

#### **5.1. Oscilador Armónico Cuántico**
El oscilador armónico es quizás el sistema más importante en física cuántica debido a su solubilidad exacta y su ubicuidad como aproximación para sistemas cerca del equilibrio. El hamiltoniano es:

$$
\hat{H} = \frac{\hat{p}^2}{2m} + \frac{1}{2} m\omega^2 \hat{x}^2
$$

El espectro de energía se obtiene mediante el **método algebraico** introducido por Dirac, que define operadores de creación y aniquilación:

$$
\hat{a} = \sqrt{\frac{m\omega}{2\hbar}} \left( \hat{x} + \frac{i}{m\omega} \hat{p} \right), \quad \hat{a}^\dagger = \sqrt{\frac{m\omega}{2\hbar}} \left( \hat{x} - \frac{i}{m\omega} \hat{p} \right)
$$

Estos operadores satisfacen $[\hat{a}, \hat{a}^\dagger] = 1$, y el hamiltoniano se reescribe como:

$$
\hat{H} = \hbar\omega \left( \hat{a}^\dagger\hat{a} + \frac{1}{2} \right)
$$

Los autovalores de energía son:

$$
E_n = \hbar\omega \left( n + \frac{1}{2} \right), \quad n = 0, 1, 2, \ldots
$$

Las autofunciones en la base de posición son:

$$
\psi_n(x) = \left( \frac{m\omega}{\pi\hbar} \right)^{1/4} \frac{1}{\sqrt{2^n n!}} H_n\left( \sqrt{\frac{m\omega}{\hbar}} x \right) e^{-m\omega x^2/(2\hbar)}
$$

donde $H_n$ son los **polinomios de Hermite**. El estado fundamental $\psi_0(x)$ es una gaussiana con ancho $\Delta x = \sqrt{\hbar/(2m\omega)}$, que minimiza el producto de incertidumbres.

#### **5.2. Ecuación de Conservación de Probabilidad**
La interpretación probabilística de la función de onda exige que la probabilidad total se conserve. Esto se manifiesta en la **ecuación de continuidad** para la densidad de probabilidad $\rho(x,t) = |\psi(x,t)|^2$:

$$
\frac{\partial \rho}{\partial t} + \frac{\partial j}{\partial x} = 0
$$

donde $j(x,t)$ es la **densidad de corriente de probabilidad**:

$$
j(x,t) = \frac{\hbar}{2mi} \left( \psi^* \frac{\partial \psi}{\partial x} - \psi \frac{\partial \psi^*}{\partial x} \right)
$$

Esta ecuación asegura que:
$$
\frac{d}{dt} \int_{-\infty}^{\infty} |\psi(x,t)|^2 dx = 0
$$

Para estados estacionarios, $\frac{\partial \rho}{\partial t} = 0$, lo que implica $\frac{\partial j}{\partial x} = 0$, es decir, la corriente es constante en el espacio.

#### **5.3. Relaciones de Incertidumbre**
Las relaciones de incertidumbre son una consecuencia directa de la no conmutatividad de operadores. Para dos operadores cualesquiera $\hat{A}$ y $\hat{B}$, se cumple:

$$
\Delta A \Delta B \geq \frac{1}{2} |\langle [\hat{A}, \hat{B}] \rangle|
$$

Para posición y momento, con $[\hat{x}, \hat{p}] = i\hbar$, se obtiene la famosa relación:

$$
\Delta x \Delta p \geq \frac{\hbar}{2}
$$

La demostración utiliza la **desigualdad de Cauchy-Schwarz** en el espacio de Hilbert. El estado que satura esta desigualdad (mínima incertidumbre) es el estado fundamental del oscilador armónico, o más generalmente, los **estados coherentes**.

Existen otras relaciones de incertidumbre importantes, como la relación energía-tiempo, aunque su interpretación es más sutil ya que el tiempo no es un operador en mecánica cuántica no relativista.

#### **5.4-5.7. Problemas de Potenciales Unidimensionales**

**Potencial Escalón**: Consideremos un potencial $V(x) = V_0 \Theta(x)$ (escalón en $x=0$). Para una partícula incidente desde la izquierda con energía $E > V_0$:

- Región I ($x<0$): $\psi_I(x) = e^{ik_1x} + R e^{-ik_1x}$, con $k_1 = \sqrt{2mE}/\hbar$
- Región II ($x>0$): $\psi_{II}(x) = T e^{ik_2x}$, con $k_2 = \sqrt{2m(E-V_0)}/\hbar$

Las condiciones de empalme (continuidad de $\psi$ y $\psi'$ en $x=0$) determinan:
$$
R = \frac{k_1 - k_2}{k_1 + k_2}, \quad T = \frac{2k_1}{k_1 + k_2}
$$

Los coeficientes de reflexión y transmisión son:
$$
\mathcal{R} = |R|^2 = \left( \frac{k_1 - k_2}{k_1 + k_2} \right)^2, \quad \mathcal{T} = \frac{k_2}{k_1} |T|^2 = \frac{4k_1k_2}{(k_1+k_2)^2}
$$

Para $E < V_0$, $k_2$ se vuelve imaginario, y en la región II la función de onda decae exponencialmente. Aún hay probabilidad no nula de encontrar la partícula en $x>0$, pero no hay transmisión a infinito.

**Pozo de Potencial Finito**: Un pozo rectangular de ancho $a$ y profundidad $V_0$ admite un número finito de estados ligados. Las autofunciones son sinusoidales dentro del pozo y exponenciales decrecientes fuera. Las energías permitidas se determinan por condiciones de continuidad que conducen a ecuaciones trascendentes.

Para un pozo simétrico, las soluciones se clasifican en pares e impares. El número de estados ligados es aproximadamente $N \approx \frac{a}{\pi\hbar} \sqrt{2mV_0}$.

**Efecto Túnel**: Cuando una partícula encuentra una barrera de potencial con $E < V_{\text{max}}$, existe probabilidad no nula de atravesarla. Para una barrera rectangular de ancho $L$ y altura $V_0$, el coeficiente de transmisión es aproximadamente:
$$
T \approx \frac{16E(V_0-E)}{V_0^2} e^{-2\kappa L}, \quad \kappa = \sqrt{2m(V_0-E)}/\hbar
$$

Este efecto es crucial en fenómenos como la desintegración alfa, la microscopía de efecto túnel (STM), y diodos túnel.

#### **5.8-5.9. Condiciones de Simetría y Resonancia**

Las **simetrías** del potencial imponen restricciones sobre las funciones de onda. Para un potencial simétrico $V(-x) = V(x)$, el hamiltoniano conmuta con el operador de paridad $\hat{P}\psi(x) = \psi(-x)$. Esto implica que las autofunciones pueden clasificarse como pares o impares.

La **resonancia** en mecánica cuántica ocurre cuando la transmisión a través de una barrera es máxima ($T \approx 1$). Esto sucede cuando se cumplen condiciones similares a las de interferencia constructiva. Para una barrera doble (pozo entre dos barreras), las resonancias ocurren cerca de las energías de los estados cuasi-ligados del pozo.

### **6. CANTIDAD DE MOVIMIENTO ANGULAR**

#### **6.1. Relaciones de Conmutación**
El momento angular en mecánica cuántica se define análogamente al clásico: $\hat{\mathbf{L}} = \hat{\mathbf{r}} \times \hat{\mathbf{p}}$. En componentes:
$$
\hat{L}_x = \hat{y}\hat{p}_z - \hat{z}\hat{p}_y, \quad \hat{L}_y = \hat{z}\hat{p}_x - \hat{x}\hat{p}_z, \quad \hat{L}_z = \hat{x}\hat{p}_y - \hat{y}\hat{p}_x
$$

Las relaciones de conmutación fundamentales son:
$$
[\hat{L}_i, \hat{L}_j] = i\hbar \epsilon_{ijk} \hat{L}_k
$$
Estas relaciones definen el **álgebra de Lie de SO(3)**, el grupo de rotaciones en tres dimensiones.

Además, cada componente conmuta con el cuadrado del momento angular:
$$
[\hat{L}^2, \hat{L}_i] = 0
$$

#### **6.2. Valores y Vectores Propios**
Dado que $\hat{L}^2$ y una componente (típicamente $\hat{L}_z$) conmutan, pueden diagonalizarse simultáneamente. Los autovalores son:
$$
\hat{L}^2 |l,m\rangle = \hbar^2 l(l+1) |l,m\rangle, \quad l = 0, 1/2, 1, 3/2, \ldots
$$
$$
\hat{L}_z |l,m\rangle = \hbar m |l,m\rangle, \quad m = -l, -l+1, \ldots, l-1, l
$$

Para momento angular orbital (no spin), $l$ toma solo valores enteros: $l = 0, 1, 2, \ldots$.

Los operadores de escalera $\hat{L}_\pm = \hat{L}_x \pm i\hat{L}_y$ permiten conectar estados con diferente $m$:
$$
\hat{L}_\pm |l,m\rangle = \hbar \sqrt{l(l+1) - m(m\pm 1)} |l,m\pm 1\rangle
$$

#### **6.3. Coordenadas Polares y Momento Angular Orbital**
En coordenadas esféricas $(r, \theta, \phi)$, el operador $\hat{L}_z$ toma una forma simple:
$$
\hat{L}_z = -i\hbar \frac{\partial}{\partial \phi}
$$

Las autofunciones de $\hat{L}_z$ son $e^{im\phi}$, con $m$ entero para que sean univaluadas.

El operador $\hat{L}^2$ en coordenadas esféricas es:
$$
\hat{L}^2 = -\hbar^2 \left[ \frac{1}{\sin\theta} \frac{\partial}{\partial\theta} \left( \sin\theta \frac{\partial}{\partial\theta} \right) + \frac{1}{\sin^2\theta} \frac{\partial^2}{\partial\phi^2} \right]
$$

Las autofunciones simultáneas de $\hat{L}^2$ y $\hat{L}_z$ son los **armónicos esféricos** $Y_{lm}(\theta,\phi)$, que forman una base completa en la esfera unidad.

### **7. SPIN**

#### **7.1. Origen Experimental del Spin**
El concepto de spin surgió de evidencias experimentales que no podían explicarse con momento angular orbital:

1. **Estructura fina** de líneas espectrales atómicas
2. **Experimento de Stern-Gerlach** (1922): Un haz de átomos de plata se divide en dos al pasar por un gradiente de campo magnético, sugiriendo un momento magnético con dos orientaciones posibles
3. **Efecto Zeeman anómalo**: Desdoblamiento de líneas espectrales en campos magnéticos que no concordaba con la predicción clásica

Estos fenómenos llevaron a postular un **momento angular intrínseco** de las partículas, adicional al orbital.

#### **7.2-7.4. Formulación del Spin 1/2**
El spin es un momento angular que no deriva del movimiento espacial. Para partículas de spin 1/2 (como electrones), el espacio de estados es bidimensional (espinores).

Los operadores de spin se definen como $\hat{S}_i = \frac{\hbar}{2} \hat{\sigma}_i$, donde $\hat{\sigma}_i$ son las **matrices de Pauli**:

$$
\sigma_x = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \quad
\sigma_y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \quad
\sigma_z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}
$$

Estas matrices satisfacen:
$$
[\sigma_i, \sigma_j] = 2i\epsilon_{ijk}\sigma_k, \quad \{\sigma_i, \sigma_j\} = 2\delta_{ij}I, \quad \sigma_i^2 = I
$$

Un estado general de spin se representa como un espinor:
$$
|\chi\rangle = \begin{pmatrix} a \\ b \end{pmatrix} = a|\uparrow\rangle + b|\downarrow\rangle, \quad |a|^2 + |b|^2 = 1
$$

Los autoestados de $\hat{S}_z$ son:
$$
|\uparrow\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \quad |\downarrow\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}
$$

#### **7.5. Momento Magnético**
El momento magnético asociado al momento angular es:
$$
\hat{\boldsymbol{\mu}} = g \frac{q}{2m} \hat{\mathbf{S}}
$$

Para el electrón, $q = -e$, y el factor $g \approx 2$ (corregido a 2.0023 por QED). La interacción con un campo magnético es:
$$
\hat{H}_{\text{Zeeman}} = -\hat{\boldsymbol{\mu}} \cdot \mathbf{B}
$$

### **8. PARTÍCULA EN POTENCIAL CENTRAL Y ÁTOMO DE HIDRÓGENO**

#### **8.1. Separación en Coordenadas Esféricas**
Para un potencial central $V(r)$, el hamiltoniano conmuta con $\hat{L}^2$ y $\hat{L}_z$. Esto permite separar variables:
$$
\psi(r,\theta,\phi) = R(r) Y_{lm}(\theta,\phi)
$$

La parte radial satisface la **ecuación radial**:
$$
-\frac{\hbar^2}{2m} \frac{1}{r^2} \frac{d}{dr} \left( r^2 \frac{dR}{dr} \right) + \left[ V(r) + \frac{\hbar^2 l(l+1)}{2mr^2} \right] R = E R
$$

El término $\frac{\hbar^2 l(l+1)}{2mr^2}$ es el **potencial centrífugo**, que actúa como una barrera repulsiva.

#### **8.2. Potencial de Coulomb y Átomo de Hidrógeno**
Para el potencial de Coulomb $V(r) = -\frac{e^2}{4\pi\epsilon_0 r}$, la ecuación radial se resuelve introduciendo variables adimensionales. Las energías son:
$$
E_n = -\frac{me^4}{2(4\pi\epsilon_0)^2\hbar^2} \frac{1}{n^2} = -\frac{13.6 \text{eV}}{n^2}
$$

donde $n = 1, 2, 3, \ldots$ es el **número cuántico principal**.

Las funciones de onda radiales son:
$$
R_{nl}(r) = \sqrt{\left( \frac{2}{na_0} \right)^3 \frac{(n-l-1)!}{2n[(n+l)!]^3}} e^{-r/(na_0)} \left( \frac{2r}{na_0} \right)^l L_{n-l-1}^{2l+1}\left( \frac{2r}{na_0} \right)
$$

donde $a_0 = \frac{4\pi\epsilon_0\hbar^2}{me^2} \approx 0.529 \text{Å}$ es el **radio de Bohr**, y $L_{p}^{k}$ son los **polinomios de Laguerre asociados**.

La degeneración del nivel $n$ es $\sum_{l=0}^{n-1} (2l+1) = n^2$.

#### **8.3. Problema de Dos Cuerpos**
Para dos partículas interactuantes, se separa el movimiento del centro de masa y el movimiento relativo. Definimos:
$$
\mathbf{R} = \frac{m_1\mathbf{r}_1 + m_2\mathbf{r}_2}{m_1+m_2}, \quad \mathbf{r} = \mathbf{r}_1 - \mathbf{r}_2
$$

El hamiltoniano se separa como:
$$
\hat{H} = -\frac{\hbar^2}{2M} \nabla_R^2 - \frac{\hbar^2}{2\mu} \nabla_r^2 + V(r)
$$

donde $M = m_1+m_2$ y $\mu = \frac{m_1m_2}{m_1+m_2}$ es la **masa reducida**. El movimiento relativo es idéntico al de una partícula de masa $\mu$ en el potencial $V(r)$.

### **9. MOVIMIENTO EN CAMPO ELECTROMAGNÉTICO**

#### **9.1. Hamiltoniano con Campos EM**
El acoplamiento mínimo prescribe reemplazar $\hat{\mathbf{p}} \rightarrow \hat{\mathbf{p}} - q\mathbf{A}(\hat{\mathbf{r}}, t)$ y añadir $q\Phi(\hat{\mathbf{r}}, t)$:
$$
\hat{H} = \frac{1}{2m} [\hat{\mathbf{p}} - q\mathbf{A}(\hat{\mathbf{r}}, t)]^2 + q\Phi(\hat{\mathbf{r}}, t)
$$

Este hamiltoniano es invariante bajo transformaciones de gauge:
$$
\mathbf{A} \rightarrow \mathbf{A} + \nabla\chi, \quad \Phi \rightarrow \Phi - \frac{\partial\chi}{\partial t}, \quad \psi \rightarrow e^{iq\chi/\hbar} \psi
$$

#### **9.2-9.3. Campo Magnético Constante y Efecto Zeeman**
Para un campo magnético uniforme $\mathbf{B} = B\hat{z}$, en el gauge de Landau $\mathbf{A} = \frac{B}{2}(-y, x, 0)$, el hamiltoniano se separa en movimiento en el plano xy (oscilador armónico con frecuencia $\omega_c = \frac{qB}{m}$, frecuencia ciclotrón) y movimiento libre en z.

El **efecto Zeeman** describe el desdoblamiento de niveles atómicos en campo magnético. Para el átomo de hidrógeno:
$$
\hat{H}_{\text{Zeeman}} = \frac{eB}{2m} (\hat{L}_z + 2\hat{S}_z)
$$

El factor 2 frente a $\hat{S}_z$ es el factor g del electrón.

#### **9.5. Efecto Aharonov-Bohm**
Este efecto puramente cuántico muestra que el potencial vector $\mathbf{A}$ tiene realidad física incluso donde $\mathbf{B} = 0$. Una partícula que viaja alrededor de un solenoide (campo confinado, $\mathbf{A} \neq 0$ fuera) adquiere una fase adicional:
$$
\Delta\phi = \frac{q}{\hbar} \oint \mathbf{A} \cdot d\mathbf{l} = \frac{q}{\hbar} \Phi_B
$$

donde $\Phi_B$ es el flujo magnético encerrado. Esto produce interferencia observable.

---

## **MECÁNICA CUÁNTICA 2: MÉTODOS AVANZADOS Y APLICACIONES**

### **1. MÉTODOS DE APROXIMACIÓN PARA ESTADOS ESTACIONARIOS**

#### **1.1. Teoría de Perturbaciones Estacionaria**
Cuando el hamiltoniano puede escribirse como $\hat{H} = \hat{H}_0 + \lambda \hat{V}$, donde $\hat{H}_0$ es soluble y $\hat{V}$ es pequeño, podemos desarrollar correcciones a los autoestados y autovalores.

**Caso no degenerado**: Para un nivel $|n^{(0)}\rangle$ de $\hat{H}_0$ con energía $E_n^{(0)}$:
- Corrección a primer orden:
  $$
  E_n^{(1)} = \langle n^{(0)} | \hat{V} | n^{(0)} \rangle
  $$
  $$
  |n^{(1)}\rangle = \sum_{m \neq n} \frac{\langle m^{(0)} | \hat{V} | n^{(0)} \rangle}{E_n^{(0)} - E_m^{(0)}} |m^{(0)}\rangle
  $$
- Corrección a segundo orden en energía:
  $$
  E_n^{(2)} = \sum_{m \neq n} \frac{|\langle m^{(0)} | \hat{V} | n^{(0)} \rangle|^2}{E_n^{(0)} - E_m^{(0)}}
  $$

**Caso degenerado**: Si el nivel $E_n^{(0)}$ tiene degeneración $g$, primero debemos diagonalizar $\hat{V}$ en el subespacio degenerado. Sea $\{|\alpha\rangle\}$ la base que diagonaliza $\hat{P}_n \hat{V} \hat{P}_n$, donde $\hat{P}_n$ es el proyector al subespacio degenerado. Las correcciones a primer orden son los autovalores de esta matriz.

#### **1.2. Principio Variacional**
Para el estado fundamental, cualquier estado de prueba $|\psi_{\text{trial}}\rangle$ da una cota superior:
$$
E_0 \leq \frac{\langle \psi_{\text{trial}} | \hat{H} | \psi_{\text{trial}} \rangle}{\langle \psi_{\text{trial}} | \psi_{\text{trial}} \rangle}
$$

Minimizando esta expresión respecto a parámetros variacionales se obtiene una aproximación a $E_0$ y $|\psi_0\rangle$. Para estados excitados, se usa el método de Ritz restringiendo el estado de prueba a ser ortogonal a los estados más bajos.

#### **1.3. Método WKB (Wentzel-Kramers-Brillouin)**
Aproximación semiclásica válida cuando la longitud de onda de de Broglie varía lentamente. Las soluciones aproximadas son:

- Región clásicamente permitida ($E > V(x)$):
  $$
  \psi(x) \approx \frac{C_1}{\sqrt{p(x)}} e^{\frac{i}{\hbar} \int p(x) dx} + \frac{C_2}{\sqrt{p(x)}} e^{-\frac{i}{\hbar} \int p(x) dx}
  $$
  con $p(x) = \sqrt{2m[E - V(x)]}$

- Región clásicamente prohibida ($E < V(x)$):
  $$
  \psi(x) \approx \frac{D_1}{\sqrt{|p(x)|}} e^{\frac{1}{\hbar} \int |p(x)| dx} + \frac{D_2}{\sqrt{|p(x)|}} e^{-\frac{1}{\hbar} \int |p(x)| dx}
  $$

Las condiciones de conexión en puntos de retorno dan las **reglas de cuantización de Bohr-Sommerfeld**:
$$
\oint p(x) dx = \left( n + \frac{1}{2} \right) 2\pi\hbar, \quad n = 0, 1, 2, \ldots
$$

#### **1.4. Método de Brillouin-Wigner**
Alternativa a la teoría de perturbaciones de Rayleigh-Schrödinger. La serie de Brillouin-Wigner para la energía es:
$$
E_n = E_n^{(0)} + \langle n^{(0)} | \hat{V} | n^{(0)} \rangle + \sum_{m \neq n} \frac{|\langle m^{(0)} | \hat{V} | n^{(0)} \rangle|^2}{E_n - E_m^{(0)}} + \cdots
$$

A diferencia de la serie de Rayleigh-Schrödinger, aquí la energía exacta $E_n$ aparece en el denominador, dando una serie que converge más rápido pero que debe resolverse autoconsistentemente.

### **2. CORRECCIONES A LA ESTRUCTURA ATÓMICA**

#### **2.1. Correcciones Relativistas**
A velocidades comparables a $c$, la energía cinética relativista es:
$$
T = \sqrt{p^2c^2 + m^2c^4} - mc^2 \approx \frac{p^2}{2m} - \frac{p^4}{8m^3c^2} + \cdots
$$

El término $-\frac{p^4}{8m^3c^2}$ da una corrección a la energía:
$$
\Delta E_{\text{rel}} = -\frac{1}{8m^3c^2} \langle \hat{p}^4 \rangle = -\frac{1}{2mc^2} \left( E_n^2 - 2E_n\langle V \rangle + \langle V^2 \rangle \right)
$$

Para el átomo de hidrógeno:
$$
\Delta E_{\text{rel}} = -\frac{E_n^2}{2mc^2} \left( \frac{4n}{l+1/2} - 3 \right)
$$

#### **2.2. Acoplamiento Spin-Órbita**
Un electrón que se mueve en el campo eléctrico del núcleo ve en su sistema de referencia un campo magnético:
$$
\mathbf{B} = -\frac{\mathbf{v} \times \mathbf{E}}{c^2} = \frac{1}{2m^2c^2} \frac{1}{r} \frac{dV}{dr} \mathbf{L}
$$

La interacción con el spin del electrón es:
$$
\hat{H}_{\text{SO}} = -\hat{\boldsymbol{\mu}}_s \cdot \mathbf{B} = \frac{1}{2m^2c^2} \frac{1}{r} \frac{dV}{dr} \hat{\mathbf{L}} \cdot \hat{\mathbf{S}}
$$

Para el potencial de Coulomb $V(r) = -\frac{e^2}{4\pi\epsilon_0 r}$:
$$
\hat{H}_{\text{SO}} = \frac{e^2}{8\pi\epsilon_0 m^2c^2} \frac{\hat{\mathbf{L}} \cdot \hat{\mathbf{S}}}{r^3}
$$

La corrección a la energía es:
$$
\Delta E_{\text{SO}} = \frac{\hbar^2}{2} \frac{e^2}{8\pi\epsilon_0 m^2c^2} \frac{j(j+1) - l(l+1) - s(s+1)}{a_0^3 n^3 l(l+1/2)(l+1)}
$$

#### **2.3-2.4. Corrimiento Lamb y Estructura Hiperfina**
El **corrimiento Lamb** es un desplazamiento entre niveles $2s_{1/2}$ y $2p_{1/2}$ que deberían ser degenerados según Dirac. Surge de efectos de electrodinámica cuántica (QED), principalmente la interacción con fluctuaciones del vacío.

La **estructura hiperfina** proviene de la interacción del momento magnético del electrón con el campo magnético del núcleo. Para el estado fundamental del hidrógeno:
$$
\hat{H}_{\text{hf}} = \frac{8\pi}{3} \mu_0 \gamma_e \gamma_p \hat{\mathbf{S}}_e \cdot \hat{\mathbf{S}}_p \delta(\mathbf{r}) + \frac{\mu_0}{4\pi} \gamma_e \gamma_p \frac{3(\hat{\mathbf{S}}_e \cdot \hat{\mathbf{r}})(\hat{\mathbf{S}}_p \cdot \hat{\mathbf{r}}) - \hat{\mathbf{S}}_e \cdot \hat{\mathbf{S}}_p}{r^3}
$$

La corrección energética para el estado fundamental es:
$$
\Delta E_{\text{hf}} = \frac{\mu_0}{4\pi} \frac{4}{3} \gamma_e \gamma_p |\psi(0)|^2 \langle \hat{\mathbf{S}}_e \cdot \hat{\mathbf{S}}_p \rangle
$$

Para el hidrógeno, esto da la famosa línea de 21 cm.

#### **2.5-2.6. Efectos Stark y Zeeman**
- **Efecto Stark**: Desplazamiento de niveles en campo eléctrico. Para el átomo de hidrógeno en campo débil, el efecto es cuadrático para la mayoría de los niveles y lineal solo para niveles degenerados.
- **Efecto Zeeman**: Desdoblamiento en campo magnético. Distinguimos:
  - **Zeeman normal**: Cuando el acoplamiento spin-órbita es débil frente a la interacción con B
  - **Zeeman anómalo**: Cuando debemos considerar el acoplamiento spin-órbita

### **3. FENÓMENOS DEPENDIENTES DEL TIEMPO**

#### **3.1-3.2. Perturbaciones Dependientes del Tiempo**
Para $\hat{H}(t) = \hat{H}_0 + \hat{V}(t)$, desarrollamos el estado en la base de $\hat{H}_0$:
$$
|\psi(t)\rangle = \sum_n c_n(t) e^{-iE_n^{(0)}t/\hbar} |n^{(0)}\rangle
$$

Los coeficientes satisfacen:
$$
i\hbar \frac{dc_f}{dt} = \sum_n V_{fn}(t) e^{i\omega_{fn}t} c_n(t)
$$
con $\omega_{fn} = (E_f^{(0)} - E_n^{(0)})/\hbar$ y $V_{fn}(t) = \langle f^{(0)} | \hat{V}(t) | n^{(0)} \rangle$.

Para una perturbación armónica $\hat{V}(t) = \hat{W} e^{-i\omega t} + \hat{W}^\dagger e^{i\omega t}$ y sistema inicialmente en $|i^{(0)}\rangle$, la probabilidad de transición a primer orden es:
$$
P_{i\to f}(t) = \frac{4|W_{fi}|^2}{\hbar^2} \frac{\sin^2[(\omega_{fi}-\omega)t/2]}{(\omega_{fi}-\omega)^2}
$$

Para un continuo de estados finales con densidad $\rho(E_f)$, la **regla de oro de Fermi** da la tasa de transición:
$$
\Gamma_{i\to f} = \frac{2\pi}{\hbar} |V_{fi}|^2 \rho(E_f)
$$

#### **3.3. Interacción con Campos de Radiación**
La interacción de un átomo con el campo electromagnético se describe por:
$$
\hat{V} = -\frac{e}{m} \mathbf{A} \cdot \hat{\mathbf{p}} + \frac{e^2}{2m} A^2
$$

En la aproximación dipolar eléctrica, para una onda plana $\mathbf{A} = \mathbf{A}_0 e^{i(\mathbf{k}\cdot\mathbf{r}-\omega t)} + c.c.$, y en el gauge de Coulomb, se tiene:
$$
\hat{V} \approx -e\mathbf{r} \cdot \mathbf{E}(t) = e\mathbf{r} \cdot \mathbf{E}_0 \cos(\omega t)
$$

Las probabilidades de absorción y emisión estimulada son proporcionales a $|\langle f | \hat{\mathbf{r}} | i \rangle|^2$.

### **4. TEORÍA DE DISPERSIÓN**

#### **4.1-4.2. Fundamentos de Dispersión**
Consideramos una partícula incidente dispersada por un potencial $V(\mathbf{r})$. La función de onda asintótica es:
$$
\psi(\mathbf{r}) \overset{r\to\infty}{\sim} e^{ikz} + f(\theta,\phi) \frac{e^{ikr}}{r}
$$

La **sección eficaz diferencial** es:
$$
\frac{d\sigma}{d\Omega} = |f(\theta,\phi)|^2
$$

La amplitud de dispersión puede escribirse como:
$$
f(\theta,\phi) = -\frac{m}{2\pi\hbar^2} \int e^{-i\mathbf{k}'\cdot\mathbf{r}'} V(\mathbf{r}') \psi(\mathbf{r}') d^3r'
$$

#### **4.3. Método de Ondas Parciales**
Expandimos la onda plana incidente y la onda dispersada en ondas esféricas:
$$
e^{ikz} = \sum_{l=0}^\infty i^l (2l+1) j_l(kr) P_l(\cos\theta)
$$

Para un potencial central, la función de onda tiene simetría azimutal y se expande como:
$$
\psi(r,\theta) = \sum_{l=0}^\infty \frac{u_l(r)}{r} P_l(\cos\theta)
$$

Cada onda parcial satisface la ecuación radial:
$$
\frac{d^2 u_l}{dr^2} + \left[ k^2 - \frac{2m}{\hbar^2} V(r) - \frac{l(l+1)}{r^2} \right] u_l = 0
$$

La solución asintótica es:
$$
u_l(r) \overset{r\to\infty}{\sim} \sin\left( kr - \frac{l\pi}{2} + \delta_l \right)
$$

donde $\delta_l$ es el **desplazamiento de fase** para la onda parcial $l$.

La amplitud de dispersión se expresa en términos de los desplazamientos de fase:
$$
f(\theta) = \frac{1}{k} \sum_{l=0}^\infty (2l+1) e^{i\delta_l} \sin\delta_l P_l(\cos\theta)
$$

#### **4.4-4.8. Resultados Importantes**
- **Teorema óptico**: Relaciona la sección eficaz total con la parte imaginaria de la amplitud de dispersión hacia adelante:
  $$
  \sigma_{\text{total}} = \frac{4\pi}{k} \text{Im} f(0)
  $$
- **Dispersión resonante**: Ocurre cuando $\delta_l$ pasa rápidamente por $\pi/2$. La sección eficaz parcial tiene forma de Breit-Wigner:
  $$
  \sigma_l(E) = \frac{4\pi}{k^2} \frac{(2l+1)\Gamma^2/4}{(E-E_0)^2 + \Gamma^2/4}
  $$
- **Aproximación de Born**: Para potenciales débiles, a primer orden:
  $$
  f^{(1)}(\theta) = -\frac{m}{2\pi\hbar^2} \int e^{-i\mathbf{q}\cdot\mathbf{r}} V(\mathbf{r}) d^3r
  $$
  con $\mathbf{q} = \mathbf{k} - \mathbf{k}'$, $|\mathbf{q}| = 2k\sin(\theta/2)$.

### **5. SEGUNDA CUANTIZACIÓN**

#### **5.1-5.4. Partículas Idénticas**
El principio de indistinguibilidad de partículas idénticas requiere que los estados sean simétricos (bosones) o antisimétricos (fermiones) bajo intercambio.

Para un sistema de $N$ partículas idénticas, el espacio de Hilbert apropiado es el producto tensorial simetrizado o antisimetrizado.

**Fermiones**: Estados antisimétricos. Para dos fermiones:
$$
\Psi(\mathbf{r}_1, \mathbf{r}_2) = \frac{1}{\sqrt{2}} [\psi_a(\mathbf{r}_1)\psi_b(\mathbf{r}_2) - \psi_a(\mathbf{r}_2)\psi_b(\mathbf{r}_1)]
$$

**Bosones**: Estados simétricos. Para dos bosones:
$$
\Psi(\mathbf{r}_1, \mathbf{r}_2) = \frac{1}{\sqrt{2}} [\psi_a(\mathbf{r}_1)\psi_b(\mathbf{r}_2) + \psi_a(\mathbf{r}_2)\psi_b(\mathbf{r}_1)]
$$

#### **5.5-5.7. Espacio de Fock y Operadores de Campo**
El **espacio de Fock** es la suma directa de espacios con diferente número de partículas:
$$
\mathcal{F} = \mathcal{H}_0 \oplus \mathcal{H}_1 \oplus \mathcal{H}_2 \oplus \cdots
$$

Se definen operadores de creación $\hat{a}_\alpha^\dagger$ y aniquilación $\hat{a}_\alpha$ que satisfacen:

- Para **bosones**:
  $$
  [\hat{a}_\alpha, \hat{a}_\beta^\dagger] = \delta_{\alpha\beta}, \quad [\hat{a}_\alpha, \hat{a}_\beta] = [\hat{a}_\alpha^\dagger, \hat{a}_\beta^\dagger] = 0
  $$
- Para **fermiones**:
  $$
  \{\hat{a}_\alpha, \hat{a}_\beta^\dagger\} = \delta_{\alpha\beta}, \quad \{\hat{a}_\alpha, \hat{a}_\beta\} = \{\hat{a}_\alpha^\dagger, \hat{a}_\beta^\dagger\} = 0
  $$

El **operador de campo** se define como:
$$
\hat{\psi}(\mathbf{r}) = \sum_\alpha \phi_\alpha(\mathbf{r}) \hat{a}_\alpha
$$
donde $\{\phi_\alpha\}$ es una base completa del espacio de una partícula.

### **6. FERMIONES DE SPIN 1/2**

#### **6.1. Gas de Fermi Libre**
Para fermiones libres (gas de electrones), los estados se llenan según el principio de exclusión. A $T=0$, todos los estados con $k \leq k_F$ están ocupados, donde $k_F$ es el **momento de Fermi**:
$$
k_F = (3\pi^2 n)^{1/3}
$$

La **energía de Fermi** es:
$$
E_F = \frac{\hbar^2 k_F^2}{2m}
$$

La superficie en el espacio de momentos que separa estados ocupados y vacíos es la **superficie de Fermi**. Para el gas libre, es una esfera de radio $k_F$.

#### **6.2-6.4. Propiedades del Gas de Fermi**
La **función de correlación** para el gas de Fermi libre es:
$$
g(\mathbf{r}) = 1 - \frac{9}{(k_F r)^4} [\sin(k_F r) - k_F r \cos(k_F r)]^2
$$

La **energía del estado fundamental** por partícula es:
$$
\frac{E_0}{N} = \frac{3}{5} E_F
$$

La **presión de degeneración** es:
$$
P = \frac{2}{5} n E_F = \frac{\hbar^2}{5m} (3\pi^2)^{2/3} n^{5/3}
$$

### **7. BOSONES**

#### **7.1-7.3. Gas de Bose-Einstein**
Para bosones libres, a temperatura suficientemente baja ocurre la **condensación de Bose-Einstein**. La temperatura crítica es:
$$
T_c = \frac{2\pi\hbar^2}{m k_B} \left( \frac{n}{\zeta(3/2)} \right)^{2/3}
$$
donde $\zeta(3/2) \approx 2.612$.

Para $T < T_c$, una fracción macroscópica de partículas ocupa el estado fundamental ($k=0$):
$$
\frac{N_0}{N} = 1 - \left( \frac{T}{T_c} \right)^{3/2}
$$

Las excitaciones elementales son **fonones** con relación de dispersión lineal $\omega(k) = ck$.

### **8. APLICACIONES**

#### **8.1. Átomos Multielectrónicos**
La aproximación de campo central supone que cada electrón se mueve en un potencial efectivo esféricamente simétrico. La función de onda se aproxima por un **determinante de Slater** de orbitales atómicos.

El **principio de exclusión de Pauli** explica la estructura de la tabla periódica. La energía de los orbitales aumenta con $n$ y $l$, y el orden de llenado sigue la **regla de Madelung** (orden por $n+l$, y para igual $n+l$ por $n$).

La energía de intercambio da lugar a la **estructura multiplete** de niveles atómicos (reglas de Hund).

### **9. ECUACIONES DE ONDA RELATIVISTAS**

#### **9.1. Ecuación de Klein-Gordon**
Para partículas escalares sin spin (spin 0). Se obtiene de la relación energía-momento relativista $E^2 = p^2c^2 + m^2c^4$:
$$
\left( \frac{1}{c^2} \frac{\partial^2}{\partial t^2} - \nabla^2 + \frac{m^2c^2}{\hbar^2} \right) \psi(\mathbf{r},t) = 0
$$

Problemas: Densidad de probabilidad no definida positiva, soluciones de energía negativa.

#### **9.2. Ecuación de Dirac**
Para fermiones de spin 1/2. Se linealiza la relación energía-momento:
$$
(i\hbar\gamma^\mu \partial_\mu - mc) \psi = 0
$$

donde $\gamma^\mu$ son las **matrices de Dirac**, que satisfacen $\{\gamma^\mu, \gamma^\nu\} = 2g^{\mu\nu}$.

La ecuación de Dirac predice:
1. La existencia de **antipartículas** (soluciones de energía negativa interpretadas como partículas de carga opuesta)
2. El **spin 1/2** intrínseco de las partículas
3. El **momento magnético anómalo** del electrón (corregido por QED)
4. La **estructura fina** del átomo de hidrógeno

Para el átomo de hidrógeno, la ecuación de Dirac da niveles de energía:
$$
E_{nj} = mc^2 \left[ 1 + \left( \frac{\alpha}{n - (j+1/2) + \sqrt{(j+1/2)^2 - \alpha^2}} \right)^2 \right]^{-1/2}
$$
donde $\alpha \approx 1/137$ es la constante de estructura fina.

---
---
# **EXPANSIÓN DETALLADA DE TEMAS AVANZADOS DE MECÁNICA CUÁNTICA 2**

## **6. FERMIONES DE SPIN 1/2: TEORÍA DETALLADA**

### **6.1. Sistema de Fermiones Libres: La Esfera de Fermi y Propiedades Fundamentales**

#### **6.1.1. Formulación del Problema de N Fermiones Libres**
Consideremos un gas de $N$ fermiones idénticos de spin 1/2 (como electrones) confinados en un volumen $V = L^3$, sin interacciones entre ellos. El hamiltoniano es:

$$
\hat{H} = \sum_{i=1}^{N} \frac{\hat{\mathbf{p}}_i^2}{2m} = \sum_{\mathbf{k}, \sigma} \epsilon_{\mathbf{k}} \hat{c}_{\mathbf{k}\sigma}^\dagger \hat{c}_{\mathbf{k}\sigma}
$$

donde $\epsilon_{\mathbf{k}} = \frac{\hbar^2 k^2}{2m}$ y $\hat{c}_{\mathbf{k}\sigma}^\dagger$, $\hat{c}_{\mathbf{k}\sigma}$ son operadores de creación y aniquilación para fermiones con vector de onda $\mathbf{k}$ y proyección de spin $\sigma = \uparrow, \downarrow$.

Las condiciones de contorno periódicas imponen $\mathbf{k} = \frac{2\pi}{L}(n_x, n_y, n_z)$ con $n_i \in \mathbb{Z}$. La densidad de estados en el espacio $\mathbf{k}$ es:

$$
\frac{V}{(2\pi)^3} \quad \text{(número de estados por volumen en el espacio k)}
$$

#### **6.1.2. Estado Fundamental a T=0: Principio de Exclusión y Esfera de Fermi**
A temperatura cero, los fermiones ocupan los estados de menor energía posible, respetando el **principio de exclusión de Pauli** (máximo un fermión por estado cuántico $(\mathbf{k}, \sigma)$).

Si $N$ es grande, llenamos todos los estados con $|\mathbf{k}| \leq k_F$, donde $k_F$ es el **momento de Fermi**. El número total de partículas es:

$$
N = \sum_{|\mathbf{k}| \leq k_F, \sigma} 1 = 2 \times \frac{V}{(2\pi)^3} \times \frac{4}{3}\pi k_F^3
$$

El factor 2 viene del spin. Despejando:

$$
k_F = (3\pi^2 n)^{1/3}, \quad \text{donde } n = \frac{N}{V} \text{ es la densidad}
$$

La **energía de Fermi** correspondiente es:

$$
E_F = \frac{\hbar^2 k_F^2}{2m} = \frac{\hbar^2}{2m}(3\pi^2 n)^{2/3}
$$

La **superficie de Fermi** es la esfera de radio $k_F$ en el espacio $\mathbf{k}$. Todos los estados dentro están ocupados; todos fuera, vacíos.

#### **6.1.3. Densidad de Estados N(E)**
La densidad de estados $g(E)$ (número de estados por intervalo de energía y volumen) es crucial para calcular propiedades termodinámicas:

$$
g(E) = \frac{d}{dE} \left( \frac{\text{número de estados con energía} \leq E}{V} \right)
$$

Para fermiones libres con spin 1/2:

$$
g(E) = \frac{1}{V} \frac{d}{dE} \left[ 2 \times \frac{V}{(2\pi)^3} \times \frac{4}{3}\pi \left( \frac{2mE}{\hbar^2} \right)^{3/2} \right] = \frac{1}{2\pi^2} \left( \frac{2m}{\hbar^2} \right)^{3/2} \sqrt{E}
$$

En la energía de Fermi:

$$
g(E_F) = \frac{3n}{2E_F}
$$

#### **6.1.4. Energía del Estado Fundamental**
La energía total del estado fundamental es:

$$
E_0 = \sum_{|\mathbf{k}| \leq k_F, \sigma} \frac{\hbar^2 k^2}{2m} = 2 \times \frac{V}{(2\pi)^3} \int_{0}^{k_F} \frac{\hbar^2 k^2}{2m} \times 4\pi k^2 dk
$$

Evaluando la integral:

$$
E_0 = \frac{V}{5\pi^2} \frac{\hbar^2 k_F^5}{2m} = \frac{3}{5} N E_F
$$

La energía por partícula es $\frac{E_0}{N} = \frac{3}{5} E_F$.

#### **6.1.5. Presión y Compresibilidad del Gas de Fermi**
A $T=0$, ¡hay presión incluso sin interacciones! Esto es presión de degeneración cuántica.

La presión se obtiene de $P = -\left( \frac{\partial E_0}{\partial V} \right)_N$:

$$
P = \frac{2}{5} n E_F = \frac{\hbar^2}{5m} (3\pi^2)^{2/3} n^{5/3}
$$

El **módulo de compresibilidad** es:

$$
B = -V \left( \frac{\partial P}{\partial V} \right)_N = \frac{10}{9} \frac{E_0}{V} = \frac{2}{3} n E_F
$$

Para metales típicos, $E_F \sim 1-10$ eV, dando presiones enormes $\sim 10^{10}$ Pa. Esto es contrarrestado por la atracción coulombiana con los iones.

#### **6.1.6. Velocidad de Fermi y Temperatura de Fermi**
La **velocidad de Fermi** es:

$$
v_F = \frac{\hbar k_F}{m} = \frac{\hbar}{m}(3\pi^2 n)^{1/3}
$$

La **temperatura de Fermi**:

$$
T_F = \frac{E_F}{k_B}
$$

Para electrones en metales: $E_F \sim 1-10$ eV $\Rightarrow T_F \sim 10^4-10^5$ K. Por eso a temperatura ambiente ($T \ll T_F$), el gas de electrones está altamente degenerado.

### **6.2. Función de Correlación y Estructura de Pares**

#### **6.2.1. Función de Correlación Espacial**
La **función de correlación de pares** $g(\mathbf{r})$ mide la probabilidad relativa de encontrar una partícula en $\mathbf{r}$ dado que hay una en el origen:

$$
g(\mathbf{r}) = \frac{1}{n^2} \langle \hat{\psi}^\dagger(\mathbf{0})\hat{\psi}^\dagger(\mathbf{r})\hat{\psi}(\mathbf{r})\hat{\psi}(\mathbf{0}) \rangle
$$

Para fermiones libres no interactuantes a $T=0$:

$$
g(\mathbf{r}) = 1 - \frac{9}{(k_F r)^4} [\sin(k_F r) - k_F r \cos(k_F r)]^2
$$

#### **6.2.2. Análisis de la Función de Correlación**
- En $r=0$: $g(0) = 0$. ¡Dos fermiones idénticos no pueden estar en el mismo punto! Esto es el **agujero de intercambio** o **agujero de Fermi**.
- Para $r$ pequeño: $g(r) \approx \frac{1}{4}(k_F r)^2$ (crece parabólicamente).
- Oscilaciones de Friedel: Para $r$ grande:
  $$
  g(r) \approx 1 - \frac{9}{2(k_F r)^4} + \frac{9}{(k_F r)^3} \sin(2k_F r) \cos(2k_F r)
  $$
  Las oscilaciones con período $\pi/k_F$ reflejan la discontinuidad en la superficie de Fermi.
- En $r \to \infty$: $g(r) \to 1$ (no hay correlaciones a larga distancia para fermiones libres).

#### **6.2.3. Factor de Estructura Estático**
La transformada de Fourier de $g(\mathbf{r}) - 1$ es el **factor de estructura** $S(\mathbf{q})$:

$$
S(\mathbf{q}) = 1 + n \int [g(\mathbf{r}) - 1] e^{-i\mathbf{q}\cdot\mathbf{r}} d^3r
$$

Para fermiones libres a $T=0$:

$$
S(\mathbf{q}) = 
\begin{cases}
\frac{3q}{4k_F} - \frac{1}{16}\left(\frac{q}{k_F}\right)^3, & q \leq 2k_F \\
1, & q > 2k_F
\end{cases}
$$

La discontinuidad en $q = 2k_F$ (punto de Kohn) es característica de un líquido de Fermi.

### **6.3. Matriz de Funciones de Correlación**

#### **6.3.1. Función de Green a Tiempo Cero**
La **función de correlación uno-cuerpo** es:

$$
G(\mathbf{r}) = \langle \hat{\psi}^\dagger(\mathbf{0})\hat{\psi}(\mathbf{r}) \rangle = \frac{1}{V} \sum_{|\mathbf{k}| \leq k_F} e^{i\mathbf{k}\cdot\mathbf{r}}
$$

Para un sistema isotrópico:

$$
G(r) = \frac{1}{(2\pi)^3} \int_{0}^{k_F} 4\pi k^2 \frac{\sin(kr)}{kr} dk = \frac{3n}{2} \frac{j_1(k_F r)}{k_F r}
$$

donde $j_1(x) = \frac{\sin x}{x^2} - \frac{\cos x}{x}$ es la función esférica de Bessel de primer orden.

#### **6.3.2. Matriz Densidad Uno-Cuerpo**
La **matriz densidad** para estados de una partícula:

$$
\rho(\mathbf{r}, \mathbf{r}') = \langle \hat{\psi}^\dagger(\mathbf{r}')\hat{\psi}(\mathbf{r}) \rangle
$$

Para el gas homogéneo: $\rho(\mathbf{r}, \mathbf{r}') = G(\mathbf{r}-\mathbf{r}')$.

Los autovalores de $\rho$ son los **números de ocupación** $n_\alpha$. Para fermiones libres:
- Estados con $|\mathbf{k}| < k_F$: $n_\mathbf{k} = 1$
- Estados con $|\mathbf{k}| > k_F$: $n_\mathbf{k} = 0$

La discontinuidad en $k_F$ es característica de un líquido de Fermi.

#### **6.3.3. Longitud de Coherencia y Dependencia Espacial**
La decaimiento de $G(r)$ para $r \to \infty$ determina la **longitud de coherencia**. Para fermiones libres:

$$
G(r) \sim \frac{\cos(k_F r)}{r^2} \quad \text{(decaimiento algebraico, no exponencial)}
$$

Esto refleja la naturaleza crítica del estado fundamental de un líquido de Fermi.

### **6.4. Energía Fundamental y Teoría del Gas de Electrones**

#### **6.4.1. Expansión de Alta Densidad (Radio de Thomas-Fermi)**
Para electrones interactuantes, la energía cinética domina a alta densidad. Desarrollamos en el parámetro $r_s$, definido por:

$$
\frac{4}{3}\pi (r_s a_0)^3 = \frac{1}{n} \quad \Rightarrow \quad r_s = \left( \frac{3}{4\pi n a_0^3} \right)^{1/3}
$$

donde $a_0 = \frac{\hbar^2}{me^2}$ es el radio de Bohr. $r_s$ mide la distancia interelectrónica promedio en unidades atómicas.

#### **6.4.2. Energía por Partícula en el Gas Homogéneo de Electrones**
La energía total por partícula se escribe como:

$$
\frac{E}{N} = \frac{\epsilon_{\text{kin}} + \epsilon_{\text{pot}}}{N} = \left[ \frac{2.21}{r_s^2} - \frac{0.916}{r_s} + \epsilon_{\text{corr}}(r_s) \right] \text{Rydbergs}
$$

donde 1 Rydberg = $\frac{e^2}{2a_0} \approx 13.6$ eV.

**Términos**:
1. **Energía cinética**: $\frac{3}{5} E_F = \frac{3}{5} \frac{\hbar^2}{2m}(3\pi^2 n)^{2/3} = \frac{2.21}{r_s^2}$ Ry
2. **Energía de intercambio** (Hartree-Fock): $-\frac{3}{4\pi} (9\pi/4)^{1/3} \frac{e^2}{a_0 r_s} = -\frac{0.916}{r_s}$ Ry
3. **Energía de correlación** $\epsilon_{\text{corr}}(r_s)$: Más complicada, conocida numéricamente.

#### **6.4.3. Aproximación de Thomas-Fermi**
Para sistemas inhomogéneos, aproximamos la energía cinética como funcional de la densidad $n(\mathbf{r})$:

$$
T_{\text{TF}}[n] = \frac{3}{5} \frac{\hbar^2}{2m} (3\pi^2)^{2/3} \int n(\mathbf{r})^{5/3} d^3r
$$

La energía potencial incluye interacciones electrón-núcleo y electrón-electrón. Minimizando $E[n]$ con restricción $\int n d^3r = N$ da la **ecuación de Thomas-Fermi**:

$$
\frac{\hbar^2}{2m} (3\pi^2)^{2/3} n(\mathbf{r})^{2/3} + V_{\text{ext}}(\mathbf{r}) + \int \frac{n(\mathbf{r}')}{|\mathbf{r}-\mathbf{r}'|} d^3r' = \mu
$$

#### **6.4.4. Longitud de Pantalla de Thomas-Fermi**
Linealizando para un potencial débil, encontramos que la respuesta del gas de electrones **screena** (apantalla) las cargas:

$$
\nabla^2 V(\mathbf{r}) = 4\pi e^2 n(\mathbf{r}) \approx \frac{k_{\text{TF}}^2}{4\pi} V(\mathbf{r})
$$

donde el **vector de pantalla de Thomas-Fermi** es:

$$
k_{\text{TF}}^2 = 4\pi e^2 g(E_F) = \frac{4}{\pi} \left( \frac{3n}{\pi} \right)^{1/3} \frac{1}{a_0}
$$

La solución es potencial de Yukawa: $V(r) \sim \frac{e^{-k_{\text{TF}} r}}{r}$. La **longitud de pantalla** $\lambda_{\text{TF}} = 1/k_{\text{TF}}$ típicamente ~0.5 Å en metales.

---

## **7. BOSONES: FÍSICA DE SISTEMAS BOSÓNICOS**

### **7.1. Bosones Libres y Condensación de Bose-Einstein**

#### **7.1.1. Estadística de Bose-Einstein**
Para bosones libres, la función de distribución es:

$$
f_{\text{BE}}(\epsilon) = \frac{1}{e^{(\epsilon - \mu)/k_B T} - 1}
$$

El número total de partículas:

$$
N = \sum_{\mathbf{k}} \frac{1}{e^{(\epsilon_{\mathbf{k}} - \mu)/k_B T} - 1}
$$

Como $\mu < \epsilon_{\text{mín}} = 0$ para bosones libres, y $\mu \to 0^-$ cuando $T \to T_c$.

#### **7.1.2. Cálculo de la Temperatura Crítica**
Reemplazando suma por integral:

$$
N = \frac{V}{(2\pi)^3} \int \frac{1}{e^{(\hbar^2 k^2/2m - \mu)/k_B T} - 1} 4\pi k^2 dk
$$

A $T = T_c$, $\mu = 0$:

$$
N = \frac{V}{\lambda_T^3} \zeta(3/2)
$$

donde $\lambda_T = \sqrt{\frac{2\pi\hbar^2}{mk_B T}}$ es la **longitud de onda térmica de de Broglie** y $\zeta(3/2) \approx 2.612$.

Despejando:

$$
T_c = \frac{2\pi\hbar^2}{mk_B} \left( \frac{n}{\zeta(3/2)} \right)^{2/3}
$$

#### **7.1.3. Fracción Condensada para T < T_c**
Para $T < T_c$, una fracción macroscópica $N_0/N$ ocupa el estado fundamental ($\mathbf{k}=0$):

$$
\frac{N_0}{N} = 1 - \left( \frac{T}{T_c} \right)^{3/2}
$$

La energía del condensado $E_0 = 0$ (para partículas libres). Las partículas no condensadas tienen energía:

$$
E_{\text{exc}} = \frac{V}{\lambda_T^3} k_B T \frac{3}{2} \zeta(5/2)
$$

#### **7.1.4. Calor Específico**
El calor específico muestra una singularidad en $T_c$:

- Para $T \ll T_c$: $C_V \propto T^{3/2}$ (dominado por excitaciones)
- En $T = T_c$: $C_V$ tiene una discontinuidad (transición de fase de segundo orden)
- Para $T > T_c$: $C_V$ tiende al valor clásico $\frac{3}{2} N k_B$

### **7.2. Bosones Débilmente Interactuantes**

#### **7.2.1. Modelo de Gas de Bose con Interacciones**
Hamiltoniano con interacción de contacto:

$$
\hat{H} = \sum_{\mathbf{k}} \epsilon_{\mathbf{k}} \hat{a}_{\mathbf{k}}^\dagger \hat{a}_{\mathbf{k}} + \frac{g}{2V} \sum_{\mathbf{k},\mathbf{k}',\mathbf{q}} \hat{a}_{\mathbf{k}+\mathbf{q}}^\dagger \hat{a}_{\mathbf{k}'-\mathbf{q}}^\dagger \hat{a}_{\mathbf{k}'} \hat{a}_{\mathbf{k}}
$$

donde $g = \frac{4\pi\hbar^2 a_s}{m}$ y $a_s$ es la **longitud de dispersión**.

#### **7.2.2. Aproximación de Bogoliubov**
Para $T=0$, casi todas las partículas están en el condensado. Escribimos:

$$
\hat{a}_0 = \sqrt{N_0}, \quad \hat{a}_{\mathbf{k} \neq 0} = \text{pequeño}
$$

Mantenemos términos hasta segundo orden en $\hat{a}_{\mathbf{k} \neq 0}$. El hamiltoniano se diagonaliza mediante **transformación de Bogoliubov**:

$$
\hat{b}_{\mathbf{k}} = u_{\mathbf{k}} \hat{a}_{\mathbf{k}} + v_{\mathbf{k}} \hat{a}_{-\mathbf{k}}^\dagger
$$

con $u_{\mathbf{k}}^2 - v_{\mathbf{k}}^2 = 1$.

#### **7.2.3. Espectro de Excitanones (Bogolones)**
El hamiltoniano diagonalizado es:

$$
\hat{H} = E_0 + \sum_{\mathbf{k} \neq 0} \hbar\omega_{\mathbf{k}} \hat{b}_{\mathbf{k}}^\dagger \hat{b}_{\mathbf{k}}
$$

La energía de las excitaciones (relación de dispersión) es:

$$
\hbar\omega_{\mathbf{k}} = \sqrt{\epsilon_{\mathbf{k}}^2 + 2g n_0 \epsilon_{\mathbf{k}}}
$$

Para $k \to 0$: $\hbar\omega_{\mathbf{k}} \approx c_s \hbar k$, donde $c_s = \sqrt{\frac{g n_0}{m}}$ es la **velocidad del sonido**. Esto es el **modo de Goldstone** por ruptura de simetría U(1).

Para $k$ grande: $\hbar\omega_{\mathbf{k}} \approx \epsilon_{\mathbf{k}} + g n_0$ (partículas libres desplazadas).

#### **7.2.4. Depleción del Condensado**
Las interacciones sacan partículas del condensado incluso a $T=0$:

$$
\frac{N - N_0}{N} = \frac{8}{3\sqrt{\pi}} \sqrt{n a_s^3}
$$

### **7.3. Gas de Bosones: Propiedades Termodinámicas y Transiciones de Fase**

#### **7.3.1. Ecuación de Estado**
Usando la teoría de Bogoliubov, la presión a $T=0$ es:

$$
P = \frac{1}{2} g n^2 + \frac{64}{15\sqrt{\pi}} \frac{\hbar^2}{m} n^{5/2} a_s^{3/2} + \cdots
$$

El primer término es la **repulsión de campo medio**, el segundo es la **corrección de Lee-Huang-Yang**.

#### **7.3.2. Superfluidez y Función de Correlación**
La **función de correlación uno-cuerpo** para un condensado de Bose es:

$$
G_1(\mathbf{r}) = \langle \hat{\psi}^\dagger(\mathbf{0})\hat{\psi}(\mathbf{r}) \rangle \to n_0 \quad \text{cuando } r \to \infty
$$

Esto indica **orden de largo alcance** (ruptura de simetría U(1)).

La **función de correlación dos-cuerpos** muestra **condensación fuera de diagonal** (ODLRO):

$$
\lim_{|\mathbf{r}-\mathbf{r}'| \to \infty} \langle \hat{\psi}^\dagger(\mathbf{r})\hat{\psi}^\dagger(\mathbf{r}')\hat{\psi}(\mathbf{r}')\hat{\psi}(\mathbf{r}) \rangle \to |\langle \hat{\psi}(\mathbf{r}) \rangle|^4 = n_0^2
$$

#### **7.3.3. Ecuación de Gross-Pitaevskii**
La función de onda del condensado $\Psi(\mathbf{r}, t) = \langle \hat{\psi}(\mathbf{r}) \rangle$ satisface:

$$
i\hbar \frac{\partial \Psi}{\partial t} = \left[ -\frac{\hbar^2}{2m} \nabla^2 + V_{\text{ext}}(\mathbf{r}) + g |\Psi|^2 \right] \Psi
$$

Esta es una **ecuación no lineal de Schrödinger** (NLSE). Para el estado estacionario: $\Psi(\mathbf{r}, t) = \psi(\mathbf{r}) e^{-i\mu t/\hbar}$:

$$
\left[ -\frac{\hbar^2}{2m} \nabla^2 + V_{\text{ext}}(\mathbf{r}) + g |\psi|^2 \right] \psi = \mu \psi
$$

#### **7.3.4. Solución para Trampa Armónica**
Para $V_{\text{ext}}(\mathbf{r}) = \frac{1}{2} m (\omega_x^2 x^2 + \omega_y^2 y^2 + \omega_z^2 z^2)$, en el límite de Thomas-Fermi ($N a_s / a_{\text{ho}} \gg 1$, con $a_{\text{ho}} = \sqrt{\hbar/m\bar{\omega}}$):

$$
|\psi_{\text{TF}}(\mathbf{r})|^2 = \frac{\mu - V_{\text{ext}}(\mathbf{r})}{g} \Theta(\mu - V_{\text{ext}}(\mathbf{r}))
$$

El **perfil de densidad** es una parábola invertida:

$$
n(\mathbf{r}) = n_0 \left( 1 - \frac{x^2}{R_x^2} - \frac{y^2}{R_y^2} - \frac{z^2}{R_z^2} \right)
$$

con radios de Thomas-Fermi $R_i = \sqrt{\frac{2\mu}{m\omega_i^2}}$ y $\mu = \frac{\hbar\bar{\omega}}{2} \left( \frac{15N a_s}{a_{\text{ho}}} \right)^{2/5}$.

---

# **CONTINUACIÓN: EXPANSIÓN DETALLADA DE TEMAS AVANZADOS**

## **8. APLICACIONES: ÁTOMOS MULTIELECTRÓNICOS (CONTINUACIÓN)**

### **8.1. Aproximación de Campo Central y Determinantes de Slater**

#### **8.1.1. Hamiltonian Completo para Átomos Multielectrónicos**
El hamiltoniano exacto para un átomo con $N$ electrones y núcleo de carga $Ze$ es:

$$
\hat{H} = \sum_{i=1}^{N} \left[ -\frac{\hbar^2}{2m} \nabla_i^2 - \frac{Ze^2}{4\pi\epsilon_0 r_i} \right] + \frac{1}{2} \sum_{i \neq j} \frac{e^2}{4\pi\epsilon_0 |\mathbf{r}_i - \mathbf{r}_j|} + \hat{H}_{\text{spin-órbita}} + \cdots
$$

El término de repulsión electrón-electrón hace que el problema no sea separable exactamente.

#### **8.1.2. Aproximación de Campo Central (Hartree-Fock)**
Se aproxima el potencial real por un potencial efectivo esférico $V_{\text{eff}}(r)$:

$$
\hat{H}_{\text{aprox}} = \sum_{i=1}^{N} \left[ -\frac{\hbar^2}{2m} \nabla_i^2 + V_{\text{eff}}(r_i) \right]
$$

Cada electrón se describe por un **orbital atómico** $\phi_{nlm}(\mathbf{r}) = R_{nl}(r) Y_{lm}(\theta,\phi)$, pero ahora las funciones radiales $R_{nl}(r)$ no son las del hidrógeno.

#### **8.1.3. Determinantes de Slater**
La función de onda de $N$ electrones debe ser **antisimétrica**. Para un conjunto de orbitales $\{\phi_1, \phi_2, \ldots, \phi_N\}$, el determinante de Slater es:

$$
\Psi(\mathbf{x}_1, \mathbf{x}_2, \ldots, \mathbf{x}_N) = \frac{1}{\sqrt{N!}}
\begin{vmatrix}
\phi_1(\mathbf{x}_1) & \phi_1(\mathbf{x}_2) & \cdots & \phi_1(\mathbf{x}_N) \\
\phi_2(\mathbf{x}_1) & \phi_2(\mathbf{x}_2) & \cdots & \phi_2(\mathbf{x}_N) \\
\vdots & \vdots & \ddots & \vdots \\
\phi_N(\mathbf{x}_1) & \phi_N(\mathbf{x}_2) & \cdots & \phi_N(\mathbf{x}_N)
\end{vmatrix}
$$

donde $\mathbf{x}_i = (\mathbf{r}_i, \sigma_i)$ incluye coordenadas espaciales y spin.

#### **8.1.4. Ecuaciones de Hartree-Fock**
Minimizando la energía esperada $\langle \Psi | \hat{H} | \Psi \rangle$ con $\Psi$ un determinante de Slater, se obtienen las **ecuaciones de Hartree-Fock**:

$$
\left[ -\frac{\hbar^2}{2m} \nabla^2 - \frac{Ze^2}{4\pi\epsilon_0 r} \right] \phi_i(\mathbf{x}) + \sum_{j=1}^{N} \int d\mathbf{x}' \frac{e^2}{4\pi\epsilon_0 |\mathbf{r}-\mathbf{r}'|} |\phi_j(\mathbf{x}')|^2 \phi_i(\mathbf{x})
$$
$$
- \sum_{j=1}^{N} \delta_{\sigma_i\sigma_j} \int d\mathbf{x}' \frac{e^2}{4\pi\epsilon_0 |\mathbf{r}-\mathbf{r}'|} \phi_j^*(\mathbf{x}') \phi_i(\mathbf{x}') \phi_j(\mathbf{x}) = \epsilon_i \phi_i(\mathbf{x})
$$

El primer término de interacción es el **potencial de Hartree** (electrostático clásico), y el segundo es el **potencial de intercambio** (puramente cuántico, sin análogo clásico).

#### **8.1.5. Energía de Intercambio**
El término de intercambio surge del principio de exclusión de Pauli y tiene las propiedades:
1. Es **negativo** (estabilizador)
2. Depende del **spin**: solo opera entre electrones con el mismo spin
3. Es **no local**: depende del solapamiento de las funciones de onda

La **energía de intercambio** por electrón en el gas homogéneo es:

$$
\epsilon_{\text{exch}} = -\frac{3}{4\pi} (9\pi/4)^{1/3} \frac{e^2}{a_0 r_s} \approx -\frac{0.916}{r_s} \text{ Ry}
$$

### **8.2. Configuraciones Electrónicas y Reglas de Hund**

#### **8.2.1. Órdenes de Llenado de Orbitales**
Los orbitales se llenan en orden de energía creciente. Para átomos hidrogenoides, la energía solo depende de $n$: $E_n \propto -1/n^2$. Pero en átomos multielectrónicos:
1. **Penetración orbital**: Orbitales con $l$ menor penetran más hacia el núcleo, experimentan menos apantallamiento y tienen menor energía.
2. **Apantallamiento**: Electrones internos "apantallan" la carga nuclear para electrones externos.

El orden aproximado es:
$$
1s < 2s < 2p < 3s < 3p < 4s < 3d < 4p < 5s < 4d < 5p < 6s < 4f < 5d < \cdots
$$

#### **8.2.2. Reglas de Hund**
Para una subcapa dada (mismos $n, l$), la configuración de menor energía sigue:
1. **Máxima multiplicidad de spin**: Se llena maximizando $S$ (número de electrones con spin paralelo).
2. **Máximo $L$**: Para una multiplicidad dada, se maximiza $L$.
3. **Regla de acoplamiento spin-órbita**: Para subcapas menos de media llena, el nivel con $J = |L-S|$ es más bajo; para más de media llena, $J = L+S$ es más bajo.

Ejemplo: Configuración $p^2$ (carbono):
- $S = 1$ (triplete) es más bajo que $S = 0$ (singlete)
- Para $S=1$, $L=1$ ($P$) es más bajo que $L=2$ ($D$) o $L=0$ ($S$)
- La subcapa $p$ está menos de media llena (2 de 6), así que $J = |1-1| = 0$
- El término fundamental es $^{3}P_0$

#### **8.2.3. Notación Espectroscópica**
Los términos atómicos se denotan como $^{2S+1}L_J$, donde:
- $2S+1$ es la **multiplicidad de spin**
- $L$ se representa por letra: $S(L=0), P(1), D(2), F(3), G(4), \ldots$
- $J$ es el momento angular total

### **8.3. Estructura Fina en Átomos Multielectrónicos**

#### **8.3.1. Acoplamiento de Momentos Angulares**
En átomos ligeros, domina el **acoplamiento LS** (Russell-Saunders):
$$
\mathbf{L} = \sum_i \mathbf{l}_i, \quad \mathbf{S} = \sum_i \mathbf{s}_i, \quad \mathbf{J} = \mathbf{L} + \mathbf{S}
$$

En átomos pesados, el **acoplamiento jj**:
$$
\mathbf{j}_i = \mathbf{l}_i + \mathbf{s}_i, \quad \mathbf{J} = \sum_i \mathbf{j}_i
$$

#### **8.3.2. Interacción Spin-Órbita en Átomos Multielectrónicos**
El hamiltoniano spin-órbita es:
$$
\hat{H}_{\text{SO}} = \sum_i \xi(r_i) \mathbf{l}_i \cdot \mathbf{s}_i
$$

Para un término $^{2S+1}L$, en acoplamiento LS:
$$
\langle LSJM_J | \sum_i \mathbf{l}_i \cdot \mathbf{s}_i | LSJM_J \rangle = \frac{\zeta_{nl}}{2} [J(J+1) - L(L+1) - S(S+1)]
$$

donde $\zeta_{nl}$ es la **constante de acoplamiento spin-órbita**.

#### **8.3.3. Regla de Intervalos de Landé**
Para un multiplete dado, la separación entre niveles consecutivos $J$ y $J-1$ es:
$$
\Delta E_{J,J-1} = \frac{\zeta_{nl}}{2} J
$$

Los intervalos están en razón de los números $J$ más grandes.

### **8.4. Tabla Periódica y Propiedades Periódicas**

#### **8.4.1. Construcción de la Tabla Periódica**
Los grupos (columnas) tienen configuraciones electrónicas similares en la capa de valencia:
- **Grupo 1 (alcalinos)**: $ns^1$
- **Grupo 2 (alcalinotérreos)**: $ns^2$
- **Grupos 3-12 (metales de transición)**: llenado de $d$
- **Grupos 13-18**: llenado de $p$
- **Lantánidos y actínidos**: llenado de $f$

#### **8.4.2. Propiedades Periódicas**
1. **Radio atómico**: Disminuye a lo largo de un período (mayor carga nuclear efectiva), aumenta bajando en un grupo (nivel cuántico principal mayor).
2. **Energía de ionización**: Aumenta a lo largo de un período, disminuye bajando en un grupo.
3. **Afinidad electrónica**: Generalmente aumenta a lo largo de un período.
4. **Electronegatividad** (Pauling): Aumenta a lo largo de un período, disminuye bajando en un grupo.

#### **8.4.3. Excepciones a las Reglas de Llenado**
Debido a la competencia entre energía de intercambio (favorece llenado paralelo) y repulsión electrostática:
- $\text{Cr} (Z=24)$: $[\text{Ar}] 4s^1 3d^5$ en lugar de $4s^2 3d^4$
- $\text{Cu} (Z=29)$: $[\text{Ar}] 4s^1 3d^{10}$ en lugar de $4s^2 3d^9$

---

## **9. ECUACIONES DE ONDA RELATIVISTAS**

### **9.1. Ecuación de Klein-Gordon**

#### **9.1.1. Derivación a partir de la Relatividad Especial**
De la relación energía-momento relativista:
$$
E^2 = p^2c^2 + m^2c^4
$$

Cuantizando ($E \to i\hbar\frac{\partial}{\partial t}$, $\mathbf{p} \to -i\hbar\nabla$):
$$
-\hbar^2 \frac{\partial^2}{\partial t^2} \psi = (-\hbar^2 c^2 \nabla^2 + m^2c^4) \psi
$$

Reordenando se obtiene la **ecuación de Klein-Gordon**:
$$
\left( \frac{1}{c^2} \frac{\partial^2}{\partial t^2} - \nabla^2 + \frac{m^2c^2}{\hbar^2} \right) \psi(\mathbf{r},t) = 0
$$

O en forma covariante:
$$
(\partial_\mu \partial^\mu + \frac{m^2c^2}{\hbar^2}) \psi = 0
$$

#### **9.1.2. Soluciones de Onda Plana**
Para $\psi(\mathbf{r},t) = e^{i(\mathbf{k}\cdot\mathbf{r} - \omega t)}$, sustituyendo:
$$
\left( -\frac{\omega^2}{c^2} + k^2 + \frac{m^2c^2}{\hbar^2} \right) \psi = 0
$$

La relación de dispersión es:
$$
\omega^2 = c^2k^2 + \frac{m^2c^4}{\hbar^2}
$$

Hay soluciones con $\omega > 0$ y $\omega < 0$ (energías positivas y negativas).

#### **9.1.3. Problemas con la Interpretación Probabilística**
La densidad de probabilidad se obtiene de la ecuación de continuidad. Para Klein-Gordon:
$$
\rho = \frac{i\hbar}{2mc^2} \left( \psi^* \frac{\partial\psi}{\partial t} - \psi \frac{\partial\psi^*}{\partial t} \right)
$$

Problemas:
1. $\rho$ no es definida positiva (puede ser negativa)
2. Para soluciones de energía negativa, $\rho < 0$
3. No es una teoría de una partícula: necesita reinterpretación como teoría de campos

#### **9.1.4. Ecuación de Klein-Gordon con Potencial Electromagnético**
Acoplamiento mínimo: $\partial_\mu \to D_\mu = \partial_\mu + \frac{iq}{\hbar} A_\mu$:
$$
\left[ (\partial_\mu + \frac{iq}{\hbar} A_\mu)(\partial^\mu + \frac{iq}{\hbar} A^\mu) + \frac{m^2c^2}{\hbar^2} \right] \psi = 0
$$

Para un potencial coulombiano $A_0 = -\frac{Ze}{4\pi\epsilon_0 r}$, las soluciones dan niveles de energía:
$$
E_{n,j} = mc^2 \left[ 1 + \frac{(Z\alpha)^2}{\left( n - (j+1/2) + \sqrt{(j+1/2)^2 - (Z\alpha)^2} \right)^2 } \right]^{-1/2}
$$

donde $\alpha = \frac{e^2}{4\pi\epsilon_0\hbar c} \approx 1/137$ es la constante de estructura fina.

### **9.2. Ecuación de Dirac**

#### **9.2.1. Motivación: Linealización de la Relación Energía-Momento**
Dirac buscó una ecuación lineal en $\frac{\partial}{\partial t}$. Propuso:
$$
i\hbar \frac{\partial \psi}{\partial t} = \left[ c \boldsymbol{\alpha} \cdot (-i\hbar\nabla) + \beta mc^2 \right] \psi
$$

donde $\boldsymbol{\alpha} = (\alpha_1, \alpha_2, \alpha_3)$ y $\beta$ son matrices que deben satisfacer:
$$
\alpha_i \alpha_j + \alpha_j \alpha_i = 2\delta_{ij} I, \quad \alpha_i \beta + \beta \alpha_i = 0, \quad \beta^2 = I
$$

#### **9.2.2. Representación de Matrices de Dirac**
La representación más común (representación de Dirac-Pauli):
$$
\alpha_i = \begin{pmatrix} 0 & \sigma_i \\ \sigma_i & 0 \end{pmatrix}, \quad \beta = \begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}
$$

donde $\sigma_i$ son matrices de Pauli y $I$ es la matriz identidad 2×2.

Definiendo $\gamma^0 = \beta$, $\gamma^i = \beta\alpha_i$, la ecuación se escribe en forma covariante:
$$
(i\hbar \gamma^\mu \partial_\mu - mc) \psi = 0
$$

Las matrices $\gamma^\mu$ satisfacen el álgebra de Clifford:
$$
\{\gamma^\mu, \gamma^\nu\} = 2g^{\mu\nu} I
$$
con $g^{\mu\nu} = \text{diag}(1, -1, -1, -1)$.

#### **9.2.3. Espinores de Dirac**
La función de onda $\psi$ es un **espinor de Dirac** con 4 componentes:
$$
\psi = \begin{pmatrix} \psi_1 \\ \psi_2 \\ \psi_3 \\ \psi_4 \end{pmatrix} = \begin{pmatrix} \phi \\ \chi \end{pmatrix}
$$
donde $\phi$ y $\chi$ son espinores de 2 componentes.

#### **9.2.4. Soluciones de Onda Plana**
Para una partícula libre, buscamos soluciones $\psi(\mathbf{r},t) = u(\mathbf{p}) e^{i(\mathbf{p}\cdot\mathbf{r} - Et)/\hbar}$.

La ecuación se convierte en:
$$
(\gamma^0 E/c - \boldsymbol{\gamma} \cdot \mathbf{p} - mc) u(\mathbf{p}) = 0
$$

Hay cuatro soluciones linealmente independientes:
1. Dos con $E > 0$ (partículas)
2. Dos con $E < 0$ (antipartículas)

Para partículas en reposo ($\mathbf{p} = 0$):
$$
u^{(1)} = \begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \end{pmatrix}, \quad u^{(2)} = \begin{pmatrix} 0 \\ 1 \\ 0 \\ 0 \end{pmatrix}, \quad u^{(3)} = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix}, \quad u^{(4)} = \begin{pmatrix} 0 \\ 0 \\ 0 \\ 1 \end{pmatrix}
$$
con energías $E = mc^2$ para $u^{(1)}, u^{(2)}$ y $E = -mc^2$ para $u^{(3)}, u^{(4)}$.

#### **9.2.5. Operadores de Proyección de Energía y Helicidad**
El **operador de proyección de energía**:
$$
\Lambda_+(\mathbf{p}) = \frac{\gamma^\mu p_\mu + mc}{2mc}, \quad \Lambda_-(\mathbf{p}) = \frac{-\gamma^\mu p_\mu + mc}{2mc}
$$
proyectan sobre estados de energía positiva y negativa respectivamente.

El **operador de helicidad**:
$$
h = \frac{\boldsymbol{\Sigma} \cdot \mathbf{p}}{|\mathbf{p}|}, \quad \text{donde } \boldsymbol{\Sigma} = \begin{pmatrix} \boldsymbol{\sigma} & 0 \\ 0 & \boldsymbol{\sigma} \end{pmatrix}
$$
conmuta con el hamiltoniano libre y clasifica estados con spin paralelo o antiparalelo al momento.

#### **9.2.6. Corrientes de Probabilidad y Covarianza**
La ecuación de Dirac tiene una densidad de probabilidad definida positiva:
$$
\rho = \psi^\dagger \psi
$$

La **corriente de probabilidad**:
$$
j^\mu = c \bar{\psi} \gamma^\mu \psi
$$
donde $\bar{\psi} = \psi^\dagger \gamma^0$ es el **adjunto de Dirac**.

Se satisface la ecuación de continuidad: $\partial_\mu j^\mu = 0$.

#### **9.2.7. Acoplamiento al Campo Electromagnético**
Por acoplamiento mínimo: $\partial_\mu \to D_\mu = \partial_\mu + \frac{iq}{\hbar} A_\mu$:
$$
\left[ \gamma^\mu (i\hbar\partial_\mu - qA_\mu) - mc \right] \psi = 0
$$

#### **9.2.8. Átomo de Hidrógeno en la Ecuación de Dirac**
Para un potencial coulombiano $A_0 = -\frac{Ze}{4\pi\epsilon_0 r}$, la ecuación de Dirac puede resolverse exactamente. Los niveles de energía son:
$$
E_{n,j} = mc^2 \left[ 1 + \frac{(Z\alpha)^2}{\left( n - (j+1/2) + \sqrt{(j+1/2)^2 - (Z\alpha)^2} \right)^2 } \right]^{-1/2}
$$

Expandiendo en potencias de $(Z\alpha)^2$:
$$
E_{n,j} \approx mc^2 \left[ 1 - \frac{(Z\alpha)^2}{2n^2} - \frac{(Z\alpha)^4}{2n^4} \left( \frac{n}{j+1/2} - \frac{3}{4} \right) + \cdots \right]
$$

Términos:
1. $mc^2$: Energía en reposo
2. $-\frac{(Z\alpha)^2}{2n^2} mc^2$: Estructura de Bohr
3. $-\frac{(Z\alpha)^4}{2n^4} \left( \frac{n}{j+1/2} - \frac{3}{4} \right) mc^2$: Estructura fina

La **estructura fina** incluye:
- Corrección relativista de la energía cinética
- Acoplamiento spin-órbita
- Término de Darwin (solo para $l=0$)

#### **9.2.9. Predicciones de la Ecuación de Dirac**
1. **Spin 1/2 intrínseco**: Emerge naturalmente
2. **Momento magnético**: Relación giromagnética $g = 2$ (experimentalmente $g \approx 2.0023$, la diferencia se explica por QED)
3. **Antipartículas**: Soluciones de energía negativa interpretadas como positrones (predicho por Dirac en 1928, descubierto por Anderson en 1932)
4. **Estructura fina del hidrógeno**: Concuerda con datos espectroscópicos

#### **9.2.10. Teoría de Huecos y Mar de Dirac**
Interpretación original de Dirac: todos los estados de energía negativa están llenos (el "mar de Dirac"). Un hueco en el mar se interpreta como una antipartícula de energía positiva.

Problemas: Infinitos (el mar tiene energía infinita), violación de simetría de carga-paridad-tiempo (CPT) para fermiones.

Interpretación moderna (teoría cuántica de campos): Las soluciones de energía negativa corresponden a antipartículas en la teoría cuántica de campos.

#### **9.2.11. Límite no Relativista**
Para $v \ll c$, la ecuación de Dirac se reduce a la ecuación de Pauli:
$$
i\hbar \frac{\partial \phi}{\partial t} = \left[ \frac{1}{2m} \left( \mathbf{p} - \frac{q}{c} \mathbf{A} \right)^2 + q\Phi - \frac{q\hbar}{2mc} \boldsymbol{\sigma} \cdot \mathbf{B} \right] \phi
$$

El último término es la interacción del momento magnético de spin $\boldsymbol{\mu} = \frac{q\hbar}{2mc} \boldsymbol{\sigma}$ con el campo magnético.

#### **9.2.12. Desintegración β y Teoría de Fermi**
La ecuación de Dirac es la base de la teoría de la desintegración β:
$$
n \to p + e^- + \bar{\nu}_e
$$

La interacción de Fermi (1934) es:
$$
\mathcal{H}_{\text{Fermi}} = \frac{G_F}{\sqrt{2}} [\bar{\psi}_p \gamma^\mu (1 - g_A \gamma^5) \psi_n] [\bar{\psi}_e \gamma_\mu (1 - \gamma^5) \psi_\nu] + \text{h.c.}
$$

### **9.3. Comparación entre Klein-Gordon y Dirac**

| Propiedad | Klein-Gordon | Dirac |
|-----------|--------------|-------|
| **Espín** | 0 (escalar) | 1/2 (espinor) |
| **Densidad de probabilidad** | No definida positiva | Definida positiva |
| **Soluciones de energía negativa** | Sí | Sí |
| **Número de componentes** | 1 (escalar complejo) | 4 (espinor) |
| **Ecuación** | 2º orden en tiempo | 1º orden en tiempo |
| **Álgebra** | Escalar | Matricial (álgebra de Clifford) |
| **Aplicaciones** | Piones (π), kaones (K) | Electrones, protones, neutrinos |

### **9.4. Ecuación de Dirac en Campos Externos**

#### **9.4.1. Oscilador Armónico de Dirac**
Hamiltoniano:
$$
\hat{H} = c \boldsymbol{\alpha} \cdot \mathbf{p} + \beta mc^2 + \frac{1}{2} m\omega^2 r^2
$$

Las soluciones exactas muestran un espectro equiespaciado con degeneración.

#### **9.4.2. Partícula de Dirac en Campo Magnético Uniforme**
Para $\mathbf{B} = B\hat{z}$, en gauge de Landau $\mathbf{A} = (-By, 0, 0)$, los niveles de energía (niveles de Landau relativistas) son:
$$
E_{n,p_z} = \pm \sqrt{m^2c^4 + p_z^2c^2 + 2n\hbar\omega_c mc^2}
$$
con $\omega_c = \frac{|q|B}{mc}$ y $n = 0, 1, 2, \ldots$

Para $n=0$, solo hay un nivel (no doblemente degenerado como en el caso no relativista).

#### **9.4.3. Efecto Aharonov-Bohm para Fermiones de Dirac**
La fase Aharonov-Bohm afecta tanto a la parte orbital como a la parte de spin del espinor de Dirac.

---

# **APÉNDICE: HERRAMIENTAS MATEMÁTICAS AVANZADAS**

### **A.1. Teoría de Grupos en Mecánica Cuántica**

#### **A.1.1. Grupos de Lie y Álgebras de Lie**
- **SO(3)**: Grupo de rotaciones en 3D. Álgbra: $[J_i, J_j] = i\hbar \epsilon_{ijk} J_k$
- **SU(2)**: Cubierta doble de SO(3). Representaciones de spin.
- **Grupo de Lorentz**: Transformaciones de Lorentz. Generadores: rotaciones $i$ y boosts $K_i$.

#### **A.1.2. Teorema de Wigner-Eckart**
Para operadores tensoriales esféricos $T^{(k)}_q$$$
\langle \alpha', j', m' | T^{(k)}_q | \alpha, j, m \rangle = \langle j, m; k, q | j', m' \rangle \frac{\langle \alpha', j' || T^{(k)} || \alpha, j \rangle}{\sqrt{2j'+1}}
$$

El coeficiente de Clebsch-Gordan contiene toda la dependencia en $m, m', q$. El **elemento de matriz reducido** $\langle \alpha', j' || T^{(k)} || \alpha, j \rangle$ es independiente de $m$.

### **A.2. Métodos de Integrales de Camino**

#### **A.2.1. Formulación de Integral de Camino de Feynman**
La amplitud de transición se escribe como:
$$
K(x_f, t_f; x_i, t_i) = \int \mathcal{D}x(t) \, e^{iS[x(t)]/\hbar}
$$

Para el oscilador armónico:
$$
K(x_f, t_f; x_i, t_i) = \sqrt{\frac{m\omega}{2\pi i\hbar \sin\omega T}} \exp\left[ \frac{im\omega}{2\hbar\sin\omega T} \left( (x_i^2 + x_f^2)\cos\omega T - 2x_i x_f \right) \right]
$$

#### **A.2.2. Integral de Camino para la Ecuación de Schrödinger**
Derivación de la ecuación de Schrödinger a partir de la integral de camino:
$$
\psi(x, t+\epsilon) = \frac{1}{A} \int dy \, e^{iS[x,y]/\hbar} \psi(y, t)
$$
donde $S[x,y] \approx \frac{m}{2\epsilon}(x-y)^2 - \epsilon V\left(\frac{x+y}{2}\right)$.

Tomando $\epsilon \to 0$ se recupera la ecuación de Schrödinger.

### **A.3. Métodos Numéricos en Mecánica Cuántica**

#### **A.3.1. Método de Diferencias Finitas**
Discretización de la ecuación de Schrödinger:
$$
-\frac{\hbar^2}{2m} \frac{\psi_{i+1} - 2\psi_i + \psi_{i-1}}{(\Delta x)^2} + V_i \psi_i = E \psi_i
$$

Conduce a un problema de autovalores tridiagonal.

#### **A.3.2. Método de Colocación**
Expansión en base de funciones conocidas:
$$
\psi(x) = \sum_{n=1}^N c_n \phi_n(x)
$$

La ecuación de Schrödinger se convierte en un problema de autovalores generalizado:
$$
\sum_n (H_{mn} - E S_{mn}) c_n = 0
$$
con $H_{mn} = \langle \phi_m | \hat{H} | \phi_n \rangle$ y $S_{mn} = \langle \phi_m | \phi_n \rangle$.

#### **A.3.3. Método de Monte Carlo Cuántico**
- **Monte Carlo Variacional**: Muestreo de $|\psi_T|^2$ para calcular valores esperados.
- **Difusión de Monte Carlo**: Simulación de la ecuación de Schrödinger en tiempo imaginario $\tau = it$.
- **Path Integral Monte Carlo**: Muestreo de configuraciones en la integral de camino.

---

Esta guía completa cubre los temas fundamentales y avanzados de un programa de pregrado en física. Para aprobar los cursos, es esencial:

1. **Comprender los conceptos fundamentales** de cada tema
2. **Saber derivar resultados clave** (energías del oscilador armónico, átomo de hidrógeno, etc.)
3. **Practicar la resolución de problemas** aplicando estos conceptos
4. **Entender las conexiones entre diferentes temas**

¡Mucho éxito en tus estudios de física cuántica