# Assignment 30

> **Theorem 1** (Necessary and Sufficient Condition for Diagonalizability)<br>An matrix of order $n$ $A$ over a number field $K$ is diagonalizable if and only if $A$ has $n$ linearly independent eigenvectors.

> **Corollary 6** (Diagonalizability with $n$ Distinct Eigenvalues)<br>If an matrix of order $n$ $A$ over a number field $K$ has $n$ distinct eigenvalues, then $A$ is diagonalizable.

### Problem 1

(Problem 5.6-1) In Problems 1 and 2 of Section 5.5, which matrices are diagonalizable and which are not? For each diagonalizable matrix $A$, find an invertible matrix $P$ such that $P^{-1}AP$ is a diagonal matrix, and write down that diagonal matrix.

### Solution to Problem 1

By **Theorem 1** (Necessary and Sufficient Condition for Diagonalizability), an matrix of order $n$ $A$ over a number field $K$ is diagonalizable if and only if $A$ has $n$ linearly independent eigenvectors.

**Problem 5.5, Problem 1(1)**: $A=\left[\begin{array}{rrr}2 & 2 & -2\\2 & 5 & -4\\-2 & -4 & 5\end{array}\right]$.

Eigenvalues: $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=10$.

Find eigenvectors for $\lambda=10$:

$$
10I-A=\left[\begin{array}{rrr}
8 & -2 & 2\\
-2 & 5 & 4\\
2 & 4 & 5
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
2 & 4 & 5\\
0 & 9 & 9\\
0 & 0 & 0
\end{array}\right].
$$

Solving gives $x_{2}=-x_{3}$, $x_{1}=\frac{1}{2}x_{3}$.

A fundamental system of solutions: $\alpha_{1}=\left(1,-2,2\right)^{\top}$.

Eigenvectors for $\lambda=1$:

$$
I-A=\left[\begin{array}{rrr}
-1 & -2 & 2\\
-2 & -4 & 4\\
2 & 4 & -4
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & 2 & -2\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

Solving gives $x_{1}=-2x_{2}+2x_{3}$.

A fundamental system of solutions: $\alpha_{2}=\left(-2,1,0\right)^{\top}$, $\alpha_{3}=\left(2,0,1\right)^{\top}$.

The three eigenvectors are linearly independent, so $A$ is diagonalizable.

$$
P=\left[\begin{array}{rrr}
1 & -2 & 2\\
-2 & 1 & 0\\
2 & 0 & 1
\end{array}\right],
P^{-1}AP=\left[\begin{array}{rrr}
10 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{array}\right].
$$

**Problem 5.5, Problem 1(2)**: $A=\left[\begin{array}{rrr}2 & 3 & 2\\1 & 8 & 2\\-2 & -14 & -3\end{array}\right]$.

Eigenvalues: $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=3$.

The eigenspace for $\lambda=3$ has dimension $1$ (geometric multiplicity), while the algebraic multiplicity is $2$.

Since geometric multiplicity $< $ algebraic multiplicity, $A$ is not diagonalizable.

**Problem 5.5, Problem 1(3)**: $A=\left[\begin{array}{rrr}6 & 2 & 4\\2 & 3 & 2\\4 & 2 & 6\end{array}\right]$.

Eigenvalues: $\lambda_{1}=2$, $\lambda_{2}=11$.

(Detailed computation omitted; it is diagonalizable because it has two distinct eigenvalues, and a matrix of order $3$ then has $3$ linearly independent eigenvectors. )

**Problem 5.5, Problem 1(4)**: $A=\left[\begin{array}{rrr}2 & -1 & 2\\5 & -3 & 3\\-1 & 0 & -2\end{array}\right]$.

Eigenvalue: $\lambda=-1$ (triple root).

Geometric multiplicity $< 3$, so it is not diagonalizable.

**Problem 5.5, Problem 1(5)**: $A=\left[\begin{array}{rrr}0 & 1/2 & 1/2\\1 & -1/2 & 1/2\\1 & -1/2 & 1/2\end{array}\right]$.

Eigenvalues: $\lambda_{1}=0$, $\lambda_{2}=1$, $\lambda_{3}=-1$.

Three distinct eigenvalues, so it is diagonalizable.

**Problem 5.5, Problem 2(1)**: $A=\left[\begin{array}{rr}1 & -\sqrt{3}\\\sqrt{3} & 1\end{array}\right]$.

Regarded as a matrix over the real number field, it has no real eigenvalues, so it is not diagonalizable.

Regarded as a matrix over the complex number field, it has two distinct eigenvalues, so it is diagonalizable.

**Problem 5.5, Problem 2(2)**: $A=\left[\begin{array}{rrr}3 & 7 & -3\\-2 & -5 & 2\\-4 & -10 & 3\end{array}\right]$.

Regarded as a matrix over the real number field, it has only $1$ real eigenvalue, so it is not diagonalizable.

Regarded as a matrix over the complex number field, it has three distinct eigenvalues, so it is diagonalizable.

All of the above judgments are based on whether the matrix has $n$ linearly independent eigenvectors. $\blacksquare$

### Problem 2

(Problem 5.6-5) Let $A$ be an matrix of order $n$ over a number field $K$. Prove: if every nonzero column vector in $K^{n}$ is an eigenvector of $A$, then $A$ must be a scalar matrix.

### Solution to Problem 2

Suppose $A$ is not a scalar matrix.

Then $A$ has at least two distinct eigenvalues $\lambda_{1}\ne\lambda_{2}$.

Let $\alpha$ be an eigenvector belonging to $\lambda_{1}$, and let $\beta$ be an eigenvector belonging to $\lambda_{2}$.

By the theorem, eigenvectors belonging to distinct eigenvalues are linearly independent.

Therefore $\alpha+\beta\ne0$.

By the hypothesis, $\alpha+\beta$ is also an eigenvector of $A$.

Suppose $\alpha+\beta$ belongs to the eigenvalue $\lambda_{3}$.

Then

$$
A\left(\alpha+\beta\right)=\lambda_{3}\left(\alpha+\beta\right).
$$

On the other hand,

$$
A\left(\alpha+\beta\right)=A\alpha+A\beta=\lambda_{1}\alpha+\lambda_{2}\beta.
$$

Therefore

$$
\lambda_{1}\alpha+\lambda_{2}\beta=\lambda_{3}\alpha+\lambda_{3}\beta.
$$

That is,

$$
\left(\lambda_{1}-\lambda_{3}\right)\alpha+\left(\lambda_{2}-\lambda_{3}\right)\beta=0.
$$

Since $\alpha,\beta$ are linearly independent,

$$
\lambda_{1}-\lambda_{3}=0,\lambda_{2}-\lambda_{3}=0.
$$

That is, $\lambda_{1}=\lambda_{2}=\lambda_{3}$.

This is a contradiction.

Therefore the supposition is false; namely, $A$ is a scalar matrix. $\blacksquare$

### Problem 3

(Problem 5.6-7) Prove: an idempotent matrix $A$ of order $n$ over a number field $K$ is always diagonalizable, and the similarity canonical form of $A$ is $\operatorname{diag}\left\{I_{r},0\right\}$, where $r=\operatorname{rank}\left(A\right)$.

### Solution to Problem 3

Since $A^{2}=A$, the eigenvalues of $A$ can only be $0$ or $1$.

**Prove that $A$ is diagonalizable**.

$\ker\left(A\right)=\left\{x\mid Ax=0\right\}$ is the eigenspace belonging to the eigenvalue $0$.

$$
\ker\left(I-A\right)=\left\{x\mid \left(I-A\right)x=0\right\}=\left\{x\mid Ax=x\right\}
$$

is the eigenspace belonging to the eigenvalue $1$.

We prove that

$$
K^{n}=\ker\left(A\right)\oplus\ker\left(I-A\right).
$$

For any $x\in K^{n}$,

$$
x=Ax+\left(I-A\right)x.
$$

Since $A\left(Ax\right)=A^{2}x=Ax$, we have $Ax\in\ker\left(I-A\right)$.

Since

$$
A\left(\left(I-A\right)x\right)=\left(A-A^{2}\right)x=0,
$$

we have $\left(I-A\right)x\in\ker\left(A\right)$.

Therefore

$$
K^{n}=\ker\left(A\right)+\ker\left(I-A\right).
$$

Moreover, since

$$
\ker\left(A\right)\cap\ker\left(I-A\right)=\left\{0\right\}\ \left(\text{若}Ax=0\text{且}Ax=x\text{, 则}x=0\right).
$$

we have

$$
K^{n}=\ker\left(A\right)\oplus\ker\left(I-A\right).
$$

Therefore $A$ has $n$ linearly independent eigenvectors, and is diagonalizable.

**Find the similarity canonical form**.

$$
\dim\ker\left(A\right)=n-\operatorname{rank}\left(A\right).
$$

$$
\dim\ker\left(I-A\right)=\operatorname{rank}\left(A\right)=r.
$$

Thus $A$ has $r$ eigenvalues equal to $1$ and $n-r$ eigenvalues equal to $0$.

Therefore the similarity canonical form of $A$ is $\operatorname{diag}\left\{I_{r},0\right\}$, where $r=\operatorname{rank}\left(A\right)$.

$\blacksquare$

### Problem 4

(Problem 5.6-10) Let $A=\left(a_{ij}\right)$ be an upper triangular matrix of order $n$ over a number field $K$. Prove: if $a_{11}=a_{22}=\cdots=a_{nn}$ and at least one $a_{kl}\ne0$ ( $k< l$ ), then $A$ cannot be diagonalized.

### Solution to Problem 4

Since $A$ is upper triangular, its eigenvalues are precisely the diagonal entries $a_{11},a_{22},\cdots,a_{nn}$.

Given

$$
a_{11}=a_{22}=\cdots=a_{nn}=\lambda_{0}.
$$

That is, $\lambda_{0}$ is an eigenvalue of $A$ of multiplicity $n$ (algebraic multiplicity $n$).

**Find the dimension of the eigenspace**.

$$
\lambda_{0}I-A=\left[\begin{array}{cccc}
0 & -a_{12} & \cdots & -a_{1n}\\
0 & 0 & \cdots & -a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
0 & 0 & \cdots & 0
\end{array}\right].
$$

Since at least one $a_{kl}\ne0$ ( $k< l$ ), $\lambda_{0}I-A$ is not the zero matrix.

Therefore $\operatorname{rank}\left(\lambda_{0}I-A\right)\ge1$.

Thus the dimension of the eigenspace is

$$
n-\operatorname{rank}\left(\lambda_{0}I-A\right)\le n-1.
$$

That is, geometric multiplicity $\le n-1< n=$ algebraic multiplicity.

Therefore $A$ cannot be diagonalized. $\blacksquare$
