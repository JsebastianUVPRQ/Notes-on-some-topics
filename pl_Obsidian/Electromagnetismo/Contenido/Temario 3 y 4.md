## Capítulo 3: Métodos de solución de problemas de electrostática

### 3.1. Unicidad de la solución de la ecuación de Laplace

El teorema de unicidad es fundamental en electrostática, pues garantiza que bajo condiciones apropiadas, la solución a las ecuaciones de Laplace y Poisson es única. Matemáticamente, esto se expresa mediante las ecuaciones diferenciales:

$$
\nabla^2 \phi = 0 \quad \text{(Ecuación de Laplace)}
$$
$$
\nabla^2 \phi = -\frac{\rho}{\epsilon_0} \quad \text{(Ecuación de Poisson)}
$$

Cuando se especifican condiciones de frontera adecuadas - ya sea el valor del potencial en la superficie (condiciones de Dirichlet) o su derivada normal (condiciones de Neumann) - existe una única solución posible. Este resultado tiene profundas implicaciones prácticas, pues significa que cualquier método que encontremos para resolver estas ecuaciones (analítico, numérico o experimental) que satisfaga tanto la ecuación como las condiciones de contorno, nos dará necesariamente la solución correcta al problema físico. En la práctica, esto justifica el uso de métodos aproximados y heurísticos como el método de imágenes, donde introducimos cargas ficticias fuera de la región de interés para satisfacer las condiciones de frontera de manera más sencilla.

### 3.2. Método de separación de variables

El método de separación de variables es una técnica poderosa para resolver ecuaciones diferenciales parciales como la ecuación de Laplace. La idea fundamental es suponer que la solución puede escribirse como producto de funciones que dependen cada una de una sola variable coordenada. En coordenadas cartesianas, esto se expresa como:

$$
\phi(x,y,z) = X(x)Y(y)Z(z)
$$

Al sustituir esta forma en la ecuación de Laplace, obtenemos una ecuación separable donde cada término debe ser igual a una constante de separación. Esto nos lleva a tres ecuaciones diferenciales ordinarias independientes, cada una más fácil de resolver que la ecuación original. La elección del sistema coordenado es crucial y debe hacerse de acuerdo con las simetrías del problema. Por ejemplo, para problemas con simetría esférica, usamos coordenadas esféricas $(r,\theta,\varphi)$ donde la solución toma la forma:

$$
\phi(r,\theta,\varphi) = \sum_{l=0}^{\infty}\sum_{m=-l}^{l} [A_{lm}r^l + B_{lm}r^{-(l+1)}] Y_l^m(\theta,\varphi)
$$

Aquí, $Y_l^m$ son los armónicos esféricos, que representan las soluciones angulares. Este método es particularmente útil para problemas con fronteras que coinciden con superficies coordenadas, como esferas, cilindros o planos.

### 3.3. Función de Green en electrostática

La función de Green es un concepto fundamental en la teoría de ecuaciones diferenciales y tiene aplicaciones importantes en electrostática. Formalmente, la función de Green $G(\mathbf{r},\mathbf{r}')$ satisface:

$$
\nabla^2 G(\mathbf{r},\mathbf{r}') = -4\pi \delta(\mathbf{r}-\mathbf{r}')
$$

Esta ecuación describe el potencial creado por una carga puntual unitaria en la posición $\mathbf{r}'$. La utilidad de la función de Green radica en que nos permite expresar la solución general para el potencial electrostático como:

$$
\phi(\mathbf{r}) = \frac{1}{4\pi\epsilon_0}\int_V G(\mathbf{r},\mathbf{r}')\rho(\mathbf{r}')d^3r' + \frac{1}{4\pi}\oint_{\partial V} \left[ G\frac{\partial\phi}{\partial n'} - \phi\frac{\partial G}{\partial n'} \right] da'
$$

El primer término representa la contribución de las cargas en el volumen, mientras que el segundo término contiene las contribuciones de las condiciones de frontera. En el caso más simple de espacio infinito sin fronteras, la función de Green toma la forma familiar:

$$
G(\mathbf{r},\mathbf{r}') = \frac{1}{|\mathbf{r}-\mathbf{r}'|}
$$

Sin embargo, cuando hay conductores o dieléctricos presentes, la función de Green adquiere formas más complejas que pueden construirse usando técnicas como el método de imágenes.

### 3.4. Método de imágenes

El método de imágenes es una técnica elegante para resolver problemas de potencial electrostático en presencia de superficies conductoras. La idea básica es reemplazar el conductor por cargas ficticias ("imágenes") ubicadas fuera de la región de interés, de modo que el potencial combinado de las cargas reales e imágenes satisfaga automáticamente las condiciones de frontera. Consideremos el ejemplo clásico de una carga puntual $q$ colocada a una distancia $d$ de un plano conductor infinito conectado a tierra. La solución mediante imágenes nos da el potencial en la región $z > 0$ como:

$$
\phi(x,y,z) = \frac{q}{4\pi\epsilon_0}\left( \frac{1}{\sqrt{x^2+y^2+(z-d)^2}} - \frac{1}{\sqrt{x^2+y^2+(z+d)^2}} \right)
$$

El segundo término corresponde al potencial de una carga imagen $-q$ colocada simétricamente al otro lado del plano. Este método no solo proporciona una solución exacta, sino que también ofrece una interpretación física intuitiva del problema. Es particularmente útil para geometrías simples como planos, esferas y cilindros, donde las posiciones y magnitudes de las cargas imágenes pueden determinarse mediante consideraciones geométricas.

### 3.5. Desarrollo multipolar del potencial

El desarrollo multipolar es una herramienta poderosa para analizar el comportamiento del potencial electrostático a grandes distancias de una distribución de carga localizada. Cuando la distancia $r$ al punto de observación es mucho mayor que el tamaño de la distribución de carga ($r \gg a$), podemos expandir el potencial en una serie de términos que dependen de los momentos multipolares de la distribución:

$$
\phi(\mathbf{r}) = \frac{1}{4\pi\epsilon_0}\left[ \frac{Q}{r} + \frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^2} + \frac{1}{2}\sum_{i,j} \frac{\hat{r}_i\hat{r}_j Q_{ij}}{r^3} + \cdots \right]
$$

El primer término corresponde al monopolo ($Q = \int \rho(\mathbf{r}') dV'$), que domina si la distribución tiene carga neta no nula. El segundo término es la contribución dipolar ($\mathbf{p} = \int \mathbf{r}' \rho(\mathbf{r}') dV'$), que describe sistemas globalmente neutros pero con separación de cargas. Los términos siguientes (cuadrupolo $Q_{ij} = \int (3r'_i r'_j - r'^2 \delta_{ij}) \rho(\mathbf{r}') dV'$, etc.) capturan detalles más finos de la distribución de carga. Este desarrollo es particularmente útil porque:
1. Proporciona una aproximación sistemática del potencial a grandes distancias
2. Clasifica las contribuciones según su decaimiento con la distancia
3. Revela las simetrías fundamentales de la distribución de carga
4. Simplifica el cálculo de campos y fuerzas entre distribuciones distantes

## Capítulo 4: Campo magnetostático

### 4.1. Ecuación de continuidad y conservación de carga

En magnetostática, la ecuación de continuidad juega un papel fundamental al expresar la conservación local de la carga eléctrica:

$$
\frac{\partial \rho}{\partial t} + \nabla \cdot \mathbf{J} = 0
$$

En el régimen estacionario que caracteriza a la magnetostática, todas las cantidades son independientes del tiempo ($\partial/\partial t = 0$), por lo que la ecuación se simplifica a:

$$
\nabla \cdot \mathbf{J} = 0
$$

Esta condición implica que las líneas de corriente no tienen fuentes ni sumideros en el régimen estacionario; deben formar lazos cerrados o extenderse al infinito. Físicamente, esto significa que en un circuito de corriente continua, la corriente que entra a un nodo debe ser igual a la que sale (ley de nodos de Kirchhoff). La divergencia nula de $\mathbf{J}$ también garantiza que la carga total en cualquier volumen fijo permanece constante en el tiempo, lo que es consistente con la naturaleza estacionaria de los campos en magnetostática.

### 4.2. Ley de Biot-Savart

La ley de Biot-Savart es la relación fundamental que permite calcular el campo magnético producido por corrientes estacionarias. Para un elemento diferencial de corriente $I d\mathbf{l}$, el campo magnético producido está dado por:

$$
d\mathbf{B} = \frac{\mu_0}{4\pi} \frac{I d\mathbf{l} \times \hat{\mathbf{r}}}{r^2}
$$

Esta expresión muestra varias características importantes del campo magnético:
1. Es perpendicular tanto al elemento de corriente como al vector que une el elemento con el punto de observación
2. Decae con el cuadrado de la distancia
3. Depende de la geometría de la distribución de corriente a través del producto vectorial

Para una distribución volumétrica de corriente $\mathbf{J}(\mathbf{r}')$, la ley se generaliza a:

$$
\mathbf{B}(\mathbf{r}) = \frac{\mu_0}{4\pi} \int \frac{\mathbf{J}(\mathbf{r}') \times (\mathbf{r}-\mathbf{r}')}{|\mathbf{r}-\mathbf{r}'|^3} d^3r'
$$

Esta integral puede evaluarse analíticamente para distribuciones con alta simetría (como alambres rectos infinitos o espiras circulares) o numéricamente para configuraciones más complejas. La ley de Biot-Savart es análoga a la ley de Coulomb en electrostática, pero con la diferencia crucial de que el campo magnético no es central - su dirección está determinada por el producto vectorial, lo que refleja la naturaleza axial (pseudovectorial) del campo $\mathbf{B}$.

### 4.3. Ecuaciones diferenciales de la magnetostática

Las ecuaciones fundamentales que gobiernan los campos magnetostáticos son:

$$
\nabla \cdot \mathbf{B} = 0 \quad \text{(Ausencia de monopolos magnéticos)}
$$
$$
\nabla \times \mathbf{B} = \mu_0 \mathbf{J} \quad \text{(Ley de Ampère diferencial)}
$$

La primera ecuación establece que no existen "cargas magnéticas" aisladas (monopolos) - las líneas de campo $\mathbf{B}$ siempre forman lazos cerrados. La segunda ecuación relaciona el rotacional del campo magnético con la densidad de corriente que lo produce. La forma integral de la ley de Ampère es particularmente útil para cálculos:

$$
\oint_C \mathbf{B} \cdot d\mathbf{l} = \mu_0 I_{\text{enc}}
$$

Esta relación permite calcular campos magnéticos en configuraciones con alta simetría (como solenoides o toroides) donde la integral de línea puede evaluarse fácilmente. Comparando con las ecuaciones de la electrostática:

$$
\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0}, \quad \nabla \times \mathbf{E} = 0
$$

vemos una dualidad fundamental: mientras los campos eléctricos tienen divergencia no nula (fuentes: cargas) pero rotacional nulo (conservativos), los campos magnéticos tienen divergencia nula (sin fuentes escalares) pero rotacional no nulo (fuentes vectoriales: corrientes). Esta dualidad será unificada en las ecuaciones de Maxwell completas.

### 4.4. Potencial vectorial magnético

En magnetostática, el potencial vectorial $\mathbf{A}$ es una herramienta matemática poderosa definida por:

$$
\mathbf{B} = \nabla \times \mathbf{A}
$$

Esta definición automáticamente satisface $\nabla \cdot \mathbf{B} = 0$. En el gauge de Coulomb ($\nabla \cdot \mathbf{A} = 0$), el potencial vectorial satisface la ecuación vectorial de Poisson:

$$
\nabla^2 \mathbf{A} = -\mu_0 \mathbf{J}
$$

cuya solución es:

$$
\mathbf{A}(\mathbf{r}) = \frac{\mu_0}{4\pi} \int \frac{\mathbf{J}(\mathbf{r}')}{|\mathbf{r}-\mathbf{r}'|} d^3r'
$$

Para distribuciones localizadas de corriente, podemos desarrollar $\mathbf{A}$ en una serie multipolar. El término dominante a grandes distancias es el dipolar:

$$
\mathbf{A}(\mathbf{r}) \approx \frac{\mu_0}{4\pi} \frac{\mathbf{m} \times \hat{\mathbf{r}}}{r^2}
$$

donde $\mathbf{m}$ es el momento dipolar magnético:

$$
\mathbf{m} = \frac{1}{2} \int \mathbf{r}' \times \mathbf{J}(\mathbf{r}') d^3r'
$$

El campo dipolar correspondiente es:

$$
\mathbf{B}_{\text{dip}} = \frac{\mu_0}{4\pi} \frac{3(\mathbf{m}\cdot\hat{\mathbf{r}})\hat{\mathbf{r}} - \mathbf{m}}{r^3}
$$

que tiene la misma forma funcional que el campo eléctrico dipolar, mostrando una profunda analogía entre ambos fenómenos.

### 4.5. Medios magnetizables y el campo H

Cuando consideramos materiales magnetizables, introducimos la magnetización $\mathbf{M}$, definida como el momento dipolar magnético por unidad de volumen:

$$
\mathbf{M} = \frac{d\mathbf{m}}{dV}
$$

Esta magnetización produce corrientes de magnetización:

$$
\mathbf{J}_m = \nabla \times \mathbf{M} \quad \text{(volumétrica)}
$$
$$
\mathbf{K}_m = \mathbf{M} \times \hat{n} \quad \text{(superficial)}
$$

Para simplificar los cálculos, definimos el campo auxiliar $\mathbf{H}$:

$$
\mathbf{H} = \frac{\mathbf{B}}{\mu_0} - \mathbf{M}
$$

que satisface:

$$
\nabla \times \mathbf{H} = \mathbf{J}_f \quad \text{(Ley de Ampère para } \mathbf{H})
$$

donde $\mathbf{J}_f$ es la densidad de corriente libre. Para materiales lineales e isótropos:

$$
\mathbf{M} = \chi_m \mathbf{H}
$$
$$
\mathbf{B} = \mu_0(1 + \chi_m)\mathbf{H} = \mu\mathbf{H}
$$

donde $\chi_m$ es la susceptibilidad magnética y $\mu$ la permeabilidad magnética del material. Esta relación clasifica los materiales en:
- Diamagnéticos ($\chi_m < 0$): se magnetizan en oposición al campo aplicado
- Paramagnéticos ($\chi_m > 0$): se magnetizan en la dirección del campo aplicado
- Ferromagnéticos ($\chi_m \gg 1$): presentan magnetización espontánea y no linealidad

### 4.6. Condiciones de frontera en magnetostática

En la interfaz entre dos medios magnéticos, las componentes normales y tangenciales de los campos satisfacen:

$$
B_{1\perp} = B_{2\perp} \quad \text{(Continuidad de } \mathbf{B}_n)
$$
$$
H_{1\parallel} - H_{2\parallel} = K_f \quad \text{(Discontinuidad de } \mathbf{H}_t)
$$

donde $_f$es la densidad de corriente libre superficial perpendicular al plano de incidencia. Estas condiciones son consecuencia directa de las ecuaciones $\nabla \cdot \mathbf{B} = 0$ y $\nabla \times \mathbf{H} = \mathbf{J}_f$. En ausencia de corrientes libres superficiales ($K_f = 0$), la componente tangencial de $\mathbf{H}$ es continua.

Estas condiciones son esenciales para resolver problemas con interfaces entre materiales magnéticos diferentes. Por ejemplo, en la frontera entre un material ferromagnético ($\mu \gg \mu_0$) y el aire, las líneas de $\mathbf{B}$ son casi perpendiculares a la superficie en el lado ferromagnético, similar a como las líneas de $\mathbf{E}$ son perpendiculares a la superficie de un conductor. Este comportamiento es fundamental en el diseño de circuitos magnéticos eficientes.