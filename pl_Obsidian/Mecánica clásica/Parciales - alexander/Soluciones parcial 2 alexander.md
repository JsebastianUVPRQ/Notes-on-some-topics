
Aquí tienes la solución detallada paso a paso para los problemas de Mecánica Clásica (Transformaciones Canónicas) y Mecánica Relativista (Lagrangiano).

---

### 1. Dispersión de Rutherford

Tenemos una partícula en un potencial $V(r) = -k/r$ (potencial atractivo tipo gravitatorio o coulombiano atractivo) con trayectoria dada por la ecuación de una cónica en coordenadas polares:

$$r = \frac{l^2}{mk(1 + e \cos \psi)}$$

#### (a) Demostración del ángulo de dispersión $\theta$

El ángulo de dispersión $\theta$ se define por las asíntotas de la hipérbola (la trayectoria abierta de la partícula cuando $E > 0$).

1. Condición de la asíntota ($r \to \infty$):
    
    Para que $r$ tienda a infinito, el denominador de la ecuación de la trayectoria debe tender a cero:
    
    $$1 + e \cos \psi_{\infty} = 0 \quad \Rightarrow \quad \cos \psi_{\infty} = -\frac{1}{e}$$
    
    Aquí, $\psi_{\infty}$ es el ángulo polar de la asíntota medido desde el eje de simetría (perihelio).
    
2. Relación geométrica con $\theta$:
    
    En una dispersión atractiva, la partícula "da la vuelta" alrededor del centro de fuerza. La dirección final cambia en un ángulo $\theta$. La geometría de la hipérbola dicta que el ángulo de dispersión está relacionado con el ángulo de la asíntota por:
    
    $$\theta = 2\psi_{\infty} - \pi$$
    
    Despejamos $\psi_{\infty}$:
    
    $$\psi_{\infty} = \frac{\pi}{2} + \frac{\theta}{2}$$
    
3. Relación trigonométrica:
    
    Sustituimos esto en la condición de la asíntota $\cos \psi_{\infty} = -1/e$:
    
    $$\cos\left(\frac{\pi}{2} + \frac{\theta}{2}\right) = -\frac{1}{e}$$
    
    Usando la identidad $\cos(\pi/2 + x) = -\sin(x)$:
    
    $$-\sin\left(\frac{\theta}{2}\right) = -\frac{1}{e} \quad \Rightarrow \quad \sin\left(\frac{\theta}{2}\right) = \frac{1}{e}$$
    
4. Relacionando con $E$, $l$ y $b$:
    
    Sabemos que la excentricidad $e$ para un potencial $1/r$ está dada por:
    
    $$e = \sqrt{1 + \frac{2El^2}{mk^2}}$$
    
    Además, el momento angular se relaciona con el parámetro de impacto $b$ y la velocidad inicial $v_0$ (donde $E = \frac{1}{2}mv_0^2$) como $l = m v_0 b$.
    
    Sustituimos $l^2 = m^2 v_0^2 b^2 = 2m E b^2$ en la ecuación de $e$:
    
    $$e = \sqrt{1 + \frac{2E(2mEb^2)}{mk^2}} = \sqrt{1 + \left(\frac{2Eb}{k}\right)^2}$$
    
5. Paso final:
    
    Usamos la identidad trigonométrica $\cot(\alpha) = \sqrt{\csc^2(\alpha) - 1}$. Como $\sin(\theta/2) = 1/e$, entonces $\csc(\theta/2) = e$.
    
    $$\cot\left(\frac{\theta}{2}\right) = \sqrt{e^2 - 1} = \sqrt{\left[1 + \left(\frac{2Eb}{k}\right)^2\right] - 1} = \frac{2Eb}{k}$$
    
    Invirtiendo la cotangente, obtenemos la tangente:
    
    $$\tan\left(\frac{\theta}{2}\right) = \frac{k}{2Eb}$$
    
    (Q.E.D.)
    

---

#### (b) Sección eficaz diferencial

La definición clásica de la sección eficaz diferencial por unidad de ángulo sólido $d\Omega$ es:

$$\frac{d\sigma}{d\Omega} = \frac{b}{\sin \theta} \left| \frac{db}{d\theta} \right|$$

(Nota: El enunciado pide $d\sigma/d\theta$ igual a una expresión, pero la expresión dada corresponde físicamente a $d\sigma/d\Omega$. Procederemos a calcular esta última).

1. Despejar el parámetro de impacto $b$:
    
    De la parte (a):
    
    $$b = \frac{k}{2E} \cot\left(\frac{\theta}{2}\right)$$
    
2. Derivar $b$ respecto a $\theta$:
    
    $$\frac{db}{d\theta} = \frac{k}{2E} \left( -\csc^2\left(\frac{\theta}{2}\right) \right) \cdot \frac{1}{2} = -\frac{k}{4E} \frac{1}{\sin^2(\theta/2)}$$
    
3. Sustituir en la fórmula de la sección eficaz:
    
    Tomamos el valor absoluto de la derivada:
    
    $$\frac{d\sigma}{d\Omega} = \frac{1}{\sin \theta} \left[ \frac{k}{2E} \frac{\cos(\theta/2)}{\sin(\theta/2)} \right] \left[ \frac{k}{4E} \frac{1}{\sin^2(\theta/2)} \right]$$
    
4. Simplificación trigonométrica:
    
    Usamos la identidad del ángulo doble $\sin \theta = 2 \sin(\theta/2) \cos(\theta/2)$:
    
    $$\frac{d\sigma}{d\Omega} = \frac{1}{2 \sin(\theta/2) \cos(\theta/2)} \cdot \frac{k^2}{8E^2} \frac{\cos(\theta/2)}{\sin^3(\theta/2)}$$
    
    Cancelamos $\cos(\theta/2)$:
    
    $$\frac{d\sigma}{d\Omega} = \frac{k^2}{16E^2} \frac{1}{\sin(\theta/2) \sin^3(\theta/2)} = \left(\frac{k}{4E}\right)^2 \frac{1}{\sin^4(\theta/2)}$$
    
    Esto coincide con la expresión solicitada.
    

---

### 2. Péndulos Acoplados

Tenemos dos péndulos de masa $m$ y longitud $l$, acoplados por un resorte de constante $k$. Usaremos el formalismo Lagrangiano.

1. Coordenadas y Energías:
    
    Sean $\theta_1$ y $\theta_2$ los desplazamientos angulares de cada péndulo respecto a la vertical. Para oscilaciones pequeñas ($\sin \theta \approx \theta$, $\cos \theta \approx 1 - \theta^2/2$).
    
    - Energía Cinética ($T$):
        
        $$T = \frac{1}{2}ml^2 \dot{\theta}_1^2 + \frac{1}{2}ml^2 \dot{\theta}_2^2$$
        
    - **Energía Potencial ($V$):**
        
        - Gravitacional: $V_g = mgl(1-\cos\theta_1) + mgl(1-\cos\theta_2) \approx \frac{1}{2}mgl\theta_1^2 + \frac{1}{2}mgl\theta_2^2$.
            
        - Elástica (Resorte): La deformación del resorte es aproximadamente $x = l(\theta_2 - \theta_1)$.
            
            $$V_k = \frac{1}{2}k(l(\theta_2 - \theta_1))^2 = \frac{1}{2}kl^2(\theta_1^2 - 2\theta_1\theta_2 + \theta_2^2)$$
            
    
    Lagrangiano ($L = T - V$):
    
    $$L = \frac{1}{2}ml^2(\dot{\theta}_1^2 + \dot{\theta}_2^2) - \left[ \frac{1}{2}(mgl + kl^2)\theta_1^2 + \frac{1}{2}(mgl + kl^2)\theta_2^2 - kl^2\theta_1\theta_2 \right]$$
    
2. Ecuaciones de Movimiento:
    
    Aplicamos Euler-Lagrange $\frac{d}{dt}(\frac{\partial L}{\partial \dot{\theta}_i}) + \frac{\partial V}{\partial \theta_i} = 0$:
    
    Para $\theta_1$:
    
    $$ml^2 \ddot{\theta}_1 + (mgl + kl^2)\theta_1 - kl^2 \theta_2 = 0$$
    
    Dividimos por $ml^2$ y definimos $\omega_0^2 = g/l$:
    
    $$\ddot{\theta}_1 + \left(\frac{g}{l} + \frac{k}{m}\right)\theta_1 - \frac{k}{m}\theta_2 = 0$$
    
    Para $\theta_2$ (por simetría):
    
    $$\ddot{\theta}_2 + \left(\frac{g}{l} + \frac{k}{m}\right)\theta_2 - \frac{k}{m}\theta_1 = 0$$
    
3. Búsqueda de Frecuencias Normales (Modos Normales):
    
    Proponemos soluciones de la forma $\theta_i = A_i e^{i\omega t}$. En forma matricial:
    
    $$\begin{pmatrix} \frac{g}{l} + \frac{k}{m} - \omega^2 & -\frac{k}{m} \\ -\frac{k}{m} & \frac{g}{l} + \frac{k}{m} - \omega^2 \end{pmatrix} \begin{pmatrix} A_1 \\ A_2 \end{pmatrix} = 0$$
    
    Para soluciones no triviales, el determinante debe ser cero:
    
    $$\left( \frac{g}{l} + \frac{k}{m} - \omega^2 \right)^2 - \left( \frac{k}{m} \right)^2 = 0$$
    
    Esto nos da dos soluciones para el paréntesis:
    
    $$\frac{g}{l} + \frac{k}{m} - \omega^2 = \pm \frac{k}{m}$$
    
    - Caso 1 (Signo +):
        
        $$\omega^2 = \frac{g}{l} + \frac{k}{m} - \frac{k}{m} = \frac{g}{l}$$
        
        $$\omega_1 = \sqrt{\frac{g}{l}}$$
        
        (Modo simétrico: los péndulos se mueven juntos, el resorte no trabaja).
        
    - Caso 2 (Signo -):
        
        $$\omega^2 = \frac{g}{l} + \frac{k}{m} + \frac{k}{m} = \frac{g}{l} + \frac{2k}{m}$$
        
        $$\omega_2 = \sqrt{\frac{g}{l} + \frac{2k}{m}}$$
        
        (Modo antisimétrico: los péndulos se mueven opuestos, máxima compresión/elongación del resorte).
        

**Respuesta:** Las frecuencias normales de oscilación son $\omega_1 = \sqrt{g/l}$ y $\omega_2 = \sqrt{g/l + 2k/m}$.

---

### 3. Transformaciones Canónicas y Función Generatriz

Tenemos las ecuaciones de transformación:

$$Q = \ln(1 + q^{1/2} \cos p)$$

$$P = 2(1 + q^{1/2} \cos p) \, q^{1/2} \sin p$$

#### (a) Demostración de que (Q, P) son variables canónicas

Para demostrar que la transformación es canónica, debemos comprobar que el corchete de Poisson fundamental $\{Q, P\}_{q,p}$ es igual a 1.

$$\{Q, P\} = \frac{\partial Q}{\partial q}\frac{\partial P}{\partial p} - \frac{\partial Q}{\partial p}\frac{\partial P}{\partial q}$$

Paso 1: Derivadas de $Q$

Sea $A = 1 + q^{1/2} \cos p$. Entonces $Q = \ln A$.

$$\frac{\partial Q}{\partial q} = \frac{1}{A} \left( \frac{1}{2}q^{-1/2}\cos p \right) = \frac{\cos p}{2\sqrt{q}A}$$

$$\frac{\partial Q}{\partial p} = \frac{1}{A} \left( -q^{1/2}\sin p \right) = -\frac{\sqrt{q}\sin p}{A}$$

Paso 2: Derivadas de $P$

Reescribimos $P$ para facilitar la derivación:

$$P = 2(1 + q^{1/2} \cos p) q^{1/2} \sin p = 2q^{1/2}\sin p + 2q \sin p \cos p = 2\sqrt{q}\sin p + q \sin(2p)$$

$$\frac{\partial P}{\partial q} = 2\left(\frac{1}{2}q^{-1/2}\right)\sin p + \sin(2p) = \frac{\sin p}{\sqrt{q}} + \sin(2p)$$

$$\frac{\partial P}{\partial p} = 2\sqrt{q}\cos p + 2q\cos(2p)$$

Paso 3: Calcular el Corchete de Poisson

Calculamos los productos cruzados:

1. $\frac{\partial Q}{\partial q}\frac{\partial P}{\partial p} = \frac{\cos p}{2\sqrt{q}A} (2\sqrt{q}\cos p + 2q\cos(2p)) = \frac{1}{A} (\cos^2 p + \sqrt{q}\cos p \cos(2p))$
    
2. $\frac{\partial Q}{\partial p}\frac{\partial P}{\partial q} = -\frac{\sqrt{q}\sin p}{A} (\frac{\sin p}{\sqrt{q}} + \sin(2p)) = -\frac{1}{A} (\sin^2 p + \sqrt{q}\sin p \sin(2p))$
    

Restamos (1) - (2):

$$\{Q, P\} = \frac{1}{A} \left[ (\cos^2 p + \sin^2 p) + \sqrt{q}(\cos p \cos(2p) + \sin p \sin(2p)) \right]$$

Usamos la identidad trigonométrica $\cos(x-y) = \cos x \cos y + \sin x \sin y$:

$$\{Q, P\} = \frac{1}{A} \left[ 1 + \sqrt{q} \cos(2p - p) \right] = \frac{1 + \sqrt{q}\cos p}{1 + \sqrt{q}\cos p} = 1$$

**Conclusión:** Dado que $\{Q, P\} = 1$, las variables son canónicas.

---

#### (b) Función Generatriz $F(p, Q)$

Buscamos una función generatriz que dependa del momento viejo $p$ y la coordenada nueva $Q$. Esto corresponde a una función generatriz del tipo $F_3(p, Q)$. Las relaciones estándar para esta transformación son:

$$q = -\frac{\partial F}{\partial p} \quad \text{y} \quad P = -\frac{\partial F}{\partial Q}$$

La función propuesta es:

$$F(p, Q) = -(e^Q - 1)^2 \tan p$$

Verificación para $P$:

$$P = -\frac{\partial F}{\partial Q} = - \left[ -2(e^Q - 1)e^Q \tan p \right] = 2e^Q(e^Q - 1)\tan p$$

De la definición de $Q$, sabemos que $e^Q = 1 + \sqrt{q}\cos p$, por lo que $e^Q - 1 = \sqrt{q}\cos p$. Sustituimos:

$$P = 2(1 + \sqrt{q}\cos p)(\sqrt{q}\cos p) \frac{\sin p}{\cos p} = 2(1 + \sqrt{q}\cos p)\sqrt{q}\sin p$$

Esto coincide exactamente con la ecuación de transformación dada para $P$.

Verificación para $q$:

$$q = -\frac{\partial F}{\partial p} = - \left[ -(e^Q - 1)^2 \sec^2 p \right] = (e^Q - 1)^2 \sec^2 p$$

Sustituimos nuevamente $e^Q - 1 = \sqrt{q}\cos p$:

$$q = (\sqrt{q}\cos p)^2 \frac{1}{\cos^2 p} = q \frac{\cos^2 p}{\cos^2 p} = q$$

Esto devuelve la identidad $q=q$, confirmando la consistencia.

**Conclusión:** La función $F(p, Q) = -(e^Q - 1)^2 \tan p$ genera correctamente la transformación.

---

### 4. Lagrangiano Relativista y 4-momento

El Lagrangiano es:

$$L = \frac{1}{2} m u_\mu u^\mu + \lambda \phi(x^\sigma) \left( \frac{u_\mu u^\mu}{c^2} \right)^n$$

Donde $u^\mu = \frac{dx^\mu}{d\tau}$. Nota: Físicamente $u_\mu u^\mu = c^2$, pero en el formalismo Lagrangiano tratamos $u^\mu$ como variables independientes antes de aplicar la restricción física.

#### (a) Cálculo de $n$ para que $K^\mu u_\mu = 0$

Primero, hallamos el 4-momento canónico conjugado $p_\mu$:

$$p_\mu = \frac{\partial L}{\partial u^\mu}$$

Derivamos respecto a $u^\mu$ (recordando que $\frac{\partial (u_\nu u^\nu)}{\partial u^\mu} = 2u_\mu$):

$$p_\mu = \frac{1}{2}m(2u_\mu) + \lambda \phi \cdot n \left( \frac{u^2}{c^2} \right)^{n-1} \frac{1}{c^2} (2u_\mu)$$

$$p_\mu = u_\mu \left[ m + \frac{2n\lambda \phi}{c^2} \left( \frac{u^2}{c^2} \right)^{n-1} \right]$$

Aplicamos ahora la restricción física $u^2 = u_\nu u^\nu = c^2$, lo que hace que el término entre paréntesis $(\dots)^{n-1}$ sea $1$. Definimos la "masa efectiva" $M(\phi)$:

$$p_\mu = u_\mu \underbrace{\left( m + \frac{2n\lambda \phi}{c^2} \right)}_{M(\phi)}$$

La ecuación de movimiento de Euler-Lagrange es $\frac{d p_\mu}{d\tau} = \frac{\partial L}{\partial x^\mu}$.

El lado derecho (fuerza generalizada) es:

$$\frac{\partial L}{\partial x^\mu} = \lambda (\partial_\mu \phi) \left( \frac{u^2}{c^2} \right)^n \xrightarrow{u^2=c^2} \lambda \partial_\mu \phi$$

Entonces la ecuación de movimiento es:

$$\frac{d p_\mu}{d\tau} = \lambda \partial_\mu \phi$$

La condición $K^\mu u_\mu = 0$ (ortogonalidad de la fuerza de Minkowski) es equivalente en este contexto a decir que la proyección de la variación del momento sobre la velocidad es cero o consistente con la conservación de la norma de la velocidad. Multiplicamos la ecuación de movimiento por $u^\mu$:

$$u^\mu \frac{d p_\mu}{d\tau} = u^\mu \lambda \partial_\mu \phi$$

Sabemos que $u^\mu \partial_\mu \phi = \frac{d\phi}{d\tau} = \dot{\phi}$. Por tanto:

$$ u^\mu \dot{p}_\mu = \lambda \dot{\phi} \quad (*)$$

Ahora calculamos $u^\mu \dot{p}_\mu$ directamente desde la definición de $p_\mu = M(\phi) u_\mu$:

$$\dot{p}_\mu = \dot{M} u_\mu + M \dot{u}_\mu$$

$$u^\mu \dot{p}_\mu = \dot{M} (u^\mu u_\mu) + M (u^\mu \dot{u}_\mu)$$

Como $u^\mu u_\mu = c^2$, derivando respecto a $\tau$ obtenemos $2 u^\mu \dot{u}_\mu = 0$, por lo que el segundo término se anula.

$$u^\mu \dot{p}_\mu = c^2 \dot{M}$$

Igualamos este resultado con la ecuación $(*)$:

$$c^2 \dot{M} = \lambda \dot{\phi}$$

Sustituimos $M = m + \frac{2n\lambda \phi}{c^2}$, por lo que $\dot{M} = \frac{2n\lambda \dot{\phi}}{c^2}$:

$$c^2 \left( \frac{2n\lambda \dot{\phi}}{c^2} \right) = \lambda \dot{\phi}$$

$$2n \lambda \dot{\phi} = \lambda \dot{\phi}$$

Para que esto se cumpla para cualquier $\dot{\phi}$:

$$2n = 1 \implies n = \frac{1}{2}$$

#### (b) 4-momento canónico con $n = 1/2$

Usamos la expresión derivada en el paso anterior para $p_\mu$ y sustituimos $n = 1/2$:

$$p_\mu = u_\mu \left[ m + \frac{2(1/2)\lambda \phi}{c^2} \left( \frac{u^2}{c^2} \right)^{1/2-1} \right]$$

Bajo la condición física $u_\nu u^\nu = c^2$, el término $(u^2/c^2)$ es 1. La expresión se simplifica a:

$$p^\mu = u^\mu \left( m + \frac{\lambda \phi}{c^2} \right)$$

**¿Deseas que profundice en la interpretación física de esa "masa efectiva" dependiente del campo escalar?**