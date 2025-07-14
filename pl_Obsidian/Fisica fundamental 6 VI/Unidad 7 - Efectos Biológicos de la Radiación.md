### **Unidad 7: Efectos Biológicos de la Radiación y Aplicaciones**  
#### **1. Fundamentos Físico-Químicos de la Interacción Radiación-Materia Viva**  
La interacción de la radiación ionizante con sistemas biológicos inicia con procesos físicos que generan **especies reactivas** capaces de alterar biomoléculas críticas. La secuencia de eventos sigue una jerarquía temporal:  

**A. Fase Física (10⁻¹⁸ - 10⁻¹⁵ s)**:  
- Depósito de energía mediante ionización/excitación atómica.  
- **Producción de pares ión-electrón**:  
  $$N_{\text{pares}} = \frac{E_{\text{absorbida}}}{W} \quad \text{con} \quad W \approx 33.85  \text{eV/par (agua)}$$  

**B. Fase Fisicoquímica (10⁻¹⁵ - 10⁻¹² s)**:  
- Disociación de moléculas de agua:  
  $$\text{H}_2\text{O} \xrightarrow{\text{radiación}} \text{H}_2\text{O}^+ + e^- \to \text{H}^+ + \bullet\text{OH}$$  
- Formación de radicales libres: $\bullet\text{OH}$, $\text{H}\bullet$, $\text{e}_{aq}^-$  

**C. Fase Química (10⁻¹² - 10⁻⁶ s)**:  
- Reacciones de radicales con biomoléculas:  
  $$\bullet\text{OH} + \text{ADN} \to \text{daño oxidativo}$$  
  $$\text{e}_{aq}^- + \text{O}_2 \to \text{O}_2^{\bullet-}  \text{(superóxido)}$$  

**D. Fase Biológica (segundos - años)**:  
- Alteración de funciones celulares: ruptura de cadenas de ADN, peroxidación lipídica, inactivación enzimática.  

---

#### **2. Dosimetría de Radiación: Cuantificación del Daño**  
**A. Magnitudes Fundamentales**:  
1. **Dosis Absorbida ($D$)**:  
   $$D = \frac{d\bar{\epsilon}}{dm}  \quad [\text{Gray} = 1  \text{J/kg}]$$  
2. **Dosis Equivalente ($H_T$)**:  
   $$H_T = \sum_R w_R \cdot D_{T,R}  \quad [\text{Sievert}]$$  
   $w_R$: Factor de ponderación (α=20, γ=1, n=5-20)  
3. **Dosis Efectiva ($E$)**:  
   $$E = \sum_T w_T \cdot H_T$$  
   $w_T$: Factor de tejido (médula=0.12, tiroides=0.04)  

**B. Modelo de Depósito de Energía**:  
- **Ecuación de Bethe para tejidos blandos**:  
  $$-\frac{dE}{dx} = 0.307 \frac{z^2}{\beta^2} \rho \left( \ln \frac{2m_e c^2 \beta^2}{I} - \beta^2 \right)  \text{MeV/cm}$$  
  con $I = 75.7  \text{eV}$ para tejido muscular.  

---

#### **3. Mecanismos de Daño al ADN**  
**A. Tipos de Lesiones**:  
1. **Rupturas simple cadena (SSB)**:  
   - Reparables por vía BER (Base Excision Repair)  
2. **Rupturas doble cadena (DSB)**:  
   - Críticas para supervivencia celular  
   - **Probabilidad de inducción**:  
     $$P_{\text{DSB}} = \alpha D + \beta D^2$$  
     $\alpha$: Daño directo, $\beta$: Daño indirecto por radicales  

**B. Modelo de Mecanoquímica de Rotura**:  
- **Fuerza requerida para ruptura de enlace fosfodiéster**:  
  $$F_{\text{ruptura}} = \frac{\partial U}{\partial r} \approx 1.5  \text{nN}$$  
  - Radiación reduce la barrera energética: $U_{\text{efectiva}} = U_0 - k D$  

**C. Curvas de Supervivencia Celular (Modelo LQ)**:  
$$S = e^{-\alpha D - \beta D^2}$$  
- $\alpha/\beta$: Radio de letalidad intrínseca (tumores: 10 Gy, tejidos sanos: 3 Gy)  

---

#### **4. Efectos Sistémicos y Determinísticos vs. Estocásticos**  
**A. Efectos Determinísticos (Umbral Dependiente)**:  
| Síndrome | Dosis (Gy) | Mecanismo |  
|----------|------------|-----------|  
| **Hematopoyético** | 1-2 | Destrucción de médula ósea |  
| **Gastrointestinal** | 6-10 | Apoptosis de células epiteliales |  
| **Neurovascular** | >20 | Edema cerebral |  

**B. Efectos Estocásticos (Sin Umbral)**:  
- **Modelo de Riesgo de Cáncer**:  
  $$\text{Riesgo} = \lambda_0 + \epsilon D e^{-\gamma D}$$  
  $\lambda_0$: Tasa basal, $\epsilon = 5\%  \text{por Sv}$ (ICRP)  

---

#### **5. Radioterapia de Precisión**  
**A. Braquiterapia**:  
- **Ecuación de dosimetría puntual (Ley inversa)**:  
  $$D(r) = S_k \cdot \Lambda \cdot \frac{G(r)}{G(r_0)} \cdot g(r)$$  
  $S_k$: Intensidad de fuente, $\Lambda$: Constante de dosis  

**B. Radioterapia Externa (IMRT/VMAT)**:  
- **Optimización convexa**:  
  $$\min_D \sum_i w_i (D_i - T_i)^2 + \lambda \|\nabla D\|^2$$  
  Sujeto a:  
  $$D_{\text{médula}} < 45  \text{Gy}, \quad D_{\text{CTV}} > 70  \text{Gy}$$  

**C. Terapia con Partículas (Protones/Carbon)**:  
- **Ventaja física (Pico de Bragg)**:  
  $$D(x) = D_0 e^{-\mu x} + \Phi \cdot \frac{dE}{dx}(x_{\text{max}})$$  
  - **LET (Linear Energy Transfer) óptimo**: 100-200 keV/μm  

---

#### **6. Medicina Nuclear: Diagnóstico por Imágenes**  
**A. Tomografía por Emisión de Positrones (PET)**:  
- **Reconstrucción 3D (Transformada de Radon inversa)**:  
  $$f(x,y,z) = \int_0^\pi \int_{-\infty}^\infty R_{\phi}(p,z) e^{2\pi i p x_\phi} |p|  dp  d\phi$$  
  $x_\phi = x\cos\phi + y\sin\phi$  

**B. Dosimetría Interna (Modelo MIRD)**:  
- **Dosis absorbida en órgano $r_k$**:  
  $$D(r_k) = \sum_h \tilde{A}_h \cdot S(r_k \leftarrow r_h)$$  
  $\tilde{A}_h = \int_0^\infty A_h(t)  dt$: Actividad acumulada  

---

#### **7. Radioprotección: Principios ALARA**  
**A. Ecuación de Blindaje**:  
- Para fotones:  
  $$I = I_0 B e^{-\mu x} + \frac{S}{\mu} (1 - e^{-\mu x})$$  
  $B$: Factor de acumulación, $S$: Fuentes dispersas  

**B. Límites de Dosis (ICRP 103)**:  
| Grupo | Límite efectivo anual (mSv) |  
|-------|-----------------------------|  
| Público | 1 |  
| Ocupacional | 50 |  

**C. Modelo de Riesgo Integral**:  
$$\text{RR} = \exp\left[ \beta_0 + \beta_1 D + \beta_2 D^2 \right] \cdot \text{EF}(a,s)$$  
$\text{EF}$: Factores edad/sexo  

---

#### **8. Aplicaciones Industriales y Agrícolas**  
**A. Esterilización por Radiación**:  
- **Dosis de inactivación microbiana**:  
  $$D_{10} = \frac{2.303}{k} \quad (k = 0.23  \text{min}^{-1} \text{ para E. coli})$$  

**B. Mutagénesis en Agricultura**:  
- **Tasa de mutación inducida**:  
  $$\lambda_m = \alpha + \beta \ln D$$  
  - Ejemplo: Arroz "Atomita 2" (dosis óptima 200 Gy)  

---

### **Conclusión: La Dualidad Beneficio-Riesgo**  
Los efectos biológicos de la radiación emergen de procesos cuánticos que escalan a daño macroscópico mediante cascadas bioquímicas no lineales. El desafío científico reside en explotar la **selectividad energética** para terapia mientras se minimizan riesgos estocásticos, gobernados por la relación:  
$$\text{Beneficio terapéutico} \propto \frac{\text{LET}_{\text{tumor}}}{\text{LET}_{\text{tejido sano}}} \cdot e^{-\Delta \alpha D}$$  

> "En radiobiología, la diferencia entre veneno y cura es solo una cuestión de dosis y precisión." — Hermann Joseph Muller  

**Próximo paso**: ¿Profundizar en modelos de reparación de ADN o avanzar a la Unidad 8 (Fisión y Fusión)?
