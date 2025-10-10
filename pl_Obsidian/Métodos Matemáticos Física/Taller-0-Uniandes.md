# Preguntas
---

Voy a resolver cada problema paso a paso, explicando los conceptos clave y los prerrequisitos necesarios.

---

## **1. Álgebra Básica de Números Complejos**

### **1.1. Funciones trigonométricas**

#### **a) Demostrar:**
$$
\coth(z/2) = \frac{\sinh x - i \sin y}{\cosh x - \cos y}, \quad z = x + iy
$$

**Conceptos clave:**  
- Definiciones de funciones hiperbólicas y trigonométricas en términos de exponenciales.  
- Relaciones entre funciones hiperbólicas y trigonométricas para argumentos complejos.  

**Prerrequisitos:**  
- $\coth w = \frac{\cosh w}{\sinh w}$  
- $\sinh(iy) = i \sin y$, $\cosh(iy) = \cos y$  
- Identidades: $e^{z} = e^x (\cos y + i \sin y)$  

**Demostración:**  
Partimos de la definición:  
$$
\coth(z/2) = \frac{e^{z} + 1}{e^{z} - 1}
$$
Sustituyendo $e^{z} = e^x (\cos y + i \sin y)$:  
$$
\coth(z/2) = \frac{e^x \cos y + 1 + i e^x \sin y}{e^x \cos y - 1 + i e^x \sin y}
$$
Multiplicamos numerador y denominador por el conjugado del denominador:  
$$
\text{Denominador: } (e^x \cos y - 1)^2 + (e^x \sin y)^2 = e^{2x} - 2 e^x \cos y + 1 = 2 e^x (\cosh x - \cos y)
$$
$$
\text{Numerador: } (e^{2x} - 1) - 2 i e^x \sin y = 2 e^x (\sinh x - i \sin y)
$$
Por lo tanto:  
$$
\coth(z/2) = \frac{\sinh x - i \sin y}{\cosh x - \cos y}
$$

---

#### **b) Demostrar:**
$$
\arcsin z = -i \ln(i z \pm \sqrt{1 - z^2})
$$

**Conceptos clave:**  
- Función inversa de seno en complejos.  
- Uso del logaritmo complejo.  

**Prerrequisitos:**  
- $\sin w = \frac{e^{i w} - e^{-i w}}{2i}$  
- Resolución de ecuaciones exponenciales.  

**Demostración:**  
Sea $w = \arcsin z$, entonces $z = \sin w = \frac{e^{i w} - e^{-i w}}{2i}$.  
Multiplicando por $2i$:  
$$
2 i z = e^{i w} - e^{-i w}
$$
Sea $u = e^{i w}$, entonces:  
$$
2 i z = u - \frac{1}{u} \implies u^2 - 2 i z u - 1 = 0
$$
Resolviendo la cuadrática:  
$$
u = i z \pm \sqrt{1 - z^2}
$$
Luego:  
$$
e^{i w} = i z \pm \sqrt{1 - z^2} \implies w = -i \ln(i z \pm \sqrt{1 - z^2})
$$

---

#### **c) Demostrar:**
$$
|\sin z|^2 = \sin^2 x + \sinh^2 y
$$

**Conceptos clave:**  
- Módulo de una función compleja.  
- Partes real e imaginaria de $\sin z$.  

**Prerrequisitos:**  
- $\sin z = \sin x \cosh y + i \cos x \sinh y$  
- $|a + i b|^2 = a^2 + b^2$  

**Demostración:**  
Usando la expresión de $\sin z$:  
$$
|\sin z|^2 = (\sin x \cosh y)^2 + (\cos x \sinh y)^2
$$
Sustituyendo $\cosh^2 y = 1 + \sinh^2 y$:  
$$
|\sin z|^2 = \sin^2 x (1 + \sinh^2 y) + \cos^2 x \sinh^2 y = \sin^2 x + \sinh^2 y
$$

---

### **1.2. Condiciones de Cauchy-Riemann**

#### **a) Encontrar $w(x,y)$ si $u(x,y) = e^{-y} \cos x$**

**Conceptos clave:**  
- Ecuaciones de Cauchy-Riemann: $u_x = v_y$, $u_y = -v_x$  
- Construcción de una función analítica a partir de su parte real.  

**Prerrequisitos:**  
- Derivadas parciales de $u$.  
- Integración para encontrar $v$.  

**Solución:**  
Calculamos:  
$$
u_x = -e^{-y} \sin x, \quad u_y = -e^{-y} \cos x
$$
Por Cauchy-Riemann:  
$$
v_y = u_x = -e^{-y} \sin x, \quad v_x = -u_y = e^{-y} \cos x
$$
Integrando $v_x$ respecto a $x$:  
$$
v = e^{-y} \sin x + g(y)
$$
Derivando respecto a $y$:  
$$
v_y = -e^{-y} \sin x + g'(y) = -e^{-y} \sin x \implies g'(y) = 0
$$
Luego $v = e^{-y} \sin x$, y:  
$$
w(z) = u + i v = e^{-y} (\cos x + i \sin x) = e^{i z}
$$

---

#### **b) Encontrar $w(x,y)$ si $v(x,y) = 3x^2 y - y^3$**

**Solución:**  
Calculamos:  
$$
v_x = 6 x y, \quad v_y = 3x^2 - 3 y^2
$$
Por Cauchy-Riemann:  
$$
u_x = v_y = 3x^2 - 3 y^2, \quad u_y = -v_x = -6 x y
$$
Integrando $u_x$ respecto a $x$:  
$$
u = x^3 - 3 x y^2 + f(y)
$$
Derivando respecto a $y$:  
$$
u_y = -6 x y + f'(y) = -6 x y \implies f'(y) = 0
$$
Luego $u = x^3 - 3 x y^2$, y:  
$$
w(z) = u + i v = (x^3 - 3 x y^2) + i (3x^2 y - y^3) = z^3
$$

---

#### **c) Mostrar que $f(z) = z^{-2}$ es analítica**

**Conceptos clave:**  
- Derivabilidad en el plano complejo.  

**Prerrequisitos:**  
- Reglas de derivación.  

**Solución:**  
$f(z) = 1/z^2$ es derivable en $\mathbb{C} \setminus \{0\}$ con derivada $f'(z) = -2/z^3$. Por lo tanto, es analítica en $\mathbb{C} \setminus \{0\}$.

---

## **2. Integral polinómica**

Calcular:  
$$
I = \int_0^\infty \frac{dx}{x^4 + 1}
$$

**Conceptos clave:**  
- Integrales reales usando residuos.  
- Contorno en el plano complejo.  

**Prerrequisitos:**  
- Teorema de los residuos.  
- Lema de Jordan.  

**Solución:**  
Consideramos la integral compleja:  
$$
\int_C \frac{dz}{z^4 + 1}
$$
donde $C$ es el contorno que incluye el eje real y un semicírculo superior. Los polos en el semiplano superior son:  
$$
z_0 = e^{i \pi/4}, \quad z_1 = e^{i 3\pi/4}
$$
Residuos:  
$$
\text{Res}(z_0) = \frac{1}{4 z_0^3} = -\frac{\sqrt{2}}{8}(1 + i), \quad \text{Res}(z_1) = \frac{1}{4 z_1^3} = \frac{\sqrt{2}}{8}(1 - i)
$$
Suma de residuos:  
$$
\text{Res}(z_0) + \text{Res}(z_1) = -i \frac{\sqrt{2}}{4}
$$
Por el teorema de los residuos:  
$$
\int_C f(z) \, dz = 2\pi i \left(-i \frac{\sqrt{2}}{4}\right) = \frac{\pi \sqrt{2}}{2}
$$
La integral sobre el semicírculo tiende a cero, y por simetría:  
$$
\int_0^\infty \frac{dx}{x^4 + 1} = \frac{1}{2} \int_{-\infty}^\infty \frac{dx}{x^4 + 1} = \frac{\pi \sqrt{2}}{4}
$$

---

## **3. Integral trigonométrica, círculo unitario**

Evaluar:  
$$
I = \int_0^{2\pi} \frac{d\theta}{(a + \cos \theta)^2}, \quad |a| > 1
$$

**Conceptos clave:**  
- Sustitución $z = e^{i \theta}$.  
- Teorema de los residuos.  

**Prerrequisitos:**  
- $\cos \theta = \frac{z + z^{-1}}{2}$, $d\theta = \frac{dz}{i z}$  

**Solución:**  
Sustituyendo:  
$$
I = \frac{4}{i} \oint_{|z|=1} \frac{z}{(z^2 + 2 a z + 1)^2} \, dz
$$
Los polos son las raíces de $z^2 + 2 a z + 1 = 0$:  
$$
\alpha = -a + \sqrt{a^2 - 1}, \quad \beta = -a - \sqrt{a^2 - 1}
$$
Para $|a| > 1$, solo $\alpha$ está dentro del círculo unitario. Es un polo doble.  
Residuo en $z = \alpha$:  
$$
\text{Res} = \frac{a}{4 (a^2 - 1)^{3/2}}
$$
Entonces:  
$$
I = \frac{4}{i} \cdot 2\pi i \cdot \text{Res} = \frac{2\pi a}{(a^2 - 1)^{3/2}}
$$
**Si $|a| < 1$:** Los polos están sobre el círculo unitario y la integral diverge.

---

## **4. Dispersión en Mecánica Cuántica**

Consideramos:  
$$
I = \int_{-\infty}^{\infty} \frac{\sin t}{t} e^{i p t} \, dt, \quad p > 0
$$

#### **(a) Descomposición:**
$$
\sin t = \frac{e^{i t} - e^{-i t}}{2i} \implies I = \frac{1}{2i} \left[ \int \frac{e^{i (p+1) t}}{t} \, dt - \int \frac{e^{i (p-1) t}}{t} \, dt \right]
$$

#### **(b) Contorno:**  
Cada integral es del tipo $\int \frac{e^{i k t}}{t} \, dt$. Para $k > 0$, se cierra el contorno en el semiplano superior; para $k < 0$, en el inferior.

#### **(c) $p > 1$:**
Ambas $k_1 = p+1 > 0$, $k_2 = p-1 > 0$:  
$$
\int \frac{e^{i k_1 t}}{t} \, dt = i \pi, \quad \int \frac{e^{i k_2 t}}{t} \, dt = i \pi \implies I = 0
$$

#### **(d) $p < 1$:**
$k_1 > 0$, $k_2 < 0$:  
$$
\int \frac{e^{i k_1 t}}{t} \, dt = i \pi, \quad \int \frac{e^{i k_2 t}}{t} \, dt = -i \pi \implies I = \pi
$$

#### **(e) $p = 1$:**
$k_1 = 2 > 0$, $k_2 = 0$:  
$$
\int \frac{e^{i k_1 t}}{t} \, dt = i \pi, \quad \int \frac{1}{t} \, dt = 0 \implies I = \frac{\pi}{2}
$$

#### **(f) $p < 0$:**
Por simetría, $I(p) = I(|p|)$.

---

## **5. Integral con Lemma de Jordan**

Evaluar:  
$$
I = \int_{-\infty}^{\infty} \frac{x^2 \cos(m x)}{(x^2 + 1)^2} \, dx, \quad m \in \mathbb{R}
$$

**Conceptos clave:**  
- Integrales con coseno usando parte real de exponencial compleja.  
- Teorema de los residuos.  

**Prerrequisitos:**  
- $\cos(m x) = \text{Re}(e^{i m x})$  
- Contorno en el semiplano superior.  

**Solución:**  
Consideramos:  
$$
J = \int_{-\infty}^{\infty} \frac{x^2 e^{i m x}}{(x^2 + 1)^2} \, dx \implies I = \text{Re}(J)
$$
Polos en $z = \pm i$ (orden 2). Para $m > 0$, cerramos en el semiplano superior.  
Residuo en $z = i$:  
$$
\text{Res} = \frac{i e^{-m} (m - 1)}{4}
$$
Entonces:  
$$
J = 2\pi i \cdot \text{Res} = -\frac{\pi e^{-m} (m - 1)}{2}
$$
Luego:  
$$
I = \text{Re}(J) = \frac{\pi}{2} e^{-|m|} (1 - |m|)
$$

---

## **Respuestas finales:**

1.1. Demostrado.  
1.2. (a) $(z) = e^{i z}$ (b) $w(z) = z^3$, (c) $f(z) = z^{-2}$ es analítica en $\mathbb{C} \setminus \{0\}$.  
2. $I = \frac{\pi \sqrt{2}}{4}$.  
3. $I = \frac{2\pi a}{(a^2 - 1)^{3/2}}$ para $|a| > 1$; diverge para $|a| < 1$.  
4. $I = 0$ para $p > 1$, $I = \pi$ para $p < 1$, $I = \frac{\pi}{2}$ para $p = 1$. Para $p < 0$, $I(p) = I(|p|)$.  
5. $I = \frac{\pi}{2} e^{-|m|} (1 - |m|)$.

---