# Assignment 32

> **Definition 1** (Quadratic Form)<br>A homogeneous quadratic polynomial in $n$ variables $x_{1},x_{2},\cdots,x_{n}$ with coefficients in a number field $K$ is called an $n$-ary quadratic form over $K$.

> **Theorem 3** (Canonical Form of a Quadratic Form)<br>Any quadratic form over a number field $K$ is equivalent to a quadratic form containing only squared terms.

> **Definition 1** (Normal Form)<br>The normal form of a real quadratic form $X^{\top}AX$ is
> $$
> z_{1}^{2}+\cdots+z_{p}^{2}-z_{p+1}^{2}-\cdots-z_{r}^{2},
> $$
> where $p$ is the positive index of inertia and $r$ is the rank of the quadratic form.

### Problem 1

(Problem 6.1-3(1)) Apply a nonsingular linear substitution to reduce the following quadratic form over a number field $K$ to canonical form, and write down the nonsingular linear substitution used:

$$
f\left(x_{1},x_{2},x_{3}\right)=x_{1}^{2}+2x_{2}^{2}+2x_{1}x_{2}-2x_{1}x_{3}.
$$

### Solution to Problem 1

By **Theorem 3** (Canonical Form of a Quadratic Form), use the method of completing the square:

$$
f
=x_{1}^{2}+2x_{1}x_{2}-2x_{1}x_{3}+2x_{2}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}-\left(x_{2}-x_{3}\right)^{2}+2x_{2}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}+x_{2}^{2}+2x_{2}x_{3}-x_{3}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}+\left(x_{2}+x_{3}\right)^{2}-2x_{3}^{2}.
$$

Let

$$
\begin{cases}
y_{1}=x_{1}+x_{2}-x_{3},\\
y_{2}=x_{2}+x_{3},\\
y_{3}=x_{3}.
\end{cases}
$$

Then

$$
\begin{cases}
x_{1}=y_{1}-y_{2}+2y_{3},\\
x_{2}=y_{2}-y_{3},\\
x_{3}=y_{3}.
\end{cases}
$$

Therefore

$$
f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}.
$$

The nonsingular linear substitution is $X=CY$, where

$$
C=\left[\begin{array}{rrr}
1 & -1 & 2\\
0 & 1 & -1\\
0 & 0 & 1
\end{array}\right].
$$

$f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}$ is the canonical form. $\blacksquare$

### Problem 2

(Problem 6.1-5) Let $A$ be an matrix of order $n$ over a number field $K$. Prove: $A$ is skew-symmetric if and only if $\alpha^{\top}A\alpha=0$ for every column vector $\alpha$ in $K^{n}$.

### Solution to Problem 2

By **Definition 1** (Quadratic Form), $A$ is an matrix of order $n$ over a number field $K$.

**Necessity**. If $A$ is skew-symmetric, i.e. $A^{\top}=-A$.

Then $\alpha^{\top}A\alpha$ is a scalar, and its transpose equals itself:

$$
\left(\alpha^{\top}A\alpha\right)^{\top}=\alpha^{\top}A^{\top}\alpha=\alpha^{\top}\left(-A\right)\alpha=-\alpha^{\top}A\alpha.
$$

But $\left(\alpha^{\top}A\alpha\right)^{\top}=\alpha^{\top}A\alpha$ (since it is a scalar).

Therefore

$$
\alpha^{\top}A\alpha=-\alpha^{\top}A\alpha,
$$

i.e. $2\alpha^{\top}A\alpha=0$, and hence $\alpha^{\top}A\alpha=0$.

**Sufficiency**. If for every column vector $\alpha$, $\alpha^{\top}A\alpha=0$.

We want to prove that $A$ is skew-symmetric, i.e. $A^{\top}=-A$, i.e. $A+A^{\top}=0$.

Since $\left(A+A^{\top}\right)$ is a symmetric matrix.

For every column vector $\alpha$,

$$
\alpha^{\top}\left(A+A^{\top}\right)\alpha=\alpha^{\top}A\alpha+\alpha^{\top}A^{\top}\alpha=0+\left(\alpha^{\top}A\alpha\right)^{\top}=0+0=0.
$$

That is, for every column vector $\alpha$, $\alpha^{\top}\left(A+A^{\top}\right)\alpha=0$.

Since $\left(A+A^{\top}\right)$ is a symmetric matrix and $\alpha^{\top}\left(A+A^{\top}\right)\alpha=0$ for every column vector $\alpha$,

by the property of symmetric matrices (if a symmetric matrix satisfies $\alpha^{\top}A\alpha=0$ for all $\alpha$, then $A=0$), we get $A+A^{\top}=0$.

Therefore $A^{\top}=-A$, i.e. $A$ is skew-symmetric. $\blacksquare$

### Problem 3

(Problem 6.1-8(1)) Use the method of paired elementary row and column operations to reduce the following quadratic form over a number field $K$ to canonical form, and write down the nonsingular linear substitution used:

$$
f\left(x_{1},x_{2},x_{3}\right)=x_{1}^{2}-2x_{2}^{2}+x_{3}^{2}-2x_{1}x_{3}+4x_{2}x_{3}.
$$

### Solution to Problem 3

Use the method of completing the square:

$$
f
=x_{1}^{2}-2x_{1}x_{3}+x_{3}^{2}-2x_{2}^{2}+4x_{2}x_{3}=\left(x_{1}-x_{3}\right)^{2}-2x_{2}^{2}+4x_{2}x_{3}=\left(x_{1}-x_{3}\right)^{2}-2\left(x_{2}^{2}-2x_{2}x_{3}\right)=\left(x_{1}-x_{3}\right)^{2}-2\left(x_{2}-x_{3}\right)^{2}+2x_{3}^{2}.
$$

Let

$$
\begin{cases}
y_{1}=x_{1}-x_{3},\\
y_{2}=x_{2}-x_{3},\\
y_{3}=x_{3}.
\end{cases}
$$

Then

$$
\begin{cases}
x_{1}=y_{1}+y_{3},\\
x_{2}=y_{2}+y_{3},\\
x_{3}=y_{3}.
\end{cases}
$$

Therefore

$$
f=y_{1}^{2}-2y_{2}^{2}+2y_{3}^{2}.
$$

The nonsingular linear substitution is $X=CY$, where

$$
C=\left[\begin{array}{rrr}
1 & 0 & 1\\
0 & 1 & 1\\
0 & 0 & 1
\end{array}\right].
$$

$\blacksquare$

### Problem 4

(Problem 6.1-11) Let all eigenvalues of a real symmetric matrix $A$ of order $n$ be arranged in decreasing order: $\lambda_{1}\ge\lambda_{2}\ge\cdots\ge\lambda_{n}$. Prove: for every column vector $\alpha\ne0$ in $\mathbb{R}^{n}$,

$$
\lambda_{1}\ge\frac{\alpha^{\top}A\alpha}{\alpha^{\top}\alpha}\ge\lambda_{n}.
$$

### Solution to Problem 4

Since $A$ is a real symmetric matrix, there exists an orthogonal matrix $T$ such that

$$
T^{\top}AT=\operatorname{diag}\left\{\lambda_{1},\lambda_{2},\cdots,\lambda_{n}\right\}.
$$

Let $\alpha=T\beta$. Then

$$
\alpha^{\top}\alpha=\beta^{\top}T^{\top}T\beta=\beta^{\top}\beta.
$$

$$
\alpha^{\top}A\alpha=\beta^{\top}T^{\top}AT\beta=\beta^{\top}\operatorname{diag}\left\{\lambda_{1},\cdots,\lambda_{n}\right\}\beta=\lambda_{1}\beta_{1}^{2}+\lambda_{2}\beta_{2}^{2}+\cdots+\lambda_{n}\beta_{n}^{2}.
$$

Since $\lambda_{1}\ge\lambda_{2}\ge\cdots\ge\lambda_{n}$,

$$
\lambda_{1}\left(\beta_{1}^{2}+\beta_{2}^{2}+\cdots+\beta_{n}^{2}\right)\ge\lambda_{1}\beta_{1}^{2}+\lambda_{2}\beta_{2}^{2}+\cdots+\lambda_{n}\beta_{n}^{2}\ge\lambda_{n}\left(\beta_{1}^{2}+\beta_{2}^{2}+\cdots+\beta_{n}^{2}\right).
$$

That is,

$$
\lambda_{1}\alpha^{\top}\alpha\ge\alpha^{\top}A\alpha\ge\lambda_{n}\alpha^{\top}\alpha.
$$

Since $\alpha\ne0$, we have $\alpha^{\top}\alpha> 0$.

Divide both sides by $\alpha^{\top}\alpha$:

$$
\lambda_{1}\ge\frac{\alpha^{\top}A\alpha}{\alpha^{\top}\alpha}\ge\lambda_{n}.
$$

$\blacksquare$
