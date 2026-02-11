## 20 Ejercicios sobre Identidades de Integrales Superficie-Volumen en Teoría Electromagnética

Los siguientes ejercicios aplican identidades integrales (Teorema de la Divergencia, Teorema de Stokes) a problemas electromagnéticos, utilizando las relaciones fundamentales entre integrales de volumen, superficie y línea. Se basan en las **identidades vectoriales** presentadas en la literatura estándar y en recursos como Wikipedia .

---

### **Parte 1: Identidades Básicas y Teoremas Fundamentales**
1.  **Ley de Gauss - Carga puntual:**  
    Verifique la Ley de Gauss para una carga puntual $q$ en el origen, usando una superficie esférica $S$ de radio $R$. Calcule $\oint_S \mathbf{E} \cdot d\mathbf{S}$ y relacione el resultado con $\frac{q}{\epsilon_0}$ usando el Teorema de la Divergencia .  
    *Dificultad: Baja | Aplicación: Campo electrostático*  

2.  **Teorema de Stokes - Campo uniforme:**  
    Para un campo magnético constante $\mathbf{B} = B_0 \hat{z}$, demuestre que $\oint_C \mathbf{B} \cdot d\mathbf{l} = 0$ sobre cualquier curva cerrada $C$, usando el Teorema de Stokes y la identidad $\nabla \times \mathbf{B} = \mathbf{0}$.  
    *Dificultad: Baja | Aplicación: Campos conservativos*  

3.  **Ley de Gauss para el magnetismo:**  
    Demuestre que para cualquier superficie cerrada $S$ que encierre un volumen $V$, $\oint_S \mathbf{B} \cdot d\mathbf{S} = 0$, usando el Teorema de la Divergencia y la ecuación $\nabla \cdot \mathbf{B} = 0$.  
    *Dificultad: Baja | Aplicación: Monopolos magnéticos*  

4.  **Identidad de flujo eléctrico:**  
    Dada una región $V$ con densidad volumétrica de carga $\rho$, use el Teorema de la Divergencia para probar que $\oint_{\partial V} \mathbf{E} \cdot d\mathbf{S} = \frac{Q_{\text{int}}}{\epsilon_0}$, donde $\partial V$ es la frontera de $V$.  
    *Dificultad: Media | Aplicación: Ley de Gauss*  

5.  **Circulación de campo eléctrico estático:**  
    Para un campo electrostático $\mathbf{E}$, demuestre que $\oint_C \mathbf{E} \cdot d\mathbf{l} = 0$ sobre cualquier trayectoria cerrada $C$, usando el Teorema de Stokes y la ley de Faraday en estado estacionario.  
    *Dificultad: Media | Aplicación: Potencial eléctrico*  

---

### **Parte 2: Aplicaciones a Campos Estáticos**
6.  **Capacitancia de esfera conductora:**  
    Una esfera conductora de radio $a$ tiene carga $Q$. Use la Ley de Gauss para hallar $\mathbf{E}$ y luego calcule la diferencia de potencial $V$ entre la esfera e infinito. Finalmente, encuentre la capacitancia $C = Q/V$ .  
    *Dificultad: Media | Aplicación: Capacitancia*  

7.  **Energía en campo electrostático:**  
    Demuestre que la energía almacenada en un campo eléctrico es $U = \frac{1}{2} \int_V \epsilon_0 E^2 dV$ para una distribución de carga en un volumen $V$, usando la identidad:  
   $$
    \int_V \mathbf{E} \cdot \mathbf{D}  dV = \oint_S \phi \mathbf{D} \cdot d\mathbf{S} - \int_V \phi \nabla \cdot \mathbf{D}  dV
   $$  
    y la ecuación de Poisson.  
    *Dificultad: Alta | Aplicación: Energía electrostática*  

8.  **Fuerza entre placas de capacitor:**  
    Dos placas paralelas con cargas $+Q$ y \(-Q\) están separadas una distancia $d$. Use la relación $\mathbf{F} = \oint_S \mathbf{T} \cdot d\mathbf{S}$ (tensor de Maxwell) para calcular la fuerza de atracción, donde el tensor es $T_{ij} = \epsilon_0 \left( E_i E_j - \frac{1}{2} \delta_{ij} E^2 \right)$.  
    *Dificultad: Alta | Aplicación: Fuerzas electromagnéticas*  

9.  **Inductancia de un solenoide:**  
    Para un solenoide infinito con $n$ vueltas por unidad y corriente $I$, calcule el flujo magnético $\Phi_B$ a través de una sección transversal. Luego, use $\Phi_B = LI$ para encontrar la inductancia $L$. Verifique que $\frac{1}{2} LI^2 = \int \frac{B^2}{2\mu_0} dV$ en su volumen.  
    *Dificultad: Media | Aplicación: Inductancia*  

10. **Campo magnético de alambre infinito:**  
    Un alambre recto infinito lleva corriente $I$. Use la Ley de Ampère para hallar $\mathbf{B}$ y luego aplique el Teorema de Stokes a $\oint_C \mathbf{B} \cdot d\mathbf{l} = \mu_0 I$ para mostrar que $\nabla \times \mathbf{B} = \mu_0 \mathbf{J}$.  
    *Dificultad: Media | Aplicación: Ley de Ampère*  

11. **Teorema de Poynting estático:**  
    Demuestre que en condiciones estacionarias, $\oint_S (\mathbf{E} \times \mathbf{H}) \cdot d\mathbf{S} = 0$, usando el Teorema de la Divergencia y las ecuaciones de Maxwell.  
    *Dificultad: Media | Aplicación: Conservación de energía*  

12. **Vector de potencial magnético:**  
    Para un campo magnético $\mathbf{B} = \nabla \times \mathbf{A}$, demuestre que $\oint_S \mathbf{B} \cdot d\mathbf{S} = 0$ usando el Teorema de Stokes sobre $\nabla \cdot (\nabla \times \mathbf{A}) = 0$.  
    *Dificultad: Baja | Aplicación: Potencial vectorial*  

13. **Relación entre flujo y corriente:**  
    En un cable cilíndrico de radio $R$ con densidad de corriente uniforme $\mathbf{J}$, calcule $\oint_C \mathbf{A} \cdot d\mathbf{l}$ alrededor del borde del cable y relácionelo con $\int_S \mathbf{B} \cdot d\mathbf{S}$ usando el Teorema de Stokes .  
    *Dificultad: Alta | Aplicación: Ley de Ampère*  

14. **Campo en cavidad esférica:**  
    Una esfera de radio $R$ tiene carga uniforme $\rho$. Al remover una cavidad esférica concéntrica de radio $a$, use la Ley de Gauss para hallar $\mathbf{E}$ dentro de la cavidad.  
    *Dificultad: Media | Aplicación: Campo en medios con huecos*  

15. **Momento dipolar eléctrico:**  
    Para una esfera uniformemente cargada con densidad $\rho$, demuestre que el momento dipolar es cero usando $\mathbf{p} = \int_V \mathbf{r} \rho  dV$ y argumentos de simetría.  
    *Dificultad: Baja | Aplicación: Multipolos*  

---

### **Parte 3: Campos Dinámicos y Ondas**
16. **Ley de Faraday - Solenoide variable:**  
    Un solenoide largo con radio $R$ tiene un campo magnético $\mathbf{B}(t) = B_0 \cos(\omega t) \hat{z}$. Calcule $\oint_C \mathbf{E} \cdot d\mathbf{l}$ para un anillo de radio $r > R$ usando la Ley de Faraday:  
   $$
    \oint_C \mathbf{E} \cdot d\mathbf{l} = -\frac{d}{dt} \int_S \mathbf{B} \cdot d\mathbf{S}
   $$  
    *Dificultad: Media | Aplicación: Inducción electromagnética*  

17. **Ecuación de continuidad:**  
    Partiendo de la Ley de Ampère-Maxwell $\nabla \times \mathbf{B} = \mu_0 \mathbf{J} + \mu_0 \epsilon_0 \frac{\partial \mathbf{E}}{\partial t}$, use el Teorema de la Divergencia para demostrar la ecuación de continuidad: $\nabla \cdot \mathbf{J} + \frac{\partial \rho}{\partial t} = 0$ .  
    *Dificultad: Alta | Aplicación: Conservación de carga*  

18. **Teorema de Poynting en onda plana:**  
    Para una onda plana en el vacío con $\mathbf{E} = E_0 \cos(kz - \omega t) \hat{x}$ y $\mathbf{B} = \frac{E_0}{c} \cos(kz - \omega t) \hat{y}$, calcule el vector de Poynting $\mathbf{S} = \frac{1}{\mu_0} \mathbf{E} \times \mathbf{B}$. Demuestre que $\oint_{\partial V} \mathbf{S} \cdot d\mathbf{S} = -\frac{dU}{dt}$ en un volumen cúbico.  
    *Dificultad: Alta | Aplicación: Radiación electromagnética*  

19. **Impedancia de onda:**  
    En una guía de ondas, la potencia media se calcula como $P = \frac{1}{2} \int_S \text{Re}(\mathbf{E} \times \mathbf{H}^*) \cdot d\mathbf{S}$Relacione esta integral con la densidad de energía media usando el Teorema de Poynting complejo.  
    *Dificultad: Alta | Aplicación: Guías de onda*  

20. **Pérdidas por calor en conductor óhmico:**  
    En un material con conductividad $igma$, demuestre que la potencia disipada es $P = \int_V \mathbf{J} \cdot \mathbf{E}  dV$. Use el Teorema de Poynting para escribir esto como $\oint_S (\mathbf{E} \times \mathbf{H}) \cdot d\mathbf{S} + \frac{d}{dt} \int_V u  dV$, donde $u$ es la densidad de energía .  
    *Dificultad: Alta | Aplicación: Disipación de energía*  

---

### **Tabla Resumen de Ejercicios**
| Ejercicio | Dificultad | Teorema/Identidad Principal         | Aplicación                     |
|-----------|------------|-------------------------------------|--------------------------------|
| 1         | Baja       | Teorema de la Divergencia           | Ley de Gauss                   |
| 2         | Baja       | Teorema de Stokes                   | Campos conservativos           |
| 3         | Baja       | Teorema de la Divergencia           | Monopolos magnéticos           |
| 4         | Media      | Teorema de la Divergencia           | Ley de Gauss                   |
| 5         | Media      | Teorema de Stokes                   | Potencial eléctrico            |
| 6         | Media      | Ley de Gauss                        | Capacitancia                   |
| 7         | Alta       | Identidad energética                | Energía electrostática         |
| 8         | Alta       | Tensor de Maxwell                   | Fuerzas electromagnéticas      |
| 9         | Media      | Conservación de energía             | Inductancia                    |
| 10        | Media      | Teorema de Stokes                   | Ley de Ampère                  |
| 11        | Media      | Teorema de la Divergencia           | Conservación de energía        |
| 12        | Baja       | Teorema de Stokes                   | Potencial vectorial            |
| 13        | Alta       | Teorema de Stokes                   | Ley de Ampère                  |
| 14        | Media      | Ley de Gauss                        | Campos en cavidades            |
| 15        | Baja       | Integral de volumen                 | Multipolos                     |
| 16        | Media      | Ley de Faraday                      | Inducción                      |
| 17        | Alta       | Teorema de la Divergencia           | Conservación de carga          |
| 18        | Alta       | Teorema de Poynting                 | Radiación                      |
| 19        | Alta       | Teorema de Poynting complejo        | Guías de onda                  |
| 20        | Alta       | Teorema de Poynting                 | Disipación                     |

---

### **Clave Pedagógica**
- **Teorema de la Divergencia (Gauss):**  
  Relaciona integrales de volumen con flujo superficial:  
 $$  \int_V \nabla \cdot \mathbf{F}  dV = \oint_S \mathbf{F} \cdot d\mathbf{S}
 $$ 
  Usado en Ley de Gauss, conservación de carga, y energía .  

- **Teorema de Stokes:**  
  Relaciona circulación con flujo del rotacional:  
 $$
  \oint_C \mathbf{F} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{F}) \cdot d\mathbf{S}
 $$  
  Fundamental para Ley de Faraday y Ampère .  

- **Teorema de Poynting:**  
  Describe conservación de energía electromagnética:  
 $$
  \oint_S \mathbf{S} \cdot d\mathbf{S} = -\frac{dU}{dt} - P_{\text{dis}}
 $$  
  Aplicado en radiación, disipación y guías de onda .  

Estos ejercicios integran identidades de superficie-volumen con leyes físicas, consolidando la comprensión matemática y física del electromagnetismo. Para más detalles, consulte las fuentes citadas.

# Solución 20 ejercicios electrodinámica

## 1. Ley de Gauss - Carga puntual

**Campo eléctrico de una carga puntual:**  
Para una carga \( q \) en el origen, el campo electrostático es:  
\[
\mathbf{E} = \frac{1}{4\pi\epsilon_0} \frac{q}{r^2} \hat{r}
\]

**Flujo a través de una superficie esférica de radio \( R \):**  
En la superficie esférica, \( \mathbf{E} \) es radial y constante en magnitud:  
\[
\mathbf{E} = \frac{1}{4\pi\epsilon_0} \frac{q}{R^2} \hat{r}
\]  
El elemento de área en coordenadas esféricas:  
\[
d\mathbf{S} = \hat{r} \, R^2 \sin\theta \, d\theta \, d\phi
\]  
Entonces:  
\[
\mathbf{E} \cdot d\mathbf{S} = \frac{1}{4\pi\epsilon_0} \frac{q}{R^2} \cdot R^2 \sin\theta \, d\theta \, d\phi = \frac{q}{4\pi\epsilon_0} \sin\theta \, d\theta \, d\phi
\]  
Integrando:  
\[
\oint_S \mathbf{E} \cdot d\mathbf{S} = \frac{q}{4\pi\epsilon_0} \int_0^{2\pi} \int_0^\pi \sin\theta \, d\theta \, d\phi = \frac{q}{4\pi\epsilon_0} \cdot 2\pi \cdot 2 = \frac{q}{\epsilon_0}
\]

**Uso del Teorema de la Divergencia:**  
El teorema establece:  
\[
\oint_S \mathbf{E} \cdot d\mathbf{S} = \int_V \nabla \cdot \mathbf{E} \, dV
\]  
Para una carga puntual, \( \rho(\mathbf{r}) = q \, \delta^3(\mathbf{r}) \), y la ley de Gauss en forma diferencial es \( \nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0} \). Entonces:  
\[
\int_V \nabla \cdot \mathbf{E} \, dV = \int_V \frac{\rho}{\epsilon_0} \, dV = \frac{q}{\epsilon_0} \int_V \delta^3(\mathbf{r}) \, dV = \frac{q}{\epsilon_0}
\]  
ya que el volumen \( V \) contiene el origen. Así, se verifica la Ley de Gauss.

---

## 2. Teorema de Stokes - Campo uniforme

**Campo magnético constante:**  
\[
\mathbf{B} = B_0 \hat{z}
\]  
Su rotacional es nulo:  
\[
\nabla \times \mathbf{B} = \mathbf{0}
\]

**Aplicación del Teorema de Stokes:**  
Para cualquier curva cerrada \( C \) que limita una superficie \( S \):  
\[
\oint_C \mathbf{B} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{B}) \cdot d\mathbf{S} = \int_S \mathbf{0} \cdot d\mathbf{S} = 0
\]  
Esto demuestra que la circulación de un campo uniforme es siempre cero, confirmando su naturaleza conservativa.

---

## 3. Ley de Gauss para el magnetismo

**Ley en forma diferencial:**  
Una de las ecuaciones de Maxwell establece:  
\[
\nabla \cdot \mathbf{B} = 0
\]

**Aplicación del Teorema de la Divergencia:**  
Para cualquier superficie cerrada \( S \) que encierra un volumen \( V \):  
\[
\oint_S \mathbf{B} \cdot d\mathbf{S} = \int_V \nabla \cdot \mathbf{B} \, dV = \int_V 0 \, dV = 0
\]  
Esto prueba que el flujo magnético neto a través de cualquier superficie cerrada es nulo, reflejando la ausencia de monopolos magnéticos.

---

## 4. Identidad de flujo eléctrico

**Ley de Gauss en forma diferencial:**  
\[
\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0}
\]

**Integración sobre un volumen \( V \):**  
\[
\int_V \nabla \cdot \mathbf{E} \, dV = \int_V \frac{\rho}{\epsilon_0} \, dV
\]  
Por el Teorema de la Divergencia:  
\[
\oint_{\partial V} \mathbf{E} \cdot d\mathbf{S} = \frac{1}{\epsilon_0} \int_V \rho \, dV
\]  
La integral de \( \rho \) sobre \( V \) es la carga total encerrada \( Q_{\text{int}} \). Así:  
\[
\oint_{\partial V} \mathbf{E} \cdot d\mathbf{S} = \frac{Q_{\text{int}}}{\epsilon_0}
\]  
Esta es la forma integral de la Ley de Gauss.

---

## 5. Circulación de campo eléctrico estático

**Campo electrostático:**  
En condiciones estáticas, el campo eléctrico no varía en el tiempo y deriva de un potencial:  
\[
\nabla \times \mathbf{E} = \mathbf{0}
\]  
ya que la ley de Faraday en estado estacionario da \( \nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t} = \mathbf{0} \).

**Aplicación del Teorema de Stokes:**  
Para cualquier trayectoria cerrada \( C \):  
\[
\oint_C \mathbf{E} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{E}) \cdot d\mathbf{S} = 0
\]  
Esto demuestra que el campo electrostático es conservativo, permitiendo definir un potencial eléctrico \( V \) tal que \( \mathbf{E} = -\nabla V \).

# Aplicaciones a Campos Estáticos

## 6. Capacitancia de esfera conductora

**Campo eléctrico**: Por simetría esférica y aplicando la Ley de Gauss para \(r \geq a\):
\[
\oint \mathbf{E} \cdot d\mathbf{S} = E(r) \cdot 4\pi r^2 = \frac{Q}{\epsilon_0}
\]
\[
E(r) = \frac{Q}{4\pi\epsilon_0 r^2} \quad \text{(para } r \geq a\text{)}
\]
Dentro del conductor (\(r < a\)), \(\mathbf{E} = 0\).

**Diferencia de potencial** entre la esfera (\(r = a\)) e infinito:
\[
V = -\int_{\infty}^{a} \mathbf{E} \cdot d\mathbf{l} = \int_{a}^{\infty} \frac{Q}{4\pi\epsilon_0 r^2} dr = \frac{Q}{4\pi\epsilon_0} \left[-\frac{1}{r}\right]_{a}^{\infty} = \frac{Q}{4\pi\epsilon_0 a}
\]

**Capacitancia**:
\[
C = \frac{Q}{V} = 4\pi\epsilon_0 a
\]

---

## 7. Energía en campo electrostático

Partimos de la identidad vectorial:
\[
\nabla \cdot (\phi \mathbf{D}) = \phi \nabla \cdot \mathbf{D} + \mathbf{D} \cdot \nabla \phi
\]
Como \(\mathbf{E} = -\nabla \phi\):
\[
\mathbf{D} \cdot \nabla \phi = -\mathbf{D} \cdot \mathbf{E}
\]
Entonces:
\[
\nabla \cdot (\phi \mathbf{D}) = \phi \nabla \cdot \mathbf{D} - \mathbf{D} \cdot \mathbf{E}
\]

Integrando sobre un volumen \(V\) y aplicando el teorema de la divergencia:
\[
\oint_S \phi \mathbf{D} \cdot d\mathbf{S} = \int_V \phi \nabla \cdot \mathbf{D} \, dV - \int_V \mathbf{D} \cdot \mathbf{E} \, dV
\]
Reordenando:
\[
\int_V \mathbf{D} \cdot \mathbf{E} \, dV = \int_V \phi \nabla \cdot \mathbf{D} \, dV - \oint_S \phi \mathbf{D} \cdot d\mathbf{S}
\]

Para el vacío (\(\mathbf{D} = \epsilon_0 \mathbf{E}\)) y usando \(\nabla \cdot \mathbf{D} = \rho\):
\[
\int_V \epsilon_0 E^2 \, dV = \int_V \phi \rho \, dV - \oint_S \phi \mathbf{D} \cdot d\mathbf{S}
\]

Tomando \(V\) como todo el espacio, la integral de superficie se anula (campos que decaen suficientemente rápido):
\[
\int_{\text{todo espacio}} \epsilon_0 E^2 \, dV = \int \phi \rho \, dV
\]

La energía electrostática es:
\[
U = \frac{1}{2} \int \phi \rho \, dV = \frac{1}{2} \int_{\text{todo espacio}} \epsilon_0 E^2 \, dV
\]

---

## 8. Fuerza entre placas de capacitor

**Configuración**: Capacitor de placas paralelas con área \(A\), separación \(d\), cargas \(+Q\) y \(-Q\).

**Campo eléctrico**: Entre placas (ignorando efectos de borde):
\[
E = \frac{\sigma}{\epsilon_0} = \frac{Q}{A\epsilon_0}
\]

**Tensor de tensiones de Maxwell** (en vacío):
\[
T_{ij} = \epsilon_0 \left( E_i E_j - \frac{1}{2} \delta_{ij} E^2 \right)
\]

**Fuerza sobre la placa positiva**: Consideramos una superficie que encierra la placa. La fuerza total:
\[
\mathbf{F} = \oint_S \mathbf{T} \cdot d\mathbf{S}
\]

Elegimos una superficie cilíndrica con una tapa dentro del conductor (\(\mathbf{E} = 0\)) y la otra en el espacio entre placas. En la región entre placas, con normal \(\hat{n}\) apuntando hacia fuera del volumen (alejándose de la placa):
\[
\mathbf{T} \cdot \hat{n} = \epsilon_0 \left[ (\mathbf{E} \cdot \hat{n}) \mathbf{E} - \frac{1}{2} E^2 \hat{n} \right] = \epsilon_0 \left( E^2 \hat{n} - \frac{1}{2} E^2 \hat{n} \right) = \frac{1}{2} \epsilon_0 E^2 \hat{n}
\]

La fuerza sobre la placa es opuesta a esta dirección (hacia la otra placa). La magnitud por unidad de área:
\[
\frac{F}{A} = \frac{1}{2} \epsilon_0 E^2
\]

**Fuerza total de atracción**:
\[
F = \frac{1}{2} \epsilon_0 E^2 A = \frac{1}{2} \epsilon_0 \left( \frac{Q}{A\epsilon_0} \right)^2 A = \frac{Q^2}{2\epsilon_0 A}
\]

---

## 9. Inductancia de un solenoide

**Campo magnético en solenoide infinito**:
\[
B = \mu_0 n I \quad \text{(uniforme en el interior)}
\]

**Flujo a través de una sección transversal** (área \(A\)):
\[
\Phi_B = B \cdot A = \mu_0 n I A
\]

**Flujo concatenado** para longitud \(l\) (\(N = n l\) vueltas):
\[
\Psi = N \Phi_B = (n l)(\mu_0 n I A) = \mu_0 n^2 I A l
\]

**Inductancia**:
\[
L = \frac{\Psi}{I} = \mu_0 n^2 A l
\]

**Energía magnética**:
\[
U_m = \frac{1}{2} L I^2 = \frac{1}{2} \mu_0 n^2 A l I^2
\]

**Densidad de energía magnética**:
\[
u_m = \frac{B^2}{2\mu_0} = \frac{(\mu_0 n I)^2}{2\mu_0} = \frac{\mu_0 n^2 I^2}{2}
\]

**Integral sobre el volumen** \(V = A l\):
\[
\int_V \frac{B^2}{2\mu_0} dV = \frac{\mu_0 n^2 I^2}{2} \cdot A l = \frac{1}{2} \mu_0 n^2 A l I^2 = \frac{1}{2} L I^2
\]

Se verifica la igualdad entre la energía almacenada en la inductancia y la energía del campo magnético.