### Archivo 1: MET-MAT-UNIANDES-FINAL-2015-1t.pdf  
**I. Función gaussiana**  
1. Calcular la transformada de Fourier $\hat{g}_{\sigma}$ de:  
$$
g_{\sigma}(t) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-t^2/(2\sigma^2)} \tag{1.1}
$$  
2. Deducir:  
$$
\int_{-\infty}^{\infty} g_{\sigma}(t)  dt = 1 \tag{1.2}
$$  
3. Calcular:  
$$
\mathcal{F}\left(g_{\sigma_1} * g_{\sigma_2}\right)
$$  
4. Deducir:  
$$
g_{\sigma_1} * g_{\sigma_2} = g_{\sigma}, \quad \text{determinar } \sigma \text{ en función de } \sigma_1 \text{ y } \sigma_2.
$$  
5. Calcular:  
$$
\lim_{\sigma \to 0} g_{\sigma}
$$  
a) En sentido de funciones (límite simple).  
b) En sentido de distribuciones.  
6. Calcular la transformada de Laplace $G_{\sigma}(p)$ de $g_{\sigma}(t)$ usando:  
$$
\operatorname{erf}(z) = \frac{2}{\sqrt{\pi}} \int_{0}^{z} e^{-t^2}  dt \tag{1.3}
$$  
7. ¿Abscisa de sumabilidad? ¿Tiene polos $G_{\sigma}(p)$ en $\mathbb{C}$?  

**II. Funciones de Bessel**  
1. Usando la función generatriz:  
$$
g(t,x) = \exp\left[\frac{x}{2}\left(t - \frac{1}{t}\right)\right] = \sum_{n=-\infty}^{+\infty} J_{n}(x)  t^{n} \tag{2.1}
$$  
mostrar:  
$$
J_{-n}(x) = (-1)^{n} J_{n}(x), \quad J_{n}(-x) = (-1)^{n} J_{n}(x).
$$  
2. Con $t = e^{i\theta}$, mostrar:  
$$
e^{ix \sin \theta} = \sum_{n=-\infty}^{\infty} J_{n}(x) e^{in\theta} \tag{2.2}
$$  
3. Deducir:  
$$
J_{n}(x) = \frac{1}{2\pi} \int_{-\pi}^{\pi} e^{in\theta} e^{-ix \sin \theta}  d\theta \tag{2.3}
$$  
4. Mostrar que la transformada de Laplace $F_n$ de $J_n$ es:  
$$
F_{n}(p) = \frac{1}{2\pi} \int_{-\pi}^{\pi} \frac{e^{in\theta}}{p + i \sin \theta}  d\theta \tag{2.4}
$$  
5. Calcular $F_n(p)$ por residuos.  
6. Demostrar:  
$$
\int_{0}^{t} J_{0}(x) J_{0}(t-x)  dx = \sin t \quad (t > 0) \tag{2.5}
$$  

**III. Ecuación de Laplace**  
Bola dieléctrica de radio $R$ con campo interno constante $\mathbf{E}_0 = E_0 \hat{\mathbf{z}}$. Potencial $V(r,\theta,\phi)$ satisface $\Delta V = 0$ para $r > R$ y $\lim_{r \to \infty} V = 0$.  
1. Condición de frontera en $r = R$.  
2. Resolver para $V(r,\theta,\phi)$ ($r > R$).  
3. Escribir $V$ y $\mathbf{E} = -\nabla V$ en coordenadas cartesianas.  

---

### Archivo 2: MET-MAT-UNIANDES-FINAL-2023-1.pdf  
**1. Primera parte (50 puntos)**  
Oscilador armónico forzado:  
$$
m \frac{d^{2}X}{dt^{2}} + b \frac{dX}{dt} + kX = F(t), \quad X(0) = 0, \quad \dot{X}(0) = 0 \tag{1}
$$  
1. (5 pts) Transformar con Fourier para obtener $tilde{X}(\omega)$ en términos de $\Gamma = b/(2m)$, $\omega_0 = \sqrt{k/m}$, y $\tilde{F}(\omega)$.  
2. (10 pts) Calcular $\mathcal{F}\left\{ H(t) e^{-\gamma t} \right\}$ ($\gamma > 0$).  
3. (35 pts) Si $F(t) = F_0 H(t) e^{-\gamma t}$, usar residuos para hallar $X(t)$ ($t > 0$ y $t < 0$). Asumir $\Gamma > \omega_0$.  

**2. Segunda parte (50 puntos)**  
Esferas concéntricas: radio $a$ (potencial $\Phi(a,\theta,\phi) = V_a(\theta)$) y radio $b = 2a$ (potencial $\Phi(b,\theta,\phi) = V_b(\theta)$).  
(a) (25 pts) Hallar potencial $\Phi(r,\theta,\phi)$ en:  
- Región 1: $r < a$  
- Región 2: $a < r < b$  
- Región 3: $r > b$  
(Expresar coeficientes mediante integrales.)  
(b) Hallar coeficientes para:  
$$
V_a(\theta) = 2V_0 \sin^2 \theta, \quad V_b(\theta) = V_0 \left(2 + \cos(2\theta)\right)
$$  
(c) (15 pts bono) Solución explícita en las tres regiones.  

---

### Archivo 3: MET-MAT-UNIANDES-PARCIAL1-2022-1t.pdf  
**I. Cálculo de integrales (residuos)**  
1.  
$$
\int_{-\infty}^{\infty} \frac{dx}{1 + x^4} \tag{1.1}
$$  
2.  
$$
\int_{0}^{2\pi} \frac{4 \sin(3\theta) \sin \theta}{5 - 4 \cos \theta}  d\theta \tag{1.2}
$$  

**II. Distribuciones**  
1. Calcular en sentido de distribuciones:  
$$
\frac{d^{2}}{dx^{2}} |x| \tag{2.1}
$$  
*Aplicación:* Plano infinito $Oyz$ con densidad superficial $\sigma$.  
- Densidad volumétrica $\rho(x,y,z)$.  
- Resolver $\Delta V = -\rho/\epsilon_0$ para potencial $V$.  
1. Esfera hueca (radio $R$, carga total $Q$ uniforme).  
- Escribir $\rho(\mathbf{r})$ con delta de Dirac.  
- Verificar $\int_{\mathbb{R}^3} \rho(\mathbf{r})  d^3\mathbf{r} = Q$.

### Taller 2: UNIANDES-Taller-2.pdf  
**1. Función Zeta de Riemann (25 puntos)**  
1. Encontrar coeficientes de Fourier de $x) = x^3$ en $[-\pi, \pi)$con período $2\pi$.  
2. Graficar numéricamente:  
$$
g_N(x) = \sum_{n=-N}^{N} c_n(g) e^{i n x} \quad \text{para} \quad N \in \{2, 5, 20\}.
$$  
3. Dados coeficientes de Fourier de $h(x) = x^2$ 
$$
a_0 = \frac{\pi^2}{3}, \quad a_n = \frac{4(-1)^n}{n^2} \quad (n \geq 1), \quad b_n = 0,
$$  
demostrar:  
$$
\sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6}, \quad \sum_{n=1}^{\infty} \frac{1}{n^4} = \frac{\pi^4}{90}.
$$  
4. Usar resultados para demostrar:  
$$
\sum_{n=1}^{\infty} \frac{1}{n^6} = \frac{\pi^6}{945}.
$$  

**2. Concentración de partículas (25 puntos)**  
Ecuación:  
$$
D \frac{\partial^2 \lambda}{\partial x^2} - \Gamma \lambda = \frac{\partial \lambda}{\partial t}, \quad \lambda(x,0) = N \delta(x - x_0).
$$  
1. Demostrar solución:  
$$
\lambda(x,t) = \frac{N H(t)}{\sqrt{4\pi D t}} e^{-\Gamma t} e^{-\frac{(x-x_0)^2}{4Dt}}.
$$  
2. Mostrar que $int_{-\infty}^{\infty} \lambda(x,t)  dx \neq \text{const.}$, interpretar $N$ y $\Gamma$, y casos $\Gamma > 0$, $\Gamma < 0$.  
3. Explicar límites $D \to 0$ y $D \to \infty$.  

**3. Distribución de carga (20 puntos)**  
Dado factor de forma:  
$$
F(\mathbf{k}) = (2\pi)^{-3/2} \left(1 + \frac{k^2}{a^2}\right)^{-1},
$$  
encontrar $\rho(\mathbf{r})$ usando coordenadas esféricas, donde:  
$$
F(\mathbf{k}) = \frac{1}{(2\pi)^{3/2}} \int_{\mathbb{R}^3} \rho(\mathbf{r}) e^{i \mathbf{k} \cdot \mathbf{r}}  d^3\mathbf{r}.
$$  

**4. Resorte forzado (30 puntos)**  
Ecuación:  
$$
m \ddot{X} + \gamma \dot{X} + k X = F(t), \quad X(0)=X_0, \quad \dot{X}(0)=V_0.
$$  
(a) Aplicar transformada de Laplace $\widetilde{X}(q) = \int_0^\infty X(t) e^{-qt}  dt$ para ecuación algebraica.  
(b) Demostrar:  
$$
\mathcal{L}\{\cos(\omega t)\} = \frac{q}{q^2+\omega^2}, \quad \mathcal{L}\{\sin(\omega t)\} = \frac{\omega}{q^2+\omega^2},
$$  
$$
\mathcal{L}\{e^{at}\cos(\omega t)\} = \frac{q-a}{(q-a)^2+\omega^2}, \quad \mathcal{L}\{e^{at}\sin(\omega t)\} = \frac{\omega}{(q-a)^2+\omega^2}.
$$  
(c) Expresar $X(t)$ usando convolución.  
(d) Hallar $X(t)$ para:  
- $F(t) = P \delta(t)$  
- $F(t) = F_0$  
- $F(t) = F_0 \cos(\omega t)$ (comportamiento asintótico).  

---

### Taller 1: UNIANDES-Taller-1.pdf  
**1. Álgebra de complejos (20 puntos)**  
**1.1 (10 puntos)**  
(a) Demostrar $\mathbb{C}$ es grupo abeliano bajo suma. ¿Grupo bajo multiplicación? ¿Bajo conjugación?  
(b) Mostrar isomorfismo entre $\mathbb{C}$ y matrices $\begin{pmatrix} x & -y \\ y & x \end{pmatrix}$ (suma y multiplicación).  
(c) Usando $z = r(\cos\theta + i\sin\theta)$, mostrar isomorfismo con matrices de rotación $\begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$.  

**1.2 (10 puntos)**  
Para $f(z) = R(r,\theta) e^{i\Theta(r,\theta)}$, demostrar condiciones de Cauchy-Riemann en polares:  
$$
\frac{\partial R}{\partial r} = \frac{R}{r} \frac{\partial \Theta}{\partial \theta}, \quad \frac{1}{r} \frac{\partial R}{\partial \theta} = -R \frac{\partial \Theta}{\partial r}.
$$  

**2. Integral polinómica (20 puntos)**  
Evaluar:  
$$
\int_{-\infty}^{\infty} \frac{x  dx}{(a x^2 + b x + c)^2}, \quad b^2 < 4ac.
$$  
Explicar por qué $b^2 < 4ac$.  

**3. Colisiones cuánticas (20 puntos)**  
Calcular:  
$$
I = \int_{-\infty}^{\infty} e^{i p t} \frac{\sin t}{t}  dt.
$$  
(a) Escribir $I = I_+ + I_-$ usando $\sin t = \frac{e^{it} - e^{-it}}{2i}$.  
(b) Describir contorno para:  
- $p < -1$  
- $-1 < p < 0$  
- $0 < p < 1$  
- $p > 1$.  
(c) Evaluar $I_+$ e $I_-$ para cada caso.  
(d) Dar $I$ para $|p| > 1$ y $|p| < 1$.  
(e) Explicar $p = \pm 1$.  

**4. Trayectorias celestes (20 puntos)**  
Trayectoria:  
$$
r(\theta) = \frac{r_0}{1 + \varepsilon \cos\theta}.
$$  
Área entre $\theta_1$ y $\theta_2$:  
$$
A = \frac{1}{2} \int_{\theta_1}^{\theta_2} r^2(\theta)  d\theta.
$$  
1. Expresión general para $A$. Para órbita completa ($\theta_1=0$, $\theta_2=2\pi$), indicar cómo usar residuos.  
2. Área para órbita circular ($\varepsilon=0$) entre $\theta_1,\theta_2$ y completa.  
3. ¿Por qué no se puede usar residuos para $\varepsilon=1$ (parabólica) y $\varepsilon>1$ (hiperbólica)? Interpretación física.  
4. Calcular área para órbita elíptica ($\varepsilon<1$) con residuos.  
5. Si $\varepsilon = \sqrt{a^2 - b^2}/a$, hallar $r_0$ para una elipse.  

**5. Integral con contorno (20 puntos)**  
Evaluar:  
$$
\int_0^\infty \cos(x^4)  dx, \quad \int_0^\infty \sin(x^4)  dx.
$$  
*Ayuda:* Usar sector circular con ángulo $\pi/8$.