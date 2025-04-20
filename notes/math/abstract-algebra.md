## Group Theory  
A **group** is a set $G$ equipped with a binary operation on $G$ (let’s call it “ $\ast$ ”) that satisfies:
1. Associativity: $a\ast(b\ast c) = (a\ast b)\ast c$ for all $a,b,c\in G$
2. Identity element $e$ exists. $e\ast a = a\ast e = a$ for all $a\in G$
3. Every element has an inverse: $\forall a\in G, \exists a^{-1}$ s.t. $a\ast a^{-1}=a^{-1}\ast a = e$

If in addition $a\ast b = b\ast a$ for all $a,b$ in $G$, the group is **abelian (commutative)​**.

Classic examples of groups include:
* The integers under addition $(\mathbb{Z},+)$
* The nonzero rationals under multiplication $(\mathbb{Q}^\times,\cdot)$
* The symmetric group $S_n$ of permutations on $n$ letters (non-abelian for $n\ge 3$)
* The group of $n\times n$ invertible matrices $GL_n(F)$ over a field $F$ under matrix multiplication​

Groups can be finite or infinite, abelian or non-abelian, but all share the above axioms.

### Key Theorems and Concepts

**Lagrange’s Theorem**: if $H$ is a subgroup of a finite group $G$, then the order (size) of $H$
divides the order of $G$​.

As a consequence, order of any element $a$ of a finite group (i.e. the smallest $k$ such that $a^k=e$)
divides the order of that group. This can be used to prove **Fermat’s Little Theorem**.

**Fermat's Little Theorem.** Let $p$ be a prime number, and $a$ an integer such that $p \nmid a$. Then:

$$
a^{p-1} \equiv 1 \pmod{p}
$$

**Proof.** Let $G = (\mathbb{Z}/p\mathbb{Z})^\times$  be the multiplicative group of integers modulo $p$.
Since $p$ is prime, this group contains $1, 2, \ldots, p-1$. So, $|G| = p - 1$. Since order of every element
divides $p - 1$, for every $a \in G$ we have:

$$
a^{p-1} \equiv 1 \pmod{p}
$$

**Cauchy’s Theorem.** For a prime $p$ dividing $|G|$, there exists an element of order $p$.



