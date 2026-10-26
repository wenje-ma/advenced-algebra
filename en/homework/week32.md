# Assignment 32

> **Definition 1** (Quadratic Form)<br>A homogeneous quadratic polynomial in $n$ variables $x_{1},x_{2},\cdots,x_{n}$ with coefficients in a number field $K$ is called an $n$-ary quadratic form over $K$.

> **Theorem 3** (Canonical Form of a Quadratic Form)<br>Any quadratic form over a number field $K$ is equivalent to a quadratic form containing only squared terms.

> **Definition 1** (Normal Form)<br>The normal form of a real quadratic form $X^{T}AX$ is
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

(Problem 6.1-5) Let $A$ be an matrix of order $n$ over a number field $K$. Prove: $A$ is skew-symmetric if and only if $\alpha^{T}A\alpha=0$ for every column vector $\alpha$ in $K^{n}$.

### Solution to Problem 2

By **Definition 1** (Quadratic Form), $A$ is an matrix of order $n$ over a number field $K$.

**Necessity**. If $A$ is skew-symmetric, i.e. $A^{T}=-A$.

Then $\alpha^{T}A\alpha$ is a scalar, and its transpose equals itself:

$$
\left(\alpha^{T}A\alpha\right)^{T}=\alpha^{T}A^{T}\alpha=\alpha^{T}\left(-A\right)\alpha=-\alpha^{T}A\alpha.
$$

But $\left(\alpha^{T}A\alpha\right)^{T}=\alpha^{T}A\alpha$ (since it is a scalar).

Therefore

$$
\alpha^{T}A\alpha=-\alpha^{T}A\alpha,
$$

i.e. $2\alpha^{T}A\alpha=0$, and hence $\alpha^{T}A\alpha=0$.

**Sufficiency**. If for every column vector $\alpha$, $\alpha^{T}A\alpha=0$.

We want to prove that $A$ is skew-symmetric, i.e. $A^{T}=-A$, i.e. $A+A^{T}=0$.

Since $\left(A+A^{T}\right)$ is a symmetric matrix.

For every column vector $\alpha$,

$$
\alpha^{T}\left(A+A^{T}\right)\alpha=\alpha^{T}A\alpha+\alpha^{T}A^{T}\alpha=0+\left(\alpha^{T}A\alpha\right)^{T}=0+0=0.
$$

That is, for every column vector $\alpha$, $\alpha^{T}\left(A+A^{T}\right)\alpha=0$.

Since $\left(A+A^{T}\right)$ is a symmetric matrix and $\alpha^{T}\left(A+A^{T}\right)\alpha=0$ for every column vector $\alpha$,

by the property of symmetric matrices (if a symmetric matrix satisfies $\alpha^{T}A\alpha=0$ for all $\alpha$, then $A=0$), we get $A+A^{T}=0$.

Therefore $A^{T}=-A$, i.e. $A$ is skew-symmetric. $\blacksquare$

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
\lambda_{1}\ge\frac{\alpha^{T}A\alpha}{\alpha^{T}\alpha}\ge\lambda_{n}.
$$

### Solution to Problem 4

Since $A$ is a real symmetric matrix, there exists an orthogonal matrix $T$ such that

$$
T^{T}AT=\operatorname{diag}\left\{\lambda_{1},\lambda_{2},\cdots,\lambda_{n}\right\}.
$$

Let $\alpha=T\beta$. Then

$$
\alpha^{T}\alpha=\beta^{T}T^{T}T\beta=\beta^{T}\beta.
$$

$$
\alpha^{T}A\alpha=\beta^{T}T^{T}AT\beta=\beta^{T}\operatorname{diag}\left\{\lambda_{1},\cdots,\lambda_{n}\right\}\beta=\lambda_{1}\beta_{1}^{2}+\lambda_{2}\beta_{2}^{2}+\cdots+\lambda_{n}\beta_{n}^{2}.
$$

Since $\lambda_{1}\ge\lambda_{2}\ge\cdots\ge\lambda_{n}$,

$$
\lambda_{1}\left(\beta_{1}^{2}+\beta_{2}^{2}+\cdots+\beta_{n}^{2}\right)\ge\lambda_{1}\beta_{1}^{2}+\lambda_{2}\beta_{2}^{2}+\cdots+\lambda_{n}\beta_{n}^{2}\ge\lambda_{n}\left(\beta_{1}^{2}+\beta_{2}^{2}+\cdots+\beta_{n}^{2}\right).
$$

That is,

$$
\lambda_{1}\alpha^{T}\alpha\ge\alpha^{T}A\alpha\ge\lambda_{n}\alpha^{T}\alpha.
$$

Since $\alpha\ne0$, we have $\alpha^{T}\alpha> 0$.

Divide both sides by $\alpha^{T}\alpha$:

$$
\lambda_{1}\ge\frac{\alpha^{T}A\alpha}{\alpha^{T}\alpha}\ge\lambda_{n}.
$$

$\blacksquare$
