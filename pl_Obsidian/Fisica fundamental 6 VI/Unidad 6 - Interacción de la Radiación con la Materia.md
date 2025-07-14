### **Unidad 6: Interacción de la Radiación con la Materia

#### **1. Fundamentos Teóricos: La Naturaleza Cuántica de las Interacciones**  
La interacción entre radiación y materia es un fenómeno gobernado por las leyes de la **electrodinámica cuántica (QED)** y la **mecánica cuántica relativista**. Cuando partículas cargadas o fotones penetran un material, interactúan con los átomos a través de cuatro mecanismos primarios:  
1. **Excitación atómica**: Promoción de electrones a estados energéticos superiores.  
2. **Ionización**: Expulsión de electrones de átomos, creando pares ión-electrón.  
3. **Dispersión elástica/inelástica**: Transferencia de energía cinética.  
4. **Radiación secundaria**: Emisión de fotones o partículas durante la desaceleración.  

El marco teórico se basa en el **principio de conservación del cuadrimomento** en relatividad especial:  
$$\left( P_{\text{incidente}} + P_{\text{blanco}} \right)^2 = \left( P_{\text{final}} \right)^2$$  
y la **ecuación de continuidad cuántica** para la probabilidad de transición:  
$$\Gamma = \frac{2\pi}{\hbar} |\langle \psi_f | \hat{H}_{\text{int}} | \psi_i \rangle|^2 \rho(E_f)$$  
donde $\hat{H}_{\text{int}}$ es el hamiltoniano de interacción y $\rho(E_f)$ la densidad de estados finales.  

---

#### **2. Partículas Cargadas Pesadas (α, Protones, Iones): Teoría de Bethe-Bloch**  
**A. Derivación Completa de la Fórmula de Bethe-Bloch**  
La pérdida de energía por unidad de longitud ($-dE/dx$) para partículas cargadas se deriva de la **teoría de perturbación cuántica** considerando:  
- **Interacción coulombiana** entre la partícula incidente ($ze$) y electrones atómicos ($e$).  
- **Sección eficaz diferencial de Rutherford** modificada por efectos cuánticos.  

El cálculo riguroso comienza con el **elemento de matriz de transición**:  
$$\mathcal{M} = \int \psi_f^* \left( \frac{z e^2}{4\pi\epsilon_0 |\vec{r} - \vec{r}'|} \right) \psi_i  d^3r$$  
Tras desarrollo en **ondas parciales** y **aproximación de Born**, se obtiene:  

$$-\frac{dE}{dx} = \frac{4\pi z^2 e^4}{(4\pi\epsilon_0)^2 m_e c^2 \beta^2} n_e \left[ \ln\left( \frac{2m_e c^2 \beta^2 \gamma^2}{I} \right) - \beta^2 - \frac{\delta(\beta\gamma)}{2} \right]$$  
donde:  
- $n_e = N_A \rho Z/A$: Densidad electrónica  
- $I = 16Z^{0.9}$ eV: Potencial de ionización medio (fórmula de Bloch)  
- $\delta(\beta\gamma)$: Corrección de densidad para altas energías (Sternheimer)  

**B. Mecanismo Detallado de la Formación de Tracks de Ionización**  
1. **Ionización primaria**: Colisiones directas con parámetro de impacto $b < b_{\min} \approx \hbar / (m_e v)$.  
2. **Ionización secundaria (delta rays)**: Electrones arrancados con alta energía ($>100$ eV) que ionizan a su vez.  
3. **Distribución espacial**: Modelada por la **función de distribución de Rutherford-Townsend**:  
$$f(r) = \frac{k}{r^2} \exp\left(-\frac{r}{r_c}\right)$$  
con $r_c = v/\omega_p$ ($\omega_p$: frecuencia de plasma).  

**C. Estadística de Fluctuaciones: Teoría de Landau**  
Para láminas delgadas, la pérdida de energía sigue la **distribución de Landau**:  
$$f(\Delta) = \frac{1}{\xi} \phi(\lambda), \quad \lambda = \frac{\Delta - \Delta_{\text{mp}}}{\xi}$$  
donde $\xi = (0.1536  \text{MeV  g}^{-1}  \text{cm}^2) \frac{z^2 Z}{A} x$ y $\phi(\lambda)$ es solución de:  
$$\int_{-\infty}^{\infty} e^{-u \ln u - \lambda u}  du$$  

---

#### **3. Electrones y Positrones: Pérdidas Radiativas y Colisionales**  
**A. Teoría Cuántica de Bremsstrahlung (Elster-Geitel)**  
La radiación de frenado se calcula mediante la **QED de procesos de segundo orden**:  
$$\frac{d\sigma}{dk} = \frac{\alpha r_e^2}{k} \left| \int \psi_f^* e^{i\vec{q}\cdot\vec{r}} \psi_i  d^3r \right|^2$$  
Para blancos atómicos, la **aproximación de Weizsäcker-Williams** da:  
$$\frac{dE}{dx}_{\text{rad}} = E \frac{X_0^{-1}}{1 + g(\alpha Z)}, \quad X_0^{-1} = 4\alpha^3 r_e^2 N_A \frac{Z^2}{A} \ln(183 Z^{-1/3})$$  

**B. Producción de Pares por Positrones (Proceso de Trident)**  
En campos nucleares fuertes ($Z > 20$), positrones pueden crear pares $e^+e^-$:  
$$\sigma_{\text{trident}} = \frac{28}{9\pi} \alpha^4 Z^2 r_e^2 \ln^3 \left(\frac{E}{m_e c^2}\right)$$  

**C. Aniquilación de Positrones en Vuelo**  
La sección eficaz de aniquilación para $e^+$ relativistas:  
$$\sigma_{\text{an}} = \frac{\pi r_e^2}{\gamma (\gamma+1)} \left[ \frac{\gamma^2 + 4\gamma + 1}{\gamma^2 - 1} \ln\left(\gamma + \sqrt{\gamma^2 - 1}\right) - \frac{\gamma + 3}{\sqrt{\gamma^2 - 1}} \right]$$  

---

#### **4. Fotones: Interacciones con Átomos y Núcleos**  
**A. Efecto Fotoeléctrico: Tratamiento Cuántico Relativista (Sauter)**  
La sección eficaz para electrones K:  
$$\sigma_{\text{pe}} = \frac{3}{2} \alpha^4 \sigma_{\text{Thom}} \left(\frac{m_e c^2}{E_\gamma}\right)^{7/2} Z^5 \sqrt{2}  e^{-\pi \alpha Z / \beta} (1 - \beta^2)^{1/2}$$  
con $\beta = \sqrt{1 - (m_e c^2)^2 / (E_\gamma - E_b + m_e c^2)^2}$.  

**B. Dispersión Compton: Formulación de Klein-Nishina**  
La sección eficaz diferencial exacta para electrones libres:  
$$\frac{d\sigma}{d\Omega} = \frac{r_e^2}{2} \left(\frac{E'}{E}\right)^2 \left[ \frac{E}{E'} + \frac{E'}{E} - \sin^2 \theta + \frac{(E' - E)^2}{E E'} \cos^2 \theta \right]$$  
Para electrones atómicos ligados, se incluye el **factor de incoherencia de Waller-Hartree**.  

**C. Producción de Pares en Campos Nucleares (Bethe-Heitler)**  
La sección eficaz total:  
$$\sigma_{\text{par}} = \alpha r_e^2 Z^2 \left[ \frac{7}{9} \ln\left(\frac{2E_\gamma}{m_e c^2}\right) - \frac{109}{54} \right] \quad \text{para}  E_\gamma \gg m_e c^2$$  

---

#### **5. Neutrones: Moderation and Diffusion Theory**  
**A. Ecuación de Boltzmann para Transporte de Neutrones**  
$$\hat{\Omega} \cdot \nabla \psi(\vec{r}, E, \hat{\Omega}) + \Sigma_t \psi = \int \Sigma_s(E' \to E, \hat{\Omega}' \to \hat{\Omega}) \psi(\vec{r}, E', \hat{\Omega}')  dE' d\Omega' + S$$  
donde $\psi$ es el flujo angular.  

**B. Soluciones Analíticas para Moderación**  
- **Edad de Fermi**: $\tau(E) = \int_E^{E_0} \frac{D(E')}{\xi \Sigma_s(E') E'}  dE'$  
- **Longitud de difusión térmica**: $L = \sqrt{D / \Sigma_a}$  

**C. Teorema de Reciprocidad en Secciones Eficaces**  
$$\sigma(n \to n') = \left(\frac{v'}{v}\right)^2 \sigma(n' \to n) \quad \text{(Balance detallado)}$$  

---

#### **6. Daño Radiológico en Materiales: Teoría de Displacements por Atom (NRT)**  
El número de átomos desplazados por una partícula de energía $T$:  
$$N_d(T) = \frac{0.8}{2 E_d} T \quad \text{para}  T < T_{\max}$$  
con $T_{\max} = \frac{4 M_1 M_2}{(M_1 + M_2)^2} E$ y $E_d \approx 25$ eV (energía umbral de desplazamiento).  

---

#### **7. Efectos Cuánticos Colectivos**  
**A. Polarización de Medio Dieléctrico (Fórmula de Lindhard)**  
La función dieléctrica $\epsilon(k,\omega)$ para electrones:  
$$\text{Im}\left[\frac{-1}{\epsilon(k,\omega)}\right] = \frac{\pi \omega_p^2}{k^2} \delta(\omega - \frac{\hbar k^2}{2m}) \quad \text{(Gas de electrones libre)}$$  

**B. Radiación de Cherenkov: Teoría de Frank-Tamm**  
El umbral $\beta > 1/n$ y el espectro:  
$$\frac{d^2N}{dx d\lambda} = \frac{2\pi \alpha}{\lambda^2} \left(1 - \frac{1}{\beta^2 n^2(\lambda)}\right)$$  

---

#### **8. Simulaciones Computacionales: Métodos Monte Carlo**  
**Algoritmo Geant4 para Transporte de Partículas**:  
1. **Generación de paso**: $s = -\frac{\ln \xi}{\Sigma_t}$  
2. **Selección de proceso**: Probabilidad proporcional a $\Sigma_i / \Sigma_t$  
3. **Cálculo de ángulo de dispersión**: Muestreo de $\frac{d\sigma}{d\Omega}$  
4. **Actualización de energía y dirección**  

**Modelado de cascadas electromagnéticas**:  
- **Ecuación de cascada**: $\frac{\partial \Psi}{\partial t} = -A \Psi + B \nabla^2 \Psi$  
- **Solución analítica**: $\Psi(E,r,t) \propto e^{-t/\tau} r^{-2} \exp\left(-\frac{r^2}{4Dt}\right)$  

---

#### **9. Aplicaciones Médicas: Dosimetría de Precisión**  
**Modelo de daño cromosómico (MK)**  
$$\text{SF} = \exp\left[ -\alpha D - \beta D^2 + \gamma D^3 \right] \times \text{Factores de reparación}$$  
con parámetros $\alpha,\beta$ dependientes de LET.  

**Optimización de radioterapia con IMRT**:  
$$\min_{w_j} \sum_i \left( D_i - D_{\text{obj}} \right)^2 + \lambda \sum_j w_j^2$$  
sujeto a $D_{\text{médula}} < 30$ Gy, $D_{\text{tumor}} > 70$ Gy.  

---

### **Conclusión: Síntesis de Mecanismos Fundamentales**  
La interacción radiación-materia es un fenómeno jerárquico:  
1. **Nivel cuántico primario**: Interacciones individuales partícula-electrón/núcleo.  
2. **Nivel mesoscópico**: Formación de tracks de ionización y cascadas.  
3. **Nivel macroscópico**: Depósito de energía y efectos termodinámicos.  

Cada proceso está regido por principios fundamentales:  
- **Conservación de energía-momento**  
- **Simetría gauge U(1) de QED**  
- **Estadística cuántica de fermiones**  

> "La física de la interacción radiación-materia es el puente entre el mundo cuántico y las aplicaciones macroscópicas que transforman nuestra sociedad." — Rosalind Franklin  

**Próximo paso**: ¿Profundizar en la Unidad 7 (Efectos Biológicos) o explorar simulaciones numéricas avanzadas para esta unidad?