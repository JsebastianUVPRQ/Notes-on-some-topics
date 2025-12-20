## PROBLEMA 1

---

### **Paso 1: Configuración del Hamiltoniano**

Antes de escribir la ecuación de Hamilton-Jacobi, necesitamos construir el Hamiltoniano del sistema en coordenadas polares $(r, \theta)$.

**1. Potenciales:**

- Potencial escalar (fuerza central): $V(r) = \frac{1}{2}kr^2$.
    
- Potencial vectorial: $\vec{A} = \frac{1}{2}\vec{B} \times \vec{r}$.
    
    - Dado que $\vec{B} = B\hat{z}$ (perpendicular al plano) y $\vec{r} = r\hat{r}$ (en coordenadas polares planas), el producto cruz es:
        
        $$\vec{A} = \frac{1}{2} (B\hat{z}) \times (r\hat{r}) = \frac{1}{2}Br \hat{\theta}$$
        
    - Por lo tanto, la componente angular de $\vec{A}$ es $A_\theta = \frac{1}{2}Br$ y la radial $A_r = 0$.
        

2. Hamiltoniano para una partícula cargada:

El Hamiltoniano general para una partícula con carga $q$ en un campo electromagnético es:

$$H = \frac{1}{2m}(\vec{p} - q\vec{A})^2 + V(r)$$

1

En coordenadas polares, el término del momento cinético al cuadrado $(\vec{p} - q\vec{A})^2$ se descompone en parte radial y angular:

$$(\vec{p} - q\vec{A})^2 = p_r^2 + \left(\frac{p_\theta}{r} - qA_\theta\right)^2$$

Sustituyendo $A_\theta = \frac{1}{2}Br$:

$$H = \frac{p_r^2}{2m} + \frac{1}{2m}\left(\frac{p_\theta}{r} - \frac{qBr}{2}\right)^2 + \frac{1}{2}kr^2$$

---

### **Paso 2: La Ecuación de Hamilton-Jacobi (Inciso a)**

Buscamos la función característica de Hamilton $W(r, \theta)$. La relación con la función principal $S$ es $S = W - Et$, ya que el Hamiltoniano no depende explícitamente del tiempo.

1. Planteamiento de la ecuación:

En el formalismo H-J, reemplazamos los momentos canónicos por derivadas parciales de $W$:

$$p_r \rightarrow \frac{\partial W}{\partial r}, \quad p_\theta \rightarrow \frac{\partial W}{\partial \theta}$$

Sustituyendo en el Hamiltoniano e igualando a la energía total $E$:

$$\frac{1}{2m}\left(\frac{\partial W}{\partial r}\right)^2 + \frac{1}{2m}\left(\frac{1}{r}\frac{\partial W}{\partial \theta} - \frac{qBr}{2}\right)^2 + \frac{1}{2}kr^2 = E$$

2

2. Separación de Variables:

Observamos que la coordenada $\theta$ no aparece explícitamente en la ecuación (es una coordenada cíclica), aunque sí aparece su derivada. Esto nos permite proponer una solución separable:

$$W(r, \theta) = W_r(r) + W_\theta(\theta)$$

Como $\theta$ es cíclica, definimos la constante de separación $\alpha_\theta$ (que corresponde al momento angular canónico conservado):

$$\frac{\partial W}{\partial \theta} = \frac{dW_\theta}{d\theta} = \alpha_\theta \quad \Rightarrow \quad W_\theta = \alpha_\theta \theta$$

3. Reducción a una integral:

Sustituimos $\frac{\partial W}{\partial \theta} = \alpha_\theta$ en la ecuación H-J y despejamos la parte radial $\frac{dW_r}{dr}$:

$$\frac{1}{2m}\left(\frac{dW_r}{dr}\right)^2 + \frac{1}{2mr^2}\left(\alpha_\theta - \frac{qBr^2}{2}\right)^2 + \frac{1}{2}kr^2 = E$$

Multiplicamos por $2m$ y reorganizamos para aislar la derivada:

$$\left(\frac{dW_r}{dr}\right)^2 = 2mE - mkr^2 - \frac{1}{r^2}\left(\alpha_\theta - \frac{qBr^2}{2}\right)^2$$

Tomamos la raíz cuadrada e integramos:

$$W_r(r) = \int \sqrt{2mE - mkr^2 - \frac{1}{r^2}\left(\alpha_\theta - \frac{qBr^2}{2}\right)^2} \, dr$$

3

La función característica completa es:

$$W = \alpha_\theta \theta + \int \sqrt{2mE - mkr^2 - \frac{1}{r^2}\left(\alpha_\theta - \frac{qBr^2}{2}\right)^2} \, dr$$

---

### **Paso 3: Solución del movimiento para $p_\theta = 0$ (Inciso b)**

El problema nos pide resolver para el caso específico donde el momento canónico angular es cero en $t=0$.

1. Condición de momento angular:

Sabemos que $p_\theta = \alpha_\theta$. Como el Hamiltoniano es independiente de $\theta$, $p_\theta$ se conserva.

Si $p_\theta = 0$ en $t=0$, entonces $\alpha_\theta = 0$ para todo el movimiento.

2. Simplificación de la ecuación radial:

Sustituimos $\alpha_\theta = 0$ en la expresión dentro de la raíz (el integrando):

$$\text{Término angular} = -\frac{1}{r^2}\left(0 - \frac{qBr^2}{2}\right)^2 = -\frac{1}{r^2}\left(\frac{q^2B^2r^4}{4}\right) = -\frac{q^2B^2r^2}{4}$$

La ecuación para el momento radial queda:

$$\left(\frac{dW_r}{dr}\right)^2 = 2mE - mkr^2 - \frac{q^2B^2}{4}r^2$$

Factorizamos $r^2$:

$$(m \dot{r})^2 = 2mE - \left(mk + \frac{q^2B^2}{4}\right)r^2$$

Dividimos por $m^2$:

$$\dot{r}^2 = \frac{2E}{m} - \left(\frac{k}{m} + \frac{q^2B^2}{4m^2}\right)r^2$$

Definimos una frecuencia efectiva $\omega_{eff}$:

$$\omega_{eff}^2 \equiv \frac{k}{m} + \left(\frac{qB}{2m}\right)^2$$

Entonces:

$$\dot{r}^2 = \frac{2E}{m} - \omega_{eff}^2 r^2$$

Esta es la ecuación diferencial de un Oscilador Armónico Simple. La solución para $r(t)$ es:

$$r(t) = A \sin(\omega_{eff} t + \phi)$$

Donde la amplitud máxima es $A = \sqrt{\frac{2E}{m\omega_{eff}^2}}$. Dado que $r=0$ en el origen y $r$ debe ser positivo, la partícula oscila radialmente (pasando por el origen si las condiciones iniciales lo permiten, o simplemente oscilando en distancia).

3. Movimiento Angular:

Para encontrar $\theta(t)$, usamos una de las ecuaciones de movimiento de Hamilton ($\dot{\theta} = \frac{\partial H}{\partial p_\theta}$) o la relación H-J. Usando el Hamiltoniano que derivamos en el Paso 1:

$$\dot{\theta} = \frac{\partial H}{\partial p_\theta} = \frac{1}{m}\left(\frac{p_\theta}{r} - \frac{qBr}{2}\right) \cdot \frac{1}{r} = \frac{1}{mr^2}\left(p_\theta - \frac{qBr^2}{2}\right)$$

Con la condición $p_\theta = 0$:

$$\dot{\theta} = \frac{1}{mr^2}\left(0 - \frac{qBr^2}{2}\right) = -\frac{qB}{2m}$$

Observe que los $r^2$ se cancelan. Esto es crucial:

$$\dot{\theta} = -\frac{qB}{2m} = \text{constante}$$

Esta velocidad angular constante es exactamente la **Frecuencia de Larmor** ($\omega_L$).

---

### **Resumen de la Solución Final**

Para el caso $p_\theta = 0$:

1. **Radial:** La distancia al origen $r$ oscila armónicamente con una frecuencia $\omega_{eff} = \sqrt{\frac{k}{m} + \omega_L^2}$.
    
2. **Angular:** La partícula rota con velocidad angular constante $\dot{\theta} = -\omega_L = -\frac{qB}{2m}$.
    

La trayectoria es una elipse que rota (precesa) centrada en el origen. Físicamente, el sistema se comporta como un oscilador armónico isótropo 2D modificado por el campo magnético, lo que resulta en un cambio de frecuencia y una rotación del sistema de referencia.

---
### **2. Una H dependiente del tiempo (Goldstein Cap.10 #8)**

El problema:

Dado el Hamiltoniano:

$$H = \frac{p^2}{2m} - mAtx$$

Resolver para el movimiento con condiciones iniciales en $t=0$: $x=0$ y $p=mv_0$.

#### **Paso 1: Plantear la Ecuación de Hamilton-Jacobi**

Como el Hamiltoniano depende del tiempo ($H = H(t)$), usamos la ecuación general de Hamilton-Jacobi:

$$\frac{\partial S}{\partial t} + H\left(x, \frac{\partial S}{\partial x}, t\right) = 0$$

Sustituyendo el Hamiltoniano dado y reemplazando $p$ por $\frac{\partial S}{\partial x}$:

$$\frac{\partial S}{\partial t} + \frac{1}{2m}\left(\frac{\partial S}{\partial x}\right)^2 - mAtx = 0$$

#### **Paso 2: Proponer una solución (Ansatz)**

Aquí es donde la "pista" del problema es útil. Si pensamos brevemente en las leyes de Newton:

- Fuerza $= -\frac{\partial V}{\partial x} = -\frac{\partial}{\partial x}(-mAtx) = mAt$.
    
- $F = \dot{p} \implies \dot{p} = mAt$.
    
- Esto implica que $p(t)$ será una función **solo del tiempo**, no de la posición $x$.
    

En el formalismo H-J, el momento está dado por $p = \frac{\partial S}{\partial x}$. Si $p$ solo depende del tiempo, entonces $\frac{\partial S}{\partial x}$ debe ser una función solo de $t$, llamémosla $f(t)$.

Integrando $\frac{\partial S}{\partial x} = f(t)$ respecto a $x$, obtenemos que $S$ debe tener la forma:

$$S(x, \alpha, t) = f(t)x + g(t)$$

Donde $f(t)$ y $g(t)$ son funciones desconocidas que debemos encontrar.

#### **Paso 3: Sustituir y resolver las ecuaciones diferenciales**

Calculamos las derivadas de nuestro ansatz:

- $\frac{\partial S}{\partial t} = \dot{f}(t)x + \dot{g}(t)$
    
- $\frac{\partial S}{\partial x} = f(t)$
    

Sustituimos en la ecuación H-J del Paso 1:

$$(\dot{f}x + \dot{g}) + \frac{1}{2m}(f)^2 - mAtx = 0$$

Agrupamos los términos que tienen $x$ y los términos que no (términos independientes):

$$\left[ \dot{f} - mAt \right]x + \left[ \dot{g} + \frac{f^2}{2m} \right] = 0$$

Para que esta ecuación sea válida para _cualquier_ posición $x$, el coeficiente de $x$ debe ser cero y el término independiente debe ser cero por separado.

Ecuación A (Coeficiente de x):

$$\dot{f} - mAt = 0 \implies \dot{f} = mAt$$

Integramos respecto al tiempo:

$$f(t) = \frac{1}{2}mAt^2 + C$$

La constante de integración $C$ está relacionada con el momento. Como $p = \frac{\partial S}{\partial x} = f(t)$, en $t=0$ tenemos $p(0) = C$. El problema nos dice que $p(0) = mv_0$. Identificamos esta constante como nuestro momento generalizado constante $\alpha$.

$$f(t) = \frac{1}{2}mAt^2 + \alpha$$

(Donde hemos elegido $\alpha = mv_0$).

Ecuación B (Término independiente):

$$\dot{g} + \frac{f^2}{2m} = 0 \implies \dot{g} = -\frac{1}{2m}f(t)^2$$

Sustituimos $f(t)$:

$$\dot{g} = -\frac{1}{2m} \left( \frac{1}{2}mAt^2 + \alpha \right)^2$$

Expandimos el cuadrado:

$$\dot{g} = -\frac{1}{2m} \left( \frac{1}{4}m^2A^2t^4 + m A \alpha t^2 + \alpha^2 \right)$$

Integramos para hallar $g(t)$:

$$g(t) = -\frac{1}{2m} \left( \frac{m^2A^2}{20}t^5 + \frac{m A \alpha}{3}t^3 + \alpha^2 t \right)$$

#### **Paso 4: Construir la Función Principal S**

Ahora tenemos la función completa:

$$S(x, \alpha, t) = \left( \frac{1}{2}mAt^2 + \alpha \right)x - \frac{mA^2}{40}t^5 - \frac{A \alpha}{6}t^3 - \frac{\alpha^2}{2m}t$$

#### **Paso 5: Obtener las ecuaciones de movimiento**

Usamos la propiedad de la transformación canónica donde la nueva coordenada $Q$ (o $\beta$) es constante:

$$\beta = \frac{\partial S}{\partial \alpha}$$

Derivamos $S$ respecto a $\alpha$:

$$\beta = x(1) - \frac{A}{6}t^3 - \frac{2\alpha}{2m}t$$

$$\beta = x - \frac{A}{6}t^3 - \frac{\alpha}{m}t$$

Despejamos $x(t)$:

$$x(t) = \beta + \frac{\alpha}{m}t + \frac{A}{6}t^3$$

**Aplicar condiciones iniciales:**

- En $t=0$, $x(0) = \beta$.
    
- El problema dice que $x=0$ en $t=0$, por lo tanto, $\beta = 0$.
    
- Recordemos que definimos $\alpha = mv_0$.
    

Sustituyendo $\beta$ y $\alpha$:

$$x(t) = \frac{mv_0}{m}t + \frac{A}{6}t^3$$

Solución final:

$$x(t) = v_0 t + \frac{1}{6}At^3$$

$$p(t) = \frac{\partial S}{\partial x} = f(t) = mv_0 + \frac{1}{2}mAt^2$$

Esta solución coincide perfectamente con lo que obtendrías integrando $F=ma$ dos veces ($a = At$), validando el método de Hamilton-Jacobi.
