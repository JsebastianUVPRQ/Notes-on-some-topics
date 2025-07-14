### **Unidad 4: Inestabilidad Nuclear - Emisiones α, β y γ**

#### **1. Introducción: La Búsqueda de la Estabilidad Perdida**  
Los núcleos atómicos inestables buscan alcanzar configuraciones energéticas más favorables mediante procesos de decaimiento que transforman su estructura interna. Esta unidad explora los tres mecanismos fundamentales de desintegración nuclear: **emisión gamma (γ)**, **decaimiento beta (β)** y **emisión alfa (α)**. Cada uno de estos procesos responde a diferentes tipos de inestabilidad nuclear:  
- **Exceso de energía cinética interna** (γ)  
- **Desequilibrio en la relación neutrón-protón** (β)  
- **Inestabilidad en núcleos pesados** (α)  
Estos fenómenos están gobernados por las leyes de conservación de la energía, momento angular, paridad y carga eléctrica, y su estudio revela aspectos profundos de las interacciones fundamentales de la naturaleza.

---

#### **2. Emisión Gamma (γ): La Danza de los Fotones Nucleares**  
**Origen físico**: Cuando un núcleo excitado ($\text{A}^*$) retorna a su estado fundamental ($\text{A}$), libera el exceso de energía en forma de fotones altamente energéticos ($E_\gamma > 100$ keV). A diferencia de los fotones atómicos, los rayos γ involucran reordenamientos colectivos de nucleones.  

**Mecanismo cuántico**:  
- **Transiciones electromagnéticas multipolares**:  
  El fotón γ lleva momento angular $L$ (en unidades $\hbar$) y paridad definida. La probabilidad de transición sigue:  
  $$\lambda(E\gamma/L) = \frac{8\pi(L+1)}{L[(2L+1)!!]^2}\left(\frac{E_\gamma}{\hbar c}\right)^{2L+1}|\langle f||\mathcal{O}_L||i\rangle|^2$$  
  donde $\mathcal{O}_L$ es el operador multipolar (eléctrico o magnético) y $||\rangle$ denota estados nucleares inicial y final.  

**Reglas de selección**:  
1. **Conservación de momento angular**: $|\vec{I_i} - \vec{I_f}| \leq L \leq |\vec{I_i} + \vec{I_f}|$  
2. **Conservación de paridad**:  
   - **Transiciones eléctricas (EL)**: $\Delta\pi = (-1)^L$  
   - **Transiciones magnéticas (ML)**: $\Delta\pi = (-1)^{L+1}$  

**Ejemplo ilustrativo**: En ${}^{60}\text{Co}$, la transición de $I_i^\pi=4^+$ a $I_f^\pi=2^+$ con $\Delta\pi=+$ corresponde a $E2$ (cuadrupolar eléctrico).  

**Efecto Mössbauer**: Fenómeno de **absorción resonante sin retroceso** en sólidos rígidos. La probabilidad de emisión/absorción resonante es:  
$$f = \exp\left[-\frac{4\pi^2\langle x^2\rangle}{\lambda^2}\right]$$  
donde $\langle x^2\rangle$ es la amplitud de vibración térmica y $\lambda$ la longitud de onda del γ. Aplicación clave: medición precisa de campos gravitatorios (experimento de Pound-Rebka).

**Conversión interna**: Proceso competitivo donde la energía de transición se transfiere a un electrón atómico. El **coeficiente de conversión** $\alpha$ se define como:  
$$\alpha = \frac{\lambda_{\text{electrón}}}{\lambda_{\gamma}}$$  
Valores altos de $\alpha$ indican transiciones altamente prohibidas.

---

#### **3. Decaimiento Beta (β): La Alquimia Nuclear**  
**Fundamento termodinámico**: Núcleos con exceso de neutrones ($\beta^-$) o protones ($\beta^+$/EC) buscan la línea de estabilidad ($N/Z\approx1+0.015A^{2/3}$).  

**Tipos de procesos**:  
1. $\beta^-$: $n \rightarrow p + e^- + \bar{\nu}_e$  
2. $\beta^+$: $p \rightarrow n + e^+ + \nu_e$  
3. **Captura electrónica (EC)**: $p + e^- \rightarrow n + \nu_e$  

**Espectro energético continuo**: La energía compartida entre $e^\pm$ y $\nu$ resulta en un espectro continuo. La distribución de Fermi es:  
$$N(p)dp = \frac{G_F^2 |M_{fi}|^2}{2\pi^3\hbar^7c^3} F(Z,E_e) p_e^2 (Q - E_e)^2 dp_e$$  
- $G_F = 1.166 \times 10^{-11}$ MeV$^{-2}$: Constante de Fermi  
- $F(Z,E_e)$: Factor de Coulomb  
- $Q$: Energía máxima del espectro  

**Teoría de Fermi**:  
- **Hamiltoniano de interacción débil**:  
  $$\mathcal{H}_{\beta} = \frac{G_F}{\sqrt{2}} \left[ \bar{\psi}_p \gamma^\mu (C_V - C_A\gamma_5) \psi_n \right] \left[ \bar{\psi}_e \gamma_\mu (1 - \gamma_5) \psi_{\nu} \right] + \text{h.c.}$$  
  donde $C_V \approx 1$, $C_A \approx 1.26$ para transiciones vectoriales y axiales.  

**Gráfico de Kurie**: Herramienta para determinar $Q$ y verificar la teoría:  
$$K(E_e) = \sqrt{\frac{N(p_e)}{p_e^2 F(Z,E_e)}} \propto (Q - E_e)$$  
Desviaciones de la linealidad indican transiciones prohibidas o neutrinos masivos.  

**Captura electrónica dominante**: En núcleos pesados, la probabilidad escala como:  
$$\lambda_{\text{EC}} \propto Z^3 E_\nu^2$$  
Ejemplo: ${}^{7}\text{Be}$ decae 97% por EC con $t_{1/2}=53.22$ días.

---

#### **4. Emisión Alfa (α): El Túnel Cuántico Macroscópico**  
**Mecanismo de Gamow**: Partículas α preformadas oscilan dentro del pozo nuclear hasta atravesar la barrera coulombiana por efecto túnel.  

**Modelo cuántico**:  
- **Potencial efectivo**:  
  $$V(r) = \begin{cases} 
      -V_0 & r < R \\
      \dfrac{2(Z-2)e^2}{4\pi\epsilon_0 r} & r > R 
   \end{cases}$$  
- **Factor de transmisión**:  
  $$T = \exp\left[ -\frac{2}{\hbar} \int_R^b \sqrt{2\mu\left( \frac{2Ze^2}{4\pi\epsilon_0 r} - Q \right)} dr \right]$$  
  donde $b=\frac{2Ze^2}{4\pi\epsilon_0 Q}$ es el punto de retorno clásico.  

**Solución analítica (Gamow)**:
$$T = \exp\left[ -2\sqrt{\frac{2\mu}{\hbar^2}} \frac{Ze^2}{4\pi\epsilon_0} \left( \arccos\sqrt{\frac{R}{b}} - \sqrt{\frac{R}{b}\left(1-\frac{R}{b}\right)} \right) \right]$$  

**Energías características**:  
- Espectro discreto con $E_\alpha \approx 4-9$ MeV  
- Relación vida media-energía (**Ley de Geiger-Nuttall**):  
  $$\log t_{1/2} = a\frac{Z}{\sqrt{Q}} + b$$  

**Ejemplo paradigmático**: ${}^{238}\text{U}$ ($Q_\alpha=4.27$ MeV, $t_{1/2}=4.47\times10^9$ años) vs ${}^{212}\text{Po}$ ($Q_\alpha=8.95$ MeV, $t_{1/2}=0.3\mu$s).

---

#### **5. Verificación Experimental: Lo Invisible Hecho Visible**  
**Espectroscopía γ**:  
- **Detectores de centelleo (NaI/Tl)**: Resolución $\Delta E/E \approx 7\%$ a 662 keV  
- **Detectores HPGe**: Resolución $\Delta E \approx 1.8$ keV a 1.33 MeV  
  Identificación de "huellas digitales" nucleares mediante energías de transición.  

**Espectroscopía β**:  
- **Espectrómetros magnéticos**: Miden $p_e$ con precisión $\Delta p/p < 0.1\%$  
  - Confirmación de la violación de paridad en $\beta$-decaimiento (experimento de Wu, 1957).  

**Espectroscopía α**:  
- **Detectores de barrera superficial**: Resolución $\Delta E \approx 15$ keV  
  - Mediciones de pérdida de energía en materiales ($dE/dx$):  
    $$\frac{dE}{dx} = \frac{4\pi e^4 z^2}{m_e c^2 \beta^2} NZ \left[ \ln\frac{2m_e c^2\beta^2}{I} - \beta^2 \right]$$  
    (Fórmula de Bethe-Bloch para partículas pesadas)  

**Experimento de Rutherford**:  
- Dispersión de partículas α en láminas delgadas:  
  $$\frac{d\sigma}{d\Omega} = \left( \frac{ZZ'e^2}{16\pi\epsilon_0 E} \right)^2 \frac{1}{\sin^4(\theta/2)}$$  
  Confirmación del modelo nuclear planetario.

---

#### **6. Conclusión: La Inestabilidad como Motor de Transformación**  
Los procesos de decaimiento nuclear revelan la profunda interconexión entre las fuerzas fundamentales de la naturaleza. La emisión γ demuestra la universalidad del electromagnetismo cuántico, el decaimiento β expresa la acción de la interacción débil en escalas nucleares, y la emisión α ilustra dramáticamente el efecto túnel cuántico. Cada espectro medido es una ventana a la estructura nuclear:  
- **Líneas espectrales γ** ↔ Niveles de energía nuclear  
- **Espectro continuo β** ↔ Dinámica de la interacción débil  
- **Energías discretas α** ↔ Estados cuasi-estacionarios  

> "La radiactividad no es un signo de decadencia, sino de transformación hacia estados más armónicos." — Marie Curie  

**Próximo paso**: ¿Profundizar en la Unidad 5 (Reacciones Nucleares) o ajustar enfoque pedagógico?

Aquí tienes el texto expandido con explicaciones conceptuales más detalladas, manteniendo un tono académico claro y riguroso. Se han ampliado las ideas físicas, interpretaciones teóricas y conexiones entre ecuaciones y fenómenos:

---

#### **1. Introducción: La Búsqueda de la Estabilidad Perdida**

El núcleo atómico, compuesto por protones y neutrones (nucleones), no es una estructura estática ni universalmente estable. Su estabilidad depende de una delicada combinación entre la repulsión electrostática de los protones (que tienden a separarse por tener la misma carga positiva) y la atracción debida a la interacción nuclear fuerte (que mantiene cohesionados a los nucleones en distancias del orden de femtómetros).

Cuando esta balanza se rompe —ya sea por un exceso de energía, una relación desbalanceada entre neutrones y protones, o simplemente por una configuración demasiado masiva— el núcleo puede decaer espontáneamente hacia un estado más estable. Este proceso involucra una **transición cuántica**, en la que el sistema emite partículas o radiación para disminuir su energía total.

Los mecanismos más comunes de este reordenamiento nuclear son:

- **Emisión gamma (γ)**: el núcleo no cambia su identidad (misma A y Z), pero se desexcita internamente liberando fotones energéticos. Es análogo a una "reorganización" del mobiliario interno del núcleo.
    
- **Decaimiento beta (β)**: cambia un nucleón de tipo (neutrón a protón o viceversa), con lo que se transforma el número atómico $Z$, y por tanto, el elemento químico.
    
- **Emisión alfa (α)**: ocurre en núcleos pesados e implica la expulsión de una partícula compuesta (2 protones + 2 neutrones), alterando significativamente la identidad nuclear.
    

Estos procesos se rigen por leyes de conservación fundamentales:

- **Energía**: la masa total disminuye si es necesario para liberar energía.
    
- **Momento angular y paridad**: reflejan simetrías del sistema.
    
- **Carga eléctrica y número leptónico**: garantizan la coherencia con las interacciones fundamentales.
    

Estudiar estos decaimientos permite comprender mejor no solo la estructura nuclear, sino también las leyes cuánticas que gobiernan el universo a escalas subatómicas.

---

#### **2. Emisión Gamma (γ): La Danza de los Fotones Nucleares**

Cuando un núcleo se encuentra en un **estado excitado**, típicamente después de una reacción nuclear o un decaimiento anterior, posee un exceso de energía que no puede mantener indefinidamente. Para estabilizarse, emite este exceso en forma de un **fotón gamma**, una partícula de luz con energías del orden de cientos de keV a varios MeV.

A diferencia de las transiciones electrónicas (que generan luz visible o rayos X), las transiciones gamma son mucho más energéticas y reflejan cambios **colectivos o configuracionales en el estado cuántico de los nucleones** dentro del núcleo.

**Transiciones multipolares**: No todos los fotones gamma son iguales. Se clasifican por su **momento angular orbital** $L$:

- $L = 1$: dipolar
    
- $L = 2$: cuadrupolar
    
- $L = 3$: octupolar  
    y así sucesivamente.
    

Cada transición lleva asociada una **paridad** (simetría bajo inversión espacial), y se distingue entre:

- **Transiciones eléctricas (EL)**: asociadas a distribuciones de carga oscilantes.
    
- **Transiciones magnéticas (ML)**: ligadas a movimientos circulares de corrientes nucleares (spin o momento orbital).
    

La **probabilidad de emisión** está dada por la fórmula que involucra el operador multipolar $\mathcal{O}_L$ y su matriz de transición entre estados nucleares. Cuanto mayor sea $L$, más "prohibida" (menos probable) es la transición, y más lenta es la desexcitación.

**Efecto Mössbauer**: En ciertos materiales sólidos, los núcleos pueden emitir y absorber rayos gamma sin pérdida de energía debida al retroceso (como el de un cañón al disparar). Este fenómeno permite **mediciones de altísima precisión** en espectroscopía y en efectos gravitatorios (como en el célebre experimento de Pound-Rebka, que verificó el corrimiento gravitacional del tiempo predicho por la relatividad general).

**Conversión interna**: A veces, en lugar de emitir un fotón, el núcleo transfiere su energía directamente a un electrón de una capa interna del átomo, que es entonces expulsado. Este proceso compite con la emisión gamma y se vuelve dominante cuando la emisión está cuánticamente prohibida (por reglas de selección muy restrictivas).

---

#### **3. Decaimiento Beta (β): La Alquimia Nuclear**

El decaimiento beta representa una **transformación de la identidad química del núcleo**, ya que cambia el número de protones. Este proceso se relaciona con el **desequilibrio en la relación neutrones/protones**, lo cual aleja al núcleo de la llamada **línea de estabilidad** (núcleos estables para un número másico $A$).

**Tipos**:

- En $\beta^-$, un neutrón se convierte en un protón, liberando un electrón ($e^-$) y un antineutrino electrónico ($\bar{\nu}_e$).
    
- En $\beta^+$, un protón se transforma en neutrón, emitiendo un positrón ($e^+$) y un neutrino ($\nu_e$).
    
- En **captura electrónica (EC)**, el núcleo "atrapa" un electrón de una capa interna, convirtiendo un protón en neutrón y emitiendo un neutrino.
    

**Energía compartida**: A diferencia del decaimiento α o γ, el decaimiento β no tiene una energía fija para las partículas emitidas. En lugar de eso, la energía disponible se reparte entre el electrón/positrón y el (anti)neutrino, produciendo un espectro **continuo** de energías. Esto fue un misterio hasta que Pauli postuló la existencia del neutrino para salvar la conservación de energía y momento.

**Teoría de Fermi**: Propone una interacción cuántica de tipo punto (contacto), parecida al electromagnetismo pero mucho más débil, que involucra las corrientes de nucleones y leptones. La interacción débil tiene una estructura de tipo V-A (vector menos axial), lo que explica fenómenos como la **violación de paridad** (asimetría izquierda-derecha), observada experimentalmente por Chien-Shiung Wu.

**Gráfico de Kurie**: Es una herramienta experimental que linealiza el espectro energético del electrón. Permite verificar si el decaimiento sigue las predicciones teóricas y determinar el valor de $Q$, la energía máxima del proceso. Cualquier desviación puede sugerir la existencia de partículas nuevas o transiciones no permitidas.

**Captura electrónica** es especialmente relevante en núcleos pesados, donde los electrones están más cerca del núcleo. La probabilidad crece con $Z^3$ debido a la mayor densidad electrónica cerca del núcleo. Un ejemplo interesante es el berilio-7, cuyo decaimiento casi exclusivamente ocurre por EC.

---

#### **4. Emisión Alfa (α): El Túnel Cuántico Macroscópico**

La emisión alfa se da típicamente en **núcleos pesados (Z > 82)** y puede entenderse como un proceso en el que una **partícula α** (núcleo de helio-4, con dos protones y dos neutrones) ya preformada dentro del núcleo escapa atravesando la barrera de potencial coulombiana por **efecto túnel**.

**Modelo de Gamow**: Utiliza la mecánica cuántica para calcular la **probabilidad de que la partícula escape**, a pesar de no tener suficiente energía clásica para superar la barrera. Este proceso es una **manifestación directa del principio de incertidumbre** y del carácter ondulatorio de la materia.

El modelo describe el potencial nuclear con una región atractiva (pozo) y una barrera repulsiva exterior (potencial coulombiano). La probabilidad de escape está dada por un factor exponencial que depende fuertemente del valor de $Q_\alpha$ (energía liberada). Esto explica la **enorme variación en las vidas medias** entre isótopos con diferencias pequeñas en energía.

**Ley de Geiger-Nuttall**: Establece una relación empírica entre la energía de la partícula α emitida y la vida media del núcleo. Nótese que una pequeña variación en $Q_\alpha$ implica una **variación exponencial** en el tiempo de vida, lo que hace de la emisión α un "reloj" nuclear extremadamente sensible.

---

#### **5. Verificación Experimental: Lo Invisible Hecho Visible**

La física nuclear se apoya fuertemente en técnicas de **espectroscopía**, que permiten identificar y analizar los productos del decaimiento con precisión.

**Espectroscopía γ**: Mide la energía de los fotones emitidos por desexcitación nuclear. La alta resolución energética de los detectores HPGe permite distinguir niveles nucleares separados por pocos keV, proporcionando un "mapa de niveles" del núcleo.

**Espectroscopía β**: El análisis del espectro continuo de electrones permite inferir el tipo de decaimiento, verificar la existencia de neutrinos y estudiar efectos de física más allá del modelo estándar. El experimento de Wu (1957) demostró la **violación de la simetría izquierda-derecha**, un resultado que revolucionó la física de partículas.

**Espectroscopía α**: Los detectores de silicio miden la energía con alta precisión, permitiendo discriminar entre isótopos emisores. Además, la fórmula de Bethe-Bloch describe cómo las partículas cargadas pierden energía al atravesar materia, y esto permite deducir su tipo, energía inicial y trayectoria.

**Dispersión de Rutherford**: Históricamente fundamental, mostró que los átomos tienen un núcleo compacto. La ley angular derivada de la dispersión de partículas α contra láminas metálicas fue la primera evidencia directa de la existencia del núcleo.

---

#### **6. Conclusión: La Inestabilidad como Motor de Transformación**

Cada tipo de decaimiento nuclear ilustra una **faceta distinta de la interacción fundamental** que lo causa:

- La emisión γ es un ejemplo elegante de **electrodinámica cuántica aplicada a sistemas nucleares**, con reglas de selección que reflejan la simetría y estructura interna.
    
- El decaimiento β es la manifestación más accesible de la **interacción débil**, única entre las fuerzas por violar la simetría de paridad y por incluir leptones.
    
- La emisión α dramatiza la **penetración cuántica**, un fenómeno que permite a partículas pesadas escapar de un núcleo sin energía clásica suficiente.
    

El estudio de estos procesos revela que la radiactividad no es una anomalía, sino una **vía natural hacia el equilibrio**, en la que los núcleos se transforman espontáneamente hacia configuraciones más estables y armónicas con el universo.

> "La radiactividad no es un signo de decadencia, sino de transformación hacia estados más armónicos." — Marie Curie

---

¿Te gustaría que continúe con la **Unidad 5 (Reacciones Nucleares)** con este mismo enfoque ampliado? ¿O prefieres primero desarrollar materiales pedagógicos (esquemas, ejercicios, analogías) sobre esta unidad?