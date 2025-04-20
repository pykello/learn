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
