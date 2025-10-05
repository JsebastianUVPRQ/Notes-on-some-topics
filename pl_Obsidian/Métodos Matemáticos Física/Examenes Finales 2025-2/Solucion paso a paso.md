# Final 2

### **1. Oscilador armónico forzado**

#### **(a) Soluciones de la ecuación homogénea**

La ecuación homogénea es:
$$
\frac{d^2 x}{dt^2} + \alpha^2 x = 0
$$
La ecuación característica es:
$$
r^2 + \alpha^2 = 0 \quad \Rightarrow \quad r = \pm i\alpha
$$
La solución general es:
$$
x_h(t) = A \cos(\alpha t) + B \sin(\alpha t)
$$
o equivalentemente:
$$
x_h(t) = C_1 e^{i\alpha t} + C_2 e^{-i\alpha t}
$$
donde $A, B, C_1, C_2$ son constantes determinadas por las condiciones iniciales.

---

#### **(b) Ecuación de Green**

La función de Green $(t, t')$ satisface:
$$
\frac{\partial^2 G(t,t')}{\partial t^2} + \alpha^2 G(t,t') = \delta(t - t')
$$
Por invarianza temporal, $G(t,t') = G(t - t')$ por lo que se define $G(t)$ como:
$$
\frac{d^2 G(t)}{dt^2} + \alpha^2 G(t) = \delta(t)
$$

---

#### **(c) Transformada de Fourier de la función de Green**

La transformada de Fourier de $G(t)$ es:
$$
\tilde{G}(\omega) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{i\omega t} G(t)  dt
$$
y la inversa:
$$
G(t) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-i\omega t} \tilde{G}(\omega)  d\omega
$$

---

#### **(d) Obtención de $\tilde{G}(\omega)$ usando la ecuación de Green**

Sustituyendo la representación de Fourier en la ecuación de Green:
$$
\frac{d^2}{dt^2} \left( \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-i\omega t} \tilde{G}(\omega)  d\omega \right) + \alpha^2 \left( \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-i\omega t} \tilde{G}(\omega)  d\omega \right) = \delta(t)
$$
La derivada introduce $(-i\omega)^2 = -\omega^2$, entonces:
$$
\frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} (-\omega^2 + \alpha^2) \tilde{G}(\omega) e^{-i\omega t}  d\omega = \delta(t)
$$
Usando la representación de la delta:
$$
\delta(t) = \frac{1}{2\pi} \int_{-\infty}^{\infty} e^{-i\omega t}  d\omega
$$
Igualando integrandos:
$$
\frac{1}{\sqrt{2\pi}} (-\omega^2 + \alpha^2) \tilde{G}(\omega) = \frac{1}{2\pi}
$$
Despejando:
$$
\tilde{G}(\omega) = \frac{1}{\sqrt{2\pi}} \frac{1}{\alpha^2 - \omega^2}
$$

---

#### **(e) Función de Green y método de residuos**

La función de Green es:
$$
G(t) = \frac{1}{2\pi} \int_{-\infty}^{\infty} \frac{e^{-i\omega t}}{\alpha^2 - \omega^2}  d\omega
$$
El integrando tiene polos en $\omega = \pm \alpha$. Para evitar singularidades, se usa el valor principal de Cauchy. Reescribiendo:
$$
\frac{1}{\alpha^2 - \omega^2} = \frac{1}{2\alpha} \left( \frac{1}{\alpha - \omega} + \frac{1}{\alpha + \omega} \right)
$$
Calculando la integral:
$$
G(t) = \frac{1}{2\pi} \cdot \frac{\pi \text{sign}(t) \sin(\alpha t)}{\alpha} = \frac{\sin(\alpha |t|)}{2\alpha}
$$
Esta es la función de Green simétrica. Para condiciones de contorno específicas (e.g., retardada), se modifica el contorno de integración.

---

#### **(f) Solución para $F(t) = e^{i\beta t}$**

La solución particular es:
$$
x_p(t) = \int_{-\infty}^{\infty} G(t-t') F(t')  dt' = \int_{-\infty}^{\infty} \frac{\sin(\alpha |t-t'|)}{2\alpha} e^{i\beta t'}  dt'
$$
Usando el método de Fourier, se supone $x_p(t) = A e^{i\beta t}$. Sustituyendo en la ecuación:
$$
(-\beta^2 + \alpha^2) A e^{i\beta t} = e^{i\beta t} \quad \Rightarrow \quad A = \frac{1}{\alpha^2 - \beta^2}
$$
Por lo tanto:
$$
x_p(t) = \frac{e^{i\beta t}}{\alpha^2 - \beta^2}, \quad \beta \neq \alpha
$$
Si $\beta = \alpha$, hay resonancia y la solución es $x_p(t) = \frac{t e^{i\alpha t}}{2i\alpha}$.

---

### **2. Operador momento en mecánica cuántica**

#### **(a) Operador $P = -i \frac{d}{dx}$ es autoadjunto en $L^2(\mathbb{R})$**

Calculamos:
$$
\langle f, P g \rangle = \int_{-\infty}^{\infty} f^*(x) \left( -i \frac{d}{dx} g(x) \right) dx
$$
Integrando por partes:
$$
= -i \left[ f^*(x) g(x) \right]_{-\infty}^{\infty} + i \int_{-\infty}^{\infty} \frac{d f^*}{dx} g(x) dx
$$
El término de frontera se anula para funciones en $L^2(\mathbb{R})$ que decaen en infinito. Entonces:
$$
= \int_{-\infty}^{\infty} \left( i \frac{d f}{dx} \right)^* g(x) dx = \int_{-\infty}^{\infty} \left( -i \frac{d f}{dx} \right)^* g(x) dx = \langle P f, g \rangle
$$
Por lo tanto, $P$ es autoadjunto.

---

#### **(b) Ortogonalidad de vectores propios con diferentes valores propios**

Sean $A \psi_1 = \lambda_1 \psi_1$, $A \psi_2 = \lambda_2 \psi_2$ con $\lambda_1 \neq \lambda_2$. Entonces:
$$
\langle \psi_1, A \psi_2 \rangle = \lambda_2 \langle \psi_1, \psi_2 \rangle, \quad \langle A \psi_1, \psi_2 \rangle = \lambda_1 \langle \psi_1, \psi_2 \rangle
$$
Igualando:
$$
\lambda_1 \langle \psi_1, \psi_2 \rangle = \lambda_2 \langle \psi_1, \psi_2 \rangle \quad \Rightarrow \quad (\lambda_1 - \lambda_2) \langle \psi_1, \psi_2 \rangle = 0
$$
Como $\lambda_1 \neq \lambda_2$, se tiene $\langle \psi_1, \psi_2 \rangle = 0$.

---

#### **(c) Funciones propias de $P = -i \frac{d}{dx}$**

Resolviendo:
$$
-i \frac{d}{dx} \psi(x) = p \psi(x) \quad \Rightarrow \quad \frac{d\psi}{dx} = i p \psi
$$
La solución es:
$$
\psi(x) = C e^{i p x}
$$
donde $p \in \mathbb{R}$ es el valor propio. Estas funciones no son de cuadrado integrable, pero forman una base continua.

---

#### **(d) Descomposición en base ortogonal**

Para una base ortonormal $\{\phi_n\}$:
$$
f(x) = \sum_n c_n \phi_n(x), \quad c_n = \langle \phi_n, f \rangle
$$
Para la base continua de ondas planas:
$$
f(x) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} \tilde{f}(k) e^{i k x} dk, \quad \tilde{f}(k) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} f(x) e^{-i k x} dx
$$

---

#### **(e) Igual a (a)**

---

#### **(f) Completitud de las funciones propias de $P$**

Sí, las funciones $e^{i p x}$ forman una base completa para $L^2(\mathbb{R})$ mediante la transformada de Fourier.

---

#### **(g) Operador proyección**

Para un subespacio $V$ con base ortonormal $\{\phi_n\}$:
$$
P_V f = \sum_n \langle \phi_n, f \rangle \phi_n
$$
En el caso continuo, para un intervalo $[a,b]$ en el espacio de momentos:
$$
P_{[a,b]} f = \frac{1}{2\pi} \int_a^b \left( \int_{-\infty}^{\infty} f(x) e^{-i p x} dx \right) e^{i p x} dp
$$

---

#### **(h) Condiciones para que $P$ sea autoadjunto en $L^2([a,b])$**

Al integrar por partes:
$$
\langle f, P g \rangle = -i [f^*(x) g(x)]_a^b + \langle P f, g \rangle
$$
Para que $P$ sea autoadjunto, el término de frontera debe anularse. Esto se logra con condiciones de contorno periódicas:
$$
f(a) = f(b), \quad g(a) = g(b)
$$
Bajo estas condiciones, $P$ es autoadjunto.

---

# Final 3
