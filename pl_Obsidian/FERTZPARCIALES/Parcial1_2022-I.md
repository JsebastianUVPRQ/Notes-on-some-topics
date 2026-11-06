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
### (a) i) $U$ trAnsforma la base original en la base de kets propios simultáneos

Primero, $U$ es unitaria:
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

Estos son autovectores de $\hat B$:
$$
\hat B|b_1\rangle=-\hbar|b_1\rangle,
\qquad
\hat B|b_2\rangle=0,
\qquad
\hat B|b_3\rangle=+\hbar|b_3\rangle.
$$
Y como $\hat A=2\hbar^2 I$, todos son también autoestados de $\hat A$:
$$
\hat A|b_j\rangle=2\hbar^2|b_j\rangle,\qquad j=1,2,3.
$$
Por tanto, $\{|b_1\rangle,|b_2\rangle,|b_3\rangle\}$ es una base ortonormal de kets propios simultáneos de $\hat A$ y $\hat B$.

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

Las parejas $(a,b)$ son:
$$
|b_1\rangle\equiv |a=2\hbar^2,\; b=-\hbar\rangle,
$$
$$
|b_2\rangle\equiv |a=2\hbar^2,\; b=0\rangle,
$$
$$
|b_3\rangle\equiv |a=2\hbar^2,\; b=+\hbar\rangle.
$$

### (b) Espectro de $\hat A$ y $\hat B$

Para $\hat A$:
$$
\text{Espectro}(\hat A)=\{2\hbar^2\},
$$
con degeneración $3$.

Para $\hat B$:
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

Como $|b_j\rangle$ son autoestados de $\hat A$ con el mismo autovalor:
$$
\langle \hat A\rangle_\gamma=2\hbar^2.
$$

Para $\hat B$:
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

Las probabilidades de medición de $\hat B$ son:
$$
P(-\hbar)=\frac{1}{11},\qquad
P(0)=\frac{9}{11},\qquad
P(+\hbar)=\frac{1}{11}.
$$
Para $\hat A$, como sólo hay un autovalor posible,
$$
P(2\hbar^2)=1.
$$

Histogramas:

- Para $\hat A$: una sola barra en $2\hbar^2$, altura $1$.
- Para $\hat B$: barras en $-\hbar$, $0$, $+\hbar$ con alturas
$$
\frac1{11},\quad \frac9{11},\quad \frac1{11},
$$
respectivamente.

Era de esperar que $\langle \hat A\rangle=2\hbar^2$, pues $\hat A$ es proporcional a la identidad. También era de esperar que $\langle \hat B\rangle=0$, porque las contribuciones de $-\hbar$ y $+\hbar$ tienen el mismo peso probabilístico y se cancelan; el autovalor $0$ no contribuye.

### (d) ¿Cuál conjunto es un CCOC?

- $\{\hat A\}$ **no** es CCOC, porque $\hat A$ es degenerado: sus tres estados propios tienen el mismo autovalor y no quedan etiquetados completamente.
- $\{\hat B\}$ **sí** es CCOC, porque $\hat B$ tiene tres autovalores distintos y sus autovectores forman una base completa y única.
- $\{\hat A,\hat B\}$ también es CCOC, pues son compatibles y sus autovectores simultáneos forman base completa; sin embargo, $\hat A$ es redundante.

Por tanto, el CCOC mínimo entre los dados es
$$
\boxed{\{\hat B\}}.
$$

# Prerrequisitos y conceptos fundamentales

Antes de resolver los ejercicios, conviene tener claros cinco conceptos: el espacio de estados, los observables, la regla de Born, el valor esperado y la matriz de densidad.

## 1. El estado cuántico y los kets

En mecánica cuántica, el estado de un sistema se representa mediante un ket $|\psi\rangle$, que pertenece a un espacio de Hilbert.

Un espacio de Hilbert es, esencialmente, un espacio vectorial complejo que cuenta con un producto interno y ciertas propiedades matemáticas que permiten describir estados y calcular probabilidades.

Para que un ket represente un estado físico puro debe estar normalizado:

$$\langle\psi|\psi\rangle=1.$$

En una representación continua, como la de posición, esto equivale a:

$$\int_{-\infty}^{\infty}|\psi(x)|^2\,dx=1.$$

La razón es que las probabilidades de todos los resultados posibles deben sumar uno.

Una sutileza importante: dos kets que difieren únicamente por una fase global representan el mismo estado físico:

$$|\psi'\rangle=e^{i\alpha}|\psi\rangle.$$

Esto se debe a que esa fase desaparece al calcular las probabilidades. Por tanto, un estado físico puro corresponde realmente a una clase de kets equivalentes, no a un ket único.

## 2. Los observables y sus estados propios

Un observable es una magnitud física que puede medirse: energía, posición, momento, espín, etc.

En mecánica cuántica se representa mediante un operador hermítico $\hat A$. Sus estados y valores propios satisfacen:

$$\hat A|a_n\rangle=a_n|a_n\rangle.$$

Aquí:

- $a_n$ es un valor propio del operador.
    
- $|a_n\rangle$ es el estado propio asociado.
    
- Los posibles resultados de una medición ideal de $\hat A$ son sus valores propios.
    

Por ejemplo, si:

$$\hat A|a_1\rangle=a_1|a_1\rangle, \qquad \hat A|a_2\rangle=a_2|a_2\rangle,$$

una medición de $\hat A$ solamente puede producir $a_1$ o $a_2$.

## 3. Superposición y regla de Born

Un estado puede ser una combinación lineal de estados propios de un observable:

$$|\psi\rangle=\sum_n c_n|a_n\rangle.$$

Si los estados propios están normalizados y son ortogonales, los coeficientes satisfacen:

$$\sum_n |c_n|^2=1.$$

La regla de Born establece que la probabilidad de obtener el resultado $a_n$ al medir $\hat A$ es:

$$\boxed{P(a_n)=|c_n|^2.}$$

Por tanto, los coeficientes de la superposición contienen la información probabilística necesaria para predecir los resultados de una medición.

Si existe degeneración, se suman las probabilidades correspondientes a todos los estados propios asociados al mismo valor propio.

## 4. El valor esperado

El valor esperado de un observable $\hat A$ en un estado normalizado $|\psi\rangle$ se define como:

$$\boxed{\langle\hat A\rangle =\langle\psi|\hat A|\psi\rangle.}$$

También puede calcularse como el promedio ponderado de los resultados posibles:

$$\langle\hat A\rangle=\sum_n a_nP(a_n).$$

Representa el promedio estadístico que se obtendría al medir el observable sobre muchas copias del sistema preparadas en el mismo estado.

No significa necesariamente que ese valor pueda obtenerse en una medición individual.

## 5. La matriz de densidad

Un estado puro puede describirse mediante el operador densidad:

$$\hat\rho=|\psi\rangle\langle\psi|.$$

Pero también podemos tener una situación en la que el sistema se encuentre en uno de varios estados posibles, con probabilidades $p_i$. En ese caso:

$$\boxed{\hat\rho=\sum_i p_i|i\rangle\langle i|.}$$

Esta expresión describe una mezcla estadística de estados.

La matriz de densidad permite calcular el valor esperado de un observable mediante:

$$\boxed{\langle\hat A\rangle=\operatorname{Tr}(\hat\rho\hat A).}$$

Esta fórmula es útil porque describe tanto estados puros como mezclas estadísticas.

# Ejercicio 2 — Fundamentos de medición cuántica

## (a) ¿Qué características debe tener un ket para representar el estado físico de un sistema? ¿Por qué?

Respuesta: debe pertenecer al espacio de Hilbert del sistema y estar normalizado:

$$\boxed{\langle\psi|\psi\rangle=1.}$$

La normalización garantiza que la suma de las probabilidades de todos los resultados posibles sea uno.

Además, dos kets que difieren únicamente en una fase global representan el mismo estado físico:

$$|\psi'\rangle=e^{i\alpha}|\psi\rangle.$$

Esto ocurre porque las predicciones físicas no cambian al multiplicar el estado por una fase global.

En consecuencia, el estado físico no corresponde a un ket único, sino a una clase de kets equivalentes bajo esa transformación.

## (b) ¿Cómo predice teóricamente los posibles valores que obtendría en la medición de un observable y sus correspondientes probabilidades?

Respuesta: se expresa el estado del sistema como una superposición de estados propios del observable y se aplica la regla de Born.

Sea:

$$\hat A|a_n\rangle=a_n|a_n\rangle$$

y supongamos que el estado del sistema es:

$$|\psi\rangle=\sum_n c_n|a_n\rangle.$$

Al medir $\hat A$:

1. Los posibles resultados son sus valores propios $a_n$.
    
2. La probabilidad de obtener cada resultado es:
    

$$\boxed{P(a_n)=|c_n|^2.}$$

Si el observable tiene valores propios degenerados, la probabilidad de obtener un valor propio determinado se calcula sumando las probabilidades de los estados propios asociados a ese valor.

En general, si $\hat P_a$ es el proyector sobre el subespacio propio correspondiente a $a$:

$$\boxed{P(a)=\langle\psi|\hat P_a|\psi\rangle.}$$

Justificación: la regla de Born relaciona las amplitudes de probabilidad de la superposición con las probabilidades de los resultados experimentales.

## (c) ¿Qué representa el valor esperado de un observable de un sistema cuando se encuentra en un estado dado? Justifique.

Respuesta: representa el promedio estadístico de los resultados que se obtendrían al medir ese observable sobre muchas copias del sistema, todas preparadas en el mismo estado.

Matemáticamente:

$$\boxed{\langle\hat A\rangle =\langle\psi|\hat A|\psi\rangle.}$$

Si los posibles resultados son $a_n$, también se expresa como:

$$\langle\hat A\rangle=\sum_n a_nP(a_n).$$

Justificación: cada resultado contribuye al promedio según la probabilidad con la que puede obtenerse.

Es importante distinguir que el valor esperado no necesariamente coincide con alguno de los resultados posibles de una medición individual.

Por ejemplo, si un observable puede tomar los valores $+1$ y $-1$, con probabilidades iguales:

$$\langle\hat A\rangle =(+1)\frac12+(-1)\frac12=0.$$

Sin embargo, una medición individual nunca produciría cero.

## (d) ¿Qué se entiende por medición en mecánica cuántica?

Respuesta: es un proceso físico mediante el cual se obtiene información sobre un sistema cuántico al interactuar con un aparato de medición.

En una medición ideal de un observable $\hat A$:

- El resultado obtenido es uno de sus valores propios.
    
- La probabilidad de obtenerlo está determinada por la regla de Born.
    
- Después de la medición, el estado del sistema queda proyectado sobre el subespacio propio correspondiente al resultado obtenido.
    

Por ejemplo, si se obtiene $a_n$, el estado posterior a una medición ideal se representa mediante:

$$|\psi'\rangle= \frac{\hat P_n|\psi\rangle} {\sqrt{\langle\psi|\hat P_n|\psi\rangle}},$$

siempre que la probabilidad de ese resultado sea distinta de cero.

Idea fundamental: la medición no solo permite obtener información; también puede modificar el estado del sistema.

## (e) ¿Qué significa que los operadores $\{\hat A,\hat B,\hat C\}$ forman un conjunto completo de observables compatibles?

Respuesta: significa que los operadores:

1. Son compatibles entre sí, es decir, conmutan por pares:

$$[\hat A,\hat B]=0, \qquad [\hat A,\hat C]=0, \qquad [\hat B,\hat C]=0.$$

2. Forman un conjunto completo: sus valores propios simultáneos permiten identificar un estado propio común de manera única, salvo por una fase global.

¿Por qué es importante?

La conmutatividad permite que los observables tengan estados propios simultáneos y, por tanto, que sus valores puedan determinarse simultáneamente en el sentido de la mecánica cuántica.

La completitud garantiza que no queden degeneraciones sin resolver. Es decir, conocer simultáneamente los valores propios de todos los operadores del conjunto determina completamente el estado propio común.

A este conjunto se le conoce como un conjunto completo de observables compatibles.

# Ejercicio 3 — Superposición y fase relativa

Se tiene un observable $\hat O$ con dos valores propios:

$$\hat O|+\rangle=+|+\rangle, \qquad \hat O|-\rangle=-|-\rangle.$$

Y la familia de estados:

$$|\theta\rangle= \frac{1}{\sqrt2} \left(|+\rangle+e^{i\theta}|-\rangle\right).$$

Debemos demostrar que:

$$\langle\hat O\rangle=0$$

para cualquier valor de $\theta$, y analizar si los estados de la familia son físicamente diferentes.

## Prerrequisitos

Hay dos ideas fundamentales para resolver este ejercicio.

1. Los operadores actúan linealmente sobre las superposiciones.

Por tanto:

$$\hat O(a|\psi\rangle+b|\phi\rangle) =a\hat O|\psi\rangle+b\hat O|\phi\rangle.$$

2. El valor esperado depende de la fase relativa.

Una fase global no tiene efectos físicos, pero una fase relativa entre dos componentes de una superposición sí puede tenerlos.

Por ejemplo, los estados:

$$\frac{|+\rangle+|-\rangle}{\sqrt2} \qquad\text{y}\qquad \frac{|+\rangle-|-\rangle}{\sqrt2}$$

no son equivalentes: la diferencia de signo es una diferencia de fase relativa.

## Paso 1. Calcular el valor esperado

Por definición:

$$\langle\hat O\rangle =\langle\theta|\hat O|\theta\rangle.$$

Primero calculamos el bra correspondiente:

$$\langle\theta| =\frac{1}{\sqrt2} \left(\langle+|+e^{-i\theta}\langle-|\right).$$

Aplicamos el operador al ket:

$$\begin{aligned} \hat O|\theta\rangle &=\frac{1}{\sqrt2} \left(\hat O|+\rangle +e^{i\theta}\hat O|-\rangle\right)\\ &=\frac{1}{\sqrt2} \left(|+\rangle-e^{i\theta}|-\rangle\right). \end{aligned}$$

Sustituimos:

$$\begin{aligned} \langle\hat O\rangle &=\frac12 \left(\langle+|+e^{-i\theta}\langle-|\right) \left(|+\rangle-e^{i\theta}|-\rangle\right). \end{aligned}$$

Desarrollamos:

$$\begin{aligned} \langle\hat O\rangle =\frac12\big(&\langle+|+\rangle -e^{i\theta}\langle+|-\rangle\\ &+e^{-i\theta}\langle-|+\rangle -\langle-|- \rangle\big). \end{aligned}$$

Como los estados propios son ortonormales:

$$\langle+|+\rangle=1, \qquad \langle- |-\rangle=1,$$

$$\langle+|-\rangle =\langle-|+\rangle=0,$$

obtenemos:

$$\begin{aligned} \langle\hat O\rangle &=\frac12(1-1)\\ &=0. \end{aligned}$$

Por tanto:

$$\boxed{\langle\hat O\rangle=0 \quad \forall\theta\in\mathbb R.}$$

## Paso 2. ¿Son físicamente diferentes los estados de la familia?

Sí. Aunque todos tienen el mismo valor esperado de $\hat O$, tienen diferentes fases relativas.

Para comprobarlo, comparemos dos estados:

$$|\theta\rangle =\frac{|+\rangle+e^{i\theta}|-\rangle}{\sqrt2},$$

$$|\theta'\rangle =\frac{|+\rangle+e^{i\theta'}|-\rangle}{\sqrt2}.$$

Si representan el mismo estado físico, deben diferir únicamente por una fase global:

$$|\theta'\rangle=e^{i\alpha}|\theta\rangle.$$

Al comparar los coeficientes de $|+\rangle$, necesariamente $e^{i\alpha}=1$. Por tanto:

$$e^{i\theta'}=e^{i\theta}.$$

Esto ocurre únicamente cuando:

$$\boxed{\theta'=\theta+2\pi k,\qquad k\in\mathbb Z.}$$

Así, los estados son físicamente diferentes para valores de $\theta$ distintos módulo $2\pi$.

Otra manera de comprobarlo es calcular su producto interno:

$$\begin{aligned} \langle\theta'|\theta\rangle &=\frac12(1+e^{i(\theta-\theta')})\\ &=e^{i(\theta-\theta')/2} \cos\left(\frac{\theta-\theta'}2\right). \end{aligned}$$

Su módulo al cuadrado es:

$$\boxed{ |\langle\theta'|\theta\rangle|^2 =\cos^2\left(\frac{\theta-\theta'}2\right). }$$

Este resultado permite distinguir estados diferentes. Por ejemplo, si:

$$\theta'=\theta+\pi,$$

entonces:

$$\langle\theta'|\theta\rangle=0.$$

Los dos estados son ortogonales y, por tanto, perfectamente distinguibles mediante una medición apropiada.

## Paso 3. ¿Cómo podrían medirse y distinguirse?

Una medición de $\hat O$ no permite distinguir los estados de esta familia.

En efecto, todos tienen la misma probabilidad de obtener cada resultado:

$$P(+1)=\left|\frac1{\sqrt2}\right|^2=\frac12,$$

$$P(-1)=\left|\frac{e^{i\theta}}{\sqrt2}\right|^2=\frac12.$$

Por tanto, medir $\hat O$ siempre produce las mismas estadísticas, independientemente de $\theta$.

Sin embargo, podemos medir otro observable sensible a la fase relativa.

Definamos:

$$\hat O_x=|+\rangle\langle-|+|-\rangle\langle+|.$$

Su valor esperado es:

$$\boxed{\langle\hat O_x\rangle=\cos\theta.}$$

También podemos definir:

$$\hat O_y=-i|+\rangle\langle-| +i|-\rangle\langle+|,$$

cuyo valor esperado es:

$$\boxed{\langle\hat O_y\rangle=\sin\theta.}$$

Así, midiendo $\hat O_x$ y $\hat O_y$ sobre sistemas preparados en el mismo estado, podemos determinar la fase relativa $\theta$.

Conclusión: los estados de la familia tienen las mismas estadísticas al medir $\hat O$, pero no representan el mismo estado físico. La fase relativa puede detectarse midiendo otros observables que no conmutan con $\hat O$.

# Ejercicio 4 — Traza y operador densidad (opcional)

## Prerrequisitos

Para resolver estos numerales necesitamos conocer tres propiedades.

1. Definición de traza

La traza de un operador es la suma de sus elementos diagonales en una base ortonormal discreta:

$$\operatorname{Tr}(\hat A)=\sum_n\langle n|\hat A|n\rangle.$$

En una representación continua:

$$\boxed{ \operatorname{Tr}(\hat A) =\int dx\,\langle x|\hat A|x\rangle. }$$

2. Relación de completitud

Para una base continua ortonormal:

$$\int dx\,|x\rangle\langle x|=\hat I.$$

Es el equivalente continuo de:

$$\sum_n|n\rangle\langle n|=\hat I.$$

3. Propiedad de los operadores de la forma $|u\rangle\langle v|$

La traza de un operador de esta forma es:

$$\boxed{\operatorname{Tr}(|u\rangle\langle v|) =\langle v|u\rangle.}$$

Esta propiedad será útil en los cálculos.

## (a) Demuestre que la traza de un producto de operadores en una representación continua satisface:

$$\operatorname{Tr}[\hat A\hat B] =\operatorname{Tr}[\hat B\hat A].$$

Idea: expresar la traza mediante integrales, introducir una base completa y cambiar las variables de integración.

### Paso 1. Escribir la definición de traza

$$\operatorname{Tr}[\hat A\hat B] =\int dx\,\langle x|\hat A\hat B|x\rangle.$$

### Paso 2. Introducir la relación de completitud

Insertamos la identidad entre los operadores:

$$\hat I=\int dy\,|y\rangle\langle y|.$$

Entonces:

$$\begin{aligned} \operatorname{Tr}[\hat A\hat B] &=\int dx\,\langle x|\hat A \left(\int dy\,|y\rangle\langle y|\right) \hat B|x\rangle\\ &=\int dx\,dy\, \langle x|\hat A|y\rangle \langle y|\hat B|x\rangle. \end{aligned}$$

### Paso 3. Intercambiar las variables de integración

Como $x$ y $y$ son variables mudas, podemos intercambiarlas:

$$\operatorname{Tr}[\hat A\hat B] =\int dy\,dx\, \langle y|\hat A|x\rangle \langle x|\hat B|y\rangle.$$

Por conmutatividad de los factores escalares:

$$\operatorname{Tr}[\hat A\hat B] =\int dx\,dy\, \langle x|\hat B|y\rangle \langle y|\hat A|x\rangle.$$

### Paso 4. Reconocer nuevamente la traza

La expresión anterior corresponde a:

$$\operatorname{Tr}[\hat B\hat A].$$

Por tanto:

$$\boxed{ \operatorname{Tr}[\hat A\hat B] =\operatorname{Tr}[\hat B\hat A]. }$$

Esta propiedad se conoce como ciclicidad de la traza. El desarrollo supone que los operadores y las integrales involucradas permiten que las operaciones estén bien definidas.

## (b) Considere un sistema en un estado cuántico $|\psi\rangle$, y usando los operadores $\hat A$ y $\hat\rho=|\psi\rangle\langle\psi|$, calcule:

$$\operatorname{Tr}[\hat\rho\hat A].$$

¿Qué interpretación física le puede dar a su cálculo? ¿Qué puede concluir adicionalmente?

### Paso 1. Sustituir el operador densidad

Tenemos:

$$\hat\rho=|\psi\rangle\langle\psi|.$$

Por tanto:

$$\operatorname{Tr}[\hat\rho\hat A] = \operatorname{Tr}[|\psi\rangle\langle\psi|\hat A].$$

### Paso 2. Aplicar la propiedad de ciclicidad

Podemos intercambiar cíclicamente los factores:

$$\operatorname{Tr}[|\psi\rangle\langle\psi|\hat A] = \operatorname{Tr}[\hat A|\psi\rangle\langle\psi|].$$

### Paso 3. Aplicar la propiedad de la traza de un producto exterior

Como:

$$\operatorname{Tr}(|u\rangle\langle v|) =\langle v|u\rangle,$$

podemos escribir:

$$\begin{aligned} \operatorname{Tr}[\hat A|\psi\rangle\langle\psi|] &=\operatorname{Tr}[(\hat A|\psi\rangle)\langle\psi|]\\ &=\langle\psi|\hat A|\psi\rangle. \end{aligned}$$

Por tanto:

$$\boxed{ \operatorname{Tr}[\hat\rho\hat A] =\langle\psi|\hat A|\psi\rangle. }$$

### Interpretación física

El resultado es el valor esperado del observable $\hat A$ en el estado $|\psi\rangle$.

Es decir, corresponde al promedio estadístico de los resultados que se obtendrían al medir $\hat A$ sobre muchas copias del sistema preparadas en ese mismo estado.

### ¿Qué podemos concluir adicionalmente?

Que la formulación mediante el operador densidad reproduce exactamente el resultado de la formulación mediante kets para estados puros:

$$\boxed{ \langle\hat A\rangle =\langle\psi|\hat A|\psi\rangle =\operatorname{Tr}(\hat\rho\hat A). }$$

Por tanto, el uso de la matriz de densidad no cambia las predicciones físicas para estados puros; proporciona una forma más general de describirlos.

## (c) Si ahora el operador densidad está determinado por:

$$\hat\rho=\sum_i p_i|i\rangle\langle i|,$$

calcule nuevamente:

$$\operatorname{Tr}[\hat\rho\hat A].$$

¿Qué interpretación física le da a su cálculo? ¿La interpretación cambió o es igual a la del ítem anterior?

### Paso 1. Sustituir el operador densidad

$$\operatorname{Tr}[\hat\rho\hat A] = \operatorname{Tr}\left[ \left(\sum_i p_i|i\rangle\langle i|\right)\hat A \right].$$

Por la linealidad de la traza:

$$\operatorname{Tr}[\hat\rho\hat A] = \sum_i p_i \operatorname{Tr}[|i\rangle\langle i|\hat A].$$

### Paso 2. Aplicar la propiedad de la traza

Utilizando nuevamente:

$$\operatorname{Tr}(|u\rangle\langle v|) =\langle v|u\rangle,$$

obtenemos:

$$\begin{aligned} \operatorname{Tr}[|i\rangle\langle i|\hat A] &=\operatorname{Tr}[\hat A|i\rangle\langle i|]\\ &=\langle i|\hat A|i\rangle. \end{aligned}$$

Por tanto:

$$\boxed{ \operatorname{Tr}[\hat\rho\hat A] =\sum_i p_i\langle i|\hat A|i\rangle. }$$

### Interpretación física

Cada término:

$$\langle i|\hat A|i\rangle$$

es el valor esperado del observable $\hat A$cuando el sistema está en el estado $|i\rangle$.

Por su parte, $p_i$ representa la probabilidad de que el sistema se encuentre en ese estado dentro de la mezcla estadística.

Por tanto:

$$\boxed{ \langle\hat A\rangle =\sum_i p_i\langle\hat A\rangle_i. }$$

El resultado es el promedio ponderado de los valores esperados correspondientes a cada estado de la mezcla.

### ¿La interpretación cambió respecto al ítem (b)?

La interpretación física fundamental es la misma: en ambos casos calculamos el valor esperado del observable, es decir, el promedio estadístico de los resultados de las mediciones.

Lo que cambia es el tipo de estado descrito:

- Ítem (b): el sistema está en un estado puro $|\psi\rangle$.
    
- Ítem (c): el sistema se describe mediante una mezcla estadística de estados $|i\rangle$, con probabilidades $p_i$.
    

El caso puro puede considerarse un caso particular del general, tomando una única probabilidad igual a uno.

## Síntesis de los resultados

| Numeral | Resultado o concepto fundamental                                                                                                       |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| 2(a)    | El ket debe pertenecer al espacio de Hilbert y estar normalizado.                                                                      |
| 2(b)    | Los resultados son los valores propios; sus probabilidades se calculan con la regla de Born.                                           |
| 2(c)    | El valor esperado es el promedio estadístico de los resultados.                                                                        |
| 2(d)    | La medición obtiene un resultado y, en general, modifica el estado del sistema.                                                        |
| 2(e)    | Los observables compatibles con un conjunto completo conmutan y determinan un estado propio común sin degeneración restante.           |
| 3       | Todos los estados tienen $\langle\hat O\rangle=0$, pero pueden distinguirse midiendo otros observables sensibles a la fase relativa. |
| 4(a)    | La traza de un producto es cíclica: $\operatorname{Tr}(\hat A\hat B)=\operatorname{Tr}(\hat B\hat A)$.                               |
| 4(b)    | Para un estado puro: $\operatorname{Tr}(\hat\rho\hat A)=\langle\psi\|\hat A\|\psi\rangle$.                                           |
| 4(c)    | Para una mezcla: $\operatorname{Tr}(\hat\rho\hat A)=\sum_i p_i\langle i\|\hat A\|i\rangle$.                                          |

La conexión central entre los ejercicios 2, 3 y 4: conocer el valor esperado de un observable no significa conocer completamente el estado cuántico. El ejercicio 3 lo demuestra: estados físicamente diferentes pueden producir exactamente el mismo valor esperado y las mismas probabilidades para un observable. Para caracterizar el estado se necesita, en general, estudiar otros observables.