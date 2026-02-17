
### **Problema 21: Espacios de Hilbert**

**Objetivo:** Repasar definiciones y propiedades fundamentales.

Este es un ejercicio conceptual. Para trabajar en Mecánica Cuántica (MC), no basta con saber cálculo; necesitamos entender dónde "viven" nuestros vectores de estado.

#### 1. Definición de Espacio de Hilbert ($\mathcal{H}$)

Un espacio de Hilbert es un **espacio vectorial** sobre el cuerpo de los complejos $\mathbb{C}$ que cumple dos condiciones adicionales cruciales:

1. **Producto Interno:** Está dotado de un producto interno $\langle \phi | \psi \rangle$ que es:
    
    - Lineal en el segundo argumento (ket): $\langle \phi | (a|\psi_1\rangle + b|\psi_2\rangle) = a\langle \phi | \psi_1 \rangle + b\langle \phi | \psi_2 \rangle$.
        
    - Antilineal en el primer argumento (bra): $\langle a\phi | \psi \rangle = a^* \langle \phi | \psi \rangle$.
        
    - Definido positivo: $\langle \psi | \psi \rangle \ge 0$, siendo 0 si y solo si $|\psi\rangle = 0$.
        
2. **Completitud:** Es un espacio métrico **completo**. Esto significa que toda _sucesión de Cauchy_ de vectores en $\mathcal{H}$ converge a un límite que también está dentro de $\mathcal{H}$.
    
    - _Argumento físico:_ Esto es vital para asegurar que las superposiciones infinitas (series) de estados cuánticos (como la serie de Fourier en el pozo infinito) resulten en un estado físico válido.
        

#### 2. El Espacio Dual ($\mathcal{H}^*$)

Para cada vector ket $|\psi\rangle \in \mathcal{H}$, existe un funcional lineal único (llamado bra $\langle \psi |$) que actúa sobre $\mathcal{H}$ y devuelve un número complejo.

- La correspondencia $|\psi\rangle \leftrightarrow \langle \psi |$ es antilineal.
    
- Esto se formaliza mediante el **Teorema de Representación de Riesz**.
    

#### 3. Operadores en $\mathcal{H}$

Un operador lineal $\hat{A}$ mapea vectores de $\mathcal{H}$ en vectores de $\mathcal{H}$.

- **Adjunto ($\hat{A}^\dagger$):** Se define tal que $\langle \phi | \hat{A} \psi \rangle = \langle \hat{A}^\dagger \phi | \psi \rangle$.
    
- **Hermítico (Auto-adjunto):** $\hat{A} = \hat{A}^\dagger$. Fundamental en física porque sus valores propios son reales (observables).
    
- **Unitario:** $\hat{U}^\dagger \hat{U} = \hat{I}$. Preserva el producto interno (conserva probabilidades).
    

---

### **Problema 22: Función de onda en momento**

**Enunciado:** $\psi(x) = N e^{-|x|}$.

#### (a) Constante de normalización $N$

**Prerrequisito:** La interpretación probabilística de Born exige $\int_{-\infty}^{\infty} |\psi(x)|^2 dx = 1$.

**Cálculo:**

$$\int_{-\infty}^{\infty} |N e^{-|x|}|^2 dx = |N|^2 \int_{-\infty}^{\infty} e^{-2|x|} dx = 1$$

Como la función es par (simétrica respecto a $x=0$), integramos de 0 a $\infty$ y multiplicamos por 2:

$$|N|^2 \cdot 2 \int_{0}^{\infty} e^{-2x} dx = 1$$

La integral es elemental: $\int_0^\infty e^{-ax} dx = \frac{1}{a}$. Aquí $a=2$.

$$|N|^2 \cdot 2 \left( \frac{1}{2} \right) = 1 \implies |N|^2 = 1$$

Podemos elegir la fase real positiva:

$$N = 1$$

Por tanto, el estado normalizado es $\psi(x) = e^{-|x|}$.

---

#### (b) Coeficientes de expansión en ondas planas

**Concepto:** Las "ondas planas" son las funciones propias del operador momento $\hat{p}$. En la representación de posición, se escriben como:

$$\langle x | k \rangle = \frac{1}{\sqrt{2\pi}} e^{ikx} \quad \text{(usando } k \text{)} \quad \text{o} \quad \langle x | p \rangle = \frac{1}{\sqrt{2\pi\hbar}} e^{ipx/\hbar}$$

Expandir $\psi(x)$ en ondas planas es, por definición, encontrar la Transformada de Fourier. Los "coeficientes de expansión" son precisamente los valores de la función de onda en el espacio recíproco (k o p).

Usaremos la variable $k$ para los coeficientes matemáticos puros (como suele pedirse en expansiones de Fourier estándar):

$$\tilde{\psi}(k) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} \psi(x) e^{-ikx} dx$$

**Cálculo:**

$$\tilde{\psi}(k) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-|x|} e^{-ikx} dx$$

Partimos la integral en $(-\infty, 0)$ y $(0, \infty)$:

1. **$x < 0$:** $|x| = -x$. El término es $e^x e^{-ikx} = e^{(1-ik)x}$.
    
    $$\int_{-\infty}^0 e^{(1-ik)x} dx = \left[ \frac{e^{(1-ik)x}}{1-ik} \right]_{-\infty}^0 = \frac{1}{1-ik} - 0$$
    
2. **$x > 0$:** $|x| = x$. El término es $e^{-x} e^{-ikx} = e^{-(1+ik)x}$.
    
    $$\int_0^{\infty} e^{-(1+ik)x} dx = \left[ \frac{e^{-(1+ik)x}}{-(1+ik)} \right]_0^{\infty} = 0 - \frac{1}{-(1+ik)} = \frac{1}{1+ik}$$
    

Sumamos ambas partes:

$$\text{Integral Total} = \frac{1}{1-ik} + \frac{1}{1+ik} = \frac{(1+ik) + (1-ik)}{1 + k^2} = \frac{2}{1+k^2}$$

**Resultado (Coeficientes):**

$$\tilde{\psi}(k) = \sqrt{\frac{2}{\pi}} \frac{1}{1+k^2}$$

Esta función es una **Lorentziana** (o distribución de Cauchy).

---

#### (c) Representación de momento $\overline{\psi}(p)$

**Concepto:** Es exactamente lo mismo que el punto (b), pero usando la variable física $p = \hbar k$. La normalización cambia ligeramente para mantener la consistencia física ($\int |\overline{\psi}(p)|^2 dp = 1$).

Definición simétrica de la TF en Mecánica Cuántica:

$$\overline{\psi}(p) = \langle p | \psi \rangle = \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^{\infty} e^{-ipx/\hbar} \psi(x) dx$$

**Cálculo:**

Podemos tomar el resultado de (b) y sustituir $k = p/\hbar$. Además, ajustamos el prefactor de normalización.

El resultado de la integral fue $\frac{2}{1+(p/\hbar)^2} = \frac{2\hbar^2}{\hbar^2 + p^2}$.

Ahora aplicamos el prefactor $\frac{1}{\sqrt{2\pi\hbar}}$:

$$\overline{\psi}(p) = \frac{1}{\sqrt{2\pi\hbar}} \cdot \frac{2\hbar^2}{\hbar^2 + p^2}$$

$$\overline{\psi}(p) = \sqrt{\frac{2}{\pi\hbar}} \frac{\hbar^2}{p^2 + \hbar^2}$$

Este resultado nos dice que aunque la partícula está localizada alrededor de $x=0$ (decaimiento exponencial), tiene una dispersión de momento considerable (colas largas de la Lorentziana $\sim 1/p^2$).

---

### **Problema 23: Operadores $\hat{x}$ y $\hat{p}$**

**Contexto:** Trabajamos en el espacio $L^2(\mathbb{R})$ (funciones de onda de cuadrado integrable).

#### (a) Demostración de Hermiticidad

La condición de hermiticidad para un operador $\hat{A}$ es:

$$\langle \phi | \hat{A} \psi \rangle = \langle \psi | \hat{A} \phi \rangle^* \quad \iff \quad \int_{-\infty}^{\infty} \phi^*(x) (\hat{A}\psi(x)) dx = \left( \int_{-\infty}^{\infty} \psi^*(x) (\hat{A}\phi(x)) dx \right)^*$$

**1. Operador Posición ($\hat{x}$)**

En la representación de coordenadas, $\hat{x}$ actúa multiplicando por la variable real $x$.

$$\langle \phi | \hat{x} \psi \rangle = \int_{-\infty}^{\infty} \phi^*(x) x \psi(x) dx$$

Dado que $x$ es real ($x = x^*$), podemos reordenar:

$$= \int_{-\infty}^{\infty} (x \phi(x))^* \psi(x) dx = \langle \hat{x}\phi | \psi \rangle$$

Y por propiedad del producto interno $\langle A | B \rangle = \langle B | A \rangle^*$:

$$= \langle \psi | \hat{x} \phi \rangle^*$$

**Conclusión:** $\hat{x}$ es hermítico.

**2. Operador Momento ($\hat{p}$)**

Definición: $\hat{p} = -i\hbar \frac{d}{dx}$.

$$\langle \phi | \hat{p} \psi \rangle = \int_{-\infty}^{\infty} \phi^*(x) \left( -i\hbar \frac{d\psi}{dx} \right) dx$$

Sacamos las constantes:

$$= -i\hbar \int_{-\infty}^{\infty} \phi^*(x) \psi'(x) dx$$

**Integración por partes:**

Sea $u = \phi^*(x)$ y $dv = \psi'(x)dx$. Entonces $du = \frac{d\phi^*}{dx}dx$ y $v = \psi(x)$.

$$\int_{-\infty}^{\infty} \phi^* \psi' dx = \left[ \phi^*(x)\psi(x) \right]_{-\infty}^{\infty} - \int_{-\infty}^{\infty} \frac{d\phi^*}{dx} \psi(x) dx$$

_Argumento Físico:_ Como $\phi, \psi \in L^2(\mathbb{R})$, deben desvanecerse en el infinito ($\psi(\pm\infty) \to 0$). Por tanto, el término de frontera $[\dots]_{-\infty}^{\infty}$ es cero.

Regresando a la expresión:

$$\langle \phi | \hat{p} \psi \rangle = -i\hbar \left( 0 - \int_{-\infty}^{\infty} \frac{d\phi^*}{dx} \psi(x) dx \right) = i\hbar \int_{-\infty}^{\infty} \frac{d\phi^*}{dx} \psi(x) dx$$

Ahora, veamos el lado derecho de la definición de hermiticidad (conjugado del operador actuando sobre $\phi$):

$$\langle \psi | \hat{p} \phi \rangle^* = \left( \int_{-\infty}^{\infty} \psi^* (-i\hbar \frac{d\phi}{dx}) dx \right)^*$$

El conjugado afecta a $-i\hbar$ (cambiando a $+i\hbar$) y a las funciones:

$$= \int_{-\infty}^{\infty} \psi ( +i\hbar \frac{d\phi^*}{dx} ) dx = i\hbar \int_{-\infty}^{\infty} \psi(x) \frac{d\phi^*}{dx} dx$$

Comparando ambos resultados, son idénticos.

**Conclusión:** $\hat{p}$ es hermítico.

---

#### (b) Conmutador $[\hat{p}, \hat{x}]$

**Concepto:** El conmutador actúa sobre una función de prueba arbitraria $f(x)$. No se debe calcular "vacío".

$$[\hat{p}, \hat{x}] f(x) = (\hat{p}\hat{x} - \hat{x}\hat{p}) f(x)$$

**Paso a paso:**

1. **Término $\hat{p}\hat{x} f(x)$:**
    
    Primero aplica $\hat{x}$, luego $\hat{p}$.
    
    $$\hat{x} f(x) = x f(x)$$
    
    $$\hat{p} (x f(x)) = -i\hbar \frac{d}{dx} (x f(x))$$
    
    Regla del producto (Leibniz): $\frac{d}{dx}(xf) = 1\cdot f(x) + x \frac{df}{dx}$.
    
    $$\hat{p}\hat{x} f(x) = -i\hbar \left( f(x) + x \frac{df}{dx} \right) = -i\hbar f(x) - i\hbar x \frac{df}{dx}$$
    
2. **Término $\hat{x}\hat{p} f(x)$:**
    
    Primero aplica $\hat{p}$, luego $\hat{x}$.
    
    $$\hat{p} f(x) = -i\hbar \frac{df}{dx}$$
    
    $$\hat{x} (\hat{p} f(x)) = x \left( -i\hbar \frac{df}{dx} \right) = -i\hbar x \frac{df}{dx}$$
    
3. **Resta:**
    
    $$[\hat{p}, \hat{x}] f(x) = \left( -i\hbar f(x) - i\hbar x \frac{df}{dx} \right) - \left( -i\hbar x \frac{df}{dx} \right)$$
    
    Los términos con derivada se cancelan:
    
    $$= -i\hbar f(x)$$
    

**Resultado:**

Como esto es válido para cualquier $f(x)$, podemos escribir la identidad operatorial:

$$[\hat{p}, \hat{x}] = -i\hbar \hat{I}$$

(Nota: El orden inverso $[\hat{x}, \hat{p}] = i\hbar$ es la relación de conmutación canónica fundamental).