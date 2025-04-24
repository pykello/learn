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
* The *dihedral group* $D_{n}$ of order $2n$ is the group of symmetries (rotations and reflections) of a regular $n$-gon.
    * $D_n = \left\\{ R_0, R, R^2, \dots, R^{n-1}, F, FR, FR^2, \dots, FR^{n-1} \right\\}$
* The *general linear group* $\mathrm{GL}(n,F)$ is the group of all invertible $n\times n$ matrices over a field $F$.
* The *special linear group* $\mathrm{SL}(n,F)$ is the group of $n\times n$ matrices over $F$ with determinant $1$.

Groups can be finite or infinite, abelian or non-abelian, but all share the above axioms.

#### Exercises
1. (Gallian) Prove $(ab)^2 = a^2b^2$ iff $ab = ba$.
2. (Gallian) Let $G$ be a finite group and $n$ an odd positive integer. Show that the number of elements $x$ of $G$ such that $x^n = e$ is odd.
3. (Gallian) Prove the number of nonidentity elements s.t. $x^5=e$ is a multiple of 4.
4. (Milnor) Show that a nonempty finite set with an associative binary operation satisfying the cancellation laws is a group.

A **subgroup** of a group $G$ is a subset $H \subseteq G$ that is itself a group under the same operation as $G$.

A **left coset** of a subgroup $H$ in $G$ is a set of the form $gH = \{gh \mid h \in H\}$, for some $g \in G$. The **set of left cosets** of a subgroup $H$ in a group $G$ is $\{gH \mid g \in G\}$,
which partitions $G$ into disjoint subsets, each of the form $gH$.


**Example.** Let $G = \mathbb{Z}$ (the integers under addition), and let $H = 3\mathbb{Z} = \{ \ldots, -6, -3, 0, 3, 6, \ldots \}$. Then a left coset of $H$ is:

$$
1 + H = \{ \ldots, -5, -2, 1, 4, 7, \ldots \}.
$$

The set of all left cosets of $H = 3\mathbb{Z}$ in $G = \mathbb{Z}$ is:

$$
\{0 + H, 1 + H, 2 + H\} = \{3\mathbb{Z}, 1 + 3\mathbb{Z}, 2 + 3\mathbb{Z}\}.
$$

This partitions $\mathbb{Z}$ into three disjoint classes modulo 3.

The **center of a group** $G$, denoted $Z(G)$, is the set of elements that commute with all elements of $G$:

$$
Z(G) = \\{ z \in G \mid \forall g \in G, \; zg = gz \\}
$$

The **centralizer of an element** $a \in G$, denoted $C_G(a)$, is the set of elements in $G$ that commute with $a$:

$$
C_G(a) = \\{ g \in G \mid ga = ag \\}
$$

A **homomorphism** between two groups $(G, \cdot)$ and $(H, *)$ is a function $f : G \to H$ such that $f(x \cdot y) = f(x) * f(y)$ for all  $x, y \in G$.

#### Exercises
1. Prove: Let $H$ be a nonempty subset of group $G$. If $ab^{-1} \in H$ whenever $a, b \in H$, then $H$ is a subroup of $G$.
   - Prove: If $G$ is an Abelian group, then $H = \left\\{x \in G | x^2 = e\right\\}$ is a subgroup of $G$.
   - Prove: If $G$ is an Abelian group, then $H = \left\\{x^2 | x \in G\right\\}$ is a subgroup of $G$.
2. Prove: Let $H$ be a nonempty subset of group $G$. If $ab \in H$ whenever $a, b \in H$, and $a^{-1} \in H$ whenever $a \in H$, then $H$ is a subgroup of $G$.
   - Prove: If $G$ is an Abelian group, then $H = \left\\{x \in G | |x| \text{is finite}\right\\}$ is a subroup of $G$.
   - Prove: If $G$ is an Abelian group and $H, K$ are subroups of $G$, then $HK = \left\\{hk | h \in H, k \in K\right\\}$ is a subroup of $G$.
3. Prove that the center of a group $G$ is a subgroup of $G$. Do the same for centralizer of $a \in G$.

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

**Class Equation.** The class equation of a finite group $G$ expresses its order as a sum over conjugacy classes:

$$
|G| = |Z(G)| + \Sigma_i[G: C_G(g_i)]
$$

**Existence of Cyclic Subgroups.** For any element $g \in G$, the set $\langle g \rangle = {g^n | n \in \mathbb{Z}}$ forms a **cyclic subgroup of $G$, generated by $g$. This is the smallest subgroup containing $g$.

**Fundamental Theorem of Finite Abelian Groups** states that any finite abelian group is isomorphic to a direct sum of cyclic groups of prime-power order​.  This classification is helpful in understanding the structure of abelian groups.

Another important notion is a **group homomorphism**, a structure-preserving map between groups. The **First Isomorphism Theorem** tells us that if $f: G \to G'$ is a homomorphism, then $\text{im} f \cong G/\ker f$. That is, the image of $f$ is isomorphic to the quitent group $G / \ker f$.

### Problem Solving Strategies
* *Use Lagrange’s Theorem*: If a problem involves a finite group of known order, consider the possible orders of subgroups or elements. For example, if $|G|$ is prime, $G$ must be cyclic of that prime order. If an equation like $a^k = e$ is given, the order of $a$ divides $k$. This can restrict possibilities and simplify the problem.
* *Use Group Homomorphisms.* Look for mappings between groups to reduce complexity. A homopmorphism $\phi: G \to H$ can reveal structure via its kernel and image. The First Isomorphism Theorem is particularly powerful for understanding quotient groups.
* *Consider extreme or special elements*: The identity $e$ and inverses are often crucial. If an equation or condition is given for all group elements, try plugging in $a=e$ or $b=a^{-1}$ or such to glean information. For instance, if given a functional equation on $G$, substituting identity elements can simplify it.
* *Look for invariants or actions*: To count or classify objects up to symmetry, consider group actions. Tools like the orbit-stabilizer theorem and Burnside’s Lemma help solve problems like counting cube colorings under rotation. This strategy, common in combinatorics, often involves symmetry groups.
* *Direct algebraic manipulation*: Don’t forget to apply the basic axioms.
* *Try small cases or constructing subgroups*: If a problem states a general claim, test it on small groups (like $\mathbb{Z}_n$ or $S_3$) to see what’s going on. Sometimes understanding the claim for simple examples gives insight into the general proof. If the problem asserts something must equal the identity, attempt to show it by considering the element’s powers or the subgroup it generates.

### Exercises
1. Let $G$ be a finite group of order $n$. Show that for every integer $k$, either there is an element of order $k$ in $G$ or there is an element of order $\gcd(n,k)$ in $G$.

### Putnam Problems

**Putnam 1968 B2.**  $(G, *)$ is a finite group with $n$ elements. $K$ is a subset of $G$ with more than $n/2$ elements. Prove that for every $g ∈ G$, we can find $h, k ∈ K$ such that $g = h * k$.

*Solution.* See [psol688.html](https://prase.cz/kalva/putnam/psoln/psol688.html)

**Putnam 1969 B2.** $G$ is a finite group with identity 1. Show that we cannot find two proper subgroups $A$ and $B$ (≠ ${1}$ or $G$) such that $A ∪ B = G$. Can we find three proper subroups $A$, $B$, $C$ such that $A \cup B \cup C = G$?

*Solution.* See [psol698.html](https://prase.cz/kalva/putnam/psoln/psol698.html) and [2017-8a.pdf](https://web.ma.utexas.edu/users/rusin/Putnam/2017/2017-8a.pdf)

**Putnam 1972 B3.** A group has elements $g, h$ satisfying: $ghg = hg^2h$, $g^3 = 1$, $h^n = 1$ for some odd $n$. Prove $h = 1$.

*Solution.* [psol729.html](https://prase.cz/kalva/putnam/psoln/psol729.html)

**Putname 1975 B1.**  Let $G$ be the group $\left\\{ (m, n) : m, n \in \mathbb{Z} \right\\}$ with the operation $(a, b) + (c, d) = (a + c, b + d)$. Let $H$ be the smallest subgroup containing $(3, 8)$, $(4, -1)$ and $(5, 4)$. Let $Hab$ be the smallest subgroup containing $(0, a)$ and $(1, b)$. Find $a > 0$ such that $Hab = H$. 

*Solution.* [psol757.html](https://prase.cz/kalva/putnam/psoln/psol757.html)

**Putnam 1976 B2.** $G$ is a group generated by the two elements $g, h$, which satisfy $g^4 = 1$, $g^2 ≠ 1$, $h^7 = 1$, $h ≠ 1$, $ghg^{-1}h = 1$. The only subgroup containing $g$ and $h$ is $G$ itself. Write down all elements of $G$ which are squares.

*Solution.* [psol768.html](https://prase.cz/kalva/putnam/psoln/psol768.html)

**Putnam 1989 B2.**  Let $S$ be a non-empty set with a binary operation (written like multiplication) such that: (1) it is associative; (2) $ab = ac$ implies $b = c$; (3) $ba = ca$ implies $b = c$; (4) for each element, the set of its powers is finite. Is $S$ necessarily a group? 

*Solution.* See [psol898.html](https://prase.cz/kalva/putnam/psoln/psol898.html) and [2017-8a.pdf](https://web.ma.utexas.edu/users/rusin/Putnam/2017/2017-8a.pdf)

**Putnam 1997 A4.** Let $G$ be a group with identity $e$ and $\phi : G \to G$ a function such that

$$
\phi(g_1)\phi(g_2)\phi(g_3) = \phi(h_1)\phi(h_2)\phi(h_3)
$$

whenever $g_1 g_2 g_3 = e = h_1 h_2 h_3$. Prove that there exists an element $a \in G$ such that $\psi(x) = a \phi(x)$ is a homomorphism (i.e., $\psi(xy) = \psi(x)\psi(y)$ for all $x, y \in G$).

**Putnam 2007 A5.** Suppose that a finite group has exactly $n$ elements of order $p$, where $p$ is a prime. Prove that either $n = 0$ or $p$ divides $n + 1$.

**Putnam 2008 A6.** Prove that there exists a constant $c > 0$ such that in every nontrivial finite group $G$ there exists a sequence of length at most $c \log |G|$ with the property that each element of $G$ equals the product of some subsequence.

(The elements of $G$ in the sequence are not required to be distinct. A *subsequence* of a sequence is obtained by selecting some of the terms, not necessarily consecutive, without reordering them; for example, $4, 4, 2$ is a subsequence of $2, 4, 6, 4, 2$, but $2, 2, 4$ is not.)

**Putnam 2009 A5.** Is there a finite abelian group $G$ such that the product of the orders of all its elements is $2^{2009}$?

**Putnam 2010 A5.** Let $G$ be a group, with operation $\ast$. Suppose that

1. $G$ is a subset of $\mathbb{R}^3$ (but $\ast$ need not be related to addition of vectors);
2. For each $\mathbf{a}, \mathbf{b} \in G$, either $\mathbf{a} \times \mathbf{b} = \mathbf{a} \ast \mathbf{b}$ or $\mathbf{a} \times \mathbf{b} = \mathbf{0}$ (or both), where $\times$ is the usual cross product in $\mathbb{R}^3$.

Prove that $\mathbf{a} \times \mathbf{b} = \mathbf{0}$ for all $\mathbf{a}, \mathbf{b} \in G$.

**Putnam 2011 A6.** Let $G$ be an abelian group with $n$ elements, and let

$$
\{g_1 = e, g_2, \ldots, g_k\} \subseteq G
$$

be a (not necessarily minimal) set of distinct generators of $G$. A special die, which randomly selects one of the elements $g_1, g_2, \ldots, g_k$ with equal probability, is rolled $m$ times and the selected elements are multiplied to produce an element $g \in G$. Prove that there exists a real number $b \in (0, 1)$ such that

$$
\lim_{m \to \infty} \frac{1}{b^{2m}} \sum_{x \in G} \left( \text{Prob}(g = x) - \frac{1}{n} \right)^2
$$

is positive and finite.


**Putnam 2016 A5.** Suppose that $G$ is a finite group generated by the two elements $g$ and $h$, where the order of $g$ is odd. Show that every element of $G$ can be written in the form

$$
g^{m_1} h^{n_1} g^{m_2} h^{n_2} \cdots g^{m_r} h^{n_r}
$$

with $1 \le r \le |G|$ and $m_1, n_1, m_2, n_2, \ldots, m_r, n_r \in \{-1, 1\}$. (Here $|G|$ is the number of elements of $G$.)

**Putnam 2018 A4.** Let $m$ and $n$ be positive integers with $\gcd(m, n) = 1$, and let

$$
a_k = \left\lfloor \frac{mk}{n} \right\rfloor - \left\lfloor \frac{m(k-1)}{n} \right\rfloor
$$

for $k = 1, 2, \ldots, n$. Suppose that $g$ and $h$ are elements in a group $G$ and that

$$
gh^{a_1} g h^{a_2} \cdots g h^{a_n} = e,
$$

where $e$ is the identity element. Show that $gh = hg$. (As usual, $\lfloor x \rfloor$ denotes the greatest integer less than or equal to $x$.)

### IMC Problems

**IMC 2012 P3.** Given an integer $n > 1$, let $S_n$ be the group of permutations of the numbers $1, 2, \ldots, n$. Two players, A and B, play the following game. Taking turns, they select elements (one element at a time) from the group $S_n$. It is forbidden to select an element that has already been selected. The game ends when the selected elements generate the whole group $S_n$. The player who made the last move loses the game. The first move is made by A. Which player has a winning strategy?

**IMC 2018 P2.** Does there exist a field such that its multiplicative group is isomorphic to its additive group? 

**IMC 2020 P7.** Let $G$ be a group and $n \geq 2$ be an integer. Let $H_1$ and $H_2$ be two subgroups of $G$ that satisfy

$$
[G : H_1] = [G : H_2] = n \quad \text{and} \quad [G : (H_1 \cap H_2)] = n(n - 1).
$$

Prove that $H_1$ and $H_2$ are conjugate in $G$.

(Here $[G : H]$ denotes the \textit{index} of the subgroup $H$, i.e., the number of distinct left cosets $xH$ of $H$ in $G$. The subgroups $H_1$ and $H_2$ are \textit{conjugate} if there exists an element $g \in G$ such that $g^{-1} H_1 g = H_2$.)

**IMC 2021 P6.** For a prime number $p$, let $\mathrm{GL}_2(\mathbb{Z}/p\mathbb{Z})$ be the group of invertible $2 \times 2$ matrices of residues modulo $p$, and let $S_p$ be the symmetric group (the group of all permutations) on $p$ elements. Show that there is no injective group homomorphism

$$
\varphi : \mathrm{GL}_2(\mathbb{Z}/p\mathbb{Z}) \to S_p.
$$

**IMC 2024 P4.** Let $g$ and $h$ be two distinct elements of a group $G$, and let $n$ be a positive integer. Consider a sequence $w = (w_1, w_2, \ldots)$ which is not eventually periodic and where each $w_i$ is either $g$ or $h$. Denote by $H$ the subgroup of $G$ generated by all elements of the form

$$
w_k w_{k+1} \cdots w_{k+n-1} \quad \text{with } k \geq 1.
$$

Prove that $H$ does not depend on the choice of the sequence $w$ (but may depend on $n$).

