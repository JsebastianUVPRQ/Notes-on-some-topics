
# Primer grupo de ejercicios
Te voy a dar un largo grupo de ejercicios. Tu tarea es CREAR nuevos ejercicios acerca de los temas tratados (pero obviamente usando situaciones y enfoques distintos).
## Ejercicios teóricos
---
### A1 — $L^2(\mathbb{R}^d)$ es un espacio de Hilbert
**Enunciado.** Demuestra que $L^2(\mathbb{R}^d)$ con el producto $\langle f,g\rangle=\int_{\mathbb{R}^d} f\overline{g}$ es un espacio de Hilbert: verifica que es un producto interno y prueba su **completitud**.
**Objetivo:** familiaridad con la definición, manejo de sucesiones de Cauchy en normas $L^2$.
**Dificultad:** Medio.
**Pistas:** usa la desigualdad de Cauchy-Schwarz, considera una sucesión de Cauchy $(f_n)$ en norma $L^2$; extrae una subsecuencia convergente puntualmente casi en todas partes y aplica convergencia dominada o teoremas estándar de $L^p$.

---

### A2 — Teorema de Plancherel / Isometría de la transformada de Fourier

**Enunciado.** Con la convención $\widehat f(\xi)=\int_{\mathbb{R}^d} f(x)e^{-2\pi i x\cdot\xi}\,dx$, demuestra para $f,g$ en la clase de Schwartz que

$$
\int_{\mathbb{R}^d} f(x)\overline{g(x)}\,dx=\int_{\mathbb{R}^d}\widehat f(\xi)\overline{\widehat g(\xi)}\,d\xi.
$$

Concluye que la transformada se extiende por densidad a un operador unitario $L^2\to L^2$.
**Objetivo:** manejar transformada en espacios de prueba, extensión por densidad.
**Pistas:** prueba primero el caso $g=f$ (norma), usa Fubini y la transformada inversa en la clase de Schwartz; luego polariza.

---

### A3 — Gram–Schmidt en $L^2([-1,1])$

**Enunciado.** Aplica el proceso de Gram–Schmidt al conjunto $\{1,x,x^2\}$ en $L^2([-1,1])$ (peso 1) para obtener tres funciones ortonormales. Identifica la relación con los primeros polinomios de Legendre.
**Objetivo:** práctica con ortonormalización en espacios de funciones.
**Dificultad:** Fácil–Medio.
**Pistas:** calcula integrales $\int_{-1}^{1} x^n dx$ necesarias; normaliza cada vector al final.

---

### A4 — Riesz (esquema de prueba)

**Enunciado.** Sea $\mathcal H$ un espacio de Hilbert y $F:\mathcal H\to\mathbb C$ un funcional lineal y acotado. Muestra que existe único $g\in\mathcal H$ tal que $F(f)=\langle f,g\rangle$ para todo $f$.
**Objetivo:** comprender construcción geométrica usando el complemento ortogonal del núcleo.
**Dificultad:** Medio–Alto.
**Pistas:** si $F\equiv0$ es trivial. Si no, considera $K=\ker F$ (cerrado), usa el teorema de proyección ortogonal para elegir $u\in K^\perp$ con $F(u)\neq0$; normaliza convenientemente para construir $g$. No es necesario recurrir a Hahn–Banach para este caso.

---

### A5 — Dualidad de $L^p$

**Enunciado.** Demuestra que para $1<p<\infty$ el dual de $L^p(\mu)$ es isométrico a $L^q(\mu)$ donde $1/p+1/q=1$.
**Objetivo:** uso de Hölder y densidad de funciones simples.
**Dificultad:** Medio.
**Pistas:** construye la aplicación $\Phi:g\mapsto (f\mapsto\int f g)$, prueba que es isométrica y sobreyectiva.

---

### A6 — Derivadas en el sentido de distribuciones

**Enunciado.** Considera la función escalón de Heaviside $H(x)=\begin{cases}0,&x<0\\1,&x>0\end{cases}$ (valor en 0 irrelevante). Prueba que como distribución $H'=\delta$, es decir, la derivada de $H$ actúa sobre test functions $\varphi$ como $\langle H',\varphi\rangle=-\langle H,\varphi'\rangle=\varphi(0)$.
**Objetivo:** manejo de definiciones en espacios de distribuciones $\mathcal D'(\mathbb R)$.
**Dificultad:** Fácil.
**Pistas:** integra por partes con soporte compacto en la prueba.

---

### A7 — Transformada de Fourier de una gaussiana

**Enunciado.** Calcula $\displaystyle\int_{-\infty}^{\infty} e^{-\pi x^2} e^{-2\pi i x\xi}\,dx$ y muestra que es $e^{-\pi \xi^2}$. Generaliza al caso $e^{-a x^2}$.
**Objetivo:** técnica de completar el cuadrado y manejar integrales gaussianas.
**Dificultad:** Fácil–Medio.
**Pistas:** usar fórmula $\int e^{-ax^2+bx}dx = \sqrt{\pi/a}\, e^{b^2/(4a)}$ (para $\Re a>0$).

---

### A8 — Teorema de la convolución (Schwartz)

**Enunciado.** Para $f,g\in \mathcal S(\mathbb R^d)$ prueba que $\widehat{f*g}=\widehat f\cdot\widehat g$ y $\widehat{fg}=\widehat f * \widehat g$ (con las normalizaciones adecuadas).
**Objetivo:** manejar propiedades básicas de la FT y dominio de validez.
**Dificultad:** Medio.
**Pistas:** usar Fubini para intercambiar integrales y las definiciones.

---

## B) Ejercicios — *Aplicaciones en Física*

Divido por área; cada problema puede tener subapartados (a),(b),(c).

---

## Mecánica cuántica (Hilbert spaces, operadores, Fourier)

### B1 — Gaussiana mínima (estado coherente de 1D)

**Enunciado.** Sea $\psi(x)=A e^{-\alpha x^2}$ con $\alpha>0$ real.
a) Encuentra la normalización $A$.
b) Calcula $\langle x\rangle,\ \langle x^2\rangle$.
c) Calcula la transformada de Fourier $\widetilde\psi(p)$ (convención $p$ = momentum) y $\langle p\rangle,\ \langle p^2\rangle$.
d) Muestra que la desigualdad de Heisenberg se satisface y que este estado es un mínimo (producto de incertidumbres mínimo).
**Objetivo:** conectar $L^2$, FT y operadores de QM.
**Dificultad:** Medio.
**Pistas / esquema de resultados esperados:** $A=(2\alpha/\pi)^{1/4}$, $\langle x\rangle=0$, $\langle x^2\rangle=1/(4\alpha)$. En impulso $\sigma_p=\hbar\sqrt{\alpha}$ y $\sigma_x\sigma_p=\hbar/2$.

---

### B2 — Caja infinita: expansión en base ortonormal y evolución temporal

**Enunciado.** Partícula en caja $[0,L]$ con ondas estacionarias $\phi_n(x)=\sqrt{\tfrac{2}{L}}\sin\big(\tfrac{n\pi x}{L}\big)$. Sea la condición inicial $\psi(x,0)=C x(L-x)$ en $[0,L]$ (0 fuera).
a) Expande $\psi(x,0)$ en la base $\{\phi_n\}$ y expresa los coeficientes $c_n$.
b) Escribe $\psi(x,t)$ usando la evolución en autovalores $E_n$.
c) ¿Qué condiciones de regularidad sobre $\psi(x,0)$ garantizan la convergencia uniforme de la serie y la posibilidad de derivar término a término?
**Objetivo:** habilidad práctica con bases ortonormales y evolución por descomposición espectral.
**Dificultad:** Medio.
**Pistas:** integra por partes para expresar los $c_n$; la rapidez de decaimiento de $c_n$ está ligada a la suavidad de $\psi(x,0)$.

---

### B3 — Auto-adjunción del operador laplaciano en 1D

**Enunciado.** Considera $T=-\dfrac{d^2}{dx^2}$ con dominio $D(T)=\{u\in L^2(0,L): u,u'\ \text{abs. cont.}, u''\in L^2, \ u(0)=u(L)=0\}$.
a) Prueba que $T$ es simétrico.
b) Muestra que $T$ es auto-adjunto y encuentra su espectro puntual (autovalores y autovectores).
**Objetivo:** práctica con definiciones de simetría y autoadjunción para operadores diferenciales y su espectro discreto.
**Dificultad:** Medio–Alto.
**Pistas:** usa integración por partes; las condiciones de Dirichlet dan autovalores $ (n\pi/L)^2$ y autovectores $\sin(n\pi x/L)$.

---

### B4 — Interpretación funcional de expectativas

**Enunciado.** Sea $A:\mathcal H\to\mathcal H$ un operador acotado y auto-adjunto. Para estados $\psi\in\mathcal H$ unitarios, la expectativa se define $\langle A\rangle_\psi=\langle\psi,A\psi\rangle$. Muestra que para cada $\phi$ fijo, la aplicación $F_\phi:\psi\mapsto \langle \psi, A\phi\rangle$ es un funcional lineal y acotado, y encuentra el vector $g\in\mathcal H$ que lo representa según Riesz.
**Objetivo:** ligar Riesz con expectativas y representación mediante vectores.
**Dificultad:** Fácil–Medio.
**Pistas:** $F_\phi(\psi)=\langle\psi, A\phi\rangle$ y ya está en forma $ \langle\psi,g\rangle$ con $g=A\phi$.

---

## Electrodinámica (Poisson, potenciales, FT en $\mathbb R^3$)

### C1 — Potencial de una gaussiana (Poisson por Fourier)

**Enunciado.** Densidad de carga $\rho(x)=\dfrac{Q}{(2\pi\sigma^2)^{3/2}} e^{-|x|^2/(2\sigma^2)}$ en $\mathbb R^3$. Resuelve $\nabla^2\phi=-\rho/\varepsilon_0$ por transformada de Fourier y obtiene $\phi(r)$. (Busca la forma en términos de $\mathrm{erf}$).
**Objetivo:** usar FT para resolver Poisson en $\mathbb R^3$ y comprender regularización por carga extendida.
**Dificultad:** Medio.
**Pistas / resultado esperado:** $\widehat{\rho}(k)=Q e^{-(\sigma^2|k|^2)/2}$ y $\widehat\phi(k)=\dfrac{\widehat\rho(k)}{\varepsilon_0 |k|^2}$; tras invertir obtendrás $\phi(r)=\dfrac{Q}{4\pi\varepsilon_0 r}\operatorname{erf}\big(\dfrac{r}{\sqrt{2}\sigma}\big)$.

---

### C2 — Coulomb y transformada en el sentido de distribuciones

**Enunciado.** Muestra (en sentido de distribuciones) que en $\mathbb R^3$

$$
\mathcal F\Big(\frac{1}{|x|}\Big)(k) = \frac{C}{|k|^2}
$$

para una constante $C$ apropiada con la convención de Fourier usada. Indica cómo estas identidades deben interpretarse (regularización en $k=0$).
**Objetivo:** relación entre kernels de Green y transformadas; uso de distribuciones.
**Dificultad:** Medio–Alto.
**Pistas:** procede regularizando $1/|x|$ por multiplicación por $e^{-\varepsilon |x|}$ y pasar al límite; fíjate en factores $2\pi$.

---

## Mecánica estadística / teoría de muchos cuerpos

### D1 — Integral gaussiana y partición del oscilador clásico

**Enunciado.** Para el oscilador armónico clásico 1D $H=\dfrac{p^2}{2m}+\dfrac{1}{2}m\omega^2 x^2$, calcula la función de partición canónica $Z(\beta)$ (integrando sobre $x,p\in\mathbb R$). Deduce la energía media $\langle E\rangle$ y muestra la equipartición.
**Objetivo:** aplicar integrales gaussianas a estadísticas clásicas.
**Dificultad:** Fácil.
**Pistas / resultado esperado:** $Z(\beta)=\dfrac{2\pi}{\beta \omega}\cdot (\text{factor } 1/\sqrt{m})$ según normalización; $\langle E\rangle = k_B T$ (dos grados cuadráticos).

---

### D2 — Cadena armónica periódica y modos normales (FFT)

**Enunciado.** Considera $N$ osciladores en anillo (condición periódica) con hamiltoniano cuadrático acoplado por constantes elásticas: escribe la matriz dinámica (laplaciano discreto), diagonalízala por la transformada discreta de Fourier y obtiene las frecuencias normales $\omega_k$.
**Objetivo:** ver la conexión entre Fourier discreta y diagonalización espectral (densidad de estados luego).
**Dificultad:** Medio.
**Pistas:** para paso $a$ resultan $\omega_k^2 = \omega_0^2 + \dfrac{4K}{m}\sin^2\!(\tfrac{\pi k}{N})$ (estructura típica).

---

### D3 — Difusión y ecuación de calor (aplicación física)

**Enunciado.** La ecuación de difusión $ \partial_t u = D \Delta u$ con condición inicial $u(x,0)=\delta(x)$ en $\mathbb R$ tiene núcleo gaussiano. Deriva la solución por transformada de Fourier y calcula $\langle x^2(t)\rangle$.
**Objetivo:** manejo práctico de FT en PDEs físicas.
**Dificultad:** Fácil–Medio.
**Pistas / resultado esperado:** $u(x,t)=\dfrac{1}{\sqrt{4\pi D t}}e^{-x^2/(4Dt)}$ y $\langle x^2\rangle = 2Dt$.

---

## Ecuaciones en derivadas parciales / funciones de Green

### E1 — Ecuación del calor: suavizado y conservación de la norma $L^1$

**Enunciado.** Sea $u(x,t)$ solución de la ecuación del calor con $u(\cdot,0)=f\in L^1(\mathbb R^d)$.
a) Muestra que $u(\cdot,t)=G_t*f$ con el kernel gaussiano $G_t$.
b) Prueba que $\|u(\cdot,t)\|_{L^1}=\|f\|_{L^1}$ (conservación de masa) y que $u(\cdot,t)$ se suaviza (es $C^\infty$ para $t>0$).
**Objetivo:** propiedades de semigrupos de convolución y regularización.
**Dificultad:** Medio.
**Pistas:** usa propiedades de la convolución y diferenciación bajo el signo integral.

---

### E2 — Poisson con fuente puntual (solución débil)

**Enunciado.** Resuelve $-\Delta u=\delta$ en $\mathbb R^3$ buscando $u$ radial y determina su forma (hasta una constante). Interpreta el resultado como la función de Green del Laplaciano.
**Objetivo:** relación entre Green y distribuciones.
**Dificultad:** Fácil–Medio.
**Pistas / resultado:** $u(x)= -\dfrac{1}{4\pi |x|}$ (constante según convención del signo).

---

## Procesamiento de señales / óptica

### F1 — Energía en dominio tiempo/frecuencia (Parseval aplicado)

**Enunciado.** Sea $s(t)\in L^2(\mathbb R)$ la señal. Aplica Parseval para mostrar que la “energía” $\int |s(t)|^2 dt$ se conserva en la transformada y usa esto para evaluar la energía de una señal dada por $s(t)=\mathrm{sinc}(t)$ (o una gaussiana).
**Objetivo:** entender interpretación física de Plancherel/Parseval.
**Dificultad:** Fácil.
**Pistas:** calcula FT explícita de la señal elegida y compara integrales.

---
# Segundo grupo de ejercicios
## A) Ejercicios Teóricos
---

### A1' — Espacios de Sobolev como espacios de Hilbert

**Enunciado.** Define el espacio de Sobolev $H^1(\mathbb{R})$ como el conjunto de funciones $f \in L^2(\mathbb{R})$ cuya derivada débil $f'$ también pertenece a $L^2(\mathbb{R})$. Demuestra que con el producto interno 
$$\langle f, g \rangle_{H^1} = \int_{\mathbb{R}} f(x)\overline{g(x)}\,dx + \int_{\mathbb{R}} f'(x)\overline{g'(x)}\,dx$$
$H^1(\mathbb{R})$ es un espacio de Hilbert.

**Objetivo:** entender cómo las normas que incorporan derivadas definen espacios de Hilbert relevantes para EDPs.

**Dificultad:** Medio–Alto.

**Pistas:** verifica primero que el producto interno está bien definido; para la completitud, toma una sucesión de Cauchy en $H^1$ y demuestra que converge en $L^2$ tanto la sucesión como sus derivadas débiles; usa el teorema de convergencia dominada para relacionar los límites.

---

### A2' — Transformada de Fourier y espacios de Sobolev

**Enunciado.** Demuestra que para $f \in \mathcal{S}(\mathbb{R}^d)$ (clase de Schwartz), la norma del espacio de Sobolev $H^s(\mathbb{R}^d)$ definida por 
$$\|f\|_{H^s}^2 = \int_{\mathbb{R}^d} (1+|\xi|^2)^s |\widehat{f}(\xi)|^2\,d\xi$$
es equivalente a la norma obtenida mediante derivadas débiles. Muestra además que la transformada de Fourier extiende a un isomorfismo unitario entre $H^s(\mathbb{R}^d)$ y $L^2(\mathbb{R}^d, (1+|\xi|^2)^s d\xi)$.

**Objetivo:** conectar la suavidad en el espacio físico con el decaimiento en el espacio de Fourier.

**Dificultad:** Medio–Alto.

**Pistas:** usa la identidad $\widehat{\partial^\alpha f}(\xi) = (2\pi i \xi)^\alpha \widehat{f}(\xi)$ para relacionar derivadas con multiplicación por polinomios; prueba primero para $s \in \mathbb{N}$ y luego extiende a $s \in \mathbb{R}$ mediante interpolación.

---

### A3' — Polinomios de Hermite mediante Gram–Schmidt

**Enunciado.** Aplica el proceso de Gram–Schmidt al conjunto $\{1, x, x^2, x^3\}$ en el espacio $L^2(\mathbb{R}, e^{-x^2}dx)$ (con peso gaussiano) para obtener cuatro funciones ortonormales. Identifica la relación con los primeros polinomios de Hermite y calcula la norma de cada polinomio en este espacio con peso.

**Objetivo:** práctica con ortonormalización en espacios con peso no uniforme y conexión con polinomios ortogonales clásicos.

**Dificultad:** Medio.

**Pistas:** recuerda que $\int_{-\infty}^{\infty} x^n e^{-x^2} dx = 0$ para $n$ impar; para $n$ par usa $\int_{-\infty}^{\infty} x^{2k} e^{-x^2} dx = \frac{(2k-1)!!}{2^k}\sqrt{\pi}$; los polinomios de Hermite satisfacen $H_n'(x) = 2nH_{n-1}(x)$.

---

### A4' — Funcional de evaluación en espacios de Sobolev

**Enunciado.** Sea $H^1([0,1])$ el espacio de Sobolev con producto interno $\langle f,g \rangle = \int_0^1 fg + \int_0^1 f'g'$. Considera el funcional $F(f) = f(0)$. Demuestra que $F$ es acotado y encuentra explícitamente el vector $g \in H^1([0,1])$ tal que $F(f) = \langle f,g \rangle$ para todo $f \in H^1([0,1])$.

**Objetivo:** aplicación concreta del teorema de Riesz en un espacio de Sobolev.

**Dificultad:** Medio.

**Pistas:** usa la desigualdad $|f(0)|^2 \leq 2\|f\|_{L^2}^2 + 2\|f'\|_{L^2}^2$; resuelve la ecuación diferencial $-g'' + g = 0$ con condiciones de frontera adecuadas para encontrar $g$.

---

### A5' — Caso límite de dualidad: $L^1$ y medidas

**Enunciado.** Demuestra que el dual de $L^1(\mathbb{R}^d)$ es isométrico al espacio de medidas de Radon finitas $\mathcal{M}(\mathbb{R}^d)$, no a $L^\infty(\mathbb{R}^d)$. Muestra con un ejemplo concreto (como la delta de Dirac) que hay funcionales lineales acotados en $L^1$ que no pueden representarse mediante funciones en $L^\infty$.

**Objetivo:** entender por qué falla la dualidad $L^p$-$L^q$ en los casos límite.

**Dificultad:** Alto.

**Pistas:** usa el teorema de representación de Riesz para medidas; demuestra que la delta de Dirac define un funcional acotado en $L^1$ pero no puede escribirse como $\int f\phi$ para alguna $\phi \in L^\infty$.

---

### A6' — Derivada de la función valor absoluto

**Enunciado.** Considera la función $f(x) = |x|$ en $\mathbb{R}$. Prueba que su derivada primera en el sentido de distribuciones es $f'(x) = \text{sign}(x)$ y que su derivada segunda es $f''(x) = 2\delta(x)$, donde $\delta$ es la delta de Dirac. Verifica explícitamente que $\langle f'', \varphi \rangle = \langle 2\delta, \varphi \rangle$ para toda función test $\varphi \in C_c^\infty(\mathbb{R})$.

**Objetivo:** manejar derivadas de distribuciones para funciones continuas pero no diferenciables.

**Dificultad:** Fácil–Medio.

**Pistas:** divide la integral en $(-\infty,0)$ y $(0,\infty)$ para calcular $\langle f', \varphi \rangle = -\langle f, \varphi' \rangle$; usa integración por partes en cada intervalo y considera el salto en $x=0$.

---

## B) Ejercicios — *Aplicaciones en Física*

---

## Mecánica cuántica (Hilbert spaces, operadores, Fourier)

### B1' — Estados excitados del oscilador armónico cuántico

**Enunciado.** Considera el hamiltoniano del oscilador armónico cuántico $H = -\frac{\hbar^2}{2m}\frac{d^2}{dx^2} + \frac{1}{2}m\omega^2x^2$.
a) Define los operadores de creación y aniquilación $a^\dagger$ y $a$, y expresa $H$ en términos de ellos.
b) Partiendo del estado fundamental $\psi_0(x) = (\frac{m\omega}{\pi\hbar})^{1/4}e^{-m\omega x^2/2\hbar}$, construye explícitamente el primer estado excitado $\psi_1(x)$ usando $a^\dagger$.
c) Calcula $\langle x \rangle$, $\langle x^2 \rangle$, $\langle p \rangle$ y $\langle p^2 \rangle$ para $\psi_1(x)$.
d) Verifica que la incertidumbre satisface $\Delta x \Delta p = \frac{3\hbar}{2} > \frac{\hbar}{2}$.

**Objetivo:** entender la construcción algebraica de estados cuánticos y cómo aumenta la incertidumbre en estados excitados.

**Dificultad:** Medio.

**Pistas:** los operadores son $a = \sqrt{\frac{m\omega}{2\hbar}}(x + \frac{i}{m\omega}p)$ y $a^\dagger = \sqrt{\frac{m\omega}{2\hbar}}(x - \frac{i}{m\omega}p)$; $\psi_n(x) = \frac{(a^\dagger)^n}{\sqrt{n!}}\psi_0(x)$; usa las relaciones de conmutación $[a,a^\dagger] = 1$.

---

### B2' — Partícula en un potencial periódico (Teoría de Bloch)

**Enunciado.** Considera una partícula cuántica en un potencial periódico $V(x+a) = V(x)$.
a) Demuestra que las soluciones de la ecuación de Schrödinger $-\frac{\hbar^2}{2m}\psi'' + V\psi = E\psi$ tienen la forma $\psi_k(x) = e^{ikx}u_k(x)$ donde $u_k(x+a) = u_k(x)$ (teorema de Bloch).
b) Para el potencial débil $V(x) = V_0\cos(\frac{2\pi x}{a})$, resuelve aproximadamente la ecuación de Schrödinger cerca de $k = \pi/a$ y encuentra la brecha de energía.
c) Muestra cómo la estructura de bandas emerge de este análisis.

**Objetivo:** conectar análisis funcional con la teoría de bandas en sólidos.

**Dificultad:** Alto.

**Pistas:** usa el teorema de Floquet para EDPs con coeficientes periódicos; para el potencial débil, expande en series de Fourier y resuelve el sistema matricial resultante; la brecha en $k = \pi/a$ está relacionada con el coeficiente de Fourier $V_1$.

---

### B3' — Operador momento en un intervalo finito

**Enunciado.** Considera el operador momento $P = -i\hbar\frac{d}{dx}$ en $L^2([0,L])$.
a) Muestra que $P$ es simétrico si y solo si se imponen condiciones de frontera periódicas $\psi(0) = \psi(L)$.
b) Demuestra que bajo estas condiciones, $P$ es auto-adjunto y encuentra su espectro puntual completo.
c) Explica por qué el operador momento no puede ser auto-adjunto con condiciones de frontera de Dirichlet $\psi(0) = \psi(L) = 0$.

**Objetivo:** entender el papel crucial de las condiciones de frontera en la auto-adjunción de operadores cuánticos.

**Dificultad:** Medio–Alto.

**Pistas:** para la simetría, usa integración por partes y analiza los términos de frontera; el espectro bajo condiciones periódicas es $\{p_n = \frac{2\pi\hbar n}{L} | n \in \mathbb{Z}\}$; con condiciones de Dirichlet, el operador no es simétrico porque los términos de frontera no se cancelan.

---

## Electrodinámica (Poisson, potenciales, FT en $\mathbb{R}^3$)

### C1' — Campo magnético de un dipolo mediante Fourier

**Enunciado.** Un dipolo magnético puntual en el origen con momento $\vec{m} = m\hat{z}$ genera una densidad de corriente $\vec{J}(\vec{r}) = -\frac{1}{2}(\vec{m} \times \nabla)\delta(\vec{r})$.
a) Usa la transformada de Fourier para resolver $\nabla^2 \vec{A} = -\mu_0 \vec{J}$ y encontrar el potencial vector $\vec{A}$.
b) Calcula el campo magnético $\vec{B} = \nabla \times \vec{A}$ y muestra que coincide con la expresión conocida $\vec{B}(\vec{r}) = \frac{\mu_0}{4\pi}\left[\frac{3(\vec{m}\cdot\hat{r})\hat{r}-\vec{m}}{r^3}\right]$.
c) Explica por qué este método evita las singularidades que aparecen en el cálculo directo.

**Objetivo:** aplicar transformada de Fourier a problemas magnétostáticos y entender su ventaja para manejar distribuciones.

**Dificultad:** Medio–Alto.

**Pistas:** en el espacio de Fourier, $\widehat{\vec{A}}(\vec{k}) = \frac{\mu_0 \widehat{\vec{J}}(\vec{k})}{|\vec{k}|^2}$; usa identidades vectoriales para simplificar $\widehat{\vec{J}}(\vec{k})$; la inversión de la transformada requiere cuidado con las singularidades en $k=0$.

---

### C2' — Potencial de un disco cargado uniformemente

**Enunciado.** Un disco de radio $R$ en el plano $xy$ tiene densidad de carga superficial uniforme $\sigma$.
a) Plantea la integral para el potencial electrostático $\phi(z)$ en el eje $z$ y evalúala.
b) Usa la representación en series de Fourier-Bessel para encontrar $\phi(r,z)$ fuera del eje.
c) Muestra que en el límite $R \to \infty$, el potencial se reduce al de un plano infinito.

**Objetivo:** resolver problemas electrostáticos con simetría cilíndrica y conectar con expansiones en funciones especiales.

**Dificultad:** Medio–Alto.

**Pistas:** en el eje, $\phi(z) = \frac{\sigma}{2\epsilon_0}(\sqrt{R^2+z^2}-|z|)$; fuera del eje, usa la representación $\frac{1}{|\vec{r}-\vec{r}'|} = \int_0^\infty J_0(kr)J_0(kr')e^{-k|z-z'|}k\,dk$; el límite $R \to \infty$ corresponde a tomar solo el término $k=0$ en la expansión.

---

## Mecánica estadística / teoría de muchos cuerpos

### D1' — Gas ideal cuántico en una dimensión

**Enunciado.** Considera $N$ fermiones no interactuantes en una caja unidimensional $[0,L]$.
a) Calcula la función de partición canónica $Z(\beta)$ en el límite termodinámico $N,L \to \infty$ con $N/L$ fijo.
b) Deriva la relación entre la energía media $\langle E \rangle$ y la temperatura $T$.
c) Muestra que en el límite clásico recobras el resultado de equipartición, mientras que en el límite de degeneración completa obtienes $\langle E \rangle \propto T^2$.

**Objetivo:** conectar análisis funcional con estadística cuántica y entender transiciones entre regímenes clásico y cuántico.

**Dificultad:** Alto.

**Pistas:** los niveles de energía son $E_n = \frac{\hbar^2\pi^2n^2}{2mL^2}$; en el límite termodinámico, reemplaza sumas por integrales; usa la distribución de Fermi-Dirac $f(E) = \frac{1}{e^{\beta(E-\mu)}+1}$; el potencial químico $\mu$ satisface $N = \int_0^\infty f(E)g(E)dE$ donde $g(E)$ es la densidad de estados.

---

### D2' — Cadena de osciladores con interacciones de largo alcance

**Enunciado.** Considera $N$ partículas en una línea con hamiltoniano 
$$H = \sum_{j=1}^N \frac{p_j^2}{2m} + \frac{K}{2} \sum_{j \neq k} \frac{(q_j - q_k)^2}{|j-k|^\alpha}$$
a) Diagonaliza el hamiltoniano usando la transformada discreta de Fourier.
b) Encuentra las frecuencias normales $\omega_k$ en función de $\alpha$.
c) Analiza cómo cambia la densidad de estados para diferentes valores de $\alpha$ (especialmente $\alpha < 1$, $\alpha = 1$, $\alpha > 1$).

**Objetivo:** entender cómo las interacciones de largo alcance afectan las propiedades espectrales de sistemas many-body.

**Dificultad:** Alto.

**Pistas:** la matriz de acoplamiento tiene elementos $V_{jk} = \frac{K}{|j-k|^\alpha}$ para $j \neq k$; en el espacio de Fourier, el acoplamiento se convierte en una multiplicación por $\hat{V}(k) = K\sum_{n \neq 0} \frac{1-e^{2\pi i kn/N}}{|n|^\alpha}$; para $\alpha > 1$, $\hat{V}(k) \approx C - D|k|^{\alpha-1}$ cerca de $k=0$.

---

### D3' — Ecuación de Schrödinger libre

**Enunciado.** Considera la ecuación de Schrödinger libre $i\hbar\partial_t \psi = -\frac{\hbar^2}{2m}\Delta \psi$ en $\mathbb{R}$.
a) Resuelve la ecuación por transformada de Fourier y encuentra la solución fundamental (propagador).
b) Para una condición inicial gaussiana $\psi(x,0) = (\frac{1}{\pi\sigma^2})^{1/4}e^{-x^2/(2\sigma^2)}$, calcula $\psi(x,t)$ explícitamente.
c) Muestra que la incertidumbre en posición aumenta con el tiempo como $\Delta x(t) = \sigma\sqrt{1 + (\frac{\hbar t}{2m\sigma^2})^2}$.

**Objetivo:** comparar la dinámica cuántica con la difusión clásica y entender la dispersión de paquetes de onda.

**Dificultad:** Medio.

**Pistas:** el propagador es $U(x,t) = \sqrt{\frac{m}{2\pi i\hbar t}}e^{imx^2/(2\hbar t)}$; para la gaussiana, usa la fórmula de completar el cuadrado; la varianza en posición se calcula como $\langle x^2 \rangle - \langle x \rangle^2$.

---

## Ecuaciones en derivadas parciales / funciones de Green

### E1' — Ecuación de ondas en 1D: representación espectral

**Enunciado.** Considera la ecuación de ondas en 1D: $\partial_t^2 u = c^2 \partial_x^2 u$.
a) Usa la transformada de Fourier para encontrar la solución con condiciones iniciales $u(x,0) = f(x)$, $\partial_t u(x,0) = g(x)$.
b) Muestra que la solución coincide con la fórmula de d'Alembert $u(x,t) = \frac{1}{2}[f(x-ct) + f(x+ct)] + \frac{1}{2c}\int_{x-ct}^{x+ct} g(y)dy$.
c) Analiza cómo la regularidad de $f$ y $g$ afecta la regularidad de $u(x,t)$.

**Objetivo:** relacionar métodos espectrales con soluciones clásicas de EDPs hiperbólicas.

**Dificultad:** Medio.

**Pistas:** en el espacio de Fourier, la ecuación se convierte en $\partial_t^2 \hat{u} = -c^2|k|^2 \hat{u}$; resuelve esta EDO ordinaria para cada $k$; usa el teorema de inversión y propiedades de convolución para recuperar d'Alembert.

---

### E2' — Función de Green para el operador de Helmholtz

**Enunciado.** Encuentra la función de Green $G(\vec{r})$ para el operador de Helmholtz $(-\Delta - k^2)$ en $\mathbb{R}^3$, es decir, resuelve $(-\Delta - k^2)G = \delta$.
a) Usa la transformada de Fourier para obtener una expresión para $\hat{G}(\vec{\kappa})$.
b) Evalúa la integral de inversión usando coordenadas esféricas y demuestra que $G(r) = \frac{e^{ikr}}{4\pi r}$ corresponde a ondas salientes.
c) Explica por qué hay dos posibles soluciones (ondas salientes y entrantes) y cómo se selecciona la correcta según las condiciones de contorno.

**Objetivo:** entender la conexión entre funciones de Green, transformada de Fourier y condiciones de radiación.

**Dificultad:** Alto.

**Pistas:** en el espacio de Fourier, $\hat{G}(\vec{\kappa}) = \frac{1}{|\vec{\kappa}|^2 - k^2}$; la singularidad en $|\vec{\kappa}| = k$ requiere un desplazamiento en el contorno de integración (principio de absorción limitada); el signo del desplazamiento determina si se obtienen ondas salientes o entrantes.

---

## Procesamiento de señales / óptica

### F1' — Teorema de muestreo de Nyquist-Shannon

**Enunciado.** Sea $f \in L^2(\mathbb{R})$ una función cuya transformada de Fourier $\hat{f}$ se anula fuera del intervalo $[-\Omega, \Omega]$ (función de banda limitada).
a) Demuestra que $f$ puede reconstruirse completamente a partir de sus muestras $f(nT)$ con $T = \frac{\pi}{\Omega}$ mediante la fórmula 
$$f(t) = \sum_{n=-\infty}^{\infty} f(nT) \frac{\sin(\Omega(t-nT))}{\Omega(t-nT)}$$
b) Muestra que si el muestreo se realiza con $T > \frac{\pi}{\Omega}$, ocurre aliasing (solapamiento espectral).
c) Ilustra con un ejemplo cómo el aliasing distorsiona una señal.

**Objetivo:** entender la base matemática del muestreo digital y sus limitaciones prácticas.

**Dificultad:** Medio–Alto.

**Pistas:** usa la representación en serie de Fourier de $\hat{f}$ en $[-\Omega,\Omega]$; la fórmula de Poisson establece que $\sum_{n=-\infty}^{\infty} f(t+nT) = \frac{1}{T}\sum_{k=-\infty}^{\infty} \hat{f}(k/T)e^{2\pi i kt/T}$; el sinc es la transformada inversa de una función indicatriz.


