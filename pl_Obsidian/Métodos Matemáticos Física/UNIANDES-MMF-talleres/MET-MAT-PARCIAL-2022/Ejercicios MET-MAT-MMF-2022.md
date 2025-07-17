### **Ejercicios del taller**

#### **1. Función de Green en coordenadas esféricas**  
**Punto 1 (5 puntos):**  
Explicar por qué la distribución delta en coordenadas esféricas se puede escribir como:  
$$
\delta^3(\mathbf{r} - \mathbf{r}') = \frac{1}{r^2 \sin\theta} \delta(r - r') \delta(\theta - \theta') \delta(\phi - \phi') \tag{3}
$$  

**Punto 2 (15 puntos):**  
Escribir la distribución delta angular:  
$$
\delta(\Omega - \Omega') \equiv \frac{1}{\sin\theta} \delta(\theta - \theta') \delta(\phi - \phi') \tag{4}
$$  
como una suma de armónicos esféricos:  
$$
\delta(\Omega - \Omega') = \sum_{l=0}^\infty \sum_{m=-l}^l D_{lm} Y_l^m(\theta, \phi) \tag{5}
$$  
Encontrar los coeficientes $D_{lm}$ que determinan la serie de Fourier.  

**Punto 3 (15 puntos):**  
Usando la condición de que $G(\mathbf{r}, \mathbf{r}')$ es finita en todos los puntos, escribir la solución más general que debe satisfacer $G(\mathbf{r}, \mathbf{r}')$ cuando $r < r'$ y $r > r'$. Recordar que la solución general a $\nabla^2 f = 0$ en coordenadas esféricas es:  

$$
\delta^3(\mathbf{r} - \mathbf{r}') = \frac{1}{r^2 \sin\theta} \delta(r - r') \delta(\theta - \theta') \delta(\phi - \phi') \tag{3}$$


**Punto 4 (65 puntos):**  
Usar las condiciones de frontera (continuidad de $G$ en $r = r'$ y discontinuidad en su derivada debido a la delta) para encontrar $G(\mathbf{r}, \mathbf{r}')$. Demostrar que la función de Green es:  
La función de Green para la ecuación de Laplace en coordenadas esféricas es:  
$$
G(\mathbf{r}, \mathbf{r}') = -\frac{1}{r_>} \sum_{l=0}^\infty \sum_{m=-l}^l \left( \frac{r_<}{r_>} \right)^l \frac{Y_l^m(\theta, \phi) Y_l^{m*}(\theta', \phi')}{2l + 1} \tag{6}
$$  
**Explicación**:  
- $r_< = \min(r, r')$ y $r_> = \max(r, r')$: Garantizan la convergencia de la serie tanto para $r < r'$ como $r > r'$.  
- $Y_l^m(\theta, \phi)$: Armónicos esféricos que representan la dependencia angular.  
- El coeficiente $1/(2l + 1)$ surge de la normalización de los armónicos esféricos y la ortogonalidad en la expansión de la delta angular .    
donde $r_< = \min(r, r')$ y $r_> = \max(r, r')$.  

---

### **Explicación detallada de los ejercicios**  

#### **1. Distribución delta en coordenadas esféricas**  
La delta de Dirac en tres dimensiones en coordenadas esféricas incorpora el Jacobiano de la transformación de coordenadas cartesianas a esféricas. El volumen diferencial en esféricas es $dV = r^2 \sin\theta \, dr \, d\theta \, d\phi$, lo que explica el factor $1/(r^2 \sin\theta)$ en la ecuación (3) .  

#### **2. Delta angular y armónicos esféricos**  
La delta angular $\delta(\Omega - \Omega')$ se expande en armónicos esféricos mediante una serie de Fourier esférica. Los coeficientes $D_{lm}$ se obtienen usando la ortogonalidad de los armónicos esféricos:  
$$
\int Y_l^{m*}(\theta, \phi) Y_{l'}^{m'}(\theta, \phi) \sin\theta \, d\theta \, d\phi = \delta_{ll'} \delta_{mm'}.
$$  
Esto implica que $D_{lm} = Y_l^{m*}(\theta', \phi')$ .  

#### **3. Solución general para $\nabla^2 f = 0$**  
La solución general en coordenadas esféricas combina términos regulares ($r^l$) y singulares ($r^{-(l+1)}$). Para $G(\mathbf{r}, \mathbf{r}')$, se eligen términos que evitan singularidades en $r = 0$ y $r \to \infty$:  
- Para $r < r'$, se usan términos $r^l$.  
- Para $r > r'$, se usan términos $r^{-(l+1)}$ .  

#### **4. Condiciones de frontera y función de Green**  
Las condiciones de continuidad y discontinuidad en $r = r'$ determinan los coeficientes de la serie. La discontinuidad en la derivada se calcula integrando la ecuación diferencial $\nabla^2 G = \delta^3(\mathbf{r} - \mathbf{r}')$ sobre una esfera infinitesimal en $r = r'$, lo que lleva a la forma final (6) .  

---
