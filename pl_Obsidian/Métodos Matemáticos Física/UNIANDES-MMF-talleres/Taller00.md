# Taller de repaso
## Métodos Matemáticos de la Física
Prof. J. Madroñero  
http://javiermadronero.correounivalle.edu.co/docencia/mmf-2023i

El curso de Métodos Matemáticos de la Física requiere una sólida fundamentación en análisis real, álgebra lineal y ecuaciones diferenciales. En este taller no se pretende repasar todos los temas de dichas áreas. Aquí nos enfocaremos principalmente en coordenadas polares y conceptos básicos sobre sucesiones y series que los estudiantes deben dominar de sus cursos de cálculo y que son absolutamente necesarios para tener un buen inicio en este curso. Este taller consta de teoremas y problemas los cuales en su mayoría han sido tomados del libro [Stewart, J., Cálculo de una variable, Cengage Learning Editores (2012)]. Se invita a los estudiantes a resolver este taller y reforzar sus debilidades en caso de tenerlas.

---

### 1. 
Sea $\theta$ un número real dado cualquiera. Demuestre que las soluciones de la ecuación cuadrática $x^2 - 2x + \sin^2 \theta = 0$ son $x_1 = 2\cos^2\frac{\theta}{2}$ y $x_2 = 2\sin^2\frac{\theta}{2}$.

### 2. 
Sea $\theta$ un número real dado cualquiera. Se sabe que el número complejo $x$ satisface la identidad $x + \frac{1}{x} = 2\cos\theta$. Encuentre el valor de $x^n + \frac{1}{x^n}$, para $n$ un número natural dado.

### 3. 
Bosqueje la curva $(x^2 + y^2)^3 = 4x^2 y^2$. No use ayudas tecnológicas.

### 4. 
Grafique la curva $r = 4 + 3\sin\theta$ y encuentre el área que encierra, donde $r$ y $\theta$ son las coordenadas polares. No use ayudas tecnológicas.

### 5. 
Encuentre la longitud de la curva $r = 2(1+\cos\theta)$, donde $r$ y $\theta$ son las coordenadas polares. No use ayudas tecnológicas.

### 6. Teorema. 
Sean $\{a_n\}$ y $\{b_n\}$ dos sucesiones reales convergentes y $c$ una constante real. Demuestre que  

(a) $\displaystyle \lim_{n\to\infty}(a_n + b_n) = \lim_{n\to\infty}a_n + \lim_{n\to\infty}b_n$  

(b) $\displaystyle \lim_{n\to\infty}(a_n - b_n) = \lim_{n\to\infty}a_n - \lim_{n\to\infty}b_n$  

(c) $\displaystyle \lim_{n\to\infty}c a_n = c \lim_{n\to\infty}a_n$  

(d) $\displaystyle \lim_{n\to\infty}(a_n b_n) = \lim_{n\to\infty}a_n \cdot \lim_{n\to\infty}b_n$  

(e) $\displaystyle \lim_{n\to\infty}\frac{a_n}{b_n} = \frac{\lim_{n\to\infty}a_n}{\lim_{n\to\infty}b_n}$, si $\lim_{n\to\infty}b_n \neq 0$  

(f) $\displaystyle \lim_{n\to\infty}a_n^p = \left(\lim_{n\to\infty}a_n\right)^p$ si $p>0$ y $a_n>0$.

### 7. 
Determine en cada caso si la sucesión real converge o diverge. Si converge, encuentre el límite.  

(a) $a_n = \dfrac{3n+2}{5n}$  

(b) $a_n = \sqrt{n+1} - \sqrt{9n+1}$  

(c) $a_n = \cos(n/2)$  

(d) $a_n = \left(1 + \frac{2}{n}\right)^n$.

### 8. Comparación de series I: 
Sean $\sum a_n$ y $\sum b_n$ series con términos positivos. Demuestre que  

(i) Si $\sum b_n$ es convergente y $a_n \le b_n$ para toda $n$, entonces $\sum a_n$ también es convergente.  

(ii) Si $\sum b_n$ es divergente y $a_n \ge b_n$ para toda $n$, entonces $\sum a_n$ también es divergente.

### 9. Comparación de series II: 
Sean $\sum a_n$ y $\sum b_n$ series con términos positivos. Si $\displaystyle \lim_{n\to\infty}\frac{a_n}{b_n} = c$, donde $c$ es un número finito y $c>0$, entonces ambas series convergen o ambas divergen.

### 10. 
Sean $a, r \in \mathbb{R}$. Determine cuándo la serie $\displaystyle \sum_{n=1}^{\infty} a r^{n-1}$ converge (y a qué valor converge).

### 11. 
Demuestre que la serie armónica $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n}$ diverge.

### 12. 
Determine en cada caso si la serie es convergente o divergente.  

(a) $\displaystyle \sum_{n=2}^{\infty} \frac{\sqrt{n}}{n-1}$  

(b) $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n!}$  

(c) $\displaystyle \sum_{n=1}^{\infty} \sin\left(\frac{1}{n}\right)$  

(d) $\displaystyle \sum_{n=1}^{\infty} \left(1+\frac{1}{n}\right)^2 e^{-n}$.

### 13. 
El significado de la representación decimal de un número $0.d_1d_2d_3\ldots$ (donde el dígito $d_i$ es uno de los números $0,1,2,\ldots,9$) es que  
$$0.d_1d_2d_3d_4\ldots = \frac{d_1}{10} + \frac{d_2}{10^2} + \frac{d_3}{10^3} + \frac{d_4}{10^4} + \cdots$$  
Demuestre que esta serie siempre es convergente.

### 14. Teorema de la serie alternante: 
Si la serie alternante  
$$\sum_{n=1}^{\infty}(-1)^{n-1}b_n = b_1 - b_2 + b_3 - b_4 + b_5 - b_6 + \cdots,\quad b_n>0$$  
cumple con  

i) $b_{n+1} \le b_n$ para toda $n$  

ii) $\displaystyle \lim_{n\to\infty} b_n = 0$  

entonces la serie es convergente.

### 15. 
Determine si las siguientes series convergen:  

(a) $\displaystyle \sum_{n=1}^{\infty}(-1)^{n}\sin\left(\frac{\pi}{n}\right)$  

(b) $\displaystyle \sum_{n=1}^{\infty}(-1)^{n}\cos\left(\frac{\pi}{n}\right)$.

### 16. Teorema. 
Si una serie $\sum a_n$ es absolutamente convergente, entonces es convergente.

### 17. Criterio de la razón. 

(i) Si $\displaystyle \lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right| = L < 1$, entonces la serie $\sum_{n=1}^{\infty} a_n$ es absolutamente convergente (y, por tanto, convergente).  

(ii) Si $\displaystyle \lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right| = L > 1$, o bien $\displaystyle \lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right| = \infty$, entonces la serie $\sum_{n=1}^{\infty} a_n$ es divergente.  

(iii) Si $\displaystyle \lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right| = 1$, la prueba de la razón no es concluyente; es decir, no se puede sacar conclusión alguna con respecto a la convergencia o a la divergencia de $\sum a_n$.

### 18. Criterio de la raíz. 

(i) Si $\displaystyle \lim_{n\to\infty}\sqrt[n]{|a_n|} = L < 1$, entonces la serie $\sum_{n=1}^{\infty} a_n$ es absolutamente convergente (y, por tanto, convergente).  

(ii) Si $\displaystyle \lim_{n\to\infty}\sqrt[n]{|a_n|} = L > 1$ o $\displaystyle \lim_{n\to\infty}\sqrt[n]{|a_n|} = \infty$, entonces la serie $\sum_{n=1}^{\infty} a_n$ es divergente.  

(iii) Si $\displaystyle \lim_{n\to\infty}\sqrt[n]{|a_n|} = 1$, la prueba de la raíz no es concluyente.

### 19. 
Determine si la serie es absolutamente convergente, condicionalmente convergente o divergente.  

(a) $\displaystyle \sum_{n=1}^{\infty} \frac{\cos(n\pi/3)}{n!}$  

(b) $\displaystyle \sum_{n=1}^{\infty} \frac{(-2)^n}{n^n}$  

(c) $\displaystyle \sum_{n=1}^{\infty} \left(\frac{n^2+1}{2n^2+1}\right)^n$  

(d) $\displaystyle \sum_{n=2}^{\infty} \left(\frac{-2n}{n+1}\right)^{5n}$.


![[Pasted image 20250614183610.png]]


### 20. 
¿Para cuáles enteros positivos $k$ la serie $\displaystyle \sum_{n=1}^{\infty} \frac{(n!)^2}{(kn)!}$ es convergente?

### 21. 
(a) Demuestre que $\displaystyle \sum_{n=0}^{\infty} \frac{x^n}{n!}$ converge para toda $x$.  

(b) Deduzca que $\displaystyle \lim_{n\to\infty} \frac{x^n}{n!} = 0$ para toda $x$.

### 22. 
Los términos de una serie se definen en forma recursiva mediante las ecuaciones  
$$a_1 = 2 \quad \text{y} \quad a_{n+1} = \frac{5n+1}{4n+3} a_n.$$  
Determine si $\sum a_n$ es convergente o divergente.

### 23. 
La función de Bessel de orden 0 se define por  
$$J_0(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{2^{2n} (n!)^2}.$$  
Determine el dominio de esta función.

### 24. Teorema. 
Para una serie de potencias dada $\sum_{n=0}^{\infty} c_n (x-a)^n$ hay sólo tres posibilidades:  

(i) La serie converge sólo cuando $x = a$.  

(ii) La serie converge para toda $x$.  

(iii) Hay un número positivo $R$ tal que la serie converge si $|x-a| < R$ y diverge si $|x-a| > R$.

### 25. 
Determine el radio de convergencia y el intervalo de convergencia de la serie.  

(a) $\displaystyle \sum_{n=0}^{\infty} \frac{(x-2)^n}{n^2+1}$  

(b) $\displaystyle \sum_{n=1}^{\infty} \frac{(2x-1)^n}{5^n \sqrt{n}}$.

### 26. 
La función $J_1$ definida por  
$$J_1(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{n! (n+1)! \, 2^{2n+1}}$$  
se llama función de Bessel de orden 1. Determine su dominio.

### 27. 
La función de Airy (llamada así en honor al matemático y astrónomo inglés sir George Airy (1801-1892)) se define mediante  
$$A(x) = 1 + \frac{x^3}{2\cdot 3} + \frac{x^6}{2\cdot 3 \cdot 5 \cdot 6} + \frac{x^9}{2\cdot 3 \cdot 5 \cdot 6 \cdot 8 \cdot 9} + \cdots$$  
Determine el dominio de la función de Airy.

### 28. 
Encuentre la serie de potencias alrededor de $x=0$ de  

(a) $f(x) = \dfrac{1}{(1+x)^2}$  

(b) $f(x) = \dfrac{1}{(1+x)^3}$  

(c) $f(x) = \dfrac{x^2}{(1+x)^3}$.

### 29. 
Demuestre que la función $\displaystyle f(x) = \sum_{n=0}^{\infty} \frac{x^n}{n!}$ es una solución de la ecuación diferencial $f'(x) = f(x)$ para toda $x$ real. Concluya que $f(x) = e^x$, $x \in \mathbb{R}$.

### 30. Teorema (Series de Taylor). 
Si $f$ se puede representar como una serie de potencias (expansión) en $a$, es decir, si  
$$f(x) = \sum_{n=0}^{\infty} c_n (x-a)^n, \quad |x-a| < R,$$  
entonces sus coeficientes están dados por la fórmula  
$$c_n = \frac{f^{(n)}(a)}{n!}.$$

### 31. Serie binomial. 
Si $k$ es cualquier número real y $|x|<1$, entonces  
$$(1+x)^k = \sum_{n=0}^{\infty} \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \frac{k(k-1)(k-2)}{3!}x^3 + \cdots$$

### 32. 
En cada caso demuestre la validez de la expansión en serie de Taylor con radio de convergencia $R$:  

- $$
\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n = 1 + x + x^2 + x^3 + \cdots, \qquad R = 1
$$

- $$
e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} = 1 + \frac{x}{1!} + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots, \qquad R = \infty
$$

- $$
\sin x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots, \qquad R = \infty
$$

- $$
\cos x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots, \qquad R = \infty
$$

- $$
\arctan x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots, \qquad R = 1
$$

- $$
\ln(1+x) = \sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots, \qquad R = 1
$$

- $$
(1+x)^k = \sum_{n=0}^{\infty} \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!} x^2 + \frac{k(k-1)(k-2)}{3!} x^3 + \cdots, \qquad R = 1
$$