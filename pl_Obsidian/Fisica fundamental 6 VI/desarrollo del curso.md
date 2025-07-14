### **Desarrollo Matemático Conceptual con Pedagogía para Física Fundamental VI**

---

#### **Unidad 1: Introducción a la Física Nuclear**
**Concepto central:** *Radiactividad y propiedades nucleares*  
**Herramienta matemática:** *Ley del decaimiento exponencial y energía de enlace*

1. **Ley del decaimiento radiactivo**:  
   - **Ecuación diferencial**:  
     $$
     \frac{dN}{dt} = -\lambda N \quad \Rightarrow \quad N(t) = N_0 e^{-\lambda t}
     $$  
     - **Pedagogía**: Visualizar como una "población de núcleos" que disminuye con el tiempo. Relacionar $\lambda$(constante de decaimiento) con la probabilidad cuántica de transición.  
   - **Vida media ($\tau$)**:  
     $$
     \tau = \frac{1}{\lambda}, \quad t_{1/2} = \frac{\ln 2}{\lambda}
     $$  
     *Ejemplo práctico*: Calcular la actividad residual de $^{137}\text{Cs}$ ($t_{1/2} = 30.2$ años) después de 100 años.

2. **Energía de enlace nuclear**:  
   - **Fórmula semiempírica de Weizsäcker**:  
     $$
     B(A,Z) = a_V A - a_S A^{2/3} - a_C \frac{Z(Z-1)}{A^{1/3}} - a_A \frac{(A-2Z)^2}{A} + \delta(A,Z)
     $$  
     - **Pedagogía**:  
       - $a_V A$: Energía de volumen (nucleones interactúan solo con vecinos cercanos).  
       - $-a_S A^{2/3}$: Término de superficie (nucleones en la superficie tienen menos enlaces).  
       - **Actividad**: Graficar $B/A$ vs. $A$ para mostrar la curva de estabilidad y discutir la fisión/fusión.

---

#### **Unidad 2: Detectores e Instrumentación**
**Concepto central:** *Interacción radiación-materia y detección*  
**Herramienta matemática:** *Ecuaciones de atenuación y estadística de Poisson*

1. **Ley de atenuación para rayos $\gamma$**:  
   $$
   I = I_0 e^{-\mu x}
   $$  
   - $\mu$: Coeficiente de atenuación (depende de $Z$ del material y energía del fotón).  
   - **Pedagogía**: Simular con datos experimentales (ej: plomo vs. aluminio) y ajustar curvas exponenciales.

2. **Estadística de conteo radiactivo**:  
   - **Distribución de Poisson**:  
     $$
     P(k) = \frac{\lambda^k e^{-\lambda}}{k!}
     $$  
     - **Error estándar**: $\sigma = \sqrt{N}$ (para $N$ conteos).  
     *Ejemplo*: Analizar por qué 10,000 conteos tienen error del 1% ($\sigma/N = 1/\sqrt{N}$).

---

#### **Unidad 3: Modelos Nucleares y Estabilidad**
**Concepto central:** *Modelo de la gota líquida vs. modelo de capas*  
**Herramienta matemática:** *Ecuaciones de Bohr-Wheeler y números mágicos*

1. **Modelo de la gota líquida (fisión)**:  
   - **Energía de deformación**:  
     $$
     E_{\text{def}} = \frac{1}{2} C (\beta) \beta^2, \quad \beta = \text{parámetro de deformación}
     $$  
     - **Condición de fisión espontánea**: Cuando $E_{\text{Coulomb}} > 2E_{\text{superficie}}$.

2. **Modelo de capas**:  
   - **Números mágicos**: $2, 8, 20, 28, 50, 82, 126$.  
   - **Potencial espín-órbita**:  
     $$
     V_{so}(r) = V_0 \frac{1}{r} \frac{d f}{dr} (\vec{L} \cdot \vec{S})
     $$  
     - **Pedagogía**: Resolver la ecuación de Schrödinger para pozo infinito y mostrar división de niveles por $L \cdot S$ (ej: nivel $1f_{7/2}$ vs. $1f_{5/2}$).

---

#### **Unidad 4: Decaimiento $\alpha$, $\beta$, $\gamma$**
**Concepto central:** *Túnel cuántico y espectros continuos*  
**Herramienta matemática:** *Teoría de Gamow y ecuación de Fermi*

1. **Decaimiento $\alpha$ (Gamow)**:  
   - **Probabilidad de túnel**:  
     $$
     P \propto \exp\left[ -\frac{2}{\hbar} \int_{R}^{b} \sqrt{2m(V(r)-Q)}  dr \right]
     $$  
     - **Pedagogía**: Calcular $T_{1/2}$ para $^{238}\text{U}$ ($Q=4.27$ MeV) vs. $^{212}\text{Po}$ ($Q=8.95$ MeV) y discutir la dependencia con $Q$.

1. **Decaimiento $\beta$ (Fermi)**:  
   - **Distribución de energía**:  
     $$
     N(p)  dp \propto p^2 (Q - E_e)^2  dp
     $$  
     - **Gráfico de Kurie**:  
       $$
       K(E) = \sqrt{\frac{N(p)}{p^2 F(Z,p)}} \propto (Q - E_e)
       $$  
       *Demostración*: Usar datos simulados para mostrar linealidad y extraer $Q$.

---

#### **Unidad 5: Reacciones Nucleares**
**Concepto central:** *Sección eficaz y conservación de momento*  
**Herramienta matemática:** *Cinética relativista y ecuaciones de Breit-Wigner*

1. **Sección eficaz de resonancia**:  
   $$
   \sigma(E) = \frac{\pi \hbar^2}{2mE} \frac{\Gamma_i \Gamma_f}{(E - E_R)^2 + (\Gamma/2)^2}
   $$  
   - $\Gamma$: Anchura total ($\Gamma = \hbar / \tau$).  
   - **Pedagogía**: Relacionar $\Gamma$ con la vida media del estado compuesto.

2. **Conservación en reacciones**:  
   - **Ejemplo**: $d + {}^6\text{Li} \to \alpha + \alpha$.  
     - Calcular $Q$-value usando masas atómicas.  
     - Resolver geométricamente los ángulos de emisión de las partículas $\alpha$.

---

#### **Unidad 6: Interacción Radiación-Materia**
**Concepto central:** *Pérdida de energía de partículas cargadas*  
**Herramienta matemática:** *Fórmula de Bethe-Bloch*

$$
-\frac{dE}{dx} = K z^2 \frac{Z}{A} \frac{1}{\beta^2} \left[ \ln \frac{2m_e c^2 \beta^2 \gamma^2}{I} - \beta^2 \right]
$$
- **Análisis conceptual**:  
  - Dependencia con $z^2$: Partículas $\alpha$ pierden 4x más energía que protones.  
  - Mínimo en $\beta \gamma \approx 3$-4 (partículas mínimamente ionizantes).

---

#### **Unidad 7: Fisión y Fusión**
**Concepto central:** *Barrera de Coulomb y ignición termonuclear*  
**Herramienta matemática:** *Ecuaciones de Lawson y crítico de fisión*

1. **Condición de ignición (fusión)**:  
   $$
   n \tau > \frac{12 k T}{\langle \sigma v \rangle E_{\text{fusión}}}
   $$  
   - **Cálculo para DT**: $T \approx 15$ keV, $\langle \sigma v \rangle \approx 10^{-22}$ m³/s.

2. **Masa crítica (fisión)**:  
   - **Ecuación de difusión de neutrones**:  
     $$
     \nabla^2 \phi + B^2 \phi = 0, \quad B^2 = \frac{k_\infty - 1}{M^2}
     $$  
     - **Solución para esfera**: $B = \pi / R_{\text{crit}}$.

---

#### **Unidad 9: Partículas Elementales**
**Concepto central:** *Simetrías y modelo estándar*  
**Herramienta matemática:** *Grupos de Lie y diagramas de Feynman*

1. **Conservación de números cuánticos**:  
   - **Ejemplo**: Decaimiento $\beta$: $n \to p + e^- + \bar{\nu}_e$.  
     Verificar: $Q$, $L_e$, $B$, carga.

2. **Modelo de quarks**:  
   - **Wavefunction de protón**:  
     $$
     |p\rangle = \frac{1}{\sqrt{18}} \epsilon_{abc} \left( 2|u_a^\uparrow d_b^\downarrow u_c^\uparrow\rangle + \cdots \right)
     $$  
     - **Pedagogía**: Usar diagramas de Young para combinar momentos angulares de quarks.

---

### **Estrategia Pedagógica Integrada**
- **Problemas paradójicos**:  
  - *Paradoja del decaimiento $\alpha$*: ¿Por qué núcleos como $^{238}\text{U}$ emiten $\alpha$ si $Q > 0$ pero $^{112}\text{Sn}$ no? (Usar fórmula de Gamow).  
- **Simulaciones interactivas**:  
  - Geant4 para trayectorias de partículas en detectores.  
  - Python para ajustar espectros de decaimiento $\gamma$.  
- **Conexiones históricas**:  
  - Derivar la fórmula de Bethe-Bloch junto con el experimento de Anderson (1932) para rayos cósmicos.

---

**Próximo paso**: ¿Profundizamos en alguna unidad específica o continuamos con desarrollos matemáticos detallados?