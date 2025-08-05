### Capítulo 1: Campo Electrostático en el Vacío

#### 1.1 Ley de Coulomb y Principio de Superposición  
La electrostática se fundamenta en la **ley de Coulomb**, formulada en 1785, que cuantifica la fuerza entre dos cargas puntuales en reposo. Esta ley establece que la magnitud de la fuerza $F$ es directamente proporcional al producto de las cargas $q_1$ y $q_2$, e inversamente proporcional al cuadrado de la distancia $r$ que las separa:  
$$
\vec{F} = \frac{1}{4\pi\varepsilon_0} \frac{q_1 q_2}{r^2} \hat{r},
$$  
donde $\varepsilon_0 = 8.85 \times 10^{-12}  \text{C}^2/\text{N·m}^2$ es la permitividad del vacío, y $\${r}$ $el vector unitario que define la dirección de la fuerza. La fuerza es atractiva para cargas de signos opuestos y repulsiva para cargas del mismo signo. El **principio de superposición** extiende esta ley a sistemas complejos: la fuerza total sobre una carga es la suma vectorial de las contribuciones individuales de cada carga en el sistema. Este principio, derivado de la linealidad de las ecuaciones electrostáticas, permite analizar configuraciones arbitrarias de cargas discretas o continuas mediante integración. Por ejemplo, para una distribución volumétrica de carga $\rho(\vec{r}')$, el campo eléctrico resultante se calcula integrando las contribuciones infinitesimales sobre todo el volumen.

#### 1.3 Campo Eléctrico y Características Diferenciales  
El **campo eléctrico** $\vec{E}$ se define como la fuerza por unidad de carga experimentada por una carga de prueba infinitesimal $q_t$:  
$$
\vec{E} = \lim_{q_t \to 0} \frac{\vec{F}}{q_t}.
$$  
Esta definición desvincula el campo de la carga específica que lo mide, revelando $\vec{E}$ como una propiedad intrínseca del espacio. Sus características diferenciales se expresan mediante dos ecuaciones fundamentales. Primero, la **ley de Gauss en forma diferencial**:  
$$
\nabla \cdot \vec{E} = \frac{\rho}{\varepsilon_0},
$$  
que establece que la divergencia del campo eléctrico en un punto es proporcional a la densidad de carga local $\rho$. Esto implica que las cargas positivas actúan como *fuentes* del campo, mientras las negativas son *sumideros*. Segundo, la naturaleza conservativa del campo electrostático:  
$$
\nabla \times \vec{E} = 0,
$$  
indicando que el trabajo realizado para mover una carga entre dos puntos es independiente de la trayectoria. Esta propiedad permite definir el **potencial eléctrico** $\phi$ como $\vec{E} = -\nabla \phi$, donde $\phi$ representa la energía potencial por unidad de carga.

#### 1.4 Potencial Eléctrico y Ecuación de Poisson  
El **potencial eléctrico** $\phi$ es una función escalar que simplifica el análisis de campos electrostáticos. Para una distribución de carga $\rho(\vec{r}')$, se calcula como:  
$$
\phi(\vec{r}) = \frac{1}{4\pi\varepsilon_0} \int \frac{\rho(\vec{r}')}{|\vec{r} - \vec{r}'|}  d^3r'.
$$  
Físicamente, $\phi(\vec{r})$ es el trabajo necesario para traer una carga unitaria desde el infinito hasta $\vec{r}$. Combinando $\vec{E} = -\nabla \phi$ con la ley de Gauss, se obtiene la **ecuación de Poisson**:  
$$
\nabla^2 \phi = -\frac{\rho}{\varepsilon_0},
$$  
que gobierna el comportamiento del potencial en presencia de cargas. En regiones sin carga ($\rho = 0$), se reduce a la **ecuación de Laplace** $\nabla^2 \phi = 0$. Las soluciones a estas ecuaciones, sujetas a condiciones de frontera, determinan unívocamente el campo electrostático. Las **superficies equipotenciales** ($\phi = \text{constante}$) son perpendiculares a $\vec{E}$, proporcionando una representación geométrica útil: en conductores, estas superficies coinciden con su forma, y el campo es siempre normal a ellas.

#### 1.5 Densidad de Energía y Tensor de Esfuerzos de Maxwell  
La energía almacenada en un campo electrostático refleja el trabajo realizado para ensamblar la distribución de cargas. Para un sistema de $n$ cargas, la energía total $U$ es:  
$$
U = \frac{1}{2} \sum_{i=1}^n q_i \phi(\vec{r}_i).
$$  
Para distribuciones continuas, esto se generaliza a:  
$$
U = \frac{\varepsilon_0}{2} \int |\vec{E}|^2  d^3r,
$$  
donde la **densidad de energía** $u = \frac{\varepsilon_0}{2} E^2$ demuestra que el campo mismo porta energía. Esta expresión es universal: aplica incluso en ausencia de cargas, como en ondas electromagnéticas.  

El **tensor de esfuerzos de Maxwell** $T_{ij}$ describe las fuerzas volumétricas en medios continuos:  
$$
T_{ij} = \varepsilon_0 \left( E_i E_j - \frac{1}{2} \delta_{ij} E^2 \right).
$$  
La fuerza sobre cargas en un volumen $V$ se calcula como el flujo de $T_{ij}$ a través de su superficie $S$:  
$$
F_i = \oint_S T_{ij}  da_j.
$$  
Por ejemplo, en un conductor, la presión electrostática es $P = \frac{\varepsilon_0}{2} E^2$, lo que explica fenómenos como la atracción entre placas de un capacitor.

---

### Capítulo 2: Campo Electrostático en Medios Dieléctricos

#### 2.1 Polarización en Materiales  
Los dieléctricos son materiales que se polarizan bajo campos eléctricos externos, generando **momentos dipolares** inducidos o permanentes. La **polarización** $\vec{P}$, definida como el momento dipolar por unidad de volumen ($\vec{P} = N \langle \vec{p} \rangle$, donde $N$ es la densidad molecular), cuantifica esta respuesta. Tres mecanismos contribuyen:  
- **Polarización electrónica**: Desplazamiento de nubes electrónicas respecto a núcleos atómicos.  
- **Polarización iónica**: Desplazamiento de iones en redes cristalinas (e.g., NaCl).  
- **Polarización orientacional**: Alineamiento de dipolos permanentes (e.g., moléculas de $\text{H}_2\text{O}$).  
En materiales lineales e isótropos, $\vec{P}$ es proporcional al campo: $\vec{P} = \varepsilon_0 \chi_e \vec{E}$, donde $\chi_e$ es la **susceptibilidad eléctrica**.

#### 2.2 Ley de Gauss en Dieléctricos  
La polarización induce **cargas ligadas** ($\rho_b = -\nabla \cdot \vec{P}$ en volumen, $\sigma_b = \vec{P} \cdot \hat{n}$ en superficies). Para incluir estas cargas, se define el **desplazamiento eléctrico** $\vec{D}$:  
$$
\vec{D} = \varepsilon_0 \vec{E} + \vec{P}.
$$  
En medios lineales, $\vec{D} = \varepsilon \vec{E}$, donde $\varepsilon = \varepsilon_0(1 + \chi_e)$ es la **permitividad**. La ley de Gauss se reformula como:  
$$
\nabla \cdot \vec{D} = \rho_f,
$$  
donde $\rho_f$ es la densidad de carga libre. Esta ecuación *oculta* las cargas ligadas, simplificando cálculos en simetrías sencillas. Por ejemplo, en un capacitor con dieléctrico, $D$ depende solo de la carga libre en las placas, no de la polarización.

#### 2.3 Condiciones de Frontera  
En interfaces entre dieléctricos, las componentes de $\vec{E}$ y $\vec{D}$ satisfacen:  
1. **Continuidad tangencial**: $E_{1t} = E_{2t}$ (derivada de $\nabla \times \vec{E} = 0$).  
2. **Discontinuidad normal**: $D_{1n} - D_{2n} = \sigma_f$ (derivada de $\nabla \cdot \vec{D} = \rho_f$).  
Si no hay carga libre superficial ($\sigma_f = 0$), $D_{1n} = D_{2n}$. Estas condiciones son cruciales para resolver problemas con múltiples dieléctricos, como lentes o aislantes estratificados.

#### 2.4 Ecuaciones Constitutivas y Modelos Microscópicos  
La relación $\vec{D} = \varepsilon \vec{E}$ es válida para dieléctricos **lineales**, **homogéneos** e **isótropos**. La **constante dieléctrica** $\kappa = \varepsilon / \varepsilon_0$ mide la capacidad de polarización. Modelos microscópicos vinculan $\kappa$ con propiedades atómicas:  
- **Ecuación de Clausius-Mossotti**:  
  $$
  \frac{\kappa - 1}{\kappa + 2} = \frac{N \alpha}{3\varepsilon_0},
  $$  
  donde $\alpha$ es la polarizabilidad atómica. Aplica a gases y líquidos no polares.  
- **Ecuación de Langevin**: Para dipolos permanentes en gases,  
  $$
  \langle p \rangle = p_0 \left( \coth \xi - \frac{1}{\xi} \right), \quad \xi = \frac{p_0 E}{k_B T},
  $$  
  prediciendo saturación a altos campos.  
- **Ecuación de Debye**: Combina efectos inducidos y orientacionales:  
  $$
  \chi_e = \frac{N}{\varepsilon_0} \left( \alpha + \frac{p_0^2}{3k_B T} \right).
  $$

#### 2.5 Energía y Esfuerzos en Dieléctricos  
La **densidad de energía** en dieléctricos lineales es:  
$$
u = \frac{1}{2} \vec{D} \cdot \vec{E} = \frac{1}{2} \varepsilon E^2.
$$  
El **tensor de esfuerzos de Maxwell** se modifica a:  
$$
T_{ij} = D_i E_j - \frac{1}{2} \delta_{ij} (\vec{D} \cdot \vec{E}).
$$  
Este tensor explica fuerzas como la que atrae un dieléctrico hacia regiones de alto campo en un capacitor no uniforme.

#### 2.6 Aplicaciones  
- **Condensador con dieléctrico**:  
  La capacitancia aumenta en un factor $\kappa$: $C = \kappa C_0$. El campo eléctrico se reduce a $E = \sigma_f / (\varepsilon_0 \kappa)$, mientras $D = \sigma_f$ permanece constante.  
- **Esfera dieléctrica en campo uniforme**:  
  El campo interno es $\vec{E}_{\text{int}} = \frac{3}{\kappa + 2} \vec{E}_0$. Externamente, el campo equivale al de un dipolo inducido $\vec{p} = 4\pi\varepsilon_0 R^3 \left( \frac{\kappa - 1}{\kappa + 2} \right) \vec{E}_0$, donde $R$ es el radio.  
- **Dieléctricos en alta tensión**:  
  La ruptura dieléctrica ocurre cuando $E$ excede un valor crítico (e.g., 3 MV/m para el aire), limitando aplicaciones en capacitores y aislantes.

#### Perspectiva Física  
Los dieléctricos demuestran cómo la materia modifica campos eléctricos. Su estudio, iniciado por Faraday y formalizado por Maxwell, revela que la óptica es un caso límite de la electrodinámica ($\kappa = n^2$, donde $n$ es el índice de refracción). Los modelos aquí presentados son esenciales para diseñar dispositivos como capacitores, transductores y fibras ópticas, donde el control de la polarización es crucial.

---
---

---
