
---

**Primer Parcial Mecánica cuántica I, Septiembre 2020, K. Rodríguez**

1. Considere la matriz  
$$
M=\begin{pmatrix}1&1\\0&1\end{pmatrix},
$$
la cual claramente no es hermítica.

   (a) Muestre que la matriz $M$ tiene únicamente autovalores reales, pero sus autovectores no forman un conjunto completo.

   (b) Siendo una matriz no hermítica, $M$ viola las condiciones del Teorema 1. Encuentre un ket $|v\rangle$ tal que el valor esperado del operador representado por dicha matriz, $\langle v|M|v\rangle$, es complejo.

   (c) Debido a que $\langle \hat M\rangle=\langle v|\hat M|v\rangle$ puede ser complejo, ¿qué interpretación física no es posible usar para dicho cálculo?

   **Nota:** Este ejemplo ilustra la necesidad de representar observables físicos por operadores herméticos, y no solamente por operadores cuyo espectro sea real.

2. (a) ¿Qué características debe tener un ket para que represente el estado físico de un sistema? ¿Por qué razón debe tener estas características?

   (b) ¿Cómo predice teóricamente los posibles valores que obtendría en la medición de un observable y sus correspondientes probabilidades, cuando el sistema se encuentra en un estado determinado por la superposición de estados propios de dicho observable?

   (c) ¿Qué representa el valor esperado de un observable de un sistema cuando se encuentra en un estado dado? Justifique su respuesta.

   (d) ¿Qué significa que los operadores $\{\hat A,\hat B,\hat C\}$ forman un conjunto completo de observables compatibles?

3. En la base ortonormal completa $\{|1\rangle,|2\rangle,|3\rangle\}$ del espacio de kets de un sistema, dos observables compatibles tienen la siguiente representación:
$$
\hat A=\begin{pmatrix}
2\hbar^2&0&0\\
0&2\hbar^2&0\\
0&0&2\hbar^2
\end{pmatrix},
\qquad
\hat B=\begin{pmatrix}
0&-\frac{i\hbar}{\sqrt2}&0\\
\frac{i\hbar}{\sqrt2}&0&-\frac{i\hbar}{\sqrt2}\\
0&\frac{i\hbar}{\sqrt2}&0
\end{pmatrix}.
$$

   (a) Determine el conjunto de vectores (y kets) propios simultáneos normalizados de los dos observables, especificando a qué parejas de valores propios corresponden; exprese los kets propios simultáneos como superposición de los kets de la base original.

   (b) ¿Cuál de los siguientes conjuntos es un CCOC: $\{\hat A\}$, $\{\hat B\}$, $\{\hat A,\hat B\}$ o ninguno? En caso de haber algún CCOC, ¿cuál es el mínimo? Justifique claramente sus respuestas.

   (c) El estado más general que se puede construir como superposición de los kets propios simultáneos de los dos observables, ¿es un ket propio del observable $\hat A$? ¿Esperaba esta respuesta? ¿Por qué?

   (d) Haga un diagrama de valor propio vs probabilidad de ser medido, esto es, determine la distribución de valores propios (el espectro) para cada uno de los observables $\hat A$ y $\hat B$.

   (e) Suponga que el sistema se encuentra en el estado  
   $$
   |\gamma\rangle=\frac{1}{\sqrt{17}}\bigl(2|b_1\rangle+3|b_2\rangle+2|b_3\rangle\bigr).
   $$
   Calcule los valores esperados de $\hat A$ y $\hat B$ cuando el sistema se encuentra en el estado $|\gamma\rangle$.

4. Sea $\{|a_i,b_i,c_i\rangle\}$ la base de kets propios simultáneos ortonormales del conjunto completo de observables compatibles $\{\hat A,\hat B,\hat C\}$ de un sistema de tres grados de libertad. Si el sistema se encuentra en el estado definido por:
$$
|\eta\rangle=\frac13\left[2|a,-b,c\rangle+|-a,b,c\rangle-2|-a,-b,c\rangle\right].
$$

   (a) Normalice el ket de estado.

   (b) Determine los conjuntos de valores que puede obtener de una medición simultánea de los tres observables y sus correspondientes probabilidades.

   (c) Si se realiza la medición del observable $\hat B$, ¿cuáles son los posibles valores que medirá para este observable? ¿Con qué probabilidad?

   (d) ¿Es $\eta$ ket propio de alguno de los observables del CCOC? Justifique su respuesta.

   (e) Calcule el valor esperado de los observables $\hat A$ y $\hat C$. ¿Esperaba estas respuestas? Justifique.

5. (a) La ecuación de valores propios para el operador $\hat S_z$ de un sistema de espín $1/2$ se puede expresar  
   $$
   \hat S_z|\pm\rangle=\pm\frac{\hbar}{2}|\pm\rangle.
   $$
   El estado del sistema expresado en la base ortonormal $\{|+\rangle,|-\rangle\}$ está dado por  
   $$
   |\eta\rangle=\frac{1}{\sqrt2}\bigl(|+\rangle+i|-\rangle\bigr).
   $$
   i) ¿Cuál es la probabilidad de que el sistema quede en el estado $|+\rangle$ al realizar la medición de $\hat S_z$?  
   ii) ¿Cuáles son los posibles valores que se pueden obtener al medir $\hat S_z$?  
   iii) Calcule el valor esperado de $\hat S_z$. ¿Esperaba esta respuesta? ¿Por qué?

   (b) Sea el operador $\hat H$ que describe un sistema físico cuyos kets propios están denotados por $|\Psi_n\rangle$ y autovalores por $E_n$, tal que  
   $$
   \hat H|\Psi_n\rangle=E_n|\Psi_n\rangle.
   $$
   Pruebe para un operador arbitrario $\hat A$ la relación:
   $$
   \langle\Psi_n|[\hat A,\hat H]|\Psi_n\rangle.
   $$

---

