# Enunciados

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

# Solucion

# 0. Prerrequisitos y conceptos fundamentales

Este parcial profundiza en varios conceptos que se conectan entre sí. La idea es comprender primero las herramientas matemáticas y físicas que se utilizan repetidamente.

## 0.1. Producto interno, producto exterior y representación matricial

Dados dos kets $|\alpha\rangle$ y $|\beta\rangle$:

Producto interno:

$$\langle\alpha|\beta\rangle\in\mathbb C.$$

Es un número complejo que permite calcular amplitudes, ortogonalidad y normas.

Producto exterior:

$$|\alpha\rangle\langle\beta|.$$

Es un operador, no un número. Su acción sobre un ket arbitrario es

$$\boxed{ (|\alpha\rangle\langle\beta|)|\psi\rangle = |\alpha\rangle\langle\beta|\psi\rangle. }$$

Primero calcula cuánto se proyecta $|\psi\rangle$ sobre $|\beta\rangle$, y después multiplica $|\alpha\rangle$ por esa amplitud.

En una base ortonormal completa $\{|a_i\rangle\}$, cualquier ket se expresa como

$$|\alpha\rangle=\sum_i\alpha_i|a_i\rangle, \qquad \alpha_i=\langle a_i|\alpha\rangle.$$

Análogamente,

$$|\beta\rangle=\sum_i\beta_i|a_i\rangle.$$

La matriz de un operador $\hat O$ en dicha base tiene elementos

$$\boxed{O_{ij}=\langle a_i|\hat O|a_j\rangle.}$$

Esta definición será fundamental en el ejercicio 1.

## 0.2. Espín $1/2$ y operadores de espín

Un sistema de espín $1/2$ tiene dos estados propios de $\hat S_z$:

$$\hat S_z|+\rangle=\frac{\hbar}{2}|+\rangle,$$

$$\hat S_z|-\rangle=-\frac{\hbar}{2}|-\rangle.$$

En esta base, los operadores de espín se representan mediante

$$\hat S_x=\frac{\hbar}{2} \begin{pmatrix} 0&1\\ 1&0 \end{pmatrix},$$

$$\hat S_y=\frac{\hbar}{2} \begin{pmatrix} 0&-i\\ i&0 \end{pmatrix},$$

$$\hat S_z=\frac{\hbar}{2} \begin{pmatrix} 1&0\\ 0&-1 \end{pmatrix}.$$

Las matrices sin el factor $\hbar/2$ son las matrices de Pauli.

Estos operadores no conmutan entre sí. Esto significa que no podemos asignar, en general, valores definidos simultáneos a las tres componentes del espín.

Las relaciones fundamentales son

$$[\hat S_i,\hat S_j] =i\hbar\epsilon_{ijk}\hat S_k.$$

También satisfacen

$$\{\hat S_i,\hat S_j\} =\frac{\hbar^2}{2}\delta_{ij}\hat I.$$

Aquí $\hat I$ es la identidad. Es frecuente omitirla cuando se escribe esta relación.

## 0.3. Hermiticidad y observables físicos

Un observable físico se representa mediante un operador hermítico:

$$\boxed{\hat A^\dagger=\hat A.}$$

Esta propiedad garantiza que:

1. Sus autovalores sean reales.
    
2. Sus autovectores puedan formar una base ortonormal completa.
    
3. Sus valores esperados sean reales.
    

No basta con que el operador tenga autovalores reales. El primer ejercicio precisamente explora esta diferencia.

## 0.4. Superposición y medición

Si el estado normalizado es

$$|\psi\rangle=\sum_n c_n|a_n\rangle$$

y los kets son autovectores ortonormales de $\hat A$,

$$\hat A|a_n\rangle=a_n|a_n\rangle,$$

entonces:

$$\boxed{P(a_n)=|c_n|^2.}$$

El valor esperado es

$$\boxed{ \langle A\rangle =\sum_n a_n|c_n|^2. }$$

Es el promedio estadístico de los resultados, no necesariamente un resultado posible de una medición individual.

## 0.5. Medición como proyección

Cuando se realiza una medición que selecciona un autovalor concreto, el estado se proyecta sobre el correspondiente espacio propio.

Para un resultado no degenerado $a_n$:

$$|\psi\rangle \longrightarrow \frac{|a_n\rangle\langle a_n|\psi\rangle} {\sqrt{|\langle a_n|\psi\rangle|^2}}.$$

La probabilidad de que ocurra esa proyección es

$$P(a_n)=|\langle a_n|\psi\rangle|^2.$$

Esta idea será esencial para entender el experimento de Stern-Gerlach del ejercicio 5.

# 1. Productos exteriores, operadores de espín y degeneración

## 1(a)(i). Representación matricial de $|\alpha\rangle\langle\beta|$

Se conocen las amplitudes de probabilidad de los kets $|\alpha\rangle$ y $|\beta\rangle$ en una base ortonormal completa:

$$\{|a_i\rangle\}.$$

Debemos construir la matriz del operador

$$\hat O=|\alpha\rangle\langle\beta|.$$

### Paso 1. Expresar los kets en la base

Definimos

$$\alpha_i=\langle a_i|\alpha\rangle, \qquad \beta_i=\langle a_i|\beta\rangle.$$

Por completitud,

$$|\alpha\rangle=\sum_i\alpha_i|a_i\rangle,$$

$$\langle\beta|=\sum_j\beta_j^*\langle a_j|.$$

Por tanto,

$$\hat O= \sum_{i,j}\alpha_i\beta_j^* |a_i\rangle\langle a_j|.$$

### Paso 2. Calcular los elementos matriciales

Por definición,

$$O_{ij}=\langle a_i|\hat O|a_j\rangle.$$

Sustituyendo:

$$\begin{aligned} O_{ij} &=\langle a_i|\alpha\rangle \langle\beta|a_j\rangle\\ &=\alpha_i\beta_j^*. \end{aligned}$$

Por consiguiente,

$$\boxed{O_{ij}=\alpha_i\beta_j^*.}$$

### Resultado

La representación matricial es el producto de una columna por una fila:

$$\boxed{ [O]= \begin{pmatrix} \alpha_1\\ \alpha_2\\ \vdots \end{pmatrix} \begin{pmatrix} \beta_1^*&\beta_2^*&\cdots \end{pmatrix}. }$$

Es decir,

$$[O]=[\alpha][\beta]^\dagger.$$

Interpretación: el producto exterior permite construir la matriz de un operador directamente a partir de las componentes de dos kets.

## 1(a)(ii). Aplicación a un sistema de espín $1/2$

El enunciado repite el mismo estado para $|\alpha\rangle$ y $|\beta\rangle$:

$$|\alpha\rangle=|\beta\rangle =|s_x=\hbar/2\rangle.$$

Tomando literalmente el enunciado, debemos calcular

$$|\alpha\rangle\langle\beta| =|+x\rangle\langle+x|.$$

### Paso 1. Expresar $|+x\rangle$ en la base de $\hat S_z$

Sabemos que

$$|+x\rangle =\frac1{\sqrt2}(|+\rangle+|-\rangle).$$

Por tanto, su vector columna es

$$[+x]=\frac1{\sqrt2} \begin{pmatrix}1\\1\end{pmatrix}.$$

El bra correspondiente es

$$\langle+x| =\frac1{\sqrt2} \begin{pmatrix}1&1\end{pmatrix}.$$

### Paso 2. Calcular el producto exterior

$$\begin{aligned} |+x\rangle\langle+x| &=\frac12 \begin{pmatrix}1\\1\end{pmatrix} \begin{pmatrix}1&1\end{pmatrix}\\ &=\frac12 \begin{pmatrix} 1&1\\ 1&1 \end{pmatrix}. \end{aligned}$$

Por tanto,

$$\boxed{ [|\alpha\rangle\langle\beta|] = \frac12 \begin{pmatrix} 1&1\\ 1&1 \end{pmatrix}. }$$

Observación sobre el OCR: si el segundo ket debía ser $|s_x=-\hbar/2\rangle$, entonces

$$|-x\rangle=\frac1{\sqrt2}(|+\rangle-|-\rangle)$$

y el resultado alternativo sería

$$\boxed{ |+x\rangle\langle-x| = \frac12 \begin{pmatrix} 1&-1\\ 1&-1 \end{pmatrix}. }$$

## 1(b). Demostrar las relaciones de conmutación y anticonmutación

Debemos demostrar

$$[\hat S_i,\hat S_j] =i\hbar\epsilon_{ijk}\hat S_k$$

y

$$\{\hat S_i,\hat S_j\} =\frac{\hbar^2}{2}\delta_{ij}\hat I.$$

La herramienta principal será la ortonormalidad:

$$\langle+|+\rangle=1, \qquad \langle-|-\rangle=1, \qquad \langle+|-\rangle=0.$$

### Paso 1. Introducir operadores auxiliares

Para simplificar la demostración, definimos

$$P=|+\rangle\langle+|, \qquad Q=|-\rangle\langle-|,$$

$$X=|+\rangle\langle-|, \qquad Y=|-\rangle\langle+|.$$

La multiplicación de estos operadores se obtiene utilizando

$$(|a\rangle\langle b|)(|c\rangle\langle d|) = \langle b|c\rangle|a\rangle\langle d|.$$

Por ortonormalidad:

$$X^2=0,\qquad Y^2=0,$$

$$XY=P,\qquad YX=Q.$$

Además,

$$P+Q=\hat I, \qquad PQ=QP=0.$$

### Paso 2. Reescribir los operadores de espín

Las expresiones del problema quedan

$$\hat S_x=\frac{\hbar}{2}(X+Y),$$

$$\hat S_y=\frac{\hbar}{2}(-iX+iY),$$

$$\hat S_z=\frac{\hbar}{2}(P-Q).$$

### Paso 3. Demostrar un conmutador

Empezamos con

$$[\hat S_x,\hat S_y] =\hat S_x\hat S_y-\hat S_y\hat S_x.$$

Calculamos el primer producto:

$$\begin{aligned} \hat S_x\hat S_y &=\frac{\hbar^2}{4}(X+Y)(-iX+iY)\\ &=\frac{i\hbar^2}{4}(XY-YX)\\ &=\frac{i\hbar^2}{4}(P-Q). \end{aligned}$$

El segundo producto es

$$\begin{aligned} \hat S_y\hat S_x &=\frac{\hbar^2}{4}(-iX+iY)(X+Y)\\ &=-\frac{i\hbar^2}{4}(P-Q). \end{aligned}$$

Restando:

$$\begin{aligned} [\hat S_x,\hat S_y] &=\frac{i\hbar^2}{2}(P-Q)\\ &=i\hbar\hat S_z. \end{aligned}$$

Por tanto,

$$\boxed{[\hat S_x,\hat S_y]=i\hbar\hat S_z.}$$

Repitiendo el mismo procedimiento cíclicamente:

$$\boxed{[\hat S_y,\hat S_z]=i\hbar\hat S_x,}$$

$$\boxed{[\hat S_z,\hat S_x]=i\hbar\hat S_y.}$$

Como el conmutador es antisimétrico,

$$[\hat S_i,\hat S_j]=-[\hat S_j,\hat S_i],$$

obtenemos la expresión general:

$$\boxed{ [\hat S_i,\hat S_j] =i\hbar\epsilon_{ijk}\hat S_k. }$$

### Paso 4. Demostrar los anticonmutadores

Recordemos que

$$\{\hat A,\hat B\}=\hat A\hat B+\hat B\hat A.$$

Primero calculamos los cuadrados:

$$\begin{aligned} \hat S_x^2 &=\frac{\hbar^2}{4}(X+Y)^2\\ &=\frac{\hbar^2}{4}(XY+YX)\\ &=\frac{\hbar^2}{4}(P+Q). \end{aligned}$$

Por tanto,

$$\hat S_x^2=\frac{\hbar^2}{4}\hat I.$$

De manera análoga,

$$\hat S_y^2=\frac{\hbar^2}{4}\hat I, \qquad \hat S_z^2=\frac{\hbar^2}{4}\hat I.$$

Así,

$$\{\hat S_i,\hat S_i\} =2\hat S_i^2 =\frac{\hbar^2}{2}\hat I.$$

Para componentes diferentes, los productos se cancelan al sumarlos. Por ejemplo:

$$\hat S_x\hat S_y =-\hat S_y\hat S_x,$$

por lo que

$$\{\hat S_x,\hat S_y\}=0.$$

Lo mismo sucede con los otros pares.

En consecuencia,

$$\boxed{ \{\hat S_i,\hat S_j\} =\frac{\hbar^2}{2}\delta_{ij}\hat I. }$$

Interpretación: las relaciones de conmutación describen la incompatibilidad entre las componentes del espín; las de anticonmutación expresan otra propiedad algebraica que caracteriza las matrices de Pauli.

## 1(c). ¿Cuándo la suma de dos autokets es otro autoket?

Sean

$$\hat A|i\rangle=a_i|i\rangle,$$

$$\hat A|j\rangle=a_j|j\rangle.$$

Queremos determinar cuándo

$$|i\rangle+|j\rangle$$

también es un autoket de $\hat A$.

### Paso 1. Aplicar el operador a la suma

Por linealidad,

$$\begin{aligned} \hat A(|i\rangle+|j\rangle) &=\hat A|i\rangle+\hat A|j\rangle\\ &=a_i|i\rangle+a_j|j\rangle. \end{aligned}$$

Para que la suma sea un autoket debe existir un autovalor $\lambda$ tal que

$$\hat A(|i\rangle+|j\rangle) =\lambda(|i\rangle+|j\rangle).$$

Entonces,

$$(a_i-\lambda)|i\rangle +(a_j-\lambda)|j\rangle=0.$$

### Paso 2. Estudiar la condición

Si los dos kets son linealmente independientes, sus coeficientes deben anularse:

$$a_i-\lambda=0, \qquad a_j-\lambda=0.$$

Por tanto,

$$a_i=a_j=\lambda.$$

### Resultado

$$\boxed{ |i\rangle+|j\rangle \text{ es autoket si ambos tienen el mismo autovalor.} }$$

La suma debe ser distinta del ket nulo.

Razón física y matemática: los autovectores asociados a un mismo autovalor forman un subespacio vectorial. Cualquier combinación lineal de sus elementos continúa perteneciendo a ese espacio propio.

Esto es especialmente importante cuando existe degeneración.

# 2. Estados físicos, observables y compatibilidad

## 2(a). ¿Cómo predecir los resultados y probabilidades de una medición?

Supongamos que el observable es $\hat A$, con ecuación de valores propios

$$\hat A|a_n\rangle=a_n|a_n\rangle.$$

El estado normalizado se escribe como

$$|\psi\rangle=\sum_n c_n|a_n\rangle.$$

### Procedimiento

1. Identificar los posibles resultados.

Son los autovalores del observable:

$$\boxed{a_n.}$$

2. Encontrar las amplitudes.

$$c_n=\langle a_n|\psi\rangle.$$

3. Calcular las probabilidades.

Aplicamos la regla de Born:

$$\boxed{P(a_n)=|c_n|^2.}$$

Si el autovalor es degenerado, se suman las probabilidades de todos los componentes asociados a él.

Por tanto, la teoría predice una distribución de probabilidades, no un resultado individual determinado.

## 2(b). ¿Qué características debe tener un operador para representar un observable físico?

Debe ser lineal y hermítico:

$$\boxed{\hat A^\dagger=\hat A.}$$

La razón es que los resultados de las mediciones físicas deben ser números reales.

La hermiticidad garantiza que:

- Los autovalores son reales.
    
- Los autovectores de autovalores distintos son ortogonales.
    
- Existe una base ortonormal completa de autovectores (en el contexto finito-dimensional del ejercicio).
    
- Los valores esperados son reales.
    

En efecto,

$$\begin{aligned} \langle A\rangle^* &=\left(\langle\psi|\hat A|\psi\rangle\right)^*\\ &=\langle\psi|\hat A^\dagger|\psi\rangle\\ &=\langle\psi|\hat A|\psi\rangle. \end{aligned}$$

Por tanto,

$$\boxed{\langle A\rangle\in\mathbb R.}$$

## 2(c). ¿Qué características debe tener un ket para representar un estado físico?

Debe pertenecer al espacio de Hilbert, ser no nulo y normalizable. Se utiliza normalmente normalizado:

$$\boxed{\langle\psi|\psi\rangle=1.}$$

¿Por qué?

Porque las probabilidades deben ser no negativas y sumar uno.

Si

$$|\psi\rangle=\sum_n c_n|a_n\rangle,$$

la normalización garantiza

$$\sum_n|c_n|^2=1.$$

Además, la fase global no tiene significado físico:

$$|\psi'\rangle=e^{i\phi}|\psi\rangle.$$

Ambos kets representan el mismo estado físico.

## 2(d). ¿Una base completa de autokets simultáneos implica que los operadores conmutan?

Se tienen dos observables $\hat A$ y $\hat B$, cuyos autokets simultáneos

$$\{|a'b'\rangle\}$$

forman una base ortonormal completa.

La pregunta es si podemos concluir que

$$[\hat A,\hat B]=0.$$

Sí.

### Demostración

Por definición de autoket simultáneo,

$$\hat A|a'b'\rangle=a'|a'b'\rangle,$$

$$\hat B|a'b'\rangle=b'|a'b'\rangle.$$

Calculamos:

$$\begin{aligned} \hat A\hat B|a'b'\rangle &=\hat A(b'|a'b'\rangle)\\ &=a'b'|a'b'\rangle. \end{aligned}$$

Análogamente,

$$\begin{aligned} \hat B\hat A|a'b'\rangle &=\hat B(a'|a'b'\rangle)\\ &=a'b'|a'b'\rangle. \end{aligned}$$

Por tanto,

$$[\hat A,\hat B]|a'b'\rangle=0$$

para cada elemento de la base.

Como la base es completa, cualquier ket puede expresarse como

$$|\psi\rangle=\sum_{a',b'}c_{a'b'}|a'b'\rangle.$$

Por linealidad,

$$\begin{aligned} [\hat A,\hat B]|\psi\rangle &=\sum_{a',b'}c_{a'b'} [\hat A,\hat B]|a'b'\rangle\\ &=0. \end{aligned}$$

Como esto se cumple para cualquier ket,

$$\boxed{[\hat A,\hat B]=0.}$$

Idea clave: si existe una base completa de autovectores simultáneos de dos operadores, necesariamente conmutan.

# 3. Autovalor y autoket de una componente arbitraria del espín

Se quiere construir

$$|\hat S\cdot\hat n;+\rangle$$

tal que

$$\hat S\cdot\hat n |\hat S\cdot\hat n;+\rangle = \frac{\hbar}{2} |\hat S\cdot\hat n;+\rangle.$$

La respuesta debe expresarse como combinación de $|+\rangle$ y $|-\rangle$.

## Conceptos necesarios

El espín puede medirse en cualquier dirección espacial.

Si $\hat n$ es un vector unitario caracterizado por los ángulos polar $\beta$ y azimutal $\alpha$, entonces

$$\hat n= \begin{pmatrix} \sin\beta\cos\alpha\\ \sin\beta\sin\alpha\\ \cos\beta \end{pmatrix}.$$

La componente del espín en esa dirección es

$$\boxed{ \hat S\cdot\hat n =S_x\sin\beta\cos\alpha +S_y\sin\beta\sin\alpha +S_z\cos\beta. }$$

El problema consiste en resolver una ecuación de valores propios.

## Paso 1. Construir la matriz del operador

Utilizando las matrices de espín:

$$\boxed{ \hat S\cdot\hat n = \frac{\hbar}{2} \begin{pmatrix} \cos\beta&\sin\beta e^{-i\alpha}\\ \sin\beta e^{i\alpha}&-\cos\beta \end{pmatrix}. }$$

## Paso 2. Proponer el ket más general

Como estamos trabajando en la base de $\hat S_z$, escribimos

$$|\psi\rangle=c_+|+\rangle+c_-|-\rangle.$$

Su representación matricial es

$$|\psi\rangle= \begin{pmatrix} c_+\\c_- \end{pmatrix}.$$

## Paso 3. Aplicar la ecuación de valores propios

Tenemos

$$\frac{\hbar}{2} \begin{pmatrix} \cos\beta&\sin\beta e^{-i\alpha}\\ \sin\beta e^{i\alpha}&-\cos\beta \end{pmatrix} \begin{pmatrix} c_+\\c_- \end{pmatrix} = \frac{\hbar}{2} \begin{pmatrix} c_+\\c_- \end{pmatrix}.$$

Cancelamos $\hbar/2$:

$$\begin{pmatrix} \cos\beta&\sin\beta e^{-i\alpha}\\ \sin\beta e^{i\alpha}&-\cos\beta \end{pmatrix} \begin{pmatrix} c_+\\c_- \end{pmatrix} = \begin{pmatrix} c_+\\c_- \end{pmatrix}.$$

Obtenemos dos ecuaciones:

$$\cos\beta\,c_+ +\sin\beta e^{-i\alpha}c_-=c_+,$$

$$\sin\beta e^{i\alpha}c_+ -\cos\beta\,c_-=c_-.$$

Reordenando la primera:

$$\sin\beta e^{-i\alpha}c_- =(1-\cos\beta)c_+.$$

Despejamos:

$$\frac{c_-}{c_+} =e^{i\alpha}\frac{1-\cos\beta}{\sin\beta}.$$

## Paso 4. Utilizar identidades trigonométricas

Recordemos:

$$1-\cos\beta=2\sin^2\frac{\beta}{2},$$

$$\sin\beta=2\sin\frac{\beta}{2}\cos\frac{\beta}{2}.$$

Por tanto,

$$\frac{1-\cos\beta}{\sin\beta} =\tan\frac{\beta}{2}.$$

Así,

$$c_-=e^{i\alpha}\tan\frac{\beta}{2}c_+.$$

## Paso 5. Normalizar

Imponemos

$$|c_+|^2+|c_-|^2=1.$$

Escogiendo una fase global conveniente, podemos tomar

$$c_+=\cos\frac{\beta}{2}.$$

Entonces,

$$c_-=e^{i\alpha}\sin\frac{\beta}{2}.$$

### Resultado

$$\boxed{ |\hat S\cdot\hat n;+\rangle = \cos\frac{\beta}{2}|+\rangle + e^{i\alpha}\sin\frac{\beta}{2}|-\rangle. }$$

Es equivalente a la expresión proporcionada en el enunciado.

Interpretación: el estado propio de una componente arbitraria del espín es una superposición de los estados propios de $\hat S_z$. Los coeficientes dependen de la orientación de la dirección de medición.

# 4. Hamiltoniano de dos estados

## 4(a). Autovalores y autoestados de energía

Se tiene

$$\begin{aligned} \hat H={}&H_{11}|1\rangle\langle1| +H_{22}|2\rangle\langle2|\\ &+H_{12}\left( |1\rangle\langle2| +|2\rangle\langle1| \right). \end{aligned}$$

Los coeficientes son reales y tienen unidades de energía.

### Conceptos necesarios

El Hamiltoniano es el operador asociado a la energía del sistema. Sus autovalores son las energías posibles y sus autokets son los estados propios de energía.

En la base ortonormal $\{|1\rangle,|2\rangle\}$, el Hamiltoniano se representa como

$$\boxed{ H= \begin{pmatrix} H_{11}&H_{12}\\ H_{12}&H_{22} \end{pmatrix}. }$$

El problema consiste en diagonalizar esta matriz.

En lugar de hacerlo directamente, utilizaremos la relación del ejercicio 3.

### Paso 1. Separar la parte proporcional a la identidad

Definimos

$$H_0=\frac{H_{11}+H_{22}}{2},$$

$$\Delta=\frac{H_{11}-H_{22}}{2}.$$

Entonces,

$$H= H_0 \begin{pmatrix} 1&0\\0&1 \end{pmatrix} + \begin{pmatrix} \Delta&H_{12}\\ H_{12}&-\Delta \end{pmatrix}.$$

La primera matriz solamente desplaza los autovalores, sin modificar los autovectores.

### Paso 2. Relacionar el Hamiltoniano con el operador de espín

Definimos

$$R=\sqrt{\Delta^2+H_{12}^2}.$$

Para $R>0$, podemos elegir los ángulos $\beta,\alpha$ de manera que

$$\cos\beta=\frac{\Delta}{R},$$

$$\sin\beta=\frac{|H_{12}|}{R}.$$

Tomamos

$$\alpha= \begin{cases} 0,&H_{12}>0,\\ \pi,&H_{12}<0. \end{cases}$$

Cuando $H_{12}=0$, podemos tomar $\alpha=0$.

De esta manera,

$$\begin{pmatrix} \Delta&H_{12}\\ H_{12}&-\Delta \end{pmatrix} = \frac{2R}{\hbar}\hat S\cdot\hat n,$$

identificando

$$|+\rangle\longleftrightarrow|1\rangle, \qquad |-\rangle\longleftrightarrow|2\rangle.$$

Por consiguiente,

$$\boxed{ \hat H=H_0\hat I+\frac{2R}{\hbar}\hat S\cdot\hat n. }$$

### Paso 3. Obtener los autovalores

Sabemos que

$$\hat S\cdot\hat n|\hat n;\pm\rangle =\pm\frac{\hbar}{2}|\hat n;\pm\rangle.$$

Aplicamos el Hamiltoniano:

$$\begin{aligned} \hat H|\hat n;\pm\rangle &=\left(H_0\hat I+\frac{2R}{\hbar}\hat S\cdot\hat n\right) |\hat n;\pm\rangle\\ &=(H_0\pm R)|\hat n;\pm\rangle. \end{aligned}$$

Por tanto, las energías son

$$\boxed{ E_\pm= \frac{H_{11}+H_{22}}{2} \pm \sqrt{ \left(\frac{H_{11}-H_{22}}{2}\right)^2 +H_{12}^2 }. }$$

### Paso 4. Obtener los autoestados de energía

Utilizando el resultado del ejercicio 3:

$$|\hat n;+\rangle = \cos\frac{\beta}{2}|1\rangle + e^{i\alpha}\sin\frac{\beta}{2}|2\rangle.$$

Entonces,

$$\boxed{ |E_+\rangle = \cos\frac{\beta}{2}|1\rangle + e^{i\alpha}\sin\frac{\beta}{2}|2\rangle. }$$

El autoket ortonormal correspondiente al autovalor negativo de $\hat S\cdot\hat n$ es

$$|\hat n;-\rangle = -e^{-i\alpha}\sin\frac{\beta}{2}|1\rangle + \cos\frac{\beta}{2}|2\rangle.$$

Por tanto,

$$\boxed{ |E_-\rangle = -e^{-i\alpha}\sin\frac{\beta}{2}|1\rangle + \cos\frac{\beta}{2}|2\rangle. }$$

### Paso 5. Verificar el caso $H_{12}=0$

Este requisito es importante porque permite comprobar que los resultados tienen sentido físico.

Si $H_{12}=0$, el Hamiltoniano se reduce a

$$\hat H= H_{11}|1\rangle\langle1| + H_{22}|2\rangle\langle2|.$$

Es decir, ya es diagonal en la base original.

Consideremos dos situaciones:

Caso 1: $H_{11}>H_{22}$.

Tenemos $\beta=0$, por lo que

$$|E_+\rangle=|1\rangle, \qquad |E_-\rangle=|2\rangle.$$

Y

$$E_+=H_{11}, \qquad E_-=H_{22}.$$

Caso 2: $H_{11}<H_{22}$.

Tenemos $\beta=\pi$, por lo que, salvo fases globales,

$$|E_+\rangle=|2\rangle, \qquad |E_-\rangle=|1\rangle.$$

Y

$$E_+=H_{22}, \qquad E_-=H_{11}.$$

Ambos casos recuperan correctamente los estados originales.

Caso degenerado: si $H_{11}=H_{22}$ y $H_{12}=0$, entonces

$$\hat H=H_{11}\hat I.$$

Los dos estados tienen la misma energía y cualquier base ortonormal del espacio es una base propia válida.

## 4(b). ¿Por qué el Hamiltoniano con un solo término cruzado es ilegal?

Se propone

$$\hat H= H_{11}|1\rangle\langle1| + H_{22}|2\rangle\langle2| + H_{12}|1\rangle\langle2|.$$

### Paso 1. Representar matricialmente

En la base $\{|1\rangle,|2\rangle\}$:

$$\boxed{ H= \begin{pmatrix} H_{11}&H_{12}\\ 0&H_{22} \end{pmatrix}. }$$

### Paso 2. Comprobar la hermiticidad

Su adjunto es

$$H^\dagger= \begin{pmatrix} H_{11}&0\\ H_{12}&H_{22} \end{pmatrix},$$

porque los coeficientes son reales.

Para que sea hermítico se requiere

$$H^\dagger=H.$$

Esto no se cumple si

$$H_{12}\neq0.$$

### Paso 3. Identificar el principio violado

El Hamiltoniano representa un observable físico: la energía. Por tanto, debe ser hermítico.

Además, el Hamiltoniano genera la evolución temporal:

$$i\hbar\frac{d}{dt}|\psi(t)\rangle =\hat H|\psi(t)\rangle.$$

Para que se conserve la probabilidad total, la evolución debe ser unitaria.

En efecto,

$$\frac{d}{dt}\langle\psi|\psi\rangle = \frac{i}{\hbar} \langle\psi|(\hat H^\dagger-\hat H)|\psi\rangle.$$

Si el Hamiltoniano no es hermítico, esta derivada no tiene por qué ser cero.

Por tanto:

$$\boxed{ \text{Se viola la conservación de la probabilidad en general.} }$$

La condición fundamental incumplida es la hermiticidad del Hamiltoniano.

Observación importante: incluso si $H_{11}$ y $H_{22}$ son reales y el operador tiene autovalores reales, eso no lo convierte en un Hamiltoniano físico válido. La hermiticidad es una condición más exigente que la realidad del espectro.

# 5. Mediciones sucesivas de Stern-Gerlach

Este ejercicio utiliza una de las aplicaciones más importantes de la mecánica cuántica: la proyección del estado después de cada medición.

Se tiene una secuencia de tres aparatos:

1. El primero acepta $S_z=+\hbar/2$.
    
2. El segundo acepta $S_n=+\hbar/2$.
    
3. El tercero acepta $S_z=-\hbar/2$.
    

Nos dicen que el haz que sobrevive a la primera medición se normaliza a la unidad.

## Conceptos necesarios

La dirección del segundo aparato se caracteriza por un ángulo $\beta$ respecto al eje $z$, dentro del plano $xz$.

Por tanto,

$$\hat n=\sin\beta\,\hat x+\cos\beta\,\hat z.$$

Del ejercicio 3 conocemos el estado propio de espín positivo en esa dirección:

$$\boxed{ |n;+\rangle = \cos\frac{\beta}{2}|+\rangle + \sin\frac{\beta}{2}|-\rangle. }$$

En esta expresión hemos tomado $\alpha=0$, como corresponde a la dirección en el plano $xz$ con componente $x$ positiva.

La intensidad del haz después de una medición es la intensidad anterior multiplicada por la probabilidad de que el sistema supere el filtro.

## 5(i). Calcular la intensidad final

Hay una errata en el enunciado

El tercer aparato acepta $S_z=-\hbar/2$ y rechaza $S_z=+\hbar/2$, pero la pregunta solicita la intensidad del haz final $S_z=+\hbar/2$.

Conforme a las instrucciones de los tres aparatos, el resultado final debe tener $S_z=-\hbar/2$. Resolveremos primero esa secuencia y después indicaremos la respuesta literal.

### Paso 1. Estado después del primer aparato

El primer aparato selecciona

$$S_z=+\frac{\hbar}{2}.$$

Como el haz superviviente se normaliza a la unidad:

$$\boxed{|\psi_1\rangle=|+\rangle.}$$

### Paso 2. Probabilidad de superar el segundo aparato

El segundo aparato selecciona el estado

$$|n;+\rangle = \cos\frac{\beta}{2}|+\rangle + \sin\frac{\beta}{2}|-\rangle.$$

La probabilidad de pasar el segundo aparato es

$$P_2=|\langle n;+|+\rangle|^2.$$

Calculamos la amplitud:

$$\begin{aligned} \langle n;+|+\rangle &= \left( \cos\frac{\beta}{2}\langle+| + \sin\frac{\beta}{2}\langle-| \right)|+\rangle\\ &=\cos\frac{\beta}{2}. \end{aligned}$$

Por tanto,

$$\boxed{P_2=\cos^2\frac{\beta}{2}.}$$

El estado después de este aparato, normalizado, es

$$|\psi_2\rangle=|n;+\rangle.$$

### Paso 3. Probabilidad de superar el tercer aparato

El tercer aparato acepta

$$S_z=-\frac{\hbar}{2},$$

cuyo autoket es $|-\rangle$.

La probabilidad de pasar el tercer aparato, dado que se superó el segundo, es

$$P_3=|\langle-|n;+\rangle|^2.$$

Calculamos:

$$\langle-|n;+\rangle =\sin\frac{\beta}{2}.$$

Por tanto,

$$\boxed{P_3=\sin^2\frac{\beta}{2}.}$$

### Paso 4. Calcular la intensidad total

La intensidad final es el producto de las probabilidades de superar ambos filtros, tomando como intensidad inicial la unidad después del primer aparato:

$$I_f=P_2P_3.$$

Entonces,

$$I_f= \cos^2\frac{\beta}{2} \sin^2\frac{\beta}{2}.$$

Utilizando

$$\sin\beta=2\sin\frac{\beta}{2}\cos\frac{\beta}{2},$$

obtenemos

$$\boxed{ I_f=\frac14\sin^2\beta. }$$

Esta es la intensidad relativa del haz final con

$$S_z=-\frac{\hbar}{2}.$$

¿Y si interpretamos literalmente la pregunta?

Si realmente preguntan por la intensidad final de los átomos con

$$S_z=+\frac{\hbar}{2},$$

la respuesta es

$$\boxed{I(S_z=+\hbar/2)=0,}$$

porque el tercer aparato rechaza todos esos átomos.

La fórmula no nula anterior corresponde a la interpretación coherente con el resto del enunciado: intensidad final de $S_z=-\hbar/2$.

## 5(ii). ¿Cómo orientar el segundo aparato para maximizar la intensidad final?

Ya encontramos que

$$I_f(\beta)=\frac14\sin^2\beta.$$

Queremos maximizar esta expresión.

Sabemos que

$$0\leq\sin^2\beta\leq1.$$

El máximo se alcanza cuando

$$\sin^2\beta=1.$$

Por tanto,

$$\boxed{\beta=\frac{\pi}{2}.}$$

Esto significa que la dirección del segundo aparato debe ser perpendicular al eje $z$.

Como se encuentra en el plano $xz$, debemos orientarlo en la dirección del eje $x$ (con la convención de componente $x$ positiva).

Para esta orientación:

$$|n;+\rangle = \frac1{\sqrt2}(|+\rangle+|-\rangle).$$

La probabilidad de superar el segundo aparato es

$$P_2=\frac12.$$

La probabilidad de superar el tercero, después de superar el segundo, también es

$$P_3=\frac12.$$

Por tanto,

$$\boxed{I_{\max}=\frac12\cdot\frac12=\frac14.}$$

Resultado final

$$\boxed{ \beta=90^\circ,\qquad I_{\max}=\frac14. }$$

Interpretación física: el segundo aparato debe estar orientado a mitad de camino entre las dos direcciones seleccionadas por el primero y el tercero. Así se consigue un equilibrio óptimo entre la probabilidad de superar el segundo filtro y la de superar el tercero.

# 6. Síntesis de los conceptos que debes dominar

|Tema|Qué debes comprender|
|---|---|
|Producto exterior|Su matriz se construye multiplicando una columna por una fila conjugada.|
|Ortonormalidad|Permite simplificar productos de operadores construidos con kets y bras.|
|Operadores de espín|Las componentes satisfacen relaciones de conmutación y anticonmutación.|
|Degeneración|Las combinaciones lineales de autovectores con el mismo autovalor siguen siendo autovectores.|
|Hermiticidad|Es la condición fundamental para que un operador represente un observable físico.|
|Estados cuánticos|Deben ser elementos normalizables del espacio de Hilbert.|
|Compatibilidad|Una base completa de autovectores simultáneos implica que los operadores conmutan.|
|Espín en dirección arbitraria|Se obtiene resolviendo una ecuación matricial de valores propios.|
|Hamiltoniano|Sus autovalores y autovectores representan energías y estados propios de energía.|
|Evolución temporal|La hermiticidad del Hamiltoniano garantiza evolución unitaria y conservación de probabilidad.|
|Stern-Gerlach|Cada aparato proyecta el estado y modifica las probabilidades de las mediciones posteriores.|

## 7. Las conexiones más importantes entre los ejercicios

Hay cuatro conexiones que conviene identificar:

1. Ejercicio 1 y ejercicio 3: el álgebra de los operadores de espín permite resolver ecuaciones de valores propios sin utilizar rotaciones. Esa misma estructura reaparece al estudiar el espín en una dirección arbitraria.

2. Ejercicio 2 y ejercicio 4: la hermiticidad no es una condición matemática decorativa. Garantiza que los operadores que representan observables tengan las propiedades físicas requeridas, y en particular permite construir Hamiltonianos que generan evolución unitaria.

3. Ejercicio 3 y ejercicio 4: el Hamiltoniano de dos estados puede expresarse como una constante más un operador de espín proyectado sobre una dirección particular. Esto permite aprovechar directamente los autokets obtenidos en el ejercicio 3.

4. Ejercicio 3 y ejercicio 5: conocer los autokets del espín en una dirección arbitraria permite calcular las probabilidades de transmisión entre analizadores Stern-Gerlach orientados en direcciones diferentes.

La idea transversal del parcial es esta: resolver una ecuación de valores propios permite identificar los estados que selecciona una medición; expresar un estado arbitrario en esa base permite calcular sus probabilidades y valores esperados.

Para continuar el estudio, puedes programar un ejercicio breve de repaso sobre espín, productos exteriores y mediciones sucesivas para mañana.

🧠Ejercicio de repaso de cuántica mañanaToca para configurar