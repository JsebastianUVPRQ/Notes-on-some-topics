**Conjunto de problemas 1**

**1.**  
(a) **[5 puntos]** Demuestre que la suma de dos vectores espaciales ortogonales cualesquiera es un vector espacial.  
(b) **[5 puntos]** Demuestre que un vector temporal y un vector nulo no pueden ser ortogonales.

**2.** En cierto sistema de referencia, los campos vectoriales $\vec{U}$ y $\vec{D}$ tienen las componentes  

$$U^{\alpha}\doteq(1+t^{2},t^{2},\sqrt{2}t,0)$$  
$$D^{\alpha}\doteq(x,5tx,\sqrt{2}t,0)\ .$$

El escalar $\rho$ tiene el valor  

$$\rho=x^{2}+t^{2}-y^{2}\,.$$

(La relación "LHS $\doteq$ RHS" significa "el objeto del lado izquierdo está representado por el objeto del lado derecho en el sistema de referencia especificado").

(a) **[3 puntos]** Demuestre que $\vec{U}$ es adecuado como una 4-velocidad. ¿Lo es $\vec{D}$?  
(b) **[3 puntos]** Encuentre la velocidad espacial ${\bf v}$ de una partícula cuya 4-velocidad es $\vec{U}$, para un $t$ arbitrario. Describa el movimiento en los límites $t=0$ y $t\to\infty$.  
(c) **[3 puntos]** Calcule $\partial_{\beta}U^{\alpha}$ para todo $\alpha$, $\beta$. Muestre que $U_{\alpha}\partial_{\beta}U^{\alpha}=0$. (Hay una forma elegante de hacerlo; hágalo en cambio por la fuerza bruta).  
(d) **[3 puntos]** Calcule $\partial_{\alpha}D^{\alpha}$.  
(e) **[3 puntos]** Calcule $\partial_{\beta}(U^{\alpha}D^{\beta})$ para todo $\alpha$.  
(f) **[3 puntos]** Calcule $U_{\alpha}\partial_{\beta}(U^{\alpha}D^{\beta})$. ¿Por qué la respuesta es tan similar a la de (d)?  
(g) **[3 puntos]** Calcule $\partial_{\alpha}\rho$ para todo $\alpha$. Calcule $\partial^{\alpha}\rho$.  
(h) **[3 puntos]** Calcule $\nabla_{\vec{U}}\rho$ y $\nabla_{\vec{D}}\rho$.

**3.** Considere un 4-vector temporal unitario $\vec{U}$ y el tensor  

$$P_{\alpha\beta}=\eta_{\alpha\beta}+U_{\alpha}U_{\beta}\ .$$

Demuestre que este tensor es un operador de proyección que proyecta un vector arbitrario $\vec{V}$ en uno ortogonal a $\vec{U}$. En otras palabras, demuestre que el vector $\vec{V}_{\perp}$ cuyas componentes son  

$$V^{\alpha}_{\perp}=P^{\alpha}{}_{\beta}V^{\beta}$$

cumple que:  

(a) **[5 puntos]** es ortogonal a $\vec{U}$.  
(b) **[5 puntos]** no se ve afectado por proyecciones adicionales:  

$$V^{\alpha}_{\perp\perp}\equiv P^{\alpha}{}_{\beta}V^{\beta}_{\perp}=V^{\alpha}_{\perp}\ .$$

(c) **[5 puntos]** $P_{\alpha\beta}$ es la métrica para el espacio de vectores ortogonales a $\vec{U}$:  

$$P_{\alpha\beta}V^{\alpha}_{\perp}W^{\beta}_{\perp}=\vec{V}_{\perp}\cdot\vec{W}_{\perp}\ .$$

(d) **[5 puntos]** Demuestre que para un vector no nulo arbitrario $\vec{q}$, el tensor de proyección está dado por  

$$P_{\alpha\beta}(q^{\alpha})=\eta_{\alpha\beta}-\frac{q_{\alpha}q_{\beta}}{q^{\gamma}q_{\gamma}}\ .$$

¿Necesitamos un tensor de proyección para vectores nulos?

**4.** **[15 puntos]** Sea $\Lambda_{B}(\mathbf{v})$ un impulso de Lorentz asociado con la 3-velocidad $\mathbf{v}$. Considere  

$$\Lambda\equiv\Lambda_{B}(\mathbf{v}_{1})\cdot\Lambda_{B}(\mathbf{v}_{2})\cdot\Lambda_{B}(-\mathbf{v}_{1})\cdot\Lambda_{B}(-\mathbf{v}_{2})$$

donde $\mathbf{v}_{1}\cdot\mathbf{v}_{2}=0$. Suponga $v_{1}\ll 1$, $v_{2}\ll 1$. Demuestre que $\Lambda$ es una rotación. ¿Cuál es el eje de rotación? ¿Cuál es el ángulo de rotación?

**5. Movimiento “superlumínico”**  
El cuásar 3C 273 emite burbujas de plasma relativista desde cerca del agujero negro masivo en su centro. Las burbujas viajan a velocidad $v$ a lo largo de un chorro que forma un ángulo $\theta$ con respecto a la línea de visión del observador. Proyectadas en el cielo, las burbujas parecen viajar perpendicularmente a la línea de visión con una velocidad angular $v_{\text{app}}/r$, donde $r$ es la distancia a 3C 273 y $v_{\text{app}}$ es la velocidad aparente.

(a) **[7 puntos]** Demuestre que  

$$v_{\text{app}}=\frac{v\sin\theta}{1-v\cos\theta}\;.$$

(b) **[5 puntos]** Para un valor dado de $v$, ¿qué valor de $\theta$ maximiza $v_{\text{app}}$? ¿Cuál es el valor máximo correspondiente de $v_{\text{app}}$? ¿Puede ser mayor que la velocidad de la luz? Si es así, ¿se viola la relatividad especial?  
(c) **[3 puntos]** Para 3C 273, $v_{\text{app}}\simeq 10c$. ¿Cuál es el mayor valor posible de $\theta$$en grados)?

**6. Corte GZK en el espectro de rayos cósmicos**  
(a) **[8 puntos]** Calcule la energía umbral de un nucleón $N$ para que sufra la reacción $gamma+N\to N+\pi^{0}$, donde $\gamma$ representa un fotón del fondo cósmico de microondas de energía $kT$ con $T=2.73$ K. Suponga que la colisión es frontal y tome las masas del nucleón y del pión como 938 MeV y 135 MeV, respectivamente.  
(b) **[5 puntos]** Explique por qué cabría esperar observar muy pocos rayos cósmicos con energía por encima de $\sim 10^{11}$ GeV.  
(c) **[3 puntos]** Esta expectativa se llama el corte de Griesen-Zatsepin-Kuzmin (GZK). Observaciones modernas no muestran un corte abrupto; incluso puede haber evidencia de un *aumento* en el flujo de rayos cósmicos a estas energías. ¿Puede sugerir un mecanismo mediante el cual se pueda evitar el corte GZK?
