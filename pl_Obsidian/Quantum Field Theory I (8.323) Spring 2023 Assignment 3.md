A continuación se presenta el texto completo del archivo `mit8_323_s23_pset03.pdf`, incluyendo las expresiones en LaTeX tal como aparecen en el contenido proporcionado.

---
Quantum Field Theory I (8.323) Spring 2023 Assignment 3

Feb. 21, 2023



## Readings

- Peskin & Schroeder Chap. 2- Weinberg vol 1 Chap. 1

## Notes: useful formulae

1. All single-particle states used below follow relativistic normalization, i.e.

$$\left[|k\rangle = \sqrt{2\omega_{\vec{k}}} a_{\vec{k}}^{\dagger}|0\rangle \right]. \quad (1)$$

2. The unitary quantum operator generating a spacetime translation $y^{\mu}$ is written as

$$U_{y} = e^{-iP^{\mu}y_{\mu}} = e^{iH y^{0} - iP^{\mu}y^{i}},\qquad P^{\mu} = (H,P^{i}). \quad (2)$$

It should be understood that the vacuum energy is already subtracted from $H$ . $U_{y}$ acts on creation and annihilation operators as

$$U_{y}a_{\vec{k}}U_{\vec{y}}^{\dagger} = e^{-i\omega_{\vec{k}}y^{0} + i\vec{k}\vec{y}}a_{\vec{k}} = e^{i\vec{k}\vec{y}}a_{\vec{k}},\qquad U_{y}a_{\vec{k}}^{\dagger}U_{\vec{y}}^{\dagger} = e^{-i\vec{k}\vec{y}}a_{\vec{k}}^{\dagger}. \quad (3)$$

3. The quantum operator generating a Lorentz transformation is

$$U_{\Lambda} = e^{\frac{i}{2}\omega_{\mu \nu}M^{\mu \nu}} \quad (4)$$

where $\omega_{\mu \nu} = - \omega_{\nu \mu}$ are finite constants.

4. For a complex scalar field we also have the unitary operator which generates a phase rotation

$$U_{\alpha} = e^{-i\alpha Q}, \quad (5)$$

where

$$Q = i\int d^{3}x[\pi_{\phi^{*}}\phi^{*} - \pi_{\phi}\phi ]~. \quad (6)$$



1. Lorentz transformations for operators and states (15 points)

(a) From the commutation relation of creation and annihilation operators $a_{\vec{k}}$ and $a_{\vec{k}}^{\dagger}$

$$[a_{\vec{k}},a_{\vec{k}}^{\dagger}] = (2\pi)^{3}\delta^{(3)}(\vec{k} -\vec{k}^{\prime}) \quad (7)$$

and the result of problem 2(b) of pset 1 argue that $a_{\vec{k}},a_{\vec{k}}^{\dagger}$ should transform under a Lorentz transformation as

$$a_{\vec{k}} \rightarrow {\tilde{a}_{\vec{k}} = \sqrt{\frac{\omega_{\Lambda\vec{k}}}{\omega_{\vec{k}}}} a_{\Lambda \vec{k}}} 
$$


(b) Using the expression of $M_{\mu \nu}$ of problem 4(c) of Pset 2 to compute

$$\frac{1}{2} [\omega_{\mu \nu}M^{\mu \nu},a_{\vec{k}}],\quad \frac{1}{2} [\omega_{\mu \nu}M^{\mu \nu},a_{\vec{k}}^{\dagger}] \quad (10)$$

where $\omega_{\mu \nu} = - \omega_{\nu \mu}$ are infinitesimal constant. Show that this indeed generates an infinitesimal Lorentz transformation in $a_{\vec{k}}$ and $a_{\vec{k}}^{\dagger}$ which are consistent with (8)- (9).

(c) Now consider unitary operator generating finite Lorentz transformations

$$U_{\Lambda} = e^{\frac{1}{2}\omega_{\mu \nu}M^{\mu \nu}} \quad (11)$$

where $\omega_{\mu \nu}$ are finite constants. Show that

$$U_{\Lambda}|0\rangle = |0\rangle \quad (12)$$

i.e. the vacuum is Lorentz invariant. One can derive equations (8)- (9) by explicitly evaluating $U_{\Lambda}a_{\vec{k}}U_{\Lambda}^{\dagger}$ and $U_{\Lambda}a_{\vec{k}}^{\dagger}U_{\Lambda}^{\dagger}$ . I will NOT ask you to show this. Assuming (8)- (9) show that

$$U_{\Lambda}|k\rangle = |\Lambda k\rangle . \quad (13)$$

[Note: this part shows that the vacuum is Lorentz invariant.]

## 2. Spatially localized states of a scalar particle (25 points)

In a quantum field theory there is no natural way to define position eigenvector $|\vec{x}\rangle$ as $\vec{x}$ is now simply a label, not an operator. Also there is a fundamental

conflict: a perfectly localized state in space is not a Lorentz covariant concept
as it picks out a reference frame (we cannot perfectly localize in time at the same time).
In the problem we will make these abstract statements concrete.
Consider states of the form
$$|\vec{r}, t\rangle_f \equiv \int d^3\vec{k} f(\vec{k}) |k\rangle e^{-i\vec{k}\cdot\vec{r}+i\omega_{\vec{k}} t},$$
(14)
where $f(\vec{k})$ is a function to be determined and $|k\rangle$ is the one-particle state (1)
of momentum $\vec{k}$ and energy $\omega_{\vec{k}}$.
(a) Determine $f(\vec{k})$ by the condition of perfect localization
$$_f\langle\vec{r}_1, t|\vec{r}_2, t\rangle_f = \delta^{(3)}(\vec{r}_1 - \vec{r}_2).$$
(15)
(b) By acting unitary operator $U_\Lambda$ for a Lorentz transformation (as defined
in (4)) on your result in part (a) show that $|\vec{r}, t\rangle_f$ is not Lorentz covariant,
i.e.
$$U_\Lambda|\vec{r}, t\rangle_f \neq |\Lambda\vec{r}, \Lambda t\rangle_f$$
(16)
where $\Lambda\vec{r}$ and $\Lambda t$ denote Lorentz transformation of $\vec{r}, t$.
(c) With $f(\vec{k})$ given by (a), consider the overlap $C(\vec{r}_1-\vec{r}_2, t_1-t_2) = {}_f\langle\vec{r}_2, t_2|\vec{r}_1, t_1\rangle_f$.
Evaluate $C(\vec{r}, t)$ for a spacelike separation: $|\vec{r}| > t$.
Suppose we interpret $|_f\langle\vec{r}_2, t_2|\vec{r}_1, t_1\rangle_f|^2$ as the probability for the particle originally at $\vec{r}_1$ at time $t_1$ to transition to $\vec{r}_2$ at time $t_2$. Would the propagation
be causal (i.e. confined to the forward light-cone)?
Note: The above parts suggest that it is not sensible to interpret the state
determined from part (a) describing a particle localized at $\vec{r}$ at time $t$.
(d) Compare your resulting state $|\vec{r}, t\rangle_f$ in part (a) with the state
$$|x\rangle \equiv \varphi(x)|0\rangle$$
(17)
where $x = (\vec{x}, t)$. Are the states $|x\rangle$ perfectly localized? Show that $|x\rangle$ is
Lorentz covariant, i.e.
$$U_\Lambda|x\rangle = |\Lambda x\rangle.$$
(18)
(e) Consider a state
$$|\Psi\rangle = \int \frac{d^3\vec{k}}{(2\pi)^3} h(\vec{k})|k\rangle$$
(19)
with the corresponding “wave function” defined as
$$\Psi(x) = \langle 0|\varphi(x)|\Psi\rangle.$$
(20)


## 3 Normal ordering and smeared fields (25 points) 

Consider the free real scalar field theory discussed in lectures.

(a) First show that

$$\langle 0|\phi (\vec{x},t)|0\rangle = 0. \quad (21)$$

Evaluate the vacuum expectation value

$$\sigma^{2}\equiv \langle 0|\phi^{2}(\vec{x},t)|0\rangle . \quad (22)$$

Express $\sigma^{2}$ as an integral over a single variable and show that the integral is divergent.

This result tells you that the vacuum is not empty! While the expectation value of $\phi$ is zero, the fluctuations of $\phi$ , as measured by $\sigma^{2}$ , are nonzero, and in fact are infinitely large. This is a reflection of that a QFT has an infinite number of degrees of freedom.

(b) The general philosophy of QFT is to regard operators like $\phi^{2}(\vec{x},t)$ as "bad" operators. One then introduces "good" operators which do not suffer divergences, a procedure often referred to as renormalization. One way to remove the divergence in part (a) is to introduce normal ordered operators. The rule of normal ordering is that whenever you see products of $a_{\vec{k}}$ 's and $a_{\vec{k}}^{\dagger}$ 's move all the $a_{\vec{k}}$ 's to the right of $a_{\vec{k}}^{\dagger}$ 's. We denote the normal ordered version of an operator $\mathcal{O}$ by : $\mathcal{O}$ : For example,

$$: a_{\vec{k}_1}a_{\vec{k}_2}^{\dagger}a_{\vec{k}_3}a_{\vec{k}_4}^{\dagger} := a_{\vec{k}_2}^{\dagger}a_{\vec{k}_4}^{\dagger}a_{\vec{k}_1}a_{\vec{k}_3}. \quad (23)$$

Express normal ordered operator : $\phi^{2}(\vec{x},t)$ : in terms of $a_{\vec{k}}$ and $a_{\vec{k}}^{\dagger}$ . Show that $\langle 0|:\phi^{2}(\vec{x},t):|0\rangle = 0$ and

$$\phi^{2}(\vec{x},t) = :\phi^{2}(\vec{x},t): + \sigma^{2}\mathbf{1} \quad (24)$$

where 1 is the identity operator.

(c) Another way to introduce "good" operators is to consider the "smeared" field

$$\tilde{\phi} (\vec{x},t)\equiv N\int d^{3}y\phi (\vec{y},t)e^{-\frac{(\vec{x} - \vec{y})^{2}}{a^{2}}},\quad N = \frac{1}{\pi^{\frac{3}{2}}a^{3}}. \quad (25)$$

The definition is motivated from the fact that the divergence in part (a) comes from having two $\phi$ 's at the same spacetime point. In (25) we thus


1 Note that it is possible that the Lagrangian is invariant under phase rotations, but the vacuum is not. The phenomenon is normally referred to as "spontaneous symmetry breaking," a subject of QFT III. This happens, e.g. in superluids and superconductors, whose many fascinating properties arise from spontaneous symmetry breaking.

"smear" (or average) $\phi$ in a region of radius $a$ . $N$ is a normalization factor, chosen so that

$$\lim_{a\to 0}\tilde{\phi} (\vec{x},t) = \phi (\vec{x},t). \quad (26)$$

Show that

$$\left\langle 0|\tilde{\phi} (\vec{x},t)|0\right\rangle = 0. \quad (27)$$

Now consider the fluctuation of $\tilde{\phi}$

$$\tilde{\sigma}^{2}\equiv \left\langle 0\left|\tilde{\phi}^{2}(\vec{x},t)\right|0\right\rangle . \quad (28)$$

Express $\tilde{\sigma}^{2}$ as an integral over a single variable and show that it is finite.

(d) Without evaluating the integral in part (c), show that in the limits of small $a$ and large $a$ , the leading term in $\tilde{\sigma}^{2}$ may be written as

$$\tilde{\sigma}^{2}\approx \alpha a^{\gamma} \quad (29)$$

and calculate $\alpha$ and $\gamma$ for each of these two limits. You should discover that at large $a$ the average field approaches a classical variable whereas at small $a$ it is dominated by fluctuations.

## 4. Correlation functions for a complex scalar (15 points)

Consider a theory of a complex scalar field $\phi$ which is invariant under a phase rotation of $\phi$ . The unitary operator $U_{\alpha}$ generating a phase rotation is written in (5). We also assume that the vacuum of the theory is invariant under the phase rotation,<sup>1</sup>

$$U_{\alpha}|0\rangle = |0\rangle . \quad (30)$$

The theory can be interacting. That is, in this problem, you should not use the mode expansion for $\phi$ discussed in lecture which applies only to a free field theory.

(a) Show that

$$U_{\alpha}\phi (x)U_{\alpha}^{\dagger} = e^{i\alpha}\phi (x),\qquad U_{\alpha}\phi^{*}(x)U_{\alpha}^{\dagger} = e^{-i\alpha}\phi^{*}(x). \quad (31)$$

(b) Show that

$$\langle 0|\phi (x)\phi (x^{\prime})|0\rangle = 0. \quad (32)$$


3) Now consider a general $n$ -point function of products of $\phi$ 's and $\phi^{\dagger}$ 's inserted at different spacetime points between the vacuum, i.e.

$$\langle 0|\phi (x_1)\dots \phi^\dagger (x_i)\dots \phi_n(x_n)|0\rangle . \quad (33)$$

Show that the above quantity vanishes whenever the numbers of $\phi$ 's and $\phi^{\dagger}$ 's are not the same.




For information about citing these materials or our Terms of Use, visit: https://ocw.mit.edu/terms.

---

8.323 Relativistic Quantum Field Theory I Spring 2023