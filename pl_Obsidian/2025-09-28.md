# Análisis Comparativo: Cosmología FLRW vs. Agujero Negro de Schwarzschild

## 🌌 **Enfoque Cosmológico (LHS - ΛCDM)**

### **Contexto Físico**
El modelo ΛCDM describe un **universo homogéneo e isótropo** en expansión, gobernado por:

- **Materia** (bariones + materia oscura fría)
- **Energía oscura** (constante cosmológica Λ)
- **Radiación** (fotones + neutrinos)

### **Métrica FLRW**
$$
ds^2 = -dt^2 + a(t)^2 \left[ \frac{dr^2}{1-kr^2} + r^2(d\theta^2 + \sin^2\theta d\phi^2) \right]
$$

**Componentes:**
- $g_{00} = -1$
- $g_{11} = \frac{a(t)^2}{1-kr^2}$
- $g_{22} = a(t)^2 r^2$
- $g_{33} = a(t)^2 r^2 \sin^2\theta$

### **Acción y Ecuaciones de Campo**
**Acción de Einstein-Hilbert con Λ:**
$$
S = \int d^4x \sqrt{-g} \left( \frac{1}{2\kappa}R - \frac{1}{\kappa}\Lambda \right)
$$

**Ecuaciones de Einstein:**
$$
G_{\mu\nu} + \Lambda g_{\mu\nu} = \kappa T_{\mu\nu}
$$

**Tensor de Einstein perturbado:**
$$
\delta G_{\mu\nu} = \frac{\delta R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}\delta R - \frac{1}{2}h_{\mu\nu}R}{\kappa} + \Lambda h_{\mu\nu}
$$

### **Perturbaciones Cosmológicas**
El notebook implementa el **formalismo 3+1** para separar:
- **Perturbaciones escalares** (Φ, Ψ)
- **Perturbaciones vectoriales** 
- **Perturbaciones tensoriales** (ondas gravitacionales)

**Métrica perturbada:**
$$
g_{\mu\nu} = \bar{g}_{\mu\nu} + h_{\mu\nu}
$$
donde $\bar{g}_{\mu\nu}$ es el fondo FLRW y $h_{\mu\nu}$ son perturbaciones.

### **Aplicaciones**
- **Evolución de inhomogeneidades** en el universo temprano
- **Formación de estructuras** (galaxias, cúmulos)
- **Cálculo del espectro de potencias** de fluctuaciones
- **Estudio de modos normales** cosmológicos

---

## ⚫ **Enfoque de Schwarzschild**

### **Contexto Físico**
La solución de Schwarzschild describe el **campo gravitatorio externo** de un objeto esféricamente simétrico:

- **Agujero negro estático** sin carga ni rotación
- **Solución de vacío** ($T_{\mu\nu} = 0$)
- **Simetría esférica** completa

### **Métrica de Schwarzschild**
$$
ds^2 = -\left(1-\frac{2M}{r}\right)dt^2 + \left(1-\frac{2M}{r}\right)^{-1}dr^2 + r^2(d\theta^2 + \sin^2\theta d\phi^2)
$$

**Componentes:**
- $g_{00} = -\left(1-\frac{2M}{r}\right)$
- $g_{11} = \left(1-\frac{2M}{r}\right)^{-1}$
- $g_{22} = r^2$
- $g_{33} = r^2 \sin^2\theta$

### **Propiedades Geométricas**

#### **Tensor de Ricci**
$$
R_{\mu\nu} = 0
$$
**Interpretación:** Solución de vacío que satisface $R_{\mu\nu} = 0$ exactamente.

#### **Tensor de Einstein**
$$
G_{\mu\nu} = 0
$$
**Interpretación:** Satisface las ecuaciones de Einstein en vacío $G_{\mu\nu} = 0$.

#### **Escalar de Kretschmann**
$$
K = R_{\alpha\beta\gamma\delta}R^{\alpha\beta\gamma\delta} = \frac{48M^2}{r^6}
$$
**Interpretación:** 
- **Singularidad real** en $r = 0$ (divergencia)
- **Horizonte en** $r = 2M$ es una singularidad coordenada, no física

#### **Tensor de Riemann (componentes no nulas)**
$$
R^t_{rtr} = -\frac{2M}{r^3}, \quad R^t_{\theta t\theta} = \frac{M}{r}, \quad R^t_{\phi t\phi} = \frac{M\sin^2\theta}{r}
$$
$$
R^r_{\theta r\theta} = -\frac{M}{r}, \quad R^r_{\phi r\phi} = -\frac{M\sin^2\theta}{r}, \quad R^\theta_{\phi\theta\phi} = 2M\sin^2\theta
$$

### **Ecuaciones de las Geodésicas**
Para una geodésica $x^\mu(\lambda)$ con vector tangente $u^\mu = \frac{dx^\mu}{d\lambda}$:

**Ecuación temporal:**
$$
\frac{d^2t}{d\lambda^2} + \frac{2M}{r(r-2M)}\frac{dr}{d\lambda}\frac{dt}{d\lambda} = 0
$$
**Ecuación radial:**
$$c{d^2r}{d\lambda^2} + \frac{M(r-2M)}{r^3}\left(\frac{dt}{d\lambda}\right)^2 - \frac{M}{r(r-2M)}\left(\frac{dr}{d\lambda}\right)^2 - (r-2M)\left[\left(\frac{d\theta}{d\lambda}\right)^2 + \sin^2\theta\left(\frac{d\phi}{d\lambda}\right)^2\right] = 0
$$

**Ecuación angular:**
$$
\frac{d^2\theta}{d\lambda^2} + \frac{2}{r}\frac{dr}{d\lambda}\frac{d\theta}{d\lambda} - \sin\theta\cos\theta\left(\frac{d\phi}{d\lambda}\right)^2 = 0
$$

### **Cantidades Conservadas**
Debido a las simetrías:

**Energía:**
$$
E = \left(1-\frac{2M}{r}\right)\frac{dt}{d\lambda}
$$

**Momento angular:**
$$
L = r^2\sin^2\theta\frac{d\phi}{d\lambda}
$$

---

## 🔄 **Comparación Técnica**

| **Aspecto** | **FLRW (Cosmología)** | **Schwarzschild (Agujero Negro)** |
|-------------|----------------------|----------------------------------|
| **Simetría** | Homogéneo e isótropo | Esféricamente simétrico |
| **Dinámica** | Expansión cósmica $a(t)$ | Estático ($\partial_t$ es Killing) |
| **Contenido material** | Fluido perfecto + Λ | Vacío ($T_{\mu\nu} = 0$) |
| **Curvatura** | Dependiente del tiempo | Estática, diverge en $r=0$ |
| **Horizontes** | Horizonte de partículas | Horizonte de eventos en $r=2M$ |
| **Perturbaciones** | Esenciales para estructura | Estabilidad de agujero negro |
| **Singularidades** | Big Bang ($t=0$) | Central ($r=0$) |

### **Implementación en xAct**

#### **FLRW:**
- **Foliation** con `SetSlicing`
- **Perturbation theory** con expansiones en órdenes
- **Gauge choices** (longitudinal, síncrono, etc.)
- **Decomposition** 3+1 de tensores

#### **Schwarzschild:**
- **Exact solution** verification
- **Geodesic analysis** 
- **Invariant calculation** (Kretschmann)
- **Coordinate systems** (Schwarzschild, Eddington-Finkelstein, Kruskal)

### **Relevancia Física**

#### **FLRW:**
- **Cosmología observacional** (CMB, supernovas)
- **Evolución del universo**
- **Formación de estructuras**
- **Inflación cósmica**

#### **Schwarzschild:**
- **Agujeros negros astrofísicos**
- **Pruebas de relatividad general**
- **Ondas gravitacionales**
- **Física de horizonte de eventos**

Ambos enfoques demuestran la versatilidad de **xAct** para manejar desde las **grandes escalas cosmológicas** hasta los **campos gravitatorios intensos** de los agujeros negros, utilizando el mismo marco matemático de la relatividad general pero aplicado a regímenes físicos radicalmente diferentes.