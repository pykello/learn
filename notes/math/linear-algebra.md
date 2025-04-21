# Linear Algebra

## 1. Vector Spaces and Subspaces
- **Vector Space:** A set $V$ with two operations (vector addition and scalar multiplication) satisfying the usual axioms (commutativity, associativity, distributivity, etc.). Elements of $V$ (called **vectors**) can be added and scaled by numbers (scalars) from a field (e.g. real or complex numbers). For example, $\mathbb{R}^n$, the set of $n$-tuples of real numbers, is a vector space under componentwise addition and scalar multiplication.  
- **Subspace:** A subset $W \subseteq V$ that is itself a vector space (with the addition and scalar multiplication from $V$). Equivalently, $W$ is **nonempty**, and for any $\mathbf{u}, \mathbf{v}\in W$ and scalar $c$, one has $\mathbf{u}+\mathbf{v}\in W$ and $c\mathbf{u}\in W$. Every subspace must contain the zero vector $\mathbf{0}$. For instance, in $\mathbb{R}^3$, all lines through the origin and planes through the origin are subspaces (but a line not through the origin is not a subspace).
- **Subspace Test:** To quickly determine if $W$ is a subspace of $V$, check that (1) $\mathbf{0}\in W$, (2) $W$ is closed under addition, and (3) $W$ is closed under scalar multiplication. If all hold, $W$ is a subspace.    
- **Intersection of Subspaces:** The intersection $U\cap W$ of two subspaces $U, W \subseteq V$ is also a subspace. (In contrast, the union $U\cup W$ need not be a subspace unless one subspace is contained in the other.)

## 2. Linear Independence, Bases, and Dimension
- **Linear Combination:** Given vectors $\mathbf{v}_1,\dots,\mathbf{v}_k\in V$, a *linear combination* of them is any vector of the form $c_1\mathbf{v}_1+\cdots+c_k\mathbf{v}_k$ with scalars $c_i$.  
- **Linear Independence:** A set of vectors $\{\mathbf{v}_1,\dots,\mathbf{v}_k\}\subseteq V$ is **linearly independent** if the only solution to $c_1\mathbf{v}_1+\cdots+c_k\mathbf{v}_k=\mathbf{0}$ is $c_1=c_2=\cdots=c_k=0$. In other words, no nontrivial linear relation exists among them. If a nonzero combination yields $\mathbf{0}$, the vectors are **dependent**. For example, in $\mathbb{R}^3$, the standard unit vectors $e_1=(1,0,0), e_2=(0,1,0), e_3=(0,0,1)$ are linearly independent, whereas $\{(1,2,3), (2,4,6)\}$ is dependent because $2*(1,2,3) - (2,4,6) = \mathbf{0}$.  
- **Span and Generating Set:** The set of all linear combinations of $\{\mathbf{v}_1,\dots,\mathbf{v}_k\}$ is their **span**. If $\mathrm{span}\{\mathbf{v}_1,\dots,\mathbf{v}_k\} = V$, we say $\{\mathbf{v}_1,\dots,\mathbf{v}_k\}$ **spans** $V$ or is a **generating set** for $V$.  
- **Basis:** A set of vectors $B=\{\mathbf{b}_1,\dots,\mathbf{b}_n\}$ in $V$ is a **basis** if: (1) $B$ spans $V$, and (2) $B$ is linearly independent. Equivalently, each $\mathbf{v}\in V$ can be expressed *uniquely* as a combination of basis vectors. A basis is a “just large enough” set of vectors to span the space without any redundancy. For instance, $\{e_1,e_2,e_3\}$ is a basis for $\mathbb{R}^3$.  
- **Dimension:** If $V$ is spanned by $n$ vectors but no fewer, then $\dim(V)=n$. Equivalently, the dimension is the number of vectors in any basis of $V$. (This is well-defined: a key theorem states all bases of a finite-dimensional space have the same number of elements.) We say $V$ is *finite-dimensional* if it has a finite basis.

### Core Theorems and Properties  
- **Uniqueness of Basis Size (Dimension Theorem):** In a finite-dimensional space $V$, any two bases contain the same number of vectors. This number is $\dim(V)$. For example, any basis of $\mathbb{R}^5$ has 5 vectors.  
- **Extension and Reduction Lemmas:** (i) Any linearly independent set of vectors in a finite-dimensional $V$ can be *extended* to a full basis of $V$. (ii) Any spanning set of $V$ can be *reduced* to a basis by discarding dependent vectors. These results ensure bases exist and help construct them in practice.  
- **In $\mathbb{R}^n$:** Any set of more than $n$ vectors in $\mathbb{R}^n$ is automatically linearly dependent (pigeonhole principle for dimensions). Conversely, any set of $n$ linearly independent vectors in $\mathbb{R}^n$ is a basis (because it must span $\mathbb{R}^n$). For example, in $\mathbb{R}^3$, 4 vectors can’t be independent, and 3 independent vectors must form a basis.  
- **Coordinates:** If $B=\{\mathbf{b}_1,\dots,\mathbf{b}_n\}$ is a basis for $V$, every vector $\mathbf{v}\in V$ can be written uniquely as $\mathbf{v}=x_1\mathbf{b}_1+\cdots+x_n\mathbf{b}_n$. The scalars $(x_1,\dots,x_n)$ are the **coordinates** of $\mathbf{v}$ relative to $B$. This is very useful in problem solving—one can work with coordinates instead of vectors.

[TODO]

## Problems

1. Let $A$ be a real $n\times n$ skew‑symmetric matrix ($A^T=-A$). Show that $\det(A)\ge0$.

2. Let $A$ be a real $n\times n$ matrix satisfying $A^3=A+I_n$. Show that $\det(A)>0$.

3. If $A$ and $B$ are real $n\times n$ matrices with $AB=BA$, prove that $\det\bigl(A^2+B^2\bigr)\ge0$.

4. Let $A,B\in M_2(\Bbb R)$ commute and satisfy $\det\bigl(A^2+B^2\bigr)=0$. Prove $\det(A)=\det(B)$.

5. Let $A\in M_2(\Bbb R)$ with $\det(A)=-1$. Show $\det\bigl(A^2+I_2\bigr)\ge4$, and determine when equality holds.

6. Let $A,B\in M_3(\Bbb C)$ with $\det(A)=\det(B)=1$. Prove $\det\bigl(A+\sqrt2\,B\bigr)\neq0$.

7. Let $A,B\in M_2(\Bbb R)$. Show $\det\bigl((AB+BA)^4+(AB-BA)^4\bigr)\ge0$.

8. Let $A\in M_2(\Bbb C)$ not a scalar matrix. Prove any $X$ with $AX=XA$ has the form $X=\alpha A+\beta I_2$.

9. Let $A,B,C\in M_2(\Bbb C)$ commute with $C$ but $AB\neq BA$. Prove $C$ is a scalar matrix.

10. Let $A\in M_n(\Bbb R)$ be orthogonal ($A^TA=I_n$). (a) Prove $|\text{tr}(A)|\le n$. (b) If $n$ is odd, show $\det(A^2-I_n)=0$.

11. Define $f(X)=X^n$ on $M_2(\Bbb C)$ for $n\ge2$. Show $f$ is neither injective nor surjective.

12. Let $A\in M_2(\Bbb R)$ with $\text{tr}(A)>2$. Show $A^n\neq I_2$ for all $n\ge1$.

13. (a) If $A\in M_3(\Bbb C)$ and $A^2=0$, show $\text{tr}(A)=0$.  
    (b) If $\text{tr}(A)=\text{tr}(A^2)=0$, show $\det(A)=0$.

14. Show that for each $n\ge1$, $X^n=I_2$ has at least $n$ distinct solutions in $M_2(\Bbb R)$.

15. Let $A,B\in M_2(\Bbb R)$ commute. If $\det\bigl(A^{2n}+B^{2n}\bigr)=0$ for some $n>0$, prove $A,B$ are either both invertible or both singular.

16. Let $A,B\in M_2(\Bbb R)$ satisfy $A^2+B^2=2AB$. Prove $AB=BA$ and $\text{tr}(A)=\text{tr}(B)$.

17. Let $A,B,C\in M_3(\Bbb C)$ commute pairwise and satisfy $A^3=B^3=C^3=0$. Prove $ABC=0$.

18. If $A,B$ are same‑size complex matrices with $\text{rank}(AB-BA)=1$, show $(AB-BA)^2=0$.

19. Let $A\neq B\in M_n(\Bbb R)$ satisfy $A^3=B^3$ and $A^2B=AB^2$. Can $A^2+B^2$ be invertible?

20. If $A,B\in M_n(\Bbb R)$ satisfy $(AB)^2=0$, show $(BA)^2=0$.

21. Let $A,B\in M_n(\Bbb R)$ be orthogonal with $n$ odd. Show at least one of $A+B$ or $A-B$ is singular.

22. Let $A\in M_2(\Bbb Z)$ satisfy $A^n=I_2$ for some $n$ with $\gcd(n,6)=1$. Show $A=I_2$.

23. If $A\in M_3(\Bbb Q)$ satisfies $A^8=I_3$, show $A^4=I_3$.

24. Let $A\in M_n(\Bbb R)$ with $|\text{tr}(A)|>n$. Show $A^k\neq A^p$ for all $k\neq p\ge0$.

25. Let $A$ be $n\times n$ real. Prove $\text{tr}(A^k)=0$ for $1\le k\le n$ iff $A^n=0$.

26. (a) Can $(AB-BA)^2=I_3$? (b) Can $(AB-BA)^{1993}=I_3$?

27. For $A_1,\dots,A_k\in M_n(\Bbb R)$ show $\det\bigl(\sum A_i^TA_i\bigr)\ge0$.

28. If $B^2=0$ in $M_n(\Bbb R)$, prove $\det(AB+BA+I_n)\ge0$.

29. Find all real polynomials $P$ such that $A\neq B\implies P(A)\neq P(B)$ on $M_2(\Bbb R)$.

30. If $\det A=\det B=\det C$ and $\det(A+iB)=\det(C+iA)$, prove $\det(A+B)=\det(C+A)$.

31. Let $r,s$ be odd primes and $A,B$ commute with $A^r=I$, $B^s=I$. Show $A+B$ is invertible.

32. If $A,C$ are invertible and $A^kB=C^kD$ for all $k\ge1$, prove $B=D$.

33. Let $A,B\in M_2(\Bbb R)$ have positive entries. Show $(AB)^2=(BA)^2\iff AB=BA$.

34. Prove $\det(A^2+B^2)\ge\det(AB-BA)$ for $A,B\in M_2(\Bbb R)$.

35. If $A\in M_3(\Bbb R)$ has $\text{tr}(A)=\text{tr}(A^2)=0$, show $\det(A^2+I_3)=(\det A)^2+1$.

36. Prove no real $A,B\in M_n$ satisfy $AB-BA=I_n$.

37. Let $n$ odd and $A,B\in M_n(\Bbb C)$ satisfy $A^2+B^2=I_n$. Prove $\det(AB-BA)\ge0$.
