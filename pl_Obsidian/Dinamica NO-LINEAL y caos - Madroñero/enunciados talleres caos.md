## Taller 1: Dinámica No Lineal y Caos Cuántico

### Problema 1 — Espacio de fase de un sistema dinámico lineal  
*(6 puntos)*

Considere el sistema dinámico bidimensional gobernado por la ecuación  
$$
\dot{x} = A x, \qquad \text{con } A = \begin{pmatrix} a & 1 \\ 0 & a \end{pmatrix}.
$$  
Encuentre la solución general de las curvas $y = y(x)$ del espacio de fase de este sistema. $x$ y $y$ son las componentes del vector $\mathbf{x}$. Grafique en particular el espacio de fase en la vecindad del punto fijo $\mathbf{x}=0$ para los siguientes casos:  
(i) $a < -1$, (ii) $a = -1$, (iii) $-1 < a < 0$, (iv) $a = 0$ y (v) $a > 0$.

---

### Problema 2 — Flujos bidimensionales  
*(5 puntos)*

La dinámica de un péndulo ideal de longitud $\ell$ está descrita por la ecuación  
$$
\frac{d^2\theta}{dt^2} + \omega^2 \sin\theta = 0, \quad \text{donde } \omega = \sqrt{g/\ell},
$$  
y $g$ es la aceleración de la gravedad. Con la transformación $\tau = \omega t$ la ecuación se reduce a  
$$
\ddot{\theta} + \sin\theta = 0, \qquad (1)
$$  
donde el punto denota la derivada con respecto a $\tau$.

(a) Encuentre todos los puntos fijos de (1) clasificándolos según su estabilidad. Para ello linealice el sistema alrededor de los puntos fijos.  
(b) Ilustre esquemáticamente el espacio de fase de (1) partiendo de la forma del espacio de fase en las vecindades de los puntos fijos.

---

### Problema 3 — Mapeo Logístico: problema numérico  
*(12 puntos)*

Considere la ecuación recursiva del mapeo logístico  
$$
x_{n+1} = r x_n (1 - x_n), \quad r \in [0,4]. \qquad (2)
$$

(a) Muestre que los puntos fijos de orden 2 están dados por  
$$
x = \frac{1}{r} \left( r+1 \pm \sqrt{(r+1)(r-3)} \right).
$$

(b) Reproduzca el diagrama de bifurcación. Para ello escriba un programa (en Mathematica, por ejemplo) que haga lo siguiente:  
(i) Genere un conjunto $\Omega_0$ de $n_0$ condiciones iniciales aleatorias en el intervalo $[0,1]$, para $n_0$ dado.  
(ii) Genere el conjunto $R_0$ con $n_r$ puntos distribuidos homogéneamente en un intervalo $[r_{\min}, r_{\max}]$. Aquí $n_r$, $r_{\min}$ y $r_{\max}$ son valores dados.  
(iii) Para cada $x_0 \in \Omega_0$ y para cada $r \in R_0$ el programa debe propagar la recursión (2) hasta encontrar $x_{400}$. Con estos valores crear una lista que contenga las $n_0 \times n_r$ parejas de la forma $(r, x_{400})$.  
(iv) Graficar la lista anterior para obtener finalmente el mapeo logístico.

**Ayuda:** Funciones de Mathematica® que pueden resultarle útiles: `Random`, `Do`, `Append`, `ListPlot`, `Solve`, `NSolve`.

---

## Taller 2

### Problema 4 — Péndulo: parte analítica  

Considere un péndulo de masa $m$ y longitud $\ell$ que forma un ángulo $\theta$ con el eje vertical.

(a) **[2p]** Suponga que el péndulo oscila alcanzando un ángulo máximo $\theta_{\max} \in (0,\pi)$. Demuestre que el periodo está dado por  
$$
T = 4\sqrt{\frac{\ell}{2g}} \int_0^{\theta_{\max}} \frac{d\theta}{\sqrt{\cos\theta - \cos\theta_{\max}}} 
   = 4\sqrt{\frac{\ell}{g}} K(\kappa),
$$  
donde $K(\kappa) = \int_0^{\pi/2} \frac{d\varphi}{\sqrt{1-\kappa^2 \sin^2\varphi}}$ es la integral elíptica completa de primera clase y $\kappa = \sin(\theta_{\max}/2)$.  
**Ayuda:** $\cos\theta = 1 - 2\kappa^2 \sin^2\varphi$.

(b) **[2p]** Suponga que $\theta_{\max} \ll 1$. Demuestre que  
$$
T \approx \frac{2\pi}{\omega_0} \left(1 + \frac{\theta_{\max}^2}{16}\right), \quad \text{con } \omega_0 = \sqrt{\frac{g}{\ell}}.
$$  
Por lo tanto, en el límite de pequeñas oscilaciones ($\theta_{\max}\to0$) se reproduce el periodo del oscilador armónico de frecuencia $\omega_0$.

El Hamiltoniano del péndulo es  
$$
H = \frac{p^2}{2M} - U_0 \cos\theta, \quad \text{con } M = m\ell^2 \text{ y } U_0 = M\omega_0^2.
$$  
Para simplificar, escogiendo unidades apropiadas es siempre posible fijar $M=1$, el cual es el caso que se considera en adelante.

(c) **[2p]** La separatriz está formada por las trayectorias que separan el movimiento oscilatorio del movimiento rotacional del péndulo. Demuestre que la energía en la separatriz es $U_0$ y su ecuación en el espacio de fase está dada por  
$$
p = \pm 2\omega_0 \cos\frac{\theta}{2}.
$$

(d) **[2p]** Demuestre que para las trayectorias sobre la separatriz se tiene  
$$
\theta(t) = 4\arctan e^{\omega_0 t} - \pi.
$$

---

### Problema 5 — Péndulo: parte numérica  

Usando Mathematica reproduzca el espacio de fase del péndulo. Para ello tendrá que integrar las ecuaciones de Hamilton para obtener numéricamente $\theta(t)$ y $p(t)$ (por ejemplo usando la función `NDSolve`) para varias condiciones iniciales (puede tomar, por ejemplo, condiciones iniciales de la forma $\theta(0)=0$ variando convenientemente $p(0)$). Una forma de obtener las gráficas de las trayectorias $(\theta(t), p(t))$ en el espacio de fase es con la ayuda de la función `ParametricPlot`.

---

### Problema 6 — Ecuación de Hamilton-Jacobi para el oscilador armónico  

Considere el Hamiltoniano del oscilador armónico $H = (p^2 + q^2)/2$. La ecuación de Hamilton-Jacobi para este sistema es  
$$
\frac{1}{2} \left( \frac{\partial F_2}{\partial q} \right)^2 + \frac{1}{2} q^2 = P.
$$  
A partir de la función $F_2(q, P)$ encuentre las expresiones analíticas de $q$ y $p$ en función de las constantes de movimiento $P$ y $Q$.

Aquí tienes la extracción de los enunciados y expresiones matemáticas de los talleres 3 y 4.

---

## Taller 3

### Problema 7 — Variables de acción‑ángulo para el átomo de hidrógeno unidimensional

Considere el Hamiltoniano del átomo de hidrógeno unidimensional  

$$
H = \frac{p^2}{2m} - \frac{e^2}{z}, \quad \text{con } z > 0.
$$

(a) Muestre que el Hamiltoniano de este sistema en variables de acción‑ángulo $(I,\theta)$ toma la forma  
$$
K(I) = -\frac{m e^2}{2 I^2}.
$$

(b) Muestre que la ecuación de la trayectoria del electrón para una energía dada $E<0$ está definida de manera implícita por  

$$
t = \frac{e^2}{|E|} \sqrt{\frac{m}{2|E|}} \bigl(2\eta - \operatorname{sen} 2\eta\bigr) \Big|_{\eta_0}^{\eta},
$$  

donde $\eta$ y $\eta_0$ están determinados para $z_0 = z(0)$ y $z = z(t)$ respectivamente mediante la relación  

$$
z = \frac{2I^2}{m e^2} \operatorname{sen}^2\eta. \qquad (3)
$$

(c) Concluya que $\theta = 2\eta - \operatorname{sen}2\eta$ y por lo tanto la transformación a variables de acción‑ángulo está dada por (3) y  
$$
p = \frac{m e^2}{I} \cot\eta.
$$

---

### Problema 8 — Movimiento separable: Hamiltoniano de Stark

Encuentre la solución de la ecuación de Hamilton‑Jacobi para una partícula de masa $m$ en un potencial de Coulomb y en un potencial electrostático en la dirección $z$, cuyo Hamiltoniano es  

$$
H(\mathbf{r}, \mathbf{p}) = \frac{p^2}{2m} + \frac{\lambda}{r} - Fz, \quad \text{con } r = |\mathbf{r}|.
$$

Se puede resolver este problema siguiendo los siguientes pasos:

(a) Use las coordenadas parabólicas $(\xi, \eta, \phi)$ obtenidas a partir de las coordenadas cilíndricas $(\rho, \phi, z)$ mediante las transformaciones:  
$\xi = r + z$ y $\eta = r - z$ con $r = \sqrt{\rho^2 + z^2}$ y $\rho = \sqrt{\eta\xi} = \sqrt{x^2 + y^2}$.  
Muestre que  

$$
p_\phi = m\xi\eta\,\dot\phi, \qquad
p_\eta = \frac{m}{4\eta}(\eta+\xi)\,\dot\eta, \qquad
p_\xi = \frac{m}{4\xi}(\eta+\xi)\,\dot\xi.
$$

(b) Muestre que  

$$
H(\xi,\eta,\phi,p_\xi,p_\eta,p_\phi) = \frac{2}{m(\xi+\eta)}\left( \xi p_\xi^2 + \eta p_\eta^2 + \frac{p_\phi^2}{2m\eta\xi} + \frac{2\lambda}{\eta+\xi} - \frac{F}{2}(\xi-\eta) \right).
$$

(c) Escriba la ecuación de Hamilton‑Jacobi y muestre que es una ecuación diferencial separable en coordenadas parabólicas.

---

## Taller 4

### Problema 9 — Mapeo estándar

La dinámica del rotor golpeado está gobernada por el Hamiltoniano  

$$
H(I,\theta,t) = \frac{I^2}{2} - K \cos\theta \sum_{n=-\infty}^{\infty} \delta(t-n),
$$  

donde $I$ y $\theta$ son variables de acción‑ángulo y $K$ es una constante positiva.

(a) Sean $I_n$ y $\theta_n$ la acción y el ángulo justo antes del $n$-ésimo golpe. El mapeo estroboscópico de este sistema se conoce como *mapeo estándar*. Demuestre que se satisfacen las recursiones  

$$
\begin{aligned}
I_{n+1} &= I_n - K \sin\theta_n \pmod{2\pi},\\
\theta_{n+1} &= \theta_n + I_{n+1} \pmod{2\pi}.
\end{aligned}
$$

(b) Con ayuda de Mathematica grafique el mapeo estándar para $K = 0.1,\;0.5,\;0.8,\;2.5,\;4.0$. Para cada uno de ellos tome alrededor de 100 condiciones iniciales con $\theta_0 = 0$ e $I_0 \in (-\pi,\pi)$. (Los valores de $\theta$ e $I$ se deben tomar en el intervalo $(-\pi,\pi)$).

(c) Considere la isla resonante alrededor de $(I,\theta)=(0,0)$ que corresponde a la resonancia $1:1$ del rotor golpeado. Encuentre el ancho de esta resonancia y muestre que esta resonancia se sobrelapa consigo misma para valores de $K$ mayores que $K_c \approx \pi^2/4 \approx 2.47$. (Use teoría secular de perturbaciones a primer orden).

---

### Problema 10 — Teoría secular de perturbaciones para dos osciladores armónicos acoplados

El Hamiltoniano de dos osciladores armónicos acoplados es  

$$
H = \frac{1}{2}\sum_{j=1}^{2}\bigl(p_j^2 + \omega_j^2 q_j^2\bigr) + \varepsilon\left(q_1^2 q_2 - \frac{1}{3}q_2^3\right).
$$  

Considera la resonancia del sistema $\omega_2 : \omega_1 = 2 : 1$.

(a) Usando teoría secular de perturbaciones, el Hamiltoniano $H$ se expresa inicialmente en las variables de acción‑ángulo $(I_j,\theta_j)$, $j=1,2$, de los dos osciladores armónicos no perturbados (ver Problema 6 del Taller 2) para luego ser llevado a las variables $(J,\varphi)$ mediante la función generatriz  

$$
F_2(\theta_1,\theta_2,J_1,J_2) = (2\theta_1 - \theta_2)J_1 + \theta_2 J_2.
$$  

Muestre que el Hamiltoniano que resulta al promediar sobre la variable rápida $\varphi_2$ es  

$$
\overline{H} = \omega_2 J_2 + \frac{2J_1}{\omega_2}\sqrt{\frac{2(J_2 - J_1)}{\omega_2}}\,\sin\varphi_1.
$$

(b) Muestre que la dinámica en las vecindades de los puntos fijos estables de $\overline{H}$ se describe por un oscilador armónico.


---

## Taller 5
---

### Problema 11 — Resonancias en el cinturón de asteroides entre Marte y Júpiter  

Propongamos un modelo para describir la dinámica de un asteroide de masa $\mu$ en el cinturón de asteroides entre Marte y Júpiter con las siguientes suposiciones:  
(i) las fuerzas que dominan son las fuerzas gravitacionales del Sol (de masa $M$) y de Júpiter (de masa $m$) y se desprecian todas las demás interacciones.  
(ii) Júpiter se desplaza a lo largo de una órbita circular con frecuencia angular $\Omega$ alrededor del centro de masa $C$ entre el Sol y Júpiter.  
(iii) La dinámica del asteroide, Júpiter y el Sol transcurre en un plano.  
Bajo estas suposiciones el Hamiltoniano para el asteroide es  

$$
H = \frac{p^2}{2\mu} - \frac{GM\mu}{r} - \frac{Gm\mu}{|q - r_m(t)|}, \qquad (4)
$$  

donde $r$ es la distancia del asteroide al Sol, $q$ es la posición del asteroide relativa al centro de masa $C$ y $r_m(t)$ es la posición de Júpiter relativa a $C$.

(a) En este caso es posible eliminar la dependencia explícita de $H$ con el tiempo al pasar al sistema de referencia con origen en $C$ y que rota con frecuencia $\Omega$. Aquí se pide demostrar un resultado más general: considere una partícula de masa $\mu$ en un potencial de energía $U$ con velocidad $\mathbf{v}$ con respecto a un sistema de coordenadas que rota con velocidad angular constante $\Omega$ con respecto a un sistema inercial. Su Lagrangiano es  

$$
L = \frac{1}{2}\mu v^2 + \mu \mathbf{v} \cdot (\mathbf{\Omega} \times \mathbf{r}) + \frac{1}{2}(\mathbf{\Omega} \times \mathbf{r})^2 - U.
$$  

A partir de aquí muestre que el Hamiltoniano es  

$$
H = \frac{p^2}{2\mu} - \mathbf{p} \cdot (\mathbf{\Omega} \times \mathbf{r}) + U.
$$  

Por lo tanto el Hamiltoniano (4) en el sistema co-rotante toma la forma  

$$
H = \frac{1}{2\mu} \left( p_r^2 + \frac{p_\varphi^2}{r^2} \right) - \Omega p_\varphi - \frac{GM\mu}{r} - \frac{Gm\mu}{|q - r_m|}, \qquad (5)
$$  

donde $p_r$ y $p_\varphi$ son los momentos canónicos de las coordenadas polares $r$ y $\varphi$, respectivamente. Observe que en (5) hemos supuesto que $r \approx q$ y que $r_m$ ya no depende de $t$.

(b) Como $M \gg m \gg \mu$, el término $H_1 = - \frac{G m \mu}{|q - r_m|}$ de (5) es una perturbación al Hamiltoniano (integrable)  

$$
H_0 = \frac{1}{2\mu} \left( p_r^2 + \frac{p_\varphi^2}{r^2} \right) - \Omega p_\varphi - \frac{GM\mu}{r}.
$$  

Encuentre explícitamente las coordenadas de acción $I_r, I_\varphi$, y demuestre que  

$$
H_0(I_r, I_\varphi) = -\Omega I_\varphi - \frac{G^2 M^2 \mu^3}{2(I_r + I_\varphi)^2}.
$$  

Verifique que  

$$
\omega_{\mu} = \frac{G^2 M^2 \mu^3}{(I_r + I_\varphi)^3}
$$  

es la frecuencia de rotación del asteroide (no perturbado) con respecto al sistema de coordenadas inercial (no-rotante). A partir del teorema KAM establezca un criterio en términos de las frecuencias $\Omega$ y $\omega_\mu$ que determine cuando el movimiento del asteroide afectado por la perturbación $H_1$ es estocástico.

---
# TALLER 6

A continuación se presentan los enunciados y expresiones matemáticas extraídos del archivo `taller06.pdf`, correspondientes a los problemas 12 y 13. Se han omitido los caracteres no imprimibles al inicio del archivo.

---

## Problema 12 — Átomo de hidrógeno en variables de acción ángulo

El hamiltoniano para el átomo de hidrógeno en coordenadas esféricas es  

\[
H = \frac{p^2}{2m} - \frac{e^2}{r} = \frac{1}{2m} \left( p_r^2 + \frac{p_\theta^2}{r^2} + \frac{p_\phi^2}{r^2 \sin^2 \theta} \right) - \frac{e^2}{r}
\]

(a) Muestre que  

\[
p_r = m\dot{r}, \qquad p_\theta = m r^2 \dot{\theta}, \qquad p_\phi = m r^2 \sin\theta \, \dot{\phi} = L_z.
\]

(b) Encuentre que existen tres constantes de movimiento y por lo tanto el sistema es integrable.

(c) Demuestre que  

\[
\begin{aligned}
I_r &= \frac{1}{2\pi} \oint p_r \, dr = \frac{m e^2}{\sqrt{-2mE}} - L, \\[4pt]
I_\theta &= \frac{1}{2\pi} \oint p_\theta \, d\theta = L - L_z, \\[4pt]
I_\phi &= \frac{1}{2\pi} \oint p_\phi \, d\phi = L_z.
\end{aligned}
\]

**Ayuda:**  
\[
L^2 = p_\theta^2 + \frac{p_\phi^2}{\sin^2\theta} = p_\theta^2 + \frac{L_z^2}{\sin^2\theta}, \qquad (L \ge 0,\; -L \le L_z \le L).
\]  
Identifique los puntos de retorno para el movimiento correspondiente a las acciones \(I_r, I_\theta, I_\phi\). Las integrales se pueden escribir como integrales en el plano complejo y se pueden usar herramientas del cálculo de integrales de contorno.

(d) Muestre que la energía se puede escribir como  

\[
E = -\frac{m e^4}{2} \, \frac{1}{(I_r + I_\theta + I_\phi)^2}.
\]

---

## Problema 13 — WKB para el potencial gravitacional

La solución exacta de la ecuación de Schrödinger para una partícula de masa \(\mu\) en el potencial \(V(x) = -\mu g x\) con energía \(E\) es  

\[
\psi(x) = N \, \text{Ai}\!\left[ -\left(\frac{2\mu^2 g}{\hbar^2}\right)^{1/3} \left( x + \frac{E}{\mu g} \right) \right],
\]  

donde \(\text{Ai}(z)\) es una función de Airy. Compare \(\psi(x)\) con la solución WKB  

\[
\psi_{\text{WKB}}(x) = 
\begin{cases}
\displaystyle \frac{1}{\sqrt{|p(x)|}} \, e^{-\frac{1}{\hbar} \int_{a}^{x} |p(x')| \, dx'}, & x \to -\infty, \\[6pt]
\displaystyle \frac{2}{\sqrt{|p(x)|}} \, \cos\!\left( \frac{1}{\hbar} \int_{a}^{x} p(x') \, dx' - \frac{\phi}{2} \right), & x \to +\infty.
\end{cases}
\]  

¿Cuál debería ser el valor de la fase \(\phi\)?

**Ayuda:** Consulte la forma asintótica de las funciones de Airy (por ejemplo en el manual de Abramowitz y Stegun).

---

---
# TALLER 7
### Problema 14 — Propagador del oscilador armónico  

El propagador de una partícula en un potencial armónico está dado por la integral de camino  

$$
K(x, T|x_0, 0) = \int_{x_0}^{x} \mathcal{D}x \, e^{\frac{i}{\hbar} S[x(t)]},
$$  

donde la acción de la partícula es  

$$
S[x(t)] = \int_{0}^{T} \left( \frac{1}{2} m\dot{x}^2 - \frac{1}{2} m\omega^2 x^2 \right) dt.
$$

(a) Demuestre que el propagador se puede escribir como  

$$
K(x, T|x_0, 0) = e^{\frac{i}{\hbar} S_{cl}(x_0, x, t)} K(0, T|0, 0),
$$  

donde $S_{cl}(x_0, x, t)$ es la acción de la trayectoria clásica entre $x_0$ en $t=0$ y $x$ en $t=T$, la cual obedece la ecuación de movimiento.  
**Ayuda:** Descomponga $x(t) = x_{cl}(t) + y(t)$, donde $x_{cl}(t)$ es la trayectoria clásica.

(b) Muestre que la acción clásica definida arriba satisface  

$$
S_{cl}(x_0, x, t) = \frac{m\omega}{2 \sin \omega T} \left( (x^2 + x_0^2) \cos \omega T - 2x x_0 \right).
$$  

Argumente por qué esto significa que  

$$
K(x, T|x_0, 0) = F(T) \exp \left[ \frac{i m \omega}{2 \hbar \sin \omega T} \left( (x^2 + x_0^2) \cos \omega T - 2x x_0 \right) \right].
$$

(c) Para calcular $F(T)$ considere la integral de camino  

$$
K(0, T|0, 0) = \int_{0}^{0} \mathcal{D}y \, \exp \left[ \frac{i}{\hbar} \int_{0}^{T} \left( \frac{1}{2} m \dot{y}^2 - \frac{1}{2} m \omega^2 y^2 \right) dt \right].
$$  

Escriba $y(t)$ como una serie de Fourier $y(t) = \sum_{n=1}^{\infty} a_n \sin \frac{n\pi t}{T}$. Reemplace la integral sobre $y(t)$ con una integral sobre los coeficientes de Fourier para mostrar que  

$$
K(0, T|0, 0) = C \left( \frac{\omega T}{\sin \omega T} \right)^{1/2},
$$  

con $C$ un factor que no depende de $\omega$. Usando que en el límite $\omega \to 0$ se obtiene el resultado para una partícula libre:  

$$
K_{\text{libre}}(x, t|x_0, 0) = \left( \frac{m}{2\pi i \hbar t} \right)^{1/2} \exp \left( \frac{i m (x - x_0)^2}{2 \hbar t} \right),
$$  

muestre que el propagador de una partícula en un potencial armónico es  

$$
K(x, t|x_0, 0) = \left( \frac{m \omega}{2 \pi i \hbar \sin(\omega T)} \right)^{1/2} \exp \left( \frac{i m \omega}{2 \hbar \sin(\omega T)} \left( (x + x_0)^2 \cos(\omega T) - 2x x_0 \right) \right).
$$  

**Ayuda:** $\sin(\pi z) = \pi z \prod_{n=1}^{\infty} \left(1 - \frac{z^2}{n^2}\right)$.

---
# TALLER 8
## Problema 15: -- Función de Husimi y estados coherentes**

**(a) Demostración de que $\Phi_{q,p}(x)$ es un estado coherente**

**Objetivo:** Mostrar que la función de onda $\Phi_{q,p}(x)$ es función propia del operador de aniquilación $\hat{a}$, es decir, $\hat{a}\Phi_{q,p}(x) = \alpha\Phi_{q,p}(x)$, y encontrar el valor propio complejo $\alpha$.

La función de onda dada es:

$$\Phi_{q,p}(x) = N \exp\left[ -\frac{(x-q)^2}{2\sigma_\omega^2} + \frac{i}{\hbar}px \right]$$

donde $N = (\pi^{-1/2} \sigma_\omega^{-1})^{1/2}$ y $\sigma_\omega = \sqrt{\frac{\hbar}{m\omega}}$.

El operador de aniquilación en la representación de posición (donde $\hat{x} \to x$ y $\hat{p} \to -i\hbar\frac{d}{dx}$) se escribe como:

$$\hat{a} = \frac{1}{\sqrt{2}} \left( \frac{x}{\sigma_\omega} + \sigma_\omega \frac{d}{dx} \right)$$

Aplicamos $\hat{a}$ sobre $\Phi_{q,p}(x)$. Primero, necesitamos la derivada de la función de onda:

$$\frac{d}{dx}\Phi_{q,p}(x) = \Phi_{q,p}(x) \frac{d}{dx} \left[ -\frac{(x-q)^2}{2\sigma_\omega^2} + \frac{i}{\hbar}px \right]$$

$$\frac{d}{dx}\Phi_{q,p}(x) = \Phi_{q,p}(x) \left[ -\frac{2(x-q)}{2\sigma_\omega^2} + \frac{i}{\hbar}p \right] = \Phi_{q,p}(x) \left[ -\frac{x-q}{\sigma_\omega^2} + \frac{i}{\hbar}p \right]$$

Ahora evaluamos $\hat{a}\Phi_{q,p}(x)$:

$$\hat{a}\Phi_{q,p}(x) = \frac{1}{\sqrt{2}} \left( \frac{x}{\sigma_\omega}\Phi_{q,p}(x) + \sigma_\omega \frac{d\Phi_{q,p}(x)}{dx} \right)$$

$$\hat{a}\Phi_{q,p}(x) = \frac{1}{\sqrt{2}} \left\{ \frac{x}{\sigma_\omega} + \sigma_\omega \left[ -\frac{x-q}{\sigma_\omega^2} + \frac{i}{\hbar}p \right] \right\} \Phi_{q,p}(x)$$

$$\hat{a}\Phi_{q,p}(x) = \frac{1}{\sqrt{2}} \left\{ \frac{x}{\sigma_\omega} - \frac{x-q}{\sigma_\omega} + \frac{i}{\hbar}\sigma_\omega p \right\} \Phi_{q,p}(x)$$

Las $x/\sigma_\omega$ se cancelan:

$$\hat{a}\Phi_{q,p}(x) = \frac{1}{\sqrt{2}} \left( \frac{q}{\sigma_\omega} + \frac{i}{\hbar}\sigma_\omega p \right) \Phi_{q,p}(x)$$

**Conclusión:**

Puesto que el término entre paréntesis es una constante (no depende de $x$), $\Phi_{q,p}(x)$ es efectivamente una función propia del operador de aniquilación $\hat{a}$.

El **valor propio complejo** $\alpha$ asociado es:

$$\alpha = \frac{1}{\sqrt{2}} \left( \frac{q}{\sigma_\omega} + i\frac{\sigma_\omega}{\hbar} p \right)$$

---

**(b) Equivalencia entre $Q_\rho(q,p)$ y la distribución de Husimi $H_\rho(q,p)$**

**Objetivo:** Demostrar que la proyección $Q_\rho(q,p) = \frac{1}{\pi} \langle \Phi_{q,p} | \hat{\rho} | \Phi_{q,p} \rangle$ coincide con la distribución de Husimi general $H_\rho(q,p)$ cuando se usa una función de suavizado Gaussiana específica.

La distribución de Husimi se define clásicamente como una versión suavizada (convolución) de la función de Wigner $W_\rho(q', p')$ con una función de suavizado (Gaussiana) $f$:

$$H_\rho(q,p) = \iint W_\rho(q', p') f(q,p; q',p') \, dq' dp'$$

La función de Wigner para un estado $|\psi\rangle$ puro (donde $\hat{\rho} = |\psi\rangle\langle\psi|$) es:

$$W_\rho(q', p') = \frac{1}{\pi\hbar} \int \psi^*(q' + y) \psi(q' - y) e^{2ipy/\hbar} \, dy$$

(Nota: Se usan varias convenciones de normalización para Wigner, asumo la convención estándar donde la integral sobre el espacio fase da 1).

Nos dan la función de suavizado:

$$f(q,p; q', p') = \frac{1}{\pi\hbar} \exp\left\{ - \left[ \frac{(q-q')^2}{\sigma_\omega^2} + \frac{\sigma_\omega^2(p-p')^2}{\hbar^2} \right] \right\}$$

Por otro lado, evaluemos la definición de $Q_\rho(q,p)$ en el espacio de posiciones:

$$Q_\rho(q,p) = \frac{1}{\pi} \langle \Phi_{q,p} | \psi \rangle \langle \psi | \Phi_{q,p} \rangle = \frac{1}{\pi} \left| \int_{-\infty}^{\infty} \Phi_{q,p}^*(x) \psi(x) \, dx \right|^2$$

Para conectar esto con la función de Wigner, usamos la propiedad fundamental de que el traslape al cuadrado de dos estados puros (el estado arbitrario $|\psi\rangle$ y el estado coherente $|\Phi_{q,p}\rangle$) es igual a la integral del producto de sus respectivas funciones de Wigner en el espacio de fase (esto es un teorema clave, la traza del producto de dos matrices densidad es la integral del producto de sus funciones de Wigner):

$$|\langle \Phi_{q,p} | \psi \rangle|^2 = 2\pi\hbar \iint W_{\Phi_{q,p}}(q', p') W_\rho(q', p') \, dq' dp'$$

Por lo tanto:

$$Q_\rho(q,p) = 2\hbar \iint W_{\Phi_{q,p}}(q', p') W_\rho(q', p') \, dq' dp'$$

Para que esto coincida con la definición de Husimi, necesitamos que la función de Wigner del estado coherente (multiplicada por $2\hbar\pi$) sea exactamente la función de suavizado $f$. Calculemos la función de Wigner del estado coherente $\Phi_{q,p}(x)$:

$$W_{\Phi}(q', p') = \frac{1}{\pi\hbar} \int \Phi_{q,p}^*(q' + y) \Phi_{q,p}(q' - y) e^{2ip'y/\hbar} \, dy$$

Sustituyendo la expresión de $\Phi_{q,p}(x)$:

$$\Phi_{q,p}^*(q'+y) \Phi_{q,p}(q'-y) = N^2 \exp\left[ -\frac{(q'+y-q)^2 + (q'-y-q)^2}{2\sigma_\omega^2} - \frac{i}{\hbar}p(q'+y) + \frac{i}{\hbar}p(q'-y) \right]$$

El exponente del término real se simplifica: $(a+y)^2 + (a-y)^2 = 2a^2 + 2y^2$, donde $a = q'-q$.

$$-\frac{2(q'-q)^2 + 2y^2}{2\sigma_\omega^2} = -\frac{(q'-q)^2}{\sigma_\omega^2} - \frac{y^2}{\sigma_\omega^2}$$

El exponente del término imaginario es: $-\frac{i}{\hbar}p(2y)$.

Entonces:

$$W_{\Phi}(q', p') = \frac{N^2}{\pi\hbar} \exp\left[ -\frac{(q-q')^2}{\sigma_\omega^2} \right] \int \exp\left[ -\frac{y^2}{\sigma_\omega^2} - \frac{2iy}{\hbar}(p-p') \right] \, dy$$

La integral es de la forma Gaussiana estándar $\int e^{-ay^2 + by} dy = \sqrt{\frac{\pi}{a}} e^{b^2 / 4a}$. Aquí $a = 1/\sigma_\omega^2$ y $b = -2i(p-p')/\hbar$.

$$\int \dots = \sqrt{\pi \sigma_\omega^2} \exp\left[ \frac{(-2i(p-p')/\hbar)^2}{4/\sigma_\omega^2} \right] = \sigma_\omega \sqrt{\pi} \exp\left[ - \frac{\sigma_\omega^2(p-p')^2}{\hbar^2} \right]$$

Multiplicando por las constantes externas, recordando que $N^2 = 1/(\sqrt{\pi}\sigma_\omega)$:

$$W_{\Phi}(q', p') = \frac{1}{\pi\hbar \sqrt{\pi}\sigma_\omega} \cdot \sigma_\omega \sqrt{\pi} \cdot \exp\left[ -\frac{(q-q')^2}{\sigma_\omega^2} - \frac{\sigma_\omega^2(p-p')^2}{\hbar^2} \right]$$

$$W_{\Phi}(q', p') = \frac{1}{\pi\hbar} \exp\left\{ - \left[ \frac{(q-q')^2}{\sigma_\omega^2} + \frac{\sigma_\omega^2(p-p')^2}{\hbar^2} \right] \right\}$$

¡Esta es exactamente la función de suavizado $f(q,p; q', p')$ dada en el enunciado!

Por lo tanto, al multiplicar la ecuación de solapamiento por el factor adecuado, comprobamos que $Q_\rho(q,p)$ es la convolución de la función de Wigner del estado con una Gaussiana del estado coherente, lo cual es la **definición exacta** de la función de Husimi.

---

**(c) Gráficas en Mathematica de las funciones de Husimi para los estados de Fock**

**Objetivo:** Escribir un código de Mathematica para graficar $Q_n(q,p) = \frac{1}{\pi}|\langle \Phi_{q,p} | \psi_n \rangle|^2$ para los estados propios del oscilador armónico $n=0, 1, 2$, analizando la dependencia con el parámetro de compresión $\omega$.

Primero, necesitamos la integral analítica del producto interno $\langle \Phi_{q,p} | \psi_n \rangle$.

Para $m=1, \hbar=1$ (unidades naturales implícitas), $\omega_0=1$ determina los autoestados, por lo que su ancho es $\sigma_0 = 1$. Sin embargo, el estado coherente proyector depende de un parámetro libre $\omega$ que define su propio ancho $\sigma_\omega = 1/\sqrt{\omega}$.

El producto interno es:

$$I_n(q, p; \omega) = \int_{-\infty}^{\infty} \Phi_{q,p}^*(x; \omega) \psi_n(x; \omega_0=1) \, dx$$

El código en Mathematica a continuación define estas funciones y traza los contornos de densidad de probabilidad en el espacio fase $(q,p)$ para diferentes valores de $\omega$. Puedes copiar y pegar esto directamente en un Notebook.

Mathematica

```
(* Definimos las constantes y anchos *)
ClearAll["Global`*"];
m = 1; hbar = 1; w0 = 1;
sigma0 = Sqrt[hbar/(m w0)];
sigmaW[w_] := Sqrt[hbar/(m w)];

(* Estado propio del oscilador armonico \psi_n(x) con frecuencia w0 *)
PsiN[n_, x_] := (1/Sqrt[2^n n! Sqrt[Pi] sigma0]) * Exp[-1/2 (x/sigma0)^2] * HermiteH[n, x/sigma0]

(* Estado coherente \Phi_{q,p}(x) con frecuencia libre w *)
PhiQP[q_, p_, x_, w_] := (1/(Sqrt[Pi] sigmaW[w])^(1/2)) * Exp[-(x - q)^2/(2 sigmaW[w]^2) - I p x / hbar]

(* Producto interno numerico o simbolico <\Phi | \Psi_n> *)
(* Usamos NIntegrate dentro de la definicion para evitar expansiones lentas *)
Overlap[n_, q_?NumericQ, p_?NumericQ, w_?NumericQ] := 
 NIntegrate[
  Conjugate[PhiQP[q, p, x, w]] * PsiN[n, x], 
  {x, -Infinity, Infinity}, 
  Method -> "GlobalAdaptive", 
  MaxRecursion -> 20
 ]

(* Funcion de Husimi Q_n *)
HusimiQ[n_, q_, p_, w_] := (1/Pi) * Abs[Overlap[n, q, p, w]]^2

(* Configuración para graficar *)
plotRange = 4;
wValues = {0.5, 1.0, 2.0}; (* Variamos w alrededor de w0=1 *)
nValues = {0, 1, 2};

(* Bucle para generar una matriz de graficos (filas: n, columnas: w) *)
Grid[
 Table[
  ContourPlot[
   HusimiQ[n, q, p, w],
   {q, -plotRange, plotRange}, {p, -plotRange, plotRange},
   PlotRange -> All,
   ColorFunction -> "SunsetColors",
   PlotLegends -> Automatic,
   Contours -> 15,
   FrameLabel -> {"q", "p"},
   PlotLabel -> Row[{"n = ", n, ", \[Omega] = ", w}],
   ImageSize -> 300
  ],
  {n, nValues}, {w, wValues}
 ]
]
```

**Análisis físico de los resultados:**

1. **Cuando $\omega = \omega_0 = 1$:** La función de Husimi suaviza simétricamente la distribución. Para el estado base ($n=0$), obtienes un círculo perfecto centrado en el origen. Para $n=1, 2$, obtienes anillos concéntricos perfectos. Esto coincide exactamente con las trayectorias del espacio fase clásico del oscilador armónico (que son círculos u elipses de energía constante $E = p^2/2m + m\omega_0^2 q^2/2$).
    
2. **Cuando $\omega \neq \omega_0$ (ej. $\omega = 0.5$ o $\omega = 2.0$):** El estado coherente proyector (el "molde" Gaussiano que usamos para barrer el espacio fase) ya no empata con la simetría natural del potencial del estado. El resultado son anillos **estirados o comprimidos** (elipses o formas "squeezed"). Estás midiendo un estado puro simétrico con un estado proyector asimétrico, rompiendo la correspondencia directa con la trayectoria circular clásica en el espacio $(q,p)$ isotrópico.


---
# TALLER 9
### Problema 16 — Separación de niveles en el billar rectangular  

Considere el billar rectangular cuántico  

$$
V(x, y) = 
\begin{cases} 
0, & x \in (0,a) \text{ y } y \in (0,b), \\
\infty, & \text{en otro caso}.
\end{cases}
$$  

Encuentre el espectro de energías y grafique (por ejemplo en Mathematica) el histograma para la distribución de vecinos cercanos (NND). Como el sistema es integrable debería observar una distribución tipo Poisson. Considere dos casos: razón $a/b$ racional e irracional. Discuta las diferencias, si las hay.

---

### Problema 17 — Probabilidad conjunta de autovectores  

Considere un GOE de matrices $N \times N$ con entradas gaussianas. La probabilidad conjunta de que un autovector tenga componentes $x_1, x_2, \dots, x_N$ es  

$$
\rho(x_1, \dots, x_N) = c \, \delta\!\left(1 - \sum_{j=1}^N x_j^2\right),
$$  

donde $c$ es constante. ¿Cuál es el valor de $c$?  

**Observación:** Esta densidad de probabilidad expresa el hecho de que la única magnitud invariante del autovector es la norma.
