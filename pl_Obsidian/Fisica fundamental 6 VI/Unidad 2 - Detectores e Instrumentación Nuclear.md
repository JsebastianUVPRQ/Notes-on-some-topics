### **Unidad 2: Detectores e Instrumentación Nuclear**  
#### **Introducción Conceptual**  
La detección de radiación nuclear constituye la piedra angular de la física experimental nuclear y de partículas. Esta unidad explora los principios físicos, diseño y operación de los instrumentos que permiten observar y cuantificar fenómenos nucleares. Cada detector transforma la energía depositada por partículas cargadas o fotones en señales medibles, aprovechando interacciones fundamentales con la materia: ionización, excitación atómica o reacciones nucleares. La elección del detector depende críticamente del tipo de radiación, el rango energético y la información requerida (energía, tiempo, identidad de partícula).  

---

#### **1. Detectores de Gas: De la Ionización Básica a la Avalancha**  
**Fundamento Físico**: Cuando partículas cargadas ($\alpha$, $\beta$, iones) atraviesan un gas, arrancan electrones de los átomos, creando pares ión-electrón. Un campo eléctrico aplicado entre electrodos (cátodo y ánodo) acelera estos portadores, generando una señal eléctrica medible.  

**Regímenes de Operación**:  
1. **Cámara de Ionización** (Bajo voltaje: 50-300 V):  
   - No hay multiplicación de carga: cada par ión-electrón produce un pulso primario.  
   - La carga total recolectada es:  
     $$Q = \frac{E}{W} \cdot e$$  
     donde $E$ = energía depositada, $W$ = energía promedio para crear un par (30-35 eV para aire), $e$ = carga del electrón.  
   - *Ejemplo*: Una partícula $\alpha$ de 5 MeV en aire ($W$ = 35 eV) crea $\sim$142,857 pares, generando $Q \approx 2.3 \times 10^{-14}$ C.  

2. **Contador Proporcional** (Medio voltaje: 300-1000 V):  
   - Los electrones primarios ganan suficiente energía para ionizar átomos adicionales, iniciando una *avalancha* controlada.  
   - La ganancia $M$ sigue la **ecuación de Townsend**:  
     $$M = e^{\alpha d}$$  
     $\alpha$ = coeficiente de ionización (depende del gas y campo eléctrico), $d$ = distancia al ánodo.  
   - La señal amplificada ($10^3$-$10^4$ veces) permite detectar partículas de baja energía (rayos X, electrones).  

3. **Contador Geiger-Müller** (Alto voltaje: >1000 V):  
   - La avalancha se propaga por todo el volumen activo, produciendo pulsos grandes e independientes de la energía inicial.  
   - Requiere gas de "apagado" (halógenos, alcohol) para absorber fotones UV y detener la descarga.  
   - **Tiempo muerto ($\tau$)**: Período de inactividad post-detección ($\sim$100 $\mu$s). La actividad real se corrige como:  
     $$A_{\text{real}} = \frac{A_{\text{obs}}}{1 - A_{\text{obs}} \tau}$$  

**Aplicaciones**:  
- Cámaras de ionización: Dosimetría médica, detectores de humo.  
- Geiger-Müller: Monitoreo radiológico portátil.  

---

#### **2. Detectores de Centelleo: De la Luz a la Señal Electrónica**  
**Principio de Funcionamiento**: Ciertos materiales (cristales, plásticos, líquidos) emiten luz visible (**centelleo**) cuando la radiación deposita energía. Esta luz se convierte en señal eléctrica mediante fotomultiplicadores o fotodiodos.  

**Tipos y Mecanismos**:  
- **Centelleadores Inorgánicos** (Ej: NaI(Tl), CsI(Tl)):  
  - Mecanismo: Transiciones de banda de valencia a banda de conducción en cristales.  
  - Alta eficiencia para rayos $\gamma$ debido al alto $Z$.  
  - Número de fotones producidos:  
    $$N_{\text{fotones}} = \frac{E}{E_{\text{fotón}}} \cdot \text{CE}$$  
	CE = Coeficiente de conversión ($\sim15\%$ para NaI(Tl) , $E_{\text{fotón}} \approx 3$ eV.  
    *Ejemplo*: $\gamma$ de 662 keV ($^{137}\text{Cs}$) produce $\sim$33,100 fotones.  

- **Centelleadores Orgánicos** (Ej: plásticos, antraceno):  
  - Mecanismo: Transiciones electrónicas en moléculas orgánicas.  
  - Rápidos tiempos de respuesta ($\sim$ns), ideales para medidas de tiempo.  

**Eficiencia y Resolución**:  
- **Eficiencia geométrica ($\epsilon_g$)**: Fracción de fotones que alcanzan el fotocátodo.  
- **Eficiencia cuántica ($\epsilon_q$)**: Fracción de fotones que producen electrones en el fotocátodo ($\sim$20-30%).  
- **Resolución energética**:  
  $$\text{Res} = \frac{\Delta E}{E} \approx 2.35 \sqrt{\frac{F}{N_{\text{fotones}}}} \times 100\%$$  
  $F$ = factor de Fano. Para NaI(Tl) a 662 keV, Res $\approx$ 7-8%.  

**Aplicaciones**:  
- Espectrometría $\gamma$ (NaI(Tl)), tomografía PET (centelleadores rápidos).  

---

#### **3. Detectores Semiconductores: Precisión Cuántica**  
**Física Subyacente**: Radiación ionizante crea pares electrón-hueco en la banda prohibida de semiconductores (Si, Ge). Un campo eléctrico ($>$1000 V/cm) separa los portadores, generando corriente.  

**Ventaja Crítica**: Baja energía para crear un par ($W_{\text{Si}} = 3.6$ eV, $W_{\text{Ge}} = 2.85$ eV), lo que permite alta resolución energética.  

**Tipos de Detectores**:  
1. **Detectores de Barrera Superficial (Si)**:  
   - Para partículas cargadas ($\alpha$, protones).  
   - Resolución típica: 1-2 keV a 5.8 MeV ($\alpha$ de $^{241}\text{Am}$).  

2. **Detectores de Germanio Hiperpuro (HPGe)**:  
   - Para espectrometría $\gamma$ de alta resolución.  
   - Resolución: <2 keV a 1.33 MeV ($^{60}\text{Co}$).  
   - Requieren refrigeración criogénica (77 K) para reducir ruido térmico.  

**Resolución Energética**:  
$$\Delta E = 2.35 \sqrt{F \cdot W \cdot E}$$  
- $F$ = 0.12 (Si), 0.08 (Ge).  
- *Ejemplo*: HPGe a 1.33 MeV: $\Delta E \approx 1.8$ keV (FWHM).  

**Aplicaciones**:  
- Análisis de huellas nucleares (Si), arqueometría (HPGe).  

---

#### **4. Detectores de Neutrones: Captura Nuclear**  
**Desafío Único**: Neutrones no ionizan directamente; requieren reacciones nucleares que produzcan partículas cargadas secundarias.  

**Principales Técnicas**:  
1. **Detectores de $^3\text{He}$**:  
   - Reacción: $n + {}^3\text{He} \rightarrow p + {}^3\text{H} + 764\ \text{keV}$.  
   - Alta sección eficaz para neutrones térmicos (5330 b).  

1. **Detectores de BF$_3$**:  
   - Reacción: $n + {}^{10}\text{B} \rightarrow \alpha + {}^{7}\text{Li} + 2.31\ \text{MeV}$.  

1. **Centelleadores con $^6\text{Li}$ o $^{10}\text{B}$**:  
   - Partículas $\alpha$ producidas generan centelleo.  

**Eficiencia ($\epsilon$)**:  
$$\epsilon = 1 - e^{-\Sigma \cdot d}$$  
$\Sigma$ = sección eficaz macroscópica, $d$ = espesor del material.  

**Aplicaciones**:  
- Monitoreo en reactores nucleares, seguridad de material radiactivo.  

---

#### **5. Identificación de Partículas: Técnicas $\Delta E-E$**  
**Fundamento**: Partículas diferentes con igual energía cinética pierden energía ($dE/dx$) de modo distintivo al atravesar materia.  

**Ecuación de Bethe-Bloch**:  
$$-\frac{dE}{dx} = K z^2 \frac{Z}{A} \frac{1}{\beta^2} \left[ \ln \frac{2m_e c^2 \beta^2 \gamma^2}{I} - \beta^2 \right]$$  
- $z$: Carga de la partícula incidente, $\beta = v/c$.  

**Técnica $\Delta E-E$**:  
1. Un detector delgado mide $\Delta E$ (proporcional a $z^2/\beta^2$).  
2. Un detector grueso mide $E_{\text{residual}}$.  
3. La relación $\Delta E \cdot E \propto M z^2$ identifica la partícula.  

*Ejemplo experimental*:  

| Partícula | $\Delta E$ (MeV/cm) | $E$ (MeV) |  
|-----------|----------------------|------------|  
| Protón    | 80                   | 10         |  
| Deuteron  | 160                  | 10         |  
| Partícula $\alpha$ | 640          | 10         |  

---

#### **6. Aceleradores de Partículas: Ingeniería de Altas Energías**  
**Ciclotrón**:  
- Partículas circulan en campo magnético estático $B$.  
- Frecuencia de resonancia:  
  $$f_{\text{RF}} = \frac{qB}{2\pi m}$$  
- Energía máxima:  
  $$E_{\text{max}} = \frac{(q B R)^2}{2m}$$  
  $R$ = radio máximo del haz.  

**Sincrotrón**:  
- Campo magnético $B$ y frecuencia RF aumentan sincrónicamente con la energía.  
- Energías alcanzadas: TeV (LHC: $E_p = 6.5$ TeV).  

**Aplicaciones**:  
- Producción de radioisótopos médicos (ciclotrón), investigación de física de partículas (sincrotrón).  

---

#### **Experimentos Esenciales**  
**1. Espectroscopía $\gamma$ con NaI(Tl)**:  
- Calibración energética usando fuentes estándar (${137}\text{Cs}$: 662 keV, $^{60}\text{Co}$: 1173/1332 keV).  
- Identificación de picos: Fotopico, Compton, retrodispersión.  

**2. Efecto Compton**:  
- Energía del electrón de retroceso:  
  $$E_e = E_\gamma \frac{\alpha (1-\cos\theta)}{1 + \alpha (1-\cos\theta)}, \quad \alpha = \frac{E_\gamma}{m_e c^2}$$  
- Distribución angular:  
  $$\frac{d\sigma}{d\Omega} \propto \left( \frac{E'}{E_\gamma} \right)^2 \left( \frac{E_\gamma}{E'} + \frac{E'}{E_\gamma} - \sin^2\theta \right)$$  

---

#### **Conclusión Pedagógica**  
La instrumentación nuclear ejemplifica la aplicación directa de principios cuánticos y electromagnéticos en dispositivos prácticos. Cada detector representa una solución ingeniosa para transformar fenómenos subatómicos en datos cuantificables, permitiendo explorar desde la estructura nuclear hasta las partículas elementales. El diseño experimental requiere comprender las fortalezas y limitaciones de cada tecnología: resolución energética, eficiencia, tiempo muerto y selectividad.  

**Próximo paso**: ¿Profundizar en otra unidad o ajustar enfoques pedagógicos?