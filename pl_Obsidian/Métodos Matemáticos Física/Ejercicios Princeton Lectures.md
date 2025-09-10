# Chapter 1 - Preliminaries to Complex Analysis
---

# Chapter 2 - Cauchy’s Theorem and Its Applications

---
# Chapter 5 - capítulo 5 - Entire Functions
---
# Ejercicios

1. Dar una demostración diferente de la fórmula de Jensen en el disco unitario utilizando las funciones (llamadas factores de Blaschke) $\psi_\alpha(z) = \frac{\alpha - z}{1 - \overline{\alpha}z}$.
Sugerencia: La función $f/(\psi_{z_1}\cdots\psi_{z_N})$ no se anula en ninguna parte.

2. Encontrar el orden de crecimiento de las siguientes funciones enteras:
   (a) $p(z)$ donde $p$ es un polinomio.
   (b) Mostrar que $\theta_\tau$ es de orden 2 como función de $z$ si $\tau \neq 0$ es fijo con $\text{Im}(\tau) > 0$, donde la función theta de Jacobi es
   $$\Theta(z|\tau) = \sum_{n=-\infty}^{\infty} e^{\pi in^2\tau}e^{2\pi inz}$$
   Otras propiedades de $\Theta$ se estudiarán en el Capítulo 10. Sugerencia: $-n^2t + 2n|z| \leq -n^2t/2$ cuando $t > 0$ y $n \geq 4|z|/t$.

3. Sea $t > 0$ dado y fijo, y defínase $F(z)$ por
   $$F(z) = \prod_{n=1}^{\infty}(1 - e^{-2\pi nt}e^{2\pi iz})$$
   Nótese que el producto define una función entera de $z$.
   
   (a) Mostrar que $|F(z)| \leq Ae^{a|z|^2}$, por lo tanto $F$ es de orden 2.
   
   (b) $F$ se anula exactamente cuando $z = -int + m$ para $n \geq 1$ y $n,m$ enteros. Así, si $z_n$ es una enumeración de estos ceros tenemos
   $$\sum \frac{1}{|z_n|^2} = \infty \quad \text{pero} \quad \sum \frac{1}{|z_n|^{2+\epsilon}} < \infty$$
   Sugerencia: Para probar (a), escríbase $F(z) = F_1(z)F_2(z)$ donde
   $$F_1(z) = \prod_{n=1}^{N}(1 - e^{-2\pi nt}e^{2\pi iz}) \quad \text{y} \quad F_2(z) = \prod_{n=N+1}^{\infty}(1 - e^{-2\pi nt}e^{2\pi iz})$$
   Elíjase $N \approx c|z|$ con $c$ apropiadamente grande. Entonces, puesto que
   $$\left(\sum_{N+1}^{\infty} e^{-2\pi nt}\right)e^{2\pi|z|} \leq 1,$$
   se tiene $|F_2(z)| \leq A$. Sin embargo, $|1 - e^{-2\pi nt}e^{2\pi iz}| \leq 1 + e^{2\pi|z|} \leq 2e^{2\pi|z|}$.
   Así $|F_1(z)| \leq 2^N e^{2\pi N|z|} \leq e^{c'|z|^2}$. Nótese que una variante simple de la función $F$ surge como un factor en la fórmula del producto triple para la función theta de Jacobi $\Theta$, que se tratará en el Capítulo 10.]

4. Mostrar que si $\alpha > 1$, entonces
   $$F_\alpha(z) = \int_{-\infty}^{\infty} e^{-|t|^\alpha}e^{2\pi izt}dt$$
   es una función entera de orden de crecimiento $\alpha/(\alpha-1)$.
   Sugerencia: Mostrar que $-|t|^\alpha + 2\pi|z||t| \leq c|z|^{\alpha/(\alpha-1)}$ considerando los dos casos $|t|^{\alpha-1} \leq A|z|$ y $|t|^{\alpha-1} \geq A|z|$, para una constante $A$ apropiada.

5. Probar la fórmula del producto de Wallis:
   $$\frac{\pi}{2} = \frac{2}{1} \cdot \frac{2}{3} \cdot \frac{4}{3} \cdot \frac{4}{5} \cdots \frac{2m}{2m-1} \cdot \frac{2m}{2m+1} \cdots$$
   Sugerencia: Usar la fórmula del producto para $\sin z$ en $z = \pi/2$.

6. Establecer las siguientes propiedades de los productos infinitos.
   (a) Mostrar que si $\sum |a_n|^2$ converge, entonces el producto $\prod(1+a_n)$ converge a un límite no nulo si y sólo si $\sum a_n$ converge.
   (b) Encontrar un ejemplo de una sucesión de números complejos $\{a_n\}$ tal que $\sum a_n$ converge pero $\prod(1+a_n)$ diverge.
   (c) También encontrar un ejemplo tal que $\prod(1+a_n)$ converge y $\sum a_n$ diverge.

7. Probar que para todo $z$ el siguiente producto converge, y
   $$\cos(z/2)\cos(z/4)\cos(z/8)\cdots = \prod_{k=1}^{\infty}\cos(z/2^k) = \frac{\sin z}{z}$$
   Sugerencia: Usar el hecho de que $\sin 2z = 2\sin z\cos z$.

8. Probar que si $|z| < 1$, entonces
   $$(1+z)(1+z^2)(1+z^4)(1+z^8)\cdots = \prod_{k=0}^{\infty}(1+z^{2^k}) = \frac{1}{1-z}$$

9. Encontrar los productos de Hadamard para:
   (i) $\frac{\sin \pi z}{\pi z}$;
   (ii) $\cos \pi z$.
   Sugerencia: Las respuestas son $e^{z/2}\prod_{n=1}^{\infty}(1+z^2/4n^2\pi^2)$ y $\prod_{n=0}^{\infty}(1-4z^2/(2n+1)^2)$, respectivamente.

10. Mostrar que si $f$ es una función entera de orden finito que omite dos valores, entonces $f$ es constante. Este resultado sigue siendo válido para cualquier función entera y se conoce como el pequeño teorema de Picard.
    Sugerencia: Si $f$ no toma el valor $a$, entonces $f(z) - a$ es de la forma $e^{p(z)}$ donde $p$ es un polinomio.

11. Supóngase que $f$ es entera y nunca se anula, y que ninguna de las derivadas superiores de $f$ se anula nunca. Probar que si $f$ es también de orden finito, entonces $f(z) = e^{az+b}$ para algunas constantes $a$ y $b$.

12. Mostrar que la ecuación $e^z - z = 0$ tiene infinitas soluciones en $\mathbb{C}$.   Sugerencia: Aplicar el teorema de Hadamard.

13. Deducir del teorema de Hadamard que si $F$ es entera y de orden de crecimiento $\rho$ que no es entero, entonces $F$ tiene infinitos ceros.

14. Probar que toda función meromorfa en $\mathbb{C}$ es el cociente de dos funciones enteras. También, si $\{a_n\}$ y $\{b_n\}$ son dos sucesiones disjuntas que no tienen puntos límite finitos, entonces existe una función meromorfa en todo el plano complejo que se anula exactamente en $\{a_n\}$ y tiene polos exactamente en $\{b_n\}$.

15. Supóngase que se dan polinomios $Q_n(z) = \sum_{k=1}^{N_n} c_{nk}z^k$ para $n = 1,2,\ldots$. Supóngase también que se da una sucesión de números complejos $\{a_n\}$ sin puntos límite. Probar que existe una función meromorfa $f(z)$ cuyos únicos polos están en $\{a_n\}$, y tal que para cada $n$, la diferencia
    $$f(z) - Q_n\left(\frac{1}{z-a_n}\right)$$
    es holomorfa cerca de $a_n$. En otras palabras, $f$ tiene polos y partes principales prescritas en cada uno de estos polos. Este resultado se debe a Mittag-Leffler.

16. Dadas dos sucesiones infinitas numerables de números complejos $\{a_k\}_{k=0}^{\infty}$ y $\{b_k\}_{k=0}^{\infty}$, con $\lim_{k\to\infty}|a_k| = \infty$, ¿es siempre posible encontrar una función entera $F$ que satisfaga $F(a_k) = b_k$ para todo $k$?

    (a) Dados $n$ números complejos distintos $a_1,\ldots,a_n$, y otros $n$ números complejos $b_1,\ldots,b_n$, construir un polinomio $P$ de grado $\leq n-1$ con $P(a_i) = b_i$ para $i = 1,\ldots,n$.

    (b) Sea $\{a_k\}_{k=0}^{\infty}$ una sucesión de números complejos distintos tal que $a_0 = 0$ y $\lim_{k\to\infty}|a_k| = \infty$, y sea $E(z)$ un producto de Weierstrass asociado con $\{a_k\}$. Dados números complejos $\{b_k\}_{k=0}^{\infty}$, mostrar que existen enteros $m_k \geq 1$ tales que
    $$F(z) = \frac{b_0 E(z)}{E(0)} + \sum_{k=1}^{\infty} \frac{b_k E(z)}{E'(a_k)(z-a_k)}\left(\frac{a_k}{z}\right)^{m_k}$$
    define una función entera que satisface $F(a_k) = b_k$ para todo $k \geq 0$. Esto se conoce como la fórmula de interpolación de Pringsheim.

# Problemas

1. Probar que si $f$ es holomorfa en el disco unitario, acotada y no idénticamente cero, y $z_1,z_2,\ldots,z_n,\ldots$ son sus ceros ($|z_k| < 1$), entonces $\sum_n (1 - |z_n|) < \infty$.
   Sugerencia: Usar la fórmula de Jensen.

2. En este problema, discutimos los productos de Blaschke, que son análogos acotados en el disco de los productos de Weierstrass para funciones enteras.
   
   (a) Mostrar que para $0 < |\alpha| < 1$ y $|z| \leq r < 1$ se cumple la desigualdad
   $$\left|\frac{\alpha - z}{1 - \overline{\alpha}z}\frac{|\alpha|}{\alpha}\right| \leq \frac{1+r}{1-r}$$
   
   (b) Sea $\{\alpha_n\}$ una sucesión en el disco unitario tal que $\alpha_n \neq 0$ para todo $n$ y $\sum_{n=1}^{\infty}(1 - |\alpha_n|) < \infty$.
   Nótese que este será el caso si $\{\alpha_n\}$ son los ceros de una función holomorfa acotada en el disco unitario (ver Problema 1). Mostrar que el producto
   $$f(z) = \prod_{n=1}^{\infty}\frac{|\alpha_n|}{\alpha_n}\frac{\alpha_n - z}{1 - \overline{\alpha_n}z}$$
   converge uniformemente para $|z| \leq r < 1$, y define una función holomorfa en el disco unitario que tiene precisamente los ceros $\alpha_n$ y ningún otro cero. Mostrar que $|f(z)| \leq 1$.

3. Mostrar que $\prod_{n=1}^{\infty}(1 - \frac{z}{n!})^\alpha$ es una función entera de orden $1/\alpha$.

4. Sea $F(z) = \sum_{n=0}^{\infty} a_n z^n$ una función entera de orden finito. Entonces el orden de crecimiento de $F$ está íntimamente ligado al crecimiento de los coeficientes $a_n$ cuando $n \to \infty$.
   
   (a) Supóngase $|F(z)| \leq Ae^{a|z|^\rho}$. Entonces
   $$\limsup_{n\to\infty} |a_n|^{1/n} n^{1/\rho} < \infty$$
   
   (b) Recíprocamente, si (8) se cumple, entonces $|F(z)| \leq A'e^{a'|z|^{\rho+\epsilon}}$, para todo $\epsilon > 0$.
   Sugerencia: Para probar (a), usar la desigualdad de Cauchy $|a_n| \leq Ar^{-n}e^{ar^\rho}$, y el hecho de que la función $u^{-n}e^{u^\rho}$, $0 < u < \infty$, alcanza su valor mínimo $e^{n/\rho}(\rho/n)^{n/\rho}$ en $u = n^{1/\rho}/\rho^{1/\rho}$.        Luego, elegir $r$ en términos de $n$ para alcanzar este mínimo.
   Para establecer (b), nótese que $|F(z)| \leq \sum_{n=0}^{\infty} |c_n|r^n$, $r/n^\rho \leq \epsilon$, para alguna constante $c$,           ya que $n^n \geq n!$. Esto produce una reducción al Problema 3.

## Soluciones 5
