Aquí se extraen los enunciados, texto y ecuaciones del archivo **Tarea 6_taller7a99.pdf**, manteniendo su estructura original:

---

## **1. Problema de Kepler**  
En el contexto del potencial V(r)= -k/r
a) Utilizando un software de cálculo simbólico, dibuje el **potencial efectivo** para diferentes valores de la constante $ k $ y analice cualitativamente las posibles situaciones.  
b) Construya un código que integre las ecuaciones de movimiento y dibuje las trayectorias de la partícula en el plano $ x-y $ para condiciones iniciales variadas. Relacione las trayectorias con el análisis del potencial efectivo .  

---

## **2. Potenciales adicionales**  
Siga el mismo procedimiento del item 1 pero esta vez estudie el movimiento de la partícula en los siguientes potenciales:
a) $V(r) = -\frac{k}{r^2}$: Considere condiciones iniciales a ambos lados de la órbita circular inestable y compare las trayectorias resultantes.  
b) **Potencial de Yukawa**: $V(r) = -\frac{k}{r} e^{-r/a}$, con $k$ y $a$ constantes positivas.  

---

## **3. Componentes en coordenadas polares**  
a) Determine las componentes radial y azimutal del vector posición $\vec{r}$, velocidad $\dot{\vec{r}}$ y aceleración $\ddot{\vec{r}}$.  
b) ¿Qué fuerza central produce las siguientes trayectorias?  
   - Espiral logarítmica: $r = e^{a\phi}$.  
   - Espiral de Arquímedes inversa: $r^{-1} = b\phi$, con $a > 0$, $b > 0$.  

---

## **4. Vector de Laplace-Runge-Lenz**  
Demuestre que en el problema de Kepler ($V(r) = -\frac{k}{r}$) existe una cantidad conservada adicional:  
$$
\vec{A} = \frac{\vec{p} \times \vec{l}}{mk} - \frac{\vec{r}}{r},
$$  
donde $\vec{p}$ es el momentum y $\vec{l}$ el momentum angular. Encuentre la ecuación de la trayectoria a partir de esta cantidad .  

¡Claro! Aquí tienes una explicación exhaustiva y paso a paso del **Vector de Runge-Lenz (R-L)**, un concepto fascinante y profundo de la mecánica clásica y cuántica.

---

### **1 Concepto: ¿Qué es el Vector Runge-Lenz?**

El Vector de Runge-Lenz (denotado comúnmente como **A** o **M**) es una **cantidad conservada** (es decir, una constante del movimiento) específica del **problema de Kepler**, que describe el movimiento de dos cuerpos que interactúan a través de una fuerza central que varía con el inverso del cuadrado de la distancia, como la fuerza gravitatoria o la fuerza electrostática.

En términos simples, es un vector que:
*   **Apunta** desde el foco de la elipse (donde está el cuerpo central, p. ej., el Sol) hacia el **perihelio** (el punto de máximo acercamiento).
*   Su **magnitud** es proporcional a la **excentricidad (e)** de la órbita elíptica.
*   Su **conservación** (el hecho de que no cambie con el tiempo) es la razón profunda por la cual las órbitas en el potencial 1/r son elipses **cerradas** y no precesan.

**Definición Matemática:**
El vector se define como:
$$ \vec{A} = \vec{p} \times \vec{L} - m k \frac{\vec{r}}{r} $$
donde:
*   $\vec{p}$ es el momento lineal de la partícula en órbita.
*   $\vec{L} = \vec{r} \times \vec{p}$ es su momento angular (también conservado).
*   $m$ es su masa (en gravitación, a menudo se usa la masa reducida $\mu$).
*   $k$ es una constante que define la fuerza. Para gravitación, $k = G M m$, y para electrostática, $k = -\frac{1}{4\pi\epsilon_0} Q q$ (el signo negativo indica atracción para cargas opuestas).
*   $\vec{r}$ es el vector posición desde el cuerpo central.

---


Para seguir la derivación y entender el concepto, necesitas estar familiarizado con:

1.  **Mecánica Newtoniana:** Leyes de Newton, fuerzas centrales, momentum lineal y angular.
2.  **Cálculo Vectorial:** Producto punto (·), producto cruz (×), derivadas temporales de vectores.
3.  **Cálculo Diferencial:** Reglas de derivación, especialmente la regla de la cadena y la derivada de un cociente.
4.  **Geometría de Cónicas:** Conocimiento básico de elipses, excentricidad, focos.
5.  **El Problema de Kepler:** Saber que las órbitas en un potencial $1/r$ son elipses, parábolas o hipérbolas.

---

Derivación Paso a Paso (¿Por qué se conserva?)

Vamos a demostrar que la derivada temporal de $\vec{A}$ es cero, probando así que es una constante del movimiento.

**Paso 1: La Fuerza Central**
La fuerza que gobierna el sistema es:
$$ \vec{F} = -\frac{k}{r^2} \hat{r} $$
donde $\hat{r} = \frac{\vec{r}}{r}$ es el vector unitario radial.

**Paso 2: Derivada del Momento Angular**
Sabemos que el momento angular $\vec{L} = \vec{r} \times \vec{p}$ se conserva ($\frac{d\vec{L}}{dt} = 0$) porque la fuerza es central. Esto es crucial.

**Paso 3: Derivada de un Producto Cruz (Regla de la Cadena)**
Queremos calcular $\frac{d\vec{A}}{dt}$:
$$ \frac{d\vec{A}}{dt} = \frac{d}{dt}(\vec{p} \times \vec{L}) - m k \frac{d}{dt} \left( \frac{\vec{r}}{r} \right) $$

Calculemos cada término por separado.

**Paso 4: Primer Término - $\frac{d}{dt}(\vec{p} \times \vec{L})$**
Usamos la regla de la derivada de un producto:
$$ \frac{d}{dt}(\vec{p} \times \vec{L}) = \frac{d\vec{p}}{dt} \times \vec{L} + \vec{p} \times \frac{d\vec{L}}{dt} $$
Sabemos que:
*   $\frac{d\vec{p}}{dt} = \vec{F} = -\frac{k}{r^2} \hat{r}$ (Segunda Ley de Newton)
*   $\frac{d\vec{L}}{dt} = 0$ (Conservación del Momento Angular)

Por lo tanto, el segundo término es cero y nos queda:
$$ \frac{d}{dt}(\vec{p} \times \vec{L}) = \left( -\frac{k}{r^2} \hat{r} \right) \times \vec{L} $$

**Paso 5: Segundo Término - $m k \frac{d}{dt} \left( \frac{\vec{r}}{r} \right)$**
Este es un término más complicado. Calculamos la derivada del vector unitario:
$$ \frac{d}{dt} \left( \frac{\vec{r}}{r} \right) = \frac{d}{dt} \left( \frac{\vec{r}}{r} \right) = \frac{1}{r} \frac{d\vec{r}}{dt} + \vec{r} \frac{d}{dt}\left( \frac{1}{r} \right) $$
Usando la regla de la cadena:
*   $\frac{d\vec{r}}{dt} = \vec{v}$
*   $\frac{d}{dt}\left( \frac{1}{r} \right) = -\frac{1}{r^2} \frac{dr}{dt}$

Además, notamos que $\frac{dr}{dt} = \frac{d}{dt}(\vec{r} \cdot \vec{r})^{1/2} = \frac{1}{2}(\vec{r} \cdot \vec{r})^{-1/2} (2\vec{r} \cdot \dot{\vec{r}}) = \frac{\vec{r} \cdot \vec{v}}{r}$.

Juntando todo:
$$ \frac{d}{dt} \left( \frac{\vec{r}}{r} \right) = \frac{\vec{v}}{r} - \vec{r} \frac{1}{r^2} \left( \frac{\vec{r} \cdot \vec{v}}{r} \right) = \frac{\vec{v}}{r} - \frac{(\vec{r} \cdot \vec{v})\vec{r}}{r^3} $$

**Paso 6: Combinar Ambos Términos**
Ahora reintroducimos todo en la ecuación de $\frac{d\vec{A}}{dt}$:
$$ \frac{d\vec{A}}{dt} = \left( -\frac{k}{r^2} \hat{r} \times \vec{L} \right) - m k \left( \frac{\vec{v}}{r} - \frac{(\vec{r} \cdot \vec{v})\vec{r}}{r^3} \right) $$
Simplificamos notando que $\hat{r} = \frac{\vec{r}}{r}$, por lo que $\hat{r} \times \vec{L} = \frac{\vec{r}}{r} \times \vec{L}$:
$$ \frac{d\vec{A}}{dt} = -\frac{k}{r^3} \vec{r} \times \vec{L} - \frac{m k}{r} \vec{v} + \frac{m k}{r^3} (\vec{r} \cdot \vec{v}) \vec{r} $$

**Paso 7: El "Truco" del Momento Angular**
Recordamos la definición de momento angular: $\vec{L} = \vec{r} \times \vec{p} = m (\vec{r} \times \vec{v})$. Por una identidad vectorial, $\vec{r} \times \vec{L} = \vec{r} \times (m (\vec{r} \times \vec{v}))$.

Usamos la **identidad del triple producto vectorial**: $\vec{a} \times (\vec{b} \times \vec{c}) = \vec{b}(\vec{a} \cdot \vec{c}) - \vec{c}(\vec{a} \cdot \vec{b})$.
Aplicándola con $\vec{a}=\vec{r}, \vec{b}=\vec{r}, \vec{c}=\vec{v}$:
$$ \vec{r} \times \vec{L} = m [ \vec{r} \times (\vec{r} \times \vec{v}) ] = m [ \vec{r}(\vec{r} \cdot \vec{v}) - \vec{v}(\vec{r} \cdot \vec{r}) ] = m [ (\vec{r} \cdot \vec{v})\vec{r} - r^2 \vec{v} ] $$

**Paso 8: Sustitución Final y Cancelación Milagrosa**
Sustituimos este resultado en nuestro $\frac{d\vec{A}}{dt}$:
$$ \frac{d\vec{A}}{dt} = -\frac{k}{r^3} \left( m [ (\vec{r} \cdot \vec{v})\vec{r} - r^2 \vec{v} ] \right) - \frac{m k}{r} \vec{v} + \frac{m k}{r^3} (\vec{r} \cdot \vec{v}) \vec{r} $$
$$ \frac{d\vec{A}}{dt} = -\frac{m k}{r^3} (\vec{r} \cdot \vec{v})\vec{r} + \frac{m k}{r^3} r^2 \vec{v} - \frac{m k}{r} \vec{v} + \frac{m k}{r^3} (\vec{r} \cdot \vec{v}) \vec{r} $$

Observa que el primer y el último término son iguales pero con signo opuesto: **$-\frac{m k}{r^3} (\vec{r} \cdot \vec{v})\vec{r} + \frac{m k}{r^3} (\vec{r} \cdot \vec{v}) \vec{r} = 0$**.

Los términos del medio son: $\frac{m k}{r^3} r^2 \vec{v} - \frac{m k}{r} \vec{v} = \frac{m k}{r} \vec{v} - \frac{m k}{r} \vec{v} = 0$.

**¡Resultado Final!**
$$ \frac{d\vec{A}}{dt} = 0 $$
Hemos demostrado que la derivada temporal del vector de Runge-Lenz es cero. **Por lo tanto, es una constante del movimiento.**

---

Aplicaciones e Importancia

1.  **Determinación de la Órbita:**
    Si tomamos el producto punto $\vec{A} \cdot \vec{r}$ y usamos identidades vectoriales, se puede derivar la **ecuación de la órbita**:
    $$ \vec{A} \cdot \vec{r} = A r \cos\theta = L^2 - m k r $$
    Reordenando:
    $$ r = \frac{L^2 / m k}{1 + (A / m k) \cos\theta} $$
    ¡Esta es exactamente la ecuación de una **cónica** (elipse, parábola, hipérbola) en coordenadas polares! La comparación con la forma estándar $r = \frac{p}{1 + e \cos\theta}$ nos da:
    *   **Semilatus Rectum:** $p = L^2 / m k$
    *   **Excentricidad:** $e = A / m k$
    Esto prueba que la órbita es una elipse para $e<1$ ($A < m k$) y muestra que $\vec{A}$ apunta en la dirección del perihelio ($\theta = 0$).

2.  **Explicación de Órbitas Cerradas:**
    En la mayoría de fuerzas centrales, las órbitas no son elipses cerradas; precesan (giran). La conservación de $\vec{A}$ fuerza a la elipse a mantener una orientación fija en el espacio, evitando la precesión. Esto es una simetría **oculta** del potencial $1/r$.

3.  **Mecánica Cuántica:**
    La conservación del vector R-L se traslada al átomo de hidrógeno (que también tiene un potencial $1/r$). Allí, explica por qué los niveles de energía con diferente momento angular (diferente $l$) pero mismo número cuántico principal ($n$) están **degenerados** (tienen la misma energía). Esta simetría adicional es la razón por la que el grupo de simetría del átomo de hidrógeno es SO(4), más grande que el simple grupo de rotaciones SO(3).

4.  **Teoría de Perturbaciones:**
    En relatividad general, el potencial gravitatorio ya no es exactamente $1/r$. El vector R-L **deja de conservarse**, y esta es la razón fundamental por la que la órbita de Mercurio **precesa**.

---
Curiosidad Histórica

Aunque lleva el nombre de los físicos Carl Runge y Wilhelm Lenz, quienes lo popularizaron en la mecánica cuántica y clásica respectivamente, fue descubierto múltiples veces a lo largo de la historia. **Jakob Hermann** (1710) y **Pierre-Simon Laplace** (1799) ya lo conocían en sus formas equivalentes.

---

## **Conclusión**

El vector de Runge-Lenz es mucho más que una curiosidad matemática. Es una **ley de conservación** profunda íntimamente ligada a una **simetría oculta** del espacio en los potenciales de tipo $1/r$. Su conservación es la piedra angular que explica la forma perfectamente elíptica y cerrada de las órbitas planetarias, y su generalización en mecánica cuántica resuelve el misterio de la degeneración de energía en el átomo de hidrógeno. Es un puente elegante entre la geometría de las cónicas y las leyes dinámicas de la física.

---

## **5. Corrección relativista al potencial de Kepler**  
$V(r) = -\frac{k}{r} - \frac{\alpha}{r^3}$, con $k = GmM$, $\alpha = \frac{Gl^2M}{c^2m}$.  
a) Demuestre que la ecuación diferencial de la órbita es:  
$$
\frac{\partial^2 u}{\partial \theta^2} + u = \frac{1}{p} + \beta u^2, \quad p = \frac{l^2}{mk}, \quad \beta = \frac{3GM}{c^2}.
$$  
b) Calcule el ángulo de precesión del perihelio por ciclo $ \delta\theta $ mediante una solución perturbativa.  

---

## **6. Potencial $ V(r) = -\frac{k}{r^4} $**  
Encuentre la energía $ E $, el momento angular $ l $ y el período $ \tau $ de la órbita circular inestable de radio $ R $. Demuestre que otra órbita con mismos $ E $ y $ l $ tiende asintóticamente a $ R $, verificando con el programa del punto 1.  

---

## **7. Integral de órbita con corrección relativista**  
Calcule el ángulo de precesión del perihelio por ciclo $ \delta\theta $ como corrección al ángulo apsidal del problema de Kepler mediante la integral:  
$$
\delta\theta = 2 \int_{r_1}^{r_2} \frac{l/mr^2}{\sqrt{2m[E - V(r) - l^2/(2mr^2)]}} \, dr - 2\pi.
$$  

---

## **8. Distancia Sol-Júpiter**  
Dada la distancia promedio Tierra-Sol $ a_E = 1.49 \times 10^8 $ km y el período orbital de Júpiter ($ 11.86 $ años), determine la distancia promedio entre el Sol y Júpiter.  

---

## **9. Partícula bajo fuerza central**  
Una partícula de masa $ m $ se mueve bajo la fuerza $ \vec{F} = -m\gamma \frac{\hat{e}_r}{r^2} $.  
- Inicialmente está en $ C $, a distancia $ c $ del centro de fuerzas $ O $, con velocidad $ v_0 = (\gamma/c)^{1/2} $ formando un ángulo $ \alpha $ con $ OC $.  
- Encuentre las distancias apsidales y los ejes semi-mayor y semi-menor de la órbita elíptica resultante.  

---

## **10. Cometas Hyakutake y Hale-Bopp**  
Para el cometa Hyakutake ($ e = 0.999846 $, perihelio $ 0.230123 $ UA) y Hale-Bopp ($ e = 0.995075 $, perihelio $ 0.913959 $ AU):  
- Estime el tiempo hasta su próximo retorno.  
- Calcule el afelio y compárelo con el afelio de Plutón ($ 39.37 $ UA).  

---
## **3. Componentes en coordenadas polares**  
a) **Componentes radial y azimutal**  
- **Vector posición $ \vec{r} $:**  
  - Radial: $ r $ (directamente el módulo del vector).  
  - Azimutal: $ 0 $ (no hay componente angular en la posición) .  

- **Velocidad $ \dot{\vec{r}} $:**  
  - Radial: $ \dot{r} $ (derivada temporal del módulo).  
  - Azimutal: $ r \dot{\theta} $ (producto del módulo y la velocidad angular) .  

- **Aceleración $ \ddot{\vec{r}} $:**  
  - Radial: $ \ddot{r} - r \dot{\theta}^2 $ (aceleración centrípeta y radial).  
  - Azimutal: $ r \ddot{\theta} + 2 \dot{r} \dot{\theta} $ (aceleración de Coriolis y angular) .  

b) **Fuerza central para trayectorias específicas**  
- **Espiral logarítmica $ r = e^{a\phi} $:**  
  La fuerza es inversa al cubo de $ r $, $ F(r) \propto -\frac{1}{r^3} $, derivada de la ecuación de órbita usando la transformación $ u = \frac{1}{r} $ .  

- **Espiral de Arquímedes inversa $ r^{-1} = b\phi $:**  
  Similarmente, la fuerza también es $ F(r) \propto -\frac{1}{r^3} $, aunque con parámetros ajustados según $ b $ .  

---

## **4. Vector de Laplace-Runge-Lenz**  
**Demostración de conservación:**  
Para $V(r) = -\frac{k}{r}$, el vector $\vec{A}$ se conserva. Usando las ecuaciones de movimiento y la conservación del momento angular $\vec{l}$, se muestra que $\frac{d\vec{A}}{dt} = 0$.  

**Ecuación de la trayectoria:**  
Al tomar $\vec{A} \cdot \vec{r} = \frac{l^2}{mk} - r$, se obtiene la ecuación de una cónica:  
$$
r = \frac{l^2/mk}{1 + A \cos \theta},
$$  
donde $ A $ está relacionado con la excentricidad $ e $, confirmando órbitas elípticas, parabólicas o hiperbólicas .  

---

## **5. Corrección relativista al potencial de Kepler**  
a) **Ecuación diferencial de la órbita:**  
Usando $ u = \frac{1}{r} $ y la energía efectiva, se deriva:  
$$
\frac{\partial^2 u}{\partial \theta^2} + u = \frac{1}{p} + \beta u^2, \quad p = \frac{l^2}{mk}, \quad \beta = \frac{3GM}{c^2}.
$$  
Esto incluye la corrección relativista $ \beta u^2 $ .  

b) **Ángulo de precesión $ \delta\theta $:**  
Mediante perturbación, la precesión por ciclo es:  
$$
\delta\theta = \frac{2\pi \beta}{p} = \frac{6\pi GM}{c^2 p}.
$$  
Para $ p = a(1 - e^2) $, esto reproduce el resultado clásico de la relatividad general .  

---

**Referencias:**  
 Vectores en coordenadas polares.  
 Componentes radial y angular.  
 Coordenadas cartesianas y polares.  
 Componentes de aceleración.  
 Transformación de coordenadas y corrección relativista.