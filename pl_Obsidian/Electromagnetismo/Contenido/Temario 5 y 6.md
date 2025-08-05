## Capítulo 5: Ecuaciones de Maxwell

### 5.1 Campos Dinámicos y Ley de Inducción de Faraday

La ley de inducción de Faraday representa uno de los pilares fundamentales del electromagnetismo clásico, estableciendo una profunda conexión entre los fenómenos eléctricos y magnéticos. Matemáticamente se expresa mediante la ecuación diferencial:

$$
\nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}
$$

Esta relación muestra que un campo magnético variable en el tiempo genera un campo eléctrico rotacional, es decir, no conservativo. El significado físico de esta ley se manifiesta claramente en el fenómeno de inducción electromagnética, donde la fuerza electromotriz (FEM) inducida en un circuito viene dada por:

$$
\mathcal{E} = -\frac{d\Phi_B}{dt} = -\frac{d}{dt}\int_S \vec{B} \cdot d\vec{a}
$$

El signo negativo en estas expresiones refleja la ley de Lenz, que establece que la corriente inducida se opone al cambio de flujo magnético que la produce. Este principio es fundamental para el funcionamiento de numerosos dispositivos tecnológicos, desde generadores eléctricos hasta transformadores de potencia. Experimentalmente, Faraday demostró que el movimiento relativo entre un imán y una espira conductora genera corriente eléctrica, confirmando así que los campos magnéticos variables pueden producir campos eléctricos incluso en ausencia de cargas libres.

### 5.2 Corriente de Desplazamiento y Ecuaciones de Maxwell Completas

La introducción de la corriente de desplazamiento por parte de Maxwell representó un avance conceptual revolucionario en la teoría electromagnética. Esta cantidad, definida como:

$$
\vec{J}_d = \varepsilon_0 \frac{\partial \vec{E}}{\partial t}
$$

surge como una corrección necesaria a la ley de Ampère original para garantizar la conservación de la carga en situaciones dinámicas. La forma generalizada de la ley de Ampère, conocida ahora como ley de Ampère-Maxwell, se escribe:

$$
\nabla \times \vec{B} = \mu_0 \left( \vec{J} + \varepsilon_0 \frac{\partial \vec{E}}{\partial t} \right)
$$

Las cuatro ecuaciones de Maxwell en su forma diferencial completa constituyen la base de todo el electromagnetismo clásico:

1. **Ley de Gauss eléctrica**: $\nabla \cdot \vec{E} = \frac{\rho}{\varepsilon_0}$  
   Relaciona el campo eléctrico con sus fuentes (cargas eléctricas).

2. **Ley de Gauss magnética**: $\nabla \cdot \vec{B} = 0$  
   Indica la ausencia de monopolos magnéticos en la naturaleza.

3. **Ley de Faraday**: $\nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}$  
   Describe cómo campos magnéticos variables generan campos eléctricos.

4. **Ley de Ampère-Maxwell**: $\nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0 \varepsilon_0 \frac{\partial \vec{E}}{\partial t}$  
   Establece que tanto corrientes eléctricas como campos eléctricos variables generan campos magnéticos.

Estas ecuaciones predicen la existencia de ondas electromagnéticas que se propagan en el vacío con velocidad $c = 1/\sqrt{\mu_0 \varepsilon_0}$, valor que coincide exactamente con la velocidad de la luz, llevando a Maxwell a proponer que la luz es en sí misma una onda electromagnética.

### 5.3 Potenciales Electromagnéticos e Invariancia Gauge

La formulación en términos de potenciales electromagnéticos ofrece una poderosa herramienta matemática para resolver problemas electromagnéticos. Los campos $\vec{E}$ y $\vec{B}$ pueden expresarse mediante un potencial escalar $\phi$ y un potencial vectorial $\vec{A}$ como:

$$
\vec{E} = -\nabla \phi - \frac{\partial \vec{A}}{\partial t}
$$
$$
\vec{B} = \nabla \times \vec{A}
$$

Esta formulación introduce el importante concepto de invariancia gauge, que establece que los potenciales no están unívocamente determinados, sino que admiten transformaciones de la forma:

$$
\phi \rightarrow \phi - \frac{\partial \Lambda}{\partial t}, \quad \vec{A} \rightarrow \vec{A} + \nabla \Lambda
$$

donde $\Lambda$ es una función escalar arbitraria. Estas transformaciones dejan invariantes los campos físicos $\vec{E}$ y $\vec{B}$. Una elección particularmente útil es el gauge de Lorenz:

$$
\nabla \cdot \vec{A} + \mu_0 \varepsilon_0 \frac{\partial \phi}{\partial t} = 0
$$

que conduce a ecuaciones de onda desacopladas para los potenciales, simplificando notablemente su resolución en problemas de radiación electromagnética.

### 5.4 Energía y Flujo del Campo Electromagnético

El campo electromagnético transporta energía que puede almacenarse y propagarse a través del espacio. La densidad de energía electromagnética en el vacío está dada por:

$$
u = \frac{1}{2} \left( \varepsilon_0 E^2 + \frac{B^2}{\mu_0} \right)
$$

Esta expresión muestra contribuciones tanto del campo eléctrico como del magnético. El flujo de energía se describe mediante el vector de Poynting:

$$
\vec{S} = \frac{1}{\mu_0} \vec{E} \times \vec{B}
$$

que representa la potencia por unidad de área transportada por la onda electromagnética. La conservación de la energía se expresa mediante la ecuación de continuidad:

$$
\frac{\partial u}{\partial t} + \nabla \cdot \vec{S} = -\vec{J} \cdot \vec{E}
$$

donde el término $\vec{J} \cdot \vec{E}$ cuantifica la disipación de energía por efecto Joule en medios conductores. En sistemas aislados, esta ecuación garantiza que la energía electromagnética total se conserve.

### 5.5 Ecuaciones de Maxwell en Medios Materiales

Cuando los campos electromagnéticos interactúan con materia, las ecuaciones de Maxwell se modifican introduciendo los campos auxiliares $\vec{D}$ (desplazamiento eléctrico) y $\vec{H}$ (intensidad magnética):

$$
\nabla \cdot \vec{D} = \rho_f, \quad \nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}
$$
$$
\nabla \cdot \vec{B} = 0, \quad \nabla \times \vec{H} = \vec{J}_f + \frac{\partial \vec{D}}{\partial t}
$$

Para medios lineales e isótropos, las relaciones constitutivas son:

$$
\vec{D} = \varepsilon \vec{E} = \varepsilon_0 \varepsilon_r \vec{E}
$$
$$
\vec{H} = \frac{\vec{B}}{\mu} = \frac{\vec{B}}{\mu_0 \mu_r}
$$

Las condiciones de frontera en interfaces entre medios diferentes son cruciales para resolver problemas prácticos:

1. **Componente normal de $\vec{D}$**: $D_{1n} - D_{2n} = \sigma_f$  
   Muestra discontinuidad cuando hay carga libre superficial.

2. **Componente tangencial de $\vec{E}$**: $E_{1t} = E_{2t}$  
   Siempre continua en ausencia de campos magnéticos variables.

3. **Componente normal de $\vec{B}$**: $B_{1n} = B_{2n}$  
   Continua debido a la ausencia de monopolos magnéticos.

4. **Componente tangencial de $\vec{H}$**: $H_{1t} - H_{2t} = \vec{K}_f \times \hat{n}$  
   Presenta discontinuidad cuando hay corrientes libres superficiales.

## Capítulo 6: Propagación de Ondas Electromagnéticas

### 6.1 Ondas Electromagnéticas Planas en el Vacío

Las ecuaciones de Maxwell en ausencia de fuentes ($\rho = 0$, $\vec{J} = 0$) predicen la existencia de ondas electromagnéticas que satisfacen la ecuación de onda:

$$
\nabla^2 \vec{E} - \mu_0 \varepsilon_0 \frac{\partial^2 \vec{E}}{\partial t^2} = 0
$$
$$
\nabla^2 \vec{B} - \mu_0 \varepsilon_0 \frac{\partial^2 \vec{B}}{\partial t^2} = 0
$$

Las soluciones más simples son ondas planas monocromáticas de la forma:

$$
\vec{E}(\vec{r}, t) = \vec{E}_0 e^{i(\vec{k} \cdot \vec{r} - \omega t)}
$$
$$
\vec{B}(\vec{r}, t) = \vec{B}_0 e^{i(\vec{k} \cdot \vec{r} - \omega t)}
$$

Las relaciones fundamentales para estas ondas son:

$$
\vec{B} = \frac{1}{\omega} \vec{k} \times \vec{E}, \quad |\vec{E}| = c |\vec{B}|, \quad c = \frac{\omega}{k} = \frac{1}{\sqrt{\mu_0 \varepsilon_0}}
$$

Estas relaciones muestran que los campos $\vec{E}$ y $\vec{B}$ son perpendiculares entre sí y ambos son perpendiculares a la dirección de propagación $\vec{k}$, formando así ondas transversales. La velocidad de fase en el vacío $c \approx 3 \times 10^8$ m/s es una constante fundamental de la naturaleza.

### 6.2 Propagación en Medios Materiales

En medios materiales no conductores, la velocidad de propagación de las ondas electromagnéticas disminuye según:

$$
v = \frac{c}{n}, \quad n = \sqrt{\mu_r \varepsilon_r}
$$

donde $n$ es el índice de refracción del medio. Para medios conductores, aparece un efecto de atenuación descrito por:

$$
\vec{E}(\vec{r}, t) = \vec{E}_0 e^{-\kappa z} e^{i(k z - \omega t)}
$$

El coeficiente de atenuación $\kappa$ depende de la conductividad $\sigma$ del material y de la frecuencia $\omega$ de la onda. Este fenómeno explica el efecto piel, donde la onda penetra solo una profundidad característica:

$$
\delta = \frac{1}{\kappa} = \sqrt{\frac{2}{\mu_0 \mu_r \omega \sigma}}
$$

En buenos conductores a altas frecuencias, esta profundidad de penetración puede ser extremadamente pequeña, confinando las corrientes a una delgada capa superficial.

### 6.3 Reflexión y Refracción en Interfaces

Cuando una onda electromagnética incide sobre la interfaz entre dos medios diferentes, se producen fenómenos de reflexión y refracción gobernados por las leyes de Snell:

$$
\theta_r = \theta_i, \quad n_1 \sin \theta_i = n_2 \sin \theta_t
$$

Los coeficientes de reflexión y transmisión para incidencia normal están dados por:

$$
R = \left| \frac{n_1 - n_2}{n_1 + n_2} \right|^2, \quad T = \frac{4 n_1 n_2}{(n_1 + n_2)^2}
$$

Para incidencia oblicua, el comportamiento depende de la polarización de la onda incidente, descrito por las ecuaciones de Fresnel. Un caso particularmente importante es el ángulo de Brewster:

$$
\theta_B = \arctan\left(\frac{n_2}{n_1}\right)
$$

para el cual la onda reflejada está completamente polarizada cuando la luz incide con polarización paralela al plano de incidencia.

### 6.4 Guías de Ondas y Cavidades Resonantes

En sistemas confinados como guías de onda metálicas, las soluciones de las ecuaciones de Maxwell toman la forma de modos discretos. Para una guía de onda rectangular de dimensiones $a \times b$, las frecuencias de corte de los modos TE y TM vienen dadas por:

$$
f_{mn} = \frac{c}{2} \sqrt{\left( \frac{m}{a} \right)^2 + \left( \frac{n}{b} \right)^2}
$$

En cavidades resonantes, las ondas electromagnéticas forman patrones estacionarios con frecuencias discretas de resonancia. Estas estructuras son fundamentales en numerosas aplicaciones tecnológicas, desde hornos microondas hasta aceleradores de partículas.

### 6.5 Aplicaciones Tecnológicas

Los principios de propagación de ondas electromagnéticas encuentran aplicaciones en numerosas tecnologías modernas:

1. **Fibras ópticas**: Basadas en el fenómeno de reflexión total interna, permiten transmitir información a largas distancias con pérdidas mínimas. El perfil de índice de refracción está cuidadosamente diseñado para optimizar la propagación de los modos ópticos.

2. **Antenas**: Dispositivos que convierten corrientes oscilantes en ondas electromagnéticas radiadas (antenas transmisoras) o viceversa (antenas receptoras). El diseño de antenas depende críticamente de la frecuencia de operación y del patrón de radiación deseado.

3. **Radar**: Sistemas que utilizan la reflexión de ondas electromagnéticas (generalmente microondas) para detectar y localizar objetos. La medición del tiempo de retorno de los pulsos reflejados permite determinar distancias con gran precisión.

4. **Comunicaciones inalámbricas**: Desde radio AM/FM hasta redes 5G, todas se basan en la transmisión y recepción de ondas electromagnéticas en diferentes bandas de frecuencia.

Estas aplicaciones demuestran la importancia fundamental de entender la propagación de ondas electromagnéticas en el desarrollo de tecnologías modernas que han transformado nuestra sociedad.