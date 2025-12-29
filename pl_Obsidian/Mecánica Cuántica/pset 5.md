Aquí tienes los enunciados de los ejercicios del Problem Set 5 de Física Cuántica I (MIT 8.04), traducidos al español:

## **1. Gaussianas y saturación del producto de incertidumbre**

Considera la función de onda gaussiana $\psi(x)=N \exp(-\frac{1}{2}\frac{x^{2}}{a^{2}})$ , donde $N$ es una constante de normalización real y $a$ es una constante positiva real con unidades de longitud.

- **(a)** Utiliza la función de onda en el espacio de posiciones para calcular las incertidumbres $\Delta x$ y $\Delta p$. Confirma que tu respuesta satura el producto de incertidumbre de Heisenberg $\Delta x \Delta p \ge \frac{\hbar}{2}$.
    
- **(b)** Calcula la transformada de Fourier $\phi(p)$ de $\psi(x)$. Utiliza el teorema de Parseval para confirmar tu respuesta y luego recalcula $\Delta p$ usando el espacio de momentos.
    

---

## **2. Gaussianas complejas y el producto de incertidumbre**

Considera la función de onda gaussiana $\psi(x)=N \exp(-\frac{1}{2}\frac{x^{2}}{\Delta^{2}})$, donde $\Delta \in \mathbb{C}$ y $Re(\Delta^{2})>0$. Aquí $N$ es una constante de normalización real y $\Delta$ es ahora un número complejo.

- **(a)** Calcula las incertidumbres $\Delta x$ y $\Delta p$ dejando tu respuesta en términos de $|\Delta|$ y $Re(\Delta^{2})$.
    
- **(b)** Calcula la transformada de Fourier $\phi(p)$ de $\psi(x)$, confirma con Parseval y recalcula $\Delta p$ en el espacio de momentos.
    
- **(c)** Parametrizando $\Delta = |\Delta|e^{i\phi_{\Delta}}$, calcula el producto $\Delta x \Delta p$ y confirma que puede expresarse mediante una función trigonométrica de $\phi_{\Delta}$.
    
- **(d)** Examina la evolución temporal de un paquete de ondas gaussiano y confirma que $\Delta p$ da un resultado independiente del tiempo.
    

---

## **3. Ejercicios con una partícula en una caja**

Para una partícula de masa $m$ en un intervalo $x \in [0, a]$ con potencial $V(x)=0$ dentro y $V(x)=\infty$ fuera , considera la solución $\Psi_{n}(x,t)=N \sin(\frac{n\pi}{a}x) e^{-i\phi_{n}(t)}$.

- **(a)** Halla la fase real $\phi_{n}(t)$ para que la función satisfaga la ecuación de Schrödinger y encuentra la constante de normalización $N$.
    
- **(b)** Calcula $\langle x \rangle$, $\langle x^{2} \rangle$ y $\Delta x$ para $t=0$.
    
- **(c)** Calcula $\langle p \rangle$, $\langle p^{2} \rangle$ y $\Delta p$ para $t=0$.
    
- **(d)** ¿Se satisface la desigualdad de incertidumbre? ¿Se satura?
    
- **(e)** ¿Qué resultados de los apartados (b) y (c) cambian para $t > 0$? Explica.
    

---

## **4. Una pared rígida**

Para un potencial $V(x) = 0$ si $x > 0$ y $V(x) = \infty$ si $x \le 0$ , encuentra los estados estacionarios y sus energías.

---

## **5. Un escalón en la línea infinita**

Para el potencial $V(x) = V_0$ si $x > 0$ y $V(x) = 0$ si $x \le 0$ , encuentra los estados estacionarios que existen para energías $0 < E < V_0$.

---

## **6. Una pared y la mitad de un pozo finito**

Dado el potencial $V(x) = \infty$ ($x < 0$), $V(x) = -V_0$ ($0 < x < a$) y $V(x) = 0$ ($x > a$):

- Encuentra los estados estacionarios correspondientes a estados ligados ($E < 0$).
    
- ¿Existe siempre un estado ligado?
    
- Halla el valor mínimo de $z_{0}^{2} = \frac{2ma^{2}V_{0}}{\hbar^{2}}$ para el cual existen tres estados ligados.
    

---

## **7. Imitando al hidrógeno con un pozo cuadrado unidimensional**

Diseña un pozo cuadrado finito unidimensional $V(x) = -V_0$ para $|x| < a_0$ y $V(x) = 0$ para $|x| > [cite_start]a_0$ que simule el átomo de hidrógeno. Calcula el valor de $V_0$ en eV para que el estado fundamental del pozo tenga la profundidad correcta ($E_0 = -13.6$ eV).

---

## **8. No hay estados con $E < V(x)$**

Considera un estado estacionario real con energía $E$:

- **(a)** Demuestra que $E$ debe exceder el valor mínimo de $V(x)$ notando que $E = \langle H \rangle$.
    
- **(b)** Explica esta afirmación intentando dibujar una función de onda consistente con estar en la región clásicamente inaccesible para todos los valores de $x$.
    

¿Te gustaría que te ayude a resolver alguno de estos problemas paso a paso?