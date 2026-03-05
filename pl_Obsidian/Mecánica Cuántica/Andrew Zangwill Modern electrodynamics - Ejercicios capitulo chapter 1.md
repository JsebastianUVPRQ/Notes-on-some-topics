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

(c) $$g_3(E) = \int_{-\infty}^{\infty} dk_x \int_{-\infty}^{\infty} dk_y \int_{-\infty}^{\infty} dk_z \, \delta(E - k_x^2 - k_y^2 - k_z^2).$$

---

# Solución
Here are the step-by-step proofs and evaluations for these Dirac delta function identities, using a smooth, well-behaved test function $f(x)$ as required.

---

## **Part (a): Prove $\delta(ax) = \frac{1}{|a|} \delta(x)$**

To prove an identity involving the Dirac delta distribution, we evaluate it inside an integral multiplied by a generic test function $f(x)$.

We start with the integral:

$$\int_{-\infty}^{\infty} \delta(ax) f(x) dx$$

Let us perform a change of variables. Set $y = ax$. This means $x = y/a$ and $dx = dy/a$. We must consider two cases based on the sign of $a$:

1. **If $a > 0$:** The limits of integration remain the same ($-\infty$ to $\infty$).
    
    $$\int_{-\infty}^{\infty} \delta(y) f\left(\frac{y}{a}\right) \frac{dy}{a} = \frac{1}{a} f(0)$$
    
2. **If $a < 0$:** The limits of integration are reversed ($\infty$ to $-\infty$).
    
    $$\int_{\infty}^{-\infty} \delta(y) f\left(\frac{y}{a}\right) \frac{dy}{a} = -\int_{-\infty}^{\infty} \delta(y) f\left(\frac{y}{a}\right) \frac{dy}{a} = -\frac{1}{a} f(0)$$
    

Since $a < 0$, we can write $-\frac{1}{a}$ as $\frac{1}{|a|}$. Similarly, when $a > 0$, $\frac{1}{a} = \frac{1}{|a|}$. We can combine both cases into a single expression:

$$\int_{-\infty}^{\infty} \delta(ax) f(x) dx = \frac{1}{|a|} f(0)$$

By the fundamental definition of the delta function, $\int_{-\infty}^{\infty} \frac{1}{|a|} \delta(x) f(x) dx = \frac{1}{|a|} f(0)$. Therefore, the identity holds:

$$\delta(ax) = \frac{1}{|a|} \delta(x)$$

---

### **Part (b): Prove $\delta[g(x)] = \sum_m \frac{1}{|g'(x_m)|} \delta(x - x_m)$**

Consider the integral:

$$\int_{-\infty}^{\infty} \delta(g(x)) f(x) dx$$

The delta function $\delta(g(x))$ is zero everywhere except at the roots where $g(x) = 0$. Let's call these roots $x_m$. Assuming the roots are simple (i.e., $g'(x_m) \neq 0$), we can break the integral into a sum of integrals over small neighborhoods $N_m$ around each root $x_m$:

$$\int_{-\infty}^{\infty} \delta(g(x)) f(x) dx = \sum_m \int_{N_m} \delta(g(x)) f(x) dx$$

Within each infinitesimal neighborhood $N_m$, we can approximate $g(x)$ using a first-order Taylor expansion around the root $x_m$:

$$g(x) \approx g(x_m) + g'(x_m)(x - x_m)$$

Since $x_m$ is a root, $g(x_m) = 0$, leaving $g(x) \approx g'(x_m)(x - x_m)$. Substituting this into our local integral yields:

$$\int_{N_m} \delta(g'(x_m)(x - x_m)) f(x) dx$$

Using the identity proven in part (a), where the constant $a = g'(x_m)$, we can rewrite the delta function:

$$\delta(g'(x_m)(x - x_m)) = \frac{1}{|g'(x_m)|} \delta(x - x_m)$$

Substituting this back into the integral gives:

$$\sum_m \int_{N_m} \frac{1}{|g'(x_m)|} \delta(x - x_m) f(x) dx = \sum_m \frac{1}{|g'(x_m)|} f(x_m)$$

This is exactly the result we would get if we evaluated:

$$\int_{-\infty}^{\infty} \left( \sum_m \frac{1}{|g'(x_m)|} \delta(x - x_m) \right) f(x) dx$$

Thus, equating the arguments of the integrals proves the identity:

$$\delta[g(x)] = \sum_m \frac{1}{|g'(x_m)|} \delta(x - x_m)$$

---

### **Part (c): Evaluate $I = \int_0^\infty dx \, \delta(\cos x) \exp(-x)$**

Here, our function is $g(x) = \cos x$. First, we need to find the roots $x_m$ where $\cos x = 0$ within the integration domain $[0, \infty)$.

The roots are:

$$x_m = \frac{\pi}{2} + m\pi, \quad m = 0, 1, 2, \dots$$

Next, we evaluate the derivative $g'(x) = -\sin x$ at each root:

$$|g'(x_m)| = \left|-\sin\left(\frac{\pi}{2} + m\pi\right)\right| = |\pm 1| = 1$$

Using the identity from part (b), we can expand the delta function:

$$\delta(\cos x) = \sum_{m=0}^\infty \frac{1}{1} \delta\left(x - \left(\frac{\pi}{2} + m\pi\right)\right)$$

Substitute this expansion back into the original integral $I$:

$$I = \int_0^\infty dx \left( \sum_{m=0}^\infty \delta\left(x - \left(\frac{\pi}{2} + m\pi\right)\right) \right) \exp(-x)$$

Interchanging the sum and the integral, the sifting property of the delta function evaluates $\exp(-x)$ at each root $x_m$:

$$I = \sum_{m=0}^\infty \exp\left(-\left(\frac{\pi}{2} + m\pi\right)\right)$$

Factor out the common term:

$$I = \exp(-\pi/2) \sum_{m=0}^\infty \exp(-m\pi)$$

The summation is an infinite geometric series of the form $\sum_{m=0}^\infty r^m = \frac{1}{1-r}$, where the common ratio is $r = \exp(-\pi) < 1$.

$$I = \exp(-\pi/2) \left( \frac{1}{1 - \exp(-\pi)} \right)$$

To simplify this into hyperbolic functions, multiply the numerator and the denominator by $\exp(\pi/2)$:

$$I = \frac{1}{\exp(\pi/2) - \exp(-\pi/2)}$$

Recall the definition of the hyperbolic sine function: $2 \sinh(z) = \exp(z) - \exp(-z)$. Applying this to our denominator with $z = \pi/2$ gives the final confirmed result:

$$I = \frac{1}{2 \sinh(\pi/2)}$$

---

## 1.6

In both cases, the key is to remember that in 3D spherical coordinates, the radial integration measure is $r^2 dr$ (derived from the volume element $d^3r = r^2 \sin\theta \, dr \, d\theta \, d\phi$).

### **Part (a): Prove $\delta(r)/r = -\delta'(r)$**

To prove this, we must evaluate both sides of the identity inside a radial integral with the measure $r^2 dr$.

First, let's look at why a standard smooth test function $f(r)$ yields no information:

- **Left side with $f(r)$:**
    
    $$\int_0^\infty dr \, r^2 \frac{\delta(r)}{r} f(r) = \int_0^\infty dr \, r \delta(r) f(r) = 0 \cdot f(0) = 0$$
    
- **Right side with $f(r)$:**
    
    $$-\int_0^\infty dr \, r^2 \delta'(r) f(r) = \int_0^\infty dr \, \delta(r) \frac{d}{dr}(r^2 f(r)) = \left[ 2r f(r) + r^2 f'(r) \right]_{r=0} = 0$$
    

Because both evaluate trivially to $0$, we cannot confirm the identity's precise behavior. The $r^2$ measure suppresses the singularity at the origin. As suggested, we instead use a test function of the form $f(r)/r$, where $f(r)$ is a smooth function and $f(0) \neq 0$. This mimics operating on a physical potential that diverges as $1/r$ at the origin.

- **Left side with $f(r)/r$:**
    
    $$\int_0^\infty dr \, r^2 \frac{\delta(r)}{r} \left( \frac{f(r)}{r} \right) = \int_0^\infty dr \, \delta(r) f(r) = f(0)$$
    
- **Right side with $f(r)/r$:**
    
    $$-\int_0^\infty dr \, r^2 \delta'(r) \left( \frac{f(r)}{r} \right) = -\int_0^\infty dr \, r \delta'(r) f(r)$$
    
    Applying integration by parts (and assuming $f(r)$ vanishes sufficiently fast at infinity so the boundary term is zero):
    
    $$= \int_0^\infty dr \, \delta(r) \frac{d}{dr}(r f(r)) = \left[ f(r) + r f'(r) \right]_{r=0} = f(0) + 0 = f(0)$$
    

Since both sides yield exactly $f(0)$ under the spherical integration measure, the distributions are equivalent in this context:

$$\frac{\delta(r)}{r} = -\delta'(r)$$

---

### **Part (b): Prove $\nabla \cdot [\delta(r-a)\hat{r}] = \frac{a^2}{r^2}\delta'(r-a)$**

The divergence of a purely radial vector field $\mathbf{A} = A_r(r)\hat{r}$ in spherical coordinates is:

$$\nabla \cdot \mathbf{A} = \frac{1}{r^2} \frac{\partial}{\partial r} (r^2 A_r)$$

Substituting our specific vector field component $A_r = \delta(r-a)$, the left-hand side of our identity becomes:

$$\nabla \cdot [\delta(r-a)\hat{r}] = \frac{1}{r^2} \frac{\partial}{\partial r} [r^2 \delta(r-a)]$$

To prove this is equivalent to the right-hand side, $\frac{a^2}{r^2}\delta'(r-a)$, we integrate both expressions against a smooth test function $f(r)$ using the spherical measure $r^2 dr$.

- **Evaluating the Left-Hand Side:**
    
    $$\int_0^\infty dr \, r^2 \left( \frac{1}{r^2} \frac{\partial}{\partial r} [r^2 \delta(r-a)] \right) f(r) = \int_0^\infty dr \, \frac{\partial}{\partial r}[r^2 \delta(r-a)] f(r)$$
    
    Applying integration by parts (assuming $a > 0$ so the boundary term at $r=0$ vanishes):
    
    $$= \left[ r^2 \delta(r-a) f(r) \right]_0^\infty - \int_0^\infty dr \, r^2 \delta(r-a) f'(r) = 0 - a^2 f'(a) = -a^2 f'(a)$$
    
- **Evaluating the Right-Hand Side:**
    
    $$\int_0^\infty dr \, r^2 \left( \frac{a^2}{r^2} \delta'(r-a) \right) f(r) = a^2 \int_0^\infty dr \, \delta'(r-a) f(r)$$
    
    Applying integration by parts once again:
    
    $$= a^2 \left[ \delta(r-a) f(r) \right]_0^\infty - a^2 \int_0^\infty dr \, \delta(r-a) f'(r) = 0 - a^2 f'(a) = -a^2 f'(a)$$
    

Both expressions yield $-a^2 f'(a)$ when integrated against an arbitrary test function in spherical coordinates, confirming the distributional identity:

$$\nabla \cdot [\delta(r-a)\hat{r}] = \frac{a^2}{r^2}\delta'(r-a)$$

---
## 1.7

Here is the step-by-step proof to show that the given sequence of functions, known as the Dirichlet kernel or scaled sinc function, acts as a representation of the Dirac delta function.

To prove that $D(x) = \lim_{m \to \infty} \frac{\sin mx}{\pi x}$ is a representation of $\delta(x)$, we must evaluate it inside an integral with a smooth, well-behaved test function $f(x)$:

$$I = \lim_{m \to \infty} \int_{-\infty}^{\infty} f(x) \frac{\sin mx}{\pi x} dx$$

Here is the standard analytical approach to solving this:

### **Step 1: Isolate the value at $x = 0$**

We can rewrite the test function by adding and subtracting $f(0)$ in the numerator:

$$f(x) = f(0) + [f(x) - f(0)]$$

Substitute this expanded form back into the integral:

$$I = \lim_{m \to \infty} \left[ \int_{-\infty}^{\infty} f(0) \frac{\sin mx}{\pi x} dx + \int_{-\infty}^{\infty} \frac{f(x) - f(0)}{x} \frac{\sin mx}{\pi} dx \right]$$

### **Step 2: Apply the Riemann-Lebesgue Lemma to the second term**

Let's analyze the second integral. Define a new function $g(x) = \frac{f(x) - f(0)}{x}$.

Because $f(x)$ is a smooth test function, $g(x)$ is perfectly well-behaved at the origin. In fact, taking the limit as $x \to 0$ simply gives the derivative $f'(0)$.

The second integral is essentially the Fourier sine transform of $g(x)$:

$$\lim_{m \to \infty} \frac{1}{\pi} \int_{-\infty}^{\infty} g(x) \sin(mx) dx$$

The **Riemann-Lebesgue lemma** states that the Fourier transform of any integrable function vanishes as the frequency approaches infinity ($m \to \infty$). The rapid oscillations of $\sin(mx)$ cause the positive and negative areas of the integrand to cancel each other out entirely.

Therefore, the second integral evaluates to $0$.

### **Step 3: Evaluate the remaining integral**

We are now left with only the first term, where $f(0)$ can be pulled out of the integral since it is a constant:

$$I = f(0) \lim_{m \to \infty} \frac{1}{\pi} \int_{-\infty}^{\infty} \frac{\sin mx}{x} dx$$

To solve this, we perform a change of variables. Let $y = mx$. This implies $dy = m dx$, and consequently $\frac{dx}{x} = \frac{dy}{y}$. The limits of integration remain $-\infty$ to $\infty$.

$$I = f(0) \frac{1}{\pi} \int_{-\infty}^{\infty} \frac{\sin y}{y} dy$$

### **Step 4: Use the Dirichlet Integral**

The integral of the unnormalized sinc function over the entire real line is a well-known standard result, often evaluated using contour integration in complex analysis:

$$\int_{-\infty}^{\infty} \frac{\sin y}{y} dy = \pi$$

Substitute this exact value back into our equation:

$$I = f(0) \frac{1}{\pi} (\pi) = f(0)$$

Thus, we have proven that under the integral sign:

$$\int_{-\infty}^{\infty} dx f(x) \left( \lim_{m \to \infty} \frac{\sin mx}{\pi x} \right) = f(0)$$

This confirms that $D(x) = \lim_{m \to \infty} \frac{\sin mx}{\pi x}$ is a valid mathematical representation of the Dirac delta distribution $\delta(x)$.

---
## 1.8

To prove these relations without relying on pre-packaged vector identities, the most rigorous approach is to drop down into **tensor index notation**. By using the Levi-Civita symbol ($\epsilon_{ijk}$) for cross products and the Kronecker delta ($\delta_{ij}$) for dot products, we can manipulate the components directly.

Here is the step-by-step derivation for each part.

---

### **(a) Establishing the Left-Side Equality**

We start with the standard Stokes' Theorem:

$$\int_S d\mathbf{S} \cdot (\nabla \times \mathbf{A}) = \oint_C d\mathbf{s} \cdot \mathbf{A}$$

Let $\mathbf{A} = \mathbf{c} \times \mathbf{F}$, where $\mathbf{c}$ is an arbitrary constant vector.

**1. Evaluate the Right-Hand Side (RHS):**

Using index notation, the dot product and cross product can be written as:

$$d\mathbf{s} \cdot (\mathbf{c} \times \mathbf{F}) = ds_i \epsilon_{ijk} c_j F_k$$

Since the Levi-Civita symbol is invariant under cyclic permutations ($\epsilon_{ijk} = \epsilon_{jki}$):

$$ds_i \epsilon_{ijk} c_j F_k = c_j \epsilon_{jki} F_k ds_i = c_j (\mathbf{F} \times d\mathbf{s})_j = \mathbf{c} \cdot (\mathbf{F} \times d\mathbf{s})$$

Because reversing a cross product flips the sign ($\mathbf{F} \times d\mathbf{s} = -d\mathbf{s} \times \mathbf{F}$), the RHS integral becomes:

$$\oint_C d\mathbf{s} \cdot (\mathbf{c} \times \mathbf{F}) = -\mathbf{c} \cdot \oint_C (d\mathbf{s} \times \mathbf{F})$$

**2. Evaluate the Left-Hand Side (LHS):**

Now look at the integrand $\nabla \times (\mathbf{c} \times \mathbf{F})$. The $i$-th component is:

$$[\nabla \times (\mathbf{c} \times \mathbf{F})]_i = \epsilon_{ijk} \partial_j (\epsilon_{klm} c_l F_m)$$

Because $\mathbf{c}$ is a constant, we can pull $c_l$ out of the derivative. Rearranging the Levi-Civita symbols:

$$= \epsilon_{ijk} \epsilon_{klm} c_l \partial_j F_m$$

Using the fundamental contraction identity $\epsilon_{ijk} \epsilon_{klm} = \epsilon_{kij} \epsilon_{klm} = \delta_{il}\delta_{jm} - \delta_{im}\delta_{jl}$, we get:

$$= (\delta_{il}\delta_{jm} - \delta_{im}\delta_{jl}) c_l \partial_j F_m = c_i \partial_j F_j - c_j \partial_j F_i$$

Now, dot this result with the area element $d\mathbf{S} = dS \, \hat{\mathbf{n}}$:

$$d\mathbf{S} \cdot (\nabla \times (\mathbf{c} \times \mathbf{F})) = dS \, \hat{n}_i (c_i \partial_j F_j - c_j \partial_j F_i) = dS [ c_i \hat{n}_i (\partial_j F_j) - c_j \hat{n}_i \partial_j F_i ]$$

Notice that $c_i \hat{n}_i = \mathbf{c} \cdot \hat{\mathbf{n}}$ and $\partial_j F_j = \nabla \cdot \mathbf{F}$. Also, we can factor out $\mathbf{c}$ (represented by $c_j$ in the second term) to express this as a dot product:

$$= \mathbf{c} \cdot [ dS \, \hat{\mathbf{n}} (\nabla \cdot \mathbf{F}) - dS (\hat{n}_i \nabla F_i) ]$$

Integrating over the surface gives the LHS:

$$\mathbf{c} \cdot \int_S dS [ \hat{\mathbf{n}} (\nabla \cdot \mathbf{F}) - \hat{n}_i \nabla F_i ]$$

**3. Equate and Simplify:**

Setting LHS = RHS:

$$\mathbf{c} \cdot \int_S dS [ \hat{\mathbf{n}} (\nabla \cdot \mathbf{F}) - \hat{n}_i \nabla F_i ] = -\mathbf{c} \cdot \oint_C (d\mathbf{s} \times \mathbf{F})$$

Since $\mathbf{c}$ is an arbitrary constant vector, it can be dropped from both sides. Multiplying by $-1$ yields the desired left-side equality:

$$\oint_C d\mathbf{s} \times \mathbf{F} = \int_S dS \{ \hat{n}_i \nabla F_i - \hat{\mathbf{n}}(\nabla \cdot \mathbf{F}) \}$$

---

### **(b) Confirming the Right-Side Equality**

We need to show that the integrand from part (a) is equivalent to $(\hat{\mathbf{n}} \times \nabla) \times \mathbf{F}$. Let's evaluate the $i$-th component of this double cross product.

Let $\mathbf{V} = \hat{\mathbf{n}} \times \nabla$, which means $V_j = \epsilon_{jlm} \hat{n}_l \partial_m$.

$$[(\hat{\mathbf{n}} \times \nabla) \times \mathbf{F}]_i = \epsilon_{ijk} V_j F_k = \epsilon_{ijk} (\epsilon_{jlm} \hat{n}_l \partial_m) F_k$$

Rearrange the Levi-Civita symbols using $\epsilon_{ijk} = -\epsilon_{jik}$:

$$= -\epsilon_{jik} \epsilon_{jlm} \hat{n}_l \partial_m F_k = -(\delta_{il}\delta_{km} - \delta_{im}\delta_{kl}) \hat{n}_l \partial_m F_k$$

Distribute the negative sign and apply the deltas:

$$= (\delta_{im}\delta_{kl} - \delta_{il}\delta_{km}) \hat{n}_l \partial_m F_k = \hat{n}_k \partial_i F_k - \hat{n}_i \partial_k F_k$$

Now, let's translate this back into vector notation:

- The vector whose $i$-th component is $\hat{n}_k \partial_i F_k$ is precisely $\hat{n}_k \nabla F_k$ (changing the dummy index $k$ to $i$ matches your expression: $\hat{n}_i \nabla F_i$).
    
- The vector whose $i$-th component is $\hat{n}_i (\partial_k F_k)$ is simply $\hat{\mathbf{n}} (\nabla \cdot \mathbf{F})$.
    

Therefore:

$$(\hat{\mathbf{n}} \times \nabla) \times \mathbf{F} = \hat{n}_i \nabla F_i - \hat{\mathbf{n}} (\nabla \cdot \mathbf{F})$$

This perfectly confirms the equality on the right side of the expression.

---

### **(c) Showing that $\oint_C \mathbf{r} \times d\mathbf{s} = 2 \int_S d\mathbf{S}$**

We can use the powerful generalized theorem we just proved. Notice that $\mathbf{r} \times d\mathbf{s} = - d\mathbf{s} \times \mathbf{r}$.

Let $\mathbf{F} = \mathbf{r}$, where $\mathbf{r} = x\hat{\mathbf{i}} + y\hat{\mathbf{j}} + z\hat{\mathbf{k}}$. Substituting this into our theorem:

$$\oint_C d\mathbf{s} \times \mathbf{r} = \int_S dS [ (\hat{\mathbf{n}} \times \nabla) \times \mathbf{r} ]$$

Using the expanded form from part (b), we need to evaluate $\hat{n}_i \nabla r_i - \hat{\mathbf{n}} (\nabla \cdot \mathbf{r})$:

1. **Divergence of $\mathbf{r}$:** $\nabla \cdot \mathbf{r} = \frac{\partial x}{\partial x} + \frac{\partial y}{\partial y} + \frac{\partial z}{\partial z} = 1 + 1 + 1 = 3$.
    
2. **Gradient term $\hat{n}_i \nabla r_i$:** Since $r_1=x, r_2=y, r_3=z$, the gradients are $\nabla r_1 = \hat{\mathbf{i}}$, $\nabla r_2 = \hat{\mathbf{j}}$, and $\nabla r_3 = \hat{\mathbf{k}}$. Therefore, the sum is $n_1 \hat{\mathbf{i}} + n_2 \hat{\mathbf{j}} + n_3 \hat{\mathbf{k}} = \hat{\mathbf{n}}$.
    

Substitute these back into the integrand:

$$(\hat{\mathbf{n}} \times \nabla) \times \mathbf{r} = \hat{\mathbf{n}} - 3\hat{\mathbf{n}} = -2\hat{\mathbf{n}}$$

Now evaluate the integral:

$$\oint_C d\mathbf{s} \times \mathbf{r} = \int_S dS (-2\hat{\mathbf{n}}) = -2 \int_S d\mathbf{S}$$

Finally, flip the cross product on the left side to absorb the negative sign:

$$\oint_C \mathbf{r} \times d\mathbf{s} = 2 \int_S d\mathbf{S}$$

---

## 1.16

Here are the step-by-step evaluations for these integrals, which represent the energy density of states for a free particle in one, two, and three dimensions (setting constants like $\hbar$ and $2m$ to $1$).

---

### **(a) Evaluate $g_1(E) = \int_{-\infty}^{\infty} dk_x \, \delta(E - k_x^2)$**

To evaluate this, we use the property of the Dirac delta function for a scalar function $f(x)$:

$$\delta(f(x)) = \sum_i \frac{\delta(x - x_i)}{|f'(x_i)|}$$

where $x_i$ are the roots of $f(x) = 0$.

1. **Find the roots:** Let $f(k_x) = E - k_x^2$. Since $E$ is a positive real number, the roots are $k_x = \pm\sqrt{E}$.
    
2. **Evaluate the derivative:** $f'(k_x) = -2k_x$.
    
3. **Calculate at the roots:**
    
    - At $k_x = \sqrt{E}$, $|f'(\sqrt{E})| = |-2\sqrt{E}| = 2\sqrt{E}$
        
    - At $k_x = -\sqrt{E}$, $|f'(-\sqrt{E})| = |-2(-\sqrt{E})| = 2\sqrt{E}$
        

Rewrite the delta function:

$$\delta(E - k_x^2) = \frac{1}{2\sqrt{E}}\delta(k_x - \sqrt{E}) + \frac{1}{2\sqrt{E}}\delta(k_x + \sqrt{E})$$

Substitute this back into the integral:

$$g_1(E) = \int_{-\infty}^{\infty} \left( \frac{1}{2\sqrt{E}}\delta(k_x - \sqrt{E}) + \frac{1}{2\sqrt{E}}\delta(k_x + \sqrt{E}) \right) dk_x$$

Using the fundamental property of the delta function $\int \delta(x - a)dx = 1$, we get:

$$g_1(E) = \frac{1}{2\sqrt{E}} + \frac{1}{2\sqrt{E}} = \frac{1}{\sqrt{E}} = E^{-1/2}$$

---

### **(b) Evaluate $g_2(E) = \int_{-\infty}^{\infty} dk_x \int_{-\infty}^{\infty} dk_y \, \delta(E - k_x^2 - k_y^2)$**

For a 2D integral with circular symmetry, it is easiest to switch to polar coordinates:

- $k^2 = k_x^2 + k_y^2$
    
- $dk_x \, dk_y = k \, dk \, d\theta$
    

The limits for $k$ are $0$ to $\infty$, and for $\theta$ are $0$ to $2\pi$:

$$g_2(E) = \int_0^{2\pi} d\theta \int_0^{\infty} dk \, k \, \delta(E - k^2)$$

Evaluate the angular integral to get a factor of $2\pi$:

$$g_2(E) = 2\pi \int_0^{\infty} k \, \delta(E - k^2) \, dk$$

Now, apply a simple $u$-substitution:

- Let $u = k^2$, so $du = 2k \, dk$, which means $k \, dk = \frac{1}{2} du$.
    
- The limits remain $0$ to $\infty$.
    

$$g_2(E) = 2\pi \int_0^{\infty} \delta(E - u) \frac{1}{2} du = \pi \int_0^{\infty} \delta(E - u) du$$

Since $E$ is a positive real number, the root $u = E$ lies within the integration domain $[0, \infty)$. Therefore, the integral evaluates to $1$:

$$g_2(E) = \pi$$

---

### **(c) Evaluate $g_3(E) = \int_{-\infty}^{\infty} dk_x \int_{-\infty}^{\infty} dk_y \int_{-\infty}^{\infty} dk_z \, \delta(E - k_x^2 - k_y^2 - k_z^2)$**

For a 3D integral with spherical symmetry, we switch to spherical coordinates:

- $k^2 = k_x^2 + k_y^2 + k_z^2$
    
- $dk_x \, dk_y \, dk_z = k^2 \sin\theta \, dk \, d\theta \, d\phi$
    

The limits are $k \in [0, \infty)$, $\theta \in [0, \pi]$, and $\phi \in [0, 2\pi]$:

$$g_3(E) = \int_0^{2\pi} d\phi \int_0^{\pi} \sin\theta \, d\theta \int_0^{\infty} dk \, k^2 \delta(E - k^2)$$

The angular integrations simply yield the total solid angle of a sphere, $4\pi$:

$$g_3(E) = 4\pi \int_0^{\infty} k^2 \delta(E - k^2) \, dk$$

We can evaluate this using the same composition rule used in part (a). Since $k$ is strictly positive ($k \geq 0$), there is only one root in our domain: $k = \sqrt{E}$.

The derivative of $f(k) = E - k^2$ gives $|-2k| = 2k$. At the root, this is $2\sqrt{E}$.

Thus, the delta function translates to:

$$\delta(E - k^2) \rightarrow \frac{\delta(k - \sqrt{E})}{2\sqrt{E}}$$

Substitute this into our radial integral:

$$g_3(E) = 4\pi \int_0^{\infty} k^2 \frac{\delta(k - \sqrt{E})}{2\sqrt{E}} \, dk$$

Applying the sifting property of the delta function evaluates $k^2$ at $k = \sqrt{E}$:

$$g_3(E) = 4\pi \frac{(\sqrt{E})^2}{2\sqrt{E}} = 4\pi \frac{E}{2\sqrt{E}} = 2\pi \sqrt{E}$$