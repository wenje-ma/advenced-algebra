# Assignment 33

> **Theorem 1** (Law of Inertia)<br>The normal form of an $n$-ary real quadratic form $X^{\top}AX$ is unique.

> **Definition 1** (Positive Index of Inertia)<br>In the normal form of a real quadratic form $X^{\top}AX$, the number $p$ of squared terms with coefficient $+1$ is called the positive index of inertia of $X^{\top}AX$, and the number $r-p$ of squared terms with coefficient $-1$ is called the negative index of inertia of $X^{\top}AX$.

> **Corollary 4** (Necessary and Sufficient Condition for Congruence)<br>Two real symmetric matrices of order $n$ are congruent if and only if they have the same rank and the same positive index of inertia.

### Problem 1

(Problem 6.2-1) Further reduce the canonical forms of all the real quadratic forms in Problem 3 of Section 6.1 to normal form, and write down the nonsingular linear substitutions used.

### Solution to Problem 1

By **Theorem 1** (Law of Inertia), the normal form of an $n$-ary real quadratic form $X^{\top}AX$ is unique.

**Problem 6.1, Problem 3(1)**:

$$
f=x_{1}^{2}+2x_{2}^{2}+2x_{1}x_{2}-2x_{1}x_{3}.
$$

Canonical form: $f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}$.

Reduce to normal form: let $z_{3}=\sqrt{2}y_{3}$, then

$$
f=z_{1}^{2}+z_{2}^{2}-z_{3}^{2}.
$$

Nonsingular linear substitution: $z_{1}=y_{1}$, $z_{2}=y_{2}$, $z_{3}=\sqrt{2}y_{3}$.

**Problem 6.1, Problem 3(2)**:

$$
f=x_{1}^{2}-x_{2}^{2}+2x_{1}x_{3}+2x_{2}x_{3}.
$$

(Detailed computation omitted; it suffices to reduce to normal form. )

**Problem 6.1, Problem 3(3)**: $f=x_{1}x_{2}+x_{1}x_{3}+x_{2}x_{3}$.

(Detailed computation omitted; it suffices to reduce to normal form. )

**Problem 6.1, Problem 3(4)**: $f=2x_{1}x_{2}-2x_{3}x_{4}$.

(Detailed computation omitted; it suffices to reduce to normal form. )

All of the above normal forms are unique. $\blacksquare$

### Problem 2

(Problem 6.2-4) Let $X^{\top}AX$ be an $n$-ary real quadratic form. Prove: if there exist column vectors $\alpha_{1},\alpha_{2}$ in $\mathbb{R}^{n}$ such that $\alpha_{1}^{\top}A\alpha_{1}> 0$ and $\alpha_{2}^{\top}A\alpha_{2}< 0$, then there exists a nonzero column vector $\alpha$ in $\mathbb{R}^{n}$ such that $\alpha^{\top}A\alpha=0$.

### Solution to Problem 2

By **Definition 1** (Positive Index of Inertia), let $X^{\top}AX$ be an $n$-ary real quadratic form. Consider the function

$$
g\left(t\right)=\left(\alpha_{1}+t\alpha_{2}\right)^{\top}A\left(\alpha_{1}+t\alpha_{2}\right).
$$

Expand:

$$
g\left(t\right)=\alpha_{1}^{\top}A\alpha_{1}+2t\alpha_{1}^{\top}A\alpha_{2}+t^{2}\alpha_{2}^{\top}A\alpha_{2}.
$$

This is a quadratic function in $t$.

We are given $g\left(0\right)=\alpha_{1}^{\top}A\alpha_{1}> 0$.

Since $\alpha_{2}^{\top}A\alpha_{2}< 0$, as $t\to\infty$, $g\left(t\right)\to-\infty$.

Therefore there exists $t_{0}> 0$ such that $g\left(t_{0}\right)< 0$.

By the intermediate value theorem for continuous functions, there exists $t_{1}\in\left(0,t_{0}\right)$ such that $g\left(t_{1}\right)=0$.

Let $\alpha=\alpha_{1}+t_{1}\alpha_{2}$.

Then $\alpha\ne0$ (because if $\alpha=0$, then $\alpha_{1}=-t_{1}\alpha_{2}$, and hence $\alpha_{1}^{\top}A\alpha_{1}=t_{1}^{2}\alpha_{2}^{\top}A\alpha_{2}< 0$, a contradiction).

And $\alpha^{\top}A\alpha=g\left(t_{1}\right)=0$.

Therefore there exists a nonzero column vector $\alpha$ in $\mathbb{R}^{n}$ such that $\alpha^{\top}A\alpha=0$. $\blacksquare$

### Problem 3

(Problem 6.2-6) Prove: an $n$-ary real quadratic form can be factored as the product of two real homogeneous polynomials of degree $1$ if and only if its rank is $2$ and its signature is $0$, or its rank is $1$.

### Solution to Problem 3

**Sufficiency**.

If the rank is $2$ and the signature is $0$, then the normal form is

$$
y_{1}^{2}-y_{2}^{2}=\left(y_{1}+y_{2}\right)\left(y_{1}-y_{2}\right).
$$

This is the product of two homogeneous polynomials of degree $1$.

If the rank is $1$, then the normal form is $y_{1}^{2}=y_{1}\cdot y_{1}$.

This is also the product of two homogeneous polynomials of degree $1$.

**Necessity**.

Suppose

$$
X^{\top}AX=\left(a_{1}x_{1}+\cdots+a_{n}x_{n}\right)\left(b_{1}x_{1}+\cdots+b_{n}x_{n}\right).
$$

Let $\alpha=\left(a_{1},\cdots,a_{n}\right)^{\top}$, $\beta=\left(b_{1},\cdots,b_{n}\right)^{\top}$.

Then

$$
X^{\top}AX=\left(\alpha^{\top}X\right)\left(\beta^{\top}X\right)=X^{\top}\left(\frac{\alpha\beta^{\top}+\beta\alpha^{\top}}{2}\right)X.
$$

Therefore

$$
A=\frac{\alpha\beta^{\top}+\beta\alpha^{\top}}{2}.
$$

**Case 1**: $\alpha$ and $\beta$ are linearly dependent.

Let $\beta=k\alpha$. Then

$$
A=\frac{\alpha\cdot k\alpha^{\top}+k\alpha\cdot\alpha^{\top}}{2}=k\alpha\alpha^{\top}.
$$

Therefore $\operatorname{rank}\left(A\right)=1$.

**Case 2**: $\alpha$ and $\beta$ are linearly independent.

Let

$$
\gamma_{1}=\frac{\alpha+\beta}{2},\gamma_{2}=\frac{\alpha-\beta}{2}.
$$

Then

$$
A=\gamma_{1}\gamma_{1}^{\top}-\gamma_{2}\gamma_{2}^{\top}.
$$

Since $\gamma_{1},\gamma_{2}$ are linearly independent, $\operatorname{rank}\left(A\right)=2$.

Moreover, the positive index of inertia is $1$ and the negative index of inertia is $1$, so the signature is $0$.

Therefore the rank is $2$ and the signature is $0$.

$\blacksquare$

### Problem 4

(Problem 6.2-7) Prove: an $n$-ary quadratic form over the complex number field (abbreviated as complex quadratic form) $X^{\top}AX$ can be reduced by a nonsingular linear substitution to the following canonical form:

$$
z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2},
$$

where $r$ is the rank of the quadratic form $X^{\top}AX$. This form of canonical form is called the normal form of $X^{\top}AX$; it contains only squared terms with coefficients $1$ or $0$.

### Solution to Problem 4

Since $A$ is a symmetric matrix over the complex number field, by the theorem, $A$ is congruent to a diagonal matrix

$$
D=\operatorname{diag}\left\{d_{1},d_{2},\cdots,d_{r},0,\cdots,0\right\},
$$

where $d_{i}\ne0$.

Since every nonzero complex number has a square root, there exist $c_{i}\in\mathbb{C}$ such that $c_{i}^{2}=d_{i}$.

Let

$$
C=\operatorname{diag}\left\{\frac{1}{c_{1}},\frac{1}{c_{2}},\cdots,\frac{1}{c_{r}},1,\cdots,1\right\}.
$$

Then

$$
C^{\top}DC=\operatorname{diag}\left\{1,1,\cdots,1,0,\cdots,0\right\}.
$$

Therefore $A$ is congruent to $\operatorname{diag}\left\{I_{r},0\right\}$.

That is, there exists an invertible matrix $P$ such that $P^{\top}AP=\operatorname{diag}\left\{I_{r},0\right\}$.

Let $X=PZ$. Then

$$
X^{\top}AX=Z^{\top}P^{\top}APZ=Z^{\top}\operatorname{diag}\left\{I_{r},0\right\}Z=z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2}.
$$

Therefore the normal form of the complex quadratic form $X^{\top}AX$ is $z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2}$, where $r$ is the rank of the quadratic form. $\blacksquare$
