# 20 Ejercicios sobre Identidades de Integrales Superficie-Volumen en Teoría Electromagnética

Los siguientes ejercicios aplican identidades integrales (Teorema de la Divergencia, Teorema de Stokes) a problemas electromagnéticos, utilizando las relaciones fundamentales entre integrales de volumen, superficie y línea. Se basan en las **identidades vectoriales** presentadas en la literatura estándar y en recursos como Wikipedia .

---
## **Parte 1: Identidades Básicas y Teoremas Fundamentales**

1.  Ley de Gauss - Carga puntual:
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

## **Parte 2: Aplicaciones a Campos Estáticos**
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
    Dos placas paralelas con cargas $+Q$ y $-Q$ están separadas una distancia $d$. Use la relación $\mathbf{F} = \oint_S \mathbf{T} \cdot d\mathbf{S}$ (tensor de Maxwell) para calcular la fuerza de atracción, donde el tensor es $T_{ij} = \epsilon_0 \left( E_i E_j - \frac{1}{2} \delta_{ij} E^2 \right)$.  
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

## **Parte 3: Campos Dinámicos y Ondas**
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
| Ejercicio | Dificultad | Teorema/Identidad Principal  | Aplicación                |
| --------- | ---------- | ---------------------------- | ------------------------- |
| 1         | Baja       | Teorema de la Divergencia    | Ley de Gauss              |
| 2         | Baja       | Teorema de Stokes            | Campos conservativos      |
| 3         | Baja       | Teorema de la Divergencia    | Monopolos magnéticos      |
| 4         | Media      | Teorema de la Divergencia    | Ley de Gauss              |
| 5         | Media      | Teorema de Stokes            | Potencial eléctrico       |
| 6         | Media      | Ley de Gauss                 | Capacitancia              |
| 7         | Alta       | Identidad energética         | Energía electrostática    |
| 8         | Alta       | Tensor de Maxwell            | Fuerzas electromagnéticas |
| 9         | Media      | Conservación de energía      | Inductancia               |
| 10        | Media      | Teorema de Stokes            | Ley de Ampère             |
| 11        | Media      | Teorema de la Divergencia    | Conservación de energía   |
| 12        | Baja       | Teorema de Stokes            | Potencial vectorial       |
| 13        | Alta       | Teorema de Stokes            | Ley de Ampère             |
| 14        | Media      | Ley de Gauss                 | Campos en cavidades       |
| 15        | Baja       | Integral de volumen          | Multipolos                |
| 16        | Media      | Ley de Faraday               | Inducción                 |
| 17        | Alta       | Teorema de la Divergencia    | Conservación de carga     |
| 18        | Alta       | Teorema de Poynting          | Radiación                 |
| 19        | Alta       | Teorema de Poynting complejo | Guías de onda             |
| 20        | Alta       | Teorema de Poynting          | Disipación                |

---

# **Clave Pedagógica**
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
Para una carga $q$ en el origen, el campo electrostático es:  
$$
\mathbf{E} = \frac{1}{4\pi\epsilon_0} \frac{q}{r^2} \hat{r}
$$

**Flujo a través de una superficie esférica de radio $ R $:**  
En la superficie esférica, $\mathbf{E}$ es radial y constante en magnitud:  
$$
\mathbf{E} = \frac{1}{4\pi\epsilon_0} \frac{q}{R^2} \hat{r}
$$  
El elemento de área en coordenadas esféricas:  
$$
d\mathbf{S} = \hat{r} \, R^2 \sin\theta \, d\theta \, d\phi
$$  
Entonces:  
$$
\mathbf{E} \cdot d\mathbf{S} = \frac{1}{4\pi\epsilon_0} \frac{q}{R^2} \cdot R^2 \sin\theta \, d\theta \, d\phi = \frac{q}{4\pi\epsilon_0} \sin\theta \, d\theta \, d\phi
$$  
Integrando:  
$$
\oint_S \mathbf{E} \cdot d\mathbf{S} = \frac{q}{4\pi\epsilon_0} \int_0^{2\pi} \int_0^\pi \sin\theta \, d\theta \, d\phi = \frac{q}{4\pi\epsilon_0} \cdot 2\pi \cdot 2 = \frac{q}{\epsilon_0}
$$

**Uso del Teorema de la Divergencia:**  
El teorema establece:  
$$
\oint_S \mathbf{E} \cdot d\mathbf{S} = \int_V \nabla \cdot \mathbf{E} \, dV
$$  
Para una carga puntual, $\rho(\mathbf{r}) = q \, \delta^3(\mathbf{r})$, y la ley de Gauss en forma diferencial es $\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0}$. Entonces:  
$$
\int_V \nabla \cdot \mathbf{E} \, dV = \int_V \frac{\rho}{\epsilon_0} \, dV = \frac{q}{\epsilon_0} \int_V \delta^3(\mathbf{r}) \, dV = \frac{q}{\epsilon_0}
$$  
ya que el volumen $V$ contiene el origen. Así, se verifica la Ley de Gauss.

---

## 2. Teorema de Stokes - Campo uniforme

**Campo magnético constante:**  
$$
\mathbf{B} = B_0 \hat{z}
$$  
Su rotacional es nulo:  
$$
\nabla \times \mathbf{B} = \mathbf{0}
$$

**Aplicación del Teorema de Stokes:**  
Para cualquier curva cerrada $C$ que limita una superficie $S$:  
$$
\oint_C \mathbf{B} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{B}) \cdot d\mathbf{S} = \int_S \mathbf{0} \cdot d\mathbf{S} = 0
$$  
Esto demuestra que la circulación de un campo uniforme es siempre cero, confirmando su naturaleza conservativa.

---

## 3. Ley de Gauss para el magnetismo

**Ley en forma diferencial:**  
Una de las ecuaciones de Maxwell establece:  
$$
\nabla \cdot \mathbf{B} = 0
$$

**Aplicación del Teorema de la Divergencia:**  
Para cualquier superficie cerrada $S$ que encierra un volumen $V$:  
$$
\oint_S \mathbf{B} \cdot d\mathbf{S} = \int_V \nabla \cdot \mathbf{B} \, dV = \int_V 0 \, dV = 0
$$  
Esto prueba que el flujo magnético neto a través de cualquier superficie cerrada es nulo, reflejando la ausencia de monopolos magnéticos.

---

## 4. Identidad de flujo eléctrico

**Ley de Gauss en forma diferencial:**  
$$
\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0}
$$

**Integración sobre un volumen $V$:**  
$$
\int_V \nabla \cdot \mathbf{E} \, dV = \int_V \frac{\rho}{\epsilon_0} \, dV
$$  
Por el Teorema de la Divergencia:  
$$
\oint_{\partial V} \mathbf{E} \cdot d\mathbf{S} = \frac{1}{\epsilon_0} \int_V \rho \, dV
$$  
La integral de $\rho$ sobre $V$ es la carga total encerrada $Q_{\text{int}}$. Así:  
$$
\oint_{\partial V} \mathbf{E} \cdot d\mathbf{S} = \frac{Q_{\text{int}}}{\epsilon_0}
$$  
Esta es la forma integral de la Ley de Gauss.

---

## 5. Circulación de campo eléctrico estático

**Campo electrostático:**  
En condiciones estáticas, el campo eléctrico no varía en el tiempo y deriva de un potencial:  
$$
\nabla \times \mathbf{E} = \mathbf{0}
$$  
ya que la ley de Faraday en estado estacionario da $\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t} = \mathbf{0}$.

**Aplicación del Teorema de Stokes:**  
Para cualquier trayectoria cerrada $C$:  
$$
\oint_C \mathbf{E} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{E}) \cdot d\mathbf{S} = 0
$$  
Esto demuestra que el campo electrostático es conservativo, permitiendo definir un potencial eléctrico $V$ tal que $\mathbf{E} = -\nabla V$.

# Aplicaciones a Campos Estáticos

## 6. Capacitancia de esfera conductora

**Campo eléctrico**: Por simetría esférica y aplicando la Ley de Gauss para $r \geq a$:
$$
\oint \mathbf{E} \cdot d\mathbf{S} = E(r) \cdot 4\pi r^2 = \frac{Q}{\epsilon_0}
$$
$$
E(r) = \frac{Q}{4\pi\epsilon_0 r^2} \quad \text{(para } r \geq a\text{)}
$$
Dentro del conductor ($r < a$), $\mathbf{E} = 0$.

**Diferencia de potencial** entre la esfera ($r = a$) e infinito:
$$
V = -\int_{\infty}^{a} \mathbf{E} \cdot d\mathbf{l} = \int_{a}^{\infty} \frac{Q}{4\pi\epsilon_0 r^2} dr = \frac{Q}{4\pi\epsilon_0} \left[-\frac{1}{r}\right]_{a}^{\infty} = \frac{Q}{4\pi\epsilon_0 a}
$$

**Capacitancia**:
$$
C = \frac{Q}{V} = 4\pi\epsilon_0 a
$$

---

## 7. Energía en campo electrostático

Partimos de la identidad vectorial:
$$
\nabla \cdot (\phi \mathbf{D}) = \phi \nabla \cdot \mathbf{D} + \mathbf{D} \cdot \nabla \phi
$$
Como $\mathbf{E} = -\nabla \phi$:
$$
\mathbf{D} \cdot \nabla \phi = -\mathbf{D} \cdot \mathbf{E}
$$
Entonces:
$$
\nabla \cdot (\phi \mathbf{D}) = \phi \nabla \cdot \mathbf{D} - \mathbf{D} \cdot \mathbf{E}
$$

Integrando sobre un volumen $V$ y aplicando el teorema de la divergencia:
$$
\oint_S \phi \mathbf{D} \cdot d\mathbf{S} = \int_V \phi \nabla \cdot \mathbf{D} \, dV - \int_V \mathbf{D} \cdot \mathbf{E} \, dV
$$
Reordenando:
$$
\int_V \mathbf{D} \cdot \mathbf{E} \, dV = \int_V \phi \nabla \cdot \mathbf{D} \, dV - \oint_S \phi \mathbf{D} \cdot d\mathbf{S}
$$

Para el vacío ($\mathbf{D} = \epsilon_0 \mathbf{E}$) y usando $\nabla \cdot \mathbf{D} = \rho$:
$$
\int_V \epsilon_0 E^2 \, dV = \int_V \phi \rho \, dV - \oint_S \phi \mathbf{D} \cdot d\mathbf{S}
$$

Tomando $V$ como todo el espacio, la integral de superficie se anula (campos que decaen suficientemente rápido):
$$
\int_{\text{todo espacio}} \epsilon_0 E^2 \, dV = \int \phi \rho \, dV
$$

La energía electrostática es:
$$
U = \frac{1}{2} \int \phi \rho \, dV = \frac{1}{2} \int_{\text{todo espacio}} \epsilon_0 E^2 \, dV
$$

---

## 8. Fuerza entre placas de capacitor

**Configuración**: Capacitor de placas paralelas con área $A$, separación $d$, cargas $+Q$ y $-Q$.

**Campo eléctrico**: Entre placas (ignorando efectos de borde):
$$
E = \frac{\sigma}{\epsilon_0} = \frac{Q}{A\epsilon_0}
$$

**Tensor de tensiones de Maxwell** (en vacío):
$$
T_{ij} = \epsilon_0 \left( E_i E_j - \frac{1}{2} \delta_{ij} E^2 \right)
$$

**Fuerza sobre la placa positiva**: Consideramos una superficie que encierra la placa. La fuerza total:
$$
\mathbf{F} = \oint_S \mathbf{T} \cdot d\mathbf{S}
$$

Elegimos una superficie cilíndrica con una tapa dentro del conductor ($\mathbf{E} = 0$) y la otra en el espacio entre placas. En la región entre placas, con normal $\hat{n}$ apuntando hacia fuera del volumen (alejándose de la placa):
$$
\mathbf{T} \cdot \hat{n} = \epsilon_0 \left[ (\mathbf{E} \cdot \hat{n}) \mathbf{E} - \frac{1}{2} E^2 \hat{n} \right] = \epsilon_0 \left( E^2 \hat{n} - \frac{1}{2} E^2 \hat{n} \right) = \frac{1}{2} \epsilon_0 E^2 \hat{n}
$$

La fuerza sobre la placa es opuesta a esta dirección (hacia la otra placa). La magnitud por unidad de área:
$$
\frac{F}{A} = \frac{1}{2} \epsilon_0 E^2
$$

**Fuerza total de atracción**:
$$
F = \frac{1}{2} \epsilon_0 E^2 A = \frac{1}{2} \epsilon_0 \left( \frac{Q}{A\epsilon_0} \right)^2 A = \frac{Q^2}{2\epsilon_0 A}
$$

---

## 9. Inductancia de un solenoide

**Campo magnético en solenoide infinito**:
$$
B = \mu_0 n I \quad \text{(uniforme en el interior)}
$$

**Flujo a través de una sección transversal** (área $A$):
$$
\Phi_B = B \cdot A = \mu_0 n I A
$$

**Flujo concatenado** para longitud $l$ ($N = n l$ vueltas):
$$
\Psi = N \Phi_B = (n l)(\mu_0 n I A) = \mu_0 n^2 I A l
$$

**Inductancia**:
$$
L = \frac{\Psi}{I} = \mu_0 n^2 A l
$$

**Energía magnética**:
$$
U_m = \frac{1}{2} L I^2 = \frac{1}{2} \mu_0 n^2 A l I^2
$$

**Densidad de energía magnética**:
$$
u_m = \frac{B^2}{2\mu_0} = \frac{(\mu_0 n I)^2}{2\mu_0} = \frac{\mu_0 n^2 I^2}{2}
$$

**Integral sobre el volumen** $V = A l$:
$$
\int_V \frac{B^2}{2\mu_0} dV = \frac{\mu_0 n^2 I^2}{2} \cdot A l = \frac{1}{2} \mu_0 n^2 A l I^2 = \frac{1}{2} L I^2
$$

Se verifica la igualdad entre la energía almacenada en la inductancia y la energía del campo magnético.


---

### 10. Campo magnético de alambre infinito (Paso de Integral a Diferencial)

**Conceptos Generales:**

1. **Ley de Ampère (Forma Integral):** $\oint_C \mathbf{B} \cdot d\mathbf{l} = \mu_0 I_{enc}$. Relaciona la circulación del campo con la corriente encerrada.
    
2. **Teorema de Stokes:** $\oint_C \mathbf{B} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{B}) \cdot d\mathbf{S}$. Convierte una integral de línea en una de superficie.
    
3. **Densidad de Corriente ($\mathbf{J}$):** La corriente es el flujo de la densidad: $I = \int_S \mathbf{J} \cdot d\mathbf{S}$.
    

**Solución Paso a Paso:**

1. **Cálculo de $\mathbf{B}$ (Ley de Ampère):**
    
    Por simetría cilíndrica, el campo $\mathbf{B}$ es constante en magnitud a una distancia $r$ y apunta en dirección acimutal ($\hat{\phi}$).
    
    $$\oint \mathbf{B} \cdot d\mathbf{l} = B(2\pi r) = \mu_0 I \implies \mathbf{B} = \frac{\mu_0 I}{2\pi r} \hat{\phi}$$
    
2. **Aplicación del Teorema de Stokes:**
    
    Tomamos la ecuación original de Ampère y aplicamos Stokes al lado izquierdo:
    
    $$\oint_C \mathbf{B} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{B}) \cdot d\mathbf{S}$$
    
3. **Expresión de la Corriente en términos de $\mathbf{J}$:**
    
    Reescribimos el lado derecho de la Ley de Ampère usando la densidad de corriente:
    
    $$\mu_0 I = \mu_0 \int_S \mathbf{J} \cdot d\mathbf{S}$$
    
4. **Igualdad de Integrandos:**
    
    Igualando los resultados de los pasos 2 y 3:
    
    $$\int_S (\nabla \times \mathbf{B}) \cdot d\mathbf{S} = \int_S (\mu_0 \mathbf{J}) \cdot d\mathbf{S}$$
    
    Para que esto sea cierto para _cualquier_ superficie $S$, los integrandos deben ser iguales punto a punto.
    

**Resultado:** $\nabla \times \mathbf{B} = \mu_0 \mathbf{J}$ (Forma diferencial de la Ley de Ampère).

---

### 11. Teorema de Poynting estático

**Conceptos Generales:**

1. **Vector de Poynting ($\mathbf{S}_{P}$):** Representa el flujo de energía direccional: $\mathbf{S}_{P} = \mathbf{E} \times \mathbf{H}$.
    
2. **Identidad Vectorial de la Divergencia:** $\nabla \cdot (\mathbf{A} \times \mathbf{B}) = \mathbf{B} \cdot (\nabla \times \mathbf{A}) - \mathbf{A} \cdot (\nabla \times \mathbf{B})$.
    
3. **Ecuaciones de Maxwell Estáticas:** En electrostática $\nabla \times \mathbf{E} = 0$. En magnetostática (sin corrientes variables), $\nabla \times \mathbf{H} = \mathbf{J}$.
    

**Solución Paso a Paso:**

1. **Aplicación del Teorema de la Divergencia:**
    
    Queremos evaluar el flujo total de energía a través de una superficie cerrada $S$:
    
    $$\oint_S (\mathbf{E} \times \mathbf{H}) \cdot d\mathbf{S} = \int_V \nabla \cdot (\mathbf{E} \times \mathbf{H}) dV$$
    
2. **Expansión del Integrando:**
    
    Usamos la identidad vectorial mencionada arriba:
    
    $$\nabla \cdot (\mathbf{E} \times \mathbf{H}) = \mathbf{H} \cdot (\nabla \times \mathbf{E}) - \mathbf{E} \cdot (\nabla \times \mathbf{H})$$
    
3. **Sustitución de Maxwell (Condiciones Estacionarias):**
    
    - Como es electrostática, el campo es conservativo: $\nabla \times \mathbf{E} = 0$.
        
    - Por tanto, el primer término se anula.
        
        $$\nabla \cdot (\mathbf{E} \times \mathbf{H}) = - \mathbf{E} \cdot (\nabla \times \mathbf{H})$$
        
4. **Análisis de la Región (Argumento Físico):**
    
    Sustituimos la Ley de Ampère $\nabla \times \mathbf{H} = \mathbf{J}$:
    
    $$\nabla \cdot (\mathbf{E} \times \mathbf{H}) = - \mathbf{E} \cdot \mathbf{J}$$
    
    - **Caso 1 (Vacío):** Si el volumen $V$ no contiene corrientes ($\mathbf{J}=0$), entonces $\nabla \cdot (\mathbf{E} \times \mathbf{H}) = 0$, y la integral es 0.
        
    - **Caso 2 (Sistema Aislado):** Si integramos sobre todo el espacio, asumimos que los campos decaen lo suficientemente rápido en el infinito, haciendo que la integral de superficie sea 0.
        
    
    El término $-\mathbf{E} \cdot \mathbf{J}$ representa el trabajo realizado por el campo sobre las cargas (Ley de Joule). En condiciones puramente estáticas donde no hay disipación o movimiento de carga (equilibrio), $\mathbf{J}=0$ o es ortogonal a $\mathbf{E}$.
    

**Resultado:** $\oint_S (\mathbf{E} \times \mathbf{H}) \cdot d\mathbf{S} = 0$ (en regiones libres de fuentes o sistemas conservativos).

---

### 12. Vector de potencial magnético (Divergencia nula)

**Conceptos Generales:**

1. **Potencial Vectorial ($\mathbf{A}$):** Se define tal que $\mathbf{B} = \nabla \times \mathbf{A}$.
    
2. **Identidad de Cálculo Vectorial:** La divergencia de un rotacional es siempre cero: $\nabla \cdot (\nabla \times \mathbf{F}) = 0$.
    
3. **Teorema de la Divergencia:** $\oint_S \mathbf{F} \cdot d\mathbf{S} = \int_V (\nabla \cdot \mathbf{F}) dV$.
    

**Solución Paso a Paso:**

1. **Planteamiento del flujo magnético:**
    
    Calculamos el flujo neto a través de una superficie cerrada $S$:
    
    $$\Phi_B = \oint_S \mathbf{B} \cdot d\mathbf{S}$$
    
2. **Conversión a Volumen:**
    
    Aplicamos el Teorema de la Divergencia:
    
    $$\oint_S \mathbf{B} \cdot d\mathbf{S} = \int_V (\nabla \cdot \mathbf{B}) dV$$
    
3. **Sustitución y Propiedad Matemática:**
    
    Sustituimos la definición $\mathbf{B} = \nabla \times \mathbf{A}$:
    
    $$\int_V (\nabla \cdot (\nabla \times \mathbf{A})) dV$$
    
    Dado que $\nabla \cdot (\nabla \times \mathbf{A}) \equiv 0$ (identidad matemática fundamental para cualquier campo vectorial diferenciable dos veces), el integrando es idénticamente cero.
    

**Resultado:** $\oint_S \mathbf{B} \cdot d\mathbf{S} = 0$ (Esto confirma la inexistencia de monopolos magnéticos).

---

### 13. Relación entre flujo y corriente (Interpretación de A)

**Conceptos Generales:**

1. **Definición de Flujo Magnético:** $\Phi = \int_S \mathbf{B} \cdot d\mathbf{S}$.
    
2. **Teorema de Stokes:** Relaciona la integral de línea de un vector con el flujo de su rotacional.
    

**Solución Paso a Paso:**

1. **Planteamiento de la Circulación de $\mathbf{A}$:**
    
    Queremos calcular $\Gamma_A = \oint_C \mathbf{A} \cdot d\mathbf{l}$ alrededor del borde del cable (curva $C$).
    
2. **Aplicación de Stokes:**
    
    $$\oint_C \mathbf{A} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{A}) \cdot d\mathbf{S}$$
    
    Aquí, $S$ es la superficie transversal del cable delimitada por el borde $C$.
    
3. **Identificación Física:**
    
    Sabemos que $\nabla \times \mathbf{A} = \mathbf{B}$.
    
    $$\int_S (\nabla \times \mathbf{A}) \cdot d\mathbf{S} = \int_S \mathbf{B} \cdot d\mathbf{S}$$
    
4. **Conclusión:**
    
    El término de la derecha $\int_S \mathbf{B} \cdot d\mathbf{S}$ es, por definición, el **Flujo Magnético ($\Phi_B$)** que atraviesa la sección del cable.
    

**Resultado:** La circulación del potencial vectorial alrededor de un bucle es igual al flujo magnético a través de ese bucle: $\oint_C \mathbf{A} \cdot d\mathbf{l} = \Phi_B$.

---

### 14. Campo en cavidad esférica (Principio de Superposición)

**Conceptos Generales:**

1. **Principio de Superposición:** Una cavidad puede modelarse matemáticamente como la suma de una esfera sólida con carga $+\rho$ y una esfera más pequeña (la cavidad) con carga $-\rho$.
    
2. **Campo de una esfera uniforme:** Dentro de una esfera uniformemente cargada, el campo es lineal con la distancia: $\mathbf{E} = \frac{\rho}{3\epsilon_0} \mathbf{r}$.
    

**Solución Paso a Paso:**

1. **Definición de Vectores:**
    
    Sea el origen el centro de la esfera grande.
    
    - Campo debido a la esfera completa ($+\rho$) en un punto $P$:
        
        $$\mathbf{E}_{total} = \frac{\rho}{3\epsilon_0} \mathbf{r}$$
        
    - Campo debido a la "esfera de hueco" ($-\rho$) centrada en el origen (dado que es concéntrica):
        
        $$\mathbf{E}_{hueco} = \frac{-\rho}{3\epsilon_0} \mathbf{r}$$
        
2. **Superposición:**
    
    El campo neto en un punto $\mathbf{r}$ dentro de la cavidad es:
    
    $$\mathbf{E}_{neto} = \mathbf{E}_{total} + \mathbf{E}_{hueco}$$
    
    $$\mathbf{E}_{neto} = \frac{\rho}{3\epsilon_0} \mathbf{r} - \frac{\rho}{3\epsilon_0} \mathbf{r} = 0$$
    
3. **Generalización (Si no fuera concéntrica):**
    
    Si la cavidad estuviera desplazada por un vector $\mathbf{a}$ (centro en $\mathbf{a}$), el campo del hueco sería $\mathbf{E}_{hueco} = \frac{-\rho}{3\epsilon_0} (\mathbf{r} - \mathbf{a})$.
    
    $$\mathbf{E}_{neto} = \frac{\rho}{3\epsilon_0} \mathbf{r} - \frac{\rho}{3\epsilon_0} (\mathbf{r} - \mathbf{a}) = \frac{\rho}{3\epsilon_0} \mathbf{a}$$
    
    Esto daría un campo constante y uniforme. Pero en tu caso específico (**concéntrica**), $\mathbf{a}=0$.
    

**Resultado:** $\mathbf{E} = 0$ dentro de una cavidad esférica concéntrica.

---

### 15. Momento dipolar eléctrico (Argumento de Simetría)

**Conceptos Generales:**

1. **Momento Dipolar ($\mathbf{p}$):** Medida de la separación de carga en un sistema. $\mathbf{p} = \int_V \mathbf{r} \rho(\mathbf{r}) dV$.
    
2. **Simetría de Paridad:** Una función es impar si $f(-x) = -f(x)$ y su integral sobre un intervalo simétrico es cero.
    

**Solución Paso a Paso:**

1. **Planteamiento de la Integral:**
    
    Asumimos el origen en el centro de la esfera. $\rho$ es constante.
    
    $$\mathbf{p} = \rho \int_{Esfera} \mathbf{r} \, dV$$
    
2. **Descomposición en Cartesianas:**
    
    Analicemos la componente $x$:
    
    $$p_x = \rho \iiint x \, dx dy dz$$
    
    La región de integración es una esfera $x^2 + y^2 + z^2 \le R^2$, que es simétrica respecto al origen ($x \to -x$).
    
3. **Argumento de Simetría:**
    
    El integrando $f(x,y,z) = x$ es una función **impar** en la variable $x$.
    
    Dado que el dominio de integración es simétrico (para cada punto positivo $x$ hay un punto correspondiente $-x$ dentro de la esfera), la integral se anula.
    
    Lo mismo aplica para $y$ y $z$.
    
    $$\int x dV = 0, \quad \int y dV = 0, \quad \int z dV = 0$$
    
4. **Conclusión Vectorial:**
    
    Como todas las componentes son cero:
    
    $$\mathbf{p} = 0$$
    

**Resultado:** Una distribución de carga esféricamente simétrica no tiene momento dipolar eléctrico (ni multipolos superiores, solo carga neta monopolar).

# Campos Dinámicos y Ondas

Aquí tienes la última serie de ejercicios sobre Campos Dinámicos, Ondas y Teoremas de Conservación. Estos problemas son fundamentales porque conectan las ecuaciones abstractas de Maxwell con cantidades físicas reales como la energía y la potencia.

---
---

## 16. Ley de Faraday - Solenoide variable

**Conceptos y Definiciones Generales:**

1. **Ley de Inducción de Faraday:** Establece que un campo magnético variable en el tiempo genera un campo eléctrico inducido (no conservativo). La "fuerza electromotriz" (FEM) inducida es igual a la tasa de cambio negativa del flujo magnético.
    
    $$\mathcal{E} = \oint_C \mathbf{E} \cdot d\mathbf{l} = -\frac{d\Phi_B}{dt}$$
    
2. **Flujo Magnético ($\Phi_B$):** Es la integral de superficie del campo magnético: $\Phi_B = \int_S \mathbf{B} \cdot d\mathbf{S}$.
    
    - _Punto Clave:_ Debes distinguir cuidadosamente entre el área del bucle de integración (radio $r$) y el área donde realmente existe el campo magnético (radio $R$).
        
3. **Simetría Cilíndrica:** Debido a que el solenoide es circular y largo, el campo eléctrico inducido $\mathbf{E}$ debe ser tangencial (en dirección $\hat{\phi}$) y constante en magnitud para una distancia radial fija $r$.
    

**Argumentos Conceptuales y Matemáticos Específicos:**

1. **Cálculo del Flujo Magnético ($\Phi_B$):**
    
    Queremos el flujo a través de un anillo de radio $r > R$.
    
    El campo $\mathbf{B}$ es no nulo solo dentro del solenoide ($0 < \rho < R$). En la región $R < \rho < r$, el campo magnético es cero. Por lo tanto, aunque la superficie de integración se extiende hasta $r$, la contribución al flujo se "corta" en $R$.
    
    $$\Phi_B = \int \mathbf{B} \cdot d\mathbf{S} = \int_{0}^{R} (B_0 \cos(\omega t) \hat{z}) \cdot (\hat{z} dA)$$
    
    El área efectiva es la sección transversal del solenoide: $A = \pi R^2$.
    
    $$\Phi_B(t) = B_0 \pi R^2 \cos(\omega t)$$
    
2. **Aplicación de la Ley de Faraday (Lado Derecho):**
    
    Derivamos el flujo respecto al tiempo:
    
    $$-\frac{d\Phi_B}{dt} = - \frac{d}{dt} \left[ B_0 \pi R^2 \cos(\omega t) \right]$$
    
    $$-\frac{d\Phi_B}{dt} = - \left[ B_0 \pi R^2 (-\omega \sin(\omega t)) \right]$$
    
    $$-\frac{d\Phi_B}{dt} = B_0 \pi R^2 \omega \sin(\omega t)$$
    
3. **Cálculo de la Circulación (Lado Izquierdo):**
    
    Evaluamos $\oint_C \mathbf{E} \cdot d\mathbf{l}$ en el camino circular de radio $r$.
    
    $$\oint_C \mathbf{E} \cdot d\mathbf{l} = \mathcal{E}_{inducida}$$
    
    _(Nota: El problema pide explícitamente calcular esta integral, que es equivalente a la FEM)_.
    
    Igualando ambos lados según la Ley de Faraday:
    
    $$\oint_C \mathbf{E} \cdot d\mathbf{l} = B_0 \pi R^2 \omega \sin(\omega t)$$
    

**Resultado:** La integral de línea del campo eléctrico (FEM inducida) es $\mathcal{E} = \pi R^2 B_0 \omega \sin(\omega t)$.

---

## 17. Ecuación de continuidad (Desde Maxwell)

**Conceptos y Definiciones Generales:**

1. **Ley de Ampère-Maxwell:** $\nabla \times \mathbf{B} = \mu_0 \mathbf{J} + \mu_0 \epsilon_0 \frac{\partial \mathbf{E}}{\partial t}$. Esta ecuación corrige la ley original de Ampère añadiendo la "corriente de desplazamiento", lo que la hace consistente con la conservación de la carga en campos variables.
    
2. **Identidad Vectorial de la Divergencia del Rotacional:** Para cualquier campo vectorial $\mathbf{A}$ bien comportado, la divergencia de su rotacional es siempre cero:
    
    $$\nabla \cdot (\nabla \times \mathbf{A}) \equiv 0$$
    
3. **Ley de Gauss:** Relaciona la divergencia del campo eléctrico con la densidad de carga: $\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0}$.
    
4. **Conmutatividad de Operadores:** Asumimos que las derivadas espaciales ($\nabla$) y temporales ($\partial/\partial t$) conmutan (Teorema de Schwarz), es decir: $\nabla \cdot \frac{\partial \mathbf{E}}{\partial t} = \frac{\partial}{\partial t} (\nabla \cdot \mathbf{E})$.
    

**Argumentos Conceptuales y Matemáticos Específicos:**

1. **Operación Inicial:**
    
    Tomamos la divergencia ($\nabla \cdot$) a ambos lados de la ecuación de Ampère-Maxwell:
    
    $$\nabla \cdot (\nabla \times \mathbf{B}) = \nabla \cdot \left( \mu_0 \mathbf{J} + \mu_0 \epsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right)$$
    
2. **Simplificación del Lado Izquierdo:**
    
    Usando la identidad vectorial (Concepto 2), el lado izquierdo se anula idénticamente:
    
    $$0 = \nabla \cdot \left( \mu_0 \mathbf{J} + \mu_0 \epsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right)$$
    
3. **Desarrollo del Lado Derecho:**
    
    Distribuimos el operador divergencia (que es lineal) y factorizamos las constantes:
    
    $$0 = \mu_0 (\nabla \cdot \mathbf{J}) + \mu_0 \epsilon_0 \left( \nabla \cdot \frac{\partial \mathbf{E}}{\partial t} \right)$$
    
    Podemos dividir toda la ecuación por $\mu_0$ (ya que $\mu_0 \neq 0$):
    
    $$0 = \nabla \cdot \mathbf{J} + \epsilon_0 \frac{\partial}{\partial t} (\nabla \cdot \mathbf{E})$$
    
4. **Sustitución con Ley de Gauss:**
    
    Sabemos por Gauss que $\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0}$. Sustituimos esto en el término temporal:
    
    $$0 = \nabla \cdot \mathbf{J} + \epsilon_0 \frac{\partial}{\partial t} \left( \frac{\rho}{\epsilon_0} \right)$$
    
5. **Resultado Final:**
    
    Las constantes $\epsilon_0$ se cancelan en el segundo término:
    
    $$\nabla \cdot \mathbf{J} + \frac{\partial \rho}{\partial t} = 0$$
    

**Resultado:** Hemos demostrado que la ecuación de continuidad (conservación local de la carga) es una consecuencia matemática directa y necesaria de las ecuaciones de Maxwell completas.

---
## 18. Teorema de Poynting en onda plana

**Conceptos Generales:**

1. **Vector de Poynting ($\mathbf{S}$):** Representa el flujo de energía direccional (potencia por unidad de área) de un campo electromagnético: $\mathbf{S} = \frac{1}{\mu_0} \mathbf{E} \times \mathbf{B}$.
    
2. **Densidad de Energía ($u$):** La energía almacenada por unidad de volumen en los campos: $u = \frac{1}{2} \epsilon_0 E^2 + \frac{1}{2\mu_0} B^2$.
    
3. **Conservación de Energía Local:** La disminución de energía dentro de un volumen debe ser igual al flujo de energía que sale a través de su superficie (si no hay disipación óhmica): $-\frac{\partial u}{\partial t} = \nabla \cdot \mathbf{S}$.
    

**Argumentos Conceptuales y Matemáticos:**

1. **Cálculo del Vector de Poynting ($\mathbf{S}$):**
    
    Dadas las ondas:
    
    $\mathbf{E} = E_0 \cos(kz - \omega t) \hat{x}$
    
    $\mathbf{B} = \frac{E_0}{c} \cos(kz - \omega t) \hat{y}$
    
    Calculamos el producto cruz $\hat{x} \times \hat{y} = \hat{z}$:
    
    $$\mathbf{S} = \frac{1}{\mu_0} \left( E_0 \cos(...) \right) \left( \frac{E_0}{c} \cos(...) \right) (\hat{x} \times \hat{y})$$
    
    $$\mathbf{S} = \frac{E_0^2}{\mu_0 c} \cos^2(kz - \omega t) \hat{z}$$
    
    Usando $c = 1/\sqrt{\epsilon_0 \mu_0}$, podemos escribir el coeficiente como $c \epsilon_0 E_0^2$.
    
2. **Cálculo de la Densidad de Energía ($u$):**
    
    $$u = \frac{1}{2} \epsilon_0 E^2 + \frac{1}{2\mu_0} B^2$$
    
    Sustituyendo $B = E/c$ y $c^2 = 1/(\mu_0 \epsilon_0)$, el término magnético se vuelve igual al eléctrico:
    
    $\frac{1}{2\mu_0} (E/c)^2 = \frac{1}{2\mu_0} E^2 (\mu_0 \epsilon_0) = \frac{1}{2} \epsilon_0 E^2$.
    
    Por lo tanto:
    
    $$u = \epsilon_0 E^2 = \epsilon_0 E_0^2 \cos^2(kz - \omega t)$$
    
3. **Verificación del Teorema en un Cubo:**
    
    Considera un cubo de lado $L$ con caras perpendiculares a los ejes.
    
    - **Lado Izquierdo (Tasa de cambio de energía):**
        
        $$-\frac{dU}{dt} = - \int_V \frac{\partial u}{\partial t} dV$$
        
        Derivada temporal de $u$: $\frac{\partial u}{\partial t} = \epsilon_0 E_0^2 (2 \cos(...))(-\sin(...))(-\omega) = \omega \epsilon_0 E_0^2 \sin(2(kz-\omega t))$.
        
    - **Lado Derecho (Flujo neto de salida):**
        
        $$\oint \mathbf{S} \cdot d\mathbf{S}$$
        
        Como $\mathbf{S}$ apunta solo en $\hat{z}$, solo contribuyen las caras en $z$ y $z+L$.
        
        $\text{Flujo} = \int_{Area} [S_z(z+L) - S_z(z)] da = L^2 [S(z+L) - S(z)]$.
        
    
    Matemáticamente, para un volumen diferencial, usamos la divergencia: $\nabla \cdot \mathbf{S} = \frac{\partial S_z}{\partial z}$.
    
    $$\frac{\partial S_z}{\partial z} = c \epsilon_0 E_0^2 (2\cos(...))(-\sin(...))(k) = -k c \epsilon_0 E_0^2 \sin(2(kz-\omega t))$$
    
    Como $\omega = ck$, los términos coinciden exactamente:
    
    $$\nabla \cdot \mathbf{S} = -\frac{\partial u}{\partial t}$$
    
    Esto demuestra que la energía que "desaparece" del cubo es exactamente la que "fluye" hacia afuera por las caras.
    

---

## 19. Impedancia de onda y Teorema de Poynting Complejo

**Conceptos Generales:**

1. **Fasores:** En régimen armónico (sinusoidal), usamos $\mathbf{E}(\mathbf{r}, t) = \text{Re}\{ \tilde{\mathbf{E}}(\mathbf{r}) e^{j\omega t} \}$.
    
2. **Vector de Poynting Complejo:** $\mathbf{S}_{comp} = \frac{1}{2} \tilde{\mathbf{E}} \times \tilde{\mathbf{H}}^*$. La parte real de su divergencia representa la potencia activa (disipada o radiada), y la parte imaginaria representa la potencia reactiva (energía oscilante almacenada).
    

**Argumentos Conceptuales y Matemáticos:**

1. **Identidad Vectorial:**
    
    Calculamos la divergencia de $\mathbf{S}_{comp}$:
    
    $$\nabla \cdot (\tilde{\mathbf{E}} \times \tilde{\mathbf{H}}^*) = \tilde{\mathbf{H}}^* \cdot (\nabla \times \tilde{\mathbf{E}}) - \tilde{\mathbf{E}} \cdot (\nabla \times \tilde{\mathbf{H}}^*)$$
    
2. **Sustitución de Maxwell (Fasores):**
    
    $\nabla \times \tilde{\mathbf{E}} = -j\omega \mu \tilde{\mathbf{H}}$
    
    $\nabla \times \tilde{\mathbf{H}} = \tilde{\mathbf{J}} + j\omega \epsilon \tilde{\mathbf{E}} \implies \nabla \times \tilde{\mathbf{H}}^* = \tilde{\mathbf{J}}^* - j\omega \epsilon^* \tilde{\mathbf{E}}^*$
    
    Sustituyendo en la identidad:
    
    $$\nabla \cdot (\tilde{\mathbf{E}} \times \tilde{\mathbf{H}}^*) = \tilde{\mathbf{H}}^* \cdot (-j\omega \mu \tilde{\mathbf{H}}) - \tilde{\mathbf{E}} \cdot (\tilde{\mathbf{J}}^* - j\omega \epsilon^* \tilde{\mathbf{E}}^*)$$
    
    $$\nabla \cdot (\tilde{\mathbf{E}} \times \tilde{\mathbf{H}}^*) = -j\omega \mu |\tilde{H}|^2 - \tilde{\mathbf{E}} \cdot \tilde{\mathbf{J}}^* + j\omega \epsilon^* |\tilde{E}|^2$$
    
3. **Relación Integral (Teorema de Poynting Complejo):**
    
    Integrando sobre el volumen y multiplicando por $1/2$:
    
    $$\oint_S \mathbf{S}_{comp} \cdot d\mathbf{S} = -\frac{1}{2} \int_V \tilde{\mathbf{E}} \cdot \tilde{\mathbf{J}}^* dV + 2j\omega \int_V \left( \frac{1}{4}\epsilon |\tilde{E}|^2 - \frac{1}{4}\mu |\tilde{H}|^2 \right) dV$$
    
4. **Interpretación Física:**
    
    - **Parte Real (Potencia Media):**
        
        $$P_{media} = \text{Re} \oint \mathbf{S}_{comp} \cdot d\mathbf{S} = -\frac{1}{2} \text{Re} \int \tilde{\mathbf{E}} \cdot \tilde{\mathbf{J}}^* dV$$
        
        Esto corresponde a las pérdidas óhmicas (calor).
        
    - **Parte Imaginaria (Potencia Reactiva):**
        
        Se relaciona con la diferencia entre la energía eléctrica media ($\bar{W}_e$) y magnética media ($\bar{W}_m$) almacenadas:
        
        $$\text{Im}(P) = 2\omega (\bar{W}_e - \bar{W}_m)$$
        

---

## 20. Pérdidas por calor en conductor óhmico

**Conceptos Generales:**

1. **Ley de Joule:** La potencia disipada por unidad de volumen es $\mathbf{J} \cdot \mathbf{E}$.
    
2. **Trabajo de Campos:** El trabajo realizado por el campo sobre las cargas es lo que se convierte en calor (energía cinética aleatorizada de los portadores de carga).
    

**Argumentos Conceptuales y Matemáticos:**

1. **Inicio desde el término de disipación:**
    
    Queremos expresar $P = \int_V \mathbf{J} \cdot \mathbf{E} dV$ en términos de campos y energía.
    
    Usamos la ley de Ampère-Maxwell para sustituir $\mathbf{J}$:
    
    $$\mathbf{J} = \nabla \times \mathbf{H} - \frac{\partial \mathbf{D}}{\partial t}$$
    
2. **Producto punto con $\mathbf{E}$:**
    
    $$\mathbf{J} \cdot \mathbf{E} = \mathbf{E} \cdot (\nabla \times \mathbf{H}) - \mathbf{E} \cdot \frac{\partial \mathbf{D}}{\partial t}$$
    
3. **Identidad Vectorial (La clave del teorema):**
    
    Sabemos que $\nabla \cdot (\mathbf{E} \times \mathbf{H}) = \mathbf{H} \cdot (\nabla \times \mathbf{E}) - \mathbf{E} \cdot (\nabla \times \mathbf{H})$.
    
    Despejamos el término que tenemos:
    
    $$\mathbf{E} \cdot (\nabla \times \mathbf{H}) = \mathbf{H} \cdot (\nabla \times \mathbf{E}) - \nabla \cdot (\mathbf{E} \times \mathbf{H})$$
    
4. **Sustitución de Faraday:**
    
    Reemplazamos $\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t}$:
    
    $$\mathbf{E} \cdot (\nabla \times \mathbf{H}) = -\mathbf{H} \cdot \frac{\partial \mathbf{B}}{\partial t} - \nabla \cdot (\mathbf{E} \times \mathbf{H})$$
    
5. **Reconstrucción de la Ecuación:**
    
    Sustituimos todo de nuevo en la ecuación del paso 2:
    
    $$\mathbf{J} \cdot \mathbf{E} = \left[ -\mathbf{H} \cdot \frac{\partial \mathbf{B}}{\partial t} - \nabla \cdot (\mathbf{E} \times \mathbf{H}) \right] - \mathbf{E} \cdot \frac{\partial \mathbf{D}}{\partial t}$$
    
    $$\mathbf{J} \cdot \mathbf{E} = -\nabla \cdot (\mathbf{E} \times \mathbf{H}) - \left( \mathbf{E} \cdot \frac{\partial \mathbf{D}}{\partial t} + \mathbf{H} \cdot \frac{\partial \mathbf{B}}{\partial t} \right)$$
    
6. **Interpretación de Energía:**
    
    El término entre paréntesis es la derivada temporal de la densidad de energía $u = \frac{1}{2}(\mathbf{E}\cdot\mathbf{D} + \mathbf{B}\cdot\mathbf{H})$.
    
    $$\mathbf{J} \cdot \mathbf{E} = -\nabla \cdot \mathbf{S} - \frac{\partial u}{\partial t}$$
    
7. **Integración de Volumen:**
    
    Integrando sobre $V$ y usando el Teorema de la Divergencia:
    
    $$\int_V \mathbf{J} \cdot \mathbf{E} dV = - \oint_S (\mathbf{E} \times \mathbf{H}) \cdot d\mathbf{S} - \frac{d}{dt} \int_V u dV$$
    
    Reordenando para que tenga sentido físico intuitivo (Trabajo hecho por campos + Flujo saliente + Tasa de cambio de energía almacenada = 0):
    
    $$\underbrace{-\oint_S \mathbf{S} \cdot d\mathbf{S}}_{\text{Energía que entra}} = \underbrace{\int_V \mathbf{J} \cdot \mathbf{E} dV}_{\text{Calor disipado}} + \underbrace{\frac{d}{dt} \int_V u dV}_{\text{Energía almacenada}}$$
    

**Resultado:** La potencia disipada por efecto Joule proviene de la disminución de la energía almacenada en el campo o del flujo de energía que entra al volumen desde el exterior.

