
### Resolución Paso a Paso

---

#### **Punto 1 (5 puntos): Explicación de la distribución delta en coordenadas esféricas**

La distribución delta tridimensional $\delta^3(\mathbf{r} - \mathbf{r}')$ en coordenadas cartesianas es:
$$
\delta^3(\mathbf{r} - \mathbf{r}') = \delta(x - x') \delta(y - y') \delta(z - z').
$$

Al cambiar a coordenadas esféricas $(r, \theta, \phi)$, se debe considerar el **Jacobiano de la transformación**. El elemento de volumen en coordenadas esféricas es:
$$
dV = r^2 \sin\theta  dr  d\theta  d\phi.
$$

Para que la integral de la delta sobre todo el espacio sea 1, la delta debe compensar el factor del Jacobiano. La integral es:
$$
\int \delta^3(\mathbf{r} - \mathbf{r}')  dV = \int_0^\infty \int_0^\pi \int_0^{2\pi} \delta^3(\mathbf{r} - \mathbf{r}')  r^2 \sin\theta  dr  d\theta  d\phi = 1.
$$

Si se expresa la delta como:
$$
\delta^3(\mathbf{r} - \mathbf{r}') = \frac{1}{r^2 \sin\theta} \delta(r - r') \delta(\theta - \theta') \delta(\phi - \phi'),
$$
al sustituir en la integral:
$$
\int_0^\infty \int_0^\pi \int_0^{2\pi} \left[ \frac{1}{r^2 \sin\theta} \delta(r - r') \delta(\theta - \theta') \delta(\phi - \phi') \right] r^2 \sin\theta  dr  d\theta  d\phi = \int_0^\infty \delta(r - r')  dr \int_0^\pi \delta(\theta - \theta')  d\theta \int_0^{2\pi} \delta(\phi - \phi')  d\phi = 1,
$$
si $r' > 0$, $\theta' \in (0, \pi)$, y $\phi' \in [0, 2\pi)$. Los factores $r^2 \sin\theta$ se cancelan, y la integral es 1, como debe ser.

**Conclusión:**  
La expresión (3) es correcta debido al Jacobiano de la transformación, que asegura la normalización adecuada de la delta.

---

#### **Punto 2 (15 puntos): Delta angular como suma de armónicos esféricos**

La distribución delta angular se define como:
$$
\delta(\Omega - \Omega') = \frac{1}{\sin\theta} \delta(\theta - \theta') \delta(\phi - \phi').
$$

Se busca expresarla como:
$$
\delta(\Omega - \Omega') = \sum_{l=0}^\infty \sum_{m=-l}^l D_{lm} Y_l^m(\theta, \phi).
$$

Los armónicos esféricos $Y_l^m(\theta, \phi)$ forman una base ortonormal completa en la esfera unidad. La relación de completitud es:
$$
\sum_{l=0}^\infty \sum_{m=-l}^l Y_l^m(\theta, \phi) Y_l^{m*}(\theta', \phi') = \delta(\cos\theta - \cos\theta') \delta(\phi - \phi'),
$$
donde $*$ denota conjugado complejo.

Usando la propiedad de la delta para cambios de variable:
$$
\delta(\theta - \theta') = \delta(\cos\theta - \cos\theta') \left| \frac{d(\cos\theta)}{d\theta} \right|^{-1} = \delta(\cos\theta - \cos\theta') \frac{1}{\sin\theta},
$$
ya que $\frac{d(\cos\theta)}{d\theta} = -\sin\theta$ y $\sin\theta > 0$ para $\theta \in (0, \pi)$. Sustituyendo:
$$
\delta(\Omega - \Omega') = \frac{1}{\sin\theta} \delta(\theta - \theta') \delta(\phi - \phi') = \delta(\cos\theta - \cos\theta') \delta(\phi - \phi').
$$

Comparando con la completitud:
$$
\delta(\Omega - \Omega') = \sum_{l=0}^\infty \sum_{m=-l}^l Y_l^m(\theta, \phi) Y_l^{m*}(\theta', \phi').
$$

De la serie (5), se tiene:
$$
\delta(\Omega - \Omega') = \sum_{l=0}^\infty \sum_{m=-l}^l D_{lm} Y_l^m(\theta, \phi).
$$

Igualando ambas expresiones:
$$
\sum_{l=0}^\infty \sum_{m=-l}^l D_{lm} Y_l^m(\theta, \phi) = \sum_{l=0}^\infty \sum_{m=-l}^l Y_l^m(\theta, \phi) Y_l^{m*}(\theta', \phi').
$$

Por la independencia lineal de los armónicos esféricos:
$$
D_{lm} = Y_l^{m*}(\theta', \phi').
$$

**Conclusión:**  
Los coeficientes son:
$$
D_{lm} = Y_l^{m*}(\theta', \phi') = \overline{Y_l^m(\theta', \phi')},
$$
y la serie es:
$$
\boxed{\delta(\Omega - \Omega') = \sum_{l=0}^\infty \sum_{m=-l}^l Y_l^{m*}(\theta', \phi') Y_l^m(\theta, \phi)}
$$

---

#### **Punto 3 (15 puntos): Solución general para la función de Green**

La función de Green $G(\mathbf{r}, \mathbf{r}')$ satisface:
$$
\nabla^2 G(\mathbf{r}, \mathbf{r}') = -4\pi \delta^3(\mathbf{r} - \mathbf{r}').
$$

Para $\mathbf{r} \neq \mathbf{r}'$, $\nabla^2 G = 0$. La solución general de $\nabla^2 f = 0$ en coordenadas esféricas es una combinación lineal de soluciones de la forma:
$$
f(r, \theta, \phi) = \sum_{l=0}^\infty \sum_{m=-l}^l \left[ A_{lm} r^l + B_{lm} r^{-l-1} \right] Y_l^m(\theta, \phi),
$$
pero $G$ debe ser finita en todos los puntos, lo que impone restricciones diferentes en las regiones $r < r'$ y $r > r'$:$- **Para $r < r'$ (región interior):**  
  Cerca de $r = 0$, $G$ debe ser finita. La solución $r^{-l-1}$ diverge en $r = 0$, por lo que $B_{lm} = 0$. La solución general es:
  $$
  G(\mathbf{r}, \mathbf{r}') = \sum_{l=0}^\infty \sum_{m=-l}^l A_{lm}(r')  r^l  Y_l^m(\theta, \phi), \quad r < r'.
  $$
  Los coeficientes $A_{lm}(r')$ dependen de $r'$ (la posición de la fuente).

- **Para $r > r'$ (región exterior):**  
  Cuando $r \to \infty$, $G$ debe ser finita (o tender a cero). La solución $r^l$ diverge en $r = \infty$, por lo que $A_{lm} = 0$. La solución general es:
  $$
  G(\mathbf{r}, \mathbf{r}') = \sum_{l=0}^\infty \sum_{m=-l}^l B_{lm}(r')  r^{-l-1}  Y_l^m(\theta, \phi), \quad r > r'.
  $$
  Los coeficientes $B_{lm}(r')$ dependen de $r'$.

**Conclusión:**  
La solución más general, finita en todos los puntos, es:
- Para $r < r'$:
  $$
  \boxed{G(\mathbf{r}, \mathbf{r}') = \sum_{l=0}^\infty \sum_{m=-l}^l A_{lm}(r')  r^l  Y_l^m(\theta, \phi)}
  $$
- Para $r > r'$:
  $$
  \boxed{G(\mathbf{r}, \mathbf{r}') = \sum_{l=0}^\infty \sum_{m=-l}^l B_{lm}(r')  r^{-l-1}  Y_l^m(\theta, \phi)}
  $$
Los coeficientes $A_{lm}(r')$ y $B_{lm}(r')$ se determinan imponiendo continuidad en $r = r'$ y la discontinuidad en la derivada radial debida a la delta. Esto no se solicita en este punto.

--- 

**Final**  
Las respuestas están dadas en los recuadros correspondientes.