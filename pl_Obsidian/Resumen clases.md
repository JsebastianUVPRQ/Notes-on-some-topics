# Fundamentos de Física — Clases 001–006

> [!abstract] Idea general del bloque
> Estas seis clases construyen progresivamente el formalismo básico de la mecánica cuántica.
>
> La secuencia conceptual es:
>
> **Stern–Gerlach → espín → superposición → números complejos → kets y bras → producto interno → espacio de Hilbert → operadores → observables → autovalores/autovectores → medición → probabilidades → valor esperado → representación matricial.**

---

# Clase 001 — 08/09/2026

## 1. Los cinco pilares de la mecánica cuántica

La clase comienza identificando cinco características fundamentales:

1. **Linealidad de la mecánica cuántica.**
2. **Números complejos.**
3. **Pérdida del determinismo → probabilidad.**
4. **Superposición.**
5. **Entrelazamiento → información.**

En estas primeras clases se empieza principalmente por los tres elementos que permiten construir el formalismo:

$$
\boxed{
\text{linealidad}
+
\text{números complejos}
+
\text{superposición}
}
$$

La interpretación probabilística aparece asociada a la medición.

---

## 2. ¿Por qué empezar con Stern–Gerlach?

El experimento de **Stern–Gerlach** proporciona una manera física de observar directamente características que no tienen una explicación clásica sencilla.

La idea básica es hacer pasar partículas por un campo magnético no uniforme.

El montaje conceptual es:

$$
\text{fuente}
\rightarrow
\text{colimador}
\rightarrow
\text{campo magnético no uniforme}
\rightarrow
\text{detector}
$$

El experimento permite estudiar el momento magnético asociado al espín.

---

## 3. Momento magnético y espín

Se introduce el momento magnético $\vec\mu$ y el espín $\vec S$.

La relación utilizada en las notas es:

$$
\vec{\mu}
=
-\frac{|e|}{m_ec}\vec S
$$

donde:

* $\vec\mu$ es el momento magnético.
* $\vec S$ es el momento angular de espín.
* $e$ es la carga del electrón.
* $m_e$ es la masa del electrón.
* $c$ es la velocidad de la luz.

La interacción con el campo magnético $\vec B$ produce una fuerza cuando el campo no es uniforme.

Se utiliza:

$$
F_z
=
\frac{\partial}{\partial z}
(\vec\mu\cdot\vec B)
$$

y, para la configuración considerada:

$$
F_z
=
\mu_z
\frac{\partial B_z}{\partial z}
$$

Por eso el campo magnético debe tener un **gradiente**.

---

## 4. ¿Qué se esperaría clásicamente?

Si imagináramos un momento magnético clásico orientado arbitrariamente, su componente $z$ podría tomar continuamente diferentes valores.

Se tendría conceptualmente:

$$
-\mu\leq\mu_z\leq\mu
$$

Por tanto, esperaríamos una distribución continua sobre el detector.

Pero eso no es lo que ocurre.

---

## 5. Resultado del experimento de Stern–Gerlach

Experimentalmente aparecen **dos haces separados**.

Esto indica que la componente del espín que se está midiendo no puede tomar cualquier valor continuo.

Para un sistema de espín $1/2$:

$$
S_z=\pm\frac{\hbar}{2}
$$

donde:

$$
\hbar=\frac{h}{2\pi}
$$

y aproximadamente:

$$
\hbar\approx1.054\times10^{-34}\,\mathrm{J\,s}
$$

La medición de $S_z$ tiene entonces dos posibles resultados:

$$
+\frac{\hbar}{2}
$$

y

$$
-\frac{\hbar}{2}
$$

---

## 6. El espín no es una rotación clásica

Una idea importante de la clase es que el **espín es un grado de libertad cuántico intrínseco**.

No debemos imaginarlo simplemente como una pequeña esfera que gira físicamente sobre sí misma.

El experimento muestra que el sistema posee una propiedad angular cuantizada que responde al campo magnético.

---

## 7. Diferentes componentes del espín

Podemos estudiar diferentes componentes:

$$
S_x,\qquad S_y,\qquad S_z
$$

Cada componente puede medirse mediante una configuración apropiada del experimento de Stern–Gerlach.

Aquí aparece una idea fundamental:

> Las mediciones asociadas a diferentes componentes del espín no se comportan como mediciones simultáneamente determinadas de una variable clásica.

Por ejemplo, podemos hacer una secuencia:

$$
S_z\rightarrow S_x
$$

y observar qué ocurre.

---

## 8. Secuencias de Stern–Gerlach

Supongamos que seleccionamos primero un estado asociado a $S_z$ y después medimos $S_x$.

Después de la segunda medición aparecen los dos resultados asociados a $S_x$.

Si posteriormente volvemos a medir $S_z$, vuelven a aparecer ambos resultados de $S_z$.

Esto conduce a una característica fundamental:

$$
\boxed{
\text{medir una componente puede modificar la información disponible sobre otra}
}
$$

Este comportamiento motiva la introducción del formalismo de estados y superposición.

---

## 9. Estados de espín

Se comienza a utilizar una notación para representar los estados.

Por ejemplo:

$$
|+z\rangle
$$

representa el estado correspondiente al resultado positivo de $S_z$.

Análogamente:

$$
|-z\rangle
$$

representa el estado correspondiente al resultado negativo.

También podemos utilizar:

$$
|+x\rangle,\qquad|-x\rangle
$$

para los estados asociados a $S_x$.

---

# Clase 002 — 11/09/2026

## 1. Continuación de Stern–Gerlach

La segunda clase desarrolla la estructura matemática que necesitamos para describir los estados observados en Stern–Gerlach.

El punto de partida es que un estado preparado como $|+z\rangle$ puede dar resultados diferentes si posteriormente medimos otra componente.

Esto conduce directamente a la **superposición**.

---

## #2. Principio de superposición

Un estado cuántico puede escribirse como combinación lineal de otros estados:

$$
|\psi\rangle
=
A_+|+z\rangle
+
A_-|-z\rangle
$$

Los coeficientes $A_+$ y $A_-$ son, en general, números complejos.

Esto es fundamental.

En física clásica podemos pensar en un sistema que simplemente posee una configuración determinada.

En mecánica cuántica, en cambio, un estado puede ser una combinación lineal de estados posibles de un observable.

---

## #3. Números complejos

Los coeficientes de la superposición pertenecen a los números complejos.

Un número complejo puede escribirse como:

$$
C=|C|e^{i\theta}
$$

donde:

* $|C|$ es el módulo.
* $\theta$ es la fase.

Esta estructura será fundamental porque la probabilidad dependerá del módulo al cuadrado, mientras que las fases relativas pueden producir efectos físicos.

---

## 4. Estado general de espín $1/2$

Para un sistema de espín $1/2$:

$$
|\psi\rangle
=
A_+|+z\rangle
+
A_-|-z\rangle
$$

Si el estado está normalizado:

$$
|A_+|^2+|A_-|^2=1
$$

Los números $|A_+|^2$ y $|A_-|^2$ están relacionados con las probabilidades de los resultados de una medición de $S_z$.

---

## #5. Fase global y fase relativa

Consideremos:

$$
|\psi\rangle
=
A_+|+z\rangle
+
A_-|-z\rangle
$$

Podemos escribir:

$$
A_+=|A_+|e^{i\theta_+}
$$

y

$$
A_-=|A_-|e^{i\theta_-}
$$

Lo importante para muchas mediciones no es cada fase por separado, sino la diferencia:

$$
\theta_--\theta_+
$$

Esta es la **fase relativa**.

Una fase global multiplicando todo el estado no cambia las probabilidades.

En cambio, una fase relativa puede modificar los resultados de otras mediciones.

---

## #6. Notación de Dirac

Se introduce la notación de Dirac.

Un estado se representa mediante un **ket**:

$$
|\psi\rangle
$$

Al objeto dual correspondiente se le llama **bra**:

$$
\langle\psi|
$$

El producto entre un bra y un ket produce un número:

$$
\langle\phi|\psi\rangle
$$

Este objeto es el **producto interno**.

---

## 7. Espacio de Hilbert
estados físicos se representan mediante vectores de un espacio de Hilbert.

Podemos escribir:

$$
|\psi\rangle\in\mathcal H
$$

El espacio dual contiene los bras:

$$
\langle\psi|\in\mathcal H^*
$$

Esta estructura matemática permite hablar de:

* normas,
* ortogonalidad,
* bases,
* proyecciones,
* amplitudes de probabilidad.

---

## 8. Base de estados

Si tenemos una base ${|i\rangle}$, cualquier estado puede escribirse como:

$$
|\psi\rangle
=
\sum_i A_i|i\rangle
$$

Los coeficientes se obtienen mediante el producto interno cuando la base es ortonormal:

$$
A_i=\langle i|\psi\rangle
$$

Esta expresión será una de las herramientas fundamentales de todo el curso.

---

## 9. Normalización

Un estado físico debe estar normalizado:

$$
\langle\psi|\psi\rangle=1
$$

Si:

$$
|\psi\rangle
=
\sum_iA_i|i\rangle
$$

y la base es ortonormal, entonces:

$$
\sum_i|A_i|^2=1
$$

Esto garantiza que las probabilidades sumen uno.

---

# Clase 003 — 15/09/2026

## 1. Objetivo de la clase

Esta clase formaliza matemáticamente las ideas introducidas mediante Stern–Gerlach.

Los conceptos principales son:

* superposición,
* kets,
* bras,
* producto interno,
* norma,
* ortonormalidad,
* independencia lineal,
* amplitudes de probabilidad,
* fases relativas,
* observables,
* espín,
* relación entre Stern–Gerlach y otros sistemas de dos niveles.

---

## 2. Ejemplo de superposición

Se considera un estado como:

$$
|S_x^+\rangle
=
\frac{1}{\sqrt2}
|S_z^+\rangle
+
\frac{1}{\sqrt2}
|S_z^-\rangle
$$

Este ejemplo muestra que un estado que tiene un valor bien definido para una componente puede ser una superposición respecto de otra base.

En particular:

$$
|+x\rangle
=
\frac{1}{\sqrt2}
\left(
|+z\rangle+|-z\rangle
\right)
$$

---

## 3. Estado con coeficientes complejos

Se utiliza un ejemplo general:

$$
|\alpha\rangle
=
(2+i)|a_1\rangle
+
(5-6i)|a_2\rangle
+
3|a_3\rangle
$$

La finalidad es mostrar que los coeficientes de una superposición no tienen por qué ser reales.

Pueden ser elementos de $\mathbb C$.

---

## 4. Espacio de kets

El conjunto de estados se representa mediante un espacio vectorial.

Podemos escribir:

$$
|\alpha\rangle\in\mathcal F
$$

Al correspondiente bra:

$$
\langle\alpha|\in\mathcal F^*
$$

El producto interno:

$$
\langle\beta|\alpha\rangle
$$

es un número complejo en general.

---

## 5. Propiedades del producto interno

### Linealidad

El producto interno respeta la estructura lineal del espacio.

Por ejemplo:

$$
\langle\phi|(\alpha+\beta)\rangle
=
\langle\phi|\alpha\rangle
+
\langle\phi|\beta\rangle
$$

y:

$$
\langle\phi|c|\psi\rangle
=
c\langle\phi|\psi\rangle
$$

teniendo en cuenta la convención de conjugación correspondiente al bra.

---

### Conjugación compleja

Se tiene:

$$
\langle\phi|\psi\rangle
=
\langle\psi|\phi\rangle^*
$$

Esta propiedad es fundamental para trabajar correctamente con coeficientes complejos.

---

### Positividad

Para cualquier estado:

$$
\langle\psi|\psi\rangle\geq0
$$

y:

$$
\langle\psi|\psi\rangle=0
\iff
|\psi\rangle=0
$$

---

## 6. Norma

La norma de un estado se define como:

$$
\|\psi\|
=
\sqrt{\langle\psi|\psi\rangle}
$$

Un estado normalizado cumple:

$$
\|\psi\|=1
$$

o equivalentemente:

$$
\langle\psi|\psi\rangle=1
$$

---

## 7. Ortonormalidad

Una base ${|a_i\rangle}$ es ortonormal si:

$$
\langle a_i|a_j\rangle
=
\delta_{ij}
$$

Esto significa:

$$
\langle a_i|a_i\rangle=1
$$

y para $i\neq j$:

$$
\langle a_i|a_j\rangle=0
$$

La ortonormalidad permite extraer fácilmente los coeficientes de una superposición.

---

## 8. Independencia lineal

Un conjunto de estados es linealmente independiente si:

$$
\sum_i c_i|\psi_i\rangle=0
$$

implica:

$$
c_i=0
$$

para todos los $i$.

Esto permite hablar de bases y expansión de estados.

---

## 9. Amplitudes de probabilidad

Si:

$$
|\psi\rangle
=
\sum_iA_i|a_i\rangle
$$

entonces, para una base ortonormal:

$$
A_i=\langle a_i|\psi\rangle
$$

El coeficiente $A_i$ es una **amplitud**.

La probabilidad asociada será:

$$
P_i=|A_i|^2
$$

Por tanto:

$$
P_i
=
|\langle a_i|\psi\rangle|^2
$$

Esta relación conecta el formalismo abstracto con la interpretación experimental.

---

## 10. Fase relativa

Consideremos:

$$
|\psi\rangle
=
A_1|a_1\rangle
+
A_2|a_2\rangle
$$

Podemos escribir:

$$
A_1=|A_1|e^{i\theta_1}
$$

y:

$$
A_2=|A_2|e^{i\theta_2}
$$

La fase relativa es:

$$
\Delta\theta=\theta_2-\theta_1
$$

Esta fase puede no aparecer en las probabilidades de una medición particular, pero puede hacerse observable utilizando otra elección de base.

Esta será precisamente la idea del ejercicio de fase relativa.

---

# Clase 004 — 18/09/2026

# 1. ¿Por qué introducir operadores?

Hasta ahora hemos hablado de estados y de mediciones.

Pero necesitamos una herramienta matemática que represente las cantidades físicas que queremos medir.

Esa herramienta es el **operador**.

Un operador puede transformar un estado en otro estado:

$$
\hat A:\mathcal F\rightarrow\mathcal F
$$

---

# 2. Operadores lineales

Un operador $\hat A$ es lineal si:

$$
\hat A
\left(
|\psi\rangle+|\phi\rangle
\right)
=
\hat A|\psi\rangle
+
\hat A|\phi\rangle
$$

y:

$$
\hat A(c|\psi\rangle)
=
c\hat A|\psi\rangle
$$

Por tanto:

$$
\hat A
\left(
c_1|\psi_1\rangle+c_2|\psi_2\rangle
\right)
=
c_1\hat A|\psi_1\rangle
+
c_2\hat A|\psi_2\rangle
$$

La linealidad es fundamental porque mantiene la estructura de superposición.

---

# 3. Operador identidad

El operador identidad no cambia el estado:

$$
\hat I|\psi\rangle=|\psi\rangle
$$

Es el equivalente, en el espacio de estados, al número $1$ en la multiplicación ordinaria.

---

# 4. Operador nulo

El operador nulo transforma cualquier estado en el vector cero:

$$
\hat 0|\psi\rangle=0
$$

---

# 5. Producto de operadores

Podemos aplicar primero un operador y después otro:

$$
\hat A\hat B|\psi\rangle
=
\hat A
\left(
\hat B|\psi\rangle
\right)
$$

Esto representa una composición de operaciones.

Una propiedad fundamental es que, en general:

$$
\hat A\hat B\neq\hat B\hat A
$$

Es decir, los operadores **no necesariamente conmutan**.

---

# 6. Conmutador

Para cuantificar esta diferencia se define:

$$
[\hat A,\hat B]
=
\hat A\hat B-\hat B\hat A
$$

Si:

$$
[\hat A,\hat B]=0
$$

entonces los operadores conmutan.

Si:

$$
[\hat A,\hat B]\neq0
$$

entonces el orden de aplicación importa.

Esta estructura está relacionada con la idea experimental de que determinadas mediciones cuánticas no se comportan como variables clásicas independientes.

---

# 7. Operador adjunto

A cada operador $\hat A$ podemos asociarle un operador adjunto:

$$
\hat A^\dagger
$$

Su definición se expresa mediante el producto interno:

$$
\langle\phi|\hat A|\psi\rangle
=
\langle\hat A^\dagger\phi|\psi\rangle
$$

Esta definición será importante para identificar operadores físicamente relevantes.

---

# 8. Operadores hermíticos

Un operador es hermítico si:

$$
\boxed{
\hat A=\hat A^\dagger
}
$$

Los operadores hermíticos son especialmente importantes porque serán los operadores asociados a los **observables físicos**.

---

# 9. Observables

La conexión fundamental que comienza a establecerse es:

$$
\boxed{
\text{observable}
\longleftrightarrow
\text{operador hermítico}
}
$$

Por ejemplo, la energía estará asociada al Hamiltoniano $\hat H$.

Las componentes del espín estarán asociadas a operadores correspondientes:

$$
\hat S_x,\qquad
\hat S_y,\qquad
\hat S_z
$$

---

# 10. Producto de un bra, operador y ket

Una expresión fundamental es:

$$
\langle\phi|\hat A|\psi\rangle
$$

El operador actúa sobre el ket:

$$
\hat A|\psi\rangle
$$

y luego se toma el producto interno con $\langle\phi|$.

Esta estructura aparecerá constantemente en los cálculos de valores esperados y elementos de matriz.

---

# Clase 005 — 22/09/2026

# 1. Observables y operadores hermíticos

La clase continúa desarrollando la relación:

$$
\boxed{
\text{observable}
\longleftrightarrow
\text{operador hermítico}
}
$$

Un observable se representa mediante un operador $\hat A$ que satisface:

$$
\hat A=\hat A^\dagger
$$

---

# 2. ¿Qué significa medir un observable?

La pregunta matemática fundamental es:

> ¿Qué estados producen un resultado definido cuando medimos un observable?

La respuesta se obtiene mediante la ecuación de autovalores.

---

# 3. Autovalores y autovectores

Un estado $|\alpha\rangle$ es un autestado de $\hat A$ si:

$$
\hat A|\alpha\rangle
=
a|\alpha\rangle
$$

donde $a$ es el autovalor.

La interpretación física es:

* $|\alpha\rangle$ → estado propio.
* $a$ → posible resultado de la medición.

Por tanto:

$$
\boxed{
\text{posibles resultados de medir }\hat A
=
\text{autovalores de }\hat A
}
$$

---

# 4. ¿Por qué son importantes los operadores hermíticos?

Para un observable físico, los autovalores deben ser reales.

Si:

$$
\hat A|\alpha\rangle=a|\alpha\rangle
$$

y $\hat A$ es hermítico:

$$
\hat A=\hat A^\dagger
$$

entonces se demuestra que:

$$
a=a^*
$$

Por tanto:

$$
\boxed{a\in\mathbb R}
$$

Esto es necesario porque un resultado de medición física debe ser un número real.

---

# 5. Ortogonalidad de autovectores

Si $\hat A$ es hermítico y dos estados propios tienen autovalores diferentes:

$$
\hat A|a\rangle=a|a\rangle
$$

y:

$$
\hat A|b\rangle=b|b\rangle
$$

con:

$$
a\neq b
$$

entonces:

$$
\boxed{
\langle a|b\rangle=0
}
$$

Es decir, los estados propios correspondientes a autovalores distintos son ortogonales.

---

# 6. Base de autestados

Los autestados de un observable pueden formar una base.

Si ${|a_i\rangle}$ es una base ortonormal de autestados:

$$
\hat A|a_i\rangle
=
a_i|a_i\rangle
$$

y:

$$
\langle a_i|a_j\rangle
=
\delta_{ij}
$$

Entonces cualquier estado puede escribirse como:

$$
|\psi\rangle
=
\sum_i c_i|a_i\rangle
$$

---

# 7. Relación de completitud

Para una base completa de estados:

$$
\boxed{
\sum_i|a_i\rangle\langle a_i|
=
\hat I
}
$$

Esta expresión significa que podemos reconstruir cualquier estado utilizando todos los elementos de la base.

Aplicándola sobre $|\psi\rangle$:

$$
|\psi\rangle
=
\sum_i|a_i\rangle\langle a_i|\psi\rangle
$$

Definimos:

$$
c_i=\langle a_i|\psi\rangle
$$

y recuperamos:

$$
|\psi\rangle
=
\sum_i c_i|a_i\rangle
$$

---

# 8. Proyectores

A cada estado $|a\rangle$ podemos asociarle un operador proyector:

$$
\hat P_a
=
|a\rangle\langle a|
$$

Su función es seleccionar la componente del estado asociada a $|a\rangle$.

Aplicado a un estado $|\psi\rangle$:

$$
\hat P_a|\psi\rangle
=
|a\rangle\langle a|\psi\rangle
$$

El número:

$$
\langle a|\psi\rangle
$$

es la amplitud asociada a esa componente.

---

# 9. Conexión con la medición

Si:

$$
|\psi\rangle
=
\sum_i c_i|a_i\rangle
$$

y ${|a_i\rangle}$ son los autestados del observable $\hat A$, entonces una medición de $\hat A$ puede producir cualquiera de los autovalores $a_i$.

La probabilidad correspondiente será:

$$
P(a_i)
=
|c_i|^2
$$

o:

$$
\boxed{
P(a_i)
=
|\langle a_i|\psi\rangle|^2
}
$$

Aquí se conecta toda la construcción matemática anterior con la interpretación física.

---

# Clase 006 — 25/09/2026

# 1. Objetivo de la clase

La sexta clase reúne las ideas anteriores y comienza a utilizarlas de forma sistemática.

La estructura fundamental es:

$$
|\psi\rangle
\rightarrow
\text{expansión en autestados}
\rightarrow
\text{amplitudes}
\rightarrow
\text{probabilidades}
\rightarrow
\text{valor esperado}
$$

---

# 2. Expansión de un estado

Si ${|a_i\rangle}$ es una base ortonormal de autestados de un observable $\hat A$:

$$
\hat A|a_i\rangle
=
a_i|a_i\rangle
$$

podemos escribir:

$$
|\psi\rangle
=
\sum_i c_i|a_i\rangle
$$

Los coeficientes son:

$$
c_i
=
\langle a_i|\psi\rangle
$$

---

# 3. Probabilidad

La probabilidad de obtener el resultado $a_i$ es:

$$
\boxed{
P(a_i)
=
|\langle a_i|\psi\rangle|^2
}
$$

Como:

$$
c_i=\langle a_i|\psi\rangle
$$

también podemos escribir:

$$
P(a_i)=|c_i|^2
$$

---

# 4. Normalización

Si el estado está normalizado:

$$
\langle\psi|\psi\rangle=1
$$

entonces:

$$
\sum_i|c_i|^2=1
$$

Como:

$$
P(a_i)=|c_i|^2
$$

obtenemos:

$$
\boxed{
\sum_iP(a_i)=1
}
$$

Esto expresa que la suma de las probabilidades de todos los resultados posibles debe ser uno.

---

# 5. Valor esperado

Para un observable $\hat A$, el valor esperado se define como:

$$
\boxed{
\langle\hat A\rangle
=
\langle\psi|\hat A|\psi\rangle
}
$$

Este valor no debe confundirse con el resultado de una medición individual.

Es el valor medio que aparece al considerar muchas mediciones sobre sistemas preparados de la misma manera.

---

# 6. Valor esperado en la base de autestados

Tenemos:

$$
|\psi\rangle
=
\sum_i c_i|a_i\rangle
$$

y:

$$
\hat A|a_i\rangle
=
a_i|a_i\rangle
$$

Entonces:

$$
\langle\hat A\rangle
=
\sum_i a_i|c_i|^2
$$

Como:

$$
P(a_i)=|c_i|^2
$$

podemos escribir:

$$
\boxed{
\langle\hat A\rangle
=
\sum_i a_iP(a_i)
}
$$

Es decir, el valor esperado es el promedio ponderado de los posibles resultados.

---

# 7. Ejemplo conceptual

Supongamos que un observable puede producir dos resultados:

$$
a_1
$$

y:

$$
a_2
$$

con probabilidades:

$$
P(a_1)
$$

y:

$$
P(a_2)
$$

Entonces:

$$
\langle\hat A\rangle
=
a_1P(a_1)
+
a_2P(a_2)
$$

Pero una medición individual solamente puede producir $a_1$ o $a_2$.

El valor esperado no tiene por qué ser uno de los resultados posibles.

---

# 8. Representación matricial

Una vez establecido el formalismo abstracto, podemos representar los estados y operadores mediante matrices.

Si:

$$
|\psi\rangle
=
\sum_i c_i|a_i\rangle
$$

entonces, respecto de esa base:

$$
|\psi\rangle
\longleftrightarrow
\begin{pmatrix}
c_1\\
c_2\\
\vdots\\
c_n
\end{pmatrix}
$$

El ket se representa mediante un **vector columna**.

---

# 9. Bra en representación matricial

El bra correspondiente se obtiene mediante conjugación compleja y transposición:

$$
\langle\psi|
\longleftrightarrow
\begin{pmatrix}
c_1^*&c_2^*&\cdots&c_n^*
\end{pmatrix}
$$

Por ejemplo, si:

$$
|\psi\rangle
\longleftrightarrow
\begin{pmatrix}
c_1\\
c_2
\end{pmatrix}
$$

entonces:

$$
\langle\psi|
\longleftrightarrow
\begin{pmatrix}
c_1^*&c_2^*
\end{pmatrix}
$$

---

# 10. Producto interno en forma matricial

Para dos estados:

$$
|\psi\rangle
\longleftrightarrow
\vec c
$$

y:

$$
|\phi\rangle
\longleftrightarrow
\vec d
$$

el producto interno es:

$$
\langle\phi|\psi\rangle
=
\vec d^{\,\dagger}\vec c
$$

En componentes:

$$
\langle\phi|\psi\rangle
=
\sum_i d_i^*c_i
$$

---

# 11. Representación matricial de un operador

Un operador $\hat A$ puede representarse mediante una matriz cuyos elementos son:

$$
A_{ij}
=
\langle a_i|\hat A|a_j\rangle
$$

Por tanto:

$$
\hat A
\longleftrightarrow
[A_{ij}]
$$

La matriz depende de la base que hayamos elegido.

---

# 12. Elementos de matriz

La cantidad:

$$
\langle a_i|\hat A|a_j\rangle
$$

se denomina un elemento de matriz de $\hat A$ en la base ${|a_i\rangle}$.

Si la base está formada por autestados de $\hat A$:

$$
\hat A|a_j\rangle=a_j|a_j\rangle
$$

entonces:

$$
\langle a_i|\hat A|a_j\rangle
=
a_j\langle a_i|a_j\rangle
$$

Usando ortonormalidad:

$$
\langle a_i|a_j\rangle
=
\delta_{ij}
$$

obtenemos:

$$
\langle a_i|\hat A|a_j\rangle
=
a_j\delta_{ij}
$$

Por tanto, en su propia base de autestados, el operador queda representado por una matriz diagonal:

$$
\hat A
\longleftrightarrow
\begin{pmatrix}
a_1&0&\cdots&0\\
0&a_2&\cdots&0\\
\vdots&\vdots&\ddots&\vdots\\
0&0&\cdots&a_n
\end{pmatrix}
$$

---

