## Explicación completa del tensor de esfuerzos $T_{ij}$ y ecuaciones asociadas

### **Prerrequisitos matemáticos y físicos**
1. **Álgebra lineal avanzada**:
   - Espacios vectoriales, bases y cambio de base
   - Diagonalización de matrices, valores y vectores propios
   - Formas bilineales y cuadráticas
   - 
2. **Cálculo tensorial**:
   - Convención de suma de Einstein
   - Transformación de coordenadas: $T'_{ij} = \frac{\partial x^k}{\partial x'^i} \frac{\partial x^l}{\partial x'^j} T_{kl}$
   - Operaciones tensoriales: contracción, producto exterior
   - 
3. **Mecánica del medio continuo**:
   - Concepto de partícula fluida y volumen de control
   - Deformación infinitesimal y tensor de deformación $\epsilon_{ij}$ 
   - 
   - 4. **Termodinámica**:
   - Leyes de conservación (masa, energía, momento)
   - Ecuaciones constitutivas para materiales


---

### **El tensor de esfuerzos $T_{ij}$ (Tensor de Cauchy)**
#### **Definición y significado físico**
El tensor de esfuerzos $T_{ij}$ es un tensor simétrico de segundo orden ($T_{ij} = T_{ji}$) que describe completamente el estado de esfuerzos en un punto de un medio continuo. Sus componentes tienen unidades de fuerza por unidad de área (Pa en SI).

- **Componentes diagonales ($T_{11}, T_{22}, T_{33}$)**: Esfuerzos normales (tracción/compresión)
- **Componentes no diagonales ($T_{12}, T_{13}$, etc.)**: Esfuerzos cortantes (cizalladura)

**Interpretación física**: El componente $T_{ij}$ representa la fuerza en dirección $i$ que actúa sobre una superficie con normal $j$.

#### **Ecuación fundamental: Conservación del momento lineal**
La ecuación diferencial gobernante, derivada de la segunda ley de Newton, es:

$$
\rho \frac{Dv_i}{Dt} = \frac{\partial T_{ij}}{\partial x_j} + f_i
$$

donde:
- $\rho$: densidad del material
- $v_i$: componentes del vector velocidad
- $f_i$: fuerzas de cuerpo por unidad de volumen (e.g., gravedad)
- $\frac{D}{Dt}$: derivada material ($\frac{\partial}{\partial t} + v_k \frac{\partial}{\partial x_k}$)

**Forma expandida**:
$$
\rho \left( \frac{\partial v_i}{\partial t} + v_j \frac{\partial v_i}{\partial x_j} \right) = \frac{\partial T_{ij}}{\partial x_j} + \rho g_i
$$

---

### **Ecuaciones constitutivas para materiales**
#### **Para fluidos newtonianos (Ecuación de Navier-Stokes)**
$$
T_{ij} = -p \delta_{ij} + \lambda \delta_{ij} \frac{\partial v_k}{\partial x_k} + \mu \left( \frac{\partial v_i}{\partial x_j} + \frac{\partial v_j}{\partial x_i} \right)
$$

- $p$: presión termodinámica
- $\mu$: viscosidad dinámica
- $\lambda$: segundo coeficiente de viscosidad ($\lambda = -\frac{2}{3}\mu$ para gases)

**Conservación de masa (continuidad)**:
$$
\frac{\partial \rho}{\partial t} + \frac{\partial (\rho v_j)}{\partial x_j} = 0
$$

#### **Para sólidos elásticos lineales (Ley de Hooke generalizada)**
$$
T_{ij} = C_{ijkl}  \epsilon_{kl}
$$
donde $C_{ijkl}$ es el tensor de rigidez de cuarto orden, y $\epsilon_{kl}$ es el tensor de deformación infinitesimal:
$$
\epsilon_{kl} = \frac{1}{2} \left( \frac{\partial u_k}{\partial x_l} + \frac{\partial u_l}{\partial x_k} \right)
$$

**Para materiales isótropos**:
$$
T_{ij} = \lambda \delta_{ij} \epsilon_{kk} + 2\mu \epsilon_{ij}
$$
con $\lambda, \mu$ coeficientes de Lamé.

---

### **Ecuaciones de campo completas**
#### **Sistema para fluidos incompresibles**
1. **Conservación de masa**:
   $$
   \nabla \cdot \mathbf{v} = 0
   $$

2. **Conservación de momento**:
   $$
   \rho \left( \frac{\partial \mathbf{v}}{\partial t} + (\mathbf{v} \cdot \nabla) \mathbf{v} \right) = -\nabla p + \mu \nabla^2 \mathbf{v} + \rho \mathbf{g}
   $$

#### **Sistema para sólidos elásticos**
1. **Ecuación de movimiento**:
   $$
   \rho \frac{\partial^2 u_i}{\partial t^2} = \frac{\partial T_{ij}}{\partial x_j} + f_i
   $$

2. **Ley constitutiva**:
   $$
   T_{ij} = \lambda \delta_{ij} \frac{\partial u_k}{\partial x_k} + \mu \left( \frac{\partial u_i}{\partial x_j} + \frac{\partial u_j}{\partial x_i} \right)
   $$

---

### **Tensor de esfuerzos en relatividad general**
En la teoría de Einstein, el tensor energía-esfuerzo $T_{\mu\nu}$ es fundamental para la ecuación de campo:

$$
R_{\mu\nu} - \frac{1}{2} R g_{\mu\nu} = \frac{8\pi G}{c^4} T_{\mu\nu}
$$

**Componentes**:
- $T_{00}$: densidad de energía
- $T_{0i}$: flujo de energía/momento
- $T_{ij}$: tensor de esfuerzos clásico

**Conservación covariante**:
$$
\nabla_\mu T^{\mu\nu} = 0
$$

---

### **Aplicaciones importantes**
#### **Mecánica de fracturas (Criterio de von Mises)**
$$
\sigma_{\text{vm}} = \sqrt{\frac{3}{2} T'_{ij} T'_{ij}} \quad \text{con} \quad T'_{ij} = T_{ij} - \frac{1}{3} T_{kk} \delta_{ij}
$$
La fractura ocurre cuando $\sigma_{\text{vm}} > \sigma_{\text{yield}}$.

#### **Geomecánica (Tensor de esfuerzos terrestres)**
$$
T_{ij} = \begin{pmatrix}
\sigma_h & 0 & 0 \\
0 & \sigma_h & 0 \\
0 & 0 & \sigma_v
\end{pmatrix} + \text{tectónicos}
$$
donde $\sigma_v$ es el esfuerzo vertical por peso de roca.

---

### **Solución de ecuaciones diferenciales asociadas**
#### **Técnicas comunes**
1. **Método de separación de variables**:
   Para geometrías simétricas (esferas, cilindros)

2. **Funciones de Green**:
   Solución fundamental para ecuaciones lineales:
   $$
   T_{ij}(\mathbf{x}) = \int G_{ijk}(\mathbf{x},\mathbf{x}') f_k(\mathbf{x}')  dV'
   $$

3. **Métodos numéricos**:
   - Elementos Finitos (FEM): Discretización de $\nabla \cdot \mathbf{T} + \mathbf{f} = 0$
   - Volúmenes Finitos: Conservación en celdas discretas

#### **Teorema de descomposición de Helmholtz**
Para desacoplar componentes irrotacionales y solenoidales:
$$
\mathbf{v} = \nabla \phi + \nabla \times \mathbf{A}
$$
$$
\nabla^2 \phi = \frac{\partial v_k}{\partial x_k}, \quad \nabla^2 \mathbf{A} = -\nabla \times (\nabla \times \mathbf{v})
$$

---

### **Ejemplo concreto: Esfera elástica bajo presión**
**Ecuación de equilibrio**:
$$
\frac{d}{dr}\left( r^2 \frac{du}{dr} \right) - 2u = 0
$$

**Solución**:
$$
u(r) = Ar + \frac{B}{r^2}, \quad T_{rr} = (3\lambda + 2\mu)A - \frac{4\mu B}{r^3}
$$

**Condiciones de frontera**:
$$
T_{rr}(R_{\text{int}}) = -p_{\text{int}}, \quad T_{rr}(R_{\text{ext}}) = -p_{\text{ext}}
$$

---

Esta estructura integra los conceptos matemáticos, físicos y de ingeniería asociados al tensor de esfuerzos, proporcionando una comprensión completa de sus ecuaciones diferenciales y aplicaciones prácticas.