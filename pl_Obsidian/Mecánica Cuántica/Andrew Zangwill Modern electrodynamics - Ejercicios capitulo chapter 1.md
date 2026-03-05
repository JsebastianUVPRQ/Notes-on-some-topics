### 1.5 Delta Function Identities

A test function as part of the integrand is required to prove any delta function identity. With this in mind,

(a) Prove that $\delta(ax) = \frac{1}{|a|} \delta(x), \quad a \neq 0.$

(b) Use the identity in part (a) to prove that

$$\delta[g(x)] = \sum_m \frac{1}{|g'(x_m)|} \delta(x - x_m), \quad \text{where } g(x_m) = 0 \text{ and } g'(x_m) \neq 0.$$

(c) Confirm that

$$I = \int_0^\infty dx \, \delta(\cos x) \exp(-x) = \frac{1}{2 \sinh(\pi/2)}.$$

---

### 1.6 Radial Delta Functions

(a) Show that $\delta(r)/r = -\delta'(r)$ when it appears as part of the integrand of a three-dimensional integral in spherical coordinates. Convince yourself that the test function $f(r)$ does not provide any information. Then try $f(r)/r$.

(b) Show that $\nabla \cdot [\delta(r-a)\hat{r}] = (a^2/r^2)\delta'(r-a)$ when it appears as part of the integrand of a three-dimensional integral in spherical coordinates.

---

### 1.7 A Representation of the Delta Function

Show that  
$$D(x) = \lim_{m \to \infty} \frac{\sin mx}{\pi x}$$  
is a representation of $\delta(x)$ by showing that  
$$\int_{-\infty}^{\infty} dx f(x)D(x) = f(0).$$

---

### 1.8 An Application of Stokes’ Theorem

Without using vector identities,

(a) use Stokes’ Theorem $$\int dS \cdot (\nabla \times A) = \oint ds \cdot A$$ with $A = c \times F$ where $c$ is an arbitrary constant vector to establish the equality on the left side of

$$\oint_C ds \times F = \int_S dS \{ \hat{n}_i \nabla F_i - \hat{n}(\nabla \cdot F) \} = \int_S dS (\hat{n} \times \nabla) \times F.$$

(b) confirm the equality on the right side of this expression.

(c) show that $$\oint_C r \times ds = 2 \int_S dS.$$

---

### 1.16 Densities of States

Let $E$ be a positive real number. Evaluate

(a) $$g_1(E) = \int_{-\infty}^{\infty} dk_x \, \delta(E - k_x^2).$$

(b) $$g_2(E) = \int_{-\infty}^{\infty} dk_x \int_{-\infty}^{\infty} dk_y \, \delta(E - k_x^2 - k_y^2).$$

(c) $$g_3(E) = \int_{-\infty}^{\infty} dk_x \int_{-\infty}^{\infty} dk_y \int_{-\infty}^{\infty} dk_z \, \delta(E - k_x^2 - k_y^2 - k_z^2).$$---
