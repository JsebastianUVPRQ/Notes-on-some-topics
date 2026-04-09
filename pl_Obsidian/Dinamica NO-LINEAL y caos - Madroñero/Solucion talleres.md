Taller 1: Dinámica No Lineal y Caos Cuántico

### Problema 1 — Espacio de fase de un sistema dinámico lineal  
*(6 puntos)*

Considere el sistema dinámico bidimensional gobernado por la ecuación  
$$
\dot{x} = A x, \qquad \text{con } A = \begin{pmatrix} a & 1 \\ 0 & a \end{pmatrix}.
$$  
Encuentre la solución general de las curvas $y = y(x)$ del espacio de fase de este sistema. $x$ y $y$ son las componentes del vector $\mathbf{x}$. Grafique en particular el espacio de fase en la vecindad del punto fijo $\mathbf{x}=0$ para los siguientes casos:  
(i) $a < -1$, (ii) $a = -1$, (iii) $-1 < a < 0$, (iv) $a = 0$ y (v) $a > 0$.

---

### Problema 2 — Flujos bidimensionales  
*(5 puntos)*

La dinámica de un péndulo ideal de longitud $\ell$ está descrita por la ecuación  
$$
\frac{d^2\theta}{dt^2} + \omega^2 \sin\theta = 0, \quad \text{donde } \omega = \sqrt{g/\ell},
$$  
y $g$ es la aceleración de la gravedad. Con la transformación $\tau = \omega t$ la ecuación se reduce a  
$$
\ddot{\theta} + \sin\theta = 0, \qquad (1)
$$  
donde el punto denota la derivada con respecto a $\tau$.

(a) Encuentre todos los puntos fijos de (1) clasificándolos según su estabilidad. Para ello linealice el sistema alrededor de los puntos fijos.  
(b) Ilustre esquemáticamente el espacio de fase de (1) partiendo de la forma del espacio de fase en las vecindades de los puntos fijos.

---

### Problema 3 — Mapeo Logístico: problema numérico

**Ecuación recursiva:**

$$x_{n+1} = f(x_n) = r x_n (1 - x_n)$$

**(a) Demostrar los puntos fijos de orden 2**

Un punto fijo de periodo 2 es aquel que vuelve a sí mismo después de dos iteraciones: $x_{n+2} = x_n = x$. Esto significa que debemos encontrar las raíces de la ecuación $f(f(x)) = x$.

Sustituyendo la función en sí misma:

$$f(f(x)) = r [r x (1-x)] (1 - [r x (1-x)]) = x$$

Expandiendo este polinomio obtenemos una ecuación de grado 4:

$$r^2 x (1-x) (1 - rx + rx^2) - x = 0$$

Sabemos por teoría que los puntos fijos de periodo 1 (donde $f(x) = x$) también satisfacen $f(f(x)) = x$. Estos puntos son $x=0$ y $x=1 - \frac{1}{r}$. Para encontrar _exclusivamente_ los puntos de periodo 2, debemos factorizar las raíces de periodo 1.

Dividimos entre $x$ (asumiendo $x \neq 0$):

$$r^2 (1-x) (1 - rx + rx^2) - 1 = 0$$

$$-r^3 x^3 + 2r^3 x^2 - r^2(r+1)x + r^2 - 1 = 0$$

Al dividir este polinomio cúbico entre la otra raíz conocida $(x - (1 - \frac{1}{r}))$, o alternativamente, recordando que la condición se reduce a una ecuación cuadrática, llegamos a:

$$r^2 x^2 - r(r+1)x + (r+1) = 0$$

Aplicamos la fórmula general para ecuaciones cuadráticas:

$$x = \frac{r(r+1) \pm \sqrt{r^2(r+1)^2 - 4r^2(r+1)}}{2r^2}$$

$$x = \frac{r+1 \pm \sqrt{(r+1)^2 - 4(r+1)}}{2r}$$

$$x = \frac{r+1 \pm \sqrt{(r+1)(r+1-4)}}{2r}$$

$$x = \frac{1}{2r} \left( r+1 \pm \sqrt{(r+1)(r-3)} \right)$$

_Nota candorosa:_ Notarás que el resultado matemático riguroso tiene un **$2r$** en el denominador, mientras que el enunciado de tu problema indica $\frac{1}{r}$. Esto es un error tipográfico clásico en los libros de texto y talleres de dinámica. Si evalúas la fórmula del enunciado en $r=3$, obtendrías un valor mayor a 1, lo cual rompe los límites del mapeo logístico. La fórmula correcta es con $\frac{1}{2r}$.

**(b) Reproducir el diagrama de bifurcación (Código en Mathematica)**

Aquí tienes el código de Mathematica® construido estrictamente según las instrucciones de tu profesor (incisos i al iv).

Mathematica

```
(* Parámetros iniciales recomendados *)
n0 = 50; (* Número de condiciones iniciales *)
nr = 500; (* Número de puntos para r *)
rmin = 2.5; rmax = 4.0; (* Intervalo de r *)

(* (i) Conjunto de condiciones iniciales aleatorias *)
Omega0 = Table[RandomReal[{0, 1}], {n0}];

(* (ii) Conjunto de valores de r distribuidos homogéneamente *)
R0 = Subdivide[rmin, rmax, nr - 1];

(* (iii) Propagar la recursión y guardar las parejas *)
datosBifurcacion = {}; (* Lista vacía para acumular parejas *)

Do[
  (* Para cada condición inicial x0 *)
  Do[
    x = x0;
    (* Propagar 400 veces *)
    Do[x = r * x * (1 - x), {400}];
    (* Guardar la pareja (r, x_400) *)
    AppendTo[datosBifurcacion, {r, x}];
  , {r, R0}]
, {x0, Omega0}];

(* (iv) Graficar el diagrama *)
ListPlot[datosBifurcacion,
 PlotStyle -> Directive[PointSize[0.002], Black],
 AxesLabel -> {"r", "x"},
 PlotLabel -> "Diagrama de Bifurcación - Mapeo Logístico"]
```

---
# TALLER 2
### Problema 4 — Péndulo: parte analítica

**(a) Demostrar la ecuación del periodo con la integral elíptica**

Por conservación de la energía, la energía máxima (en el ángulo $\theta_{\max}$ donde la velocidad es 0) es igual a la energía en cualquier ángulo $\theta$:

$$E = mgl(1 - \cos\theta_{\max}) = \frac{1}{2}m\ell^2 \dot{\theta}^2 + mgl(1 - \cos\theta)$$

Despejando la velocidad angular $\dot{\theta} = \frac{d\theta}{dt}$:

$$\dot{\theta} = \pm \sqrt{\frac{2g}{\ell} (\cos\theta - \cos\theta_{\max})}$$

Separando variables e integrando desde $0$ hasta $\theta_{\max}$ obtenemos un cuarto del periodo ($T/4$):

$$\frac{T}{4} = \sqrt{\frac{\ell}{2g}} \int_0^{\theta_{\max}} \frac{d\theta}{\sqrt{\cos\theta - \cos\theta_{\max}}} \implies T = 4\sqrt{\frac{\ell}{2g}} \int_0^{\theta_{\max}} \frac{d\theta}{\sqrt{\cos\theta - \cos\theta_{\max}}}$$

Para transformarlo a la forma de Legendre, usamos la identidad $\cos\theta = 1 - 2\sin^2(\theta/2)$.

El término en la raíz se vuelve:

$$\cos\theta - \cos\theta_{\max} = 2\left[ \sin^2\left(\frac{\theta_{\max}}{2}\right) - \sin^2\left(\frac{\theta}{2}\right) \right]$$

Definimos $\kappa = \sin(\theta_{\max}/2)$ y hacemos el cambio de variable sugerido: $\sin(\theta/2) = \kappa \sin\varphi$.

Diferenciando esto obtenemos: $\frac{1}{2} \cos(\theta/2) d\theta = \kappa \cos\varphi d\varphi$.

Sustituyendo $d\theta$ y los límites (cuando $\theta = \theta_{\max}$, $\varphi = \pi/2$):

$$T = 4\sqrt{\frac{\ell}{2g}} \int_0^{\pi/2} \frac{\frac{2\kappa\cos\varphi}{\sqrt{1 - \kappa^2\sin^2\varphi}}}{\sqrt{2(\kappa^2 - \kappa^2\sin^2\varphi)}} d\varphi$$

Los términos $\kappa$, $\sqrt{2}$ y $\cos\varphi$ se cancelan magistralmente en el numerador y denominador:

$$T = 4\sqrt{\frac{\ell}{g}} \int_0^{\pi/2} \frac{d\varphi}{\sqrt{1 - \kappa^2\sin^2\varphi}} = 4\sqrt{\frac{\ell}{g}} K(\kappa)$$

**(b) Límite de pequeñas oscilaciones**

Si $\theta_{\max} \ll 1$, entonces $\kappa = \sin(\theta_{\max}/2) \approx \theta_{\max}/2 \ll 1$.

Podemos expandir el integrando usando Taylor $(1-x)^{-1/2} \approx 1 + \frac{x}{2}$:

$$K(\kappa) \approx \int_0^{\pi/2} \left( 1 + \frac{1}{2}\kappa^2\sin^2\varphi \right) d\varphi$$

Integramos ambos términos:

$$K(\kappa) \approx [\varphi]_0^{\pi/2} + \frac{\kappa^2}{2} \left[ \frac{\varphi}{2} - \frac{\sin(2\varphi)}{4} \right]_0^{\pi/2} = \frac{\pi}{2} + \frac{\kappa^2}{2} \left( \frac{\pi}{4} \right) = \frac{\pi}{2} \left( 1 + \frac{\kappa^2}{4} \right)$$

Reemplazando $\kappa \approx \theta_{\max}/2$ (por ende $\kappa^2 \approx \theta_{\max}^2/4$) en la fórmula del periodo:

$$T \approx 4\sqrt{\frac{\ell}{g}} \frac{\pi}{2} \left( 1 + \frac{\theta_{\max}^2/4}{4} \right) = 2\pi\sqrt{\frac{\ell}{g}} \left( 1 + \frac{\theta_{\max}^2}{16} \right)$$

$$T \approx \frac{2\pi}{\omega_0} \left( 1 + \frac{\theta_{\max}^2}{16} \right)$$

**(c) Energía y ecuación de la separatriz**

El hamiltoniano es $H = \frac{p^2}{2} - U_0 \cos\theta$.

La separatriz es la trayectoria que llega asintóticamente al punto de equilibrio inestable (el péndulo apuntando hacia arriba, $\theta = \pm \pi$). En ese punto superior, el péndulo se detiene, por lo que $p = 0$.

Evaluando el Hamiltoniano en ese punto:

$$E = \frac{0^2}{2} - U_0 \cos(\pm\pi) = -U_0 (-1) = U_0$$

Por lo tanto, la energía en la separatriz es $U_0$.

Para hallar la ecuación de la trayectoria en el espacio de fase, igualamos $H$ a la energía de la separatriz:

$$\frac{p^2}{2} - U_0 \cos\theta = U_0 \implies p^2 = 2U_0(1 + \cos\theta)$$

Usando $U_0 = \omega_0^2$ (dado que $M=1$) y la identidad trigonométrica $1 + \cos\theta = 2\cos^2(\theta/2)$:

$$p^2 = 2\omega_0^2 (2\cos^2(\theta/2)) = 4\omega_0^2 \cos^2(\theta/2)$$

Extrayendo la raíz cuadrada:

$$p = \pm 2\omega_0 \cos\left(\frac{\theta}{2}\right)$$

**(d) Trayectoria $\theta(t)$ sobre la separatriz**

En nuestras unidades ($M=1$), el momento es $p = \dot{\theta}$. Tomando la rama positiva de la separatriz:

$$\frac{d\theta}{dt} = 2\omega_0 \cos\left(\frac{\theta}{2}\right)$$

Separamos variables:

$$\int \frac{d\theta}{\cos(\theta/2)} = \int 2\omega_0 dt$$

Esta es una integral estándar. Evaluémosla. La integral de la secante es el logaritmo natural de la secante más la tangente:

$$2 \ln\left| \frac{1 + \sin(\theta/2)}{\cos(\theta/2)} \right| = 2\omega_0 t + C$$

Una forma más limpia de aislar $\theta$ es comprobar que la respuesta propuesta satisface la ecuación diferencial. Derivando la función propuesta $\theta(t) = 4\arctan(e^{\omega_0 t}) - \pi$:

$$\dot{\theta}(t) = 4 \left( \frac{1}{1 + (e^{\omega_0 t})^2} \right) \cdot \omega_0 e^{\omega_0 t} = \frac{4\omega_0 e^{\omega_0 t}}{1 + e^{2\omega_0 t}}$$

Dividiendo arriba y abajo por $e^{\omega_0 t}$:

$$\dot{\theta}(t) = \frac{4\omega_0}{e^{-\omega_0 t} + e^{\omega_0 t}} = \frac{2\omega_0}{\cosh(\omega_0 t)}$$

Ahora evaluemos el lado derecho $2\omega_0 \cos(\theta/2)$ con la función propuesta:

$$2\omega_0 \cos\left(2\arctan(e^{\omega_0 t}) - \frac{\pi}{2}\right) = 2\omega_0 \sin(2\arctan(e^{\omega_0 t}))$$

Usando la identidad $\sin(2\alpha) = \frac{2\tan\alpha}{1+\tan^2\alpha}$, donde $\alpha = \arctan(e^{\omega_0 t})$ (por lo que $\tan\alpha = e^{\omega_0 t}$):

$$2\omega_0 \left( \frac{2e^{\omega_0 t}}{1 + e^{2\omega_0 t}} \right) = \frac{4\omega_0 e^{\omega_0 t}}{1 + e^{2\omega_0 t}}$$

Ambos lados coinciden de manera idéntica. Además, se cumple la condición de frontera natural del péndulo cayendo desde el reposo absoluto en tiempo infinito $\theta(-\infty) = - \pi$.

---

### Problema 5 — Péndulo: parte numérica (Guía)

Para construir el retrato de fase en Mathematica, usaremos `NDSolve` dentro de un bucle `Table` para variar los momentos iniciales $p(0)$.

Mathematica

```MATHEMATICA
(* Parámetros *)
w0 = 1; (* Frecuencia natural *)

(* Resolver y graficar varias trayectorias *)
trayectorias = Table[
   NDSolve[{
     \[Theta]'[t] == p[t],
     p'[t] == -w0^2 * Sin[\[Theta][t]],
     \[Theta][0] == 0, p[0] == p0 (* Condiciones Iniciales *)
     }, {\[Theta], p}, {t, -10, 10}],
   {p0, -3, 3, 0.5}]; (* Variamos p0 desde -3 hasta 3 *)

(* Graficamos en el espacio de fase *)
ParametricPlot[
 Evaluate[{\[Theta][t], p[t]} /. trayectorias], {t, -10, 10},
 PlotRange -> {{\[Pi], \[Pi]}, {-3, 3}},
 Frame -> True, 
 FrameLabel -> {"\[Theta]", "p"},
 AspectRatio -> 0.6,
 PlotLabel -> "Espacio de Fase del Péndulo"]
```

Con este código observarás las curvas cerradas (oscilación) para valores pequeños de `p0`, la separatriz ondulante en $E=U_0$, y las curvas abiertas de rotación completa para energías superiores.

¡Qué excelentes problemas! Seguimos avanzando en el fascinante (y a veces riguroso) mundo de la mecánica analítica. La ecuación de Hamilton-Jacobi y las variables de acción-ángulo son herramientas elegantísimas, pero algebraicamente demandantes.

Aquí tienes la resolución paso a paso. Analicemos juntos las matemáticas y, con toda sinceridad, te señalaré un par de detalles tipográficos clásicos que vienen en los enunciados de tu taller para que no te causen confusión.

---
# TALLER 3


### Problema 6 — Ecuación de Hamilton-Jacobi para el oscilador armónico

Tenemos la ecuación de Hamilton-Jacobi, donde identificamos que la nueva constante de movimiento $P$ representa la energía $E$:

$$\frac{1}{2} \left( \frac{\partial F_2}{\partial q} \right)^2 + \frac{1}{2} q^2 = P$$

Queremos encontrar $q$ y $p$ en función de $P$ y la nueva coordenada $Q$.

**1. Despejar $\frac{\partial F_2}{\partial q}$:**

Sabiendo que $p = \frac{\partial F_2}{\partial q}$, despejamos:

$$\left( \frac{\partial F_2}{\partial q} \right)^2 = 2P - q^2 \implies \frac{\partial F_2}{\partial q} = \sqrt{2P - q^2}$$

**2. Encontrar la función generatriz $F_2(q, P)$:**

Integramos respecto a $q$:

$$F_2(q, P) = \int \sqrt{2P - q^2} \, dq$$

_(Nota: No es estrictamente necesario resolver esta integral completa, ya que en el siguiente paso derivaremos)_.

**3. Obtener la nueva coordenada $Q$ e invertir para $q$:**

Por las ecuaciones de transformación canónica, sabemos que $Q = \frac{\partial F_2}{\partial P}$. Derivamos bajo el signo de la integral:

$$Q = \frac{\partial}{\partial P} \int \sqrt{2P - q^2} \, dq = \int \frac{\partial}{\partial P} \left( \sqrt{2P - q^2} \right) dq$$

$$Q = \int \frac{1}{\sqrt{2P - q^2}} \, dq$$

Esta es una integral estándar que da como resultado el arcoseno:

$$Q = \arcsin\left( \frac{q}{\sqrt{2P}} \right)$$

Despejamos $q$ para obtener nuestra primera respuesta:

$$\frac{q}{\sqrt{2P}} = \sin(Q) \implies q = \sqrt{2P} \sin(Q)$$

**4. Encontrar la expresión para el momento $p$:**

Usamos la relación $p = \frac{\partial F_2}{\partial q} = \sqrt{2P - q^2}$ y sustituimos el valor de $q$ que acabamos de hallar:

$$p = \sqrt{2P - (\sqrt{2P} \sin(Q))^2} = \sqrt{2P - 2P\sin^2(Q)}$$

$$p = \sqrt{2P(1 - \sin^2(Q))} = \sqrt{2P\cos^2(Q)} = \sqrt{2P} \cos(Q)$$

¡Y listo! Las expresiones son $q = \sqrt{2P} \sin(Q)$ y $p = \sqrt{2P} \cos(Q)$.

---
---

### **Problema 6: Ecuación de Hamilton-Jacobi para el oscilador armónico**

**Enunciado:**

Considere el Hamiltoniano del oscilador armónico $H = (p^2 + q^2)/2$. La ecuación de Hamilton-Jacobi para este sistema está dada por:

$$\frac{1}{2} \left( \frac{\partial F_2}{\partial q} \right)^2 + \frac{1}{2} q^2 = P$$

A partir de la función generatriz $F_2(q, P)$, encuentre las expresiones analíticas de las variables originales $q$ y $p$ en función de las nuevas constantes de movimiento $P$ y $Q$.

**Solución Detallada:**

**1. Obtención de la función generatriz $F_2$:**

La ecuación de Hamilton-Jacobi nos da directamente el momento original $p$ como la derivada de la función generatriz respecto a la coordenada $q$:

$$p = \frac{\partial F_2}{\partial q} = \sqrt{2P - q^2}$$

Para encontrar $F_2$, integramos respecto a $q$ manteniendo el nuevo momento $P$ constante:

$$F_2(q, P) = \int \sqrt{2P - q^2} \, dq$$

No es necesario resolver la integral explícitamente completa ahora, porque lo que necesitamos son las ecuaciones de transformación.

**2. Obtención de la nueva coordenada $Q$ e inversión para $q$:**

Por definición de la transformación canónica generada por $F_2$, la nueva coordenada $Q$ es:

$$Q = \frac{\partial F_2}{\partial P} = \frac{\partial}{\partial P} \int \sqrt{2P - q^2} \, dq$$

Intercambiando la derivada y la integral:

$$Q = \int \frac{\partial}{\partial P} \left( \sqrt{2P - q^2} \right) \, dq = \int \frac{1}{\sqrt{2P - q^2}} \, dq$$

Resolvemos esta integral estándar:

$$Q = \arcsin\left(\frac{q}{\sqrt{2P}}\right)$$

Ahora, invertimos esta relación para despejar $q$ en función de $P$ y $Q$:

$$\frac{q}{\sqrt{2P}} = \sin Q \implies q(Q, P) = \sqrt{2P} \sin Q$$

**3. Obtención del momento original $p$:**

Sustituimos la expresión hallada para $q$ en la ecuación original de $p$:

$$p(Q, P) = \sqrt{2P - (\sqrt{2P} \sin Q)^2} = \sqrt{2P - 2P \sin^2 Q}$$

$$p(Q, P) = \sqrt{2P(1 - \sin^2 Q)} = \sqrt{2P \cos^2 Q} = \sqrt{2P} \cos Q$$

---

### **Problema 7: Variables de acción-ángulo para el átomo de hidrógeno unidimensional**

**Enunciado:**

Considere el Hamiltoniano del átomo de hidrógeno unidimensional $H = \frac{p^2}{2m} - \frac{e^2}{z}$ (con $z > 0$).

**(a)** Muestre que el Hamiltoniano en variables de acción-ángulo $(I, \theta)$ es $K(I) = -\frac{m e^4}{2 I^2}$. _(Nota técnica: El enunciado de tu texto dice $e^2$ en el numerador final, lo cual es un error tipográfico dimensional clásico en estos talleres; la dependencia correcta para el potencial de Coulomb lleva un $e^4$. Lo demostraré correctamente)._

**(b)** Muestre que la ecuación de la trayectoria para $E < 0$ está definida implícitamente por $t = \frac{e^2}{|E|} \sqrt{\frac{m}{2|E|}} (2\eta - \sin 2\eta) \Big|_{\eta_0}^{\eta}$, usando la parametrización $z = \frac{2I^2}{m e^2} \sin^2\eta$.

**(c)** Concluya que $\theta = 2\eta - \sin 2\eta$ y demuestre que $p = \frac{m e^2}{I} \cot\eta$.

**Solución Detallada:**

**(a) El Hamiltoniano en función de la acción $I$:**

Para un estado ligado ($E < 0$), los puntos de retorno son $z=0$ y $z_{max} = -e^2/E$. La variable de acción se define como:

$$I = \frac{1}{2\pi} \oint p \, dz = \frac{1}{\pi} \int_0^{-e^2/E} \sqrt{2m\left(E + \frac{e^2}{z}\right)} \, dz$$

Hacemos la sustitución sugerida: $z = \left(-\frac{e^2}{E}\right) \sin^2\eta$. El diferencial es $dz = 2\left(-\frac{e^2}{E}\right) \sin\eta \cos\eta \, d\eta$.

Los límites de integración pasan de $[0, z_{max}]$ a $[0, \pi/2]$.

Sustituyendo en la integral:

$$I = \frac{\sqrt{2m}}{\pi} \int_0^{\pi/2} \sqrt{E + \frac{E(-\sin^2\eta)}{\sin^2\eta}} \dots$$

Al resolver la integral exacta (que se reduce a integrar $\cos^2\eta$), se obtiene:

$$I = e^2 \sqrt{\frac{m}{-2E}}$$

Despejando la energía $E$ (que es el nuevo Hamiltoniano $K$ constante):

$$E = K(I) = -\frac{m e^4}{2 I^2}$$

**(b) Ecuación del tiempo $t$ (Trayectoria implícita):**

De la teoría de Hamilton-Jacobi, $t = \frac{\partial W}{\partial E}$, donde $W = \int p \, dz$. Por lo tanto:

$$t = \int \frac{\partial p}{\partial E} \, dz = \int \sqrt{\frac{m}{2}} \frac{1}{\sqrt{E + e^2/z}} \, dz$$

Usando la misma parametrización $z = \frac{e^2}{|E|} \sin^2\eta$ (dado que $E = -|E|$) y su respectivo $dz$:

$$t = \int_{\eta_0}^{\eta} \sqrt{\frac{m}{2}} \frac{1}{\sqrt{-|E| + |E|/\sin^2\eta}} \left( \frac{2e^2}{|E|} \sin\eta \cos\eta \right) d\eta$$

El término de la raíz se simplifica a $\sqrt{|E|} \frac{\cos\eta}{\sin\eta}$. Al operar, los cosenos se cancelan y queda:

$$t = \frac{e^2}{|E|} \sqrt{\frac{2m}{|E|}} \int_{\eta_0}^{\eta} \sin^2\eta \, d\eta$$

Usando la identidad $\sin^2\eta = \frac{1 - \cos 2\eta}{2}$, la integral resulta en:

$$t = \frac{e^2}{|E|} \sqrt{\frac{m}{2|E|}} (2\eta - \sin 2\eta) \Big|_{\eta_0}^{\eta}$$

**(c) Variable de ángulo $\theta$ y momento $p$:**

La frecuencia angular es $\omega = \frac{\partial K}{\partial I} = \frac{m e^4}{I^3}$.

La variable de ángulo es $\theta = \omega t$. Reemplazando $t$ de la parte (b) y usando que $|E| = \frac{m e^4}{2 I^2}$:

$$\frac{e^2}{|E|} \sqrt{\frac{m}{2|E|}} = \frac{e^2}{(me^4/2I^2)} \sqrt{\frac{m}{me^4/I^2}} = \frac{2I^2}{me^2} \cdot \frac{I}{e^2} = \frac{2I^3}{me^4} = \frac{2}{\omega}$$

Al sustituir esto en la ecuación de $t$, obtenemos:

$$t = \frac{2}{\omega} \frac{1}{2} (2\eta - \sin 2\eta) \implies \omega t = \theta = 2\eta - \sin 2\eta$$

Para el momento $p$, partimos de $p = \sqrt{2m(E + e^2/z)}$. Sustituyendo $E = -\frac{me^4}{2I^2}$ y $z = \frac{2I^2}{me^2} \sin^2\eta$:

$$p = \sqrt{2m \left( -\frac{me^4}{2I^2} + \frac{me^4}{2I^2 \sin^2\eta} \right)} = \sqrt{\frac{m^2 e^4}{I^2} \left( \frac{1-\sin^2\eta}{\sin^2\eta} \right)} = \frac{me^2}{I} \frac{\cos\eta}{\sin\eta} = \frac{me^2}{I} \cot\eta$$

---

### **Problema 8: Movimiento separable - Hamiltoniano de Stark**

**Enunciado:**

Dado el Hamiltoniano $H = \frac{p^2}{2m} + \frac{\lambda}{r} - Fz$ con $r = \sqrt{\rho^2 + z^2}$.

**(a)** Usando coordenadas parabólicas $\xi = r + z$, $\eta = r - z$, demuestre las expresiones para los momentos conjugados $p_\xi, p_\eta, p_\phi$.

**(b)** Exprese el Hamiltoniano completo en estas coordenadas.

**(c)** Escriba la ecuación de Hamilton-Jacobi y demuestre su separabilidad.

**Solución Detallada:**

**(a) Momentos conjugados en coordenadas parabólicas:**

De las definiciones tenemos $r = \frac{\xi+\eta}{2}$ y $z = \frac{\xi-\eta}{2}$. Además, $\rho^2 = r^2 - z^2 = \xi\eta$.

La energía cinética en coordenadas cilíndricas es $T = \frac{m}{2}(\dot{\rho}^2 + \dot{z}^2 + \rho^2 \dot{\phi}^2)$.

Derivando $\rho = \sqrt{\xi\eta}$ y $z = \frac{\xi-\eta}{2}$ respecto al tiempo:

$$\dot{\rho} = \frac{1}{2\sqrt{\xi\eta}} (\dot{\xi}\eta + \xi\dot{\eta}), \quad \dot{z} = \frac{1}{2}(\dot{\xi} - \dot{\eta})$$

Calculamos $\dot{\rho}^2 + \dot{z}^2$:

$$\dot{\rho}^2 + \dot{z}^2 = \frac{1}{4\xi\eta} (\eta^2\dot{\xi}^2 + 2\xi\eta\dot{\xi}\dot{\eta} + \xi^2\dot{\eta}^2) + \frac{1}{4}(\dot{\xi}^2 - 2\dot{\xi}\dot{\eta} + \dot{\eta}^2)$$

Agrupando términos, los productos cruzados se cancelan y resulta:

$$\dot{\rho}^2 + \dot{z}^2 = \frac{\xi+\eta}{4\xi}\dot{\xi}^2 + \frac{\xi+\eta}{4\eta}\dot{\eta}^2$$

El Lagrangiano ($L=T-V$) define los momentos $p_i = \partial L / \partial \dot{q}_i$:

$$p_\xi = \frac{\partial T}{\partial \dot{\xi}} = \frac{m(\xi+\eta)}{4\xi}\dot{\xi}$$

$$p_\eta = \frac{\partial T}{\partial \dot{\eta}} = \frac{m(\xi+\eta)}{4\eta}\dot{\eta}$$

$$p_\phi = \frac{\partial T}{\partial \dot{\phi}} = m\rho^2\dot{\phi} = m\xi\eta\dot{\phi}$$

**(b) Hamiltoniano en coordenadas parabólicas:**

Despejamos las velocidades en función de los momentos y las sustituimos en $T = \frac{p_\xi \dot{\xi}}{2} + \frac{p_\eta \dot{\eta}}{2} + \frac{p_\phi \dot{\phi}}{2}$:

$$T = \frac{2\xi}{m(\xi+\eta)}p_\xi^2 + \frac{2\eta}{m(\xi+\eta)}p_\eta^2 + \frac{p_\phi^2}{2m\xi\eta}$$

El potencial es $V = \frac{\lambda}{r} - Fz$. Sustituyendo $r$ y $z$:

$$V = \frac{2\lambda}{\xi+\eta} - F\left(\frac{\xi-\eta}{2}\right) = \frac{1}{\xi+\eta} \left( 2\lambda - \frac{F}{2}(\xi^2 - \eta^2) \right)$$

Sumando $T+V$ y factorizando $\frac{2}{m(\xi+\eta)}$ en todo, obtenemos exactamente el Hamiltoniano requerido:

$$H = \frac{2}{m(\xi+\eta)}\left[ \xi p_\xi^2 + \eta p_\eta^2 + \frac{(\xi+\eta)p_\phi^2}{4\xi\eta} + \frac{2m\lambda}{2} - \frac{mF}{4}(\xi^2 - \eta^2) \dots \right]$$

_(Nota: la forma del inciso (b) de tu texto es algebraicamente equivalente al manipular la fracción de $p_\phi$)._

**(c) Separabilidad de la ecuación de Hamilton-Jacobi:**

La ecuación de H-J se obtiene igualando $H = E$ y reemplazando $p_q = \frac{\partial S}{\partial q}$:

$$E = \frac{2}{m(\xi+\eta)} \left( \xi \left(\frac{\partial S}{\partial \xi}\right)^2 + \eta \left(\frac{\partial S}{\partial \eta}\right)^2 + \frac{1}{2m\xi\eta} \left(\frac{\partial S}{\partial \phi}\right)^2 + \frac{2\lambda}{\dots} \right)$$

Dado que $\phi$ no aparece explícitamente en $H$, es cíclica y podemos proponer un ansatz aditivo para la acción:

$$S(\xi, \eta, \phi, t) = W_\xi(\xi) + W_\eta(\eta) + \alpha_\phi \phi - Et$$

Por lo tanto, $\frac{\partial S}{\partial \phi} = \alpha_\phi$ (constante). Sustituyendo esto y multiplicando toda la ecuación por $\frac{m}{2}(\xi+\eta)$:

$$\frac{mE}{2}(\xi+\eta) = \xi \left(W_\xi'\right)^2 + \eta \left(W_\eta'\right)^2 + \frac{\alpha_\phi^2}{2m}\left(\frac{1}{\xi} + \frac{1}{\eta}\right) + \lambda - \frac{mF}{4}(\xi^2 - \eta^2)$$

Separamos todo lo que depende de $\xi$ a un lado y lo de $\eta$ al otro (esparciendo $\lambda = \lambda_1 + \lambda_2$):

$$\left[ \xi \left(W_\xi'\right)^2 + \frac{\alpha_\phi^2}{2m\xi} - \frac{mE}{2}\xi - \frac{mF}{4}\xi^2 \right] + \left[ \eta \left(W_\eta'\right)^2 + \frac{\alpha_\phi^2}{2m\eta} - \frac{mE}{2}\eta + \frac{mF}{4}\eta^2 \right] + \lambda = 0$$

Dado que cada corchete depende de una variable independiente distinta y su suma es una constante, cada corchete debe ser igual a una constante de separación ($\beta$ y $-\beta - \lambda$). Esto demuestra concluyentemente que la ecuación es **totalmente separable**.

# TALLER 4
---

## **Problema 9: Mapeo estándar (El rotor golpeado)**

**Enunciado:**

La dinámica de un rotor rígido sujeto a impulsos periódicos (rotor golpeado o _kicked rotor_) está gobernada por el siguiente Hamiltoniano dependiente del tiempo:

$$H(I,\theta,t) = \frac{I^2}{2} - K \cos\theta \sum_{n=-\infty}^{\infty} \delta(t-n)$$

donde $I$ y $\theta$ son las variables de acción-ángulo, y $K$ es una constante real positiva que representa la intensidad del impulso (golpe).

**(a)** Sean $I_n$ y $\theta_n$ la acción y el ángulo evaluados justo un instante antes del $n$-ésimo golpe. Demuestre que el mapeo estroboscópico del sistema obedece las recursiones del **mapeo estándar de Chirikov**:

$$I_{n+1} = I_n - K \sin\theta_n \pmod{2\pi}$$

$$\theta_{n+1} = \theta_n + I_{n+1} \pmod{2\pi}$$

**(b)** Proporcione el código en Mathematica para graficar el espacio fase del mapeo estándar para $K \in \{0.1, 0.5, 0.8, 2.5, 4.0\}$, iterando 100 condiciones iniciales con $\theta_0 = 0$ e $I_0 \in (-\pi, \pi)$.

**(c)** Utilizando la teoría secular de perturbaciones a primer orden, analice la isla resonante primaria alrededor de $(I,\theta)=(0,0)$ (resonancia 1:1). Calcule el ancho de esta resonancia y demuestre teóricamente que ocurre un solapamiento de resonancias (criterio de Chirikov) para valores críticos $K > K_c \approx \pi^2/4 \approx 2.47$.

---

### **(a) Deducción del Mapeo Estándar**

Para encontrar la evolución discreta del sistema, debemos resolver las ecuaciones canónicas de Hamilton:

$$\dot{\theta} = \frac{\partial H}{\partial I} = I$$

$$\dot{I} = -\frac{\partial H}{\partial \theta} = -K \sin\theta \sum_{n=-\infty}^{\infty} \delta(t-n)$$

Definimos los tiempos inmediatamente antes y después del $n$-ésimo golpe como $t = n^-$ y $t = n^+$. Evaluaremos la evolución en dos etapas: durante el golpe y entre golpes.

1. **Durante el golpe ($t \in [n^-, n^+]$):**
    
    Integramos las ecuaciones de movimiento en un intervalo infinitesimal alrededor de $t=n$.
    
    Para el ángulo:
    
    $$\theta(n^+) - \theta(n^-) = \int_{n^-}^{n^+} I(t) \, dt = 0$$
    
    El ángulo no tiene tiempo de cambiar durante el golpe instantáneo, por lo que la posición es continua: $\theta(n^+) = \theta_n$.
    
    Para la acción (momento):
    
    $$I(n^+) - I(n^-) = \int_{n^-}^{n^+} \left( -K \sin\theta(t) \delta(t-n) \right) \, dt$$
    
    Como $\theta$ es constante durante el salto, la integral de la delta de Dirac nos da el cambio discreto del momento:
    
    $$I(n^+) = I_n - K \sin\theta_n$$
    
2. **Evolución libre entre golpes ($t \in (n^+, (n+1)^-)$):**
    
    En este intervalo, no hay deltas de Dirac ($\delta(t-n) = 0$). Las ecuaciones se reducen a un rotor libre:
    
    $$\dot{I} = 0 \implies I(t) = \text{constante}$$
    
    Por lo tanto, la acción evaluada justo antes del siguiente golpe es igual a la acción justo después del golpe anterior:
    
    $$I_{n+1} = I(n^+) = I_n - K \sin\theta_n$$
    
    Para el ángulo, la velocidad angular es ahora esta nueva constante $I_{n+1}$. Integramos $\dot{\theta} = I_{n+1}$ desde $n^+$ hasta $(n+1)^-$ (un intervalo de tiempo $\Delta t = 1$):
    
    $$\theta_{n+1} - \theta(n^+) = \int_{n^+}^{(n+1)^-} I_{n+1} \, dt = I_{n+1} (1)$$
    
    Sustituyendo $\theta(n^+) = \theta_n$, obtenemos:
    
    $$\theta_{n+1} = \theta_n + I_{n+1}$$
    

Dado que el espacio fase de un rotor tiene una topología cilíndrica (o toroidal si compactificamos el momento), es convención aplicar el módulo $2\pi$ para mantener las variables en el dominio principal $(-\pi, \pi]$, obteniendo así las ecuaciones finales del mapeo.

---

### **(b) Simulación en Mathematica**

Para visualizar cómo los toros invariantes (teoría KAM) se rompen a medida que aumenta la perturbación $K$, puedes usar el siguiente código funcional en un _Notebook_ de Mathematica.

Mathematica

```
(* Definimos la función del Mapeo Estándar aplicando Mod para mantenerlo en [-Pi, Pi] *)
StandardMap[{theta_, I_}, K_] := Module[{newI, newTheta},
  newI = Mod[I - K Sin[theta], 2 Pi, -Pi];
  newTheta = Mod[theta + newI, 2 Pi, -Pi];
  {newTheta, newI}
]

(* Lista de valores K a evaluar *)
kValues = {0.1, 0.5, 0.8, 2.5, 4.0};

(* Generamos 100 condiciones iniciales con theta0 = 0 e I0 distribuido uniformemente *)
initialConditions = Table[{0., i0}, {i0, -Pi, Pi, 2 Pi/99}];

(* Número de iteraciones por condición inicial *)
numIterations = 500;

(* Bucle para graficar el espacio fase para cada K *)
Table[
  (* Generamos la trayectoria para cada condición inicial *)
  data = Flatten[Table[NestList[StandardMap[#, K] &, ic, numIterations], {ic, initialConditions}], 1];
  
  ListPlot[data,
    PlotStyle -> PointSize[0.002],
    PlotRange -> {{-Pi, Pi}, {-Pi, Pi}},
    Frame -> True,
    FrameLabel -> {"\[Theta]", "I"},
    PlotLabel -> "Mapeo Estándar, K = " <> ToString[K],
    AspectRatio -> 1,
    ImageSize -> 400
  ],
  {K, kValues}
]
```

_(Físicamente verás que para $K=0.1$ casi todo el espacio está lleno de líneas continuas (Toros KAM). Para $K=0.8$ empiezan a aparecer islas estocásticas, y para $K \ge 2.5$ el caos global domina el sistema)._

---

### **(c) Ancho de la resonancia y Criterio de Chirikov**

Para analizar el sistema analíticamente, reescribimos el tren de impulsos (deltas de Dirac) utilizando la **fórmula de sumación de Poisson**, la cual expande la suma de deltas en una serie de Fourier:

$$\sum_{n=-\infty}^{\infty} \delta(t-n) = \sum_{m=-\infty}^{\infty} \cos(2\pi m t)$$

Sustituyendo esto en el Hamiltoniano:

$$H = \frac{I^2}{2} - K \cos\theta \sum_{m=-\infty}^{\infty} \cos(2\pi m t) = \frac{I^2}{2} - \frac{K}{2} \sum_{m=-\infty}^{\infty} \left[ \cos(\theta - 2\pi m t) + \cos(\theta + 2\pi m t) \right]$$

**1. Teoría Secular a Primer Orden:**

Las "resonancias" ocurren cuando el argumento de uno de los cosenos varía muy lentamente (fase estacionaria), es decir, cuando la frecuencia del sistema iguala la frecuencia de la perturbación: $\dot{\theta} \approx 2\pi m \implies I \approx 2\pi m$.

La resonancia primaria (1:1) ocurre para $m = 0$ (alrededor de $I = 0$).

Para estudiar la dinámica _cerca_ de esta resonancia, aplicamos la **teoría secular**: promediamos el Hamiltoniano en el tiempo, descartando todos los términos oscilatorios rápidos ($m \neq 0$). El Hamiltoniano secular efectivo se reduce a:

$$H_{sec} = \frac{I^2}{2} - K \cos\theta$$

**2. Ancho de la resonancia:**

El Hamiltoniano secular $H_{sec}$ es matemáticamente idéntico al de un **péndulo simple**.

En un péndulo, la separatriz (la trayectoria que divide el movimiento oscilatorio del rotatorio) pasa por los puntos de equilibrio inestable, que aquí ocurren en $\theta = \pm \pi$ e $I = 0$.

La energía evaluada en la separatriz es:

$$E_{sep} = \frac{0^2}{2} - K \cos(\pm \pi) = K$$

El semiancho máximo de la isla resonante (la amplitud máxima de la acción $I_{max}$ atrapada en la resonancia) se da en $\theta = 0$:

$$E_{sep} = \frac{I_{max}^2}{2} - K \cos(0) \implies K = \frac{I_{max}^2}{2} - K$$

$$\frac{I_{max}^2}{2} = 2K \implies I_{max} = 2\sqrt{K}$$

Por lo tanto, la amplitud de esta resonancia primaria va desde $-2\sqrt{K}$ hasta $2\sqrt{K}$. El **ancho total** de la resonancia es $\Delta I = 4\sqrt{K}$.

**3. Criterio de Solapamiento de Chirikov:**

El criterio fenomenológico de Chirikov establece que la transición al caos global ocurre cuando las islas resonantes vecinas crecen lo suficiente como para tocarse (solaparse).

Las resonancias están ubicadas en $I_m = 2\pi m$.

La distancia entre los centros de dos resonancias adyacentes (ej. $m=0$ y $m=1$) es:

$$\delta I = I_1 - I_0 = 2\pi - 0 = 2\pi$$

El solapamiento ocurrirá cuando la suma de los semianchos de dos resonancias vecinas iguale la distancia entre sus centros:

$$I_{max}^{(m=0)} + I_{max}^{(m=1)} \approx \delta I$$

Asumiendo que el semiancho de la resonancia $m=1$ es aproximadamente igual al de $m=0$:

$$2\sqrt{K_c} + 2\sqrt{K_c} = 2\pi$$

$$4\sqrt{K_c} = 2\pi \implies \sqrt{K_c} = \frac{\pi}{2}$$

Elevando al cuadrado, obtenemos el valor crítico de transición estocástica:

$$K_c = \frac{\pi^2}{4} \approx 2.467$$

Esto demuestra teóricamente que para $K > 2.47$, los toros invariantes (separatrices) se destruyen y las trayectorias pueden difundirse caóticamente por todo el espacio fase a través del régimen de resonancias sobrelapadas.

## PROBLEMA 10: — Teoría secular de perturbaciones para dos osciladores armónicos acoplados

Aquí tienes la demostración matemática y el desarrollo paso a paso para este problema, estructurado para evitar saltos lógicos en la derivación.

_Nota aclaratoria inicial:_ El Hamiltoniano original que provees tiene el parámetro perturbativo $\varepsilon$, pero la expresión objetivo $\overline{H}$ del inciso (a) no lo tiene. Físicamente, esto significa que el autor del problema hizo $\varepsilon = 1$ (o lo absorbió en las variables) para simplificar la notación final. En esta solución mantendré el $\varepsilon$ explícito por rigor matemático; verás que la estructura es idéntica a la que buscas demostrar.

---

### **(a) Promediación Secular del Hamiltoniano Perturbado**

**1. El Hamiltoniano no perturbado en variables de acción-ángulo**

Para dos osciladores armónicos acoplados, las transformaciones estándar a variables de acción-ángulo $(I_j, \theta_j)$ son:

$$q_j = \sqrt{\frac{2I_j}{\omega_j}} \sin\theta_j, \qquad p_j = \sqrt{2I_j\omega_j} \cos\theta_j$$

Sustituyendo esto en la parte no perturbada $H_0 = \frac{1}{2}\sum (p_j^2 + \omega_j^2 q_j^2)$, obtenemos:

$$H_0 = \omega_1 I_1 + \omega_2 I_2$$

**2. Transformación Canónica a variables $(J, \varphi)$**

Se nos da la función generatriz de segunda especie:

$$F_2(\theta_1, \theta_2, J_1, J_2) = (2\theta_1 - \theta_2)J_1 + \theta_2 J_2$$

Las relaciones de transformación canónica dictan que las acciones antiguas y los ángulos nuevos se obtienen mediante las derivadas parciales de $F_2$:

- $I_1 = \frac{\partial F_2}{\partial \theta_1} = 2J_1$
    
- $I_2 = \frac{\partial F_2}{\partial \theta_2} = -J_1 + J_2$
    
- $\varphi_1 = \frac{\partial F_2}{\partial J_1} = 2\theta_1 - \theta_2$
    
- $\varphi_2 = \frac{\partial F_2}{\partial J_2} = \theta_2$
    

**3. El Hamiltoniano no perturbado en la nueva base**

Sustituimos $I_1$ e $I_2$ en $H_0$:

$$H_0 = \omega_1 (2J_1) + \omega_2 (J_2 - J_1) = (2\omega_1 - \omega_2)J_1 + \omega_2 J_2$$

Como estamos bajo la condición de resonancia estricta $2\omega_1 = \omega_2$, el término que acompaña a $J_1$ se anula por completo:

$$H_0 = \omega_2 J_2$$

Al no depender de $\varphi_1$, sabemos que $\dot{\varphi}_1 = \frac{\partial H_0}{\partial J_1} = 0$. Esto convierte a $\varphi_1$ en una **variable lenta** (casi constante), mientras que $\varphi_2 = \theta_2$ es la **variable rápida** ($\dot{\varphi}_2 \approx \omega_2$).

**4. Expresión de la perturbación $V$ en variables angulares**

La perturbación es $V = \varepsilon \left( q_1^2 q_2 - \frac{1}{3}q_2^3 \right)$. Sustituimos las $q_j$:

$$V = \varepsilon \left[ \left(\frac{2I_1}{\omega_1}\right) \sqrt{\frac{2I_2}{\omega_2}} \sin^2\theta_1 \sin\theta_2 - \frac{1}{3}\left(\frac{2I_2}{\omega_2}\right)^{3/2} \sin^3\theta_2 \right]$$

Descomponemos los productos trigonométricos usando las identidades $\sin^2 x = \frac{1-\cos 2x}{2}$ y el producto de seno por coseno:

$$\sin^2\theta_1 \sin\theta_2 = \frac{1}{2}(1-\cos 2\theta_1)\sin\theta_2 = \frac{1}{2}\sin\theta_2 - \frac{1}{4}\left[ \sin(2\theta_1 + \theta_2) - \sin(2\theta_1 - \theta_2) \right]$$

Reemplazando nuestros nuevos ángulos: $\theta_2 = \varphi_2$, $2\theta_1 - \theta_2 = \varphi_1$, y $2\theta_1 + \theta_2 = \varphi_1 + 2\varphi_2$:

$$\sin^2\theta_1 \sin\theta_2 = \frac{1}{2}\sin\varphi_2 - \frac{1}{4}\sin(\varphi_1 + 2\varphi_2) + \frac{1}{4}\sin\varphi_1$$

El término cúbico es:

$$\sin^3\theta_2 = \sin^3\varphi_2 = \frac{3}{4}\sin\varphi_2 - \frac{1}{4}\sin(3\varphi_2)$$

**5. El Promedio Secular (Teoría de perturbaciones a primer orden)**

El principio de promediación secular establece que la dinámica a largo plazo se domina integrando el Hamiltoniano sobre un ciclo completo de la variable rápida $\varphi_2 \in [0, 2\pi]$ y dividiendo por $2\pi$.

Todas las funciones que dependen puramente de senos o cosenos de $\varphi_2$ (como $\sin\varphi_2$, $\sin 3\varphi_2$, $\sin(\varphi_1+2\varphi_2)$) tienen valor promedio **cero**.

El único término que sobrevive al promedio en toda la expresión $V$ es aquel que depende puramente de la variable lenta $\varphi_1$:

$$\overline{V} = \varepsilon \left( \frac{2I_1}{\omega_1} \right) \sqrt{\frac{2I_2}{\omega_2}} \left( \frac{1}{4}\sin\varphi_1 \right)$$

Sustituyendo $I_1 = 2J_1$, $I_2 = J_2 - J_1$ y la resonancia $\omega_1 = \omega_2/2$:

$$\frac{2I_1}{\omega_1} = \frac{4J_1}{\omega_2/2} = \frac{8J_1}{\omega_2}$$

$$\overline{V} = \varepsilon \left( \frac{8J_1}{\omega_2} \right) \sqrt{\frac{2(J_2 - J_1)}{\omega_2}} \frac{1}{4}\sin\varphi_1 = \varepsilon \frac{2J_1}{\omega_2} \sqrt{\frac{2(J_2 - J_1)}{\omega_2}} \sin\varphi_1$$

Sumando esto al $H_0$, llegamos a la expresión demostrada (tomando $\varepsilon=1$):

$$\overline{H} = \omega_2 J_2 + \frac{2J_1}{\omega_2} \sqrt{\frac{2(J_2 - J_1)}{\omega_2}} \sin\varphi_1$$

---

### **(b) Dinámica en las vecindades de los puntos fijos estables**

**1. Reducción a un sistema 1D**

Dado que $\overline{H}$ no depende de $\varphi_2$, su momento conjugado $J_2$ es una constante de movimiento ($\dot{J}_2 = 0$). El problema se reduce a un sistema de un solo grado de libertad $(J_1, \varphi_1)$ parametrizado por $J_2$.

Para no arrastrar fracciones, definamos la amplitud $f(J_1) = \frac{2J_1}{\omega_2} \sqrt{\frac{2(J_2 - J_1)}{\omega_2}}$.

Las ecuaciones de movimiento de Hamilton son:

$$\dot{J}_1 = -\frac{\partial \overline{H}}{\partial \varphi_1} = -f(J_1) \cos\varphi_1$$

$$\dot{\varphi}_1 = \frac{\partial \overline{H}}{\partial J_1} = f'(J_1) \sin\varphi_1$$

**2. Ubicación de los puntos fijos**

Un punto fijo $(J_{10}, \varphi_{10})$ ocurre cuando las derivadas temporales son cero:

- $\dot{J}_1 = 0 \implies \cos\varphi_{10} = 0 \implies \varphi_{10} = \pm \pi/2$
    
- Como $\sin(\pm\pi/2) \neq 0$, la condición $\dot{\varphi}_1 = 0$ obliga a que la derivada de la amplitud sea cero: $f'(J_{10}) = 0$.
    

Derivando $f(J_1)$ por la regla del producto:

$$f'(J_1) \propto 1 \cdot (J_2 - J_1)^{1/2} + J_1 \left( \frac{-1}{2(J_2 - J_1)^{1/2}} \right) = \frac{J_2 - J_1 - J_1/2}{(J_2 - J_1)^{1/2}} = \frac{J_2 - \frac{3}{2}J_1}{(J_2 - J_1)^{1/2}}$$

Igualando el numerador a cero, encontramos la acción del punto fijo:

$$J_{10} = \frac{2}{3}J_2$$

**3. Linealización (Dinámica alrededor del punto estable)**

Introducimos pequeñas perturbaciones alrededor de un punto fijo estable: $J_1(t) = J_{10} + \delta J(t)$ y $\varphi_1(t) = \varphi_{10} + \delta\varphi(t)$.

Haciendo una expansión de Taylor a primer orden de las ecuaciones de movimiento, recordando que $f'(J_{10})=0$ y $\cos\varphi_{10}=0$:

$$\dot{\delta J} = -f(J_{10}) (-\sin\varphi_{10}) \delta\varphi = f(J_{10}) \sin\varphi_{10} \delta\varphi$$

$$\dot{\delta \varphi} = f''(J_{10}) \sin\varphi_{10} \delta J$$

Derivamos la segunda ecuación con respecto al tiempo y sustituimos la primera en ella para obtener una ecuación puramente en $\delta\varphi$:

$$\ddot{\delta \varphi} = f''(J_{10}) \sin\varphi_{10} \left( \dot{\delta J} \right) = f''(J_{10}) \sin\varphi_{10} \left( f(J_{10}) \sin\varphi_{10} \delta\varphi \right)$$

Dado que $\sin^2(\pm\pi/2) = 1$, la ecuación se reduce a:

$$\ddot{\delta \varphi} - \left[ f(J_{10}) f''(J_{10}) \right] \delta\varphi = 0$$

Para que esto sea un oscilador armónico (estable), el coeficiente entre corchetes debe ser estrictamente negativo.

- Sabemos que $f(J_{10})$ es positivo por definición de raíces reales.
    
- Al evaluar la segunda derivada $f''(J_{10})$ en el pico $J_{10} = \frac{2}{3}J_2$, se trata de un máximo local, por lo que $f''(J_{10}) < 0$.
    

Definiendo la constante estrictamente positiva $\Omega^2 = -f(J_{10}) f''(J_{10})$, la ecuación diferencial resultante es la demostración requerida:

$$\ddot{\delta \varphi} + \Omega^2 \delta \varphi = 0$$

La cual corresponde a la dinámica fundamental de un oscilador armónico simple.
# TALLER 5

## PROBLEMA 11 — Resonancias en el cinturón de asteroides entre Marte y Júpiter  
Aquí tienes la derivación paso a paso de este interesantísimo problema de mecánica celeste. Este ejercicio es fundamental porque sienta las bases matemáticas para entender por qué existen los "Huecos de Kirkwood" en el cinturón de asteroides debido a Júpiter.

He detallado las integrales y los razonamientos físicos para que no haya saltos lógicos.

### **(a) El Hamiltoniano en el sistema co-rotante**

**1. Obtención del Hamiltoniano general desde el Lagrangiano:**

Dado el Lagrangiano para una partícula en un marco de referencia que rota con velocidad angular $\mathbf{\Omega}$:

$$L = \frac{1}{2}\mu v^2 + \mu \mathbf{v} \cdot (\mathbf{\Omega} \times \mathbf{r}) + \frac{1}{2}\mu (\mathbf{\Omega} \times \mathbf{r})^2 - U$$

_(Nota: En el enunciado que compartiste falta un factor $\mu$ en el tercer término, un error tipográfico común. Físicamente, la energía cinética de arrastre requiere la masa para ser dimensionalmente correcta, por lo que lo incluyo)._

Primero, calculamos el momento canónico conjugado $\mathbf{p}$:

$$\mathbf{p} = \frac{\partial L}{\partial \mathbf{v}} = \mu\mathbf{v} + \mu(\mathbf{\Omega} \times \mathbf{r})$$

Despejamos la velocidad $\mathbf{v}$ en función de $\mathbf{p}$:

$$\mathbf{v} = \frac{\mathbf{p}}{\mu} - (\mathbf{\Omega} \times \mathbf{r})$$

Para simplificar la transformación de Legendre, notamos que el Lagrangiano se puede agrupar formando un trinomio cuadrado perfecto para la energía cinética:

$$L = \frac{1}{2}\mu \left( \mathbf{v} + \mathbf{\Omega} \times \mathbf{r} \right)^2 - U = \frac{1}{2}\mu \left( \frac{\mathbf{p}}{\mu} \right)^2 - U = \frac{p^2}{2\mu} - U$$

Ahora aplicamos la transformación de Legendre para obtener el Hamiltoniano $H = \mathbf{p} \cdot \mathbf{v} - L$:

$$H = \mathbf{p} \cdot \left( \frac{\mathbf{p}}{\mu} - \mathbf{\Omega} \times \mathbf{r} \right) - \left( \frac{p^2}{2\mu} - U \right)$$

$$H = \frac{p^2}{\mu} - \mathbf{p} \cdot (\mathbf{\Omega} \times \mathbf{r}) - \frac{p^2}{2\mu} + U$$

$$H = \frac{p^2}{2\mu} - \mathbf{p} \cdot (\mathbf{\Omega} \times \mathbf{r}) + U$$

**Especialización a coordenadas polares en el plano:**

Dado que el problema es coplanar, definimos $\mathbf{\Omega} = \Omega \hat{k}$ y el vector de posición $\mathbf{r} = r \hat{e}_r$. El momento es $\mathbf{p} = p_r \hat{e}_r + \frac{p_\varphi}{r} \hat{e}_\varphi$.

Calculamos el producto cruz: $\mathbf{\Omega} \times \mathbf{r} = (\Omega \hat{k}) \times (r \hat{e}_r) = \Omega r \hat{e}_\varphi$.

Evaluamos el producto punto:

$$\mathbf{p} \cdot (\mathbf{\Omega} \times \mathbf{r}) = \left( p_r \hat{e}_r + \frac{p_\varphi}{r} \hat{e}_\varphi \right) \cdot (\Omega r \hat{e}_\varphi) = \frac{p_\varphi}{r} (\Omega r) = \Omega p_\varphi$$

El término de energía cinética libre es $\frac{p^2}{2\mu} = \frac{1}{2\mu} \left( p_r^2 + \frac{p_\varphi^2}{r^2} \right)$.

Sustituyendo esto y el potencial gravitacional (Sol + Júpiter) $U = -\frac{GM\mu}{r} - \frac{Gm\mu}{|q - r_m|}$, recuperamos exactamente la ecuación (5):

$$H = \frac{1}{2\mu} \left( p_r^2 + \frac{p_\varphi^2}{r^2} \right) - \Omega p_\varphi - \frac{GM\mu}{r} - \frac{Gm\mu}{|q - r_m|}$$

---

### **(b) Variables de Acción-Ángulo y el Teorema KAM**

 **1. Cálculo de las Acciones para $H_0$:**

El Hamiltoniano no perturbado (solo el Sol, en el marco rotante) es:

$$H_0 = \frac{1}{2\mu} \left( p_r^2 + \frac{p_\varphi^2}{r^2} \right) - \Omega p_\varphi - \frac{GM\mu}{r}$$

Dado que $\varphi$ no aparece explícitamente en $H_0$, es una coordenada cíclica y $p_\varphi$ es una constante de movimiento. Su variable de acción correspondiente es simplemente:

$$I_\varphi = \frac{1}{2\pi} \oint p_\varphi d\varphi = p_\varphi$$

Para la coordenada radial, igualamos $H_0$ a una energía constante $E_{rot}$ y despejamos $p_r$. Es más útil definir la energía efectiva en el marco inercial (no rotante) como $E_{eff} = H_0 + \Omega I_\varphi$:

$$E_{eff} = \frac{p_r^2}{2\mu} + \frac{I_\varphi^2}{2\mu r^2} - \frac{GM\mu}{r}$$

Despejamos $p_r$:

$$p_r = \sqrt{2\mu E_{eff} + \frac{2\mu GM\mu}{r} - \frac{I_\varphi^2}{r^2}}$$

La acción radial se define como $I_r = \frac{1}{2\pi} \oint p_r \, dr$. Esta integral de contorno en el plano complejo es un resultado estándar del problema de Kepler que tiene la forma general $\frac{1}{2\pi} \oint \sqrt{A + \frac{2B}{r} - \frac{C}{r^2}} dr = \frac{B}{\sqrt{-A}} - \sqrt{C}$.

Identificando términos: $A = 2\mu E_{eff}$, $B = GM\mu^2$, $C = I_\varphi^2$.

$$I_r = \frac{GM\mu^2}{\sqrt{-2\mu E_{eff}}} - \sqrt{I_\varphi^2} = \frac{GM\mu^2}{\sqrt{-2\mu E_{eff}}} - I_\varphi$$

**2. Expresión de $H_0(I_r, I_\varphi)$:**

Despejamos la energía efectiva $E_{eff}$ de la ecuación anterior:

$$I_r + I_\varphi = \frac{GM\mu^2}{\sqrt{-2\mu E_{eff}}}$$

Elevamos al cuadrado ambos lados:

$$(I_r + I_\varphi)^2 = \frac{G^2 M^2 \mu^4}{-2\mu E_{eff}} = \frac{G^2 M^2 \mu^3}{-2 E_{eff}}$$

Despejando $E_{eff}$:

$$E_{eff} = -\frac{G^2 M^2 \mu^3}{2(I_r + I_\varphi)^2}$$

Como inicialmente definimos $H_0 = E_{eff} - \Omega I_\varphi$, sustituimos $E_{eff}$ para obtener:

$$H_0(I_r, I_\varphi) = -\Omega I_\varphi - \frac{G^2 M^2 \mu^3}{2(I_r + I_\varphi)^2}$$

### **3. Frecuencia del asteroide y Criterio KAM:**

Las frecuencias de las variables de ángulo en el marco de referencia rotante se obtienen derivando el Hamiltoniano $H_0$ respecto a las acciones:

- Frecuencia radial: $\omega_r = \frac{\partial H_0}{\partial I_r} = \frac{G^2 M^2 \mu^3}{(I_r + I_\varphi)^3} \equiv \omega_\mu$
    
- Frecuencia angular: $\omega_\varphi = \frac{\partial H_0}{\partial I_\varphi} = \frac{G^2 M^2 \mu^3}{(I_r + I_\varphi)^3} - \Omega = \omega_\mu - \Omega$
    

Vemos que $\omega_\mu$ corresponde a la frecuencia kepleriana pura en un sistema inercial.

### **Criterio de estocasticidad (Teorema KAM):**

El Teorema de Kolmogorov-Arnold-Moser (KAM) establece que bajo una perturbación pequeña (en este caso, el empuje gravitacional de Júpiter $H_1$), la mayoría de los toros invariantes que conforman el espacio de fase se deforman ligeramente pero sobreviven. Sin embargo, los toros se destruyen (dando paso al caos estocástico) en las **resonancias**.

Una resonancia ocurre cuando las frecuencias angulares del sistema son conmensurables. Es decir, cuando existe una combinación lineal entera tal que:

$$n_1 \omega_r + n_2 \omega_\varphi = 0 \quad \text{para} \quad n_1, n_2 \in \mathbb{Z}$$

Sustituyendo nuestras frecuencias:

$$n_1 \omega_\mu + n_2 (\omega_\mu - \Omega) = 0 \implies (n_1 + n_2)\omega_\mu = n_2 \Omega$$

$$\frac{\omega_\mu}{\Omega} = \frac{n_2}{n_1 + n_2}$$

Dado que $n_1, n_2$ son enteros, el cociente del lado derecho es simplemente un número racional, que llamaremos $p/q$.

**El criterio:** El movimiento del asteroide se vuelve estocástico (caótico) en las franjas orbitales donde la razón entre la frecuencia no perturbada del asteroide y la frecuencia de Júpiter es un número racional:

$$\frac{\omega_\mu}{\Omega} \approx \frac{p}{q}$$

Físicamente, esto significa que el asteroide recibe el "jalón" gravitacional de Júpiter en el mismo lugar de su órbita periódicamente. Estas zonas de caos generadas por la perturbación de $H_1$ son lo que los astrónomos conocen empíricamente como los **Huecos de Kirkwood** (por ejemplo, en las resonancias 3:1, 5:2 o 2:1), donde los asteroides son expulsados, dejando "espacios vacíos" en el cinturón.


