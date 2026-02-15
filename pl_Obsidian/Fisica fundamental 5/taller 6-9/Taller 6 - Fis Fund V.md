
## Problem 1: Delta Potential in Momentum Space

This problem demonstrates a powerful alternative to the usual position-space method for solving the delta well, relying on Fourier transforms.

### (a) Finding $V(p)$ and the Form of $\psi(p)$

**1. Find $V(p)$.** The problem defines the transform as:
$$
\tilde{f}(p) = \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^{\infty} dx \, e^{-\frac{i}{\hbar} px} f(x)
$$
For the potential $V(x) = -g\delta(x)$, we compute its Fourier transform:
$$
V(p) = \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^{\infty} dx \, e^{-\frac{i}{\hbar} px} (-g\delta(x))
$$
Using the sifting property of the delta function, $\int_{-\infty}^{\infty} f(x)\delta(x) dx = f(0)$:
$$
V(p) = -\frac{g}{\sqrt{2\pi\hbar}} e^{0} = -\frac{g}{\sqrt{2\pi\hbar}}
$$
So, $V(p)$ is a constant in momentum space. This is a key simplification: a Dirac delta in position becomes a constant in momentum .

**2. Substitute into the momentum-space Schrödinger equation.** The given equation is:
$$
\frac{p^2}{2\mu} \psi(p) + \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^{\infty} dp' \, V(p-p') \psi(p') = E \psi(p)
$$
Notice there's a slight mismatch: the problem statement has $V(p') - p$ which seems like a typo. From the context of a convolution, it should be $V(p-p')$. We'll proceed with the correct form. Substituting $V(p-p') = -\frac{g}{\sqrt{2\pi\hbar}}$:
$$
\frac{p^2}{2\mu} \psi(p) + \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^{\infty} dp' \left( -\frac{g}{\sqrt{2\pi\hbar}} \right) \psi(p') = E \psi(p)
$$
The term in the integral is no longer dependent on $p'$, so we can factor it out:
$$
\frac{p^2}{2\mu} \psi(p) - \frac{g}{2\pi\hbar} \int_{-\infty}^{\infty} \psi(p') dp' = E \psi(p)
$$

**3. Solve for $\psi(p)$.** The integral $\int_{-\infty}^{\infty} \psi(p') dp'$ is just a number (a constant). Let's call this constant $C$.
$$
C = \int_{-\infty}^{\infty} \psi(p') dp'
$$
The equation becomes:
$$
\left( \frac{p^2}{2\mu} - E \right) \psi(p) = \frac{g}{2\pi\hbar} C
$$
Since $E < 0$ for a bound state, we can define $p_0 = \sqrt{-2\mu E} > 0$. Then:
$$
\frac{p^2}{2\mu} - E = \frac{p^2}{2\mu} + \frac{p_0^2}{2\mu} = \frac{1}{2\mu}(p^2 + p_0^2)
$$
Solving for $\psi(p)$:
$$
\psi(p) = \frac{ \frac{g}{2\pi\hbar} C }{ \frac{1}{2\mu}(p^2 + p_0^2) } = \frac{ g \mu C }{ \pi\hbar } \cdot \frac{1}{p^2 + p_0^2}
$$
This confirms the required form $\psi(p) = \frac{N}{p^2 + p_0^2}$, where the constant $N = \frac{g \mu C}{\pi\hbar}$.

### (b) Determining $p_0$ and Concluding Uniqueness

**1. Use the definition of $C$ to find a consistency condition.** The constant $C$ is not independent; it is defined as the integral of $\psi(p)$. We substitute our solution for $\psi(p)$ back into the definition of $C$:
$$
C = \int_{-\infty}^{\infty} \psi(p) dp = \int_{-\infty}^{\infty} \frac{N}{p^2 + p_0^2} dp
$$
We are given the useful integral $\int_{-\infty}^{\infty} \frac{dp}{p^2 + p_0^2} = \frac{\pi}{p_0}$. Therefore:
$$
C = N \cdot \frac{\pi}{p_0}
$$

**2. Solve for $p_0$.** We have two expressions for $N$:
- From the form of the solution: $N = \frac{g \mu C}{\pi\hbar}$
- From the integral condition: $N = \frac{C p_0}{\pi}$

Equate these two expressions for $N$:
$$
\frac{g \mu C}{\pi\hbar} = \frac{C p_0}{\pi}
$$
Assuming $C \neq 0$ (which would imply no wavefunction), we can cancel $C/\pi$ from both sides:
$$
\frac{g \mu}{\hbar} = p_0
$$
This is the unique value of $p_0$. Since $p_0$ is fixed, there is only one possible bound state. This matches the well-known result from the position-space solution, where the energy is $E = -\frac{p_0^2}{2\mu} = -\frac{\mu g^2}{2\hbar^2}$ .

---

## Problem 2: Infinite Square Well

This problem deals with the standard particle in a box and the time evolution of a superposition state.

### (a) Eigenfunctions and Eigenvalues

**1. Verify the eigenfunctions.** The time-independent Schrödinger equation inside the well ($0 \le x \le L$) is:
$$
-\frac{\hbar^2}{2m} \frac{d^2 \phi(x)}{dx^2} = E \phi(x)
$$
The general solution is $\phi(x) = A \sin(kx) + B \cos(kx)$, where $k = \sqrt{2mE}/\hbar$.

**2. Apply boundary conditions.** The wavefunction must be zero at the boundaries because the potential is infinite.
- Condition $\phi(0) = 0$: $\phi(0) = A \sin(0) + B \cos(0) = B = 0$. So $B=0$ and $\phi(x) = A \sin(kx)$.
- Condition $\phi(L) = 0$: $\phi(L) = A \sin(kL) = 0$. Since $A \neq 0$, we require $\sin(kL)=0$, which means $kL = n\pi$ for $n = 1, 2, 3, \dots$. The quantum number $n$ starts at 1; $n=0$ gives the trivial solution $\phi(x)=0$, which is not a valid wavefunction.

**3. Normalize and find energies.** The wave number is quantized: $k_n = \frac{n\pi}{L}$. The constant $A$ is found by normalization:
$$
\int_0^L |\phi_n(x)|^2 dx = |A|^2 \int_0^L \sin^2\left(\frac{n\pi x}{L}\right) dx = |A|^2 \cdot \frac{L}{2} = 1
$$
Thus, $A = \sqrt{\frac{2}{L}}$ (choosing the positive real phase). The normalized eigenfunctions are:
$$
\boxed{\phi_n(x) = \sqrt{\frac{2}{L}} \sin\left(\frac{n\pi x}{L}\right)}
$$
The corresponding energies come from $E = \frac{\hbar^2 k^2}{2m}$:
$$
\boxed{E_n = \frac{n^2 \pi^2 \hbar^2}{2m L^2}}
$$

### (b) Normalization of the Initial State

The initial state is $\psi_0(x) = A[\phi_1(x) + \phi_2(x)]$. To find $A$, we impose normalization $\int_0^L |\psi_0(x)|^2 dx = 1$.

Since the $\phi_n$ are orthonormal ($\int \phi_m \phi_n dx = \delta_{mn}$), the integral becomes:
$$
\int_0^L |A|^2 [\phi_1(x) + \phi_2(x)]^* [\phi_1(x) + \phi_2(x)] dx = |A|^2 \left( \int \phi_1^2 dx + \int \phi_2^2 dx + 2\int \phi_1 \phi_2 dx \right)
$$
The cross term $\int \phi_1 \phi_2 dx = 0$ due to orthogonality, and each $\int \phi_n^2 dx = 1$ due to normalization. Therefore:
$$
|A|^2 (1 + 1) = 2|A|^2 = 1
$$
So the normalization constant is $\boxed{A = \frac{1}{\sqrt{2}}}$ (choosing the positive real root).

### (c) Probability at $t = \tau$

**1. Write the time-evolved state.** The time evolution of an energy eigenstate is $\phi_n(x,t) = \phi_n(x) e^{-iE_n t/\hbar}$. Our initial state is $\psi_0(x) = \frac{1}{\sqrt{2}}[\phi_1(x) + \phi_2(x)]$. The state at time $t$ is:
$$
\psi(x,t) = \frac{1}{\sqrt{2}} \left[ \phi_1(x) e^{-iE_1 t/\hbar} + \phi_2(x) e^{-iE_2 t/\hbar} \right]
$$
Given $E_n = n^2 E_1$, we have $E_2 = 4E_1$. Substituting:
$$
\psi(x,t) = \frac{1}{\sqrt{2}} \left[ \phi_1(x) e^{-iE_1 t/\hbar} + \phi_2(x) e^{-i 4E_1 t/\hbar} \right]
$$

**2. Evaluate at $t = \tau = \frac{\pi\hbar}{E_1}$.** Plug in $t = \tau$:
- Phase for $\phi_1$: $e^{-iE_1 \tau/\hbar} = e^{-iE_1 \cdot (\pi\hbar/E_1)/\hbar} = e^{-i\pi} = -1$
- Phase for $\phi_2$: $e^{-i 4E_1 \tau/\hbar} = e^{-i 4E_1 \cdot (\pi\hbar/E_1)/\hbar} = e^{-i 4\pi} = 1$
Therefore, the wavefunction at $t=\tau$ is:
$$
\psi(x,\tau) = \frac{1}{\sqrt{2}} \left[ -\phi_1(x) + \phi_2(x) \right]
$$
This is essentially the initial state but with a relative minus sign. This phenomenon is known as a *revival*, where the wavefunction returns to a form very close to its initial state .

**3. Calculate the probability in $(0, L/2)$.** The probability is:
$$
P = \int_0^{L/2} |\psi(x,\tau)|^2 dx = \frac{1}{2} \int_0^{L/2} | -\phi_1(x) + \phi_2(x) |^2 dx
$$
$$
P = \frac{1}{2} \int_0^{L/2} \left[ \phi_1^2(x) + \phi_2^2(x) - 2\phi_1(x)\phi_2(x) \right] dx
$$
Substitute $\phi_n(x) = \sqrt{\frac{2}{L}} \sin\left(\frac{n\pi x}{L}\right)$:
$$
P = \frac{1}{2} \cdot \frac{2}{L} \int_0^{L/2} \left[ \sin^2\left(\frac{\pi x}{L}\right) + \sin^2\left(\frac{2\pi x}{L}\right) - 2 \sin\left(\frac{\pi x}{L}\right) \sin\left(\frac{2\pi x}{L}\right) \right] dx
$$
$$
P = \frac{1}{L} \left[ I_1 + I_2 - 2I_3 \right]
$$

**4. Evaluate the integrals.** Use the given formulas, with $y = x/L$ so $dx = L dy$ and the limits become $0$ to $1/2$.
- For $I_1 = \int_0^{L/2} \sin^2\left(\frac{\pi x}{L}\right) dx = L \int_0^{1/2} \sin^2(\pi y) dy$.
Using $\int \sin^2 y\, dy = \frac{y}{2} - \frac{1}{4}\sin 2y$:
$$
I_1 = L \left[ \frac{y}{2} - \frac{\sin(2\pi y)}{4\pi} \right]_0^{1/2} = L \left[ \left(\frac{1}{4} - \frac{\sin \pi}{4\pi}\right) - 0 \right] = \frac{L}{4}
$$

- For $I_2 = \int_0^{L/2} \sin^2\left(\frac{2\pi x}{L}\right) dx = L \int_0^{1/2} \sin^2(2\pi y) dy$.
$$
I_2 = L \left[ \frac{y}{2} - \frac{\sin(4\pi y)}{8\pi} \right]_0^{1/2} = L \left[ \left(\frac{1}{4} - \frac{\sin(2\pi)}{8\pi}\right) - 0 \right] = \frac{L}{4}
$$

- For $I_3 = \int_0^{L/2} \sin\left(\frac{\pi x}{L}\right) \sin\left(\frac{2\pi x}{L}\right) dx = L \int_0^{1/2} \sin(\pi y) \sin(2\pi y) dy$.
Use the given formula $\int \sin \alpha y \sin \beta y \, dy$ with $\alpha = \pi$, $\beta = 2\pi$ (so $\alpha - \beta = -\pi$, $\alpha + \beta = 3\pi$).
$$
\int \sin(\pi y) \sin(2\pi y) dy = \frac{\sin[(-\pi) y]}{2(-\pi)} - \frac{\sin[(3\pi) y]}{2(3\pi)} = -\frac{\sin(\pi y)}{2\pi} - \frac{\sin(3\pi y)}{6\pi}
$$
Evaluate from $0$ to $1/2$:
$$
I_3 = L \left[ -\frac{\sin(\pi y)}{2\pi} - \frac{\sin(3\pi y)}{6\pi} \right]_0^{1/2}
$$
At $y=1/2$: $\sin(\pi/2)=1$, $\sin(3\pi/2) = -1$. So the term is $-\frac{1}{2\pi} - \frac{(-1)}{6\pi} = -\frac{1}{2\pi} + \frac{1}{6\pi} = -\frac{1}{3\pi}$.
At $y=0$: $\sin(0)=0$, so the term is 0.
Therefore, $I_3 = L \left( -\frac{1}{3\pi} - 0 \right) = -\frac{L}{3\pi}$.

**5. Combine the results.**
$$
P = \frac{1}{L} \left[ \frac{L}{4} + \frac{L}{4} - 2\left( -\frac{L}{3\pi} \right) \right] = \frac{1}{L} \left[ \frac{L}{2} + \frac{2L}{3\pi} \right] = \frac{1}{2} + \frac{2}{3\pi}
$$
$$
\boxed{P = \frac{1}{2} + \frac{2}{3\pi}}
$$

---
---
# Respuestas taller 6 fisica fundamental 5 V

## **Problema 27**

Sean $\hat{A}$ y $\hat{B}$ dos observables compatibles, es decir, $[\hat{A},\hat{B}]=0$. Esto implica que sus proyectores espectrales también conmutan. Denotemos por $P_n$ el proyector sobre el autoespacio de $\hat{A}$ con autovalor $a_n$, y por $Q_m$ el proyector sobre el autoespacio de $\hat{B}$ con autovalor $b_m$. Entonces $[P_n, Q_m]=0$ para todo $n,m$.

La probabilidad de obtener $a_n$ en la primera medición y luego $b_m$ en la segunda, partiendo de un estado normalizado $|\psi\rangle$, es
$$
\mathcal{P}(a_n, b_m) = \|Q_m P_n |\psi\rangle\|^2 = \langle\psi|P_n Q_m P_n|\psi\rangle.
$$
Análogamente,
$$
\mathcal{P}(b_m, a_n) = \|P_n Q_m |\psi\rangle\|^2 = \langle\psi|Q_m P_n Q_m|\psi\rangle.
$$
Como $P_n$ y $Q_m$ conmutan, se tiene $P_n Q_m = Q_m P_n$, y además son proyectores ($P_n^2=P_n$, etc.). Entonces
$$
\|Q_m P_n |\psi\rangle\|^2 = \langle\psi|P_n Q_m Q_m P_n|\psi\rangle = \langle\psi|P_n Q_m P_n|\psi\rangle,
$$
$$
\|P_n Q_m |\psi\rangle\|^2 = \langle\psi|Q_m P_n P_n Q_m|\psi\rangle = \langle\psi|Q_m P_n Q_m|\psi\rangle = \langle\psi|P_n Q_m P_n|\psi\rangle,
$$
donde en el último paso se usó nuevamente la conmutación. Por lo tanto,
$$
\mathcal{P}(a_n, b_m) = \mathcal{P}(b_m, a_n).
$$

El estado final después de medir primero $\hat{A}$ y luego $\hat{B}$ es, salvo normalización,
$$
|\psi_{nm}\rangle \propto Q_m P_n |\psi\rangle.
$$
Si se invierte el orden, el estado final es
$$
|\psi_{mn}\rangle \propto P_n Q_m |\psi\rangle.
$$
Como $P_n Q_m = Q_m P_n$, ambos son proporcionales al mismo vector, y al normalizarlos obtenemos el mismo estado (las fases pueden diferir, pero el estado físico es el mismo). Luego $|\psi_{nm}\rangle = |\psi_{mn}\rangle$.

---

## **Problema 28**

#### (a) Hermiticidad
Los operadores están dados en la base ortonormal $\{|\varphi_1\rangle,|\varphi_2\rangle,|\varphi_3\rangle\}$.  
$\hat{H}_0 = \hbar\omega_0(|\varphi_1\rangle\langle\varphi_1| - |\varphi_2\rangle\langle\varphi_2| - |\varphi_3\rangle\langle\varphi_3|)$ es diagonal con coeficientes reales, por tanto $\hat{H}_0^\dagger = \hat{H}_0$.  
$\hat{A} = a(|\varphi_1\rangle\langle\varphi_1| + |\varphi_2\rangle\langle\varphi_3| + |\varphi_3\rangle\langle\varphi_2|)$ con $a\in\mathbb{R}$. Los términos $|\varphi_2\rangle\langle\varphi_3|$ y $|\varphi_3\rangle\langle\varphi_2|$ son conjugados entre sí, y $|\varphi_1\rangle\langle\varphi_1|$ es autoadjunto. Luego $\hat{A}^\dagger = \hat{A}$. Ambos son hermíticos.

#### (b) Representación matricial
En la base $\{|\varphi_1\rangle,|\varphi_2\rangle,|\varphi_3\rangle\}$ (en ese orden):
$$
\hat{H}_0 = \begin{pmatrix}
\hbar\omega_0 & 0 & 0 \\
0 & -\hbar\omega_0 & 0 \\
0 & 0 & -\hbar\omega_0
\end{pmatrix}, \qquad
\hat{A} = \begin{pmatrix}
a & 0 & 0 \\
0 & 0 & a \\
0 & a & 0
\end{pmatrix}.
$$

#### (c) Autovalores y autovectores de $\hat{H} = \hat{H}_0 + \hat{A}$
Sumando:
$$
\hat{H} = \begin{pmatrix}
\hbar\omega_0 + a & 0 & 0 \\
0 & -\hbar\omega_0 & a \\
0 & a & -\hbar\omega_0
\end{pmatrix}.
$$
Es diagonal por bloques. El bloque $1\times1$ da el autovalor $E_1 = \hbar\omega_0 + a$ con autovector $|\varphi_1\rangle$.  
El bloque $2\times2$:
$$
M = \begin{pmatrix}
-\hbar\omega_0 & a \\
a & -\hbar\omega_0
\end{pmatrix}
$$
tiene autovalores $\lambda = -\hbar\omega_0 \pm a$. Sus autovectores:
- Para $\lambda = -\hbar\omega_0 - a$: $(1,-1)$ en la base $\{|\varphi_2\rangle,|\varphi_3\rangle\}$, es decir $\frac{1}{\sqrt{2}}(|\varphi_2\rangle - |\varphi_3\rangle)$.
- Para $\lambda = -\hbar\omega_0 + a$: $(1,1)$, es decir $\frac{1}{\sqrt{2}}(|\varphi_2\rangle + |\varphi_3\rangle)$.

Por tanto, los autovalores y autovectores de $\hat{H}$ son:
$$
\begin{aligned}
E_1 &= \hbar\omega_0 + a, & |\psi_1\rangle &= |\varphi_1\rangle,\\
E_2 &= -\hbar\omega_0 - a, & |\psi_2\rangle &= \frac{1}{\sqrt{2}}(|\varphi_2\rangle - |\varphi_3\rangle),\\
E_3 &= -\hbar\omega_0 + a, & |\psi_3\rangle &= \frac{1}{\sqrt{2}}(|\varphi_2\rangle + |\varphi_3\rangle).
\end{aligned}
$$

#### (d) Conmutación y base común
Calculamos el conmutador. Con las matrices:
$$
\hat{H}_0\hat{A} = \begin{pmatrix}
\hbar\omega_0 a & 0 & 0 \\
0 & 0 & -\hbar\omega_0 a \\
0 & -\hbar\omega_0 a & 0
\end{pmatrix}, \quad
\hat{A}\hat{H}_0 = \begin{pmatrix}
a\hbar\omega_0 & 0 & 0 \\
0 & 0 & -a\hbar\omega_0 \\
0 & -a\hbar\omega_0 & 0
\end{pmatrix},
$$
iguales, luego $[\hat{H}_0,\hat{A}]=0$.

Buscamos una base de autovectores comunes. $\hat{H}_0$ tiene autovalor $\hbar\omega_0$ para $|\varphi_1\rangle$ y autovalor $-\hbar\omega_0$ para cualquier combinación de $|\varphi_2\rangle,|\varphi_3\rangle$. $\hat{A}$ tiene autovalores $a$ (degenerado: $|\varphi_1\rangle$ y $\frac{1}{\sqrt{2}}(|\varphi_2\rangle+|\varphi_3\rangle)$) y $-a$ (no degenerado: $\frac{1}{\sqrt{2}}(|\varphi_2\rangle-|\varphi_3\rangle)$). Así, una base común es:
$$
\{ |\varphi_1\rangle,\; \frac{1}{\sqrt{2}}(|\varphi_2\rangle+|\varphi_3\rangle),\; \frac{1}{\sqrt{2}}(|\varphi_2\rangle-|\varphi_3\rangle) \}.
$$
Verificando:
- $|\varphi_1\rangle$: $\hat{H}_0$ da $\hbar\omega_0$, $\hat{A}$ da $a$.
- $\frac{1}{\sqrt{2}}(|\varphi_2\rangle+|\varphi_3\rangle)$: $\hat{H}_0$ da $-\hbar\omega_0$, $\hat{A}$ da $a$.
- $\frac{1}{\sqrt{2}}(|\varphi_2\rangle-|\varphi_3\rangle)$: $\hat{H}_0$ da $-\hbar\omega_0$, $\hat{A}$ da $-a$.

#### (e) ¿Cuáles conjuntos forman un CCOC?
Un conjunto de observables que conmutan forma un CCOC, [[Conjunto Completo de Observables que Conmutan (CCOC)]], si sus autovalores conjuntos etiquetan unívocamente cada estado de la base (no hay degeneración residual).

- $\{\hat{H}_0\}$: tiene autovalor $\hbar\omega_0$ (no degenerado) y $-\hbar\omega_0$ (doble degeneración). No es CCOC.
- $\{\hat{A}\}$: tiene autovalor $a$ (doble degeneración) y $-a$ (no degenerado). No es CCOC.
- $\{\hat{H}_0,\hat{A}\}$: Los pares de autovalores son:
  * $(\hbar\omega_0, a)$ → $|\varphi_1\rangle$
  * $(-\hbar\omega_0, a)$ → $\frac{1}{\sqrt{2}}(|\varphi_2\rangle+|\varphi_3\rangle)$
  * $(-\hbar\omega_0, -a)$ → $\frac{1}{\sqrt{2}}(|\varphi_2\rangle-|\varphi_3\rangle)$
  Cada par corresponde a un único estado (salvo fase). Por tanto, $\{\hat{H}_0,\hat{A}\}$ es un CCOC.
- $\{\hat{H}_0^2,\hat{A}\}$: $\hat{H}_0^2 = (\hbar\omega_0)^2 \hat{I}$ es proporcional a la identidad, no aporta información. El conjunto equivale a $\{\hat{A}\}$, que es degenerado. No es CCOC.

Solo $\{\hat{H}_0,\hat{A}\}$ forma un CCOC.

## **Problema 29 — Operador paridad**

#### (a) Hermiticidad y valores propios

El operador de paridad $\hat{\Pi}$ actúa sobre funciones de onda como $\hat{\Pi}\psi(x) = \psi(-x)$. Para demostrar que es hermítico, consideramos el producto escalar en $L^2(\mathbb{R})$:

$$
\langle \hat{\Pi}\phi | \psi \rangle = \int_{-\infty}^{\infty} (\hat{\Pi}\phi)^*(x) \psi(x) \, dx = \int_{-\infty}^{\infty} \phi^*(-x) \psi(x) \, dx.
$$

Realizamos el cambio de variable $y = -x$, de modo que $x = -y$, $dx = -dy$. Los límites de integración se invierten:

$$
\int_{-\infty}^{\infty} \phi^*(-x) \psi(x) \, dx = \int_{\infty}^{-\infty} \phi^*(y) \psi(-y) (-dy) = \int_{-\infty}^{\infty} \phi^*(y) \psi(-y) \, dy.
$$

Esta última expresión es precisamente $\langle \phi | \hat{\Pi}\psi \rangle$. Por lo tanto, $\hat{\Pi}^\dagger = \hat{\Pi}$, es decir, es hermítico.

Para encontrar los valores propios, notamos que aplicar $\hat{\Pi}$ dos veces devuelve la función original:

$$
\hat{\Pi}^2 \psi(x) = \hat{\Pi} \psi(-x) = \psi(x) \quad \Rightarrow \quad \hat{\Pi}^2 = \mathbb{I}.
$$

Si $\lambda$ es un valor propio de $\hat{\Pi}$, entonces $\lambda^2 = 1$, de donde $\lambda = \pm 1$. Estos son los únicos valores posibles, y son reales, como corresponde a un operador hermítico.

#### (b) Consecuencias de la conmutación con un hamiltoniano no degenerado

Supongamos que $\hat{\Pi}$ conmuta con el hamiltoniano $\hat{H}$, es decir, $[\hat{H}, \hat{\Pi}] = 0$. Además, $\hat{H}$ es no degenerado, lo que significa que cada autovalor de energía tiene un único autovector (salvo fase).

Sea $\psi$ un autovector de $\hat{H}$ con energía $E$: $\hat{H}\psi = E\psi$. Aplicando $\hat{\Pi}$ a ambos lados y usando la conmutación:

$$
\hat{H}(\hat{\Pi}\psi) = \hat{\Pi} \hat{H}\psi = E (\hat{\Pi}\psi).
$$

Por lo tanto, $\hat{\Pi}\psi$ también es un autovector de $\hat{H}$ con la misma energía $E$. Dado que el espectro es no degenerado, $\hat{\Pi}\psi$ debe ser proporcional a $\psi$:

$$
\hat{\Pi}\psi = \lambda \psi, \quad \text{con } \lambda \in \mathbb{C}.
$$

Pero como $\hat{\Pi}$ es hermítico y $\lambda$ es un valor propio, ya sabemos que $\lambda = \pm 1$. En consecuencia, toda autofunción de $\hat{H}$ tiene paridad definida: es par ($\lambda = 1$) o impar ($\lambda = -1$). Así, las funciones propias de $\hat{H}$ pertenecen a los subespacios propios de $\hat{\Pi}$.

---

### **Problema 30 — Pozo de potencial par**

#### (a) Paridad de las funciones propias

El potencial es par: $V(x)=V(-x)$. El operador de paridad $\hat{\Pi}$ definido por $\hat{\Pi}\psi(x)=\psi(-x)$ conmuta con el hamiltoniano $\hat{H}$, pues $\hat{H}$ depende de $x$ a través de $V(x)$ y del laplaciano, que es invariante ante $x\to -x$. Así, $[\hat{H},\hat{\Pi}]=0$.

Sea $\psi(x)$ una autofunción de $\hat{H}$ con energía $E$ (estado ligado). Entonces $\hat{\Pi}\psi(x)=\psi(-x)$ también es autofunción con la misma energía. En una dimensión, los estados ligados de un potencial regular son no degenerados, por lo que $\psi(-x)$ debe ser proporcional a $\psi(x)$:
$$
\psi(-x) = \lambda \psi(x).
$$
Aplicando $\hat{\Pi}$ nuevamente,
$$
\psi(x) = \lambda \psi(-x) = \lambda^2 \psi(x),
$$
de donde $\lambda^2=1$ y, por tanto, $\lambda=\pm 1$. Así, $\psi$ es par ($\lambda=1$) o impar ($\lambda=-1$).

#### (b) Existencia de al menos un estado ligado

El pozo tiene profundidad $V_0 = \frac{\hbar^2 k_0^2}{2m}$ con $k_0 = \sqrt{2m V_0}/\hbar$, y ancho $L$ centrado en el origen. Para estados ligados ($E<0$), definimos
$$
k = \sqrt{\frac{2m(V_0-|E|)}{\hbar^2}}, \quad \kappa = \sqrt{\frac{2m|E|}{\hbar^2}},
$$
de modo que $k^2+\kappa^2 = k_0^2$.

Buscamos soluciones pares (estado fundamental). En la región interior $|x|<L/2$, la función par es $\psi(x)=A\cos(kx)$; en el exterior $|x|>L/2$, $\psi(x)=B e^{-\kappa |x|}$. Las condiciones de continuidad de $\psi$ y su derivada en $x=L/2$ conducen a la ecuación
$$
k \tan\left(\frac{kL}{2}\right) = \kappa = \sqrt{k_0^2 - k^2}.
$$
Para $k=0$, el lado izquierdo es 0 y el derecho es $k_0>0$. Para $k\to k_0$, el lado derecho tiende a 0, mientras que el izquierdo crece sin límite cuando $kL/2\to \pi/2$ (si $k_0L/2 < \pi/2$ aún se alcanza un valor finito). En cualquier caso, la función $f(k)=k\tan(kL/2)$ es continua y creciente en $(0, \pi/L)$ (o hasta donde $kL/2<\pi/2$), y $g(k)=\sqrt{k_0^2-k^2}$ es decreciente de $k_0$ a 0. Por el teorema del valor intermedio, existe al menos un $k\in(0,k_0)$ que satisface la ecuación. Esto garantiza un estado ligado par, y por tanto existe al menos un estado ligado.

#### (c) Estimación del número de estados ligados para $V_0 \gg \frac{\hbar^2}{mL^2}$

En el límite de pozo profundo, $k_0 L \gg 1$. Los estados ligados se aproximan a los de un pozo infinito de ancho $L$, cuyos números de onda son $k_n = n\pi/L$ con $n=1,2,3,\ldots$ (los impares corresponden a funciones pares y los pares a impares). La condición de ligadura es $k_n < k_0$, es decir,
$$
\frac{n\pi}{L} < k_0 = \sqrt{\frac{2m V_0}{\hbar^2}} \quad \Rightarrow \quad n < \frac{L}{\pi}\sqrt{\frac{2m V_0}{\hbar^2}}.
$$
Por lo tanto, el número de estados ligados $N$ es aproximadamente el mayor entero menor que ese valor, es decir,
$$
N \approx \left\lfloor \frac{L}{\pi}\sqrt{\frac{2m V_0}{\hbar^2}} \right\rfloor.
$$
En el límite de gran profundidad, esto equivale a
$$
N \approx \frac{L}{\pi}\sqrt{\frac{2m V_0}{\hbar^2}} \quad \text{con un error de } \pm 1.
$$