## Essential Theorems

**Fundamental Theorem of Algebra (FTA).** Every nonconstant polynomial with complex coefficients has at least
one complex root. In fact, a degree-n polynomial has exactly n complex roots (counting multiplicities).

**Factor Theorem and Root Factorization.** If $P(r) = 0$ for polynomial $P(x)$, then $(x - r)$ is a factor of
$P(x)$. Conversely, any polynomial of degree $n$ can be factored as $a \cdot (x - r_1) \cdots (x-r_n)$ over
$\mathbb{C}$ (by FTA).

A consequence is that a non-zero polynomial of degree $n$ have at most $n$ distinct roots in $\mathbb{R}$ or
$\mathbb{C}$.

**Vieta's Formulas.** For a monic polynomial $x^n + c_{n-1} x^{n-1} + \cdots + c_1 x + c_0 =
a_n \prod_{i=1}^n (x - r_i)$ (with roots $r_i$), the coefficients relate to symmetric sums of
roots: $c_{n-1} = -\sum_{i} r_i$, $c_{n-2} = \sum_{i<j} r_i r_j$, ..., $c_0 = (-1)^n r_1 r_2 \cdots r_n$.

**Rational Root Theorem.** For a polynomial with integer coefficients, any rational root $p/q$
(in lowest terms) must satisfy that $p$ divides the constant term and $q$ divides the leading coefficient.

**Polynomial Remainder Theorem.** The remainder of $P(x)$ upon division by $(x - r)$ is $P(r)$.
In particular, $P(r)=0$ iff $(x-r)$ is a factor (which is the Factor Theorem).

**Binomial Theorem.** $(x+y)^n = \sum_{k=0}^n \binom{n}{k} x^{n-k} y^k$.

**Arithmetic Mean - Geometric Mean (AM-GM) Inequality.** For nonnegative reals
$x_1,\dots,x_m$, $\displaystyle \frac{x_1 + x_2 + \cdots + x_m}{m} \ge \sqrt[m]{x_1 x_2 \cdots x_m}$,
with equality iff $x_1=\cdots=x_m$. 

**Cauchy-Schwarz Inequality.** For any real sequences $(a_i)$ and $(b_i)$,

$$
\left(\sum_{i=1}^n a_i b_i\right)^2 \le \left(\sum_{i=1}^n a_i^2\right)\left(\sum_{i=1}^n b_i^2\right)
$$

Equality holds iff $a_i/b_i$ is constant for all $i$ (sequences are proportional).

**Triangle Inequality.** For any real (or complex) numbers, $|x + y| \le |x| + |y|$.
In $\mathbb{R}^n$, $\|\mathbf{u}\| + \|\mathbf{v}\| \le \|\mathbf{u}\| + \|\mathbf{v}\|$.

## Other Techniques

**Vieta Jumping.** TODO (https://en.wikipedia.org/wiki/Vieta_jumping)

## Problems

### IMO

**IMO 2012/2.** Let $a_2, a_3, \ldots a_n$ be positive reals with product 1, where $n \ge 3$. Show that

$$
(1 + a_2)^2 (1+a_3)^3 \cdots (1+a_n)^n > n^n.
$$

**Hint.** Use AM-GM for each term.

**Solution.** See [IMO-2012-notes.pdf](https://web.evanchen.cc/exams/IMO-2012-notes.pdf)

**Math 2012/4.** Find all functions $f: \mathbb{Z} \rightarrow \mathbb{Z}$ such that, for all integers
$a, b, c$ that satisfy $a + b + c = 0$, the following equality holds:

$$
f(a)^2 + f(b)^2 + f(c)^2 = 2 f(a) f(b) + 2 f(b) f(c) + 2 f(c) f(a)
$$

**Solution.** See [IMO-2012-notes.pdf](https://web.evanchen.cc/exams/IMO-2012-notes.pdf)

