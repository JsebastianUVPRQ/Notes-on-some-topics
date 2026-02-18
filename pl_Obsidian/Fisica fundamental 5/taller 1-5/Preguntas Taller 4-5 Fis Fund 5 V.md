

---

## Taller 04

### Problema 19 — Pozo cuadrado infinito
Considere una partícula de masa $m$ en un pozo unidimensional infinito  
$V(x) = 0$ para $0 \le x \le L$, $+\infty$ para $x < 0$ y $x > L$.  

(a) Muestre que las funciones propias normalizadas son  
$\psi_n(x) = \sqrt{\frac{2}{L}} \operatorname{sen}(k_n x)$, $0 \le x \le L$, con $k_n = n\pi/L$, $n = 1, 2, 3, \dots$. Encuentre además los correspondientes valores propios de energía $E_n$.  

(b) En el tiempo $t = 0$ la partícula se describe por el paquete de ondas $\psi(x, t = 0) = N x (L - x)$. Si este paquete de ondas está normalizado a uno,  
 (i) encuentre la constante de normalización.  
 (ii) encuentre los coeficientes $a_n$ de la expansión de $\psi(x, t = 0)$ en la base de funciones propias $\psi_n$:  
$$\psi(x, t = 0) = \sum_{n=1}^{\infty} a_n \psi_n(x).$$  

(c) Escriba la serie que define la función de onda $\psi(x, t)$ para cualquier tiempo $t$. Sea $T = \pi\hbar/E_1$ el tiempo definido en términos de la energía $E_1 = \frac{\hbar^2 \pi^2}{2m L^2}$ del estado base. Grafique la función $\psi(x, t)$ para tiempos $t$ que son múltiplos enteros de $T$, $t = \nu T$, $\nu \in \mathbb{Z}$. ¿Cómo se diferencia el caso cuando $\nu$ es par del caso cuando $\nu$ es impar?

### Problema 20 — Potencial localizado idealizado por una función delta de Dirac
Un potencial localizado se puede idealizar mediante la función delta de Dirac, $V(x) = -g \delta(x)$ con $g > 0$.  

(a) Existe exactamente un estado discreto en ese potencial. Encuentre su función propia y la respectiva energía propia.  

(b) Calcule la incertidumbre de la posición $\Delta x$ y del momento $\Delta p$ para este estado discreto.  

(c) Calcule la transformada de Fourier del estado discreto y grafique la función de onda en el espacio de momento. ¿Dónde se encuentra el máximo de la distribución de momento?  

**Ayuda:** La condición de acople en $x = 0$ para la solución del potencial $\delta$ para $x > 0$ y para $x < 0$ se obtiene mediante integración de la ecuación de Schrödinger en un intervalo infinitesimal $(-\epsilon, \epsilon)$ alrededor del origen:  
$$lim_{\epsilon \to 0} \int_{-\epsilon}^{\epsilon} \left( -\frac{\hbar^2}{2m} \frac{d^2}{dx^2} - g\delta(x) \right) \psi(x) \, dx = \lim_{\epsilon \to 0} \int_{-\epsilon}^{\epsilon} E\psi(x) \, dx.$$

### Problema 21 — Potencial de paso: reflexión cuántica
Considere una partícula de masa $m$ en el salto de potencial (o potencial de paso)  
$$V(x) = \begin{cases} 0, & \text{para } x \ge 0, \\ V_0 = -\dfrac{\hbar^2 k_0^2}{2m}, & \text{para } x < 0. \end{cases}$$ 

(a) En cada intervalo $x < 0$ y $x > 0$ encuentre dos soluciones linealmente independientes de la ecuación estacionaria de Schrödinger (EES) para una energía dada $E$. Considere los casos $E = \hbar^2 k^2/(2m) > 0$ y $E = -\hbar^2 k^2/(2m) < 0$ separadamente. Explique por qué el espectro de energías es continuo.  

(b) Una partícula viene desde $x = +\infty$ con energía $E = \hbar^2 k^2/(2m)$. Explique por qué la solución de la EES debe tener la forma  
$$\begin{array}{rcl} 
\psi(x) & = & e^{-ikx} + R e^{ikx} \quad \text{para } x \ge 0, \\ 
\psi(x) & = & T e^{-iqx} \quad \text{para } x < 0, 
\end{array} \quad \text{con } q^2 = k^2 + k_0^2.$$  
Encuentre explícitamente $R$ y $T$ como función de $k$.  

(c) Muestre que la amplitud de reflexión para energías cercanas a cero es  
$R \underset{k \to 0}{\approx} -1 + 2bk + \mathcal{O}(k^2)$, con $b = 1/k_0$, y por lo tanto la probabilidad de reflexión es  
$P_R \underset{k \to 0}{\approx} 1 - 4bk + \mathcal{O}(k^2)$. ¿Cómo es la probabilidad de reflexión en el límite $E \to \infty$?

### Problema 22 — Efecto túnel en una barrera de potencial
Considere una partícula de masa $m$ bajo la acción del potencial unidimensional  
$$V(x) = \begin{cases} 
V_0 = \dfrac{\hbar^2 k_0^2}{2m}, & -a \le x \le a, \\ 
0, & x < -a \;\land\; x > a. 
\end{cases}$$  
Suponga que la partícula se acerca a la barrera desde $-\infty$ con energía cinética $E = \dfrac{\hbar^2 k^2}{2m} < V_0$. Entonces la solución de la ecuación estacionaria de Schrödinger tiene la forma $\phi(x) = A e^{ikx} + B e^{-ikx}$ en la región $x \le -a$ y $\phi(x) = C e^{ikx}$ en la región $x \ge a$. Muestre que la probabilidad de transmisión de la partícula a través de la barrera está dada por  
$$P(E) = \left| \frac{C}{A} \right|^2 = \frac{1}{1 + \left(1 + \frac{\epsilon^2}{4}\right) \sinh^2(2qa)} = \frac{1 - E/V_0}{(1 - E/V_0) + \frac{V_0}{4E} \sinh^2(2qa)},$$  
donde $q = \sqrt{k_0^2 - k^2}$ y $\epsilon = \frac{q}{k} - \frac{k}{q}$. En particular, en el límite $aq \gg 1$, la probabilidad de transmisión es  
$$P(E) \approx \frac{16E(V_0 - E)}{V_0^2} e^{-4qa}. \qquad (2)$$  

**Aplicación:** Un núcleo de uranio 238 ($Q = +92e$) dura aproximadamente $4.5 \times 10^9$ años antes de que decaiga por emisión de una partícula $\alpha$ ($q = +2e$, $M = 4M_{\text{protón}}$).  
a) Suponiendo que la partícula $\alpha$ es un punto, y el núcleo tiene aproximadamente $8\,\text{fm}$ de radio, estime la altura de la barrera de Coulomb.  
b) La partícula alfa, cuando está libre, tiene energía cinética $\approx 4\,\text{MeV}$. Estime el ancho de la barrera.  
c) Suponiendo que el pozo cuadrado tiene $U = 0$ en el interior (y $U = 0$ lejos del núcleo), calcule la rapidez de la partícula alfa y con cuánta frecuencia golpea el interior de la barrera, y a partir de esto estime la vida del uranio.  

Sugerencia: En este ejercicio use (2). En c) sustituya la barrera de Coulomb $1/r$ con una barrera rectangular “promediada” de ancho igual a $\frac{1}{3}$ del calculado en b).

---
## Taller 05

### Problema 21 — Espacios de Hilbert
Repase las definiciones y propiedades fundamentales de los espacios de Hilbert, del dual de un espacio de Hilbert y de operadores actuando sobre éstos.

### Problema 22 — Función de onda en representación de momento
Considere la función de onda unidimensional $\psi(x) = Ne^{-|x|}$.  
(a) Encuentre la constante de normalización $N$.  
(b) Encuentre los coeficientes de expansión de $\psi(x)$ en onda planas.  
(c) Encuentre la representación de momento $\hat{\psi}(p)$ de $\psi(x)$.

### Problema 23 — Operadores de posición y momento
Considere los operadores de posición y momento actuando sobre el espacio de funciones cuadráticamente integrables.  
(a) Demuestre que $\mathbf{r}$ y $\mathbf{p}$ son hermíticos.  
(b) Para el caso de funciones cuadráticamente integrables en una dimensión, demuestre que $[p, x] = -i\hbar$.  

**Observación:** Recuerde que un operador $A$ es hermítico si para cualesquier par de funciones de onda $\xi(\mathbf{r})$$ $\$rphi(\mathbf{r})$ se satisface  
$$\langle \phi | \hat{A} | \xi \rangle = \langle \xi | \hat{A} | \phi \rangle^* .$$