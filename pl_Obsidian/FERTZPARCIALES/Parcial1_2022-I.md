## ENUNCIADOS


1. **(2 puntos.)** En la base ortonormal $\{|1\rangle,|2\rangle,|3\rangle\}$ del espacio de kets de un sistema, los observables compatibles $\hat A$ y $\hat B$ tienen la siguiente representación matricial:  

$$
\hat A=2\hbar^2 I_3=
\begin{pmatrix}
2\hbar^2&0&0\\
0&2\hbar^2&0\\
0&0&2\hbar^2
\end{pmatrix},
$$

$$
\hat B=
\begin{pmatrix}
0&-\dfrac{i\hbar}{\sqrt2}&0\\
\dfrac{i\hbar}{\sqrt2}&0&-\dfrac{i\hbar}{\sqrt2}\\
0&\dfrac{i\hbar}{\sqrt2}&0\\
\end{pmatrix},
$$

$$
U=
\begin{pmatrix}
\dfrac{i}{2}&\dfrac1{\sqrt2}&-\dfrac{i}{2}\\
\dfrac1{\sqrt2}&0&\dfrac1{\sqrt2}\\
-\dfrac{i}{2}&\dfrac1{\sqrt2}&\dfrac{i}{2}
\end{pmatrix}.
$$
   la matriz que representa una transformación unitaria de cambio de base.”

   (a) i) Demuestre que $\hat U$ transforma la base $\{|1\rangle,|2\rangle,|3\rangle\}$ en la base $\{|b_1\rangle,|b_2\rangle,|b_3\rangle\}$ de kets propios simultáneos de $\hat A$ y $\hat B$.  
   ii) Con base en esta información exprese los kets propios simultáneos como superposición de los kets de la base original y defina a qué parejas de valores propios corresponden. Justifique sus respuestas.

   (b) Determine la distribución de valores propios (el espectro) para cada uno de los observables $\hat A$ y $\hat B$ y haga un esquema correspondiente.

   (c) Suponga que el sistema se encuentra en el estado  
   $$
   |\gamma\rangle=\frac{1}{\sqrt{11}}\bigl(-i|b_1\rangle+3|b_2\rangle+i|b_3\rangle\bigr).
   $$
   Calcule los valores esperados de $\hat A$ y $\hat B$ cuando el sistema se encuentra en el estado $|\gamma\rangle$ y haga un histograma correspondiente a cada uno. ¿Esperaba estas respuestas? ¿Por qué?

   (d) ¿Cuál de los siguientes conjuntos es un CCOC: $\{\hat A\}$, $\{\hat B\}$ y $\{\hat A,\hat B\}$? ¿Cuál de los CCOC es mínimo? Justifique claramente sus respuestas.

2. **(2 puntos.)**

   (a) ¿Qué características debe tener un ket para que represente el estado físico de un sistema? ¿Por qué razón debe tener estas características?

   (b) ¿Cómo predice teóricamente los posibles valores que obtendría en la medición de un observable y sus correspondientes probabilidades, cuando el sistema se encuentra en un estado determinado por la superposición de estados propios de dicho observable?

   (c) ¿Qué representa el valor esperado de un observable de un sistema cuando se encuentra en un estado dado? Justifique su respuesta.

   (d) ¿Qué se entiende por medición en mecánica cuántica?

   (e) ¿Qué significa que los operadores $\{\hat A,\hat B,\hat C\}$ forman un conjunto completo de observables compatibles?

3. **(1 punto.)** Considere el observable $\hat O$, el cual tiene sólo dos autovalores, $+1$ o $-1$, cuyos kets propios son $|+\rangle$ y $|-\rangle$ respectivamente. Considere la familia de estados  
   $$
   |\theta\rangle=\sqrt{\frac12}\bigl(|+\rangle+e^{i\theta}|-\rangle\bigr),
   $$
   donde $\theta$ es un parámetro real arbitrario. Muestre que $\langle\hat O\rangle=0$ para toda la familia de estados. ¿Cuál es la diferencia, si es que hay alguna, entre los estados miembros de dicha familia? ¿Se le ocurre alguna manera en la que podrían ser ellos medidos?

4. **(1 punto. Opcional)**

   (a) (0.2 pts) Demuestre que la traza de un producto de operadores en una representación continua satisface  
   $$
   \operatorname{Tr}[\hat A\hat B]=\operatorname{Tr}[\hat B\hat A].
   $$

   (b) (0.4 pts) Considere un sistema en un estado cuántico $|\psi\rangle$, y usando los operadores $\hat A$ y $\hat\rho=|\psi\rangle\langle\psi|$, calcule  
   $$
   \operatorname{Tr}[\hat\rho\hat A].
   $$
   ¿Qué interpretación física le puede dar a su cálculo? ¿Qué puede concluir adicionalmente de su cálculo?

   (c) (0.4 pts) Si ahora el operador $\hat\rho$ asociado al sistema está determinado por  
   $$
   \hat\rho=\sum_i p_i|i\rangle\langle i|,
   $$
   calcule nuevamente $\operatorname{Tr}[\hat\rho\hat A]$. ¿Qué interpretación física le da a su cálculo? ¿La interpretación cambió o es igual a la del ítem anterior b)?

---

## SOLUCION


$$
\hat A=2\hbar^2 I_3=
\begin{pmatrix}
2\hbar^2&0&0\\
0&2\hbar^2&0\\
0&0&2\hbar^2
\end{pmatrix},
$$

$$
\hat B=
\begin{pmatrix}
0&-\dfrac{i\hbar}{\sqrt2}&0\\
\dfrac{i\hbar}{\sqrt2}&0&-\dfrac{i\hbar}{\sqrt2}\\
0&\dfrac{i\hbar}{\sqrt2}&0\\
\end{pmatrix},
$$

$$
U=
\begin{pmatrix}
\dfrac{i}{2}&\dfrac1{\sqrt2}&-\dfrac{i}{2}\\
\dfrac1{\sqrt2}&0&\dfrac1{\sqrt2}\\
-\dfrac{i}{2}&\dfrac1{\sqrt2}&\dfrac{i}{2}
\end{pmatrix}.
$$
### (a) i) \(U\) trAnsforma la base original en la base de kets propios simultáneos

Primero, \(U\) es unitaria:
$$
U^\dagger U=I.
$$
Sus columnas son ortonormales.

Además, definiendo
$$
|b_j\rangle=U|j\rangle,
$$
se obtiene
$$
|b_1\rangle=U|1\rangle
=\frac{i}{2}|1\rangle+\frac1{\sqrt2}|2\rangle-\frac{i}{2}|3\rangle,
$$
$$
|b_2\rangle=U|2\rangle
=\frac1{\sqrt2}|1\rangle+\frac1{\sqrt2}|3\rangle,
$$
$$
|b_3\rangle=U|3\rangle
=-\frac{i}{2}|1\rangle+\frac1{\sqrt2}|2\rangle+\frac{i}{2}|3\rangle.
$$

Estos son autovectores de \(\hat B\):
$$
\hat B|b_1\rangle=-\hbar|b_1\rangle,
\qquad
\hat B|b_2\rangle=0,
\qquad
\hat B|b_3\rangle=+\hbar|b_3\rangle.
$$
Y como \(\hat A=2\hbar^2 I\), todos son también autoestados de \(\hat A\):
$$
\hat A|b_j\rangle=2\hbar^2|b_j\rangle,\qquad j=1,2,3.
$$
Por tanto, \(\{|b_1\rangle,|b_2\rangle,|b_3\rangle\}\) es una base ortonormal de kets propios simultáneos de \(\hat A\) y \(\hat B\).

Equivalentemente,
$$
U^\dagger \hat A U=2\hbar^2 I_3,
$$
$$
U^\dagger \hat B U=
\hbar
\begin{pmatrix}
-1&0&0\\
0&0&0\\
0&0&1
\end{pmatrix}.
$$

### (a) ii) Parejas de valores propios

Las parejas \((a,b)\) son:
$$
|b_1\rangle\equiv |a=2\hbar^2,\; b=-\hbar\rangle,
$$
$$
|b_2\rangle\equiv |a=2\hbar^2,\; b=0\rangle,
$$
$$
|b_3\rangle\equiv |a=2\hbar^2,\; b=+\hbar\rangle.
$$

### (b) Espectro de \(\hat A\) y \(\hat B\)

Para \(\hat A\):
$$
\text{Espectro}(\hat A)=\{2\hbar^2\},
$$
con degeneración \(3\).

Para \(\hat B\):
$$
\text{Espectro}(\hat B)=\{-\hbar,\,0,\,+\hbar\},
$$
cada uno no degenerado.

Esquema:
$$
\begin{array}{c|c}
\hat A & 2\hbar^2\quad(\text{degenerado 3 veces})\\
\hline
\hat B & -\hbar,\quad 0,\quad +\hbar
\end{array}
$$

### (c) Estado
$$
|\gamma\rangle=\frac1{\sqrt{11}}\left(-i|b_1\rangle+3|b_2\rangle+i|b_3\rangle\right).
$$

Como \(|b_j\rangle\) son autoestados de \(\hat A\) con el mismo autovalor:
$$
\langle \hat A\rangle_\gamma=2\hbar^2.
$$

Para \(\hat B\):
$$
\langle \hat B\rangle_\gamma
=
\frac{1}{11}\left[|-i|^2(-\hbar)+|3|^2(0)+|i|^2(+\hbar)\right],
$$
es decir,
$$
\langle \hat B\rangle_\gamma
=
\frac{1}{11}(-\hbar+0+\hbar)=0.
$$

Las probabilidades de medición de \(\hat B\) son:
$$
P(-\hbar)=\frac{1}{11},\qquad
P(0)=\frac{9}{11},\qquad
P(+\hbar)=\frac{1}{11}.
$$
Para \(\hat A\), como sólo hay un autovalor posible,
$$
P(2\hbar^2)=1.
$$

Histogramas:

- Para \(\hat A\): una sola barra en \(2\hbar^2\), altura \(1\).
- Para \(\hat B\): barras en \(-\hbar\), \(0\), \(+\hbar\) con alturas
$$
\frac1{11},\quad \frac9{11},\quad \frac1{11},
$$
respectivamente.

Era de esperar que \(\langle \hat A\rangle=2\hbar^2\), pues \(\hat A\) es proporcional a la identidad. También era de esperar que \(\langle \hat B\rangle=0\), porque las contribuciones de \(-\hbar\) y \(+\hbar\) tienen el mismo peso probabilístico y se cancelan; el autovalor \(0\) no contribuye.

### (d) ¿Cuál conjunto es un CCOC?

- \(\{\hat A\}\) **no** es CCOC, porque \(\hat A\) es degenerado: sus tres estados propios tienen el mismo autovalor y no quedan etiquetados completamente.
- \(\{\hat B\}\) **sí** es CCOC, porque \(\hat B\) tiene tres autovalores distintos y sus autovectores forman una base completa y única.
- \(\{\hat A,\hat B\}\) también es CCOC, pues son compatibles y sus autovectores simultáneos forman base completa; sin embargo, \(\hat A\) es redundante.

Por tanto, el CCOC mínimo entre los dados es
$$
\boxed{\{\hat B\}}.
$$