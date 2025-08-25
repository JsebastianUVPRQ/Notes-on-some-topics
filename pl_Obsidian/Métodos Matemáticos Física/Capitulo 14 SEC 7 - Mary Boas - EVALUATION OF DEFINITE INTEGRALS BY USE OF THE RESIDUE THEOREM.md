# TEORÍA

### Explicación Paso a Paso de la Sección "EVALUATION OF DEFINITE INTEGRALS BY USE OF THE RESIDUE THEOREM"

#### **Introducción**
El objetivo de esta sección es evaluar integrales definidas reales utilizando el **teorema de los residuos** del análisis complejo. El teorema establece que para una función analítica en una región, excepto en polos aislados, la integral sobre un contorno cerrado es $2\pi i$ veces la suma de los residuos dentro del contorno. Aquí se aplica este teorema a cuatro tipos de integrales reales mediante ejemplos.

---

#### **Ejemplo 1: Integrales de Funciones Racionales de $\sin \theta$ y $\cos \theta$ (periódicas en $[0, 2\pi]$)**
**Problema:** Calcular $\int_0^{2\pi} \frac{d\theta}{5 + 4\cos\theta}$.

**Pasos:**
1. **Sustitución compleja:**  
   - Se usa $z = e^{i\theta}$ (con $\theta: 0 \to 2\pi$, $z$ recorre el círculo unitario $|z| = 1$).  
   - Entonces:  
     $$
     d\theta = \frac{dz}{iz}, \quad \cos\theta = \frac{z + z^{-1}}{2} = \frac{z^2 + 1}{2z}.
     $$

2. **Reescribir la integral:**  
   $$
   I = \oint_{|z|=1} \frac{1}{5 + 4 \cdot \frac{z^2 + 1}{2z}} \cdot \frac{dz}{iz} = \frac{1}{i} \oint_{|z|=1} \frac{dz}{2z^2 + 5z + 2}.
   $$

3. **Factorizar el denominador:**  
   $$
   2z^2 + 5z + 2 = (2z + 1)(z + 2).
   $$

4. **Identificar polos y residuos:**  
   - Polos: $z = -1/2$ (dentro de $|z| = 1$) y $z = -2$ (fuera).  
   - Residuo en $z = -1/2$:  
     $$
     \text{Res} = \lim_{z \to -1/2} (z + 1/2) \cdot \frac{1}{(2z + 1)(z + 2)} = \frac{1}{2(-1/2 + 2)} = \frac{1}{3}.
     $$

5. **Aplicar teorema de residuos:**  
   $$
   I = \frac{1}{i} \cdot 2\pi i \cdot \frac{1}{3} = \frac{2\pi}{3}.
   $$

**Conclusión:**  
Este método funciona para cualquier función racional de $\sin \theta$ y $\cos \theta$ en $[0, 2\pi]$, siempre que el denominador no se anule.

---

#### **Ejemplo 2: Integrales Impropias de Funciones Racionales en $(-\infty, \infty)$**
**Problema:** Calcular $\int_{-\infty}^{\infty} \frac{dx}{1 + x^2}$.

**Pasos:**
1. **Contorno semicircular:**  
   - Se usa un semicírculo en el semiplano superior con radio $\rho$ (centro en origen).  
   - Contorno $C$: eje real $[- \rho, \rho]$ + arco superior $|z| = \rho$.

2. **Función compleja y polos:**  
   $$
   \oint_C \frac{dz}{1 + z^2}, \quad \text{polos en } z = i \text{ (dentro)} \text{ y } z = -i \text{ (fuera)}.
   $$

3. **Residuo en $z = i$:**  
   $$
   \text{Res} = \lim_{z \to i} (z - i) \frac{1}{(z - i)(z + i)} = \frac{1}{2i}.
   $$

4. **Teorema de residuos:**  
   $$
   \oint_C = 2\pi i \cdot \frac{1}{2i} = \pi.
   $$

5. **Descomponer y tomar límite $\rho \to \infty$:**  
   $$
   \oint_C = \int_{-\rho}^{\rho} \frac{dx}{1 + x^2} + \int_{\text{arco}} \frac{dz}{1 + z^2}.
   $$
   - Integral sobre el arco $\to 0$ cuando $\rho \to \infty$ (grado denominador > numerador +1).  
   - Entonces: $\int_{-\infty}^{\infty} \frac{dx}{1 + x^2} = \pi$.

**Condiciones:**  
- $P(x)/Q(x)$ con $Q(x)$ sin ceros reales.  
- Grado $Q(x) \geq$ grado $P(x) + 2$.

---

#### **Ejemplo 3: Integrales con Exponenciales Complejos ($\cos mx$, $\sin mx$)**
**Problema:** Calcular $\int_0^\infty \frac{\cos x}{1 + x^2} dx$.

**Pasos:**
1. **Función compleja asociada:**  
   $$
   I_c = \oint_C \frac{e^{iz}}{1 + z^2} dz \quad (\text{contorno semicircular superior}).
   $$

2. **Polos y residuos:**  
   - Polo en $z = i$:  
     $$
     \text{Res} = \frac{e^{i \cdot i}}{2i} = \frac{e^{-1}}{2i}.
     $$
   - Integral de contorno: $2\pi i \cdot \frac{e^{-1}}{2i} = \frac{\pi}{e}$.

2. **Descomponer y límite $\rho \to \infty$:**  
   $$
   \oint_C = \int_{-\rho}^{\rho} \frac{e^{ix}}{1 + x^2} dx + \int_{\text{arco}} \frac{e^{iz}}{1 + z^2} dz.
   $$
   - Integral sobre arco $\to 0$ porque $|e^{iz}| = e^{-\text{Im}(z) \leq 1$ en semiplano superior.  
   - Entonces: $\int_{-\infty}^{\infty} \frac{e^{ix}}{1 + x^2} dx = \frac{\pi}{e}$.

4. **Tomar parte real:**  
   $$
   \int_{-\infty}^{\infty} \frac{\cos x}{1 + x^2} dx = \frac{\pi}{e}, \quad \int_0^\infty = \frac{\pi}{2e} \quad (\text{función par}).
   $$

**Condiciones:**  
- $m > 0$.  
- Grado $Q(x) \geq$ grado $P(x) + 1$.  
- $Q(x)$ sin ceros reales.

---

#### **Ejemplo 4: Integrales con Polos Reales (Valor Principal)**
**Problema:** Calcular $\int_{-\infty}^{\infty} \frac{\sin x}{x} dx$.

**Pasos:**
1. **Contorno con desvío:**  
   - Evitar polo en $z = 0$ con semicírculo pequeño de radio $r$ en semiplano superior (Figura 7.3).  
   - Contorno completo: eje real $[-R, -r] \cup [r, R]$ + arco grande $|z| = R$ + semicírculo pequeño $|z| = r$.

2. **Función compleja:**  
   $$
   \oint \frac{e^{iz}}{z} dz = 0 \quad (\text{no polos dentro}).
   $$

3. **Descomponer integral:**  
   $$
   0 = \left( \int_{-R}^{-r} + \int_{r}^{R} \right) \frac{e^{ix}}{x} dx + \int_{\text{arco grande}} + \int_{\text{semicírculo pequeño}}.
   $$

4. **Límites $R \to \infty$, $r \to 0$:**  
   - Integral sobre arco grande $\to 0$ (lema de Jordan).  
   - Integral sobre semicírculo pequeño ($z = r e^{i\theta}$, $\theta: \pi \to 0$):  
     $$
     \int_\pi^0 \frac{e^{i r e^{i\theta}}}{r e^{i\theta}} i r e^{i\theta} d\theta = \int_\pi^0 i  d\theta = -i\pi \quad (r \to 0).
     $$

5. **Ecuación resultante:**  
   $$
   \int_{-\infty}^{\infty} \frac{e^{ix}}{x} dx - i\pi = 0 \implies \int_{-\infty}^{\infty} \frac{\sin x}{x} dx = \pi \quad (\text{parte imaginaria}).
   $$

**Regla para polos simples en eje real:**  
- Contribución: $\pm i\pi \times$ residuo ($\pm$ depende del semiplano usado).

---

#### **Ejemplo 5: Integrales con Cortes de Rama (Funciones Multivaluadas)**
**Problema:** Calcular $\int_0^\infty \frac{r^{p-1}}{1 + r} dr$, $0 < p < 1$.

**Pasos:**
1. **Contorno "keyhole":**  
   - Corte de rama en eje real positivo (Figura 7.4).  
   - $z^{p-1} = e^{(p-1) \ln z}$ con $\arg z \in [0, 2\pi)$.

2. **Función compleja:**  
   $$
   \oint_C \frac{z^{p-1}}{1 + z} dz.
   $$
   - Polo en $z = -1 = e^{i\pi}$: Residuo = $(-1)^{p-1} = -e^{i\pi p}$.

3. **Teorema de residuos:**  
   $$
   \oint_C = 2\pi i (-e^{i\pi p}) = -2\pi i e^{i\pi p}.
   $$

4. **Descomponer en caminos:**  
   - $AB$ ($\theta = 0$): $\int_\epsilon^R \frac{x^{p-1}}{1 + x} dx$.  
   - $DE$ ($\theta = 2\pi$): $\int_R^\epsilon \frac{(x e^{2\pi i})^{p-1}}{1 + x} e^{2\pi i} dx = -e^{2\pi i p} \int_\epsilon^R \frac{x^{p-1}}{1 + x} dx$.  
   - Integrales sobre círculos $\to 0$ cuando $\epsilon \to 0$, $R \to \infty$.

5. **Sumar contribuciones:**  
   $$
   (1 - e^{2\pi i p}) \int_0^\infty \frac{x^{p-1}}{1 + x} dx = -2\pi i e^{i\pi p}.
   $$
   $$
   \implies \int_0^\infty \frac{x^{p-1}}{1 + x} dx = \frac{\pi}{\sin \pi p}.
   $$

**Aplicación:**  
Relaciona con función Beta: $B(p, 1-p) = \Gamma(p) \Gamma(1-p) = \frac{\pi}{\sin \pi p}$.

---

#### **Principio del Argumento**
**Objetivo:** Contar ceros y polos de una función dentro de un contorno.

**Teorema:**  
$$
\frac{1}{2\pi i} \oint_C \frac{f'(z)}{f(z)} dz = N - P,
$$
donde:  
- $N$ = número de ceros (contando multiplicidad).  
- $P$ = número de polos (contando multiplicidad).  

**Interpretación geométrica:**  
El cambio total en $\arg f(z)$ al recorrer $C$ es $2\pi (N - P)$.

**Aplicación:**  
Estabilidad de sistemas (ubicación de ceros en semiplano izquierdo).

---

#### **Transformada Inversa de Laplace (Integral de Bromwich)**
**Fórmula:**  
$$
f(t) = \frac{1}{2\pi i} \int_{c - i\infty}^{c + i\infty} F(z) e^{zt} dz, \quad t > 0.
$$
- $c$: constante mayor que parte real de todos los polos de $F(z)$.

**Método:**  
1. Cerrar contorno con semicírculo izquierdo (Figura 7.4 modificada).  
2. Si integral sobre arco $\to 0$ cuando $R \to \infty$$entonces:  
   $$
   f(t) = \sum \text{residuos de } F(z) e^{zt} \text{ en todos los polos}.
   $$

**Ejemplo:**  
$(z) = \frac{5}{(z+2)(z^2+1)} \implies f(t) = e^{-2t} + 2\sin t - \cos t$.

---

#### **Relaciones de Dispersión (Kramers-Kronig)**
**Contexto:**  
Para $f(z) = u(x) + i v(x)$ analítica en semiplano superior y que decae en $\infty$:  
$$
u(a) = \frac{1}{\pi} PV \int_{-\infty}^{\infty} \frac{v(x)}{x - a} dx, \quad v(a) = -\frac{1}{\pi} PV \int_{-\infty}^{\infty} \frac{u(x)}{x - a} dx.
$$

**Aplicaciones:**  
Óptica (índice de refracción complejo), mecánica cuántica, teoría de partículas.

---

### Resumen de Métodos
| **Tipo de Integral**                        | **Contorno**                           | **Condiciones Clave**                              |
| ------------------------------------------- | -------------------------------------- | -------------------------------------------------- |
| Funciones racionales de $\sin/\cos$       | Círculo unitario                       | Denominador ≠ 0 en $[0, 2\pi]$                   |
| $\int_{-\infty}^{\infty} P(x)/Q(x) dx$    | Semicírculo superior/inferior          | Grado $Q \geq$ grado $P + 2$, sin polos reales |
| $\int_{-\infty}^{\infty} e^{imx} g(x) dx$ | Semicírculo superior ($m>0$)         | Grado $Q \geq$ grado $P + 1$, sin polos reales |
| Integrales con polos reales                 | Desvío con semicírculo                 | Valor principal, polo simple en eje real           |
| Integrales con cortes de rama               | "Keyhole" o rectángulo                 | Definir rama de función multivaluada               |
| Transformada inversa de Laplace             | Línea vertical + semicírculo izquierdo | $F(z)$ racional, decaimiento en arco             |

Esta sección proporciona herramientas poderosas para evaluar integrales reales difíciles mediante la explotación de propiedades de funciones complejas.
# EJERCICIOS (SECCIÓN 7)

Los valores de las siguientes integrales son conocidos y pueden encontrarse en tablas de integrales o mediante computadora. Su objetivo al evaluarlas es aprender sobre la integración de contorno aplicando los métodos discutidos en los ejemplos anteriores. Luego verifique sus respuestas mediante computadora.

1. $\int_0^{2\pi} \frac{d\theta}{13+5\sin\theta}$

2. $\int_0^{2\pi} \frac{d\theta}{5-3\cos\theta}$

3. $\int_0^{2\pi} \frac{d\theta}{5-4\sin\theta}$

4. $\int_0^{2\pi} \frac{\sin^2\theta\ d\theta}{5+3\cos\theta}$

5. $\int_0^{2\pi} \frac{d\theta}{1-2r\cos\theta+r^2}$ $(0\leq r<1)$

6. $\int_0^{2\pi} \frac{d\theta}{(2+\cos\theta)^2}$

7. $\int_0^{2\pi} \frac{\cos 2\theta\ d\theta}{5+4\cos\theta}$

8. $\int_0^{2\pi} \frac{\sin^2\theta\ d\theta}{13-12\cos\theta}$

9. $\int_0^{2\pi} \frac{d\theta}{1+\sin\theta\cos\alpha}$ $(\alpha=\text{constante})$

10. $\int_{-\infty}^{\infty} \frac{dx}{x^2+4x+5}$

11. $\int_{-\infty}^{\infty} \frac{x^2\ dx}{(4x^2+1)^3}$

12. $\int_0^{\infty} \frac{x\ dx}{x^4+1}$

13. $\int_{-\infty}^{\infty} \frac{x\ dx}{(x^2+4)(x^2+9)}$

14. $\int_{-\infty}^{\infty} \frac{\sin x\ dx}{x^2+4x+5}$

15. $\int_{-\infty}^{\infty} \frac{\cos 2x\ dx}{9x^2+4}$

16. $\int_{-\infty}^{\infty} \frac{x\sin x\ dx}{9x^2+4}$

17. $\int_{-\infty}^{\infty} \frac{x\sin x\ dx}{x^2+4x+5}$

18. $\int_{-\infty}^{\infty} \frac{\cos x\ dx}{1+x+x^4}$

19. $\int_{-\infty}^{\infty} \frac{\cos 2x\ dx}{(4x+9)^2}$

20. $\int_{-\infty}^{\infty} \frac{\cos x\ dx}{(1+9x)^2}$

21. En el Ejemplo 4 enunciamos una regla para evaluar una integral de contorno cuando el contorno pasa por polos simples. Demostramos que el resultado es correcto para $PV \int \frac{dz}{z}$ alrededor del contorno $\Gamma$ mostrado aquí.
    (a) Siguiendo el mismo método (integrando alrededor de $C'$ de la Figura 7.3 y haciendo $r \rightarrow 0$) demuestre que el resultado es correcto si reemplazamos $e^{i\theta/2}$ por cualquier $f(z)$ que sea analítica en $z=0$.
    (b) Repita la demostración en (a) para $PV \int \frac{f(z)}{z-a} dz$, $a$ real (es decir, un polo en el eje $x$), con $f(z)$ analítica en $z=a$.

Usando la regla del Ejemplo 4 (véase también el problema 21), evalúe las siguientes integrales. Encuentre valores principales si es necesario.

22. $\int_{-\infty}^{\infty} \frac{dx}{(x-1)(x+1)}$

23. $\int_{-\infty}^{\infty} \frac{dx}{(x+4)(2-x)}$

24. $\int_{-\infty}^{\infty} \frac{x\sin\pi x}{9x^2-\pi^2} dx$

25. $\int_{-\infty}^{\infty} \frac{dx}{1-x^4}$

26. $\int_{-\infty}^{\infty} \frac{\sin x}{(x-1)^4-1} dx$

27. $\int_{-\infty}^{\infty} \frac{\cos\pi x}{1-4x^2} dx$

28. $\int_{-\infty}^{\infty} \frac{dx}{1-x^4}$

29. $\int_{-\infty}^{\infty} \frac{\sin ax}{x} dx$

30. (a) Por el método del Ejemplo 2 evalúe $\int_0^{\infty} \frac{dx}{1+x^4}$
    (b) Evalúe la misma integral usando tablas o computadora para obtener la integral indefinida; a menos que sea muy cuidadoso, podría obtener cero. Explique por qué.
    (c) Haga el cambio de variable $u = 1/x$ en la integral de (a) y evalúe la integral en $u$ usando (7.5).

31. Use el método del Problema 30(c) para evaluar $\int_0^{\infty} \frac{dx}{1+x^6}$

32. Use el método del Problema 30(c) y el contorno y método del Ejemplo 5 para evaluar $\int_0^{\infty} \frac{dx}{(1+x^4)^2}$

Evalúe las siguientes integrales por el método del Ejemplo 5.

33. $\int_0^{\infty} \frac{\sqrt{x}\ dx}{1+x^2}$

34. $\int_0^{\infty} \frac{\sqrt{x}\ dx}{(1+x)^2}$

35. $\int_0^{\infty} \frac{x^{1/3}\ dx}{(1+x)(2+x)}$

36. $\int_0^{\infty} \frac{\ln x\ dx}{x^{3/4}(1+x)}$

37. (a) Demuestre que $\int_{-\infty}^{\infty} \frac{e^{px}}{1+e^x} dx = \frac{\pi}{\sin\pi p}$ para $0<p<1$. Sugerencia: Encuentre $\oint \frac{e^{pz}}{1+e^z} dz$ alrededor del contorno rectangular mostrado. Demuestre que las integrales a lo largo de los lados verticales tienden a cero cuando $A \rightarrow \infty$. Note que la integral a lo largo del lado superior es un múltiplo de la integral a lo largo del eje $x$.
    (b) Haga el cambio de variable $y = e^x$ en la integral $x$ de la parte (a), y usando (6.5) del Capítulo 11, demuestre que esta integral es la función beta, $B(p,1-p)$. Luego usando (7.1) del Capítulo 11, demuestre que $\Gamma(p)\Gamma(1-p)=\pi/\sin\pi p$.

38. Usando el mismo contorno y método que en el Problema 37a evalúe $\int_{-\infty}^{\infty} \frac{e^{px}}{1-e^x} dx$, $0<p<1$. Sugerencia: La única diferencia entre este problema y el Problema 37a es que ahora tiene dos polos simples en el contorno en lugar de un polo dentro. Use la regla del Ejemplo 4.

39. Evalúe $\int_{-\infty}^{\infty} \frac{dx}{\cosh\pi x}$. Sugerencia: Use un rectángulo como en el Problema 37a pero de altura 1 en lugar de 2. Note que hay un polo en $i/2$.

40. Evalúe $\int_0^{\infty} \frac{x\ dx}{\sinh x}$. Sugerencia: Primero encuentre la integral de $-\infty$ a $\infty$. Use un rectángulo de altura $\pi$ y note el polo simple en $i$ en el contorno.

41. Las integrales de Fresnel, $\int_0^{\infty} \sin u^2 du$ y $\int_0^{\infty} \cos u^2 du$, son importantes en óptica. Para el caso de límites superiores infinitos, evalúe estas integrales de la siguiente manera: Haga el cambio de variable $x = u^2$; para evaluar las integrales resultantes, encuentre $\oint z^{1/2}e^{iz^2}dz$ alrededor del contorno mostrado. Deje $r \rightarrow 0$ y $R \rightarrow \infty$ y demuestre que las integrales a lo largo de estos cuartos de círculo tienden a cero. Reconozca la integral a lo largo del eje $y$ como una función $\Gamma$ y evalúela. Por lo tanto, evalúe la integral a lo largo del eje $x$; las partes real e imaginaria de esta integral son las integrales que está tratando de encontrar.

42. Si $F(z)=f'(z)/f(z)$,
    (a) demuestre que el residuo de $F(z)$ en un cero de orden $n$ de $f(z)$, es $n$. Sugerencia: Si $f(z)$ tiene un cero de orden $n$ en $z=a$, entonces $f(z)=a_n(z-a)^n+a_{n+1}(z-a)^{n+1}+\ldots$
    (b) También demuestre que el residuo de $F(z)$ en un polo de orden $p$ de $f(z)$, es $-p$. Sugerencia: Vea la definición de un polo de orden $p$ al final de la Sección 4.

43. Usando el teorema (7.8), demuestre que $z^3+z+9=0$ tiene exactamente una raíz en el primer cuadrante. Por lo tanto, demuestre que tiene una raíz en el cuarto cuadrante y una en el eje real negativo. Sugerencia: Vea el Ejemplo 6.

44. El teorema fundamental del álgebra dice que toda ecuación de la forma $f(z)=a_n z^n+a_{n-1}z^{n-1}+\ldots+a_0=0$, $a_n \neq 0$, $n \geq 1$, tiene al menos una raíz. De esto se sigue que una ecuación de grado $n$ tiene $n$ raíces. Demuestre esto usando el principio del argumento. Sugerencia: Siga el aumento en el ángulo de $f(z)$ alrededor de un círculo muy grande $z=re^{i\theta}$; para $r$ suficientemente grande, todas las raíces están incluidas, y $f(z)$ es aproximadamente $a_n z^n$.

Como en el Problema 43, determine en qué cuadrantes se encuentran las raíces de las siguientes ecuaciones:

45. $z^3+z^2+z+4=0$

46. $z^3+3z^2+4z+2=0$

47. $z^3+4z^2+12=0$

48. $z^4-z^3+6z^2-32z+5=0$

# Soluciones

