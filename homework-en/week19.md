# week19

> **Theorem 5.6.1 (Necessary and Sufficient Condition for Diagonalizability)**
> 
> An $n\times{n}$ matrix $A$ over a number field $K$ is diagonalizable if and only if $A$ has $n$ linearly independent eigenvectors.

> **Corollary 5.6.6 (Distinct Eigenvalues Imply Diagonalizability)**
> 
> If an $n\times{n}$ matrix $A$ over a number field $K$ has $n$ distinct eigenvalues, then $A$ is diagonalizable.

$$
\beta_{i}=\alpha_{i}-\sum_{k=1}^{i-1}\frac{\left(\alpha_{i},\beta_{k}\right)}{\left(\beta_{k},\beta_{k}\right)}\beta_{k}.
$$
Then $\beta_{1},\beta_{2},\cdots,\beta_{m}$ is an orthogonal vector group equivalent to the original one.

> **Theorem 5.7.1 (Eigenvalues of a Real Symmetric Matrix)**
> 
> Every root of the characteristic polynomial of a real symmetric matrix, over the complex number field, is a real number.

> **Theorem 5.7.3 (A Real Symmetric Matrix Is Orthogonally Diagonalizable)**
> 
> For any $n\times{n}$ real symmetric matrix $A$, there exists an $n\times{n}$ orthogonal matrix $T$ such that $T^{-1}AT$ is a diagonal matrix.

> **Definition 6.1.1 (Quadratic Form)**
> 
> A homogeneous quadratic polynomial in $n$ variables $x_{1},x_{2},\cdots,x_{n}$ with coefficients in a number field $K$ is called an $n$-variable quadratic form over $K$.

> **Definition 6.1.2 (Canonical Form)**
> 
> The canonical form of a real quadratic form $X^{\top}AX$ is

$$
z_{1}^{2}+\cdots+z_{p}^{2}-z_{p+1}^{2}-\cdots-z_{r}^{2},
$$
where $p$ is the positive index of inertia and $r$ is the rank of the quadratic form.

> **Theorem 6.1.3 (Canonical Form of a Quadratic Form)**
> 
> Every quadratic form over a number field $K$ is equivalent to a quadratic form containing only square terms.

## 5.6-10

Let $A=\left(a_{ij}\right)$ be an $n\times{n}$ upper triangular matrix over a number field $K$. Prove: if $a_{11}=a_{22}=\cdots=a_{nn}$ and at least one $a_{kl}\ne0$ ( $k<{}l$ ), then $A$ cannot be diagonalized.

### Solution to 5.6-10

Since $A$ is upper triangular, its eigenvalues are exactly the diagonal entries $a_{11},a_{22},\cdots,a_{nn}$.

We are given

$$
a_{11}=a_{22}=\cdots=a_{nn}=\lambda_{0}.
$$

That is, $\lambda_{0}$ is an $n$-fold eigenvalue of $A$ (algebraic multiplicity $n$).

Find the dimension of the eigenspace.

$$
\lambda_{0}I-A=\left[\begin{array}{cccc}
0&-a_{12}&\cdots&-a_{1n}\\
0&0&\cdots&-a_{2n}\\
\vdots&\vdots&\ddots&\vdots\\
0&0&\cdots&0
\end{array}\right].
$$

Since at least one $a_{kl}\ne0$ ( $k<{}l$ ), $\lambda_{0}I-A$ is not the zero matrix.

Therefore $\operatorname{rank}\left(\lambda_{0}I-A\right)\ge1$.

Hence the dimension of the eigenspace is

$$
n-\operatorname{rank}\left(\lambda_{0}I-A\right)\le{n}-1.
$$

That is, the geometric multiplicity $\le{n}-1<{}n=$ the algebraic multiplicity.

Therefore $A$ cannot be diagonalized. $\blacksquare$

## 5.7-1(1)

For the following real symmetric matrix $A$, find an orthogonal matrix $T$ such that $T^{\top}AT$ is diagonal:

$$
A=\left[\begin{array}{rrr}
0&-2&2\\
-2&-3&4\\
2&4&-3
\end{array}\right].
$$

### Solution to 5.7-1(1)

By **Theorem 5.7.3 (A Real Symmetric Matrix Is Orthogonally Diagonalizable)**, there is an orthogonal matrix $T$ such that $T^{\top}AT$ is diagonal. Compute the characteristic polynomial:

$$
\left|\lambda{I}-A\right|=\left|\begin{array}{rrr}
\lambda&2&-2\\
2&\lambda+3&-4\\
-2&-4&\lambda+3
\end{array}\right|=\left(\lambda-1\right)^{2}\left(\lambda+8\right).
$$

Thus the eigenvalues are $\lambda_{1}=\lambda_{2}=1$ and $\lambda_{3}=-8$.

Find the eigenvectors for $\lambda=1$.

$$
I-A=\left[\begin{array}{rrr}
1&2&-2\\
2&4&-4\\
-2&-4&4
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1&2&-2\\
0&0&0\\
0&0&0
\end{array}\right].
$$

A fundamental solution system: $\alpha_{1}=\left(-2,1,0\right)^{\top}$, $\alpha_{2}=\left(2,0,1\right)^{\top}$.

By The Schmidt Orthogonalization Process:

$$
\beta_{1}=\alpha_{1}=\left(-2,1,0\right)^{\top}.
$$

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}
=\left(2,0,1\right)^{\top}-\frac{-4}{5}\left(-2,1,0\right)^{\top}
=\left(\frac{2}{5},\frac{4}{5},1\right)^{\top}.
$$

Normalize:

$$
\eta_{1}=\left(-\frac{2}{\sqrt{5}},\frac{1}{\sqrt{5}},0\right)^{\top}.
$$

$$
\eta_{2}=\left(\frac{2}{3\sqrt{5}},\frac{4}{3\sqrt{5}},\frac{\sqrt{5}}{3}\right)^{\top}.
$$

Find the eigenvectors for $\lambda=-8$.

$$
-8I-A=\left[\begin{array}{rrr}
-8&2&-2\\
2&-5&-4\\
-2&-4&-5
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1&0&1/2\\
0&1&1\\
0&0&0
\end{array}\right].
$$

A fundamental solution system: $\alpha_{3}=\left(-1,2,-4\right)^{\top}$.

Normalize:

$$
\eta_{3}=\left(-\frac{1}{\sqrt{21}},\frac{2}{\sqrt{21}},-\frac{4}{\sqrt{21}}\right)^{\top}.
$$

Thus the orthogonal matrix is

$$
T=\left[\begin{array}{ccc}
-2/\sqrt{5}&2/\left(3\sqrt{5}\right)&-1/\sqrt{21}\\
1/\sqrt{5}&4/\left(3\sqrt{5}\right)&2/\sqrt{21}\\
0&\sqrt{5}/3&-4/\sqrt{21}
\end{array}\right].
$$

By **Theorem 5.7.3 (A Real Symmetric Matrix Is Orthogonally Diagonalizable)**,

$$
T^{\top}AT=\operatorname{diag}\left\{1,1,-8\right\}.
$$

$\blacksquare$

## 5.7-1(3)

For the following real symmetric matrix $A$, find an orthogonal matrix $T$ such that $T^{\top}AT$ is diagonal:

$$
A=\left[\begin{array}{rrr}
3&-2&0\\
-2&2&-2\\
0&-2&1
\end{array}\right].
$$

### Solution to 5.7-1(3)

Compute the characteristic polynomial:

$$
\left|\lambda{I}-A\right|=\left|\begin{array}{rrr}
\lambda-3&2&0\\
2&\lambda-2&2\\
0&2&\lambda-1
\end{array}\right|=\left(\lambda+1\right)\left(\lambda-2\right)\left(\lambda-5\right).
$$

Thus the eigenvalues are $\lambda_{1}=-1$, $\lambda_{2}=2$ and $\lambda_{3}=5$.

Find the eigenvectors for $\lambda=-1$.

A fundamental solution system: $\alpha_{1}=\left(1,2,2\right)^{\top}$.

Find the eigenvectors for $\lambda=2$.

A fundamental solution system: $\alpha_{2}=\left(2,1,-2\right)^{\top}$.

Find the eigenvectors for $\lambda=5$.

A fundamental solution system: $\alpha_{3}=\left(-2,2,-1\right)^{\top}$.

Verify orthogonality: $\left(\alpha_{1},\alpha_{2}\right)=0$, $\left(\alpha_{1},\alpha_{3}\right)=0$, $\left(\alpha_{2},\alpha_{3}\right)=0$.

Normalize:

$$
\eta_{1}=\left(\frac{1}{3},\frac{2}{3},\frac{2}{3}\right)^{\top}.
$$

$$
\eta_{2}=\left(\frac{2}{3},\frac{1}{3},-\frac{2}{3}\right)^{\top}.
$$

$$
\eta_{3}=\left(-\frac{2}{3},\frac{2}{3},-\frac{1}{3}\right)^{\top}.
$$

Thus the orthogonal matrix is

$$
T=\left[\begin{array}{rrr}
1/3&2/3&-2/3\\
2/3&1/3&2/3\\
2/3&-2/3&-1/3
\end{array}\right].
$$

$$
T^{\top}AT=\operatorname{diag}\left\{-1,2,5\right\}.
$$

$\blacksquare$

## 5.7-2

Prove: if $n\times{n}$ real symmetric matrices $A,B$ have the same characteristic polynomial, then $A$ and $B$ are similar.

### Solution to 5.7-2

Since $A$ is real symmetric, by **Theorem 5.7.3 (A Real Symmetric Matrix Is Orthogonally Diagonalizable)**, $A$ is orthogonally similar to a diagonal matrix $D_{A}$, whose diagonal entries are all eigenvalues of $A$ (with multiplicity).

Similarly, $B$ is orthogonally similar to a diagonal matrix $D_{B}$, whose diagonal entries are all eigenvalues of $B$ (with multiplicity).

Since $A,B$ have the same characteristic polynomial, they have the same eigenvalues (with multiplicity).

Hence the diagonal entries of $D_{A}$ and $D_{B}$ agree (up to order).

By permuting the diagonal entries of $D_{B}$, we can make $D_{A}=D_{B}$.

Permuting the diagonal entries amounts to a similarity transformation by an orthogonal matrix $Q$: $Q^{\top}D_{B}Q=D_{A}$.

Therefore

$$
A\sim{D}_{A}=D_{B}\sim{B}.
$$

Hence $A$ and $B$ are similar. $\blacksquare$

## 5.7-3

Prove: if a real matrix $A$ is orthogonally similar to a diagonal matrix, then $A$ must be symmetric.

### Solution to 5.7-3

Suppose $A$ is orthogonally similar to a diagonal matrix $D$, i.e. there is an orthogonal matrix $T$ such that

$$
T^{\top}AT=D.
$$

Then

$$
A=TDT^{\top}.
$$

Since $D$ is diagonal, $D^{\top}=D$.

Therefore

$$
A^{\top}=\left(TDT^{\top}\right)^{\top}=TD^{\top}T^{\top}=TDT^{\top}=A.
$$

Hence $A$ is symmetric. $\blacksquare$

## 6.1-3(1)

Make a nondegenerate linear substitution to reduce the following quadratic form over a number field $K$ to canonical form, and write down the substitution:

$$
f\left(x_{1},x_{2},x_{3}\right)=x_{1}^{2}+2x_{2}^{2}+2x_{1}x_{2}-2x_{1}x_{3}.
$$

### Solution to 6.1-3(1)

By **Theorem 6.1.3 (Canonical Form of a Quadratic Form)**, complete the squares:

$$
f
=x_{1}^{2}+2x_{1}x_{2}-2x_{1}x_{3}+2x_{2}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}-\left(x_{2}-x_{3}\right)^{2}+2x_{2}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}+x_{2}^{2}+2x_{2}x_{3}-x_{3}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}+\left(x_{2}+x_{3}\right)^{2}-2x_{3}^{2}.
$$

Set

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

The nondegenerate linear substitution is $X=CY$, where

$$
C=\left[\begin{array}{rrr}
1&-1&2\\
0&1&-1\\
0&0&1
\end{array}\right].
$$

$f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}$ is the canonical form. $\blacksquare$

## 6.1-5

Let $A$ be an $n\times{n}$ matrix over a number field $K$. Prove: $A$ is skew-symmetric if and only if $\alpha^{\top}A\alpha=0$ for every column vector $\alpha$ in $K^{n}$.

### Solution to 6.1-5

By **Definition 6.1.1 (Quadratic Form)**, $A$ is an $n\times{n}$ matrix over a number field $K$.

Necessity. If $A$ is skew-symmetric, i.e. $A^{\top}=-A$.

Then $\alpha^{\top}A\alpha$ is a scalar, and its transpose equals itself:

$$
\left(\alpha^{\top}A\alpha\right)^{\top}=\alpha^{\top}A^{\top}\alpha=\alpha^{\top}\left(-A\right)\alpha=-\alpha^{\top}A\alpha.
$$

But $\left(\alpha^{\top}A\alpha\right)^{\top}=\alpha^{\top}A\alpha$ (because it is a scalar).

Therefore

$$
\alpha^{\top}A\alpha=-\alpha^{\top}A\alpha,
$$

i.e. $2\alpha^{\top}A\alpha=0$, and hence $\alpha^{\top}A\alpha=0$.

Sufficiency. Suppose $\alpha^{\top}A\alpha=0$ for every column vector $\alpha$.

We prove $A$ is skew-symmetric, i.e. $A^{\top}=-A$, i.e. $A+A^{\top}=0$.

Since $\left(A+A^{\top}\right)$ is symmetric.

For every column vector $\alpha$,

$$
\alpha^{\top}\left(A+A^{\top}\right)\alpha=\alpha^{\top}A\alpha+\alpha^{\top}A^{\top}\alpha=0+\left(\alpha^{\top}A\alpha\right)^{\top}=0+0=0.
$$

That is, for every column vector $\alpha$, $\alpha^{\top}\left(A+A^{\top}\right)\alpha=0$.

Since $\left(A+A^{\top}\right)$ is symmetric and $\alpha^{\top}\left(A+A^{\top}\right)\alpha=0$ for every $\alpha$, by the property of symmetric matrices (if a symmetric matrix satisfies $\alpha^{\top}A\alpha=0$ for all $\alpha$, then $A=0$), we get $A+A^{\top}=0$.

Therefore $A^{\top}=-A$, i.e. $A$ is skew-symmetric. $\blacksquare$
