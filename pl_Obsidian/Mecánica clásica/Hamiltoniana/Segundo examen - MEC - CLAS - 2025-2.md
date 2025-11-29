

## **3. Aplicaciones del Formalismo Lagrangiano**

### **3.1 Pequeñas Oscilaciones - EXPANSIÓN DETALLADA**

#### **Fundamentos Teóricos**

**Equilibrio y Estabilidad:**
- **Condición de equilibrio**: Para un sistema con coordenadas generalizadas $q_1, q_2, ..., q_n$, los puntos de equilibrio satisfacen:
  $$
  \left.\frac{\partial V}{\partial q_i}\right|_{\mathbf{q}_0} = 0 \quad \forall i = 1, ..., n
  $$
  donde $V(\mathbf{q})$ es el potencial del sistema.

- **Clasificación de equilibrios**:
  - **Estable**: Matriz hessiana $K_{ij} = \frac{\partial^2 V}{\partial q_i \partial q_j}$ definida positiva
  - **Inestable**: Al menos un autovalor negativo
  - **Indiferente**: Autovalores nulos

**Desarrollo Matemático Completo:**

1. **Expansión alrededor del equilibrio**:
   $$
   V(\mathbf{q}) = V(\mathbf{q}_0) + \frac{1}{2} \sum_{i,j} K_{ij} \eta_i \eta_j + O(\eta^3)
   $$
   donde $\eta_i = q_i - q_{0i}$ son los desplazamientos.

2. **Energía cinética general**:
   $$
   T = \frac{1}{2} \sum_{i,j} M_{ij}(\mathbf{q}) \dot{q}_i \dot{q}_j
   $$
   Aproximando alrededor del equilibrio:
   $$
   T \approx \frac{1}{2} \sum_{i,j} M_{ij} \dot{\eta}_i \dot{\eta}_j
   $$
   donde $M_{ij} = M_{ij}(\mathbf{q}_0)$.

3. **Lagrangiano aproximado**:
   $$
   L = \frac{1}{2} \sum_{i,j} (M_{ij} \dot{\eta}_i \dot{\eta}_j - K_{ij} \eta_i \eta_j)
   $$

#### **Problema de Autovalores Generalizado**

Las ecuaciones de movimiento:
$$
\sum_j (M_{ij} \ddot{\eta}_j + K_{ij} \eta_j) = 0
$$

Buscamos soluciones armónicas:
$$
\eta_j(t) = a_j e^{i\omega t}
$$

Sustituyendo obtenemos:
$$
\sum_j (K_{ij} - \omega^2 M_{ij}) a_j = 0
$$

**Problema de autovalores**:
$$
(\mathbf{K} - \omega^2 \mathbf{M}) \mathbf{a} = 0
$$

La condición para soluciones no triviales:
$$
\det(\mathbf{K} - \omega^2 \mathbf{M}) = 0
$$

#### **Diagonalización y Modos Normales**

1. **Autovalores y autovectores**:
   - Soluciones $\omega_\alpha^2$ (α = 1,...,n): frecuencias normales
   - Autovectores $\mathbf{a}^{(\alpha)}$: modos normales

2. **Ortogonalidad**:
   $$
   \mathbf{a}^{(\alpha)T} \mathbf{M} \mathbf{a}^{(\beta)} = \delta_{\alpha\beta} m_\alpha
   $$
   $$
   \mathbf{a}^{(\alpha)T} \mathbf{K} \mathbf{a}^{(\beta)} = \delta_{\alpha\beta} m_\alpha \omega_\alpha^2
   $$

3. **Coordenadas normales** $Q_\alpha$:
   $$
   \eta_i(t) = \sum_{\alpha} a_i^{(\alpha)} Q_\alpha(t)
   $$

   El lagrangiano se diagonaliza:
   $$
   L = \frac{1}{2} \sum_{\alpha} (\dot{Q}_\alpha^2 - \omega_\alpha^2 Q_\alpha^2)
   $$

#### **Oscilaciones No Lineales - Teoría Avanzada**

**Método de Perturbaciones**:

Para un potencial anarmónico:
$$
V = \frac{1}{2} \omega_0^2 x^2 + \frac{1}{3} \alpha x^3 + \frac{1}{4} \beta x^4
$$

Ecuación de movimiento:
$$
\ddot{x} + \omega_0^2 x + \alpha x^2 + \beta x^3 = 0
$$

**Teoría de perturbaciones**:
- Expansión: $x(t) = x_0(t) + \epsilon x_1(t) + \epsilon^2 x_2(t) + \cdots$
- Correcciones a la frecuencia: $\omega = \omega_0 + \epsilon \omega_1 + \epsilon^2 \omega_2 + \cdots$

**Método de Promedio** (Método de Krylov-Bogoliubov):
Para $\ddot{x} + \omega_0^2 x = \epsilon f(x, \dot{x})$, suponemos:
$$
x(t) = a(t) \cos(\omega_0 t + \phi(t))
$$
$$
\dot{x}(t) = -a(t) \omega_0 \sin(\omega_0 t + \phi(t))
$$

Evolución lenta de amplitud y fase:
$$
\dot{a} = -\frac{\epsilon}{2\pi\omega_0} \int_0^{2\pi} f(a\cos\psi, -a\omega_0\sin\psi) \sin\psi \, d\psi
$$
$$
\dot{\phi} = -\frac{\epsilon}{2\pi\omega_0 a} \int_0^{2\pi} f(a\cos\psi, -a\omega_0\sin\psi) \cos\psi \, d\psi
$$

---

### **3.2 Cuerpo Rígido - EXPANSIÓN DETALLADA**

#### **Cinemática del Cuerpo Rígido**

**Transformaciones Ortogonales**:
- Matriz de rotación $\mathbf{R}$ satisface $\mathbf{R}^T \mathbf{R} = \mathbf{I}$, $\det(\mathbf{R}) = 1$
- Composición de rotaciones: $\mathbf{R} = \mathbf{R}_1 \mathbf{R}_2$

**Teorema de Euler**: Cualquier desplazamiento de un cuerpo rígido con un punto fijo puede describirse como una rotación alrededor de algún eje.

**Velocidad Angular**:
- Derivada de la matriz de rotación:
  $$
  \dot{\mathbf{R}} = \boldsymbol{\Omega} \mathbf{R}
  $$
  donde $\boldsymbol{\Omega}$ es la matriz antisimétrica:
  $$
  \boldsymbol{\Omega} = \begin{pmatrix}
  0 & -\omega_z & \omega_y \\
  \omega_z & 0 & -\omega_x \\
  -\omega_y & \omega_x & 0
  \end{pmatrix}
  $$

- Velocidad de un punto: $\mathbf{v} = \mathbf{V} + \boldsymbol{\omega} \times \mathbf{r}$

#### **Tensor de Inercia - Desarrollo Completo**

**Definición**:
$$
\mathbf{I} = \begin{pmatrix}
I_{xx} & I_{xy} & I_{xz} \\
I_{yx} & I_{yy} & I_{yz} \\
I_{zx} & I_{zy} & I_{zz}
\end{pmatrix}
$$

Componentes:
$$
I_{xx} = \int (y^2 + z^2) dm, \quad I_{xy} = -\int xy dm, \quad \text{etc.}
$$

**Teorema de Steiner**:
$$
\mathbf{I} = \mathbf{I}_{CM} + M(\mathbf{a}^T \mathbf{a} \cdot \mathbf{I} - \mathbf{a} \mathbf{a}^T)
$$
donde $\mathbf{a}$ es el vector del centro de masa al nuevo origen.

**Ejes Principales**:
- Diagonalización: $\mathbf{I} = \text{diag}(I_1, I_2, I_3)$
- Energía cinética rotacional: $T_{\text{rot}} = \frac{1}{2} \boldsymbol{\omega} \cdot \mathbf{I} \boldsymbol{\omega} = \frac{1}{2}(I_1 \omega_1^2 + I_2 \omega_2^2 + I_3 \omega_3^2)$

#### **Ángulos de Euler - Formulación Completa**

**Definición de los ángulos**:
1. $\phi$: Precesión (rotación alrededor de Z)
2. $\theta$: Nutación (rotación alrededor de línea de nodos)
3. $\psi$: Rotación propia (rotación alrededor de z')

**Matrices de rotación**:
$$
\mathbf{R}(\phi, \theta, \psi) = \mathbf{R}_z(\phi) \mathbf{R}_x(\theta) \mathbf{R}_z(\psi)
$$

**Velocidad angular en ejes del cuerpo**:
$$
\boldsymbol{\omega} = \begin{pmatrix}
\omega_x \\
\omega_y \\
\omega_z
\end{pmatrix} = \begin{pmatrix}
\dot{\phi} \sin\theta \sin\psi + \dot{\theta} \cos\psi \\
\dot{\phi} \sin\theta \cos\psi - \dot{\theta} \sin\psi \\
\dot{\phi} \cos\theta + \dot{\psi}
\end{pmatrix}
$$

**Velocidad angular en ejes espaciales**:
$$
\boldsymbol{\omega}' = \begin{pmatrix}
\dot{\theta} \cos\phi + \dot{\psi} \sin\theta \sin\phi \\
\dot{\theta} \sin\phi - \dot{\psi} \sin\theta \cos\phi \\
\dot{\phi} + \dot{\psi} \cos\theta
\end{pmatrix}
$$

#### **Ecuaciones de Euler - Deducción Completa**

**Momento angular en sistema rotante**:
$$
\left(\frac{d\mathbf{L}}{dt}\right)_{\text{lab}} = \left(\frac{d\mathbf{L}}{dt}\right)_{\text{cuerpo}} + \boldsymbol{\omega} \times \mathbf{L}
$$

**Ecuaciones de Euler**:
$$
\begin{aligned}
I_1 \dot{\omega}_1 - (I_2 - I_3) \omega_2 \omega_3 &= \tau_1 \\
I_2 \dot{\omega}_2 - (I_3 - I_1) \omega_3 \omega_1 &= \tau_2 \\
I_3 \dot{\omega}_3 - (I_1 - I_2) \omega_1 \omega_2 &= \tau_3
\end{aligned}
$$

#### **Trompo Simétrico - Análisis Matemático Completo**

**Lagrangiano del trompo**:
$$
L = \frac{1}{2} I_1(\dot{\theta}^2 + \dot{\phi}^2 \sin^2\theta) + \frac{1}{2} I_3(\dot{\psi} + \dot{\phi} \cos\theta)^2 - Mgl\cos\theta
$$

**Constantes de movimiento**:
1. Energía: $E = T + V$
2. $p_\psi = \frac{\partial L}{\partial \dot{\psi}} = I_3(\dot{\psi} + \dot{\phi} \cos\theta)$ (momento conjugado de $\psi$)
3. $p_\phi = \frac{\partial L}{\partial \dot{\phi}} = I_1 \dot{\phi} \sin^2\theta + I_3(\dot{\psi} + \dot{\phi} \cos\theta) \cos\theta$ (momento conjugado de $\phi$)

**Reducción a problema unidimensional**:
Definiendo $u = \cos\theta$, obtenemos:
$$
\dot{u}^2 = f(u) = (1 - u^2)(2E' - 2Mglu) - \frac{(p_\phi - p_\psi u)^2}{I_1^2}
$$
donde $E' = E - \frac{p_\psi^2}{2I_3}$

**Potencial efectivo**:
$$
V_{\text{ef}}(u) = Mglu + \frac{(p_\phi - p_\psi u)^2}{2I_1(1 - u^2)}
$$

**Casos especiales**:
- **Precesión estable**: $\dot{\theta} = 0$, $\theta = \theta_0$
- **Precesión dormida**: $\theta = 0$
- **Movimiento de nutación**: Oscilaciones en $\theta$

## **4. Mecánica Hamiltoniana - EXPANSIÓN DETALLADA**

### **4.1 Transformación de Legendre - Fundamentos Matemáticos**

**Definición rigurosa**:
Dada una función convexa $x)$, su transformada de Legendre $g(p)$ es:
$$
g(p) = \sup_x [px - f(x)]
$$

**Aplicación a la mecánica**:
$$
H(\mathbf{q}, \mathbf{p}, t) = \sum_{i=1}^n p_i \dot{q}_i - L(\mathbf{q}, \dot{\mathbf{q}}, t)
$$

**Condiciones de convexidad**:
$$
\det\left(\frac{\partial^2 L}{\partial \dot{q}_i \partial \dot{q}_j}\right) \neq 0
$$

**Diferencial del Hamiltoniano**:
$$
dH = \sum_{i=1}^n (\dot{q}_i dp_i - \dot{p}_i dq_i) - \frac{\partial L}{\partial t} dt
$$

### **4.2 Ecuaciones de Hamilton - Formulación Variacional**

**Principio de Hamilton modificado**:
$$
\delta \int_{t_1}^{t_2} \left[ \sum_{i=1}^n p_i \dot{q}_i - H(\mathbf{q}, \mathbf{p}, t) \right] dt = 0
$$

**Ecuaciones canónicas**:
$$
\dot{q}_i = \frac{\partial H}{\partial p_i}, \quad \dot{p}_i = -\frac{\partial H}{\partial q_i}
$$

**Flujo Hamiltoniano**:
El campo vectorial en el espacio fase:
$$
X_H = \sum_{i=1}^n \left( \frac{\partial H}{\partial p_i} \frac{\partial}{\partial q_i} - \frac{\partial H}{\partial q_i} \frac{\partial}{\partial p_i} \right)
$$

### **4.3 Corchetes de Poisson - Estructura Algebraica**

**Definición y propiedades**:
$$
\{f, g\} = \sum_{i=1}^n \left( \frac{\partial f}{\partial q_i} \frac{\partial g}{\partial p_i} - \frac{\partial f}{\partial p_i} \frac{\partial g}{\partial q_i} \right)
$$

**Propiedades algebraicas**:
1. Antisimetría: $\{f, g\} = -\{g, f\}$
2. Bilinealidad
3. Regla de Leibniz: $\{f, gh\} = \{f, g\}h + g\{f, h\}$
4. Identidad de Jacobi: $\{f, \{g, h\}\} + \{g, \{h, f\}\} + \{h, \{f, g\}\} = 0$

**Relaciones fundamentales**:
$$
\{q_i, q_j\} = 0, \quad \{p_i, p_j\} = 0, \quad \{q_i, p_j\} = \delta_{ij}
$$

**Teorema de Poisson**:
Si $f$ y $g$ son constantes de movimiento, entonces $\{f, g\}$ también lo es.

### **4.4 Transformaciones Canónicas - Teoría Completa**

**Definición**: Transformación $(\mathbf{q}, \mathbf{p}) \to (\mathbf{Q}, \mathbf{P})$ que preserva la forma de las ecuaciones de Hamilton.

**Condición de canonicidad**:
$$
\sum_{i=1}^n (p_i dq_i - P_i dQ_i) = dF
$$
para alguna función generatriz $F$.

**Tipos de funciones generatrices**:

1. **Tipo I**: $F_1(\mathbf{q}, \mathbf{Q}, t)$
   $$
   p_i = \frac{\partial F_1}{\partial q_i}, \quad P_i = -\frac{\partial F_1}{\partial Q_i}, \quad K = H + \frac{\partial F_1}{\partial t}
   $$

2. **Tipo II**: $F_2(\mathbf{q}, \mathbf{P}, t)$
   $$
   p_i = \frac{\partial F_2}{\partial q_i}, \quad Q_i = \frac{\partial F_2}{\partial P_i}, \quad K = H + \frac{\partial F_2}{\partial t}
   $$

3. **Tipo III**: $F_3(\mathbf{p}, \mathbf{Q}, t)$
4. **Tipo IV**: $F_4(\mathbf{p}, \mathbf{P}, t)$

**Transformaciones canónicas infinitesimales**:
$$
F_2(\mathbf{q}, \mathbf{P}, t) = \sum_{i=1}^n q_i P_i + \epsilon G(\mathbf{q}, \mathbf{P}, t)
$$
donde $G$ es la función generatriz infinitesimal.

### **4.5 Teorema de Liouville - Mecánica Estadística**

**Formulación diferencial**:
La densidad $\rho(\mathbf{q}, \mathbf{p}, t)$ satisface:
$$
\frac{\partial \rho}{\partial t} + \{\rho, H\} = 0
$$

**Formulación integral**:
El volumen en el espacio fase se conserva:
$$
\frac{d}{dt} \int_{\Omega(t)} dq dp = 0
$$

**Teorema del flujo incompresible**:
$$
\nabla \cdot \mathbf{v} = \sum_{i=1}^n \left( \frac{\partial \dot{q}_i}{\partial q_i} + \frac{\partial \dot{p}_i}{\partial p_i} \right) = 0
$$

### **4.6 Ecuación de Hamilton-Jacobi - Solución Completa**

**Ecuación de Hamilton-Jacobi**:
$$
H\left(\mathbf{q}, \frac{\partial S}{\partial \mathbf{q}}, t\right) + \frac{\partial S}{\partial t} = 0
$$

**Separación de variables**:
Si $H$ no depende explícitamente del tiempo:
$$
S(\mathbf{q}, t) = W(\mathbf{q}) - Et
$$
obtenemos la ecuación de Hamilton-Jacobi independiente del tiempo:
$$
H\left(\mathbf{q}, \frac{\partial W}{\partial \mathbf{q}}\right) = E
$$

**Solución completa**:
Una solución $S(\mathbf{q}, \boldsymbol{\alpha}, t)$ que depende de $n$ constantes $\alpha_1, ..., \alpha_n$ (excluyendo la constante aditiva).

**Relación con la acción**:
$$
S(\mathbf{q}, t) = \int L dt
$$

**Interpretación geométrica**:
Las superficies $S(\mathbf{q}, t) = \text{constante}$ se propagan como frentes de onda.

### **4.7 Variables Ángulo-Acción - Sistemas Integrables**

**Definición de integrabilidad**:
Un sistema con $n$ grados de libertad es integrable si existen $n$ constantes de movimiento $F_i$ en involución:
$$
\{F_i, F_j\} = 0 \quad \forall i,j
$$

**Teorema de Arnold-Liouville**:
El espacio fase de un sistema integrable es foliado por toros n-dimensionales invariantes.

**Variables acción**:
$$
J_k = \frac{1}{2\pi} \oint_{\gamma_k} \mathbf{p} \cdot d\mathbf{q}
$$
donde $\gamma_k$ son los ciclos fundamentales del toro invariante.

**Variables ángulo**:
$$
\theta_k = \frac{\partial W}{\partial J_k}
$$
donde $W(\mathbf{q}, \mathbf{J})$ es la función característica de Hamilton.

**Ecuaciones de movimiento**:
$$
\dot{J}_k = 0, \quad \dot{\theta}_k = \frac{\partial H}{\partial J_k} = \nu_k(\mathbf{J})
$$

**Frecuencias**:
$$
\nu_k(\mathbf{J}) = \frac{\partial H}{\partial J_k}
$$

**Aplicaciones**:
1. Teoría de perturbaciones para sistemas casi-integrables
2. Teorema KAM (Kolmogorov-Arnold-Moser)
3. Cuantización semiclásica (reglas de Bohr-Sommerfeld)

---

Este tratamiento teórico completo proporciona las bases matemáticas rigurosas para cada tema, incluyendo las demostraciones y desarrollos formales necesarios para un entendimiento profundo de la mecánica clásica a nivel de pregrado en física pura.