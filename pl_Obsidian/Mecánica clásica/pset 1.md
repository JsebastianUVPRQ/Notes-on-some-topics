
---

## **3. Algunos ejercicios con sistemas de coordenadas**

**a)** Encuentra la conversión de coordenadas esféricas (también llamadas _polares_) a coordenadas cartesianas, es decir, las funciones  
$x(r,\theta,\phi)$, $y(r,\theta,\phi)$ y $z(r,\theta,\phi)$.  
Encuentra también las funciones inversas $r(x,y,z)$, etc.

---

**b)** Encuentra la conversión de coordenadas cilíndricas a coordenadas cartesianas, es decir, las funciones  
$x(\rho,\phi,z)$, etc.  
Encuentra también las funciones inversas $\rho(x,y,z)$, etc.

---

**c)** Una partícula que parte del origen se mueve en la dirección $\hat{r}$ con velocidad $v_0$ y ángulos polares $\phi_0$ y $\theta_0$, tales que  
$\vec{v} = v_0 \hat{r}$.  
Expresa $\vec{v}$ en coordenadas cartesianas.

---

**d) OPCIONAL:** Una partícula que parte de un punto $\vec{x}_0$ se mueve con la misma velocidad del apartado (c) anterior (ya no en la dirección $\hat{r}$). Expresa $\vec{v}$ en coordenadas polares.  
A partir de este ejercicio, deberías notar una **gran debilidad del sistema de coordenadas polares**.

---
# Soluciones

---
# Prerrequisitos / teoría y matemáticas usadas

Antes de empezar, estas son las herramientas teóricas y matemáticas que usaremos:

1. **Geometría en $\mathbb{R}^3$**: vectores, producto escalar, norma, proyecciones.
    
2. **Sistemas de coordenadas**:
    
    - Definición y convención de **coordenadas esféricas**: $(r,\theta,\phi)$ con $r\ge0$, $\theta\in[0,\pi]$ (colatitud o ángulo polar medido desde el eje $z$) y $\phi\in(-\pi,\pi]$ (azimutal en el plano $xy$).
        
    - Definición de **coordenadas cilíndricas**: $(\rho,\phi,z)$ con $\rho\ge0$, $\phi$ igual que antes, $z\in\mathbb R$.
        
3. **Vectores unitarios en coordenadas esféricas**: expresiones de $\hat r,\hat\theta,\hat\phi$ en la base cartesiana.
    
4. **Funciones inversas y la función $\operatorname{atan2}(y,x)$** para obtener el ángulo azimutal de forma correcta en los cuatro cuadrantes.
    
5. **Producto escalar para proyectar vectores** sobre una base ortonormal.
    

---

# Ejercicio (a) — Conversión esféricas $\leftrightarrow$ cartesianas

**Enunciado:** Encuentra la conversión de coordenadas esféricas (aka “polares”) a cartesianas: $x(r,\theta,\phi)$, $y(r,\theta,\phi)$, $z(r,\theta,\phi)$. Encuentra también las funciones inversas $r(x,y,z)$, $\theta(x,y,z)$, $\phi(x,y,z)$.

## Paso 1 — Definición geométrica

Sea un punto en $\mathbb{R}^3$ cuya posición en coordenadas esféricas es $(r,\theta,\phi)$. Por definición:

- $r$ es la distancia desde el origen,
    
- $\theta$ es el ángulo entre el vector posición y el eje $z$,
    
- $\phi$ es el ángulo en el plano $xy$ medido desde el eje $x$.
    

## Paso 2 — Transformación directa (esféricas a cartesianas)

Proyección sobre los ejes usando trigonometría:

- Componente en $z$: $z = r\cos\theta$.
    
- Proyección radial en el plano $xy$ (distancia desde el eje $z$): $r\sin\theta$.
    
    - Luego las componentes $x,y$ son:
        

$x = r\sin\theta\cos\phi$  
$y = r\sin\theta\sin\phi$  
$z = r\cos\theta$

## Paso 3 — Transformación inversa (cartesianas a esféricas)

Dado $(x,y,z)$:

- $r = \sqrt{x^2 + y^2 + z^2}$.
    
- $\theta = \arccos!\left(\dfrac{z}{r}\right)$ (si $r\neq 0$). Alternativamente $\theta = \operatorname{atan2}!\big(\sqrt{x^2+y^2},, z\big)$.
    
- $\phi = \operatorname{atan2}(y,x)$ (maneja correctamente los cuadrantes).
    

**Observaciones:** para $r=0$ $\theta$ y $\phi$ son indefinidos (singularidad en el origen).

---

# Ejercicio (b) — Conversión cilíndricas $\leftrightarrow$ cartesianas

**Enunciado:** Encuentra la conversión de coordenadas cilíndricas a cartesianas: $x(\rho,\phi,z)$, etc. Y las inversas $\rho(x,y,z)$, etc.

## Paso 1 — Definición geométrica

Coordenadas cilíndricas $(\rho,\phi,z)$:

- $\rho$ = distancia al eje $z$ (en el plano $xy$),
    
- $\phi$ = ángulo azimutal en el plano $xy$,
    
- $z$ = altura (misma que la coordenada $z$ cartesiana).
    

## Paso 2 — Transformación directa

Usando trigonometría en el plano $xy$:

$x = \rho\cos\phi$  
$y = \rho\sin\phi$  
$z = z$ (se conserva)

## Paso 3 — Transformación inversa

Dado $(x,y,z)$:

- $\rho = \sqrt{x^2 + y^2}$.
    
- $\phi = \operatorname{atan2}(y,x)$.
    
- $z = z$.
    

**Observación:** $\rho=0$ es el eje $z$, donde $\phi$ es indefinido.

---

# Ejercicio (c) — Partícula desde el origen moviéndose en dirección $\hat r$

**Enunciado:** Una partícula iniciando en el origen se mueve en la dirección $\hat r$ con velocidad $v_0$ y ángulos polares $\phi_0$ y $\theta_0$, tal que $\vec v = v_0 \hat r$. Expresa $\vec v$ en coordenadas cartesianas.

## Paso 1 — Expresión del vector unitario $\hat r$ en la base cartesiana

Recordemos la expresión de $\hat r$ (para ángulos $\theta,\phi$ generales):

$\hat r(\theta,\phi) = (\sin\theta\cos\phi),\hat i + (\sin\theta\sin\phi),\hat j + (\cos\theta),\hat k.$

(Se puede verificar que tiene norma 1.)

## Paso 2 — Sustituir los ángulos dados $\theta_0,\phi_0$ y escalar por $v_0$

Dado que $\vec v = v_0 \hat r(\theta_0,\phi_0)$:

$\vec v = v_0\big( \sin\theta_0\cos\phi_0,\hat i ;+; \sin\theta_0\sin\phi_0,\hat j ;+; \cos\theta_0,\hat k \big).$

## Comentario adicional (si se quiere la dependencia temporal)

Si la partícula parte del origen con velocidad constante $v_0$ en esa dirección, la trayectoria es $\vec r(t)=v_0 t,\hat r(\theta_0,\phi_0)$ y la velocidad es la constante indicada arriba.

---

# Ejercicio (d) — OPCIONAL: partícula que parte de $\vec x_0$ con la misma velocidad del (c); expresar $\vec v$ en coordenadas polares (esféricas)

**Enunciado:** Una partícula que parte de un punto $\vec x_0$ se mueve con la misma velocidad del apartado (c) (ya no en la dirección local $\hat r$). Expresa $\vec v$ en coordenadas polares. Deberías notar una gran debilidad del sistema de coordenadas polares.

> **Interpretación:** la velocidad es el mismo vector cartesiano $\vec v = v_0 \hat r(\theta_0,\phi_0)$ que en (c), pero ahora la partícula está localizada en una posición con coordenadas esféricas distintas (por ejemplo $(r_1,\theta_1,\phi_1)$). Nos piden expresar ese mismo vector en la base local esférica ${\hat r(\theta_1,\phi_1),,\hat\theta(\theta_1,\phi_1),,\hat\phi(\theta_1,\phi_1)}$ del punto inicial $\vec x_0$.

## Paso 1 — Expresiones de la base local en términos cartesianos

En un punto con ángulos $(\theta,\phi)$ (renombramos localmente los ángulos del punto $\vec x_0$ con $\theta,\phi$), los vectores unitarios son:

$\hat r(\theta,\phi) = (\sin\theta\cos\phi),\hat i + (\sin\theta\sin\phi),\hat j + (\cos\theta),\hat k.$

$\hat\theta(\theta,\phi) = (\cos\theta\cos\phi),\hat i + (\cos\theta\sin\phi),\hat j - (\sin\theta),\hat k.$

$\hat\phi(\theta,\phi) = (-\sin\phi),\hat i + (\cos\phi),\hat j + 0,\hat k.$

Estas tres direcciones forman una base ortonormal (para $0<\theta<\pi$).

## Paso 2 — Proyección del vector $\vec v$ sobre la base local

Sea $\vec v = v_0 \hat r(\theta_0,\phi_0)$ (vector dado por los ángulos $\theta_0,\phi_0$). Las componentes locales $v_r,v_\theta,v_\phi$ en el punto con ángulos $(\theta,\phi)$ se obtienen por producto escalar:

$v_r = \vec v \cdot \hat r(\theta,\phi)$  
$v_\theta = \vec v \cdot \hat\theta(\theta,\phi)$  
$v_\phi = \vec v \cdot \hat\phi(\theta,\phi)$

Sustituimos $\vec v = v_0 \hat r(\theta_0,\phi_0)$ y usamos linealidad:

$v_r = v_0,\big(\hat r(\theta_0,\phi_0)\cdot\hat r(\theta,\phi)\big)$  
$v_\theta = v_0,\big(\hat r(\theta_0,\phi_0)\cdot\hat\theta(\theta,\phi)\big)$  
$v_\phi = v_0,\big(\hat r(\theta_0,\phi_0)\cdot\hat\phi(\theta,\phi)\big)$

## Paso 3 — Calcular los productos escalares (desarrollo)

Usando las componentes explícitas de los unitarios y la identidad trigonométrica para la diferencia de ángulos en $\phi$, se obtiene:

1. Componente radial:
    

$v_r = v_0\big(\sin\theta_0\sin\theta\cos(\phi_0-\phi) + \cos\theta_0\cos\theta\big).$

(derivación: producto componente a componente y suma)

2. Componente polar (dirección $\hat\theta$):
    

$v_\theta = v_0\big(\sin\theta_0\cos\theta\cos(\phi_0-\phi) - \cos\theta_0\sin\theta\big).$

3. Componente azimutal (dirección $\hat\phi$):
    

$v_\phi = v_0\big(-\sin\theta_0\sin(\phi_0-\phi)\big).$

## Verificación rápida (consistencia)

Si el punto $\vec x_0$ tiene $(\theta,\phi)=(\theta_0,\phi_0)$, las fórmulas reducen a:

- $v_r = v_0(\sin^2\theta_0 + \cos^2\theta_0)=v_0$,
    
- $v_\theta = 0$,
    
- $v_\phi = 0$,  
    como debe ser (porque en (c) el vector fue exactamente $v_0\hat r$ en ese punto).
    

## Interpretación / debilidad del sistema polar(esférico)

- En coordenadas esféricas la **base unitaria depende de la posición**: $\hat r,\hat\theta,\hat\phi$ varían con $\theta,\phi$. Por eso un vector constante en el espacio (como $\vec v$) tendrá **componentes que dependen de la posición** donde se evalúa la base — esto complica la interpretación física de componentes locales y de derivadas temporales (aparecen términos con $\dot\theta,\dot\phi$ cuando se expresa $\vec v$ en la base local).
    
- Además existe una **singularidad en $r=0$**: los ángulos no están bien definidos y la base no es útil ahí.
    
- Para problemas con movimiento no puramente radial desde el origen, a menudo es más práctico usar componentes cartesianas porque la base es fija e ingenuamente intuitiva.
    

---

# Resumen final (fórmulas clave agrupadas)

**(a) Esféricas $\to$ cartesianas**  
$x = r\sin\theta\cos\phi$  
$y = r\sin\theta\sin\phi$  
$z = r\cos\theta$

**(a) Cartesianas $\to$ esféricas**  
$r = \sqrt{x^2+y^2+z^2}$  
$\theta = \arccos!\left(\dfrac{z}{r}\right)$  
$\phi = \operatorname{atan2}(y,x)$

**(b) Cilíndricas $\to$ cartesianas**  
$x = \rho\cos\phi$  
$y = \rho\sin\phi$  
$z = z$

**(b) Cartesianas $\to$ cilíndricas**  
$\rho = \sqrt{x^2+y^2}$  
$\phi = \operatorname{atan2}(y,x)$  
$z = z$

**(c) Velocidad en cartesianas (partícula desde el origen)**  
$\displaystyle \vec v = v_0\big( \sin\theta_0\cos\phi_0,\hat i + \sin\theta_0\sin\phi_0,\hat j + \cos\theta_0,\hat k \big)$

**(d) Componentes en la base esférica en un punto $(\theta,\phi)$ de un vector $\vec v = v_0\hat r(\theta_0,\phi_0)$**  
$\displaystyle v_r = v_0\big(\sin\theta_0\sin\theta\cos(\phi_0-\phi) + \cos\theta_0\cos\theta\big)$

$\displaystyle v_\theta = v_0\big(\sin\theta_0\cos\theta\cos(\phi_0-\phi) - \cos\theta_0\sin\theta\big)$

$\displaystyle v_\phi = v_0\big(-\sin\theta_0\sin(\phi_0-\phi)\big)$

---

Si quieres, continúo con cualquiera de estas posibles ampliaciones:

- Resolver un ejemplo numérico (elige valores para $v_0,\theta_0,\phi_0$ y $\vec x_0$) y muestro los cálculos numéricos paso a paso.
    
- Mostrar cómo cambia la expresión de la velocidad cuando la base esférica es dependiente del tiempo (por ejemplo $\vec r(t)=r(t)\hat r$ con $\hat r$ variable) y derivar las fórmulas con $\dot r,\dot\theta,\dot\phi$.
    
- Generar un archivo $\LaTeX$ con todas estas derivaciones listo para compilar, o un cuaderno Jupyter que grafique ejemplos.
    

---

**Archivo original (ruta en el sistema):**  
`/mnt/data/3fb2494b-b671-4e61-a434-8781403d1322.png`

Dime cuál de las ampliaciones quieres que haga ahora.