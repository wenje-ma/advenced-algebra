# week20

> **Definition 6.1.1 (Quadratic Form)**
> 
> A homogeneous quadratic polynomial in $n$ variables $x_{1},x_{2},\cdots,x_{n}$ with coefficients in a number field $K$ is called an $n$-variable quadratic form over $K$.

> **Definition 6.1.2 (Canonical Form)**
> 
> The canonical form of a real quadratic form $X^{\top}AX$ is

> **Theorem 6.1.3 (Canonical Form of a Quadratic Form)**
> 
> Every quadratic form over a number field $K$ is equivalent to a quadratic form containing only square terms.

> **Definition 6.2.1 (Positive Index of Inertia)**
> 
> In the canonical form of a real quadratic form $X^{\top}AX$, the number $p$ of square terms with coefficient $+1$ is called the positive index of inertia of $X^{\top}AX$, and the number $r-p$ of square terms with coefficient $-1$ is called its negative index of inertia.

> **Theorem 6.2.1 (Law of Inertia)**
> 
> The canonical form of an $n$-variable real quadratic form $X^{\top}AX$ is unique.

> **Corollary 6.2.4 (Necessary and Sufficient Condition for Congruence)**
> 
> Two $n\times{n}$ real symmetric matrices are congruent if and only if they have the same rank and the same positive index of inertia.

> **Definition 7.2.1 (Divisibility)**
> 
> Let $f\left(x\right),g\left(x\right)\in{K}\left[x\right]$. If there exists $h\left(x\right)\in{K}\left[x\right]$ such that $f\left(x\right)=h\left(x\right)g\left(x\right)$, then $g\left(x\right)$ divides $f\left(x\right)$, written $g\left(x\right)\mid{f}\left(x\right)$.

> **Theorem 7.2.1 (Division with Remainder)**
> 
> In $K\left[x\right]$, for any two polynomials $f\left(x\right),g\left(x\right)$ with $g\left(x\right)\ne0$, there exists a unique pair of polynomials $h\left(x\right),r\left(x\right)$ such that

$$
f\left(x\right)=h\left(x\right)g\left(x\right)+r\left(x\right),\deg{r}\left(x\right)<\deg{g}\left(x\right).
$$

## 6.1-8(1)

Use the method of paired elementary row and column operations to reduce the following quadratic form over a number field $K$ to canonical form, and write down the nondegenerate linear substitution:

$$
f\left(x_{1},x_{2},x_{3}\right)=x_{1}^{2}-2x_{2}^{2}+x_{3}^{2}-2x_{1}x_{3}+4x_{2}x_{3}.
$$

### Solution to 6.1-8(1)

Complete the squares:

$$
f
=x_{1}^{2}-2x_{1}x_{3}+x_{3}^{2}-2x_{2}^{2}+4x_{2}x_{3}=\left(x_{1}-x_{3}\right)^{2}-2x_{2}^{2}+4x_{2}x_{3}=\left(x_{1}-x_{3}\right)^{2}-2\left(x_{2}^{2}-2x_{2}x_{3}\right)=\left(x_{1}-x_{3}\right)^{2}-2\left(x_{2}-x_{3}\right)^{2}+2x_{3}^{2}.
$$

Set

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

The nondegenerate linear substitution is $X=CY$, where

$$
C=\left[\begin{array}{rrr}
1&0&1\\
0&1&1\\
0&0&1
\end{array}\right].
$$

$\blacksquare$

## 6.1-11

Let the eigenvalues of an $n\times{n}$ real symmetric matrix $A$ be ordered as $\lambda_{1}\ge\lambda_{2}\ge\cdots\ge\lambda_{n}$. Prove: for every nonzero column vector $\alpha$ in $\mathbb{R}^{n}$,

$$
\lambda_{1}\ge\frac{\alpha^{\top}A\alpha}{\alpha^{\top}\alpha}\ge\lambda_{n}.
$$

### Solution to 6.1-11

Since $A$ is real symmetric, there is an orthogonal matrix $T$ such that

$$
T^{\top}AT=\operatorname{diag}\left\{\lambda_{1},\lambda_{2},\cdots,\lambda_{n}\right\}.
$$

Set $\alpha=T\beta$; then

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

Since $\alpha\ne0$, $\alpha^{\top}\alpha>0$.

Divide by $\alpha^{\top}\alpha$:

$$
\lambda_{1}\ge\frac{\alpha^{\top}A\alpha}{\alpha^{\top}\alpha}\ge\lambda_{n}.
$$

$\blacksquare$

## 6.2-1

Further reduce the canonical forms of all real quadratic forms in Exercise 6.1, problem 3, to their canonical form, and write down the nondegenerate linear substitutions.

### Solution to 6.2-1

By **Theorem 6.2.1 (Law of Inertia)**, the canonical form of an $n$-variable real quadratic form $X^{\top}AX$ is unique.

**Exercise 6.1, problem 3(1)**:

$$
f=x_{1}^{2}+2x_{2}^{2}+2x_{1}x_{2}-2x_{1}x_{3}.
$$

Canonical form: $f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}$.

Reduce to the canonical form: set $z_{3}=\sqrt{2}y_{3}$; then

$$
f=z_{1}^{2}+z_{2}^{2}-z_{3}^{2}.
$$

Nondegenerate linear substitution: $z_{1}=y_{1}$, $z_{2}=y_{2}$, $z_{3}=\sqrt{2}y_{3}$.

**Exercise 6.1, problem 3(2)**:

$$
f=x_{1}^{2}-x_{2}^{2}+2x_{1}x_{3}+2x_{2}x_{3}.
$$

Reduce to the canonical form.

**Exercise 6.1, problem 3(3)**: $f=x_{1}x_{2}+x_{1}x_{3}+x_{2}x_{3}$.

Reduce to the canonical form.

**Exercise 6.1, problem 3(4)**: $f=2x_{1}x_{2}-2x_{3}x_{4}$.

Reduce to the canonical form.

All these canonical forms are unique. $\blacksquare$

## 6.2-4

Let $X^{\top}AX$ be an $n$-variable real quadratic form. Prove: if there are column vectors $\alpha_{1},\alpha_{2}$ in $\mathbb{R}^{n}$ such that $\alpha_{1}^{\top}A\alpha_{1}>0$ and $\alpha_{2}^{\top}A\alpha_{2}<0$, then there is a nonzero column vector $\alpha$ in $\mathbb{R}^{n}$ such that $\alpha^{\top}A\alpha=0$.

### Solution to 6.2-4

By **Definition 6.2.1 (Positive Index of Inertia)**, let $X^{\top}AX$ be an $n$-variable real quadratic form. Consider the function

$$
g\left(t\right)=\left(\alpha_{1}+t\alpha_{2}\right)^{\top}A\left(\alpha_{1}+t\alpha_{2}\right).
$$

Expanding:

$$
g\left(t\right)=\alpha_{1}^{\top}A\alpha_{1}+2t\alpha_{1}^{\top}A\alpha_{2}+t^{2}\alpha_{2}^{\top}A\alpha_{2}.
$$

This is a quadratic function in $t$.

We are given $g\left(0\right)=\alpha_{1}^{\top}A\alpha_{1}>0$.

Since $\alpha_{2}^{\top}A\alpha_{2}<0$, as $t\to\infty$, $g\left(t\right)\to-\infty$.

Hence there is $t_{0}>0$ such that $g\left(t_{0}\right)<0$.

By the intermediate value theorem for continuous functions, there is $t_{1}\in\left(0,t_{0}\right)$ such that $g\left(t_{1}\right)=0$.

Set $\alpha=\alpha_{1}+t_{1}\alpha_{2}$.

Then $\alpha\ne0$ (because if $\alpha=0$, then $\alpha_{1}=-t_{1}\alpha_{2}$, and hence $\alpha_{1}^{\top}A\alpha_{1}=t_{1}^{2}\alpha_{2}^{\top}A\alpha_{2}<0$, a contradiction).

And $\alpha^{\top}A\alpha=g\left(t_{1}\right)=0$.

Therefore there is a nonzero column vector $\alpha$ in $\mathbb{R}^{n}$ such that $\alpha^{\top}A\alpha=0$. $\blacksquare$

## 6.2-6

Prove: an $n$-variable real quadratic form can be factored into the product of two homogeneous linear polynomials with real coefficients if and only if its rank is $2$ with signature $0$, or its rank is $1$.

### Solution to 6.2-6

Sufficiency.

If the rank is $2$ with signature $0$, the canonical form is

$$
y_{1}^{2}-y_{2}^{2}=\left(y_{1}+y_{2}\right)\left(y_{1}-y_{2}\right).
$$

This is the product of two homogeneous linear polynomials.

If the rank is $1$, the canonical form is $y_{1}^{2}=y_{1}\cdot{y}_{1}$.

This is also the product of two homogeneous linear polynomials.

Necessity.

Suppose

$$
X^{\top}AX=\left(a_{1}x_{1}+\cdots+a_{n}x_{n}\right)\left(b_{1}x_{1}+\cdots+b_{n}x_{n}\right).
$$

Set $\alpha=\left(a_{1},\cdots,a_{n}\right)^{\top}$, $\beta=\left(b_{1},\cdots,b_{n}\right)^{\top}$.

Then

$$
X^{\top}AX=\left(\alpha^{\top}X\right)\left(\beta^{\top}X\right)=X^{\top}\left(\frac{\alpha\beta^{\top}+\beta\alpha^{\top}}{2}\right)X.
$$

Therefore

$$
A=\frac{\alpha\beta^{\top}+\beta\alpha^{\top}}{2}.
$$

Case 1: $\alpha$ and $\beta$ are linearly dependent.

Set $\beta=k\alpha$. Then

$$
A=\frac{\alpha\cdot{k}\alpha^{\top}+k\alpha\cdot\alpha^{\top}}{2}=k\alpha\alpha^{\top}.
$$

Hence $\operatorname{rank}\left(A\right)=1$.

Case 2: $\alpha$ and $\beta$ are linearly independent.

Set

$$
\gamma_{1}=\frac{\alpha+\beta}{2},\gamma_{2}=\frac{\alpha-\beta}{2}.
$$

Then

$$
A=\gamma_{1}\gamma_{1}^{\top}-\gamma_{2}\gamma_{2}^{\top}.
$$

Since $\gamma_{1},\gamma_{2}$ are linearly independent, $\operatorname{rank}\left(A\right)=2$.

The positive index of inertia is $1$ and the negative index is $1$, so the signature is $0$.

Therefore the rank is $2$ with signature $0$.

$\blacksquare$

## 6.2-7

Prove: a complex $n$-variable quadratic form $X^{\top}AX$ can, by a nondegenerate linear substitution, be reduced to the canonical form

$$
z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2},
$$

where $r$ is the rank of $X^{\top}AX$. This canonical form contains only square terms with coefficient $1$ or $0$.

### Solution to 6.2-7

Since $A$ is a symmetric matrix over the complex number field, $A$ is congruent to a diagonal matrix

$$
D=\operatorname{diag}\left\{d_{1},d_{2},\cdots,d_{r},0,\cdots,0\right\},
$$

where $d_{i}\ne0$.

Since every nonzero complex number has a square root, there exist $c_{i}\in\mathbb{C}$ such that $c_{i}^{2}=d_{i}$.

Set

$$
C=\operatorname{diag}\left\{\frac{1}{c_{1}},\frac{1}{c_{2}},\cdots,\frac{1}{c_{r}},1,\cdots,1\right\}.
$$

Then

$$
C^{\top}DC=\operatorname{diag}\left\{1,1,\cdots,1,0,\cdots,0\right\}.
$$

Hence $A$ is congruent to $\operatorname{diag}\left\{I_{r},0\right\}$.

That is, there is an invertible matrix $P$ such that $P^{\top}AP=\operatorname{diag}\left\{I_{r},0\right\}$.

Set $X=PZ$; then

$$
X^{\top}AX=Z^{\top}P^{\top}APZ=Z^{\top}\operatorname{diag}\left\{I_{r},0\right\}Z=z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2}.
$$

Therefore the canonical form of the complex quadratic form $X^{\top}AX$ is $z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2}$, where $r$ is its rank. $\blacksquare$

## 7.2-3(2)

Divide $f\left(x\right)$ by $g\left(x\right)$ and find the quotient and remainder:

$$
f\left(x\right)=x^{4}+x^{3}-2x+3,\quad{g}\left(x\right)=3x^{2}-x+2.
$$

### Solution to 7.2-3(2)

By **Theorem 7.2.1 (Division with Remainder)**, perform polynomial long division:

$$
f\left(x\right)=x^{4}+x^{3}+0x^{2}-2x+3.
$$

Leading term of the quotient: $x^{4}/3x^{2}=\frac{1}{3}x^{2}$.

$$
\frac{1}{3}x^{2}\cdot{g}\left(x\right)=x^{4}-\frac{1}{3}x^{3}+\frac{2}{3}x^{2}.
$$

Remainder:

$$
f-\frac{1}{3}x^{2}g=\frac{4}{3}x^{3}-\frac{2}{3}x^{2}-2x+3.
$$

Second term of the quotient: $\frac{4}{3}x^{3}/3x^{2}=\frac{4}{9}x$.

$$
\frac{4}{9}x\cdot{g}=\frac{4}{3}x^{3}-\frac{4}{9}x^{2}+\frac{8}{9}x.
$$

Remainder:

$$
-\frac{2}{9}x^{2}-\frac{26}{9}x+3.
$$

Third term of the quotient: $-\frac{2}{9}x^{2}/3x^{2}=-\frac{2}{27}$.

$$
-\frac{2}{27}\cdot{g}=-\frac{2}{9}x^{2}+\frac{2}{27}x-\frac{4}{27}.
$$

Remainder:

$$
-\frac{80}{27}x+\frac{85}{27}.
$$

Therefore, by **Theorem 7.2.1 (Division with Remainder)**,

$$
\text{quotient~}h\left(x\right)=\frac{1}{3}x^{2}+\frac{4}{9}x-\frac{2}{27}.
$$

$$
\text{remainder~}r\left(x\right)=-\frac{80}{27}x+\frac{85}{27}.
$$

$\blacksquare$
