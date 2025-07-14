### **6. Potencial $V(r) = -\frac{k}{r^4}$**

Para la órbita circular inestable de radio $R$:

- **Energía $E$:**  
  $$
  E = \frac{k}{R^4}
  $$

- **Momento angular $l$:**  
  $$
  l = \frac{2m \sqrt{k}}{R}
  $$

- **Período $\tau$:**  
  $$
  \tau = \pi \sqrt{\frac{m}{k}}  R^3
  $$

**Demostración de la órbita asintótica:**  
Para otra órbita con los mismos $E$ y $l$, la ecuación radial es:
$$
\dot{r}^2 = \frac{2k}{m} \left( \frac{1}{R^2} - \frac{1}{r^2} \right)^2
$$
Para $r > R$, se tiene:
$$
\dot{r} = -\sqrt{\frac{2k}{m}} \left( \frac{1}{R^2} - \frac{1}{r^2} \right)
$$
Definiendo $\delta r = r - R$ con $\delta r > 0$ pequeño, la ecuación se aproxima a:
$$
\frac{d(\delta r)}{dt} \approx -C \delta r, \quad C = \sqrt{\frac{2k}{m}} \frac{2}{R^3} > 0
$$
La solución es $\delta r \propto e^{-Ct}$, que tiende asintóticamente a 0 cuando $t \to \infty$. Por lo tanto, la órbita tiende asintóticamente a $r = R$ desde $r > R$. Esto se verifica con el programa del punto 1, que muestra la convergencia exponencial.

---

### **7. Integral de órbita con corrección relativista**

El ángulo de precesión del perihelio por ciclo se calcula con la integral dada y la corrección relativista al potencial de Kepler. Para el potencial $V(r) = -\frac{k}{r}$, la corrección relativista es $V_{\text{eff}} = -\frac{k}{r} + \frac{l^2}{2m r^2} - \frac{k l^2}{c^2 m^2 r^3}$, que corresponde a $V(r) = -\frac{k}{r} - \frac{\beta}{r^3}$ con $\beta = \frac{k l^2}{c^2 m^2}$ en la integral. La expresión resultante es:
$$
\delta\theta = 2 \int_{r_1}^{r_2} \frac{l / (m r^2)}{\sqrt{2m \left[ E + \frac{k}{r} + \frac{k l^2}{c^2 m^2 r^3} - \frac{l^2}{2m r^2} \right]}}  dr - 2\pi
$$
Tras el desarrollo y evaluación, el ángulo de precesión es:
$$
\delta\theta = \frac{6\pi G M}{c^2 a (1 - e^2)}
$$
donde $G M = \frac{k}{m}$, $a$ es el semieje mayor y $e$ la excentricidad. Esta es la corrección relativista estándar para el problema de Kepler.

---

### **8. Distancia Sol-Júpiter**

Dada la distancia promedio Tierra-Sol $a_E = 1.49 \times 10^8$ km y el período orbital de Júpiter $T_J = 11.86$ años (con el período terrestre $T_E = 1$ año), se aplica la tercera ley de Kepler:
$$
\left( \frac{T_J}{T_E} \right)^2 = \left( \frac{a_J}{a_E} \right)^3
$$
Sustituyendo:
$$
a_J = a_E \left( \frac{T_J}{T_E} \right)^{2/3} = (1.49 \times 10^8) \times (11.86)^{2/3}  \text{km}
$$
Cálculo de $(11.86)^{2/3}$:
$$
11.86^{2/3} \approx 5.20177
$$
Entonces:
$$
a_J = 1.49 \times 10^8 \times 5.20177 = 7.7506 \times 10^8  \text{km}
$$
La distancia promedio Sol-Júpiter es $7.75 \times 10^8$ km.

---

### **9. Partícula bajo fuerza central**

Fuerza central $\vec{F} = -m \gamma \frac{\hat{e}_r}{r^2}$, con condiciones iniciales en $r = c$, velocidad $v_0 = \sqrt{\gamma / c}$, ángulo $\alpha$ con $OC$.

- **Distancias apsidales (perihelio y afelio):**  
  $$
  r_{\text{min}} = c (1 - | \cos \alpha |), \quad r_{\text{max}} = c (1 + | \cos \alpha |)
  $$

- **Semieje mayor y semieje menor:**  
  $$
  a = c, \quad b = c | \sin \alpha |
  $$

**Justificación:**  
La energía y momento angular son:
$$
E = -\frac{1}{2} m \gamma / c, \quad l = m \sqrt{\gamma c} | \sin \alpha |
$$
Para órbita elíptica, $E = -\frac{m \gamma}{2a}$ implica $a$c$. El momento angular da $e = | \cos \alpha |$, luego $r_{\text{min}} = a(1 - e)$, $r_{\text{max}} = a(1 + e)$, y $b = a \sqrt{1 - e^2}$.

---

### **10. Cometas Hyakutake y Hale-Bopp**

**Para el cometa Hyakutake ($e = 0.999846$, perihelio $q = 0.230123$ UA):**  
- Semieje mayor:  
  $$
  a = \frac{q}{1 - e} = \frac{0.230123}{1 - 0.999846} = 1494.305  \text{UA}
  $$
- Período orbital (tiempo hasta próximo retorno):  
  $$
  T = a^{3/2} = (1494.305)^{3/2} \approx 57764  \text{años}
  $$
- Afelio:  
  $$
  Q = a(1 + e) = 1494.305 \times (1 + 0.999846) \approx 2988.38  \text{UA}
  $$
- Comparación con afelio de Plutón (39.37 UA): $2988.38 > 39.37$.

**Para el cometa Hale-Bopp ($e = 0.995075$, perihelio $q = 0.913959$ UA):**  
- Semieje mayor:  
  $$
  a = \frac{q}{1 - e} = \frac{0.913959}{1 - 0.995075} = 185.5753  \text{UA}
  $$
- Período orbital (tiempo hasta próximo retorno):  
  $$
  T = a^{3/2} = (185.5753)^{3/2} \approx 2528  \text{años}
  $$
- Afelio:  
  $$
  Q = a(1 + e) = 185.5753 \times (1 + 0.995075) \approx 370.24  \text{UA}
  $$
- Comparación con afelio de Plutón (39.37 UA): $370.24 > 39.37$.

--- 

**Nota:** En el problema 7, la expresión para $\delta\theta$ es la corrección relativista estándar. En los demás problemas, los cálculos son directos aplicando las leyes de Kepler y mecánica orbital.