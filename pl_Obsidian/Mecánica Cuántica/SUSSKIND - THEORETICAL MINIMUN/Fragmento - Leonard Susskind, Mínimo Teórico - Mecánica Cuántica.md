# Lección 1

# Sistemas y Experimentos

### 1.1 La Mecánica Cuántica es Diferente

¿Qué tiene de especial la mecánica cuántica? ¿Por qué es tan difícil de entender? Sería fácil culpar a las "matemáticas duras", y puede que haya algo de verdad en esa idea. Pero eso no puede ser todo. Muchos no físicos son

   

2 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

capaces de dominar la mecánica clásica y la teoría de campos, que también requieren matemáticas complejas.

La mecánica cuántica trata el comportamiento de objetos tan pequeños que los humanos estamos mal equipados para visualizarlos en absoluto. Los átomos individuales están cerca del extremo superior de esta escala en términos de tamaño. Los electrones se utilizan con frecuencia como objetos de estudio. Nuestros órganos sensoriales simplemente no están hechos para percibir el movimiento de un electrón. Lo mejor que podemos hacer es intentar comprender los electrones y su movimiento como abstracciones matemáticas.

"¿Y qué?", dice el escéptico. "La mecánica clásica está repleta de abstracciones matemáticas: masas puntuales, cuerpos rígidos, marcos de referencia inerciales, posiciones, momentos, campos, ondas... la lista continúa. No hay nada nuevo en las abstracciones matemáticas." Este es en realidad un punto justo, y de hecho los mundos clásico y cuántico tienen algunas cosas importantes en común. Sin embargo, la mecánica cuántica es diferente en dos aspectos:

1.  **Diferentes Abstracciones.** Las abstracciones cuánticas son fundamentalmente diferentes de las clásicas. Por ejemplo, veremos que la idea de un estado en mecánica cuántica es conceptualmente muy diferente de su contraparte clásica. Los estados se representan mediante objetos matemáticos diferentes y tienen una estructura lógica diferente.

2.  **Estados y Mediciones.** En el mundo clásico, la relación entre el estado de un sistema y el resultado de una medición sobre ese sistema es muy directa. De hecho, es trivial. Las etiquetas que describen

    ESPINES Y CÚBITS

un estado (la posición y el momento de una partícula, por ejemplo) son las mismas etiquetas que caracterizan las mediciones de ese estado. Dicho de otra manera, se puede realizar un experimento para determinar el estado de un sistema. En el mundo cuántico, esto no es cierto. Los estados y las mediciones son dos cosas diferentes, y la relación entre ellos es sutil y no intuitiva.

Estas ideas son cruciales, y volveremos a ellas una y otra vez.

### 1.2 Espines y Cúbits

El concepto de espín deriva de la física de partículas. Las partículas tienen propiedades además de su ubicación en el espacio. Por ejemplo, pueden tener o no carga eléctrica, o masa. Un electrón no es lo mismo que un quark o un neutrino. Pero incluso un tipo específico de partícula, como un electrón, no está completamente especificado por su ubicación. Al electrón se le atribuye un grado de libertad adicional llamado su espín. Ingenuamente, el espín puede imaginarse como una pequeña flecha que apunta en alguna dirección, pero esa imagen ingenua es demasiado clásica para representar con precisión la situación real. El espín de un electrón es tan cuántico como un sistema puede ser, y cualquier intento de visualizarlo clásicamente fallará estrepitosamente.

Podemos y abstraeremos la idea de un espín, y olvidaremos que está adherido a un electrón. El espín cuántico es un sistema que puede estudiarse por derecho propio. De hecho, el espín cuántico, aislado del electrón que lo lleva

   CCIÓN 1. SISTEMAS Y EXPERIMENTOS

a través del espacio, es a la vez el más simple y el más cuántico de los sistemas.

El espín cuántico aislado es un ejemplo de la clase general de sistemas simples que llamamos cúbits (quantum bits), que juegan el mismo papel en el mundo cuántico que los bits lógicos juegan al definir el estado de tu ordenador. Muchos sistemas – quizás incluso todos los sistemas – pueden construirse combinando cúbits. Así, al aprender sobre ellos, estamos aprendiendo sobre mucho más.

### 1.3 Un Experimento

Concretemos estas ideas, utilizando el ejemplo más simple que podamos encontrar. En la primera lección del Volumen I, comenzamos discutiendo un sistema determinista muy simple: una moneda que puede mostrar cara $(C)$ o cruz $(X)$. Podemos llamar a esto un sistema de dos estados, o un bit, con los dos estados siendo $C$ y $X$. Más formalmente, inventamos un "grado de libertad" llamado $\sigma$ que puede tomar dos valores, a saber $+1$ y $-1$. $l$ estado $C$ es reemplazado por

$$\sigma = +1$$

y el estado $X$ por

$$\sigma = -1.$$

Clásicamente, eso es todo lo que hay en el espacio de estados. El sistema está en el estado $\sigma = +1$ o $\sigma = -1$ y no hay


nada intermedio. En mecánica cuántica, pensaremos en este sistema como un cúbit.

El Volumen $I$ también discutió leyes de evolución simples que nos dicen cómo actualizar el estado de un instante a otro. La ley más simple es simplemente que nada cambia. En ese caso, si vamos de un instante discreto $(n)$ al siguiente $(n + 1)$, la ley de evolución es

$$\sigma (n + 1) = \sigma (n). \quad (1.1)$$

Revelemos una suposición oculta que descuidamos en el Volumen $I$. Un experimento implica más que solo un sistema a estudiar. También implica un aparato $\mathcal{A}$ para realizar mediciones y registrar los resultados de las mediciones. En el caso del sistema de dos estados, el aparato interactúa con el sistema (el espín) y registra el valor de $\sigma$. Piensa en el aparato como una caja negra $^{1}$ con una ventana que muestra el resultado de una medición. También hay una flecha de "este lado hacia arriba" en el aparato. La flecha hacia arriba es importante porque muestra cómo está orientado el aparato en el espacio, y su dirección afectará los resultados de nuestras mediciones. Comenzamos apuntándolo a lo largo del eje $z$ (Fig. 1.1). Inicialmente, no tenemos conocimiento de si $\sigma = +1$ o $\sigma = -1$. Nuestro propósito es hacer un experimento para averiguar el valor de $\sigma$.

Antes de que el aparato interactúe con el espín, la ventana está en blanco (etiquetada con un signo de interrogación en nuestros diagramas). Después de que mide $\sigma$, la ventana muestra un $+1$ o un $-1$. Al
mirar el aparato, determinamos el valor de $\sigma$. Todo ese proceso constituye un experimento muy simple diseñado para medir $\sigma$.

Ahora que hemos medido $\sigma$, reiniciemos el aparato a neutral y, sin perturbar el espín, midamos $\sigma$ nuevamente. Asumiendo la ley simple de la Ec. 1.1, deberíamos obtener la misma respuesta que la primera vez. El resultado $\sigma = +1$ será

seguido de $\sigma = +1$. Igualmente para $\sigma = -1$. Lo mismo será cierto para cualquier número de repeticiones. Esto es bueno porque nos permite confirmar el resultado de un experimento. También podemos decirlo de la siguiente manera: La primera interacción con el aparato $\mathcal{A}$ prepara el sistema en uno de los dos estados. Experimentos subsiguientes confirman ese estado. Hasta ahora, no hay diferencia entre la física clásica y la cuántica.

 Figura 1.2: El aparato se voltea sin perturbar el espín previamente medido. Una nueva medición da como resultado $\sigma_{z} = -1$.  

Ahora hagamos algo nuevo. Después de preparar el espín midiéndolo con $\mathcal{A}$, volteamos el aparato boca abajo y luego medimos $\sigma$ nuevamente (Fig. 1.2). Lo que encontramos es que si preparamos originalmente $\sigma = +1$, el aparato invertido registra $\sigma = -1$. De manera similar, si preparamos originalmente $\sigma = -1$, el aparato invertido registra $\sigma = +1$. En otras palabras,

   ear el aparato intercambia $\sigma = +1$ y $\sigma = -1$. De estos resultados, podríamos concluir que $\sigma$ es un grado de libertad que está asociado con un sentido de dirección en el espacio. Por ejemplo, si $\sigma$ fuera un vector orientado de algún tipo, entonces sería natural esperar que voltear el aparato invirtiera la lectura. Una explicación simple es que el aparato mide la componente del vector a lo largo de un eje incrustado en el aparato. ¿Es esta explicación correcta para todas las configuraciones?

Si estamos convencidos de que el espín es un vector, naturalmente lo describiríamos por tres componentes: $\sigma_{z}$, $\sigma_{x}$ y $\sigma_{y}$. Cuando el aparato está vertical a lo largo del eje $z$, está posicionado para medir $\sigma_{z}$.

 Figura 1.3: El aparato rotado $90^{\circ}$. Una nueva medición da como resultado $\sigma_{z} = -1$ con un 50 por ciento de probabilidad

    UN EXPERIMENTO

y la física cuántica. La diferencia solo se hace aparente cuando rotamos el aparato un ángulo arbitrario, digamos $\frac{\pi}{2}$ radianes (90 grados). El aparato comienza en la posición vertical (con la flecha hacia arriba a lo largo del eje $z$). Se prepara un espín con $\sigma = +1$. Luego, se rota $\mathcal{A}$ de modo que la flecha hacia arriba apunte a lo largo del eje $x$ (Fig. 1.3), y entonces se realiza una medición de lo que presumiblemente es la componente $x$ del espín, $\sigma_{x}$.

Si de hecho $\sigma$ realmente representa la componente de un vector a lo largo de la flecha hacia arriba, uno esperaría obtener cero. ¿Por qué? Inicialmente, confirmamos que $\sigma$ estaba dirigido a lo largo del eje $z$, sugiriendo que su componente a lo largo de $x$ debe ser cero. Pero nos llevamos una sorpresa cuando medimos $\sigma_{x}$: en lugar de dar $\sigma_{x} = 0$, el aparato da $\sigma_{x} = +1$ o $\sigma_{x} = -1$. $\mathcal{A}$ es muy terco: no importa cómo esté orientado, se niega a dar otra respuesta que no sea $\sigma = \pm 1$. Si el espín es realmente un vector, es uno muy peculiar.

Sin embargo, sí encontramos algo interesante. Supongamos que repetimos la operación muchas veces, cada vez siguiendo el mismo procedimiento, es decir:

- Comenzando con $\mathcal{A}$ a lo largo del eje $z$, preparar $\sigma = +1$.
- Rotar el aparato para que esté orientado a lo largo del eje $x$.
- Medir $\sigma$.

El experimento repetido escupe una serie aleatoria de unos positivos y unos negativos. El determinismo se ha roto, pero de una manera particular. Si hacemos muchas repeticiones, encontraremos

  1 ECCIÓN 1. SISTEMAS Y EXPERIMENTOS

que los números de eventos con $\sigma = +1$ y eventos con $\sigma = -1$ son estadísticamente iguales. En otras palabras, el valor promedio de $\sigma$ es cero. En lugar del resultado clásico (a saber, que la componente de $\sigma$ a lo largo del eje $x$ es cero), encontramos que el promedio de estas mediciones repetidas es cero.

 1.4: El aparato rotado un ángulo arbitrario dentro del plano $x - z$. El resultado promedio de la medición es $\hat{n} \cdot \hat{m}$.  hagamos todo de nuevo, pero en lugar de rotar $\mathcal{A}$ para que se sitúe en el eje $x$, rotémoslo a una dirección arbitraria a lo largo del vector unitario $^2\hat{n}$. Clásicamente, si $\sigma$ fuera un vector, esperaríamos que el resultado del experimento fuera la componente de $\sigma$ a lo largo del eje $\hat{n}$. Si $\hat{n}$ forma un ángulo $\theta$
con respecto a $z$, la respuesta clásica sería $\sigma = \cos \theta$. Pero como habrás adivinado, cada vez que hacemos el experimento obtenemos $\sigma = +1$ o $\sigma = -1$. Sin embargo, el resultado está estadísticamente sesgado de modo que el valor promedio es $\cos \theta$.

La situación es, por supuesto, más general. No tuvimos que comenzar con $\mathcal{A}$ orientado a lo largo de $z$. Elige cualquier dirección $\hat{m}$ y comienza con la flecha hacia arriba apuntando a lo largo de $\hat{m}$. Prepara un espín para que el aparato lea $+1$. Luego, sin perturbar el espín, rota el aparato a la dirección $\hat{n}$, como se muestra en la Fig. 1.4. Un nuevo experimento sobre el mismo espín dará resultados aleatorios $\pm 1$, pero con un valor promedio igual al coseno del ángulo entre $\hat{n}$ y $\hat{m}$. En otras palabras, el promedio será $\hat{n} \cdot \hat{m}$.

La notación mecanocuántica para el promedio estadístico de una cantidad $Q$ es la notación de corchetes de Dirac $\langle Q \rangle$. Podemos resumir los resultados de nuestra investigación experimental de la siguiente manera: Si comenzamos con $\mathcal{A}$ orientado a lo largo de $\hat{m}$ y confirmamos que $\sigma = +1$, entonces la medición subsiguiente con $\mathcal{A}$ orientado a lo largo de $\hat{n}$ da el resultado estadístico

$$\langle \sigma \rangle = \hat{n}\cdot \hat{m}.$$

Lo que estamos aprendiendo es que los sistemas mecánico-cuánticos no son deterministas —los resultados de los experimentos pueden ser estadísticamente aleatorios— pero si repetimos un experimento muchas veces, las cantidades promedio pueden seguir las expectativas de la física clásica, al menos hasta cierto punto.

Cada experimento involucra un sistema externo —un aparato— que debe interactuar con el sistema para registrar un resultado. En ese sentido, cada experimento es invasivo. Esto es cierto tanto en la física clásica como en la cuántica, pero solo la física cuántica le da gran importancia a esto. ¿Por qué es así? Clásicamente, un aparato de medición ideal tiene un efecto insignificantemente pequeño sobre el sistema que está midiendo. Los experimentos clásicos pueden ser arbitrariamente suaves y aun así registrar los resultados del experimento de manera precisa y reproducible. Por ejemplo, la dirección de una flecha se puede determinar reflejando luz en la flecha y enfocándola para formar una imagen. Si bien es cierto que la luz debe tener una longitud de onda lo suficientemente pequeña para formar una imagen, no hay nada en la física clásica que impida que la imagen se haga con luz arbitrariamente débil. En otras palabras, la luz puede tener un contenido de energía arbitrariamente pequeño.

En mecánica cuántica, la situación es fundamentalmente diferente. Cualquier interacción que sea lo suficientemente fuerte como para medir algún aspecto de un sistema es necesariamente lo suficientemente fuerte como para perturbar algún otro aspecto del mismo sistema. Por lo tanto, no se puede aprender nada sobre un sistema cuántico sin cambiar algo más.

Esto debería ser evidente en los ejemplos que involucran a $\mathcal{A}$ y $\sigma$. Supongamos que comenzamos con $\sigma = +1$ a lo largo del eje $z$. Si medimos $\sigma$ nuevamente con $\mathcal{A}$ orientado a lo largo de $z$, confirmaremos el valor anterior. Podemos hacer esto una y otra vez sin cambiar el resultado. Pero considera esta posibilidad: entre mediciones sucesivas a lo largo del eje $z$, giramos $\mathcal{A}$ a través de

  1 

90 grados, hacemos una medición intermedia y lo giramos de vuelta a su dirección original. ¿Una medición subsiguiente a lo largo del eje $z$ confirmará la medición original? La respuesta es no. La medición intermedia a lo largo del eje $x$ dejará el espín en una configuración completamente aleatoria en lo que respecta a la siguiente medición. No hay manera de hacer la determinación intermedia del espín sin alterar completamente la medición final. Se podría decir que medir una componente del espín destruye la información sobre otra componente. De hecho, simplemente no se pueden conocer simultáneamente las componentes del espín a lo largo de dos ejes diferentes, al menos no de manera reproducible. Hay algo fundamentalmente diferente entre el estado de un sistema cuántico y el estado de un sistema clásico.

### 1.5 Proposiciones

El espacio de estados de un sistema clásico es un conjunto matemático. Si el sistema es una moneda, el espacio de estados es un conjunto de dos elementos, $C$ y $X$. Usando notación de conjuntos, escribiríamos $\{C, X\}$. Si el sistema es un dado de seis caras, el espacio de estados tiene seis elementos etiquetados $\{1, 2, 3, 4, 5, 6\}$. La lógica de la teoría de conjuntos se llama lógica booleana. La lógica booleana es solo una versión formalizada de la lógica clásica familiar de proposiciones.

Una idea fundamental en la lógica booleana es la noción de un valor de verdad. El valor de verdad de una proposición es verdadero o falso. No se permite nada intermedio. El concepto relacionado en la teoría de conjuntos es un subconjunto. En términos generales, una proposición es verdadera para todos los elementos en su subconjunto correspondiente y falsa para todos los elementos que no están en este subconjunto. Por ejemplo,
representa los estados posibles de un dado, se puede considerar la proposición

A: El dado muestra una cara con número impar.

El subconjunto correspondiente contiene los tres elementos $\{1,3,5\}$.

Otra proposición establece

B: El dado muestra un número menor que 4.

El subconjunto correspondiente contiene los estados $\{1,2,3\}$.

Cada proposición tiene su opuesta (también llamada su negación). Por ejemplo,

no A: El dado no muestra una cara con número impar.

El subconjunto para esta proposición negada es $\{2,4,6\}$.

Hay reglas para combinar proposiciones en proposiciones más complejas, siendo las más importantes **y**, **o**, y **no**. Acabamos de ver un ejemplo de **no**, que se aplica a un solo subconjunto o proposición. **Y** es directo y se aplica a un par de proposiciones. Significa que ambas son verdaderas. Aplicado a dos subconjuntos, **y** da los elementos comunes a ambos, es decir, la intersección de los dos subconjuntos. En el ejemplo del dado, la intersección de los subconjuntos $A$ y $B$ es el subconjunto de elementos que son a la vez impares y menores que 4. La Fig. 1.5 utiliza un diagrama de Venn para mostrar cómo funciona esto.



1.5. PROPOSICIONES

La regla **o** es similar a **y**, pero tiene una sutileza adicional. En el habla cotidiana, la palabra "o" se usa generalmente en el sentido exclusivo: la versión exclusiva es verdadera si una u otra de las dos proposiciones es verdadera, pero no ambas. Sin embargo, la lógica booleana utiliza la versión inclusiva de **o**, que es verdadera si una u otra (o ambas) de las proposiciones son verdaderas. Así, de acuerdo con el **o** inclusivo, la proposición

Albert Einstein descubrió la relatividad o Isaac Newton era inglés

es verdadera. También lo es

Albert Einstein descubrió la relatividad o Isaac Newton era ruso.

El **o** inclusivo solo es incorrecto si ambas proposiciones son falsas. Por ejemplo,

Albert Einstein descubrió América o Isaac Newton era ruso.

El **o** inclusivo tiene una interpretación en teoría de conjuntos como la unión de dos conjuntos: denota el subconjunto que contiene cualquier elemento que esté en uno u otro (o en ambos) de los subconjuntos componentes. En el ejemplo del dado, (A o B) denota el subconjunto $\{1,2,3,5\}$.

  1 ECCIÓN 1. SISTEMAS Y EXPERIMENTOS

Figura 1.5: Un Ejemplo del modelo clásico de Espacio de Estados. El subconjunto $A$ representa la proposición "el dado muestra una cara con número impar". El subconjunto $B$: "El dado muestra un número $< 4$". El sombreado oscuro muestra la intersección de $A$ y $B$, que representa la proposición ( $A$ y $B$ ). Los números blancos son elementos de la unión de $A$ con $B$, representando la proposición ( $A$ o $B$ ).

### 1.6 Probando Proposiciones Clásicas

Regresemos al sistema cuántico simple que consiste en un solo espín, y a las diversas proposiciones cuya verdad podríamos probar usando el aparato $A$. Considera las dos proposiciones siguientes:

A: La componente $z$ del espín es $+1$.

  1  PROBANDO PROPOSICIONES CLÁSICAS

B: La componente $x$ del espín es $+1$.

Cada una de estas es significativa y puede ser probada orientando $\mathcal{A}$ a lo largo del eje apropiado. La negación de cada una también es significativa. Por ejemplo, la negación de la primera proposición es

no A: La componente $z$ del espín es $-1$.

Pero ahora considera las proposiciones compuestas

(A o $B$ ): La componente $z$ del espín es $+1$ o la componente $x$ del espín es $+1$.

(A y $B$ ): La componente $z$ del espín es $+1$ y la componente $x$ del espín es $+1$.

Considera cómo probaríamos la proposición (A o $B$). Si los espines se comportaran clásicamente (y por supuesto no lo hacen), procederíamos de la siguiente manera: $^5$

- Medir suavemente $\sigma_{z}$ y registrar el valor. Si es $+1$, hemos terminado: la proposición (A o $B$) es verdadera. Si $\sigma_{z}$ es $-1$, continuar con el siguiente paso.
- Medir suavemente $\sigma_{x}$. Si es $+1$, entonces la proposición (A o $B$) es verdadera. Si no, esto significa que ni $\sigma_{z}$ ni $\sigma_{x}$ fueron iguales a $+1$, y (A o $B$) es falsa.

  1 

18 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

Hay un procedimiento alternativo, que es intercambiar el orden de las dos mediciones. Para enfatizar esta inversión de orden, llamaremos al nuevo procedimiento ( $B$ o $A$ ):

- Medir suavemente $\sigma_{x}$ y registrar el valor. Si es $+1$ hemos terminado: La proposición ( $B$ o $A$ ) es verdadera. Si $\sigma_{x}$ es $-1$ continuar con el siguiente paso.
- Medir suavemente $\sigma_{z}$. Si es $+1$, entonces ( $B$ o $A$ ) es verdadera. Si no, significa que ni $\sigma_{x}$ ni $\sigma_{z}$ fueron iguales a $+1$, y ( $B$ o $A$ ) es falsa.

En la física clásica, los dos órdenes de operación dan la misma respuesta. La razón de esto es que las mediciones pueden ser arbitrariamente suaves, tan suaves que no afectan los resultados de mediciones subsiguientes. Por lo tanto, la proposición ( $A$ o $B$ ) tiene el mismo significado que la proposición ( $B$ o $A$ ).

### 1.7 Probando Proposiciones Cuánticas

Ahora llegamos al mundo cuántico que describí anteriormente. Imaginemos una situación en la que alguien (o algo) desconocido para nosotros ha preparado secretamente un espín en el estado $\sigma_{z} = +1$. Nuestra tarea es usar el aparato $\mathcal{A}$ para determinar si la proposición ( $A$ o $B$ ) es verdadera o falsa. Intentaremos usar los procedimientos descritos anteriormente.

Comenzamos midiendo $\sigma_{z}$. Dado que el agente desconocido ha preparado las cosas, descubriremos que $\sigma_{z} = +1$. Es innecesario continuar: ( $A$ o $B$ ) es verdadera. Sin embargo, podríamos probar $\sigma_{x}$

  1 

1.7. PROBANDO PROPOSICIONES CUÁNTICAS 19

solo para ver qué sucede. La respuesta es impredecible. Encontramos aleatoriamente que $\sigma_{x} = +1$ o $\sigma_{x} = -1$. Pero ninguno de estos resultados afecta la verdad de la proposición (A o $B$).

Pero ahora invirtamos el orden de la medición. Como antes, llamaremos al procedimiento invertido ( $B$ o $A$ ), y esta vez mediremos $\sigma_{x}$ primero. Debido a que el agente desconocido fijó el espín en $+1$ a lo largo del eje $z$, la medición de $\sigma_{x}$ es aleatoria. Si resulta que $\sigma_{x} = +1$, hemos terminado: ( $B$ o $A$ ) es verdadera. Pero supongamos que encontramos el resultado opuesto, $\sigma_{x} = -1$. El espín está orientado a lo largo de la dirección $-x$. Detengámonos aquí brevemente, para asegurarnos de que entendemos lo que acaba de suceder. Como resultado de nuestra primera medición, el espín ya no está en su estado original $\sigma_{z} = +1$. Está en un nuevo estado, que es $\sigma_{x} = +1$ o $\sigma_{x} = -1$. Por favor, tómate un momento para dejar que esta idea se asiente. No podemos enfatizar demasiado su importancia.

Ahora estamos listos para probar la segunda mitad de la proposición ( $B$ o $A$ ). Rota el aparato $\mathcal{A}$ al eje $z$ y mide $\sigma_{z}$. Según la mecánica cuántica, el resultado será aleatoriamente $\pm 1$. Esto significa que hay un 25 por ciento de probabilidad de que el experimento produzca $\sigma_{x} = -1$ y $\sigma_{z} = -1$. En otras palabras, con una probabilidad de $\frac{1}{4}$, encontramos que ( $B$ o $A$ ) es falsa; esto ocurre a pesar de que el agente oculto había asegurado originalmente que $\sigma_{z} = +1$.

Evidentemente, en este ejemplo, el **o** inclusivo no es simétrico. La verdad de ( $A$ o $B$ ) puede depender del orden en que confirmamos las dos proposiciones. Esto no es algo menor; significa no solo que las leyes de la física cuántica son diferentes de sus contrapartes clásicas, sino que los fundamentos mismos de la lógica son diferentes en la física cuántica también.

  2 

20 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

¿Qué pasa con (A y $B$)? Supongamos que nuestra primera medición da $\sigma_{z} = +1$ y la segunda, $\sigma_{x} = +1$. Este es, por supuesto, un resultado posible. Estaríamos inclinados a decir que (A y $B$) es verdadera. Pero en la ciencia, especialmente en la física, la verdad de una proposición implica que la proposición puede ser verificada mediante observación subsiguiente. En la física clásica, la suavidad de las observaciones implica que los experimentos subsiguientes no se ven afectados y confirmarán un experimento anterior. Una moneda que muestra Cara no se volteará a Cruz por el acto de observarla —al menos no clásicamente. Cuánticamente, la segunda medición ( $\sigma_{x} = +1$ ) arruina la posibilidad de verificar la primera. Una vez que $\sigma_{x}$ ha sido preparado a lo largo del eje $x$, otra medición de $\sigma_{z}$ dará una respuesta aleatoria. Por lo tanto, (A y $B$) no es confirmable: la segunda parte del experimento interfiere con la posibilidad de confirmar la primera parte.

Si sabes un poco de mecánica cuántica, probablemente reconozcas que estamos hablando del principio de incertidumbre. El principio de incertidumbre no solo se aplica a la posición y el momento (o velocidad); se aplica a muchos pares de cantidades medibles. En el caso del espín, se aplica a proposiciones que involucran dos componentes diferentes de $\sigma$. En el caso de la posición y el momento, las dos proposiciones que podríamos considerar son:

Una cierta partícula tiene posición $x$.

Esa misma partícula tiene momento $p$.

A partir de estas, podemos formar las dos proposiciones compuestas

  2  INTERLUDIO: NÚMEROS COMPLEJOS

La partícula tiene posición $x$ y la partícula tiene momento $p$.

La partícula tiene posición $x$ o la partícula tiene momento $p$.

Por extrañas que parezcan, ambas proposiciones tienen significado en el idioma inglés, y también en la física clásica. Sin embargo, en la física cuántica, la primera de estas proposiciones es completamente carente de significado (ni siquiera errónea), y la segunda significa algo bastante diferente de lo que podrías pensar. Todo se reduce a una profunda diferencia lógica entre los conceptos clásico y cuántico del estado de un sistema. Explicar el concepto cuántico de estado requerirá algo de matemáticas abstractas, así que hagamos una pausa para un breve interludio sobre números complejos y espacios vectoriales. La necesidad de cantidades complejas se aclarará más adelante, cuando estudiemos la representación matemática de los estados de espín.

### 1.8 Interludio Matemático: Números Complejos

Todos los que han llegado hasta aquí en la serie del Mínimo Teórico conocen los números complejos. Sin embargo, dedicaré unas líneas a recordar los elementos esenciales. La Fig. 1.6 muestra algunos de sus elementos básicos.

Un número complejo $z$ es la suma de un número real y un número imaginario. Podemos escribirlo como

$$z = x + iy,$$

  2 

22 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

 Figura 1.6: Dos Formas Comunes de Representar Números Complejos. En la representación cartesiana, $x$ e $y$ son las componentes horizontal (real) y vertical (imaginaria). En la representación polar, $r$ es el radio, y $\theta$ es el ángulo formado con el eje $x$. En cada caso, se necesitan dos números reales para representar un solo número complejo.  

donde $x$ e $y$ son reales y $i^2 = -1$. Los números complejos se pueden sumar, multiplicar y dividir mediante las reglas estándar de la aritmética. Se pueden visualizar como puntos en el plano complejo con coordenadas $x, y$. También se pueden representar en coordenadas polares:

  2 

1.8. INTERLUDIO: NÚMEROS COMPLEJOS

$$z = re^{i\theta} = r(\cos \theta + i\sin \theta).$$

Sumar números complejos es fácil en forma de componentes: simplemente suma los componentes. De manera similar, multiplicarlos es fácil en su forma polar: simplemente multiplica los radios y suma los ángulos:

$$\left(r_{1}e^{i\theta_{1}}\right)\left(r_{2}e^{i\theta_{2}}\right) = \left(r_{1}r_{2}\right)e^{i(\theta_{1} + \theta_{2})}.$$

Todo número complejo $z$ tiene un complejo conjugado $z^{*}$ que se obtiene simplemente invirtiendo el signo de la parte imaginaria. Si

$$z = x + iy = re^{i\theta},$$

entonces

$$z^{*} = x - iy = re^{-i\theta}.$$

Multiplicar un número complejo por su conjugado siempre da un resultado real positivo:

$$z^{*}z = r^{2}.$$

Por supuesto, es cierto que todo complejo conjugado es en sí mismo un número complejo, pero a menudo es útil pensar en $z$ y $z^{*}$ como pertenecientes a sistemas numéricos "duales" separados. Dual aquí significa que para cada $z$ hay un $z^{*}$ único y viceversa.

  2 

24 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

Hay una clase especial de números complejos que llamaré "factores de fase". Un factor de fase es simplemente un número complejo cuya componente $r$ es 1. Si $z$ es un factor de fase, entonces se cumple lo siguiente:

$$z^{*}z = 1$$ $$z = e^{i\theta}$$ $$z = \cos \theta + i\sin \theta.$$

### 1.9 Interludio Matemático: Espacios Vectoriales

#### 1.9.1 Axiomas

Para un sistema clásico, el espacio de estados es un conjunto (el conjunto de estados posibles), y la lógica de la física clásica es booleana. Eso parece obvio y es difícil imaginar cualquier otra posibilidad. Sin embargo, el mundo real opera siguiendo líneas completamente diferentes, al menos cuando la mecánica cuántica es importante. El espacio de estados de un sistema cuántico no es un conjunto matemático; es un espacio vectorial. Las relaciones entre los elementos de un espacio vectorial son diferentes de aquellas entre los elementos de un conjunto, y la lógica de las proposiciones también es diferente.

Antes de hablar sobre espacios vectoriales, necesito aclarar el término vector. Como sabes, usamos este término para indicar un

  2 

1.9. INTERLUDIO: ESPACIOS VECTORIALES

objeto en el espacio ordinario que tiene una magnitud y una dirección. Tales vectores tienen tres componentes, correspondientes a las tres dimensiones del espacio. Quiero que olvides completamente ese concepto de vector. De ahora en adelante, siempre que quiera hablar de una cosa con magnitud y dirección en el espacio ordinario, la llamaré explícitamente un 3-vector. Un espacio vectorial matemático es una construcción abstracta que puede tener o no algo que ver con el espacio ordinario. Puede tener cualquier número de dimensiones desde 1 hasta $\infty$ y puede tener componentes que sean enteros, números reales, o incluso cosas más generales.

Los espacios vectoriales que usamos para definir los estados mecánico-cuánticos se llaman espacios de Hilbert. No daremos la definición matemática aquí, pero puedes añadir este término a tu vocabulario. Cuando te encuentres con el término espacio de Hilbert en mecánica cuántica, se refiere al espacio de estados. Un espacio de Hilbert puede tener un número finito o infinito de dimensiones.

En mecánica cuántica, un espacio vectorial está compuesto por elementos $|A\rangle$ llamados vectores ket o simplemente kets. Aquí están los axiomas que usaremos para definir el espacio vectorial de estados de un sistema cuántico ($z$ y $w$ son números complejos):

1.  La suma de dos vectores ket cualesquiera es también un vector ket:

$$|A\rangle + |B\rangle = |C\rangle.$$

  2 

2.  La adición de vectores es conmutativa:

$$|A\rangle + |B\rangle = |B\rangle + |A\rangle.$$

3.  La adición de vectores es asociativa:

$$\{|A\rangle + |B\rangle\} + |C\rangle = |A\rangle + \{|B\rangle + |C\rangle\}.$$

4.  Existe un vector único 0 tal que cuando lo sumas a cualquier ket, obtienes el mismo ket:

$$|A\rangle + 0 = |A\rangle.$$

5.  Dado cualquier ket $|A\rangle$, existe un ket único $-|A\rangle$ tal que

$$|A\rangle + (-|A\rangle) = 0.$$

6.  Dado cualquier ket $|A\rangle$ y cualquier número complejo $z$, puedes multiplicarlos para obtener un nuevo ket. Además, la multiplicación por un escalar es lineal:

$$|zA\rangle = z|A\rangle = |B\rangle.$$

7.  La propiedad distributiva se cumple:

$$z\{|A\rangle + |B\rangle\} = z|A\rangle + z|B\rangle$$ $$\{z + w\} |A\rangle = z|A\rangle + w|A\rangle.$$

  2 

1.9. INTERLUDIO: ESPACIOS VECTORIALES 27

Los axiomas 6 y 7 tomados en conjunto a menudo se llaman linealidad.

Los 3-vectores ordinarios satisfarían estos axiomas excepto por una cosa: el axioma 6 permite que un vector sea multiplicado por cualquier número complejo. Los 3-vectores ordinarios pueden ser multiplicados por números reales (positivos, negativos o cero) pero la multiplicación por números complejos no está definida. Se puede pensar que los 3-vectores forman un espacio vectorial real, y los kets forman un espacio vectorial complejo. Nuestra definición de vectores ket es bastante abstracta. Como veremos, hay varias formas concretas de representar los vectores ket también.

#### 1.9.2 Funciones y Vectores Columna

Veamos algunos ejemplos concretos de espacios vectoriales complejos. En primer lugar, considera el conjunto de funciones continuas de variable compleja de una variable $x$. Llama a las funciones $A(x)$. Puedes sumar dos funciones cualesquiera y multiplicarlas por números complejos. Puedes comprobar que satisfacen los siete axiomas. Este ejemplo debería hacerte obvio que estamos hablando de algo mucho más general que las flechas tridimensionales.

Los vectores columna bidimensionales proporcionan otro ejemplo concreto. Los construimos apilando un par de números complejos, $\alpha_{1}$ y $\alpha_{2}$, en la forma

$$\left( \begin{array}{c}\alpha_{1}\\ \alpha_{2} \end{array} \right)$$

e identificando esta "pila" con el vector ket $|A\rangle$. Los números complejos $\alpha$ son los componentes de $|A\rangle$. Puedes sumar dos vectores columna sumando sus componentes:

  2 

28 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

$$\left( \begin{array}{c}\alpha_{1}\\ \alpha_{2} \end{array} \right) + \left( \begin{array}{c}\beta_{1}\\ \beta_{2} \end{array} \right) = \left( \begin{array}{c}\alpha_{1} + \beta_{1}\\ \alpha_{2} + \beta_{2} \end{array} \right).$$

Además, puedes multiplicar el vector columna por un número complejo $z$ simplemente multiplicando los componentes,

$$z\left( \begin{array}{c}\alpha_{1}\\ \alpha_{2} \end{array} \right) = \left( \begin{array}{c}z\alpha_{1}\\ z\alpha_{2} \end{array} \right).$$

Se pueden construir espacios vectoriales columna de cualquier número de dimensiones. Por ejemplo, aquí hay un vector columna de cinco dimensiones:

$$\left( \begin{array}{c}\alpha_{1}\\ \alpha_{2}\\ \alpha_{3}\\ \alpha_{4}\\ \alpha_{5} \end{array} \right).$$

Normalmente, no mezclamos vectores de diferente dimensionalidad.

#### 1.9.3 Bras y Kets

Como hemos visto, los números complejos tienen una versión dual: en forma de números complejos conjugados. Del mismo modo, un espacio vectorial complejo tiene una versión dual que es esencialmente el espacio vectorial complejo conjugado. Por cada vector ket $|A\rangle$, hay un vector "bra" en el espacio dual, denotado por $\langle A|$. ¿Por qué los extraños términos bra y ket? Pronto definiremos productos internos de bras y kets, usando expresiones como $\langle B|A\rangle$ para formar bra-kets o corchetes. Los productos internos son extremadamente

  2 

1.9. INTERLUDIO: ESPACIOS VECTORIALES 29

importantes en la maquinaria matemática de la mecánica cuántica, y para caracterizar espacios vectoriales en general.

Los vectores bra satisfacen los mismos axiomas que los vectores ket, pero hay dos cosas a tener en cuenta sobre la correspondencia entre kets y bras:

1.  Supongamos que $\langle A|$ es el bra correspondiente al ket $|A\rangle$ y $\langle B|$ es el bra correspondiente al ket $|B\rangle$. Entonces el bra correspondiente a

$$|A\rangle + |B\rangle$$

es

$$\langle A| + \langle B|.$$

2.  Si $z$ es un número complejo, entonces no es cierto que el bra correspondiente a $z|A\rangle$ sea $\langle A|z$. Tienes que recordar conjugar complejamente. Por lo tanto, el bra correspondiente a

$$z|A\rangle$$

es

$$\langle A|z^{*}.$$

En el ejemplo concreto donde los kets se representan por vectores columna, los bras duales se representan por vectores fila,

  3 

30 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

con las entradas siendo los números complejos conjugados. Así, si el ket $|A\rangle$ está representado por la columna

$$\left( \begin{array}{c}\alpha_{1}\\ \alpha_{2}\\ \alpha_{3}\\ \alpha_{4}\\ \alpha_{5} \end{array} \right),$$

entonces el bra correspondiente $\langle A|$ está representado por la fila

$$\left(\alpha_{1}^{*}\ \alpha_{2}^{*}\ \alpha_{3}^{*}\ \alpha_{4}^{*}\ \alpha_{5}^{*}\right).$$

#### 1.9.4 Productos Internos

Sin duda estás familiarizado con el producto escalar definido para 3-vectores ordinarios. La operación análoga para bras y kets es el producto interno. El producto interno es siempre el producto de un bra y un ket y se escribe de esta manera:

$$\langle B|A\rangle.$$

El resultado de esta operación es un número complejo. Los axiomas para los productos internos no son demasiado difíciles de adivinar:

1.  Son lineales:

$$\langle C|\{|A\rangle + |B\rangle\} = \langle C|A\rangle + \langle C|B\rangle.$$

  3 

1.9. INTERLUDIO: ESPACIOS VECTORIALES 31

2.  Intercambiar bras y kets corresponde a la conjugación compleja:

$$\langle B|A\rangle = \langle A|B\rangle^{*}.$$

# Ejercicio 1.1:

a) Usando los axiomas para productos internos, demuestra

$$\{\langle \mathbf{A}| + \langle \mathbf{B}|\} |\mathbf{C}\rangle = \langle \mathbf{A}|\mathbf{C}\rangle + \langle \mathbf{B}|\mathbf{C}\rangle.$$

b) Demuestra que $\langle \mathbf{A}|\mathbf{A}\rangle$ es un número real.

En la representación concreta de bras y kets mediante vectores fila y columna, el producto interno se define en términos de componentes:

$$\langle B|A\rangle = \left(\beta_{1}^{*}\ \beta_{2}^{*}\ \beta_{3}^{*}\ \beta_{4}^{*}\ \beta_{5}^{*}\right) \left( \begin{array}{c}\alpha_{1}\\ \alpha_{2}\\ \alpha_{3}\\ \alpha_{4}\\ \alpha_{5} \end{array} \right)$$

$$= \beta_{1}^{*}\alpha_{1} + \beta_{2}^{*}\alpha_{2} + \beta_{3}^{*}\alpha_{3} + \beta_{4}^{*}\alpha_{4} + \beta_{5}^{*}\alpha_{5}. \quad (1.2)$$

La regla para los productos internos es esencialmente la misma que para los productos escalares: suma los productos de los componentes correspondientes de los vectores cuyo producto interno se está calculando.

  3 

32 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

**Ejercicio 1.2:** Muestra que el producto interno definido por la Ec. 1.2 satisface todos los axiomas de los productos internos.

Usando el producto interno, podemos definir algunos conceptos que son familiares de los 3-vectores ordinarios:

- **Vector Normalizado:** Se dice que un vector está normalizado si su producto interno consigo mismo es 1. Los vectores normalizados satisfacen,

$$\langle A|A\rangle = 1.$$

Para los 3-vectores ordinarios, el término vector normalizado se reemplaza usualmente por vector unitario, es decir, un vector de longitud unitaria.

- **Vectores Ortogonales:** Se dice que dos vectores son ortogonales si su producto interno es cero. $|A\rangle$ y $|B\rangle$ son ortogonales si

$$\langle B|A\rangle = 0.$$

Este es el análogo de decir que dos 3-vectores son ortogonales si su producto escalar es cero.

#### 1.9.5 Bases Ortonormales

Al trabajar con 3-vectores ordinarios, es extremadamente útil introducir un conjunto de tres vectores unitarios mutuamente ortogonales y usarlos como base para construir cualquier vector. Un ejemplo

  3 

1.9. INTERLUDIO: ESPACIOS VECTORIALES 33

simple serían los 3-vectores unitarios que apuntan a lo largo de los ejes $x$, $y$ y $z$. Usualmente se llaman $\hat{i}, \hat{j}$ y $\hat{k}$. Cada uno es de longitud unitaria y ortogonal a los demás. Si intentaras encontrar un cuarto vector ortogonal a estos tres, no lo habría —al menos no en tres dimensiones. Sin embargo, si hubiera más dimensiones del espacio, habría más vectores base. La dimensión de un espacio puede definirse como el número máximo de vectores mutuamente ortogonales en ese espacio.

Obviamente, no hay nada especial en los ejes particulares $x, y$ y $z$. Siempre que los vectores base sean de longitud unitaria y sean mutuamente ortogonales, comprenden una base ortonormal.

El mismo principio es cierto para los espacios vectoriales complejos. Se puede comenzar con cualquier vector normalizado y luego buscar un segundo, ortogonal al primero. Si encuentras uno, entonces el espacio es al menos bidimensional. Luego busca un tercero, cuarto, y así sucesivamente. Eventualmente, puedes quedarte sin nuevas direcciones y no habrá más candidatos ortogonales. El número máximo de vectores mutuamente ortogonales es la dimensión del espacio. Para vectores columna, la dimensión es simplemente el número de entradas en la columna.

Consideremos un espacio $N$-dimensional y una base ortonormal particular de vectores ket etiquetados $|i\rangle$. La etiqueta $i$ va desde 1 hasta $N$. Considera un vector $|A\rangle$, escrito como una suma de vectores

  3 

34 LECCIÓN 1. SISTEMAS Y EXPERIMENTOS

base:

$$|A\rangle = \sum_{i}\alpha_{i}|i\rangle. \quad (1.3)$$

Los $\alpha_{i}$ son números complejos llamados los componentes del vector, y para calcularlos tomamos el producto interno de ambos lados con un bra base $\langle j|$:

$$\langle j|A\rangle = \sum_{i}\alpha_{i}\langle j|i\rangle. \quad (1.4)$$

A continuación, usamos el hecho de que los vectores base son ortonormales. Esto implica que $\langle j|i\rangle = 0$ si $i$ no es igual a $j$, y $\langle j|i\rangle = 1$ si $i = j$. En otras palabras, $\langle j|i\rangle = \delta_{ij}$. Esto hace que la suma en la Ec. 1.4 colapse a un solo término:

$$\langle j|A\rangle = \alpha_{j}. \quad (1.5)$$

Por lo tanto, vemos que los componentes de un vector son simplemente sus productos internos con los vectores base. Podemos reescribir la Ec. 1.3 en la forma elegante

$$|A\rangle = \sum_{i}|i\rangle \langle i|A\rangle.$$

---

[Fin de la Parte 1/5. Continuará...]

[PARTE 2/5]

---

# Lección 2

## Estados Cuánticos

Art: Curiosamente, esa cerveza hizo que mi cabeza dejara de dar vueltas. ¿En qué estado estamos?

Lenny: Ojalá lo supiera. ¿Importa?

Art: Podría ser. No creo que sigamos en California.

### 2.1 Estados y Vectores

En física clásica, conocer el estado de un sistema implica conocer todo lo necesario para predecir el futuro de ese sistema. Como hemos visto en la lección anterior, los sistemas cuánticos no son completamente predecibles. Evidentemente, los estados cuánticos tienen un significado diferente al de los estados clásicos. De manera muy aproximada, conocer un estado cuántico significa saber todo lo que se puede saber sobre cómo se preparó el sistema. En el capítulo anterior, hablamos sobre el uso de un aparato para preparar el estado de un espín. De hecho, asumimos implícitamente que

  3 

36 LECCIÓN 2. ESTADOS CUÁNTICOS

no había más detalles finos que especificar o que pudieran especificarse sobre el estado del espín.

La pregunta obvia que surge es si la impredecibilidad se debe a una incompletitud en lo que llamamos un estado cuántico. Hay varias opiniones sobre este asunto. Aquí hay una muestra:

- Sí, la noción habitual de estado cuántico es incompleta. Hay "variables ocultas" que, si solo pudiéramos acceder a ellas, permitirían una predictibilidad completa. Hay dos versiones de esta visión. En la versión $A$, las variables ocultas son difíciles de medir pero en principio están experimentalmente disponibles para nosotros. En la versión $B$, debido a que estamos hechos de materia mecánico-cuántica y por lo tanto sujetos a las restricciones de la mecánica cuántica, las variables ocultas son, en principio, no detectables.

- No, el concepto de variables ocultas no nos lleva en una dirección provechosa. La mecánica cuántica es inevitablemente impredecible. La mecánica cuántica es un cálculo de probabilidades tan completo como es posible. El trabajo de un físico es aprender y usar este cálculo.

No sé cuál será la respuesta definitiva a esta pregunta, o incluso si resultará ser una pregunta útil. Pero para nuestros propósitos, no es importante lo que un físico en particular crea sobre el significado último del estado cuántico. Por razones prácticas, adoptaremos la segunda visión.

En la práctica, lo que esto significa para el espín cuántico de la Lección 1 es que, cuando el aparato $\mathcal{A}$ actúa y nos dice que $\sigma_{z} = +1$ o $\sigma_{z} = -1$, no hay más que conocer, o

  3 

2.2. REPRESENTANDO ESTADOS DE ESPÍN

que se pueda conocer. Del mismo modo, si rotamos $\mathcal{A}$ y medimos $\sigma_{x} = +1$ o $\sigma_{x} = -1$, no hay más que conocer. Igualmente para $\sigma_{y}$ o cualquier otra componente del espín.

### 2.2 Representando Estados de Espín

Ahora es el momento de intentar representar los estados de espín utilizando vectores de estado. Nuestro objetivo es construir una representación que capture todo lo que sabemos sobre el comportamiento de los espines. En este punto, el proceso será más intuitivo que formal. Intentaremos encajar las piezas lo mejor que podamos, basándonos en lo que ya hemos aprendido. Por favor, lee esta sección con atención. Créeme, valdrá la pena.

Comencemos etiquetando los posibles estados de espín a lo largo de los tres ejes de coordenadas. Si $\mathcal{A}$ está orientado a lo largo del eje $z$, los dos estados posibles que se pueden preparar corresponden a $\sigma_{z} = \pm 1$. Llamémoslos arriba y abajo y denotémoslos mediante vectores ket $|u\rangle$ y $|d\rangle$ (del inglés *up* y *down*). Así, cuando el aparato está orientado a lo largo del eje $z$ y registra $+1$, se ha preparado el estado $|u\rangle$.

Por otro lado, si el aparato está orientado a lo largo del eje $x$ y registra $-1$, se ha preparado el estado $|l\rangle$ (del inglés *left*). Lo llamaremos izquierda. Si $\mathcal{A}$ está a lo largo del eje $y$, puede preparar los estados $|i\rangle$ y $|o\rangle$ (del inglés *in* y *out*, adentro y afuera). Entiendes la idea.

La idea de que no hay variables ocultas tiene una representación matemática muy simple: el espacio de estados para un solo espín tiene solo dos dimensiones. Este punto merece énfasis:

  3 

38 LECCIÓN 2. ESTADOS CUÁNTICOS

Todos los estados de espín posibles se pueden representar en un espacio vectorial bidimensional.

Podríamos, de manera algo arbitraria, elegir $|u\rangle$ y $|d\rangle$ como los dos vectores base y escribir cualquier estado como una superposición lineal de estos dos. Adoptaremos esa elección por ahora. Usemos el símbolo $|A\rangle$ para un estado genérico. Podemos escribir esto como una ecuación,

$$|A\rangle = \alpha_u|u\rangle + \alpha_d|d\rangle,$$

donde $\alpha_{u}$ y $\alpha_{d}$ son los componentes de $|A\rangle$ a lo largo de las direcciones base $|u\rangle$ y $|d\rangle$. Matemáticamente, podemos identificar los componentes de $|A\rangle$ como

$$\begin{array}{rcl}{\alpha_u} & = & {\langle u|A\rangle}\\ {\alpha_d} & = & {\langle d|A\rangle.} \end{array} \quad (2.1)$$

Estas ecuaciones son extremadamente abstractas, y no es en absoluto obvio cuál es su significado físico. Te lo voy a decir ahora mismo: En primer lugar, $|A\rangle$ puede representar cualquier estado del espín, preparado de cualquier manera. Los componentes $\alpha_{u}$ y $\alpha_{d}$ son números complejos; por sí mismos, no tienen significado experimental, pero sus magnitudes sí lo tienen. En particular, $\alpha_{u}^{*}\alpha_{u}$ y $\alpha_{d}^{*}\alpha_{d}$ tienen el siguiente significado:

- Dado que el espín ha sido preparado en el estado $|A\rangle$, y que el aparato está orientado a lo largo de $z$, la

  3 

2.2. REPRESENTANDO ESTADOS DE ESPÍN 39

cantidad $\alpha_{u}^{*}\alpha_{u}$ es la probabilidad de que el espín se mida como $\sigma_{z} = +1$. En otras palabras, es la probabilidad de que el espín esté arriba si se mide a lo largo del eje $z$.

- Igualmente, $\alpha_{d}^{*}\alpha_{d}$ es la probabilidad de que $\sigma_{z}$ esté abajo si se mide.

Los valores $\alpha$, o equivalentemente $\langle u|A\rangle$ y $\langle d|A\rangle$, se llaman amplitudes de probabilidad. No son probabilidades en sí mismas. Para calcular una probabilidad, sus magnitudes deben elevarse al cuadrado. En otras palabras, las probabilidades para las mediciones de arriba y abajo están dadas por

$$\begin{array}{rcl}{P_u} & = & {\langle A|u\rangle \langle u|A\rangle}\\ {} & {} & {}\\ {P_d} & = & {\langle A|d\rangle \langle d|A\rangle.} \end{array} \quad (2.2)$$

Nótese que no he dicho nada sobre qué es $\sigma_{z}$ antes de ser medido. Antes de la medición, todo lo que tenemos es el vector $|A\rangle$, que representa las posibilidades potenciales pero no los valores reales de nuestras mediciones.

Otros dos puntos son importantes: Primero, nótese que $|u\rangle$ y $|d\rangle$ son mutuamente ortogonales. En otras palabras,

$$\begin{array}{rcl}{\langle u|d\rangle} & = & {0}\\ {} & {} & {}\\ {\langle d|u\rangle} & = & {0.} \end{array} \quad (2.3)$$

  4 

40 LECCIÓN 2. ESTADOS CUÁNTICOS

El significado físico de esto es que, si el espín está preparado arriba, entonces la probabilidad de detectarlo abajo es cero, y viceversa. Este punto es tan importante, lo diré de nuevo: Dos estados ortogonales son físicamente distintos y mutuamente excluyentes. Si el espín está en uno de estos estados, no puede estar (tiene probabilidad cero de estar) en el otro. Esta idea se aplica a todos los sistemas cuánticos, no solo al espín.

Pero no confundas la ortogonalidad de los vectores de estado con direcciones ortogonales en el espacio. De hecho, las direcciones arriba y abajo no son direcciones ortogonales en el espacio, aunque sus vectores de estado asociados sean ortogonales en el espacio de estados.

El segundo punto importante es que para que la probabilidad total sea igual a la unidad, debemos tener

$$\alpha_{u}^{*}\alpha_{u} + \alpha_{d}^{*}\alpha_{d} = 1. \quad (2.4)$$

Esto es equivalente a decir que el vector $|A\rangle$ está normalizado a un vector unitario:

$$\langle A|A\rangle = 1.$$

Este es un principio muy general de la mecánica cuántica que se extiende a todos los sistemas cuánticos: el estado de un sistema está representado por un vector unitario (normalizado) en un espacio vectorial de estados. Además, las magnitudes al cuadrado de los componentes del vector de estado, a lo largo de vectores base particulares, representan probabilidades para varios resultados experimentales.

  4 

2.3. A LO LARGO DEL EJE X

### 2.3 A lo largo del eje $x$

Dijimos antes que podemos representar cualquier estado de espín como una combinación lineal de los vectores base $|u\rangle$ y $|d\rangle$. Intentemos hacer esto ahora para los vectores $|r\rangle$ y $|l\rangle$ (del inglés *right* y *left*), que representan espines preparados a lo largo del eje $x$. Comenzaremos con $|r\rangle$. Como recordarás de la Lección 1, si $\mathcal{A}$ prepara inicialmente $|r\rangle$, y luego se rota para medir $\sigma_{z}$, habrá probabilidades iguales para arriba y abajo. Por lo tanto, $\alpha_{u}^{*}\alpha_{u}$ y $\alpha_{d}^{*}\alpha_{d}$ deben ser ambos iguales a $\frac{1}{2}$. Un vector simple que satisface esta regla es

$$|r\rangle = \frac{1}{\sqrt{2}} |u\rangle + \frac{1}{\sqrt{2}} |d\rangle. \quad (2.5)$$

Hay cierta ambigüedad en esta elección, pero como veremos más adelante, no es más que la ambigüedad en nuestra elección de las direcciones exactas para los ejes $x$ e $y$.

A continuación, observemos el vector $|l\rangle$. Esto es lo que sabemos: cuando el espín ha sido preparado en la configuración izquierda, las probabilidades para $\sigma_{z}$ son nuevamente iguales a $\frac{1}{2}$. Eso no es suficiente para determinar los valores $\alpha_{u}^{*}\alpha_{u}$ y $\alpha_{d}^{*}\alpha_{d}$, pero hay otra condición que podemos inferir. Anteriormente, te dije que $|u\rangle$ y $|d\rangle$ son ortogonales por la simple razón de que, si el espín está arriba, definitivamente no está abajo. Pero no hay nada especial sobre arriba y abajo que no sea también cierto para derecha e izquierda. En particular, si el espín está a la derecha, tiene probabilidad cero de estar a la izquierda. Así, por analogía con la Ec. 2.3,

$$\langle r|l\rangle = 0$$
$$\langle l|r\rangle = 0.$$

  4 

42 LECCIÓN 2. ESTADOS CUÁNTICOS

Esto prácticamente fija $|l\rangle$ en la forma

$$|l\rangle = \frac{1}{\sqrt{2}} |u\rangle - \frac{1}{\sqrt{2}} |d\rangle. \quad (2.6)$$

**Ejercicio 2.1:** Demuestra que el vector $|r\rangle$ en la Ec. 2.5 es ortogonal al vector $|l\rangle$ en la Ec. 2.6.

Nuevamente, hay cierta ambigüedad en la elección de $|l\rangle$. Esta se llama la ambigüedad de fase. Supongamos que multiplicamos $|l\rangle$ por cualquier número complejo $z$. Eso no tendrá efecto en si es ortogonal a $|r\rangle$, aunque en general el resultado ya no estará normalizado (tendrá longitud unitaria). Pero si elegimos $z = e^{i\theta}$ (donde $\theta$ puede ser cualquier número real), entonces no habrá efecto en la normalización porque $e^{i\theta}$ tiene magnitud unitaria. En otras palabras, $\alpha_{u}^{*}\alpha_{u} + \alpha_{d}^{*}\alpha_{d}$ seguirá siendo igual a 1. Dado que un número de la forma $z = e^{i\theta}$ se llama factor de fase, la ambigüedad se llama ambigüedad de fase. Más adelante, descubriremos que ninguna cantidad medible es sensible al factor de fase global, y por lo tanto podemos ignorarlo al especificar estados.

### 2.4 A lo largo del eje $y$

Finalmente, esto nos lleva a $|i\rangle$ y $|o\rangle$, los vectores que representan espines orientados a lo largo del eje $y$. Veamos las condiciones que deben satisfacer. Primero,

$$\langle i|o\rangle = 0. \quad (2.7)$$

  4 

2.4. A LO LARGO DEL EJE Y 43

Esta condición establece que adentro y afuera están representados por vectores ortogonales de la misma manera que arriba y abajo. Físicamente, esto significa que si el espín está adentro, definitivamente no está afuera.

Hay restricciones adicionales sobre los vectores $|i\rangle$ y $|o\rangle$. Usando las relaciones expresadas en las Ecs. 2.1 y 2.2, y los resultados estadísticos de nuestros experimentos, podemos escribir lo siguiente:

$$\begin{array}{rcl}{\langle o|u\rangle\langle u|o\rangle} & = & {\frac{1}{2}}\\ {} & {} & {}\\ {\langle o|d\rangle\langle d|o\rangle} & = & {\frac{1}{2}}\\ {} & {} & {} \\ {\langle i|u\rangle\langle u|i\rangle} & = & {\frac{1}{2}}\\ {} & {} & {}\\ {\langle i|d\rangle\langle d|i\rangle} & = & {\frac{1}{2}.} \end{array} \quad (2.8)$$

En las dos primeras ecuaciones, $|o\rangle$ toma el papel de $|A\rangle$ de las Ecs. 2.1 y 2.2. En las dos segundas, $|i\rangle$ toma ese papel. Estas condiciones establecen que si el espín está orientado a lo largo de $y$, y luego se mide a lo largo de $z$, es igualmente probable que esté arriba o abajo. También deberíamos esperar que si el espín se midiera a lo largo del eje $x$, sería igualmente probable que esté a la derecha o a la izquierda. Esto lleva a condiciones adicionales:

$$\begin{array}{rcl}{\langle o|r\rangle\langle r|o\rangle} & = & {\frac{1}{2}}\\ {} & {} & {}\\ {\langle o|l\rangle\langle l|o\rangle} & = & {\frac{1}{2}} \end{array} \quad (2.9)$$

  4 

44 LECCIÓN 2. ESTADOS CUÁNTICOS

$$\begin{array}{rcl}{\langle i|r\rangle\langle r|i\rangle} & = & {\frac{1}{2}}\\ {} & {} & {}\\ {\langle i|l\rangle\langle l|i\rangle} & = & {\frac{1}{2}.} \end{array} \quad (2.10)$$

Estas condiciones son suficientes para determinar la forma de los vectores $|i\rangle$ y $|o\rangle$, aparte de la ambigüedad de fase. Aquí está el resultado:

$$\begin{array}{rcl}{|i\rangle} & = & {\frac{1}{\sqrt{2}} |u\rangle + \frac{i}{\sqrt{2}} |d\rangle}\\ {} & {} & {}\\ {|o\rangle} & = & {\frac{1}{\sqrt{2}} |u\rangle - \frac{i}{\sqrt{2}} |d\rangle.} \end{array} \quad (2.11)$$

**Ejercicio 2.2:** Demuestra que $|i\rangle$ y $|o\rangle$ satisfacen todas las condiciones en las Ecs. 2.7, 2.8, 2.9 y 2.10. ¿Son únicos en ese aspecto?

Es interesante que dos de los componentes en las Ecs. 2.11 sean imaginarios. Por supuesto, hemos dicho todo el tiempo que el espacio de estados es un espacio vectorial complejo, pero hasta ahora no hemos tenido que usar números complejos en nuestros cálculos. ¿Son los números complejos en las Ecs. 2.11 una conveniencia o una necesidad? Dado nuestro marco para los estados de espín, no hay manera de evitarlos. Es algo tedioso demostrar esto, pero los pasos son sencillos. El siguiente ejercicio te da una hoja de ruta. La necesidad de números complejos es una característica general de la mecánica cuántica, y veremos más ejemplos a medida que avancemos.

  4 

2.5. CONTANDO PARÁMETROS 45

**Ejercicio 2.3:** Por el momento, olvida que las Ecs. 2.11 nos dan definiciones operativas para $|i\rangle$ y $|o\rangle$ en términos de $|u\rangle$ y $|d\rangle$, y supón que los componentes $\alpha$, $\beta$, $\gamma$ y $\delta$ son desconocidos:

$$|i\rangle = \alpha |u\rangle + \beta |d\rangle$$

$$|o\rangle = \gamma |u\rangle + \delta |d\rangle.$$

a) Usa las Ecs. 2.8 para mostrar que

$$\alpha^{*}\alpha = \beta^{*}\beta = \gamma^{*}\gamma = \delta^{*}\delta = \frac{1}{2}.$$

b) Usa el resultado anterior y las Ecs. 2.9-2.10 para mostrar que

$$\alpha^{*}\beta + \alpha \beta^{*} = \gamma^{*}\delta + \gamma \delta^{*} = 0.$$

c) Muestra que $\alpha^{*}\beta$ y $\gamma^{*}\delta$ deben ser cada uno puramente imaginarios.

Si $\alpha^{*}\beta$ es puramente imaginario, entonces $\alpha$ y $\beta$ no pueden ser ambos reales. El mismo razonamiento se aplica a $\gamma^{*}\delta$.

### 2.5 Contando Parámetros

Siempre es importante saber cuántos parámetros independientes se necesitan para caracterizar un sistema. Por ejemplo, las coordenadas generalizadas que usamos en el Volumen I (denominadas $q_{i}$) representaban cada una un grado de libertad independiente. Ese enfoque nos liberó de la difícil tarea de escribir ecuaciones explícitas para describir restricciones físicas. En la misma línea, nuestra próxima tarea es contar el número de estados físicamente distintos que hay para un espín. Lo haré de dos maneras, para mostrar que se obtiene la misma respuesta de cualquier forma.

  4 

46 LECCIÓN 2. ESTADOS CUÁNTICOS

La primera forma es simple. Apunta el aparato a lo largo de cualquier 3-vector unitario $\hat{n}$ y prepara un espín con $\sigma = +1$ a lo largo de ese eje. Si $\sigma = -1$, puedes pensar en el espín como orientado a lo largo del eje $-\hat{n}$. Por lo tanto, debe haber un estado para cada orientación del 3-vector unitario $\hat{n}$. ¿Cuántos parámetros se necesitan para especificar tal orientación? La respuesta es, por supuesto, dos. Se necesitan dos ángulos para definir una dirección en el espacio tridimensional. $^3$

Ahora, consideremos la misma pregunta desde otra perspectiva. El estado de espín general se define por dos números complejos, $\alpha_{u}$ y $\alpha_{d}$. Eso parece sumar cuatro parámetros reales, con cada parámetro complejo contando como dos reales. Pero recuerda que el vector tiene que estar normalizado como en la Ec. 2.4. La condición de normalización nos da una ecuación que involucra variables reales, y reduce el número de parámetros a tres.

Como dije antes, eventualmente veremos que las propiedades físicas de un vector de estado no dependen del factor de fase global. Esto significa que uno de los tres parámetros restantes es redundante, dejando solo dos —el mismo número de parámetros que necesitamos para especificar una dirección en el espacio tridimensional. Por lo tanto, hay suficiente libertad en la expresión

$$\alpha_{u}|u\rangle + \alpha_{d}|d\rangle$$

  4 

2.6. REPRESENTANDO ESTADOS DE ESPÍN

para describir todas las orientaciones posibles de un espín, a pesar de que solo hay dos resultados posibles de un experimento a lo largo de cualquier eje.

### 2.6 Representando Estados de Espín como Vectores Columna

Hasta ahora, hemos podido aprender mucho utilizando las formas abstractas de nuestros vectores de estado, es decir, $|u\rangle$ y $|d\rangle$ y así sucesivamente. Estas abstracciones nos ayudan a centrarnos en las relaciones matemáticas sin preocuparnos por detalles innecesarios. Sin embargo, pronto necesitaremos realizar cálculos detallados sobre estados de espín, y para ello necesitaremos escribir nuestros vectores de estado en forma de columna. Debido a la "indiferencia de fase", las representaciones de columna no son únicas, e intentaremos elegir las más simples y convenientes que podamos encontrar.

Como es habitual, comenzaremos con $|u\rangle$ y $|d\rangle$. Necesitamos que tengan longitud unitaria y que sean mutuamente ortogonales. Un par de columnas que satisface estos requisitos es

$$\begin{array}{l}{|u\rangle = \left( \begin{array}{c}{1}\\ {0} \end{array} \right)}\\ {|d\rangle = \left( \begin{array}{c}{0}\\ {1} \end{array} \right).} \end{array} \quad (2.12)$$

Con estos vectores columna en mano, será fácil crear vectores columna para $|r\rangle$ y $|l\rangle$ usando las Ecs. 2.5 y 2.6, y para $|i\rangle$ y $|o\rangle$ usando las Ecs. 2.11. Haremos eso en la próxima lección, donde se necesitan estos resultados.

  4 

2.7 Poniendo Todo Junto

Hemos cubierto mucho terreno en esta lección. Antes de continuar, hagamos un balance de lo que hemos hecho. Nuestro objetivo era sintetizar lo que sabemos sobre los espines y los espacios vectoriales. Descubrimos cómo usar vectores para representar estados de espín, y en el proceso vislumbramos el tipo de información que contiene (¡y no contiene!) un vector de estado. Aquí hay un breve resumen de lo que hicimos:

- Basándonos en nuestro conocimiento de las mediciones de espín, elegimos tres pares de vectores base mutuamente ortogonales. Por pares, los nombramos $|u\rangle$ y $|d\rangle$, $|r\rangle$ y $|l\rangle$, y $|i\rangle$ y $|o\rangle$. Debido a que los vectores base $|u\rangle$ y $|d\rangle$ representan estados físicamente distintos, pudimos afirmar que son mutuamente ortogonales. En otras palabras, $\langle u|d\rangle = 0$. Lo mismo ocurre para $|r\rangle$ y $|l\rangle$, y también para $|i\rangle$ y $|o\rangle$.

- Encontramos que se necesitan dos parámetros independientes para especificar un estado de espín, y luego elegimos arbitrariamente uno de los pares ortogonales, $|u\rangle$ y $|d\rangle$, como nuestros vectores base para representar todos los estados de espín —a pesar de que los dos números complejos en un vector de estado requieren cuatro números reales para especificarlos. ¿Cómo nos salimos con la nuestra? Fuimos lo suficientemente inteligentes para notar que estos cuatro números no son todos independientes.$^4$ La restricción de normalización (la probabilidad total debe ser igual a 1) elimina un parámetro independiente, y la "indiferencia de fase"

  4 

2.7. PONIENDO TODO JUNTO

(la física de un vector de estado no se ve afectada por su factor de fase global) elimina un segundo.

- Habiendo elegido $|u\rangle$ y $|d\rangle$ como nuestros vectores base principales, descubrimos cómo representar los otros dos pares de vectores base como combinaciones lineales de $|u\rangle$ y $|d\rangle$ utilizando restricciones adicionales de ortogonalidad y basadas en probabilidad.

- Finalmente, establecimos una forma de representar nuestros vectores base principales como columnas. Esta representación no es única. En la próxima lección, usaremos nuestros vectores columna $|u\rangle$ y $|d\rangle$ para derivar vectores columna para las otras dos bases.

Mientras lográbamos estos resultados concretos, tuvimos la oportunidad de ver algo de matemáticas de vectores de estado en acción y aprender algo sobre cómo estos objetos matemáticos corresponden a espines físicos. Aunque nos centraremos en el espín, los mismos conceptos y técnicas se aplican a otros sistemas cuánticos también. Por favor, tómate un poco de tiempo para asimilar el material que hemos cubierto hasta ahora antes de pasar a la siguiente lección. Como dije al principio, realmente valdrá la pena.

  5 

1

  5 

# Lección 3

## Principios de la Mecánica Cuántica

Art: No soy como tú, Lenny. Mi cerebro simplemente no fue construido para la mecánica cuántica.

Lenny: Nah, el mío tampoco. Simplemente no puedo visualizar esas cosas. Pero te diré, una vez conocí a un tipo que pensaba exactamente como un electrón.

Art: ¿Qué le pasó?

Lenny: Art, todo lo que te voy a decir es que no fue nada bonito.

Art: Hmm, supongo que ese gen no voló.

No, no fuimos construidos para percibir fenómenos cuánticos; no de la misma manera que fuimos construidos para sentir cosas clásicas como la fuerza o la temperatura. Pero somos criaturas muy adaptables y hemos podido sustituir las matemáticas abstractas por

  5 

52 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

los sentidos que nos faltan y que podrían habernos permitido visualizar directamente la mecánica cuántica. Y eventualmente desarrollamos nuevos tipos de intuición.

Esta lección introduce los principios de la mecánica cuántica. Para poder describir esos principios, necesitaremos algunas herramientas matemáticas nuevas. Empecemos.

### 3.1 Interludio Matemático: Operadores Lineales

#### 3.1.1 Máquinas y Matrices

Los estados en mecánica cuántica se describen matemáticamente como vectores en un espacio vectorial. Los observables físicos —las cosas que puedes medir— se describen mediante operadores lineales. Tomaremos esto como un axioma, y descubriremos más tarde (en la Sección 3.1.5) que los operadores correspondientes a observables físicos deben ser hermíticos además de lineales. La correspondencia entre operadores y observables es sutil, y entenderla requerirá algo de esfuerzo.

Los observables son las cosas que mides. Por ejemplo, podemos hacer mediciones directas de las coordenadas de una partícula; la energía, el momento o el momento angular de un sistema; o el campo eléctrico en un punto del espacio. Los observables también están asociados con un espacio vectorial, pero no son vectores de estado. Son las cosas que mides — $\sigma_{x}$ sería un ejemplo— y están representados por operadores lineales. A John Wheeler le gustaba llamar a tales objetos matemáticos máquinas. Imaginaba una máquina con dos puertos: una entrada

  5 

3.1. INTERLUDIO: OPERADORES LINEALES

y una salida. En el puerto de entrada insertas un vector, como $|A\rangle$. Los engranajes giran y la máquina entrega un resultado en el puerto de salida. Este resultado es otro vector, digamos $|B\rangle$.

Denotemos el operador con la letra negrita $\mathbf{M}$ (por "máquina"). Aquí está la ecuación para expresar el hecho de que $\mathbf{M}$ actúa sobre el vector $|A\rangle$ para dar $|B\rangle$:

$$\mathbf{M}|A\rangle = |B\rangle.$$

No todas las máquinas son operadores lineales. La linealidad implica algunas propiedades simples. Para empezar, un operador lineal debe dar una salida única para cada vector en el espacio. Podemos imaginar una máquina que da una salida para algunos vectores, pero simplemente tritura otros y no da nada. Esta máquina no sería un operador lineal. Debe salir algo para cualquier cosa que introduzcas.

La siguiente propiedad establece que cuando un operador lineal $\mathbf{M}$ actúa sobre un múltiplo de un vector de entrada, da el mismo múltiplo del vector de salida. Por lo tanto, si $\mathbf{M}|A\rangle = |B\rangle$, y $z$ es cualquier número complejo, entonces

$$\mathbf{M}z|A\rangle = z|B\rangle.$$

La única otra regla es que cuando $\mathbf{M}$ actúa sobre una suma de vectores, los resultados simplemente se suman:

$$\mathbf{M}\{|A\rangle + |B\rangle\} = \mathbf{M}|A\rangle + \mathbf{M}|B\rangle.$$

Para dar una representación concreta de los operadores lineales, volvemos a la representación de vectores fila y columna para bras

  5 

54 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

y kets que usamos en la Lección 1. La notación de fila-columna depende de nuestra elección de vectores base. Si el espacio vectorial es $N$-dimensional, elegimos un conjunto de $N$ vectores ket ortonormales (ortogonales y normalizados). Etiquetémoslos $|j\rangle$, y sus vectores bra duales $\langle j|$.

Ahora vamos a tomar la ecuación

$$\mathbf{M}|A\rangle = |B\rangle$$

y escribirla en forma de componentes. Como hicimos en la Ec. 1.3, representaremos un ket arbitrario $|A\rangle$ como una suma sobre vectores base:

$$|A\rangle = \sum_{j}\alpha_{j}|j\rangle.$$

Aquí, estamos usando $j$ como índice en lugar de $i$ para que no te sientas tentado a pensar que estamos hablando del estado de espín *in* (adentro). Ahora, representaremos $|B\rangle$ de la misma manera y sustituiremos ambas sustituciones en $\mathbf{M}|A\rangle = |B\rangle$. Eso da

$$\sum_{j}\mathbf{M}|j\rangle \alpha_{j} = \sum_{j}\beta_{j}|j\rangle.$$

El último paso es tomar el producto interno de ambos lados con un vector base particular $\langle k|$, resultando

$$\sum_{j}\langle k|\mathbf{M}|j\rangle \alpha_{j} = \sum_{j}\beta_{j}\langle k|j\rangle. \quad (3.1)$$

Para dar sentido a este resultado, recuerda que $\langle k|j\rangle$ es cero si $j$ y $k$ no son iguales, y 1 si son iguales. Eso significa que la suma en el lado derecho colapsa a un solo término, $\beta_{k}$.

  5 

3.1. INTERLUDIO: OPERADORES LINEALES 55

En el lado izquierdo, vemos un conjunto de cantidades $\langle k|\mathbf{M}|j\rangle \alpha_{j}$. Podemos abreviar $\langle k|\mathbf{M}|j\rangle$ con el símbolo $m_{kj}$. Nótese que cada $m_{kj}$ es solo un número complejo. Para ver por qué, piensa en $\mathbf{M}$ operando sobre $|j\rangle$ para dar algún nuevo vector ket. El producto interno de $\langle k|$ con este nuevo vector ket debe ser un número complejo. Las cantidades $m_{kj}$ se llaman los elementos de matriz de $\mathbf{M}$ y a menudo se organizan en una matriz cuadrada $N\times N$. Por ejemplo, si $N = 3$, podemos escribir la ecuación simbólica

$$\mathbf{M} = \left( \begin{array}{ccc}m_{11} & m_{12} & m_{13}\\ m_{21} & m_{22} & m_{23}\\ m_{31} & m_{32} & m_{33} \end{array} \right). \quad (3.2)$$

Esta ecuación implica un ligero abuso de notación que le daría indigestión a un purista. El lado izquierdo es un operador lineal abstracto y el lado derecho es una representación concreta del mismo en una base particular. Igualarlos es descuidado pero no debería causar confusión.

Ahora revisitemos la Ec. 3.1 y reemplacemos $\langle k|\mathbf{M}|j\rangle$ con $m_{kj}$. Obtenemos

$$\sum_{j}m_{kj}\alpha_{j} = \beta_{k}. \quad (3.3)$$

Podemos escribir esto en forma matricial también. La Ec. 3.3 se convierte en

$$\left( \begin{array}{ccc}m_{11} & m_{12} & m_{13}\\ m_{21} & m_{22} & m_{23}\\ m_{31} & m_{32} & m_{33} \end{array} \right)\left( \begin{array}{c}\alpha_{1}\\ \alpha_{2}\\ \alpha_{3} \end{array} \right) = \left( \begin{array}{c}\beta_{1}\\ \beta_{2}\\ \beta_{3} \end{array} \right). \quad (3.4)$$

  5 

56 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

Probablemente estés familiarizado con la regla para la multiplicación de matrices, pero te la recordaré por si acaso. Para calcular la primera entrada a la derecha, $\beta_{1}$, toma la primera fila de la matriz y "multiplícala escalarmente" con la columna $\alpha$:

$$\beta_{1} = m_{11}\alpha_{1} + m_{12}\alpha_{2} + m_{13}\alpha_{3}.$$

Para la segunda entrada, multiplica escalarmente la segunda fila de la matriz con la columna $\alpha$:

$$\beta_{2} = m_{21}\alpha_{1} + m_{22}\alpha_{2} + m_{23}\alpha_{3}.$$

Y así sucesivamente. Si no estás familiarizado con la multiplicación de matrices, corre a tu ordenador y búscalo de inmediato. Es una parte crucial de nuestro kit de herramientas, y asumiré que lo sabes de ahora en adelante.

Hay tanto ventajas como desventajas en representar vectores y operadores lineales de forma concreta con columnas, filas y matrices (conocidos colectivamente como componentes). Las ventajas son obvias. Los componentes proporcionan un conjunto completamente explícito de reglas aritméticas para operar la máquina. La desventaja es que dependen de una elección específica de vectores base. Las relaciones subyacentes entre vectores y operadores son independientes de la base particular que elijamos, y la representación concreta oscurece ese hecho.

#### 3.1.2 Valores Propios y Vectores Propios

En general, cuando un operador lineal actúa sobre un vector, cambiará la dirección del vector. Esto significa que lo que

  5 

3.1. INTERLUDIO: OPERADORES LINEALES 57

sale de la máquina no será simplemente el vector de entrada multiplicado por un número. Pero para un operador lineal particular, habrá ciertos vectores cuyas direcciones serán las mismas cuando salgan que cuando entraron. Estos vectores especiales se llaman vectores propios. La definición de un vector propio de $\mathbf{M}$ es un vector $|\lambda \rangle$ tal que

$$\mathbf{M}|\lambda \rangle = \lambda |\lambda \rangle. \quad (3.5)$$

El doble uso de $\lambda$ es admitidamente un poco confuso. En primer lugar, $\lambda$ (a diferencia de $|\lambda \rangle$) es un número —generalmente complejo, pero sigue siendo un número. Por otro lado, $|\lambda \rangle$ es un vector ket. Además, es un ket con una relación muy especial con $\mathbf{M}$. Cuando $|\lambda \rangle$ se introduce en la máquina $\mathbf{M}$, todo lo que sucede es que se multiplica por el número $\lambda$. Te daré un ejemplo. Si $\mathbf{M}$ es la matriz $2 \times 2$

$$\mathbf{M} = \left( \begin{array}{cc}3 & 0\\ 0 & -1 \end{array} \right),$$

entonces es fácil ver que el vector

$$\left( \begin{array}{c}{1}\\ {0} \end{array} \right)$$

simplemente se multiplica por 3 cuando $\mathbf{M}$ actúa sobre él. Pruébalo. $\mathbf{M}$ también tiene otro vector propio:

$$\left( \begin{array}{c}{0}\\ {1} \end{array} \right).$$

  5 

58 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

Cuando $\mathbf{M}$ actúa sobre este vector propio, multiplica el vector por un número diferente, a saber $-1$. Por otro lado, si $\mathbf{M}$ actúa sobre el vector

$$\left( \begin{array}{c}{1}\\ {1} \end{array} \right),$$

el vector no se multiplica simplemente por un número. $\mathbf{M}$ altera la dirección del vector así como su magnitud.

Así como los vectores que se multiplican por números cuando $\mathbf{M}$ actúa sobre ellos se llaman vectores propios de $\mathbf{M}$, las constantes que los multiplican se llaman valores propios. En general, los valores propios son números complejos. Aquí hay un ejemplo que puedes resolver por ti mismo. Toma la matriz

$$\mathbf{M} = \left( \begin{array}{cc}0 & 1\\ -1 & 0 \end{array} \right)$$

y muestra que el vector

$$\left( \begin{array}{c}{1}\\ {i} \end{array} \right)$$

es un vector propio con valor propio $-i$.

Los operadores lineales también pueden actuar sobre vectores bra. La notación para multiplicar $\langle B|$ por $\mathbf{M}$ es

$$\langle B|\mathbf{M}.$$

Mantendré la discusión breve diciéndote la regla para este tipo de multiplicación. Es más simple en forma de componentes.

  5 

3.1. INTERLUDIO: OPERADORES LINEALES 59

Recuerda que los vectores bra se representan en forma de componentes como vectores fila. Por ejemplo, el bra $\langle B|$ podría representarse por

$$\langle B| = \left( \begin{array}{ccc}\beta_{1}^{*} & \beta_{2}^{*} & \beta_{3}^{*} \end{array} \right).$$

La regla es nuevamente solo la multiplicación de matrices. Con un ligero abuso de notación,

$$\langle B|\mathbf{M} = \left( \begin{array}{ccc}\beta_{1}^{*} & \beta_{2}^{*} & \beta_{3}^{*} \end{array} \right)\left( \begin{array}{ccc}m_{11} & m_{12} & m_{13} \\ m_{21} & m_{22} & m_{23} \\ m_{31} & m_{32} & m_{33} \end{array} \right). \quad (3.6)$$

#### 3.1.3 Conjugación Hermítica

Podrías pensar que si $\mathbf{M}|A\rangle = |B\rangle$ entonces $\langle A|\mathbf{M} = \langle B|$, pero si lo haces, estás equivocado. El problema es la conjugación compleja. Incluso cuando $Z$ es solo un número complejo, si $Z|A\rangle = |B\rangle$, no es generalmente cierto que $\langle A|Z = \langle B|$. Tienes que conjugar complejamente $Z$ al pasar de kets a bras: $\langle A|Z^{*} = \langle B|$. Por supuesto, si $Z$ resulta ser un número real, entonces la conjugación compleja no tiene efecto —todo número real es igual a su propio complejo conjugado.

Lo que necesitamos es un concepto de conjugación compleja para operadores. Veamos la ecuación $\mathbf{M}|A\rangle = |B\rangle$ en notación de componentes,

$$\sum_{i}m_{ji}\alpha_{i} = \beta_{j},$$

y formemos su complejo conjugado,

  6 

60 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

$$\sum_{i}m_{ji}^{*}\alpha_{i}^{*} = \beta_{j}^{*}.$$

Nos gustaría escribir esta ecuación en forma matricial, usando bras en lugar de kets. Al hacer esto, tenemos que recordar que los vectores bra se representan mediante filas, no columnas. Para que el resultado funcione correctamente, también necesitamos reorganizar los elementos complejos conjugados de la matriz $\mathbf{M}$. La notación para esta reorganización es $\mathbf{M}^{\dagger}$, como se explica a continuación. Nuestra nueva ecuación es

$$\langle A|\mathbf{M}^{\dagger} = \left( \begin{array}{ccc}\alpha_{1}^{*} & \alpha_{2}^{*} & \alpha_{3}^{*} \end{array} \right)\left( \begin{array}{ccc}m_{11}^{*} & m_{21}^{*} & m_{31}^{*} \\ m_{12}^{*} & m_{22}^{*} & m_{32}^{*} \\ m_{13}^{*} & m_{23}^{*} & m_{33}^{*} \end{array} \right). \quad (3.7)$$

Observa cuidadosamente la diferencia entre la matriz en esta ecuación y la matriz en la Ec. 3.6. Verás dos diferencias. La más obvia es la conjugación compleja de cada elemento, pero también puedes ver una diferencia en los índices de los elementos. Por ejemplo, donde ves $m_{23}$ en la Ec. 3.6, ves $m_{32}^{*}$ en la Ec. 3.7. En otras palabras, las filas y las columnas se han intercambiado.

Cuando cambiamos una ecuación de la forma ket a la forma bra, debemos modificar la matriz en dos pasos:

1.  Intercambiar las filas y las columnas.
2.  Conjugar complejamente cada elemento de la matriz.

En notación matricial, intercambiar filas y columnas se llama transponer y se indica con un superíndice $T$. Por lo tanto, la transpuesta de la matriz $\mathbf{M}$ es

  6 

3.1. INTERLUDIO: OPERADORES LINEALES 61

$$\mathbf{M}^{T} = \left( \begin{array}{ccc}m_{11} & m_{21} & m_{31} \\ m_{12} & m_{22} & m_{32} \\ m_{13} & m_{23} & m_{33} \end{array} \right).$$

Nótese que transponer una matriz la voltea sobre la diagonal principal (la diagonal desde la esquina superior izquierda a la inferior derecha).

El complejo conjugado de una matriz transpuesta se llama su conjugada hermítica, denotada por una daga. Podrías pensar en la daga como un híbrido de la notación de estrella (*) usada en la conjugación compleja y la $T$ usada en la transposición. En símbolos,

$$\mathbf{M}^{\dagger} = [\mathbf{M}^{T}]^{*}.$$

Para resumir: si $\mathbf{M}$ actúa sobre el ket $|A\rangle$ para dar $|B\rangle$, entonces se sigue que $\mathbf{M}^{\dagger}$ actúa sobre el bra $\langle A|$ para dar $\langle B|$. En símbolos:

Si

$$\mathbf{M}|A\rangle = |B\rangle,$$

entonces

$$\langle A|\mathbf{M}^{\dagger} = \langle B|.$$

#### 3.1.4 Operadores Hermíticos

Los números reales juegan un papel especial en la física. Los resultados de cualquier medición son números reales. A veces, medimos dos cantidades, las juntamos con una $i$ (formando un

  6 

62 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

número complejo), y llamamos a este número el resultado de una medición. Pero en realidad es solo una forma de combinar dos mediciones reales. Si queremos ser pedantes, podríamos decir que las cantidades observables son iguales a sus propios complejos conjugados. Eso es, por supuesto, solo una forma elegante de decir que son reales. Vamos a descubrir muy pronto que los observables de la mecánica cuántica están representados por operadores lineales. ¿Qué tipo de operadores lineales? El tipo que es lo más parecido a un operador real. Los observables en mecánica cuántica están representados por operadores lineales que son iguales a sus propias conjugadas hermíticas. Se llaman operadores hermíticos en honor al matemático francés Charles Hermite. Los operadores hermíticos satisfacen la propiedad

$$\mathbf{M} = \mathbf{M}^{\dagger}.$$

En términos de elementos de matriz, esto se puede expresar como

$$m_{ji} = m_{ij}^{*}.$$

En otras palabras, si volteas una matriz hermítica sobre la diagonal principal y luego tomas su compleja conjugada, el resultado es el mismo que la matriz original. Los operadores (y matrices) hermíticos tienen algunas propiedades especiales. La primera es que sus valores propios son todos reales. Demostrémoslo.

Supongamos que $\lambda$ y $|\lambda \rangle$ representan un valor propio y el vector propio correspondiente del operador hermítico $\mathbf{L}$. En símbolos,

  6 

3.1. INTERLUDIO: OPERADORES LINEALES

$$\mathbf{L}|\lambda \rangle = \lambda |\lambda \rangle.$$

Entonces, por la definición de conjugación hermítica,

$$\langle \lambda |\mathbf{L}^{\dagger} = \langle \lambda |\lambda^{*}.$$

Sin embargo, dado que $\mathbf{L}$ es hermítico, es igual a $\mathbf{L}^{\dagger}$. Por lo tanto, podemos reescribir las dos ecuaciones como

$$\mathbf{L}|\lambda \rangle = \lambda |\lambda \rangle \quad (3.8)$$

y

$$\langle \lambda |\mathbf{L} = \langle \lambda |\lambda^{*}. \quad (3.9)$$

Ahora multiplica la Ec. 3.8 por $\langle \lambda |$ y la Ec. 3.9 por $|\lambda \rangle$. Se convierten en

$$\langle \lambda |\mathbf{L}|\lambda \rangle = \lambda \langle \lambda |\lambda \rangle$$

y

$$\langle \lambda |\mathbf{L}|\lambda \rangle = \lambda^{*}\langle \lambda |\lambda \rangle.$$

Obviamente, para que ambas ecuaciones sean verdaderas, $\lambda$ debe ser igual a $\lambda^{*}$. En otras palabras, $\lambda$ (y por lo tanto cualquier valor propio de un operador hermítico) debe ser real.

  6 

64 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

#### 3.1.5 Operadores Hermíticos y Bases Ortonormales

Llegamos ahora al teorema matemático básico —lo llamaré el teorema fundamental— que sirve como fundamento de la mecánica cuántica. La idea básica es que las cantidades observables en mecánica cuántica están representadas por operadores hermíticos. Es un teorema muy simple, pero es extremadamente importante. Podemos enunciarlo más precisamente como sigue:

## El Teorema Fundamental

- Los vectores propios de un operador hermítico son un conjunto completo. Esto significa que cualquier vector que el operador pueda generar puede expandirse como una suma de sus vectores propios.
- Si $\lambda_{1}$ y $\lambda_{2}$ son dos valores propios desiguales de un operador hermítico, entonces los vectores propios correspondientes son ortogonales.
- Incluso si los dos valores propios son iguales, los vectores propios correspondientes pueden elegirse para que sean ortogonales. Esta situación, donde dos vectores propios diferentes tienen el mismo valor propio, tiene un nombre: se llama degeneración. La degeneración entra en juego cuando dos operadores tienen vectores propios simultáneos, como se discute más adelante en la Sección 5.1.

Se puede resumir el teorema fundamental de la siguiente manera: Los vectores propios de un operador hermítico forman una base ortonormal. Demostrémoslo, comenzando con el segundo punto.

  6 

3.1. INTERLUDIO: OPERADORES LINEALES 65

Según la definición de vectores propios y valores propios, podemos escribir

$$\mathbf{L}|\lambda_{1}\rangle = \lambda_{1}|\lambda_{1}\rangle$$ $$\mathbf{L}|\lambda_{2}\rangle = \lambda_{2}|\lambda_{2}\rangle.$$

Ahora, usando el hecho de que $\mathbf{L}$ es hermítico (su propia conjugada hermítica), podemos voltear la primera ecuación en una ecuación de bra. Por lo tanto,

$$\langle \lambda_{1}|\mathbf{L} = \lambda_{1}\langle \lambda_{1}|$$ $$\mathbf{L}|\lambda_{2}\rangle = \lambda_{2}|\lambda_{2}\rangle.$$

A estas alturas, el truco debería ser obvio, pero lo detallaré. Toma la primera ecuación y forma su producto interno con $|\lambda_{2}\rangle$. Luego, toma la segunda ecuación y forma su producto interno con $\langle \lambda_{1}|$. El resultado es

$$\langle \lambda_{1}|\mathbf{L}|\lambda_{2}\rangle = \lambda_{1}\langle \lambda_{1}|\lambda_{2}\rangle$$ $$\langle \lambda_{1}|\mathbf{L}|\lambda_{2}\rangle = \lambda_{2}\langle \lambda_{1}|\lambda_{2}\rangle.$$

Restando, obtenemos

$$(\lambda_{1} - \lambda_{2})\langle \lambda_{1}|\lambda_{2}\rangle = 0.$$

Por lo tanto, si $\lambda_{1}$ y $\lambda_{2}$ son diferentes, el producto interno $\langle \lambda_{1}|\lambda_{2}\rangle$ debe ser cero. En otras palabras, los dos vectores propios deben ser ortogonales.

  6 

66 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

A continuación, demostremos que incluso si $\lambda_{1} = \lambda_{2}$, los dos vectores propios pueden elegirse para que sean ortogonales. Supongamos

$$\begin{array}{rcl}{\mathbf{L}|\lambda_{1}\rangle} & = & {\lambda |\lambda_{1}\rangle}\\ {} & {} & {}\\ {\mathbf{L}|\lambda_{2}\rangle} & = & {\lambda |\lambda_{2}\rangle.} \end{array} \quad (3.10)$$

En otras palabras, hay dos vectores propios distintos con el mismo valor propio. Debería quedar claro que cualquier combinación lineal de los dos vectores propios es también un vector propio con el mismo valor propio. Con tanta libertad, siempre es posible encontrar dos combinaciones lineales ortogonales.

Veamos cómo. Considera una combinación lineal arbitraria de estos dos vectores propios:

$$|A\rangle = \alpha |\lambda_{1}\rangle + \beta |\lambda_{2}\rangle.$$

Operando en ambos lados con $\mathbf{L}$, obtenemos

$$\mathbf{L}|A\rangle = \alpha \mathbf{L}|\lambda_{1}\rangle + \beta \mathbf{L}|\lambda_{2}\rangle,$$

$$\mathbf{L}|A\rangle = \alpha \lambda |\lambda_{1}\rangle + \beta \lambda |\lambda_{2}\rangle,$$

y finalmente

$$\mathbf{L}|A\rangle = \lambda (\alpha |\lambda_{1}\rangle + \beta |\lambda_{2}\rangle) = \lambda |A\rangle.$$

Esta ecuación demuestra que cualquier combinación lineal de $|\lambda_{1}\rangle$ y $|\lambda_{2}\rangle$ es también un vector propio de $\mathbf{L}$, con el mismo

  6 

3.1. INTERLUDIO: OPERADORES LINEALES 67

valor propio. Por suposición, estos dos vectores son linealmente independientes —de lo contrario, no representarían estados distintos. También supondremos que generan el subespacio de vectores propios de $\mathbf{L}$ que tienen valor propio $\lambda$. Hay un proceso directo, llamado procedimiento de Gram-Schmidt, para encontrar una base ortonormal para un subespacio, dado un conjunto de vectores independientes que generan el subespacio. En español sencillo, podemos encontrar dos vectores propios ortonormales escribiéndolos como una combinación lineal de $|\lambda_{1}\rangle$ y $|\lambda_{2}\rangle$. Esbozamos el procedimiento de Gram-Schmidt a continuación, en la Sección 3.1.6.

La parte final del teorema establece que los vectores propios son completos. En otras palabras, si el espacio es $N$-dimensional, habrá $N$ vectores propios ortonormales. La prueba es fácil y la dejaré para ti.

**Ejercicio 3.1:** Demuestra lo siguiente: Si un espacio vectorial es $N$-dimensional, se puede construir una base ortonormal de $N$ vectores a partir de los vectores propios de un operador hermítico.

#### 3.1.6 El Procedimiento de Gram-Schmidt

A veces nos encontramos con un conjunto de vectores propios linealmente independientes que no forman un conjunto ortonormal. Esto suele ocurrir cuando un sistema tiene estados degenerados —estados distintos que tienen el mismo valor propio. En esa situación, siempre podemos usar los vectores linealmente independientes que tenemos, para crear un conjunto ortonormal que genere el mismo espacio. El método es el procedimiento de Gram-Schmidt al que me referí anteriormente. La Fig. 3.1 ilustra cómo funciona para el caso simple de dos

  6 

68 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

vectores linealmente independientes. Comenzamos con los dos vectores $\vec{V}_{1}$ y $\vec{V}_{2}$, y a partir de estos construimos dos vectores ortonormales, $\hat{\mathbf{v}}_{1}$ y $\hat{\mathbf{v}}_{2}$.

 Figura 3.1: El Procedimiento de Gram-Schmidt. Dados dos vectores linealmente independientes, $\vec{V}_{1}$ y $\vec{V}_{2}$, que no son necesariamente ortogonales, podemos construir dos vectores ortonormales, $\hat{\mathbf{v}}_{1}$ y $\hat{\mathbf{v}}_{2}$. $\vec{V}_{2\perp}$ es un resultado intermedio utilizado en el proceso de construcción. Podemos extender este procedimiento a conjuntos más grandes de vectores linealmente independientes.  

El primer paso es dividir $\vec{V}_{1}$ por su propia longitud, $|\vec{V}_{1}|$, lo que nos da un vector unitario paralelo a $\vec{V}_{1}$. Llamaremos a ese vector unitario $\hat{\mathbf{v}}_{1}$, y $\hat{\mathbf{v}}_{1}$ se convierte en el primer vector de nuestro conjunto ortonormal. A continuación, proyectamos $\vec{V}_{2}$ sobre la dirección de $\hat{\mathbf{v}}_{1}$ formando el producto interno $\langle \vec{V}_{2}|\hat{\mathbf{v}}_{1}\rangle$. Ahora, restamos $\langle \vec{V}_{2}|\hat{\mathbf{v}}_{1}\rangle$ de $\vec{V}_{2}$. Llamaremos al resultado de esta resta $\vec{V}_{2\perp}$. Puedes ver en la Fig. 3.1 que $\vec{V}_{2\perp}$ es ortogonal a $\hat{\mathbf{v}}_{1}$. Por último, dividimos $\vec{V}_{2\perp}$ por su propia longitud para formar el segundo miembro de nuestra

  6 

3.2. LOS PRINCIPIOS

conjunto ortonormal, $\hat{\mathbf{v}}_{2}$. Debería quedar claro que podemos extender este procedimiento a conjuntos más grandes de vectores linealmente independientes en más dimensiones. Por ejemplo, si tuviéramos un tercer vector linealmente independiente, digamos $\vec{V}_{3}$, apuntando fuera de la página, restaríamos sus proyecciones sobre cada uno de los vectores unitarios $\hat{\mathbf{v}}_{1}$ y $\hat{\mathbf{v}}_{2}$, y luego dividiríamos el resultado por su propia longitud. $^{1}$

### 3.2 Los Principios

Ahora estamos completamente preparados para enunciar los principios de la mecánica cuántica, así que sin más preámbulos, hagámoslo.

Los principios involucran todos la idea de un observable, y presuponen la existencia de un espacio vectorial complejo subyacente cuyos vectores representan los estados del sistema. En esta lección, presentamos los cuatro principios que no involucran la evolución de los vectores de estado con el tiempo. En la Lección 4, añadiremos un quinto principio que aborda el desarrollo temporal de los estados del sistema.

Un observable también podría llamarse un medible. Es algo que puedes medir con un aparato adecuado. Anteriormente, hablamos sobre medir las componentes de un espín, $\sigma_{x}$, $\sigma_{y}$ y $\sigma_{z}$. Estos son ejemplos de observables. Volveremos a ellos, pero primero veamos los principios:

- **Principio 1:** Las cantidades observables o medibles de la mecánica cuántica están representadas por operadores lineales **L**.

  7 

70 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

Me doy cuenta de que este es el tipo de declaración hopelessmente abstracta que hace que la gente abandone la mecánica cuántica y se dedique al surf. No te preocupes —su significado se aclarará al final de la lección.

Pronto veremos que **L** también debe ser hermítico. Algunos autores consideran esto como un postulado, o principio básico. Nosotros hemos elegido en cambio derivarlo de los otros principios. El resultado final es el mismo de cualquier manera: los operadores que representan observables son hermíticos.

- **Principio 2:** Los resultados posibles de una medición son los valores propios del operador que representa el observable. Llamaremos a estos valores propios $\lambda_{i}$. El estado para el cual el resultado de una medición es inequívocamente $\lambda_{i}$ es el vector propio correspondiente $|\lambda_{i}\rangle$. No desempagues tu tabla de surf todavía.

Aquí hay otra forma de decirlo: si el sistema está en el estado propio $|\lambda_{i}\rangle$, se garantiza que el resultado de una medición es $\lambda_{i}$.

- **Principio 3:** Los estados inequívocamente distinguibles están representados por vectores ortogonales.

- **Principio 4:** Si $|A\rangle$ es el vector de estado de un sistema, y se mide el observable **L**, la probabilidad de observar el valor $\lambda_{i}$ es

$$P(\lambda_{i}) = \langle A|\lambda_{i}\rangle \langle \lambda_{i}|A\rangle. \quad (3.11)$$

Te recuerdo que los $\lambda_{i}$ son los valores propios de **L**, y $|\lambda_{i}\rangle$ son los vectores propios correspondientes.

  7 

3.2. LOS PRINCIPIOS

Estas breves declaraciones no son autoevidentes, y necesitaremos desarrollarlas. Por el momento, aceptemos el primer punto, a saber, que todo observable se identifica con un operador lineal. Ya podemos empezar a ver que un operador es una forma de empaquetar estados junto con sus valores propios, que son los resultados posibles de medir esos estados. Estas ideas deberían aclararse a medida que avanzamos.

Recordemos algunos puntos importantes de nuestra discusión anterior sobre espines. En primer lugar, el resultado de una medición es generalmente estadísticamente incierto. Sin embargo, para cualquier observable dado, hay estados particulares para los cuales el resultado es absolutamente cierto. Por ejemplo, si el aparato de medición de espín $\mathcal{A}$ está orientado a lo largo del eje $z$, el estado $|u\rangle$ siempre conduce al valor $\sigma_{z} = +1$. Del mismo modo, el estado $|d\rangle$ nunca da nada más que $\sigma_{z} = -1$. El Principio 1 nos da una nueva forma de ver estos hechos. Implica que cada observable ($\sigma_{x}, \sigma_{y},$ y $\sigma_{z}$) se identifica con un operador lineal específico en el espacio bidimensional de estados que describen el espín.

Cuando se mide un observable, el resultado es siempre un número real extraído de un conjunto de resultados posibles. Por ejemplo, si se mide la energía de un átomo, el resultado será uno de los niveles de energía establecidos del átomo. Para el caso familiar del espín, los valores posibles de cualquiera de las componentes son $\pm 1$. El aparato nunca da ningún otro resultado. El Principio 2 define la relación entre el operador que representa un observable y las salidas numéricas posibles de la medición. Es decir, el resultado de una medición es siempre uno de los valores propios del operador correspondiente. Por lo tanto, cada componente del operador de espín debe tener dos

  7 

72 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

valores propios iguales a $\pm 1.^{2}$

El Principio 3 es el más interesante. Al menos yo lo encuentro así. Habla de estados inequívocamente distintos, una idea clave que ya hemos encontrado. Dos estados son físicamente distintos si hay una medición que pueda diferenciarlos sin ambigüedad. Por ejemplo, $|u\rangle$ y $|d\rangle$ pueden distinguirse midiendo $\sigma_{z}$. Si te dan un espín y te dicen que está en el estado $|u\rangle$ o en el estado $|d\rangle$, para averiguar cuál de los dos estados es el correcto, todo lo que tienes que hacer es alinear $\mathcal{A}$ con el eje $z$ y medir $\sigma_{z}$. No hay posibilidad de error. Lo mismo es cierto para $|l\rangle$ y $|r\rangle$. Puedes distinguirlos midiendo $\sigma_{x}$.

Pero supongamos que en cambio te dicen que el espín está en uno de los dos estados, $|u\rangle$ o $|r\rangle$ (arriba o derecha). No hay nada que puedas medir que te diga inequívocamente el estado verdadero del espín. Medir $\sigma_{z}$ no lo hará. Si obtienes $\sigma_{z} = +1$, es posible que el estado inicial fuera $|r\rangle$ ya que hay un 50 por ciento de probabilidad de obtener esta respuesta en el estado $|r\rangle$. Por esa razón, se dice que $|u\rangle$ y $|d\rangle$ son físicamente distinguibles, pero $|u\rangle$ y $|r\rangle$ no lo son. Se podría decir que el producto interno de dos estados es una medida de la incapacidad para distinguirlos con certeza. A veces este producto interno se llama solapamiento. El Principio 3 requiere que los estados físicamente distintos estén representados por vectores de estado ortogonales, es decir, vectores sin solapamiento. Así, para estados de espín, $\langle u|d\rangle = 0$ pero $\langle u|r\rangle = \frac{1}{\sqrt{2}}$.

  7 

3.2. LOS PRINCIPIOS 73

Finalmente, el Principio 4 cuantifica estas ideas en una regla que expresa las probabilidades para varios resultados de un experimento. Si asumimos que un sistema ha sido preparado en el estado $|A\rangle$, y posteriormente se mide el observable $\mathbf{L}$, entonces el resultado será uno de los valores propios $\lambda_{i}$ del operador $\mathbf{L}$. Pero, en general, no hay forma de saber con certeza cuál de estos valores se observará. Solo hay una probabilidad —llamémosla $P(\lambda_{i})$— de que el resultado sea $\lambda_{i}$. El Principio 4 nos dice cómo calcular esa probabilidad, y se expresa en términos del solapamiento de $|A\rangle$ y $|\lambda_{i}\rangle$. Más precisamente, la probabilidad es el cuadrado de la magnitud del solapamiento:

$$P(\lambda_{i}) = |\langle A|\lambda_{i}\rangle|^{2}$$

o, equivalentemente,

$$P(\lambda_{i}) = \langle A|\lambda_{i}\rangle \langle \lambda_{i}|A\rangle.$$

Podrías preguntarte por qué la probabilidad no es el solapamiento mismo. ¿Por qué el cuadrado del solapamiento? Ten en cuenta que el producto interno de dos vectores no es siempre positivo, o incluso real. Las probabilidades, por otro lado, son tanto positivas como reales. Así que no tendría sentido identificar $P(\lambda_{i})$ con $\langle A|\lambda_{i}\rangle$. Pero el cuadrado de la magnitud, $\langle A|\lambda_{i}\rangle \langle \lambda_{i}|A\rangle$, es siempre positivo y real y, por lo tanto, puede identificarse con la probabilidad de un resultado dado.

Una consecuencia importante de los principios es la siguiente:

**Los operadores que representan observables son hermíticos.**

  7 

74 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

La razón de esto es doble. Primero, dado que el resultado de un experimento debe ser un número real, los valores propios de un operador $\mathbf{L}$ también deben ser reales. En segundo lugar, los vectores propios que representan resultados inequívocamente distinguibles deben tener diferentes valores propios, y también deben ser ortogonales. Estas condiciones son suficientes para demostrar que $\mathbf{L}$ debe ser hermítico.

### 3.3 Un Ejemplo: Operadores de Espín

Puede ser difícil de creer, pero los espines individuales —por simples que sean— todavía tienen mucho que enseñarnos sobre la mecánica cuántica, y planeamos exprimirlos al máximo. Nuestro objetivo en esta sección es escribir los operadores de espín en forma concreta, como matrices $2 \times 2$. Luego, veremos cómo funcionan en situaciones específicas. Construiremos nuestros operadores de espín y vectores de estado en breve. Pero antes de sumergirnos en los detalles, me gustaría decir un poco más sobre cómo se relacionan los operadores con las mediciones físicas. La relación es sutil, y diremos más sobre ella a medida que avancemos.

Como sabes, los físicos reconocen varios tipos de cantidades físicas, como escalares y vectores. No debería sorprender, entonces, que un operador asociado con la medición de un vector (como el espín) tenga un carácter vectorial propio.

En nuestros viajes hasta ahora, hemos visto más de un tipo de vector. El 3-vector es el más directo y sirve como prototipo. Es una representación matemática de una flecha en el espacio tridimensional, y a menudo se representa por tres números reales, escritos como una matriz columna. Debido a que sus componentes son de valor real, los 3-vectores no son lo suficientemente ricos

  7 

3.4. CONSTRUYENDO OPERADORES DE ESPÍN

para representar estados cuánticos. Para eso, necesitamos bras y kets, que tienen componentes de valor complejo.

¿Qué tipo de vector es el operador de espín $\sigma$? Definitivamente no es un vector de estado (un bra o un ket). Tampoco es exactamente un 3-vector, pero tiene un fuerte parecido familiar porque está asociado con una dirección en el espacio. De hecho, utilizaremos frecuentemente $\sigma$ como si fuera un simple 3-vector. Sin embargo, intentaremos mantener las cosas claras llamando a $\sigma$ un **3-vector operador**.

Pero ¿qué significa eso realmente? En términos físicos, significa esto: Así como un aparato de medición de espín solo puede responder preguntas sobre la orientación de un espín en una dirección específica, un operador de espín solo puede proporcionar información sobre la componente del espín en una dirección específica. Para medir físicamente el espín en una dirección diferente, necesitamos rotar el aparato para que apunte en la nueva dirección. La misma idea se aplica al operador de espín —si queremos que nos hable sobre la componente del espín en una nueva dirección, también debe ser "rotado", pero este tipo de rotación se logra matemáticamente. El resultado final es que hay un operador de espín para cada dirección en la que el aparato puede ser orientado.

### 3.4 Construyendo Operadores de Espín

Ahora, trabajemos en los detalles de los operadores de espín. El primer objetivo es construir operadores para representar las componentes del espín, $\sigma_{x}$, $\sigma_{y}$ y $\sigma_{z}$. Luego construiremos sobre esos resultados para construir un operador que represente una componente de espín en cualquier dirección. Como es habitual, comenzamos con $\sigma_{z}$. Sabemos que $\sigma_{z}$ tiene valores definidos e inequívocos para los estados $|u\rangle$ y $|d\rangle$,

  7 

76 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

y que los valores de medición correspondientes son $\sigma_{z} = +1$ y $\sigma_{z} = -1$. Esto es lo que nos dicen los primeros tres principios:

- **Principio 1:** Cada componente de $\sigma$ está representada por un operador lineal.
- **Principio 2:** Los vectores propios de $\sigma_{z}$ son $|u\rangle$ y $|d\rangle$. Los valores propios correspondientes son $+1$ y $-1$. Podemos expresar esto con las ecuaciones abstractas

$$\begin{array}{rcl}{\sigma_{z}|u\rangle} & = & {|u\rangle}\\ {} & {} & {}\\ {\sigma_{z}|d\rangle} & = & {-|d\rangle.} \end{array} \quad (3.12)$$

- **Principio 3:** Los estados $|u\rangle$ y $|d\rangle$ son ortogonales entre sí. Esto puede expresarse como

$$\langle u|d\rangle = 0. \quad (3.13)$$

Recordando nuestras representaciones columna de $|u\rangle$ y $|d\rangle$ de las Ecs. 2.12, podemos escribir las Ecs. 3.12 en forma matricial como

$$\left( \begin{array}{cc}(\sigma_{z})_{11} & (\sigma_{z})_{12}\\ (\sigma_{z})_{21} & (\sigma_{z})_{22} \end{array} \right)\left( \begin{array}{c}1\\ 0 \end{array} \right) = \left( \begin{array}{c}1\\ 0 \end{array} \right) \quad (3.14)$$

y

$$\left( \begin{array}{cc}(\sigma_{z})_{11} & (\sigma_{z})_{12}\\ (\sigma_{z})_{21} & (\sigma_{z})_{22} \end{array} \right)\left( \begin{array}{c}0\\ 1 \end{array} \right) = -\left( \begin{array}{c}0\\ 1 \end{array} \right). \quad (3.15)$$

  7 

3.4. CONSTRUYENDO OPERADORES DE ESPÍN

Solo hay una matriz que satisface estas ecuaciones. Dejo como ejercicio demostrar que

$$\left( \begin{array}{cc}(\sigma_{z})_{11} & (\sigma_{z})_{12}\\ (\sigma_{z})_{21} & (\sigma_{z})_{22} \end{array} \right) = \left( \begin{array}{cc}1 & 0\\ 0 & -1 \end{array} \right) \quad (3.16)$$

o, más concisamente,

$$\sigma_{z} = \left( \begin{array}{cc}1 & 0\\ 0 & -1 \end{array} \right). \quad (3.17)$$

**Ejercicio 3.2:** Demuestra que la Ec. 3.16 es la única solución a las Ecs. 3.14 y 3.15.

Este es nuestro primer ejemplo de un operador mecánico-cuántico. Resumamos lo que implicó. Primero, algunos datos experimentales: hay ciertos estados que llamamos $|u\rangle$ y $|d\rangle$, en los cuales la medición de $\sigma_{z}$ da resultados inequívocos $\pm 1$. Luego, los principios nos dijeron que $|u\rangle$ y $|d\rangle$ son ortogonales y son vectores propios de un operador lineal $\sigma_{z}$. Finalmente, aprendimos de los principios que los valores propios correspondientes son los valores observados (o medidos), nuevamente $\pm 1$. Eso es todo lo que se necesita para derivar la Ec. 3.17.

¿Podemos hacer lo mismo para las otras dos componentes del espín, $\sigma_{x}$ y $\sigma_{y}$? Sí, podemos. $^3$ Los vectores propios de $\sigma_{x}$ son $|r\rangle$ y $|l\rangle$, con valores propios $+1$ y $-1$ respectivamente. En forma de ecuación,

  7 

78 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

$$\begin{array}{rcl}{\sigma_{x}|r\rangle} & = & {|r\rangle}\\ {} & {} & {}\\ {\sigma_{x}|l\rangle} & = & {-|l\rangle.} \end{array} \quad (3.18)$$

Recordemos que $|r\rangle$ y $|l\rangle$ son superposiciones lineales de $|u\rangle$ y $|d\rangle$:

$$\begin{array}{rcl}{|r\rangle} & = & \frac{1}{\sqrt{2}} |u\rangle + \frac{1}{\sqrt{2}} |d\rangle \\ |l\rangle & = & \frac{1}{\sqrt{2}} |u\rangle - \frac{1}{\sqrt{2}} |d\rangle. \end{array} \quad (3.19)$$

Sustituyendo los vectores columna apropiados para $|u\rangle$ y $|d\rangle$, obtenemos

$$|r\rangle = \left( \begin{array}{c}\frac{1}{\sqrt{2}}\\ \frac{1}{\sqrt{2}} \end{array} \right), \quad |l\rangle = \left( \begin{array}{c}\frac{1}{\sqrt{2}}\\ \frac{-1}{\sqrt{2}} \end{array} \right).$$

Para hacer las Ecs. 3.18 concretas, podemos escribirlas en forma matricial:

$$\left( \begin{array}{cc}(\sigma_{x})_{11} & (\sigma_{x})_{12}\\ (\sigma_{x})_{21} & (\sigma_{x})_{22} \end{array} \right)\left( \begin{array}{c}\frac{1}{\sqrt{2}}\\ \frac{1}{\sqrt{2}} \end{array} \right) = \left( \begin{array}{c}\frac{1}{\sqrt{2}}\\ \frac{1}{\sqrt{2}} \end{array} \right)$$

y

  7 

3.4. CONSTRUYENDO OPERADORES DE ESPÍN 79

$$\left( \begin{array}{cc}(\sigma_{x})_{11} & (\sigma_{x})_{12}\\ (\sigma_{x})_{21} & (\sigma_{x})_{22} \end{array} \right)\left( \begin{array}{c}\frac{1}{\sqrt{2}}\\ \frac{-1}{\sqrt{2}} \end{array} \right) = -\left( \begin{array}{c}\frac{1}{\sqrt{2}}\\ \frac{-1}{\sqrt{2}} \end{array} \right).$$

Si escribes estas ecuaciones en forma desarrollada, se convierten en cuatro ecuaciones fácilmente resolubles para los elementos de matriz $(\sigma_{x})_{11}, (\sigma_{x})_{12}, (\sigma_{x})_{21},$ y $(\sigma_{x})_{22}$. Aquí está la solución:

$$\left( \begin{array}{cc}(\sigma_{x})_{11} & (\sigma_{x})_{12}\\ (\sigma_{x})_{21} & (\sigma_{x})_{22} \end{array} \right) = \left( \begin{array}{cc}0 & 1\\ 1 & 0 \end{array} \right)$$

o

$$\sigma_{x} = \left( \begin{array}{cc}0 & 1\\ 1 & 0 \end{array} \right). \quad (3.20)$$

Finalmente, podemos hacer lo mismo para $\sigma_{y}$. Los vectores propios de $\sigma_{y}$ son los estados adentro y afuera $|i\rangle$ y $|o\rangle$:

$$\begin{array}{l}{{|i\rangle=\frac{1}{\sqrt{2}}|u\rangle+\frac{i}{\sqrt{2}}|d\rangle}}\\ {{|o\rangle=\frac{1}{\sqrt{2}}|u\rangle-\frac{i}{\sqrt{2}}|d\rangle.}}\end{array} \quad (3.21)$$

En forma de componentes, estas ecuaciones se convierten en

$$|i\rangle = \left( \begin{array}{c}\frac{1}{\sqrt{2}}\\ \frac{i}{\sqrt{2}} \end{array} \right), \quad |o\rangle = \left( \begin{array}{c}\frac{1}{\sqrt{2}}\\ \frac{-i}{\sqrt{2}} \end{array} \right),$$

y un cálculo fácil da

  8 

80 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

$$\sigma_{y} = \left( \begin{array}{cc}0 & -i\\ i & 0 \end{array} \right). \quad (3.22)$$

Para resumir, los tres operadores $\sigma_{x}$, $\sigma_{y}$ y $\sigma_{z}$ están representados por las tres matrices

$$\begin{array}{rcl}{\sigma_{z}} & = & {\left( \begin{array}{cc}1 & 0\\ 0 & -1 \end{array} \right)}\\ {\sigma_{x}} & = & {\left( \begin{array}{cc}0 & 1\\ 1 & 0 \end{array} \right)}\\ {\sigma_{y}} & = & {\left( \begin{array}{cc}0 & -i\\ i & 0 \end{array} \right).} \end{array} \quad (3.23)$$

Estas tres matrices son muy famosas y llevan el nombre de su descubridor. Son las matrices de Pauli. $^{4}$

### 3.5 Un Error Común

Este es un momento conveniente para advertirte sobre un peligro potencial. La correspondencia entre operadores y mediciones es fundamental en la mecánica cuántica. También es muy fácil de malinterpretar. Esto es lo que es cierto sobre los operadores en mecánica cuántica:

1.  Los operadores son las cosas que usamos para calcular valores propios y vectores propios.
2.  Los operadores actúan sobre vectores de estado (que son objetos matemáticos abstractos), no sobre sistemas físicos reales.

  8 

3.  Cuando un operador actúa sobre un vector de estado, produce un nuevo vector de estado.

Habiendo dicho lo que es cierto sobre los operadores, quiero advertirte sobre un error común. A menudo se piensa que medir un observable es lo mismo que operar con el operador correspondiente sobre el estado. Por ejemplo, supongamos que estamos interesados en medir un observable $\mathbf{L}$. La medición es algún tipo de operación que el aparato hace al sistema, pero esa operación no es de ninguna manera lo mismo que actuar sobre el estado con el operador $\mathbf{L}$. Por ejemplo, si el estado del sistema antes de hacer la medición es $|A\rangle$, no es correcto decir que la medición de $\mathbf{L}$ cambia el estado a $\mathbf{L}|A\rangle$.

Para entender esto, veamos un ejemplo de cerca. Afortunadamente, el ejemplo del espín de la subsección anterior es justo lo que necesitamos. Recordemos las Ecs. 3.12:

$$\sigma_{z}|u\rangle = |u\rangle$$

$$\sigma_{z}|d\rangle = -|d\rangle.$$

En estas situaciones, no hay trampa porque $|u\rangle$ y $|d\rangle$ son vectores propios de $\sigma_{z}$. Si el sistema se prepara en, digamos, el estado $|d\rangle$, una medición definitivamente dará el resultado $-1$, y el operador $\sigma_{z}$ transforma el estado preparado en el estado post-medición correspondiente, $- |d\rangle$. El estado $- |d\rangle$ es el mismo que $|d\rangle$ excepto por una constante multiplicativa, por lo que los dos estados son realmente el mismo. No hay problemas aquí.

  8 

82 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

Pero ahora revisemos la acción de $\sigma_{z}$ sobre el estado preparado $|r\rangle$, que no es uno de sus vectores propios. De la Ec. 3.19, sabemos que

$$|r\rangle = \frac{1}{\sqrt{2}} |u\rangle + \frac{1}{\sqrt{2}} |d\rangle.$$

Actuando sobre este vector de estado con $\sigma_{z}$ da el resultado

$$\sigma_{z}|r\rangle = \frac{1}{\sqrt{2}}\sigma_{z}|u\rangle + \frac{1}{\sqrt{2}}\sigma_{z}|d\rangle$$

o

$$\sigma_{z}|r\rangle = \frac{1}{\sqrt{2}} |u\rangle - \frac{1}{\sqrt{2}} |d\rangle. \quad (3.24)$$

Bien, aquí está nuestra trampa. Contrariamente a lo que puedas pensar, el vector de estado en el lado derecho de la Ec. 3.24 definitivamente no es el estado que resultaría de una medición de $\sigma_{z}$. Ese resultado de medición sería $+1$, dejando el sistema en el estado $|u\rangle$, o $-1$, dejándolo en el estado $|d\rangle$. Ninguno de estos resultados dejaría el vector de estado del sistema en la superposición representada por la Ec. 3.24.

Pero seguramente ese vector de estado debe tener algo que ver con el resultado de la medición? De hecho, sí. Encontraremos parte de la respuesta en la Lección 4, donde veremos cómo el nuevo vector de estado nos permite calcular las probabilidades de cada resultado posible de la medición. Sin embargo, el resultado de una medición no puede describirse adecuadamente sin tener en cuenta el aparato como parte del sistema. Lo que realmente sucede durante una medición es el tema de la Sección 7.8.

  8 

3.6. 3-VECTORES OPERADORES REVISITADOS

### 3.6 3-Vectores Operadores Revisitados

Ahora, revisitemos la idea de un 3-vector operador. He llamado a $\sigma_{x}$, $\sigma_{y}$ y $\sigma_{z}$ las componentes del espín a lo largo de los tres ejes, lo que implica que son las componentes de algún tipo de 3-vector. Este es un buen momento para volver a las dos nociones de vectores que aparecen todo el tiempo en física. Primero, está el vector de jardín común en el espacio tridimensional ordinario, que hemos decidido llamar 3-vector. Como hemos visto, un 3-vector tiene componentes a lo largo de las tres direcciones del espacio.

El otro significado completamente distinto del término vector es el vector de estado de un sistema. Por lo tanto, $|u\rangle$ y $|d\rangle$, $|r\rangle$ y $|l\rangle$, y $|i\rangle$ y $|o\rangle$ son vectores de estado en un espacio bidimensional de estados de espín. ¿Qué pasa con $\sigma_{x}$, $\sigma_{y}$ y $\sigma_{z}$? ¿Son vectores, y si es así, de qué tipo?

Claramente, no son vectores de estado; son operadores (escritos como matrices) que corresponden a las tres componentes medibles del espín. De hecho, estos 3-vectores operadores representan un nuevo tipo de vector. Son diferentes tanto de los vectores de estado como de los 3-vectores ordinarios. Sin embargo, debido a que los operadores de espín se comportan tanto como 3-vectores, no hace daño pensar en ellos de esa manera, y eso es lo que haremos aquí.

Medimos las componentes del espín orientando el aparato $\mathcal{A}$ a lo largo de cualquiera de los tres ejes y luego activándolo. Pero entonces, ¿por qué no orientar $\mathcal{A}$ a lo largo de cualquier eje y medir la componente de $\sigma$ a lo largo de ese eje? En otras palabras, toma cualquier 3-vector unitario $\hat{n}$ con componentes $n_{x}$, $n_{y}$ y $n_{z}$, y orienta

  8 

84 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

el aparato $\mathcal{A}$ con su flecha a lo largo de $\hat{n}$. Activar $\mathcal{A}$ mediría entonces la componente de $\sigma$ a lo largo del eje $\hat{n}$. Debe haber un operador que corresponda a esta cantidad medible.

Si $\sigma$ realmente se comporta como un 3-vector, entonces la componente de $\sigma$ a lo largo de $\hat{n}$ no es más que el producto escalar ordinario de $\sigma$ y $\hat{n}$. $^{5,6}$ Denotemos esa componente de $\sigma$ por $\sigma_{n}$, de modo que

$$\sigma_{n} = \vec{\sigma}\cdot \hat{n}$$

o, en forma expandida,

$$\sigma_{n} = \sigma_{x}n_{x} + \sigma_{y}n_{y} + \sigma_{z}n_{z}. \quad (3.25)$$

Para aclarar el significado de esta ecuación, ten en cuenta que los componentes de $\hat{n}$ son solo números. Ellos mismos no son operadores. La Ec. 3.25 describe un vector-operador que se construye como la suma de tres términos, cada uno conteniendo un coeficiente numérico $n_{x}$, $n_{y}$ o $n_{z}$. Para ser más concretos, podemos escribir la Ec. 3.25 en forma matricial:

$$\sigma_{n} = n_{x}\left( \begin{array}{cc}0 & 1\\ 1 & 0 \end{array} \right) + n_{y}\left( \begin{array}{cc}0 & -i\\ i & 0 \end{array} \right) + n_{z}\left( \begin{array}{cc}1 & 0\\ 0 & -1 \end{array} \right).$$

  8 

3.7. COSECHANDO LOS RESULTADOS 85

O incluso más explícitamente, podemos combinar estos tres términos en una sola matriz:

$$\sigma_{n} = \left( \begin{array}{cc}{n_{z}} & {(n_{x} - in_{y})}\\ {(n_{x} + in_{y})} & {-n_{z}} \end{array} \right). \quad (3.26)$$

¿Para qué sirve esto? No mucho, hasta que encontremos los vectores propios y valores propios de $\sigma_{n}$. Pero una vez que hagamos eso, sabremos los resultados posibles de una medición a lo largo de la dirección de $\hat{n}$. Y también podremos calcular probabilidades para esos resultados. En otras palabras, tendremos una imagen completa de las mediciones de espín en el espacio tridimensional. Eso es bastante genial, si lo digo yo mismo.

### 3.7 Cosechando los Resultados

Ahora estamos en posición de hacer algunos cálculos reales, algo que debería hacer saltar de alegría a tu físico interior. Veamos el caso especial donde $\hat{n}$ se encuentra en el plano $x - z$, que es el plano de esta página. Dado que $\hat{n}$ es un vector unitario, podemos escribir

$$n_{z} = \cos \theta$$ $$n_{x} = \sin \theta$$ $$n_{y} = 0,$$

donde $\theta$ es el ángulo entre el eje $z$ y el eje $\hat{n}$. Sustituyendo estos valores en la Ec. 3.26, podemos escribir

$$\sigma_{n} = \left( \begin{array}{cc}{\cos \theta} & {\sin \theta}\\ {\sin \theta} & {-\cos \theta} \end{array} \right).$$

  8 

86 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

**Ejercicio 3.3:** Calcula los vectores propios y valores propios de $\sigma_{n}$. *Sugerencia*: Supón que el vector propio $\lambda_{1}$ tiene la forma

$$\left( \begin{array}{c}{\cos \frac{\theta}{2}}\\ {\sin \frac{\theta}{2}} \end{array} \right)$$

donde $\alpha$ es un parámetro desconocido. Sustituye este vector en la ecuación de valores propios y resuelve para $\alpha$ en términos de $\theta$. ¿Por qué usamos un solo parámetro $\alpha$? Observa que nuestro vector columna sugerido debe tener longitud unitaria.

Aquí están los resultados:

$$\lambda_{1} = 1$$ $$|\lambda_{1}\rangle = \left( \begin{array}{c}{\cos \frac{\theta}{2}}\\ {\sin \frac{\theta}{2}} \end{array} \right)$$

y

$$\lambda_{2} = -1$$ $$|\lambda_{2}\rangle = \left( \begin{array}{c}{-\sin \frac{\theta}{2}}\\ {\cos \frac{\theta}{2}} \end{array} \right).$$

Nótese algunos hechos importantes. Primero, los dos valores propios son nuevamente $+1$ y $-1$. Esto no debería ser una sorpresa; el aparato $\mathcal{A}$ solo puede dar una de estas dos respuestas sin importar hacia dónde apunte. Pero es bueno ver esto surgir de las ecuaciones. El segundo hecho es que los dos vectores propios son ortogonales.

  8 

3.7. COSECHANDO LOS RESULTADOS 87

Ahora estamos listos para hacer una predicción experimental. Supongamos que $\mathcal{A}$ inicialmente apunta a lo largo del eje $z$ y que preparamos un espín en el estado arriba $|u\rangle$. Luego, rotamos $\mathcal{A}$ para que se sitúe a lo largo del eje $\hat{n}$. ¿Cuál es la probabilidad de observar $\sigma_{n} = +1?$ De acuerdo con el Principio 4, y usando las expansiones de fila y columna de $\langle u|$ y $|\lambda_{1}\rangle$, la respuesta es

$$P(+1) = |\langle u|\lambda_{1}\rangle|^{2} = \cos^{2}\frac{\theta}{2}. \quad (3.27)$$

De manera similar, para la misma configuración,

$$P(-1) = |\langle u|\lambda_{2}\rangle|^{2} = \sin^{2}\frac{\theta}{2}. \quad (3.28)$$

Con este resultado, hemos casi cerrado el círculo. Al introducir los espines, hicimos la afirmación de que si preparamos un gran número de ellos en el estado arriba y luego medimos su componente a lo largo de $\hat{n}$, en un ángulo $\theta$ con respecto al eje $z$, entonces el valor promedio de los resultados medidos sería $\cos \theta$ —el mismo resultado que obtendríamos para un simple 3-vector en física clásica. ¿Nuestro marco matemático da el mismo resultado? ¡Más le vale! Si una teoría está en desacuerdo con el experimento, es la teoría la que tiene que irse. Veamos qué tan bien se sostiene nuestra teoría hasta ahora.

Desafortunadamente, necesitamos hacer un poco de trampa usando una ecuación que no explicaremos completamente hasta la próxima lección. Esta es la ecuación que nos dice cómo calcular el valor promedio (también llamado valor esperado) de una medición. Aquí está:

$$\langle \mathbf{L}\rangle = \sum_{i}\lambda_{i}P(\lambda_{i}). \quad (3.29)$$

  8 

88 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

Vale la pena mencionar que la Ec. 3.29 es solo una fórmula estándar para un valor promedio. No es exclusiva de la mecánica cuántica.

Para calcular el valor esperado de una medición correspondiente al operador $\mathbf{L}$, multiplicamos cada valor propio por su probabilidad, y luego sumamos los resultados. Por supuesto, el operador que estamos viendo ahora es solo $\sigma_{n}$, y ya tenemos todos los valores que necesitamos. Sustituyamos. Usando las Ecs. 3.27 y 3.28, junto con nuestros valores propios conocidos, podemos escribir

$$\langle \sigma_{n}\rangle = (+1)\cos^{2}\frac{\theta}{2} + (-1)\sin^{2}\frac{\theta}{2}$$

o

$$\langle \sigma_{n}\rangle = \cos^{2}\frac{\theta}{2} - \sin^{2}\frac{\theta}{2}.$$

Si recuerdas tu trigonometría, esto da

$$\langle \sigma_{n}\rangle = \cos \theta,$$

¡lo que concuerda perfectamente con el experimento! ¡Sí! ¡Lo hemos logrado!

Habiendo llegado tan lejos, quizás quieras probar suerte con un problema ligeramente más general. Como antes, comenzamos con el aparato $\mathcal{A}$ apuntando en la dirección $z$. Pero ahora, una vez que el espín ha sido preparado en el estado arriba, podemos rotar $\mathcal{A}$ a una dirección arbitraria en el espacio para el segundo conjunto de mediciones. En esta situación, $n_{y} \neq 0$. Adelante, inténtalo.

**Ejercicio 3.4:** Sean $n_{z} = \cos \theta$, $n_{x} = \sin \theta \cos \phi$, y $n_{y} = \sin \theta \sin \phi$. Los ángulos $\theta$ y $\phi$ están definidos según las convenciones habituales para coordenadas esféricas (Fig. 3.2). Calcula los valores propios y vectores propios para la matriz de la Ec. 3.26.

  8 

3.7. COSECHANDO LOS RESULTADOS 89

 Figura 3.2: Coordenadas Esféricas. Este diagrama ilustra las etiquetas de coordenadas esféricas convencionales $r$, $\theta$ y $\phi$. También ilustra la conversión a coordenadas cartesianas: $x = r \sin \theta \cos \phi$, $y = r \sin \theta \sin \phi$, y $z = r \cos \theta$.  

  9 

90 LECCIÓN 3. PRINCIPIOS DE LA MECÁNICA CUÁNTICA

También podrías intentar resolver un ejemplo mucho más elaborado que involucra dos direcciones, $\hat{n}$ y $\hat{m}$. En esta configuración, $\mathcal{A}$ no solo termina en una dirección arbitraria; también comienza en una dirección (diferente) arbitraria.

**Ejercicio 3.5:** Supongamos que se prepara un espín de modo que $\sigma_{m} = +1$. Luego, el aparato se rota a la dirección $\hat{n}$ y se mide $\sigma_{n}$. ¿Cuál es la probabilidad de que el resultado sea $+1$? Nótese que $\sigma_{m} = \sigma \cdot \hat{m}$, usando la misma convención que usamos para $\sigma_{n}$.

La respuesta es el cuadrado del coseno de la mitad del ángulo entre $\hat{m}$ y $\hat{n}$. ¿Puedes demostrarlo?

### 3.8 El Principio de Polarización del Espín

Hay un teorema importante que puedes intentar demostrar. Lo llamaré

**El Principio de Polarización del Espín:** Cualquier estado de un solo espín es un vector propio de alguna componente del espín.

En otras palabras, dado cualquier estado

$$|A\rangle = \alpha_{u}|u\rangle + \alpha_{d}|d\rangle,$$

existe alguna dirección $\hat{n}$, tal que

$$\vec{\sigma}\cdot \vec{n} |A\rangle = |A\rangle.$$

  9 

3.8. EL PRINCIPIO DE POLARIZACIÓN DEL ESPÍN 91

Esto significa que para cualquier estado de espín, hay alguna orientación del aparato $\mathcal{A}$ tal que $\mathcal{A}$ registrará $+1$ cuando actúe. En lenguaje físico, decimos que los estados de un espín se caracterizan por un vector de polarización, y a lo largo de ese vector de polarización la componente del espín es predeciblemente $+1$ asumiendo, por supuesto, que conoces el vector de estado.

Una consecuencia interesante de este teorema es que no hay estado para el cual los valores esperados de las tres componentes del espín sean cero. Hay una forma cuantitativa de expresar esto. Considera el valor esperado del espín a lo largo de la dirección $\hat{n}$. Dado que $|A\rangle$ es un vector propio de $\vec{\sigma}\cdot \vec{n}$ (con valor propio $+1$), se sigue que el valor esperado puede expresarse como

$$\langle \vec{\sigma}\cdot \vec{n}\rangle = 1.$$

Por otro lado, el valor esperado de las componentes perpendiculares de $\sigma$ es cero en el estado $|A\rangle$. Se sigue que los cuadrados de los valores esperados de las tres componentes de $\sigma$ suman 1. Además, esto es cierto para cualquier estado:

$$\langle \sigma_{x}\rangle^{2} + \langle \sigma_{y}\rangle^{2} + \langle \sigma_{z}\rangle^{2} = 1. \quad (3.30)$$

Recuerda este hecho. Volveremos a él en la Lección 6.

---
[Fin de la Parte 2/5. Continuará...]

[PARTE 3/5]

---

# Lección 4

## Tiempo y Cambio

Lenny: El tiempo es lo que evita que todo suceda a la vez.

Art: ¿Espacio? ¿Tiempo? ¿Espacio-tiempo? ¿Qué tiene eso que ver con la mecánica cuántica?

Lenny: Relatividad. Olvídalo. Eso es para más tarde.

Art: No puedo esperar.

Lenny: Vas a tener que hacerlo.

### 4.1 Evolución Temporal

Hasta ahora, nuestra discusión sobre la mecánica cuántica ha ignorado el movimiento, el cambio y la evolución temporal. Hemos tratado principalmente con situaciones estáticas: la preparación de un estado, la medición de un observable, y las probabilidades de varios resultados. Pero el mundo no es estático. Las cosas cambian con el tiempo: los péndulos oscilan, los planetas orbitan, los electrones saltan de un nivel de energía a otro. Necesitamos una ley que describa cómo evolucionan los estados cuánticos.

  9 

94 LECCIÓN 4. TIEMPO Y CAMBIO

En mecánica clásica, la evolución temporal está gobernada por las ecuaciones de Hamilton o, equivalentemente, por el principio de mínima acción. En mecánica cuántica, la evolución temporal está gobernada por la ecuación de Schrödinger. Al igual que las ecuaciones de Hamilton, la ecuación de Schrödinger es determinista. Dado el estado de un sistema en un instante de tiempo, la ecuación nos dice cuál será el estado en cualquier otro instante. Sin embargo, a diferencia de la mecánica clásica, el resultado de una medición individual no es determinista. Pero el estado en sí mismo —el vector ket— evoluciona de manera completamente determinista.

En esta lección, formularemos el quinto principio de la mecánica cuántica, que describe la evolución temporal de los vectores de estado. También introduciremos un nuevo concepto matemático: el Hamiltoniano, que es el operador que genera la evolución temporal.

### 4.2 El Operador Hamiltoniano

En mecánica clásica, la función que gobierna la evolución temporal es el Hamiltoniano, que normalmente es la energía del sistema expresada en términos de coordenadas y momentos. En mecánica cuántica, el Hamiltoniano es un operador, y juega un papel análogo. Lo denotaremos con la letra $\mathbf{H}$.

El Hamiltoniano es el generador de las traslaciones temporales. Así como el momento es el generador de las traslaciones espaciales, la energía (el Hamiltoniano) es el generador de las traslaciones en el tiempo. Esta es una idea profunda que conecta la mecánica cuántica con la mecánica clásica y con las simetrías del espacio-tiempo.

  9 

4.2. EL OPERADOR HAMILTONIANO 95

El Hamiltoniano es un operador hermítico porque corresponde a un observable: la energía. Por lo tanto, sus valores propios son reales y corresponden a los posibles resultados de una medición de energía. Sus vectores propios son los estados de energía definida, a menudo llamados estados estacionarios.

Pero, ¿cómo actúa exactamente $\mathbf{H}$ sobre un estado para cambiar su evolución temporal? La respuesta es la ecuación de Schrödinger.

#### 4.2.1 La Ecuación de Schrödinger

La ecuación de Schrödinger dependiente del tiempo es

$$i\hbar \frac{d}{dt} |\Psi(t)\rangle = \mathbf{H} |\Psi(t)\rangle. \quad (4.1)$$

Aquí, $\hbar$ (h barra) es la constante de Planck dividida por $2\pi$. Es una constante física fundamental con unidades de acción (energía × tiempo). Su valor numérico es aproximadamente $1.054 \times 10^{-34}$ J·s, pero para nuestros propósitos, su valor exacto no es tan importante como su presencia en la ecuación.

Observa que la Ec. 4.1 es una ecuación diferencial de primer orden en el tiempo. Esto significa que si conocemos el estado en el tiempo $t=0$, digamos $|\Psi(0)\rangle$, podemos (en principio) determinar el estado en cualquier tiempo futuro $t$. La evolución es determinista y, lo que es crucial, es unitaria.

  9 

96 LECCIÓN 4. TIEMPO Y CAMBIO

#### 4.2.2 Evolución Unitaria

¿Qué significa que la evolución sea unitaria? Significa que la norma del vector de estado se conserva. Si $|\Psi(t)\rangle$ está normalizado en $t=0$, lo estará para todo $t$. Esto es esencial para la interpretación probabilística: las probabilidades deben sumar 1 en todo momento.

Podemos escribir la solución formal a la ecuación de Schrödinger. Si $\mathbf{H}$ es independiente del tiempo, entonces

$$|\Psi(t)\rangle = e^{-i\mathbf{H}t/\hbar} |\Psi(0)\rangle. \quad (4.2)$$

El operador $\mathbf{U}(t) = e^{-i\mathbf{H}t/\hbar}$ se llama operador de evolución temporal. Es un operador unitario, lo que significa que $\mathbf{U}^{\dagger}\mathbf{U} = \mathbf{I}$. La unitariedad garantiza la conservación de la probabilidad.

### 4.3 Estados Estacionarios

Supongamos que preparas un sistema en un estado propio del Hamiltoniano. Es decir, sea $|E\rangle$ tal que

$$\mathbf{H}|E\rangle = E|E\rangle,$$

donde $E$ es un número real (el valor propio de la energía). ¿Cómo evoluciona este estado? Aplicamos la Ec. 4.2:

$$|\Psi(t)\rangle = e^{-i\mathbf{H}t/\hbar} |E\rangle = e^{-iEt/\hbar} |E\rangle.$$

  9 

4.4. EL QUINTO PRINCIPIO 97

El estado $|\Psi(t)\rangle$ es simplemente el estado original $|E\rangle$ multiplicado por un factor de fase $e^{-iEt/\hbar}$. Pero, como hemos discutido, un factor de fase global no tiene consecuencias físicas medibles. Por lo tanto, el estado es físicamente el mismo en todo momento. Por esta razón, los autoestados de energía se llaman estados estacionarios.

Esto no significa que nada esté sucediendo. Si el estado es una superposición de diferentes autoestados de energía, la evolución temporal se manifiesta a través de la interferencia entre las fases relativas de estos componentes.

### 4.4 El Quinto Principio

Ahora podemos enunciar formalmente el quinto principio de la mecánica cuántica:

- **Principio 5 (Evolución Temporal):** La evolución temporal de un sistema cuántico está gobernada por la ecuación de Schrödinger,

$$i\hbar \frac{d}{dt} |\Psi(t)\rangle = \mathbf{H} |\Psi(t)\rangle,$$

donde $\mathbf{H}$ es el operador Hamiltoniano, que es el operador hermítico correspondiente a la energía total del sistema.

Este principio completa el conjunto de principios fundamentales que necesitamos para hacer mecánica cuántica no relativista.

  9 

98 LECCIÓN 4. TIEMPO Y CAMBIO

### 4.5 Ejemplo: El Espín en un Campo Magnético

Apliquemos estos conceptos a nuestro sistema favorito: un solo espín. ¿Cómo evoluciona un espín con el tiempo? Para que evolucione, debe interactuar con algo. El ejemplo más simple es un espín en un campo magnético externo.

Clásicamente, un momento magnético en un campo magnético experimenta un torque que tiende a alinearlo con el campo. Cuánticamente, el comportamiento es diferente, pero podemos modelarlo fácilmente.

El momento magnético de un espín es proporcional a su operador de espín. Para un electrón, la relación es

$$\vec{\mu} = \gamma \vec{\sigma},$$

donde $\gamma$ es la razón giromagnética. La energía de un momento magnético en un campo magnético $\vec{B}$ es

$$E = -\vec{\mu} \cdot \vec{B} = -\gamma \vec{\sigma} \cdot \vec{B}.$$

Por lo tanto, el Hamiltoniano para un espín en un campo magnético es

$$\mathbf{H} = -\gamma \vec{B} \cdot \vec{\sigma}.$$

Es común escribir esto como

$$\mathbf{H} = -\vec{B} \cdot \vec{\sigma},$$

  9 

4.5. EJEMPLO: EL ESPÍN EN UN CAMPO MAGNÉTICO 99

absorbiendo la constante $\gamma$ en la definición de $\vec{B}$ (o estableciendo unidades donde $\gamma = 1$ y $\hbar = 1$). Nosotros, para simplificar, a menudo pondremos $\hbar = 1$ también.

Consideremos el caso más simple: un campo magnético constante y uniforme a lo largo del eje $z$. Entonces $\vec{B} = B \hat{z}$, y

$$\mathbf{H} = -B \sigma_{z} = -B \left( \begin{array}{cc}1 & 0\\ 0 & -1 \end{array} \right).$$

Los autoestados de $\mathbf{H}$ son, por supuesto, $|u\rangle$ y $|d\rangle$, con energías

$$E_{u} = -B, \quad E_{d} = B.$$

Supongamos que preparamos el espín en el estado $|r\rangle$ en $t=0$:

$$|\Psi(0)\rangle = |r\rangle = \frac{1}{\sqrt{2}} (|u\rangle + |d\rangle).$$

Ahora aplicamos la evolución temporal. Usando la Ec. 4.2 (con $\hbar = 1$):

$$|\Psi(t)\rangle = e^{-i\mathbf{H}t} |r\rangle = \frac{1}{\sqrt{2}} \left( e^{-i\mathbf{H}t}|u\rangle + e^{-i\mathbf{H}t}|d\rangle \right).$$

Como $|u\rangle$ y $|d\rangle$ son autoestados de $\mathbf{H}$,

$$e^{-i\mathbf{H}t}|u\rangle = e^{-iE_{u}t}|u\rangle = e^{iBt}|u\rangle,$$
$$e^{-i\mathbf{H}t}|d\rangle = e^{-iE_{d}t}|d\rangle = e^{-iBt}|d\rangle.$$

  10 

100 LECCIÓN 4. TIEMPO Y CAMBIO

Por lo tanto,

$$|\Psi(t)\rangle = \frac{1}{\sqrt{2}} \left( e^{iBt} |u\rangle + e^{-iBt} |d\rangle \right).$$

Podemos factorizar una fase global $e^{iBt}$:

$$|\Psi(t)\rangle = \frac{e^{iBt}}{\sqrt{2}} \left( |u\rangle + e^{-2iBt} |d\rangle \right).$$

Ignorando la fase global (que no tiene efectos físicos), el estado es

$$|\Psi(t)\rangle \propto |u\rangle + e^{-2iBt} |d\rangle.$$

Comparemos esto con el estado genérico para un espín preparado a lo largo de una dirección en el plano $x-y$. Recordemos que

$$|r\rangle = \frac{1}{\sqrt{2}} (|u\rangle + |d\rangle),$$
$$|l\rangle = \frac{1}{\sqrt{2}} (|u\rangle - |d\rangle),$$
$$|i\rangle = \frac{1}{\sqrt{2}} (|u\rangle + i|d\rangle),$$
$$|o\rangle = \frac{1}{\sqrt{2}} (|u\rangle - i|d\rangle).$$

Nuestro estado $|\Psi(t)\rangle$ tiene la forma $|u\rangle + e^{-i\phi}|d\rangle$ con $\phi = 2Bt$. Dependiendo del valor de $\phi$, este estado corresponde a una dirección diferente en el plano $x-y$:

- $\phi = 0$: $|r\rangle$ (eje $x$ positivo)
- $\phi = \pi$: $|l\rangle$ (eje $x$ negativo)
- $\phi = \pi/2$: $|o\rangle$? Cuidado: $|o\rangle = |u\rangle - i|d\rangle$ corresponde a $e^{-i\phi} = -i = e^{-i\pi/2}$, así que $\phi = \pi/2$ da $|o\rangle$ (eje $y$ negativo).
- $\phi = 3\pi/2$ (o $-\pi/2$): $|i\rangle$ (eje $y$ positivo).

  10 

4.6. CONMUTADORES Y EL PRINCIPIO DE INCERTIDUMBRE 101

A medida que pasa el tiempo, $\phi = 2Bt$ aumenta linealmente. El espín precesa en el plano $x-y$. La probabilidad de medir, digamos, $\sigma_x = +1$ oscila con el tiempo. Este fenómeno se llama **precesión de espín** o **precesión de Larmor**.

La frecuencia de precesión es $\omega = 2B$ (en unidades donde $\hbar = 1$). En unidades reales, es $\omega = 2\gamma B / \hbar$ o algo similar dependiendo de las constantes exactas.

Este es un ejemplo hermoso y simple de cómo la evolución temporal cuántica produce un comportamiento dinámico rico y predecible.

### 4.6 Conmutadores y el Principio de Incertidumbre

Antes de concluir esta lección, necesitamos introducir otra herramienta matemática crucial: el **conmutador**. El conmutador de dos operadores $\mathbf{A}$ y $\mathbf{B}$ se define como

$$[\mathbf{A}, \mathbf{B}] = \mathbf{A}\mathbf{B} - \mathbf{B}\mathbf{A}. \quad (4.3)$$

Si los operadores conmutan, es decir, $[\mathbf{A}, \mathbf{B}] = 0$, entonces $\mathbf{A}\mathbf{B} = \mathbf{B}\mathbf{A}$. Si no conmutan, el orden de aplicación importa.

El conmutador es fundamental en mecánica cuántica por varias razones. Una de las más importantes es que está en el corazón del principio de incertidumbre de Heisenberg.

  10 

102 LECCIÓN 4. TIEMPO Y CAMBIO

#### 4.6.1 Conmutadores de los Operadores de Espín

Calculemos los conmutadores de las matrices de Pauli. Por ejemplo,

$$[\sigma_x, \sigma_y] = \sigma_x \sigma_y - \sigma_y \sigma_x.$$

Sabemos que

$$\sigma_x \sigma_y = \left( \begin{array}{cc}0 & 1\\ 1 & 0 \end{array} \right) \left( \begin{array}{cc}0 & -i\\ i & 0 \end{array} \right) = \left( \begin{array}{cc}i & 0\\ 0 & -i \end{array} \right) = i\sigma_z,$$
$$\sigma_y \sigma_x = \left( \begin{array}{cc}0 & -i\\ i & 0 \end{array} \right) \left( \begin{array}{cc}0 & 1\\ 1 & 0 \end{array} \right) = \left( \begin{array}{cc}-i & 0\\ 0 & i \end{array} \right) = -i\sigma_z.$$

Por lo tanto,

$$[\sigma_x, \sigma_y] = i\sigma_z - (-i\sigma_z) = 2i\sigma_z.$$

De manera similar, se pueden obtener las relaciones cíclicas:

$$[\sigma_x, \sigma_y] = 2i\sigma_z,$$
$$[\sigma_y, \sigma_z] = 2i\sigma_x,$$
$$[\sigma_z, \sigma_x] = 2i\sigma_y. \quad (4.4)$$

Estas relaciones son análogas a las relaciones de conmutación del momento angular en mecánica cuántica. No es casualidad: el espín es un momento angular intrínseco.

  10 

4.6. CONMUTADORES Y EL PRINCIPIO DE INCERTIDUMBRE 103

#### 4.6.2 El Principio de Incertidumbre Generalizado

El principio de incertidumbre de Heisenberg para posición y momento es el ejemplo más famoso, pero existe una forma general. Para dos observables $\mathbf{A}$ y $\mathbf{B}$, el principio de incertidumbre establece que

$$\Delta A \, \Delta B \geq \frac{1}{2} |\langle [\mathbf{A}, \mathbf{B}] \rangle|, \quad (4.5)$$

donde $\Delta A$ es la desviación estándar de $\mathbf{A}$ en un estado dado, $\Delta B$ es la desviación estándar de $\mathbf{B}$, y $\langle [\mathbf{A}, \mathbf{B}] \rangle$ es el valor esperado del conmutador en ese estado.

Para el espín, apliquemos esto a $\sigma_x$ y $\sigma_y$. Sabemos que $[\sigma_x, \sigma_y] = 2i\sigma_z$. Por lo tanto,

$$\Delta \sigma_x \, \Delta \sigma_y \geq \frac{1}{2} |\langle 2i\sigma_z \rangle| = |\langle \sigma_z \rangle|.$$

Si el espín está en el estado $|u\rangle$ (arriba a lo largo de $z$), entonces $\langle \sigma_z \rangle = 1$, y la desigualdad se convierte en

$$\Delta \sigma_x \, \Delta \sigma_y \geq 1.$$

Pero en el estado $|u\rangle$, ¿cuáles son $\Delta \sigma_x$ y $\Delta \sigma_y$? Las probabilidades para $\sigma_x$ son $P(+1)=1/2$ y $P(-1)=1/2$, por lo que la desviación estándar es $\Delta \sigma_x = 1$. Lo mismo para $\sigma_y$. Por lo tanto, $\Delta \sigma_x \Delta \sigma_y = 1$, que satisface la desigualdad como igualdad. ¡El estado $|u\rangle$ es un estado de mínima incertidumbre para el par ($\sigma_x, \sigma_y$)!

  10 

104 LECCIÓN 4. TIEMPO Y CAMBIO

### 4.7 Resumen de la Lección 4

En esta lección, hemos dado un gran salto. Introdujimos la dinámica en la mecánica cuántica a través del quinto principio: la ecuación de Schrödinger. Vimos cómo el Hamiltoniano, el operador de energía, gobierna la evolución temporal. Aprendimos que la evolución es unitaria y que los autoestados de energía son estados estacionarios.

Aplicamos esto al problema simple pero profundo de un espín en un campo magnético constante, descubriendo la precesión de espín. Finalmente, introdujimos el conmutador y vimos cómo conduce a una versión generalizada del principio de incertidumbre, aplicándolo a los componentes del espín.

Con estos principios y herramientas, estamos armados para abordar sistemas más complejos.

---

# Lección 5

## Sistemas Compuestos y Entrelazamiento

Art: Espera, espera. ¿Me estás diciendo que si tengo dos espines, el espacio de estados no es solo la suma de los espacios de cada uno?

Lenny: No, no es una suma. Es un producto.

Art: ¿Producto? ¿Como multiplicar?

Lenny: Sí. Y de ahí viene toda la diversión.

Art: No me gusta cómo suena eso.

  10 

5.1. ESPACIOS DE HILBERT DE MÚLTIPLES PARTÍCULAS 105

### 5.1 Espacios de Hilbert de Múltiples Partículas

Hasta ahora, hemos tratado con sistemas cuánticos muy simples: un solo cúbit, un solo espín. Pero el mundo está lleno de muchas partículas. ¿Cómo describimos el estado cuántico de dos espines, o de una partícula moviéndose en el espacio, o de un átomo con muchos electrones?

La respuesta es un principio nuevo que a veces se explicita como un principio separado, y otras veces se deduce. Nosotros lo trataremos como un principio.

- **Principio 6 (Sistemas Compuestos):** El espacio de estados de un sistema compuesto es el producto tensorial de los espacios de estados de sus componentes.

El producto tensorial se denota con el símbolo $\otimes$. Si tenemos un sistema A con espacio de Hilbert $\mathcal{H}_A$ y un sistema B con espacio $\mathcal{H}_B$, entonces el espacio de Hilbert del sistema combinado A+B es

$$\mathcal{H}_{AB} = \mathcal{H}_A \otimes \mathcal{H}_B.$$

¿Qué significa esto en la práctica? Significa que si $\{|i\rangle_A\}$ es una base para $\mathcal{H}_A$ y $\{|j\rangle_B\}$ es una base para $\mathcal{H}_B$, entonces una base para $\mathcal{H}_{AB}$ está formada por todos los pares ordenados

$$|i\rangle_A \otimes |j\rangle_B,$$

que a menudo escribimos simplemente como $|i\rangle_A |j\rangle_B$ o $|i, j\rangle_{AB}$ o incluso $|ij\rangle$.

  10 

106 LECCIÓN 5. SISTEMAS COMPUESTOS Y ENTRELAZAMIENTO

La dimensionalidad se multiplica. Si $\mathcal{H}_A$ tiene dimensión $d_A$ y $\mathcal{H}_B$ tiene dimensión $d_B$, entonces $\mathcal{H}_{AB}$ tiene dimensión $d_A \times d_B$. Para dos espines (cada uno con espacio bidimensional), el espacio combinado tiene dimensión $2 \times 2 = 4$.

### 5.2 Estados Producto y Estados Entrelazados

No todos los estados en $\mathcal{H}_{AB}$ se pueden escribir como un producto de un estado de A y un estado de B. De hecho, la mayoría no pueden.

Un **estado producto** (o estado separable) es aquel que se puede escribir como

$$|\Psi\rangle_{AB} = |\phi\rangle_A \otimes |\chi\rangle_B.$$

En este tipo de estado, las mediciones en A y B son independientes. No hay correlaciones más allá de las clásicas.

Un **estado entrelazado** (o enredado, del inglés *entangled*) es aquel que **no** se puede escribir como un producto. En un estado entrelazado, los dos subsistemas están correlacionados de una manera puramente cuántica que no tiene análogo clásico.

El ejemplo más famoso de estado entrelazado para dos espines es uno de los **estados de Bell**:

$$|\Phi^+\rangle = \frac{1}{\sqrt{2}} (|u\rangle_A |u\rangle_B + |d\rangle_A |d\rangle_B). \quad (5.1)$$

  10 

5.2. ESTADOS PRODUCTO Y ESTADOS ENTRELAZADOS 107

Este estado no se puede factorizar. Intenta encontrar $|\phi\rangle_A = \alpha|u\rangle + \beta|d\rangle$ y $|\chi\rangle_B = \gamma|u\rangle + \delta|d\rangle$ tal que el producto dé la Ec. 5.1. Verás que es imposible porque el producto daría términos cruzados $|u\rangle|d\rangle$ y $|d\rangle|u\rangle$ que no están presentes en $|\Phi^+\rangle$, a menos que $\alpha\delta = 0$ y $\beta\gamma = 0$, lo que forzaría que todos los coeficientes fueran cero, lo cual es imposible para un estado normalizado.

#### 5.2.1 Propiedades Asombrosas del Entrelazamiento

Supongamos que preparamos dos espines en el estado $|\Phi^+\rangle$. Ahora los separamos: Alice se lleva el espín A a la Luna, y Bob se queda en la Tierra con el espín B.

Alice decide medir $\sigma_z$ en su espín. ¿Qué probabilidades tiene? Del estado $|\Phi^+\rangle$, la probabilidad de que Alice obtenga $+1$ es $|\langle u|_A \otimes I_B |\Phi^+\rangle|^2$. Calculemos:

$$\langle u|_A \otimes I_B |\Phi^+\rangle = \frac{1}{\sqrt{2}} ( \langle u|u\rangle_A |u\rangle_B + \langle u|d\rangle_A |d\rangle_B ) = \frac{1}{\sqrt{2}} |u\rangle_B.$$

La norma de este estado (no normalizado) es $\sqrt{\langle u|u\rangle_B / 2} = 1/\sqrt{2}$. Por lo tanto, la probabilidad es $|1/\sqrt{2}|^2 = 1/2$. Similarmente, la probabilidad de que Alice obtenga $-1$ es también $1/2$.

Pero hay algo más. Después de que Alice mide y obtiene, digamos, $+1$, el estado colapsa. El estado post-medición es el proyector sobre el resultado. Específicamente, el estado de los dos espines se convierte en

$$(|u\rangle\langle u|_A \otimes I_B) |\Phi^+\rangle$$

  10 

108 LECCIÓN 5. SISTEMAS COMPUESTOS Y ENTRELAZAMIENTO

normalizado. Eso es exactamente $|u\rangle_A |u\rangle_B$. De repente, el espín de Bob, que está en la Luna, está en el estado $|u\rangle_B$. Si Alice hubiera obtenido $-1$, el espín de Bob estaría en $|d\rangle_B.

El resultado de la medición de Alice es aleatorio, pero una vez que ella lo obtiene, el estado de Bob queda determinado instantáneamente, sin importar la distancia. Esto es lo que Einstein llamó "acción fantasmal a distancia" (*spooky action at a distance*).

Es crucial entender que esto no permite comunicación superlumínica. Bob no puede controlar qué resultado obtiene Alice, ni puede saber si Alice midió o no. Para Bob, su espín individual está en una mezcla estadística: 50% arriba, 50% abajo. Solo cuando Alice le llama por teléfono (a velocidad ≤ c) y le dice su resultado, Bob puede seleccionar los subsistemas que corresponden a ese resultado. El entrelazamiento no viola la relatividad especial.

### 5.3 Operadores para Sistemas Compuestos

¿Cómo actúan los operadores en un espacio de producto tensorial? Si tenemos un operador $\mathbf{A}$ que actúa solo sobre el sistema A, y un operador $\mathbf{B}$ que actúa solo sobre el sistema B, entonces el operador conjunto es $\mathbf{A} \otimes \mathbf{B}$. Su acción sobre un estado producto es

$$(\mathbf{A} \otimes \mathbf{B}) (|\phi\rangle_A \otimes |\chi\rangle_B) = (\mathbf{A}|\phi\rangle_A) \otimes (\mathbf{B}|\chi\rangle_B),$$

y se extiende por linealidad a estados no factorizables.

Si queremos medir $\sigma_z$ solo en el espín A, eso corresponde al operador $\sigma_z \otimes I$. Para medir $\sigma_x$ solo en el espín B, es $I \otimes \sigma_x$.

  10 

5.4. BASES PARA DOS ESPINES 109

### 5.4 Bases para Dos Espines

Una base ortonormal natural para el espacio de dos espines es la base producto:

$$|u\rangle|u\rangle, \quad |u\rangle|d\rangle, \quad |d\rangle|u\rangle, \quad |d\rangle|d\rangle.$$

A veces se escribe como $|uu\rangle, |ud\rangle, |du\rangle, |dd\rangle$.

Otra base muy útil es la **base de Bell**, que consiste en cuatro estados máximamente entrelazados:

$$|\Phi^+\rangle = \frac{1}{\sqrt{2}} (|uu\rangle + |dd\rangle),$$
$$|\Phi^-\rangle = \frac{1}{\sqrt{2}} (|uu\rangle - |dd\rangle),$$
$$|\Psi^+\rangle = \frac{1}{\sqrt{2}} (|ud\rangle + |du\rangle),$$
$$|\Psi^-\rangle = \frac{1}{\sqrt{2}} (|ud\rangle - |du\rangle).$$

Estos estados son ortonormales y forman una base completa para el espacio de 4 dimensiones.

### 5.5 La Paradoja EPR y el Teorema de Bell

El entrelazamiento llevó a Einstein, Podolsky y Rosen (EPR) a argumentar que la mecánica cuántica era incompleta. Propusieron que debería haber "elementos de realidad" (variables ocultas) que determinaran los resultados de las mediciones, y que la mecánica cuántica era solo una descripción estadística de esos elementos subyacentes.

  11 

110 LECCIÓN 5. SISTEMAS COMPUESTOS Y ENTRELAZAMIENTO

Durante décadas, esto fue un debate filosófico. Pero en 1964, John Bell demostró que la hipótesis de las variables ocultas locales hace predicciones concretas que son incompatibles con las predicciones de la mecánica cuántica. Además, estas predicciones pueden ser probadas experimentalmente.

Los experimentos, comenzando con los de Alain Aspect en la década de 1980 y continuando hasta hoy, han confirmado repetidamente las predicciones de la mecánica cuántica y han refutado las desigualdades de Bell. Las variables ocultas locales no pueden existir. La naturaleza es inherentemente no local (o, más precisamente, las correlaciones cuánticas violan el realismo local).

Este es uno de los descubrimientos más profundos de la física del siglo XX. El entrelazamiento no es solo una rareza matemática; es una característica fundamental de cómo funciona el mundo.

### 5.6 Resumen de la Lección 5

Introdujimos el producto tensorial como la forma de construir espacios de Hilbert para sistemas compuestos. Vimos que esto lleva a la existencia de estados entrelazados, que no pueden factorizarse en estados individuales. El entrelazamiento produce correlaciones fuertes entre subsistemas separados que violan las desigualdades de Bell y desafían nuestra intuición clásica. El estudio de sistemas compuestos y entrelazamiento es fundamental para la información cuántica, la computación cuántica y la comprensión de la naturaleza.

---

[Fin de la Parte 3/5. Continuará...]

---

---

[PARTE 1/5 - Capítulo 6]

---

  17 

# Lección 6

## Combinando Sistemas: Entrelazamiento

Art: Después de todo, este lugar es bastante amigable. Excepto por Menos Uno, no veo muchos solitarios.

Lenny: Relacionarse es algo natural en un lugar como este. Y no solo porque está abarrotado. Solo cuida tu cartera y no te enredes demasiado.

### 6.1 Interludio Matemático: Productos Tensoriales

#### 6.1.1 Conoce a Alicia y a Beto

Descubrir cómo se combinan los sistemas para formar sistemas más grandes es una gran parte de lo que hacemos en física. No hace falta que te diga que un átomo es una colección de nucleones y electrones, cada uno de los cuales podría considerarse un sistema cuántico por derecho propio.

  17 

150 LECCIÓN 6. ENTRELAZAMIENTO

Cuando se habla de sistemas compuestos, es fácil atascarse en un lenguaje formal como "Sistema A" y "Sistema B". La mayoría de los físicos prefieren en su lugar un lenguaje informal más ligero, y Alicia y Beto se han convertido en sustitutos casi universales de A y B. Podemos pensar en Alicia y Beto como proveedores de sistemas compuestos y montajes de laboratorio de todo tipo. Su inventario y experiencia están limitados solo por nuestra imaginación, y abordan con gusto asignaciones difíciles o peligrosas como saltar a agujeros negros. ¡Son auténticos superhéroes geeks!

Digamos que Alicia y Beto han proporcionado dos sistemas: el sistema de Alicia y el sistema de Beto. El sistema de Alicia —sea lo que sea— se describe mediante un espacio de estados llamado $S_{A}$, y de manera similar, el sistema de Beto se describe mediante un espacio de estados llamado $S_{B}$.

Ahora digamos que queremos combinar los dos sistemas en un único sistema compuesto. Antes de seguir adelante, seamos más específicos sobre los sistemas con los que empezamos. Por ejemplo, el sistema de Alicia podría ser una moneda mecánico-cuántica con dos estados base $C$ y $X$. Por supuesto, una moneda clásica debe estar en un estado u otro, pero una moneda cuántica puede existir en una superposición:

$$\alpha_{C}|C\rangle + \alpha_{X}|X\rangle.$$

Notarás que he usado una notación inusual para los vectores ket de Alicia. Esto es para distinguirlos de los kets de Beto. La nueva notación pretende disuadirnos de sumar vectores en el espacio de Alicia $S_{A}$ con vectores en el espacio de Beto $S_{B}$. El $S_{A}$ de Alicia es un espacio vectorial bidimensional, definido por los dos vectores base $|C\rangle$ y $|X\rangle$.

  17 

6.1. INTERLUDIO: PRODUCTOS TENSORIALES

El sistema de Beto también podría ser una moneda, pero también podría ser otra cosa. Supongamos que es un dado cuántico. El espacio de estados de Beto $S_{B}$ sería entonces de seis dimensiones, con la base

$$|1\rangle, |2\rangle, |3\rangle, |4\rangle, |5\rangle, |6\rangle$$

denotando las seis caras del dado. Al igual que la moneda de Alicia, el dado de Beto es mecánico-cuántico, y los seis estados pueden superponerse de manera similar.

#### 6.1.2 Representando el Sistema Combinado

Ahora imagina que los sistemas de Beto y Alicia existen ambos y forman un único sistema compuesto. La primera pregunta es: ¿Cómo podríamos construir el espacio de estados —llamémoslo $S_{AB}$— para el sistema combinado? La respuesta es formar el producto tensorial de $S_{A}$ y $S_{B}$. La notación para esta operación es

$$S_{AB} = S_{A} \otimes S_{B}.$$

Para definir $S_{AB}$, es suficiente especificar sus vectores base. Los vectores base son exactamente lo que cabría esperar. La parte superior

  17 

152 LECCIÓN 6. ENTRELAZAMIENTO

 Figura 6.1: Los estados base del sistema compuesto $S_{AB}$, mostrados como una tabla. En la parte superior están las etiquetas de estado para el dado de Beto. Las etiquetas de estado para la moneda de Alicia se muestran a la izquierda. Las etiquetas de estado para el sistema combinado son las entradas de la tabla. Cada etiqueta de estado combinada muestra el estado de cada uno de los dos subsistemas. Por ejemplo, la etiqueta de estado $C4$ denota un estado en el que la moneda de Alicia muestra $C$ y el dado de Beto muestra 4.  

  17 

6.1. INTERLUDIO: PRODUCTOS TENSORIALES

de la Fig. 6.1 muestra una tabla cuyas columnas corresponden a los seis vectores base de Beto y cuyas filas corresponden a los dos vectores base de Alicia. Cada casilla de la tabla denota un vector base para el sistema $S_{AB}$. Por ejemplo, la casilla etiquetada $C4$ representa un estado en $S_{AB}$ en el que la moneda muestra Cara y el dado muestra el número 4. En el sistema combinado, hay doce vectores base en total.

Hay varias formas de representar estos estados simbólicamente. Podríamos representar el estado $C4$ usando notación explícita, como $|C\rangle \otimes |4\rangle$ o $|C\rangle |4\rangle$. Normalmente, es más conveniente usar la notación compuesta $|C4\rangle$. Esto enfatiza que estamos hablando de un solo estado con una etiqueta de dos partes. La mitad izquierda etiqueta el subsistema de Alicia, y la mitad derecha etiqueta el de Beto. Las notaciones explícita y compuesta tienen el mismo significado: se refieren al mismo estado.

Una vez que se enumeran los vectores base —en este caso, doce de ellos— podemos combinarlos linealmente para formar superposiciones arbitrarias. Por lo tanto, el espacio producto tensorial en este caso es de doce dimensiones. Una superposición de dos de estos vectores base podría verse como

$$\alpha_{c3}|C3\rangle + \alpha_{x4}|X4\rangle.$$

En cada caso, la primera mitad de la etiqueta de estado describe el estado de la moneda de Alicia, y la segunda mitad describe el estado del dado de Beto.

A veces, necesitaremos referirnos a un vector base arbitrario en $S_{AB}$. Para hacer eso, usaremos vectores ket que se ven así,

$$|ab\rangle,$$

  17 

154 LECCIÓN 6. ENTRELAZAMIENTO

o así,

$$|a'b'\rangle.$$

En esta notación, la $a$ o $a'$ (o cualquier carácter izquierdo de la etiqueta) representa uno de los estados de Alicia, y la $b$ o $b'$ representa uno de los estados de Beto.

Hay un aspecto de esta notación que es engañoso. Aunque nuestras etiquetas de estado de $S_{AB}$ tienen doble índice, los vectores ket como $|ab\rangle$ o $|C3\rangle$ representan un solo estado del sistema combinado. En otras palabras, estamos usando un doble índice para etiquetar un solo estado. Esto requerirá algo de práctica. La parte de Alicia de la etiqueta de estado está siempre a la izquierda y la parte de Beto siempre a la derecha —mantener a Alicia y Beto en orden alfabético hace que esta convención sea fácil de recordar.

Las reglas son las mismas para sistemas más generales. La única diferencia es que los dos estados de A y los seis estados de B serían reemplazados por $N_{A}$ y $N_{B}$ estados respectivamente, y el producto tensorial tendría dimensión

$$N_{AB} = N_{A}N_{B}.$$

Los sistemas con tres o más componentes pueden representarse mediante productos tensoriales de tres o más espacios de estados, pero no haremos eso aquí.

Ahora que hemos descrito los espacios separados de Alicia y Beto, $S_{A}$ y $S_{B}$, así como el espacio combinado $S_{AB}$, todavía nos queda un poco más de notación por establecer. Alicia tiene un conjunto de operadores, etiquetados como $\sigma$, que actúan sobre su sistema. Beto tiene un conjunto similar

  17 

6.2. CORRELACIÓN CLÁSICA 155

para su sistema, que podemos etiquetar como $\tau$, para no confundirlos con los de Alicia. Alicia puede tener varios operadores $\sigma$, y del mismo modo Beto puede tener varios operadores $\tau$. Con este marco en mano, estamos listos para explorar los sistemas compuestos con mayor profundidad. Más adelante, en la Lección 7, explicaremos cómo trabajar con operadores de producto tensorial en forma de componentes —expresados como matrices y vectores columna.

A estas alturas, no debería haber duda en tu mente de que la física cuántica es diferente de la física clásica, hasta en sus raíces lógicas. En esta lección y en la siguiente, voy a impactarte aún más con esta idea. Vamos a discutir un aspecto de la física cuántica que es tan diferente de la física clásica que, al día de hoy, ha desconcertado —y exasperado— a físicos y filósofos durante casi 80 años. Impulsó a su descubridor, Einstein, a la conclusión de que algo muy profundo falta en la mecánica cuántica, y los físicos han estado discutiendo sobre ello desde entonces. Como Einstein se dio cuenta, al aceptar la mecánica cuántica estamos comprando una visión de la realidad que es radicalmente diferente de la visión clásica.

### 6.2 Correlación Clásica

Antes de llegar al entrelazamiento cuántico, dediquemos unos minutos a lo que podríamos llamar entrelazamiento clásico. En el siguiente experimento, Alicia (A) y Beto (B) recibirán ayuda de Carlos (C).

Carlos tiene dos monedas en sus manos —una de diez centavos y una de veinticinco centavos (un *dime* y un *quarter*). Las mezcla y las sostiene, una en cada mano, para

  17 

156 LECCIÓN 6. ENTRELAZAMIENTO

Alicia y Beto, y les da una moneda a cada uno. Nadie mira las monedas y nadie sabe quién tiene cuál. Entonces, Alicia aborda el transbordador hacia Alfa Centauri mientras Beto se queda en Palo Alto. Carlos ha hecho su trabajo y ya no importa (lo siento, Carlos).

Antes del gran viaje de Alicia, Alicia y Beto sincronizan sus relojes —han hecho su tarea de relatividad y han tenido en cuenta la dilatación del tiempo y todo eso. Acuerdan que Alicia mirará su moneda solo un segundo o dos antes de que Beto mire la suya.

Todo procede sin problemas, y cuando Alicia llega a Alfa Centauri, efectivamente mira su moneda. Sorprendentemente, en el instante en que la mira, inmediatamente sabe exactamente qué moneda verá Beto, incluso antes de que él mire. ¿Es esto una locura? ¿Han logrado Alicia y Beto violar la regla más fundamental de la relatividad, que establece que la información no puede viajar más rápido que la velocidad de la luz?

Por supuesto que no. Lo que violaría la relatividad sería que la observación de Alicia le dijera instantáneamente a Beto qué esperar. Alicia puede saber qué moneda verá Beto, pero no tiene forma de decírselo —no sin enviarle un mensaje real desde Alfa Centauri, y eso tomaría al menos los cuatro años que la luz necesita para hacer el viaje.

Hagamos este experimento muchas veces, ya sea con muchas parejas Alicia-Beto o con la misma pareja a lo largo del tiempo. Para ser cuantitativos, Carlos (ha vuelto, habiendo aceptado nuestras disculpas) pinta un "$\sigma = +1$" en cada moneda de diez centavos y un "$\sigma = -1$" en cada moneda de veinticinco centavos. Si asumimos que Carlos es realmente aleatorio en la forma en que mezcla las monedas, surgirán los siguientes hechos:

  17 

6.2. CORRELACIÓN CLÁSICA 157

- En promedio, tanto A como B obtendrán tantas monedas de diez como de veinticinco. Llamando a los valores de las observaciones de A $\sigma_{A}$ y a las observaciones de B $\sigma_{B}$, podemos expresar este hecho matemáticamente como

$$\langle \sigma_{A}\rangle = 0$$ $$\langle \sigma_{B}\rangle = 0.$$

- Si A y B registran sus observaciones y luego se reúnen de nuevo en Palo Alto para compararlas, encontrarán una fuerte correlación. Para cada prueba, si A observó $\sigma_{A} = +1$, entonces B observó $\sigma_{B} = -1$, y viceversa. En otras palabras, el producto $\sigma_{A}\sigma_{B}$ siempre es igual a $-1$:

$$\langle \sigma_{A}\sigma_{B}\rangle = -1.$$

Observa que el promedio de los productos (de $\sigma_{A}$ y $\sigma_{B}$) no es igual al producto de los promedios —las Ecs. 6.1 nos dicen que $\langle \sigma_{A}\rangle \langle \sigma_{B}\rangle$ es cero. En símbolos,

$$\langle \sigma_{A}\rangle \langle \sigma_{B}\rangle \neq \langle \sigma_{A}\sigma_{B}\rangle,$$

o

$$\langle \sigma_{A}\sigma_{B}\rangle - \langle \sigma_{A}\rangle \langle \sigma_{B}\rangle \neq 0. \quad (6.2)$$

  17 

158 LECCIÓN 6. ENTRELAZAMIENTO

Esto indica que las observaciones de Alicia y Beto están correlacionadas. De hecho, la cantidad

$$\langle \sigma_A\sigma_B\rangle - \langle \sigma_A\rangle \langle \sigma_B\rangle$$

se llama la correlación estadística entre las observaciones de Beto y Alicia. Se llama correlación estadística incluso si es cero. Cuando la correlación estadística es distinta de cero, decimos que las observaciones están correlacionadas. La fuente de esta correlación es el hecho de que originalmente Alicia y Beto estaban en la misma ubicación y Carlos tenía una moneda de cada tipo. La correlación permaneció cuando Alicia se fue a Alfa Centauri simplemente porque las monedas no cambiaron durante el viaje. No hay absolutamente nada extraño en esto ni en la Desigualdad 6.2. Es una propiedad muy común de las distribuciones estadísticas.

Supongamos que tienes una distribución de probabilidad $P(a,b)$ para dos variables $a$ y $b$. Si las variables están completamente no correlacionadas, entonces la probabilidad se factorizará:

$$P(a,b) = P_A(a)P_B(b), \quad (6.3)$$

donde $P_A(a)$ y $P_B(b)$ son las probabilidades individuales para $a$ y $b$. (Agregué subíndices a los símbolos de función como recordatorio de que podrían ser funciones diferentes de sus argumentos). Es fácil ver que si la probabilidad se factoriza de esta manera, entonces no hay correlación; en otras palabras, el promedio del producto es el producto de los promedios.

**Ejercicio 6.1:** Demuestra que si $P(a,b)$ se factoriza, entonces la correlación entre $a$ y $b$ es cero.

  18 

6.2. CORRELACIÓN CLÁSICA 159

Permíteme usar un ejemplo para ilustrar el tipo de situación que conduce a probabilidades factorizadas. Supongamos que en lugar de un solo Carlos, hay dos Carloses: Carlos-A y Carlos-B, que nunca se han comunicado. Carlos-B mezcla sus dos monedas y le da una a Beto; la otra se desecha.

Carlos-A hace exactamente lo mismo, excepto que le da una moneda a Alicia en lugar de a Beto. Este es el tipo de situación que conduce a probabilidades de producto factorizadas sin correlación.

En física clásica usamos estadística y teoría de probabilidad cuando ignoramos algo que es, en principio, conocible. Por ejemplo, después de mezclar las monedas en el primer experimento, Carlos podría haber hecho una observación suave (una mirada rápida) y luego dejar que Alicia y Beto tuvieran sus monedas. Esto no habría hecho ninguna diferencia en el resultado. En mecánica clásica, la distribución de probabilidad $P(a,b)$ representa una especificación incompleta del estado del sistema. Hay más por conocer —más que podría conocerse— sobre el sistema. En física clásica, el uso de la probabilidad siempre está asociado con una incompletitud del conocimiento en relación con todo lo que podría conocerse.

Un punto relacionado es que el conocimiento completo de un sistema en física clásica implica el conocimiento completo de cada parte del sistema. No tendría sentido decir que Carlos sabía todo lo que se podía saber sobre el sistema de dos monedas pero le faltaba información sobre las monedas individuales.

Estos conceptos clásicos están profundamente arraigados en nuestro pensamiento. Son la base de nuestra comprensión instintiva del mundo físico, y es muy difícil superarlos.

  18 

160 LECCIÓN 6. ENTRELAZAMIENTO

Pero superarlos debemos, si queremos entender el mundo cuántico.

### 6.3 Combinando Sistemas Cuánticos

Las dos monedas de Carlos formaban un único sistema clásico, compuesto por dos subsistemas clásicos. La mecánica cuántica también nos permite combinar sistemas, como descubrimos en el Interludio Matemático sobre productos tensoriales (Sección 6.1).

Alicia y Beto han aceptado amablemente proporcionar una variante del sistema moneda/dado que nos prestaron para el Interludio sobre productos tensoriales. En lugar de una moneda y un dado, el nuevo sistema se construye a partir de dos espines, lo que significa que tendremos la oportunidad de poner en práctica nuestro conocimiento de los espines individuales.

Como antes, a veces usaremos la notación poco ortodoxa $|a\rangle$ para recordarnos que los vectores de estado de Alicia no están en el mismo espacio de estados que los de Beto, y que no se nos permite sumarlos. Por otro lado, recuerda que cada miembro de una base ortonormal para $S_{AB}$ está etiquetado por un par de vectores, uno de $S_{A}$ y uno de $S_{B}$. Haremos un uso frecuente de la notación $|ab\rangle$ para etiquetar un solo vector base del sistema combinado. Estos vectores base de doble índice se pueden sumar, y haremos eso mucho.

Como explicamos en el Interludio, etiquetar un vector base con un par de índices requiere algo de práctica. Debes pensar en el par $ab$ como un solo índice que etiqueta un solo estado.

Veamos un ejemplo. Considera algún operador lineal $\mathbf{M}$ que actúa sobre el espacio de estados del sistema compuesto. Como es habitual, puede representarse como una matriz. Los elementos de matriz se construyen colocando el operador entre

  18 

6.4. DOS ESPINES

vectores base. Por lo tanto, los elementos de matriz de $\mathbf{M}$ se expresan como

$$\langle a'b'|\mathbf{M}|ab\rangle = M_{a'b',ab}.$$

Cada fila de la matriz está etiquetada con un solo índice $(a'b')$ del sistema compuesto y cada columna con $(ab)$.

Los vectores $|ab\rangle$ se toman como ortonormales, lo que significa que sus productos internos son cero a menos que ambas etiquetas coincidan. Esto no significa que $a$ coincida con $b$, sino que $ab$ coincide con $a'b'$. También podemos expresar esta idea usando el símbolo delta de Kronecker:

$$\langle ab|a'b'\rangle = \delta_{aa'}\delta_{bb'}.$$

El lado derecho es cero a menos que $a = a'$ y $b = b'$. Si las etiquetas coinciden, el producto interno es uno.

Ahora que tenemos los vectores base, se permite cualquier superposición lineal de ellos. Por lo tanto, cualquier estado en el sistema compuesto puede expandirse como

$$|\Psi \rangle = \sum_{a,b}\psi(a,b)|ab\rangle.$$

### 6.4 Dos Espines

Volviendo a nuestro ejemplo, imaginemos dos espines: el de Alicia y el de Beto. Para ponerlo en un contexto que podamos visualizar, imagina que los espines están unidos a dos partículas y que las dos partículas están fijas en el espacio en dos ubicaciones diferentes pero cercanas.

  18 

162 LECCIÓN 6. ENTRELAZAMIENTO

Alicia y Beto tienen cada uno sus propios aparatos, llamados $\mathcal{A}$ y $\mathcal{B}$ respectivamente, que pueden usar para preparar estados y medir componentes de espín. Cada uno puede orientarse independientemente a lo largo de cualquier eje.

Vamos a necesitar nombres para los dos espines. Cuando solo teníamos un espín, simplemente lo llamábamos $\sigma$, y tenía tres componentes a lo largo de los ejes $x, y$ y $z$. Ahora tenemos dos espines, y la pregunta es cómo etiquetarlos sin saturar los símbolos con demasiados subíndices y superíndices. Podríamos llamarlos $\sigma^{A}$ y $\sigma^{B}$, y a las componentes, $\sigma_{x}^{A}, \sigma_{y}^{B}$, y así sucesivamente. Para mí, eso es demasiados subíndices para seguirles la pista, especialmente en la pizarra. En cambio, seguiré la misma convención que usamos en el Interludio sobre productos tensoriales. Llamaré al espín de Alicia $\sigma$ y asignaré la siguiente letra del alfabeto griego, $\tau$, al espín de Beto. Los conjuntos completos de componentes para los espines de Alicia y Beto son

$$\sigma_{x},\sigma_{y},\sigma_{z}$$

y

$$\tau_{x},\tau_{y},\tau_{z}.$$

De acuerdo con los principios que establecimos anteriormente, el espacio de estados para el sistema de dos espines es un producto tensorial. Podemos hacer una tabla de los cuatro estados, tal como lo hicimos en el Interludio. Esta vez, es un cuadrado de $2 \times 2$, que comprende cuatro estados base.

Trabajemos en una base en la que se especifiquen las componentes $z$ de ambos espines. Los vectores base son

  18 

6.5. ESTADOS PRODUCTO 163

$$|uu\rangle, |ud\rangle, |du\rangle, |dd\rangle,$$

donde la primera parte de cada etiqueta representa el estado de $\sigma$ y la segunda parte representa $\tau$. Por ejemplo, el primer vector base $|uu\rangle$ representa el estado en el que ambos espines están arriba. El vector $|du\rangle$ es el estado en el que el espín de Alicia está abajo y el espín de Beto está arriba.

### 6.5 Estados Producto

El tipo más simple de estado para el sistema compuesto se llama estado producto. Un estado producto es el resultado de preparaciones completamente independientes por parte de Alicia y Beto, en las que cada uno usa su propio aparato para preparar un espín. Usando notación explícita, supongamos que Alicia prepara su espín en el estado

$$\alpha_{u}|u\rangle + \alpha_{d}|d\rangle$$

y Beto prepara el suyo en el estado

$$\beta_{u}|u\rangle + \beta_{d}|d\rangle.$$

Asumimos que cada estado está normalizado:

$$\begin{array}{rcl}\alpha_u^*\alpha_u + \alpha_d^*\alpha_d & = & 1\\ \beta_u^*\beta_u + \beta_d^*\beta_d & = & 1. \end{array} \quad (6.4)$$

  18 

164 LECCIÓN 6. ENTRELAZAMIENTO

Y de hecho, estas ecuaciones de normalización separadas para cada subsistema juegan un papel crucial en la definición de los estados producto. Si no se cumplieran, no tendríamos un estado producto. El estado producto que describe el sistema combinado es

$$|\text{estado producto}\rangle = \left\{\alpha_u|u\rangle + \alpha_d|d\rangle \right\} \otimes \left\{\beta_u|u\rangle + \beta_d|d\rangle \right\},$$

donde el primer factor representa el estado de Alicia y el segundo factor representa el de Beto. Expandiendo el producto y cambiando a la notación compuesta, el lado derecho se convierte en

$$\alpha_u\beta_u|uu\rangle + \alpha_u\beta_d|ud\rangle + \alpha_d\beta_u|du\rangle + \alpha_d\beta_d|dd\rangle. \quad (6.5)$$

La característica principal de un estado producto es que cada subsistema se comporta independientemente del otro. Si Beto hace un experimento sobre su propio subsistema, el resultado es exactamente el mismo que sería si el subsistema de Alicia no existiera. Lo mismo es cierto para Alicia, por supuesto.

**Ejercicio 6.2:** Muestra que si se satisfacen las dos condiciones de normalización de las Ecs. 6.4, entonces el vector de estado de la Ec. 6.5 está automáticamente normalizado también. En otras palabras, muestra que para este estado producto, normalizar el vector de estado general no impone restricciones adicionales sobre las $\alpha$ y las $\beta$.

Mencionaré aquí que los productos tensoriales y los estados producto son dos cosas diferentes, a pesar de sus nombres de sonido similar.$^2$

  18 

6.6. PARÁMETROS DEL ESTADO PRODUCTO 165

Un producto tensorial es un espacio vectorial para estudiar sistemas compuestos. Un estado producto es un vector de estado. Es uno de los muchos vectores de estado que habitan un espacio producto. Como veremos, la mayoría de los vectores de estado en el espacio producto no son estados producto.

### 6.6 Contando Parámetros para el Estado Producto

Consideremos el número de parámetros que se necesitan para especificar tal estado producto. Cada factor requiere dos números complejos ( $\alpha_{u}$ y $\alpha_{d}$ para Alicia, $\beta_{u}$ y $\beta_{d}$ para Beto), lo que significa que necesitamos cuatro números complejos en total. Eso es equivalente a ocho parámetros reales. Pero recuerda que las condiciones de normalización en las Ecs. 6.4 reducen esto en dos. Además, las fases globales de cada estado no tienen significado físico, por lo que el número total de parámetros reales es cuatro. Eso no es sorprendente: se necesitaban dos parámetros para describir el estado de un solo espín, por lo que dos espines independientes requieren cuatro.

### 6.7 Estados Entrelazados

Los principios de la mecánica cuántica nos permiten superponer vectores base de maneras más generales que solo estados producto. El vector más general en el espacio compuesto de estados es

$$\psi_{uu}|uu\rangle + \psi_{ud}|ud\rangle + \psi_{du}|du\rangle + \psi_{dd}|dd\rangle,$$

donde hemos usado los símbolos con subíndice $\psi$ (en lugar de

  18 

166 LECCIÓN 6. ENTRELAZAMIENTO

$\alpha$ y $\beta$) para representar los coeficientes complejos. De nuevo, tenemos cuatro números complejos, pero esta vez solo tenemos una condición de normalización,

$$\psi_{uu}^*\psi_{uu} + \psi_{ud}^*\psi_{ud} + \psi_{du}^*\psi_{du} + \psi_{dd}^*\psi_{dd} = 1,$$

y solo una fase global que ignorar. El resultado es que el estado más general para un sistema de dos espines tiene seis parámetros reales. Evidentemente, el espacio de estados es más rico que solo aquellos estados producto que pueden ser preparados independientemente por Beto y Alicia. Algo nuevo está sucediendo. Lo nuevo se llama entrelazamiento.

El entrelazamiento no es una proposición de todo o nada. Algunos estados están más entrelazados que otros. Aquí hay un ejemplo de un estado máximamente entrelazado —un estado que está tan entrelazado como es posible. Se llama el estado singlete, y puede escribirse como

$$|sing\rangle = \frac{1}{\sqrt{2}}\big(|ud\rangle - |du\rangle \big).$$

El estado singlete no puede escribirse como un estado producto. Lo mismo es cierto para los estados triplete,

$$\frac{1}{\sqrt{2}}\big(|ud\rangle + |du\rangle \big)$$ $$\frac{1}{\sqrt{2}}\big(|uu\rangle + |dd\rangle \big)$$ $$\frac{1}{\sqrt{2}}\big(|uu\rangle - |dd\rangle \big),$$

  18 

6.8. OBSERVABLES DE ALICIA Y BETO 167

que también están máximamente entrelazados. La razón para llamarlos singlete y triplete se explicará más adelante.

**Ejercicio 6.3:** Demuestra que el estado $|sing\rangle$ no puede escribirse como un estado producto.

¿Qué tienen los estados máximamente entrelazados que es tan fascinante? Puedo resumir esto en dos declaraciones:

- Un estado entrelazado es una descripción completa del sistema combinado. No se puede saber más sobre él.
- En un estado máximamente entrelazado, no se sabe nada sobre los subsistemas individuales.

¿Cómo puede ser eso? ¿Cómo podríamos saber tanto como es posible saber sobre el sistema Alicia-Beto de dos espines, y sin embargo no saber nada sobre los espines individuales que son sus subcomponentes? Ese es el misterio del entrelazamiento, y espero que al final de esta lección entiendas las reglas del juego, incluso si la naturaleza más profunda del entrelazamiento sigue siendo una paradoja.

### 6.8 Observables de Alicia y Beto

Hasta ahora, hemos discutido el espacio de estados del sistema de dos espines Alicia-Beto, pero no sus observables. Algunos de estos observables son obvios, incluso si su representación matemática no lo es. En particular, utilizando sus aparatos $\mathcal{A}$ y $\mathcal{B}$, Alicia y Beto pueden medir las componentes de sus espines:

  18 

168 LECCIÓN 6. ENTRELAZAMIENTO

$$\sigma_{x},\sigma_{y},\sigma_{z}$$

y

$$\tau_{x},\tau_{y},\tau_{z}.$$

¿Cómo se representan estos observables como operadores hermíticos en el espacio compuesto de estados? La respuesta es simple. Los operadores de Beto actúan sobre los estados de espín de Beto exactamente como lo harían si Alicia nunca hubiera aparecido. Lo mismo ocurre con Alicia. Repasemos cómo actúan los operadores de espín sobre los estados de un solo espín. Primero, veamos el espín de Alicia:

$$\begin{array}{rcl}{\sigma_z|u\rangle} & = & {|u\rangle}\\ {} & {} & {}\\ {\sigma_z|d\rangle} & = & {-|d\rangle}\\ {} & {} & {}\\ {\sigma_x|u\rangle} & = & {|d\rangle}\\ {} & {} & {}\\ {\sigma_x|d\rangle} & = & {|u\rangle}\\ {} & {} & {}\\ {\sigma_y|u\rangle} & = & {i|d\rangle}\\ {} & {} & {}\\ {\sigma_y|d\rangle} & = & {-i|u\rangle}. \end{array} \quad (6.6)$$

Por supuesto, la configuración de Beto es idéntica a la de Alicia, por lo que podemos escribir un conjunto paralelo de ecuaciones que muestran cómo actúan las componentes de $\tau$ sobre los estados de Beto:

  19 

6.8. OBSERVABLES DE ALICIA Y BETO 169

$$\begin{array}{rcl}{\tau_z|u\rangle} & = & {|u\rangle}\\ {} & {} & {}\\ {\tau_z|d\rangle} & = & {-|d\rangle}\\ {} & {} & {}\\ {\tau_x|u\rangle} & = & {|d\rangle}\\ {} & {} & {}\\ {\tau_x|d\rangle} & = & {|u\rangle}\\ {} & {} & {}\\ {\tau_y|u\rangle} & = & {i|d\rangle}\\ {} & {} & {}\\ {\tau_y|d\rangle} & = & {-i|u\rangle.} \end{array} \quad (6.7)$$

Ahora consideremos cómo deberían definirse los operadores cuando actúan sobre los estados producto tensorial, $|uu\rangle$, $|ud\rangle$, $|du\rangle$ y $|dd\rangle$. La respuesta es que cuando $\sigma$ actúa, simplemente ignora la mitad de Beto de la etiqueta de estado. Hay muchas combinaciones posibles de operadores y estados, pero elegiré algunas al azar. Puedes completar las otras, o buscarlas en el apéndice. Empezando con los operadores de Alicia, encontramos que

$$\begin{array}{rcl}{\sigma_z|uu\rangle} & = & {|uu\rangle}\\ {} & {} & {}\\ {\sigma_z|du\rangle} & = & {-|du\rangle}\\ {} & {} & {}\\ {\sigma_x|ud\rangle} & = & {|dd\rangle}\\ {} & {} & {}\\ {\sigma_x|dd\rangle} & = & {|ud\rangle} \end{array} \quad (6.8)$$

  19 

170 LECCIÓN 6. ENTRELAZAMIENTO

$$\begin{array}{rcl}{\sigma_{y}|uu\rangle} & = & {i|du\rangle}\\ {} & {} & {}\\ {\sigma_{y}|du\rangle} & = & {-i|uu\rangle}\\ {} & {} & {}\\ {\tau_{z}|uu\rangle} & = & {|uu\rangle}\\ {} & {} & {}\\ {\tau_{z}|du\rangle} & = & {|du\rangle}\\ {} & {} & {}\\ {\tau_{x}|ud\rangle} & = & {|uu\rangle}\\ {} & {} & {}\\ {\tau_{x}|du\rangle} & = & {|dd\rangle}\\ {} & {} & {}\\ {\tau_{y}|uu\rangle} & = & {i|ud\rangle}\\ {} & {} & {}\\ {\tau_{y}|dd\rangle} & = & {-i|du\rangle}. \end{array} \quad (6.9)$$

De nuevo, la regla es que las componentes del espín de Alicia actúan solo sobre la mitad de Alicia del sistema compuesto. La mitad de Beto es un espectador pasivo que no participa. En términos de símbolos, cuando actúan $\sigma_{x}, \sigma_{y},$ o $\sigma_{z}$, la mitad de Beto del estado de espín no cambia. Y cuando actúan los operadores de espín $\tau$ de Beto, la mitad de Alicia es igualmente pasiva.

Estamos siendo un poco descuidados con nuestra notación. Los vectores de un espacio producto tensorial son nuevos vectores, construidos a partir de los vectores de dos espacios más pequeños. Técnicamente, lo mismo es cierto para los operadores. Si fuéramos pedantes, insistiríamos en escribir las versiones de producto tensorial de $\sigma_{z}$ y $\tau_{x}$ como $\sigma_{z} \otimes I$ y $I \otimes \tau_{x}$, respectivamente, donde $I$ es el operador identidad. De hecho, podemos resaltar dos propiedades importantes de los operadores de producto

  19 

6.8. OBSERVABLES DE ALICIA Y BETO 171

tensorial reescribiendo la ecuación

$$\sigma_{z}|du\rangle = -|du\rangle \quad (6.10)$$

como

$$\begin{array}{rcl}(\sigma_z \otimes I)(|d\rangle \otimes |u\rangle) & = & (\sigma_z|d\rangle \otimes I|u\rangle)\\ & = & (-|d\rangle \otimes |u\rangle). \end{array} \quad (6.11)$$

Esta notación es engorrosa, y normalmente nos limitaremos al lenguaje más simple de la Ec. 6.10. Sin embargo, el lenguaje de la Ec. 6.11 deja claras dos cosas:

1. Un operador compuesto $\sigma_z \otimes I$ está operando sobre un vector compuesto $|d\rangle \otimes |u\rangle$ para producir un nuevo vector compuesto $-|d\rangle \otimes |u\rangle$.

2. La mitad de Alicia (la mitad izquierda) del operador compuesto solo afecta a su mitad del vector compuesto. Asimismo, la mitad de Beto del operador solo afecta a su mitad del vector.

Tendremos más que decir sobre los operadores compuestos en la próxima sección. Además, en la Lección 7, el lenguaje de la Ec. 6.11 nos ayudará a ver cómo trabajar con productos tensoriales en forma de componentes.

  19 

172 LECCIÓN 6. ENTRELAZAMIENTO

**Ejercicio 6.4:** Usa las formas matriciales de $\sigma_{z}$, $\sigma_{x}$ y $\sigma_{y}$ y los vectores columna para $|u\rangle$ y $|d\rangle$ para verificar las Ecs. 6.6. Luego, usa las Ecs. 6.6 y 6.7 para escribir las ecuaciones que faltaron en las Ecs. 6.8 y 6.9. Usa el apéndice para verificar tus respuestas.

**Ejercicio 6.5:** Demuestra el siguiente teorema:

Cuando cualquiera de los operadores de espín de Alicia o de Beto actúa sobre un estado producto, el resultado sigue siendo un estado producto.

Muestra que en un estado producto, el valor esperado de cualquier componente de $\vec{\sigma}$ o $\vec{\tau}$ es exactamente el mismo que sería en los estados individuales de un solo espín.

Este último ejercicio prueba algo importante sobre los estados producto. En un estado producto, cada predicción sobre la mitad de Beto del sistema es exactamente la misma que habría sido en la teoría de espín único correspondiente. Lo mismo ocurre con Alicia.

Un ejemplo de esta propiedad de los estados producto involucra lo que llamé el Principio de Polarización del Espín en la Lección 3. Una forma útil de enunciar ese principio es:

Para cualquier estado de un solo espín, hay alguna dirección para la cual el espín es $+1$.

Como expliqué, esto significa que los valores esperados de las componentes satisfacen la ecuación

$$\langle \sigma_{x}\rangle^{2} + \langle \sigma_{y}\rangle^{2} + \langle \sigma_{z}\rangle^{2} = 1, \quad (6.12)$$

lo que nos dice que no todos los valores esperados pueden ser cero. Este hecho sigue siendo válido para todos los estados producto. Sin embargo,

  19 

6.8. OBSERVABLES DE ALICIA Y BETO 173

no se cumple para el estado entrelazado $|sing\rangle$. De hecho, para el estado $|sing\rangle$ el lado derecho de la Ec. 6.12 se convierte en cero, como mostraremos a continuación.

Recordemos que el estado entrelazado $|sing\rangle$ se define como

$$|sing\rangle = \frac{1}{\sqrt{2}} (|ud\rangle - |du\rangle).$$

Veamos los valores esperados de $\sigma$ en este estado. Tenemos toda la maquinaria que necesitamos para calcularlos. Primero, consideremos $\langle \sigma_z\rangle$:

$$\langle \sigma_z\rangle = \langle sing|\sigma_z|sing\rangle$$ $$= \langle sing|\sigma_z\frac{1}{\sqrt{2}} (|ud\rangle - |du\rangle).$$

Aquí es donde entran en juego las Ecs. 6.8 (junto con el Ejercicio 6.4, que completa este conjunto de ecuaciones!). Nos dicen cómo actúa $\sigma_z$ sobre cada vector base. El resultado es

$$\langle sing|\sigma_z|sing\rangle = \langle sing|\frac{1}{\sqrt{2}} (|ud\rangle + |du\rangle)$$

o

$$\langle \sigma_z\rangle = \frac{1}{2}\Big(\langle ud| - \langle du|\Big)\Big(|ud\rangle + |du\rangle \Big).$$

Una inspección rápida muestra que esto es igual a cero. A continuación, consideremos $\langle \sigma_x\rangle$:

  19 

174 LECCIÓN 6. ENTRELAZAMIENTO

$$\langle \sigma_{x}\rangle = \langle sing|\sigma_{x}|sing\rangle$$ $$= \langle sing|\sigma_{x}\frac{1}{\sqrt{2}}\big(|ud\rangle - |du\rangle \big)$$

o

$$\langle \sigma_{x}\rangle = \frac{1}{2}\Big(\langle ud| - \langle du|\Big)\Big(|dd\rangle - |uu\rangle \Big).$$

De nuevo, esta ecuación nos da cero. Finalmente, veamos $\langle \sigma_{y}\rangle$:

$$\langle \sigma_{y}\rangle = \langle sing|\sigma_{y}|sing\rangle$$ $$= \frac{1}{2}\Big(\langle ud| - \langle du|\Big)\Big(i|dd\rangle + i|uu\rangle \Big).$$

Como habrás adivinado, una vez más nos quedamos con cero. Por lo tanto, hemos demostrado que para el estado $|sing\rangle$,

$$\langle \sigma_{z}\rangle = \langle \sigma_{x}\rangle = \langle \sigma_{y}\rangle = 0,$$

y de hecho todos los valores esperados de $\sigma$ son cero. No hace falta decir que lo mismo es cierto para los valores esperados de $\tau$. Claramente, $|sing\rangle$ es muy diferente de un estado producto. ¿Qué dice todo esto sobre las mediciones que podemos hacer?

Si el valor esperado de una componente de $\sigma$ es cero, significa que el resultado experimental es igualmente probable que sea

  19 

1 o $-1$. En otras palabras, el resultado es completamente incierto. Aunque conocemos el vector de estado exacto, $|sing\rangle$, no sabemos nada en absoluto sobre el resultado de cualquier medición de cualquier componente de cualquiera de los dos espines.

Quizás esto significa que el estado $|sing\rangle$ es de alguna manera incompleto —que hay detalles del sistema que descuidamos y no medimos. Después de todo, antes vimos un ejemplo perfectamente clásico en el que Alicia y Beto no sabían nada sobre sus monedas hasta que realmente las miraron. ¿En qué se diferencia la versión cuántica?

En nuestro ejemplo de "entrelazamiento clásico" que involucra a Alicia, Beto y Carlos, está perfectamente claro que había más por conocer. Carlos podría haber echado un vistazo a las monedas sin cambiar nada, porque las mediciones clásicas pueden ser arbitrariamente suaves.

¿Podría haber las llamadas variables ocultas en el sistema cuántico? La respuesta es que según las reglas de la mecánica cuántica, no hay nada que conocer más allá de lo que está codificado en el vector de estado —en el presente caso, $|sing\rangle$. El vector de estado es una descripción tan completa de un sistema como es posible hacer. Así que parece que en mecánica cuántica, podemos saber todo sobre un sistema compuesto —todo lo que hay que saber, de todos modos— y aún así no saber nada sobre sus partes constituyentes. Esta es la verdadera rareza del entrelazamiento, que tanto perturbó a Einstein.

### 6.9 Observables Compuestos

Imaginemos una configuración cuántica de Alicia-Beto-Carlos. El papel de Carlos es preparar dos espines en el estado entrelazado

  19 

176 LECCIÓN 6. ENTRELAZAMIENTO

$|sing\rangle$. Luego, sin mirar los espines (recuerda, las mediciones cuánticas no son suaves), le da un espín a Alicia y uno a Beto. Aunque Alicia y Beto saben exactamente en qué estado está el sistema combinado, no pueden predecir nada sobre el resultado de sus mediciones individuales.

Pero seguramente conocer el estado exacto del sistema compuesto debe decirles algo, incluso si el estado está altamente entrelazado. Y de hecho es así. Sin embargo, para entender lo que les dice, tenemos que considerar una familia más amplia de observables que aquellos que Alicia y Beto pueden medir por separado, cada uno usando solo su propio detector. Resulta que hay observables que solo pueden medirse usando ambos detectores. Los resultados de tales experimentos solo pueden ser conocidos por Alicia o Beto si se reúnen y comparan notas.

La primera pregunta es si Alicia y Beto pueden medir simultáneamente sus propios observables. Hemos visto que hay cantidades que no pueden medirse simultáneamente. En particular, dos observables que no conmutan no pueden medirse ambos sin que las mediciones interfieran entre sí. Pero para Alicia y Beto, es fácil ver que cada componente de $\sigma$ conmuta con cada componente de $\tau$. Este es un hecho general sobre los productos tensoriales. Los operadores que actúan sobre los dos factores separados conmutan entre sí. Por lo tanto, Alicia puede hacer cualquier medición en su espín y Beto puede hacer cualquier medición en el suyo, sin que ninguno interfiera con el experimento del otro.

Supongamos que Alicia mide $\sigma_{z}$ y Beto mide $\tau_{z}$, y luego multiplican los resultados. En otras palabras, conspiran para medir el producto $\tau_{z}\sigma_{z}$.

  19 

6.9. OBSERVABLES COMPUESTOS 177

El producto $\tau_{z}\sigma_{z}$ es un observable que se representa matemáticamente aplicando primero $\sigma_{z}$ a un ket y luego aplicando subsiguientemente $\tau_{z}$. Ten en cuenta que estas son solo las operaciones matemáticas que definen un nuevo operador: son diferentes del acto de realizar una medición física. No necesitas un aparato para multiplicar dos operadores; solo necesitas lápiz y papel. Veamos qué sucede si aplicamos el producto $\tau_{z}\sigma_{z}$ al estado $|sing\rangle$:

$$\tau_{z}\sigma_{z}\frac{1}{\sqrt{2}}\Big(|ud\rangle - |du\rangle \Big).$$

Primero, usando la tabla en las Ecs. 6.8, aplicamos $\sigma_{z}$:

$$\tau_{z}\sigma_{z}\frac{1}{\sqrt{2}}\Big(|ud\rangle - |du\rangle \Big) = \tau_{z}\frac{1}{\sqrt{2}}\Big(|ud\rangle + |du\rangle \Big).$$

Ahora, aplicamos $\tau_{z}$ para obtener

$$\tau_{z}\sigma_{z}\frac{1}{\sqrt{2}}\Big(|ud\rangle - |du\rangle \Big) = \frac{1}{\sqrt{2}}\Big(-|ud\rangle + |du\rangle \Big).$$

Observa que el resultado final es simplemente cambiar el signo de $|sing\rangle$:

$$\tau_{z}\sigma_{z}|sing\rangle = -|sing\rangle.$$

Evidentemente, $|sing\rangle$ es un vector propio del observable $\tau_{z}\sigma_{z}$ con valor propio $-1$. Examinemos el significado de este resultado. Alicia mide $\sigma_{z}$ y Beto mide $\tau_{z}$; cuando se reúnen y comparan resultados, encuentran que han medido valores opuestos. A veces, Beto mide $+1$ y

  19 

178 LECCIÓN 6. ENTRELAZAMIENTO

Alicia mide $-1$. Otras veces, Alicia mide $+1$ y Beto mide $-1$. El producto de las dos mediciones es siempre $-1$.

No debería haber nada sorprendente en este resultado. El vector de estado $|sing\rangle$ es una superposición de dos vectores, $|ud\rangle$ y $|du\rangle$, ambos comprenden dos espines con componentes $z$ opuestas. La situación es completamente similar al ejemplo clásico con Carlos y sus dos monedas.

Pero ahora llegamos a algo que no tiene análogo clásico. Supongamos que en lugar de medir las componentes $z$ de sus espines, Alicia y Beto miden las componentes $x$. Para descubrir cómo se correlacionan sus resultados, debemos estudiar el observable $\tau_{x}\sigma_{x}$.

Actuemos sobre $|sing\rangle$ con este producto. Aquí están los pasos:

$$\tau_{x}\sigma_{x}|sing\rangle = \tau_{x}\sigma_{x}\frac{1}{\sqrt{2}}\Big(|ud\rangle - |du\rangle \Big)$$ $$= \tau_{x}\frac{1}{\sqrt{2}}\Big(|dd\rangle - |uu\rangle \Big)$$ $$= \frac{1}{\sqrt{2}}\Big(|du\rangle - |ud\rangle \Big)$$

o, más simplemente,

$$\tau_{x}\sigma_{x}|sing\rangle = -|sing\rangle.$$

Ahora esto es un poco sorprendente: $|sing\rangle$ también es un vector propio de $\tau_{x}\sigma_{x}$ con valor propio $-1$. Es mucho menos obvio con solo mirar $|sing\rangle$ que las componentes $x$ de los dos espines

  20 

6.9. OBSERVABLES COMPUESTOS 179

son siempre opuestas. Sin embargo, cada vez que Alicia y Beto las miden, encuentran que $\sigma_{x}$ y $\tau_{x}$ tienen valores opuestos. En este punto, probablemente no te sorprenderá saber que lo mismo es cierto para las componentes $y$.

**Ejercicio 6.6:** Supón que Carlos ha preparado los dos espines en el estado singlete. Esta vez, Beto mide $\tau_{y}$ y Alicia mide $\sigma_{x}$. ¿Cuál es el valor esperado de $\sigma_{x}\tau_{y}$?

¿Qué dice esto sobre la correlación entre las dos mediciones?

**Ejercicio 6.7:** A continuación, Carlos prepara los espines en un estado diferente, llamado $|T_{1}\rangle$, donde

$$|T_{1}\rangle = \frac{1}{\sqrt{2}}\Big(|ud\rangle + |du\rangle \Big).$$

En estos ejemplos, $T$ significa triplete. Estos estados triplete son completamente diferentes de los estados en los ejemplos de la moneda y el dado. ¿Cuáles son los valores esperados de los operadores $\sigma_{z}\tau_{z}$, $\sigma_{x}\tau_{x}$ y $\sigma_{y}\tau_{y}$?

¡Qué diferencia puede hacer un signo!

**Ejercicio 6.8:** Haz lo mismo para los otros dos estados triplete entrelazados,

$$|T_{2}\rangle = \frac{1}{\sqrt{2}}\Big(|uu\rangle + |dd\rangle \Big)$$ $$|T_{3}\rangle = \frac{1}{\sqrt{2}}\Big(|uu\rangle - |dd\rangle \Big),$$

e interpreta.

  20 

180 LECCIÓN 6. ENTRELAZAMIENTO

Finalmente, consideremos un observable más. Este no puede ser medido por Alicia y Beto haciendo mediciones separadas con sus aparatos individuales, incluso si se reúnen y comparan notas. Sin embargo, la mecánica cuántica insiste en que se puede construir algún tipo de aparato para medir el observable.

El observable al que me refiero puede pensarse como el producto escalar ordinario de los operadores vectoriales $\vec{\sigma}$ y $\vec{\tau}$:

$$\vec{\sigma} \cdot \vec{\tau} = \sigma_x \tau_x + \sigma_y \tau_y + \sigma_z \tau_z.$$

Uno podría pensar que se puede encontrar un valor para este observable si Beto mide todas las componentes de $\tau$, mientras que Alicia mide todas las componentes de $\sigma$; entonces podrían multiplicar las componentes y sumarlas. El problema es que Beto no puede medir simultáneamente las componentes individuales de $\tau$, porque no conmutan. Del mismo modo, Alicia no puede medir más de una componente de $\sigma$ a la vez. Para medir $\vec{\sigma} \cdot \vec{\tau}$, se debe construir un nuevo tipo de aparato, uno que mida $\vec{\sigma} \cdot \vec{\tau}$ sin medir ninguna componente individual. No es obvio cómo podría hacerse eso. Aquí hay un ejemplo concreto de cómo podría llevarse a cabo tal medición: Algunos átomos tienen espines que se describen de la misma manera que los espines de los electrones. Cuando dos de estos átomos están cerca uno del otro —por ejemplo, dos átomos vecinos en una red cristalina— el Hamiltoniano dependerá de los espines. En algunas situaciones, el Hamiltoniano de los espines vecinos es proporcional a $\vec{\sigma} \cdot \vec{\tau}$. Si ese es el caso, entonces medir $\vec{\sigma} \cdot \vec{\tau}$ es equivalente a medir la energía del par atómico. Medir esta energía es una sola medición del operador compuesto

  20 

6.9. OBSERVABLES COMPUESTOS 181

y no implica medir las componentes individuales de ninguno de los dos espines.

**Ejercicio 6.9:** Demuestra que los cuatro vectores $|sing\rangle, |T_1\rangle, |T_2\rangle,$ y $|T_3\rangle$ son vectores propios de $\vec{\sigma} \cdot \vec{\tau}$. ¿Cuáles son sus valores propios?

Echa un vistazo a tus resultados de este último ejercicio. ¿Ves por qué uno de estos vectores de estado se llama singlete, mientras que los otros tres se llaman tripletes? La razón es que si observas su relación con el operador $\vec{\sigma} \cdot \vec{\tau}$, el singlete es un vector propio con un valor propio, y los tripletes son todos vectores propios con un valor propio degenerado diferente.

Aquí hay un buen ejercicio que combina el concepto de entrelazamiento con los conceptos de tiempo y cambio de la Lección 4. Úsalo para repasar las ideas de la evolución temporal unitaria y el significado del Hamiltoniano.

**Ejercicio 6.10:** Un sistema de dos espines tiene el Hamiltoniano

$$\mathbf{H} = \frac{\omega}{2} \vec{\sigma} \cdot \vec{\tau}.$$

¿Cuáles son las posibles energías del sistema, y cuáles son los vectores propios del Hamiltoniano?

Supón que el sistema comienza en el estado $|uu\rangle$. ¿Cuál es el estado en cualquier tiempo posterior? Responde la misma pregunta para los estados iniciales $|ud\rangle, |du\rangle,$ y $|dd\rangle$.

---

[Fin de la Parte 1/5. Continuará con Capítulo 7...]

---
[PARTE 2/5 - Capítulo 7]

---

  20 

# Lección 7

## Más sobre Entrelazamiento

Hilbert's Place, verano de 1935:

Ddos parroquianos desaliñados entran por las puertas batientes, en medio de una intensa conversación. El de pelo grisáceo alborotado y suéter raído dice: "No, no aceptaré tu teoría a menos que puedas decirme cuáles son los elementos de la realidad física".

El otro mira a su alrededor, levanta las manos en obvia frustración, y le dice a Art y Lenny: "Otra vez con eso. Elementos de la realidad física, EPR, EPR, es lo único en lo que piensa. Albert, deja de ser obsesivo y acepta los hechos".

"¡Nunca! No puedo aceptar que uno pueda saber todo lo que hay que saber sobre una cosa, y aún así no saber nada sobre sus partes. Eso es un completo sinsentido, Niels".

"Lo siento, Albert. Así son las cosas. Toma, déjame invitarte una cerveza".

  20 

184 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

En esta lección, examinaremos el entrelazamiento con mayor profundidad. Para ello, necesitaremos algunas herramientas matemáticas adicionales. Primero, descubriremos cómo trabajar con productos tensoriales en forma de componentes. Luego, aprenderemos sobre un nuevo operador llamado la matriz densidad.

Estas herramientas no son inherentemente difíciles de dominar, pero requieren algo de paciencia y una cantidad considerable de manipulación de índices.

### 7.1 Interludio Matemático: Productos Tensoriales en Forma de Componentes

En la Lección 6, explicamos cómo formar el producto tensorial de dos espacios vectoriales utilizando la notación abstracta de bras, kets y símbolos de operadores como $\sigma_z$. ¿Cómo se traduce eso en columnas, filas y matrices?

Construir productos tensoriales a partir de matrices y vectores columna no es difícil. Las reglas son sencillas, como veremos a continuación.

La parte complicada es entender por qué estas reglas funcionan —por qué nos permiten construir matrices y vectores columna que tienen las propiedades que deseamos. Abordaremos el problema de dos maneras diferentes. Primero, construiremos operadores compuestos utilizando el método probado y verdadero que desarrollamos en la Lección 3. Luego, te mostraremos cómo construir operadores compuestos directamente a partir de sus operadores componentes.

  20 

7.1. INTERLUDIO: MATRICES DE PRODUCTO TENSORIAL 185

#### 7.1.1 Construcción de Matrices de Producto Tensorial a partir de Principios Básicos

En la Lección 3, te mostramos cómo escribir cualquier observable $\mathbf{M}$ en forma matricial, relativo a una base específica. Tómate un momento para repasar las Ecs. 3.1 a 3.4. En esa sección, calculamos los valores numéricos $m_{jk}$ de los elementos de matriz de $\mathbf{M}$ con la expresión

$$m_{jk} = \langle j|\mathbf{M}|k\rangle, \quad (7.1)$$

donde $|j\rangle$ y $|k\rangle$ representan los vectores base. Cada combinación de $|j\rangle, |k\rangle$ genera un elemento de matriz diferente.$^1$

Nuestro plan es aplicar esta fórmula a algunos operadores de producto tensorial y ver qué obtenemos. Debido a nuestra convención de doble índice para los vectores base del producto tensorial, los "sándwiches" en estas ecuaciones se verán un poco diferentes de los de la Ec. 7.1. En cada extremo del sándwich, recorreremos los vectores base $|uu\rangle, |ud\rangle, |du\rangle,$ y $|dd\rangle$.$^2$

Para mantener las cosas simples, usaremos el operador $\sigma_z \otimes I$ como ejemplo, donde $I$ es el operador identidad. Como hemos visto, $\sigma_z \otimes I$ actúa sobre la mitad de Alicia del vector de estado con $\sigma_z$, y no hace absolutamente nada en la mitad de Beto. Debido a que estamos trabajando en un espacio vectorial de cuatro dimensiones, la matriz resultante

$^1$En la Lección 3, por casualidad escribimos el índice $j$ en el lado izquierdo de $\mathbf{M}$ y $k$ en el derecho, lo contrario de lo que estamos haciendo aquí. Como $j$ y $k$ son variables índice, esto no hace ninguna diferencia siempre que mantengamos la consistencia dentro de un grupo de ecuaciones.

$^2$Por supuesto, podríamos haber usado un conjunto diferente de vectores base, como $|rr\rangle, |rl\rangle$, etc. Hacerlo resultaría en un conjunto diferente de elementos de matriz.

  20 

186 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

será de $4 \times 4$. Omitiendo múltiples símbolos $\otimes$ para evitar desorden visual, podemos escribir la matriz así:

$$\sigma_z \otimes I =
\begin{pmatrix}
\langle uu|\sigma_z I|uu\rangle & \langle uu|\sigma_z I|ud\rangle & \langle uu|\sigma_z I|du\rangle & \langle uu|\sigma_z I|dd\rangle \\
\langle ud|\sigma_z I|uu\rangle & \langle ud|\sigma_z I|ud\rangle & \langle ud|\sigma_z I|du\rangle & \langle ud|\sigma_z I|dd\rangle \\
\langle du|\sigma_z I|uu\rangle & \langle du|\sigma_z I|ud\rangle & \langle du|\sigma_z I|du\rangle & \langle du|\sigma_z I|dd\rangle \\
\langle dd|\sigma_z I|uu\rangle & \langle dd|\sigma_z I|ud\rangle & \langle dd|\sigma_z I|du\rangle & \langle dd|\sigma_z I|dd\rangle
\end{pmatrix}. \quad (7.2)$$

Para evaluar estos elementos de matriz, podríamos permitir que $\sigma_z$ e $I$ operen hacia la izquierda o hacia la derecha. Supongamos que $\sigma_z$ opera hacia la izquierda e $I$ opera hacia la derecha. Dado que $I$ no hace nada, todo lo que nos importa es lo que $\sigma_z$ le hace al vector bra a su izquierda. Y dentro de ese vector bra, $\sigma_z$ solo actúa sobre la etiqueta de estado más a la izquierda (es decir, la de Alicia). Usando las reglas que ya hemos establecido (ver Ecs. 6.6 y 6.7), podemos llevar a cabo todas estas operaciones de $\sigma_z$ para obtener una matriz de productos internos:

$$\sigma_z \otimes I =
\begin{pmatrix}
\langle uu|uu\rangle & \langle uu|ud\rangle & \langle uu|du\rangle & \langle uu|dd\rangle \\
\langle ud|uu\rangle & \langle ud|ud\rangle & \langle ud|du\rangle & \langle ud|dd\rangle \\
-\langle du|uu\rangle & -\langle du|ud\rangle & -\langle du|du\rangle & -\langle du|dd\rangle \\
-\langle dd|uu\rangle & -\langle dd|ud\rangle & -\langle dd|du\rangle & -\langle dd|dd\rangle
\end{pmatrix}. \quad (7.3)$$

  20 

7.1. INTERLUDIO: MATRICES DE PRODUCTO TENSORIAL 187

Debido a que estos vectores propios son ortonormales, la matriz se reduce a

$$\sigma_z \otimes I =
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{pmatrix}. \quad (7.4)$$

¿Cómo escribimos los vectores propios $|uu\rangle, |ud\rangle, |du\rangle,$ y $|dd\rangle$ como vectores columna?

Por ahora, solo te diré que representaremos $|uu\rangle$ y $|du\rangle$ como

$$|uu\rangle =
\begin{pmatrix}
1 \\ 0 \\ 0 \\ 0
\end{pmatrix},
\quad
|du\rangle =
\begin{pmatrix}
0 \\ 0 \\ 1 \\ 0
\end{pmatrix}. \quad (7.5)$$

Veamos qué sucede cuando $\sigma_z \otimes I$ opera sobre estos vectores columna. Aplicando la matriz a $|uu\rangle$ resulta en

$$\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{pmatrix}
\begin{pmatrix}
1 \\ 0 \\ 0 \\ 0
\end{pmatrix}
=
\begin{pmatrix}
1 \\ 0 \\ 0 \\ 0
\end{pmatrix}.$$

En otras palabras,

$$(\sigma_z \otimes I)|uu\rangle = |uu\rangle,$$

tal como esperamos. ¿Qué sucede si aplicamos la misma matriz al vector columna $|du\rangle$ de las Ecs. 7.5? Realizando la multiplicación de matrices obtenemos $-|du\rangle$, tal como debería ser.

  20 

188 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

#### 7.1.2 Construcción de Matrices de Producto Tensorial a partir de Matrices Componentes

El método anterior para calcular elementos de matriz es muy general: funciona para todos los observables. Si necesitamos construir el producto tensorial de dos operadores, y ya conocemos los elementos de matriz de los bloques constituyentes, podemos combinarlos directamente. Aquí está la regla para combinar matrices $2 \times 2$ para formar matrices $4 \times 4$:

$$A \otimes B =
\begin{pmatrix}
A_{11}B & A_{12}B \\
A_{21}B & A_{22}B
\end{pmatrix} \quad (7.6)$$

o

$$A \otimes B =
\begin{pmatrix}
A_{11}B_{11} & A_{11}B_{12} & A_{12}B_{11} & A_{12}B_{12} \\
A_{11}B_{21} & A_{11}B_{22} & A_{12}B_{21} & A_{12}B_{22} \\
A_{21}B_{11} & A_{21}B_{12} & A_{22}B_{11} & A_{22}B_{12} \\
A_{21}B_{21} & A_{21}B_{22} & A_{22}B_{21} & A_{22}B_{22}
\end{pmatrix}. \quad (7.7)$$

El mismo patrón funciona para matrices de cualquier tamaño. Este tipo de multiplicación de matrices a veces se llama producto de Kronecker, un término que solo se aplica a matrices —es la versión matricial del producto tensorial. El producto de Kronecker de dos matrices $2 \times 2$ es una matriz $4 \times 4$, y el patrón es similar para matrices de tamaño arbitrario. En general, el producto de Kronecker de una matriz $m \times n$ y una matriz $p \times q$ es una matriz $mp \times nq$.

Todo esto se aplica perfectamente a los vectores columna y fila, que son solo matrices especializadas. El producto tensorial de dos vectores columna $2 \times 1$ es un vector columna $4 \times 1$. Si $a$ y $b$ son vectores columna $2 \times 1$, su producto tensorial se ve así:

  21 

7.1. INTERLUDIO: MATRICES DE PRODUCTO TENSORIAL 189

$$\begin{pmatrix} a_{11} \\ a_{21} \end{pmatrix} \otimes
\begin{pmatrix} b_{11} \\ b_{21} \end{pmatrix} =
\begin{pmatrix}
a_{11}b_{11} \\
a_{11}b_{21} \\
a_{21}b_{11} \\
a_{21}b_{21}
\end{pmatrix}. \quad (7.8)$$

Veamos cómo funciona esto para Alicia y Beto. Primero, construiremos los cuatro vectores base del producto tensorial, usando $|u\rangle$ y $|d\rangle$ como bloques de construcción. Recordemos las Ecs. 2.11 y 2.12 de la Lección 2,

$$|u\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \quad |d\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}.$$

Si insertamos las combinaciones apropiadas de $|u\rangle$ y $|d\rangle$ en la Ec. 7.8, nuestros cuatro vectores columna $4 \times 1$ son

$$|uu\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \otimes \begin{pmatrix} 1 \\ 0 \end{pmatrix} =
\begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \end{pmatrix}$$
$$|ud\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \otimes \begin{pmatrix} 0 \\ 1 \end{pmatrix} =
\begin{pmatrix} 0 \\ 1 \\ 0 \\ 0 \end{pmatrix}$$
$$|du\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \otimes \begin{pmatrix} 1 \\ 0 \end{pmatrix} =
\begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix}$$

  21 

190 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

$$|dd\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \otimes \begin{pmatrix} 0 \\ 1 \end{pmatrix} =
\begin{pmatrix} 0 \\ 0 \\ 0 \\ 1 \end{pmatrix}. \quad (7.9)$$

A continuación, usaremos la regla de la Ec. 7.7 para combinar los operadores $\sigma_z$ y $\tau_x$. Usando las Ecs. 3.20 para definir las matrices $\sigma_z$ y $\tau_x$, esta regla da la matriz de producto tensorial

$$\sigma_z \otimes \tau_x =
\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} \otimes
\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} =
\begin{pmatrix}
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 0 & 0 & -1 \\
0 & 0 & -1 & 0
\end{pmatrix}.$$

Comparemos este resultado con el producto de $\sigma_x$ y $\tau_z$,

$$\sigma_x \otimes \tau_z =
\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \otimes
\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} =
\begin{pmatrix}
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1 \\
1 & 0 & 0 & 0 \\
0 & -1 & 0 & 0
\end{pmatrix}.$$

Observa que $\sigma_x \otimes \tau_z$ no es lo mismo que $\sigma_z \otimes \tau_x$. Eso es natural, porque representan observables diferentes.

Hasta aquí, todo bien. Pero a continuación, veremos algo un poco más interesante. Con la ayuda de algunos ejercicios, intentaremos convencerte de que el producto de Kronecker es realmente el producto tensorial para matrices —en otras palabras, que la mitad de Alicia de la matriz solo afecta a su mitad del vector columna, y lo mismo para Beto. Esto es complicado debido a la forma en que el producto de Kronecker mezcla los elementos de sus bloques constituyentes.

  21 

7.1. INTERLUDIO: MATRICES DE PRODUCTO TENSORIAL 191

Como ejemplo, veamos cómo $\sigma_z \otimes \tau_x$ actúa sobre $|ud\rangle$. Traduciendo los símbolos abstractos a componentes, podemos escribir

$$(\sigma_z \otimes \tau_x)|ud\rangle =
\begin{pmatrix}
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 0 & 0 & -1 \\
0 & 0 & -1 & 0
\end{pmatrix}
\begin{pmatrix}
0 \\ 1 \\ 0 \\ 0
\end{pmatrix}
=
\begin{pmatrix}
1 \\ 0 \\ 0 \\ 0
\end{pmatrix}.$$

Pero el vector columna del lado derecho corresponde a $|uu\rangle$ en las Ecs. 7.9. Traducido de nuevo a notación abstracta, esto se convierte en

$$(\sigma_z \otimes \tau_x)|ud\rangle = |uu\rangle.$$

Esto es exactamente lo que queremos —una representación matricial de nuestros operadores abstractos y vectores de estado que replica su comportamiento conocido.

El siguiente ejercicio ayudará a cristalizar la idea de que la mitad-$\sigma$ de $\sigma \otimes \tau$ solo afecta a la mitad de Alicia del vector de estado, y que la mitad-$\tau$ solo afecta a la de Beto. El que sigue después proporciona práctica para calcular los elementos de matriz de un operador, asumiendo que ya sabemos lo que el operador le hace a cada vector base.

**Ejercicio 7.1:** Escribe el producto tensorial $I \otimes \tau_x$ como una matriz, y aplica esa matriz a cada uno de los vectores columna $|uu\rangle, |ud\rangle, |du\rangle,$ y $|dd\rangle$. Muestra que la mitad de Alicia del vector de estado no cambia en cada caso. Recuerda que $I$ es la matriz unitaria $2 \times 2$.

**Ejercicio 7.2:** Calcula los elementos de matriz de $\sigma_z \otimes \tau_x$ formando productos internos como hicimos en la Ec. 7.2.

  21 

192 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

El tercer ejercicio es un poco tedioso, pero realmente consolida las cosas. Considera la ecuación

$$(A \otimes B) (a \otimes b) = (Aa \otimes Bb). \quad (7.10)$$

Como en las Ecs. 7.7 y 7.8, $A$ y $B$ representan matrices (u operadores) $2 \times 2$, y $a$ y $b$ representan vectores columna $2 \times 1$. El ejercicio te pide expandir la ecuación en componentes y mostrar que el lado izquierdo coincide con el lado derecho.

**Ejercicio 7.3:**

a) Reescribe la Ec. 7.10 en forma de componentes, reemplazando los símbolos $A, B, a,$ y $b$ con las matrices y vectores columna de las Ecs. 7.7 y 7.8.

b) Realiza las multiplicaciones de matrices $Aa$ y $Bb$ en el lado derecho. Verifica que cada resultado sea una matriz $4 \times 1$.

c) Expande los tres productos de Kronecker.

d) Verifica los tamaños de fila y columna de cada producto de Kronecker:
   * $A \otimes B$: $4 \times 4$
   * $a \otimes b$: $4 \times 1$
   * $Aa \otimes Bb$: $4 \times 1$

e) Realiza la multiplicación de matrices en el lado izquierdo, resultando en un vector columna $4 \times 1$. Cada fila debe ser la suma de cuatro términos separados.

f) Finalmente, verifica que los vectores columna resultantes en los lados izquierdo y derecho sean idénticos.

  21 

7.2. INTERLUDIO: PRODUCTOS EXTERNOS 193

### 7.2 Interludio Matemático: Productos Externos

Dado un bra $\langle \varphi|$ y un ket $|\psi\rangle$, podemos formar el producto interno $\langle \varphi|\psi\rangle$. Como hemos visto, el producto interno es un número complejo. Sin embargo, hay otro tipo de producto llamado producto externo, escrito

$$|\psi\rangle \langle \varphi|.$$

El producto externo no es un número; es un operador lineal.

Consideremos qué sucede cuando $|\psi\rangle \langle \varphi|$ actúa sobre otro ket $|A\rangle$:

$$|\psi\rangle \langle \varphi| |A\rangle.$$

En estos ejemplos, estamos usando el espaciado en lugar de paréntesis para mostrar la agrupación de las operaciones. Recuerda que todas las operaciones con bras, kets y operadores lineales son asociativas, lo que significa que podemos agruparlas de la manera que queramos, siempre que mantengamos el mismo orden de izquierda a derecha.$^3$

La acción del operador producto externo es muy simple y puede definirse como

$$|\psi\rangle \langle \varphi| |A\rangle \equiv |\psi\rangle \langle \varphi|A\rangle.$$

$^3$A veces también podemos cambiar el orden de izquierda a derecha, pero eso requiere más cuidado.

  21 

194 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

En otras palabras, tomamos el producto interno de $\langle \varphi|$ con $|A\rangle$ (el resultado es un número complejo) y lo multiplicamos por el ket $|\psi\rangle$.

La notación bra-ket es tan eficiente que prácticamente nos fuerza a adoptar esta definición. Ese fue el genio de Paul Dirac. Es fácil demostrar que el producto externo también puede actuar sobre bras:

$$\langle B| |\psi\rangle \langle \varphi| \equiv \langle B|\psi\rangle \langle \varphi|.$$

Un caso especial es el producto externo de un ket con su bra correspondiente, $|\psi\rangle \langle \psi|$. Suponiendo que $|\psi\rangle$ está normalizado, este operador se llama operador de proyección. Así es como actúa:

$$|\psi\rangle \langle \psi| |A\rangle = |\psi\rangle \langle \psi|A\rangle$$

Observa que el resultado es siempre proporcional a $|\psi\rangle$. Se puede decir que un operador de proyección proyecta un vector sobre la dirección definida por $|\psi\rangle$. Aquí hay algunas propiedades de los operadores de proyección que puedes demostrar fácilmente (recuerda que $|\psi\rangle$ está normalizado a 1):

* Los operadores de proyección son hermíticos.
* El vector $|\psi\rangle$ es un vector propio de su operador de proyección con valor propio 1:
  $$|\psi\rangle \langle \psi| |\psi\rangle = |\psi\rangle$$
* Cualquier vector ortogonal a $|\psi\rangle$ es un vector propio con valor propio cero. Por lo tanto, los valores propios de $|\psi\rangle \langle \psi|$ son todos 0 o 1, y solo hay un vector propio con valor propio unitario. Ese vector propio es el propio $|\psi\rangle$.

  21 

7.2. INTERLUDIO: PRODUCTOS EXTERNOS 195

* El cuadrado de un operador de proyección es el mismo que el operador de proyección mismo:
  $$|\psi\rangle \langle \psi|^2 = |\psi\rangle \langle \psi|.$$
* La traza de un operador (o de cualquier matriz cuadrada) se define como la suma de sus elementos diagonales. Usando el símbolo Tr para la traza, podemos definir la traza de un operador $\mathbf{L}$ como
  $$\text{Tr} \, \mathbf{L} = \sum_i \langle i|\mathbf{L}|i\rangle,$$
  que es simplemente la suma de los elementos de la matriz diagonal de $\mathbf{L}$. La traza de un operador de proyección es 1. Esto se sigue del hecho de que la traza de un operador hermítico es la suma de sus valores propios.$^4$
* Si sumamos todos los operadores de proyección para un sistema de base, obtenemos el operador identidad:
  $$\sum_i |i\rangle \langle i| = I. \quad (7.11)$$

Finalmente, aquí hay un teorema muy importante sobre los operadores de proyección y los valores esperados. El valor esperado de cualquier observable $\mathbf{L}$ en el estado $|\psi\rangle$ está dado por

$$\langle \psi|\mathbf{L}|\psi\rangle = \text{Tr} \, |\psi\rangle \langle \psi| \, \mathbf{L}. \quad (7.12)$$

Aquí están los pasos para demostrarlo. Elige cualquier base $|i\rangle$. Luego, usando la definición de traza, escribe

$$\text{Tr} \, |\psi\rangle \langle \psi| \, \mathbf{L} = \sum_i \langle i|\psi\rangle \langle \psi|\mathbf{L}|i\rangle.$$

$^4$Una matriz hermítica $\mathbf{M}$ puede diagonalizarse mediante una transformación $\mathbf{P}^\dagger\mathbf{MP}$, donde $\mathbf{P}$ es una matriz unitaria cuyas columnas son los vectores propios normalizados de $\mathbf{M}$. La traza de $\mathbf{M}$ es invariante bajo esta transformación. No hemos demostrado este conocido resultado.

  21 

196 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

Los dos factores en la suma son solo números, por lo que podemos invertir su orden:

$$\text{Tr} \, |\psi\rangle \langle \psi| \, \mathbf{L} = \sum_i \langle \psi|\mathbf{L}|i\rangle \langle i|\psi\rangle.$$

Realizando la suma y usando $\sum |i\rangle \langle i| = I$, obtenemos

$$\text{Tr} \, |\psi\rangle \langle \psi| \, \mathbf{L} = \langle \psi|\mathbf{L}|\psi\rangle.$$

El lado derecho es justamente el valor esperado de $\mathbf{L}$.

### 7.3 Matrices Densidad: Una Nueva Herramienta

Hasta ahora, hemos aprendido cómo hacer predicciones sobre un sistema cuando conocemos el estado cuántico exacto del sistema. Pero la mayoría de las veces, no tenemos un conocimiento completo del estado. Por ejemplo, supongamos que Alicia ha preparado un espín usando un aparato orientado a lo largo de algún eje. Ella le da el espín a Beto pero no le dice el eje a lo largo del cual estaba orientado el aparato. Quizás le da alguna información parcial, como el hecho de que el eje estaba a lo largo del eje $z$ o del eje $x$, pero se niega a decirle más. ¿Qué hace Beto? ¿Cómo utiliza esta información para hacer predicciones?

Beto razona de la siguiente manera: Si Alicia preparó el espín en el estado $|\psi\rangle$, entonces el valor esperado de cualquier observable $\mathbf{L}$ es $\text{Tr} \, |\psi\rangle \langle \psi|\mathbf{L} = \langle \psi|\mathbf{L}|\psi\rangle$.

Por otro lado, si Alicia preparó el espín en el estado $|\varphi\rangle$, entonces el valor esperado de $\mathbf{L}$ es $\text{Tr} \, |\varphi\rangle \langle \varphi|\mathbf{L} = \langle \varphi|\mathbf{L}|\varphi\rangle$.

  21 

7.3. MATRICES DENSIDAD 197

¿Qué sucede si hay un 50 por ciento de probabilidad de que ella haya preparado $|\psi\rangle$ y un 50 por ciento de probabilidad de que haya preparado $|\varphi\rangle$? Obviamente, el valor esperado es

$$\langle \mathbf{L} \rangle = \frac{1}{2} \text{Tr} \, |\psi\rangle \langle \psi|\mathbf{L} + \frac{1}{2} \text{Tr} \, |\varphi\rangle \langle \varphi|\mathbf{L}.$$

Todo lo que estamos haciendo es promediar sobre la ignorancia de Beto acerca del estado preparado por Alicia.

Pero ahora podemos combinar los términos en una sola expresión definiendo una **matriz densidad** $\rho$ que codifica el conocimiento de Beto. En este caso, la matriz densidad es la mitad del operador de proyección sobre $|\varphi\rangle$ más la mitad del operador de proyección sobre $|\psi\rangle$,

$$\rho = \frac{1}{2} |\psi\rangle \langle \psi| + \frac{1}{2} |\varphi\rangle \langle \varphi|.$$

Hemos empaquetado todo el conocimiento de Beto sobre el sistema en un solo operador $\rho$. En este punto, la regla para calcular valores esperados se vuelve muy simple:

$$\langle \mathbf{L} \rangle = \text{Tr} \, \rho \mathbf{L}. \quad (7.13)$$

Podemos generalizar esto. Supongamos que Alicia le dice a Beto que ha preparado uno de varios estados —llamémoslos $|\varphi_1\rangle, |\varphi_2\rangle, |\varphi_3\rangle$, y así sucesivamente. Además, especifica probabilidades $P_1, P_2, P_3, \ldots$ para cada uno de estos estados. Beto aún puede empaquetar todo su conocimiento en una matriz densidad:

$$\rho = P_1 |\varphi_1\rangle \langle \varphi_1| + P_2 |\varphi_2\rangle \langle \varphi_2| + P_3 |\varphi_3\rangle \langle \varphi_3| + \ldots.$$

Además, puede usar exactamente la misma regla, Ec. 7.13, para calcular el valor esperado.

  21 

198 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

Cuando la matriz densidad corresponde a un solo estado, es un operador de proyección que proyecta sobre ese estado. En este caso, decimos que el estado es **puro**. Un estado puro representa la cantidad máxima de conocimiento que Beto puede tener de un sistema cuántico. Pero en el caso más general, la matriz densidad es una mezcla de varios operadores de proyección. Entonces decimos que la matriz densidad representa un **estado mezcla**.

He utilizado el término matriz densidad, pero estrictamente hablando, $\rho$ es un operador. Solo se convierte en una matriz cuando se elige una base. Supongamos que elegimos la base $|a\rangle$. La matriz densidad es simplemente la representación matricial de $\rho$ con respecto a esta base:

$$\rho_{aa'} = \langle a|\rho|a'\rangle.$$

Si la representación matricial de $\mathbf{L}$ es $L_{a',a}$, entonces 7.13 toma la forma

$$\langle \mathbf{L} \rangle = \sum_{a,a'} L_{a',a} \rho_{a,a'}. \quad (7.14)$$

### 7.4 Entrelazamiento y Matrices Densidad

La física clásica también tiene su noción de estados puros y mezcla, aunque no se llaman con esos nombres. Solo para ilustrar, consideremos un sistema de dos partículas moviéndose a lo largo de una línea. Según las reglas de la mecánica clásica, podemos calcular las órbitas de las partículas si conocemos los valores de sus posiciones ($x_1$ y $x_2$) y momentos ($p_1$ y $p_2$) en un cierto instante de tiempo. El estado del sistema se especifica así mediante cuatro números: $x_1, x_2, p_1,$ y $p_2$. Si conocemos estos cuatro números, tenemos una descripción tan completa del sistema de dos partículas como es posible tener: no hay más que saber. Podemos llamar a esto un estado clásico puro.

  22 

7.4. ENTRELAZAMIENTO Y MATRICES DENSIDAD 199

A menudo, sin embargo, no conocemos el estado exacto, sino solo alguna información probabilística. Esa información puede codificarse en una densidad de probabilidad

$$\rho(x_1, x_2, p_1, p_2).$$

Un estado clásico puro es solo un caso especial de una densidad de probabilidad, en la que $\rho$ es distinta de cero en un solo punto. Pero más generalmente, $\rho$ estará extendida, en cuyo caso podríamos llamarlo un estado clásico mezcla.$^5$ Cuando $\rho$ está extendida, significa que nuestro conocimiento del estado del sistema es incompleto. Cuanto más extendida esté, mayor es nuestra ignorancia.

Una cosa debería ser completamente obvia a partir de este ejemplo: si conoces el estado puro para el sistema combinado de dos partículas, entonces conoces todo sobre cada partícula. En otras palabras, un estado puro para dos partículas clásicas implica un estado puro para cada una de las partículas individuales.

Pero esto es exactamente lo que **no** es cierto en mecánica cuántica cuando un sistema está entrelazado. El estado de un sistema compuesto puede ser absolutamente puro, pero cada uno de sus constituyentes debe describirse mediante un estado mezcla.

Tomemos un sistema compuesto por dos partes, A y B. Podrían ser dos espines o cualquier otro sistema compuesto.

En este caso, supondremos que Alicia tiene un conocimiento completo del estado del sistema combinado. En otras palabras, conoce la función de onda

$$\Psi(a, b).$$

$^5$Por "extendida" queremos decir que $\rho(x_1, x_2, p_1, p_2)$ será distinta de cero para un rango de valores de sus argumentos, no solo un valor. Cuanto mayor sea este rango, más extendida se vuelve $\rho$.

  22 

200 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

No falta nada en su conocimiento del sistema combinado. Sin embargo, Alicia no está interesada en B. En cambio, desea averiguar todo lo que pueda sobre A sin mirar a B. Selecciona un observable $\mathbf{L}$ que pertenece a A, y que no hace nada a B cuando actúa. La regla para calcular el valor esperado de $\mathbf{L}$ es

$$\langle \mathbf{L} \rangle = \sum_{ab, a'b'} \Psi^*(a'b') L_{a'b',ab} \Psi(ab). \quad (7.15)$$

Hasta ahora, esto es completamente general. Sin embargo, si el observable $\mathbf{L}$ está asociado solo con A, entonces actúa trivialmente sobre el índice $b$ y podemos escribir el valor esperado como

$$\langle \mathbf{L} \rangle = \sum_{a,b,a'} \Psi^*(a'b) L_{a',a} \Psi(ab). \quad (7.16)$$

Ahora, Alicia puede resumir todo su conocimiento, al menos para el propósito de estudiar A, en términos de una matriz $\rho$:

$$\rho_{aa'} = \sum_b \Psi^*(a'b) \Psi(ab). \quad (7.17)$$

Sorprendentemente, la Ec. 7.16 tiene exactamente la misma forma que la Ec. 7.14 para el valor esperado de un estado mezcla. De hecho, solo en el caso muy especial de un estado producto tendrá $\rho$ la forma de un operador de proyección. En otras palabras, a pesar de que el sistema compuesto se describe mediante un estado perfectamente puro, el subsistema A debe describirse mediante un estado mezcla.

Hay un punto sutil sobre nuestra notación para matrices densidad que vale la pena notar: en la Ec. 7.17, el índice derecho de $\rho$, es decir, el índice $a'$, corresponde al vector de estado conjugado complejo $\Psi^*(a'b)$ en la suma. Esto es una consecuencia de nuestra convención

$$L_{aa'} = \langle a|\mathbf{L}|a'\rangle$$

  22 

7.5. ENTRELAZAMIENTO PARA DOS ESPINES 201

para etiquetar los elementos de matriz de un operador $\mathbf{L}$. Aplicando esta convención a

$$\rho = |\Psi\rangle \langle \Psi|$$

resulta en

$$\rho_{aa'} = \langle a|\Psi\rangle \langle \Psi|a'\rangle,$$

o

$$\rho_{aa'} = \Psi(a) \Psi^*(a').$$

### 7.5 Entrelazamiento para Dos Espines

Antes de adentrarte más en el mundo del entrelazamiento, te daré una definición simple y un ejercicio rápido de calentamiento.

Si Alicia solo tiene un solo espín en un estado conocido, su matriz densidad se define como

$$\rho_{aa'} = \psi^*(a') \psi(a).$$

Esta ecuación te dice cómo calcular un elemento de la matriz densidad de Alicia. Si nos limitamos a nuestra familiar base de $\sigma_z$, cada índice $a$ y $a'$ puede tomar los valores arriba y abajo, por lo que Alicia tiene una matriz densidad de $2 \times 2$.

  22 

202 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

**Ejercicio 7.4:** Calcula la matriz densidad para

$$|\Psi\rangle = \alpha|u\rangle + \beta|d\rangle.$$

Respuesta:

$$\psi(u) = \alpha; \quad \psi^*(u) = \alpha^*$$
$$\psi(d) = \beta; \quad \psi^*(d) = \beta^*$$

$$\rho_{a'a} =
\begin{pmatrix}
\alpha^*\alpha & \alpha^*\beta \\
\beta^*\alpha & \beta^*\beta
\end{pmatrix}.$$

Ahora intenta insertar algunos números para $\alpha$ y $\beta$. Asegúrate de que estén normalizados a 1. Por ejemplo, $\alpha = \frac{1}{\sqrt{2}}, \beta = \frac{1}{\sqrt{2}}$. Este ejemplo simple es una buena manera de entender las propiedades de las matrices densidad. Puedes consultarlo más adelante cuando analicemos el ejemplo más complejo de un estado entrelazado.

Supongamos que conocemos la función de onda de un sistema compuesto, por ejemplo

$$\psi(a, b),$$

pero solo estamos interesados en el subsistema de Alicia. En otras palabras, queremos mantener un registro de todo lo que Alicia puede medir. ¿Tenemos que conocer toda la función de onda? ¿O hay alguna manera de deshacernos de las variables de Beto?

La respuesta a esta última pregunta es sí; podemos capturar la descripción completa de Alicia en términos de una matriz densidad $\rho$.

Consideremos un observable $\mathbf{L}$ del sistema de Alicia. Como cualquier observable, puede representarse como una matriz:

  22 

7.5. ENTRELAZAMIENTO PARA DOS ESPINES 203

$$L_{a'b', ab} = \langle a'b'|\mathbf{L}|ab\rangle.$$

Recuerda, para el sistema compuesto, el par $ab$ es realmente un solo índice que etiqueta un vector base.

Cuando decimos "$\mathbf{L}$ es un observable de Alicia", lo que queremos decir es que $\mathbf{L}$ no hace nada a la mitad de Beto de la etiqueta de estado. Esto impone algunas restricciones sobre la forma de $\mathbf{L}$. La idea es filtrar (igualar a cero) cualquier elemento de matriz de $\mathbf{L}$ que tenga el efecto de cambiar la mitad de Beto de la etiqueta de estado. En otras palabras, $\mathbf{L}$ tiene la forma especial

$$L_{a'b', ab} = L_{a'a} \delta_{b'b}. \quad (7.18)$$

Esta ecuación de aspecto simple requiere alguna explicación, y es posible que desees revisar el material sobre productos tensoriales en forma de componentes, en el Interludio sobre productos tensoriales (Sección 6.1). El lado izquierdo de la ecuación es un elemento de una matriz $4 \times 4$. Cada uno de sus dos índices puede tomar cuatro valores distintos: $uu, ud, du,$ o $dd$. ¿Qué hay del lado derecho? El elemento de matriz $L_{a'a}$ también tiene dos índices, pero cada uno de ellos puede tomar solo dos valores distintos: $u$ o $d$. De hecho, el mismo símbolo $\mathbf{L}$ se refiere a dos matrices diferentes en cada lado de la Ec. 7.18.

A primera vista, parece que hemos igualado una matriz $4 \times 4$ a una matriz $2 \times 2$, y ciertamente eso sería un problema. Sin embargo, el factor $\delta_{b'b}$ hace que todo funcione. El término $L_{a'a} \delta_{b'b}$ es un elemento del producto tensorial de dos matrices $2 \times 2$, y ese producto tensorial es una matriz $4 \times 4$.$^6$

$^6$También podríamos llamarlo producto de Kronecker, ya que estamos hablando de matrices. La distinción formal no es importante para nuestros propósitos.

  22 

204 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

Aquí está la forma de leer la Ec. 7.18:

La matriz $4 \times 4$ $L_{a'b', ab}$ puede factorizarse como un producto tensorial de las dos matrices $2 \times 2$ $L_{a'a}$ y $\delta_{b'b}$, donde $\delta_{b'b}$ es equivalente a la matriz identidad $2 \times 2$.

Ahora, calculemos el valor esperado de $\mathbf{L}$ (la versión $4 \times 4$) utilizando todo el aparato del sistema compuesto:

$$\langle \Psi|\mathbf{L}|\Psi\rangle = \sum_{a,b,a',b'} \psi^*(a', b') L_{a'b',ab} \psi(a, b).$$

Como advertí, hay muchos índices. Pero se simplifica si usamos la forma especial de la matriz $\mathbf{L}$. El factor $\delta_{b'b}$ en la Ec. 7.18 —una delta de Kronecker— filtra cualquier elemento que cambie la mitad de Beto de la etiqueta, y deja intactos los demás. Nos dice que establezcamos $b' = b$ para obtener

$$\langle \Psi|\mathbf{L}|\Psi\rangle = \sum_{a',b,a} \psi^*(a', b) L_{a',a} \psi(a, b). \quad (7.19)$$

Por el momento, ignoremos las sumas sobre $a$ y $a'$, y concentrémonos en cambio en la suma sobre $b$. Encontramos la cantidad

$$\rho_{a'a} = \sum_b \psi^*(a, b) \psi(a', b). \quad (7.20)$$

La matriz $2 \times 2$ $\rho_{a'a}$ es la **matriz densidad de Alicia**. Observa que $\rho_{a'a}$ no depende de ningún índice $b$ ya que ha sido

  22 

7.5. ENTRELAZAMIENTO PARA DOS ESPINES 205

sumado sobre $b$. Es puramente una función de las variables de Alicia $a$ y $a'$. De hecho, solo mantuvimos las $b$ en la ecuación para hacer más fácil de seguir el ejemplo en la próxima sección.

Podemos simplificar la Ec. 7.19 insertando $\rho_{a'a}$ de la Ec. 7.20. El valor esperado de $\mathbf{L}$ (la versión $2 \times 2$) se convierte entonces en

$$\langle \mathbf{L} \rangle = \sum_{a'a} \rho_{a'a} L_{a,a'}. \quad (7.21)$$

Al sumar sobre $b$, hemos colapsado una matriz $4 \times 4$ en una matriz $2 \times 2$. Esto tiene sentido. Esperamos que un operador que actúa sobre el sistema compuesto sea una matriz $4 \times 4$, y esperamos que un operador de Alicia sea $2 \times 2$.

Observa que el lado derecho de la Ec. 7.21 es una suma de elementos diagonales de la matriz. En otras palabras, es la traza de la matriz $\rho \mathbf{L}$, que podemos escribir como

$$\langle \mathbf{L} \rangle = \text{Tr} \, \rho \mathbf{L}.$$

La lección es esta: Para calcular la matriz densidad $\rho$ de Alicia, podemos necesitar conocer la función de onda completa, incluyendo la dependencia de las variables de Beto. Pero una vez que conocemos $\rho$, podemos olvidar de dónde vino y usarla para calcular cualquier cosa sobre las observaciones de Alicia. Como ejemplo simple, podemos usar $\rho$ para calcular la probabilidad $P(a)$ de que el sistema de Alicia quede en el estado $a$ si se realiza una medición.

Para determinar $P(a)$, comenzamos con $P(a, b)$, la probabilidad de que el sistema combinado esté en el estado $|ab\rangle$. Eso es simplemente

$$P(a, b) = \psi^*(a, b) \psi(a, b).$$

  22 

206 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

Por las reglas estándar de la probabilidad, si sumamos sobre $b$, obtenemos la probabilidad para $a$:

$$P(a) = \sum_b \psi^*(a, b) \psi(a, b).$$

Esta es precisamente una entrada diagonal en la matriz densidad:

$$P(a) = \rho_{aa}. \quad (7.22)$$

Aquí hay algunas propiedades de las matrices densidad:

* Las matrices densidad son hermíticas:
  $$\rho_{aa'} = \rho^*_{a'a}.$$
* La traza de una matriz densidad es 1:
  $$\text{Tr}(\rho) = 1.$$
  La Ec. 7.22 debería ayudar a aclarar esto porque el lado izquierdo es una probabilidad.
* Los valores propios de la matriz densidad son todos positivos y se encuentran entre 0 y 1. Se sigue que si algún valor propio es 1, todos los demás son 0. ¿Puedes interpretar este resultado?
* Para un estado puro:
  $$\rho^2 = \rho$$
  $$\text{Tr}(\rho^2) = 1$$

  22 

7.5. ENTRELAZAMIENTO PARA DOS ESPINES 207

* Para un estado mezcla o entrelazado:
  $$\rho^2 \neq \rho$$
  $$\text{Tr}(\rho^2) < 1$$

Las dos últimas propiedades nos dan una forma clara de distinguir matemáticamente entre estados puros y estados mezcla. Un subsistema de un estado entrelazado (como la mitad de Alicia del estado singlete) se considera un estado mezcla.

Vale la pena tomarse un momento para entender estas dos propiedades un poco mejor. Para simplificar las cosas, asumiremos que $\rho$ es una matriz diagonal —en otras palabras, todos sus elementos fuera de la diagonal son cero. Esta simplificación no nos cuesta nada porque $\rho$ es hermítica, y resulta que toda matriz hermítica puede expresarse en forma diagonal en alguna base.$^7$

Elevar al cuadrado una matriz diagonal es bastante simple: todo lo que necesitas hacer es elevar al cuadrado cada elemento individual. Dado que $\rho$ representa un estado mezcla, y los elementos diagonales de $\rho$ deben sumar 1, ninguno de los elementos diagonales de $\rho$ puede ser igual a 1. De lo contrario, $\rho$ representaría un estado puro. Por lo tanto, $\rho$ debe tener al menos dos elementos diagonales positivos que sean menores que 1. Elevar al cuadrado estos elementos da una nueva matriz $\rho^2$ cuyos elementos son aún más pequeños. Esto explica ambas propiedades del estado mezcla.

Antes de que intentes los siguientes ejercicios, mencionaré una cosa más sobre la traza. Resulta que la traza tiene muchas

$^7$Como mencionamos anteriormente, en la Sección 7.2, una matriz hermítica $\mathbf{M}$ puede diagonalizarse mediante una transformación $\mathbf{P}^\dagger\mathbf{MP}$, donde $\mathbf{P}$ es una matriz unitaria cuyas columnas son los vectores propios normalizados de $\mathbf{M}$.

  22 

208 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

propiedades matemáticas interesantes. Una de sus propiedades más útiles es que la traza de un producto de dos matrices no depende del orden de multiplicación. En otras palabras,

$$\text{Tr} \, \mathbf{A}\mathbf{B} = \text{Tr} \, \mathbf{B}\mathbf{A},$$

incluso si

$$\mathbf{A}\mathbf{B} \neq \mathbf{B}\mathbf{A}.$$

Menciono esto porque a veces verás la traza de la matriz densidad escrita como $\text{Tr} \, \mathbf{L}\rho$, en lugar de $\text{Tr} \, \rho\mathbf{L}$. Estas dos expresiones son equivalentes.

**Ejercicio 7.5:**

a) Muestra que
   $$\begin{pmatrix} a & 0 \\ 0 & b \end{pmatrix}^2 = \begin{pmatrix} a^2 & 0 \\ 0 & b^2 \end{pmatrix}.$$

b) Ahora, supongamos
   $$\rho = \begin{pmatrix} \frac{1}{3} & 0 \\ 0 & \frac{2}{3} \end{pmatrix}.$$
   Calcula
   $$\rho^2$$
   $$\text{Tr}(\rho)$$
   $$\text{Tr}(\rho^2).$$

c) Si $\rho$ es una matriz densidad, ¿representa un estado puro o un estado mezcla?

  23 

7.6. CÁLCULO DE LA MATRIZ DENSIDAD DE ALICIA 209

**Ejercicio 7.6:** Usa la Ec. 7.22 para mostrar que si $\rho$ es una matriz densidad, entonces

$$\text{Tr}(\rho) = 1.$$

### 7.6 Un Ejemplo Concreto: Cálculo de la Matriz Densidad de Alicia

Hasta ahora, la discusión sobre matrices densidad puede haber sido un poco abstracta para algunos lectores. Aquí hay un ejemplo resuelto que debería ayudar a enfocar mejor las matrices densidad. Recordemos la definición de la matriz densidad de Alicia de la Ec. 7.20:

$$\rho_{a'a} = \sum_b \psi^*(a, b) \psi(a', b). \quad (7.23)$$

Ahora, considera el vector de estado

$$|\Psi\rangle = \frac{1}{\sqrt{2}} \left( |ud\rangle + |du\rangle \right).$$

Observa que dos de los vectores base tienen un coeficiente de $\frac{1}{\sqrt{2}}$, mientras que los otros dos tienen coeficientes de cero. El estado está normalizado porque la suma de los coeficientes al cuadrado es 1. Además, los cuatro coeficientes resultan ser reales, lo que simplifica el proceso de conjugación compleja.

  23 

210 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

Calculemos la matriz densidad de Alicia para este estado. Primero, para todas las entradas posibles $a$ y $b$, listaremos los valores de $\psi(a, b)$. Recordemos que estos son solo los coeficientes de los vectores base:

$$\psi(u, u) = 0$$
$$\psi(u, d) = \frac{1}{\sqrt{2}}$$
$$\psi(d, u) = \frac{1}{\sqrt{2}}$$
$$\psi(d, d) = 0.$$

A continuación, usaremos estas cuatro ecuaciones para calcular cada elemento de la matriz densidad de Alicia expandiendo la suma de la Ec. 7.23. En la expansión, observa que para cada factor de la forma $\psi^*(a, b)\psi(a', b)$, la entrada de Beto es la misma para ambos factores. Descartamos cualquier término que no tenga esta propiedad. Esto es lo que queremos decir con "igualar $b'$ a $b$ en la suma".

Aquí está la expansión:

$$\rho_{uu} = \psi^*(u, u)\psi(u, u) + \psi^*(u, d)\psi(u, d) = \frac{1}{2}$$
$$\rho_{ud} = \psi^*(u, u)\psi(d, u) + \psi^*(u, d)\psi(d, d) = 0$$
$$\rho_{du} = \psi^*(d, u)\psi(u, u) + \psi^*(d, d)\psi(u, d) = 0$$
$$\rho_{dd} = \psi^*(d, u)\psi(d, u) + \psi^*(d, d)\psi(d, d) = \frac{1}{2}.$$

Estos valores son los elementos de una matriz $2 \times 2$:

  23 

7.6. CÁLCULO DE LA MATRIZ DENSIDAD DE ALICIA 211

$$\rho = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{2} \end{pmatrix}. \quad (7.24)$$

La traza de nuestra matriz es 1. Y nuestra matriz densidad está lista.$^8$

**Ejercicio 7.7:** Usa la Ec. 7.24 para calcular $\rho^2$. ¿Cómo confirma este resultado que $\rho$ representa un estado entrelazado? Pronto descubriremos que hay otras formas de verificar el entrelazamiento.

**Ejercicio 7.8:** Considera los siguientes estados:

$$|\psi_1\rangle = \frac{1}{2} \left( |uu\rangle + |ud\rangle + |du\rangle + |dd\rangle \right)$$
$$|\psi_2\rangle = \frac{1}{\sqrt{2}} \left( |uu\rangle + |dd\rangle \right)$$
$$|\psi_3\rangle = \frac{1}{5} \left( 3|uu\rangle + 4|ud\rangle \right).$$

Para cada uno, calcula la matriz densidad de Alicia y la matriz densidad de Beto. Verifica sus propiedades.

$^8$Art es poeta, y ni siquiera es consciente de ello.

  23 

212 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

### 7.7 Pruebas de Entrelazamiento

Supongamos que te doy una función de onda

$$\psi(a, b)$$

para el sistema compuesto $S_{AB}$. ¿Cómo podrías saber si el estado correspondiente está entrelazado?

No me refiero a una prueba experimental sino a un procedimiento matemático. Una pregunta relacionada es si existen diferentes grados de entrelazamiento. Si los hay, ¿cómo podrías cuantificarlos?

El entrelazamiento es la generalización mecánico-cuántica de la correlación. En otras palabras, indica que Alicia puede aprender algo sobre la mitad de Beto del sistema midiendo la suya propia. En el ejemplo clásico de la lección anterior, ilustré la idea de correlación usando monedas. Si Alicia observa la moneda que Carlos le dio, no solo sabe si su propia moneda es de diez o veinticinco centavos; también sabe qué moneda tiene Beto. Esa es la imagen experimental. La indicación matemática de la correlación es que la función de probabilidad $P(a, b)$ no se factoriza (es decir, no se ve como la Ec. 6.3).

Siempre que la distribución de probabilidad no se factorice, hay correlaciones no nulas como las describí en la Desigualdad 6.2.

  23 

7.7. PRUEBAS DE ENTRELAZAMIENTO 213

#### 7.7.1 La Prueba de Correlación para el Entrelazamiento

Supongamos que $A$ es un observable de Alicia y $B$ es un observable de Beto. La correlación entre ellos se define en términos de los valores promedio (también conocidos como valores esperados) de los observables individuales, y de su producto. Supongamos que

$$\langle A \rangle$$
$$\langle B \rangle$$
$$\langle AB \rangle$$

son estos valores esperados. La correlación $C(A, B)$ entre $A$ y $B$ se define como

$$C(A, B) = \langle AB \rangle - \langle A \rangle \langle B \rangle.$$

**Ejercicio 7.9:** Dado cualquier observable $A$ de Alicia y cualquier observable $B$ de Beto, muestra que para un estado producto, la correlación $C(A, B)$ es cero.

A partir de este ejercicio, podemos aprender algo sobre el entrelazamiento. Si un sistema está en un estado donde se pueden encontrar dos observables cualesquiera $A$ y $B$ que estén correlacionados —es decir, que $C(A, B) \neq 0$— entonces el estado está entrelazado. Las correlaciones se definen para estar en el rango de $-1$ a $+1$. Estos valores extremos representan las mayores correlaciones negativas y positivas posibles. Cuanto mayor sea la magnitud de $C(A, B)$, más entrelazado está el estado.

Si $C(A, B) = 0$, entonces no hay correlación (y no hay entrelazamiento) en absoluto.

  23 

214 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

#### 7.7.2 La Prueba de la Matriz Densidad para el Entrelazamiento

Para calcular correlaciones, tienes que conocer tanto la parte de Beto como la parte de Alicia del sistema, junto con la función de onda del sistema. Pero hay otra prueba para el entrelazamiento que solo requiere que conozcamos la matriz densidad de Alicia (o de Beto). Supongamos que el estado $|\Psi\rangle$ es un estado producto de un factor de Beto $|\varphi\rangle$ y un factor de Alicia $|\psi\rangle$. Eso significa que la función de onda compuesta es también el producto de un factor de Beto y un factor de Alicia:

$$\psi(a, b) = \psi(a) \varphi(b).$$

Ahora, calculemos la matriz densidad de Alicia. Usamos la definición en la Ec. 7.20 para obtener

$$\rho_{a'a} = \psi^*(a) \psi(a') \sum_b \varphi^*(b) \varphi(b).$$

Pero si el estado de Beto está normalizado, entonces

$$\sum_b \varphi^*(b) \varphi(b) = 1,$$

lo que hace que la matriz densidad de Alicia sea particularmente simple:

$$\rho_{a'a} = \psi^*(a) \psi(a'). \quad (7.25)$$

Observa que solo depende de las variables de Alicia. Quizás no es muy sorprendente que todo lo que necesitamos saber sobre el sistema de Alicia esté contenido en la función de onda de Alicia.

Ahora, voy a demostrar un teorema clave sobre los valores propios de la matriz densidad de Alicia, bajo la suposición de un estado producto. Es cierto solo para estados no entrelazados y sirve para identificarlos. El teorema dice que para cualquier estado producto, la matriz densidad de Alicia (o de Beto) tiene exactamente un

  23 

7.7. PRUEBAS DE ENTRELAZAMIENTO 215

valor propio distinto de cero, y ese valor propio es exactamente 1. Comenzamos el teorema escribiendo la ecuación de valores propios para la matriz $\rho$:

$$\sum_{a'} \rho_{a'a} \alpha_{a'} = \lambda \alpha_a.$$

En otras palabras, la matriz $\rho$ actuando sobre el vector columna $\alpha$ devuelve el mismo vector multiplicado por un valor propio $\lambda$. Usando la forma simple de $\rho$ en la Ec. 7.25, podemos escribir

$$\psi(a') \sum_a \psi^*(a) \alpha_a = \lambda \alpha_{a'}. \quad (7.26)$$

Ahora, puedes notar un par de cosas. Primero, la cantidad

$$\sum_a \psi^*(a) \alpha_a$$

tiene la forma de un producto interno. Si el vector columna $\alpha$ es ortogonal a $\psi$, entonces el lado izquierdo de la Ec. 7.26 es cero. Tal vector es un vector propio de $\rho$ con valor propio cero.

Si la dimensión del espacio de estados de Alicia es $N_A$, entonces hay $N_A - 1$ vectores ortogonales a $\psi$. Cada uno de ellos es un vector propio de $\rho$ con valor propio 0. Eso deja solo una dirección posible para un vector propio con un valor propio distinto de cero, a saber, el vector $\psi(a)$. De hecho, si insertamos $\alpha_a = \psi(a)$, encontramos que efectivamente es un vector propio de $\rho$ con valor propio 1.

Para resumir el teorema: Si el sistema compuesto Alicia-Beto está en un estado producto, entonces la matriz densidad de Alicia (o de Beto)

  23 

216 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

tiene uno y solo un valor propio igual a 1, y todos los demás son cero. Además, el vector propio con un valor propio distinto de cero no es más que la función de onda de la mitad de Alicia del sistema.

En esta situación, el sistema de Alicia está en un estado puro. Todas las observaciones de Alicia se describen como si Beto y su sistema nunca hubieran existido y Alicia tuviera un sistema aislado descrito por la función de onda $\psi(a')$.

El extremo opuesto de un estado puro es un estado **máximamente entrelazado**. Los estados máximamente entrelazados son estados de un sistema combinado en los que no se sabe nada sobre ninguno de los subsistemas, a pesar de que son descripciones completas del sistema en su conjunto —tan completas como la mecánica cuántica lo permite. El estado $|sing\rangle$ es un estado máximamente entrelazado.

Cuando Alicia calcula su matriz densidad para un estado máximamente entrelazado, encuentra algo muy decepcionante: la matriz densidad es proporcional a la matriz unitaria. Todos los valores propios son iguales, y dado que todos suman la unidad, cada valor propio es igual a $1/N_A$. En otras palabras,

$$\rho_{a'a} = \frac{1}{N_A} \delta_{a'a}. \quad (7.27)$$

¿Por qué está decepcionada Alicia? Vuelve a la Ec. 7.22. Esta ecuación dice que la probabilidad de un estado particular $a$ es el elemento diagonal de $\rho$, pero la Ec. 7.27 nos dice que todas las probabilidades son iguales. ¿Qué podría ser menos informativo que una distribución de probabilidad tan carente de estructura que cada resultado posible es igualmente probable?

  23 

7.8. EL PROCESO DE MEDICIÓN 217

El entrelazamiento máximo implica una completa falta de información sobre el subsistema de Alicia para experimentos que solo involucran ese subsistema. Por otro lado, implica una gran correlación entre las mediciones de Alicia y Beto. Para el estado singlete, si Alicia mide cualquier componente de su espín, automáticamente sabe el resultado que Beto obtendría si él midiera la misma componente de su espín. Este es exactamente el tipo de conocimiento que está excluido en un estado producto.

Así que en cada tipo de estado, algunas cosas son predecibles y otras no. En un estado producto, podemos hacer predicciones estadísticas sobre las mediciones realizadas en cada subsistema por separado, pero las mediciones de Alicia no le dicen nada sobre el sistema de Beto. En un estado máximamente entrelazado, por otro lado, Alicia no puede predecir nada sobre sus propias mediciones, pero sabe mucho sobre la relación entre sus resultados y los de Beto.

### 7.8 El Proceso de Medición

Hemos visto que los sistemas cuánticos evolucionan de maneras que parecen irreconciliablemente diferentes: mediante evolución unitaria entre mediciones, y mediante colapso de la función de onda cuando tienen lugar las mediciones. Esta circunstancia ha llevado a algunos de los debates más polémicos y afirmaciones confusas sobre la llamada realidad. Voy a alejarme de esos debates y ceñirme a los hechos. Una vez que sepas cómo funciona la mecánica cuántica, puedes decidir por ti mismo si crees que hay un problema.

Comencemos notando que cada medición involucra

  23 

218 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

un sistema y un aparato. Pero si la mecánica cuántica es una teoría consistente, entonces debería ser posible combinar el sistema y el aparato en un único sistema más grande. Para simplificar, tomemos el sistema como un solo espín. El aparato $\mathcal{A}$ es el mismo que usamos en la primera lección. La ventana del aparato puede mostrar tres lecturas posibles. La primera está en blanco —representa el estado neutral del aparato antes de que entre en contacto con el espín. Las otras dos lecturas registran los dos resultados posibles de la medición: $+1$ o $-1$.

Si el aparato es un sistema cuántico (por supuesto, debe serlo), entonces se describe mediante un espacio de estados. En la descripción más simple, el aparato tiene exactamente tres estados: un estado en blanco y dos estados de resultado. Por lo tanto, los vectores base para el aparato son

$$|b\rangle$$
$$|+1\rangle$$
$$|-1\rangle.$$

Mientras tanto, los estados base del espín pueden ser los estados habituales arriba y abajo:

$$|u\rangle$$
$$|d\rangle.$$

A partir de estos dos conjuntos de vectores base, podemos construir un espacio de estados compuesto (producto tensorial) que tiene los seis vectores base

  24 

7.8. EL PROCESO DE MEDICIÓN 219

$$|u, b\rangle$$
$$|u, +1\rangle$$
$$|u, -1\rangle$$
$$|d, b\rangle$$
$$|d, +1\rangle$$
$$|d, -1\rangle.$$

La mecánica detallada de lo que sucede cuando el sistema se encuentra con el aparato puede ser complicada, pero somos libres de hacer algunas suposiciones sobre cómo evoluciona el sistema combinado. Supongamos que el aparato comienza en el estado en blanco y el espín comienza en el estado arriba. Después de que el aparato interactúa con el espín, el estado final (por suposición) es

$$|u, +1\rangle.$$

En otras palabras, la interacción deja el espín sin cambios pero cambia el aparato al estado $+1$. Escribimos esto como

$$|u, b\rangle \rightarrow |u, +1\rangle. \quad (7.28)$$

De manera similar, podemos requerir que si el espín está en el estado abajo, cambie el aparato al estado $-1$:

$$|d, b\rangle \rightarrow |d, -1\rangle. \quad (7.29)$$

  24 

220 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

Por lo tanto, al mirar el aparato después de que interactúa con el espín, puedes saber cuál era el espín inicialmente.

Ahora, supongamos que el estado inicial del espín es más general, a saber

$$\alpha_u|u\rangle + \alpha_d|d\rangle.$$

Si incluimos el aparato como parte del sistema, el estado inicial es

$$\alpha_u|u, b\rangle + \alpha_d|d, b\rangle. \quad (7.30)$$

Este estado inicial es un estado producto, específicamente un producto del estado inicial del espín y el estado en blanco del aparato. Puedes comprobar que está completamente no entrelazado.

**Ejercicio 7.10:** Verifica que el vector de estado en 7.30 representa un estado completamente no entrelazado.

Debido a que sabemos por las Ecs. 7.28 y 7.29 cómo evolucionan los términos individuales en 7.30, podemos determinar fácilmente el estado final:

$$\alpha_u|u, b\rangle + \alpha_d|d, b\rangle \rightarrow \alpha_u|u, +1\rangle + \alpha_d|d, -1\rangle.$$

Este estado final es un estado entrelazado. De hecho, si $\alpha_u = -\alpha_d$, es el estado singlete máximamente entrelazado. Efectivamente, se puede mirar el aparato e inmediatamente deducir cuál es el estado del espín: si el aparato lee $+1$, el espín está arriba, y si lee $-1$, el espín está abajo. Además, la probabilidad de que el aparato final muestre $+1$ es

  24 
<!--SR:!2000-01-01,1,250!2026-02-15,1,230-->

7.8. EL PROCESO DE MEDICIÓN 221

$$\alpha_u^* \alpha_u.$$

Este número representa una probabilidad —es exactamente la misma que la probabilidad original de que el espín estuviera arriba. En esta descripción de una medición, no ocurre ningún colapso de la función de onda. En cambio, el entrelazamiento entre el aparato y el sistema simplemente ocurre mediante la evolución unitaria del vector de estado.

El único problema es que, en cierto sentido, solo hemos retrasado la dificultad. No es muy satisfactorio que se nos diga que el aparato "sabe" el estado del espín a menos que se permita al experimentador —digamos Alicia— mirar el aparato. ¿No es cierto que cuando ella lo hace, colapsará la función de onda del sistema compuesto? Sí y no. Para todos los propósitos de Alicia, sí; ella concluirá que el aparato, y el espín, están en una de las dos configuraciones posibles y procederá en consecuencia.

Pero ahora incorporemos a Beto en la imagen. Hasta ahora, no ha interactuado con el espín, el aparato o Alicia. Desde su punto de vista, los tres forman un único sistema cuántico. No ocurrió ningún colapso de la función de onda cuando Alicia miró el aparato. En cambio, Beto dice que Alicia se entrelazó con los otros dos sistemas componentes.

Todo esto está muy bien, pero ¿qué sucede cuando Beto mira a Alicia? Para sus propósitos, él ha colapsado la función de onda. Pero entonces está el buen viejo Carlos...

¿El último ente en mirar el sistema colapsa la función de onda, o solo se entrelaza? ¿O hay

  24 

222 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

un último observador? No intentaré responder estas preguntas, pero lo que debería ser evidente es que la mecánica cuántica es un cálculo de probabilidades consistente para un cierto tipo de experimento que involucra un sistema y un aparato. Lo usamos, y funciona, pero cuando tratamos de hacer preguntas sobre la "realidad" subyacente, nos confundimos.

### 7.9 Entrelazamiento y Localidad

¿Viola la mecánica cuántica la localidad? Algunas personas creen que sí. Einstein se enfureció contra la "espeluznante acción a distancia" (*spooky action at a distance*) que, según él, estaba implicada por la mecánica cuántica. Y John Bell se convirtió en una figura casi de culto al demostrar que la mecánica cuántica es no local.

Por otro lado, la mayoría de los físicos teóricos, particularmente aquellos que estudian la teoría cuántica de campos, que está plagada de entrelazamiento, afirmarían lo contrario: la mecánica cuántica hecha correctamente asegura la localidad.

El problema, por supuesto, es que los dos grupos entienden cosas diferentes por localidad. Comencemos con la comprensión del término por parte del teórico de campos cuánticos. Desde este punto de vista, la localidad tiene un solo significado: es imposible enviar una señal más rápido que la velocidad de la luz. Te mostraré cómo la mecánica cuántica hace cumplir esta regla.

Primero, ampliemos la definición del sistema de Alicia y el sistema de Beto. Hasta ahora, he usado el término sistema de Alicia para significar algún sistema que Alicia lleva consigo y en el que puede hacer experimentos. Para el resto de esta sección, usaré el término para significar otra cosa: el sistema de Alicia consiste no solo en algún sistema que ella lleva, sino también en el aparato

  24 

7.9. ENTRELAZAMIENTO Y LOCALIDAD 223

que usa, e incluso ella misma. Lo mismo, por supuesto, se aplica al sistema de Beto. Los vectores ket base

$$|a\rangle$$

describen todo con lo que Alicia puede interactuar. Del mismo modo, los vectores ket

$$|b\rangle$$

describen todo con lo que Beto puede interactuar. Y los estados producto tensorial

$$|ab\rangle$$

describen la combinación de los mundos de Alicia y Beto.

Asumiremos que Alicia y Beto pueden haber estado lo suficientemente cerca como para interactuar en algún momento en el pasado, pero en el presente Alicia está en Alfa Centauri y Beto está en Palo Alto. La función de onda Alicia-Beto es

$$\psi(ab),$$

y puede estar entrelazada. La descripción completa de Alicia de su sistema, su aparato y ella misma está contenida en su matriz densidad $\rho$:

$$\rho_{aa'} = \sum_b \psi^*(a'b) \psi(ab). \quad (7.31)$$

  24 

224 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

Considera esta pregunta: ¿Puede Beto, desde su lado, hacer algo para cambiar instantáneamente la matriz densidad de Alicia? Ten en cuenta que Beto solo puede hacer cosas que las leyes de la mecánica cuántica permiten.

En particular, la evolución de Beto, sea cual sea su causa, debe ser unitaria. En otras palabras, debe describirse mediante una matriz unitaria

$$U_{bb'}.$$

La matriz $U$ representa lo que sea que le suceda al sistema de Beto, ya sea que Beto haga un experimento o no. Actúa sobre la función de onda para producir una nueva función de onda, que llamaremos la función de onda "final":

$$\psi_{\text{final}}(ab) = \sum_{b'} U_{bb'} \psi(ab').$$

También podemos escribir el complejo conjugado de esta función de onda:

$$\psi^*_{\text{final}}(a'b) = \sum_{b''} \psi^*(a'b'') U^\dagger_{b''b}.$$

Observa que agregamos primas a algunos de los símbolos para evitar mezclarlos en el siguiente paso. Ahora, calculemos la nueva matriz densidad de Alicia. Usaremos la Ec. 7.31, pero reemplazaremos las funciones de onda originales con las finales:

$$\rho_{aa'} = \sum_{b,b',b''} \psi^*(a'b'') U^\dagger_{b''b} U_{bb'} \psi(ab').$$

  24 

7.10. EL SIMULADOR CUÁNTICO: INTRO AL TEOREMA DE BELL 225

Hay muchos índices volando ahora, pero las matemáticas no son tan difíciles como parecen. De hecho, observa cómo las matrices $U$ entran a través de la combinación

$$U^\dagger_{b''b} U_{bb'}.$$

Esta combinación es solo el producto matricial $U^\dagger U$. Pero recuerda que $U$ es unitaria. Esto te dice que el producto $U^\dagger U$ es la matriz unidad $\delta_{b''b'}$. Como antes, esto equivale a una instrucción para incluir todos los términos donde $b'' = b'$, e ignorar todos los demás. Con esta simplificación, obtenemos

$$\rho_{aa'} = \sum_b \psi^*(a'b) \psi(ab).$$

Esto es exactamente lo mismo que la Ec. 7.31. En otras palabras, $\rho_{aa'}$ es exactamente la misma que era antes de que $U$ actuara. Nada de lo que sucede en el lado de Beto tiene ningún efecto inmediato sobre la matriz densidad de Alicia, incluso si Beto y Alicia están máximamente entrelazados. Esto significa que la visión de Alicia de su subsistema (su modelo estadístico) permanece exactamente como era. Este notable resultado puede parecer sorprendente para un sistema máximamente entrelazado, pero también garantiza que no se ha enviado ninguna señal más rápida que la luz.

### 7.10 El Simulador Cuántico: Una Introducción al Teorema de Bell

Es interesante que la unitariedad jugó un papel prominente en garantizar que ninguna señal pueda enviarse instantáneamente. Si $U$ no hubiera sido unitaria, la matriz densidad final de Alicia sí se habría visto afectada por Beto.

  24 

226 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

¿Qué fue entonces lo que perturbó tanto a Einstein que habló de una espeluznante acción a distancia? Para responder a esta pregunta, es importante entender que él y Bell estaban hablando de una noción totalmente diferente de localidad. Para ilustrar esto, voy a inventar un juego de ordenador. Lo que hace mi nuevo juego de ordenador es intentar engañarte para que pienses que hay un espín cuántico en un campo magnético dentro del ordenador. Tú puedes hacer experimentos para probar esta posibilidad. Ver Fig. 7.1 para un esquema.

Así es como funciona: Dentro del ordenador, la memoria almacena dos números complejos, $\alpha_u$ y $\alpha_d$, sujetos a la regla de normalización habitual,

$$\alpha_u^* \alpha_u + \alpha_d^* \alpha_d = 1.$$

Al comienzo del juego, los coeficientes $\alpha$ se inicializan con algún valor. El ordenador entonces resuelve la ecuación de Schrödinger para actualizar los $\alpha$ exactamente como si fueran los componentes del vector de estado del espín.

El ordenador también almacena la orientación tridimensional clásica del aparato en forma de dos ángulos o un

  24 

7.10. EL SIMULADOR CUÁNTICO: INTRO AL TEOREMA DE BELL 227

 Figura 7.1: Simulador Cuántico. La pantalla del ordenador muestra la orientación controlada por el usuario del aparato. Por simplicidad, solo se muestra la orientación bidimensional aquí. El usuario puede presionar el botón M cada vez que quiera medir el espín (no se muestra). Entre mediciones, el estado del espín evoluciona según la ecuación de Schrödinger. 

vector unitario. El teclado te permite establecer estos ángulos y cambiarlos a voluntad. Un elemento más se almacena en la memoria, a saber, el valor ($+1$ o $-1$) que representa el número en la ventana del aparato. La pantalla del ordenador muestra el aparato. Como experimentador, tú eliges cómo se orientará tu aparato. También hay

  24 

228 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

un botón de medir M que activa el aparato.

El elemento final del programa es un generador de números aleatorios que produce los resultados de medición $+1$ o $-1$ con probabilidades $\alpha_u^* \alpha_u$ y $\alpha_d^* \alpha_d$, respectivamente.

Ten en cuenta que los generadores de números aleatorios no son realmente generadores de números aleatorios; son simuladores de números aleatorios. Se basan en mecanismos deterministas completamente clásicos, utilizando cosas como los dígitos de $\pi$ para generar números. Sin embargo, son lo suficientemente buenos como para engañarte.

El juego comienza, y el ordenador actualiza continuamente los valores de $\alpha_u$ y $\alpha_d$. Esperas todo el tiempo que quieras y luego presionas el botón M. Entonces, con la ayuda del generador de números aleatorios, el juego produce un resultado que se muestra en la pantalla. Basándose en este resultado, el ordenador actualiza el estado mediante colapso. Si el resultado es $+1$, el valor de $\alpha_d$ se reinicia a cero, y el valor de $\alpha_u$ se reinicia a la unidad. Si el resultado es $-1$, el valor de $\alpha_d$ se reinicia a la unidad, y el valor de $\alpha_u$ se reinicia a cero. Luego, la ecuación de Schrödinger toma el control hasta que presiones M de nuevo.

Siendo un buen experimentador, haces muchas pruebas y recopilas estadísticas, que comparas con las predicciones de la mecánica cuántica. Si todo funciona correctamente, concluyes que la mecánica cuántica es la descripción correcta de lo que sea que esté sucediendo en el ordenador. Por supuesto, el ordenador sigue siendo completamente clásico, pero simula un espín cuántico sin mucha dificultad.

A continuación, intentemos lo mismo con dos ordenadores, A y B, simulando dos espines cuánticos. Si los espines comienzan en un estado producto y nunca interactúan, podemos simplemente jugar

  25 

7.10. EL SIMULADOR CUÁNTICO: INTRO AL TEOREMA DE BELL 229

el juego en cada uno de los dos ordenadores sin ningún cruce de información. Pero ahora, Alicia, Beto y Carlos regresan para ayudarnos. Carlos, por supuesto, quiere crear un par entrelazado. Comienza conectando los dos ordenadores con un cable para formar un solo ordenador, y asumimos que el cable puede enviar señales instantáneas. En su memoria, el ordenador combinado ahora almacena cuatro números complejos,

$$\alpha_{uu}, \alpha_{ud}, \alpha_{du}, \alpha_{dd},$$

y actualiza estos números usando la ecuación de Schrödinger. Cada pantalla de ordenador muestra un aparato. La pantalla de Alicia muestra A y la pantalla de Beto muestra B. Cada aparato virtual puede orientarse independientemente, y cada uno puede activarse independientemente con su propio botón M. Cuando se presiona cualquiera de los botones M, la memoria conjunta (con la ayuda del generador de números aleatorios) envía una señal al aparato correspondiente y produce un resultado.

¿Puede este dispositivo simular la mecánica cuántica del sistema de dos espines? Sí, puede —siempre que el cable que conecta los ordenadores no esté desconectado, y siempre que pueda enviar mensajes instantáneamente. Pero a menos que el sistema esté en un estado producto y permanezca en un estado producto, desconectar los dos ordenadores destruirá la simulación.

¿Podemos probar esto? De nuevo, la respuesta es sí—y ese es el contenido esencial del teorema de Bell. Cualquier simulación clásica de la mecánica cuántica que intente separar espacialmente los aparatos de Alicia y Beto debe tener un cable instantáneo que conecte los ordenadores separados con una memoria central que almacene y actualice el vector de estado.

  25 

230 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

Pero, ¿no significa esto que se puede enviar información violando la localidad a través del cable? Lo haría, si a Alicia, Beto y Carlos se les permitiera hacer cualquier cosa que los sistemas clásicos no relativistas pueden hacer.$^9$ Pero si las únicas operaciones que están permitidas son aquellas que simulan operaciones cuánticas, entonces la respuesta es no. Como hemos visto, la mecánica cuántica no permite que la matriz densidad de Alicia sea afectada por las acciones de Beto.

Este problema no es un problema para la mecánica cuántica. Es un problema para simular la mecánica cuántica con un ordenador booleano clásico. Ese es el contenido del teorema de Bell: Los ordenadores clásicos tienen que estar conectados con un cable instantáneo para simular el entrelazamiento.

### 7.11 Resumen del Entrelazamiento

De todas las ideas contraintuitivas que la mecánica cuántica nos impone, el entrelazamiento puede ser la más difícil de aceptar. No hay análogo clásico para un sistema cuya descripción completa del estado no contiene información sobre sus subcomponentes individuales. La no localidad es sorprendentemente difícil incluso de definir. La mejor manera de llegar a un acuerdo con estos problemas es internalizar las matemáticas. Lo que sigue es un resumen compacto de lo que hemos aprendido sobre el entrelazamiento. En particular, hemos tratado de mapear las diferencias entre estados entrelazados, no entrelazados y parcialmente entrelazados creando "hojas de antecedentes" para tres ejemplos específicos: el estado singlete, un estado producto y un estado "casi singlete". Esperamos que este

$^9$En otras palabras, sistemas que permiten enviar señales al instante.

  25 

7.11. RESUMEN DEL ENTRELAZAMIENTO 231

formato ayude a aclarar las similitudes y diferencias matemáticas. Por favor, tómate un tiempo para revisar este material y trabajar los ejercicios antes de continuar.

---

**Hoja de Antecedentes del Vector de Estado 1**

**Nombre:** Estado Producto (Sin Entrelazamiento)

**Buscado por:** Excesiva Localidad, Suplantación de Sistema Clásico

**Descripción:** Cada subsistema está completamente caracterizado. No hay correlaciones entre los sistemas de Alicia y Beto.

**Vector de Estado:** $\alpha_u\beta_u|uu\rangle + \alpha_u\beta_d|ud\rangle + \alpha_d\beta_u|du\rangle + \alpha_d\beta_d|dd\rangle$

**Normalización:** $\alpha_u^*\alpha_u + \alpha_d^*\alpha_d = 1$, $\beta_u^*\beta_u + \beta_d^*\beta_d = 1$

**Matriz Densidad:** La matriz densidad de Alicia tiene exactamente un valor propio distinto de cero, que es igual a 1. El vector propio con este valor propio distinto de cero es la función de onda del subsistema de Alicia. Lo mismo para Beto.

**Función de Onda:** Factorizada: $\psi(a)\varphi(b)$

**Valores Esperados:**
$$\langle \sigma_x \rangle^2 + \langle \sigma_y \rangle^2 + \langle \sigma_z \rangle^2 = 1$$
$$\langle \tau_x \rangle^2 + \langle \tau_y \rangle^2 + \langle \tau_z \rangle^2 = 1$$

**Correlación:** $\langle \sigma_z \tau_z \rangle - \langle \sigma_z \rangle \langle \tau_z \rangle = 0$

  25 

232 LECCIÓN 7. MÁS SOBRE ENTRELAZAMIENTO

---

**Hoja de Antecedentes del Vector de Estado 2**

**Nombre:** Estado Singlete (Máximo Entrelazamiento)

**Buscado por:** No localidad, Completa Rareza Cuántica

**Descripción:** El sistema compuesto en su conjunto está completamente caracterizado. No hay información sobre los subsistemas de Alicia o Beto.

**Vector de Estado:**
$$\frac{1}{\sqrt{2}} \left( |ud\rangle - |du\rangle \right)$$

**Normalización:** $\psi_{uu}^*\psi_{uu} + \psi_{ud}^*\psi_{ud} + \psi_{du}^*\psi_{du} + \psi_{dd}^*\psi_{dd} = 1$

**Matriz Densidad:**
- Sistema Compuesto Completo: $\rho^2 = \rho$, y $\text{Tr}(\rho^2) = 1$.
- Subsistema de Alicia: La matriz densidad es proporcional a la matriz unidad, con valores propios iguales que suman 1. Por lo tanto, cada resultado de medición es igualmente probable. $\rho^2 \neq \rho$, y $\text{Tr}(\rho^2) < 1$.

**Función de Onda:** No Factorizada: $\psi(a, b)$

**Valores Esperados:**
$$\langle \sigma_z \rangle, \langle \sigma_x \rangle, \langle \sigma_y \rangle = 0$$
$$\langle \tau_z \rangle, \langle \tau_x \rangle, \langle \tau_y \rangle = 0$$
$$\langle \tau_z \sigma_z \rangle, \langle \tau_x \sigma_x \rangle, \langle \tau_y \sigma_y \rangle = -1$$

**Correlación:** $\langle \sigma_z \tau_z \rangle - \langle \sigma_z \rangle \langle \tau_z \rangle = -1$

  25 

7.11. RESUMEN DEL ENTRELAZAMIENTO 233

---

**Hoja de Antecedentes del Vector de Estado 3**

**Nombre:** "Casi Singlete" (Entrelazamiento Parcial)

**Buscado por:** Indecisión, Vaguedad General, Problemas para distinguir arriba de abajo

**Descripción:** Hay algo de información sobre el sistema compuesto, y algo sobre cada subsistema. Incompleta en cada caso.

**Vector de Estado:**
$$\sqrt{0.6}|ud\rangle - \sqrt{0.4}|du\rangle$$

**Normalización:** $\psi_{uu}^*\psi_{uu} + \psi_{ud}^*\psi_{ud} + \psi_{du}^*\psi_{du} + \psi_{dd}^*\psi_{dd} = 1$

**Matriz Densidad:**
- Sistema Compuesto Completo: $\rho^2 \neq \rho$, y $\text{Tr}(\rho^2) < 1$.
- Subsistema de Alicia: $\rho^2 \neq \rho$, y $\text{Tr}(\rho^2) < 1$.

**Función de Onda:** No Factorizada: $\psi(a, b)$

**Valores Esperados:**
$$\langle \sigma_z \rangle = 0.2$$
$$\langle \sigma_x \rangle, \langle \sigma_y \rangle = 0; \quad \langle \tau_z \rangle = -0.2$$
$$\langle \tau_x \rangle, \langle \tau_y \rangle = 0$$
$$\langle \tau_z \sigma_z \rangle = -1$$
$$\langle \tau_x \sigma_x \rangle = -2\sqrt{0.24}$$

**Correlación:** $\langle \sigma_z \tau_z \rangle - \langle \sigma_z \rangle \langle \tau_z \rangle = -0.96$ para este ejemplo. Para estados parcialmente entrelazados en general, la correlación está entre $-1$ y $+1$, pero no exactamente 0.

**Ejercicio 7.11:** Calcula la matriz densidad de Alicia para $\sigma_z$ para el estado "casi singlete".

**Ejercicio 7.12:** Verifica los valores numéricos en cada hoja de antecedentes.

---

[Fin de la Parte 2/5. Continuará con Capítulo 8...]

---
[PARTE 3/5 - Capítulo 8]

---

  25 

# Lección 8

## Partículas y Ondas

Art y Lenny ya han tenido suficiente entrelazamiento por ahora. Están listos para algo más simple.

Lenny: Oye Hilbert, ¿tienes algo en una dimensión?

Hilbert: Déjame ver. Las dimensiones individuales son muy populares últimamente. A veces nos quedamos sin existencias.

Art: Me conformaría con algo clásico, si eso es todo lo que tienes.

Hilbert: No aquí, amigo. Perderíamos la licencia.

Art: Buen punto.

Para el ciudadano de a pie, la mecánica cuántica trata sobre la luz que son partículas y los electrones que son ondas. Pero hasta ahora, apenas he mencionado las partículas, y la única mención de las ondas ha sido la función de onda, que hasta ahora no ha tenido nada que ver con ondas. Entonces, ¿cuándo llegamos a la mecánica cuántica "real"?

  25 

236 LECCIÓN 8. PARTÍCULAS Y ONDAS

La respuesta, por supuesto, es que la mecánica cuántica real no trata tanto sobre partículas y ondas como sobre los principios lógicos no clásicos que gobiernan su comportamiento. La dualidad onda-partícula es una extensión fácil de las cosas que ya has aprendido, como veremos en esta lección. Pero antes de entrar en la física, quiero repasar algunas matemáticas, algunas de las cuales son antiguas —aparecieron en lecciones anteriores— y otras son nuevas.

### 8.1 Interludio Matemático: Trabajando con Funciones Continuas

#### 8.1.1 Repaso de la Función de Onda

Usaremos el lenguaje de las funciones de onda en esta lección, así que repasemos algo de ese material antes de sumergirnos. En la Lección 5, discutimos las funciones de onda como objetos abstractos, sin explicar qué tenían que ver con ondas o funciones. Antes de corregir esta omisión, repasaré lo que discutimos anteriormente.

Comienza eligiendo un observable $\mathbf{L}$, con valores propios $\lambda$ y vectores propios $|\lambda\rangle$. Sea $|\Psi\rangle$ un vector de estado. Dado que los vectores propios de un operador hermítico forman una base ortonormal completa, el vector $|\Psi\rangle$ puede expandirse como

$$|\Psi\rangle = \sum_{\lambda} \psi(\lambda) |\lambda\rangle. \quad (8.1)$$

Como recordarás de las Secciones 5.1.2 y 5.1.3, las cantidades

  25 

8.1. INTERLUDIO: FUNCIONES CONTINUAS 237

$$\psi(\lambda)$$

se llaman la función de onda del sistema. Pero observa: la forma específica de $\psi(\lambda)$ depende del observable específico $\mathbf{L}$ que elijamos inicialmente. Si elegimos un observable diferente, la función de onda (junto con los vectores base y los valores propios) será diferente, aunque todavía estemos hablando del mismo estado. Por lo tanto, debemos calificar la afirmación de que $\psi(\lambda)$ es la función de onda asociada con $|\Psi\rangle$. Para ser más precisos, deberíamos decir que $\psi(\lambda)$ es la función de onda en la **base-$\mathbf{L}$**. Si usamos las propiedades de ortonormalidad de los vectores base,

$$\langle \lambda_i | \lambda_j \rangle = \delta_{ij},$$

entonces la función de onda en la base-$\mathbf{L}$ también puede identificarse con los productos internos (o proyecciones) del vector de estado $|\Psi\rangle$ sobre los vectores propios $|\lambda\rangle$:

$$\psi(\lambda) = \langle \lambda | \Psi \rangle.$$

Puedes pensar en la función de onda de dos maneras. En primer lugar, es el conjunto de componentes del vector de estado en una base particular. Estas componentes pueden apilarse para formar un vector columna:

$$\begin{pmatrix}
\psi(\lambda_1) \\
\psi(\lambda_2) \\
\psi(\lambda_3) \\
\psi(\lambda_4) \\
\psi(\lambda_5)
\end{pmatrix}.$$

  25 

238 LECCIÓN 8. PARTÍCULAS Y ONDAS

Otra forma de pensar en la función de onda es como una función de $\lambda$. Si especificas cualquier valor admisible de $\lambda$, la función $\psi(\lambda)$ produce un número complejo. Por lo tanto, se puede decir que

$$\psi(\lambda)$$

es una función de valor complejo de la variable discreta $\lambda$. Cuando se piensa de esta manera, los operadores lineales se convierten en operaciones que se aplican a funciones y devuelven nuevas funciones.

Un último recordatorio: la probabilidad de que un experimento tenga el resultado $\lambda$ es

$$P(\lambda) = \psi^*(\lambda)\psi(\lambda).$$

#### 8.1.2 Funciones como Vectores

Hasta ahora, los sistemas que hemos estudiado han tenido vectores de estado de dimensión finita. Por ejemplo, el espín simple se describe mediante un espacio de estados bidimensional. Por esta razón, los observables han tenido solo un número finito de valores observables posibles. Pero hay observables más complicados que pueden tener un número infinito de valores. Un ejemplo es una partícula. Las coordenadas de una partícula son observables, pero, a diferencia del espín, las coordenadas tienen un número infinito de valores posibles. Por ejemplo, una partícula que se mueve a lo largo del eje $x$ puede encontrarse en cualquier valor real de $x$. En otras palabras, $x$ es una variable continuamente infinita. Cuando los observables de un sistema son continuos, la función de onda se convierte verdaderamente en una función de una variable continua. Para aplicar la mecánica cuántica a este tipo de sistema, tenemos que expandir la idea

  26 

8.1. INTERLUDIO: FUNCIONES CONTINUAS 239

de vectores para incluir funciones.

Las funciones son funciones, y los vectores son vectores —parecen cosas diferentes, así que ¿en qué sentido son vectores las funciones? Si piensas en los vectores como flechas que apuntan en el espacio tridimensional, entonces no son lo mismo que las funciones. Pero si adoptas la visión más amplia de los vectores como un conjunto de objetos matemáticos que satisfacen ciertos postulados, entonces las funciones pueden formar efectivamente un espacio vectorial. Tal espacio vectorial a menudo se llama espacio de Hilbert en honor al matemático David Hilbert.

Consideremos el conjunto de funciones complejas $\psi(x)$ de una sola variable real $x$. Por funciones complejas, quiero decir que para cada $x$, $\psi(x)$ es un número complejo. Por otro lado, la variable independiente $x$ es una variable real ordinaria. Puede tomar cualquier valor real desde $-\infty$ hasta $+\infty$.

Ahora, precisemos qué queremos decir cuando decimos "Las funciones son vectores". Esto no es una analogía vaga o una metáfora. Con las restricciones apropiadas (a las que volveremos), funciones como $\psi(x)$ satisfacen los axiomas matemáticos que definen un espacio vectorial. Mencionamos esta idea brevemente en la Sección 1.9.2, y ahora haremos uso completo de ella. Mirando hacia atrás a los axiomas que definen un espacio vectorial complejo (en la Sección 1.9.1), podemos ver que las funciones complejas satisfacen todos ellos:

1. La suma de dos funciones cualesquiera es una función.
2. La adición de funciones es conmutativa.
3. La adición de funciones es asociativa.
4. Hay una función cero única tal que cuando la sumas a cualquier función, obtienes la misma función.

  26 

240 LECCIÓN 8. PARTÍCULAS Y ONDAS

5. Dada cualquier función $\psi(x)$, hay una función única $-\psi(x)$ tal que $\psi(x) + (-\psi(x)) = 0$.
6. Multiplicar una función por cualquier número complejo da una función y es lineal.
7. La propiedad distributiva se cumple, lo que significa que
   $$z[\psi(x) + \varphi(x)] = z\psi(x) + z\varphi(x)$$
   $$[z + w]\psi(x) = z\psi(x) + w\psi(x),$$
   donde $z$ y $w$ son números complejos.

Todo esto implica que podemos identificar las funciones $\psi(x)$ con los vectores ket $|\Psi\rangle$ en un espacio vectorial abstracto. No es sorprendente que también podamos definir vectores bra. El vector bra $\langle \Psi|$ correspondiente al ket $|\Psi\rangle$ se identifica con la función conjugada compleja $\psi^*(x)$.

Para usar esta idea de manera efectiva, necesitaremos generalizar algunos de los elementos de nuestro kit de herramientas matemáticas. En lecciones anteriores, las etiquetas que identificaban las funciones de onda eran miembros de algún conjunto discreto finito —por ejemplo, los valores propios de algún observable. Pero ahora la variable independiente es continua. Entre otras cosas, esto significa que no podemos sumar sobre ella usando sumas ordinarias. Creo que sabes qué hacer, sin embargo. Aquí hay reemplazos orientados a funciones para tres de nuestros conceptos basados en vectores, dos de los cuales reconocerás fácilmente:

* Las **integrales** reemplazan a las sumas.

  26 

8.1. INTERLUDIO: FUNCIONES CONTINUAS 241

* Las **densidades de probabilidad** reemplazan a las probabilidades.
* Las **funciones delta de Dirac** reemplazan a las deltas de Kronecker.

Veamos estos elementos más de cerca.

**Las Integrales Reemplazan a las Sumas:**
Si quisiéramos ser realmente rigurosos, comenzaríamos reemplazando el eje $x$ por un conjunto discreto de puntos separados por una distancia muy pequeña $\epsilon$, y luego tomaríamos el límite $\epsilon \to 0$. Tomaría varias páginas justificar cada paso. Pero podemos evitar este problema con algunas definiciones intuitivas, como reemplazar sumas con integrales. Esquemáticamente, este concepto puede escribirse como

$$\sum_i \rightarrow \int dx.$$

Por ejemplo, si queremos calcular el área bajo una curva, dividimos el eje $x$ en segmentos diminutos y luego sumamos las áreas de un gran número de rectángulos, exactamente como hacemos en cálculo elemental. Cuando dejamos que los segmentos se reduzcan a tamaño cero, la suma se convierte en una integral.

Consideremos un bra $\langle \Psi|$ y un ket $|\Phi\rangle$ y definamos su producto interno. La forma obvia de hacer esto es reemplazar la suma en la Ec. 1.2 con una integral. Definimos el producto interno como

$$\langle \Psi | \Phi \rangle = \int_{-\infty}^{\infty} \psi^*(x) \varphi(x) dx. \quad (8.2)$$

  26 

242 LECCIÓN 8. PARTÍCULAS Y ONDAS

**Las Densidades de Probabilidad Reemplazan a las Probabilidades:**
Más adelante, identificaremos

$$P(x) = \psi^*(x)\psi(x)$$

como una densidad de probabilidad para la variable $x$. ¿Por qué una densidad de probabilidad y no solo una probabilidad? Si $x$ es una variable continua, la probabilidad de que tenga un valor exacto es típicamente cero. Una pregunta más útil es: ¿Cuál es la probabilidad de que $x$ se encuentre entre dos valores, $x = a$ y $x = b$? Las densidades de probabilidad se definen de modo que esta probabilidad esté dada por una integral:

$$P(a, b) = \int_a^b P(x) dx = \int_a^b \psi^*(x)\psi(x) dx.$$

Debido a que la probabilidad total debe ser 1, podemos definir un vector normalizado mediante

$$\int_{-\infty}^{\infty} \psi^*(x)\psi(x) dx = 1. \quad (8.3)$$

**Las Funciones Delta de Dirac Reemplazan a las Deltas de Kronecker:**
Hasta ahora, esto debería ser muy familiar. La función delta de Dirac puede serlo menos. La función delta es el análogo de la delta de Kronecker, $\delta_{ij}$. La delta de Kronecker se define como 0 para $i \neq j$ y 1 para $i = j$. Pero también puede definirse de otra manera. Considera cualquier vector $F_i$ en un espacio de dimensión finita. Es fácil ver que la delta de Kronecker satisface

  26 

8.1. INTERLUDIO: FUNCIONES CONTINUAS 243

$$\sum_j \delta_{ij} F_j = F_i.$$

Esto se debe a que el único término distinto de cero en la suma es aquel donde $j = i$. Dentro de la suma, el símbolo de Kronecker filtra todas las $F$ excepto $F_i$. La generalización obvia es definir una nueva función que tenga propiedades de filtrado similares cuando se use dentro de una integral. En otras palabras, queremos una nueva entidad

$$\delta(x - x')$$

con la propiedad de que, para cualquier función $F(x)$,

$$\int_{-\infty}^{\infty} \delta(x - x') F(x') dx' = F(x). \quad (8.4)$$

La Ec. 8.4 define esta nueva entidad, llamada función delta de Dirac, que resulta ser una herramienta esencial en mecánica cuántica. Pero a pesar de su nombre, no es realmente una función en el sentido habitual. Es cero siempre que $x \neq x'$, pero cuando $x = x'$ es infinita. De hecho, es justo lo suficientemente infinita como para que el área bajo $\delta(x)$ sea igual a 1. Hablando de manera aproximada, es una función que es distinta de cero en un intervalo infinitesimal $\epsilon$, pero en ese intervalo tiene el valor $1/\epsilon$. Por lo tanto, su área es 1 y, lo que es más importante, satisface la Ec. 8.4. La función

$$\frac{n}{\sqrt{\pi}} e^{-(nx)^2}$$

  26 

244 LECCIÓN 8. PARTÍCULAS Y ONDAS

 Figura 8.1: Aproximaciones a la Función Delta de Dirac. Estas aproximaciones se basan en $\frac{n}{\sqrt{\pi}} e^{-(nx)^2}$ y se representan para valores crecientes de $n$. 

  26 

8.1. INTERLUDIO: FUNCIONES CONTINUAS 245

aproxima la función delta razonablemente bien a medida que $n$ se vuelve muy grande. La Fig. 8.1 representa esta aproximación para valores crecientes de $n$. Aunque nos detenemos en $n = 10$, un valor muy pequeño, observa que la gráfica ya se ha vuelto muy estrecha y con un pico agudo.

#### 8.1.3 Integración por Partes

Antes de discutir los operadores lineales, haremos un breve desvío para recordarte una técnica llamada integración por partes. Es bastante simple e indispensable para nuestros propósitos. La usaremos una y otra vez. Supongamos que tomamos dos funciones, $F$ y $G$, y consideramos la diferencial de su producto $FG$. Podemos escribir

$$d(FG) = F dG + G dF$$

o

$$d(FG) - G dF = F dG.$$

Tomando la integral definida nos da

$$\int_a^b d(FG) - \int_a^b G dF = \int_a^b F dG$$

o

$$FG \Big|_a^b - \int_a^b G dF = \int_a^b F dG.$$

  26 

246 LECCIÓN 8. PARTÍCULAS Y ONDAS

Esta es la fórmula estándar que puedes recordar del cálculo. Pero en mecánica cuántica los límites de integración tienden a abarcar todo el eje, y nuestras funciones de onda deben tender a cero en el infinito para estar adecuadamente normalizadas. Por lo tanto, el primer término de esta expresión siempre se evaluará como cero. Con eso en mente, podemos usar una versión simplificada de la integración por partes:

$$\int_{-\infty}^{\infty} F \frac{dG}{dx} dx = -\int_{-\infty}^{\infty} \frac{dF}{dx} G dx.$$

Esta forma es correcta siempre que $F$ y $G$ tiendan a cero apropiadamente en el infinito, de modo que el término de frontera se anule. Te harás un gran favor si simplemente memorizas este patrón: Cambia la derivada de un factor del integrando al otro a costa de un signo menos.

#### 8.1.4 Operadores Lineales

Los bras y kets son la mitad de la historia en mecánica cuántica; la otra mitad es el concepto de operadores lineales y, en particular, los operadores hermíticos. Esto plantea dos preguntas:

* ¿Qué se entiende por un operador lineal en un espacio de funciones?
* ¿Cuál es la condición para que un operador lineal sea hermítico?

El concepto de un operador lineal es bastante simple: es una máquina que actúa sobre una función y da otra función.

  26 

8.1. INTERLUDIO: FUNCIONES CONTINUAS 247

Cuando actúa sobre la suma de dos funciones, da la suma de los resultados individuales. Cuando actúa sobre un múltiplo numérico complejo de una función, da el mismo múltiplo del resultado original. En otras palabras, es (¡sorpresa!) lineal.

Veamos algunos ejemplos. Una operación simple que podemos realizar en una función $\psi(x)$ es multiplicarla por $x$. Eso da una nueva función $x\psi(x)$, y puedes verificar fácilmente que la acción es lineal. Representaremos el operador "multiplicar por $x$" con el símbolo $\mathbf{X}$. Por definición, entonces,

$$\mathbf{X} \psi(x) = x \psi(x). \quad (8.5)$$

Aquí hay otro ejemplo. Define $\mathbf{D}$ como el operador de diferenciación:

$$\mathbf{D} \psi(x) = \frac{d\psi(x)}{dx}. \quad (8.6)$$

**Ejercicio 8.1:** Demuestra que $\mathbf{X}$ y $\mathbf{D}$ son operadores lineales.

Esto, por supuesto, es un subconjunto minúsculo de los posibles operadores lineales que pueden construirse, pero pronto veremos que $\mathbf{X}$ y $\mathbf{D}$ juegan un papel muy central en la mecánica cuántica de las partículas.

Ahora, consideremos la propiedad de ser hermítico. Una forma conveniente de definir un operador hermítico es a través de sus elementos de matriz, colocándolo entre un bra y un ket. Puedes colocar un operador $\mathbf{L}$ de dos maneras diferentes:

  26 

248 LECCIÓN 8. PARTÍCULAS Y ONDAS

$$\langle \Psi | \mathbf{L} | \Phi \rangle$$

o

$$\langle \Phi | \mathbf{L} | \Psi \rangle.$$

En general, no hay una relación simple entre estos dos "sándwiches". Pero en el caso de un operador hermítico (para el cual, por definición, $\mathbf{L}^\dagger = \mathbf{L}$) hay una relación simple: los dos sándwiches son complejos conjugados el uno del otro:

$$\langle \Psi | \mathbf{L} | \Phi \rangle = \langle \Phi | \mathbf{L} | \Psi \rangle^*.$$

Veamos si los operadores $\mathbf{X}$ y $\mathbf{D}$ son hermíticos. Recordando que

$$\mathbf{X} \psi(x) = x \psi(x),$$

y usando la fórmula del producto interno Ec. 8.2, podemos escribir

$$\langle \Psi | \mathbf{X} | \Phi \rangle = \int \psi^*(x) x \varphi(x) dx$$

y

$$\langle \Phi | \mathbf{X} | \Psi \rangle = \int \varphi^*(x) x \psi(x) dx.$$

Debido a que $x$ es real, es fácil ver que estas dos integrales son complejas conjugadas entre sí, y por lo tanto que $\mathbf{X}$ es hermítico.

  27 

8.1. INTERLUDIO: FUNCIONES CONTINUAS 249

¿Qué pasa con el operador $\mathbf{D}$? En este caso, los dos sándwiches son

$$\langle \Psi | \mathbf{D} | \Phi \rangle = \int \psi^*(x) \frac{d\varphi(x)}{dx} dx \quad (8.7)$$

y

$$\langle \Phi | \mathbf{D} | \Psi \rangle = \int \varphi^*(x) \frac{d\psi(x)}{dx} dx. \quad (8.8)$$

Para determinar si $\mathbf{D}$ es hermítico, necesitamos comparar estas dos integrales y ver si son complejas conjugadas entre sí. En esta forma, es un poco difícil de determinar. El truco es hacer la segunda integral por partes. Como explicamos, la integración por partes te permite cambiar la derivada de un factor en el integrando al otro, siempre que cambies el signo al mismo tiempo. Por lo tanto, la integral en la Ec. 8.8 puede reescribirse como

$$\langle \Phi | \mathbf{D} | \Psi \rangle = -\int \psi(x) \frac{d\varphi^*(x)}{dx} dx. \quad (8.9)$$

Ahora, solo necesitamos comparar las dos expresiones en las Ecs. 8.7 y 8.9, lo que resulta ser fácil. Debido al signo menos, está claro que definitivamente no son complejas conjugadas entre sí. En cambio, su relación se captura mediante

$$\langle \Psi | \mathbf{D} | \Phi \rangle = -\langle \Phi | \mathbf{D} | \Psi \rangle^*,$$

que es el diametralmente opuesto a lo que queríamos. A diferencia del operador $\mathbf{X}$, $\mathbf{D}$ no es hermítico. En cambio, satisface

  27 

250 LECCIÓN 8. PARTÍCULAS Y ONDAS

$$\mathbf{D}^\dagger = -\mathbf{D}.$$

Un operador con esta propiedad se llama **antihermítico**.

Aunque los operadores antihermíticos y hermíticos son opuestos, es muy fácil pasar de uno a otro. Todo lo que tienes que hacer es multiplicar por el número imaginario $i$ o $-i$. Por lo tanto, podemos usar $\mathbf{D}$ para construir un operador que sea hermítico, a saber

$$-i\hbar \mathbf{D}.$$

Si observamos la acción de este nuevo operador hermítico sobre funciones de onda, encontramos que

$$-i\hbar \mathbf{D} \psi(x) = -i\hbar \frac{d\psi(x)}{dx}. \quad (8.10)$$

Mantén esta fórmula en mente. Pronto jugará un papel principal en la definición de una propiedad muy importante de las partículas —su momento.

### 8.2 El Estado de una Partícula

En mecánica clásica, el "estado de un sistema" significa todo lo que necesitas saber para predecir el futuro del sistema, dadas las fuerzas que actúan sobre él. Eso, por supuesto, significa las posiciones de todas las partículas que componen el sistema, así como los momentos de esas partículas. Desde una perspectiva clásica, las posiciones y momentos instantáneos son variables completamente independientes. Por ejemplo, para una partícula de masa $m$ que se mueve

  27 

8.2. EL ESTADO DE UNA PARTÍCULA 251

a lo largo de un eje unidimensional $x$, el estado momentáneo del sistema se describe mediante el par $(x, p)$. La coordenada $x$ es la ubicación de la partícula, y $p = m\dot{x}$ es su momento. Tomados en conjunto, estos dos variables definen el espacio de fases del sistema. Si también conocemos la fuerza sobre la partícula en función de su posición, las ecuaciones de Hamilton nos permiten calcular su posición y momento en todos los tiempos posteriores. Definen un flujo a través del espacio de fases.

Dado esto, uno podría adivinar que el estado cuántico de una partícula estaría generado por una base de estados etiquetados por posición y momento:

$$|x, p\rangle.$$

La función de onda sería entonces una función de ambas variables:

$$\psi(x, p) = \langle x, p | \Psi \rangle.$$

Sin embargo, esto es incorrecto. Ya hemos visto que las cosas que serían simultáneamente conocibles en la física clásica pueden no serlo en mecánica cuántica. Diferentes componentes de un espín, por ejemplo $\sigma_z$ y $\sigma_x$, son un ejemplo. No se pueden conocer ambas componentes simultáneamente; por lo tanto, no se tienen estados en los que ambas componentes estén especificadas. Lo mismo es cierto para $x$ y $p$: especificar ambos valores es demasiado.

Ya sea que estemos hablando de espines ($\sigma_z, \sigma_x$) o de posiciones y momentos ($x, p$), la incompatibilidad es en última instancia un hecho experimental.

  27 

252 LECCIÓN 8. PARTÍCULAS Y ONDAS

¿Qué podemos saber entonces sobre la partícula en el eje $x$, si no $x$ y $p$? La respuesta es $x$ **o** $p$; porque según las matemáticas de los operadores de posición y momento, los dos no conmutan. Pero enfatizo que esto no es algo que pudieras haber predicho de antemano; es la destilación de muchas décadas de observaciones experimentales.

Si la posición de una partícula es un observable, debe haber un operador hermítico asociado a ella. El candidato obvio es el operador $\mathbf{X}$. El primer paso para entender esta conexión fundamental entre el concepto intuitivo de posición y el operador matemático $\mathbf{X}$ es calcular los vectores propios y valores propios de $\mathbf{X}$. Los valores propios son los posibles valores de posición que pueden observarse, y los vectores propios representan los estados de posición definida.

#### 8.2.1 Los Valores Propios y Vectores Propios de la Posición

La siguiente pregunta obvia es: ¿Cuáles son los resultados posibles de medir $\mathbf{X}$, y cuáles son los estados en los que tiene un valor definido (predecible)? En otras palabras, ¿cuáles son sus valores propios y vectores propios? Comenzaremos con $\mathbf{X}$. La ecuación propia para $\mathbf{X}$ es

$$\mathbf{X} |\Psi\rangle = x_0 |\Psi\rangle,$$

donde el valor propio se denota por $x_0$. En términos de funciones de onda, esto se convierte en

$$x \psi(x) = x_0 \psi(x). \quad (8.11)$$

  27 

8.2. EL ESTADO DE UNA PARTÍCULA 253

Esta última ecuación parece extraña. ¿Cómo puede $x$ veces una función ser proporcional a la misma función? A primera vista, esto parece imposible. Pero prosigamos. Podemos reescribir la Ec. 8.11 en la forma

$$(x - x_0) \psi(x) = 0.$$

Por supuesto, si un producto es cero, entonces al menos uno de los factores debe ser cero. Pero los otros factores pueden ser diferentes de cero. Por lo tanto, si $x \neq x_0$, entonces $\psi(x) = 0$. Esa es una condición muy fuerte. Dice que para un valor propio dado $x_0$, la función $\psi(x)$ puede ser distinta de cero en un solo punto, a saber, en

$$x = x_0.$$

Para una función continua ordinaria, esta condición sería mortal: ninguna función sensata puede ser cero en todas partes excepto en un punto, y ser distinta de cero solo en ese punto. Pero esa es exactamente la propiedad de la función delta de Dirac

$$\delta(x - x_0).$$

Evidentemente, entonces, cada número real $x_0$ es un valor propio de $\mathbf{X}$, y los vectores propios correspondientes son funciones (a menudo las llamamos funciones propias) que están infinitamente concentradas en $x = x_0$. El significado de esto es claro: las funciones de onda

$$\psi(x) = \delta(x - x_0)$$

  27 

254 LECCIÓN 8. PARTÍCULAS Y ONDAS

representan estados en los que la partícula está ubicada justo en el punto $x_0$ en el eje $x$.

Por supuesto, tiene mucho sentido que la función de onda que representa una partícula que se sabe que está en $x_0$ sea cero en todas partes excepto en $x_0$. ¿Cómo podría ser de otra manera? Pero es gratificante ver que las matemáticas confirman esta intuición.

Considera el producto interno de un estado $|\Psi\rangle$ y un estado propio de posición $|x_0\rangle$:

$$\langle x_0 | \Psi \rangle.$$

Usando la Ec. 8.2, obtenemos

$$\langle x_0 | \Psi \rangle = \int_{-\infty}^{\infty} \delta(x - x_0) \psi(x) dx.$$

Por la definición de las funciones delta dada en la Ec. 8.4, esta integral se evalúa como

$$\langle x_0 | \Psi \rangle = \psi(x_0). \quad (8.12)$$

Debido a que esto es cierto para cualquier $x_0$, podemos omitir el subíndice y escribir la ecuación general

$$\langle x | \Psi \rangle = \psi(x). \quad (8.13)$$

En otras palabras, la función de onda, $\psi(x)$, de una partícula que se mueve en la dirección $x$ es la proyección de un vector de estado $|\Psi\rangle$ sobre los vectores propios de la posición. También nos referiremos a $\psi(x)$ como la función de onda en la **representación de posiciones**.

  27 

8.2. EL ESTADO DE UNA PARTÍCULA 255

#### 8.2.2 Momento y Sus Vectores Propios

La posición es intuitiva; el momento lo es menos, particularmente en mecánica cuántica. Solo más tarde veremos la conexión entre el operador que identificamos con el momento y el concepto clásico familiar de masa por velocidad. Pero te aseguro que haremos la conexión. Por ahora, tomemos la ruta matemática abstracta. El operador de momento en mecánica cuántica se llama $\mathbf{P}$, y se define en términos del operador $-i\mathbf{D}$:

$$-i\mathbf{D} = -i \frac{d}{dx}.$$

Como vimos anteriormente en la Ec. 8.10, necesitamos el factor $-i$ para hacer que este operador sea hermítico.

Podríamos simplemente definir $\mathbf{P}$ como $-i\mathbf{D}$, pero si lo hiciéramos, tendríamos un problema más adelante cuando conectemos estas ideas con las de la física clásica. La razón debería ser clara: hay una discrepancia dimensional. En física clásica, las unidades de momento son masa por velocidad —en otras palabras, masa por longitud dividida por tiempo (ML/T). Por otro lado, el operador $\mathbf{D}$ tiene unidades de longitud inversa, o 1/L. La resolución de la discrepancia la proporciona la constante de Planck $\hbar$, que tiene unidades de ML$^2$/T. La relación correcta entre $\mathbf{P}$ y $\mathbf{D}$ es, por lo tanto,

$$\mathbf{P} = -i\hbar \mathbf{D} \quad (8.14)$$

o, en términos de su acción sobre funciones de onda,

$$\mathbf{P} \psi(x) = -i\hbar \frac{d\psi(x)}{dx}. \quad (8.15)$$

  27 

256 LECCIÓN 8. PARTÍCULAS Y ONDAS

Los físicos cuánticos a menudo usan unidades en las que $\hbar$ es exactamente uno, y de esa manera simplifican las ecuaciones. Por tentador que sea, no haremos eso aquí.

Calculemos los vectores propios y valores propios de $\mathbf{P}$. La ecuación propia en notación vectorial abstracta es

$$\mathbf{P} |\Psi\rangle = p |\Psi\rangle, \quad (8.16)$$

donde el símbolo $p$ es un valor propio de $\mathbf{P}$. La Ec. 8.16 también puede expresarse en términos de funciones de onda. Usando la identificación $\mathbf{P} = -i\hbar \frac{d}{dx}$, podemos escribir la ecuación propia como

$$-i\hbar \frac{d\psi(x)}{dx} = p \psi(x)$$

o

$$\frac{d\psi(x)}{dx} = \frac{ip}{\hbar} \psi(x).$$

Este es un tipo de ecuación que hemos encontrado antes. La solución tiene la forma de una exponencial:

$$\psi_p(x) = A e^{\frac{ipx}{\hbar}}.$$

El subíndice $p$ es solo un recordatorio de que $\psi_p(x)$ es el vector propio de $\mathbf{P}$ con el valor propio específico $p$. Es una función de $x$, pero está etiquetada por un valor propio de $\mathbf{P}$.

  27 

8.2. EL ESTADO DE UNA PARTÍCULA 257

La constante $A$ que multiplica la exponencial no está determinada por la ecuación de vectores propios. Eso no es nada nuevo; la ecuación de valores propios nunca nos dice la normalización general de la función de onda. Como regla, fijamos la constante requiriendo que la función de onda esté normalizada a probabilidad unitaria. Un ejemplo que se remonta a la Sección 2.3 es el vector propio de la componente $x$ del espín:

$$|r\rangle = \frac{1}{\sqrt{2}}|u\rangle + \frac{1}{\sqrt{2}}|d\rangle.$$

El factor $1/\sqrt{2}$ está ahí para asegurar que la probabilidad total sea 1.

Normalizar los vectores propios de $\mathbf{P}$ es una operación más sutil, pero el resultado es simple. El factor $A$ es solo ligeramente más complicado que en el caso del espín. Para ahorrar tiempo, te diré la respuesta y dejaré que la demuestres más tarde. El factor correcto es $A = 1/\sqrt{2\pi}$. Por lo tanto,

$$\psi_p(x) = \frac{1}{\sqrt{2\pi}} e^{\frac{ipx}{\hbar}}. \quad (8.17)$$

Un punto de cierto interés se sigue de las Ecs. 8.13 y 8.17. El producto interno de un vector propio de posición $|x\rangle$ y un vector propio de momento $|p\rangle$ tiene una forma muy simple y simétrica:

$$\langle x | p \rangle = \frac{1}{\sqrt{2\pi}} e^{\frac{ipx}{\hbar}}$$
$$\langle p | x \rangle = \frac{1}{\sqrt{2\pi}} e^{-\frac{ipx}{\hbar}}. \quad (8.18)$$

  27 

258 LECCIÓN 8. PARTÍCULAS Y ONDAS

La segunda ecuación es simplemente el complejo conjugado de la primera. Estos resultados son fáciles de verificar si tienes en cuenta que $|x\rangle$ está representado por una función delta.

Me gustaría mencionar dos puntos importantes antes de continuar:

1. La Ec. 8.17 representa una función propia de momento en la base de posiciones. En otras palabras, aunque representa un estado propio de momento, es una función de $x$, y no una función explícita de $p$.
2. Hemos estado usando el símbolo $\psi$ tanto para estados propios de posición como de momento. Un matemático podría no aprobar el uso del mismo símbolo para dos funciones diferentes, pero los físicos lo hacen todo el tiempo. $\psi(x)$ es solo el símbolo genérico para la función que sea que estemos discutiendo.

En este punto, comenzamos a vislumbrar por qué la función de onda se llama función de onda. Lo que deberías notar es que las funciones propias (funciones de onda que representan vectores propios) del operador de momento tienen la forma de ondas —ondas seno y ondas coseno, para ser precisos. De hecho, ahora podemos ver uno de los aspectos más fundamentales de la dualidad onda-partícula de la mecánica cuántica. La longitud de onda de la función

$$e^{\frac{ipx}{\hbar}}$$

está dada por

  28 

8.2. EL ESTADO DE UNA PARTÍCULA 259

$$\lambda = \frac{2\pi\hbar}{p}$$

porque el valor de la función no cambia si sumamos $\frac{2\pi\hbar}{p}$ a la variable $x$:

$$e^{\frac{ip(x + \frac{2\pi\hbar}{p})}{\hbar}} = e^{\frac{ipx}{\hbar}} e^{2\pi i} = e^{\frac{ipx}{\hbar}}.$$

Hagamos una pausa para discutir la importancia de esta conexión entre momento y longitud de onda. No es solo importante: en muchos sentidos, es la relación que definió la física del siglo XX.

Durante los últimos cien años, los físicos se han preocupado principalmente por descubrir las leyes del mundo microscópico. Esto ha significado descubrir cómo se construyen los objetos a partir de objetos más pequeños. Los ejemplos son obvios: las moléculas están hechas de átomos; los átomos de electrones y núcleos; los núcleos de protones y neutrones. Estas partículas subnucleares se construyen a partir de quarks y gluones. Y el juego continúa mientras los científicos buscan entidades cada vez más pequeñas y más ocultas.

Todos estos objetos son demasiado pequeños para ser vistos con los mejores microscopios ópticos, y mucho menos a simple vista. La razón no es solo que nuestros ojos sean insuficientemente sensibles. El hecho más importante es que los ojos y los microscopios ópticos son sensibles al espectro visible, que comprende longitudes de onda al menos unos pocos miles de veces más largas que el tamaño de un átomo. Como regla general, no se pueden resolver objetos mucho más pequeños que la longitud de onda que se utiliza para observarlos. Por esta razón, la historia de la física del siglo XX fue en gran parte una búsqueda

  28 

260 LECCIÓN 8. PARTÍCULAS Y ONDAS

de longitudes de onda de luz —o cualquier otro tipo de onda— cada vez más pequeñas. En la Lección 10, descubriremos que la luz de una longitud de onda dada está compuesta por fotones cuyo momento está relacionado con la longitud de onda exactamente por la relación

$$\lambda = \frac{2\pi\hbar}{p}.$$

La implicación es que para sondear objetos de tamaño cada vez más pequeño se necesitan fotones (u otros objetos) de momento cada vez mayor. Un momento grande significa inevitablemente una gran energía. Es por esa razón que el descubrimiento de las propiedades microscópicas de la materia requirió aceleradores de partículas cada vez más potentes.

### 8.3 Transformadas de Fourier y la Base de Momento

La función de onda $\psi(x)$ tiene el papel importante de determinar la probabilidad de encontrar la partícula en la posición $x$:

$$P(x) = \psi^*(x)\psi(x).$$

Como veremos, ningún experimento puede determinar simultáneamente la posición y el momento de una partícula. Pero si renunciamos a determinar cualquier cosa sobre la posición, el momento puede medirse con precisión. La situación es bastante análoga a la de las componentes $x$ y $z$ de un espín. Cualquier valor puede medirse, pero no ambos.

  28 

8.3. TRANSFORMADAS DE FOURIER / BASE DE MOMENTO 261

¿Cuál es la probabilidad de que una partícula tenga momento $p$ si elegimos medirlo? La respuesta es una generalización directa de los principios establecidos en la Lección 3. La probabilidad de que una medición de momento dé el momento $p$ es

$$P(p) = |\langle p | \Psi \rangle|^2. \quad (8.19)$$

La entidad $\langle p | \Psi \rangle$ se llama la función de onda de $|\Psi\rangle$ en la **representación de momentos**. Naturalmente, es una función de $p$ y se denota con un nuevo símbolo:

$$\tilde{\psi}(p) = \langle p | \Psi \rangle. \quad (8.20)$$

Ahora está claro que hay dos formas de representar un vector de estado. Una forma es en la base de posiciones y la otra es en la base de momentos. Ambas funciones de onda —la función de onda de posición $\psi(x)$ y la función de onda de momento $\tilde{\psi}(p)$— representan exactamente el mismo vector de estado $|\Psi\rangle$. Se sigue que debe haber alguna transformación entre ellas tal que si conoces $\psi(x)$, la transformación produce $\tilde{\psi}(p)$, y viceversa. De hecho, las dos representaciones son **transformadas de Fourier** la una de la otra.

#### 8.3.1 Resolviendo la Identidad

Estamos a punto de ver el gran poder de la notación bra-ket de Dirac para simplificar cosas complicadas. Primero, recordemos una idea importante de lecciones anteriores. Supongamos que definimos una base ortonormal de estados a través de los vectores propios de

  28 

262 LECCIÓN 8. PARTÍCULAS Y ONDAS

algún observable hermítico. Llamemos a los vectores base $|i\rangle$. En la Lección 7, expliqué un truco muy útil, y ahora vamos a ver cuán útil es. Se llama **resolver la identidad**. El truco dado en (Ec. 7.11) es escribir el operador identidad $\mathbf{I}$ (el operador que actúa sobre cualquier vector para dar el mismo vector) en la forma

$$\mathbf{I} = \sum_i |i\rangle \langle i|.$$

Debido a que el momento y la posición son ambos hermíticos, los conjuntos de vectores $|x\rangle$ y $|p\rangle$ definen cada uno vectores base. Reemplazando la sumatoria por integración descubrimos dos formas de resolver la identidad:

$$\mathbf{I} = \int dx |x\rangle \langle x| \quad (8.21)$$

y

$$\mathbf{I} = \int dp |p\rangle \langle p|. \quad (8.22)$$

Supongamos que conocemos la función de onda del vector abstracto $|\Psi\rangle$ en la representación de posiciones. Por definición, es igual a

$$\psi(x) = \langle x | \Psi \rangle. \quad (8.23)$$

Ahora supongamos que queremos conocer la función de onda $\tilde{\psi}(p)$ en la representación de momentos. Aquí están los pasos detallados:

  28 

8.3. TRANSFORMADAS DE FOURIER / BASE DE MOMENTO 263

* Primero, usa la definición de la función de onda en la representación de momentos:
  $$\tilde{\psi}(p) = \langle p | \Psi \rangle.$$
* Ahora, inserta el operador unidad entre el bra y el ket, en la forma dada en la Ec. 8.21:
  $$\tilde{\psi}(p) = \int dx \langle p | x \rangle \langle x | \Psi \rangle.$$
* La expresión $\langle x | \Psi \rangle$ es justamente la función de onda $\psi(x)$, y $\langle p | x \rangle$ nos la da la segunda ecuación de las Ecs. 8.18:
  $$\langle p | x \rangle = \frac{1}{\sqrt{2\pi}} e^{-\frac{ipx}{\hbar}}.$$
* Juntándolo todo, encontramos que
  $$\tilde{\psi}(p) = \frac{1}{\sqrt{2\pi}} \int dx e^{-\frac{ipx}{\hbar}} \psi(x). \quad (8.24)$$

Esta ecuación nos muestra exactamente cómo transformar una función de onda dada en la representación de posiciones en la función de onda correspondiente en la representación de momentos. ¿Para qué sirve? Supongamos que se conoce la función de onda de posición para alguna partícula; sin embargo, el objetivo de tu experimento es medir el momento, y quieres conocer

  28 

264 LECCIÓN 8. PARTÍCULAS Y ONDAS

la probabilidad de observar el momento $p$. El procedimiento es primero calcular $\tilde{\psi}(p)$ usando la Ec. 8.24 y luego calcular la probabilidad

$$P(p) = \tilde{\psi}^*(p) \tilde{\psi}(p).$$

Es igual de fácil ir en la otra dirección. Supongamos que conocemos $\tilde{\psi}(p)$ y deseamos recuperar $\psi(x)$. Esta vez, usamos la Ec. 8.22 para resolver la identidad. Aquí están los pasos (observa que se parecen sospechosamente a los anteriores):

* Primero, usa la definición de la función de onda en la representación de posiciones:
  $$\psi(x) = \langle x | \Psi \rangle.$$
* Ahora, inserta el operador unidad entre el bra y el ket, en la forma dada en la Ec. 8.22:
  $$\psi(x) = \int dp \langle x | p \rangle \langle p | \Psi \rangle.$$
* La expresión $\langle p | \Psi \rangle$ es justamente la función de onda $\tilde{\psi}(p)$, y $\langle x | p \rangle$ nos la da la primera de las Ecs. 8.18.
  $$\langle x | p \rangle = \frac{1}{\sqrt{2\pi}} e^{\frac{ipx}{\hbar}}.$$

  28 

8.4. CONMUTADORES Y CORCHETES DE POISSON 265

* Juntándolo todo, encontramos que
  $$\psi(x) = \frac{1}{\sqrt{2\pi}} \int dp e^{\frac{ipx}{\hbar}} \tilde{\psi}(p). \quad (8.25)$$

Echemos otro vistazo a las dos ecuaciones para ir de la posición al momento y viceversa. Observa lo simétricas que son. La única asimetría es que una ecuación contiene $e^{\frac{ipx}{\hbar}}$ y la otra contiene $e^{-\frac{ipx}{\hbar}}$:

$$\tilde{\psi}(p) = \frac{1}{\sqrt{2\pi}} \int dx e^{-\frac{ipx}{\hbar}} \psi(x)$$
$$\psi(x) = \frac{1}{\sqrt{2\pi}} \int dp e^{\frac{ipx}{\hbar}} \tilde{\psi}(p). \quad (8.26)$$

La relación entre la representación de posiciones y la de momentos resumida por las Ecs. 8.26 es que son **transformadas de Fourier recíprocas** una de la otra. De hecho, estas son las ecuaciones centrales en el campo del análisis de Fourier. Quiero que notes lo fácil que fue derivar esas ecuaciones usando la elegante notación de Dirac.

### 8.4 Conmutadores y Corchetes de Poisson

Anteriormente, en la Lección 4, formulamos dos principios importantes sobre los conmutadores. El primero tenía que ver con la conexión entre la mecánica clásica y la mecánica cuántica;

  28 

266 LECCIÓN 8. PARTÍCULAS Y ONDAS

el segundo tenía que ver con la incertidumbre. Ahora terminaré esta larga lección mostrándote lo que estos principios tienen que ver con $\mathbf{X}$ y $\mathbf{P}$.

Comenzaremos con la conexión entre conmutadores y la física clásica. Como recordarás, encontramos que los conmutadores tienen una gran similitud con los corchetes de Poisson, una relación que hicimos explícita en la Ec. 4.21. Si insertamos los símbolos de operador $\mathbf{L}$ y $\mathbf{M}$ que hemos estado usando en esta lección, obtenemos

$$[\mathbf{L}, \mathbf{M}] \quad \Longleftrightarrow \quad i\hbar \{\mathbf{L}, \mathbf{M}\}, \quad (8.27)$$

y recordamos que las ecuaciones para el movimiento cuántico se asemejan fuertemente a sus equivalentes clásicos. Esto sugiere que podemos aprender algo calculando el conmutador de los observables $\mathbf{X}$ y $\mathbf{P}$. Afortunadamente, esto es fácil de hacer.

Primero, veamos qué hace el producto $\mathbf{X}\mathbf{P}$ cuando actúa como operador sobre una función de onda arbitraria $\psi(x)$. Recordando las Ecs. 8.5 y 8.15, podemos escribir

$$\mathbf{X} \psi(x) = x \psi(x)$$
$$\mathbf{P} \psi(x) = -i\hbar \frac{d\psi(x)}{dx}.$$

Juntas, estas ecuaciones nos dicen cómo actúa el producto $\mathbf{X}\mathbf{P}$ sobre $\psi(x)$:

$$\mathbf{X}\mathbf{P} \psi(x) = -i\hbar x \frac{d\psi(x)}{dx}. \quad (8.28)$$

Ahora, intentémoslo con $\mathbf{X}$ y $\mathbf{P}$ en el orden opuesto:

  28 

8.4. CONMUTADORES Y CORCHETES DE POISSON 267

$$\mathbf{P}\mathbf{X} \psi(x) = -i\hbar \frac{d\left( x \psi(x) \right)}{dx}.$$

Para calcular esta última expresión, solo usamos la regla estándar para diferenciar el producto $x\psi(x)$. Usando esta regla, es fácil ver que

$$\mathbf{P}\mathbf{X} \psi(x) = -i\hbar x \frac{d\psi(x)}{dx} - i\hbar \psi(x). \quad (8.29)$$

Ahora, restaremos la Ec. 8.29 de la Ec. 8.28 para mostrar cómo actúa el conmutador sobre la función de onda:

$$[\mathbf{X}, \mathbf{P}] \psi(x) = \mathbf{X}\mathbf{P} \psi(x) - \mathbf{P}\mathbf{X} \psi(x)$$

o

$$[\mathbf{X}, \mathbf{P}] \psi(x) = i\hbar \psi(x).$$

En otras palabras, cuando el conmutador $[\mathbf{X}, \mathbf{P}]$ actúa sobre cualquier función de onda $\psi(x)$, todo lo que hace es multiplicar $\psi(x)$ por el número $i\hbar$. Podemos expresar esto escribiendo

$$[\mathbf{X}, \mathbf{P}] = i\hbar. \quad (8.30)$$

Esto en sí mismo es extremadamente importante. El hecho de que $\mathbf{X}$ y $\mathbf{P}$ no conmuten es la clave para entender por qué no son medibles simultáneamente. Pero las cosas se vuelven aún más interesantes cuando comparamos esta ecuación con la Equivalencia 8.27, que relaciona conmutadores con corchetes de Poisson clásicos. En

  28 

268 LECCIÓN 8. PARTÍCULAS Y ONDAS

de hecho, la Ec. 8.30 sugiere que el correspondiente corchete de Poisson clásico es

$$\{x, p\} = 1,$$

que es exactamente la relación clásica entre coordenadas y sus momentos conjugados (ver Volumen I, Lección 10, Ec. 8). En última instancia, es esta conexión la que explica por qué el concepto cuántico de momento está conectado con el concepto clásico.

Usando el principio de incertidumbre general de la Lección 5, ahora podemos especializarnos al caso

$$[\mathbf{X}, \mathbf{P}] = i\hbar,$$

y

$$\Delta \mathbf{X} \, \Delta \mathbf{P} \geq \frac{\hbar}{2}.$$

Haremos eso en la próxima sección.

Ahora recordemos el segundo principio que involucra conmutadores. En la Lección 4, encontramos que dos observables $\mathbf{L}$ y $\mathbf{M}$ no pueden determinarse simultáneamente a menos que conmuten. Si no conmutan, no puedes medir $\mathbf{L}$ sin interferir con una medición de $\mathbf{M}$. No es posible encontrar vectores propios simultáneos de dos observables que no conmutan. Esto llevó al principio de incertidumbre general.

  29 

8.5. EL PRINCIPIO DE INCERTIDUMBRE DE HEISENBERG 269

### 8.5 El Principio de Incertidumbre de Heisenberg

Y ahora, damas y caballeros, esto es lo que todos han estado esperando. Por fin: el Principio de Incertidumbre de Heisenberg.

El Principio de Incertidumbre de Heisenberg es uno de los resultados más famosos de la mecánica cuántica: no solo afirma que la posición y el momento de una partícula no pueden conocerse simultáneamente, sino que también proporciona un límite cuantitativo exacto para sus incertidumbres mutuas. En este punto, te sugiero que vuelvas a visitar la Lección 5, donde expliqué el principio de incertidumbre general. Hicimos todo el trabajo allí, y ahora cosechamos los beneficios.

Como hemos visto, el principio de incertidumbre general pone un límite cuantitativo a las incertidumbres simultáneas de dos observables $\mathbf{A}$ y $\mathbf{B}$. Esta idea se capturó en la Desigualdad 5.13:

$$\Delta \mathbf{A} \, \Delta \mathbf{B} \geq \frac{1}{2} |\langle \Psi | [\mathbf{A}, \mathbf{B}] | \Psi \rangle|.$$

Ahora apliquemos este principio directamente a los operadores de posición y momento $\mathbf{X}$ y $\mathbf{P}$. En este caso, el conmutador es solo un número y su valor esperado es ese mismo número. Reemplazando $\mathbf{A}$ y $\mathbf{B}$ con $\mathbf{X}$ y $\mathbf{P}$ da

$$\Delta \mathbf{X} \, \Delta \mathbf{P} \geq \frac{1}{2} |\langle \Psi | [\mathbf{X}, \mathbf{P}] | \Psi \rangle|,$$

y reemplazando $[\mathbf{X}, \mathbf{P}]$ con $i\hbar$ resulta en

  29 

270 LECCIÓN 8. PARTÍCULAS Y ONDAS

$$\Delta \mathbf{X} \, \Delta \mathbf{P} \geq \frac{1}{2} | i\hbar \langle \Psi | \Psi \rangle |.$$

Pero $\langle \Psi | \Psi \rangle = 1$, y el resultado final es

$$\Delta \mathbf{X} \, \Delta \mathbf{P} \geq \frac{1}{2} \hbar.$$

Ningún experimento puede superar jamás esta limitación. Puedes intentar lo mejor que puedas para determinar el momento y la posición de una partícula simultáneamente de manera reproducible, pero no importa cuán cuidadoso seas, la incertidumbre en la posición multiplicada por la incertidumbre en el momento nunca será menor que $\frac{1}{2}\hbar$.

Como vimos en la Sección 8.2.1, la función de onda de un estado propio de $\mathbf{X}$ está altamente concentrada alrededor de algún punto $x_0$; en este estado propio, la probabilidad también está perfectamente localizada. Por otro lado, la probabilidad $P(x)$ para un estado propio de momento está uniformemente extendida sobre todo el eje $x$. Para ver esto, tomemos la función de onda en la Ec. 8.17 y multipliquémosla por su complejo conjugado:

$$\psi_p^*(x) \psi_p(x) = \left( \frac{1}{\sqrt{2\pi}} e^{-\frac{ipx}{\hbar}} \right) \left( \frac{1}{\sqrt{2\pi}} e^{\frac{ipx}{\hbar}} \right) = \frac{1}{2\pi}.$$

El resultado es completamente uniforme, sin picos en ninguna parte del eje $x$. Evidentemente, un estado con momento definido es completamente incierto en su posición.

La Fig. 8.2 ilustra la definición de incertidumbre para la variable de posición $x$. En la mitad superior de la figura, puedes ver que la incertidumbre $\Delta x$ es una medida de cuán extendida está la función en relación con su valor esperado $\langle x \rangle$. La

  29 

8.5. EL PRINCIPIO DE INCERTIDUMBRE DE HEISENBERG 271

etiqueta $d$ muestra la desviación de un punto en relación con $\langle x \rangle$; esta puede ser una cantidad positiva o negativa. La incertidumbre $\Delta x$ es el resultado de un proceso de promediado sobre todas las $d$ posibles y caracteriza la función en su conjunto. Para evitar que las $d$ positivas cancelen a las negativas, cada valor de $d$ se eleva al cuadrado durante este proceso de promediado.

La mitad inferior de la Fig. 8.2 muestra cómo se puede simplificar el cálculo desplazando el origen para que coincida con $\langle x \rangle$. El valor numérico de $\Delta x$ no cambia con este desplazamiento.

 Figura 8.2: Conceptos Básicos de Incertidumbre. Arriba: $\langle x \rangle$ a la derecha del origen. Las desviaciones $d$ pueden ser positivas o negativas. La incertidumbre general $\Delta x$ ($> 0$) se deriva del valor promedio de $d^2$. Abajo: Origen desplazado a la derecha, $\langle x \rangle = 0$, $\Delta x$ tiene el mismo valor. 

---

[Fin de la Parte 3/5. Continuará con Capítulo 9...]

---

[PARTE 4/5 - Capítulo 9]

---

  29 

# Lección 9

## Dinámica de Partículas

Art y Lenny esperaban algo de acción en el Hilbert's Place. Pero todos los vectores de estado estaban absolutamente quietos —congelados, podría decirse.

Lenny: Esto es aburrido, Art. ¿Nunca pasa nada por aquí? Oye Hilbert, ¿por qué está este lugar tan parado?

Hilbert: Oh, no te preocupes. Las cosas se animarán en cuanto llegue el Hamiltoniano.

Art: ¿El Hamiltoniano? Suena como un tipo que realmente opera.¹

### 9.1 Un Ejemplo Sencillo

Los dos primeros volúmenes de la serie Mínimo Teórico se han centrado en gran medida en dos preguntas. La primera es: ¿Qué entendemos por sistema y cómo describimos los estados momentáneos de un sistema? Como hemos visto, las respuestas clásica y cuántica a esta pregunta son muy diferentes. El espacio de fases clásico

¹N. del T.: Juego de palabras intraducible entre "operator" (operador matemático) y "operator" (cirujano, operario).

  29 

274 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

—el espacio de coordenadas y momentos— se reemplaza en la teoría cuántica por el espacio vectorial lineal de estados.

La segunda gran pregunta es: ¿Cómo cambian los estados con el tiempo?

Tanto en mecánica clásica como en mecánica cuántica, la respuesta es según la **ley menos primera**. En otras palabras, los estados cambian de modo que la información y las distinciones nunca se borran. En mecánica clásica, este principio condujo a las ecuaciones de Hamilton y al teorema de Liouville. Anteriormente, en la Lección 4, expliqué cómo en mecánica cuántica esta ley condujo al principio de unitariedad, que a su vez condujo a la ecuación de Schrödinger general.

La Lección 8 trataba sobre la primera pregunta: ¿Cómo describimos el estado de una partícula? Ahora, en la lección actual, llegamos a la segunda pregunta, que podríamos reformular: ¿Cómo se mueven las partículas en mecánica cuántica?

En la Lección 4, expuse las reglas básicas de cómo cambian los estados cuánticos con el tiempo. El ingrediente esencial es el Hamiltoniano $\mathbf{H}$, que tanto en mecánica clásica como en mecánica cuántica representa la energía total de un sistema. En mecánica cuántica, el Hamiltoniano controla la evolución temporal de un sistema a través de la ecuación de Schrödinger dependiente del tiempo:

$$i\hbar \frac{\partial |\Psi\rangle}{\partial t} = \mathbf{H} |\Psi\rangle. \quad (9.1)$$

Esta lección trata sobre la **Ecuación de Schrödinger Original** —la ecuación que Schrödinger escribió para describir una partícula mecánico-cuántica. La Ecuación de Schrödinger Original es un caso especial de la Ec. 9.1.

El movimiento de partículas ordinarias (no relativistas) en mecánica clásica está gobernado por un Hamiltoniano, igual a la

  29 

9.1. UN EJEMPLO SENCILLO 275

energía cinética más la energía potencial. Pronto llegaremos a la versión cuántica de este Hamiltoniano, pero primero veamos un Hamiltoniano que es aún más simple.

Comenzaremos con el Hamiltoniano más simple que se me ocurre. En este caso, el operador Hamiltoniano $\mathbf{H}$ es una constante fija multiplicada por el operador de momento $\mathbf{P}$:

$$\mathbf{H} = c \mathbf{P}. \quad (9.2)$$

Este ejemplo rara vez se escribe, aunque resulta ser bastante instructivo. La constante $c$ es un número fijo. ¿Es $c\mathbf{P}$ un Hamiltoniano razonable para una partícula? Sí lo es, y en un momento descubriremos qué tipo de partícula describe. Por ahora, solo observa que la Ec. 9.2 es diferente de lo que podríamos esperar para una partícula no relativista. En otras palabras, no es $\mathbf{P}^2/2m$. Vale la pena explorar primero este ejemplo más simple, solo para ver cómo funciona el aparato matemático.

¿Cómo representamos este ejemplo en términos de funciones de onda $\psi(x)$ en la base de posiciones? Comenzaremos insertando nuestros operadores en la ecuación de Schrödinger dependiente del tiempo (Ec. 9.1):

$$i\hbar \frac{\partial \psi(x, t)}{\partial t} = -c i\hbar \frac{\partial \psi(x, t)}{\partial x}.$$

Observa que ahora estamos escribiendo $\psi$ como una función tanto de $x$ como de $t$. Cancelando los términos $i\hbar$ nos da

$$\frac{\partial \psi(x, t)}{\partial t} = -c \frac{\partial \psi(x, t)}{\partial x}, \quad (9.3)$$

  29 

276 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

que es una ecuación bastante simple. De hecho, cualquier función de $(x - ct)$ es una solución. Por "función de $(x - ct)$", me refiero a cualquier función que no dependa de $x$ y $t$ por separado, sino solo de la combinación $(x - ct)$. Para ver cómo funciona esto, considera una función arbitraria $\psi(x - ct)$ y observa sus derivadas.

Si tomas la parcial con respecto a $x$, obtienes

$$\frac{\partial \psi(x - ct)}{\partial x}$$

porque la derivada de $(x - ct)$ con respecto a $x$ es 1. Pero si tomas la parcial con respecto a $t$, obtienes

$$-c \frac{\partial \psi(x - ct)}{\partial t}.$$

Está claro que esta combinación de derivadas satisface la Ec. 9.3; por lo tanto, cualquier función de esta forma resuelve la ecuación de Schrödinger.

Ahora, veamos cómo se comporta una función $\psi(x - ct)$. ¿Qué aspecto tiene? ¿Cómo evoluciona con el tiempo? Supongamos que comenzamos observando una instantánea en $t = 0$. Podemos llamar a la instantánea $\psi(x)$ porque nos dice cómo se ve $\psi$ en cada punto del espacio en el tiempo específico $t = 0$. Por supuesto, no queremos cualquier función de $(x - ct)$. Queremos que la probabilidad total

$$\int_{-\infty}^{\infty} \psi^*(x)\psi(x) dx$$

sea igual a 1. En otras palabras, queremos que $\psi(x)$ decaiga agradablemente a cero en el infinito para que la integral no explote. La Fig.

  29 

9.1. UN EJEMPLO SENCILLO 277

 Figura 9.1: Paquete de Ondas de Forma Fija Moviéndose a Velocidad Constante $c$ 

9.1 muestra $\psi(x)$ esquemáticamente. Con estas características, tiene sentido llamar a $\psi(x)$ un **paquete de ondas**.

Ahora que hemos descrito la instantánea $\psi(x)$ en $t = 0$, ¿qué sucede si dejamos que el tiempo avance? A medida que $t$ aumenta, el paquete de ondas mantiene exactamente la misma forma. Cada característica de la función de valor complejo $\psi(x, t)$ se mueve con velocidad uniforme $c$ hacia la derecha.²

Tuve una razón para darle el nombre $c$ a nuestra constante —el símbolo $c$ a menudo representa la velocidad de la luz. Entonces, ¿es esta partícula un fotón? No, en realidad no. Pero nuestra descripción de esta partícula hipotética está bastante cerca de la descripción correcta de un neutrino que se mueve a la velocidad de la luz. (Los

²Esto incluye tanto la parte real como la imaginaria de $\psi(x)$.

  29 

278 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

neutrinos reales probablemente se mueven a una velocidad que es inmensamente menor que la velocidad de la luz). Este Hamiltoniano sería una muy buena descripción de un neutrino unidimensional excepto por un problema: la partícula descrita por nuestra función de onda solo puede moverse hacia la derecha. Para completar esta descripción, tendríamos que añadir otra posibilidad —que la partícula también pudiera moverse hacia la izquierda.³

Nuestro zaxón⁴ diestro tiene otra característica peculiar: su energía puede ser positiva o negativa. Esto se debe a que el operador $\mathbf{P}$, como vector, puede tomar valores positivos o negativos. En general, la energía de una partícula con momento negativo es negativa, y la energía de una partícula con momento positivo es positiva. No diré más sobre esto excepto que el problema de la energía negativa para este tipo de partícula fue resuelto por Dirac, quien lo utilizó para establecer la base teórica de las antipartículas. Para nuestros propósitos, podemos ignorar este problema y simplemente permitir que la energía de nuestra partícula sea positiva o negativa.

Dado que la función de onda de nuestra partícula se mueve rígidamente a lo largo del eje $x$, también lo hace la distribución de probabilidad. Como resultado, el valor esperado de $x$ se mueve exactamente de la misma manera, es decir, se mueve hacia la derecha con velocidad $c$. Esa es la mecánica cuántica esencial de este sistema. Sin embargo, hay otra cosa importante a tener en cuenta. Cuando dijimos que la velocidad $c$ es una constante fija,

³Nuestras partículas diestras me recuerdan el cuento clásico de Dr. Seuss "The Zax", y me siento tentado a llamarlos "zaxones diestros". No se sabe cómo habría resultado la historia si Theodor Geisel hubiera sabido más sobre neutrinos.

⁴N. del T.: "Zaxon" es una adaptación del término "zax" del cuento de Dr. Seuss, usado en el texto original.

  30 

9.1. UN EJEMPLO SENCILLO 279

no estábamos bromeando. Nuestra partícula solo puede existir en un estado en el que se mueve a esta velocidad particular. Nunca puede frenar o acelerar.

¿Cómo se compara esto con la descripción clásica de tal partícula? Comenzando con el mismo Hamiltoniano, un físico clásico simplemente escribiría las ecuaciones de Hamilton. Con $H = cP$, las ecuaciones de Hamilton son

$$\frac{\partial H}{\partial p} = \dot{x}$$

y

$$\frac{\partial H}{\partial x} = -\dot{p}.$$

Realizando las derivadas parciales, estas se convierten en

$$\frac{\partial H}{\partial p} = \dot{x} = c$$

y

$$\frac{\partial H}{\partial x} = -\dot{p} = 0.$$

Por lo tanto, en la descripción clásica de nuestra partícula, el momento se conserva y la posición se mueve con velocidad fija $c$. En la descripción mecánico-cuántica, toda la distribución de probabilidad y el valor esperado se mueven con velocidad $c$. En otras palabras, el valor esperado de la posición se comporta según las ecuaciones clásicas del movimiento.

  30 

280 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

### 9.2 Partículas Libres No Relativistas

Solo las partículas sin masa pueden moverse a la velocidad de la luz y, añadiría, solo pueden moverse a esa velocidad. Todas las partículas conocidas, excepto los fotones y los gravitones, tienen masa y pueden moverse a cualquier velocidad menor que $c$. Cuando se mueven con una velocidad mucho menor que $c$, se dice que son no relativistas y su movimiento está gobernado por la mecánica newtoniana ordinaria, al menos clásicamente. La primera aplicación de la mecánica cuántica fue al movimiento de partículas no relativistas.

Mostré anteriormente (en las Lecciones 4 y 8) que los corchetes de Poisson juegan el mismo papel matemático en la mecánica clásica que los conmutadores en la mecánica cuántica. Escritas con estos constructos, las ecuaciones de movimiento clásicas y cuánticas son casi idénticas en forma. En particular, el Hamiltoniano entra en juego de la misma manera con los corchetes de Poisson que con los conmutadores. Por lo tanto, si quieres escribir las ecuaciones mecánico-cuánticas de un sistema cuya física clásica ya conoces, es muy razonable intentar usar el Hamiltoniano clásico, traducido a forma de operador.

Para una partícula libre no relativista, el Hamiltoniano natural para probar es $p^2/2m$. Cuando decimos que la partícula es libre, lo que realmente queremos decir es que no actúan fuerzas sobre ella y, por lo tanto, podemos ignorar la energía potencial. Todo lo que nos importa es la energía cinética, que se define como

$$T = \frac{1}{2} m v^2.$$

Como recordarás, el momento de una partícula clásica es

  30 

9.2. PARTÍCULAS LIBRES NO RELATIVISTAS 281

$$p = m v.$$

El Hamiltoniano es solo la energía cinética, que podemos escribir en términos del momento $p$. Esto nos da

$$H = \frac{1}{2} m v^2 = \frac{p^2}{2m}$$

para el Hamiltoniano de una partícula libre no relativista clásica. A diferencia del zaxón diestro del ejemplo anterior, la energía de esta partícula no depende de su dirección de movimiento. Esto se debe a que la energía es proporcional a $p^2$ en lugar de a $p$ mismo. Así que comenzaremos con una partícula cuya energía es $p^2/2m$ y desarrollaremos la ecuación de Schrödinger (la original que Schrödinger descubrió) para una partícula libre.

Nuestro plan es seguir el mismo proceso que usamos en el ejemplo anterior, utilizando el Hamiltoniano para escribir una ecuación de Schrödinger dependiente del tiempo. Como es habitual, el lado izquierdo de la ecuación es

$$i\hbar \frac{\partial \psi}{\partial t}.$$

Derivaremos el lado derecho reescribiendo el Hamiltoniano clásico —la energía cinética— como un operador. La energía cinética clásica es

$$p^2/2m.$$

La versión cuántica reemplaza $p$ con $\mathbf{P}$:

  30 

282 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

$$\mathbf{H} = \mathbf{P}^2/2m.$$

¿Cuál es el significado de esto? Como hemos visto, el operador $\mathbf{P}$ se define como

$$\mathbf{P} = -i\hbar \frac{\partial}{\partial x}.$$

El cuadrado de $\mathbf{P}$ es simplemente el operador que se obtiene al permitir que $\mathbf{P}$ actúe dos veces sucesivamente. Por lo tanto,

$$\mathbf{P}^2 = (-i\hbar \frac{\partial}{\partial x})(-i\hbar \frac{\partial}{\partial x}),$$

o

$$\mathbf{P}^2 = -\hbar^2 \frac{\partial^2}{\partial x^2},$$

y el Hamiltoniano se convierte en

$$\mathbf{H} = -\frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2}.$$

Finalmente, si igualamos los lados izquierdo y derecho de la ecuación de Schrödinger dependiente del tiempo, obtenemos

$$i\hbar \frac{\partial \psi}{\partial t} = -\frac{\hbar^2}{2m} \frac{\partial^2 \psi}{\partial x^2}. \quad (9.4)$$

Esta es la ecuación de Schrödinger tradicional para una partícula libre no relativista ordinaria. Es un tipo particular de ecuación de onda, pero, en contraste con el ejemplo anterior, las ondas

  30 

9.3. ECUACIÓN DE SCHRÖDINGER INDEPENDIENTE DEL TIEMPO 283

de diferentes longitudes de onda (y momentos) se mueven con diferentes velocidades. Debido a esto, la función de onda no mantiene su forma. A diferencia de la función de onda del zaxón, tiende a extenderse y desintegrarse. Esto se muestra esquemáticamente en la Fig. 9.2.

 Figura 9.2: Paquete de Ondas Típico para una Partícula Libre No Relativista. Arriba: El paquete de ondas inicial es compacto y altamente localizado. Abajo: Con el tiempo, el paquete de ondas se mueve hacia la derecha y se extiende. 

### 9.3 Ecuación de Schrödinger Independiente del Tiempo

Vamos a resolver la ecuación de Schrödinger dependiente del tiempo para partículas libres no relativistas, pero primero necesitamos

  30 

284 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

resolver la versión independiente del tiempo. La ecuación independiente del tiempo es esencialmente la ecuación de vectores propios para el Hamiltoniano,

$$\mathbf{H} |\Psi\rangle = E |\Psi\rangle,$$

escrita explícitamente en términos de la función de onda $\psi(x)$:

$$-\frac{\hbar^2}{2m} \frac{\partial^2 \psi(x)}{\partial x^2} = E \psi(x). \quad (9.5)$$

Es muy fácil encontrar un conjunto completo de vectores propios que satisfagan esta ecuación. De hecho, los vectores propios del momento hacen el trabajo. Probemos la función

$$\psi(x) = e^{\frac{ipx}{\hbar}} \quad (9.6)$$

como una posible solución. Realizando las derivadas, encontramos que esta función es efectivamente una solución de la Ec. 9.5, siempre que establezcamos

$$E = \frac{p^2}{2m}. \quad (9.7)$$

Esto no debería ser una sorpresa —después de todo, $E$ representa un valor propio de energía en la Ec. 9.5.

**Ejercicio 9.1:** Deriva la Ec. 9.7 insertando la Ec. 9.6 en la Ec. 9.5.

Como vimos en la Sección 4.13, cada solución de la ecuación de Schrödinger independiente del tiempo nos permite construir una solución dependiente del tiempo.

  30 

9.3. ECUACIÓN DE SCHRÖDINGER INDEPENDIENTE DEL TIEMPO 285

Todo lo que necesitamos hacer es multiplicar la solución independiente del tiempo —en este caso $e^{\frac{ipx}{\hbar}}$— por $e^{-\frac{i E t}{\hbar}} = e^{-\frac{i p^2 t}{2m\hbar}}$. Por lo tanto, un conjunto completo de soluciones puede escribirse como

$$\psi(x, t) = \exp \frac{i(px - \frac{p^2 t}{2m})}{\hbar}.$$

Cualquier solución es una suma, o integral, de estas soluciones:

$$\psi(x, t) = \int \tilde{\psi}(p) \exp \frac{i(px - \frac{p^2 t}{2m})}{\hbar} dp.$$

Puedes comenzar con cualquier función de onda en $t = 0$, encontrar $\tilde{\psi}(p)$ mediante la transformada de Fourier, y dejar que evolucione. La forma cambiará porque las ondas para diferentes valores de $p$ viajan a diferentes velocidades. Pero, como pronto veremos, el paquete de ondas en general viajará a la velocidad $\langle p/m \rangle$ tal como lo haría una partícula clásica.

Esta solución general simple tiene una implicación importante. Entre otras cosas, dice que la función de onda en la representación de momentos cambia con el tiempo de una manera muy simple:

$$\tilde{\psi}(p, t) = \tilde{\psi}(p) \exp \frac{i(px - \frac{p^2 t}{2m})}{\hbar}.$$

En otras palabras, solo la fase cambia con el tiempo, mientras que la magnitud permanece constante. Lo que hace esto tan interesante es que la probabilidad $P(p)$ no cambia en absoluto con el tiempo. Esto, por supuesto, es una consecuencia de la conservación del momento, pero solo se cumple si no hay fuerzas actuando sobre la partícula.

  30 

286 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

### 9.4 Velocidad y Momento

Hasta ahora, no he explicado la conexión entre el operador $\mathbf{P}$ y la noción clásica de momento —es decir, masa por velocidad, o

$$v = p/m. \quad (9.8)$$

¿Qué entendemos por la velocidad de una partícula mecánico-cuántica? La respuesta más simple es que nos referimos a la derivada temporal de la posición promedio $\langle \Psi | \mathbf{X} | \Psi \rangle$:

$$v = \frac{d \langle \Psi | \mathbf{X} | \Psi \rangle}{dt}$$

o, más concretamente, en términos de funciones de onda,

$$v = \frac{d}{dt} \int \psi^*(x, t) \, x \, \psi(x, t) dx.$$

¿Por qué $\langle \Psi | \mathbf{X} | \Psi \rangle$ varía con el tiempo? Porque $\psi$ depende del tiempo, y de hecho sabemos exactamente cómo. La dependencia temporal de $\psi$ está gobernada por la ecuación de Schrödinger dependiente del tiempo. Podríamos usar ese hecho para deducir cómo $\langle \Psi | \mathbf{X} | \Psi \rangle$ varía con el tiempo. Lo he hecho de esta manera —por fuerza bruta— y lleva varias páginas. Afortunadamente, los métodos abstractos que aprendiste en lecciones anteriores lo hacen más fácil; de hecho, ya hemos hecho la mayor parte del trabajo en la Lección 4. De hecho, antes de continuar, te recomiendo que repases la Lección 4, especialmente la Sección 4.9, desde el principio hasta la aparición de la Ec. 4.17. Para reafirmar la Ec. 4.17,

  30 

9.4. VELOCIDAD Y MOMENTO 287

$$\frac{d}{dt} \langle \mathbf{L} \rangle = \frac{i}{\hbar} \langle [ \mathbf{H}, \mathbf{L} ] \rangle.$$

En palabras: la derivada temporal del valor esperado de cualquier observable $\mathbf{L}$ está dada por $i/\hbar$ veces el valor esperado del conmutador del Hamiltoniano con $\mathbf{L}$. Aplicando este principio a la velocidad $v$, encontramos que

$$v = \frac{i}{2m\hbar} \langle [ \mathbf{P}^2, \mathbf{X} ] \rangle. \quad (9.9)$$

Ahora, todo lo que tenemos que hacer es calcular el conmutador de $\mathbf{P}^2$ y $\mathbf{X}$. Un par de pasos simples muestra que

$$[ \mathbf{P}^2, \mathbf{X} ] = \mathbf{P}[ \mathbf{P}, \mathbf{X} ] + [ \mathbf{P}, \mathbf{X} ] \mathbf{P}. \quad (9.10)$$

Esta relación puede confirmarse expandiendo cada conmutador y detectando algunas cancelaciones obvias.

**Ejercicio 9.2:** Demuestra la Ec. 9.10 expandiendo cada lado y comparando los resultados.

El último paso utiliza la relación de conmutación estándar

$$[ \mathbf{P}, \mathbf{X} ] = -i\hbar.$$

Sustituyendo esto en la Ec. 9.10 e insertando ese resultado en la Ec. 9.9, encontramos que

$$v = \frac{\langle \mathbf{P} \rangle}{m}$$

  30 

288 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

o, quizás de manera más familiar,

$$\langle \mathbf{P} \rangle = m v. \quad (9.11)$$

Hemos probado exactamente lo que nos propusimos probar: el momento es igual a la masa por la velocidad, o, más exactamente, el momento promedio es igual a la masa por la velocidad.

Para tener una mejor idea de lo que esto significa, supongamos que la función de onda tiene la forma de un paquete, o un bulto bastante estrecho. El valor esperado de $x$ estará aproximadamente en el centro del bulto. Lo que nos dice la Ec. 9.11 es que el centro del paquete de ondas viaja según la regla clásica $p = mv$.

### 9.5 Cuantización

Antes de pasar al tema de las fuerzas en mecánica cuántica, quiero hacer una pausa y discutir lo que hemos hecho. Comenzamos con un sistema clásico bien conocido y confiable —la partícula libre— y lo **cuantizamos**. Podemos codificar este procedimiento de la siguiente manera:

1. Comienza con un sistema clásico. Esto significa un conjunto de coordenadas $x$ y momentos $p$. En nuestro ejemplo, solo había una coordenada y un momento, pero el procedimiento es fácil de generalizar. Las coordenadas y los momentos vienen en pares, $x_i$ y $p_i$. El sistema clásico también tiene un Hamiltoniano, que es una función de las $x$ y las $p$.

  31 

9.5. CUANTIZACIÓN 289

2. Reemplaza el espacio de fases clásico con un espacio vectorial lineal. En la representación de posiciones, el espacio de estados está representado por una función de onda $\psi(x)$ que depende de las coordenadas —en general, de todas ellas.

3. Reemplaza las $x$ y las $p$ con operadores $\mathbf{X}_i$ y $\mathbf{P}_i$. Cada $\mathbf{X}_i$ actúa sobre la función de onda para multiplicarla por $x_i$. Cada $\mathbf{P}_i$ actúa según la regla

$$\mathbf{P}_i \rightarrow -i\hbar \frac{\partial}{\partial x_i}.$$

4. Cuando se realizan estos reemplazos, el Hamiltoniano se convierte en un operador que puede usarse en la ecuación de Schrödinger dependiente del tiempo o independiente del tiempo. La ecuación dependiente del tiempo nos dice cómo cambia la función de onda con el tiempo. La forma independiente del tiempo nos permite encontrar los vectores propios y valores propios del Hamiltoniano.

Este procedimiento de **cuantización** es el medio por el cual las ecuaciones clásicas de un sistema se convierten en ecuaciones cuánticas. Se ha utilizado una y otra vez, en campos que van desde el movimiento de partículas hasta la electrodinámica cuántica; incluso ha habido intentos (no muy exitosos) de cuantizar la teoría de la gravedad de Einstein. Como vimos en un caso simple, el procedimiento garantiza que el movimiento de los valores esperados esté estrechamente relacionado con el movimiento clásico.

Todo esto plantea una pregunta del "huevo y la gallina": ¿Qué viene primero —la teoría clásica o la teoría cuántica? ¿Debería

  31 

290 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

el punto de partida lógico de la física ser la mecánica clásica o la mecánica cuántica? Creo que la respuesta es obvia. La mecánica cuántica es la descripción real de la naturaleza. La mecánica clásica, aunque hermosa y elegante, es sin embargo una aproximación. En términos generales, se cumple cuando las funciones de onda mantienen su forma como paquetes.

A veces, tenemos suerte y la teoría cuántica de un sistema puede adivinarse —y eso es todo lo que es, una conjetura— comenzando con un sistema clásico familiar y cuantizándolo. A veces esto funciona. El movimiento cuántico de los electrones, deducido de la mecánica clásica de partículas, es un caso concreto. La electrodinámica cuántica, deducida de las ecuaciones de Maxwell, es otro. Pero a veces no hay una teoría clásica para usar como punto de partida. El espín de una partícula no tiene un verdadero equivalente clásico. Y la cuantización de la relatividad general ha fracasado en gran medida. La teoría cuántica es probablemente mucho más fundamental que la teoría clásica, que generalmente debe entenderse como una aproximación.

Dicho esto, ahora continuaré cuantizando el movimiento de partículas, pero esta vez incorporando los efectos de las fuerzas.

### 9.6 Fuerzas

El mundo sería un lugar aburrido si todas las partículas fueran libres. Las fuerzas son lo que hace que las partículas hagan cosas interesantes, como ensamblarse en átomos, moléculas, barras de chocolate y agujeros negros. La fuerza sobre una partícula dada es la suma total de las fuerzas ejercidas sobre ella por todas las demás partículas del universo. En la práctica, generalmente asumimos que conocemos

  31 

9.6. FUERZAS 291

lo que están haciendo todas las demás partículas y reemplazamos su efecto por una función de energía potencial para la partícula que estamos estudiando. Esto es cierto tanto en mecánica clásica como en mecánica cuántica.

La función de energía potencial se denota por $V(x)$. En mecánica clásica está relacionada con la fuerza sobre una partícula mediante la ecuación

$$F(x) = -\frac{\partial V}{\partial x}.$$

Si el movimiento es unidimensional, la derivada parcial puede reemplazarse por una derivada ordinaria, pero lo dejaré como está. Si luego combinamos esta ecuación con la segunda ley de Newton, $F = ma$, obtenemos

$$m \frac{d^2 x}{dt^2} = -\frac{\partial V}{\partial x}.$$

En mecánica cuántica, procedemos de manera diferente; escribimos un Hamiltoniano y resolvemos la ecuación de Schrödinger. Incorporar la energía potencial en este programa es sencillo. La energía potencial $V(x)$ se convierte en un operador $\mathbf{V}$ que se suma al Hamiltoniano.

¿Qué tipo de operador es $\mathbf{V}$? La respuesta es más fácil de expresar si pensamos en el lenguaje de las funciones de onda en lugar de en términos de bras y kets abstractos. Cuando el operador $\mathbf{V}$ actúa sobre cualquier función de onda $\psi(x)$, multiplica la función de onda por la función $V(x)$.

$$\mathbf{V} |\Psi\rangle \rightarrow V(x) \psi(x).$$

  31 

292 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

Al igual que en mecánica clásica, una vez que se incluyen las fuerzas, el momento de una partícula no se conserva. De hecho, las leyes de movimiento de Newton pueden enunciarse en la forma

$$\frac{dp}{dt} = F$$

o

$$\frac{dp}{dt} = -\frac{\partial V}{\partial x}. \quad (9.12)$$

Las reglas de la cuantización requieren que sumemos $\mathbf{V}(x)$ al Hamiltoniano,⁵

$$\mathbf{H} = \frac{\mathbf{P}^2}{2m} + \mathbf{V}(x), \quad (9.13)$$

y modifiquemos las ecuaciones de Schrödinger de la manera obvia:

$$i\hbar \frac{\partial \psi}{\partial t} = -\frac{\hbar^2}{2m} \frac{\partial^2 \psi}{\partial x^2} + V(x) \psi$$
$$E \psi = -\frac{\hbar^2}{2m} \frac{\partial^2 \psi}{\partial x^2} + V(x) \psi. \quad (9.14)$$

¿Qué efecto tiene esto? El término adicional ciertamente afecta la forma en que $\psi$ cambia con el tiempo. Eso, por supuesto, debe ser así si la posición promedio de un paquete de ondas debe seguir una trayectoria clásica. Para comprobar nuestro razonamiento, veamos

⁵Técnicamente, esto también es cierto para partículas libres. Sin embargo, en el caso de partículas libres, establecemos $V(x)$ igual a 0.

  31 

9.6. FUERZAS 293

si lo hace. En primer lugar, ¿la Ec. 9.11 sigue siendo válida? Debería serlo, porque la conexión entre momento y velocidad no se ve afectada por la presencia de fuerzas.

Debido a que se ha añadido un nuevo término a $\mathbf{H}$, habrá un nuevo término en el conmutador de $\mathbf{X}$ y $\mathbf{H}$. Potencialmente, eso podría modificar la expresión para la velocidad en la Ec. 9.9, pero es fácil ver que esto no sucede. El nuevo término involucra el conmutador de $\mathbf{X}$ con $\mathbf{V}(x)$. Pero multiplicar por $x$ y multiplicar por una función de $x$ son operaciones que conmutan. En otras palabras,

$$[\mathbf{X}, \mathbf{V}(x)] = 0.$$

Por lo tanto, la conexión entre velocidad y momento no se ve afectada por las fuerzas en mecánica cuántica, como es el caso en mecánica clásica.

La pregunta más interesante es: ¿Podemos entender la versión cuántica de la ley de Newton? Como se indicó anteriormente, esta ley puede escribirse como

$$\frac{dp}{dt} = F.$$

Calculemos la derivada temporal del valor esperado de $\mathbf{P}$. De nuevo, el truco es conmutar $\mathbf{P}$ con el Hamiltoniano:

$$\frac{d}{dt} \langle \mathbf{P} \rangle = \frac{i}{2m\hbar} \langle [\mathbf{P}^2, \mathbf{P}] \rangle + \frac{i}{\hbar} \langle [\mathbf{V}, \mathbf{P}] \rangle. \quad (9.15)$$

El primer término es cero porque un operador conmuta con cualquier función de sí mismo. Para calcular el segundo término, usaremos

  31 

294 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

una ecuación que aún no hemos demostrado:

$$[\mathbf{V}(x), \mathbf{P}] = i\hbar \frac{dV(x)}{dx}. \quad (9.16)$$

Insertando la Ec. 9.16 en la Ec. 9.15, obtenemos

$$\frac{d}{dt} \langle \mathbf{P} \rangle = -\langle \frac{dV}{dx} \rangle.$$

Ahora, demostremos la Ec. 9.16. Dejando que el conmutador actúe sobre una función de onda, podemos escribir

$$[\mathbf{V}(x), \mathbf{P}] \psi(x) = V(x) \left( -i\hbar \frac{d}{dx} \right) \psi(x) - \left( -i\hbar \frac{d}{dx} \right) V(x) \psi(x). \quad (9.17)$$

Esto se simplifica fácilmente y da como resultado la Ec. 9.16. Por lo tanto, hemos demostrado que

$$\frac{d}{dt} \langle \mathbf{P} \rangle = -\langle \frac{dV}{dx} \rangle, \quad (9.18)$$

que es el análogo cuántico de la ecuación de Newton para la tasa de cambio temporal del momento.

**Ejercicio 9.3:** Muestra que el lado derecho de la Ec. 9.17 se simplifica al lado derecho de la Ec. 9.16. Pista: Primero expande el segundo término tomando la derivada del producto. Luego busca cancelaciones.

  31 

9.7. MOVIMIENTO LINEAL Y LÍMITE CLÁSICO 295

### 9.7 Movimiento Lineal y el Límite Clásico

Podrías pensar que hemos demostrado que el valor esperado de $\mathbf{X}$ sigue exactamente la trayectoria clásica. Pero lo que realmente hemos demostrado es bastante diferente. Esta diferencia existe porque el promedio de una función de $x$ no es lo mismo que la función del promedio de $x$. Si la Ec. 9.18 hubiera sido

$$\frac{d}{dt} \langle \mathbf{P} \rangle = -\frac{dV(\langle x \rangle)}{d\langle x \rangle} \quad [\text{¡Esto es incorrecto!}]$$

(y, déjame enfatizar, no lo es), entonces efectivamente diríamos que la posición y el momento promedio satisfacen las ecuaciones clásicas. Pero en realidad las ecuaciones clásicas son solo aproximaciones, buenas siempre que podamos reemplazar el promedio de $dV/dx$ por la función del promedio de $x$. ¿Cuándo es razonable hacer esto? La respuesta es siempre que $V(x)$ varíe lentamente en comparación con el tamaño del paquete de ondas. Si $V$ varía rápidamente a través del paquete de ondas, la aproximación clásica fallará. De hecho, en esa situación, un paquete de ondas agradable y estrecho se romperá en una onda mal dispersa que no se parecerá en nada al paquete de ondas original. La función de probabilidad también se dispersará. Entonces no tendrás más remedio que resolver la ecuación de Schrödinger.

Examinemos este punto más de cerca. Matemáticamente, no hemos hecho suposiciones sobre las formas de nuestros paquetes de ondas. Pero tácitamente los hemos imaginado como funciones bien formadas con un solo máximo, que se desvanecen suavemente hacia cero en las direcciones positiva y negativa. Esta con-

  31 

296 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

dición, aunque no es explícita en nuestras suposiciones matemáticas, tiene un impacto real en si una partícula se comporta como la mecánica clásica nos llevaría a esperar.

 Figura 9.3: Función Bimodal (de Dos Jorobas), Centrada en $x = 0$. Nótese que $\langle x \rangle = 0$, pero $\Delta x > 0$. 

Para ilustrar este punto, consideremos un paquete de ondas ligeramente "extraño". La Fig. 9.3 muestra un paquete de ondas bimodal (que tiene dos máximos), centrado en el origen del eje $x$. Ahora, consideremos alguna función de $x$, digamos $F(x)$, donde $F$ representa la fuerza. El valor esperado de $F(x)$ no es lo mismo que la función $F$ del valor esperado de $x$. En otras palabras,

$$\langle F(x) \rangle \neq F(\langle x \rangle).$$

El lado derecho es una función del centro del paquete de ondas. No es lo mismo que el lado izquierdo, que corres-

  31 

9.7. MOVIMIENTO LINEAL Y LÍMITE CLÁSICO 297

ponde a nuestros resultados de la sección anterior —$\langle F(x) \rangle$ tiene la misma forma que el lado derecho de la Ec. 9.18.⁶

Permíteme darte un ejemplo donde estas dos expresiones podrían ser extremadamente diferentes. Supongamos que $F$ es igual a $x$ al cuadrado:

$$F = x^2.$$

Y supongamos que el paquete de ondas se ve como la Fig. 9.3. ¿Cuál es el valor esperado de $x$? Es cero, y también lo es $F(\langle x \rangle)$, porque $F(0) = 0^2 = 0$. Por otro lado, ¿cuál es el valor esperado de $x^2$? Es mayor que cero. Así que cuando un paquete de ondas no es un bulto único y agradable que se caracteriza principalmente por su centro, no siempre es cierto que la tasa de cambio temporal del momento sea la fuerza evaluada en el valor esperado de $x$. Es solo cuando la función de onda está concentrada en un rango bastante estrecho que el valor esperado de $F(x)$ es el mismo que $F(\langle x \rangle)$. Así que hemos hecho un poco de trampa al decir que nuestra ecuación de movimiento cuántica parece clásica. Eso depende de que el paquete de ondas sea coherente y esté bien localizado.

En igualdad de condiciones, cuando la masa de una partícula es grande, la función de onda tiende a estar muy bien concentrada. Si no hay picos muy agudos en la función potencial $V(x)$, entonces será una buena aproximación reemplazar $\langle F(x) \rangle$ con $F(\langle x \rangle)$. Cuando $V(x)$ tiene picos, sin embargo, el paquete de ondas tiende a romperse. Por ejemplo, supongamos que tenemos un buen paquete de ondas moviéndose hacia la derecha, y choca con una estructura puntual, como un átomo, con una función potencial simi-

⁶Recuerda que $-\langle \frac{dV}{dx} \rangle$ representa la fuerza en esa ecuación.

  31 

298 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

lar a la Fig. 9.4. El paquete de ondas se extenderá y se desintegrará. Si, por otro lado, choca con un potencial muy suave, entonces atravesará el potencial suave, moviéndose más o menos según las ecuaciones clásicas del movimiento. No esperamos que la mecánica cuántica reproduzca la mecánica clásica en cada circunstancia posible. Esperamos que reproduzca la mecánica clásica en circunstancias donde debería hacerlo —donde las partículas son pesadas, los potenciales son suaves y nada causa que la función de onda se desintegre o se disperse.⁷

 Figura 9.4: Función Potencial con Picos. Las funciones potenciales con picos agudos tienden a hacer que las funciones de onda se dispersen. Cuanto más pequeñas sean estas características en relación con el paquete de ondas, más se dispersará el paquete de ondas y menos "clásico" se volverá. 

¿Qué situaciones físicas conducen a "potenciales malos" que rompen la función de onda? Supongamos que un potencial tiene ca-

⁷No tan elocuente como la frase final de Garrison Keillor, pero cierto de todos modos.

  32 

9.7. MOVIMIENTO LINEAL Y LÍMITE CLÁSICO 299

racterísticas que tienen un cierto tamaño asociado. Piensa en la Fig. 9.4 en esteroides, con muchos picos grandes y muy juntos. Supongamos que llamamos al tamaño de estas características $\delta x$, y que $\delta x$ es significativamente más pequeño que la incertidumbre en la posición de la partícula entrante:

$$\delta x < \Delta x.$$

Si las características agudas de $V(x)$ existen en una escala que es mucho más pequeña que el tamaño del paquete de ondas entrante, el paquete se romperá en muchos pedazos pequeños. Cada uno se dispersará en una dirección diferente.

En términos generales, cuando las características del potencial son más cortas que la longitud de onda de la partícula entrante, la función de onda tenderá a romperse.

Digamos que tomas una bola de boliche y preguntas: "¿Cuál es $\Delta x$?" Podemos usar el principio de incertidumbre para obtener algo de intuición sobre esta pregunta. Típicamente, $\Delta p \times \Delta x$ es mayor que $\hbar$. Pero en muchos casos razonables es del orden de $\hbar$:

$$\Delta p \, \Delta x \sim \hbar.$$

Ahora, $p$ está tan concentrado como puede estarlo, pero para un objeto macroscópico ordinario, la relación de incertidumbre está más o menos saturada —el lado izquierdo es aproximadamente igual a $\hbar$. Las razones para esto son muy complicadas y no entraré en ellas aquí. En cambio, supongamos que esto es cierto y analicemos las implicaciones. ¿Qué es $\Delta p$? Es $m \Delta v$, lo que nos da

$$m \Delta v \, \Delta x \sim \hbar.$$

  32 

300 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

Reordenando los símbolos, podemos escribir entonces

$$\Delta v \, \Delta x \sim \frac{\hbar}{m}$$

o

$$\Delta x \sim \frac{\hbar}{m \Delta v}.$$

Ahora, si pongo una bola de boliche en el suelo, sé muy bien que la incertidumbre en su velocidad no es muy grande. A medida que la bola se vuelve más y más pesada, cabría esperar que la incertidumbre en la velocidad se vuelva más y más pequeña. Pero, en cualquier caso, el lado derecho tiene una $m$ en el denominador, e independientemente de $\Delta v$, a medida que $m$ se hace más pequeña, $\Delta x$ se hará más grande. Y en particular, tenderá a hacerse más grande que las características del potencial.

En el límite de la mecánica cuántica, donde $m$ es muy pequeña y $\Delta x$ tiende a ser grande, la función de onda se moverá bajo la influencia de un potencial irregular, que percibe como mucho más agudo y con más características que la propia función de onda. Eso es cuando la función de onda se rompe. Por otro lado, a medida que $m$ se hace muy grande, $\Delta x$ se hace pequeño. Para una bola de boliche grande, el paquete de ondas podría estar muy concentrado. Cuando se mueve a través de un potencial con picos, esta diminuta función de onda encuentra un potencial cuyas características son (comparativamente) muy amplias. Moverse a través de características amplias y suaves no rompe la función de onda en pedazos. Las masas grandes y los potenciales suaves caracterizan el límite clásico. Una partícula con baja masa, moviéndose a través de un potencial abrupto, se comporta como un sistema mecánico-cuántico.

  32 

9.8. INTEGRALES DE TRAYECTORIA 301

¿Qué pasa con los electrones? ¿Son lo suficientemente masivos como para comportarse clásicamente? La respuesta depende de la interacción entre el potencial y la masa. Por ejemplo, si tienes dos placas de condensador separadas por un centímetro, con un campo eléctrico suave entre ellas, entonces el electrón se moverá a través del espacio como una partícula clásica agradable, coherente y casi clásica. Por otro lado, el potencial asociado con el núcleo de un átomo siempre tiene una característica aguda. Si un paquete de ondas de electrones choca con este potencial, se dispersará por todas partes.

Antes de dejar este tema, me gustaría mencionar los **paquetes de ondas de mínima incertidumbre**. Estos son paquetes de ondas donde $\Delta x \Delta p$ es igual a $\hbar/2$ (en lugar de ser mayor). En otras palabras, en estos casos, $\Delta x \Delta p$ es tan pequeño como la mecánica cuántica permite. Estos paquetes de ondas tienen la forma de una curva gaussiana, y a menudo se llaman paquetes de ondas gaussianos. Con el tiempo, se extienden y se aplanan. Tales paquetes de ondas no son tan comunes, pero existen. Una bola de boliche en reposo es una buena aproximación. En la Lección 10, veremos que el estado fundamental de un oscilador armónico es un paquete de ondas gaussiano.

### 9.8 Integrales de Trayectoria

La mecánica hamiltoniana clásica se centra en los cambios incrementales paso a paso en el estado de un sistema. Pero hay otra forma de formular la mecánica —el **Principio de Mínima Acción**— en el que el enfoque está en historias completas. Para una partícula, esto significa observar la trayectoria completa de la partícula desde algún tiempo inicial hasta algún tiempo final. El contenido de los dos enfoques es el mismo, pero el énfasis es diferen-

  32 

302 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

te. La mecánica hamiltoniana se centra en un instante y te dice cómo cambia el sistema entre ese instante y el siguiente. El principio de mínima acción da un paso atrás y adopta una visión global. Uno puede imaginar que la naturaleza muestrea todas las trayectorias posibles y elige la que minimiza la acción entre un par de puntos inicial y final fijos.⁸

La mecánica cuántica también tiene una descripción hamiltoniana que se concentra en cambios incrementales. Se llama la ecuación de Schrödinger dependiente del tiempo, y es muy general. Hasta donde sabemos, puede usarse para describir todos los sistemas físicos. Aún así, parece justo preguntar, como hizo Richard Feynman hace casi setenta años, si hay una manera de ver la mecánica cuántica que imagine historias completas. En otras palabras, ¿existe una formulación que sea paralela al Principio de Mínima Acción? No explicaré la descripción de la **integral de trayectoria** de Feynman en detalle en esta lección, pero solo para abrir el apetito, te daré una pista de cómo funciona.

Primero, permíteme recordarte muy brevemente el principio clásico de mínima acción, como lo expliqué en el Volumen I. Supongamos que una partícula clásica comienza en la posición $x_1$ en el tiempo $t_1$ y llega a la posición $x_2$ en el tiempo $t_2$ (Fig. 9.5). La pregunta es: ¿Cuál fue la trayectoria que tomó entre $t_1$ y $t_2$?

Según el principio de mínima acción, la trayectoria real es aquella de **acción mínima**. La acción es, por supuesto, un término técnico, y representa la integral del Lagrangiano entre los puntos finales de la trayectoria. Para sistemas simples,

⁸Estrictamente hablando, el principio debería llamarse Principio de Acción Estacionaria. Las trayectorias reales son puntos estacionarios de la acción y no siempre mínimos. Para nuestros propósitos, este detalle no es importante.

  32 

9.8. INTEGRALES DE TRAYECTORIA 303

 Figura 9.5: Trayectoria Clásica. Esto muestra una trayectoria que una partícula puede tomar al moverse del punto 1 ($x_1, t_1$) al punto 2 ($x_2, t_2$). Para mantener las cosas simples, no se muestra el eje $\dot{x}$, que representa la velocidad de la partícula en la dirección $x$. 

el Lagrangiano es la energía cinética menos la energía potencial. Por lo tanto, para una partícula que se mueve en una dimensión, la acción es

$$A = \int_{t_1}^{t_2} L(x, \dot{x}) dt \quad (9.19)$$

o

  32 

304 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

 Figura 9.6: Primer Paso Hacia la Cuantización de la Trayectoria. Divide el camino de la partícula en dos partes iguales (iguales en tiempo, eso es). La partícula tiene los mismos puntos de inicio y final, pero ahora su trayectoria pasa por el punto intermedio $x$. 

$$A = \int_{t_1}^{t_2} \left( \frac{m \dot{x}^2}{2} - V(x) \right) dt.$$

La idea es probar todas las trayectorias posibles que conectan los dos puntos finales, y calcular $A$ para cada una de ellas. La

  32 

9.8. INTEGRALES DE TRAYECTORIA 305

 Figura 9.7: Pasos Adicionales Hacia la Construcción de la Integral de Trayectoria. Manteniendo los mismos puntos de inicio y final, divide la trayectoria en un gran número de segmentos de igual tamaño. 

ganadora es la que tiene la menor acción.⁹,¹⁰

Ahora, pasemos a la mecánica cuántica. La idea de una trayectoria bien definida entre dos puntos no tiene sentido en mecánica cuántica debido al principio de incertidumbre.

⁹Así es como funciona conceptualmente, de todos modos. En la práctica, las ecuaciones de Euler-Lagrange proporcionan un atajo, como se explicó en el Volumen I.

¹⁰Para mantener nuestros diagramas simples, no mostramos un eje $\dot{x}$ aunque el Lagrangiano claramente depende de $\dot{x}$.

  32 

306 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

Sin embargo, una pregunta que podemos hacer es: Dado que una partícula comienza en $(x_1, t_1)$, ¿cuál es la probabilidad de que aparezca en $(x_2, t_2)$ si se hace una observación de su posición?

Como siempre en mecánica cuántica, la probabilidad es el cuadrado del valor absoluto de una amplitud compleja. La versión global de la mecánica cuántica pregunta:

Dado que una partícula comienza en $(x_1, t_1)$, ¿cuál es la amplitud de que aparezca en $(x_2, t_2)$?

Llamemos a esa amplitud $C(x_1, t_1; x_2, t_2)$ o, más simplemente, $C_{1,2}$. El estado inicial de la partícula es $|\Psi(t_1)\rangle = |x_1\rangle$. Durante el intervalo de tiempo entre $t_1$ y $t_2$, el estado evoluciona a

$$|\Psi(t_2)\rangle = e^{-i\mathbf{H}(t_2 - t_1)} |x_1\rangle. \quad (9.20)$$

La amplitud para detectar la partícula en $|x_2\rangle$ es simplemente el producto interno de $|\Psi(t_2)\rangle$ con $|x_2\rangle$. Su valor es

$$C_{1,2} = \langle x_2 | e^{-i\mathbf{H}(t_2 - t_1)} | x_1 \rangle. \quad (9.21)$$

En otras palabras, la amplitud para ir de $x_1$ a $x_2$ durante el intervalo de tiempo $t_2 - t_1$ se construye colocando $e^{-i\mathbf{H}(t_2 - t_1)}$ entre las posiciones inicial y final. Para simplificar la fórmula, definamos $t_2 - t_1 = t$. Entonces la amplitud es

$$C_{1,2} = \langle x_2 | e^{-i\mathbf{H}t} | x_1 \rangle. \quad (9.22)$$

Ahora, dividamos el intervalo de tiempo $t$ en dos intervalos más pequeños de tamaño $t/2$ (ver Fig. 9.6). El operador $e^{-i\mathbf{H}t}$ puede escribirse

  32 

9.8. INTEGRALES DE TRAYECTORIA 307

como el producto de dos operadores:

$$e^{-i\mathbf{H}t} = e^{-i\mathbf{H}t/2} e^{-i\mathbf{H}t/2}. \quad (9.23)$$

Insertando el operador identidad en la forma

$$\mathbf{I} = \int dx |x\rangle \langle x|, \quad (9.24)$$

podemos reescribir la amplitud como

$$C_{1,2} = \int dx \langle x_2 | e^{-i\mathbf{H}t/2} | x \rangle \langle x | e^{-i\mathbf{H}t/2} | x_1 \rangle. \quad (9.25)$$

Esta forma de la ecuación parece más complicada, pero tiene una interpretación muy interesante. Permíteme ponerlo en palabras. La amplitud para ir de $x_1$ a $x_2$ durante un intervalo de tiempo $t$ es una integral sobre una posición intermedia $x$. El integrando es la amplitud para ir de $x_1$ a $x$ durante el intervalo de tiempo $t/2$ multiplicada por la amplitud para ir de $x$ a $x_2$ durante otro intervalo de tiempo $t/2$.

La Fig. 9.6 muestra la misma idea en términos visuales. Clásicamente, para ir de $x_1$ a $x_2$, la partícula debe pasar por un punto intermedio $x$. Pero en mecánica cuántica, la amplitud para ir de $x_1$ a $x_2$ es una integral sobre todos los puntos intermedios posibles.

Podemos llevar esta idea más allá y dividir el intervalo de tiempo en muchos intervalos diminutos, como se ilustra en la Fig. 9.7. No escribiré las fórmulas complicadas, pero la idea debería ser clara. Para cada pequeño intervalo de tiempo, digamos de tamaño $\epsilon$,

  32 

308 LECCIÓN 9. DINÁMICA DE PARTÍCULAS

incluimos un factor

$$e^{-i\epsilon \mathbf{H}}.$$

Luego, entre cada par de factores, insertamos la identidad, de modo que la amplitud $C_{1,2}$ se convierte en una integral múltiple sobre todas las ubicaciones intermedias. El integrando se construye a partir de productos de expresiones de la forma

$$\langle x_i | e^{-i\epsilon \mathbf{H}} | x_{i+1} \rangle.$$

Si definimos $\mathbf{U}(\epsilon)$ como

$$\mathbf{U}(\epsilon) = e^{-i\epsilon \mathbf{H}},$$

entonces podemos escribir el producto completo como

$$\langle x_2 | \mathbf{U}^N | x_1 \rangle$$

o

$$\langle x_2 | \mathbf{U}\mathbf{U}\mathbf{U}\mathbf{U} \ldots | x_1 \rangle.$$

En esta ecuación, $\mathbf{U}$ aparece $N$ veces como factor, donde $N$ es el número de pasos epsilon. Luego podemos insertar operadores identidad entre los $\mathbf{U}$.

Tal expresión puede llamarse la amplitud para la trayectoria dada. Pero la partícula no viaja a lo largo de una trayectoria particular. En cambio, en el límite de un gran número de intervalos de tiempo infinitesimales, la amplitud es una integral sobre

  33 

9.8. INTEGRALES DE TRAYECTORIA 309

todas las trayectorias posibles entre los puntos finales. El hecho elegante que descubrió Feynman es que la amplitud para cada trayectoria tiene una relación simple con una expresión familiar de la mecánica clásica —la **acción** para esa trayectoria. La expresión exacta para cada trayectoria es

$$e^{iA/\hbar},$$

donde $A$ es la acción para la trayectoria individual.

La formulación de Feynman puede resumirse en una sola ecuación:

$$C_{1,2} = \sum_{\text{trayectorias}} e^{iA/\hbar}. \quad (9.26)$$

La formulación de integral de trayectoria no es meramente un truco matemático elegante; tiene poder real. De hecho, puede usarse para derivar ambas ecuaciones de Schrödinger, y todas las relaciones de conmutación de la mecánica cuántica. Pero realmente alcanza su máximo esplendor en el contexto de la teoría cuántica de campos, donde es la herramienta principal para formular las leyes de la física de partículas elementales.

---

[Fin de la Parte 4/5. Continuará con Capítulo 10...]

---

[PARTE 5/5 - Capítulo 10]

---

  33 

# Lección 10

## El Oscilador Armónico

Art: Creo que lo estoy viendo, Lenny. Toda la imagen se está enfocando lentamente. Menos Uno, la Incertidumbre General, pares entrelazados, el Hamiltoniano — incluso los degenerados. ¿Qué sigue?

Lenny: Oscilaciones, Art. Vibraciones. Tú tocas el violín — tócanos una última melodía esta noche. Algo con buenas vibras.

De todos los ingredientes que intervienen en la construcción de una descripción cuántica del mundo, dos destacan como especialmente fundamentales. El espín, o cúbit, es por supuesto uno de ellos. En lógica clásica, todo puede construirse a partir de preguntas de sí o no. De manera similar, en mecánica cuántica, cada pregunta lógica se reduce a una pregunta sobre cúbits. Pasamos mucho tiempo en lecciones anteriores aprendiendo sobre cúbits.

En esta lección, aprenderemos sobre el segundo ingrediente básico de la mecánica cuántica: el **oscilador armónico**.

El oscilador armónico no es un objeto particular como un átomo de hidrógeno o un quark. Es realmente un marco matemático para comprender una enorme cantidad de fenómenos. Este

  33 

312 LECCIÓN 10. EL OSCILADOR ARMÓNICO

concepto del oscilador armónico también existe en la física clásica, pero realmente alcanza su máximo esplendor en la teoría cuántica.

Un ejemplo de un oscilador armónico es una partícula que se mueve bajo una fuerza restauradora lineal; por ejemplo, el icónico peso en el extremo de un resorte. Un resorte idealizado satisface la ley de Hooke: la fuerza sobre la masa desplazada es proporcional a la distancia que ha sido desplazada. Llamamos a la fuerza una fuerza restauradora porque empuja la masa de vuelta hacia la posición de equilibrio.

Otro ejemplo es una canica que rueda de un lado a otro en el fondo de un cuenco, sin pérdida de energía por fricción. Lo que caracteriza a estos sistemas es una función de energía potencial que se asemeja a una parábola:

$$V(x) = \frac{k}{2} x^2. \quad (10.1)$$

La constante $k$ se llama constante del resorte. Si recordamos que la fuerza sobre un objeto es menos el gradiente de $V$, encontramos que la fuerza sobre el objeto es

$$F = -k x. \quad (10.2)$$

El signo negativo nos dice que la fuerza actúa opuesta al desplazamiento y empuja la masa de vuelta hacia el origen.

¿Por qué los osciladores armónicos son tan prevalentes en física? Porque casi cualquier función suave se asemeja a una parábola cerca de un mínimo de la función. De hecho, muchos tipos de sistemas se caracterizan por una función de energía que puede aproximarse mediante una función cuadrática de alguna variable que representa un desplazamiento del equilibrio. Cuando se perturban,

  33 

313

estos sistemas oscilarán todos alrededor del punto de equilibrio. Aquí hay otros ejemplos:

* Un átomo situado en una red cristalina. Si el átomo se desplaza ligeramente de su posición de equilibrio, es empujado de vuelta con una fuerza restauradora aproximadamente lineal. Este movimiento es tridimensional y realmente consiste en tres oscilaciones independientes.
* La corriente eléctrica en un circuito de baja resistencia a menudo oscila con una frecuencia característica. Las matemáticas de los circuitos son idénticas a las matemáticas de las masas unidas a resortes.
* Ondas. Si se perturba la superficie de un estanque, envía ondas. Alguien que observe en una ubicación particular verá la superficie oscilar a medida que la onda pasa. Este movimiento puede describirse como movimiento armónico simple. Lo mismo ocurre con las ondas sonoras.
* Ondas electromagnéticas. Como cualquier otra onda, una onda de luz o una onda de radio oscila cuando te atraviesa. La misma matemática que describe la partícula oscilante también se aplica a las ondas electromagnéticas.

La lista continúa, pero la matemática es siempre la misma. Solo para tener un ejemplo en mente, imaginemos el oscilador como un peso que cuelga de un resorte. No hace falta decir que apenas necesitamos mecánica cuántica para describir un peso y resorte ordinarios, así que imaginemos una versión muy pequeña de este mismo sistema y luego cuanticémosla.

  33 

314 LECCIÓN 10. EL OSCILADOR ARMÓNICO

### 10.1 La Descripción Clásica

Usemos $y$ para denotar la altura del peso que cuelga. Elegiremos el origen de modo que el peso esté en $y = 0$ cuando esté en equilibrio —es decir, cuando el peso cuelgue en reposo. Para estudiar este sistema clásicamente, podemos usar el método lagrangiano que aprendimos en el Volumen I. Las energías cinética y potencial son $\frac{1}{2} m \dot{y}^2$ y $\frac{1}{2} k y^2$ respectivamente.

Como recordarás, el Lagrangiano es la energía cinética menos la energía potencial:

$$L = \frac{1}{2} m \dot{y}^2 - \frac{1}{2} k y^2.$$

Primero, pondremos el Lagrangiano en una cierta forma estándar cambiando de $y$ a otra variable que llamaremos $x$. Esta coordenada no es algo nuevo. Todavía representa el desplazamiento de la masa. Al cambiar de $y$ a $x$, simplemente estamos haciendo un cambio conveniente de unidades. Definamos la nueva variable como

$$x = \sqrt{m} \, y.$$

En términos de $x$, el Lagrangiano se convierte en

$$L = \frac{1}{2} \dot{x}^2 - \frac{1}{2} \omega^2 x^2. \quad (10.3)$$

La constante $\omega$ se define como $\omega = \sqrt{\frac{k}{m}}$ y resulta ser la frecuencia del oscilador.

  33 

10.1. LA DESCRIPCIÓN CLÁSICA 315

Al hacer este cambio de variables, podemos describir cada oscilador exactamente en la misma forma. En esta forma, los osciladores se distinguen entre sí solo por su frecuencia $\omega$.

Ahora, usemos las ecuaciones de Lagrange para deducir las ecuaciones de movimiento. Para este sistema unidimensional, solo hay una ecuación de Lagrange, a saber

$$\frac{\partial L}{\partial x} = \frac{d}{dt} \frac{\partial L}{\partial \dot{x}}. \quad (10.4)$$

Realizando estas operaciones en la Ec. 10.3, encontramos que

$$\frac{\partial L}{\partial \dot{x}} = \dot{x}. \quad (10.5)$$

Esto se llama el **momento canónico conjugado a $x$**. Diferenciando con respecto al tiempo da

$$\frac{d}{dt} \frac{\partial L}{\partial \dot{x}} = \ddot{x}, \quad (10.6)$$

y ahora tenemos el lado derecho de la Ec. 10.4. Pasando al lado izquierdo, encontramos que

$$\frac{\partial L}{\partial x} = -\omega^2 x. \quad (10.7)$$

Igualando los lados izquierdo y derecho (Ecs. 10.7 y 10.6) de la ecuación de Lagrange, obtenemos

$$-\omega^2 x = \ddot{x}. \quad (10.8)$$

  33 

316 LECCIÓN 10. EL OSCILADOR ARMÓNICO

Esta ecuación es, por supuesto, equivalente a $F = ma$. ¿Por qué hay un signo menos? Porque la fuerza es una fuerza restauradora —su dirección es opuesta a la dirección del desplazamiento.

A estas alturas ya has visto este tipo de ecuación suficientes veces como para saber que la solución contiene senos y cosenos. La solución general es

$$x = A \cos(\omega t) + B \sin(\omega t), \quad (10.9)$$

lo que nos muestra que $\omega$ es efectivamente la frecuencia del oscilador. Cuando diferenciamos dos veces, extraemos un factor de $\omega^2$.

**Ejercicio 10.1:** Encuentra la segunda derivada temporal de $x$ en la Ec. 10.9, y muestra que resuelve la Ec. 10.8.

### 10.2 La Descripción Mecánico-Cuántica

Ahora, volvamos a nuestra versión microscópica del sistema peso-y-resorte —digamos, no más grande que una sola molécula. Al principio, esto parece ridículo. ¿Cómo podríamos construir un resorte tan pequeño? Pero de hecho, la naturaleza proporciona todo tipo de resortes microscópicos. Muchas moléculas consisten en dos átomos —por ejemplo, un átomo pesado y uno ligero. Hay fuerzas que mantienen la molécula en equilibrio con los átomos separados por una cierta distancia. Cuando el átomo ligero se desplaza, será atraído de vuelta a la ubicación de equilibrio. La

  33 

10.2. DESCRIPCIÓN MECÁNICO-CUÁNTICA 317

molécula es una versión miniatura del sistema peso-y-resorte, pero es tan pequeña que tenemos que usar la mecánica cuántica para entenderla.

Habiendo deducido el Lagrangiano clásico, intentemos construir una descripción mecánico-cuántica de nuestro sistema. Lo primero que necesitamos es un espacio de estados. Como hemos visto, el estado de una partícula que se mueve en una línea se representa mediante una función de onda $\psi(x)$. Hay muchos estados posibles del sistema, y cada uno está representado por una función de onda diferente. Una función $\psi(x)$ se define de tal manera que $\psi^*(x)\psi(x)$ es la densidad de probabilidad (la probabilidad por unidad de intervalo) de encontrar la partícula en la posición $x$:

$$\psi^*(x)\psi(x) = P(x).$$

En esta ecuación, $P(x)$ representa la densidad de probabilidad. Ahora tenemos una especie de cinemática —una especificación de cuáles son los estados del sistema.

¿Puede $\psi(x)$ ser cualquier función? Aparte del requisito de que debe ser continua y diferenciable, la única condición extra es que la probabilidad total de encontrar la partícula en cualquier posición debe ser 1:

$$\int_{-\infty}^{+\infty} \psi^*(x)\psi(x) dx = 1. \quad (10.10)$$

Esto no parecería ser una gran restricción. Sea cual sea el lado derecho de esta ecuación, siempre podríamos multiplicar $\psi$ por alguna constante para hacer que la integral sea igual a 1 — a menos que la integral sea cero o infinita. Dado que $\psi^*(x)\psi(x)$

  33 

318 LECCIÓN 10. EL OSCILADOR ARMÓNICO

es positiva, no tenemos que preocuparnos por cero, pero el infinito es un asunto completamente diferente; hay muchas funciones que harían que la integral en la Ec. 10.10 explotara. Las condiciones para una función de onda sensata incluyen, por lo tanto, el requisito de que $\psi$ decaiga a cero lo suficientemente rápido como para que la integral converja. Las funciones que cumplen esta condición se llaman **normalizables**.

Hay dos preguntas que podríamos hacer sobre nuestro oscilador armónico:

* ¿Cómo cambia el vector de estado en función del tiempo? Para responder a esta pregunta, necesitamos conocer el Hamiltoniano.
* ¿Cuáles son las energías posibles del oscilador? Estas también están determinadas por el Hamiltoniano.

Así que para saber algo útil necesitamos el Hamiltoniano. Afortunadamente, podemos derivarlo del Lagrangiano, y te recordaré cómo en un momento. Pero primero recuerda que el momento canónico conjugado a $x$ se define como $\partial L / \partial \dot{x}$.¹ Combinando esto con la Ec. 10.5, obtenemos

$$p = \frac{\partial L}{\partial \dot{x}} = \dot{x}.$$

Usando la definición directa de la mecánica clásica, encontramos que el Hamiltoniano para el oscilador armónico es

¹Esta idea se explica en el Volumen I.

  34 

10.2. DESCRIPCIÓN MECÁNICO-CUÁNTICA 319

$$H = p \dot{x} - L,$$

donde $p$ es el momento canónico conjugado a $x$, y $L$ representa el Lagrangiano.²

Podríamos trabajar directamente a partir de esta definición, pero en su lugar tomaremos un atajo. Debido a que el Lagrangiano es la energía cinética menos la energía potencial, el Hamiltoniano es la energía cinética más la energía potencial —en otras palabras, la energía total. El Hamiltoniano para el oscilador puede, por lo tanto, escribirse como

$$H = \frac{1}{2} \dot{x}^2 + \frac{1}{2} \omega^2 x^2.$$

Hasta aquí, todo bien, pero no hemos terminado. Hemos expresado la energía cinética en términos de la velocidad; en mecánica cuántica, sin embargo, necesitamos representar nuestros observables como operadores, y no tenemos un operador de velocidad. Para solucionar esto, tendremos que reformular las cosas en términos de posición y momento canónico, que sí tiene una forma de operador estándar. Reescribir el Hamiltoniano en términos del momento canónico es fácil porque

$$p = \frac{\partial L}{\partial \dot{x}} = \dot{x},$$

lo que nos permite escribir

$$H = \frac{1}{2} p^2 + \frac{1}{2} \omega^2 x^2. \quad (10.11)$$

²No necesitamos usar un signo de suma porque solo hay un grado de libertad.

  34 

320 LECCIÓN 10. EL OSCILADOR ARMÓNICO

Ese es el Hamiltoniano clásico. Ahora podemos convertirlo en una ecuación mecánico-cuántica reinterpretando $x$ y $p$ como operadores, definidos por su acción sobre $\psi(x)$. Como hemos hecho antes, usaremos los símbolos en negrita, $\mathbf{X}$ y $\mathbf{P}$, para distinguir nuestros operadores cuánticos de sus contrapartes clásicas, $x$ y $p$. De lecciones anteriores, sabemos exactamente cómo funcionan estos operadores. $\mathbf{X}$ simplemente multiplica la función de onda por la variable de posición:

$$\mathbf{X} |\psi(x)\rangle \quad \Rightarrow \quad x \psi(x).$$

Y $\mathbf{P}$ toma la misma forma que en otros problemas unidimensionales:

$$\mathbf{P} |\psi(x)\rangle \quad \Rightarrow \quad -i\hbar \frac{d}{dx} \psi(x).$$

Ahora, podemos determinar la acción del Hamiltoniano sobre una función de onda dejando que $\mathbf{P}$ actúe dos veces sobre la función de onda. Este es el mismo procedimiento que seguimos en la Lección 9. En otras palabras,

$$\mathbf{H} |\psi(x)\rangle \quad \Rightarrow \quad \frac{1}{2} \left( -i\hbar \frac{\partial}{\partial x} \right) \left( -i\hbar \frac{\partial \psi(x)}{\partial x} \right) + \frac{1}{2} \omega^2 x^2 \psi(x),$$

o

$$\mathbf{H} |\psi(x)\rangle \quad \Rightarrow \quad -\frac{\hbar^2}{2} \frac{\partial^2 \psi(x)}{\partial x^2} + \frac{1}{2} \omega^2 x^2 \psi(x). \quad (10.12)$$

Estamos usando derivadas parciales porque en general $\psi$ también depende de otra variable, el tiempo. El tiempo no es un operador y

  34 

10.3. LA ECUACIÓN DE SCHRÖDINGER 321

no tiene el mismo estatus que $x$, pero el vector de estado sí cambia con el tiempo, y por lo tanto tratamos el tiempo como un parámetro. La derivada parcial indica que estamos describiendo el sistema "en un tiempo fijo".

### 10.3 La Ecuación de Schrödinger

La Ec. 10.12 muestra cómo opera el Hamiltoniano sobre $\psi$. Ahora, pongámoslo a trabajar. Como dijimos en la sección anterior, uno de sus trabajos es decirte cómo cambia el vector de estado con el tiempo. Así que escribamos la ecuación de Schrödinger dependiente del tiempo:

$$i \frac{\partial \psi}{\partial t} = \frac{1}{\hbar} \mathbf{H} \psi.$$

Sustituyendo $\mathbf{H}$ usando 10.12, obtenemos

$$i \frac{\partial \psi}{\partial t} = -\frac{\hbar}{2} \frac{\partial^2 \psi}{\partial x^2} + \frac{1}{2\hbar} \omega^2 x^2 \psi. \quad (10.13)$$

Esta ecuación dice que si conoces $\psi$ (tanto la parte real como la imaginaria) en algún momento particular, puedes predecir lo que será en un momento futuro. Observa que la ecuación es compleja —contiene $i$ como factor. Esto significa que incluso si $\psi$ comienza siendo de valor real en el tiempo $t = 0$, muy rápidamente desarrollará una parte imaginaria. Cualquier solución $\psi$ debe ser, por lo tanto, una función compleja de $x$ y $t$.

Puedes resolver esta ecuación de varias maneras. Por ejemplo, puedes resolverla numéricamente en un ordenador. Comienza con un valor conocido de $\psi(x)$ y actualízalo ligeramente calculando la derivada. Una vez que tengas la derivada, calcula cómo cambia $\psi(x)$ en un pequeño incremento de tiempo. Luego,

  34 

322 LECCIÓN 10. EL OSCILADOR ARMÓNICO

añade este cambio incremental a $\psi(x)$ y sigue haciéndolo una y otra vez. Resulta que $\psi(x)$ hará cosas interesantes —se moverá de alguna manera. De hecho, bajo ciertas circunstancias, formará un paquete de ondas que se moverá de manera muy similar a un oscilador armónico.

### 10.4 Niveles de Energía

La otra cosa que puedes hacer con el Hamiltoniano es calcular los niveles de energía del oscilador, encontrando los vectores propios y valores propios de la energía. Como aprendimos en la Lección 4, una vez que conoces estos vectores propios y valores propios, puedes determinar la dependencia temporal sin resolver ninguna ecuación diferencial. Esto se debe a que ya conoces la dependencia temporal de cada vector propio de energía. Quizás quieras repasar la receta del Ket de Schrödinger que proporcionamos en la Sección 4.13.

Por ahora, concentrémonos en encontrar los vectores propios de la energía en sí mismos, utilizando la ecuación de Schrödinger independiente del tiempo:

$$\mathbf{H} |\psi_E\rangle = E |\psi_E\rangle.$$

El subíndice $E$ indica que $\psi_E$ es el vector propio para un valor propio particular $E$. Esta ecuación define dos cosas: las funciones de onda $\psi_E(x)$ y los niveles de energía $E$. Hagamos las cosas menos abstractas expandiendo $\mathbf{H}$ usando la Ec. 10.12:

$$-\frac{\hbar^2}{2} \frac{\partial^2 \psi_E(x)}{\partial x^2} + \frac{1}{2} \omega^2 x^2 \psi_E(x) = E \psi_E(x). \quad (10.14)$$

Para resolver esta ecuación, debemos:

  34 

10.4. NIVELES DE ENERGÍA 323

* Encontrar los valores admisibles de $E$ que permiten una solución matemática.
* Encontrar los vectores propios y los valores propios posibles de la energía.

Esto es un poco más complicado de lo que podrías pensar. Resulta que hay una solución para la ecuación para cada valor de $E$, incluyendo todos los números complejos, pero la mayoría de las soluciones son físicamente absurdas. Si comenzamos en algún punto y resolvemos la ecuación de Schrödinger dando pequeños pasos incrementales, casi siempre encontraremos que $\psi(x)$ crece o "explota" a medida que $x$ se vuelve grande. En otras palabras, podemos ser capaces de encontrar soluciones a la ecuación, pero solo muy raramente encontraremos una solución **normalizable**.

De hecho, para la mayoría de los valores de $E$, incluyendo todos los números complejos, las soluciones de la Ec. 10.14 crecen exponencialmente a medida que $x$ se aproxima a $\infty$, $-\infty$, o ambos. Este tipo de solución no tiene sentido físico; nos dice que hay una probabilidad abrumadora de que la coordenada del oscilador esté infinitamente lejos. Claramente, queremos imponer alguna condición que elimine tales soluciones. Así que impongamos una:

**Las soluciones físicas de la ecuación de Schrödinger deben ser normalizables.**

Esta es una restricción muy poderosa. De hecho, para casi todos los valores de $E$, no hay soluciones normalizables. Pero para ciertos valores muy especiales de $E$ tales soluciones existen, y las encontraremos.

  34 

324 LECCIÓN 10. EL OSCILADOR ARMÓNICO

### 10.5 El Estado Fundamental

¿Cuál es el nivel de energía más bajo posible para un oscilador armónico? En física clásica, la energía nunca puede ser negativa porque el Hamiltoniano tiene un término $x^2$ y un término $p^2$; para minimizar la energía, simplemente establecemos $p$ y $x$ iguales a cero.

Pero en mecánica cuántica, eso es pedir demasiado. El principio de incertidumbre dice que no puedes establecer $x$ y $p$ ambos iguales a cero. Lo mejor que puedes hacer es encontrar un estado de compromiso en el que $x$ y $p$ no estén demasiado extendidos. Debido a que tienes que comprometerte, la energía más baja posible no será cero. Ni $p^2$ ni $x^2$ serán cero. Dado que los operadores $\mathbf{X}^2$ y $\mathbf{P}^2$ solo pueden tener valores propios positivos, el oscilador armónico no tiene niveles de energía negativos, y de hecho, tampoco tiene un estado con energía cero.

Si todos los niveles de energía de un sistema deben ser positivos, debe haber una energía admisible más baja y una función de onda que la acompañe. Este nivel de energía más bajo se llama **estado fundamental** y se denota por $\psi_0(x)$. Ten en cuenta que el subíndice 0 no significa que la energía sea cero; significa que es la energía admisible más baja.

Hay un teorema matemático muy útil que ayuda a identificar el estado fundamental. No lo demostraremos aquí, pero es muy simple de enunciar:

**La función de onda del estado fundamental para cualquier potencial no tiene ceros y es el único estado propio de energía que no tiene nodos.**

Por lo tanto, todo lo que tenemos que hacer para encontrar el estado fundamental de nuestro oscilador armónico es encontrar una solución sin nodos para algún valor

  34 

10.5. EL ESTADO FUNDAMENTAL 325

de $E$. No importa cómo la encontremos —podemos usar trucos matemáticos, hacer conjeturas, o simplemente preguntarle al profesor. Usemos este último método. (Haré el papel del profesor.)

 Figura 10.1: Estado Fundamental del Oscilador Armónico 

Aquí hay una función que funciona:

$$\psi(x) = e^{-\frac{\omega}{2\hbar} x^2}. \quad (10.15)$$

Esta función se muestra esquemáticamente en la Fig. 10.1. Como puedes ver, está concentrada cerca del origen, donde esperamos que el estado de energía más baja esté concentrado. Tiende a cero muy rápidamente a medida que se aleja del origen, por lo que la integral de la densidad de probabilidad es finita. Y, lo que es importante, no tiene nodos. Así que tiene la posibilidad de ser nuestro estado fundamental.

Veamos si podemos determinar qué le hace el Hamiltoniano a esta función. El primer término del Hamiltoniano (el lado izquierdo de la Ec. 10.14) nos dice que apliquemos el operador

  34 

326 LECCIÓN 10. EL OSCILADOR ARMÓNICO

$$-\frac{\hbar^2}{2} \frac{\partial}{\partial x^2}$$

a $\psi(x)$. Calculemos ese término, una derivada a la vez. El primer paso es

$$\frac{\partial \psi(x)}{\partial x} = -\frac{\omega}{2\hbar} (2x) e^{-\frac{\omega}{2\hbar} x^2},$$

que se simplifica a

$$\frac{\partial \psi(x)}{\partial x} = -\frac{\omega}{\hbar} x e^{-\frac{\omega}{2\hbar} x^2}.$$

Cuando tomamos la segunda derivada, habrá dos términos debido a la regla del producto:

$$\frac{\partial^2 \psi(x)}{\partial x^2} = -\frac{\omega}{\hbar} e^{-\frac{\omega}{2\hbar} x^2} + \frac{\omega^2}{\hbar^2} x^2 e^{-\frac{\omega}{2\hbar} x^2}.$$

Insertemos este resultado de nuevo en la Ec. 10.14, y al mismo tiempo reemplacemos $\psi$ en el lado derecho con nuestra conjetura, $e^{-\frac{\omega}{2\hbar} x^2}$:

$$-\frac{\hbar^2}{2} \left( -\frac{\omega}{\hbar} e^{-\frac{\omega}{2\hbar} x^2} + \frac{\omega^2}{\hbar^2} x^2 e^{-\frac{\omega}{2\hbar} x^2} \right) + \frac{1}{2} \omega^2 x^2 e^{-\frac{\omega}{2\hbar} x^2} = E e^{-\frac{\omega}{2\hbar} x^2}.$$

Simplificando el primer término:

$$-\frac{\hbar^2}{2} \cdot -\frac{\omega}{\hbar} e^{-\frac{\omega}{2\hbar} x^2} = \frac{\hbar \omega}{2} e^{-\frac{\omega}{2\hbar} x^2}$$
$$-\frac{\hbar^2}{2} \cdot \frac{\omega^2}{\hbar^2} x^2 e^{-\frac{\omega}{2\hbar} x^2} = -\frac{1}{2} \omega^2 x^2 e^{-\frac{\omega}{2\hbar} x^2}.$$

Por lo tanto, la ecuación completa se convierte en

$$\frac{\hbar \omega}{2} e^{-\frac{\omega}{2\hbar} x^2} - \frac{1}{2} \omega^2 x^2 e^{-\frac{\omega}{2\hbar} x^2} + \frac{1}{2} \omega^2 x^2 e^{-\frac{\omega}{2\hbar} x^2} = E e^{-\frac{\omega}{2\hbar} x^2}.$$

  34 

10.6. OPERADORES DE CREACIÓN Y ANIQUILACIÓN 327

Después de cancelar los términos proporcionales a $x^2 e^{-\frac{\omega}{2\hbar} x^2}$, descubrimos el hecho notable de que resolver la ecuación de Schrödinger solo se reduce a resolver

$$\frac{\hbar \omega}{2} e^{-\frac{\omega}{2\hbar} x^2} = E e^{-\frac{\omega}{2\hbar} x^2}.$$

Como puedes ver, la única forma de resolver esta ecuación es igualar la energía $E$ a $\frac{\omega \hbar}{2}$. En otras palabras, hemos encontrado no solo la función de onda sino también el valor de la energía del estado fundamental. Llamando a la energía del estado fundamental $E_0$, podemos escribir

$$E_0 = \frac{\omega \hbar}{2}. \quad (10.16)$$

La función de onda del estado fundamental, mientras tanto, es simplemente la función gaussiana que nos dio el profesor:

$$\psi_0(x) = e^{-\frac{\omega}{2\hbar} x^2}.$$

Es un tipo astuto, ese profesor.

### 10.6 Operadores de Creación y Aniquilación

A lo largo de estas lecciones, hemos visto dos formas de pensar sobre la mecánica cuántica. Se remontan a Heisenberg y Schrödinger. A Heisenberg le gustaba el álgebra, las matrices y, si hubiera sabido cómo llamarlos, los operadores lineales. Schrödinger, por el contrario, pensaba en términos de funciones de onda y ecuaciones de onda, siendo la ecuación de Schrödinger un ejemplo famoso. Por supuesto, las dos formas de pensar no son contradictorias; las funciones forman un espacio vectorial y las derivadas son operadores.

Hasta ahora, en nuestro estudio del oscilador armónico nos hemos centrado en funciones y ecuaciones diferenciales. Pero la herramienta más poderosa en muchos casos —particularmente para el oscilador

 
328 LECCIÓN 10. EL OSCILADOR ARMÓNICO

armónico— es el método del operador. Reduce todo el estudio de funciones de onda y ecuaciones de onda a un número muy pequeño de trucos algebraicos, que casi siempre involucran las relaciones de conmutación. De hecho, cada vez que veas un par de operadores, mi consejo es que determines su conmutador. Si el conmutador es un nuevo operador que no has visto antes, encuentra su conmutador con el par original. Ahí es cuando comienza la diversión.

Obviamente, este consejo puede llevar a una cadena interminable de cálculos aburridos. Pero de vez en cuando puedes tener suerte y encontrar un conjunto de operadores que se cierran bajo conmutación. Siempre que eso suceda, estás en el negocio; como veremos, los métodos de operadores tienen un poder tremendo.

Ahora, apliquemos este enfoque a nuestro oscilador armónico. Comenzamos con el Hamiltoniano expresado en términos de los operadores $\mathbf{P}$ y $\mathbf{X}$:

$$\mathbf{H} = \frac{\mathbf{P}^2 + \omega^2 \mathbf{X}^2}{2}. \quad (10.17)$$

Para determinar el resto de los niveles de energía, usaremos algunos trucos. La idea es utilizar hábilmente las propiedades de $\mathbf{X}$ y $\mathbf{P}$ (en particular, la relación de conmutación $[\mathbf{X}, \mathbf{P}] = i\hbar$) para construir dos nuevos operadores, llamados **operadores de creación y aniquilación**. Cuando un operador de creación actúa sobre un vector propio de energía, produce un nuevo vector propio que tiene el siguiente nivel de energía más alto. Un operador de aniquilación hace exactamente lo contrario: produce un vector propio cuya energía es un nivel más bajo que la energía del vector propio con el que comenzó. Así que, hablando aproximadamente, lo que crean y aniquilan es energía. También se les llama operadores de **subida y bajada**. Pero recuerda: los operadores actúan sobre vectores de estado, no sobre sistemas. Para ver cómo funcionan estos operadores, reescribamos el Hamiltoniano en la forma

  35 

10.6. OPERADORES DE CREACIÓN Y ANIQUILACIÓN 329

$$\mathbf{H} = \frac{1}{2} (\mathbf{P}^2 + \omega^2 \mathbf{X}^2). \quad (10.18)$$

Este es un Hamiltoniano tanto clásico como mecánico-cuántico, y sería igualmente correcto usar los símbolos en minúscula $p$ y $x$. Sin embargo, estamos usando $\mathbf{P}$ y $\mathbf{X}$ en negrita porque planeamos centrarnos en el Hamiltoniano mecánico-cuántico.

Comencemos haciendo una manipulación que es correcta para la física clásica pero que requerirá alguna modificación para la mecánica cuántica. En el paréntesis de arriba, tenemos una suma de cuadrados. Usando la fórmula

$$a^2 + b^2 = (a + ib)(a - ib),$$

parece que podemos reescribir el Hamiltoniano como

$$\mathbf{H} \ "=" \ \frac{1}{2} (\mathbf{P} + i\omega \mathbf{X})(\mathbf{P} - i\omega \mathbf{X}), \quad (10.19)$$

y eso es casi correcto. ¿Por qué casi? Porque cuánticamente, $\mathbf{P}$ y $\mathbf{X}$ no conmutan, y debemos tener cuidado con el orden de las operaciones. Expandamos nuestra expresión factorizada y veamos en qué podría diferir del Hamiltoniano original en la Ec. 10.18. Manteniendo un cuidadoso registro del orden de los factores, podemos expandir la expresión de la siguiente manera:

  35 

330 LECCIÓN 10. EL OSCILADOR ARMÓNICO

$$\frac{1}{2} (\mathbf{P} + i\omega \mathbf{X})(\mathbf{P} - i\omega \mathbf{X}) = \frac{1}{2} (\mathbf{P}^2 + i\omega \mathbf{X}\mathbf{P} - i\omega \mathbf{P}\mathbf{X} - i^2 \omega^2 \mathbf{X}^2)$$
$$= \frac{1}{2} (\mathbf{P}^2 + i\omega (\mathbf{X}\mathbf{P} - \mathbf{P}\mathbf{X}) - i^2 \omega^2 \mathbf{X}^2)$$
$$= \frac{1}{2} (\mathbf{P}^2 + i\omega (\mathbf{X}\mathbf{P} - \mathbf{P}\mathbf{X}) + \omega^2 \mathbf{X}^2)$$
$$= \frac{1}{2} (\mathbf{P}^2 + \omega^2 \mathbf{X}^2) + \frac{1}{2} i\omega (\mathbf{X}\mathbf{P} - \mathbf{P}\mathbf{X}).$$

Mira el conjunto de paréntesis en el lado derecho de la última línea. Hemos visto esa expresión antes —es el conmutador de $\mathbf{X}$ y $\mathbf{P}$. De hecho, ya conocemos su valor:

$$(\mathbf{X}\mathbf{P} - \mathbf{P}\mathbf{X}) = [\mathbf{X}, \mathbf{P}] = i\hbar.$$

Por lo tanto, la expresión para nuestro Hamiltoniano factorizado se convierte en

$$\frac{1}{2} (\mathbf{P}^2 + \omega^2 \mathbf{X}^2) + \frac{1}{2} i\omega (i\hbar)$$

o

$$\frac{1}{2} (\mathbf{P}^2 + \omega^2 \mathbf{X}^2) - \frac{1}{2} \omega \hbar.$$

En otras palabras, la expresión factorizada con la que empezamos en la Ec. 10.19 es en realidad menor que el Hamiltoniano en $\frac{\omega \hbar}{2}$. Para recuperar el Hamiltoniano real, necesitamos sumar $\frac{\omega \hbar}{2}$:

$$\mathbf{H} = \frac{1}{2} (\mathbf{P} + i\omega \mathbf{X})(\mathbf{P} - i\omega \mathbf{X}) + \frac{\omega \hbar}{2}.$$

  35 

10.6. OPERADORES DE CREACIÓN Y ANIQUILACIÓN 331

Reescribir el Hamiltoniano de esta manera y de aquella puede parecer un ejercicio de futilidad, pero créeme, no lo es. En primer lugar, el último término es solo una constante aditiva que suma el valor numérico $\frac{\omega \hbar}{2}$ a cada valor propio de energía. Podemos ignorarlo por ahora. Más tarde, después de que hayamos resuelto el resto del problema, podemos volver a añadirlo. El meollo del problema se encuentra en la expresión $(\mathbf{P} + i\omega \mathbf{X})(\mathbf{P} - i\omega \mathbf{X})$. Resulta que estos dos factores, $(\mathbf{P} + i\omega \mathbf{X})$ y $(\mathbf{P} - i\omega \mathbf{X})$, tienen algunas propiedades muy notables. De hecho, son los operadores de subida y bajada (u operadores de creación y aniquilación) de los que te hablé antes. Por ahora, estos son solo nombres, pero a medida que avancemos veremos que los nombres estaban bien elegidos.

Las definiciones obvias serían

$$a_- = (\mathbf{P} - i\omega \mathbf{X})$$

para el operador de bajada, y

$$a_+ = (\mathbf{P} + i\omega \mathbf{X})$$

para el operador de subida. Pero la historia a veces se adelanta a lo obvio. Históricamente, los operadores de subida y bajada se han definido con un factor extra delante de ellos. Aquí están las definiciones oficiales:

$$a_- = \frac{i}{\sqrt{2\omega \hbar}} (\mathbf{P} - i\omega \mathbf{X}), \quad (10.20)$$
$$a_+ = \frac{-i}{\sqrt{2\omega \hbar}} (\mathbf{P} + i\omega \mathbf{X}), \quad (10.21)$$

  35 

332 LECCIÓN 10. EL OSCILADOR ARMÓNICO

Si usamos estas definiciones, el Hamiltoniano comienza a verse muy simple:

$$\mathbf{H} = \omega \hbar (a_+ a_- + 1/2). \quad (10.22)$$

Solo hay dos propiedades de $a_+$ y $a_-$ que necesitamos conocer. La primera es que son conjugados hermíticos entre sí. Eso se sigue de sus definiciones. La otra propiedad es la que realmente les da poder. El conmutador de $a_+$ y $a_-$ es

$$[a_-, a_+] = 1.$$

Esto es fácil de demostrar. Primero, usamos las definiciones para escribir

$$[a_-, a_+] = \frac{1}{2\omega \hbar} [(\mathbf{P} - i\omega \mathbf{X}), (\mathbf{P} + i\omega \mathbf{X})].$$

El siguiente paso es usar las relaciones de conmutación $[\mathbf{X}, \mathbf{X}] = 0$, $[\mathbf{P}, \mathbf{P}] = 0$, y $[\mathbf{X}, \mathbf{P}] = i\hbar$. Aplica estas a la ecuación anterior, y rápidamente encontrarás que $[a_-, a_+] = 1$.

Podemos hacer el Hamiltoniano en la Ec. 10.22 aún más simple definiendo un nuevo operador,

$$N = a_+ a_-,$$

llamado el **operador número**. Una vez más, esto es solo un nombre, pero como veremos, es un nombre muy apropiado. Expresado en términos del operador número, el Hamiltoniano se convierte en

$$\mathbf{H} = \omega \hbar (N + 1/2). \quad (10.23)$$

  35 

10.6. OPERADORES DE CREACIÓN Y ANIQUILACIÓN 333

Hasta ahora, todo lo que hemos hecho es definir algunos símbolos, $a_+$, $a_-$ y $N$, que hacen que el Hamiltoniano parezca engañosamente simple; no está claro que estemos realmente más cerca de determinar los valores propios de la energía. Para proceder, recordemos mi consejo anterior: cada vez que veas dos operadores, conmútalos. En este caso, ya conocemos un conmutador:

$$[a_-, a_+] = 1. \quad (10.24)$$

A continuación, encontremos el conmutador de los operadores de subida y bajada con el operador número $N$. Haremos esto por fuerza bruta. Aquí están los pasos:

$$[a_-, N] = a_- N - N a_- = a_- a_+ a_- - a_+ a_- a_-.$$

Ahora, combinaremos los términos en la forma

$$[a_-, N] = (a_- a_+ - a_+ a_-) a_-.$$

Esto parece complicado hasta que notamos que la expresión en el paréntesis es justamente $[a_-, a_+]$, que resulta ser 1. Usando este hecho para simplificar, obtenemos

$$[a_-, N] = a_-.$$

Podemos hacer lo mismo con $a_+$ y $N$. El resultado es casi el mismo excepto por el signo. Aquí está la lista completa de conmutadores en un paquete ordenado:

  35 

334 LECCIÓN 10. EL OSCILADOR ARMÓNICO

$$[a_-, a_+] = 1$$
$$[a_-, N] = a_-$$
$$[a_+, N] = -a_+. \quad (10.25)$$

Esto es lo que podrías llamar un álgebra de conmutadores: un conjunto de operadores que se cierra bajo conmutación. Las álgebras de conmutadores tienen propiedades maravillosas que las convierten en una de las herramientas favoritas del físico teórico. Ahora vamos a ver el poder de esta álgebra de conmutadores en el ejemplo icónico del oscilador armónico, usándola para encontrar los valores propios y vectores propios de $N$. Una vez que conozcamos estos, podemos leer inmediatamente los valores propios de $\mathbf{H}$ de la Ec. 10.23. El truco es usar una especie de procedimiento de inducción: comenzamos suponiendo que tenemos un valor propio y un vector propio de $N$. Llama al valor propio $n$ y al vector propio $|n\rangle$. Por definición,

$$N |n\rangle = n |n\rangle.$$

Ahora, consideremos un nuevo vector, obtenido al actuar sobre $|n\rangle$ con $a_+$. Probemos que el resultado es un vector propio diferente de $N$, con un valor propio diferente. De nuevo, logramos esto mediante la aplicación directa de las relaciones de conmutación. Comenzaremos escribiendo la expresión $N(a_+|n\rangle)$ de una forma ligeramente más complicada,

$$N(a_+|n\rangle) = [a_+ N - (a_+ N - N a_+)]|n\rangle.$$

La expresión entre corchetes en el lado derecho es la misma que $N a_+$, con el término $a_+ N$ sumado y luego restado. Pero

  35 

10.6. OPERADORES DE CREACIÓN Y ANIQUILACIÓN 335

observa que la expresión en paréntesis es el último de los conmutadores de las Ecs. 10.25. Si insertamos eso, obtenemos

$$N(a_+|n\rangle) = a_+ (N + 1) |n\rangle.$$

El último paso es usar el hecho de que $|n\rangle$ es un vector propio de $N$ con valor propio $n$. Eso significa que podemos reemplazar $(N + 1)$ con $(n + 1)$:

$$N(a_+|n\rangle) = (n + 1)(a_+|n\rangle). \quad (10.26)$$

Como siempre, cuando operamos en piloto automático, tenemos que mantener los ojos abiertos para resultados interesantes. La Ec. 10.26 es interesante. Dice que el vector $a_+|n\rangle$ es un nuevo vector propio de $N$ con valor propio $(n+1)$. En otras palabras, dado el vector propio $|n\rangle$, hemos descubierto otro vector propio cuyo valor propio se incrementa en 1. Todo esto puede resumirse mediante la ecuación

$$a_+|n\rangle = |n+1\rangle. \quad (10.27)$$

Obviamente, podemos hacer esto una y otra vez para encontrar los vectores propios $|n+2\rangle, |n+3\rangle$, y así sucesivamente. Notablemente, encontramos que si hay un valor propio $n$, debe haber una secuencia infinita de valores propios por encima de él, espaciados por enteros. El nombre de operador de subida parece bien elegido.

¿Qué pasa con el operador de bajada? No es sorprendente que encontremos que $a_-|n\rangle$ produce un vector propio cuyo valor propio es una unidad más bajo:

$$a_-|n\rangle = |n-1\rangle. \quad (10.28)$$

  35 

336 LECCIÓN 10. EL OSCILADOR ARMÓNICO

Esto sugiere que debe haber una secuencia interminable de valores propios por debajo de $n$, pero eso no puede ser correcto. Ya sabemos que el estado fundamental tiene energía positiva, y debido a que $\mathbf{H} = \omega \hbar (N + 1/2)$ la secuencia descendente debe terminar. Pero la única forma posible de que termine es que haya un vector propio $|0\rangle$ tal que cuando $a_-$ actúa sobre él, el resultado sea cero. (No debemos confundir $|0\rangle$ con el vector cero.³) Simbólicamente, esto puede expresarse como

$$a_- |0\rangle = 0. \quad (10.29)$$

Al ser el estado de energía más baja, $|0\rangle$ es el estado fundamental, y su energía es $E_0 = \omega \hbar / 2$. Es un vector propio de $N$ con un valor propio 0. A menudo decimos que el estado fundamental es **aniquilado** por $a_-$.

Así que ves, la construcción abstracta de $a_+$, $a_-$ y $N$ dio sus frutos. Nos permitió encontrar todo el espectro de niveles de energía del oscilador armónico sin resolver una sola ecuación difícil. Este espectro consiste en los valores de energía,

$$E_n = \omega \hbar (n + 1/2) = \omega \hbar (1/2, 3/2, 5/2, \ldots). \quad (10.30)$$

Esta cuantización de los niveles de energía del oscilador armónico fue uno de los primeros resultados de la mecánica cuántica, y posiblemente el más importante. El átomo de hidrógeno es un ejemplo maravilloso de la mecánica cuántica, pero es, después de todo, solo

³El vector 0 es el vector cuyos componentes son todos cero. El vector $|0\rangle$, por otro lado, es un vector de estado con componentes distintos de cero.

  35 

10.7. DE VUELTA A LAS FUNCIONES DE ONDA 337

el átomo de hidrógeno. El oscilador armónico, por otro lado, aparece en todas partes, desde vibraciones cristalinas hasta circuitos eléctricos y ondas electromagnéticas. La lista continúa. Incluso los osciladores macroscópicos, como un niño en un columpio, tienen niveles de energía cuantizados, pero la presencia de la constante de Planck en la Ec. 10.30 significa que el espaciado entre niveles es tan pequeño que son completamente indetectables.

El espectro infinito de niveles de energía positivos para un oscilador armónico a veces se llama una **torre**, y a veces se llama una **escalera**. Se ilustra esquemáticamente en la Fig. 10.2.

### 10.7 De Vuelta a las Funciones de Onda

Este ejercicio ha demostrado ampliamente el notable poder de las álgebras de operadores, y el método del operador es ciertamente notable. Pero también es muy abstracto. ¿Es útil para ayudarnos a encontrar funciones de onda, que son más concretas y fáciles de visualizar? Absolutamente.

Comencemos con el estado fundamental. Acabamos de ver en la Ec. 10.29 que el estado fundamental es el estado único que es aniquilado por $a_-$. Ahora, reescribamos la Ec. 10.29 en términos de los operadores de posición y momento, y la función de onda del estado fundamental $\psi_0(x)$:

$$\frac{i}{\sqrt{2\omega \hbar}} (\mathbf{P} - i\omega \mathbf{X}) \psi_0(x) = 0,$$

o, dividiendo por la constante,

$$(\mathbf{P} - i\omega \mathbf{X}) \psi_0(x) = 0.$$

  35 

338 LECCIÓN 10. EL OSCILADOR ARMÓNICO

 Figura 10.2: Escalera de Niveles de Energía del Oscilador Armónico. Los niveles de energía están uniformemente espaciados. $a_+$ y $a_-$ suben y bajan el nivel de energía respectivamente. $N$ tiene un límite inferior de cero (el estado fundamental), pero ningún límite superior. 

Si ahora reemplazamos $\mathbf{P}$ con $-i\hbar \frac{d}{dx}$, obtenemos una ecuación diferencial de primer orden que es mucho más simple que la ecuación de Schrödinger de segundo orden:

$$\frac{d\psi_0}{dx} = -\frac{\omega x}{\hbar} \psi_0(x).$$

Esta es una ecuación diferencial simple que puedes resolver fácilmente.

  36 

10.7. DE VUELTA A LAS FUNCIONES DE ONDA 339

O, simplemente puedes comprobar que la función de onda del estado fundamental

$$e^{-\frac{\omega}{2\hbar} x^2}$$

en la Ec. 10.15 la resuelve. Calcular las funciones de onda para los estados excitados (no fundamentales) es aún más fácil —ni siquiera tenemos que resolver ninguna ecuación. Subamos la escalera hasta $n = 1$. Podemos hacerlo aplicando $a_+$ al estado fundamental. Llamemos a la función de onda de este nuevo estado $\psi_1(x)$.

Para evitar arrastrar la constante $\frac{-i}{\sqrt{2\omega \hbar}}$ en nuestros cálculos, simplemente la eliminaremos en nuestra definición de $a_+$. Esto solo afecta al coeficiente numérico. La ecuación resultante es

$$\psi_1(x) = (\mathbf{P} + i\omega \mathbf{X}) \psi_0(x)$$

o

$$\psi_1(x) = \left( -i\hbar \frac{\partial}{\partial x} + i\omega x \right) e^{-\frac{\omega}{2\hbar} x^2}.$$

Factorizando la $i$, obtenemos

$$\psi_1(x) = i \left( -\hbar \frac{\partial}{\partial x} + \omega x \right) e^{-\frac{\omega}{2\hbar} x^2}.$$

La parte "más difícil" de resolver esto es realizar una derivada fácil de $e^{-\frac{\omega}{2\hbar} x^2}$. Aquí está el resultado:

$$\psi_1(x) = i \left( -\hbar \left( -\frac{\omega}{\hbar} x e^{-\frac{\omega}{2\hbar} x^2} \right) + \omega x e^{-\frac{\omega}{2\hbar} x^2} \right)$$
$$= i \left( \omega x e^{-\frac{\omega}{2\hbar} x^2} + \omega x e^{-\frac{\omega}{2\hbar} x^2} \right)$$
$$= 2i \omega x e^{-\frac{\omega}{2\hbar} x^2},$$

  36 

340 LECCIÓN 10. EL OSCILADOR ARMÓNICO

o

$$\psi_1(x) = 2i \omega x \, \psi_0(x).$$

La única diferencia importante entre $\psi_0$ y $\psi_1$ es la presencia del factor $x$ en $\psi_1$. Esto tiene un efecto: hace que la función de onda del primer estado excitado tenga un cero, o nodo, en $x = 0$. Este es un patrón que continúa a medida que subimos en la escalera: cada estado excitado sucesivo tiene un nodo adicional. Podemos ver este patrón emerger calculando el segundo estado excitado en $n = 2$. Todo lo que tenemos que hacer es aplicar $a_+$ de nuevo:

$$\psi_2(x) = i \left( -\hbar \frac{\partial}{\partial x} + \omega x \right) \left( x e^{-\frac{\omega}{2\hbar} x^2} \right).$$

Podemos ver de inmediato que el término $\omega x$ resultará en un término $\omega x^2$. El $-\frac{\partial}{\partial x}$, mientras tanto, resultará en dos términos debido a la regla del producto para derivadas. Uno de estos términos provendrá de la exponencial (produciendo otro $\omega x^2$). El otro provendrá de tomar la derivada de $x$. Está claro que lo que obtendremos es un polinomio cuadrático. Si calculamos estas derivadas, la función de onda resultante es

$$\psi_2(x) = \left( -\hbar + 2\omega x^2 \right) e^{-\frac{\omega}{2\hbar} x^2}.$$

Y así continúa, todo el camino hacia arriba en la escalera. Podemos ver otro patrón aquí: cada función propia es un polinomio en $x$ multiplicado por $e^{-\frac{\omega}{2\hbar} x^2}$. Debido a que la exponencial tiende a cero más rápido

  36 

10.7. DE VUELTA A LAS FUNCIONES DE ONDA 341

que cualquiera de estos polinomios crece, cada función propia se aproxima a cero asintóticamente a medida que $x$ va a más o menos infinito. Además, dado que el grado de cada polinomio es uno mayor que el grado del anterior, cada función propia tiene un cero más que la anterior.⁴ Esto también explica por qué las funciones propias sucesivas alternan entre ser simétricas y antisimétricas. Específicamente, las funciones propias con polinomios de grado par son simétricas, mientras que aquellas con polinomios de grado impar son antisimétricas. Los polinomios en esta secuencia son muy conocidos. Se llaman los **polinomios de Hermite**. La función propia del estado fundamental $e^{-\frac{\omega}{2} x^2}$, que aparece en todas estas funciones propias de mayor energía, es simétrica en $x$.

La Fig. 10.3 muestra las funciones propias para varios niveles de energía diferentes. Cada función propia sucesiva oscila más rápidamente que la anterior. Esto corresponde a un aumento en el momento. Cuanto más rápidamente oscila la función de onda, mayor es el momento del sistema. En niveles de energía más altos, la función de onda también se vuelve más extendida. En términos físicos, esto significa que la masa se está moviendo más lejos del punto de equilibrio, y moviéndose más rápido.

Estas funciones propias contienen otra lección importante. Aunque se aproximan a cero asintóticamente (bastante rápido) nunca llegan a cero por completo. Eso significa que hay una pequeña pero finita probabilidad de encontrar la partícula "fuera del cuenco" que define su función de energía potencial. Este fenómeno,

⁴Resulta que estos ceros ocurren para valores reales de $x$, pero eso no es obvio a partir de lo que hemos visto. En un sentido físico, los ceros parecen un poco extraños, porque son puntos donde la masa en movimiento nunca se encontrará, aunque esté yendo y viniendo alegremente.

  36 

342 LECCIÓN 10. EL OSCILADOR ARMÓNICO

 Figura 10.3: Funciones Propias del Oscilador Armónico. Las amplitudes se muestran a la izquierda, las probabilidades a la derecha. Las funciones de onda de mayor energía oscilan más rápidamente y están más extendidas. 

conocido como **efecto túnel cuántico**, es completamente desconocido en la física clásica.

### 10.8 La Importancia de la Cuantización

Hemos escalado una montaña alta en estas lecciones, pero no es la última montaña. Mirando desde el punto de vista actual, podemos vislumbrar el enorme paisaje de la teoría cuántica de campos. Eso es material para otro libro. O quizás tres. Pero aún así, podemos ver un poco del terreno desde donde estamos.

Considera el ejemplo de la radiación electromagnética en una cavidad, como se muestra en la Fig. 10.4. En este contexto, una cavidad es una región del espacio delimitada por un par de espejos perfectamente reflectantes que mantienen la radiación rebotando sin fin de un lado a otro. Piensa en la cavidad como un largo tubo metálico a lo largo del cual la radiación puede viajar en ambas direcciones.

Hay muchas longitudes de onda que pueden caber en la cavidad. Consideremos ondas de longitud $\lambda$. Como todas las ondas, estas ondas oscilan, muy parecido a una masa en el extremo de un resorte. Pero es importante no confundirse aquí: los osciladores no son masas unidas a resortes. Lo que realmente oscila son los campos eléctrico y magnético. Para cada longitud de onda, hay un oscilador armónico matemático que describe la amplitud o intensidad del campo. Eso es un montón de osciladores armónicos funcionando todos simultáneamente. Afortunadamente, sin embargo, todos oscilan independientemente, por lo que podemos centrar nuestra atención en ondas de una longitud de onda particular e ignorar todas las


  36 


344 LECCIÓN 10. EL OSCILADOR ARMÓNICO

 Figura 10.4: Radiación Electromagnética en una Cavidad 

demás.

Solo hay un número importante asociado con un oscilador armónico —a saber, su frecuencia. Probablemente ya sabes cómo calcular la frecuencia de una onda de longitud $\lambda$:

$$\omega = \frac{2\pi c}{\lambda}.$$

En física clásica, por supuesto, la frecuencia es solo la frecuencia. Pero en mecánica cuántica, la frecuencia determina el cuanto de energía del oscilador. En otras palabras, la energía contenida en ondas de longitud $\lambda$ tiene que ser

$$(n + 1/2) \hbar \omega.$$

El término $(1/2)\hbar \omega$ no es importante para nuestros propósitos. Se llama **energía de punto cero**, y podemos ignorarlo. Si lo hacemos, la energía de las ondas de longitud $\lambda$ se convierte en

$$\frac{2\pi \hbar c}{\lambda} n,$$

donde $n$ puede ser cualquier entero desde cero en adelante. En otras palabras,

  36 

10.8. LA IMPORTANCIA DE LA CUANTIZACIÓN 345

la energía de una onda electromagnética está cuantizada en unidades indivisibles de

$$\frac{2\pi \hbar c}{\lambda}.$$

Para un físico clásico esto es muy extraño. No importa lo que hagas, la energía siempre viene en unidades irrompibles.

Puede que ya sepas que estas unidades se llaman **fotones**. De hecho, fotón es solo otro nombre para la unidad cuantizada de energía en un oscilador armónico cuántico. Pero también podemos describir los mismos hechos de otra manera. Al ser indivisibles, los fotones pueden considerarse partículas elementales. Una onda excitada a su $n$-ésimo estado cuántico puede considerarse como una colección de $n$ fotones.

¿Cuál es la energía de un solo fotón? Es fácil. Es solo la energía que se necesita para añadir una unidad más, a saber

$$E(\lambda) = \frac{2\pi \hbar c}{\lambda}.$$

Aquí, podemos ver algo que ha dominado la física durante más de un siglo: cuanto más corta es la longitud de onda de un fotón, mayor es su energía. ¿Por qué estaría un físico interesado en hacer fotones de longitud de onda corta, dado que son costosos en energía? La respuesta es para ver con mayor claridad. Como se discutió en la Lección 1, para resolver un objeto de un tamaño dado, debes usar ondas de ese tamaño o más pequeñas. Para ver una figura humana, una longitud de onda de unas pocas pulgadas es suficientemente buena. Para ver una mota de polvo diminuta, puede que necesites luz visible de una longitud de onda mucho más pequeña. Para resolver las partes de un protón, la longitud de onda debe ser más pequeña que $10^{-15}$ metros, y los correspondientes

  36 

346 LECCIÓN 10. EL OSCILADOR ARMÓNICO

fotones deben ser muy energéticos. Al final, todo vuelve al oscilador armónico.

Con esa nota, mis amigos, concluimos este volumen de la serie Mínimo Teórico. Espero veros en Relatividad Especial.

© Margaret Sloan

  36 

# Apéndice

**Matrices de Pauli**

$$\sigma_z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$
$$\sigma_x = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$$
$$\sigma_y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}$$

  36 

348 APÉNDICE

**Acción de los Operadores de Espín**

$$|u\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \quad \Leftrightarrow \quad
\sigma_z|u\rangle = |u\rangle,\quad
\sigma_x|u\rangle = |d\rangle,\quad
\sigma_y|u\rangle = i|d\rangle$$

$$|d\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \quad \Leftrightarrow \quad
\sigma_z|d\rangle = -|d\rangle,\quad
\sigma_x|d\rangle = |u\rangle,\quad
\sigma_y|d\rangle = -i|u\rangle$$

$$|r\rangle = \begin{pmatrix} \frac{1}{\sqrt{2}} \\ \frac{1}{\sqrt{2}} \end{pmatrix} \quad \Leftrightarrow \quad
\sigma_z|r\rangle = |l\rangle,\quad
\sigma_x|r\rangle = |r\rangle,\quad
\sigma_y|r\rangle = -i|l\rangle$$

$$|l\rangle = \begin{pmatrix} \frac{1}{\sqrt{2}} \\ -\frac{1}{\sqrt{2}} \end{pmatrix} \quad \Leftrightarrow \quad
\sigma_z|l\rangle = |r\rangle,\quad
\sigma_x|l\rangle = -|l\rangle,\quad
\sigma_y|l\rangle = i|r\rangle$$

$$|i\rangle = \begin{pmatrix} \frac{1}{\sqrt{2}} \\ \frac{i}{\sqrt{2}} \end{pmatrix} \quad \Leftrightarrow \quad
\sigma_z|i\rangle = |o\rangle,\quad
\sigma_x|i\rangle = i|o\rangle,\quad
\sigma_y|i\rangle = |i\rangle$$

$$|o\rangle = \begin{pmatrix} \frac{1}{\sqrt{2}} \\ -\frac{i}{\sqrt{2}} \end{pmatrix} \quad \Leftrightarrow \quad
\sigma_z|o\rangle = |i\rangle,\quad
\sigma_x|o\rangle = -i|i\rangle,\quad
\sigma_y|o\rangle = -|o\rangle$$

  37 

APÉNDICE 349

**Cambio de Base**

$$|r\rangle = \frac{1}{\sqrt{2}}|u\rangle + \frac{1}{\sqrt{2}}|d\rangle$$
$$|l\rangle = \frac{1}{\sqrt{2}}|u\rangle - \frac{1}{\sqrt{2}}|d\rangle$$
$$|i\rangle = \frac{1}{\sqrt{2}}|u\rangle + \frac{i}{\sqrt{2}}|d\rangle$$
$$|o\rangle = \frac{1}{\sqrt{2}}|u\rangle - \frac{i}{\sqrt{2}}|d\rangle$$

**Componente de Espín en la Dirección $\hat{n}$**

*Notación vectorial:*
$$\sigma_n = \vec{\sigma} \cdot \hat{n}$$

*Forma de componentes:*
$$\sigma_n = \sigma_x n_x + \sigma_y n_y + \sigma_z n_z$$

*Más concretamente:*
$$\sigma_n = n_x \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} + n_y \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} + n_z \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$

*Combinado en una sola matriz:*
$$\sigma_n = \begin{pmatrix}
n_z & (n_x - i n_y) \\
(n_x + i n_y) & -n_z
\end{pmatrix}$$

  37 

350 APÉNDICE

**Tablas de Multiplicación de Operadores de Espín**

Una palabra sobre la notación: La Tabla 3 a continuación usa el símbolo $i$ de dos maneras diferentes. Dentro de un ket, como $|io\rangle$, es parte de una etiqueta de estado —$io$ significa "in-out" (adentro-afuera). Pero cuando $i$ aparece fuera de un símbolo ket, como en $i|oo\rangle$, significa la unidad imaginaria.

**Tabla 1: Base Arriba-Abajo**

Vectores propios de 2 espines: $|uu\rangle, |ud\rangle, |du\rangle, |dd\rangle$

$$\begin{array}{c|cccc}
& |uu\rangle & |ud\rangle & |du\rangle & |dd\rangle \\ \hline
\sigma_z & |uu\rangle & |ud\rangle & -|du\rangle & -|dd\rangle \\
\sigma_x & |du\rangle & |dd\rangle & |uu\rangle & |ud\rangle \\
\sigma_y & i|du\rangle & i|dd\rangle & -i|uu\rangle & -i|ud\rangle \\ \hline
\tau_z & |uu\rangle & -|ud\rangle & |du\rangle & -|dd\rangle \\
\tau_x & |ud\rangle & |uu\rangle & |dd\rangle & |du\rangle \\
\tau_y & i|ud\rangle & -i|uu\rangle & i|dd\rangle & -i|du\rangle
\end{array}$$

**Tabla 2: Base Derecha-Izquierda**

Vectores propios de 2 espines: $|rr\rangle, |rl\rangle, |lr\rangle, |ll\rangle$

$$\begin{array}{c|cccc}
& |rr\rangle & |rl\rangle & |lr\rangle & |ll\rangle \\ \hline
\sigma_z & |lr\rangle & |ll\rangle & |rr\rangle & |rl\rangle \\
\sigma_x & |rr\rangle & |rl\rangle & -|lr\rangle & -|ll\rangle \\
\sigma_y & -i|lr\rangle & -i|ll\rangle & i|rr\rangle & i|rl\rangle \\ \hline
\tau_z & |rl\rangle & |rr\rangle & |ll\rangle & |lr\rangle \\
\tau_x & |rr\rangle & -|rl\rangle & |lr\rangle & -|ll\rangle \\
\tau_y & -i|rl\rangle & i|rr\rangle & -i|ll\rangle & i|lr\rangle
\end{array}$$

**Tabla 3: Base Adentro-Afuera**

Vectores propios de 2 espines: $|ii\rangle, |io\rangle, |oi\rangle, |oo\rangle$

$$\begin{array}{c|cccc}
& |ii\rangle & |io\rangle & |oi\rangle & |oo\rangle \\ \hline
\sigma_z & |oi\rangle & |oo\rangle & |ii\rangle & |io\rangle \\
\sigma_x & i|oi\rangle & i|oo\rangle & -|ii\rangle & -|io\rangle \\
\sigma_y & |ii\rangle & |io\rangle & -|oi\rangle & -|oo\rangle \\ \hline
\tau_z & |io\rangle & |ii\rangle & |oo\rangle & |oi\rangle \\
\tau_x & i|io\rangle & -i|ii\rangle & i|oo\rangle & -i|oi\rangle \\
\tau_y & |ii\rangle & -|io\rangle & |oi\rangle & -|oo\rangle
\end{array}$$

  37 
