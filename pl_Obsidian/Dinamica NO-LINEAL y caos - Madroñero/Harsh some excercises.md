
**4.1.** The linear system of conics in $\mathbf{P}^2$ with two assigned base points $P_1$ and $P_2$ (4.1) determines a morphism $\psi$ of $X'$ (which is $\mathbf{P}^2$ with $P_1$ and $P_2$ blown up) to a nonsingular quadric surface $Y$ in $\mathbf{P}^3$, and furthermore $X'$ via $\psi$ is isomorphic to $Y$ with one point blown up.

**4.2.** Let $\varphi$ be the quadratic transformation of (4.2.3), centered at $P_1,P_2,P_3$. If $C$ is an irreducible curve of degree $d$ in $\mathbf{P}^2$, with points of multiplicity $r_1,r_2,r_3$ at $P_1,P_2,P_3$, then the strict transform $C'$ of $C$ by $\varphi$ has degree $d' = 2d - r_1 - r_2 - r_3$, and has points of multiplicity $d - r_2 - r_3$ at $Q_1$, $d - r_1 - r_3$ at $Q_2$ and $d - r_1 - r_2$ at $Q_3$. The curve $C$ may have arbitrary singularities. 

**4.3.** Let $C$ be an irreducible curve in $\mathbf{P}^2$. Then there exists a finite sequence of quadratic transformations, centered at suitable triples of points, so that the strict transform $C'$ of $C$ has only *ordinary* singularities, i.e., multiple points with all distinct tangent directions (I, Ex. 5.14). Use (3.8).

**4.4. (a)** Use (4.5) to prove the following lemma on cubics: If $C$ is an irreducible plane cubic curve, if $L$ is a line meeting $C$ in points $P,Q,R$, and $L'$ is a line meeting $C$ in $ints $P',Q'$'$, let $P''$ be the third intersection of the line $PP'$ with $C$, and define $Q'',R''$ similarly. Then $P'',Q'',R''$ are collinear.

**4.10.** A curious consequence of the implication (iv) $\Rightarrow$ (iii) of (4.11) is the following numerical fact: Given integers $a, b_1, \dots, b_6$ such that $b_i > 0$ for each $i$, $a - b_i - b_j > 0$ for each $i, j$ and $2a - \sum_{i \neq j} b_i > 0$ for each $j$, we must necessarily have $a^2 - \sum b_i^2 > 0$. Prove this directly (for $a, b_1, \dots, b_6 \in \mathbf{R}$) using methods of freshman calculus.

**4.11.** *The Weyl Groups.* Given any diagram consisting of points and line segments joining some of them, we define an abstract group, given by generators and relations, as follows: each point represents a generator $x_i$. The relations are $x_i^2 = 1$ for each $i$; $(x_i x_j)^2 = 1$ if $i$ and $j$ are not joined by a line segment, and $(x_i x_j)^3 = 1$ if $i$ and $j$ are joined by a line segment.
(a) *The Weyl group* $\mathbf{A}_n$ is defined using the diagram
of $n - 1$ points, each joined to the next. Show that it is isomorphic to the symmetric group $\Sigma_n$ as follows: map the generators of $\mathbf{A}_n$ to the elements $(12), (23), \dots, (n - 1, n)$ of $\Sigma_n$, to get a surjective homomorphism $\mathbf{A}_n \to \Sigma_n$. Then estimate the number of elements of $\mathbf{A}_n$ to show in fact it is an isomorphism.

Here are the extracted statements from the exercises in the image:

**5.1.** Let $f$ be a rational function on the surface $X$. Show that it is possible to "resolve the singularities of $f$" in the following sense: there is a birational morphism $g: X' \to X$ so that $f$ induces a morphism of $X'$ to $\mathbf{P}^1$. *Hints:* Write the divisor of $f$ as $(f) = \sum n_i C_i$. Then apply embedded resolution (3.9) to the curve $Y = \bigcup C_i$. Then blow up further as necessary whenever a curve of zeros meets a curve of poles until the zeros and poles of $f$ are disjoint.

**5.2.** Let $Y \cong \mathbf{P}^1$ be a curve in a surface $X$, with $Y^2 < 0$. Show that $Y$ is contractible (5.7.2) to a point on a projective variety $X_0$ (in general singular).

**5.3.** If $\pi: \tilde{X} \to X$ is a monoidal transformation with center $P$, show that $H^1(\tilde{X}, \Omega_{\tilde{X}}) \cong H^1(X, \Omega_X) \oplus k$. This gives another proof of (5.8). *Hints:* Use the projection formula (III, Ex. 8.3) and (III, Ex. 8.1) to show that $H^i(X, \Omega_X) \cong H^i(\tilde{X}, \pi^*\Omega_X)$ for each $i$. Next use the exact sequence
$$
0 \to \pi^*\Omega_X \to \Omega_{\tilde{X}} \to \Omega_{\tilde{X} \mid E} \to 0
$$
and a local calculation with coordinates to show that there is a natural isomorphism $\Omega_{\tilde{X} \mid E} \cong \Omega_E$, where $E$ is the exceptional curve. Now use the cohomology sequence of the above sequence (you will need every term) and Serre duality to get the result.]

**5.4.** Let $f: X \to X'$ be a birational morphism of nonsingular surfaces.
(a) If $Y \subseteq X$ is an irreducible curve such that $f(Y)$ is a point, then $Y \cong \mathbf{P}^1$ and $Y^2 < 0$.
(b) (Mumford [6].) Let $P' \in X'$ be a fundamental point of $f^{-1}$, and let $Y_1, \ldots, Y_r$ be the irreducible components of $f^{-1}(P')$. Show that the matrix $\| Y_i \cdot Y_j \|$ is negative definite.