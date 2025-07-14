### Problema 32: Teorema de Ehrenfest
El teorema de Ehrenfest establece que las ecuaciones de evolución temporal para los valores esperados de la posición y el momento en mecánica cuántica son análogas a las ecuaciones de Hamilton en mecánica clásica. Para un hamiltoniano $$\hat{H} = \frac{\hat{p}^2}{2m} + V(\hat{x})$$, las ecuaciones son:
$$
\frac{d}{dt} \langle \hat{x} \rangle = \frac{\langle \hat{p} \rangle}{m}, \quad \frac{d}{dt} \langle \hat{p} \rangle = - \left\langle \frac{\partial V}{\partial x} \right\rangle.
$$

**Demostración:**  
La evolución temporal del valor esperado de un operador $$\hat{A}$$ que no depende explícitamente del tiempo está dada por:
$$
\frac{d}{dt} \langle \hat{A} \rangle = \frac{i}{\hbar} \langle [\hat{H}, \hat{A}] \rangle.
$$

- Para $$\langle \hat{x} \rangle$$:
  $$
  [\hat{H}, \hat{x}] = \left[ \frac{\hat{p}^2}{2m}, \hat{x} \right] + [V(\hat{x}), \hat{x}].
  $$
  El segundo término es cero. Usando $$[\hat{p}, \hat{x}] = -i\hbar$$:
  $$
  [\hat{p}^2, \hat{x}] = \hat{p}[\hat{p}, \hat{x}] + [\hat{p}, \hat{x}]\hat{p} = \hat{p}(-i\hbar) + (-i\hbar)\hat{p} = -2i\hbar \hat{p},
  $$
  $$
  \left[ \frac{\hat{p}^2}{2m}, \hat{x} \right] = \frac{1}{2m} (-2i\hbar \hat{p}) = -\frac{i\hbar}{m} \hat{p}.
  $$
  Entonces:
  $$
  \frac{d}{dt} \langle \hat{x} \rangle = \frac{i}{\hbar} \left\langle -\frac{i\hbar}{m} \hat{p} \right\rangle = \frac{\langle \hat{p} \rangle}{m}.
  $$

- Para $$\langle \hat{p} \rangle$$:
  $$
  [\hat{H}, \hat{p}] = \left[ \frac{\hat{p}^2}{2m}, \hat{p} \right] + [V(\hat{x}), \hat{p}].
  $$
  El primer término es cero. En representación de coordenadas, $$\hat{p} = -i\hbar \frac{d}{dx}$$, y:
  $$
  [V(\hat{x}), \hat{p}] \psi = i\hbar \frac{dV}{dx} \psi \implies [V(\hat{x}), \hat{p}] = i\hbar \frac{dV}{dx}(\hat{x}).
  $$
  Entonces:
  $$
  \frac{d}{dt} \langle \hat{p} \rangle = \frac{i}{\hbar} \left\langle i\hbar \frac{dV}{dx}(\hat{x}) \right\rangle = - \left\langle \frac{\partial V}{\partial x} \right\rangle.
  $$

Así, se demuestran las ecuaciones de Ehrenfest.

---

### Problema 33: Operadores de creación y destrucción
#### (a) Demostraciones:
**(i)** $$[\hat{a}, \hat{a}^\dagger] = 1$$  
Definimos $$\alpha = \sqrt{\frac{m\eta}{\hbar}}$$, $$\beta = \frac{1}{\sqrt{m\hbar\eta}}$$, así que $$\hat{a} = \frac{1}{\sqrt{2}} (\alpha \hat{x} + i \beta \hat{p})$$, $$\hat{a}^\dagger = \frac{1}{\sqrt{2}} (\alpha \hat{x} - i \beta \hat{p})$$.  
Calculamos:
$$
\hat{a} \hat{a}^\dagger = \frac{1}{2} (\alpha \hat{x} + i \beta \hat{p})(\alpha \hat{x} - i \beta \hat{p}) = \frac{1}{2} \left[ \alpha^2 \hat{x}^2 + \alpha \beta \hbar + \beta^2 \hat{p}^2 \right],
$$
$$
\hat{a}^\dagger \hat{a} = \frac{1}{2} (\alpha \hat{x} - i \beta \hat{p})(\alpha \hat{x} + i \beta \hat{p}) = \frac{1}{2} \left[ \alpha^2 \hat{x}^2 - \alpha \beta \hbar + \beta^2 \hat{p}^2 \right].
$$
El conmutador es:
$$
[\hat{a}, \hat{a}^\dagger] = \hat{a} \hat{a}^\dagger - \hat{a}^\dagger \hat{a} = \frac{1}{2} (2 \alpha \beta \hbar) = \alpha \beta \hbar.
$$
Como $$\alpha \beta = \frac{1}{\hbar}$$, entonces $$[\hat{a}, \hat{a}^\dagger] = 1$$.

**(ii)** Con $$\hat{N} = \hat{a}^\dagger \hat{a}$$:  
- $$[\hat{N}, \hat{a}] = \hat{N} \hat{a} - \hat{a} \hat{N}$$. Usando $$\hat{a} \hat{a}^\dagger = \hat{a}^\dagger \hat{a} + 1$$:
  $$
  \hat{a} \hat{N} = \hat{a} (\hat{a}^\dagger \hat{a}) = (\hat{a}^\dagger \hat{a} + 1) \hat{a} = \hat{N} \hat{a} + \hat{a},
  $$
  $$
  [\hat{N}, \hat{a}] = \hat{N} \hat{a} - (\hat{N} \hat{a} + \hat{a}) = -\hat{a}.
  $$
- $$[\hat{N}, \hat{a}^\dagger}] = \hat{N} \hat{a}^\dagger - \hat{a}^\dagger \hat{N}$$. Usando $$\hat{a} \hat{a}^\dagger = \hat{a}^\dagger \hat{a} + 1$$:
  $$
  \hat{N} \hat{a}^\dagger = \hat{a}^\dagger \hat{a} \hat{a}^\dagger = \hat{a}^\dagger (\hat{a}^\dagger \hat{a} + 1) = \hat{a}^\dagger \hat{N} + \hat{a}^\dagger,
  $$
  $$
  [\hat{N}, \hat{a}^\dagger}] = (\hat{a}^\dagger \hat{N} + \hat{a}^\dagger) - \hat{a}^\dagger \hat{N} = \hat{a}^\dagger.
  $$

**(iii)** $$\frac{\hat{p}^2}{2m} + \frac{1}{2} m \eta^2 \hat{x}^2 = \hbar \eta \left( \hat{N} + \frac{1}{2} \right)$$  
De (i), $$\hat{a} \hat{a}^\dagger = \hat{N} + 1$$. Expresamos:
$$
\hat{a} \hat{a}^\dagger = \frac{1}{2} \left[ \frac{m\eta}{\hbar} \hat{x}^2 + 1 + \frac{1}{m\hbar\eta} \hat{p}^2 \right],
$$
$$
\hat{N} + 1 = \frac{1}{2} \left[ \frac{m\eta}{\hbar} \hat{x}^2 + \frac{1}{m\hbar\eta} \hat{p}^2 + 1 \right].
$$
El hamiltoniano es:
$$
\hat{H} = \frac{\hat{p}^2}{2m} + \frac{1}{2} m \eta^2 \hat{x}^2 = \frac{1}{2} \hbar \eta \left( \frac{m\eta}{\hbar} \hat{x}^2 + \frac{1}{m\hbar\eta} \hat{p}^2 \right).
$$
De la expresión de $$\hat{N} + 1$$:
$$
\frac{m\eta}{\hbar} \hat{x}^2 + \frac{1}{m\hbar\eta} \hat{p}^2 = 2(\hat{N} + 1) - 1 = 2\hat{N} + 1.
$$
Sustituyendo:
$$
\hat{H} = \frac{1}{2} \hbar \eta (2\hat{N} + 1) = \hbar \eta \left( \hat{N} + \frac{1}{2} \right).
$$

#### (b) Estado $$|\varphi_0\rangle$$ tal que $$\hat{a} |\varphi_0\rangle = 0$$  
En representación de coordenadas, $$\hat{x} = x$$, $$\hat{p} = -i\hbar \frac{d}{dx}$$. La ecuación $$\hat{a} \varphi_0(x) = 0$$ es:
$$
\sqrt{\frac{m\eta}{\hbar}} x \varphi_0 + \sqrt{\frac{\hbar}{m\eta}} \frac{d\varphi_0}{dx} = 0 \implies \frac{d\varphi_0}{dx} = -\frac{m\eta}{\hbar} x \varphi_0.
$$
Solución:
$$
\varphi_0(x) = A e^{-\frac{m\eta}{2\hbar} x^2}.
$$
Normalización:
$$
\int_{-\infty}^{\infty} |\varphi_0(x)|^2 dx = A^2 \int_{-\infty}^{\infty} e^{-\frac{m\eta}{\hbar} x^2} dx = A^2 \sqrt{\frac{\pi \hbar}{m\eta}} = 1 \implies A = \left( \frac{m\eta}{\pi \hbar} \right)^{1/4}.
$$
Así:
$$
\varphi_0(x) = \left( \frac{m\eta}{\pi \hbar} \right)^{1/4} e^{-\frac{m\eta}{2\hbar} x^2}.
$$

---

### Problema 34: Valores esperados en oscilador armónico
#### (a) Cálculo en el estado $$|n\rangle$$
- $$\langle \hat{x} \rangle = \langle n | \hat{x} | n \rangle = 0$$, $$\langle \hat{p} \rangle = \langle n | \hat{p} | n \rangle = 0$$, por simetría.
- $$\hat{x} = \sqrt{\frac{\hbar}{2m\eta}} (\hat{a} + \hat{a}^\dagger)$$, $$\hat{p} = -i \sqrt{\frac{\hbar m \eta}{2}} (\hat{a} - \hat{a}^\dagger)$$.
- $$\langle \hat{x}^2 \rangle = \frac{\hbar}{2m\eta} \langle n | (\hat{a} + \hat{a}^\dagger)^2 | n \rangle = \frac{\hbar}{2m\eta} (2n + 1)$$.
- $$\langle \hat{p}^2 \rangle = -\frac{\hbar m \eta}{2} \langle n | (\hat{a} - \hat{a}^\dagger)^2 | n \rangle = \frac{\hbar m \eta}{2} (2n + 1)$$.
- $$\langle \hat{K} \rangle = \left\langle \frac{\hat{p}^2}{2m} \right\rangle = \frac{1}{2m} \cdot \frac{\hbar m \eta}{2} (2n + 1) = \frac{\hbar \eta}{2} \left(n + \frac{1}{2}\right)$$.
- $$\langle V \rangle = \left\langle \frac{1}{2} m \eta^2 \hat{x}^2 \right\rangle = \frac{1}{2} m \eta^2 \cdot \frac{\hbar}{2m\eta} (2n + 1) = \frac{\hbar \eta}{2} \left(n + \frac{1}{2}\right)$$.

#### (b) $$\Delta x \Delta p = \hbar \left(n + \frac{1}{2}\right)$$ y estado base
- $$\Delta x = \sqrt{\langle \hat{x}^2 \rangle - \langle \hat{x} \rangle^2} = \sqrt{\frac{\hbar}{2m\eta} (2n + 1)}$$, $$\Delta p = \sqrt{\langle \hat{p}^2 \rangle - \langle \hat{p} \rangle^2} = \sqrt{\frac{\hbar m \eta}{2} (2n + 1)}$$.
- $$\Delta x \Delta p = \sqrt{ \frac{\hbar}{2m\eta} (2n + 1) \cdot \frac{\hbar m \eta}{2} (2n + 1) } = \frac{\hbar}{2} (2n + 1) = \hbar \left(n + \frac{1}{2}\right)$$.
- Para $$n=0$$, $$\Delta x \Delta p = \frac{\hbar}{2}$$, que es el mínimo permitido por el principio de incertidumbre, ya que el estado base es gaussiano y satura la desigualdad.

---

### Problema 35: Evolución temporal en oscilador armónico
Estado inicial normalizado: $$|\psi(0)\rangle = \frac{1}{\sqrt{5}} (|0\rangle + 2 |1\rangle)$$. Energías: $$E_n = \hbar \eta \left(n + \frac{1}{2}\right)$$.

#### (a) Probabilidad de medir $$E_n$$ en tiempo $$t$$
- $$|\psi(t)\rangle = \frac{1}{\sqrt{5}} \left( e^{-i \eta t / 2} |0\rangle + 2 e^{-i 3\eta t / 2} |1\rangle \right)$$.
- Probabilidad $$P(E_n) = |\langle n | \psi(t) \rangle|^2$$:
  - $$n=0$$: $$|\langle 0 | \psi(t) \rangle|^2 = \left| \frac{1}{\sqrt{5}} e^{-i \eta t / 2} \right|^2 = \frac{1}{5}$$.
  - $$n=1$$: $$|\langle 1 | \psi(t) \rangle|^2 = \left| \frac{2}{\sqrt{5}} e^{-i 3\eta t / 2} \right|^2 = \frac{4}{5}$$.
  - $$n \geq 2$$: 0.

#### (b) $$\mathcal{P}(t) = | \langle \psi(0) | \psi(t) \rangle |^2$$
$$
\langle \psi(0) | \psi(t) \rangle = \frac{1}{5} \left( e^{-i \eta t / 2} + 4 e^{-i 3\eta t / 2} \right).
$$
$$
| \langle \psi(0) | \psi(t) \rangle |^2 = \frac{1}{25} \left| e^{-i \theta} + 4 e^{-i 3\theta} \right|^2, \quad \theta = \eta t / 2.
$$
$$
\left| e^{-i\theta} + 4 e^{-i 3\theta} \right|^2 = (e^{-i\theta} + 4 e^{-i 3\theta})(e^{i\theta} + 4 e^{i 3\theta}) = 17 + 8 \cos(2\theta) = 17 + 8 \cos(\eta t).
$$
Así:
$$
\mathcal{P}(t) = \frac{1}{25} (17 + 8 \cos(\eta t)).
$$
- **Gráfica e interpretación:** Función oscilatoria con periodo $$T = \frac{2\pi}{\eta}$$ (periodo clásico), entre $$\frac{9}{25}$$ y 1. Representa la probabilidad de que el estado en $$t$$ coincida con el estado inicial, mostrando revivals periódicos.

#### (c) $$\langle \hat{x}(t) \rangle$$ y $$\langle \hat{p}(t) \rangle$$
- $$\hat{x} = \sqrt{\frac{\hbar}{2m\eta}} (\hat{a} + \hat{a}^\dagger)$$.
- $$\langle \hat{a} \rangle = \langle \psi(t) | \hat{a} | \psi(t) \rangle = \frac{2}{5} e^{-i \eta t}$$, $$\langle \hat{a}^\dagger \rangle = \frac{2}{5} e^{i \eta t}$$.
- $$\langle \hat{a} + \hat{a}^\dagger \rangle = \frac{4}{5} \cos(\eta t)$$.
- $$\langle \hat{x}(t) \rangle = \sqrt{\frac{\hbar}{2m\eta}} \cdot \frac{4}{5} \cos(\eta t) = \frac{4}{5} \sqrt{\frac{\hbar}{2m\eta}} \cos(\eta t)$$.
- $$\langle \hat{p}(t) \rangle = -i \sqrt{\frac{\hbar m \eta}{2}} \langle \hat{a} - \hat{a}^\dagger \rangle = -i \sqrt{\frac{\hbar m \eta}{2}} \left( -\frac{4i}{5} \sin(\eta t) \right) = -\frac{4}{5} \sqrt{\frac{\hbar m \eta}{2}} \sin(\eta t)$$.

#### (d) Teorema de Ehrenfest y comparación
- Ecuaciones:
  $$
  \frac{d}{dt} \langle \hat{x} \rangle = \frac{\langle \hat{p} \rangle}{m}, \quad \frac{d}{dt} \langle \hat{p} \rangle = -m \eta^2 \langle \hat{x} \rangle.
  $$
- De (c):
  $$
  \frac{d}{dt} \langle \hat{x} \rangle = -\frac{4}{5} \sqrt{\frac{\hbar}{2m\eta}} \eta \sin(\eta t), \quad \frac{\langle \hat{p} \rangle}{m} = -\frac{4}{5} \sqrt{\frac{\hbar}{2m\eta}} \eta \sin(\eta t).
  $$
  Coincide. Similarmente para $$\langle \hat{p} \rangle$$.

---

### Problema 36: Polinomios de Hermite
#### (a) Demostración de equivalencia
$$
H_n(y) := e^{y^2/2} \left( y - \frac{d}{dy} \right)^n e^{-y^2/2} = (-1)^n e^{y^2} \frac{d^n}{dy^n} e^{-y^2}.
$$
Definimos el operador $$\hat{A} = y - \frac{d}{dy}$$. Se cumple:
$$
\hat{A} = - e^{y^2/2} \frac{d}{dy} e^{-y^2/2}.
$$
Entonces:
$$
\hat{A}^n = (-1)^n \left( e^{y^2/2} \frac{d}{dy} e^{-y^2/2} \right)^n = (-1)^n e^{y^2/2} \frac{d^n}{dy^n} e^{-y^2/2}.
$$
Sustituyendo:
$$
H_n(y) = e^{y^2/2} \hat{A}^n e^{-y^2/2} = (-1)^n e^{y^2} \frac{d^n}{dy^n} e^{-y^2}.
$$

#### (b) Polinomios
- $$H_0(y) = 1$$.
- $$H_1(y) = (-1) e^{y^2} \frac{d}{dy} e^{-y^2} = 2y$$.
- $$H_2(y) = e^{y^2} \frac{d^2}{dy^2} e^{-y^2} = 4y^2 - 2$$.
- $$H_3(y) = -e^{y^2} \frac{d^3}{dy^3} e^{-y^2} = 8y^3 - 12y$$.

#### (c) Ortogonalidad
$$
\int_{-\infty}^{\infty} e^{-y^2} H_n(y) H_m(y)  dy = 2^n n! \sqrt{\pi}  \delta_{nm}.
$$
Usando la función generatriz $$G(y,t) = e^{2yt - t^2} = \sum_{n=0}^{\infty} \frac{H_n(y) t^n}{n!}$$:
$$
\int_{-\infty}^{\infty} e^{-y^2} G(y,t) G(y,s) dy = e^{2ts} \sqrt{\pi} = \sum_{k=0}^{\infty} \frac{(2ts)^k}{k!} \sqrt{\pi}.
$$
Comparando coeficientes de $$t^n s^m$$:
$$
\frac{1}{n! m!} \int e^{-y^2} H_n H_m dy = \delta_{nm} \frac{2^n}{n!} \sqrt{\pi} \implies \int e^{-y^2} H_n H_m dy = 2^n n! \sqrt{\pi} \delta_{nm}.
$$

#### (d) Ecuación diferencial
$$
\left[ \frac{d^2}{dy^2} - 2y \frac{d}{dy} + 2n \right] H_n(y) = 0.
$$
Usando las relaciones de recurrencia:
- $$\frac{d}{dy} H_n = 2n H_{n-1}$$.
- $$H_{n+1} = 2y H_n - 2n H_{n-1}$$.
Sustituyendo:
$$
\frac{d^2 H_n}{dy^2} = 4n(n-1) H_{n-2}, \quad -2y \frac{d H_n}{dy} = -4n y H_{n-1}.
$$
Usando $$y H_{n-1} = \frac{1}{2} H_n + (n-1) H_{n-2}$$:
$$
\frac{d^2 H_n}{dy^2} - 2y \frac{d H_n}{dy} + 2n H_n = 4n(n-1) H_{n-2} - 4n \left( \frac{1}{2} H_n + (n-1) H_{n-2} \right) + 2n H_n = 0.
$$

---
### Problema 36: Polinomios de Hermite (Parte b completa)

**Deducción explícita de $$H_n(y)$$ usando $$H_n(y) = (-1)^n e^{y^2} \frac{d^n}{dy^n} e^{-y^2}$$:**

1. **Cálculo de $$H_0(y)$$:**  
   $$
   H_0(y) = (-1)^0 e^{y^2} \frac{d^0}{dy^0} e^{-y^2} = e^{y^2} \cdot e^{-y^2} = \boxed{1}.
   $$

2. **Cálculo de $$H_1(y)$$:**  
   $$
   \frac{d}{dy} e^{-y^2} = -2y e^{-y^2} \implies H_1(y) = (-1)^1 e^{y^2} \left(-2y e^{-y^2}\right) = -(-2y) = \boxed{2y}.
   $$

3. **Cálculo de $$H_2(y)$$:**  
   $$
   \frac{d^2}{dy^2} e^{-y^2} = \frac{d}{dy} \left(-2y e^{-y^2}\right) = -2e^{-y^2} + 4y^2 e^{-y^2} = e^{-y^2} (4y^2 - 2)
   $$
   $$
   H_2(y) = (-1)^2 e^{y^2} \left[e^{-y^2} (4y^2 - 2)\right] = \boxed{4y^2 - 2}.
   $$

4. **Cálculo de $$H_3(y)$$:**  
   $$
   \frac{d^3}{dy^3} e^{-y^2} = \frac{d}{dy} \left[e^{-y^2} (4y^2 - 2)\right] = e^{-y^2} (-8y^3 + 12y)
   $$
   $$
   H_3(y) = (-1)^3 e^{y^2} \left[e^{-y^2} (-8y^3 + 12y)\right] = -(-8y^3 + 12y) = \boxed{8y^3 - 12y}.
   $$

**Resultados finales:**  
$$
\boxed{
\begin{array}{c}
H_0(y) = 1 \\
H_1(y) = 2y \\
H_2(y) = 4y^2 - 2 \\
H_3(y) = 8y^3 - 12y \\
\end{array}
}
$$