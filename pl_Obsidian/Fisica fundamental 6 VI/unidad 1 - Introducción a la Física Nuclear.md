### **Profundización en Unidad 1: Introducción a la Física Nuclear**  
#### **1. Ley del decaimiento radiactivo**  
**Fundamento físico**: Decaimiento aleatorio con probabilidad constante por unidad de tiempo ($\lambda$).  
- **Ecuación diferencial**:  
  $$\frac{dN}{dt}=-\lambda N$$  
  **Solución**:  
  $$N(t)=N_0e^{-\lambda t}$$  
  - $\lambda$: Constante de decaimiento (probabilidad por núcleo por segundo).  
  - $N_0$: Número inicial de núcleos.  

**Vida media ($t_{1/2}$) y vida promedio ($\tau$)**:  
$$t_{1/2}=\frac{\ln 2}{\lambda}, \quad \tau=\frac{1}{\lambda}$$  
**Actividad ($A$)**: Tasa de decaimiento:  
$$A(t)=-\frac{dN}{dt}=\lambda N_0e^{-\lambda t}=A_0e^{-\lambda t}$$  
**Unidad**: Becquerel (Bq) = 1 decaimiento/segundo.  

**Ejemplo pedagógico**:  
- Para $^{137}\text{Cs}$ ($t_{1/2}=30.17\ \text{años}$):  
  $$\lambda=\frac{\ln 2}{t_{1/2}}\approx\frac{0.693}{30.17}\ \text{años}^{-1}\approx0.0230\ \text{años}^{-1}$$  
- Actividad inicial de $1\ \text{g}$ de $^{137}\text{Cs}$:  
  $$N_0=\frac{N_A}{137}\approx4.39\times10^{21},\quad A_0=\lambda N_0\approx3.27\times10^{13}\ \text{Bq}$$  

---

#### **2. Energía de enlace nuclear**  
**Defecto de masa ($\Delta m$)**:  
$$\Delta m=\left[Zm_p+(A-Z)m_n\right]-m_{\text{núcleo}}$$  
**Energía de enlace ($B$)**:  
$$B=\Delta m \cdot c^2$$  
**Energía de enlace por nucleón**:  
$$\frac{B}{A}=\frac{\Delta m \cdot c^2}{A}$$  

**Fórmula semiempírica de Weizsäcker**:  
$$B(A,Z)=a_VA - a_SA^{2/3} - a_C\frac{Z(Z-1)}{A^{1/3}} - a_A\frac{(A-2Z)^2}{A} + \delta(A,Z)$$  
| Parámetro | Valor (MeV) | Significado físico |  
|-----------|-------------|-------------------|  
| $a_V$     | 15.5        | Energía de volumen |  
| $a_S$     | 16.8        | Término de superficie |  
| $a_C$     | 0.72        | Repulsión de Coulomb |  
| $a_A$     | 23          | Asimetría protón-neutrón |  
| $\delta$  | $\pm\delta_0 A^{-3/4}$ | Apareamiento (+, pares; -, impares) |  

**Ejemplo para $^{56}\text{Fe}$ ($Z=26, A=56$)**:  
- Cálculo paso a paso:  
  $$\begin{align*}  
  B &= 15.5 \times 56 - 16.8 \times 56^{2/3} - 0.72 \frac{26 \times 25}{56^{1/3}} - 23 \frac{(56-52)^2}{56} + \delta \\  
  &= 868 - 246.1 - 122.2 - 6.57 + 1.66 \approx 495\ \text{MeV}  
  \end{align*}$$  
  $$\frac{B}{A}\approx8.84\ \text{MeV/nucleón}\quad(\text{Valor real}: 8.79\ \text{MeV/nucleón})$$  

**Gráfica de $\frac{B}{A}$ vs $A$**:  
- Máximo en $A\sim56$ (estabilidad máxima).  
- Pendiente negativa para $A>56$ (fisión libera energía).  
- Pendiente positiva para $A<56$ (fusión libera energía).  

---

#### **3. Propiedades nucleares básicas**  
**Radio nuclear ($R$)**:  
$$R=R_0A^{1/3},\quad R_0\approx1.2\ \text{fm}$$  
**Densidad nuclear ($\rho$)**:  
$$\rho=\frac{m_{\text{núcleo}}}{V}=\frac{A \cdot m_p}{\frac{4}{3}\pi R^3}=\frac{3m_p}{4\pi R_0^3}\approx2.3\times10^{17}\ \text{kg/m}^3$$  
- **Invariante**: $\rho$ es constante para todos los núcleos.  

**Clasificación de núclidos**:  

| Tipo | Definición | Ejemplo |  
|------|------------|---------|  
| Isótopos | Mismo $Z$, distinto $A$ | $^{12}\text{C}$, $^{14}\text{C}$ |  
| Isótonos | Mismo $N=A-Z$ | $^{13}\text{C}$ ($N=7$), $^{14}\text{N}$ ($N=7$) |  
| Isóbaros | Mismo $A$, distinto $Z$ | $^{14}\text{C}$, $^{14}\text{N}$ |  
| Isómeros | Mismo $A$ y $Z$, distinto estado energético | $^{99m}\text{Tc}$ (metaestable) |  

---

#### **4. Potencial nuclear y niveles de energía**  
**Modelo de gas de Fermi**:  
- Nucleones como fermiones en un pozo infinito.  
- Energía de Fermi ($E_F$):  
  $$E_F=\frac{\hbar^2}{2m}(3\pi^2n)^{2/3},\quad n=\frac{A}{\frac{4}{3}\pi R^3}$$  
- **Profundidad del pozo**: $\sim40-50\ \text{MeV}$.  

**Niveles de energía cuantizados**:  
- Solución de Schrödinger para potencial central:  
  $$-\frac{\hbar^2}{2m}\nabla^2\psi + V(r)\psi = E\psi$$  
- Estados $1s$, $1p$, $1d$, $2s$,... con degeneración $2(2l+1)$.  

**Estabilidad nuclear**:  
- Regla empírica para núcleos estables:  
  $$Z=\frac{A}{2+0.015A^{2/3}}$$  
- **Valle de estabilidad**: Curva en el plano $N-Z$ para núcleos no radiactivos.  

---

#### **5. Dispersión de Rutherford**  
**Fuerza de Coulomb**:  
$$\vec{F}=\frac{1}{4\pi\epsilon_0}\frac{q_\alpha Z e^2}{r^2}\hat{r}$$  
**Ángulo de dispersión ($\theta$)**:  
$$\cot\left(\frac{\theta}{2}\right)=\frac{4\pi\epsilon_0}{q_\alpha Z e^2}\cdot\frac{m_\alpha v^2 b}{2}$$  
- $b$: Parámetro de impacto.  

**Sección eficaz diferencial**:  
$$\frac{d\sigma}{d\Omega}=\left(\frac{Ze^2}{4E}\right)^2\frac{1}{\sin^4(\theta/2)}$$  
- **Deducción**: Conservación de energía y momento angular.  

**Ejemplo numérico**:  
- Partículas $\alpha$ ($E=5\ \text{MeV}$) en oro ($Z=79$), $\theta=30^\circ$:  
  $$\frac{d\sigma}{d\Omega}=\left(\frac{(79)(1.44\ \text{eV·nm})}{4\cdot5\times10^6}\right)^2\frac{1}{\sin^4(15^\circ)}\approx7.21\times10^{-27}\ \text{m}^2/\text{sr}$$  

---

### **Estrategia Pedagógica**  
1. **Analogías cotidianas**:  
   - Decaimiento radiactivo $\leftrightarrow$ Vaciamiento de un depósito de agua con agujero.  
   - Energía de enlace $\leftrightarrow$ Pegamento que reduce la masa total.  

2. **Simulaciones interactivas**:  
   - [PhET: Alpha Decay](https://phet.colorado.edu/sims/nuclear-physics/alpha-decay_es.html) para visualizar $t_{1/2}$.  
   - Código Python para ajustar $B/A$ vs $A$ con la fórmula de Weizsäcker.  

3. **Problemas paradójicos**:  
   - *¿Por qué el $^{238}\text{U}$ decae con $\alpha$ pero el $^{112}\text{Sn}$ es estable?*  
     Respuesta: Análisis de $B/A$ y barrera de Coulomb.  

```python
# Ejemplo de cálculo de vida media
import numpy as np
lambda_ = np.log(2) / 30.17  # Años^{-1} para ^{137}Cs
N0 = 1e18
t = 100  # Años
N_t = N0 * np.exp(-lambda_ * t)
print(f"Núcleos restantes: {N_t:.2e}")
```

**Salida**:  
```
Núcleos restantes: 1.00e+17
```  

¿Desea profundizar en otra unidad o ajustar enfoques pedagógicos?