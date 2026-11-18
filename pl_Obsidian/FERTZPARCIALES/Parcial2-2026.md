# Segundo parcial — Física Fundamental V (II-2026)


# Segundo parcial — Física Fundamental V (II-2026)

**Fecha:** 06.11.2026, 9:00 a. m. – 11.11.2026, 8:00 p. m.  
**Profesora:** Karem Rodríguez

## Indicaciones generales

Dispone del orden de 5 días para entregar su solución individual, manuscrita y escaneada en el Campusvirtual. Puede consultar el material que considere necesario.

Responda de manera corta, concisa y asertiva cada pregunta. Para esto debe: entender la pregunta, identificar la respuesta clave, responder claramente sólo con la información necesaria, evitar detalles irrelevantes y justificar cada una de sus respuestas. En los numerales en los que se solicite una predicción, ésta debe plasmarse antes del cálculo correspondiente.

---

## 1. Espín 1: amplitudes de probabilidad y cambio de base

Un haz de átomos con espín 1 ha sido preparado en el estado

$$
|\psi\rangle=\frac{1}{\sqrt{6}}\left(2|+1\rangle_z+|0\rangle_z+i|-1\rangle_z\right),
$$

donde $\{|+1\rangle_z,|0\rangle_z,|-1\rangle_z\}$ es la base de estados propios de $\hat S_z$. Los estados propios de $\hat S_x$, expresados en la base de $\hat S_z$, son

$$
|+1\rangle_x=\frac{1}{2}\left(|+1\rangle_z+\sqrt{2}|0\rangle_z+|-1\rangle_z\right),
$$

$$
|0\rangle_x=\frac{1}{\sqrt{2}}\left(|+1\rangle_z-|-1\rangle_z\right),
$$

$$
|-1\rangle_x=\frac{1}{2}\left(|+1\rangle_z-\sqrt{2}|0\rangle_z+|-1\rangle_z\right).
$$

**(a)** Si el haz descrito por $|\psi\rangle$ atraviesa un aparato de Stern-Gerlach orientado en la dirección $z$, determine los resultados posibles y sus probabilidades. Identifique explícitamente qué cantidades en $|\psi\rangle$ son amplitudes de probabilidad y cuáles determinan probabilidades.

**(b)** Exprese el mismo ket $|\psi\rangle$ en la base de estados propios de $\hat S_x$. Obtenga los nuevos coeficientes mediante productos interiores. ¿Cuál es la matriz de transformación?

**(c)** A partir de la superposición en la nueva base, determine las probabilidades de los resultados de una medición de $\hat S_x$. Compare estas probabilidades con las obtenidas para $\hat S_z$.

**(d)** Explique, utilizando este sistema físico, la diferencia entre las siguientes afirmaciones:

- El estado es una superposición de estados propios de $\hat S_z$.
- El estado se representa en la base de $\hat S_z$ o en la base de $\hat S_x$.
- Se realiza una transformación de cambio de base.

Indique lo que cambia matemáticamente y lo que permanece físicamente inalterado entre estas tres afirmaciones.

---

## 2. Átomo de hidrógeno: observables compatibles y degeneración

Considere un átomo de hidrógeno sin incluir el espín. Los observables $\{\hat H,\hat L^2,\hat L_z\}$ forman un conjunto completo de observables compatibles y sus estados propios simultáneos se denotan por $\{|n,\ell,m\rangle\}$. Un conjunto de átomos se prepara en el estado

$$
|\psi\rangle=\frac{1}{2}\left(|2,0,0\rangle+|2,1,-1\rangle+|2,1,0\rangle+|2,1,1\rangle\right).
$$

**(a)** Si se mide únicamente la energía, ¿cuál será el resultado? ¿Permite esa medición determinar completamente el estado del átomo después de la medición? Explique la relación con la degeneración.

**(b)** Si, además de la energía, se mide $L^2$, determine los resultados posibles. Para el resultado $L^2=2\hbar^2$, explique por qué todavía no se ha identificado un único estado propio del sistema.

**(c)** Muestre qué información adicional proporciona una medición de $L_z$. Explique por qué el conjunto $\{\hat H,\hat L^2,\hat L_z\}$ es completo, mientras que $\{\hat H\}$ o $\{\hat H,\hat L^2\}$ no lo son para este problema.

**(d)** Si una medición conjunta produce los valores asociados a $|2,1,-1\rangle$, indique qué puede afirmarse inmediatamente acerca del estado después de la medición. Distinga claramente entre valor propio, estado propio, resultado de medición y probabilidad.

---

## 3. Pozo infinito unidimensional: representaciones discreta y continua

Una partícula se encuentra descrita por el estado

$$
\phi_n(x)=\sqrt{\frac{2}{L}}\sin\left(\frac{n\pi x}{L}\right),
$$

la partícula se encuentra confinada en un pozo infinito unidimensional; bajo estas circunstancias, los estados propios de energía representados en la base de coordenadas (formando una base discreta de funciones de onda) están dados por

$$
|\psi\rangle=\frac{1}{\sqrt{5}}\left(2|1\rangle+i|2\rangle\right).
$$

**(a)** En la base discreta de energía, identifique las amplitudes de probabilidad y determine las probabilidades correspondientes a una medición de la energía.

**(b)** Obtenga la representación del mismo estado en la base continua de posición, $\psi(x)=\langle x|\psi\rangle$. Explique las similitudes y diferencias entre $|\psi\rangle$ y $\psi(x)$; ¿representan dos estados diferentes?

**(c)** Distinga cuidadosamente el significado físico de $\psi(x)$, $|\psi(x)|^2$, $|\psi(x)|^2dx$, y compárelo con el significado de $c_n$, $|c_n|^2$ en la base discreta de energía.

**(d)** Escriba la probabilidad de encontrar la partícula en el intervalo $x_1<x<x_2$. Explique por qué esta probabilidad requiere una integral, mientras que la probabilidad de obtener uno de los valores discretos de energía no la requiere.

---

## 4. Partícula libre: paquete de onda en las representaciones de momentum y posición

Una partícula libre en una dimensión se prepara en un paquete de onda cuya representación en la base continua que proporciona el observable de momentum ($\hat p|p\rangle=p|p\rangle$) es

$$
\phi(p)=\frac{1}{(2\pi\sigma_p^2)^{1/4}}\exp\left[-\frac{(p-p_0)^2}{4\sigma_p^2}\right].
$$

Utilice

$$
\langle x|p\rangle=\frac{1}{\sqrt{2\pi\hbar}}e^{ipx/\hbar}.
$$

**(a)** Antes de realizar ningún cálculo, describa físicamente qué información suministran $\phi(p)$, $|\phi(p)|^2$, $|\phi(p)|^2dp$. Prediga alrededor de qué valor de momentum estará concentrada la distribución.

**(b)** Utilice la relación de completez de la base adecuada para obtener $\psi(x)=\langle x|\psi\rangle$ a partir de $\phi(p)$. Identifique qué papel desempeña el núcleo $\langle x|p\rangle$ en esta transformación.

**(c)** Escriba la transformación inversa que permite recuperar $\phi(p)$ a partir de $\psi(x)$. Explique por qué ambas funciones representan exactamente el mismo estado físico aunque tengan formas funcionales y variables diferentes.

**(d)** Suponga que se prepara un segundo paquete con un valor de $\sigma'_p$ menor que $\sigma_p$. Sin realizar la transformada completa, prediga qué ocurrirá con la extensión espacial del paquete. Explique su razonamiento en términos de las representaciones de posición y momentum. Luego, realice el cálculo y reevalúe su predicción.

---

## 5. Espín 1/2: cambio de base frente a transformación física

Un átomo de espín 1/2 sale de un primer aparato de Stern-Gerlach preparado en el estado $|+z\rangle$. En la base de estados propios de $\hat S_x$,

$$
|+z\rangle=\frac{1}{\sqrt{2}}\left(|+x\rangle+|-x\rangle\right).
$$

Considere ahora dos procedimientos diferentes.

- **En el procedimiento I**, el experimentador no modifica físicamente el sistema y simplemente decide describir $|+z\rangle$ utilizando la base de $\hat S_x$.
- **En el procedimiento II**, sobre el espín se aplica físicamente una rotación de $\pi/2$ alrededor del eje $y$,

$$
\hat U_y\left(\frac{\pi}{2}\right)=\exp\left(-\frac{i\pi}{2\hbar}\hat S_y\right),
$$

de modo que

$$
\hat U_y\left(\frac{\pi}{2}\right)|+z\rangle=|+x\rangle.
$$

**(a)** En el procedimiento I, ¿ha cambiado el estado físico del sistema? ¿Qué ha cambiado entonces al escribir

$$
|+z\rangle=\frac{1}{\sqrt{2}}\left(|+x\rangle+|-x\rangle\right)?
$$

**(b)** Si después del procedimiento I se mide $\hat S_x$, determine los resultados posibles y sus probabilidades. Explique cómo la superposición expresada en esa base permite realizar la predicción.

**(c)** En el procedimiento II, ¿ha ocurrido solamente un cambio de representación? Compare el estado inicial $|+z\rangle$ con el estado final $|+x\rangle$ y determine qué resultado se obtiene ahora al medir $\hat S_x$.

**(d)** A partir de los dos procedimientos, explique la diferencia y la relación entre: superposición, representación, cambio de base, transformación física y medición.

Su explicación debe identificar claramente cuáles operaciones modifican el estado físico y cuáles modifican únicamente su descripción matemática.

---
---

**Fecha:** 06.11.2026, 9:00 a. m. – 11.11.2026, 8:00 p. m.  
**Profesora:** Karem Rodríguez

## Indicaciones generales

Dispone del orden de 5 días para entregar su solución individual, manuscrita y escaneada en el Campusvirtual. Puede consultar el material que considere necesario.

Responda de manera corta, concisa y asertiva cada pregunta. Para esto debe: entender la pregunta, identificar la respuesta clave, responder claramente sólo con la información necesaria, evitar detalles irrelevantes y justificar cada una de sus respuestas. En los numerales en los que se solicite una predicción, ésta debe plasmarse antes del cálculo correspondiente.

---

## 1. Espín 1: amplitudes de probabilidad y cambio de base

Un haz de átomos con espín 1 ha sido preparado en el estado

$$
|\psi\rangle=\frac{1}{\sqrt{6}}\left(2|+1\rangle_z+|0\rangle_z+i|-1\rangle_z\right),
$$

donde $\{|+1\rangle_z,|0\rangle_z,|-1\rangle_z\}$ es la base de estados propios de $\hat S_z$. Los estados propios de $\hat S_x$, expresados en la base de $\hat S_z$, son

$$
|+1\rangle_x=\frac{1}{2}\left(|+1\rangle_z+\sqrt{2}|0\rangle_z+|-1\rangle_z\right),
$$

$$
|0\rangle_x=\frac{1}{\sqrt{2}}\left(|+1\rangle_z-|-1\rangle_z\right),
$$

$$
|-1\rangle_x=\frac{1}{2}\left(|+1\rangle_z-\sqrt{2}|0\rangle_z+|-1\rangle_z\right).
$$

**(a)** Si el haz descrito por $|\psi\rangle$ atraviesa un aparato de Stern-Gerlach orientado en la dirección $z$, determine los resultados posibles y sus probabilidades. Identifique explícitamente qué cantidades en $|\psi\rangle$ son amplitudes de probabilidad y cuáles determinan probabilidades.

**(b)** Exprese el mismo ket $|\psi\rangle$ en la base de estados propios de $\hat S_x$. Obtenga los nuevos coeficientes mediante productos interiores. ¿Cuál es la matriz de transformación?

**(c)** A partir de la superposición en la nueva base, determine las probabilidades de los resultados de una medición de $\hat S_x$. Compare estas probabilidades con las obtenidas para $\hat S_z$.

**(d)** Explique, utilizando este sistema físico, la diferencia entre las siguientes afirmaciones:

- El estado es una superposición de estados propios de $\hat S_z$.
- El estado se representa en la base de $\hat S_z$ o en la base de $\hat S_x$.
- Se realiza una transformación de cambio de base.

Indique lo que cambia matemáticamente y lo que permanece físicamente inalterado entre estas tres afirmaciones.

---

## 2. Átomo de hidrógeno: observables compatibles y degeneración

Considere un átomo de hidrógeno sin incluir el espín. Los observables $\{\hat H,\hat L^2,\hat L_z\}$ forman un conjunto completo de observables compatibles y sus estados propios simultáneos se denotan por $\{|n,\ell,m\rangle\}$. Un conjunto de átomos se prepara en el estado

$$
|\psi\rangle=\frac{1}{2}\left(|2,0,0\rangle+|2,1,-1\rangle+|2,1,0\rangle+|2,1,1\rangle\right).
$$

**(a)** Si se mide únicamente la energía, ¿cuál será el resultado? ¿Permite esa medición determinar completamente el estado del átomo después de la medición? Explique la relación con la degeneración.

**(b)** Si, además de la energía, se mide $L^2$, determine los resultados posibles. Para el resultado $L^2=2\hbar^2$, explique por qué todavía no se ha identificado un único estado propio del sistema.

**(c)** Muestre qué información adicional proporciona una medición de $L_z$. Explique por qué el conjunto $\{\hat H,\hat L^2,\hat L_z\}$ es completo, mientras que $\{\hat H\}$ o $\{\hat H,\hat L^2\}$ no lo son para este problema.

**(d)** Si una medición conjunta produce los valores asociados a $|2,1,-1\rangle$, indique qué puede afirmarse inmediatamente acerca del estado después de la medición. Distinga claramente entre valor propio, estado propio, resultado de medición y probabilidad.

---

## 3. Pozo infinito unidimensional: representaciones discreta y continua

Una partícula se encuentra descrita por el estado

$$
\phi_n(x)=\sqrt{\frac{2}{L}}\sin\left(\frac{n\pi x}{L}\right),
$$

la partícula se encuentra confinada en un pozo infinito unidimensional; bajo estas circunstancias, los estados propios de energía representados en la base de coordenadas (formando una base discreta de funciones de onda) están dados por

$$
|\psi\rangle=\frac{1}{\sqrt{5}}\left(2|1\rangle+i|2\rangle\right).
$$

**(a)** En la base discreta de energía, identifique las amplitudes de probabilidad y determine las probabilidades correspondientes a una medición de la energía.

**(b)** Obtenga la representación del mismo estado en la base continua de posición, $\psi(x)=\langle x|\psi\rangle$. Explique las similitudes y diferencias entre $|\psi\rangle$ y $\psi(x)$; ¿representan dos estados diferentes?

**(c)** Distinga cuidadosamente el significado físico de $\psi(x)$, $|\psi(x)|^2$, $|\psi(x)|^2dx$, y compárelo con el significado de $c_n$, $|c_n|^2$ en la base discreta de energía.

**(d)** Escriba la probabilidad de encontrar la partícula en el intervalo $x_1<x<x_2$. Explique por qué esta probabilidad requiere una integral, mientras que la probabilidad de obtener uno de los valores discretos de energía no la requiere.

---

## 4. Partícula libre: paquete de onda en las representaciones de momentum y posición

Una partícula libre en una dimensión se prepara en un paquete de onda cuya representación en la base continua que proporciona el observable de momentum ($\hat p|p\rangle=p|p\rangle$) es

$$
\phi(p)=\frac{1}{(2\pi\sigma_p^2)^{1/4}}\exp\left[-\frac{(p-p_0)^2}{4\sigma_p^2}\right].
$$

Utilice

$$
\langle x|p\rangle=\frac{1}{\sqrt{2\pi\hbar}}e^{ipx/\hbar}.
$$

**(a)** Antes de realizar ningún cálculo, describa físicamente qué información suministran $\phi(p)$, $|\phi(p)|^2$, $|\phi(p)|^2dp$. Prediga alrededor de qué valor de momentum estará concentrada la distribución.

**(b)** Utilice la relación de completez de la base adecuada para obtener $\psi(x)=\langle x|\psi\rangle$ a partir de $\phi(p)$. Identifique qué papel desempeña el núcleo $\langle x|p\rangle$ en esta transformación.

**(c)** Escriba la transformación inversa que permite recuperar $\phi(p)$ a partir de $\psi(x)$. Explique por qué ambas funciones representan exactamente el mismo estado físico aunque tengan formas funcionales y variables diferentes.

**(d)** Suponga que se prepara un segundo paquete con un valor de $\sigma'_p$ menor que $\sigma_p$. Sin realizar la transformada completa, prediga qué ocurrirá con la extensión espacial del paquete. Explique su razonamiento en términos de las representaciones de posición y momentum. Luego, realice el cálculo y reevalúe su predicción.

---

## 5. Espín 1/2: cambio de base frente a transformación física

Un átomo de espín 1/2 sale de un primer aparato de Stern-Gerlach preparado en el estado $|+z\rangle$. En la base de estados propios de $\hat S_x$,

$$
|+z\rangle=\frac{1}{\sqrt{2}}\left(|+x\rangle+|-x\rangle\right).
$$

Considere ahora dos procedimientos diferentes.

- **En el procedimiento I**, el experimentador no modifica físicamente el sistema y simplemente decide describir $|+z\rangle$ utilizando la base de $\hat S_x$.
- **En el procedimiento II**, sobre el espín se aplica físicamente una rotación de $\pi/2$ alrededor del eje $y$,

$$
\hat U_y\left(\frac{\pi}{2}\right)=\exp\left(-\frac{i\pi}{2\hbar}\hat S_y\right),
$$

de modo que

$$
\hat U_y\left(\frac{\pi}{2}\right)|+z\rangle=|+x\rangle.
$$

**(a)** En el procedimiento I, ¿ha cambiado el estado físico del sistema? ¿Qué ha cambiado entonces al escribir

$$
|+z\rangle=\frac{1}{\sqrt{2}}\left(|+x\rangle+|-x\rangle\right)?
$$

**(b)** Si después del procedimiento I se mide $\hat S_x$, determine los resultados posibles y sus probabilidades. Explique cómo la superposición expresada en esa base permite realizar la predicción.

**(c)** En el procedimiento II, ¿ha ocurrido solamente un cambio de representación? Compare el estado inicial $|+z\rangle$ con el estado final $|+x\rangle$ y determine qué resultado se obtiene ahora al medir $\hat S_x$.

**(d)** A partir de los dos procedimientos, explique la diferencia y la relación entre: superposición, representación, cambio de base, transformación física y medición.

Su explicación debe identificar claramente cuáles operaciones modifican el estado físico y cuáles modifican únicamente su descripción matemática.