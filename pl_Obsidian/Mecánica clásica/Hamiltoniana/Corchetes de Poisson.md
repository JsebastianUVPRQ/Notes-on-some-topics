![[Pasted image 20250805203056.png]]Ecuaciones canónicas como notacion simplectica

![[Pasted image 20250805203530.png]]

Ahora que ya hemos tomado nota de los puntos m´as relevantes de la teor´ıa hamiltonia-
na, vamos a considerar el punto que da pie a la teor´ıa de Hamilton-Jacobi y a desarrollos
ulteriores, las transformaciones can´onicas.
## Graficas espacio de fases
![[bcf80f47-0874-482c-872a-ae58829a6db6.png]]

---
```python
import numpy as np
import matplotlib.pyplot as plt

# Crear una figura para graficar múltiples sistemas en subplots individuales
fig, axes = plt.subplots(2, 2, figsize=(14, 10))

# ======================
# (1) Oscilador armónico
# ======================
q = np.linspace(-2, 2, 400)
p = np.sqrt(2*(1 - 0.5*q**2))  # Energía total E = 1
axes[0, 0].plot(q, p, label='Órbita de energía constante')
axes[0, 0].plot(q, -p)
axes[0, 0].set_title("Oscilador armónico (E = constante)")
axes[0, 0].set_xlabel("q (posición)")
axes[0, 0].set_ylabel("p (momento)")
axes[0, 0].grid()
axes[0, 0].legend()
axes[0, 0].axhline(0, color='black', linewidth=0.5)
axes[0, 0].axvline(0, color='black', linewidth=0.5)

# ================================
# (2) Puntos fijos: centro y silla
# ================================
# Campo vectorial: \dot{q} = p, \dot{p} = -q (oscilador armónico)
Q, P = np.meshgrid(np.linspace(-2, 2, 20), np.linspace(-2, 2, 20))
dQ = P
dP = -Q
axes[0, 1].quiver(Q, P, dQ, dP, color='blue', alpha=0.6)
axes[0, 1].set_title("Campo vectorial en el espacio de fases")
axes[0, 1].set_xlabel("q")
axes[0, 1].set_ylabel("p")
axes[0, 1].grid()
axes[0, 1].axhline(0, color='black', linewidth=0.5)
axes[0, 1].axvline(0, color='black', linewidth=0.5)

# ======================================
# (3) Sistema con punto de silla (inestable)
# ======================================
# Hamiltoniano tipo H = p^2/2 - q^2/2
q = np.linspace(-2, 2, 400)
p = np.sqrt(2*(1 + 0.5*q**2))  # E = 1 (punto de silla)
axes[1, 0].plot(q, p, label='Órbita de energía')
axes[1, 0].plot(q, -p)
axes[1, 0].set_title("Sistema con punto de silla (inestabilidad)")
axes[1, 0].set_xlabel("q")
axes[1, 0].set_ylabel("p")
axes[1, 0].grid()
axes[1, 0].legend()
axes[1, 0].axhline(0, color='black', linewidth=0.5)
axes[1, 0].axvline(0, color='black', linewidth=0.5)

# ============================
# (4) Trayectoria caótica (ejemplo simple aproximado)
# ============================
# Simulación numérica simple de péndulo no lineal
def pendulo_nolineal(q0, p0, dt=0.05, steps=1000):
    q, p = [q0], [p0]
    for _ in range(steps):
        dq = p[-1]
        dp = -np.sin(q[-1])  # Ecuación del péndulo
        q.append(q[-1] + dq * dt)
        p.append(p[-1] + dp * dt)
    return q, p

for q0, p0 in [(-2, 1.5), (1, 0), (2, -1.2)]:
    q, p = pendulo_nolineal(q0, p0)
    axes[1, 1].plot(q, p, lw=0.8)

axes[1, 1].set_title("Trayectorias complejas (péndulo no lineal)")
axes[1, 1].set_xlabel("q")
axes[1, 1].set_ylabel("p")
axes[1, 1].grid()
axes[1, 1].axhline(0, color='black', linewidth=0.5)
axes[1, 1].axvline(0, color='black', linewidth=0.5)

plt.tight_layout()
plt.show()
```
---
## Ejercicios mecanica lagrangiana y Corchetes de Poisson
* Lagrangianos  
* Hamiltonianos  
* Matrices simplécticas $J$  
* Coordenadas curvilíneas  

Este enfoque es ideal para **física universitaria avanzada**, especialmente cursos como *Mecánica Clásica*, *Dinámica Analítica*, o preparación para *física teórica/mecánica cuántica*.  

---  

## 🧩 PARTE I: LAGRANGIANOS — CLAVES PARA RESOLVER EJERCICIOS  

### 📌 Paso a paso:  

1. **Elegir coordenadas generalizadas $q_i$**  
   Adapta el sistema a su geometría:  
   * Péndulo → $\theta$  
   * Masa en plano inclinado → $s$  
   * Cuerpo rígido → ángulos de Euler  

2. **Escribir las energías**:  
   * **Energía cinética** $T = \frac{1}{2} m \dot{x}^2 + \cdots$  
   * **Energía potencial** $V$  

3. **Construir el lagrangiano**:  
   $$  
   L(q_i, \dot{q}_i, t) = T - V  
   $$  

4. **Aplicar las ecuaciones de Euler-Lagrange**:  
   $$  
   \frac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}_i} \right) - \frac{\partial L}{\partial q_i} = 0  
   $$  

---  

### ✅ EJEMPLO: Péndulo simple  

* Coordenada: $\theta$  
* $T = \frac{1}{2} m l^2 \dot{\theta}^2$  
* $V = -mgl\cos\theta$  
* $L = \frac{1}{2} m l^2 \dot{\theta}^2 + mgl\cos\theta$  

Ecuación de movimiento:  
$$  
\frac{d}{dt}(ml^2 \dot{\theta}) + mgl\sin\theta = 0 \Rightarrow \ddot{\theta} + \frac{g}{l} \sin\theta = 0  
$$  

---  

## 🧩 PARTE II: HAMILTONIANOS — CLAVES PARA TRANSFORMAR  

### 📌 Pasos para ir de Lagrangiano a Hamiltoniano:  

1. Calcular momento canónico:  
   $$  
   p_i = \frac{\partial L}{\partial \dot{q}_i}  
   $$  

2. **Invertir** para obtener $\dot{q}_i(p_i, q_i)$  

3. Hamiltoniano por transformación de Legendre:  
   $$  
   H(q_i, p_i) = \sum_i p_i \dot{q}_i - L  
   $$  

4. Usar ecuaciones de Hamilton:  
   $$  
   \dot{q}_i = \frac{\partial H}{\partial p_i}, \quad \dot{p}_i = -\frac{\partial H}{\partial q_i}  
   $$  

---  

### ✅ EJEMPLO: Oscilador armónico 1D  

* $L = \frac{1}{2} m \dot{q}^2 - \frac{1}{2} k q^2$  
* $p = m\dot{q} \Rightarrow \dot{q} = \frac{p}{m}$  

Entonces:  
$$  
H(q, p) = p \cdot \frac{p}{m} - \left( \frac{1}{2} m \cdot \frac{p^2}{m^2} - \frac{1}{2} k q^2 \right) = \frac{p^2}{2m} + \frac{1}{2} k q^2  
$$  

Ecuaciones de Hamilton:  
$$  
\dot{q} = \frac{p}{m}, \quad \dot{p} = -kq  
$$  

---  

## 🧩 PARTE III: MATRIZ SIMPLÉCTICA $J$ — ESTRUCTURA DEL ESPACIO DE FASES  

### 🔧 Definición:  

Para un sistema con $n$ grados de libertad, el espacio de fases tiene $2n$ dimensiones con coordenadas $(q_1, ..., q_n, p_1, ..., p_n)$.  

Se define la **matriz simpléctica estándar** $J$:  
$$  
J = \begin{pmatrix}  
0 & I \\  
-I & 0  
\end{pmatrix}  
$$  
donde $I$ es la matriz identidad $n \times n$.  

---  

### ✅ Aplicación: Ecuaciones de Hamilton como ecuación vectorial  

Define:  
$$  
\mathbf{z} = \begin{pmatrix} q \\ p \end{pmatrix}, \quad \dot{\mathbf{z}} = J \nabla H  
$$  
Entonces:  
$$  
\dot{z}_i = \sum_j J_{ij} \frac{\partial H}{\partial z_j}  
$$  

---  

## 🧩 PARTE IV: COORDENADAS CURVILÍNEAS — CÓMO CAMBIAR Y USARLAS  

### ⚙️ ¿Qué son?  

Coordenadas adaptadas a la geometría del problema. Ejemplos:  
* Cilíndricas: $(r, \phi, z)$  
* Esféricas: $(r, \theta, \phi)$  
* Coordenadas generalizadas: $q_i$  

---  

### 📌 Cálculo de energías:  

1. **Cinemática**: Vector de posición $\vec{r}(q_i)$  
2. Derivar para velocidad: $\dot{\vec{r}}$  
3. Energía cinética:  
   $$  
   T = \frac{1}{2} m |\dot{\vec{r}}|^2  
   $$  
4. Energía potencial según campo  

---  

### ✅ Ejemplo: Péndulo doble (coordenadas angulares)  
Posición del segundo péndulo depende de $\theta_1$ y $\theta_2$. Lagrangiano:  
$$  
L(\theta_1, \theta_2, \dot{\theta}_1, \dot{\theta}_2)  
$$
---  

## 💡 RESUMEN DE CLAVES PRÁCTICAS  

| Tema                    | Claves                                                                |     |
| ----------------------- | --------------------------------------------------------------------- | --- |
| Lagrangianos            | $L = T - V$, coordenadas adaptadas, ecuaciones de Euler-Lagrange      |     |
| Hamiltonianos           | $H = p\dot{q} - L$, momento canónico, transformación de Legendre      |     |
| Matriz $J$              | Ecuaciones vectorizadas: $\dot{\mathbf{z}} = J \nabla H$              |     |
| Coordenadas curvilíneas | $\vec{r}(q_i) \rightarrow \dot{\vec{r}} \rightarrow T = \frac{1}{2}m$ |     |

---  

## 🧠 ¿Cómo practicar?  

* **Sistemas simples**: Péndulo, resorte, partícula libre  
* Cambios de coordenadas: Cartesianas → Polares  
* Calcular: $L \rightarrow p_i \rightarrow H \rightarrow J$  
* Dibujar espacio de fases  

---  

¿Quieres **problemas resueltos paso a paso** o una plantilla para resolver automáticamente (ej. con Python/SymPy)?