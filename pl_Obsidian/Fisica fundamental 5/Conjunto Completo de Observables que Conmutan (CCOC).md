
Para entender el concepto de **Conjunto Completo de Observables que Conmutan (CCOC)** y su aplicación en problemas como el 28, es necesario dominar varios conceptos fundamentales de la mecánica cuántica y el álgebra lineal. A continuación, se presenta una explicación detallada de la teoría matemática y conceptual involucrada.

---

## 1. Conceptos básicos

### 1.1 Observables y operadores hermíticos
- Un **observable** en mecánica cuántica es un operador lineal $\hat{A}$ que actúa sobre el espacio de Hilbert $\mathcal{H}$ y que es **hermítico** (autoadjunto): $\hat{A}^\dagger = \hat{A}$. Esto garantiza que sus autovalores son reales (posibles resultados de medición) y que sus autoestados forman una base (completa) del espacio (en caso de espectro discreto).

### 1.2 Conmutador y compatibilidad
- Dos observables $\hat{A}$ y $\hat{B}$ son **compatibles** si su conmutador es nulo: $[\hat{A}, \hat{B}] = \hat{A}\hat{B} - \hat{B}\hat{A} = 0$. Esto implica que pueden ser medidos simultáneamente con precisión arbitraria y que existe una base de autoestados comunes.

### 1.3 Degeneración
- Un autovalor $a$ de $\hat{A}$ es **degenerado** si existen al menos dos vectores linealmente independientes $|\psi_1\rangle, |\psi_2\rangle$ tales que $\hat{A}|\psi_i\rangle = a|\psi_i\rangle$. El conjunto de todos estos vectores forma un **subespacio propio** de dimensión mayor que 1. En tal caso, conocer el autovalor $a$ no identifica unívocamente un estado; se necesita información adicional.

---

## 2. Teorema de diagonalización simultánea

Si $\hat{A}$ y $\hat{B}$ son hermíticos y conmutan, entonces existe una base ortonormal de $\mathcal{H}$ formada por vectores que son autoestados de ambos operadores. Es decir, se pueden diagonalizar simultáneamente. Esto se extiende a cualquier colección finita de operadores que conmutan entre sí.

**Interpretación**: Los autovalores de estos operadores proporcionan "etiquetas" que pueden usarse para caracterizar los estados de la base. Sin embargo, si alguno de los operadores tiene degeneración, puede que las etiquetas no sean suficientes para distinguir todos los estados.

---

## 3. Definición de CCOC

Un **Conjunto Completo de Observables que Conmutan** (CCOC) es una colección $\{\hat{A}_1, \hat{A}_2, \dots, \hat{A}_k\}$ de observables hermíticos que satisfacen:

1. **Conmutatividad**: Todos los operadores del conjunto conmutan entre sí: $[\hat{A}_i, \hat{A}_j] = 0$ para todo $i,j$.
2. **Completitud**: La especificación de los autovalores de todos ellos (es decir, una tupla $(a_1, a_2, \dots, a_k)$) determina unívocamente un vector (salvo una fase global) en el espacio de Hilbert. En otras palabras, el subespacio de vectores que son autoestados comunes con esos autovalores es unidimensional.

Equivalentemente, la base de autoestados comunes está etiquetada de manera única por los autovalores conjuntos, sin que exista degeneración residual.

---

## 4. ¿Por qué es importante?

- **Identificación de estados**: Los autovalores de un CCOC constituyen un conjunto completo de números cuánticos que caracterizan por completo un estado cuántico. Por ejemplo, en el átomo de hidrógeno, el CCOC suele ser $\{\hat{H}, \hat{L}^2, \hat{L}_z\}$ (energía, momento angular total y su proyección), cuyos autovalores $(n, \ell, m)$ etiquetan cada estado ligado.
- **Medición simultánea**: Si se mide un CCOC, se obtiene la máxima información posible sobre el sistema sin ambigüedad.
- **Simplificación de problemas**: En sistemas con simetrías, encontrar un CCOC que incluya al hamiltoniano permite resolver la ecuación de Schrödinger mediante separación de variables.

---

## 5. Ejemplo en el Problema 28

El espacio es tridimensional con base $\{|\varphi_1\rangle, |\varphi_2\rangle, |\varphi_3\rangle\}$. Se tienen:

- $\hat{H}_0 = \hbar\omega_0(|\varphi_1\rangle\langle\varphi_1| - |\varphi_2\rangle\langle\varphi_2| - |\varphi_3\rangle\langle\varphi_3|)$
- $\hat{A} = a(|\varphi_1\rangle\langle\varphi_1| + |\varphi_2\rangle\langle\varphi_3| + |\varphi_3\rangle\langle\varphi_2|)$

### Análisis de cada conjunto propuesto:

#### a) $\{\hat{H}_0\}$
- $\hat{H}_0$ es diagonal en la base dada: autovalores $\hbar\omega_0$ (no degenerado) y $-\hbar\omega_0$ (doble degeneración, asociado a $|\varphi_2\rangle$ y $|\varphi_3\rangle$).
- No es CCOC porque el autovalor $-\hbar\omega_0$ no distingue entre los dos estados.

#### b) $\{\hat{A}\}$
- En la base $\{|\varphi_1\rangle, |\varphi_2\rangle, |\varphi_3\rangle\}$, $\hat{A}$ tiene matriz:
  $$
  \begin{pmatrix}
  a & 0 & 0 \\
  0 & 0 & a \\
  0 & a & 0
  \end{pmatrix}
  $$
  Sus autovalores: $a$ (doble degeneración) y $-a$ (no degenerado). Los autoestados para $a$ son $|\varphi_1\rangle$ y $\frac{1}{\sqrt{2}}(|\varphi_2\rangle + |\varphi_3\rangle)$; para $-a$ es $\frac{1}{\sqrt{2}}(|\varphi_2\rangle - |\varphi_3\rangle)$.
- No es CCOC por la degeneración en $a$.

#### c) $\{\hat{H}_0, \hat{A}\}$
- Ya se verificó que conmutan. Busquemos autoestados comunes:
  - $|\varphi_1\rangle$: $\hat{H}_0$ da $\hbar\omega_0$, $\hat{A}$ da $a$.
  - $\frac{1}{\sqrt{2}}(|\varphi_2\rangle + |\varphi_3\rangle)$: $\hat{H}_0$ da $-\hbar\omega_0$, $\hat{A}$ da $a$.
  - $\frac{1}{\sqrt{2}}(|\varphi_2\rangle - |\varphi_3\rangle)$: $\hat{H}_0$ da $-\hbar\omega_0$, $\hat{A}$ da $-a$.
- Los pares de autovalores son distintos: $(\hbar\omega_0, a)$, $(-\hbar\omega_0, a)$, $(-\hbar\omega_0, -a)$. Cada par corresponde a un único estado (salvo fase). Por tanto, **sí es un CCOC**.

#### d) $\{\hat{H}_0^2, \hat{A}\}$
- $\hat{H}_0^2 = (\hbar\omega_0)^2 \hat{I}$ (identidad). Todos los estados tienen el mismo autovalor para $\hat{H}_0^2$. Luego, el conjunto equivale a $\{\hat{A}\}$, que ya vimos que es degenerado. No es CCOC.

---

## 6. Resumen de condiciones para un CCOC

- Los operadores deben conmutar.
- Los autoespacios comunes deben ser unidimensionales.
- En espacios de dimensión finita, esto equivale a que la representación espectral conjunta no tenga degeneración.
- Si hay degeneración, se necesitan más observables que la levanten.

---

## 7. Conexión con otros problemas

En el Problema 29, la paridad $\hat{\Pi}$ conmuta con un hamiltoniano par. Si el hamiltoniano es no degenerado, entonces cada autoestado tiene paridad definida, y el conjunto $\{\hat{H}, \hat{\Pi}\}$ podría ser un CCOC (dependiendo de si hay degeneración accidental). En general, la paridad ayuda a clasificar estados.

En el Problema 30, el potencial par también implica que los estados tienen paridad definida, lo que es consecuencia de la conmutación con $\hat{\Pi}$.

---

Esta base teórica permite abordar problemas donde se requiere identificar si un conjunto de observables es completo, y entender cómo los números cuánticos surgen de la estructura algebraica de los operadores.