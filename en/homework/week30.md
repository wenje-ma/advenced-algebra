# week30

> **Theorem 5.6.1 (Necessary and Sufficient Condition for Diagonalizability)**<br>An $n\times n$ matrix $A$ over a number field $K$ is diagonalizable if and only if $A$ has $n$ linearly independent eigenvectors.

> **Corollary 5.6.6 (Distinct Eigenvalues Imply Diagonalizability)**<br>If an $n\times n$ matrix $A$ over a number field $K$ has $n$ distinct eigenvalues, then $A$ is diagonalizable.

---

## 5.6-1

Among the matrices in Exercises 5.5, problems 1 and 2, which are diagonalizable and which are not? For each diagonalizable matrix $A$, find an invertible matrix $P$ such that $P^{-1}AP$ is diagonal, and write down that diagonal matrix.

### Solution 5.6-1

By **Theorem 5.6.1 (Necessary and Sufficient Condition for Diagonalizability)**, an $n\times n$ matrix $A$ over a number field $K$ is diagonalizable if and only if $A$ has $n$ linearly independent eigenvectors.

**Exercise 5.5, problem 1(1)**: $A=\left[\begin{array}{rrr}2 & 2 & -2\\2 & 5 & -4\\-2 & -4 & 5\end{array}\right]$.

Eigenvalues: $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=10$.

Find the eigenvectors for $\lambda=10$:

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

Solving gives $x_{2}=-x_{3}$ and $x_{1}=\frac{1}{2}x_{3}$.

A fundamental solution system: $\alpha_{1}=\left(1,-2,2\right)^{\top}$.

Eigenvectors for the eigenvalue $\lambda=1$:

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

A fundamental solution system: $\alpha_{2}=\left(-2,1,0\right)^{\top}$, $\alpha_{3}=\left(2,0,1\right)^{\top}$.

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

**Exercise 5.5, problem 1(2)**: $A=\left[\begin{array}{rrr}2 & 3 & 2\\1 & 8 & 2\\-2 & -14 & -3\end{array}\right]$.

Eigenvalues: $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=3$.

The eigenspace for $\lambda=3$ has dimension $1$ (geometric multiplicity), while the algebraic multiplicity is $2$.

Geometric multiplicity $< $ algebraic multiplicity, so $A$ is not diagonalizable.

**Exercise 5.5, problem 1(3)**: $A=\left[\begin{array}{rrr}6 & 2 & 4\\2 & 3 & 2\\4 & 2 & 6\end{array}\right]$.

Eigenvalues: $\lambda_{1}=2$, $\lambda_{2}=11$.

There are two distinct eigenvalues, and the $3\times 3$ matrix has $3$ linearly independent eigenvectors, so it is diagonalizable.

**Exercise 5.5, problem 1(4)**: $A=\left[\begin{array}{rrr}2 & -1 & 2\\5 & -3 & 3\\-1 & 0 & -2\end{array}\right]$.

Eigenvalue: $\lambda=-1$ (triple root).

Geometric multiplicity $< 3$, so it is not diagonalizable.

**Exercise 5.5, problem 1(5)**: $A=\left[\begin{array}{rrr}0 & 1/2 & 1/2\\1 & -1/2 & 1/2\\1 & -1/2 & 1/2\end{array}\right]$.

Eigenvalues: $\lambda_{1}=0$, $\lambda_{2}=1$, $\lambda_{3}=-1$.

Three distinct eigenvalues, so it is diagonalizable.

**Exercise 5.5, problem 2(1)**: $A=\left[\begin{array}{rr}1 & -\sqrt{3}\\\sqrt{3} & 1\end{array}\right]$.

Regarded as a real matrix, it has no real eigenvalue, so it is not diagonalizable.

Regarded as a complex matrix, it has two distinct eigenvalues, so it is diagonalizable.

**Exercise 5.5, problem 2(2)**: $A=\left[\begin{array}{rrr}3 & 7 & -3\\-2 & -5 & 2\\-4 & -10 & 3\end{array}\right]$.

Regarded as a real matrix, it has only $1$ real eigenvalue, so it is not diagonalizable.

Regarded as a complex matrix, it has three distinct eigenvalues, so it is diagonalizable.

All these judgments rest on whether the matrix has $n$ linearly independent eigenvectors. $\blacksquare$

---

## 5.6-5

Let $A$ be an $n\times n$ matrix over a number field $K$. Prove: if every nonzero column vector in $K^{n}$ is an eigenvector of $A$, then $A$ must be a scalar matrix.

### Solution 5.6-5

Suppose $A$ is not a scalar matrix.

Then $A$ has at least two distinct eigenvalues $\lambda_{1}\ne\lambda_{2}$.

Let $\alpha$ be an eigenvector belonging to $\lambda_{1}$ and $\beta$ an eigenvector belonging to $\lambda_{2}$.

Eigenvectors belonging to distinct eigenvalues are linearly independent.

Hence $\alpha+\beta\ne0$.

By the assumption, $\alpha+\beta$ is also an eigenvector of $A$.

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
\lambda_{1}-\lambda_{3}=0,\quad\lambda_{2}-\lambda_{3}=0.
$$

Namely $\lambda_{1}=\lambda_{2}=\lambda_{3}$.

This is a contradiction.

Hence the assumption fails, and $A$ is a scalar matrix. $\blacksquare$

---

## 5.6-7

Prove: an $n\times n$ idempotent matrix $A$ over a number field $K$ is always diagonalizable, and its canonical form under similarity is $\operatorname{diag}\left\{I_{r},0\right\}$, where $r=\operatorname{rank}\left(A\right)$.

### Solution 5.6-7

Since $A^{2}=A$, the eigenvalues of $A$ can only be $0$ or $1$.

**Prove that $A$ is diagonalizable.**

$\ker\left(A\right)=\left\{x\mid Ax=0\right\}$ is the eigenspace belonging to the eigenvalue $0$.

$$
\ker\left(I-A\right)=\left\{x\mid \left(I-A\right)x=0\right\}=\left\{x\mid Ax=x\right\}
$$

is the eigenspace belonging to the eigenvalue $1$.

We prove

$$
K^{n}=\ker\left(A\right)\oplus\ker\left(I-A\right).
$$

For any $x\in K^{n}$,

$$
x=Ax+\left(I-A\right)x.
$$

Since $A\left(Ax\right)=A^{2}x=Ax$, $Ax\in\ker\left(I-A\right)$.

Since

$$
A\left(\left(I-A\right)x\right)=\left(A-A^{2}\right)x=0,
$$

$\left(I-A\right)x\in\ker\left(A\right)$.

Therefore

$$
K^{n}=\ker\left(A\right)+\ker\left(I-A\right).
$$

Moreover,

$$
\ker\left(A\right)\cap\ker\left(I-A\right)=\left\{0\right\}\ \left(\text{if }Ax=0\text{ and }Ax=x\text{, then }x=0\right).
$$

Hence

$$
K^{n}=\ker\left(A\right)\oplus\ker\left(I-A\right).
$$

Thus $A$ has $n$ linearly independent eigenvectors, and is diagonalizable.

**Find the canonical form under similarity.**

$$
\dim\ker\left(A\right)=n-\operatorname{rank}\left(A\right).
$$

$$
\dim\ker\left(I-A\right)=\operatorname{rank}\left(A\right)=r.
$$

Hence $A$ has $r$ eigenvalues equal to $1$ and $n-r$ eigenvalues equal to $0$.

Therefore the canonical form of $A$ under similarity is $\operatorname{diag}\left\{I_{r},0\right\}$, where $r=\operatorname{rank}\left(A\right)$.

$\blacksquare$

---

## 5.6-10

Let $A=\left(a_{ij}\right)$ be an $n\times n$ upper triangular matrix over a number field $K$. Prove: if $a_{11}=a_{22}=\cdots=a_{nn}$ and at least one $a_{kl}\ne0$ ( $k< l$ ), then $A$ cannot be diagonalized.

### Solution 5.6-10

Since $A$ is upper triangular, its eigenvalues are exactly the diagonal entries $a_{11},a_{22},\cdots,a_{nn}$.

We are given

$$
a_{11}=a_{22}=\cdots=a_{nn}=\lambda_{0}.
$$

That is, $\lambda_{0}$ is an $n$-fold eigenvalue of $A$ (algebraic multiplicity $n$).

**Find the dimension of the eigenspace.**

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

Hence the dimension of the eigenspace is

$$
n-\operatorname{rank}\left(\lambda_{0}I-A\right)\le n-1.
$$

That is, the geometric multiplicity $\le n-1< n=$ the algebraic multiplicity.

Therefore $A$ cannot be diagonalized. $\blacksquare$
