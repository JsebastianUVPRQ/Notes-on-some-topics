Aquí se extraen los enunciados, texto y ecuaciones del archivo **Tarea 6_taller7a99.pdf**, manteniendo su estructura original:

---

### **1. Problema de Kepler**  
En el contexto del potencial V(r)= -k/r
a) Utilizando un software de cálculo simbólico, dibuje el **potencial efectivo** para diferentes valores de la constante $ k $ y analice cualitativamente las posibles situaciones.  
b) Construya un código que integre las ecuaciones de movimiento y dibuje las trayectorias de la partícula en el plano $ x-y $ para condiciones iniciales variadas. Relacione las trayectorias con el análisis del potencial efectivo .  

---

### **2. Potenciales adicionales**  
Siga el mismo procedimiento del item 1 pero esta vez estudie el movimiento de la partícula en los siguientes potenciales:
a) $ V(r) = -\frac{k}{r^2} $: Considere condiciones iniciales a ambos lados de la órbita circular inestable y compare las trayectorias resultantes.  
b) **Potencial de Yukawa**: $ V(r) = -\frac{k}{r} e^{-r/a} $, con $ k $ y $ a $ constantes positivas.  

---

### **3. Componentes en coordenadas polares**  
a) Determine las componentes radial y azimutal del vector posición $ \vec{r} $, velocidad $ \dot{\vec{r}} $ y aceleración $ \ddot{\vec{r}} $.  
b) ¿Qué fuerza central produce las siguientes trayectorias?  
   - Espiral logarítmica: $ r = e^{a\phi} $.  
   - Espiral de Arquímedes inversa: $ r^{-1} = b\phi $, con $ a > 0 $, $ b > 0 $.  

---

### **4. Vector de Laplace-Runge-Lenz**  
Demuestre que en el problema de Kepler ($ V(r) = -\frac{k}{r} $) existe una cantidad conservada adicional:  
$$
\vec{A} = \frac{\vec{p} \times \vec{l}}{mk} - \frac{\vec{r}}{r},
$$  
donde $ \vec{p} $ es el momentum y $ \vec{l} $ el momentum angular. Encuentre la ecuación de la trayectoria a partir de esta cantidad .  

---

### **5. Corrección relativista al potencial de Kepler**  
$ V(r) = -\frac{k}{r} - \frac{\alpha}{r^3} $, con $ k = GmM $, $ \alpha = \frac{Gl^2M}{c^2m} $.  
a) Demuestre que la ecuación diferencial de la órbita es:  
$$
\frac{\partial^2 u}{\partial \theta^2} + u = \frac{1}{p} + \beta u^2, \quad p = \frac{l^2}{mk}, \quad \beta = \frac{3GM}{c^2}.
$$  
b) Calcule el ángulo de precesión del perihelio por ciclo $ \delta\theta $ mediante una solución perturbativa.  

---

### **6. Potencial $ V(r) = -\frac{k}{r^4} $**  
Encuentre la energía $ E $, el momento angular $ l $ y el período $ \tau $ de la órbita circular inestable de radio $ R $. Demuestre que otra órbita con mismos $ E $ y $ l $ tiende asintóticamente a $ R $, verificando con el programa del punto 1.  

---

### **7. Integral de órbita con corrección relativista**  
Calcule el ángulo de precesión del perihelio por ciclo $ \delta\theta $ como corrección al ángulo apsidal del problema de Kepler mediante la integral:  
$$
\delta\theta = 2 \int_{r_1}^{r_2} \frac{l/mr^2}{\sqrt{2m[E - V(r) - l^2/(2mr^2)]}} \, dr - 2\pi.
$$  

---

### **8. Distancia Sol-Júpiter**  
Dada la distancia promedio Tierra-Sol $ a_E = 1.49 \times 10^8 $ km y el período orbital de Júpiter ($ 11.86 $ años), determine la distancia promedio entre el Sol y Júpiter.  

---

### **9. Partícula bajo fuerza central**  
Una partícula de masa $ m $ se mueve bajo la fuerza $ \vec{F} = -m\gamma \frac{\hat{e}_r}{r^2} $.  
- Inicialmente está en $ C $, a distancia $ c $ del centro de fuerzas $ O $, con velocidad $ v_0 = (\gamma/c)^{1/2} $ formando un ángulo $ \alpha $ con $ OC $.  
- Encuentre las distancias apsidales y los ejes semi-mayor y semi-menor de la órbita elíptica resultante.  

---

### **10. Cometas Hyakutake y Hale-Bopp**  
Para el cometa Hyakutake ($ e = 0.999846 $, perihelio $ 0.230123 $ UA) y Hale-Bopp ($ e = 0.995075 $, perihelio $ 0.913959 $ AU):  
- Estime el tiempo hasta su próximo retorno.  
- Calcule el afelio y compárelo con el afelio de Plutón ($ 39.37 $ UA).  

---
### **3. Componentes en coordenadas polares**  
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

### **4. Vector de Laplace-Runge-Lenz**  
**Demostración de conservación:**  
Para $V(r) = -\frac{k}{r}$, el vector $\vec{A}$ se conserva. Usando las ecuaciones de movimiento y la conservación del momento angular $\vec{l}$, se muestra que $\frac{d\vec{A}}{dt} = 0$.  

**Ecuación de la trayectoria:**  
Al tomar $\vec{A} \cdot \vec{r} = \frac{l^2}{mk} - r$, se obtiene la ecuación de una cónica:  
$$
r = \frac{l^2/mk}{1 + A \cos \theta},
$$  
donde $ A $ está relacionado con la excentricidad $ e $, confirmando órbitas elípticas, parabólicas o hiperbólicas .  

---

### **5. Corrección relativista al potencial de Kepler**  
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