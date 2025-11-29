
## **4.4 Transformaciones Canónicas - Teoría Profunda**

### **Fundamentos Matemáticos de las Transformaciones Canónicas**

**Definición Formal**:
Una transformación $(\mathbf{q}, \mathbf{p}) \rightarrow (\mathbf{Q}, \mathbf{P})$ es canónica si preserva la forma simpléctica del espacio fase:
$$
\sum_{i=1}^n dp_i \wedge dq_i = \sum_{i=1}^n dP_i \wedge dQ_i
$$

**Formulación Diferencial Exacta**:
La condición fundamental es:
$$
\sum_{i=1}^n (p_i dq_i - P_i dQ_i) = dF
$$
donde $F$ es una función generatriz.

### **Tipos de Funciones Generatrices - Desarrollo Completo**

#### **Tipo I: $F_1(\mathbf{q}, \mathbf{Q}, t)$**
**Relaciones de transformación**:
$$
p_i = \frac{\partial F_1}{\partial q_i}, \quad P_i = -\frac{\partial F_1}{\partial Q_i}, \quad K = H + \frac{\partial F_1}{\partial t}
$$

**Ejemplo concreto**: Transformación identidad
$$
F_1 = \sum_{i=1}^n q_i Q_i \Rightarrow p_i = Q_i, \quad P_i = -q_i
$$

#### **Tipo II: $F_2(\mathbf{q}, \mathbf{P}, t)$ - Más Común**
**Relaciones**:
$$
p_i = \frac{\partial F_2}{\partial q_i}, \quad Q_i = \frac{\partial F_2}{\partial P_i}, \quad K = H + \frac{\partial F_2}{\partial t}
$$

**Transformación de Legendre**:
$$
F_2(\mathbf{q}, \mathbf{P}, t) = \sum_{i=1}^n q_i P_i + G(\mathbf{q}, \mathbf{P}, t)
$$

**Ejemplo importante**: Transformación puntual extendida
$$
F_2 = \sum_{i,j} f_i(\mathbf{q}) P_j A_{ji} \Rightarrow Q_i = \sum_j A_{ji} f_j(\mathbf{q})
$$

#### **Tipo III: $F_3(\mathbf{p}, \mathbf{Q}, t)$**
$$
q_i = -\frac{\partial F_3}{\partial p_i}, \quad P_i = -\frac{\partial F_3}{\partial Q_i}, \quad K = H + \frac{\partial F_3}{\partial t}
$$

#### **Tipo IV: $F_4(\mathbf{p}, \mathbf{P}, t)$**
$$
q_i = -\frac{\partial F_4}{\partial p_i}, \quad Q_i = \frac{\partial F_4}{\partial P_i}, \quad K = H + \frac{\partial F_4}{\partial t}
$$

### **Matriz Jacobiana y Condición de Canonicidad**

**Matriz Jacobiana de la transformación**:
$$
\mathbf{J} = \begin{pmatrix}
\frac{\partial \mathbf{Q}}{\partial \mathbf{q}} & \frac{\partial \mathbf{Q}}{\partial \mathbf{p}} \\
\frac{\partial \mathbf{P}}{\partial \mathbf{q}} & \frac{\partial \mathbf{P}}{\partial \mathbf{p}}
\end{pmatrix}
$$

**Condición simpléctica**:
$$
\mathbf{J}^T \boldsymbol{\Omega} \mathbf{J} = \boldsymbol{\Omega}
$$
donde $\boldsymbol{\Omega} = \begin{pmatrix} \mathbf{0} & \mathbf{I} \\ -\mathbf{I} & \mathbf{0} \end{pmatrix}$ es la matriz simpléctica fundamental.

### **Transformaciones Canónicas Infinitesimales - Teoría Detallada**

**Función generatriz infinitesimal**:
$$
F_2(\mathbf{q}, \mathbf{P}, t) = \sum_{i=1}^n q_i P_i + \epsilon G(\mathbf{q}, \mathbf{P}, t)
$$

**Transformaciones resultantes**:
$$
Q_i = q_i + \epsilon \frac{\partial G}{\partial P_i}, \quad p_i = P_i + \epsilon \frac{\partial G}{\partial q_i}
$$

**Aproximación a primer orden**:
$$
Q_i \approx q_i + \epsilon \frac{\partial G}{\partial p_i}, \quad P_i \approx p_i - \epsilon \frac{\partial G}{\partial q_i}
$$

**Interpretación física**: Toda función $G$ genera una transformación canónica infinitesimal.

### **Corchetes de Lagrange y Paréntesis Fundamentales**

**Corchetes de Lagrange**:
$$
[Q_i, Q_j]_{\mathbf{q},\mathbf{p}} = \sum_{k=1}^n \left( \frac{\partial Q_i}{\partial q_k} \frac{\partial Q_j}{\partial p_k} - \frac{\partial Q_i}{\partial p_k} \frac{\partial Q_j}{\partial q_k} \right)
$$

**Condiciones de canonicidad en términos de corchetes**:
- $[Q_i, Q_j]_{\mathbf{q},\mathbf{p}} = 0$
- $[P_i, P_j]_{\mathbf{q},\mathbf{p}} = 0$
- $[Q_i, P_j]_{\mathbf{q},\mathbf{p}} = \delta_{ij}$

### **Ejemplos Avanzados de Transformaciones Canónicas**

#### **Transformación a Coordenadas Armónicas**
Para un oscilador armónico $H = \frac{p^2}{2m} + \frac{1}{2}m\omega^2 q^2$:
$$
F_1(q, Q) = \frac{1}{2}m\omega q^2 \cot Q
$$
Resulta en:
$$
p = \frac{\partial F_1}{\partial q} = m\omega q \cot Q, \quad P = -\frac{\partial F_1}{\partial Q} = \frac{m\omega q^2}{2\sin^2 Q}
$$

#### **Transformación de Fourier en el Espacio Fase**
$$
F_2(\mathbf{q}, \mathbf{P}) = \sum_i q_i P_i + \frac{1}{2} \sum_{i,j} A_{ij} q_i q_j
$$
con $\mathbf{A}$ simétrica.

### **Teorema de Generación de Transformaciones Canónicas**

**Teorema**: Toda función diferenciable $G(\mathbf{q}, \mathbf{p})$ genera una familia uniparamétrica de transformaciones canónicas a través de:
$$
\frac{dq_i}{d\epsilon} = \frac{\partial G}{\partial p_i}, \quad \frac{dp_i}{d\epsilon} = -\frac{\partial G}{\partial q_i}
$$

---

## **4.5 Teorema de Liouville - Mecánica Estadística Profunda**

### **Formulaciones Múltiples del Teorema**

#### **Formulación Diferencial**
Para un sistema Hamiltoniano, el flujo en el espacio fase es incompresible:
$$
\nabla \cdot \mathbf{v} = \sum_{i=1}^n \left( \frac{\partial \dot{q}_i}{\partial q_i} + \frac{\partial \dot{p}_i}{\partial p_i} \right) = 0
$$

**Demostración rigurosa**:
$$
\frac{\partial \dot{q}_i}{\partial q_i} = \frac{\partial^2 H}{\partial q_i \partial p_i}, \quad \frac{\partial \dot{p}_i}{\partial p_i} = -\frac{\partial^2 H}{\partial p_i \partial q_i}
$$
$$
\Rightarrow \nabla \cdot \mathbf{v} = \sum_i \left( \frac{\partial^2 H}{\partial q_i \partial p_i} - \frac{\partial^2 H}{\partial p_i \partial q_i} \right) = 0
$$

#### **Formulación Integral**
Para cualquier volumen $V(t)$ en el espacio fase que evoluciona con el flujo Hamiltoniano:
$$
\frac{d}{dt} \int_{V(t)} d\Gamma = 0, \quad \text{donde } d\Gamma = dq_1 \cdots dq_n dp_1 \cdots dp_n
$$

### **Ecuación de Liouville para la Densidad**

#### **Derivación Completa**
Sea $\rho(\mathbf{q}, \mathbf{p}, t)$ la densidad en el espacio fase. La conservación de probabilidad implica:
$$
\frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \mathbf{v}) = 0
$$

Usando $\nabla \cdot \mathbf{v} = 0$:
$$
\frac{\partial \rho}{\partial t} + \mathbf{v} \cdot \nabla \rho = 0
$$

En términos de corchetes de Poisson:
$$
\frac{\partial \rho}{\partial t} + \{\rho, H\} = 0
$$

#### **Formulación en Derivada Total**
$$
\frac{d\rho}{dt} = \frac{\partial \rho}{\partial t} + \sum_{i=1}^n \left( \frac{\partial \rho}{\partial q_i} \dot{q}_i + \frac{\partial \rho}{\partial p_i} \dot{p}_i \right) = 0
$$

### **Teorema de Liouville en Coordenadas Generales**

**Elemento de volumen invariante**:
$$
d\Gamma = \sqrt{\det(\mathbf{J}^T \boldsymbol{\Omega} \mathbf{J})} dq_1 \cdots dp_n = dq_1 \cdots dp_n
$$
donde la igualdad se mantiene para transformaciones canónicas.

### **Aplicaciones en Mecánica Estadística**

#### **Distribución Microcanónica**
Para un sistema aislado con energía $E$:
$$
\rho(\mathbf{q}, \mathbf{p}) = \frac{1}{\Omega(E)} \delta(H(\mathbf{q}, \mathbf{p}) - E)
$$
donde $\Omega(E) = \int \delta(H - E) d\Gamma$ es la densidad de estados.

#### **Teorema del Virial**
Para cualquier función $A(\mathbf{q}, \mathbf{p})$:
$$
\left\langle \frac{dA}{dt} \right\rangle = 0
$$
en el ensemble microcanónico, donde $\langle \cdot \rangle$ denota promedio temporal.

### **Generalizaciones y Teoremas Relacionados**

#### **Teorema de Recurrencia de Poincaré**
Para un sistema Hamiltoniano acotado, casi todo estado regresa arbitrariamente cerca de su condición inicial infinitas veces.

#### **Teorema KAM (Kolmogorov-Arnold-Moser)**
Bajo pequeñas perturbaciones, la mayoría de los toros invariantes de sistemas integrables persisten.

### **Formulación en Espacio Fase Extendido**

Incluyendo el tiempo como variable adicional $(q_0 = t, p_0 = -H)$:
$$
d\Gamma_{\text{ext}} = dq_0 dq_1 \cdots dq_n dp_0 dp_1 \cdots dp_n
$$

El teorema de Liouville se mantiene en este espacio extendido.

---

## **4.6 Ecuación de Hamilton-Jacobi - Teoría Completa**

### **Fundamentos Matemáticos**

#### **Ecuación de Hamilton-Jacobi General**
$$
H\left(\mathbf{q}, \frac{\partial S}{\partial \mathbf{q}}, t\right) + \frac{\partial S}{\partial t} = 0
$$

#### **Interpretación Geométrica**
La función $S(\mathbf{q}, t)$ define una familia de superficies en el espacio de configuración que se propagan como frentes de onda.

### **Solución Completa - Teoría Detallada**

#### **Definición Rigurosa**
Una solución completa es una función $S(\mathbf{q}, \boldsymbol{\alpha}, t)$ que:
1. Satisface la ecuación de Hamilton-Jacobi
2. Depende de $n$ constantes independientes $\alpha_1, \ldots, \alpha_n$
3. Cumple $\det\left( \frac{\partial^2 S}{\partial q_i \partial \alpha_j} \right) \neq 0$

#### **Método de Separación de Variables**

**Caso 1: Hamiltoniano independiente del tiempo**
$$
S(\mathbf{q}, t) = W(\mathbf{q}) - Et
$$
donde $W$ satisface:
$$
H\left(\mathbf{q}, \frac{\partial W}{\partial \mathbf{q}}\right) = E
$$

**Caso 2: Separación completa**
Si $H = \sum_{i=1}^n H_i(q_i, p_i)$, entonces:
$$
W(\mathbf{q}) = \sum_{i=1}^n W_i(q_i)
$$
con $H_i\left(q_i, \frac{dW_i}{dq_i}\right) = \alpha_i$ y $\sum \alpha_i = E$

### **Teoría de Jacobi para la Integración**

#### **Ecuaciones de Movimiento desde S**
Dada una solución completa $S(\mathbf{q}, \boldsymbol{\alpha}, t)$, las ecuaciones del movimiento son:
$$
\frac{\partial S}{\partial \alpha_i} = \beta_i, \quad \frac{\partial S}{\partial q_i} = p_i
$$
donde $\beta_i$ son constantes.

#### **Matriz Hessiana y Condición de No Degeneración**
$$
\mathbf{M} = \left( \frac{\partial^2 S}{\partial q_i \partial \alpha_j} \right), \quad \det(\mathbf{M}) \neq 0
$$
Esta condición asegura que podemos resolver $\mathbf{q} = \mathbf{q}(\boldsymbol{\alpha}, \boldsymbol{\beta}, t)$.

### **Ejemplos Avanzados de Separación**

#### **Partícula en Potencial Central**
Hamiltoniano:
$$
H = \frac{1}{2m} \left( p_r^2 + \frac{p_\theta^2}{r^2} + \frac{p_\phi^2}{r^2 \sin^2\theta} \right) + V(r)
$$

Solución separada:
$$
S = -Et + \int \sqrt{2m(E - V(r)) - \frac{\alpha_\theta^2}{r^2}} dr + \int \sqrt{\alpha_\theta^2 - \frac{\alpha_\phi^2}{\sin^2\theta}} d\theta + \alpha_\phi \phi
$$

#### **Oscilador Armónico Multidimensional**
Para $H = \sum_{i=1}^n \frac{1}{2}(p_i^2 + \omega_i^2 q_i^2)$:
$$
S = -Et + \sum_{i=1}^n \int \sqrt{2E_i - \omega_i^2 q_i^2} dq_i
$$
con $um E_i = E$
### **Relación con la Óptica Geométrica**

#### **Analogía Óptico-Mecánica**
- $S$ análogo al eikonal óptico
- Superficies $S =$ constante análogas a frentes de onda
- Trayectorias ortogonales a superficies $S =$ constante

#### **Principio de Fermat vs. Principio de Maupertuis**
$$
\delta \int \sqrt{2m(E - V)} ds = 0 \quad \text{(Maupertuis)}
$$
$$
\delta \int n ds = 0 \quad \text{(Fermat)}
$$
con $n \propto \sqrt{E - V}$

### **Aplicación a Problemas de Contorno**

#### **Problema de dos puntos**
Dados $(\mathbf{q}_0, t_0)$ y $(\mathbf{q}_1, t_1)$, la solución $S(\mathbf{q}_1, t_1; \mathbf{q}_0, t_0)$ satisface:
$$
\frac{\partial S}{\partial \mathbf{q}_1} = \mathbf{p}_1, \quad \frac{\partial S}{\partial \mathbf{q}_0} = -\mathbf{p}_0
$$

### **Conexión con la Mecánica Cuántica**

#### **Límite Semiclásico**
La función de onda semicláscica:
$$
\psi(\mathbf{q}, t) = A(\mathbf{q}, t) e^{iS(\mathbf{q}, t)/\hbar}
$$

Sustituyendo en la ecuación de Schrödinger y tomando $\hbar \to 0$ se recupera la ecuación de Hamilton-Jacobi.

#### **Reglas de Cuantización de Bohr-Sommerfeld**
$$
\oint p_i dq_i = \left(n_i + \frac{\mu_i}{4}\right)h
$$
donde $\mu_i$ es el índice de Maslov.

### **Método de Hamilton-Jacobi en Teoría de Perturbaciones**

#### **Teoría de Perturbaciones para Sistemas Integrables**
Para $H = H_0(\mathbf{J}) + \epsilon H_1(\boldsymbol{\theta}, \mathbf{J})$, buscamos una transformación canónica a nuevas variables acción-ángulo donde $H$ dependa solo de $\mathbf{J}$.

**Función generatriz**:
$$
S(\boldsymbol{\theta}, \mathbf{J}') = \boldsymbol{\theta} \cdot \mathbf{J}' + \epsilon S_1(\boldsymbol{\theta}, \mathbf{J}') + \cdots
$$

### **Ecuación de Hamilton-Jacobi Relativista**

Para una partícula relativista:
$$
\frac{1}{c^2} \left( \frac{\partial S}{\partial t} \right)^2 - \left( \frac{\partial S}{\partial \mathbf{q}} \right)^2 = m^2 c^2
$$

Esta expansión detallada proporciona una comprensión profunda de estos temas avanzados de mecánica clásica, incluyendo las demostraciones matemáticas rigurosas y las aplicaciones físicas significativas.