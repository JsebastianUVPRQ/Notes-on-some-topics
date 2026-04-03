Aquí tienes las soluciones detalladas y las demostraciones para cada uno de los problemas planteados.

### Problema 1: Ecuación Cuadrática Trigonométrica

Para encontrar las soluciones de la ecuación cuadrática $x^2 - 2x + \sin^2\theta = 0$, podemos utilizar la fórmula general cuadrática:

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

Sustituyendo $a = 1$, $b = -2$, y $c = \sin^2\theta$:

$$x = \frac{2 \pm \sqrt{(-2)^2 - 4(1)(\sin^2\theta)}}{2}$$

$$x = \frac{2 \pm \sqrt{4 - 4\sin^2\theta}}{2}$$

Factorizamos el 4 dentro de la raíz:

$$x = \frac{2 \pm 2\sqrt{1 - \sin^2\theta}}{2}$$

$$x = 1 \pm \sqrt{1 - \sin^2\theta}$$

Usando la identidad pitagórica $\cos^2\theta + \sin^2\theta = 1$, sabemos que $1 - \sin^2\theta = \cos^2\theta$. Por lo tanto, $\sqrt{\cos^2\theta} = |\cos\theta|$. Dado que tenemos el símbolo $\pm$, podemos omitir el valor absoluto:

$$x = 1 \pm \cos\theta$$

Esto nos da dos soluciones:

1. $x_1 = 1 + \cos\theta$
    
2. $x_2 = 1 - \cos\theta$
    

Ahora, aplicamos las identidades de ángulo medio:

- $\cos\theta = 2\cos^2\frac{\theta}{2} - 1 \implies 1 + \cos\theta = 2\cos^2\frac{\theta}{2}$
    
- $\cos\theta = 1 - 2\sin^2\frac{\theta}{2} \implies 1 - \cos\theta = 2\sin^2\frac{\theta}{2}$
    

Sustituyendo estas identidades obtenemos las soluciones deseadas:

$$x_1 = 2\cos^2\frac{\theta}{2}$$

$$x_2 = 2\sin^2\frac{\theta}{2}$$

---

### Problema 2: Identidad con Números Complejos

Dada la ecuación $x + \frac{1}{x} = 2\cos\theta$, multiplicamos toda la expresión por $x$ para obtener una ecuación cuadrática (asumiendo $x \neq 0$):

$$x^2 - 2x\cos\theta + 1 = 0$$

Aplicando la fórmula cuadrática:

$$x = \frac{2\cos\theta \pm \sqrt{4\cos^2\theta - 4}}{2} = \cos\theta \pm \sqrt{\cos^2\theta - 1}$$

Sabiendo que $\cos^2\theta - 1 = -\sin^2\theta$, la raíz cuadrada se convierte en un número imaginario:

$$x = \cos\theta \pm i\sin\theta$$

Según la fórmula de De Moivre o la identidad de Euler ($x = e^{\pm i\theta}$), para cualquier número natural $n$, tenemos:

$$x^n = (\cos\theta \pm i\sin\theta)^n = \cos(n\theta) \pm i\sin(n\theta)$$

Por otro lado, la inversa $\frac{1}{x^n} = x^{-n}$ es:

$$x^{-n} = (\cos\theta \pm i\sin\theta)^{-n} = \cos(-n\theta) \pm i\sin(-n\theta) = \cos(n\theta) \mp i\sin(n\theta)$$

Al sumar ambas expresiones, la parte imaginaria se cancela independientemente del signo que hayamos elegido originalmente para $x$:

$$x^n + \frac{1}{x^n} = [\cos(n\theta) \pm i\sin(n\theta)] + [\cos(n\theta) \mp i\sin(n\theta)]$$

$$x^n + \frac{1}{x^n} = 2\cos(n\theta)$$

---

### Problema 3: Bosquejo de la Curva $(x^2 + y^2)^3 = 4x^2y^2$

Para facilitar el bosquejo sin herramientas tecnológicas, lo más conveniente es convertir la ecuación a coordenadas polares, recordando que $x^2 + y^2 = r^2$, $x = r\cos\theta$, y $y = r\sin\theta$:

$$(r^2)^3 = 4(r\cos\theta)^2(r\sin\theta)^2$$

$$r^6 = 4r^4\cos^2\theta\sin^2\theta$$

Asumiendo $r \neq 0$ (el origen también es parte de la curva), dividimos entre $r^4$:

$$r^2 = 4\cos^2\theta\sin^2\theta$$

Recordando la identidad del ángulo doble $\sin(2\theta) = 2\sin\theta\cos\theta$, la expresión de la derecha es exactamente $(2\sin\theta\cos\theta)^2$:

$$r^2 = \sin^2(2\theta)$$

$$r = \pm\sin(2\theta)$$

**Pasos para el bosquejo:**

1. **Forma base:** La ecuación $r = \sin(2\theta)$ describe una clásica "rosa polar de cuatro pétalos".
    
2. **Máximos:** La distancia máxima desde el origen es 1, lo cual ocurre cuando $\sin(2\theta) = \pm 1$. Esto sucede en $\theta = \frac{\pi}{4}, \frac{3\pi}{4}, \frac{5\pi}{4}, \frac{7\pi}{4}$.
    
3. **Ceros (raíces):** La curva pasa por el origen ($r=0$) en los ángulos $\theta = 0, \frac{\pi}{2}, \pi, \frac{3\pi}{2}, 2\pi$.
    
4. **Bosquejo final:** Dibuja un sistema de ejes coordenados. Traza cuatro pétalos idénticos en los cuadrantes, todos con longitud 1, apuntando exactamente hacia las diagonales de los cuadrantes (ángulos de 45 grados o $\frac{\pi}{4}$ respecto a los ejes).
    

---

### Problema 4: Gráfica y Área de $r = 4 + 3\sin\theta$

**Bosquejo de la curva:**

La ecuación tiene la forma $r = a + b\sin\theta$. Como $a > b$ (4 > 3), se trata de un caracol de Pascal (o limaçon) **sin lazo interno** y que tampoco toca el polo (origen).

- En $\theta = 0$ y $\pi$, $r = 4$ (cruza el eje x horizontal en 4 y -4).
    
- En $\theta = \frac{\pi}{2}$, el valor de $\sin\theta$ es 1, por lo que alcanza su máximo: $r = 7$.
    
- En $\theta = \frac{3\pi}{2}$, el valor de $\sin\theta$ es -1, por lo que alcanza su mínimo: $r = 1$.
    
    El bosquejo es similar a un círculo "aplastado" en la parte inferior, subiendo desde $y=1$ hasta $y=7$.
    

**Cálculo del área:**

La fórmula para el área en coordenadas polares es $A = \frac{1}{2}\int_{\alpha}^{\beta} r^2 d\theta$.

Integraremos un giro completo (de 0 a $2\pi$):

$$A = \frac{1}{2}\int_0^{2\pi} (4 + 3\sin\theta)^2 d\theta$$

$$A = \frac{1}{2}\int_0^{2\pi} (16 + 24\sin\theta + 9\sin^2\theta) d\theta$$

Separando la integral en tres partes:

1. $\int_0^{2\pi} 16 d\theta = 32\pi$
    
2. $\int_0^{2\pi} 24\sin\theta d\theta = 0$ (la integral de seno sobre un periodo completo es cero).
    
3. Para la tercera parte, usamos la identidad $\sin^2\theta = \frac{1 - \cos(2\theta)}{2}$:
    
    $$\int_0^{2\pi} 9\sin^2\theta d\theta = 9 \int_0^{2\pi} \frac{1 - \cos(2\theta)}{2} d\theta = \frac{9}{2} \left[ \theta - \frac{\sin(2\theta)}{2} \right]_0^{2\pi} = \frac{9}{2}(2\pi) = 9\pi$$
    

Sumamos los resultados:

$$A = \frac{1}{2}(32\pi + 0 + 9\pi) = \frac{41\pi}{2}$$

---

### Problema 5: Longitud de la Curva $r = 2(1+\cos\theta)$

La curva es un cardioide clásico orientado hacia la derecha. La fórmula para la longitud de arco polar es:

$$L = \int_{\alpha}^{\beta} \sqrt{r^2 + \left(\frac{dr}{d\theta}\right)^2} d\theta$$

Primero, calculamos las partes dentro de la raíz:

- $r = 2 + 2\cos\theta$
    
- $r^2 = 4 + 8\cos\theta + 4\cos^2\theta$
    
- $\frac{dr}{d\theta} = -2\sin\theta$
    
- $\left(\frac{dr}{d\theta}\right)^2 = 4\sin^2\theta$
    

Sumando y simplificando con $\cos^2\theta + \sin^2\theta = 1$:

$$r^2 + \left(\frac{dr}{d\theta}\right)^2 = 4 + 8\cos\theta + 4(\cos^2\theta + \sin^2\theta) = 8 + 8\cos\theta = 8(1 + \cos\theta)$$

Usamos la identidad de ángulo medio $1 + \cos\theta = 2\cos^2\frac{\theta}{2}$:

$$8(1 + \cos\theta) = 16\cos^2\frac{\theta}{2}$$

Ahora, sustituimos en la integral de 0 a $2\pi$:

$$L = \int_0^{2\pi} \sqrt{16\cos^2\frac{\theta}{2}} d\theta = 4 \int_0^{2\pi} \left|\cos\frac{\theta}{2}\right| d\theta$$

Por la simetría del cardioide, es más fácil integrar la mitad superior (de 0 a $\pi$) y multiplicar por 2. En el intervalo $[0, \pi]$, el término $\cos\frac{\theta}{2}$ siempre es positivo, por lo que podemos eliminar el valor absoluto:

$$L = 2 \times 4 \int_0^{\pi} \cos\frac{\theta}{2} d\theta$$

$$L = 8 \left[ 2\sin\frac{\theta}{2} \right]_0^{\pi}$$

$$L = 16(\sin\frac{\pi}{2} - \sin 0) = 16(1 - 0) = 16$$

---

### Problema 6: Teoremas de Límites de Sucesiones

Definamos $\lim_{n\to\infty}a_n = L$ y $\lim_{n\to\infty}b_n = M$. Por la definición formal, para cualquier $\epsilon > 0$, existen naturales $N_1, N_2$ tales que si $n > N_1$ entonces $|a_n - L| < \epsilon_a$ y si $n > N_2$ entonces $|b_n - M| < \epsilon_b$.

**(a) Límite de la suma**

Dado $\epsilon > 0$, tomemos $N = \max(N_1, N_2)$ asegurando que $|a_n - L| < \frac{\epsilon}{2}$ y $|b_n - M| < \frac{\epsilon}{2}$.

Usando la desigualdad triangular:

$$|(a_n + b_n) - (L + M)| = |(a_n - L) + (b_n - M)| \leq |a_n - L| + |b_n - M| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

Queda demostrado.

**(b) Límite de la resta**

Análogo a (a), si tomamos $N = \max(N_1, N_2)$:

$$|(a_n - b_n) - (L - M)| = |(a_n - L) - (b_n - M)| \leq |a_n - L| + |- (b_n - M)| = |a_n - L| + |b_n - M| < \epsilon$$

Queda demostrado.

**(c) Múltiplo constante**

Si $c=0$, la demostración es trivial ya que toda la sucesión es cero. Si $c \neq 0$, dado $\epsilon > 0$, existe un $N$ tal que para $n>N$, se cumple $|a_n - L| < \frac{\epsilon}{|c|}$.

Por lo tanto:

$$|ca_n - cL| = |c||a_n - L| < |c| \left(\frac{\epsilon}{|c|}\right) = \epsilon$$

Queda demostrado.

**(d) Límite del producto**

Como la sucesión $\{a_n\}$ es convergente, está acotada. Existe una constante $K > 0$ tal que $|a_n| \leq K$ para todo $n$.

Sumamos y restamos $a_nM$ dentro del valor absoluto:

$$|a_n b_n - LM| = |a_n b_n - a_n M + a_n M - LM| \leq |a_n||b_n - M| + |M||a_n - L|$$

Dado $\epsilon > 0$, elegimos $N$ tal que para $n>N$, $|b_n - M| < \frac{\epsilon}{2K}$ y $|a_n - L| < \frac{\epsilon}{2(|M|+1)}$ (usamos $|M|+1$ para evitar división por cero si $M=0$). Sustituyendo:

$$|a_n b_n - LM| < K\left(\frac{\epsilon}{2K}\right) + |M|\left(\frac{\epsilon}{2(|M|+1)}\right) < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

Queda demostrado.

**(e) Límite del cociente**

Primero, probemos que $\lim_{n\to\infty} \frac{1}{b_n} = \frac{1}{M}$ asumiendo $M \neq 0$.

Como $M \neq 0$, para un $n$ suficientemente grande, los valores de $|b_n|$ están acotados lejos de cero; específicamente, existe $N_1$ tal que $|b_n| > \frac{|M|}{2}$.

Evaluamos la distancia al límite:

$$\left|\frac{1}{b_n} - \frac{1}{M}\right| = \frac{|M - b_n|}{|b_n||M|}$$

Sustituyendo nuestra cota para el denominador:

$$\frac{|M - b_n|}{|b_n||M|} < \frac{|M - b_n|}{\left(\frac{|M|}{2}\right)|M|} = \frac{2|b_n - M|}{|M|^2}$$

Como $\{b_n\}$ converge, existe $N_2$ tal que $|b_n - M| < \frac{|M|^2 \epsilon}{2}$. Tomando $N = \max(N_1, N_2)$, la expresión completa será menor que $\epsilon$, lo que prueba el límite del recíproco.

Finalmente, aplicamos el teorema del producto (demostrado en d) para $a_n \cdot \frac{1}{b_n}$:

$$\lim_{n\to\infty} \left( a_n \cdot \frac{1}{b_n} \right) = L \cdot \frac{1}{M} = \frac{L}{M}$$

Queda demostrado.

**(f) Límite de la potencia real**

Este es un corolario de la continuidad de funciones. Sabemos que si $p > 0$ y $x > 0$, la función real $f(x) = x^p$ es continua en su dominio $(0, \infty)$.

Una propiedad fundamental del análisis real dicta que si una función $f(x)$ es continua y la sucesión $\{a_n\}$ converge a un límite $L$ en el dominio de $f$, entonces el límite preserva la función:

$$\lim_{n\to\infty} f(a_n) = f\left(\lim_{n\to\infty} a_n\right)$$

Aplicando esto directamente a la función potencia $f(x) = x^p$, con $a_n > 0$ y $\lim a_n = L$:

$$\lim_{n\to\infty} (a_n)^p = \left(\lim_{n\to\infty} a_n\right)^p = L^p$$

Queda demostrado.

Aquí tienes las demostraciones y soluciones detalladas para esta segunda parte de problemas sobre series.

### Problema 8: Criterio de Comparación Directa (Comparación de series I)

Sean $\sum a_n$ y $\sum b_n$ series con términos positivos ($a_n > 0$, $b_n > 0$). Definamos sus sucesiones de sumas parciales como $S_n = \sum_{k=1}^n a_k$ y $T_n = \sum_{k=1}^n b_k$. Como los términos son positivos, ambas sucesiones de sumas parciales son monótonamente crecientes.

**(i) Demostración de convergencia:**

Sabemos que $\sum b_n$ converge a un valor finito, digamos $L$. Dado que $\{T_n\}$ es estrictamente creciente, $T_n \le L$ para todo $n$.

Por hipótesis, $a_n \le b_n$ para toda $n$. Sumando estos términos, obtenemos que las sumas parciales respetan la misma desigualdad:

$$S_n \le T_n \le L$$

La sucesión $\{S_n\}$ es creciente y está acotada superiormente por $L$. Por el Teorema de la Convergencia Monótona, toda sucesión creciente y acotada converge. Por lo tanto, $\sum a_n$ **converge**.

**(ii) Demostración de divergencia:**

Sabemos que $\sum b_n$ diverge. Como $\{T_n\}$ es creciente y divergente, no está acotada superiormente, es decir, $\lim_{n\to\infty} T_n = \infty$.

Por hipótesis, $a_n \ge b_n$ para toda $n$, lo que implica que:

$$S_n \ge T_n$$

Como $T_n$ crece sin límite, $S_n$ también debe crecer sin límite. Por el teorema de comparación de límites al infinito, $\lim_{n\to\infty} S_n = \infty$. Por lo tanto, $\sum a_n$ **diverge**.

---

### Problema 9: Criterio de Comparación en el Límite (Comparación de series II)

Por definición de límite, si $\lim_{n\to\infty} \frac{a_n}{b_n} = c$ (con $c > 0$), entonces para cualquier $\epsilon > 0$, existe un entero $N$ tal que para todo $n \ge N$:

$$\left| \frac{a_n}{b_n} - c \right| < \epsilon$$

$$c - \epsilon < \frac{a_n}{b_n} < c + \epsilon$$

Elijamos un $\epsilon$ conveniente, por ejemplo $\epsilon = \frac{c}{2}$ (que es mayor a 0 porque $c>0$). Sustituyendo:

$$c - \frac{c}{2} < \frac{a_n}{b_n} < c + \frac{c}{2}$$

$$\frac{c}{2} < \frac{a_n}{b_n} < \frac{3c}{2}$$

Como $b_n > 0$, multiplicamos la desigualdad por $b_n$ sin alterar los signos:

$$\frac{c}{2}b_n < a_n < \frac{3c}{2}b_n \quad \text{para todo } n \ge N$$

Ahora aplicamos el Criterio de Comparación Directa (Problema 8) a partir del índice $N$:

1. **Si $\sum b_n$ converge:** Entonces la serie multiplicada por una constante $\sum \frac{3c}{2}b_n$ también converge. Como $a_n < \frac{3c}{2}b_n$, se concluye que $\sum a_n$ converge.
    
2. **Si $\sum b_n$ diverge:** Entonces la serie multiplicada $\sum \frac{c}{2}b_n$ diverge. Como $a_n > \frac{c}{2}b_n$, se concluye que $\sum a_n$ diverge.
    

Por lo tanto, ambas convergen o ambas divergen al mismo tiempo.

---

### Problema 10: Convergencia de la Serie Geométrica

Queremos analizar $\sum_{n=1}^{\infty} a r^{n-1}$.

_Caso trivial:_ Si $a = 0$, la serie es una suma de ceros y converge a $0$ sin importar el valor de $r$.

Asumamos $a \neq 0$. La enésima suma parcial es:

$$S_n = a + ar + ar^2 + \dots + ar^{n-1}$$

Multiplicamos $S_n$ por $r$:

$$r S_n = ar + ar^2 + ar^3 + \dots + ar^n$$

Restamos la segunda ecuación de la primera:

$$S_n - r S_n = a - ar^n$$

$$S_n(1 - r) = a(1 - r^n)$$

- **Si $r = 1$:** La fórmula anterior dividiría por cero. Volviendo a la suma original: $S_n = a + a + \dots + a = na$. Como $\lim_{n\to\infty} na = \pm\infty$, diverge.
    
- **Si $r \neq 1$:** Podemos despejar $S_n$:
    
    $$S_n = \frac{a(1 - r^n)}{1 - r}$$
    
    Para que la serie converja, debe existir el límite de $S_n$ cuando $n \to \infty$. El único término que depende de $n$ es $r^n$.
    
    - Si $|r| < 1$, entonces $\lim_{n\to\infty} r^n = 0$. Por lo tanto, $\lim_{n\to\infty} S_n = \frac{a}{1 - r}$.
        
    - Si $|r| > 1$, el término $r^n$ crece sin límite y la serie diverge.
        
    - Si $r = -1$, el término $(-1)^n$ oscila entre $1$ y $-1$, por lo que el límite no existe y diverge.
        

**Conclusión:** La serie $\sum_{n=1}^{\infty} a r^{n-1}$ (para $a \neq 0$) converge **si y solo si** $|r| < 1$, y su valor de convergencia es $\frac{a}{1-r}$.

---

### Problema 11: Divergencia de la Serie Armónica

Analizaremos la serie armónica $\sum_{n=1}^{\infty} \frac{1}{n}$ agrupando sus términos (demostración clásica de Nicole Oresme).

Consideremos las sumas parciales especiales donde el índice superior es una potencia de 2, $S_{2^k}$:

$$S_1 = 1$$

$$S_2 = 1 + \frac{1}{2}$$

$$S_4 = 1 + \frac{1}{2} + \left(\frac{1}{3} + \frac{1}{4}\right)$$

$$S_8 = 1 + \frac{1}{2} + \left(\frac{1}{3} + \frac{1}{4}\right) + \left(\frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8}\right)$$

Podemos acotar inferiormente cada grupo de términos reemplazándolos por el término más pequeño del grupo:

- $\frac{1}{3} + \frac{1}{4} > \frac{1}{4} + \frac{1}{4} = \frac{2}{4} = \frac{1}{2}$
    
- $\frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8} > \frac{1}{8} + \frac{1}{8} + \frac{1}{8} + \frac{1}{8} = \frac{4}{8} = \frac{1}{2}$
    

En general, cada bloque que va desde $2^{m-1}+1$ hasta $2^m$ tiene $2^{m-1}$ términos, y cada término es mayor o igual a $\frac{1}{2^m}$. La suma del bloque siempre es estrictamente mayor que $\frac{1}{2}$.

Sustituyendo estas cotas en las sumas parciales obtenemos:

$$S_{2^k} > 1 + \frac{1}{2} + \frac{1}{2} + \dots + \frac{1}{2} \text{ (donde hay } k \text{ términos de un medio)}$$

$$S_{2^k} > 1 + \frac{k}{2}$$

A medida que $k \to \infty$, la expresión $1 + \frac{k}{2} \to \infty$. Dado que una subsecuencia de las sumas parciales diverge hacia infinito, la sucesión general de sumas parciales también lo hace. Por lo tanto, la serie **diverge**.

---

### Problema 12: Determinación de Convergencia o Divergencia

**(a)** $\displaystyle \sum_{n=2}^{\infty} \frac{\sqrt{n}}{n-1}$

Usamos el Criterio de Comparación Directa. Para todo $n \ge 2$, sabemos que $n-1 < n$, lo que implica que $\frac{1}{n-1} > \frac{1}{n}$. Multiplicando por $\sqrt{n}$ (que es positivo):

$$\frac{\sqrt{n}}{n-1} > \frac{\sqrt{n}}{n} = \frac{1}{n^{1/2}}$$

La serie $\sum \frac{1}{n^{1/2}}$ es una p-serie con $p = \frac{1}{2}$. Sabemos que las p-series divergen si $p \le 1$.

Como nuestra serie es término a término mayor que una serie divergente, la serie **diverge**.

**(b)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n!}$

Usamos el Criterio de la Razón (D'Alembert). Sea $a_n = \frac{1}{n!}$:

$$L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right| = \lim_{n\to\infty} \frac{\frac{1}{(n+1)!}}{\frac{1}{n!}} = \lim_{n\to\infty} \frac{n!}{(n+1)n!} = \lim_{n\to\infty} \frac{1}{n+1} = 0$$

Dado que $L = 0 < 1$, por el criterio de la razón, la serie **converge** (de hecho, converge a $e-1$).

**(c)** $\displaystyle \sum_{n=1}^{\infty} \sin\left(\frac{1}{n}\right)$

Usamos el Criterio de Comparación en el Límite (Problema 9) escogiendo la serie armónica $b_n = \frac{1}{n}$, la cual sabemos que diverge:

$$c = \lim_{n\to\infty} \frac{a_n}{b_n} = \lim_{n\to\infty} \frac{\sin(1/n)}{1/n}$$

Haciendo el cambio de variable $x = \frac{1}{n}$, cuando $n \to \infty$, $x \to 0$:

$$c = \lim_{x\to 0} \frac{\sin x}{x} = 1$$

Como $0 < c < \infty$ y la serie $\sum \frac{1}{n}$ diverge, nuestra serie propuesta también **diverge**.

**(d)** $\displaystyle \sum_{n=1}^{\infty} \left(1+\frac{1}{n}\right)^2 e^{-n}$

Usaremos el Criterio de la Raíz (Cauchy). Sea $a_n = \left(1+\frac{1}{n}\right)^2 e^{-n}$:

$$L = \lim_{n\to\infty} \sqrt[n]{a_n} = \lim_{n\to\infty} \left( \left(1+\frac{1}{n}\right)^2 e^{-n} \right)^{\frac{1}{n}} = \lim_{n\to\infty} \left(1+\frac{1}{n}\right)^{\frac{2}{n}} e^{-1}$$

El primer término es $\left(1+\frac{1}{n}\right)^{\frac{2}{n}}$. Cuando $n \to \infty$, la base $(1+\frac{1}{n}) \to 1$ y el exponente $\frac{2}{n} \to 0$. Por lo tanto, $(1)^{\text{algo que tiende a }0} = 1$.

$$L = 1 \cdot e^{-1} = \frac{1}{e}$$

Como $e \approx 2.718$, tenemos que $L = \frac{1}{e} < 1$. Por el criterio de la raíz, la serie **converge**


### Problema 13: Convergencia de la Representación Decimal

**Planteamiento:**

Debemos demostrar que la serie asociada a la representación decimal de cualquier número entre 0 y 1, dada por:

$$\sum_{n=1}^{\infty} \frac{d_n}{10^n} = \frac{d_1}{10} + \frac{d_2}{10^2} + \frac{d_3}{10^3} + \cdots$$

siempre converge, sabiendo que cada dígito $d_n$ pertenece al conjunto $\{0, 1, 2, \dots, 9\}$.

**Demostración:**

Utilizaremos el **Criterio de Comparación Directa**.

Dado que el valor máximo que puede tomar cualquier dígito $d_n$ es 9, y su valor mínimo es 0, podemos establecer la siguiente desigualdad para cada término de la serie:

$$0 \le \frac{d_n}{10^n} \le \frac{9}{10^n} \quad \text{para toda } n \ge 1$$

Ahora, observemos la serie construida con los términos mayores de nuestra desigualdad:

$$\sum_{n=1}^{\infty} \frac{9}{10^n}$$

Esta es una serie geométrica de la forma $\sum a r^{n-1}$, donde podemos factorizar el 9 para verla más claramente:

$$9 \sum_{n=1}^{\infty} \left(\frac{1}{10}\right)^n = \frac{9}{10} + \frac{9}{100} + \frac{9}{1000} + \cdots$$

La razón de esta serie geométrica es $r = \frac{1}{10}$. Dado que $|r| < 1$, sabemos por los teoremas de series geométricas que **converge** (de hecho, converge exactamente a 1, ya que $0.999\dots = 1$).

Como los términos de nuestra serie original $\frac{d_n}{10^n}$ son siempre positivos o cero, y están acotados superiormente término a término por los de una serie convergente $\frac{9}{10^n}$, el Criterio de Comparación Directa garantiza que la serie original $\sum_{n=1}^{\infty} \frac{d_n}{10^n}$ **siempre es convergente**.

---

### Problema 14: Demostración del Teorema de la Serie Alternante

**Planteamiento:**

Sea la serie alternante $\sum_{n=1}^{\infty}(-1)^{n-1}b_n$, con $b_n > 0$. Debemos probar que converge si cumple dos condiciones: (i) la sucesión $\{b_n\}$ es decreciente ($b_{n+1} \le b_n$) y (ii) el límite $\lim_{n\to\infty} b_n = 0$.

**Demostración:**

Analizaremos la sucesión de sumas parciales $\{S_m\}$, dividiéndola en sumas de índice par ($S_{2n}$) y de índice impar ($S_{2n+1}$).

**Paso 1: Análisis de las sumas parciales pares.**

Consideremos la enésima suma parcial par:

$$S_{2n} = (b_1 - b_2) + (b_3 - b_4) + \cdots + (b_{2n-1} - b_{2n})$$

Por la condición (i), sabemos que $b_k \ge b_{k+1}$ para todo $k$, lo que significa que cada agrupación entre paréntesis $(b_k - b_{k+1}) \ge 0$. Por lo tanto, al avanzar de $S_{2n}$ a $S_{2n+2}$, estamos sumando una cantidad no negativa:

$$S_{2n+2} = S_{2n} + (b_{2n+1} - b_{2n+2}) \ge S_{2n}$$

Esto demuestra que la sucesión de sumas parciales pares $\{S_{2n}\}$ es **creciente** (o monótona no decreciente).

**Paso 2: Acotación de las sumas parciales pares.**

Podemos reescribir la misma suma $S_{2n}$ agrupando los términos de forma distinta:

$$S_{2n} = b_1 - (b_2 - b_3) - (b_4 - b_5) - \cdots - (b_{2n-2} - b_{2n-1}) - b_{2n}$$

Nuevamente, cada término entre paréntesis es no negativo, y $b_{2n} > 0$. Esto significa que a $b_1$ le estamos restando puras cantidades no negativas. En consecuencia:

$$S_{2n} \le b_1 \quad \text{para toda } n$$

Como la sucesión $\{S_{2n}\}$ es creciente y está acotada superiormente por $b_1$, el **Teorema de la Convergencia Monótona** garantiza que $\{S_{2n}\}$ converge a un límite finito. Llamemos a ese límite $S$:

$$\lim_{n\to\infty} S_{2n} = S$$

**Paso 3: Análisis de las sumas parciales impares.**

Ahora consideremos las sumas parciales de índice impar, las cuales se pueden expresar a partir de las pares:

$$S_{2n+1} = S_{2n} + b_{2n+1}$$

Tomando el límite cuando $n \to \infty$ y aplicando la condición (ii) del teorema ($\lim_{n\to\infty} b_n = 0$):

$$\lim_{n\to\infty} S_{2n+1} = \lim_{n\to\infty} (S_{2n} + b_{2n+1}) = \lim_{n\to\infty} S_{2n} + \lim_{n\to\infty} b_{2n+1} = S + 0 = S$$

**Conclusión:**

Tanto la subsucesión de sumas parciales pares como la de impares convergen exactamente al mismo límite $S$. Por lo tanto, la sucesión completa de sumas parciales $\{S_m\}$ converge a $S$, lo que demuestra que la serie alternante es **convergente**.

---

### Problema 15: Convergencia de Series Alternantes Trigonométricas

**(a)** $\displaystyle \sum_{n=1}^{\infty}(-1)^{n}\sin\left(\frac{\pi}{n}\right)$

Para aplicar el Criterio de la Serie Alternante, definimos $b_n = \sin\left(\frac{\pi}{n}\right)$ y verificamos sus condiciones.

- **Condición del límite a cero:**
    
    $$\lim_{n\to\infty} \sin\left(\frac{\pi}{n}\right) = \sin(0) = 0$$
    
    La primera condición se cumple.
    
- **Condición decreciente ($b_{n+1} \le b_n$):**
    
    Para $n=1$, $b_1 = \sin(\pi) = 0$. Para $n=2$, $b_2 = \sin(\pi/2) = 1$. Aquí la serie crece de $n=1$ a $n=2$. Sin embargo, para la convergencia de una serie, solo importa el comportamiento a partir de un cierto término en adelante.
    
    Consideremos la función continua $f(x) = \sin\left(\frac{\pi}{x}\right)$ para $x \ge 2$. Para determinar si es decreciente, evaluamos su derivada:
    
    $$f'(x) = \cos\left(\frac{\pi}{x}\right) \cdot \left(-\frac{\pi}{x^2}\right)$$
    
    Para $x \ge 2$, el ángulo $\frac{\pi}{x}$ está en el intervalo $\left(0, \frac{\pi}{2}\right]$, donde el coseno es siempre estrictamente positivo. Como $-\frac{\pi}{x^2}$ es negativo, el producto $f'(x)$ es menor que cero.
    
    Dado que $f'(x) < 0$ para todo $x \ge 2$, la sucesión es estrictamente decreciente a partir del segundo término ($b_{n+1} \le b_n$ para $n \ge 2$).
    

Al cumplirse ambas condiciones (la propiedad decreciente a partir de $n=2$ es suficiente), por el Teorema de la Serie Alternante, la serie **converge**.

**(b)** $\displaystyle \sum_{n=1}^{\infty}(-1)^{n}\cos\left(\frac{\pi}{n}\right)$

Antes de intentar aplicar criterios complejos, siempre es recomendable evaluar la condición necesaria para la convergencia (Criterio de la divergencia del enésimo término), que establece que si $\lim_{n\to\infty} a_n \neq 0$, la serie diverge.

Analicemos el límite del término general $a_n = (-1)^{n}\cos\left(\frac{\pi}{n}\right)$. Evaluamos el límite del valor absoluto del término:

$$\lim_{n\to\infty} \left| (-1)^{n}\cos\left(\frac{\pi}{n}\right) \right| = \lim_{n\to\infty} \cos\left(\frac{\pi}{n}\right) = \cos(0) = 1$$

Como el límite del valor absoluto es 1, la sucesión original alternará cerca de $1$ y $-1$ a medida que $n$ crece. En consecuencia, el límite $\lim_{n\to\infty} a_n$ no existe (y claramente no es cero).

Por el Criterio de la Divergencia, la serie **diverge**.

---

### Problema 16: La Convergencia Absoluta Implica Convergencia

**Planteamiento:**

Debemos demostrar que si la serie de los valores absolutos $\sum_{n=1}^{\infty} |a_n|$ converge (convergencia absoluta), entonces la serie original $\sum_{n=1}^{\infty} a_n$ también converge.

**Demostración:**

Consideremos la relación natural que existe entre cualquier número real y su valor absoluto:

$$-|a_n| \le a_n \le |a_n|$$

Si sumamos $|a_n|$ a todas las partes de la desigualdad, obtenemos:

$$0 \le a_n + |a_n| \le 2|a_n|$$

Esto nos permite construir una nueva serie con términos exclusivamente no negativos: $\sum_{n=1}^{\infty} (a_n + |a_n|)$.

Por hipótesis del teorema, sabemos que $\sum_{n=1}^{\infty} |a_n|$ es convergente. Por las propiedades algebraicas de las series, si multiplicamos una serie convergente por una constante, el resultado también converge. Por lo tanto, la serie $\sum_{n=1}^{\infty} 2|a_n|$ es convergente.

Ahora, aplicando el **Criterio de Comparación Directa** a las series de términos no negativos:

Como $0 \le a_n + |a_n| \le 2|a_n|$ para toda $n$, y la serie "mayor" $\sum 2|a_n|$ converge, entonces la serie "menor" $\sum (a_n + |a_n|)$ **también converge**.

Finalmente, podemos expresar el término original $a_n$ algebraicamente como la diferencia de dos términos:

$$a_n = (a_n + |a_n|) - |a_n|$$

Como $\sum_{n=1}^{\infty} a_n$ se puede expresar como la resta de dos series que ya hemos demostrado que son convergentes:

$$\sum_{n=1}^{\infty} a_n = \sum_{n=1}^{\infty} (a_n + |a_n|) - \sum_{n=1}^{\infty} |a_n|$$

Por la propiedad de linealidad de las series (la resta de dos series convergentes resulta en una serie convergente), se concluye de forma definitiva que $\sum_{n=1}^{\infty} a_n$ **es convergente**.

### Problema 17: Demostración del Criterio de la Razón (D'Alembert)

**Planteamiento:**

Sea una serie $\sum_{n=1}^{\infty} a_n$ con términos distintos de cero y definamos $L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right|$.

**(i) Si $L < 1$, la serie es absolutamente convergente:**

Dado que $L < 1$, podemos elegir un número real $r$ tal que $L < r < 1$. Por la definición de límite, existirá un número entero $N$ suficientemente grande tal que, para todo $n \ge N$:

$$\left| \frac{a_{n+1}}{a_n} \right| < r$$

Podemos reescribir esto como $|a_{n+1}| < r|a_n|$. Si evaluamos los términos siguientes a partir de $N$:

$|a_{N+1}| < r|a_N|$

$|a_{N+2}| < r|a_{N+1}| < r^2|a_N|$

$|a_{N+3}| < r|a_{N+2}| < r^3|a_N|$

En general, para cualquier entero $k \ge 1$:

$$|a_{N+k}| < r^k|a_N|$$

La serie de los valores absolutos a partir del índice $N+1$ es $\sum_{k=1}^{\infty} |a_{N+k}|$. Sabemos que está acotada término a término por la serie $\sum_{k=1}^{\infty} |a_N|r^k$. Como $|a_N|$ es una constante y $0 < r < 1$, esta última es una serie geométrica convergente. Por el Criterio de Comparación Directa, la cola de la serie $\sum |a_n|$ converge, lo que implica que toda la serie $\sum |a_n|$ converge. Por tanto, $\sum a_n$ es **absolutamente convergente**.

**(ii) Si $L > 1$ o $L = \infty$, la serie diverge:**

Si el límite es estrictamente mayor que 1 (o infinito), entonces existirá un número entero $N$ a partir del cual todos los términos de la sucesión cumplen:

$$\left| \frac{a_{n+1}}{a_n} \right| > 1 \implies |a_{n+1}| > |a_n|$$

Esto significa que la sucesión de los valores absolutos de los términos, $\{|a_n|\}$, es estrictamente creciente a partir de $N$. Por lo tanto, es imposible que $\lim_{n\to\infty} a_n = 0$.

Por el Criterio de la Divergencia (si el límite del enésimo término no es cero, la serie diverge), la serie $\sum a_n$ es **divergente**.

**(iii) Si $L = 1$, el criterio no es concluyente:**

Para demostrar esto, basta exhibir dos series que den $L=1$, pero donde una converja y la otra diverja.

- _Ejemplo convergente:_ La p-serie $\sum \frac{1}{n^2}$ converge, y su límite es $\lim_{n\to\infty} \frac{n^2}{(n+1)^2} = 1$.
    
- _Ejemplo divergente:_ La serie armónica $\sum \frac{1}{n}$ diverge, y su límite es $\lim_{n\to\infty} \frac{n}{n+1} = 1$.
    
    Esto demuestra que el valor $L=1$ no aporta información suficiente.
    

---

### Problema 18: Demostración del Criterio de la Raíz (Cauchy)

**Planteamiento:**

Sea la serie $\sum_{n=1}^{\infty} a_n$ y definamos $L = \lim_{n\to\infty} \sqrt[n]{|a_n|}$.

**(i) Si $L < 1$, la serie es absolutamente convergente:**

Si $L < 1$, elegimos un número real $r$ tal que $L < r < 1$. Por la definición de límite, existe un entero $N$ tal que para todo $n \ge N$:

$$\sqrt[n]{|a_n|} < r$$

Elevando ambas partes a la enésima potencia (lo cual preserva la desigualdad porque ambas cantidades son positivas), obtenemos:

$$|a_n| < r^n$$

Consideremos la serie formada por estos términos a partir de $N$: $\sum_{n=N}^{\infty} |a_n|$. Cada término es menor que $r^n$. Puesto que $\sum_{n=N}^{\infty} r^n$ es una serie geométrica convergente (ya que $r < 1$), por el Criterio de Comparación Directa, la serie $\sum_{n=N}^{\infty} |a_n|$ también converge. En consecuencia, la serie completa es **absolutamente convergente**.

**(ii) Si $L > 1$ o $L = \infty$, la serie diverge:**

Si $L > 1$, existe un entero $N$ tal que para todo $n \ge N$:

$$\sqrt[n]{|a_n|} > 1 \implies |a_n| > 1^n = 1$$

Como los términos de la serie en valor absoluto son mayores que 1, el límite $\lim_{n\to\infty} a_n$ no puede ser 0. Por el Criterio de la Divergencia del enésimo término, la serie **diverge**.

**(iii) Si $L = 1$, el criterio no es concluyente:**

Igual que en el criterio de la razón, podemos usar:

- $\sum \frac{1}{n^2}$ (convergente): $\lim_{n\to\infty} \sqrt[n]{1/n^2} = \lim_{n\to\infty} \left(n^{-2}\right)^{1/n} = \lim_{n\to\infty} \left(n^{1/n}\right)^{-2} = 1^{-2} = 1$.
    
- $\sum \frac{1}{n}$ (divergente): $\lim_{n\to\infty} \sqrt[n]{1/n} = \lim_{n\to\infty} \left(n^{1/n}\right)^{-1} = 1^{-1} = 1$.
    
    Ambas dan $L=1$ a pesar de tener distintos comportamientos de convergencia.
    

---

### Problema 19: Determinación del Tipo de Convergencia

Para cada serie, determinaremos si es absolutamente convergente, condicionalmente convergente o divergente.

**(a) $\displaystyle \sum_{n=1}^{\infty} \frac{\cos(n\pi/3)}{n!}$**

Primero analizamos la convergencia absoluta aplicando valor absoluto al término general:

$$\left| \frac{\cos(n\pi/3)}{n!} \right| = \frac{|\cos(n\pi/3)|}{n!}$$

Sabemos que la función coseno está acotada entre -1 y 1 para cualquier ángulo, por lo que $|\cos(n\pi/3)| \le 1$. Esto nos permite establecer la desigualdad:

$$\frac{|\cos(n\pi/3)|}{n!} \le \frac{1}{n!}$$

Sabemos que la serie $\sum \frac{1}{n!}$ es convergente (demostrado anteriormente con el Criterio de la Razón). Por el Criterio de Comparación Directa, la serie de los valores absolutos converge.

**Conclusión:** La serie es **absolutamente convergente**.

**(b) $\displaystyle \sum_{n=1}^{\infty} \frac{(-2)^n}{n^n}$**

Analizamos la serie de los valores absolutos: $\sum_{n=1}^{\infty} \left| \frac{(-2)^n}{n^n} \right| = \sum_{n=1}^{\infty} \frac{2^n}{n^n} = \sum_{n=1}^{\infty} \left(\frac{2}{n}\right)^n$.

Aplicamos el **Criterio de la Raíz**:

$$L = \lim_{n\to\infty} \sqrt[n]{\left(\frac{2}{n}\right)^n} = \lim_{n\to\infty} \frac{2}{n} = 0$$

Como $L = 0 < 1$, la serie de los valores absolutos converge por el Criterio de la Raíz.

**Conclusión:** La serie es **absolutamente convergente**.

**(c) $\displaystyle \sum_{n=1}^{\infty} \left(\frac{n^2+1}{2n^2+1}\right)^n$**

Los términos de esta serie ya son estrictamente positivos para todo $n \ge 1$, por lo que converger es equivalente a converger absolutamente.

Aplicamos el **Criterio de la Raíz**:

$$L = \lim_{n\to\infty} \sqrt[n]{\left(\frac{n^2+1}{2n^2+1}\right)^n} = \lim_{n\to\infty} \frac{n^2+1}{2n^2+1}$$

Dividiendo numerador y denominador entre $n^2$:

$$L = \lim_{n\to\infty} \frac{1 + \frac{1}{n^2}}{2 + \frac{1}{n^2}} = \frac{1 + 0}{2 + 0} = \frac{1}{2}$$

Dado que $L = \frac{1}{2} < 1$, el criterio dictamina que converge.

**Conclusión:** La serie es **absolutamente convergente**.

**(d) $\displaystyle \sum_{n=2}^{\infty} \left(\frac{-2n}{n+1}\right)^{5n}$**

Analizamos la convergencia absoluta aplicando valor absoluto:

$$|a_n| = \left| \left(\frac{-2n}{n+1}\right)^{5n} \right| = \left(\frac{2n}{n+1}\right)^{5n}$$

Aplicamos el **Criterio de la Raíz** a la serie en valor absoluto:

$$L = \lim_{n\to\infty} \sqrt[n]{\left(\frac{2n}{n+1}\right)^{5n}} = \lim_{n\to\infty} \left(\frac{2n}{n+1}\right)^5$$

Primero evaluamos el límite de la base:

$$\lim_{n\to\infty} \frac{2n}{n+1} = \lim_{n\to\infty} \frac{2}{1 + \frac{1}{n}} = 2$$

Por la continuidad de la función potencia $f(x)=x^5$:

$$L = (2)^5 = 32$$

Como $L = 32 > 1$, la serie no solo no es absolutamente convergente, sino que diverge. (El término general no tiende a cero).

**Conclusión:** La serie es **divergente**.

A continuación se resuelven los problemas del 20 al 32 del taller.

---

### Problema 20: Valores de $k$ para la convergencia

**Planteamiento:**

Determinar para cuáles enteros positivos $k$ la serie $\displaystyle \sum_{n=1}^{\infty} \frac{(n!)^2}{(kn)!}$ es convergente.

**Resolución:**

Aplicaremos el **Criterio de la Razón**. Sea $a_n = \frac{(n!)^2}{(kn)!}$.

Evaluamos el límite $L = \displaystyle \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right|$:

$$a_{n+1} = \frac{((n+1)!)^2}{(k(n+1))!} = \frac{(n+1)^2 (n!)^2}{(kn+k)!}$$

$$\frac{a_{n+1}}{a_n} = \frac{(n+1)^2 (n!)^2}{(kn+k)!} \cdot \frac{(kn)!}{(n!)^2} = \frac{(n+1)^2 \cdot (kn)!}{(kn+k)!}$$

Desarrollamos el factorial del denominador: $(kn+k)! = (kn+k)(kn+k-1)\cdots(kn+1)(kn)!$.

Sustituyendo esto en la expresión, se cancela el factor $(kn)!$:

$$\frac{a_{n+1}}{a_n} = \frac{(n+1)^2}{(kn+k)(kn+k-1)\cdots(kn+1)}$$

Analizamos el comportamiento de este cociente para diferentes valores enteros positivos de $k$:

- **Si $k = 1$:** El denominador tiene solo un término adicional: $(n+1)$.
    
    $$L = \lim_{n\to\infty} \frac{(n+1)^2}{n+1} = \lim_{n\to\infty} (n+1) = \infty$$
    
    Como $L > 1$, la serie diverge para $k=1$.
    
- **Si $k = 2$:** El denominador tiene dos términos: $(2n+2)(2n+1)$.
    
    $$L = \lim_{n\to\infty} \frac{n^2+2n+1}{4n^2+6n+2} = \frac{1}{4}$$
    
    Como $L = 1/4 < 1$, la serie converge para $k=2$.
    
- **Si $k \ge 3$:** El polinomio del numerador es de grado 2, pero el polinomio del denominador es de grado $k$ (donde $k \ge 3$). Como el grado del denominador es estrictamente mayor que el del numerador, el límite es:
    
    $$L = 0$$
    
    Como $L = 0 < 1$, la serie converge para todo $k \ge 3$.
    

**Conclusión:** La serie converge para todos los enteros $k \ge 2$.

---

### Problema 21: Convergencia de la Serie Exponencial

**(a) Demostrar que $\displaystyle \sum_{n=0}^{\infty} \frac{x^n}{n!}$ converge para toda $x$.**

Utilizamos el Criterio de la Razón con $a_n = \frac{x^n}{n!}$:

$$L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right| = \lim_{n\to\infty} \left| \frac{x^{n+1}}{(n+1)!} \cdot \frac{n!}{x^n} \right|$$

$$L = \lim_{n\to\infty} \frac{|x|}{n+1}$$

Como $x$ es un número real fijo (constante respecto a $n$), a medida que $n$ crece sin límite, el cociente tiende a cero:

$$L = 0$$

Dado que $L = 0 < 1$ independientemente del valor de $x$, la serie es absolutamente convergente para cualquier $x \in \mathbb{R}$.

**(b) Deducir que $\displaystyle \lim_{n\to\infty} \frac{x^n}{n!} = 0$ para toda $x$.**

Existe un teorema fundamental en el estudio de las series (Criterio de divergencia del enésimo término) que establece: si una serie $\sum a_n$ es convergente, entonces obligatoriamente el límite de su término general cuando $n \to \infty$ debe ser cero ($\lim a_n = 0$).

Como en el inciso (a) demostramos que la serie $\sum \frac{x^n}{n!}$ converge para todo número real $x$, se deduce directamente por este teorema que su término general debe tender a cero:

$$\lim_{n\to\infty} \frac{x^n}{n!} = 0 \quad \text{para toda } x.$$

---

### Problema 22: Serie Definida Recursivamente

**Planteamiento:**

Tenemos $a_1 = 2$ y $a_{n+1} = \frac{5n+1}{4n+3} a_n$. Determinar si $\sum a_n$ converge.

**Resolución:**

La definición recursiva nos da directamente la expresión para aplicar el Criterio de la Razón:

$$\frac{a_{n+1}}{a_n} = \frac{5n+1}{4n+3}$$

Dado que $a_1 > 0$ y el factor $\frac{5n+1}{4n+3} > 0$ para todo $n \ge 1$, todos los términos $a_n$ son positivos, por lo que podemos prescindir del valor absoluto en el límite:

$$L = \lim_{n\to\infty} \frac{a_{n+1}}{a_n} = \lim_{n\to\infty} \frac{5n+1}{4n+3}$$

Dividiendo numerador y denominador entre $n$:

$$L = \lim_{n\to\infty} \frac{5 + \frac{1}{n}}{4 + \frac{3}{n}} = \frac{5}{4}$$

Como $L = \frac{5}{4} > 1$, por el Criterio de la Razón, la serie **diverge**.

---

### Problema 23: Dominio de la Función de Bessel $J_0(x)$

**Planteamiento:**

El dominio de una función definida mediante una serie de potencias es el conjunto de valores de $x$ para los cuales la serie converge.

$$J_0(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{2^{2n} (n!)^2}$$

**Resolución:**

Aplicamos el Criterio de la Razón a la serie en valor absoluto, sea $a_n = \frac{(-1)^n x^{2n}}{2^{2n} (n!)^2}$:

$$L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right| = \lim_{n\to\infty} \left| \frac{x^{2(n+1)}}{2^{2(n+1)} ((n+1)!)^2} \cdot \frac{2^{2n} (n!)^2}{x^{2n}} \right|$$

$$L = \lim_{n\to\infty} \left| \frac{x^{2n+2}}{x^{2n}} \cdot \frac{2^{2n}}{2^{2n+2}} \cdot \frac{(n!)^2}{((n+1)!)^2} \right|$$

$$L = \lim_{n\to\infty} \frac{|x|^2}{2^2 \cdot (n+1)^2} = \frac{|x|^2}{4} \lim_{n\to\infty} \frac{1}{(n+1)^2}$$

Para cualquier valor real fijado de $x$, el límite es:

$$L = \frac{|x|^2}{4} \cdot 0 = 0$$

Puesto que $L = 0 < 1$ para todo número real $x$, la serie converge en todas partes.

**Conclusión:** El dominio de $J_0(x)$ es $(-\infty, \infty)$ o $\mathbb{R}$.

---

### Problema 24: Teorema del Radio de Convergencia

**Demostración:**

Supongamos que la serie de potencias $\sum c_n (x-a)^n$ converge para un valor $x = x_0$ (con $x_0 \neq a$). Por el teorema de divergencia, el límite de su término general debe ser cero: $\lim c_n (x_0-a)^n = 0$.

Esto implica que la sucesión está acotada; existe una constante $M > 0$ tal que $|c_n (x_0-a)^n| \le M$ para todo $n$.

Consideremos ahora un punto $x$ que esté más cerca de $a$ que $x_0$, es decir, tal que $|x-a| < |x_0-a|$. Reescribimos el término general evaluado en $x$:

$$|c_n (x-a)^n| = |c_n (x_0-a)^n| \cdot \left| \frac{x-a}{x_0-a} \right|^n \le M \cdot r^n$$

donde $r = \left| \frac{x-a}{x_0-a} \right|$. Como $|x-a| < |x_0-a|$, tenemos que $0 \le r < 1$.

La serie $\sum M r^n$ es una serie geométrica convergente. Por el Criterio de Comparación Directa, la serie original $\sum |c_n (x-a)^n|$ converge absolutamente para todo $x$ tal que $|x-a| < |x_0-a|$.

Este resultado (Lema de Abel) garantiza que el conjunto de convergencia es un intervalo centrado en $a$. Si definimos $R$ como el supremo (la cota superior mínima) de las distancias $|x-a|$ para las cuales la serie converge, nos enfrentamos lógicamente a tres escenarios exclusivos:

1. El supremo es $0$: La serie solo converge en su "centro" trivial, $x=a$. **(Caso i)**
    
2. El supremo es infinito: No hay cota, converge para cualquier $x$. **(Caso ii)**
    
3. El supremo es un número finito positivo $R$: Converge absolutamente cuando $|x-a| < R$ y diverge cuando $|x-a| > R$ (pues si convergiera más allá, $R$ no sería el supremo). **(Caso iii)**
    

---

### Problema 25: Radio e Intervalo de Convergencia

**(a) $\displaystyle \sum_{n=0}^{\infty} \frac{(x-2)^n}{n^2+1}$**

Aplicamos el Criterio de la Razón:

$$L = \lim_{n\to\infty} \left| \frac{(x-2)^{n+1}}{(n+1)^2+1} \cdot \frac{n^2+1}{(x-2)^n} \right| = |x-2| \lim_{n\to\infty} \frac{n^2+1}{n^2+2n+2} = |x-2|$$

Para la convergencia, exigimos $L < 1$, por lo que $|x-2| < 1$. El **radio de convergencia es $R = 1$**.

Esto nos da un intervalo abierto $(1, 3)$. Analizamos los extremos:

- Si $x = 3$: Obtenemos $\sum \frac{1^n}{n^2+1} = \sum \frac{1}{n^2+1}$. Por comparación en el límite con $\sum \frac{1}{n^2}$ (p-serie convergente, $p=2$), esta serie converge.
    
- Si $x = 1$: Obtenemos $\sum \frac{(-1)^n}{n^2+1}$. Como la serie de los valores absolutos converge (acabamos de verlo en $x=3$), esta serie es absolutamente convergente.
    
    **Intervalo de convergencia:** $[1, 3]$.
    

**(b) $\displaystyle \sum_{n=1}^{\infty} \frac{(2x-1)^n}{5^n \sqrt{n}}$**

Aplicamos el Criterio de la Razón:

$$L = \lim_{n\to\infty} \left| \frac{(2x-1)^{n+1}}{5^{n+1} \sqrt{n+1}} \cdot \frac{5^n \sqrt{n}}{(2x-1)^n} \right| = \frac{|2x-1|}{5} \lim_{n\to\infty} \sqrt{\frac{n}{n+1}} = \frac{|2x-1|}{5} \cdot 1 = \frac{|2x-1|}{5}$$

Exigimos $L < 1 \implies |2x-1| < 5 \implies \left|x - \frac{1}{2}\right| < \frac{5}{2}$.

El centro de la serie es $a=1/2$ y el **radio de convergencia es $R = \frac{5}{2}$**.

La desigualdad se traduce en $-5 < 2x-1 < 5 \implies -4 < 2x < 6 \implies -2 < x < 3$. Analizamos los extremos:

- Si $x = 3$: Obtenemos $\sum \frac{5^n}{5^n \sqrt{n}} = \sum \frac{1}{\sqrt{n}}$. Esta es una p-serie con $p=1/2 \le 1$, por lo tanto, diverge.
    
- Si $x = -2$: Obtenemos $\sum \frac{(-5)^n}{5^n \sqrt{n}} = \sum \frac{(-1)^n}{\sqrt{n}}$. Esta es una serie alternante que converge por el Teorema de la Serie Alternante ($1/\sqrt{n}$ es decreciente y tiende a 0).
    
    **Intervalo de convergencia:** $[-2, 3)$.
    

---

### Problema 26: Dominio de la Función de Bessel $J_1(x)$

$$J_1(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{n! (n+1)! \, 2^{2n+1}}$$

Al igual que con $J_0$, buscamos los valores de $x$ donde la serie converja usando el Criterio de la Razón.

$$L = \lim_{n\to\infty} \left| \frac{x^{2(n+1)+1}}{(n+1)! ((n+1)+1)! \, 2^{2(n+1)+1}} \cdot \frac{n! (n+1)! \, 2^{2n+1}}{x^{2n+1}} \right|$$

$$L = \lim_{n\to\infty} \left| \frac{x^{2n+3}}{x^{2n+1}} \cdot \frac{2^{2n+1}}{2^{2n+3}} \cdot \frac{n!}{(n+1)!} \cdot \frac{(n+1)!}{(n+2)!} \right|$$

$$L = \lim_{n\to\infty} \frac{|x|^2}{2^2 \cdot (n+1) \cdot (n+2)} = \frac{|x|^2}{4} \lim_{n\to\infty} \frac{1}{(n+1)(n+2)} = 0$$

Como $L = 0 < 1$ para todo número real $x$, **el dominio es $\mathbb{R}$**.

---

### Problema 27: Dominio de la Función de Airy $A(x)$

$A(x) = 1 + \frac{x^3}{2\cdot 3} + \frac{x^6}{2\cdot 3 \cdot 5 \cdot 6} + \dots$

El término general para $n \ge 1$ se puede escribir como:

$$a_n = \frac{x^{3n}}{2\cdot 3 \cdot 5 \cdot 6 \cdots (3n-1)(3n)}$$

Calculamos la razón entre el término $n+1$ y el término $n$:

$$\left| \frac{a_{n+1}}{a_n} \right| = \left| \frac{x^{3n+3}}{2\cdot 3 \cdots (3n)(3n+2)(3n+3)} \cdot \frac{2\cdot 3 \cdots (3n)}{x^{3n}} \right|$$

Cancelando todos los factores comunes desde 2 hasta $3n$ en el denominador:

$$L = \lim_{n\to\infty} \frac{|x|^3}{(3n+2)(3n+3)} = 0$$

Dado que el límite es cero independientemente del valor de $x$, la serie converge en todos los reales.

**Dominio:** $\mathbb{R}$.

---

### Problema 28: Series de Potencias de Mclaurin/Taylor $(a=0)$

Partiremos de la serie geométrica base, válida para $|x| < 1$:

$$\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n \implies \frac{1}{1+x} = \sum_{n=0}^{\infty} (-1)^n x^n$$

**(a) $f(x) = \dfrac{1}{(1+x)^2}$**

Sabemos que la derivada de $\frac{1}{1+x}$ nos dará un término relacionado.

$$\frac{d}{dx} \left( (1+x)^{-1} \right) = -(1+x)^{-2} = -\frac{1}{(1+x)^2}$$

Derivamos la serie término a término:

$$-\frac{1}{(1+x)^2} = \frac{d}{dx} \sum_{n=0}^{\infty} (-1)^n x^n = \sum_{n=1}^{\infty} (-1)^n n x^{n-1}$$

Multiplicando por $-1$ y reindexando (haciendo $k = n-1 \implies n = k+1$):

$$\frac{1}{(1+x)^2} = \sum_{k=0}^{\infty} (-1)^{-(k+1)} (k+1) x^k = \sum_{n=0}^{\infty} (-1)^{n+1} (n+1) x^n$$

Dado que $(-1)^{n+1} (-1) = (-1)^{n+2} = (-1)^n$, una forma equivalente y más estándar es:

$$\frac{1}{(1+x)^2} = \sum_{n=1}^{\infty} (-1)^{n-1} n x^{n-1} = \sum_{n=0}^{\infty} (-1)^n (n+1) x^n$$

**(b) $f(x) = \dfrac{1}{(1+x)^3}$**

Derivamos nuevamente el resultado de la parte (a):

$$\frac{d}{dx} \left( (1+x)^{-2} \right) = -2(1+x)^{-3} = \frac{-2}{(1+x)^3}$$

Derivamos la serie de la parte (a) término a término:

$$\frac{-2}{(1+x)^3} = \frac{d}{dx} \sum_{n=0}^{\infty} (-1)^n (n+1) x^n = \sum_{n=1}^{\infty} (-1)^n (n+1)n x^{n-1}$$

Reindexamos (haciendo $n \to n+1$):

$$\frac{-2}{(1+x)^3} = \sum_{n=0}^{\infty} (-1)^{n+1} (n+2)(n+1) x^n$$

Dividiendo ambas partes entre $-2$:

$$\frac{1}{(1+x)^3} = \sum_{n=0}^{\infty} \frac{(-1)^n (n+1)(n+2)}{2} x^n$$

**(c) $f(x) = \dfrac{x^2}{(1+x)^3}$**

Basta multiplicar la serie obtenida en (b) por $x^2$:

$$\frac{x^2}{(1+x)^3} = x^2 \sum_{n=0}^{\infty} \frac{(-1)^n (n+1)(n+2)}{2} x^n = \sum_{n=0}^{\infty} \frac{(-1)^n (n+1)(n+2)}{2} x^{n+2}$$

Si queremos expresar la serie donde la potencia de $x$ sea exactamente $n$, reindexamos haciendo $n_{nuevo} = n_{viejo} + 2$ (por tanto, la serie empezará en $n=2$ y sustituimos $n$ por $n-2$):

$$\sum_{n=2}^{\infty} \frac{(-1)^{n-2} (n-1)n}{2} x^n = \sum_{n=2}^{\infty} \frac{(-1)^n (n-1)n}{2} x^n$$

---

### Problema 29: Solución de Ecuación Diferencial mediante Series

**Demostrar que $\displaystyle f(x) = \sum_{n=0}^{\infty} \frac{x^n}{n!}$ cumple $f'(x) = f(x)$:**

Expandiendo la serie tenemos:

$$f(x) = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \cdots$$

Dado que el radio de convergencia de esta serie es infinito (Problema 21), está permitido derivar término a término de manera continua.

$$f'(x) = \frac{d}{dx} \left( 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \frac{x^4}{24} + \cdots \right)$$

$$f'(x) = 0 + 1 + \frac{2x}{2!} + \frac{3x^2}{3!} + \frac{4x^3}{4!} + \cdots$$

$$f'(x) = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$$

Si representamos esto formalmente en notación de suma:

$$f'(x) = \sum_{n=1}^{\infty} \frac{n x^{n-1}}{n!} = \sum_{n=1}^{\infty} \frac{x^{n-1}}{(n-1)!}$$

Haciendo un cambio de índice $k = n - 1$:

$$f'(x) = \sum_{k=0}^{\infty} \frac{x^k}{k!} = f(x)$$

Queda demostrado que $f'(x) = f(x)$.

**Concluir que $f(x) = e^x$:**

De los cursos de ecuaciones diferenciales elementales, sabemos que la única familia de funciones que es su propia derivada (la solución a $\frac{dy}{dx} = y$) adopta la forma general:

$$y(x) = C e^x$$

Para determinar el valor constante $C$, evaluamos nuestra función $f(x)$ expresada como serie en $x = 0$:

$$f(0) = \frac{0^0}{0!} + \frac{0^1}{1!} + \frac{0^2}{2!} + \cdots = 1 + 0 + 0 + \cdots = 1$$

(Por convención en series de potencias, $0^0 = 1$).

Sustituimos esto en la solución general:

$$1 = C e^0 \implies 1 = C(1) \implies C = 1$$

Por lo tanto, la función representada por la serie de potencias es exactamente la función exponencial:

$$f(x) = e^x \quad \text{para toda } x \in \mathbb{R}.$$

---
---
**Demostraciones**

---

### 30. Teorema de las series de Taylor (coeficientes)

**Hipótesis:**  
Para $|x-a|<R$ se tiene  
$$
f(x) = \sum_{n=0}^{\infty} c_n (x-a)^n.
$$  
La serie de potencias converge (absolutamente) en ese intervalo, por lo que se puede derivar término a término.

**Demostración:**  
Derivamos sucesivamente:  

$$
f'(x) = \sum_{n=1}^{\infty} n c_n (x-a)^{n-1},\quad
f''(x) = \sum_{n=2}^{\infty} n(n-1) c_n (x-a)^{n-2},\quad \ldots
$$  
Evaluando en $x=a$ obtenemos:  

$$
f(a) = c_0,\quad f'(a)=1\cdot c_1,\quad f''(a)=2\cdot1\cdot c_2,\quad \ldots,\quad f^{(n)}(a)=n!\,c_n.
$$  
Por lo tanto,  
$$
c_n = \frac{f^{(n)}(a)}{n!},\qquad n=0,1,2,\dots
$$

---

### 31. Serie binomial

**Teorema:** Para cualquier número real $k$ y $|x|<1$,  
$$
(1+x)^k = \sum_{n=0}^{\infty} \binom{k}{n} x^n,
\qquad\text{donde}\quad
\binom{k}{n}=\frac{k(k-1)\cdots(k-n+1)}{n!}.
$$

**Demostración:**  
Definimos $f(x)=(1+x)^k$. Su serie de Taylor en $x=0$ es  
$$
f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n.
$$  
Calculamos $f^{(n)}(0)=k(k-1)\cdots(k-n+1)$. Así los coeficientes son $\binom{k}{n}$.  
Radio de convergencia: Aplicando el criterio del cociente a la serie $\sum a_n x^n$ con $a_n=\binom{k}{n}$:  
$$
\left|\frac{a_{n+1}}{a_n}\right| = \left|\frac{k-n}{n+1}\right| \to 1 \quad (n\to\infty).
$$  
Por tanto, el radio es $R=1$. Para $|x|<1$ la serie converge absolutamente.  
Ahora, sea $g(x)=\sum_{n=0}^{\infty}\binom{k}{n}x^n$. Derivando término a término (válido en $|x|<1$):  
$$
g'(x)=\sum_{n=1}^{\infty}\binom{k}{n}n x^{n-1}
= \sum_{n=1}^{\infty} k\binom{k-1}{n-1}x^{n-1}=k\sum_{m=0}^{\infty}\binom{k-1}{m}x^{m}=k(1+x)^{k-1},
$$  
donde usamos que $n\binom{k}{n}=k\binom{k-1}{n-1}$. Además, $g(0)=1$. La función $h(x)=(1+x)^k$ satisface la misma ecuación diferencial: $h'(x)=k(1+x)^{k-1}$ con $h(0)=1$. Por unicidad de la solución de la EDO lineal de primer orden, $g(x)=h(x)$ para $|x|<1$.

---

### 32. Validez de las expansiones y radios de convergencia

A continuación se demuestra cada serie indicando su origen y el radio de convergencia.

---

#### $\displaystyle \frac{1}{1-x} = \sum_{n=0}^{\infty} x^n,\quad R=1$

Es la serie geométrica. La suma parcial $S_N = 1+x+\cdots+x^{N-1} = \frac{1-x^N}{1-x}$ converge a $\frac{1}{1-x}$ si y solo si $|x|<1$ (pues $x^N\to0$). Si $|x|\ge1$ el término general no tiende a cero, luego diverge. Por tanto, radio $R=1$.

---

#### $\displaystyle e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!},\quad R=\infty$

Para cualquier $x$ fijo, el criterio del cociente da  
$$
\left|\frac{x^{n+1}/(n+1)!}{x^n/n!}\right| = \frac{|x|}{n+1}\to 0 <1,
$$  
luego la serie converge absolutamente para todo $x$. La igualdad con $e^x$ se obtiene del teorema de Taylor con resto de Lagrange:  
$$
e^x = \sum_{k=0}^{n-1}\frac{x^k}{k!} + \frac{e^{\xi}}{n!}x^n,\quad \xi\in(0,x),
$$  
y el resto tiende a cero cuando $n\to\infty$ para cada $x$ fijo.

---

#### $\displaystyle \sin x = \sum_{n=0}^{\infty} (-1)^n\frac{x^{2n+1}}{(2n+1)!},\quad R=\infty$

Similar a $e^x$: el criterio del cociente da  
$$
\left|\frac{(-1)^{n+1}x^{2n+3}/(2n+3)!}{(-1)^n x^{2n+1}/(2n+1)!}\right| = \frac{x^2}{(2n+3)(2n+2)}\to 0,
$$  
radio infinito. La igualdad se demuestra mediante la serie de Taylor de $\sin x$ o usando la representación compleja $\sin x = \frac{e^{ix}-e^{-ix}}{2i}$ y las series de $e^{ix}$.

---

#### $\displaystyle \cos x = \sum_{n=0}^{\infty} (-1)^n\frac{x^{2n}}{(2n)!},\quad R=\infty$

Análogo al seno. Se obtiene derivando la serie del seno o directamente del desarrollo de Taylor.

---

#### $\displaystyle \arctan x = \sum_{n=0}^{\infty} (-1)^n\frac{x^{2n+1}}{2n+1},\quad R=1$

Sabemos que $\frac{d}{dx}\arctan x = \frac{1}{1+x^2}$. Para $|x|<1$,  
$$
\frac{1}{1+x^2} = \sum_{n=0}^{\infty} (-1)^n x^{2n}
$$  
(serie geométrica con $-x^2$). Integrando término a término desde 0 hasta $x$ (válido dentro del radio de convergencia):  
$$
\arctan x = \int_0^x \frac{dt}{1+t^2} = \sum_{n=0}^{\infty} (-1)^n \int_0^x t^{2n} dt = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}.
$$  
Para $|x|=1$ la serie converge condicionalmente (criterio de Leibniz), pero la igualdad se extiende por continuidad. El radio de convergencia es 1 porque el término general en valor absoluto es $1/(2n+1)$ que no tiende a cero rápidamente; el criterio del cociente da límite 1.

---

#### $\displaystyle \ln(1+x) = \sum_{n=1}^{\infty} (-1)^{n-1}\frac{x^n}{n},\quad R=1$

Derivamos: $\frac{d}{dx}\ln(1+x)=\frac{1}{1+x}$. Para $|x|<1$,  
$$
\frac{1}{1+x} = \sum_{n=0}^{\infty} (-1)^n x^n.
$$  
Integrando desde 0 hasta $x$:  
$$
\ln(1+x) = \int_0^x \frac{dt}{1+t} = \sum_{n=0}^{\infty} (-1)^n \frac{x^{n+1}}{n+1} = \sum_{n=1}^{\infty} (-1)^{n-1}\frac{x^n}{n}.
$$  
El radio es 1 por el criterio del cociente (límite 1) o porque la serie armónica alternada converge en $x=1$ pero la serie armónica diverge en $x=-1$.

---

#### $\displaystyle (1+x)^k = \sum_{n=0}^{\infty} \binom{k}{n} x^n,\quad R=1$

Esta es la serie binomial ya demostrada en el punto 31. El radio de convergencia es 1 (salvo para $k$ entero no negativo, donde la serie es finita y converge para todo $x$). Para $|x|<1$ converge absolutamente; en los extremos depende de $k$.

---
