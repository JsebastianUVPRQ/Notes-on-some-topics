# Notas de clase --- Física teórica

## Espacios de Hilbert y su papel en la mecánica cuántica

**Tema:** completitud, producto interno, espacios de estados y ejemplos
de espacios adecuados e inadecuados para la formulación cuántica.

------------------------------------------------------------------------

## 1. Motivación física y matemática

En la formulación matemática estándar de la mecánica cuántica, los
estados puros se representan mediante **rayos de un espacio de Hilbert
complejo**. Los observables se describen mediante operadores
autoadjuntos y la evolución cerrada del sistema mediante operadores
unitarios (o, de manera equivalente bajo hipótesis apropiadas, mediante
un Hamiltoniano autoadjunto).

La elección de un espacio de Hilbert no es arbitraria. Su estructura
permite:

-   definir amplitudes de probabilidad mediante un producto interno;
-   definir normas y normalizar vectores de estado;
-   expresar ortogonalidad y descomposiciones en bases;
-   estudiar límites de sucesiones de estados sin salir del espacio;
-   formular rigurosamente operadores y su evolución.

**Idea central:** un espacio de Hilbert es un espacio vectorial sobre
los complejos, con producto interno, que es completo respecto de la
norma inducida por ese producto interno.

No todo objeto matemático empleado en física cuántica es, por sí mismo,
un espacio de Hilbert. También aparecen espacios de Banach, espacios de
funciones de prueba, distribuciones y álgebras de operadores. Es
importante identificar qué papel desempeña cada uno.

------------------------------------------------------------------------

## 2. Preliminares: espacios vectoriales, producto interno, norma y métrica

### 2.1 Espacio vectorial complejo

Un espacio vectorial complejo (H) es un conjunto cuyos elementos pueden
sumarse y multiplicarse por escalares de (`\mathbb `{=tex}C),
satisfaciendo los axiomas usuales de un espacio vectorial.

La elección de (`\mathbb `{=tex}C) es esencial en la formulación
ordinaria de la mecánica cuántica: permite representar fases complejas y
superposiciones con amplitudes complejas.

### 2.2 Producto interno

Un producto interno es una aplicación

\[
`\langle`{=tex}`\cdot`{=tex},`\cdot`{=tex}`\rangle`{=tex}:H`\times `{=tex}H`\longrightarrow`{=tex}`\mathbb `{=tex}C
\]

que, usando la convención de linealidad en el segundo argumento,
satisface:

1.  **Linealidad en el segundo argumento** \[
    `\langle `{=tex}x,`\alpha `{=tex}y+`\beta `{=tex}z`\rangle`{=tex}
    =`\alpha`{=tex}`\langle `{=tex}x,y`\rangle`{=tex}+`\beta`{=tex}`\langle `{=tex}x,z`\rangle`{=tex}.
    \]

2.  **Simetría conjugada** \[
    `\langle `{=tex}x,y`\rangle`{=tex}=`\overline{\langle y,x\rangle}`{=tex}.
    \]

3.  **Positividad definida** \[
    `\langle `{=tex}x,x`\rangle`{=tex}`\geq 0`{=tex},`\qquad`{=tex}
    `\langle `{=tex}x,x`\rangle=0`{=tex}`\iff `{=tex}x=0. \]

En particular, (`\langle `{=tex}x,x`\rangle`{=tex}) siempre es real y no
negativo.

> **Nota de convención:** algunos textos eligen linealidad en el primer
> argumento y conjugada-linealidad en el segundo. Ambas convenciones son
> equivalentes si se usan consistentemente.

### 2.3 Norma inducida

Todo producto interno define una norma:

\[ \|x\|=`\sqrt{\langle x,x\rangle}`{=tex}. \]

La norma mide el tamaño del vector. En mecánica cuántica, un vector de
estado normalizado satisface

\[ \|`\psi`{=tex}\|=1. \]

### 2.4 Métrica inducida

La norma induce una distancia:

\[ d(x,y)=\|x-y\|. \]

Con ella podemos definir convergencia y sucesiones de Cauchy.

------------------------------------------------------------------------

## 3. Sucesiones de Cauchy y completitud

### 3.1 Definición de sucesión de Cauchy

Una sucesión ((x_n)\_{n`\in`{=tex}`\mathbb `{=tex}N}) en (H) es de
Cauchy si

\[
`\forall`{=tex}`\varepsilon`{=tex}\>0;`\exists `{=tex}N`\in`{=tex}`\mathbb `{=tex}N
\]

tal que, para todos (m,n`\geq `{=tex}N),

\[ \|x_n-x_m\|\<`\varepsilon`{=tex}. \]

La condición expresa que los términos de la sucesión se aproximan entre
sí. No exige conocer de antemano cuál será el límite.

### 3.2 Definición formal de completitud

Un espacio con una métrica es **completo** si toda sucesión de Cauchy
converge a un elemento del propio espacio.

En particular, un espacio vectorial con producto interno (H) es completo
si

\[ `\boxed{
\forall (x_n)\subset H,\quad
(x_n)\text{ de Cauchy}
\Longrightarrow
\exists x\in H:
\lim_{n\to\infty}\|x_n-x\|=0.
}`{=tex} \]

Un espacio vectorial complejo con producto interno, completo respecto de
la norma inducida, se denomina **espacio de Hilbert**.

### 3.3 El punto sutil: el límite debe pertenecer al espacio

La completitud no significa simplemente que una sucesión tenga un límite
en algún espacio más grande. Exige que el límite esté dentro del espacio
que estamos estudiando.

Por ejemplo, (`\mathbb `{=tex}Q), con la distancia usual
(d(p,q)=\|p-q\|), no es completo. Una sucesión de racionales puede
aproximar cada vez mejor a (`\sqrt 2`{=tex}), pero su límite no es
racional.

Una sucesión concreta es

\[
1,`\quad 1.4`{=tex},`\quad 1.41`{=tex},`\quad 1.414`{=tex},`\quad`{=tex}`\ldots`{=tex}
\]

Esta sucesión es de Cauchy en (`\mathbb `{=tex}Q), pero su límite en
(`\mathbb `{=tex}R) es (`\sqrt 2`{=tex}`\notin`{=tex}`\mathbb `{=tex}Q).

**Consecuencia:** (`\mathbb `{=tex}Q) no es completo. Además, no es un
espacio vectorial sobre (`\mathbb `{=tex}C), por lo que tampoco puede
ser un espacio de Hilbert complejo.

### 3.4 Completación

Todo espacio métrico puede, bajo condiciones generales, sumergirse
densamente en un espacio métrico completo llamado su **completación**.

En el ejemplo anterior, la completación de (`\mathbb `{=tex}Q) con la
métrica usual es (`\mathbb `{=tex}R).

En análisis funcional, la completación de
(C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)) con la norma (L\^2) es
(L\^2(`\mathbb `{=tex}R)).

------------------------------------------------------------------------

## 4. ¿Qué necesita la mecánica cuántica?

Conviene separar los requisitos de un espacio de Hilbert de los
postulados físicos que se construyen sobre él.

### 4.1 Estructura del espacio de estados

En la formulación estándar:

-   El espacio de estados vectorial es complejo.
-   Posee un producto interno positivo definido.
-   Es completo respecto de la norma inducida.
-   Los estados puros físicos corresponden a rayos, no a vectores
    individuales.

Un rayo identifica todos los múltiplos complejos no nulos de un mismo
vector. En particular, los vectores normalizados (`\psi`{=tex}) y
(e\^{i`\theta`{=tex}}`\psi`{=tex}) representan el mismo estado puro,
pues difieren por una fase global.

### 4.2 Normalización y probabilidades

Un vector que representa un estado puro puede elegirse normalizado:

\[ `\langle`{=tex}`\psi`{=tex},`\psi`{=tex}`\rangle=1`{=tex}. \]

Si ({`\phi`{=tex}\_n}) es una base ortonormal completa, los coeficientes
de expansión son amplitudes:

\[ `\psi`{=tex}=`\sum`{=tex}\_n c_n`\phi`{=tex}\_n,`\qquad`{=tex}
c_n=`\langle`{=tex}`\phi`{=tex}\_n,`\psi`{=tex}`\rangle`{=tex}. \]

En el caso discreto, la regla de Born asigna probabilidades

\[ P(n)=\|c_n\|\^2, `\qquad`{=tex} `\sum`{=tex}\_n \|c_n\|\^2=1. \]

En espectros continuos, la formulación requiere la teoría espectral y,
en ocasiones, el formalismo de espacios de Hilbert equipados.

### 4.3 Observables y operadores

En la formulación estándar, los observables se representan mediante
operadores autoadjuntos. En dimensión infinita, muchos de estos
operadores son **no acotados** y tienen un dominio propio, que debe
especificarse.

No basta con decir que un operador es una matriz o una transformación
lineal: para operadores no acotados, las cuestiones de dominio, cierre y
autoadjunción son esenciales.

### 4.4 Evolución temporal

Para un sistema cerrado, la evolución temporal se representa mediante
operadores unitarios:

\[ U(t)\^`\dagger `{=tex}U(t)=I. \]

Si el Hamiltoniano (H) es autoadjunto y no depende explícitamente del
tiempo, formalmente

\[ U(t)=e\^{-iHt/`\hbar`{=tex}}. \]

La autoadjunción del Hamiltoniano es la condición matemática que permite
definir rigurosamente el grupo unitario de evolución mediante el teorema
de Stone.

### 4.5 ¿La separabilidad es obligatoria?

No. Un espacio de Hilbert es separable si posee un subconjunto denso
numerable. La separabilidad se cumple en muchos modelos físicos
habituales, como (L^2(`\mathbb `{=tex}R^n)) y
(`\ell`{=tex}\^2(`\mathbb `{=tex}N)), y es una hipótesis frecuente en
tratamientos estándar.

Sin embargo, **la separabilidad no forma parte de la definición de
espacio de Hilbert** y no es una condición universal necesaria para toda
formulación cuántica posible.

### 4.6 Estados mixtos

No todos los estados cuánticos se describen mediante un vector puro. Los
estados mixtos se representan mediante operadores de densidad
(`\rho`{=tex}), que satisfacen

\[
`\rho`{=tex}`\geq 0`{=tex},`\qquad `{=tex}`\operatorname{Tr}`{=tex}(`\rho`{=tex})=1.
\]

Por tanto, el espacio de Hilbert es la estructura fundamental para los
estados puros, mientras que los estados mixtos requieren además el
formalismo de operadores de densidad.

------------------------------------------------------------------------

## 5. Espacios que sí satisfacen las condiciones: ejemplos

### 5.1 Espacio finito-dimensional (`\mathbb `{=tex}C\^2): un qubit

Consideremos

\[ H=`\mathbb `{=tex}C\^2. \]

Sus vectores tienen la forma

\[ `\psi`{=tex}=
```{=tex}
\begin{pmatrix}
a\\b
\end{pmatrix}
```
, `\qquad `{=tex}a,b`\in`{=tex}`\mathbb `{=tex}C. \]

El producto interno usual es

\[ `\langle`{=tex}`\phi`{=tex},`\psi`{=tex}`\rangle`{=tex}
=`\overline{c}`{=tex}a+`\overline{d}`{=tex}b, \]

si (`\phi`{=tex}=(c,d)\^T) y (`\psi`{=tex}=(a,b)\^T).

La norma inducida es

\[ \|`\psi`{=tex}\|=`\sqrt{|a|^2+|b|^2}`{=tex}. \]

Como todo espacio vectorial normado de dimensión finita sobre
(`\mathbb `{=tex}C) es completo, (`\mathbb `{=tex}C\^2) es un espacio de
Hilbert.

Un estado normalizado puede escribirse como

\[
\|`\psi`{=tex}`\rangle`{=tex}=a\|0`\rangle`{=tex}+b\|1`\rangle`{=tex},
`\qquad `{=tex}\|a\|^2+\|b\|^2=1. \]

**Aplicación:** sistemas de dos niveles, como el espín (1/2) o un qubit
ideal.

El ejemplo se generaliza a (`\mathbb `{=tex}C\^n), que también es un
espacio de Hilbert con el producto interno usual.

### 5.2 Espacio (`\ell`{=tex}\^2(`\mathbb `{=tex}N)): sucesiones cuadrado-sumables

Definimos

\[ `\ell`{=tex}\^2(`\mathbb `{=tex}N)=
`\left`{=tex}{a=(a_1,a_2,`\ldots`{=tex}):
`\sum`{=tex}\_{n=1}^{`\infty`{=tex}}\|a_n\|^2\<`\infty`{=tex}
`\right`{=tex}}. \]

El producto interno es

\[ `\langle `{=tex}a,b`\rangle`{=tex}
=`\sum`{=tex}\_{n=1}\^{`\infty`{=tex}}`\overline{a_n}`{=tex}b_n, \]

y la norma es

\[ \|a\|*2=
`\left`{=tex}(`\sum`{=tex}*{n=1}^{`\infty`{=tex}}\|a_n\|^2`\right`{=tex})\^{1/2}.
\]

Este espacio es completo y separable; por tanto, es un espacio de
Hilbert.

Un vector normalizado puede representarse como

\[
\|`\psi`{=tex}`\rangle`{=tex}=`\sum`{=tex}*{n=1}\^{`\infty`{=tex}}a_n\|n`\rangle`{=tex},
`\qquad`{=tex} `\sum`{=tex}*{n=1}^{`\infty`{=tex}}\|a_n\|^2=1. \]

**Aplicación:** sistemas con una base ortonormal numerable, por ejemplo,
modelos con niveles discretos de energía.

### 5.3 Espacio (L\^2(`\mathbb `{=tex}R)): funciones de onda

Definimos

\[ L\^2(`\mathbb `{=tex}R)=
`\left`{=tex}{`\psi`{=tex}:`\mathbb `{=tex}R`\to`{=tex}`\mathbb `{=tex}C:
`\int`{=tex}\_{`\mathbb `{=tex}R}\|`\psi`{=tex}(x)\|\^2,dx\<`\infty`{=tex}
`\right`{=tex}}. \]

Más precisamente, sus elementos son clases de equivalencia de funciones
que coinciden casi en todas partes. Esto evita distinguir funciones que
solo difieren en un conjunto de medida cero.

El producto interno es

\[ `\langle`{=tex}`\phi`{=tex},`\psi`{=tex}`\rangle`{=tex}
=`\int`{=tex}\_{`\mathbb `{=tex}R}`\overline{\phi(x)}`{=tex}`\psi`{=tex}(x),dx,
\]

y la norma inducida es

\[ \|`\psi`{=tex}\|*2=
`\left`{=tex}(`\int`{=tex}*{`\mathbb `{=tex}R}\|`\psi`{=tex}(x)\|^2,dx`\right`{=tex})^{1/2}.
\]

El espacio (L\^2(`\mathbb `{=tex}R)) es completo y separable, así que es
un espacio de Hilbert.

Para un estado normalizado,

\[ `\int`{=tex}\_{`\mathbb `{=tex}R}\|`\psi`{=tex}(x)\|\^2,dx=1. \]

La regla de Born asigna a una región medible
(A`\subseteq`{=tex}`\mathbb `{=tex}R) la probabilidad

\[ P(A)=`\int`{=tex}\_A\|`\psi`{=tex}(x)\|\^2,dx. \]

**Aplicación:** descripción de la función de onda de una partícula no
relativista en una dimensión.

No toda función de (L\^2) tiene que ser continua o diferenciable. La
pertenencia a (L\^2) solo exige integrabilidad cuadrática. Las
condiciones adicionales de regularidad aparecen al estudiar dominios de
operadores como el momento o el Hamiltoniano.

La construcción se generaliza a (L^2(`\mathbb `{=tex}R^n)),
(L\^2(`\Omega`{=tex})) y otros espacios de medida apropiados.

### 5.4 Espacio de Fock bosónico

Para describir sistemas con número variable de partículas, se utiliza el
espacio de Fock bosónico:

\[ `\mathcal `{=tex}F_s(H)=
`\bigoplus`{=tex}\_{n=0}^{`\infty`{=tex}}H^{`\otimes`{=tex}\_s n}. \]

Aquí (H\^{`\otimes`{=tex}\_s n}) es el producto tensorial de (n) copias
de (H), restringido al subespacio simétrico. La simetría corresponde a
la estadística bosónica. El sector (n=0) representa el vacío.

Un elemento se expresa como

\[
`\Psi`{=tex}=(`\psi`{=tex}\_0,`\psi`{=tex}\_1,`\psi`{=tex}\_2,`\ldots`{=tex}),
\]

con

\[
\|`\Psi`{=tex}\|\^2=`\sum`{=tex}\_{n=0}\^{`\infty`{=tex}}\|`\psi`{=tex}\_n\|\^2\<`\infty`{=tex}.
\]

La suma directa hilbertiana de espacios de Hilbert es nuevamente un
espacio de Hilbert. Por tanto, el espacio de Fock bosónico es completo
con el producto interno inducido.

**Aplicación:** óptica cuántica y teorías cuánticas de campos con
partículas bosónicas.

Existe una construcción análoga para fermiones, usando productos
tensoriales antisimétricos.

------------------------------------------------------------------------

## 6. Espacios que no cumplen las condiciones de Hilbert

Un espacio puede fallar por razones distintas:

1.  puede no ser completo;
2.  puede ser completo, pero su norma no proceder de un producto
    interno;
3.  puede no tener estructura de espacio vectorial complejo;
4.  puede ser un espacio de Hilbert, pero un objeto particular que se
    quiera usar como estado puede no pertenecer a él.

Estos casos no deben confundirse.

### 6.1 (C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)) con la norma (L\^2): falta de completitud

Sea (C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)) el espacio de funciones
infinitamente diferenciables y de soporte compacto.

Podemos definir el producto interno

\[ `\langle `{=tex}f,g`\rangle`{=tex}
=`\int`{=tex}\_{`\mathbb `{=tex}R}`\overline{f(x)}`{=tex}g(x),dx. \]

La norma inducida es la norma (L\^2). Sin embargo,
(C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)) no es completo respecto de
ella.

Para verlo, consideremos una función
(f`\in `{=tex}L\^2(`\mathbb `{=tex}R)) con soporte compacto que no sea
suave; por ejemplo, la función indicadora de un intervalo:

\[ f(x)=`\mathbf 1`{=tex}\_{\[0,1\]}(x). \]

Existen funciones
(f_n`\in `{=tex}C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)) que aproximan a
(f) en norma (L\^2):

\[ \|f_n-f\|\_2`\longrightarrow 0`{=tex}. \]

Por ello, ((f_n)) es de Cauchy en
(C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)), pero su límite (f), entendido
como elemento de (L\^2), no pertenece a
(C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)).

Así,

\[ `\boxed{C_c^\infty(\mathbb R)
\text{ no es completo en la norma }L^2.}`{=tex} \]

Su completación es (L\^2(`\mathbb `{=tex}R)).

**Importancia física:** las funciones suaves de soporte compacto son muy
útiles como funciones de prueba y como dominios iniciales de operadores
diferenciales. Que no formen por sí solas un espacio de Hilbert no las
vuelve inútiles.

### 6.2 (C(\[0,1\])) con la norma supremo: completitud sin producto interno compatible

Sea (C(\[0,1\])) el espacio de funciones continuas sobre el intervalo
cerrado (\[0,1\]), con norma

\[ \|f\|*`\infty`{=tex}=`\max`{=tex}*{x`\in[0,1]`{=tex}}\|f(x)\|. \]

Este espacio es completo: es un espacio de Banach. Sin embargo, la norma
supremo no procede de un producto interno.

Una norma inducida por un producto interno debe satisfacer la
**identidad del paralelogramo**:

\[ \|f+g\|^2+\|f-g\|^2 =2\|f\|^2+2\|g\|^2. \]

Tomemos

\[ f(x)=1,`\qquad `{=tex}g(x)=x. \]

Entonces,

\[ \|f\|*`\infty=1`{=tex},`\qquad `{=tex}\|g\|*`\infty=1`{=tex}, \]

\[ \|f+g\|*`\infty=2`{=tex},`\qquad`{=tex} \|f-g\|*`\infty=1`{=tex}. \]

El lado izquierdo de la identidad vale

\[ 2^2+1^2=5, \]

mientras que el derecho vale

\[ 2(1)^2+2(1)^2=4. \]

Como (5`\neq4`{=tex}), la identidad falla. Por tanto, esta norma no
puede ser inducida por ningún producto interno.

**Conclusión:** (C(\[0,1\])), con la norma supremo, es un espacio de
Banach, pero no un espacio de Hilbert con esa norma.

### 6.3 (L\^1(\[0,1\])) con la norma (L\^1): otro espacio de Banach que no es Hilbert

Consideremos

\[ L\^1(\[0,1\])=
`\left`{=tex}{f:`\int`{=tex}\_0\^1\|f(x)\|,dx\<`\infty`{=tex}`\right`{=tex}},
\]

con norma

\[ \|f\|\_1=`\int`{=tex}\_0\^1\|f(x)\|,dx. \]

Este espacio es completo, pero su norma no procede de un producto
interno.

Para demostrarlo, tomemos

\[ f(x)=1,`\qquad `{=tex}g(x)=1-2x. \]

Calculamos:

\[ \|f\|\_1=1, `\qquad`{=tex}
\|g\|\_1=`\int`{=tex}\_0\^1\|1-2x\|,dx=`\frac12`{=tex}. \]

Además,

\[ \|f+g\|\_1 =`\int`{=tex}\_0\^1\|2-2x\|,dx=1, \]

y

\[ \|f-g\|\_1 =`\int`{=tex}\_0\^1\|2x\|,dx=1. \]

Por tanto, el lado izquierdo de la identidad del paralelogramo es

\[ \|f+g\|\_1\^2+\|f-g\|\_1\^2=1+1=2, \]

mientras que el lado derecho es

\[ 2\|f\|\_1\^2+2\|g\|\_1\^2 =2+`\frac12`{=tex}=`\frac52`{=tex}. \]

La identidad falla. Así, la norma (L\^1) no es inducida por un producto
interno.

**Conclusión:** (L\^1(\[0,1\])) es un espacio de Banach, pero no un
espacio de Hilbert con su norma usual.

### 6.4 (`\mathbb `{=tex}Q) con la distancia usual: falta de completitud y de estructura compleja

Los racionales con la distancia usual no son completos, como muestra la
sucesión racional que converge a (`\sqrt 2`{=tex}).

Además, (`\mathbb `{=tex}Q) no es un espacio vectorial sobre
(`\mathbb `{=tex}C). Por tanto, falla tanto la condición de completitud
como la estructura escalar requerida para el espacio de Hilbert complejo
de la formulación estándar.

### 6.5 Ondas planas y estados generalizados: objetos que no pertenecen a (L\^2)

Consideremos la onda plana

\[ `\psi`{=tex}\_k(x)=e\^{ikx}. \]

Su módulo es constante:

\[ \|`\psi`{=tex}\_k(x)\|\^2=1. \]

Por tanto,

\[
`\int`{=tex}\_{-`\infty`{=tex}}\^{`\infty`{=tex}}\|`\psi`{=tex}\_k(x)\|\^2,dx
=`\infty`{=tex}. \]

Así, (`\psi`{=tex}\_k`\notin `{=tex}L\^2(`\mathbb `{=tex}R)). No es un
vector normalizable del espacio de Hilbert usual de una partícula en la
recta.

Sin embargo, las ondas planas son herramientas importantes para
representar estados de momento definido y para desarrollar la teoría
espectral. Se interpretan rigurosamente como **autovectores
generalizados**, dentro de un marco ampliado.

Un marco habitual es la terna de Gelfand o **espacio de Hilbert
equipado**:

\[ `\Phi`{=tex}`\subset `{=tex}H`\subset`{=tex}`\Phi`{=tex}', \]

donde:

-   (`\Phi`{=tex}) es un espacio de funciones de prueba, con topología
    más fina;
-   \(H\) es el espacio de Hilbert;
-   (`\Phi`{=tex}') es un espacio dual adecuado de distribuciones.

En este formalismo, ciertos objetos como las ondas planas pueden
entenderse como elementos de (`\Phi`{=tex}'), aunque no pertenezcan a
(H).

**Advertencia conceptual:** que una onda plana no pertenezca a
(L\^2(`\mathbb `{=tex}R)) no significa que la teoría cuántica sea
inconsistente. Significa que el objeto es generalizado y requiere un
marco matemático más amplio.

------------------------------------------------------------------------

## 7. Tabla comparativa

  ----------------------------------------------------------------------------------------------------
  Espacio y estructura                                ¿Completo?  ¿Producto interno          ¿Hilbert?
                                                                  compatible con la 
                                                                         estructura 
                                                                          indicada? 
  ------------------------------------------- ------------------ ------------------ ------------------
  (`\mathbb `{=tex}C\^n), producto interno                    Sí                 Sí                 Sí
  usual                                                                             

  (`\ell`{=tex}\^2(`\mathbb `{=tex}N)),                       Sí                 Sí                 Sí
  producto interno usual                                                            

  (L\^2(`\mathbb `{=tex}R)), producto interno                 Sí                 Sí                 Sí
  integral                                                                          

  Espacio de Fock, producto interno inducido                  Sí                 Sí                 Sí

  (C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)),                   No                 Sí                 No
  norma (L\^2)                                                                      

  (C(\[0,1\])), norma supremo                                 Sí                 No                 No

  (L\^1(\[0,1\])), norma (L\^1)                               Sí                 No                 No

  (`\mathbb `{=tex}Q), distancia usual                        No           No tiene                 No
                                                                         estructura 
                                                                           compleja 
  ----------------------------------------------------------------------------------------------------

**Observación:** la clasificación depende de la estructura elegida. Un
mismo espacio vectorial puede admitir distintas normas o productos
internos. La tabla se refiere exclusivamente a las estructuras
especificadas.

------------------------------------------------------------------------

## 8. Síntesis: por qué la completitud es importante

La completitud permite garantizar que los límites de sucesiones de
Cauchy permanecen dentro del espacio. Esta propiedad es fundamental en
análisis funcional, en la teoría espectral y en la construcción rigurosa
de la mecánica cuántica.

Sin embargo, no debe confundirse la completitud con todas las
condiciones necesarias para una teoría cuántica:

-   La completitud, por sí sola, no proporciona amplitudes de
    probabilidad.
-   Un producto interno proporciona normas, ortogonalidad y amplitudes.
-   La estructura compleja permite superposiciones con fases complejas.
-   Los operadores autoadjuntos proporcionan el marco para los
    observables.
-   Los operadores unitarios describen la evolución que conserva la
    norma.
-   La regla de Born conecta el formalismo matemático con las
    probabilidades experimentales.

La afirmación correcta es:

\[ `\boxed{
\text{Espacio de Hilbert}
=
\text{espacio vectorial complejo}
+
\text{producto interno}
+
\text{completitud}.
}`{=tex} \]

La mecánica cuántica estándar utiliza esta estructura para representar
estados puros, pero la teoría completa también necesita operadores,
dominios, reglas probabilísticas y, para estados mixtos, operadores de
densidad.

------------------------------------------------------------------------

## 9. Preguntas de comprobación

1.  ¿Por qué la condición de Cauchy no garantiza por sí sola que una
    sucesión tenga límite dentro del espacio?
2.  ¿Cuál es la diferencia entre un espacio de Banach y un espacio de
    Hilbert?
3.  ¿Por qué la identidad del paralelogramo permite comprobar si una
    norma procede de un producto interno?
4.  ¿Por qué (C_c\^`\infty`{=tex}(`\mathbb `{=tex}R)) puede ser útil en
    mecánica cuántica aunque no sea completo en la norma (L\^2)?
5.  ¿Por qué una onda plana no pertenece a (L\^2(`\mathbb `{=tex}R)), y
    cómo se maneja en el formalismo de espacios de Hilbert equipados?
6.  ¿La separabilidad forma parte de la definición de espacio de
    Hilbert?
7.  ¿Por qué un observable no acotado requiere especificar su dominio?

## 10. Bibliografía recomendada

-   John von Neumann, *Mathematical Foundations of Quantum Mechanics*.
    Obra clásica sobre la formulación matemática de la mecánica
    cuántica.
-   Michael Reed y Barry Simon, *Methods of Modern Mathematical Physics,
    Vol. I: Functional Analysis*. Referencia de análisis funcional
    aplicada a física matemática.
-   Brian C. Hall, *Quantum Theory for Mathematicians*. Desarrollo
    matemático de la teoría cuántica.
-   Gerald B. Folland, *A Course in Abstract Harmonic Analysis*.
    Referencia para herramientas de análisis funcional y armónico.
-   J. J. Sakurai y Jim Napolitano, *Modern Quantum Mechanics*.
    Introducción al formalismo de estados, observables y evolución
    cuántica.

------------------------------------------------------------------------

**Fin de las notas.**
