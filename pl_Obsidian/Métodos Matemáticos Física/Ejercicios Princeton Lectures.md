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


# # Vol. II — Complex Analysis (Tratamiento orientado a Física)

  

> **Objetivo:** dar un tratamiento extenso y enfocado a aplicaciones físicas del análisis complejo: integrales de contorno, teorema de Cauchy, residuos, ramas y cortes, continuación analítica, métodos asintóticos (saddle point / steepest descent), funciones armónicas y kernel de Poisson, y aplicaciones concretas en mecánica cuántica, teoría de campos, óptica, y mecánica de fluidos.

  

---

  

## 0. Convenciones y notación

- Denotamos funciones holomorfas por $f(z)$. Un contorno $\gamma$ orientado positivamente es recorrido antihorario salvo que se indique.

- Integral de contorno: $\displaystyle\oint_\gamma f(z)\,dz$.

- Polo de orden $m$ en $z_0$: expansión local $f(z)=\sum_{k=-m}^{\infty} a_k (z-z_0)^k$.

- Rama principal del logaritmo: $\arg z\in(-\pi,\pi]$ salvo que indiquemos otra.

  

---

  

## 1. Capítulo 1 — Funciones Analíticas y Teorema de Cauchy

  

### 1.1. Holomorfía y física

- Interpretación física: amplitud/funciones de respuesta analíticas en el plano complejo de la frecuencia/energía manifiestan causalidad y propiedades de disipación.

- Analiticidad implica infinitas derivadas y expansión en series de potencias (usos: desarrollo en series para perturbaciones pequeñas).

  

### 1.2. Teorema de Cauchy y fórmulas

- Cauchy integral formula: $f^{(n)}(z_0)=\frac{n!}{2\pi i}\oint_\gamma \frac{f(z)}{(z-z_0)^{n+1}}dz$.

- Consecuencias: representación de soluciones via integrales de contorno; valores interiores determinados por valores en la frontera (principio de unicidad para problemas de contorno).

  

### 1.3. Aplicaciones físicas

- Representaciones integrales para funciones de Green (valores dentro de dominios a partir de condiciones en la frontera).

- Identificación de singularidades en función de respuesta (poles como resonancias).

  

### 1.4. Ejercicio físico sugerido

- Dada la función de respuesta $H(\omega)=\frac{1}{\omega_0^2-\omega^2+i\gamma\omega}$, considerar $\omega$ complejo y discutir ubicación de polos (resonancias amortiguadas) y su relación con la respuesta temporal.

  

---

  

## 2. Capítulo 2 — Integrales de contorno y técnicas elementales

  

### 2.1. Integrales sobre semicírculos y caminos de Jordan

- Uso para evaluar integrales reales de la forma $\int_{-\infty}^{\infty} R(x)\,dx$ donde $R$ racional y decae apropiadamente.

- Criterio para cerrar en semicírculo superior/inferior según factor exponencial ($e^{ikx}$ con signo de $k$ y $x$).

  

### 2.2. Integración de funciones con singularidades en el eje real

- Prescripción de paso por polos (principal value) y relación con transformadas inversas de Fourier/Laplace.

  

### 2.3. Ejemplos físicos

- Integral de Fourier de una función racional que aparece en transformadas de respuesta: evaluarla mediante residuos.

- Inversas de Laplace para resolver EDOs con condiciones iniciales.

  

### 2.4. Ejercicio trabajado

- Compute $\int_{-\infty}^{\infty} \frac{e^{ikx}}{x^2+a^2}\,dx$ via residues and relate to Green's function of Helmholtz in 1D.

  

---

  

## 3. Capítulo 3 — Teorema de los residuos y aplicaciones prácticas

  

### 3.1. Residuos: definición y cálculo

- Residuo $\operatorname{Res}(f,z_0)=a_{-1}$ en la expansión de Laurent.

- Fórmulas prácticas: polo simple $\operatorname{Res} = \lim_{z\to z_0}(z-z_0)f(z)$; para polo de orden $m$ usar derivadas.

  

### 3.2. Uso en integrales reales

- Integrales con $\cos,\sin$ multiplicadas por racionales: transformar en $e^{ikx}$ y cerrar contorno; tomar contribución de polos en semiplano correspondiente.

  

### 3.3. Sumatorias mediante integrales

- Técnica: convertir series en integrales de contorno que encierran polos en enteros (ej.: fórmulas tipo Mittag-Leffler, evaluación de sumas $\sum f(n)$).

  

### 3.4. Aplicaciones físicas

- Evaluación de integrales térmicas y sumas de Matsubara en teoría estadística cuántica mediante contornos en el plano complejo de la energía.

- Residuos y resonancias: interpretación física de los términos contribuyentes.

  

### 3.5. Ejercicios sugeridos

1) Calcular $\int_{-\infty}^{\infty} \frac{x^2}{(x^2+1)^2}dx$ por residuos. 2) Sumar $\sum_{n=-\infty}^{\infty} \frac{1}{(n+a)^2}$ usando función $\pi\cot(\pi z)$.

  

---

  

## 4. Capítulo 4 — Principio del argumento y teoremas relacionados

  

### 4.1. Enunciado y significado

- El principio del argumento relaciona el número de ceros menos polos dentro de un contorno con la variación del argumento de $f(z)$ sobre la frontera.

  

### 4.2. Aplicaciones físicas

- Estabilidad de sistemas: análisis de polos/ceros de funciones de transferencia (control y respuesta lineal).

- Conteo de modos resonantes en cavidades: número de ceros de funciones determinadas por condiciones en la frontera.

  

### 4.3. Rouché y localización de ceros

- Rouché permite estimar dónde están los ceros; útil para aproximaciones de raíces de polinomios que aparecen en denominadores de funciones de respuesta.

  

### 4.4. Ejercicio sugerido

- Use Rouché to estimate zeros of a polynomial characteristic equation for a damped oscillator network.

  

---

  

## 5. Capítulos 5–6 — Funciones armónicas y kernel de Poisson; Aplicaciones a potenciales

  

### 5.1. Funciones armónicas: vínculo con campos físicos

- Una función armónica es el real (o imaginario) de una función analítica. Estas satisfacen la ecuación de Laplace: $\Delta u=0$.

- Interpretación física: potencial electrostático en regiones sin cargas.

  

### 5.2. Poisson kernel y solución de Dirichlet

- Fórmula de Poisson en disco/semiplano: reconstrucción del valor interior a partir de la frontera.

- Aplicación: resolver problemas de potencial con datos de contorno (p. ej. potencial en cavidad, temperatura estacionaria).

  

### 5.3. Conformal maps (mapeos conformes)

- Transformaciones que preservan ángulos: útil para transformar dominios complicados en dominios simples donde las soluciones son conocidas.

- Aplicación en mecánica de fluidos potenciales y electrostática (flujo alrededor de perfiles, método de Joukowski para alas).

  

### 5.4. Ejemplos trabajados

- Solve Laplace's equation in a half-plane with given boundary potential using Poisson kernel.

- Map a flow past a cylinder to flow past an airfoil via Joukowski transform and compute pressure distribution (Bernoulli + potencial).

  

---

  

## 6. Capítulos 7–9 — Extensiones útiles y funciones especiales (breve)

  

### 6.1. Continuación analítica y ramas

- Cómo extender funciones definidas por series/integrales a dominios más grandes usando contornos y la unicidad de la continuación analítica.

- Ramas y cortes: tratamiento de $\sqrt z$ y $\log z$ — vital en integrales que involucran raíces y en la elección de caminos de integración.

  

### 6.2. Aplicaciones físicas

- Elección de ramas en funciones de dispersión y en definición de impedancia compleja.

- Analytic continuation in complex energy plane: locating resonances as poles on unphysical sheets.

  

### 6.3. Funciones especiales y transformadas

- Uso de funciones gamma, beta, y zeta para evaluar integrales y regularizar sumas divergentes (casos en QFT y energía de punto cero).

  

---

  

## 7. Métodos asintóticos y la integral de paso estacionario (saddle point / steepest descent)

  

### 7.1. Idea básica

- Cuando $I(\lambda)=\int e^{\lambda S(z)}g(z)dz$ con $\lambda\gg1$, la contribución dominante viene de puntos críticos de $S$ (saddle points) y de contornos de steepest descent.

  

### 7.2. Procedimiento operativo

1. Localizar puntos críticos $S'(z_0)=0$.

2. Deformar contorno a curvas de steepest descent donde $\Im S$ es constante y $\Re S$ máximo negativo fuera del punto.

3. Aproximar integral por contribución gaussiana local: $I\sim e^{\lambda S(z_0)}\sqrt{\frac{2\pi}{\lambda |S''(z_0)|}}g(z_0)$ con factores de fase.

  

### 7.3. Aplicaciones físicas

- Asymptotics of integrals in semiclassical approximations (WKB, path integrals), diffraction integrals (Kirchhoff/Geometrical Theory of Diffraction), and integral representations of special functions (Bessel, Airy) for large parameters.

  

### 7.4. Ejemplo trabajado

- Derive asymptotic form of Bessel function for large order using saddle point, relate to stationary phase for wave propagation.

  

---

  

## 8. Aplicaciones concretas a física (resumen y ejemplos trabajados)

  

### 8.1. Evaluación de integrales de Fourier mediante contornos

- Ejemplo: integral tipo Fresnel $\int e^{i(ax^2+bx)}dx$ y relación con propagadores cuánticos y patrones de difracción.

  

### 8.2. Kramers–Kronig (relaciones de dispersión)

- La causalidad (respuesta nula para t<0) implica que la transformada de Fourier de la respuesta es analítica en el semiplano superior, lo que lleva a relaciones entre parte real e imaginaria (Hilbert transform). Estas son las relaciones Kramers–Kronig en óptica y teoría de la respuesta lineal.

  

### 8.3. Polos, cortes y resonancias (QM y QFT)

- Polos reales ↔ estados ligados; polos en semiplanos superiores/inferiores ↔ resonancias con decaimiento exponencial. Branch cuts aparecen por continua espectral (por ejemplo arriba de umbral de dispersión).

  

### 8.4. Sumas de Matsubara y contornos térmicos

- Técnica: transformar sumas sobre frecuencias discretas en integrales en el plano complejo usando contorno que envuelve polos de la función $n_B(\omega)=1/(e^{\beta\omega}-1)$ o $n_F$ para fermiones.

  

### 8.5. Transformada inversa de Laplace y problemas iniciales

- Desarrollo práctico: elegir contorno de Bromwich, desplazar y capturar polos para obtener soluciones temporales por inversión.

  

### 8.6. Ejemplo trabajado final: función de Green retarded para un oscilador acoplado a continuo

- Construir $G_R(\omega)$ con cortes y polos; analizar respuesta temporal por transformada inversa y ubicación de singularidades.

  

---

  

## 9. Ejercicios integradores y retos

1. Evalúe integrales reales relevantes mediante residuos (varios niveles). 2. Use método de steepest descent para obtener comportamiento asintótico de una integral de Fourier oscilatoria con parámetro grande. 3. Aplicar Kramers–Kronig a un modelo simple de susceptibilidad. 4. Mapear un flujo potencial alrededor de una geometría y calcular fuerzas de presión.

  

---

  

## 10. Peligros y recomendaciones prácticas

- Cuidado con la elección de hoja de la función multivaluada y con la orientación de cortes.

- Antes de deformar contornos, comprobar decaimiento/exponencial en infinito de las integrandas en dicha dirección.

- En métodos asintóticos, asegúrese de que el punto crítico contribuye (no estar en borde o en singularidad) y tenga en cuenta posibles contribuciones de endpoints y singularidades cercanas.

  

---

  

## 11. Plan de estudio y prioridades (14 días intensivos o 6 semanas tranquilo)

- Días 1–3: Cap.1 — Cauchy y fórmulas; problemas de contorno simples.

- Días 4–6: Cap.2–3 — Integrales de contorno y residuos; prácticas de evaluación de integrales reales.

- Días 7–9: Cap.4–6 — Argument principle, funciones armónicas, Poisson kernel, ejercicios de potencial.

- Días 10–12: Ramas/cortes y funciones especiales; lectura aplicada a resonances.

- Días 13–14: Métodos asintóticos (saddle point) y aplicaciones (difracción, WKB).

  

---

  

## 12. Lecturas cruzadas y recursos adicionales

- Vol. I (Fourier) — para transformadas e inversión por contornos.

- Vol. III–IV — para distribuciones y operadores no acotados en QFT/QM.

- Textos clásicos: Ahlfors (Complex Analysis), Bender & Orszag (Advanced Mathematical Methods) para técnicas asintóticas.

  

---

  

**Sugerencia final:** aplica cada técnica inmediatamente a un problema físico concreto (propagador, diferencial de respuesta, integral térmica) — la abstracción queda mucho más clara cuando ves cómo afectan polos, ramas y contornos a la evolución temporal y a la estabilidad.

  

# Ampliación de la teoría y las matemáticas tratadas anteriormente

0. Convenciones y notaciones

  

- **Integral de contorno:** Definidas en el plano complejo, estas integrales son fundamentales para el análisis complejo y se denotan como $\oint_C f(z) dz$, donde $C$ es un contorno cerrado en el plano complejo.

$$

\oint_C f(z) dz = 2\pi i \sum \text{Res}(f, z_k)

$$

Se puede interpretar intuitivamente como una generalización de la fórmula de integración por partes, donde los residuos en los polos de la función compleja $f(z)$ contribuyen a la integral a lo largo del contorno $C$. Esto es especialmente útil en física, donde a menudo se necesita evaluar integrales que aparecen en el contexto de teorías cuánticas de campos y mecánica cuántica.