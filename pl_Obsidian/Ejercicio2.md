# 2. Secuencia de mediciones de Stern–Gerlach

Tenemos un haz inicialmente preparado en

$$
|+x\rangle
=
\frac1{\sqrt2}(|+z\rangle+|-z\rangle),
$$

y

$$
|-x\rangle
=
\frac1{\sqrt2}(|+z\rangle-|-z\rangle).
$$

El analizador intermedio transmite únicamente

$$
|+n\rangle
=
\cos\left(\frac\beta2\right)|+z\rangle
+
\sin\left(\frac\beta2\right)|-z\rangle.
$$

El último analizador transmite únicamente $|-x\rangle$.

---

# I. Prerrequisitos y conceptos

## 1. Analizador de Stern–Gerlach

Un analizador que transmite únicamente $|a\rangle$ funciona como un **filtro de estados**:

* si el sistema está en $|\psi\rangle$, la probabilidad de transmisión es

$$
P(a)=|\langle a|\psi\rangle|^2;
$$

* los sistemas que atraviesan el filtro quedan preparados en el estado $|a\rangle$.

Esto último es fundamental en este ejercicio.

---

## 2. Mediciones consecutivas

Si tenemos

$$
|\psi\rangle
\longrightarrow
|a\rangle
\longrightarrow
|b\rangle,
$$

la intensidad relativa final es

$$
\boxed{
P_{\rm final}
=
|\langle a|\psi\rangle|^2
|\langle b|a\rangle|^2
}.
$$

La primera medición cambia el estado a $|a\rangle$, y la segunda actúa sobre **ese nuevo estado**, no sobre el estado original.

---

## 3. Estados ortogonales

De las definiciones,

$$
\langle-x|+x\rangle=0.
$$

Por eso, directamente de $|+x\rangle$ nunca podemos obtener $|-x\rangle$ mediante un filtro ideal:

$$
P(+x\to-x)=0.
$$

El punto interesante es que una medición intermedia puede cambiar esta situación.

---

# (a) Retirar completamente el analizador intermedio

Sin el analizador intermedio tenemos simplemente

$$
|+x\rangle\longrightarrow|-x\rangle.
$$

Pero

$$
\langle-x|+x\rangle=0.
$$

Por tanto,

$$
P(+x\to-x)
=
|\langle-x|+x\rangle|^2
=0.
$$

Así que:

$$
\boxed{I_{\rm final}=0}.
$$

### Predicción sin cálculo extenso

$|+x\rangle$ y $|-x\rangle$ son estados ortogonales. Un analizador que transmite $|-x\rangle$ no puede transmitir un haz preparado en $|+x\rangle$.

---

# (b) Introducir el analizador intermedio

Ahora la secuencia es

$$
|+x\rangle
\longrightarrow
|+n\rangle
\longrightarrow
|-x\rangle.
$$

Primero conviene hacer las predicciones especiales.

---

## Caso $\beta=0$

Si

$$
\beta=0,
$$

entonces

$$
\cos(0)=1,\qquad \sin(0)=0,
$$

por lo que

$$
|+n\rangle=|+z\rangle.
$$

La secuencia es

$$
|+x\rangle\to|+z\rangle\to|-x\rangle.
$$

Como

$$
|\langle+z|+x\rangle|^2=\frac12
$$

y

$$
|\langle-x|+z\rangle|^2=\frac12,
$$

esperamos

$$
\boxed{P_{\rm final}=\frac14}.
$$

---

## Caso $\beta=\pi/2$

Ahora

$$
\cos\frac{\pi}{4}
=
\sin\frac{\pi}{4}
=
\frac1{\sqrt2}.
$$

Entonces

$$
|+n\rangle
=
\frac1{\sqrt2}(|+z\rangle+|-z\rangle)
=
|+x\rangle.
$$

El analizador intermedio simplemente transmite el estado $|+x\rangle$ sin cambiarlo.

Pero después tenemos

$$
|+x\rangle\to|-x\rangle,
$$

lo cual es imposible.

Por tanto,

$$
\boxed{P_{\rm final}=0}.
$$

---

# Cálculo general

La probabilidad de que el primer filtro transmita es

$$
P_1
=
|\langle+n|+x\rangle|^2.
$$

Tenemos

$$
\langle+n|
=
\cos\frac\beta2\langle+z|
+
\sin\frac\beta2\langle-z|.
$$

Entonces

$$
\begin{aligned}
\langle+n|+x\rangle
&=
\frac1{\sqrt2}
\left(
\cos\frac\beta2+\sin\frac\beta2
\right).
\end{aligned}
$$

Por tanto,

$$
P_1
=
\frac12
\left(
\cos\frac\beta2+\sin\frac\beta2
\right)^2.
$$

Usando

$$
(\cos a+\sin a)^2=1+\sin(2a),
$$

con $a=\beta/2$:

$$
\boxed{
P_1=\frac{1+\sin\beta}{2}
}.
$$

---

Ahora calculamos la probabilidad de que el estado $|+n\rangle$ atraviese el último analizador:

$$
P_2
=
|\langle-x|+n\rangle|^2.
$$

Como

$$
\langle-x|
=
\frac1{\sqrt2}
(\langle+z|-\langle-z|),
$$

tenemos

$$
\langle-x|+n\rangle
=
\frac1{\sqrt2}
\left(
\cos\frac\beta2-\sin\frac\beta2
\right).
$$

Así,

$$
P_2
=
\frac12
\left(
\cos\frac\beta2-\sin\frac\beta2
\right)^2.
$$

Usando

$$
(\cos a-\sin a)^2=1-\sin(2a),
$$

obtenemos

$$
\boxed{
P_2=\frac{1-\sin\beta}{2}
}.
$$

---

## Probabilidad total

Las dos etapas son consecutivas, así que multiplicamos:

$$
P_{\rm final}=P_1P_2.
$$

Por tanto,

$$
\begin{aligned}
P_{\rm final}
&=
\frac{1+\sin\beta}{2}
\frac{1-\sin\beta}{2}\\
&=
\frac{1-\sin^2\beta}{4}\\
&=
\boxed{\frac{\cos^2\beta}{4}}.
\end{aligned}
$$

Por tanto, la intensidad final relativa a la inicial es

$$
\boxed{
\frac{I_{\rm final}}{I_0}
=
\frac{\cos^2\beta}{4}
}.
$$

---

## ¿Cuándo es máxima?

Necesitamos maximizar

$$
\cos^2\beta.
$$

Su máximo es $1$, cuando

$$
\cos^2\beta=1.
$$

Por tanto,

$$
\boxed{\beta=0,\pi}
$$

si consideramos $0\leq\beta\leq\pi$.

En cualquiera de esas orientaciones:

$$
\boxed{
\frac{I_{\rm final}}{I_0}=\frac14
}.
$$

En particular, para $\beta=0$:

$$
|+n\rangle=|+z\rangle,
$$

y la secuencia es

$$
|+x\rangle
\xrightarrow{1/2}
|+z\rangle
\xrightarrow{1/2}
|-x\rangle,
$$

dando

$$
\frac12\frac12=\frac14.
$$

---

# (c) ¿Por qué la medición intermedia permite algo que inicialmente era imposible?

Sin medición intermedia:

$$
|+x\rangle\to|-x\rangle
$$

tiene probabilidad

$$
|\langle-x|+x\rangle|^2=0.
$$

Pero con la medición intermedia:

$$
|+x\rangle
\longrightarrow
|+n\rangle
\longrightarrow
|-x\rangle,
$$

el primer analizador **proyecta el estado** sobre $|+n\rangle$.

Es decir, después de atravesarlo, el sistema ya no está en $|+x\rangle$, sino en

$$
\boxed{|+n\rangle}.
$$

Y, en general,

$$
\langle-x|+n\rangle\neq0.
$$

Por eso el último analizador puede transmitir partículas.

La medición intermedia no simplemente "revela" una propiedad que ya tenía el sistema: **modifica el estado mediante la proyección asociada a la medición**.

---

# Idea física central

La secuencia ilustra una característica fundamental de la mecánica cuántica:

$$
\boxed{
\text{Una medición intermedia puede cambiar las posibilidades de mediciones posteriores.}
}
$$

En este caso:

$$
\boxed{
P(+x\to-x)=0
}
$$

pero

$$
\boxed{
P(+x\to+n\to-x)
=
\frac{\cos^2\beta}{4}
}
$$

puede ser distinta de cero.

Para $\beta=0$:

$$
\boxed{
P(+x\to+z\to-x)=\frac14.
}
$$

La razón no es que las probabilidades simplemente se "redistribuyan", sino que **el estado se transforma al realizar la medición intermedia**.

---

Si quieres, puedo:

* Continuar con ejercicio 3 y análisis de fases en espín
* Continuar con explicación del ejercicio 4 y estados propios de energía
* Expandir análisis de resultado esperado y medición individual
