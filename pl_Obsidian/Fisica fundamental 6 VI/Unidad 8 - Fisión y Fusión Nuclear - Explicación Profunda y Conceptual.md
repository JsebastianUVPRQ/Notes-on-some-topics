
#### **1. Fundamentos Termodinámicos de la Estabilidad Nuclear**  
**Mecanismo físico:**  
Los núcleos atómicos son sistemas cuánticos gobernados por la **competencia entre la fuerza nuclear fuerte** (atracción de corto alcance entre nucleones) y la **repulsión coulombiana** (entre protones). La energía de enlace por nucleón ($B/A$) sigue una curva característica:  
- **Máximo en hierro-56** ($\sim$8.8 MeV/nucleón): Núcleos más estables.  
- **Decrecimiento para $A>56$:** Predominio de repulsión coulombiana → fisión libera energía.  
- **Decrecimiento para $A<56$:** Predominio de efectos de superficie → fusión libera energía.  

**Ecuación de Weizsäcker:**  
$$\frac{B}{A} = \underbrace{15.85}_{\text{Volumen}} - \underbrace{18.34 \ A^{-1/3}}_{\text{Superficie}} - \underbrace{0.71 \ Z^2 A^{-4/3}}_{\text{Coulomb}} - \underbrace{23.21 \frac{(A-2Z)^2}{A^2}}_{\text{Asimetría}} + \delta(A,Z)$$  
- **$\delta$:** Término de apareamiento ($+$ para pares, $-$ para impares).  
- **Ejemplo numérico:** Para ${}^{235}\text{U}$ ($Z=92,A=235$):  
  $$\frac{B}{A} \approx 7.6 \ \text{MeV/nucleón} < 8.8 \ \text{(Fe)} \ \Rightarrow \ \text{Inestable}$$  

---

#### **2. Teoría Cuántica de la Fisión**  
**Modelo de la gota líquida (Bohr-Wheeler):**  
1. **Deformación nuclear:** El núcleo se deforma como una gota cargada.  
2. **Energía de deformación:**  
   $$E_{\text{def}}(\beta) = \frac{1}{2} C_2 \beta^2 + \frac{1}{3} C_3 \beta^3 + \cdots$$  
   - $C_2 = \frac{3}{5} \frac{Z^2 e^2}{R} - \frac{1}{2} a_S A^{2/3}$ (**coeficiente de rigidez**).  
   - Si $C_2 < 0$ → **inestabilidad a deformaciones**.  

**Barrera de fisión:**  
- **Altura ($E_f$):**  
  $$E_f = \frac{0.83 \ Z^2 e^2}{4\pi\epsilon_0 R} \left(1 - \frac{Z^2}{48.1 \ A}\right)$$  
  Para ${}^{235}\text{U}$: $E_f \approx 6.2 \ \text{MeV}$.  
- **Túnel cuántico (WKB):**  
  $$P_{\text{túnel}} = \exp\left[ -\frac{2\sqrt{2\mu}}{\hbar} \int_{R_0}^{R_{\text{sc}}} \sqrt{V(r) - Q}  dr \right]$$  
  $R_{\text{sc}} \approx 1.5 R_0$: Radio de scission (separación en fragmentos).  

---

#### **3. Fisión Inducida por Neutrones**  
**Mecanismo detallado:**  
1. **Captura neutrónica:**  
   $$n + {}^{235}\text{U} \to {}^{236}\text{U}^* \quad (\text{núcleo compuesto excitado})$$  
2. **Modos de decaimiento:**  
   - **Fisión ($\sim 85\%$):** Vibraciones colectivas superan barrera.  
   - **Emisión $\gamma$ ($\sim 15\%$):** Desexcitación radiativa.  

**Sección eficaz resonante (Breit-Wigner):**  
$$\sigma_f(E_n) = \frac{\pi \hbar^2}{2\mu E_n} \frac{\Gamma_n \Gamma_f}{(E_n - E_R)^2 + (\Gamma/2)^2}$$  
- $\Gamma_n$: Anchura de captura neutrónica.  
- $\Gamma_f$: Anchura de fisión.  
- **Ejemplo:** Para $E_n = 0.025 \ \text{eV}$ (neutrones térmicos), $\sigma_f({}^{235}\text{U}) = 585 \ \text{b}$ (barns).  

---

#### **4. Reactores de Fisión: Física de Criticalidad**  
**Ecuación de difusión de neutrones:**  
$$\frac{1}{v} \frac{\partial \phi}{\partial t} = D \nabla^2 \phi - \Sigma_a \phi + k_\infty \Sigma_a \phi$$  
- $D = \frac{1}{3\Sigma_{\text{tr}}}$: Coeficiente de difusión.  
- $\Sigma_a$: Sección eficaz macroscópica de absorción.  

**Factor de multiplicación efectivo ($k_{\text{eff}}$):**  
$$k_{\text{eff}} = \eta \cdot \epsilon \cdot p \cdot f \cdot P_{\text{no fuga}}$$  
- **$\eta = \nu \frac{\Sigma_f}{\Sigma_a^{\text{comb}}}$:** Neutrones generados por absorción (${}^{235}\text{U}$: $\eta \approx 2.07$).  
- **Geometría crítica:**  
  $$B_g^2 = \left( \frac{\pi}{R_{\text{crit}}} \right)^2 = \frac{k_\infty - 1}{M^2}, \quad M^2 = L^2 + \tau$$  
  $L$: Longitud de difusión, $\tau$: Edad de Fermi.  

---

#### **5. Fusión Termonuclear: Física de Plasmas**  
**Condición de Lawson (ignición):**  
$$n \tau_E > \frac{12 \ k_B T}{\langle \sigma v \rangle \ E_{\text{fusión}}}$$  
- **Para DT (deuterio-tritio):**  
  $$n \tau_E > 10^{20} \ \text{s/m}^3, \quad T > 10 \ \text{keV}$$  

**Sección eficaz de fusión (Gamow):**  
$$\sigma(E) = \frac{S(E)}{E} e^{-\sqrt{E_G/E}} \quad \text{con} \quad E_G = (\pi \alpha Z_a Z_X)^2 \ 2 \mu c^2$$  
- $S(E)$: Factor astrofísico (extrapolado experimentalmente).  

**Tasa de reacción en plasma:**  
$$\langle \sigma v \rangle = \sqrt{\frac{8}{\pi \mu}} \frac{1}{(k_B T)^{3/2}} \int_0^\infty \sigma(E) \ E \ e^{-E/k_B T}  dE$$  
- **Ejemplo DT a 15 keV:** $\langle \sigma v \rangle \approx 10^{-22} \ \text{m}^3/\text{s}$.  

---

#### **6. Confinamiento Magnético: Tokamaks**  
**Ecuaciones de equilibrio MHD:**  
1. **Balance de fuerzas:**  
   $$\nabla p = \vec{J} \times \vec{B}$$  
2. **Estabilidad kink (criterio de Kruskal-Shafranov):**  
   $$q(r) = \frac{r B_T}{R B_P} > 1$$  
   - $q$: Factor de seguridad, $B_T$: Campo toroidal, $B_P$: Campo poloidal.  

**Pérdidas de energía:**  
- **Conductividad térmica neoclásica:**  
  $$\chi \propto \frac{\rho_i^2 \nu_{ii}}{a^2} \quad (\rho_i: \text{radio de Larmor}, \nu_{ii}: \text{frecuencia de colisión})$$  

---

#### **7. Fusión Inercial: Física de Implosiones**  
**Ecuación de cohete (implosión simétrica):**  
$$\frac{d u_s}{d t} = -\frac{1}{\rho} \frac{\partial p}{\partial r}$$  
- **Compresión adiabática:**  
  $$p \rho^{-\gamma} = \text{const.}, \quad \gamma = 5/3 \ \text{(gas ideal)}$$  

**Criterio de ignición:**  
$$\rho R > 0.3 \ \text{g/cm}^2 \quad \text{para} \ T > 5 \ \text{keV}$$  

---

#### **8. Nucleosíntesis Estelar**  
**Cadena protón-protón (Sol):**  
1. **Fusión $p+p$:**  
   $$p + p \to d + e^+ + \nu_e + 1.44 \ \text{MeV} \quad (\tau \sim 10^9 \ \text{años})$$  
2. **Reacción dominante:**  
   $${}^3\text{He} + {}^3\text{He} \to {}^4\text{He} + 2p + 12.86 \ \text{MeV}$$  

**Proceso triple-$\alpha$ (estrellas masivas):**  
$${}^4\text{He} + {}^4\text{He} \leftrightarrow {}^8\text{Be} \quad (Q = -92 \ \text{keV})$$  
$${}^8\text{Be} + {}^4\text{He} \to {}^{12}\text{C}^* \quad (\text{Estado de Hoyle})$$  
$${}^{12}\text{C}^* \to {}^{12}\text{C} + \gamma + 7.65 \ \text{MeV}$$  

---

#### **9. Simulaciones Computacionales**  
**Transporte de neutrones (Ecuación de Boltzmann):**  
$$\hat{\Omega} \cdot \nabla \psi(\vec{r},E,\hat{\Omega}) + \Sigma_t \psi = \int \Sigma_s(E' \to E, \hat{\Omega}' \to \hat{\Omega}) \psi  dE' d\Omega' + S$$  
- $\psi$: Flujo angular de neutrones.  

---

### **Conclusión: El Ciclo Energético Cósmico**  
La fisión y fusión son procesos complementarios en el universo:  
- **Fusión:** Sintetiza elementos hasta el hierro en estrellas.  
- **Fisión:** Recicla elementos pesados en supernovas.  

**Balance energético fundamental:**  
$$\mathcal{F} = \underbrace{\frac{E_{\text{liberada}}}{E_{\text{invertida}}}}_{\text{Ganancia}} \times \underbrace{\tau_{\text{confinamiento}}}_{\text{Eficiencia}}$$  
- **Fusión comercial:** $\mathcal{F} > 10^{14} \ \text{keV·s/m}^3$ (ITER: $\mathcal{F} \sim 5 \times 10^{13}$).  
- **Núcleo solar:** $\mathcal{F} \sim 10^{21} \ \text{keV·s/m}^3$.  

> "La energía nuclear es la respuesta definitiva a la paradoja de Kardashev: dominar la energía de las estrellas en la Tierra." — Freeman Dyson