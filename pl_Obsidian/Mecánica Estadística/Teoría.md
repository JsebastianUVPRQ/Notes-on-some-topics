
A continuación, presento el desarrollo de los contenidos solicitados estructurados como un **capítulo de libro de texto universitario de Mecánica Estadística**. El tono es formal, riguroso y matemático, diseñado para estudiantes de física o química física.

---

# UNIDAD 2: DESCRIPCIÓN ESTADÍSTICA DE UN SISTEMA FÍSICO

La mecánica estadística nace de la necesidad de conectar el comportamiento microscópico de $N$ partículas (donde $N \sim 10^{23}$) con las observables macroscópicas de la termodinámica.

### 2.1 Especificación Microscópica y Espacio de Fase

El **microestado** es la especificación más completa posible del sistema.

- Caso Clásico: Para un sistema de $N$ partículas puntuales, el estado se define por sus coordenadas generalizadas $\mathbf{q} = (q_1, ..., q_{3N})$ y sus momentos conjugados $\mathbf{p} = (p_1, ..., p_{3N})$. Esto define un punto en un espacio de fase de $6N$ dimensiones. La evolución temporal está regida por las ecuaciones de Hamilton:
    
    $$\dot{q}_i = \frac{\partial \mathcal{H}}{\partial p_i}, \quad \dot{p}_i = - \frac{\partial \mathcal{H}}{\partial q_i}$$
    
    donde $\mathcal{H}(\mathbf{q}, \mathbf{p})$ es el Hamiltoniano del sistema.
    
- **Caso Cuántico:** El microestado está descrito por una función de onda $\Psi(t)$ que obedece la ecuación de Schrödinger, o más comúnmente en mecánica estadística, por un estado propio estacionario $| \psi_i \rangle$ con energía $E_i$.
    

**Estados Accesibles:** Son todos los microestados teóricos que son compatibles con las restricciones externas impuestas al sistema (por ejemplo, que la energía total esté confinada en un intervalo $E \pm \delta E$ y que las partículas estén dentro de un volumen $V$).

### 2.2 Descripción Macroscópica

Un macroestado está definido por un número reducido de variables termodinámicas $(N, V, E)$. Un solo macroestado corresponde a un número inmenso de microestados.

Si denotamos una propiedad macroscópica como $f$, su valor medido experimentalmente corresponde al promedio temporal de la variable dinámica $f(\mathbf{q}, \mathbf{p})$ a lo largo de la trayectoria del sistema:

$$\bar{f}_{tiempo} = \lim_{T \to \infty} \frac{1}{T} \int_0^T f(\mathbf{q}(t), \mathbf{p}(t)) dt$$

### 2.3 Definición de Ensamble Estadístico

Calcular el promedio temporal es analíticamente imposible para $10^{23}$ partículas. Gibbs introdujo el concepto de **ensamble**: una colección mental de $\mathcal{N}$ réplicas idénticas del sistema (donde $\mathcal{N} \to \infty$), todas en el mismo macroestado pero en diferentes microestados posibles.

La Hipótesis Ergódica establece que, para un sistema en equilibrio, el promedio temporal es igual al promedio sobre el ensamble:

$$\langle f \rangle_{ensamble} = \sum_{i} f_i P_i$$

donde $P_i$ es la probabilidad de que el sistema se encuentre en el microestado $i$.

### 2.4 Número y Densidad de Estados

Para cuantificar la probabilidad, necesitamos contar estados.

- Volumen en el espacio de fase: $\Gamma(E)$ es el volumen ocupado por todos los estados con energía menor o igual a $E$:
    
    $$\Gamma(E) = \int_{H(\mathbf{q},\mathbf{p}) \le E} d^{3N}q \, d^{3N}p$$
    
    Debido al principio de incertidumbre, la unidad mínima de volumen en el espacio de fase es $h^{3N}$.
    
- Número de estados ($\Omega$): El número de estados con energía entre $E$ y $E + \delta E$ es:
    
    $$\Omega(E) = \frac{1}{h^{3N}} \frac{\partial \Gamma}{\partial E} \delta E$$
    
- Densidad de estados ($g(E)$):
    
    $$g(E) = \frac{\Omega(E)}{\delta E} = \frac{1}{h^{3N}} \int \delta(E - \mathcal{H}(\mathbf{q}, \mathbf{p})) d^{3N}q \, d^{3N}p$$
    

---

## UNIDAD 3: ENSAMBLE MICROCANÓNICO

Este ensamble representa un sistema **aislado** $(E, V, N)$ constantes.

### 3.1 Postulado Fundamental

Para un sistema aislado en equilibrio, todos los microestados accesibles son equiprobables.

Si $\Omega(E, V, N)$ es el número total de estados accesibles, la probabilidad $P_i$ de encontrar el sistema en el estado $i$ es:

$$P_i = \begin{cases} \frac{1}{\Omega(E,V,N)} & \text{si } E < E_i < E+\delta E \\ 0 & \text{en otro caso} \end{cases}$$

### 3.2 Conexión con la Termodinámica: Entropía

Ludwig Boltzmann estableció el puente entre el conteo de estados (microscópico) y la entropía (macroscópico):

$$S(E, V, N) = k_B \ln \Omega(E, V, N)$$

Donde $k_B \approx 1.38 \times 10^{-23} \, J/K$ es la constante de Boltzmann.

A partir de esta definición, la temperatura absoluta $T$ se define termodinámicamente como:

$$\frac{1}{T} = \left( \frac{\partial S}{\partial E} \right)_{V, N}$$

Esto implica que la temperatura es una medida de qué tan rápido aumenta el número de estados accesibles al aumentar la energía.

### 3.3 Presión y Potencial Químico

Usando la relación termodinámica fundamental $dE = TdS - PdV + \mu dN$, obtenemos:

$$P = T \left( \frac{\partial S}{\partial V} \right)_{E, N} = k_B T \left( \frac{\partial \ln \Omega}{\partial V} \right)_{E, N}$$

$$\mu = -T \left( \frac{\partial S}{\partial N} \right)_{E, V}$$

---

## UNIDAD 4: ENSAMBLE CANÓNICO

Describe un sistema en **contacto térmico** con un reservorio (baño térmico) a temperatura $T$. El sistema puede intercambiar energía, pero $V$ y $N$ son fijos.

### 4.1 Distribución de Boltzmann

Consideramos un sistema $S$ y un reservorio $R$. La energía total es $E_{tot} = E_S + E_R = \text{cte}$. Dado que $R$ es mucho más grande que $S$ ($E_S \ll E_{tot}$), expandimos la entropía del reservorio en serie de Taylor alrededor de $E_{tot}$:

$$S_R(E_{tot} - E_S) \approx S_R(E_{tot}) - E_S \left( \frac{\partial S_R}{\partial E} \right) = S_R(E_{tot}) - \frac{E_S}{T}$$

La probabilidad de que el sistema esté en un estado $i$ con energía $E_i$ es proporcional al número de estados del reservorio:

$$P_i \propto \Omega_R(E_{tot} - E_i) = e^{S_R/k_B} \propto e^{-E_i / k_B T}$$

Definiendo $\beta \equiv \frac{1}{k_B T}$, obtenemos el factor de Boltzmann:

$$P_i = \frac{1}{Z} e^{-\beta E_i}$$

### 4.2 Función de Partición Canónica ($Z$)

El factor de normalización $Z$ es la cantidad más importante en este ensamble:

$$Z(T, V, N) = \sum_{i} e^{-\beta E_i}$$

Si el espectro de energía es continuo:

$$Z = \frac{1}{N! h^{3N}} \int e^{-\beta \mathcal{H}(\mathbf{q}, \mathbf{p})} d^{3N}q \, d^{3N}p$$

(Nota: El factor $1/N!$ se introduce ad hoc en mecánica clásica para resolver la Paradoja de Gibbs sobre la indistinguibilidad de las partículas y hacer extensiva la entropía).

### 4.3 Relación con la Termodinámica

La conexión fundamental es a través de la Energía Libre de Helmholtz ($F$):

$$F(T, V, N) = -k_B T \ln Z(T, V, N)$$

A partir de $F = U - TS$, podemos derivar todas las propiedades:

- **Entropía:** $S = -\left(\frac{\partial F}{\partial T}\right)_V$
    
- **Presión:** $P = -\left(\frac{\partial F}{\partial V}\right)_T$
    
- **Energía Interna Media:** $\langle E \rangle = -\frac{\partial \ln Z}{\partial \beta}$
    

### 4.4 Teorema de Equipartición

Si el Hamiltoniano es cuadrático en una coordenada o momento (ej. $E_{cin} = p^2/2m$), entonces:

$$\langle \text{Término cuadrático} \rangle = \frac{1}{2} k_B T$$

Para un gas ideal monoatómico con 3 grados de libertad traslacionales: $U = \frac{3}{2} N k_B T$.

### 4.5 Distribución de Velocidades de Maxwell

Para un gas ideal clásico, la probabilidad de encontrar una partícula con velocidad $v$ es:

$$f(v) dv = 4\pi \left( \frac{m}{2\pi k_B T} \right)^{3/2} v^2 e^{-\frac{mv^2}{2k_B T}} dv$$

Esto predice la velocidad más probable ($v_p = \sqrt{2k_B T/m}$) y la velocidad cuadrática media ($v_{rms} = \sqrt{3k_B T/m}$).Shutterstock

---

## UNIDAD 5: ENSAMBLE GRAN CANÓNICO

Describe un sistema abierto que intercambia **energía y partículas** con un reservorio caracterizado por $(T, \mu)$. Variables fijas: $V, T, \mu$.

### 5.1 Probabilidad Gran Canónica

Siguiendo un razonamiento análogo al canónico, pero expandiendo la entropía respecto a la energía y al número de partículas, la probabilidad de encontrar al sistema con $N$ partículas en el estado cuántico $i$ con energía $E_{i,N}$ es:

$$P(N, i) = \frac{1}{\Xi} e^{-\beta (E_{i,N} - \mu N)}$$

Donde $\mu$ es el potencial químico.

### 5.2 Función de Partición Gran Canónica ($\Xi$)

Llamada a veces $\mathcal{Z}$, se define como:

$$\Xi(T, V, \mu) = \sum_{N=0}^{\infty} \sum_{i} e^{-\beta (E_{i,N} - \mu N)}$$

A menudo se introduce la fugacidad $z = e^{\beta \mu}$, reescribiendo $\Xi$ como una suma ponderada de funciones de partición canónicas:

$$\Xi = \sum_{N=0}^{\infty} z^N Z(T, V, N)$$

### 5.3 El Gran Potencial ($\Phi_G$ o $\Omega_G$)

El potencial termodinámico asociado es el Gran Potencial:

$$\Phi_G(T, V, \mu) = -k_B T \ln \Xi$$

Termodinámicamente, $\Phi_G = U - TS - \mu N = -PV$. Esto es extremadamente útil para encontrar la ecuación de estado:

$$PV = k_B T \ln \Xi$$

### 5.4 Promedios y Fluctuaciones

- Número medio de partículas:
    
    $$\langle N \rangle = -\left( \frac{\partial \Phi_G}{\partial \mu} \right)_{T,V} = k_B T \frac{\partial \ln \Xi}{\partial \mu}$$
    
- **Fluctuaciones:** En el límite termodinámico ($N \to \infty$), las fluctuaciones relativas del número de partículas $\frac{\Delta N}{\langle N \rangle}$ decaen como $1/\sqrt{N}$, lo que demuestra que, para sistemas macroscópicos, las predicciones del ensamble Gran Canónico coinciden con las del Canónico y el Microcanónico.
---

**Capítulo: Fundamentos de la Teoría de Ensamble**

La Mecánica Estadística es el puente formal entre la dinámica microscópica (reversible y determinista o probabilística cuántica) y la termodinámica macroscópica (irreversible y fenomenológica).

---

#  DESCRIPCIÓN ESTADÍSTICA DE UN SISTEMA FÍSICO

En esta unidad establecemos el lenguaje matemático necesario para describir sistemas de $N$ cuerpos donde $N \sim 10^{23}$.

### 2.1 Especificación Microscópica: El Espacio de Fase

El estado dinámico completo de un sistema clásico de $N$ partículas con $f$ grados de libertad se describe mediante un punto en un espacio abstracto de $2f$ dimensiones, conocido como el **Espacio de Fase ($\Gamma$)**.

Sea $q_i$ la coordenada generalizada y $p_i$ el momento conjugado. Un microestado en el instante $t$ está dado por el vector:

$$\mathbf{x}(t) = (q_1, \dots, q_{3N}, p_1, \dots, p_{3N})$$

La evolución temporal del sistema traza una trayectoria de fase gobernada por las ecuaciones canónicas de Hamilton:

$$\dot{q}_k = \frac{\partial \mathcal{H}}{\partial p_k}, \quad \dot{p}_k = - \frac{\partial \mathcal{H}}{\partial q_k}$$

donde $\mathcal{H}(\mathbf{q}, \mathbf{p})$ es el Hamiltoniano del sistema.

Estados Accesibles:

Si el sistema está aislado con energía $E$, el movimiento está restringido a una hipersuperficie de energía constante $\mathcal{H}(\mathbf{q}, \mathbf{p}) = E$. En la práctica, debido a la incertidumbre experimental o cuántica, consideramos una capa de espesor $\delta E$. El volumen de estados accesibles es la región en $\Gamma$ tal que $E \le \mathcal{H} \le E + \delta E$.

> **Nota Cuántica:** En mecánica cuántica, el espacio de fase continuo se reemplaza por un espacio de Hilbert discreto. El microestado es un vector ket $|\psi\rangle$. Debido al principio de incertidumbre de Heisenberg $\Delta q \Delta p \ge h$, existe una correspondencia fundamental: el volumen mínimo de una "celda" en el espacio de fase clásico que corresponde a un estado cuántico es $h^{3N}$.

### 2.2 Descripción Macroscópica y Parámetros

Un **macroestado** se define mediante un conjunto reducido de variables termodinámicas $(N, V, E)$. La descripción estadística asume que realizamos medidas macroscópicas que son promedios de variables microscópicas.

Si $A(\mathbf{q}, \mathbf{p})$ es una propiedad física, su valor macroscópico observado $A_{obs}$ es el promedio temporal:

$$A_{obs} = \lim_{\tau \to \infty} \frac{1}{\tau} \int_0^\tau A(\mathbf{q}(t), \mathbf{p}(t)) \, dt$$

### 2.3 El Concepto de Ensamble Estadístico y la Hipótesis Ergódica

Calcular la trayectoria exacta es imposible. Gibbs introdujo el ensamble: una colección mental infinita de réplicas del sistema, todas en el mismo macroestado, pero distribuidas sobre todos los microestados posibles.

Se define la función de densidad de probabilidad $\rho(\mathbf{q}, \mathbf{p}, t)$, tal que $\rho \, d\Gamma$ es la probabilidad de encontrar una réplica en el elemento de volumen $d\Gamma$.

El promedio de ensamble se define como:

$$\langle A \rangle = \int A(\mathbf{q}, \mathbf{p}) \rho(\mathbf{q}, \mathbf{p}, t) \, d\Gamma$$

Teorema de Liouville:

Para un sistema conservativo, la densidad de puntos en el espacio de fase se comporta como un fluido incompresible. La derivada convectiva es cero:

$$\frac{d\rho}{dt} = \frac{\partial \rho}{\partial t} + \{\rho, \mathcal{H}\} = 0$$

Para sistemas en equilibrio, la distribución debe ser estacionaria ($\partial \rho / \partial t = 0$), lo que implica que $\rho$ debe ser una función explícita solo de las constantes del movimiento (principalmente la Energía, $\mathcal{H}$). Por tanto, $\rho_{eq} = \rho(\mathcal{H})$.

**Hipótesis Ergódica:** Se asume que, para tiempos suficientemente largos, la trayectoria de fase de un sistema pasa arbitrariamente cerca de cualquier punto de la superficie de energía constante. Esto justifica igualar el promedio temporal con el promedio del ensamble: $A_{obs} = \langle A \rangle$.

### 2.4 Conteo de Estados: $\Omega(E)$ y $g(E)$

Para conectar con la termodinámica, debemos "contar" cuántos microestados corresponden a un macroestado.

Definimos $\Phi(E)$ como el volumen del espacio de fase con energía menor a $E$:

$$\Phi(E) = \int_{\mathcal{H}<E} d^{3N}q \, d^{3N}p$$

El número de estados accesibles $\Omega(E)$ en el rango $(E, E+\delta E)$ es:

$$\Omega(E) = \frac{1}{h^{3N}} \frac{\partial \Phi}{\partial E} \delta E$$

La densidad de estados se define como $g(E) \equiv \frac{\partial \Phi}{\partial E} \frac{1}{h^{3N}}$.

---

## UNIDAD 3: ENSAMBLE MICROCANÓNICO

Este es el formalismo fundamental para sistemas **aislados** (Energía $E$, Volumen $V$, Partículas $N$ fijos).

### 3.1 El Postulado de Probabilidades A Priori Iguales

Dada la falta de información sobre el microestado específico de un sistema aislado en equilibrio, el principio de la razón insuficiente (Bayesiano) o la hipótesis ergódica nos llevan al postulado fundamental:

> **Postulado:** Un sistema aislado en equilibrio tiene la misma probabilidad de encontrarse en cualquiera de sus microestados accesibles.

Matemáticamente, la densidad de probabilidad es:

$$\rho(\mathbf{q}, \mathbf{p}) = \begin{cases} \text{cte} & \text{si } E \le \mathcal{H}(\mathbf{q}, \mathbf{p}) \le E + \delta E \\ 0 & \text{en otro caso} \end{cases}$$

La constante de normalización obliga a que $\int \rho d\Gamma = 1$, por lo tanto $\text{cte} = 1/\Omega(E,V,N)$.

### 3.2 Entropía Estadística y Conexión Termodinámica

Boltzmann definió la entropía $S$ no como una cantidad de calor, sino como una medida del "desorden" o multiplicidad de estados:

$$S(E, V, N) = k_B \ln \Omega(E, V, N)$$

Esta definición satisface la propiedad de extensividad. Si tenemos dos subsistemas independientes A y B, $\Omega_{total} = \Omega_A \cdot \Omega_B$, entonces $S_{total} = k_B \ln(\Omega_A \Omega_B) = S_A + S_B$.

Derivación de la Temperatura:

Considere dos sistemas en contacto térmico (intercambian energía) pero aislados del resto del universo ($E_{tot} = E_1 + E_2 = \text{cte}$). El número de estados del sistema combinado es $\Omega_{tot}(E_1) = \Omega_1(E_1)\Omega_2(E_{tot}-E_1)$.

En equilibrio, la configuración más probable es la que maximiza $\Omega_{tot}$ (o su logaritmo, la entropía).

$$\frac{\partial \ln \Omega_{tot}}{\partial E_1} = 0 \implies \frac{\partial \ln \Omega_1}{\partial E_1} + \frac{\partial \ln \Omega_2}{\partial E_2} \frac{\partial E_2}{\partial E_1} = 0$$

Como $dE_2 = -dE_1$, tenemos:

$$\frac{\partial \ln \Omega_1}{\partial E_1} = \frac{\partial \ln \Omega_2}{\partial E_2}$$

Esto define una propiedad intensiva que se iguala en el equilibrio: la temperatura.

$$\beta \equiv \frac{\partial \ln \Omega}{\partial E} = \frac{1}{k_B T} \implies \frac{1}{T} = \left(\frac{\partial S}{\partial E}\right)_{V,N}$$

### 3.3 Aplicaciones

El procedimiento estándar en este ensamble es:

1. Calcular el volumen de fase $\Phi(E)$.
    
2. Obtener $\Omega(E)$ derivando $\Phi$.
    
3. Calcular $S = k_B \ln \Omega$.
    
4. Usar termodinámica: $1/T = (\partial S/\partial E)_V$ y $P/T = (\partial S/\partial V)_E$.
    

---

## UNIDAD 4: ENSAMBLE CANÓNICO

Este ensamble describe un sistema en **contacto térmico** con un reservorio de calor (baño térmico) a temperatura $T$. El sistema intercambia energía, pero su temperatura está fijada por el reservorio.

### 4.1 Derivación de la Distribución de Boltzmann

Sea el sistema de interés $\mathcal{S}$ y el reservorio $\mathcal{R}$. El conjunto $\mathcal{S} + \mathcal{R}$ es microcanónico con energía $E_{tot}$.

La probabilidad $P_i$ de que $\mathcal{S}$ esté en un microestado $i$ con energía $E_i$ es proporcional al número de microestados disponibles para el reservorio $\Omega_R(E_{tot} - E_i)$:

$$P_i \propto \Omega_R(E_{tot} - E_i)$$

Expandimos la entropía del reservorio $S_R = k_B \ln \Omega_R$ en serie de Taylor alrededor de $E_{tot}$, asumiendo $E_i \ll E_{tot}$:

$$k_B \ln \Omega_R(E_{tot} - E_i) \approx S_R(E_{tot}) - E_i \left( \frac{\partial S_R}{\partial E} \right)_{E_{tot}} = S_R(E_{tot}) - \frac{E_i}{T}$$

Tomando la exponencial:

$$\Omega_R(E_{tot} - E_i) \propto e^{S_R(E_{tot})/k_B} \cdot e^{-E_i / k_B T}$$

Dado que el primer término es constante, obtenemos la Distribución Canónica:

$$P_i = \frac{1}{Z} e^{-\beta E_i}$$

### 4.2 La Función de Partición Canónica ($Z$)

La constante de normalización $Z$ (del alemán Zustandssumme, suma sobre estados) es central:

$$Z(T, V, N) = \sum_{microestados \ i} e^{-\beta E_i}$$

Si los niveles de energía son degenerados con multiplicidad $g(E)$, entonces $Z = \sum_E g(E) e^{-\beta E}$.

En el límite clásico continuo:

$$Z_N = \frac{1}{N! h^{3N}} \int e^{-\beta \mathcal{H}(\mathbf{q}, \mathbf{p})} d^{3N}q \, d^{3N}p$$

### 4.3 Potenciales Termodinámicos y Energía Libre de Helmholtz

La conexión con la termodinámica macroscópica se realiza a través de la Energía Libre de Helmholtz, $F$.

Sabemos que la energía interna media es $U = \langle E \rangle = -\frac{\partial \ln Z}{\partial \beta}$.

Se puede demostrar que la entropía en este ensamble es $S = -k_B \sum P_i \ln P_i$. Sustituyendo $P_i$:

$$S = -k_B \sum P_i (-\beta E_i - \ln Z) = \frac{U}{T} + k_B \ln Z$$

Reordenando $U - TS = -k_B T \ln Z$. Como $F = U - TS$, llegamos a la Relación Puente:

$$F(T, V, N) = -k_B T \ln Z(T, V, N)$$

Esta ecuación es la "receta" fundamental: calcule $Z$, tome el logaritmo, y obtenga todas las propiedades termodinámicas derivando $F$.

### 4.4 Paradoja de Gibbs e Indistinguibilidad

Al calcular $Z$ para un gas ideal clásico, si tratamos las partículas como distinguibles, la entropía resultante no es extensiva (no se duplica al duplicar el sistema), lo cual es físicamente incorrecto (Paradoja de Gibbs).

La resolución es cuántica: las partículas idénticas son indistinguibles. No existe diferencia física entre el estado "partícula A en $x_1$, B en $x_2$" y "partícula B en $x_1$, A en $x_2$".

Por tanto, debemos dividir el volumen del espacio de fase por el número de permutaciones posibles ($N!$). El factor $1/N!$ en la definición de $Z$ clásico corrige la entropía y la hace extensiva (Fórmula de Sackur-Tetrode).

### 4.5 Teorema de Equipartición Generalizado

Sea $x_i$ una coordenada o momento que aparece en el Hamiltoniano como un término cuadrático $\alpha x_i^2$.

$$\langle \alpha x_i^2 \rangle = \frac{\int \alpha x_i^2 e^{-\beta \alpha x_i^2} dx_i \prod_{j \ne i} \int e^{-\beta H_j} dx_j}{\int e^{-\beta \alpha x_i^2} dx_i \prod_{j \ne i} \int e^{-\beta H_j} dx_j} = \frac{1}{2\beta} = \frac{1}{2} k_B T$$

Cada término cuadrático independiente en el Hamiltoniano contribuye con $k_B T / 2$ a la energía interna media.

---

## UNIDAD 5: ENSAMBLE GRAN CANÓNICO

Este ensamble generaliza el caso anterior para sistemas **abiertos** que pueden intercambiar tanto energía como partículas con un reservorio. El reservorio fija la temperatura $T$ y el potencial químico $\mu$.

### 5.1 Probabilidad Gran Canónica

Consideramos un sistema con $N$ variable y energía $E$. El reservorio impone las condiciones de conservación: $E_{tot} = E + E_R$ y $N_{tot} = N + N_R$.

La probabilidad $P(N, E_i)$ es proporcional a $\Omega_R(E_{tot}-E_i, N_{tot}-N)$. Expandiendo la entropía del reservorio en dos variables:

$$S_R \approx S_{R,0} - E_i \left( \frac{\partial S_R}{\partial E} \right) - N \left( \frac{\partial S_R}{\partial N} \right)$$

Usando las definiciones termodinámicas $\beta = 1/k_B T$ y $\mu = -T (\partial S / \partial N)$, obtenemos:

$$P(N, E_i) = \frac{1}{\Xi} e^{-\beta (E_i - \mu N)}$$

### 5.2 La Función de Gran Partición ($\Xi$)

La normalización requiere sumar sobre todos los números de partículas posibles ($0 \to \infty$) y todos los microestados energéticos para cada $N$:

$$\Xi(T, V, \mu) = \sum_{N=0}^{\infty} \sum_{i} e^{-\beta E_{i,N}} e^{\beta \mu N}$$

Introduciendo la fugacidad $z = e^{\beta \mu}$, podemos escribir $\Xi$ como una serie de potencias de las funciones de partición canónicas $Z_N$:

$$\Xi(T, V, \mu) = \sum_{N=0}^{\infty} z^N Z_N(T, V)$$

Esta estructura matemática convierte a la función de gran partición en la función generatriz de los ensambles canónicos.

### 5.3 El Gran Potencial ($\Omega_G$)

El potencial termodinámico asociado se obtiene análogamente a la energía libre:

$$\Omega_G(T, V, \mu) = -k_B T \ln \Xi$$

Desde la termodinámica, el gran potencial se define como la transformada de Legendre de la energía interna respecto a la entropía y el número de partículas:

$$\Omega_G = U - TS - \mu N$$

Para un sistema grande homogéneo, la relación de Euler nos dice que $U = TS - PV + \mu N$, por lo tanto:

$$\Omega_G = -PV$$

Esto ofrece una vía directa para encontrar la Ecuación de Estado:

$$\frac{PV}{k_B T} = \ln \Xi$$

### 5.4 Fluctuaciones y Equivalencia de Ensambles

Una pregunta crucial es: ¿Da el ensamble Gran Canónico (donde $N$ fluctúa) los mismos resultados que el Canónico (donde $N$ es fijo)?

Calculamos la varianza del número de partículas $\sigma_N^2 = \langle N^2 \rangle - \langle N \rangle^2$:

$$\langle N \rangle = \frac{1}{\beta} \frac{\partial \ln \Xi}{\partial \mu}, \quad \sigma_N^2 = \frac{1}{\beta^2} \frac{\partial^2 \ln \Xi}{\partial \mu^2} = k_B T \frac{\partial \langle N \rangle}{\partial \mu}$$

La fluctuación relativa es:

$$\frac{\sqrt{\langle (\Delta N)^2 \rangle}}{\langle N \rangle} \sim \frac{1}{\sqrt{\langle N \rangle}}$$

--- 

Para un sistema macroscópico donde $\langle N \rangle \sim 10^{23}$, las fluctuaciones son despreciables ($\sim 10^{-11.5}$). Las distribuciones de probabilidad se vuelven funciones delta de Dirac extremadamente afiladas. Esto demuestra la equivalencia de los ensambles en el límite termodinámico: no importa si fijamos $N$ o $\mu$, o $E$ o $T$; los valores medios de las propiedades intensivas convergen al mismo resultado
# ejercicios

---

## UNIDAD 2:

1. Caminata Aleatoria (Random Walk) 1D

Un borracho da $N$ pasos de longitud $l$ en una dimensión. Cada paso tiene probabilidad $p=1/2$ de ser a la derecha y $q=1/2$ a la izquierda.

- a) ¿Cuál es el desplazamiento medio $\langle x \rangle$?
    
- b) ¿Cuál es el desplazamiento cuadrático medio $\langle x^2 \rangle$?
    
- Solución:
    
    Sea $n_1$ pasos a la derecha y $n_2$ a la izquierda. $N = n_1 + n_2$. El desplazamiento es $x = (n_1 - n_2)l$.
    
    a) $\langle x \rangle = \langle n_1 - n_2 \rangle l = (\langle n_1 \rangle - \langle n_2 \rangle)l$. Como $p=q=1/2$, $\langle n_1 \rangle = N/2$. Por tanto, $\langle x \rangle = 0$.
    
    b) $x^2 = (\sum_{i=1}^N s_i)^2 = \sum s_i^2 + \sum_{i \neq j} s_i s_j$. Como $s_i = \pm l$, $s_i^2 = l^2$. Los términos cruzados promedian a cero (no hay correlación).
    
    $\langle x^2 \rangle = \sum_{i=1}^N \langle s_i^2 \rangle = N l^2$.
    
    Resultado: La dispersión crece como $\sqrt{N}$.
    

2. Volumen en el Espacio de Fase del Oscilador Armónico

Considere un oscilador armónico 1D con energía $E = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 q^2$.

Calcule el volumen del espacio de fase $\Gamma(E)$ accesible para energías menores a $E$.

- Solución:
    
    La ecuación $ \frac{p^2}{2mE} + \frac{q^2}{2E/(m\omega^2)} = 1$ describe una elipse con semiejes $a = \sqrt{2mE}$ y $b = \sqrt{2E/m\omega^2}$.
    
    El área de la elipse es $A = \pi a b = \pi \sqrt{2mE} \sqrt{\frac{2E}{m\omega^2}} = \frac{2\pi E}{\omega}$.
    
    $\Gamma(E) = \frac{2\pi E}{\omega}$. (En unidades de $h$, el número de estados es $E/\hbar\omega$).
    

3. Densidad de estados de una partícula libre en 3D

Calcule la densidad de estados $g(E)$ para una partícula libre en una caja de volumen $V$.

- Solución:
    
    El número de estados es el volumen de una esfera en el espacio de momentos (octante positivo) dividido por el volumen de celda unitaria.
    
    $\Omega(p) = \frac{1}{8} \frac{4}{3}\pi p^3 / (\frac{h}{2L})^3 = \frac{4\pi V p^3}{3h^3}$.
    
    Usando $E = p^2/2m \Rightarrow p = \sqrt{2mE}$, tenemos $\Omega(E) \propto E^{3/2}$.
    
    $g(E) = \frac{d\Omega}{dE} \propto E^{1/2}$.
    
    Respuesta: $g(E) = \frac{2\pi V}{h^3} (2m)^{3/2} E^{1/2}$.
    

4. Aproximación de Stirling

Demuestre que $\ln N! \approx N \ln N - N$ para $N$ grande.

- Solución:
    
    $\ln N! = \sum_{x=1}^N \ln x \approx \int_1^N \ln x \, dx = [x \ln x - x]_1^N = N \ln N - N + 1 \approx N \ln N - N$.
    

5. Espín en Campo Magnético (Microscópico)

Un sistema de $N$ espines $1/2$ está en un campo $B$. Momento magnético $\mu$.

Escriba la energía total en función del número de espines "arriba" ($n_+$).

- Solución:
    
    $E = - \mu B (n_+ - n_-)$. Con $N = n_+ + n_-$, $n_- = N - n_+$.
    
    $E = -\mu B (2n_+ - N)$.
    

---

## UNIDAD 3: ENSAMBLE MICROCANÓNICO

6. Sistema de Dos Niveles (El "Schottky" Microcanónico)

Considere $N$ partículas distinguibles con dos niveles de energía: $0$ y $\epsilon$. La energía total es $E = M\epsilon$ (donde $M$ es entero).

- a) Calcule la entropía $S(E)$.
    
- b) Calcule la temperatura $T$.
    
- Solución:
    
    a) Hay que elegir $M$ partículas para estar en el nivel excitado de un total de $N$.
    
    $\Omega = \frac{N!}{M!(N-M)!}$.
    
    $S = k_B \ln \Omega \approx k_B [N \ln N - M \ln M - (N-M)\ln(N-M)]$.
    
    b) $1/T = (\partial S / \partial E)$. Como $E = M\epsilon$, $\partial E = \epsilon \partial M$.
    
    $\frac{1}{T} = \frac{1}{\epsilon} \frac{\partial S}{\partial M} = \frac{k_B}{\epsilon} \ln \left( \frac{N-M}{M} \right)$.
    
    Despejando: $M = \frac{N}{e^{\epsilon/k_B T} + 1}$ (Distribución de Fermi-Dirac/Planck clásica).
    

7. Temperatura Negativa

Usando el ejercicio 6, ¿qué sucede si $E > N\epsilon / 2$?

- Solución:
    
    Si $M > N/2$, el argumento del logaritmo $\frac{N-M}{M}$ es menor que 1. El logaritmo es negativo.
    
    Por lo tanto, $T < 0$. Esto ocurre porque al agregar energía, el número de microestados disminuye (nos acercamos al estado donde todos están excitados, que es único).
    

8. Gas Ideal Clásico (Sackur-Tetrode)

Derive la entropía de un gas ideal monoatómico usando el conteo de estados en el espacio de fase.

- Solución:
    
    $\Omega(E,V,N) = \frac{1}{N! h^{3N}} \int d^{3N}q \int_{H \le E} d^{3N}p$.
    
    La integral espacial da $V^N$. La integral de momento es el volumen de una hiperesfera $3N$-dimensional de radio $R = \sqrt{2mE}$.
    
    Volumen esfera $\approx \frac{(2\pi)^{3N/2}}{(3N/2)!} R^{3N}$.
    
    Tomando el $\ln$ y usando Stirling:
    
    $S = Nk_B \left[ \ln \left( \frac{V}{N} \left( \frac{4\pi m E}{3Nh^2} \right)^{3/2} \right) + \frac{5}{2} \right]$. (Ecuación de Sackur-Tetrode).
    

9. Ecuación de Estado del Gas Ideal

A partir de la ecuación de Sackur-Tetrode (Ej. 8), calcule la presión.

- Solución:
    
    $P = T (\partial S / \partial V)_{E,N}$.
    
    En la expresión de $S$, el único término con $V$ es $Nk_B \ln V$.
    
    $P = T \frac{\partial}{\partial V} (N k_B \ln V) = \frac{N k_B T}{V} \Rightarrow PV = N k_B T$.
    

10. Equilibrio Térmico

Dos sistemas A y B con $\Omega_A(E_A) \propto E_A^n$ y $\Omega_B(E_B) \propto E_B^m$ están en contacto. $E_{tot} = E_A + E_B$ fijo. Encuentre la energía de equilibrio $\bar{E}_A$.

- Solución:
    
    Maximizar $\Omega_{tot} = \Omega_A(E_A) \Omega_B(E_{tot}-E_A)$.
    
    $\frac{d}{dE_A} (E_A^n (E_{tot}-E_A)^m) = 0$.
    
    $n E_A^{n-1}(E_{tot}-E_A)^m - m E_A^n (E_{tot}-E_A)^{m-1} = 0$.
    
    Dividiendo por el factor común: $n(E_{tot}-E_A) - m E_A = 0 \Rightarrow n E_{tot} = (n+m)E_A$.
    
    $\bar{E}_A = \frac{n}{n+m} E_{tot}$. (Reparto proporcional a los grados de libertad).
    

11. Defectos de Frenkel

Un cristal tiene $N$ átomos y $N'$ sitios intersticiales ($N' \approx N$). Se requiere energía $\epsilon$ para mover un átomo a un intersticio. Calcule el número de defectos $n$ en equilibrio.

- Solución:
    
    Hay $\binom{N}{n}$ formas de elegir los átomos a mover y $\binom{N'}{n}$ formas de colocarlos.
    
    $\Omega = \frac{N!}{n!(N-n)!} \frac{N'!}{n!(N'-n)!}$.
    
    Maximizar $\ln \Omega - \beta E$ con $E = n\epsilon$.
    
    Resultado aproximado para $n \ll N$: $n \approx \sqrt{NN'} e^{-\epsilon / 2k_B T}$.
    

12. Osciladores Cuánticos (Einstein Solid)

$N$ osciladores armónicos 1D con energía total $E = q \hbar \omega$. Calcule la multiplicidad.

- Solución:
    
    Problema de poner $q$ cuantos de energía en $N$ cajas.
    
    $\Omega = \binom{q+N-1}{q}$.
    

---

## UNIDAD 4: ENSAMBLE CANÓNICO

13. Oscilador Armónico Clásico

Calcule $Z$, $F$, $U$ y $C_v$ para un oscilador armónico 1D clásico.

- Solución:
    
    $H = p^2/2m + kx^2/2$.
    
    $Z_1 = \frac{1}{h} \int_{-\infty}^{\infty} e^{-\beta p^2/2m} dp \int_{-\infty}^{\infty} e^{-\beta kx^2/2} dx$.
    
    Son integrales gaussianas ($\int e^{-ax^2} = \sqrt{\pi/a}$).
    
    $Z_1 = \frac{1}{h} \sqrt{\frac{2\pi m}{\beta}} \sqrt{\frac{2\pi}{\beta k}} = \frac{2\pi}{h\beta} \sqrt{\frac{m}{k}} = \frac{1}{\beta \hbar \omega}$. (donde $\omega = \sqrt{k/m}$).
    
    $Z_1 = \frac{k_B T}{\hbar \omega}$.
    
    $U = -\partial \ln Z / \partial \beta = k_B T$.
    
    $C_v = k_B$.
    

14. Paramagnetismo (Espines Independientes)

$N$ espines $1/2$ en campo $B$. $E = \pm \mu B$. Calcule la magnetización media $M$.

- Solución:
    
    Función de partición de una partícula: $Z_1 = e^{\beta \mu B} + e^{-\beta \mu B} = 2 \cosh(\beta \mu B)$.
    
    $Z_N = (Z_1)^N$.
    
    Energía libre $F = -N k_B T \ln(2 \cosh(x))$ con $x = \beta \mu B$.
    
    Magnetización $M = - (\partial F / \partial B)_T = N k_B T \frac{1}{Z_1} (2 \sinh(x)) \beta \mu$.
    
    $M = N \mu \tanh(\frac{\mu B}{k_B T})$.
    

15. Fluctuaciones de Energía

Demuestre que $\langle (\Delta E)^2 \rangle = k_B T^2 C_v$.

- Solución:
    
    $\langle E \rangle = -\frac{\partial \ln Z}{\partial \beta} = -\frac{1}{Z} \frac{\partial Z}{\partial \beta}$.
    
    $\frac{\partial^2 \ln Z}{\partial \beta^2} = \frac{\partial}{\partial \beta} \left( -\frac{1}{Z} \frac{\partial Z}{\partial \beta} \right) = \frac{1}{Z^2} (\frac{\partial Z}{\partial \beta})^2 - \frac{1}{Z} \frac{\partial^2 Z}{\partial \beta^2} = \langle E \rangle^2 - \langle E^2 \rangle$.
    
    Por otro lado, $\frac{\partial \langle E \rangle}{\partial \beta} = \frac{\partial \langle E \rangle}{\partial T} \frac{\partial T}{\partial \beta} = C_v (-k_B T^2)$.
    
    Igualando: $-\langle (\Delta E)^2 \rangle = - k_B T^2 C_v$. QED.
    

16. Gas Ideal Diatómico (Rotores)

Modelo de rotor rígido con momento de inercia $I$. Calcule la contribución rotacional a $C_v$ a altas temperaturas.

- Solución:
    
    Niveles: $E_j = \frac{\hbar^2}{2I} j(j+1)$ con degeneración $g_j = 2j+1$.
    
    $Z_{rot} = \sum (2j+1) e^{-\beta E_j} \approx \int_0^\infty (2j+1) e^{-\frac{\beta \hbar^2}{2I} j(j+1)} dj$.
    
    Cambio de variable $u = j(j+1) \Rightarrow du = (2j+1)dj$.
    
    $Z_{rot} \approx \int e^{-\theta u} du \propto T$.
    
    $\ln Z \sim \ln T \Rightarrow U \sim k_B T \Rightarrow C_v = k_B$ (por molécula, o $R$ por mol).
    
    Total gas diatómico $C_v = \frac{3}{2}R (trasl) + R (rot) = \frac{5}{2}R$.
    

17. Paradoja de Gibbs (Teórico)

Calcule $S$ para dos gases ideales distintos que se mezclan vs dos gases idénticos.

- Solución:
    
    Si son distintos, $Z = Z_A Z_B$. La entropía aumenta en $2N k_B \ln 2$ (entropía de mezcla).
    
    Si son idénticos, debemos dividir por $(2N)!$ en lugar de $N!N!$, eliminando el término de mezcla. Esto justifica el factor $1/N!$ en el ensamble canónico.
    

18. Sistema de 3 Niveles

Niveles $-\epsilon, 0, +\epsilon$. Calcule la capacidad calorífica.

- Solución:
    
    $Z_1 = e^{\beta \epsilon} + 1 + e^{-\beta \epsilon} = 1 + 2\cosh(\beta \epsilon)$.
    
    $U = - N \frac{\partial}{\partial \beta} \ln(1 + 2\cosh(\beta \epsilon)) = -N \frac{2\epsilon \sinh(\beta \epsilon)}{1 + 2\cosh(\beta \epsilon)}$.
    
    Derivar respecto a $T$ para obtener $C_v$.
    

19. Gas en Campo Gravitacional (Ley del Barómetro)

Gas ideal en una columna de altura $H$ y área $A$. Potencial $V(z) = mgz$. Calcule la densidad $\rho(z)$.

- Solución:
    
    La probabilidad de estar a altura $z$ es $P(z) \propto e^{-\beta mgz}$.
    
    $\rho(z) = \rho(0) e^{-mgz / k_B T}$.
    

20. Teorema de Equipartición Generalizado

Si $H = A x^n$, ¿cuánto vale $\langle H \rangle$?

- Solución:
    
    $\langle x^n \rangle = \frac{\int x^n e^{-\beta A x^n} dx}{\int e^{-\beta A x^n} dx}$.
    
    Haciendo cambio de variable $y = \beta A x^n$, se demuestra que $\langle H \rangle = \frac{1}{n} k_B T$.
    
    Para oscilador armónico ($n=2$), da $\frac{1}{2}k_B T$.
    

21. Gas Ultra-Relativista

Gas ideal con relación de dispersión $E = pc$ (fotones o partículas extremas).

- Solución:
    
    Integrar $e^{-\beta pc} 4\pi p^2 dp$.
    
    Resultado: $PV = \frac{1}{3} U$ (en contraste con $2/3 U$ para gas no relativista).
    

22. Impurezas en un Sólido

Un sólido tiene $N$ sitios. Energía 0 si está vacío, energía $\epsilon$ si tiene una impureza.

- Solución:
    
    Es equivalente a un sistema de dos niveles. $Z = (1 + e^{-\beta \epsilon})^N$.
    
    Número medio de impurezas $\langle n \rangle = \frac{N}{e^{\beta \epsilon} + 1}$.
    

---

## UNIDAD 5: ENSAMBLE GRAN CANÓNICO

23. Adsorción de Langmuir (Ejercicio Clásico)

Una superficie tiene $M$ sitios. Cada sitio puede adsorber 0 o 1 partícula del gas (reservorio $\mu, T$). Energía de adsorción $-\epsilon_0$.

Calcule la fracción de sitios ocupados $\theta$.

- Solución:
    
    Función de partición para un sitio:
    
    Estado 0: $N=0, E=0 \Rightarrow \text{factor } 1$.
    
    Estado 1: $N=1, E=-\epsilon_0 \Rightarrow \text{factor } e^{-\beta(-\epsilon_0)} e^{\beta \mu} = e^{\beta(\epsilon_0 + \mu)}$.
    
    $\Xi_1 = 1 + e^{\beta(\epsilon_0 + \mu)}$.
    
    Número medio de partículas por sitio $\langle n \rangle = \frac{\partial \ln \Xi_1}{\partial (\beta \mu)} = \frac{e^{\beta(\epsilon_0+\mu)}}{1 + e^{\beta(\epsilon_0+\mu)}} = \frac{1}{e^{-\beta(\epsilon_0+\mu)} + 1}$.
    
    Esta es la isoterma de Langmuir: $\theta = \frac{P}{P + P_0(T)}$.
    

24. Gas Ideal en Gran Canónico

Calcule $\Xi$ y demuestre $PV = k_B T \ln \Xi$.

- Solución:
    
    $\Xi = \sum_{N=0}^\infty z^N Z_N$. Para gas ideal, $Z_N = \frac{(Z_1)^N}{N!}$.
    
    $\Xi = \sum \frac{(z Z_1)^N}{N!} = \exp(z Z_1)$.
    
    El Gran Potencial $\Omega_G = -k_B T \ln \Xi = -k_B T z Z_1$.
    
    Como $\Omega_G = -PV$, entonces $PV = k_B T z Z_1$.
    
    Como $\langle N \rangle = z \frac{\partial}{\partial z} \ln \Xi = z Z_1$, recuperamos $PV = \langle N \rangle k_B T$.
    

25. Fluctuaciones del Número de Partículas

Demuestre que $\frac{\Delta N}{N} \sim \frac{1}{\sqrt{N}}$.

- Solución:
    
    $\langle N \rangle = k_B T \frac{\partial \ln \Xi}{\partial \mu}$.
    
    $\langle (\Delta N)^2 \rangle = (k_B T)^2 \frac{\partial^2 \ln \Xi}{\partial \mu^2} = k_B T \frac{\partial \langle N \rangle}{\partial \mu}$.
    
    Usando termodinámica, $\frac{\partial N}{\partial \mu} \propto N \kappa_T$ (compresibilidad).
    
    Entonces $\langle (\Delta N)^2 \rangle \propto N$.
    
    $\frac{\sqrt{\langle (\Delta N)^2 \rangle}}{\langle N \rangle} = \frac{\sqrt{N}}{N} = \frac{1}{\sqrt{N}}$.
    

26. Estadística de Fermi-Dirac (Derivación)

Considere un solo estado cuántico de energía $\epsilon$ que puede tener 0 o 1 fermión.

- Solución:
    
    $\Xi = 1 + e^{-\beta(\epsilon - \mu)}$.
    
    $\langle n \rangle = \frac{0 \cdot 1 + 1 \cdot e^{-\beta(\epsilon - \mu)}}{\Xi} = \frac{1}{e^{\beta(\epsilon - \mu)} + 1}$.
    

27. Estadística de Bose-Einstein (Derivación)

Considere un estado cuántico de energía $\epsilon$ que puede tener $n = 0, 1, 2... \infty$ bosones.

- Solución:
    
    Suma geométrica: $\Xi = \sum_{n=0}^\infty (e^{-\beta(\epsilon - \mu)})^n = \frac{1}{1 - e^{-\beta(\epsilon - \mu)}}$.
    
    $\langle n \rangle = - \frac{\partial \Omega_G}{\partial \mu} = \frac{1}{e^{\beta(\epsilon - \mu)} - 1}$.
    

28. Condensación de Bose-Einstein (Cualitativo)

A partir del Ej. 27, ¿qué pasa si $\mu \to \epsilon_{ground}$?

- Solución:
    
    El denominador se hace cero y la ocupación $\langle n \rangle$ diverge. Esto indica una transición de fase donde un número macroscópico de partículas ocupa el estado base.
    

29. Reacción Química

Considerar la reacción $A \rightleftharpoons B$. Condición de equilibrio.

- Solución:
    
    En el gran canónico, el equilibrio se alcanza cuando los potenciales químicos se igualan: $\mu_A = \mu_B$.
    
    Esto deriva la ley de acción de masas usando las funciones de partición interna $z_A, z_B$: $\frac{N_A}{N_B} = \frac{Z_A}{Z_B} e^{-\beta \Delta E}$.
    

30. Modelo de ADN (Zipper Model)

Una cadena de ADN tiene $N$ eslabones. Cada uno puede estar cerrado (energía 0) o abierto (energía $\epsilon$). Si un eslabón se abre, todos los anteriores deben estar abiertos (efecto cremallera).

- Solución:
    
    Este problema se suele resolver con la suma gran canónica simplificada o canónica.
    
    Los estados son: todo cerrado, 1 abierto, 2 abiertos... $N$ abiertos.
    
    $Z = 1 + e^{-\beta \epsilon} + e^{-2\beta \epsilon} + ... + e^{-N\beta \epsilon}$.
    
    Es una serie geométrica. Permite calcular la temperatura de desnaturalización del ADN.