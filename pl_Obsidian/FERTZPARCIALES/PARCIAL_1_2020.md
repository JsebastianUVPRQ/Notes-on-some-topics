
# Enunciados
---
Explica los prerrequisitos, los conceptos usados (en general), la razón de ser, etc; de los ejercicios. Luego resuelve paso a paso
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



# Soluciones

## 0. Prerrequisitos y conceptos fundamentales

Los ejercicios evalúan principalmente cinco ideas: estados cuánticos, operadores y observables, ecuaciones de valores propios, mediciones y probabilidades, y conjuntos completos de observables compatibles.

### 0.1. Estados cuánticos y kets

Un estado cuántico puro se representa mediante un ket $|\psi\rangle$, perteneciente a un espacio de Hilbert. En términos prácticos, debe cumplir:

- Ser distinto del ket nulo: $|\psi\rangle\neq 0$.
    
- Ser normalizable: su norma debe ser finita.
    
- Estar normalizado: se elige su representación de modo que  
    $$ 
    \langle\psi|\psi\rangle=1.  
   $$
    

La normalización permite interpretar los módulos cuadrados de las amplitudes como probabilidades cuya suma es uno.

Dos kets que difieren únicamente por una fase global, $e^{i\phi}$, representan el mismo estado físico:

$$|\psi'\rangle=e^{i\phi}|\psi\rangle.$$

### 0.2. Operadores, autovalores y autovectores

Un operador $\hat A$ actúa sobre los kets. Sus autovectores y autovalores satisfacen

$$\hat A|a_n\rangle=a_n|a_n\rangle.$$

Los autovalores indican los posibles resultados de una medición del observable representado por $\hat A$.

Un operador es hermítico cuando

$$\hat A^\dagger=\hat A.$$

Esta condición es fundamental porque garantiza, entre otras propiedades, que sus autovalores sean reales y que sus autovectores puedan formar una base ortonormal completa del espacio.

Importante: que una matriz tenga autovalores reales no es suficiente para que represente un observable físico. El ejercicio 1 muestra precisamente por qué.

### 0.3. Medición y regla de Born

Si los autovectores de un observable forman una base ortonormal y el estado está normalizado, podemos escribir

$$|\psi\rangle=\sum_n c_n|a_n\rangle, \qquad c_n=\langle a_n|\psi\rangle.$$

Al medir $\hat A$:

- Los posibles resultados son sus autovalores $a_n$.
    
- La probabilidad de obtener $a_n$, si es no degenerado, es  
    $$ 
    P(a_n)=|c_n|^2.  
   $$
    

Si un autovalor es degenerado, hay que sumar las probabilidades de todos los autovectores ortonormales asociados a él.

El valor esperado es

$$\boxed{\langle A\rangle=\langle\psi|\hat A|\psi\rangle =\sum_n a_nP(a_n).}$$

Es decir, representa el promedio estadístico de los resultados obtenidos al medir el mismo observable sobre muchos sistemas preparados en el mismo estado. No tiene por qué ser un resultado posible de una medición individual.

### 0.4. Observables compatibles y CCOC

Dos operadores son compatibles cuando conmutan:

$$[\hat A,\hat B]=\hat A\hat B-\hat B\hat A=0.$$

En ese caso pueden tener autovectores propios simultáneos.

Un conjunto completo de observables compatibles (CCOC) es un conjunto de observables que:

1. Conmutan entre sí, por pares.
    
2. Admiten una base común de autovectores.
    
3. Permiten identificar unívocamente cada estado de esa base mediante la combinación de sus valores propios.
    

La tercera condición es la completitud: no debe quedar una degeneración conjunta sin resolver.

Un conjunto completo debe ser además mínimo cuando ninguno de sus observables puede eliminarse sin perder esa propiedad.

# 1. Matriz no hermítica

Se tiene

$$M=\begin{pmatrix}1&1\\0&1\end{pmatrix}.$$

## 1(a). Autovalores reales y autovectores incompletos

Paso 1. Calcular los autovalores.

Se resuelve la ecuación característica:

$$\det(M-\lambda I)=0.$$

$$\begin{vmatrix} 1-\lambda&1\\ 0&1-\lambda \end{vmatrix}=0.$$

Por tanto,

$$(1-\lambda)^2=0 \quad\Longrightarrow\quad \boxed{\lambda=1}$$

con multiplicidad algebraica dos.

El único autovalor es real.

Paso 2. Calcular los autovectores.

Resolvemos

$$(M-I)|v\rangle=0.$$

Como

$$M-I= \begin{pmatrix} 0&1\\ 0&0 \end{pmatrix},$$

para $|v\rangle=(x,y)^T$ resulta

$$\begin{pmatrix} 0&1\\ 0&0 \end{pmatrix} \begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}0\\0\end{pmatrix}.$$

La única condición es

$$y=0.$$

Por consiguiente,

$$|v\rangle= \begin{pmatrix}x\\0\end{pmatrix} =x\begin{pmatrix}1\\0\end{pmatrix}.$$

El espacio propio tiene dimensión uno: solo existe un autovector linealmente independiente.

Conclusión:

La matriz tiene dos autovalores reales contando multiplicidad, pero únicamente un autovector linealmente independiente. Como el espacio tiene dimensión dos, sus autovectores no forman una base completa.

$$\boxed{\text{M tiene espectro real, pero no una base completa de autovectores.}}$$

## 1(b). Encontrar un valor esperado complejo

Buscamos un ket normalizado para el cual

$$\langle v|M|v\rangle\notin\mathbb R.$$

Tomemos

$$|v\rangle=\frac{1}{\sqrt2} \begin{pmatrix}1\\i\end{pmatrix}, \qquad \langle v|=\frac{1}{\sqrt2} \begin{pmatrix}1&-i\end{pmatrix}.$$

Primero verificamos su normalización:

$$\langle v|v\rangle =\frac12(1+(-i)i)=1.$$

Ahora aplicamos la matriz:

$$M|v\rangle = \frac{1}{\sqrt2} \begin{pmatrix} 1+i\\i \end{pmatrix}.$$

Entonces,

$$\begin{aligned} \langle v|M|v\rangle &=\frac12 \begin{pmatrix}1&-i\end{pmatrix} \begin{pmatrix}1+i\\i\end{pmatrix}\\ &=\frac12(1+i-i^2)\\ &=\boxed{1+\frac{i}{2}}. \end{aligned}$$

El valor esperado es complejo, como se requería.

## 1(c). ¿Qué interpretación física no se puede utilizar?

No podemos interpretar el valor esperado como el promedio estadístico de los resultados de una medición física.

La razón es que los resultados de una medición de un observable deben ser reales. Por tanto, cualquier promedio de esos resultados, ponderado por probabilidades reales, también debe ser real.

Como aquí obtenemos un valor complejo, $M$ no puede representar un observable físico.

Conclusión: tener autovalores reales no basta para representar un observable; se requiere hermiticidad.

# 2. Fundamentos de estados y mediciones

## 2(a). ¿Qué características debe tener un ket para representar un estado físico?

Debe ser un elemento no nulo y normalizable del espacio de Hilbert. Se acostumbra representarlo normalizado:

$$\boxed{\langle\psi|\psi\rangle=1.}$$

La razón es que la norma determina la probabilidad total. Con la normalización, la suma de las probabilidades de todos los resultados posibles es uno.

Además, dos kets que solo difieren en una fase global representan el mismo estado físico:

$$|\psi'\rangle=e^{i\phi}|\psi\rangle.$$

## 2(b). ¿Cómo se predicen los resultados y sus probabilidades?

Se expresa el estado como superposición de los autokets del observable:

$$|\psi\rangle=\sum_n c_n|a_n\rangle,$$

donde

$$\hat A|a_n\rangle=a_n|a_n\rangle.$$

La regla de Born establece que:

- Los resultados posibles son los autovalores $a_n$.
    
- La probabilidad de obtener cada resultado no degenerado es
    

$$\boxed{P(a_n)=|c_n|^2.}$$

Para un autovalor degenerado, se suman los módulos cuadrados de todas las amplitudes correspondientes a ese mismo autovalor.

## 2(c). ¿Qué representa el valor esperado?

Representa el promedio estadístico de los resultados de muchas mediciones del mismo observable sobre sistemas preparados en el mismo estado.

Se calcula mediante

$$\boxed{\langle A\rangle=\langle\psi|\hat A|\psi\rangle =\sum_n a_nP(a_n).}$$

No necesariamente coincide con un resultado posible de una medición individual. Por ejemplo, si los únicos resultados posibles son $+1$ y $-1$, el promedio puede ser cero, aunque cero no sea un resultado posible.

## 2(d). ¿Qué significa que $\{\hat A,\hat B,\hat C\}$ formen un CCOC?

Significa que:

1. Los operadores conmutan por pares:  
    $$ 
    [\hat A,\hat B]=[\hat A,\hat C]=[\hat B,\hat C]=0.  
   $$
    
2. Poseen autokets simultáneos.
    
3. Cada combinación de valores propios identifica unívocamente un autoket.
    

En otras palabras, sus mediciones simultáneas permiten determinar completamente el estado dentro de la base considerada, sin degeneración conjunta restante.

# 3. Observables compatibles y autovectores simultáneos

Se tiene la base ortonormal

$$\{|1\rangle,|2\rangle,|3\rangle\}$$

y los operadores

$$\hat A= \begin{pmatrix} 2\hbar^2&0&0\\ 0&2\hbar^2&0\\ 0&0&2\hbar^2 \end{pmatrix}, \qquad \hat B=\frac{\hbar}{\sqrt2} \begin{pmatrix} 0&-i&0\\ i&0&-i\\ 0&i&0 \end{pmatrix}.$$

## 3(a). Vectores y kets propios simultáneos normalizados

Paso 1. Analizar el operador $\hat A$.

Observamos que

$$\hat A=2\hbar^2 I.$$

Por tanto, para cualquier ket del espacio,

$$\hat A|\psi\rangle=2\hbar^2|\psi\rangle.$$

Todos los kets son autovectores de $\hat A$, con el mismo autovalor:

$$\boxed{a=2\hbar^2.}$$

Esto significa que $\hat A$ tiene un autovalor triplemente degenerado.

Paso 2. Encontrar los autovalores de $\hat B$.

Sea

$$\hat B|b\rangle=b|b\rangle, \qquad |b\rangle= \begin{pmatrix}x\\y\\z\end{pmatrix}.$$

La ecuación característica es

$$\det(\hat B-bI)=0.$$

Podemos definir $\lambda=b/\hbar$ y utilizar la matriz adimensional:

$$\det\begin{pmatrix} -\lambda&-\frac{i}{\sqrt2}&0\\ \frac{i}{\sqrt2}&-\lambda&-\frac{i}{\sqrt2}\\ 0&\frac{i}{\sqrt2}&-\lambda \end{pmatrix}=0.$$

Al desarrollar el determinante,

$$-\lambda(\lambda^2-1)=0.$$

Así,

$$\lambda=1,\quad 0,\quad -1.$$

Los autovalores de $\hat B$ son

$$\boxed{b_1=+\hbar,\qquad b_2=0,\qquad b_3=-\hbar.}$$

Paso 3. Calcular los autovectores de $\hat B$.

Para $b_1=+\hbar$, resolvemos

$$(\hat B-\hbar I)|b_1\rangle=0.$$

Las ecuaciones resultantes permiten obtener

$$y=i\sqrt2x,\qquad z=-x.$$

Escogiendo $x=1/2$ y normalizando:

$$\boxed{ |b_1\rangle= \begin{pmatrix} \frac12\\[2pt] \frac{i}{\sqrt2}\\[2pt] -\frac12 \end{pmatrix}. }$$

Para $b_2=0$:

$$\hat B|b_2\rangle=0.$$

Se obtiene

$$y=0,\qquad z=x.$$

Normalizando:

$$\boxed{ |b_2\rangle= \begin{pmatrix} \frac1{\sqrt2}\\[2pt] 0\\[2pt] \frac1{\sqrt2} \end{pmatrix}. }$$

Para $b_3=-\hbar$:

$$(\hat B+\hbar I)|b_3\rangle=0.$$

Se obtiene

$$y=-i\sqrt2x,\qquad z=-x.$$

Normalizando:

$$\boxed{ |b_3\rangle= \begin{pmatrix} \frac12\\[2pt] -\frac{i}{\sqrt2}\\[2pt] -\frac12 \end{pmatrix}. }$$

Paso 4. Expresar los autokets en la base original.

Como los componentes de un vector son sus coeficientes respecto de la base dada:

$$\boxed{ |b_1\rangle= \frac12|1\rangle+\frac{i}{\sqrt2}|2\rangle-\frac12|3\rangle }$$

$$\boxed{ |b_2\rangle= \frac1{\sqrt2}|1\rangle+\frac1{\sqrt2}|3\rangle }$$

$$\boxed{ |b_3\rangle= \frac12|1\rangle-\frac{i}{\sqrt2}|2\rangle-\frac12|3\rangle. }$$

Como $\hat A$ es proporcional a la identidad, estos tres autokets de $\hat B$ también son autokets de $\hat A$.

Las parejas de autovalores correspondientes son:

|Ket propio simultáneo|Autovalor de $\hat A$|Autovalor de $\hat B$|
|---|---|---|
|$\|b_1\rangle$|$2\hbar^2$|$+\hbar$|
|$\|b_2\rangle$|$2\hbar^2$|$0$|
|$\|b_3\rangle$|$2\hbar^2$|$-\hbar$|

Estos kets forman una base ortonormal.

## 3(b). ¿Cuál de los conjuntos es un CCOC?

Se consideran:

$$\{\hat A\},\qquad \{\hat B\},\qquad \{\hat A,\hat B\}.$$

1. Conjunto $\{\hat A\}$.

No es completo porque $\hat A$ tiene un único autovalor, $2\hbar^2$, con degeneración tres. Medirlo no permite distinguir entre los tres estados.

2. Conjunto $\{\hat B\}$.

Sí es completo porque sus tres autovalores son distintos y cada uno identifica un único autoket.

$$\boxed{\{\hat B\}\text{ es un CCOC.}}$$

3. Conjunto $\{\hat A,\hat B\}$.

También es completo: sus parejas de autovalores identifican unívocamente los tres autokets. Además, los operadores conmutan porque $\hat A$ es proporcional a la identidad:

$$[\hat A,\hat B]=0.$$

Sin embargo, $\hat A$ es redundante para conseguir la completitud.

Conclusión:

$$\boxed{ \{\hat B\}\text{ es el CCOC mínimo.} }$$

El conjunto $\{\hat A,\hat B\}$ es completo, pero no mínimo.

## 3(c). ¿La superposición más general es un autoket de $\hat A$?

La superposición más general normalizada de los autokets simultáneos es

$$|\psi\rangle=c_1|b_1\rangle+c_2|b_2\rangle+c_3|b_3\rangle,$$

con

$$|c_1|^2+|c_2|^2+|c_3|^2=1.$$

Aplicamos $\hat A$:

$$\begin{aligned} \hat A|\psi\rangle &=c_1\hat A|b_1\rangle +c_2\hat A|b_2\rangle +c_3\hat A|b_3\rangle\\ &=2\hbar^2c_1|b_1\rangle +2\hbar^2c_2|b_2\rangle +2\hbar^2c_3|b_3\rangle. \end{aligned}$$

Por tanto,

$$\boxed{\hat A|\psi\rangle=2\hbar^2|\psi\rangle.}$$

Sí, cualquier superposición de esos kets es un autoket de $\hat A$.

¿Era esperable? Sí. El operador $\hat A$ tiene un único autovalor y todo el espacio pertenece a su espacio propio. Una combinación lineal de sus autovectores sigue siendo un autovector con ese mismo autovalor.

## 3(d). Espectros y probabilidades de medición

Primero hay que distinguir dos conceptos:

- Espectro: conjunto de autovalores de un observable.
    
- Distribución de probabilidades: probabilidades de obtener esos autovalores, que dependen del estado del sistema.
    

### Observable $\hat A$

Su espectro consiste en un solo autovalor:

$$\boxed{\operatorname{Esp}(\hat A)=\{2\hbar^2\}.}$$

Es triplemente degenerado. Como cualquier estado es un autoket suyo, la distribución es:

|Autovalor|Probabilidad|
|---|---|
|$2\hbar^2$|$1$|

Esquema:

```
Probabilidad
  1 ┤       ●
    │
  0 ┼────────────────
          2ℏ²
       Autovalor
```

### Observable $\hat B$

Su espectro es

$$\boxed{\operatorname{Esp}(\hat B)=\{-\hbar,0,+\hbar\}.}$$

Los tres autovalores son no degenerados.

Para un estado general

$$|\psi\rangle=c_1|b_1\rangle+c_2|b_2\rangle+c_3|b_3\rangle,$$

las probabilidades son:

|Autovalor|Probabilidad|
|---|---|
|$+\hbar$|$\|c_1\|^2$|
|$0$|$\|c_2\|^2$|
|$-\hbar$|$\|c_3\|^2$|

Por tanto, sin conocer el estado no es posible asignar probabilidades numéricas a los tres resultados. Lo que sí queda determinado por las matrices es el espectro.

## 3(e). Valores esperados en el estado $|\gamma\rangle$

Se da

$$|\gamma\rangle= \frac1{\sqrt{17}} \left(2|b_1\rangle+3|b_2\rangle+2|b_3\rangle\right).$$

Paso 1. Comprobar la normalización.

Como los kets son ortonormales:

$$\langle\gamma|\gamma\rangle =\frac1{17}(4+9+4)=1.$$

Paso 2. Calcular el valor esperado de $\hat A$.

Utilizamos

$$\hat A|b_i\rangle=2\hbar^2|b_i\rangle.$$

Entonces,

$$\begin{aligned} \langle A\rangle &=\langle\gamma|\hat A|\gamma\rangle\\ &=\frac1{17} \left[4(2\hbar^2)+9(2\hbar^2)+4(2\hbar^2)\right]\\ &=\boxed{2\hbar^2}. \end{aligned}$$

Paso 3. Calcular el valor esperado de $\hat B$.

Sabemos que

$$\hat B|b_1\rangle=\hbar|b_1\rangle, \quad \hat B|b_2\rangle=0, \quad \hat B|b_3\rangle=-\hbar|b_3\rangle.$$

Por tanto,

$$\begin{aligned} \langle B\rangle &=\frac1{17} \left[4\hbar+9(0)-4\hbar\right]\\ &=\boxed{0}. \end{aligned}$$

Los resultados son:

$$\boxed{\langle A\rangle=2\hbar^2,\qquad \langle B\rangle=0.}$$

La interpretación es directa: $\hat A$ siempre produce el resultado $2\hbar^2$, mientras que los resultados de $\hat B$ tienen probabilidades $4/17,\ 9/17,\ 4/17$, respectivamente. Las contribuciones de $+\hbar$ y $-\hbar$ se cancelan en el promedio.

# 4. Mediciones simultáneas de un CCOC

Se proporciona

$$|\eta\rangle=\frac13 \left[ 2|a,-b,c\rangle +|-a,b,c\rangle -2|-a,-b,c\rangle \right].$$

Los kets son autokets simultáneos de $\hat A,\hat B,\hat C$. Por ejemplo,

$$\hat A|a,-b,c\rangle=a|a,-b,c\rangle,$$

$$\hat B|a,-b,c\rangle=-b|a,-b,c\rangle,$$

$$\hat C|a,-b,c\rangle=c|a,-b,c\rangle.$$

Además, son ortonormales.

## 4(a). Normalizar el ket

Calculamos su norma:

$$\begin{aligned} \langle\eta|\eta\rangle &=\frac19\left[ 4\langle a,-b,c|a,-b,c\rangle\right.\\ &\quad+\langle-a,b,c|-a,b,c\rangle\\ &\quad\left.+4\langle-a,-b,c|-a,-b,c\rangle \right]. \end{aligned}$$

Los productos cruzados son cero por ortogonalidad y los productos de cada ket consigo mismo son uno:

$$\langle\eta|\eta\rangle =\frac19(4+1+4)=1.$$

Por tanto, el estado ya está normalizado:

$$\boxed{|\eta\rangle_{\mathrm{norm}}=|\eta\rangle.}$$

## 4(b). Resultados y probabilidades de una medición simultánea

Los posibles resultados son las ternas de autovalores presentes en el estado:

$$(a,-b,c),\qquad (-a,b,c),\qquad (-a,-b,c).$$

La probabilidad de cada terna es el módulo cuadrado de su coeficiente.

|Resultado $(A,B,C)$|Amplitud|Probabilidad|
|---|---|---|
|$(a,-b,c)$|$2/3$|$4/9$|
|$(-a,b,c)$|$1/3$|$1/9$|
|$(-a,-b,c)$|$-2/3$|$4/9$|

Se verifica:

$$\frac49+\frac19+\frac49=1.$$

## 4(c). Posibles resultados de medir $\hat B$

Agrupamos las probabilidades de los estados que tienen el mismo autovalor de $\hat B$.

Para obtener $+b$, el único estado presente es $|-a,b,c\rangle$:

$$\boxed{P(B=+b)=\frac19.}$$

Para obtener $-b$, hay dos estados posibles:

$$\begin{aligned} P(B=-b) &=P(a,-b,c)+P(-a,-b,c)\\ &=\frac49+\frac49. \end{aligned}$$

Por tanto,

$$\boxed{P(B=-b)=\frac89.}$$

Los resultados posibles son $+b$ y $-b$, con probabilidades $1/9$ y $8/9$, respectivamente.

## 4(d). ¿Es $|\eta\rangle$ autoket de alguno de los observables?

Examinamos la superposición:

- Para $\hat A$, aparecen autovalores $+a$ y $-a$.
    
- Para $\hat B$, aparecen autovalores $+b$ y $-b$.
    
- Para $\hat C$, todos los kets tienen el mismo autovalor $c$.
    

Por tanto,

$$\boxed{\hat C|\eta\rangle=c|\eta\rangle.}$$

El estado es autoket de $\hat C$, pero no de $\hat A$ ni de $\hat B$, suponiendo que $a\neq -a$ y $b\neq-b$.

## 4(e). Valores esperados de $\hat A$ y $\hat C$

Para $\hat A$:

El resultado $+a$ tiene probabilidad $4/9$, mientras que $-a$ tiene probabilidad $1/9+4/9=5/9$.

Entonces,

$$\begin{aligned} \langle A\rangle &=a\left(\frac49\right)+(-a)\left(\frac59\right)\\ &=\frac{4a-5a}{9}. \end{aligned}$$

$$\boxed{\langle A\rangle=-\frac a9.}$$

Para $\hat C$:

Todos los componentes del estado tienen autovalor $c$. Por tanto,

$$\boxed{\langle C\rangle=c.}$$

¿Eran esperables estos resultados?

- Para $\hat A$, no es sorprendente que el valor esperado no sea uno de sus autovalores: el estado no es un autoket de $\hat A$.
    
- Para $\hat C$, sí: como el estado es un autoket de este observable, su valor esperado coincide con su autovalor $c$.
    

# 5. Espín $1/2$ y conmutadores

## 5(a). Medición de $\hat S_z$

Se tiene

$$\hat S_z|\pm\rangle =\pm\frac{\hbar}{2}|\pm\rangle$$

y el estado

$$|\eta\rangle=\frac1{\sqrt2}\left(|+\rangle+i|-\rangle\right).$$

### i. Probabilidad de obtener $|+\rangle$

La amplitud correspondiente es

$$c_+=\langle+|\eta\rangle=\frac1{\sqrt2}.$$

Aplicando la regla de Born:

$$\boxed{P(+)=|c_+|^2=\frac12.}$$

### ii. Posibles resultados de medir $\hat S_z$

Los resultados posibles son sus autovalores:

$$\boxed{S_z=+\frac{\hbar}{2} \quad\text{o}\quad S_z=-\frac{\hbar}{2}.}$$

Cada resultado tiene probabilidad $1/2$.

### iii. Valor esperado de $\hat S_z$

Por definición:

$$\langle S_z\rangle =\langle\eta|\hat S_z|\eta\rangle.$$

Primero aplicamos el operador:

$$\begin{aligned} \hat S_z|\eta\rangle &=\frac1{\sqrt2} \left( \hat S_z|+\rangle+i\hat S_z|-\rangle \right)\\ &=\frac{\hbar}{2\sqrt2} \left(|+\rangle-i|-\rangle\right). \end{aligned}$$

El bra correspondiente es

$$\langle\eta| =\frac1{\sqrt2}(\langle+|-i\langle-|).$$

Entonces,

$$\begin{aligned} \langle S_z\rangle &=\frac{\hbar}{4} (\langle+|-i\langle-|) (|+\rangle-i|-\rangle)\\ &=\frac{\hbar}{4}(1-1)\\ &=\boxed{0}. \end{aligned}$$

¿Era esperable? Sí. Los dos resultados posibles tienen igual probabilidad y valores opuestos:

$$\langle S_z\rangle =\frac12\left(\frac{\hbar}{2}\right) +\frac12\left(-\frac{\hbar}{2}\right)=0.$$

Es importante notar que $0$ es el valor promedio, pero no es un resultado posible de una medición individual de $\hat S_z$.

## 5(b). Valor esperado de un conmutador en un autoestado del Hamiltoniano

El enunciado parece tener una omisión: probablemente solicita demostrar que

$$\boxed{ \langle\Psi_n|[\hat A,\hat H]|\Psi_n\rangle=0. }$$

Se conoce que

$$\hat H|\Psi_n\rangle=E_n|\Psi_n\rangle.$$

Además, al tratarse de un Hamiltoniano físico, es hermítico:

$$\hat H^\dagger=\hat H.$$

Paso 1. Desarrollar el conmutador.

Por definición,

$$[\hat A,\hat H]=\hat A\hat H-\hat H\hat A.$$

Por tanto,

$$\begin{aligned} \langle\Psi_n|[\hat A,\hat H]|\Psi_n\rangle &=\langle\Psi_n|\hat A\hat H|\Psi_n\rangle\\ &\quad-\langle\Psi_n|\hat H\hat A|\Psi_n\rangle. \end{aligned}$$

Paso 2. Evaluar el primer término.

Utilizamos la ecuación de valores propios:

$$\begin{aligned} \langle\Psi_n|\hat A\hat H|\Psi_n\rangle &=\langle\Psi_n|\hat A(E_n|\Psi_n\rangle)\\ &=E_n\langle\Psi_n|\hat A|\Psi_n\rangle. \end{aligned}$$

Paso 3. Evaluar el segundo término.

Como $\hat H$ es hermítico y $E_n$ es real, también se cumple

$$\langle\Psi_n|\hat H=E_n\langle\Psi_n|.$$

Por consiguiente,

$$\begin{aligned} \langle\Psi_n|\hat H\hat A|\Psi_n\rangle &=E_n\langle\Psi_n|\hat A|\Psi_n\rangle. \end{aligned}$$

Paso 4. Restar los términos.

$$\begin{aligned} \langle\Psi_n|[\hat A,\hat H]|\Psi_n\rangle &=E_n\langle\Psi_n|\hat A|\Psi_n\rangle\\ &\quad-E_n\langle\Psi_n|\hat A|\Psi_n\rangle\\ &=0. \end{aligned}$$

Por tanto,

$$\boxed{ \langle\Psi_n|[\hat A,\hat H]|\Psi_n\rangle=0. }$$

La demostración es válida para cualquier operador $\hat A$; no necesitamos que $\hat A$ sea hermítico.

## Síntesis: ideas que debes dominar para este parcial

|Concepto|Idea fundamental|
|---|---|
|Hermiticidad|Garantiza autovalores reales y una base ortonormal completa de autovectores.|
|Degeneración|Un mismo autovalor puede corresponder a varios autovectores independientes.|
|Regla de Born|La probabilidad de un resultado es el módulo cuadrado de su amplitud.|
|Valor esperado|Es el promedio estadístico de los posibles resultados, no necesariamente un resultado posible.|
|Compatibilidad|Los observables compatibles conmutan y pueden tener autovectores simultáneos.|
|CCOC|Sus valores propios conjuntos identifican unívocamente cada estado de la base.|
|Superposición|Una combinación de autovectores con distintos autovalores no suele ser autovector; si comparten el mismo autovalor, sí lo es.|
|Conmutadores|En un autoestado de $\hat H$, el valor esperado de $[\hat A,\hat H]$ es cero para cualquier $\hat A$.|

La conexión más importante entre los ejercicios: el parcial gira alrededor de cómo un estado se descompone en autokets de un observable y cómo esa descomposición permite predecir resultados, probabilidades y valores esperados. Comprender esa relación facilita resolver prácticamente todos los numerales sin memorizar procedimientos aislados.