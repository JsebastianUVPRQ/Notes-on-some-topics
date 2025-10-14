
1. Una partícula de masa $m$ se mueve sin fricción sobre la superficie $z = r^2$ (coordenadas cilíndricas), donde $z$ s la dirección vertical.
   a) Encuentre la condición de estabilidad de una órbita circular de radio $r_0$ sobre esta superficie.
   b) Encuentre la frecuencia de pequeñas oscilaciones radiales alrededor de esta órbita circular.

2. Un cometa de masa $m$e mueve en una trayectoria parabólica alrededor del Sol y cruza la órbita terrestre. Suponga que la órbita terrestre es circular y que está en el mismo plano que la trayectoria del cometa. Encuentre el máximo número de días que esta en el cometa puede permanecer dentro de la órbita de la Tierra.

3. Una partícula se mueve en el potencial $V(r) = \frac{a}{r} + \frac{b}{r^2}$.
   a) Determine la órbita de la partícula.
   b) Dibuje esquemáticamente el potencial efectivo para este sistema.

4. Una partícula con momento angular $l$ describe la órbita $r = a(1 + \cos\theta)$.
   a) Encuentre la fuerza central que produce esta órbita.
   b) Calcule el período de esta órbita.
   c) Determine la energía mínima que debe tener la partícula para escapar de esta órbita.

5. Encuentre la relación entre la distancia radial y el tiempo para un asteroide con energía igual a cero, sujeto a la atracción solar.

6. Una partícula describe la órbita $r = ab^2$, con $a =$ constante. Encuentre la fuerza que causa esta órbita.

7. Se observa que un cometa está a 10^8 km del Sol y se mueve con una velocidad de 50.9 km/s que forma un ángulo de 45° con el radio vector dirigido desde el Sol.
   a) Determine los parámetros $e$ y $q$ de la órbita del cometa.
   b) Calcule el ángulo al cual fue observado el cometa.
   c) Calcule el período del cometa.

8. Una partícula se mueve en el potencial $V(r) = a/r^p + b/r^q$, donde $a$ y $b$ son constantes.
   a) Encuentre los valores de $p$ y $q$ que producen la órbita $r = k\theta^2$, con $k$ constante.
   b) Encuentre los valores de las constantes $a$ y $b$ en ese caso.
   c) Determine y dibuje el potencial efectivo para esta órbita.

9. El perihelio de un asteroide es la mitad del radio de la órbita terrestre alrededor del Sol (supuesta circular), y su velocidad en el perihelio es el doble de la velocidad orbital de la Tierra. Suponga que la órbita de la Tierra se encuentra en el mismo plano que la órbita del asteroide. Ignore los efectos de la Tierra y otros planetas sobre el asteroide.
   a) Encuentre la velocidad del asteroide cuando está cruzando la órbita terrestre.
   b) Determine si el asteroide escapa del sistema solar.

10. La trayectoria de una partícula con momento angular $l$ en un campo central se puede describir por $r = a \cos\theta$.
    a) Encuentre el potencial asociado a esta trayectoria.
    b) Si la partícula se encuentra a una distancia $a$ del centro de atracción, calcule el tiempo que la partícula tarda en caer al centro.
    c) Determine la energía total de la partícula.

11. Una partícula describe una órbita circular bajo la influencia de una fuerza central atractiva $f(r) = -k/r^2$, dirigida hacia un punto fijo en el círculo.
    a) Demuestre que la fuerza debe variar como el inverso de la quinta potencia de la distancia, es decir, $n = 5$.
    b) Demuestre que la energía total de la partícula es cero.
    c) Encuentre el período del movimiento.

12. Una partícula se mueve en una órbita dada por $r = R e^{-\theta}$, donde $R$ y $\alpha$ son constantes.
    a) Encuentre la fuerza que causa esta órbita.
    b) Si la partícula se encuentra inicialmente a una distancia $R$ del centro de atracción, calcule el tiempo que tarda en caer al centro.
    c) ¿Cuáles son revoluciones completa la partícula hasta alcanzar el centro?
13. Una partícula de masa $m$ y momento angular $l$ se mueve en el potencial $V = -k/r^2$.
    a) Encuentre la condición para que la partícula caiga al centro de atracción.
    b) Determine la órbita descrita por la partícula para alcanzar el centro.
14. Considere el movimiento de una partícula de masa $m$ en el potencial $V = kr^{1/2}$.
    a) Encuentre el potencial efectivo para esta partícula.
    b) Encuentre la relación entre el período y el radio $r_0$ de una órbita circular.
# Solución a Problemas de cosenza cap 3

---

## 1. Partícula sobre la superficie $z = r^2$

La Lagrangiana del sistema es:
$$L = \frac{1}{2} m \left[ \dot{r}^2 (1 + 4r^2) + r^2 \dot{\theta}^2 \right] - mg r^2$$
El potencial efectivo $V_{\text{eff}}(r)$ es:
$$V_{\text{eff}}(r) = \frac{\ell^2}{2 m r^2} + mg r^2$$

### a) Condición de estabilidad de una órbita circular

La condición de órbita circular de radio $r_0$ es:
$$\frac{d V_{\text{eff}}}{d r} \bigg|_{r=r_0} = - \frac{\ell^2}{m r_0^3} + 2mg r_0 = 0 \implies \ell^2 = 2 m^2 g r_0^4$$

La estabilidad se determina por la segunda derivada:
$$\frac{d^2 V_{\text{eff}}}{d r^2} \bigg|_{r=r_0} = \frac{3 \ell^2}{m r_0^4} + 2mg$$
Dado que todos los términos son positivos, $\frac{d^2 V_{\text{eff}}}{d r^2} \bigg|_{r=r_0} > 0$.
La órbita circular es **siempre estable**.

### b) Frecuencia de pequeñas oscilaciones radiales

La frecuencia angular $\omega$ para pequeñas oscilaciones alrededor de $r_0$ es:
$$\omega^2 = \frac{1}{m(1 + 4r_0^2)} \left( \frac{d^2 V_{\text{eff}}}{d r^2} \bigg|_{r_0} \right)$$
Sustituyendo $\ell^2 = 2 m^2 g r_0^4$:
$$\omega^2 = \frac{1}{m(1 + 4r_0^2)} (6mg + 2mg) = \frac{8g}{1 + 4r_0^2}$$
La frecuencia de oscilación es:
$$\omega = \sqrt{\frac{8g}{1 + 4r_0^2}}$$

---

## 2. Cometa en trayectoria parabólica cruzando la órbita terrestre

El cometa tiene una órbita parabólica ($E=0$). El máximo tiempo $\Delta t_{\max}$ dentro del radio terrestre ($R$) ocurre cuando el perihelio es $r_{\min} = R/2$.

Usando la Ley de Kepler para la Tierra ($P_T \approx 365.25 \text{ días}$):
$$\Delta t_{\max} = \frac{365.25 \text{ días}}{3\pi}$$
$$\Delta t_{\max} \approx 38.74 \text{ días}$$
El máximo número de días (redondeando al entero) es $\mathbf{39 \text{ días}}$.

---

## 3. Partícula en el potencial $V(r) = \frac{a}{r} + \frac{b}{r^2}$

### a) Determine la órbita de la partícula

La ecuación diferencial de la órbita es:
$$\frac{d^2 u}{d\theta^2} + \left( 1 + \frac{2 m b}{\ell^2} \right) u = - \frac{m a}{\ell^2}$$
Con $\alpha^2 = 1 + \frac{2 m b}{\ell^2}$ y $C = - \frac{m a}{\ell^2}$:
$$r(\theta) = \frac{1}{\frac{C}{\alpha^2} + A \cos(\alpha\theta + \delta)}$$
La órbita es una **cónica** si $b=0$ (donde $\alpha=1$), o una **roseta** con precesión si $b \ne 0$ ($\alpha \ne 1$).

### b) Dibuje esquemáticamente el potencial efectivo

El potencial efectivo es $V_{\text{eff}}(r) = \frac{a}{r} + \frac{B}{r^2}$, donde $B = b + \frac{\ell^2}{2 m} > 0$.

Si $a < 0$ (atracción): El potencial forma un **pozo** con un mínimo en $r_0 = -2B/a$.


---

## 4. Partícula en órbita $r = a(1 + \cos\theta)$

### a) Encuentre la fuerza central que produce esta órbita

Usando la ecuación de Binet, se encuentra:
$$\frac{d^2 u}{d\theta^2} + u = \frac{3 a}{r^2}$$
La fuerza central es:
$$F(r) = - \frac{\ell^2}{m r^2} \left( \frac{3 a}{r^2} \right) = - \frac{k}{r^4}, \quad \text{donde } k = \frac{3 a \ell^2}{m}$$
Es una fuerza **atractiva** inversamente proporcional a la **cuarta potencia** de la distancia.

### b) Calcule el período de esta órbita

El área $A$ de la Cardioide es $A = \frac{3 \pi a^2}{2}$.
El período $T$ es:
$$T = \frac{2m}{\ell} A = \frac{2m}{\ell} \left( \frac{3 \pi a^2}{2} \right) = \frac{3 \pi m a^2}{\ell}$$

### c) Determine la energía mínima que debe tener la partícula para escapar de esta órbita

El potencial es $V(r) = - \frac{a \ell^2}{m r^3}$.
La energía mínima para escapar es $E_{\text{esc}} = V(\infty) = 0$.
La energía total de la órbita dada es $E = 0$.
Por lo tanto, la energía mínima que debe tener la partícula para escapar es **cero** ($E_{\text{esc}} = 0$).

---

## 5. Relación entre la distancia radial y el tiempo para un asteroide con energía igual a cero

Para una órbita parabólica en un potencial newtoniano, la relación entre el tiempo $t$ (desde el perihelio $r_{\min}$) y la distancia radial $r$ es:
$$t(r) = \frac{1}{3} \sqrt{\frac{2 m}{k}} \sqrt{r - r_{\min}} (r + 2 r_{\min})$$
donde $k = G M_{\text{Sol}} m$ y $r_{\min} = \ell^2/(2mk)$.

---

## 6. Partícula describe la órbita $r = a b^2$

**Asumiendo** que la órbita es $\mathbf{r = a/\theta^2}$:
La fuerza central es:
$$F(r) = - \frac{\ell^2}{m r^2} \left( \frac{2}{a} + \frac{1}{r} \right) = - \frac{K_2}{r^2} - \frac{K_3}{r^3}$$
donde $K_2 = \frac{2 \ell^2}{m a}$ y $K_3 = \frac{\ell^2}{m}$.

---

## 7. Observación de un cometa

Datos: $r = 10^8 \text{ km}$, $v = 50.9 \text{ km/s}$, $\gamma = 45^{\circ}$, $\mu = 1.327 \times 10^{11} \text{ km}^3/\text{s}^2$.

### a) Determine los parámetros $e$ y $q$ de la órbita del cometa

1.  **Momento angular por unidad de masa ($h$):** $h = r v \sin\gamma \approx 3.599 \times 10^9 \text{ km}^2/\text{s}$
2.  **Parámetro orbital ($q$):** $q = h^2/\mu$
    $$q \approx \mathbf{9.76 \times 10^7 \text{ km}}$$
3.  **Energía por unidad de masa ($\varepsilon$):** $\varepsilon = \frac{1}{2} v^2 - \frac{\mu}{r} \approx -31.595 \text{ km}^2/\text{s}^2$
4.  **Excentricidad ($e$):** $e = \sqrt{1 + \frac{2 \varepsilon h^2}{\mu^2}}$
    $$e \approx \mathbf{0.9765}$$

### b) Calcule el ángulo al cual fue observado el cometa

Usando $r = \frac{q}{1 + e \cos\theta}$:
$$\cos\theta = \frac{1}{e} \left( \frac{q}{r} - 1 \right) \approx -0.02458$$
$$\theta \approx \mathbf{91.41^\circ}$$

### c) Calcule el período del cometa

1.  **Semieje mayor ($a$):** $a = - \frac{\mu}{2\varepsilon} \approx 2.098 \times 10^9 \text{ km}$
2.  **Período ($P$):** $P = 2 \pi \sqrt{\frac{a^3}{\mu}}$
    $$P \approx 1.656 \times 10^9 \text{ s} \approx \mathbf{52.47 \text{ años}}$$
## 8. Partícula en el potencial $V(r) = a/r^p + b/r^q$ con órbita $r = k\theta^2$

El objetivo es encontrar $p, q, a,$ y $b$ que satisfagan la órbita $\mathbf{r = k\theta^2}$ bajo el potencial $V(r)$.

### 1. Encontrar la Fuerza $F(r)$ de la órbita (Ecuación de Binet)

La ecuación general de Binet para la fuerza central $F(r)$ es:
$$F(r) = - \frac{\ell^2}{m r^2} \left( \frac{d^2 u}{d\theta^2} + u \right)$$
donde $u = 1/r$.

* **Paso 1.1: Calcular derivadas de $u$.**
    Dado $r = k\theta^2$, entonces $u = \frac{1}{k\theta^2}$.
    $$\frac{d u}{d\theta} = - \frac{2}{k\theta^3}$$
    $$\frac{d^2 u}{d\theta^2} = \frac{6}{k\theta^4}$$

* **Paso 1.2: Sustituir en la Ecuación de Binet.**
    $$\frac{d^2 u}{d\theta^2} + u = \frac{6}{k\theta^4} + \frac{1}{k\theta^2} = \frac{6 + \theta^2}{k\theta^4}$$
    Usando $\theta^2 = r/k$:
    $$\frac{d^2 u}{d\theta^2} + u = \frac{6 + r/k}{k (r/k)^2} = \frac{6k}{r^2} + \frac{1}{r}$$

* **Paso 1.3: Expresar la fuerza en términos de $r$.**
    $$F(r) = - \frac{\ell^2}{m r^2} \left( \frac{6k}{r^2} + \frac{1}{r} \right) = - \frac{6 k \ell^2}{m r^4} - \frac{\ell^2}{m r^3}$$

### 2. Encontrar la Fuerza $F(r)$ del Potencial

La fuerza se obtiene derivando el potencial $V(r) = a r^{-p} + b r^{-q}$:
$$F(r) = - \frac{d V}{d r} = a p r^{-(p+1)} + b q r^{-(q+1)}$$

### 3. Comparar y Resolver para $p, q, a, b$

Igualamos las dos expresiones para $F(r)$:
$$a p r^{-(p+1)} + b q r^{-(q+1)} = - \frac{6 k \ell^2}{m} r^{-4} - \frac{\ell^2}{m} r^{-3}$$

#### a) Encuentre los valores de $p$ y $q$
Comparando los exponentes de $r$:
$$\begin{cases} -(p+1) = -4 \implies \mathbf{p = 3} \\ -(q+1) = -3 \implies \mathbf{q = 2} \end{cases}$$

#### b) Encuentre los valores de las constantes $a$ y $b$ en ese caso
Sustituimos $p=3$ y $q=2$ y comparamos los coeficientes:
* **Para $r^{-4}$:** $3 a = - \frac{6 k \ell^2}{m} \implies \mathbf{a = - \frac{2 k \ell^2}{m}}$
* **Para $r^{-3}$:** $2 b = - \frac{\ell^2}{m} \implies \mathbf{b = - \frac{\ell^2}{2 m}}$

#### c) Determine y dibuje el potencial efectivo para esta órbita
El potencial efectivo $V_{\text{eff}}(r)$ es $V_{\text{eff}}(r) = V(r) + \frac{\ell^2}{2 m r^2}$.
$$V_{\text{eff}}(r) = \frac{a}{r^3} + \frac{b}{r^2} + \frac{\ell^2}{2 m r^2}$$
Sustituimos $a$ y $b$:
$$V_{\text{eff}}(r) = \frac{1}{r^3} \left( - \frac{2 k \ell^2}{m} \right) + \frac{1}{r^2} \left( - \frac{\ell^2}{2 m} \right) + \frac{1}{r^2} \left( \frac{\ell^2}{2 m} \right)$$
Los términos $1/r^2$ se cancelan.
$$V_{\text{eff}}(r) = - \frac{2 k \ell^2}{m r^3}$$
Como $k>0$, $\ell \ne 0$ y $m>0$, la constante $C = 2 k \ell^2 / m$ es positiva.
$$\mathbf{V_{\text{eff}}(r) = - \frac{C}{r^3}}$$
Este potencial es siempre negativo y tiende a $-\infty$ cuando $r \to 0$. No hay mínimo, lo que indica que la órbita (espiral) termina en una **caída al centro**. 

---
## 9. Asteroide y órbita terrestre

Datos: $R_T=R$, $V_T=\sqrt{\mu/R}$, $r_{\min}=R/2$, $v_{\min}=2V_T$.

### 1. Determinar la energía $\varepsilon$ del asteroide

La energía por unidad de masa $\varepsilon$ se conserva. La calculamos en el perihelio:
$$\varepsilon = \frac{1}{2} v_{\min}^2 - \frac{\mu}{r_{\min}} = \frac{1}{2} (2 V_T)^2 - \frac{\mu}{R/2} = 2 V_T^2 - \frac{2\mu}{R}$$
Sustituimos $V_T^2 = \mu/R$:
$$\varepsilon = 2 \left( \frac{\mu}{R} \right) - \frac{2\mu}{R} = \mathbf{0}$$
La órbita es **parabólica**.

### a) Encuentre la velocidad del asteroide cuando está cruzando la órbita terrestre
En la órbita terrestre, $r=R$. Usamos la conservación de la energía $\varepsilon = 0$:
$$\frac{1}{2} v_R^2 - \frac{\mu}{R} = 0 \implies v_R^2 = \frac{2\mu}{R}$$
$$v_R = \sqrt{\frac{2\mu}{R}}$$
Como $V_T = \sqrt{\mu/R}$, la velocidad es:
$$\mathbf{v_R = \sqrt{2} V_T}$$

### b) Determine si el asteroide escapa del sistema solar
La condición de escape es $\varepsilon \ge 0$.
Dado que la energía del asteroide es $\mathbf{\varepsilon = 0}$, el asteroide se encuentra en la velocidad de escape (órbita parabólica) y, por lo tanto, **escapa del sistema solar**.

---
## 10. Trayectoria $r = a \cos\theta$ en un campo central

### a) Encuentre el potencial asociado a esta trayectoria

* **Paso 1: Ecuación de Binet.**
    $u = \frac{1}{a} \sec\theta$. Calculamos $\frac{d^2 u}{d\theta^2} + u$:
    $$\frac{d^2 u}{d\theta^2} + u = \frac{2}{a} \sec^3\theta$$
    Sustituimos $\sec\theta = a/r$:
    $$\frac{d^2 u}{d\theta^2} + u = \frac{2}{a} \left( \frac{a}{r} \right)^3 = \frac{2 a^2}{r^3}$$

* **Paso 2: Fuerza $F(r)$.**
    $$F(r) = - \frac{\ell^2}{m r^2} \left( \frac{2 a^2}{r^3} \right) = - \frac{2 a^2 \ell^2}{m r^5}$$

* **Paso 3: Potencial $V(r)$.**
    $$V(r) = - \int F(r) dr = - \int \left( - \frac{2 a^2 \ell^2}{m r^5} \right) dr = - \frac{2 a^2 \ell^2}{m} \left( \frac{r^{-4}}{-4} \right)$$
    $$\mathbf{V(r) = - \frac{a^2 \ell^2}{2 m r^4}}$$

### b) Si la partícula se encuentra a una distancia $a$ del centro de atracción, calcule el tiempo que la partícula tarda en caer al centro

* **Paso 1: Límites angulares.**
    El radio inicial es $r=a$, lo que implica $\cos\theta = 1$, $\mathbf{\theta=0}$.
    La caída al centro es $r=0$, lo que implica $\cos\theta = 0$, $\mathbf{\theta=\pi/2}$.

* **Paso 2: Integración del tiempo.**
    Usamos $dt = \frac{m r^2}{\ell} d\theta$:
    $$T = \frac{m}{\ell} \int_0^{\pi/2} (a \cos\theta)^2 d\theta = \frac{m a^2}{\ell} \int_0^{\pi/2} \cos^2\theta d\theta$$
    $$T = \frac{m a^2}{2\ell} \left[ \theta + \frac{\sin(2\theta)}{2} \right]_0^{\pi/2} = \frac{m a^2}{2\ell} \left( \frac{\pi}{2} \right)$$
    $$\mathbf{T = \frac{\pi m a^2}{4\ell}}$$

### c) Determine la energía total de la partícula

La energía total $E$ se calcula como $E = T_{\text{radial}} + T_{\text{angular}} + V(r)$.
$$E = \frac{a^2 \ell^2}{2 m r^4} + V(r)$$
Sustituimos $V(r)$:
$$E = \frac{a^2 \ell^2}{2 m r^4} - \frac{a^2 \ell^2}{2 m r^4} = \mathbf{0}$$

---
## 11. Órbita circular bajo $f(r) = -k/r^2$ con centro de fuerza en el círculo

La órbita es un círculo de radio $R$ que pasa por el centro de fuerza, de ecuación $\mathbf{r(\theta) = 2R \cos\theta}$.

### a) Demuestre que la fuerza debe variar como el inverso de la quinta potencia de la distancia, es decir, $n=5$

* **Paso 1: Ecuación de Binet para $r = 2R \cos\theta$.**
    El cálculo de $\frac{d^2 u}{d\theta^2} + u$ (similar al Problema 10a) da:
    $$\frac{d^2 u}{d\theta^2} + u = \frac{8 R^2}{r^3}$$

* **Paso 2: Fuerza $F(r)$.**
    $$F(r) = - \frac{\ell^2}{m r^2} \left( \frac{8 R^2}{r^3} \right) = - \frac{8 R^2 \ell^2}{m r^5}$$
    La fuerza es de la forma $F(r) = - C/r^n$ con $\mathbf{n = 5}$.
    (La ley de la fuerza $f(r) = -k/r^2$ es **incorrecta** para esta órbita. La fuerza real es $1/r^5$).

### b) Demuestre que la energía total de la partícula es cero

* **Paso 1: Potencial $V(r)$.**
    Para $F(r) \propto 1/r^5$, el potencial es $V(r) = - \frac{2 R^2 \ell^2}{m r^4}$ (del Problema 10a).

* **Paso 2: Energía $E$.**
    Usamos $E = \frac{4 R^2 \ell^2}{2 m r^4} + V(r)$:
    $$E = \frac{2 R^2 \ell^2}{m r^4} - \frac{2 R^2 \ell^2}{m r^4} = \mathbf{0}$$

### c) Encuentre el período del movimiento

El período $T$ es $T = \frac{2m}{\ell} A$.
El área $A$ del círculo de diámetro $2R$ es $\mathbf{A = \pi R^2}$.
$$T = \frac{2m}{\ell} (\pi R^2) = \mathbf{\frac{2 \pi m R^2}{\ell}}$$

---
## 12. Partícula en órbita $r = R e^{-\theta}$

### a) Encuentre la fuerza que causa esta órbita

* **Paso 1: Ecuación de Binet para $u = \frac{1}{R} e^{\theta}$.**
    $$\frac{d^2 u}{d\theta^2} + u = \frac{1}{R} e^{\theta} + \frac{1}{R} e^{\theta} = \frac{2}{R} e^{\theta}$$
    Sustituimos $e^{\theta} = R/r$:
    $$\frac{d^2 u}{d\theta^2} + u = \frac{2}{R} \left( \frac{R}{r} \right) = \frac{2}{r}$$

* **Paso 2: Fuerza $F(r)$.**
    $$F(r) = - \frac{\ell^2}{m r^2} \left( \frac{2}{r} \right) = \mathbf{- \frac{2 \ell^2}{m r^3}}$$
    La fuerza sigue la **ley del inverso del cubo**.

### b) Si la partícula se encuentra inicialmente a una distancia $R$ del centro de atracción, calcule el tiempo que tarda en caer al centro

* **Límites de integración:** $r=R \implies \theta=0$. $r=0 \implies \theta=\infty$.
* **Tiempo $T$:**
    $$T = \frac{m R^2}{\ell} \int_0^{\infty} e^{-2\theta} d\theta = \frac{m R^2}{\ell} \left[ - \frac{1}{2} e^{-2\theta} \right]_0^{\infty}$$
    $$\mathbf{T = \frac{m R^2}{2\ell}}$$

### c) ¿Cuáles son revoluciones completa la partícula hasta alcanzar el centro?

La partícula cae al centro cuando $\theta \to \infty$. El número de revoluciones es $\frac{\Delta\theta}{2\pi}$.
$$\text{Revoluciones} = \frac{\infty - 0}{2\pi} = \mathbf{\infty}$$

---
## 13. Partícula de masa $m$ y momento angular $\ell$ se mueve en el potencial $V = -k/r^2$

El potencial efectivo es $V_{\text{eff}}(r) = \frac{1}{r^2} \left( \frac{\ell^2}{2 m} - k \right)$.

### a) Encuentre la condición para que la partícula caiga al centro de atracción

La caída al centro ocurre si $V_{\text{eff}}(r) < 0$ para todo $r$, es decir, si $r=0$ es accesible incluso a energía $E=0$.
$$\frac{\ell^2}{2 m} - k < 0 \implies \mathbf{\ell^2 < 2 m k}$$

### b) Determine la órbita descrita por la partícula para alcanzar el centro

Si $\ell^2 < 2mk$, la partícula cae al centro en un número infinito de vueltas. La órbita es una **espiral logarítmica** de la forma:
$$r(\theta) = r_0 e^{- \alpha |\theta|}, \quad \text{donde } \alpha = \frac{\sqrt{2m k - \ell^2}}{\ell}$$

---
## 14. Partícula de masa $m$ en el potencial $V = kr^{1/2}$

### a) Encuentre el potencial efectivo para esta partícula

$$V_{\text{eff}}(r) = V(r) + \frac{\ell^2}{2 m r^2}$$
$$\mathbf{V_{\text{eff}}(r) = k r^{1/2} + \frac{\ell^2}{2 m r^2}}$$

### b) Encuentre la relación entre el período y el radio $r_0$ de una órbita circular

* **Paso 1: Condición de órbita circular.** $\frac{d V_{\text{eff}}}{d r} \bigg|_{r_0} = 0$.
    $$\frac{k}{2 \sqrt{r_0}} - \frac{\ell^2}{m r_0^3} = 0 \implies \ell^2 = \frac{k m}{2} r_0^{5/2}$$

* **Paso 2: Relación de $\dot{\theta}_0$ con $r_0$.**
    $\dot{\theta}_0 = \frac{\ell}{m r_0^2}$.
    $$\dot{\theta}_0 = \frac{\sqrt{\frac{k m}{2}} r_0^{5/4}}{m r_0^2} = \sqrt{\frac{k}{2m}} r_0^{-3/4}$$

* **Paso 3: Período $T$.** $T = \frac{2\pi}{\dot{\theta}_0}$.
    $$T = 2 \pi \sqrt{\frac{2m}{k}} r_0^{3/4}$$
    La relación entre el período y el radio es $\mathbf{T \propto r_0^{3/4}}$.
```