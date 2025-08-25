Vamos a resolver detalladamente los **Ejercicios 3 y 4** de variable compleja.

---

## **Ejercicio 3**

### **a)** Dado $u(x,y) = 2x(1 - y)$, determine la función armónica conjugada $v(x,y)$ tal que $f(z) = u + iv$ sea analítica.

#### **Paso 1: Verificar que $u$ es armónica**
Para que exista una función conjugada armónica $v$, $u$ debe ser armónica, es decir, debe satisfacer la ecuación de Laplace:

$$
\nabla^2 u = u_{xx} + u_{yy} = 0
$$

Calculemos:

$$
u(x,y) = 2x(1 - y) = 2x - 2xy
$$

$$
u_x = 2 - 2y, \quad u_{xx} = 0
$$
$$
u_y = -2x, \quad u_{yy} = 0
$$

$$
\Rightarrow u_{xx} + u_{yy} = 0 + 0 = 0
$$

Entonces $u$ es armónica. ✅

#### **Paso 2: Usar las ecuaciones de Cauchy-Riemann**

$$
u_x = v_y, \quad u_y = -v_x
$$

Sabemos:

$$
u_x = 2 - 2y \Rightarrow v_y = 2 - 2y
$$
$$
u_y = -2x \Rightarrow -v_x = -2x \Rightarrow v_x = 2x
$$

Ahora integramos para hallar $v$:

- De $v_x = 2x$, integramos respecto a $x$:

$$
v(x,y) = \int 2x \, dx = x^2 + g(y)
$$

- Ahora derivamos respecto a $y$:

$$
v_y = g'(y)
$$

Pero también $v_y = 2 - 2y$, así que:

$$
g'(y) = 2 - 2y \Rightarrow g(y) = \int (2 - 2y)\,dy = 2y - y^2 + C
$$

Entonces:

$$
v(x,y) = x^2 + 2y - y^2 + C
$$

La constante $C$ se puede tomar como 0 (porque las funciones conjugadas se definen salvo constante real).

**Respuesta a):**

$$
\boxed{v(x,y) = x^2 - y^2 + 2y}
$$

---

### **b)** Dado $v(x,y) = \sinh x \cos y$, obtenga $u(x,y)$

Nuevamente, buscamos $u(x,y)$ tal que $f = u + iv$ sea analítica.

#### **Paso 1: Verificar armonicidad de $v$**

$$
v(x,y) = \sinh x \cos y
$$

$$
v_x = \cosh x \cos y, \quad v_{xx} = \sinh x \cos y
$$
$$
v_y = -\sinh x \sin y, \quad v_{yy} = -\sinh x \cos y
$$

$$
v_{xx} + v_{yy} = \sinh x \cos y - \sinh x \cos y = 0
$$

Entonces $v$ es armónica. ✅

#### **Paso 2: Ecuaciones de Cauchy-Riemann**

$$
u_x = v_y, \quad u_y = -v_x
$$

Sabemos:

$$
v_y = -\sinh x \sin y \Rightarrow u_x = -\sinh x \sin y
$$
$$
v_x = \cosh x \cos y \Rightarrow u_y = -\cosh x \cos y
$$

Ahora integramos $u_x$ respecto a $x$:

$$
u(x,y) = \int -\sinh x \sin y \, dx = -\sin y \int \sinh x \, dx = -\sin y \cdot \cosh x + g(y)
$$

$$
\Rightarrow u(x,y) = -\cosh x \sin y + g(y)
$$

Derivamos respecto a $y$:

$$
u_y = -\cosh x \cos y + g'(y)
$$

Pero también $u_y = -\cosh x \cos y$, entonces:

$$
-\cosh x \cos y + g'(y) = -\cosh x \cos y \Rightarrow g'(y) = 0 \Rightarrow g(y) = C
$$

Tomamos $C = 0$.

**Respuesta b):**

$$
\boxed{u(x,y) = -\cosh x \sin y}
$$

---

## **Ejercicio 4**

### **a)** Evalúe $\int_C f(z)\,dz$ con $f(z) = z^m (\overline{z})^n$, $m, n \in \mathbb{Z}^+$, $C: |z| = R$, sentido positivo.

Sabemos que $z = Re^{i\theta}$, entonces $\overline{z} = R e^{-i\theta}$, y $dz = i R e^{i\theta} d\theta$

Sustituimos:

$$
z^m = R^m e^{i m \theta}, \quad (\overline{z})^n = R^n e^{-i n \theta}
$$

$$
f(z) = z^m (\overline{z})^n = R^{m+n} e^{i(m - n)\theta}
$$

$$
dz = i R e^{i\theta} d\theta
$$

Entonces:

$$
\int_C f(z)\,dz = \int_0^{2\pi} R^{m+n} e^{i(m - n)\theta} \cdot i R e^{i\theta} d\theta = i R^{m+n+1} \int_0^{2\pi} e^{i(m - n + 1)\theta} d\theta
$$

Ahora analicemos la integral:

$$
\int_0^{2\pi} e^{i k \theta} d\theta = 
\begin{cases}
2\pi & \text{si } k = 0 \\
0 & \text{si } k \ne 0
\end{cases}
$$

Aquí $k = m - n + 1$

Como $m, n \in \mathbb{Z}^+$, $m - n + 1 = 0$ solo si $m - n = -1$, es decir, $m = n - 1$

Pero $m \geq 1$, así que $n \geq 2$, $m = n - 1$

Pero en general, para $m,n$ arbitrarios positivos, **$m - n + 1$ es entero, pero rara vez cero**.

Pero notemos que **la integral es cero salvo que $m - n + 1 = 0$**.

Sin embargo, observemos que $f(z) = z^m \overline{z}^n$ **no es analítica** (porque depende de $\overline{z}$), así que no podemos usar Cauchy directamente.

Pero ya hicimos el cálculo explícito:

$$
\int_C f(z)\,dz = i R^{m+n+1} \int_0^{2\pi} e^{i(m - n + 1)\theta} d\theta
$$

Esta integral es cero a menos que $m - n + 1 = 0$, es decir, $m = n - 1$

Pero como $m \in \mathbb{Z}^+$, $n - 1 \geq 1 \Rightarrow n \geq 2$

Pero aún así, **para valores fijos arbitrarios de $m,n$**, la integral será cero si $m - n + 1 \ne 0$

Pero en general, **¿es siempre cero?**

No, solo cuando $m - n + 1 = 0$

Pero veamos: ¿puede $m - n + 1 = 0$? Sí, por ejemplo $m = 1, n = 2$

Pero el problema no especifica valores particulares, sino $m,n$ enteros positivos generales.

Así que la integral es:

$$
\int_C f(z)\,dz = 
\begin{cases}
i R^{m+n+1} \cdot 2\pi & \text{si } m - n + 1 = 0 \Rightarrow m = n - 1 \\
0 & \text{en otro caso}
\end{cases}
$$

Pero notemos que $m \geq 1$, $n \geq 1$, entonces $m = n - 1 \Rightarrow n = m + 1 \geq 2$

Así que solo cuando $n = m + 1$, la integral es distinta de cero.

Pero el problema pide evaluar **para enteros positivos $m,n$**, sin más, así que debemos dar una expresión general.

Sin embargo, en la mayoría de los casos, **la integral es cero**, porque $m - n + 1 \ne 0$

Pero mejor escribamos:

$$
\int_C f(z)\,dz = i R^{m+n+1} \cdot 2\pi \cdot \delta_{m - n + 1, 0} = 
\begin{cases}
2\pi i R^{m+n+1} & \text{si } m = n - 1 \\
0 & \text{en otro caso}
\end{cases}
$$

Pero en realidad, cuando $m = n - 1$, $m + n + 1 = (n - 1) + n + 1 = 2n$, así que $R^{2n}$

Pero quizás se espera una respuesta más simple.

Sin embargo, hay una forma más elegante de verlo:

Notemos que en $|z| = R$, $z \overline{z} = R^2 \Rightarrow \overline{z} = \frac{R^2}{z}$

Entonces:

$$
f(z) = z^m (\overline{z})^n = z^m \left( \frac{R^2}{z} \right)^n = R^{2n} z^{m - n}
$$

¡Ah! Esta es una forma mucho mejor.

En la curva $|z| = R$, podemos reemplazar $\overline{z} = R^2 / z$, entonces:

$$
f(z) = z^m \left( \frac{R^2}{z} \right)^n = R^{2n} z^{m - n}
$$

Entonces:

$$
\int_C f(z)\,dz = R^{2n} \int_C z^{m - n} dz
$$

Ahora, $C$ es un círculo alrededor del origen, sentido positivo.

Sabemos que:

$$
\int_C z^k dz = 
\begin{cases}
2\pi i & \text{si } k = -1 \\
0 & \text{en otro caso}
\end{cases}
$$

Entonces:

$$
\int_C z^{m - n} dz = 
\begin{cases}
2\pi i & \text{si } m - n = -1 \Rightarrow m = n - 1 \\
0 & \text{en otro caso}
\end{cases}
$$

Entonces:

$$
\int_C f(z)\,dz = 
\begin{cases}
R^{2n} \cdot 2\pi i & \text{si } m = n - 1 \\
0 & \text{en otro caso}
\end{cases}
$$

Pero como $m,n$ son enteros positivos, $m = n - 1$ implica $n \geq 2$, $m \geq 1$

Pero el problema no especifica relación entre $m,n$, así que la respuesta general es:

$$
\boxed{
\int_C f(z)\,dz = 
\begin{cases}
2\pi i R^{2n} & \text{si } m = n - 1 \\
0 & \text{en otro caso}
\end{cases}
}
$$

Pero si se pide un solo valor, y no hay condiciones, en general es cero, pero mejor dejarlo condicional.

Sin embargo, en muchos contextos, se espera que se diga que **es cero a menos que $m - n = -1$**.

Pero como el problema no da valores específicos, debemos dejarlo así.

Pero quizás se espera que digamos que **es cero**, porque $f(z)$ no es analítica y la integral de funciones no analíticas puede no ser cero, pero en este caso, usando el truco de $\overline{z} = R^2/z$, reducimos a una función racional.

Pero en cualquier caso, la respuesta es:

$$
\boxed{\int_C f(z)\,dz = \begin{cases} 2\pi i R^{2n} & \text{si } m = n - 1 \\ 0 & \text{en otro caso} \end{cases}}
$$

---

### **b)** Calcule $\int_C \frac{z}{z^2 + 4} dz$, donde $C: 4x^2 + (y - 2)^2 = 4$

Primero, grafiquemos $C$.

La ecuación:

$$
4x^2 + (y - 2)^2 = 4 \Rightarrow \frac{x^2}{1} + \frac{(y - 2)^2}{4} = 1
$$

Es una **elipse** centrada en $(0,2)$, con semieje horizontal $a = 1$, vertical $b = 2$.

Ahora, consideremos la función:

$$
f(z) = \frac{z}{z^2 + 4} = \frac{z}{(z - 2i)(z + 2i)}
$$

Singularidades en $z = 2i$ y $z = -2i$

Veamos cuáles están dentro de $C$

Centro de la elipse: $(0,2)$, es decir, $z = 2i$

Altura total: de $y = 0$ a $y = 4$, porque $(y - 2)^2 \leq 4 \Rightarrow |y - 2| \leq 2 \Rightarrow y \in [0,4]$

- $z = 2i$ → $y = 2$, está dentro (centro)
- $z = -2i$ → $y = -2$, está fuera (porque $y \geq 0$ en la elipse)

Entonces solo $z = 2i$ está dentro de $C$

Ahora, usemos el teorema del residuo.

$$
\int_C f(z)\,dz = 2\pi i \cdot \text{Res}(f, 2i)
$$

Calculemos el residuo en el polo simple $z = 2i$:

$$
\text{Res}(f, 2i) = \lim_{z \to 2i} (z - 2i) \frac{z}{(z - 2i)(z + 2i)} = \frac{2i}{2i + 2i} = \frac{2i}{4i} = \frac{1}{2}
$$

Entonces:

$$
\int_C f(z)\,dz = 2\pi i \cdot \frac{1}{2} = \pi i
$$

**Gráfica:** Elipse vertical centrada en $(0,2)$, pasa por $(1,2), (-1,2), (0,4), (0,0)$. Singularidad $2i$ en el centro, $-2i$ abajo, fuera.

**Respuesta:**

$$
\boxed{\pi i}
$$

---

### **c)** Evalúe $\int_C \frac{\cos z}{z^{2n+1}} dz$, $n = 0,1,2,\ldots$, $C: |z| = 1$, sentido positivo.

Sabemos que $\cos z$ es entera (analítica en todo $\mathbb{C}$), y $\frac{\cos z}{z^{2n+1}}$ tiene un polo de orden $2n+1$ en $z = 0$, que está dentro de $C$.

Entonces, por la fórmula integral de Cauchy para derivadas:

$$
\int_C \frac{f(z)}{z^{k+1}} dz = \frac{2\pi i}{k!} f^{(k)}(0)
$$

Aquí, $f(z) = \cos z$, $k + 1 = 2n + 1 \Rightarrow k = 2n$

Entonces:

$$
\int_C \frac{\cos z}{z^{2n+1}} dz = \frac{2\pi i}{(2n)!} \cdot \cos^{(2n)}(0)
$$

Ahora, derivadas de $\cos z$:

Sabemos que:

$$
\frac{d^k}{dz^k} \cos z = \cos\left(z + \frac{k\pi}{2}\right)
$$

Entonces:

$$
\cos^{(2n)}(z) = \cos\left(z + n\pi\right) = (-1)^n \cos z
$$

Entonces:

$$
\cos^{(2n)}(0) = (-1)^n \cos 0 = (-1)^n
$$

Por tanto:

$$
\int_C \frac{\cos z}{z^{2n+1}} dz = \frac{2\pi i}{(2n)!} \cdot (-1)^n = 2\pi i \cdot \frac{(-1)^n}{(2n)!}
$$

**Gráfica:** Círculo unitario centrado en el origen, recorrido en sentido antihorario.

**Respuesta:**

$$
\boxed{2\pi i \cdot \frac{(-1)^n}{(2n)!}}
$$

---

## **Resumen de respuestas**

### **Ejercicio 3**

a) $\boxed{v(x,y) = x^2 - y^2 + 2y}$

b) $\boxed{u(x,y) = -\cosh x \sin y}$

### **Ejercicio 4**

a) $\boxed{\int_C f(z)\,dz = \begin{cases} 2\pi i R^{2n} & \text{si } m = n - 1 \\ 0 & \text{en otro caso} \end{cases}}$

b) $\boxed{\pi i}$

c) $\boxed{2\pi i \cdot \frac{(-1)^n}{(2n)!}}$

---

✅ Todos los resultados están en forma $a + bi$, como se pide.