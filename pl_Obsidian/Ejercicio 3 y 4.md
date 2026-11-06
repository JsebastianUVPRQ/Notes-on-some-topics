# Ejercicio 3 — Fase relativa y elección de la medición

## Prerrequisitos

Para resolver este ejercicio necesitamos únicamente conceptos que ya fueron vistos en las clases.

### 1. Superposición

Un estado cuántico puede escribirse como una combinación lineal de otros estados:

$$
|\psi\rangle=c_1|1\rangle+c_2|2\rangle
$$

Los coeficientes $c_1$ y $c_2$ pueden ser **números complejos**.

Esto es importante porque en el ejercicio aparece el número $i$.

---

### 2. Probabilidad de una medición

Si $|a\rangle$ es el estado asociado a un resultado de medición, la probabilidad de obtener dicho resultado viene dada por

$$
P(a)=|\langle a|\psi\rangle|^2
$$

Por tanto, no basta con observar los coeficientes del estado. Primero debemos calcular el **producto interno** con el estado asociado al resultado que queremos medir y después tomar el módulo al cuadrado.

---

### 3. Producto interno y ortonormalidad

Los estados $|+z\rangle$ y $|-z\rangle$ forman una base ortonormal. Por tanto:

$$
\langle +z|+z\rangle=1
$$

$$
\langle -z|-z\rangle=1
$$

y

$$
\langle +z|-z\rangle=0
$$

$$
\langle -z|+z\rangle=0
$$

---

### 4. Fase relativa

Un número complejo puede escribirse como

$$
c=|c|e^{i\theta}
$$

Una fase común a todo el estado no modifica las probabilidades. Sin embargo, una **fase relativa** entre dos componentes de una superposición puede modificar los resultados de determinadas mediciones.

Este ejercicio está construido precisamente para mostrar esa idea.

---

# (a) ¿Por qué medir $\hat S_z$ no permite distinguir los estados?

Las dos fuentes preparan:

$$
|\psi_A\rangle
=
\frac{1}{\sqrt{2}}
\left(
|+z\rangle+|-z\rangle
\right)
$$

y

$$
|\psi_B\rangle
=
\frac{1}{\sqrt{2}}
\left(
|+z\rangle+i|-z\rangle
\right)
$$

Queremos entender por qué ambas producen la misma estadística al medir $\hat S_z$, a pesar de que los estados no son iguales.

---

## Fuente A

Para obtener el resultado $+\hbar/2$, necesitamos calcular la amplitud

$$
\langle +z|\psi_A\rangle
$$

Sustituimos $|\psi_A\rangle$:

$$
\langle +z|\psi_A\rangle
=
\frac{1}{\sqrt{2}}
\left(
\langle +z|+z\rangle
+
\langle +z|-z\rangle
\right)
$$

Usando la ortonormalidad:

$$
\langle +z|+z\rangle=1
$$

y

$$
\langle +z|-z\rangle=0
$$

obtenemos

$$
\langle +z|\psi_A\rangle
=
\frac{1}{\sqrt{2}}
$$

Por tanto:

$$
P_A(+z)
=
\left|
\frac{1}{\sqrt{2}}
\right|^2
=
\frac{1}{2}
$$

De forma análoga:

$$
P_A(-z)=\frac{1}{2}
$$

Por tanto, para la fuente A:

$$
P_A(+z)=P_A(-z)=\frac{1}{2}
$$

---

## Fuente B

Ahora tenemos

$$
|\psi_B\rangle
=
\frac{1}{\sqrt{2}}
\left(
|+z\rangle+i|-z\rangle
\right)
$$

La amplitud para obtener $+\hbar/2$ es

$$
\langle +z|\psi_B\rangle
=
\frac{1}{\sqrt{2}}
\left(
\langle +z|+z\rangle
+
i\langle +z|-z\rangle
\right)
$$

Por ortonormalidad:

$$
\langle +z|\psi_B\rangle
=
\frac{1}{\sqrt{2}}
$$

Así:

$$
P_B(+z)
=
\left|
\frac{1}{\sqrt{2}}
\right|^2
=
\frac{1}{2}
$$

Para $-z$:

$$
\langle -z|\psi_B\rangle
=
\frac{i}{\sqrt{2}}
$$

Entonces:

$$
P_B(-z)
=
\left|
\frac{i}{\sqrt{2}}
\right|^2
=
\frac{1}{2}
$$

Por tanto:

$$
P_B(+z)=P_B(-z)=\frac{1}{2}
$$

---

## ¿Qué hemos aprendido?

Ambas fuentes producen exactamente la misma estadística al medir $\hat S_z$:

$$
P(+z)=P(-z)=\frac{1}{2}
$$

Pero eso **no significa que los estados sean iguales**.

Tenemos:

$$
|\psi_A\rangle
=
\frac{1}{\sqrt{2}}
|+z\rangle
+
\frac{1}{\sqrt{2}}
|-z\rangle
$$

mientras que

$$
|\psi_B\rangle
=
\frac{1}{\sqrt{2}}
|+z\rangle
+
\frac{i}{\sqrt{2}}
|-z\rangle
$$

La diferencia está en la **fase relativa** entre los dos componentes.

En $|\psi_A\rangle$, los coeficientes tienen la relación de fase $1$.

En $|\psi_B\rangle$, la relación de fase es $i$.

La medición de $\hat S_z$ no permite observar esa diferencia.

> **Idea fundamental:** que dos estados produzcan la misma estadística para una medición particular no implica que sean el mismo estado físico.

---

# (b) Analizador de Stern–Gerlach que transmite $|+x\rangle$

Tenemos:

$$
|+x\rangle
=
\frac{1}{\sqrt{2}}
\left(
|+z\rangle+|-z\rangle
\right)
$$

Antes de hacer los cálculos podemos hacer una predicción.

Observamos que

$$
|\psi_A\rangle=|+x\rangle
$$

Por tanto, la fuente A prepara exactamente el estado que el analizador transmite.

Esperamos entonces:

$$
P_A(+x)=1
$$

La fuente B, en cambio, tiene una fase relativa diferente. Por tanto, esperamos una probabilidad de transmisión menor.

Ahora lo comprobamos.

---

## Fuente A

La amplitud de transmisión es

$$
\langle +x|\psi_A\rangle
$$

Como $|\psi_A\rangle=|+x\rangle$:

$$
\langle +x|\psi_A\rangle
=
\langle +x|+x\rangle
=
1
$$

Por tanto:

$$
P_A(+x)
=
|\langle +x|\psi_A\rangle|^2
=
1
$$

Así:

$$
\boxed{P_A(+x)=1}
$$

Toda la intensidad de la fuente A es transmitida.

---

## Fuente B

Queremos calcular

$$
\langle +x|\psi_B\rangle
$$

Primero escribimos el bra correspondiente a $|+x\rangle$:

$$
\langle +x|
=
\frac{1}{\sqrt{2}}
\left(
\langle +z|+\langle -z|
\right)
$$

Entonces:

$$
\langle +x|\psi_B\rangle
=
\frac{1}{\sqrt{2}}
\left(
\langle +z|+\langle -z|
\right)
\frac{1}{\sqrt{2}}
\left(
|+z\rangle+i|-z\rangle
\right)
$$

Sacamos los factores:

$$
\langle +x|\psi_B\rangle
=
\frac{1}{2}
\left(
\langle +z|+\langle -z|
\right)
\left(
|+z\rangle+i|-z\rangle
\right)
$$

Distribuimos:

$$
\langle +x|\psi_B\rangle
=
\frac{1}{2}
\left[
\langle +z|+z\rangle
+
i\langle +z|-z\rangle
+
\langle -z|+z\rangle
+
i\langle -z|-z\rangle
\right]
$$

Aplicamos la ortonormalidad:

$$
\langle +z|+z\rangle=1
$$

$$
\langle -z|-z\rangle=1
$$

$$
\langle +z|-z\rangle=0
$$

$$
\langle -z|+z\rangle=0
$$

Entonces:

$$
\langle +x|\psi_B\rangle
=
\frac{1+i}{2}
$$

La probabilidad de transmisión es:

$$
P_B(+x)
=
\left|
\frac{1+i}{2}
\right|^2
$$

Como

$$
|1+i|^2=1^2+1^2=2
$$

tenemos:

$$
P_B(+x)
=
\frac{2}{4}
=
\frac{1}{2}
$$

Por tanto:

$$
\boxed{P_B(+x)=\frac{1}{2}}
$$

---

## Resultado de la parte (b)

Tenemos:

$$
\boxed{
P_A(+x)=1
}
$$

y

$$
\boxed{
P_B(+x)=\frac{1}{2}
}
$$

Por tanto, el analizador de Stern–Gerlach orientado para seleccionar $|+x\rangle$ permite distinguir los estados preparados por las dos fuentes.

La razón es que la nueva medición es sensible a la **fase relativa** que no podía observarse mediante la medición de $\hat S_z$.

---

# (c) Producto interior $\langle\psi_A|\psi_B\rangle$

Queremos calcular:

$$
\langle\psi_A|\psi_B\rangle
$$

Primero obtenemos el bra correspondiente a $|\psi_A\rangle$:

$$
\langle\psi_A|
=
\frac{1}{\sqrt{2}}
\left(
\langle +z|+\langle -z|
\right)
$$

Entonces:

$$
\langle\psi_A|\psi_B\rangle
=
\frac{1}{2}
\left(
\langle +z|+\langle -z|
\right)
\left(
|+z\rangle+i|-z\rangle
\right)
$$

Distribuyendo:

$$
\langle\psi_A|\psi_B\rangle
=
\frac{1}{2}
\left[
\langle +z|+z\rangle
+
i\langle +z|-z\rangle
+
\langle -z|+z\rangle
+
i\langle -z|-z\rangle
\right]
$$

Usando la ortonormalidad:

$$
\boxed{
\langle\psi_A|\psi_B\rangle
=
\frac{1+i}{2}
}
$$

Su módulo es:

$$
\left|
\langle\psi_A|\psi_B\rangle
\right|
=
\frac{1}{\sqrt{2}}
$$

y por tanto:

$$
\left|
\langle\psi_A|\psi_B\rangle
\right|^2
=
\frac{1}{2}
$$

Esto coincide con la probabilidad que encontramos anteriormente:

$$
P_B(+x)=\frac{1}{2}
$$

porque $|\psi_A\rangle=|+x\rangle$.

---

## Interpretación geométrica

El producto interno mide el **solapamiento** entre los estados.

Como

$$
\left|
\langle\psi_A|\psi_B\rangle
\right|
=
\frac{1}{\sqrt{2}}
$$

los estados no son ortogonales, pero tampoco son el mismo estado.

En la interpretación geométrica del espacio de estados, podemos asociar un ángulo $\theta$ mediante

$$
\cos\theta
=
\frac{1}{\sqrt{2}}
$$

de donde

$$
\theta=\frac{\pi}{4}
$$

Además:

$$
\frac{1+i}{2}
=
\frac{1}{\sqrt{2}}e^{i\pi/4}
$$

La expresión contiene tanto información sobre el módulo del solapamiento como sobre la fase.

---

# Idea central del ejercicio 3

El ejercicio demuestra:

$$
\boxed{
\text{Misma estadística para una medición}
\not\Rightarrow
\text{mismo estado cuántico}
}
$$

La medición de $\hat S_z$ no permite distinguir las fuentes:

$$
P_A(+z)=P_B(+z)=\frac{1}{2}
$$

y

$$
P_A(-z)=P_B(-z)=\frac{1}{2}
$$

Pero una medición en la dirección $x$ sí permite distinguirlas:

$$
P_A(+x)=1
$$

mientras que

$$
P_B(+x)=\frac{1}{2}
$$

La diferencia que hace posible esta distinción es la **fase relativa**.

---

# Ejercicio 4 — Superposición, degeneración y valor esperado de la energía

## Prerrequisitos

Este ejercicio combina varias ideas que ya fueron introducidas.

---

## 1. Hamiltoniano como observable

El Hamiltoniano $\hat H$ es el operador asociado a la energía.

Por tanto, sus autovalores son los posibles resultados de una medición de energía.

Si

$$
\hat H|\psi\rangle=E|\psi\rangle
$$

entonces $|\psi\rangle$ es un estado propio de $\hat H$ y posee energía bien definida $E$.

---

## 2. Superposición

Un estado puede ser una combinación lineal de estados propios:

$$
|\psi\rangle
=
c_1|u_1\rangle+c_2|u_2\rangle
$$

La pregunta fundamental es:

> ¿Los estados que forman la superposición tienen el mismo autovalor o autovalores diferentes?

---

## 3. Degeneración

El ejercicio proporciona:

$$
\hat H|u_1\rangle=E|u_1\rangle
$$

y

$$
\hat H|u_2\rangle=E|u_2\rangle
$$

Los dos estados son diferentes, pero tienen el mismo autovalor $E$.

Decimos que el autovalor $E$ es **degenerado**.

La consecuencia importante para este ejercicio es:

> Una combinación lineal de estados propios correspondientes al mismo autovalor sigue siendo un estado propio con ese mismo autovalor.

---

# (a) Predicción

Tenemos:

$$
|\alpha\rangle
=
\frac{1}{\sqrt{5}}
\left(
2|u_1\rangle+i|u_2\rangle
\right)
$$

y

$$
|\beta\rangle
=
\frac{1}{\sqrt{5}}
\left(
2|u_1\rangle+i|u_3\rangle
\right)
$$

Además:

$$
\hat H|u_1\rangle=E|u_1\rangle
$$

$$
\hat H|u_2\rangle=E|u_2\rangle
$$

$$
\hat H|u_3\rangle=3E|u_3\rangle
$$

con $E>0$.

---

## Estado $|\alpha\rangle$

Los estados que aparecen en $|\alpha\rangle$ son:

$$
|u_1\rangle,\qquad |u_2\rangle
$$

Ambos tienen el mismo autovalor:

$$
E
$$

Por tanto, podemos predecir que $|\alpha\rangle$ tendrá energía bien definida.

---

## Estado $|\beta\rangle$

Los estados que aparecen en $|\beta\rangle$ son:

$$
|u_1\rangle,\qquad |u_3\rangle
$$

pero sus autovalores son diferentes:

$$
E
$$

y

$$
3E
$$

Por tanto, esperamos que $|\beta\rangle$ no sea un estado propio de $\hat H$ y, por tanto, no tenga una energía bien definida.

---

## Predicción

$$
\boxed{
|\alpha\rangle:\text{ energía bien definida}
}
$$

$$
\boxed{
|\beta\rangle:\text{ energía no bien definida}
}
$$

La característica que permite hacer esta predicción es si los estados que aparecen en la superposición tienen **el mismo autovalor de energía**.

---

# (b) Comprobación aplicando $\hat H$

## Estado $|\alpha\rangle$

Partimos de:

$$
|\alpha\rangle
=
\frac{1}{\sqrt{5}}
\left(
2|u_1\rangle+i|u_2\rangle
\right)
$$

Aplicamos $\hat H$:

$$
\hat H|\alpha\rangle
=
\hat H
\left[
\frac{1}{\sqrt{5}}
\left(
2|u_1\rangle+i|u_2\rangle
\right)
\right]
$$

Por linealidad:

$$
\hat H|\alpha\rangle
=
\frac{1}{\sqrt{5}}
\left(
2\hat H|u_1\rangle
+
i\hat H|u_2\rangle
\right)
$$

Utilizamos las ecuaciones dadas:

$$
\hat H|\alpha\rangle
=
\frac{1}{\sqrt{5}}
\left(
2E|u_1\rangle
+
iE|u_2\rangle
\right)
$$

Sacamos $E$:

$$
\hat H|\alpha\rangle
=
E
\frac{1}{\sqrt{5}}
\left(
2|u_1\rangle+i|u_2\rangle
\right)
$$

Reconocemos el estado $|\alpha\rangle$:

$$
\boxed{
\hat H|\alpha\rangle=E|\alpha\rangle
}
$$

Por tanto, $|\alpha\rangle$ es un estado propio del Hamiltoniano.

Su energía está bien definida:

$$
\boxed{E_\alpha=E}
$$

---

# Estado $|\beta\rangle$

Partimos de:

$$
|\beta\rangle
=
\frac{1}{\sqrt{5}}
\left(
2|u_1\rangle+i|u_3\rangle
\right)
$$

Aplicamos $\hat H$:

$$
\hat H|\beta\rangle
=
\frac{1}{\sqrt{5}}
\left(
2\hat H|u_1\rangle
+
i\hat H|u_3\rangle
\right)
$$

Sustituimos las ecuaciones de los estados propios:

$$
\hat H|\beta\rangle
=
\frac{1}{\sqrt{5}}
\left(
2E|u_1\rangle
+
i(3E)|u_3\rangle
\right)
$$

Por tanto:

$$
\boxed{
\hat H|\beta\rangle
=
\frac{E}{\sqrt{5}}
\left(
2|u_1\rangle+3i|u_3\rangle
\right)
}
$$

Comparemos esto con:

$$
|\beta\rangle
=
\frac{1}{\sqrt{5}}
\left(
2|u_1\rangle+i|u_3\rangle
\right)
$$

Para que $|\beta\rangle$ fuera un estado propio debería existir un único número $E'$ tal que

$$
\hat H|\beta\rangle=E'|\beta\rangle
$$

Pero el componente $|u_1\rangle$ adquiere un factor $E$, mientras que el componente $|u_3\rangle$ adquiere un factor $3E$.

No existe un único factor que multiplique a ambos componentes.

Por tanto:

$$
\boxed{
|\beta\rangle\text{ no es un estado propio de }\hat H
}
$$

y, por tanto, su energía no está bien definida.

---

# Posibles resultados de una medición de energía

El estado es:

$$
|\beta\rangle
=
\frac{2}{\sqrt{5}}|u_1\rangle
+
\frac{i}{\sqrt{5}}|u_3\rangle
$$

Los estados $|u_1\rangle$ y $|u_3\rangle$ son estados propios de $\hat H$.

Sus autovalores son:

$$
E
$$

y

$$
3E
$$

Por tanto, los posibles resultados de la medición son:

$$
\boxed{E\quad\text{y}\quad3E}
$$

---

## Probabilidad de obtener $E$

El coeficiente de $|u_1\rangle$ es:

$$
c_1=\frac{2}{\sqrt{5}}
$$

Por la regla de probabilidad:

$$
P(E)=|c_1|^2
$$

Por tanto:

$$
P(E)
=
\left|
\frac{2}{\sqrt{5}}
\right|^2
=
\frac{4}{5}
$$

Así:

$$
\boxed{
P(E)=\frac{4}{5}
}
$$

---

## Probabilidad de obtener $3E$

El coeficiente de $|u_3\rangle$ es:

$$
c_3=\frac{i}{\sqrt{5}}
$$

Entonces:

$$
P(3E)=|c_3|^2
$$

y:

$$
P(3E)
=
\left|
\frac{i}{\sqrt{5}}
\right|^2
=
\frac{1}{5}
$$

Por tanto:

$$
\boxed{
P(3E)=\frac{1}{5}
}
$$

Comprobamos que las probabilidades están normalizadas:

$$
\frac{4}{5}+\frac{1}{5}=1
$$

---

# Valor esperado de la energía

El ejercicio define:

$$
\langle\hat H\rangle
=
\langle\beta|\hat H|\beta\rangle
$$

Como los posibles resultados son $E$ y $3E$, con probabilidades $4/5$ y $1/5$, respectivamente, el valor esperado es:

$$
\langle\hat H\rangle
=
E\frac{4}{5}
+
3E\frac{1}{5}
$$

Calculamos:

$$
\langle\hat H\rangle
=
\frac{4E}{5}
+
\frac{3E}{5}
$$

Por tanto:

$$
\boxed{
\langle\hat H\rangle=\frac{7E}{5}
}
$$

Observamos que:

$$
E<\frac{7E}{5}<3E
$$

Esto tiene sentido porque $\langle\hat H\rangle$ es un promedio ponderado de los posibles resultados.

---

# (c) Análisis de las afirmaciones del estudiante

## Primera afirmación

> "Un estado escrito como superposición de dos estados nunca puede ser un estado propio de la energía."

Esta afirmación es **falsa**.

El estado $|\alpha\rangle$ proporciona directamente un contraejemplo:

$$
|\alpha\rangle
=
\frac{1}{\sqrt{5}}
\left(
2|u_1\rangle+i|u_2\rangle
\right)
$$

Es una superposición de dos estados.

Sin embargo:

$$
\hat H|\alpha\rangle=E|\alpha\rangle
$$

Por tanto, $|\alpha\rangle$ sí es un estado propio del Hamiltoniano y tiene energía bien definida $E$.

La razón es que los dos estados que forman la superposición tienen el mismo autovalor:

$$
E_1=E_2=E
$$

Esto es precisamente el caso de **degeneración**.

### Formulación correcta

Una formulación correcta sería:

> Una superposición de estados propios con autovalores diferentes no es, en general, un estado propio del observable.

El estado $|\beta\rangle$ muestra este caso:

$$
E_1=E
$$

mientras que

$$
E_3=3E
$$

y por ello:

$$
\hat H|\beta\rangle
\neq
E'|\beta\rangle
$$

para cualquier único $E'$.

---

# Segunda afirmación

> "Además, si el valor esperado de la energía es $\langle\hat H\rangle$, éste debe ser el valor registrado en una medición individual."

Esta afirmación también es **falsa**.

Para $|\beta\rangle$ encontramos:

$$
\langle\hat H\rangle=\frac{7E}{5}
$$

Pero los únicos resultados posibles de una medición individual son:

$$
E
$$

o

$$
3E
$$

El valor

$$
\frac{7E}{5}
$$

no es uno de los posibles resultados de una medición individual.

Por tanto:

$$
\boxed{
\text{Medición individual}
\longrightarrow
E\ \text{o}\ 3E
}
$$

mientras que:

$$
\boxed{
\text{Muchas mediciones}
\longrightarrow
\text{promedio}
\longrightarrow
\frac{7E}{5}
}
$$

El valor esperado representa el promedio estadístico que se obtiene al repetir muchas veces la preparación del mismo estado y medir el mismo observable.

---

# Resumen conceptual del ejercicio 4

## Superposición de estados con el mismo autovalor

Si:

$$
\hat H|u_1\rangle=E|u_1\rangle
$$

y

$$
\hat H|u_2\rangle=E|u_2\rangle
$$

entonces una combinación lineal:

$$
a|u_1\rangle+b|u_2\rangle
$$

también es un estado propio de $\hat H$ con autovalor $E$.

Por eso:

$$
\boxed{
|\alpha\rangle\text{ tiene energía bien definida}
}
$$

---

## Superposición de estados con autovalores diferentes

Si:

$$
\hat H|u_1\rangle=E|u_1\rangle
$$

pero:

$$
\hat H|u_3\rangle=3E|u_3\rangle
$$

entonces una superposición como:

$$
a|u_1\rangle+b|u_3\rangle
$$

no es, en general, un estado propio del Hamiltoniano.

Por eso:

$$
\boxed{
|\beta\rangle\text{ no tiene energía bien definida}
}
$$

y una medición de energía puede producir:

$$
\boxed{
E\quad\text{con probabilidad }\frac{4}{5}
}
$$

o:

$$
\boxed{
3E\quad\text{con probabilidad }\frac{1}{5}
}
$$

El valor esperado es:

$$
\boxed{
\langle\hat H\rangle=\frac{7E}{5}
}
$$

---

# Conexión entre los ejercicios 3 y 4

Los dos ejercicios están trabajando una misma idea general:

> **Una superposición no debe interpretarse solamente mirando sus coeficientes. Hay que considerar qué observable se mide y cuáles son sus estados propios.**

En el ejercicio 3:

$$
|\psi_A\rangle
=
\frac{1}{\sqrt2}
\left(
|+z\rangle+|-z\rangle
\right)
$$

y

$$
|\psi_B\rangle
=
\frac{1}{\sqrt2}
\left(
|+z\rangle+i|-z\rangle
\right)
$$

producen la misma estadística para $\hat S_z$, pero diferentes resultados cuando se selecciona $|+x\rangle$.

En el ejercicio 4:

$$
|\alpha\rangle
=
\frac{1}{\sqrt5}
\left(
2|u_1\rangle+i|u_2\rangle
\right)
$$

es una superposición pero tiene energía bien definida porque $|u_1\rangle$ y $|u_2\rangle$ tienen el mismo autovalor.

En cambio:

$$
|\beta\rangle
=
\frac{1}{\sqrt5}
\left(
2|u_1\rangle+i|u_3\rangle
\right)
$$

es una superposición de estados con energías diferentes y, por tanto, no tiene una energía bien definida.

La pregunta que debemos acostumbrarnos a hacer es:

$$
\boxed{
\text{¿Respecto de qué observable estoy describiendo el estado?}
}
$$

y, para ese observable:

$$
\boxed{
\text{¿Cuáles son sus estados propios y sus autovalores?}
}
$$
# resumidas

# 3. Fase relativa y elección de la medición

### (a) ¿Por qué medir $\hat S_z$ no permite distinguir los estados?

Los estados son

$$
|\psi_A\rangle=\frac{1}{\sqrt2}(|+z\rangle+|-z\rangle),
$$

$$
|\psi_B\rangle=\frac{1}{\sqrt2}(|+z\rangle+i|-z\rangle).
$$

**Respuesta:** No pueden distinguirse midiendo $\hat S_z$ porque ambos producen las mismas probabilidades:

$$
P_A(+z)=P_B(+z)=\frac12,
$$

$$
P_A(-z)=P_B(-z)=\frac12.
$$

Por ejemplo,

$$
P_B(-z)=|\langle-z|\psi_B\rangle|^2
=\left|\frac{i}{\sqrt2}\right|^2
=\frac12.
$$

La diferencia entre los estados está en la **fase relativa** $i$, que esta medición no detecta.

---

### (b) Analizador que transmite $|+x\rangle$

Sabemos que

$$
|+x\rangle=\frac1{\sqrt2}(|+z\rangle+|-z\rangle).
$$

Por tanto,

$$
|\psi_A\rangle=|+x\rangle.
$$

**Predicción:** La fuente A debe transmitirse completamente, mientras que la fuente B debe transmitirse con probabilidad menor que 1, porque tiene una fase relativa diferente.

Para A:

$$
P_A(+x)=|\langle+x|\psi_A\rangle|^2=1.
$$

Para B:

$$
\langle+x|\psi_B\rangle
=
\frac{1+i}{2},
$$

por lo que

$$
P_B(+x)
=
\left|\frac{1+i}{2}\right|^2
=
\frac12.
$$

Por tanto,

$$
\boxed{P_A(+x)=1,\qquad P_B(+x)=\frac12}.
$$

Así, medir en la dirección $x$ permite distinguir las dos fuentes.

---

### (c) Calcule $\langle\psi_A|\psi_B\rangle$ e interprételo.

Usando la ortonormalidad de $|+z\rangle$ y $|-z\rangle$:

$$
\langle\psi_A|\psi_B\rangle
=
\frac12(1+i).
$$

Por tanto,

$$
\boxed{\langle\psi_A|\psi_B\rangle=\frac{1+i}{2}}.
$$

Su módulo al cuadrado es

$$
|\langle\psi_A|\psi_B\rangle|^2
=
\frac12.
$$

**Interpretación:** Los estados no son ortogonales, pero tampoco son idénticos. El valor $\frac12$ coincide con la probabilidad de que el estado $|\psi_B\rangle$ sea transmitido por un analizador que selecciona $|\psi_A\rangle=|+x\rangle$.

---

# 4. Superposición, degeneración y valor esperado de la energía

Tenemos

$$
\hat H|u_1\rangle=E|u_1\rangle,
\qquad
\hat H|u_2\rangle=E|u_2\rangle,
\qquad
\hat H|u_3\rangle=3E|u_3\rangle.
$$

Y

$$
|\alpha\rangle
=
\frac1{\sqrt5}(2|u_1\rangle+i|u_2\rangle),
$$

$$
|\beta\rangle
=
\frac1{\sqrt5}(2|u_1\rangle+i|u_3\rangle).
$$

### (a) Predicción

**Predicción:** $|\alpha\rangle$ tendrá energía bien definida porque $|u_1\rangle$ y $|u_2\rangle$ tienen el mismo autovalor $E$.

En cambio, $|\beta\rangle$ no tendrá energía bien definida porque combina estados con energías diferentes, $E$ y $3E$.

---

### (b) Compruebe su predicción mediante $\hat H$.

Para $|\alpha\rangle$:

$$
\hat H|\alpha\rangle
=
\frac1{\sqrt5}
(2E|u_1\rangle+iE|u_2\rangle)
=
E|\alpha\rangle.
$$

Por tanto,

$$
\boxed{|\alpha\rangle\text{ es un estado propio con energía }E}.
$$

Para $|\beta\rangle$:

$$
\hat H|\beta\rangle
=
\frac1{\sqrt5}
(2E|u_1\rangle+3iE|u_3\rangle).
$$

Esto no puede escribirse como $E'|\beta\rangle$ con un único $E'$, porque los dos componentes adquieren factores diferentes, $E$ y $3E$.

Por tanto,

$$
\boxed{|\beta\rangle\text{ no es un estado propio de }\hat H}.
$$

Los posibles resultados de una medición de energía son $E$ y $3E$.

Sus probabilidades son:

$$
P(E)=\left|\frac2{\sqrt5}\right|^2=\frac45,
$$

$$
P(3E)=\left|\frac{i}{\sqrt5}\right|^2=\frac15.
$$

---

### (c) Analice las afirmaciones.

**1. “Un estado escrito como superposición de dos estados nunca puede ser un estado propio de la energía.”**

**Falsa.** $|\alpha\rangle$ es una superposición, pero

$$
\hat H|\alpha\rangle=E|\alpha\rangle.
$$

Esto ocurre porque los dos estados de la superposición tienen el mismo autovalor.

---

**2. “Si el valor esperado de la energía es $\langle\hat H\rangle$, este debe ser el valor registrado en una medición individual.”**

**Falsa.** Para $|\beta\rangle$:

$$
\langle\hat H\rangle
=
E\frac45+3E\frac15
=
\frac{7E}{5}.
$$

Sin embargo, una medición individual solo puede dar los autovalores $E$ o $3E$.

Por tanto,

$$
\boxed{\langle\hat H\rangle=\frac{7E}{5}}
$$

es el **promedio de muchas mediciones**, no el resultado de una medición individual.
