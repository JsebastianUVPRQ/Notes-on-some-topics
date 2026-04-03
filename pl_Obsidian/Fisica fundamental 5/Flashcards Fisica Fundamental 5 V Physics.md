#flashcards/fisica/mecanica_avanzada

Condición simpléctica de la Matriz Jacobiana (Conservación de volumen)
?
$$M^T J M = J$$
Donde $J = \begin{pmatrix} 0 & I \\ -I & 0 \end{pmatrix}$. Esto implica la conservación del volumen en el espacio de fase (Teorema de Liouville).


Variable de Acción ($J_i$) en sistemas periódicos
?
$$J_i = \oint_{C_i} p_i \, dq_i$$
La integral se realiza sobre un ciclo cerrado topológicamente independiente en el toro invariante del espacio de fase.


Frecuencia del movimiento ($\omega_i$) en variables de Acción-Ángulo
?
$$\omega_i(J) = \frac{\partial H(J)}{\partial J_i}$$
En sistemas integrables, las frecuencias son constantes de movimiento y dependen solo de las acciones.


Paréntesis de Poisson Fundamental (Álgebra de Lie clásica)
?
$$\{q_i, p_j\} = \delta_{ij}, \quad \{q_i, q_j\} = 0, \quad \{p_i, p_j\} = 0$$
Cualquier transformación que deje invariantes estos corchetes es una transformación canónica.


Ecuación de Liouville (Evolución de la densidad de probabilidad)
?
$$\frac{\partial \rho}{\partial t} = -\{\rho, H\} = -\sum_{i=1}^{N} \left( \frac{\partial \rho}{\partial q_i} \frac{\partial H}{\partial p_i} - \frac{\partial \rho}{\partial p_i} \frac{\partial H}{\partial q_i} \right)$$
Describe el flujo de un fluido incompresible en el espacio de fase.


Exponente de Lyapunov Máximo ($\lambda$)
?
$$|\delta Z(t)| \approx e^{\lambda t} |\delta Z_0|$$
Límite formal que caracteriza la sensibilidad a las condiciones iniciales (caos).


Teorema de Recurrencia de Poincaré
?
Para cualquier vecindad $U$ en el espacio de fase acotado y conservativo, existe una trayectoria que parte de $U$ y eventualmente retorna a $U$ tras un tiempo $T_R$ suficientemente largo.


Teorema del Virial (Mecánica Cuántica)
?
$$2\langle T \rangle = n \langle V \rangle$$
Relación para potenciales de la forma $V(r) \propto r^n$.
Para O.A. ($n=2$): $\langle T \rangle = \langle V \rangle$.
Para Átomo H ($n=-1$): $2\langle T \rangle = -\langle V \rangle$.


Transformada de Legendre (Lagrangiano a Hamiltoniano)
?
$$H(q, p) = \sum \dot{q}_i p_i - L(q, \dot{q})$$
Maximiza la diferencia para cambiar de variables $(q, \dot{q})$ a $(q, p)$.


#flashcards/fisica/quantum_computing

Quantum Feature Map ($\Phi$)
?
$$\Phi: \mathcal{X} \to \mathcal{H}, \quad \mathbf{x} \mapsto |\Phi(\mathbf{x})\rangle = U_{\Phi}(\mathbf{x})|0\rangle^{\otimes n}$$
Mapeo de un dato clásico a un estado cuántico mediante un circuito unitario parametrizado.


Kernel Cuántico (Fidelidad)
?
$$K(\mathbf{x}_i, \mathbf{x}_j) = |\langle \Phi(\mathbf{x}_i) | \Phi(\mathbf{x}_j) \rangle|^2 = |\langle 0| U_{\Phi}^\dagger(\mathbf{x}_i) U_{\Phi}(\mathbf{x}_j) |0\rangle|^2$$
Representa el producto interno en el espacio de características de alta dimensión.


Hamiltonian Encoding (Operador de Evolución)
?
$$U(x) = e^{-i H(x) t}$$
Generalmente $H(x) = \sum_k f_k(x) P_k$, donde $P_k$ son productos tensoriales de operadores de Pauli.


Teorema de Representación (Representer Theorem) en QSVM
?
$$f(x) = \sum_{i=1}^{M} \alpha_i K(x_i, x) + b$$
La solución óptima vive en el subespacio generado por los kernels de los datos de entrenamiento.


Teorema de No-Clonación
?
Es imposible copiar un estado cuántico arbitrario debido a la linealidad de la Mecánica Cuántica.
Si $U|\psi\rangle|0\rangle = |\psi\rangle|\psi\rangle$, la linealidad falla para superposiciones $|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$.


Compuerta Hadamard ($H$) y su matriz
?
Transforma la base computacional a la base $X$:
$H|0\rangle = |+\rangle$, $H|1\rangle = |-\rangle$.
Matriz: $\frac{1}{\sqrt{2}}\begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}$


Estado de Bell $|\Phi^+\rangle$
?
$$|\Phi^+\rangle = \frac{|00\rangle + |11\rangle}{\sqrt{2}}$$
Estado máximamente entrelazado generado por $H$ seguido de CNOT.


Criterio de Pureza (Matriz de Densidad)
?
**Puro:** $\text{Tr}(\rho^2) = 1$ (es un proyector).
**Mixto:** $\text{Tr}(\rho^2) < 1$.


Descomposición de Schmidt
?
Cualquier estado puro bipartito se puede escribir como:
$|\psi\rangle_{AB} = \sum_i \lambda_i |i_A\rangle \otimes |i_B\rangle$.
Si hay más de un $\lambda_i \neq 0$, hay entrelazamiento.


Formalismo de Estabilizadores (Stabilizers)
?
Un código se define por un grupo de operadores de Pauli $S$. El espacio de código cumple:
$$M |\psi\rangle = +|\psi\rangle \quad \forall M \in S$$
Fundamental para corrección de errores (QEC).


Entropía de Von Neumann
?
$$S(\rho) = -\text{Tr}(\rho \ln \rho)$$
Mide la información o el entrelazamiento (si es entropía reducida). Para estados puros es 0.


Fidelidad (Fidelity) entre estados mixtos
?
$$F(\rho, \sigma) = \left( \text{Tr} \sqrt{\sqrt{\rho} \sigma \sqrt{\rho}} \right)^2$$
Medida de cercanía entre dos estados cuánticos.


#flashcards/fisica/cuantica_teorica

Unitaridad y Conservación de Probabilidad
?
$$U^\dagger U = I$$
Garantiza que la norma del vector de estado se conserve ($\langle \psi|\psi \rangle = 1$) durante la evolución temporal.


El "Menos Primer" Principio (Susskind)
?
La información nunca se pierde; la evolución es reversible (unitaridad asegura que estados ortogonales sigan siéndolo).


Medición como Operador de Proyección ($P_n$)
?
$$|\psi\rangle \to \frac{P_n |\psi\rangle}{\sqrt{\langle \psi | P_n | \psi \rangle}}$$
Donde $P_n = |n\rangle\langle n|$ proyecta al autoespacio del valor medido.


Principio de Incertidumbre Generalizado (Conmutador)
?
$$\sigma_A \sigma_B \ge \frac{1}{2} |\langle [A, B] \rangle|$$
Si $[A, B] \neq 0$, no son simultáneamente diagonalizables.


Imagen de Heisenberg (Ecuación de movimiento)
?
$$\frac{dA_H}{dt} = \frac{1}{i\hbar} [A_H, H] + \left(\frac{\partial A}{\partial t}\right)_H$$
Los operadores evolucionan en el tiempo, la función de onda es estática.


Serie de Dyson (Evolución temporal)
?
$$U(t, t_0) = \mathcal{T} \exp\left( -\frac{i}{\hbar} \int_{t_0}^t H(t') dt' \right)$$
Expansión perturbativa con ordenamiento temporal $\mathcal{T}$ para Hamiltonianos dependientes del tiempo.


Teorema de Wigner-Eckart
?
$$\langle \alpha, j, m | T^{(k)}_q | \alpha', j', m' \rangle = \langle j k; m q | j k; j' m' \rangle \frac{\langle \alpha j || T^{(k)} || \alpha' j' \rangle}{\sqrt{2j+1}}$$
Separa la geometría (Coef. Clebsch-Gordan) de la dinámica (Elemento de matriz reducido).


Aproximación WKB (Función de onda)
?
$$\psi(x) \approx \frac{1}{\sqrt{p(x)}} e^{\pm \frac{i}{\hbar} \int p(x') dx'}$$
Válida en regiones clásicamente permitidas donde el potencial varía lentamente.


Fase de Berry (Geométrica)
?
$$\gamma_n = i \oint \langle n(\mathbf{R}) | \nabla_{\mathbf{R}} | n(\mathbf{R}) \rangle \cdot d\mathbf{R}$$
Fase adquirida por transporte adiabático en un camino cerrado en el espacio de parámetros.


Regla de Oro de Fermi
?
$$W_{i \to f} = \frac{2\pi}{\hbar} |\langle f | V | i \rangle|^2 \rho(E_f)$$
Probabilidad de transición por unidad de tiempo bajo perturbación constante.


Ecuación de Liouville-von Neumann
?
$$\frac{d\rho}{dt} = -\frac{i}{\hbar} [H, \rho]$$
Evolución temporal para estados mixtos.


#flashcards/fisica/matematicas_y_filtros

Generadores de SU(2) y Conmutación
?
Las Matrices de Pauli ($\sigma_i$).
$[ \frac{\sigma_i}{2}, \frac{\sigma_j}{2} ] = i \epsilon_{ijk} \frac{\sigma_k}{2}$. Base del espín y el isospín.


Teorema Espectral
?
Todo operador Hermítico en dimensión finita tiene una base ortonormal completa de vectores propios con valores propios reales.


Notación de Einstein ($A_\mu B^\mu$)
?
Suma sobre índices repetidos: $\sum_{\mu=0}^{3} A_\mu B^\mu$. Implica invariancia Lorentz si se contrae un índice covariante con uno contravariante.


Constantes de Estructura ($f_{ijk}$)
?
Definen el álgebra de Lie: $[T_i, T_j] = i \sum_k f_{ijk} T_k$.


Lema de Schur
?
Si un operador conmuta con todas las matrices de una representación irreducible, ese operador es múltiplo de la identidad.


Teorema de los Residuos
?
$$\oint_C f(z) dz = 2\pi i \sum \text{Res}(f, a_k)$$
Fundamental para calcular integrales en QFT y funciones de Green.


Función de Green ($G$)
?
$$L G(x, x') = \delta(x - x')$$
Respuesta impulso de un operador diferencial lineal.


Teorema de Ehrenfest (Límite Clásico)
?
$$\frac{d}{dt}\langle p \rangle = \langle -\nabla V(x) \rangle$$
Recupera la ley de Newton para valores esperados (exacto solo si $V$ es lineal o cuadrático).


Energía del Punto Cero (Oscilador Armónico)
?
$E_{min} = \hbar\omega/2$.
No puede ser cero porque violaría el Principio de Incertidumbre ($x=0, p=0$ no es posible).


Teoría de Perturbaciones (Corrección 1er Orden Energía)
?
$$E_n^{(1)} = \langle \psi_n^{(0)} | V | \psi_n^{(0)} \rangle$$
Valor esperado de la perturbación en el estado original.

El Principio Variacional
?
$$E_0 \le \frac{\langle \psi | H | \psi \rangle}{\langle \psi | \psi \rangle}$$
Cualquier función de prueba da una cota superior a la energía del estado base.


Propagador de Feynman $K(x,t; x',t')$
?
Amplitud de probabilidad de que una partícula vaya de $(x',t')$ a $(x,t)$. Suma sobre todos los caminos posibles.


Efecto Aharonov-Bohm
?
Una partícula cargada es afectada por un potencial vector $\mathbf{A}$ incluso si se mueve en una región donde el campo magnético $\mathbf{B}=0$. Muestra que los potenciales son fundamentales en QM.


Relaciones de Kramers-Kronig
?
Relacionan la parte real (dispersión) e imaginaria (absorción) de una función de respuesta compleja. Consecuencia de la Causalidad.


Ruptura Espontánea de Simetría
?
Ocurre cuando el Hamiltoniano posee una simetría pero el estado base (vacío) no la respeta.


Reglas de Selección (Dipolo Eléctrico)
?
Transiciones prohibidas si la integral del elemento de matriz es cero por paridad. Ej: $\Delta l = \pm 1$ es necesario; $s \to s$ está prohibido.
<!--SR:!2026-02-16,1,210-->