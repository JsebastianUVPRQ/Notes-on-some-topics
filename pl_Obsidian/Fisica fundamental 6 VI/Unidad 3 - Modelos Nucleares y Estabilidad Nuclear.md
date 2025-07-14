
#### **Introducción: La Paradoja de la Estabilidad Nuclear**  
Los núcleos atómicos exhiben un equilibrio cuántico fascinante entre fuerzas competitivas: la interacción fuerte atractiva de corto alcance que mantiene unidos a nucleones, y la repulsión electrostática de largo alcance entre protones. Esta unidad desentraña cómo modelos teóricos divergentes explican propiedades nucleares aparentemente contradictorias. Mientras núcleos ligeros muestran estructura orbital similar a átomos, núcleos pesados se comportan como gotas líquidas. La síntesis de estos enfoques revela el origen cuántico de la estabilidad nuclear, los números mágicos y los mecanismos de desintegración.  

---

#### **1. Modelo de Potencial Medio: El Gas de Fermi Cuántico**  
**Fundamento Conceptual**:  
En este modelo, los nucleones (protones y neutrones) se tratan como fermiones independientes confinados en un potencial esférico promedio generado por la interacción nuclear colectiva. Cada nucleón ocupa estados cuánticos definidos por números cuánticos $(n, l, j, m_j)$, análogos a los orbitales atómicos, pero con profundidades de pozo de ~50 MeV.  

**Desarrollo Matemático**:  
- **Ecuación de Schrödinger radial**:  
  $$-\frac{\hbar^2}{2m}\frac{d^2 u_{nl}}{dr^2} + \left[ V(r) + \frac{\hbar^2 l(l+1)}{2m r^2} \right] u_{nl} = E_{nl} u_{nl}$$  
  donde $u_{nl}(r) = r R_{nl}(r)$ es la función de onda radial.  
- **Potencial de Woods-Saxon**:  
  $$V(r) = \frac{-V_0}{1 + \exp\left(\frac{r-R}{a}\right)} \quad \text{con} \quad R = 1.25 \, A^{1/3} \, \text{fm}, \, a \approx 0.5 \, \text{fm}$$  
  Este potencial simula la densidad nuclear constante en el interior y bordes difusos.  

**Energía de Fermi**:  
- Densidad de nucleones: $n = \frac{A}{(4/3)\pi R^3} \approx 0.16 \, \text{fm}^{-3}$  
- Energía de Fermi para nucleones:  
  $$E_F = \frac{\hbar^2}{2m} (3\pi^2 n)^{2/3} \approx 38 \, \text{MeV}$$  
  *Interpretación*: Los nucleones llenan estados hasta $E_F$, explicando la independencia de la densidad nuclear con $A$.  

**Limitaciones**:  
- No explica números mágicos (2, 8, 20, 28, ...).  
- Ignora correlaciones fuertes entre nucleones.  

---

#### **2. Modelo de la Gota Líquida: Termodinámica Nuclear**  
**Fundamento Conceptual**:  
Propuesto por Niels Bohr, este modelo considera el núcleo como un fluido incompresible donde nucleones interactúan solo con vecinos inmediatos, similar a moléculas en una gota de agua. La energía de enlace surge de términos de volumen, superficie, Coulomb, asimetría y apareamiento.  

**Fórmula de Weizsäcker-Bethe**:  
$$B(A,Z) = \underbrace{a_V A}_{\text{Volumen}} - \underbrace{a_S A^{2/3}}_{\text{Superficie}} - \underbrace{a_C \frac{Z(Z-1)}{A^{1/3}}}_{\text{Coulomb}} - \underbrace{a_A \frac{(A-2Z)^2}{A}}_{\text{Asimetría}} + \delta(A,Z)$$  

| Parámetro | Valor (MeV) | Origen Físico |  
|-----------|-------------|---------------|  
| $a_V$ | 15.85       | Energía por enlace n-n |  
| $a_S$ | 18.34       | Nucleones superficiales menos enlazados |  
| $a_C$ | 0.71        | Repulsión electrostática |  
| $a_A$ | 92.86       | Exceso de neutrones/protones |  
| $\delta$ | $\frac{\pm34}{A^{3/4}}$ | Apareamiento (+, pares; -, impares) |  

**Predicción de Estabilidad**:  
- Minimizar energía de masa $M(A,Z)c^2 = [Zm_p + (A-Z)m_n]c^2 - B(A,Z)$ respecto a $Z$:  
  $$\frac{\partial M}{\partial Z} = 0 \quad \Rightarrow \quad Z_{\text{estable}} = \frac{A}{2 + 0.015 A^{2/3}}$$  
  *Ejemplo*: Para $A=56$ (hierro), $Z \approx 26$ (valor observado).  

**Fisión Nuclear**:  
- Energía de deformación:  
  $$\Delta E = \frac{1}{2} C \beta^2 \quad \text{(elipsoide)}$$  
  donde $\beta$ es el parámetro de deformación.  
- Condición de fisión espontánea:  
  $$\left. \frac{a_C Z^2}{a_S A} \right|_{\text{crit}} > 1 \quad \Rightarrow \quad \frac{Z^2}{A} > 48$$  
  Explica por qué $^{238}\text{U}$ ($Z^2/A = 35.6$) fisiona con neutrones, pero $^{208}\text{Pb}$ ($Z^2/A = 33.2$) es estable.  

---

#### **3. Modelo de Capas: Los Números Mágicos**  
**Fundamento Conceptual**:  
Maria Goeppert-Mayer y J. Hans D. Jensen descubrieron que núcleos con protones o neutrones en números "mágicos" (2, 8, 20, 28, 50, 82, 126) son excepcionalmente estables. Esto exige un potencial central con **acoplamiento espín-órbita fuerte**.  


**Hamiltoniano Cuántico**: 
$$
\hat{H} = -\frac{\hbar ^2}{2m}\nabla^2 + V_{\text{central}(r) + V_{\text{so}}(r) \hat{L} \cdot \hat{s}}
$$
- **Potencial central**: Oscilador armónico $V(r) = \frac{1}{2} m\omega^2 r^2$ o pozo infinito.  
- **Término espín-órbita**: 
 $$V_{s}(r) = -f(r) (\hat{L} \cdot \hat{S})\quad {con} \quad f(r) >0$$  
**División de Niveles**:  
- Estados con $j = l + 1/2$ bajan en energía, $j = l - 1/2$ suben.  
- Ejemplo para capa $1~f$:  
  $$E(1f_{7/2}) < E(1f_{5/2}) \quad \text{(separación ~6 MeV)}$$  
  Esto crea el número mágico 28 (llenado de $1f_{7/2}$).  

**Estructura de Capas**:  

| Nivel | $(n,l,j)$ | Capacidad | Acumulado |  
|-------|---------------|-----------|-----------|  
| 1s    | (0,0,1/2)     | 2         | 2         |  
| 1p    | (0,1,3/2)     | 4         | 6         |  
| 1d,2s | (0,2,5/2),(1,0,1/2) | 6+2=8   | 14        |  
| 1f    | (0,3,7/2)     | 8         | 28        |  

**Evidencia Experimental**:  
- $^{48}\text{Ca}$ (20p, 28n): Energía de separación de neutrones ~9.9 MeV (máxima para Ca).  
- $^{208}\text{Pb}$ (82p, 126n): Doblemente mágico, inerte a desintegraciones.  

---

#### **4. Estados Colectivos: Vibraciones y Rotaciones**  
**Fundamento Conceptual**:  
En núcleos deformados ($A>150$), los nucleones exhiben movimientos coordinados que generan modos vibracionales y rotacionales, similares a moléculas poliatómicas.  

**Vibraciones Cuadrupolares**:  
- Deformación superficial:  
  $$R(\theta,\phi) = R_0 \left[ 1 + \sum_{\mu=-2}^{2} \alpha_{2\mu} Y_{2\mu}(\theta,\phi) \right]$$  
- Hamiltonianos de bosones:  
  $$\hat{H}_{\text{vib}} = \sum_{\mu} \hbar \omega_2 \left( \hat{a}_{2\mu}^\dagger \hat{a}_{2\mu} + \frac{1}{2} \right)$$  
  Espectro de energía: $E = \hbar \omega_2 (n + 5/2)$.  
- *Ejemplo*: $^{114}\text{Cd}$uestra serie vibracional $0$ 2^+, 4^+, \ldots$ con $\hbar\omega_2 \approx 1.2$ MeV.  

**Rotaciones en Núcleos Deformados**:  
- Momento de inercia:  
  $$\mathcal{I} = \frac{\hbar^2}{2E} J(J+1) \quad \text{(para banda rotacional)}$$  
- Regla de Alaga (razones de ramificación):  
  $$\frac{I_\gamma(J \rightarrow J-1)}{I_\gamma(J \rightarrow J)} = \frac{2(J+1)}{J}$$  
- *Ejemplo*: $^{238}\text{U}$ exhibe banda rotacional con $\mathcal{I} \approx 90 \, \hbar^2/\text{MeV}$.  

**Superdeformación**:  
- Núcleos con relación ejes 2:1 (e.g., $^{152}\text{Dy}$) muestran bandas rotacionales con momento de inercia constante hasta alta $J$.  

---

#### **5. Estabilidad Nuclear: Valle de Beta**  
**Carta de Nuclidos**:  
- **Línea de estabilidad**: Sigue $Z = A/(1.98 + 0.015A^{2/3})$.  
- **Islas de estabilidad**: Predichas en $Z=114, 120, 126$ (elementos superpesados).  

**Energía de Separación**:  
- Para neutrones:  
  $$S_n = B(A,Z) - B(A-1,Z)$$  
- Núcleos mágicos tienen $S_n$ máximas (e.g., $S_n(^{132}\text{Sn}) \approx 9.5$ MeV).  

**Límites de Estabilidad**:  
- **Línea de goteo de neutrones**: Donde $S_n = 0$.  
- **Línea de goteo de protones**: Donde $S_p = 0$.  

---

#### **Conclusión: Unificación de Modelos**  
Los modelos nucleares no son excluyentes, sino complementarios:  
- **Modelo de capas** domina cerca de números mágicos.  
- **Modelo colectivo** explica núcleos deformados lejos de capas cerradas.  
- **Gota líquida** describe tendencias globales y fisión.  

**Paradoja resuelta**: La aparente contradicción entre comportamiento individual y colectivo surge de la escala energética: interacciones residuales (~1 MeV) son pequeñas comparadas con el pozo potencial (~50 MeV), pero suficientes para inducir correlaciones colectivas.  

> "El núcleo atómico es un sistema cuántico donde la simplicidad de las partículas independientes y la complejidad de los movimientos colectivos coexisten en delicado equilibrio." — Aage Bohr  

---

**Próximo paso**: ¿Profundizar en la Unidad 4 (Inestabilidad Nuclear: Emisiones α, β, γ) o ajustar enfoque pedagógico?