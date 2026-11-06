
Explica los prerrequisitos, los conceptos usados (en general), la razón de ser, etc; de los ejercicios. Luego resuelve paso a paso

---
1. **(1 punto)**

   (a) i) Considere dos kets $|\alpha\rangle$ y $|\beta\rangle$. Suponga que todas las amplitudes de probabilidad de que tanto $|\alpha\rangle$ como $|\beta\rangle$ se encuentren en cada uno de los elementos de una base completa $\{|a_i\rangle\}$ son conocidas. Encuentre la representación matricial del operador $|\alpha\rangle\langle\beta|$ en dicha base.  
   ii) Ahora considere un sistema de espín $1/2$ y tome $|\alpha\rangle$ y $|\beta\rangle$ como $|s_x=\hbar/2\rangle$ y $|s_x=\hbar/2\rangle$, respectivamente. Escriba explícitamente la matriz cuadrada que corresponde a $|\alpha\rangle\langle\beta|$ en la base usual que diagonaliza a $\hat S_z$.  
   *(Nota: el OCR repite $|s_x=\hbar/2\rangle$; posible errata en el original.)*

   (b) Sea $\{|+\rangle,|-\rangle\}$ la base propia de $\hat S_z$. Usando la ortonormalidad entre $|+\rangle$ y $|-\rangle$, pruebe que  
   $$
   [\hat S_i,\hat S_j]=i\epsilon_{ijk}\hbar\hat S_k,\qquad
   \{\hat S_i,\hat S_j\}=\left(\frac{\hbar^2}{2}\right)\delta_{ij},
   $$
   donde  
   $$
   \hat S_x=\frac{\hbar}{2}\bigl(|+\rangle\langle-|+|-\rangle\langle+|\bigr),
   $$
   $$
   \hat S_y=\frac{i\hbar}{2}\bigl(-|+\rangle\langle-|+|-\rangle\langle+|\bigr),
   $$
   $$
   \hat S_z=\frac{\hbar}{2}\bigl(|+\rangle\langle+|-|-\rangle\langle-|\bigr).
   $$

   (c) Suponga que $|i\rangle$ y $|j\rangle$ son autokets del operador hermítico $\hat A$. ¿Bajo qué condiciones puede concluir que $|i\rangle+|j\rangle$ también es un autoket de $\hat A$? Justifique su respuesta.

2. **(1 punto)**

   (a) ¿Cómo predice teóricamente los posibles valores que obtendría en la medición de un observable y sus correspondientes probabilidades, cuando el sistema se encuentra en un estado determinado por la superposición de estados propios de dicho observable?

   (b) ¿Qué características debe tener un operador para que represente un observable físico? ¿Por qué razón debe tener estas características?

   (c) ¿Qué características debe tener un ket para que represente el estado físico de un sistema? ¿Por qué razón debe tener estas características?

   (d) Sean los observables $\hat A$ y $\hat B$. Suponga que los autokets $\{|a'b'\rangle\}$, simultáneos de $\hat A$ y $\hat B$, forman un conjunto de kets base ortonormal completo. ¿Podemos concluir siempre que $[\hat A,\hat B]=0$? Si su respuesta es sí, pruebe su afirmación. Si su respuesta es no, dé un contraejemplo.

3. **(1 punto)**

   (a) Construya $|S\cdot n;+\rangle$ tal que  
   $$
   \hat S\cdot \hat n\,|\hat S\cdot \hat n;+\rangle
   =\left(\frac{\hbar}{2}\right)|\hat S\cdot \hat n;+\rangle,
   $$
   donde $\hat n$ está caracterizado por los ángulos mostrados en la figura 1. Exprese su respuesta como una combinación lineal de $|+\rangle$ y $|-\rangle$.  
   Note que la respuesta es  
   $$
   \cos\left(\frac{\beta}{2}\right)|+\rangle+
   \sin\left(\frac{\beta}{2}\right)e^{i\alpha}|-\rangle,
   $$
   pero no se limite a verificar que la respuesta satisface la ecuación de valores propios mostrada. Lo que debe hacer es tratar el ejercicio directamente como un problema de valores y kets propios. Tampoco utilice rotación de operadores, ya que esto lo veremos más adelante.

   **Fig. 1:** Ángulos polar y azimutal.

4. **(1 punto)**

   (a) Un sistema de dos estados es caracterizado por el hamiltoniano (el cual no es más que un operador hermítico con unidades de energía):
   $$
   \hat H=H_{11}|1\rangle\langle1|+H_{22}|2\rangle\langle2|
   +H_{12}\bigl(|1\rangle\langle2|+|2\rangle\langle1|\bigr),
   $$
   donde $H_{11}$, $H_{22}$ y $H_{12}$ son números reales con dimensiones de energía, y $|1\rangle$ y $|2\rangle$ son autoestados de algún observable diferente de $\hat H$. Encuentre los autoestados de energía y sus correspondientes autovalores, esto es, los autoestados y autovalores del operador $\hat H$. Asegúrese que su respuesta tiene sentido para $H_{12}=0$. Usted no necesita solucionar el problema desde ceros; puede usar la siguiente relación sin probarla:
   $$
   (\hat S\cdot \hat n)|\hat n;+\rangle
   =\left(\frac{\hbar}{2}\right)|\hat n;+\rangle,
   $$
   con  
   $$
   |\hat n;+\rangle=
   \cos\left(\frac{\beta}{2}\right)|+\rangle+
   \sin\left(\frac{\beta}{2}\right)e^{i\alpha}|-\rangle,
   $$
   donde $\beta$ y $\alpha$ son los ángulos polar y azimutal, respectivamente, que caracterizan $\hat n$ como lo muestra la figura 1.

   (b) Suponga que alguien cometió un error de typo y escribió $\hat H$ como  
   $$
   \hat H=H_{11}|1\rangle\langle1|+H_{22}|2\rangle\langle2|+H_{12}|1\rangle\langle2|.
   $$
   ¿Por qué este operador es ilegal para describir la energía? ¿Qué principio se viola?

5. **(1 punto)** Un haz de átomos con espín $1/2$ pasa a través de una serie de mediciones tipo Stern-Gerlach como sigue:

   (a) La primera medida acepta átomos $s_z=\hbar/2$ y rechaza átomos $s_z=-\hbar/2$.

   (b) La segunda medida acepta átomos $s_n=\hbar/2$ y rechaza átomos $s_n=-\hbar/2$, donde $s_n$ es el autovalor del operador $(\hat S\cdot \hat n)$, con $\hat n$ donde el ángulo $\beta$ se encuentra en el plano $xz$ con respecto al eje $z$.

   (c) La tercera medida acepta átomos $s_z=-\hbar/2$ y rechaza átomos $s_z=\hbar/2$.

   i) ¿Cuál es la intensidad del haz final $s_z=\hbar/2$ cuando el haz $s_z=\hbar/2$ que sobrevive la primera medida es normalizado a la unidad?  
   ii) ¿Cómo debemos orientar el aparato de la segunda medida si queremos maximizar la intensidad del haz final $s_z=-\hbar/2$?