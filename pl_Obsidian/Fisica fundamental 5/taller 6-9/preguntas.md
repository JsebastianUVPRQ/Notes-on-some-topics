A continuación se presentan los ejercicios extraídos de los talleres 6, 7, 8 y 9, organizados por taller y problema. Las ecuaciones y fórmulas están expresadas en formato LaTeX.

---

### **Taller 6**

**Problema 27 — Medición de observables compatibles**  
Un sistema físico se encuentra en un estado normalizado cualquiera $|\psi\rangle$. Sean $\hat{A}$ y $\hat{B}$ dos observables compatibles. Suponga que se mide $\hat{A}$ se obtiene como resultado $a_n$ e inmediatamente después se mide $\hat{B}$ se obtiene $b_m$ de forma que el estado final en este proceso es $|\psi_{nm}\rangle$. Sea $\mathcal{P}(a_n, b_m)$ la probabilidad de obtener $a_n$ en la primera medición y $b_m$ en la segunda. De manera análoga se definen $\mathcal{P}(b_m, a_n)$ y $|\psi_{mn}\rangle$. Demuestre que  
$$
\mathcal{P}(a_n, b_m) = \mathcal{P}(b_m, a_n) \quad \text{y} \quad |\psi_{nm}\rangle = |\psi_{mn}\rangle,
$$  
es decir, la medición de $\hat{B}$ no causa ninguna pérdida de información obtenida previamente de la medición de $\hat{A}$.

---

**Problema 28 — Problema de valores propios y CCOC**  
El espacio de estados de cierto sistema físico es tridimensional y está generado por la base ortonormal $\{|\varphi_1\rangle, |\varphi_2\rangle, |\varphi_3\rangle\}$. Considere los operadores  
$$
\hat{H}_0 = \hbar\omega_0(|\varphi_1\rangle \langle \varphi_1| - |\varphi_2\rangle \langle \varphi_2| - |\varphi_3\rangle \langle \varphi_3|) \quad \text{y} \quad \hat{A} = a(|\varphi_1\rangle \langle \varphi_1| + |\varphi_2\rangle \langle \varphi_3| + |\varphi_3\rangle \langle \varphi_2|)
$$  
con $a, \omega_0 \in \mathbb{R}$.  
(a) ¿Son $\hat{H}_0$ y $\hat{A}$ hermíticos?  
(b) Encuentre la representación matricial de $\hat{H}_0$ y $\hat{A}$ en la base $\{|\varphi_1\rangle, |\varphi_2\rangle, |\varphi_3\rangle\}$.  
(c) Encuentre los valores y vectores propios de $\hat{H} = \hat{H}_0 + \hat{A}$.  
(d) Muestre que $\hat{H}_0$ y $\hat{A}$ conmutan. Encuentre una base de autovectores comunes a $\hat{H}_0$ y $\hat{A}$.  
(e) ¿Cuál(es) de los siguientes conjuntos forman un CCOC: $\{\hat{H}_0\}, \{\hat{A}\}, \{\hat{H}_0, \hat{A}\}, \{\hat{H}_0^2, \hat{A}\}$?

---

**Problema 29 — Operador paridad**  
El operador de paridad $\hat{\Pi}$ de un sistema unidimensional se define por la propiedad  
$$
\hat{\Pi}\psi(x) = \psi(-x).
$$  
(a) Muestre que $\hat{\Pi}$ es hermítico y encuentre sus posibles valores propios.  
(b) Suponga que $\hat{\Pi}$ conmuta con el hamiltoniano no-degenerado $\hat{H}$. ¿Cuáles son las propiedades de las funciones propias de $\hat{H}$ que pertenecen a los subespacios propios de $\hat{\Pi}$?

---

**Problema 30 — Pozo de potencial par**  
(a) Considere una partícula en un pozo de potencial unidimensional $V(x)$ par, es decir, $V(x) = V(-x)$. Demuestre que si $\psi(x)$ es un estado propio acotado, entonces $\psi(x)$ es par o impar.  
(b) Una partícula de masa $m$ se mueve en el pozo de potencial unidimensional  
$$
V(x) = 
\begin{cases} 
V_0 = -\dfrac{\hbar^2 k_0^2}{2m}, & \text{para } |x| < L/2, \\ 
0, & \text{para } |x| > L/2.
\end{cases}
$$  
Muestre que existe al menos un estado acotado (o discreto).  
(c) Para el caso $V_0 \gg \dfrac{\hbar^2}{mL^2}$ encuentre una estimación ($\pm 1$) del número de estados acotados.

---

### **Taller 7**

**Problema 32 — Teorema de Ehrenfest**  
Demuestre el teorema de Ehrenfest.

---

**Problema 33 — Operadores de creación y destrucción**  
Una partícula de masa $m$ en un potencial armónico unidimensional $V = \dfrac{1}{2} m \eta^2 x^2$ de frecuencia $\eta$. Se definen:  
$$
\hat{a} = \frac{1}{\sqrt{2}} \left( \sqrt{\dfrac{m\eta}{\hbar}} \hat{x} + \dfrac{i}{\sqrt{m\hbar\eta}} \hat{p} \right), \quad \hat{a}^\dagger = \frac{1}{\sqrt{2}} \left( \sqrt{\dfrac{m\eta}{\hbar}} \hat{x} - \dfrac{i}{\sqrt{m\hbar\eta}} \hat{p} \right).
$$  
(a) Demuestre:  
(i) $[\hat{a}, \hat{a}^\dagger] = 1$.  
(ii) $[\hat{N}, \hat{a}] = -\hat{a}$ y $[\hat{N}, \hat{a}^\dagger] = \hat{a}^\dagger$, con $\hat{N} = \hat{a}^\dagger \hat{a}$ (operador número).  
(iii) $\dfrac{\hat{p}^2}{2m} + \dfrac{1}{2} m \eta^2 \hat{x}^2 = \hbar \eta \left( \hat{N} + \dfrac{1}{2} \right)$.  
(b) Encuentre la representación en coordenadas del estado normalizado $|\varphi_0\rangle$ tal que $\hat{a} |\varphi_0\rangle = 0$.

---

**Problema 34 — Valores esperados en oscilador armónico**  
(a) Calcule $\langle \hat{x} \rangle$, $\langle \hat{p} \rangle$, $\langle \hat{K} \rangle$ y $\langle V \rangle$ en el estado $|n\rangle$ de un oscilador armónico de masa $m$ y frecuencia $\eta$.  
(b) Demuestre que para $|n\rangle$:  
$$
\Delta x \Delta p = \hbar \left( n + \frac{1}{2} \right),
$$  
y explique por qué el estado base es de mínima incertidumbre.

---

**Problema 35 — Evolución temporal en oscilador armónico**  
Considere una partícula en un oscilador armónico de frecuencia $\eta$. En $t=0$, $|\psi(0)\rangle = |0\rangle + 2 |1\rangle$.  
(a) Probabilidad de medir energía $E_n$ en tiempo $t$.  
(b) Grafique e interprete $\mathcal{P}(t) = | \langle \psi(0) | \psi(t) \rangle |^2$.  
(c) Calcule $\langle \hat{x}(t) \rangle$ y $\langle \hat{p}(t) \rangle$.  
(d) Use el teorema de Ehrenfest para hallar $\dfrac{d}{dt}\langle \hat{x}(t) \rangle$ y $\dfrac{d}{dt}\langle \hat{p}(t) \rangle$. Resuelva y compare con (c).

---

**Problema 36 — Polinomios de Hermite**  
(a) Demuestre que:  
$$
H_n(y) := e^{y^2/2} \left( y - \frac{d}{dy} \right)^n e^{-y^2/2} = (-1)^n e^{y^2} \frac{d^n}{dy^n} e^{-y^2}.
$$  
(b) Deduzca $H_0(y)$, $H_1(y)$, $H_2(y)$, $H_3(y)$.  
(c) Demuestre:  
$$
\int_{-\infty}^{\infty} e^{-y^2} H_n(y) H_m(y)  dy = 2^n n! \sqrt{\pi}  \delta_{nm}.
$$  
(d) Demuestre que $H_n(y)$ satisface:  
$$
\left[ \frac{d^2}{dy^2} - 2y \frac{d}{dy} + 2n \right] H_n(y) = 0.
$$

---

**Problema 37 — Momento angular en coordenadas esféricas**  
Demuestre que $\hat{\vec{L}}$ es hermítico y que en coordenadas esféricas $(r, \theta, \varphi)$:  
(a) $\hat{L}_x = i\hbar \left( \sin \varphi \dfrac{\partial}{\partial \theta} + \dfrac{\cos \varphi}{\tan \theta} \dfrac{\partial}{\partial \varphi} \right)$,  
(b) $\hat{L}_y = i\hbar \left( -\cos \varphi \dfrac{\partial}{\partial \theta} + \dfrac{\sin \varphi}{\tan \theta} \dfrac{\partial}{\partial \varphi} \right)$,  
(c) $\hat{L}_z = -i\hbar \dfrac{\partial}{\partial \varphi}$,  
(d) $\hat{L}^2 = -\hbar^2 \left( \dfrac{\partial^2}{\partial \theta^2} + \dfrac{1}{\tan \theta} \dfrac{\partial}{\partial \theta} + \dfrac{1}{\sin^2 \theta} \dfrac{\partial^2}{\partial \varphi^2} \right)$,  
(e) $\nabla^2 = \dfrac{1}{r^2} \dfrac{\partial}{\partial r} \left( r^2 \dfrac{\partial}{\partial r} \right) - \dfrac{\hat{L}^2}{\hbar^2 r^2}$.

---

### **Taller 8**

**Problema 38 — Estado de mínima incertidumbre**  
Demuestre que para $|n\rangle$ en oscilador armónico:  
$$
\Delta x \Delta p = \hbar \left( n + \frac{1}{2} \right),
$$  
y explique por qué el estado base es de mínima incertidumbre.

---

**Problema 39 — Oscilador en campo electrostático**  
Hamiltoniano: $\hat{H} = \dfrac{\hat{p}^2}{2\mu} + \dfrac{1}{2}\mu\omega^2\hat{x}^2 - q\mathcal{E}\hat{x}$.  
(a) Muestre que las energías propias son:  
$$
E_n = \hbar\omega \left( n + \frac{1}{2} \right) - \frac{q^2\mathcal{E}^2}{2\mu\omega^2}, \quad n=0,1,\ldots
$$  
¿Funciones propias?  
(b) Con $\hbar = \mu = \omega = \mathcal{E} = q = 1$, encuentre la representación matricial de $\hat{x}$ y resuelva $\mathbb{H} \vec{\psi} = E \vec{\psi}$ truncando en $n_{\max}$. Verifique $E_n$ y analice dependencia en $n_{\max}$.

---

**Problema 40 — Pozo esférico infinito**  
Partícula de masa $\mu$ en $V(r) = \begin{cases} 0, & r < a \\ \infty, & r \geq a \end{cases}$.  
(a) Con $E = \dfrac{\hbar^2 k^2}{2\mu}$ y $\psi(\vec{r}) = R(r) Y_{lm}(\theta,\varphi)$, demuestre que $R(r)$ satisface:  
$$
(y^2 R')' + (y^2 - l(l+1)) R = 0, \quad y = kr.
$$  
(b) Con $u(y) = \sqrt{y} R(y)$, demuestre:  
$$
u'' + \frac{1}{y} u' + \left( 1 - \frac{(l+\frac{1}{2})^2}{y^2} \right) u = 0.
$$  
(c) Concluya que los estados propios son:  
$$
\psi_{nlm}(\vec{r}) = \begin{cases} 
\dfrac{1}{\sqrt{r}} J_{l+\frac{1}{2}}(k_{nl} r) Y_{lm}(\theta,\varphi), & r < a \\
0, & r \geq a 
\end{cases}
$$  
con $E_{nl} = \dfrac{\hbar^2 k_{nl}^2}{2\mu}$ y $k_{nl} a =$ ceros de $J_{l+\frac{1}{2}}$. ¿Degeneración de $E_{nl}$? ¿Por qué $J_{-l-\frac{1}{2}}$ no es solución física?

---

### **Taller 9**

**Problema 41 — Teorema de Feynman-Hellmann**  
(a) Demuestre:  
$$
\frac{dE_n}{d\lambda} = \left\langle \psi_n \left| \frac{\partial \hat{H}}{\partial \lambda} \right| \psi_n \right\rangle.
$$  
(b) Para átomo hidrogenoide ($\hat{H} = -\dfrac{\hbar^2}{2\mu} \dfrac{d^2}{dr^2} + \dfrac{\hbar^2 \ell(\ell+1)}{2\mu r^2} - \dfrac{Ze^2}{r}$):  
(i) Use $\lambda = e$ para mostrar $\left\langle \dfrac{1}{r} \right\rangle_{n\ell} = \dfrac{Z}{a_\mu n^2}$.  
(ii) Use $\lambda = \ell$ para mostrar $\left\langle \dfrac{1}{r^2} \right\rangle_{n\ell} = \dfrac{Z^2}{a_\mu^2 n^3 (\ell + 1/2)}$.

---

**Problema 42 — Positronium**  
Sistema electrón-positrón ($m_e = m_{e^+}$ carga para positrón).  
Calcule $\omega$, $R$, y energía de enlace en estado fundamental. Compare con hidrógeno.  
**Ayuda:** $R = \langle r \rangle$, velocidad de rotación = $\sqrt{\langle v^2 \rangle}$ (de $\langle K \rangle$).

---

**Problema 43 — Regiones prohibidas en hidrógeno**  
Para hidrógeno en estado base ($E_{1s} = -\frac{1}{2}$ u.a.):  
(a) Encuentre región clásicamente prohibida ($K < 0$).  
(b) Con $\psi_{1s}(r)$, calcule probabilidad de encontrar electrón en dicha región.

---

**Problema 44 — Valores esperados en hidrógeno**  
Átomo hidrogenoide (masa reducida $\mu$, carga nuclear $Ze^2$).  
(a) Demuestre que en estado base: $\langle r \rangle = \dfrac{3}{2} a_\mu$ con $a_\mu = \dfrac{\hbar^2}{\mu e^2}$.  
(b) Demuestre que en $|n\ell m\rangle$: $\langle v^2 \rangle = \dfrac{Z^2}{n^2} v_0^2$ con $v_0 = \dfrac{e^2}{\hbar} = 2.1876913 \times 10^6$ m/s.

--- 

**Nota:** Se han corregido errores tipográficos menores y unificado notaciones. Las ecuaciones están listas para compilar en LaTeX.