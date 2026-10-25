# Assignment 26

> **Definition 1** (Equivalence of matrices)<br>A matrix $A$ over a field $K$ is said to be equivalent to matrix $B$ if $A$ can be transformed into $B$ by a series of elementary row and column operations, denoted $A\overset{\text{相抵}}{\sim}B$.

> **Theorem 1** (Canonical form under equivalence)<br>Let $A$ be an $s\times n$ matrix over $K$ with rank $r$. If $r> 0$, then $A$ is equivalent to a matrix of the form:

$$
\left[\begin{array}{cc}I_{r} & 0\\0 & 0\end{array}\right].
$$

> **Theorem 2** (Necessary and sufficient condition for equivalence)<br>Two $s\times n$ matrices $A$ and $B$ over $K$ are equivalent if and only if their ranks are equal.

### Problem 1

(Problem 5.2-1(1)) Find the canonical form of the following matrix:

$$
A=\left[\begin{array}{rrr}
1 & -1 & 3\\
-2 & 3 & -11\\
4 & -5 & 17
\end{array}\right].
$$

### Solution to Problem 1

By **Theorem 1** (Canonical form under equivalence), perform elementary row operations on $A$:

$$
A=\left[\begin{array}{rrr}
1 & -1 & 3\\
-2 & 3 & -11\\
4 & -5 & 17
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1 & -1 & 3\\
0 & 1 & -5\\
0 & -1 & 5
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1 & -1 & 3\\
0 & 1 & -5\\
0 & 0 & 0
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1 & 0 & -2\\
0 & 1 & -5\\
0 & 0 & 0
\end{array}\right].
$$

Then perform elementary column operations: column $3$ $+2\times$ column $1$, column $3$ $+5\times$ column $2$.

$$
A\rightarrow\left[\begin{array}{rrr}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 0
\end{array}\right].
$$

Therefore, by **Theorem 1** (Canonical form under equivalence), the canonical form is

$$
\left[\begin{array}{cc}I_{2} & 0\\0 & 0\end{array}\right]
$$

$\blacksquare$

### Problem 2

(Problem 5.2-1(3)) Find the canonical form of the following matrix:

$$
A=\left[\begin{array}{rr}
1 & -2\\
-3 & -6\\
2 & -4
\end{array}\right].
$$

### Solution to Problem 2

By **Theorem 1** (Canonical form under equivalence), perform elementary row operations on $A$:

$$
A=\left[\begin{array}{rr}
1 & -2\\
-3 & -6\\
2 & -4
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1 & -2\\
0 & -12\\
0 & 0
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1 & -2\\
0 & 1\\
0 & 0
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1 & 0\\
0 & 1\\
0 & 0
\end{array}\right].
$$

Therefore, by **Theorem 1** (Canonical form under equivalence), the canonical form is

$$
\left[\begin{array}{c}I_{2}\\0\end{array}\right]
$$

$\blacksquare$

### Problem 3

(Problem 5.2-4) Prove: any matrix of rank $r$ ( $r> 0$ ) can be expressed as the sum of $r$ matrices of rank $1$.

### Solution to Problem 3

By **Theorem 1** (Canonical form under equivalence), let $A$ be an $s\times n$ matrix with $\operatorname{rank}\left(A\right)=r> 0$.

By the canonical form theorem, there exist an invertible $s$-th order matrix $P$ and an invertible $n$-th order matrix $Q$ such that

$$
A=P\left[\begin{array}{cc}I_{r} & 0\\0 & 0\end{array}\right]Q.
$$

Write the middle matrix as a sum of $r$ matrices:

$$
\left[\begin{array}{cc}I_{r} & 0\\0 & 0\end{array}\right]=E_{11}+E_{22}+\cdots+E_{rr},
$$

where $E_{ii}$ is the matrix with $1$ in row $i$, column $i$ and $0$ elsewhere.

Each $E_{ii}$ has rank $1$.

Therefore

$$
A=P\left(E_{11}+E_{22}+\cdots+E_{rr}\right)Q=PE_{11}Q+PE_{22}Q+\cdots+PE_{rr}Q.
$$

Let $A_{i}=PE_{ii}Q$.

Since $P$ and $Q$ are invertible,

$$
\operatorname{rank}\left(A_{i}\right)=\operatorname{rank}\left(E_{ii}\right)=1.
$$

Therefore $A$ can be expressed as the sum of $r$ matrices of rank $1$. $\blacksquare$

### Problem 4

(Problem 5.2-5) Let $A,B$ be $s\times n$ and $n\times m$ matrices respectively. Prove the Sylvester rank inequality:

$$
\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right)-n.
$$

### Solution to Problem 4

Following the approach of **Theorem 1** (Canonical form under equivalence), consider the block matrix

$$
M=\left[\begin{array}{cc}A & 0\\I_{n} & B\end{array}\right].
$$

**Find the upper bound for $\operatorname{rank}\left(M\right)$**.

Perform elementary column operations on the block matrix: right-multiply block column $1$ by $-B$ and add to block column $2$.

$$
M=\left[\begin{array}{cc}A & 0\\I_{n} & B\end{array}\right]
\rightarrow
\left[\begin{array}{cc}A & -AB\\I_{n} & 0\end{array}\right].
$$

Then perform elementary row operations: swap block row $1$ and block row $2$.

$$
\rightarrow
\left[\begin{array}{cc}I_{n} & 0\\A & -AB\end{array}\right].
$$

This is a block upper triangular matrix, so

$$
\operatorname{rank}\left(M\right)=\operatorname{rank}\left(I_{n}\right)+\operatorname{rank}\left(-AB\right)=n+\operatorname{rank}\left(AB\right).
$$

**Find the lower bound for $\operatorname{rank}\left(M\right)$**.

Let $\operatorname{rank}\left(A\right)=r_{1}$ and $\operatorname{rank}\left(B\right)=r_{2}$.

$A$ has $r_{1}$ linearly independent rows, and $B$ has $r_{2}$ linearly independent rows.

In the first $s$ rows of $M$, the $r_{1}$ linearly independent rows of $A$ remain linearly independent in $M$ (since the $0$ on the right does not affect them).

In the last $n$ rows of $M$, the $r_{2}$ linearly independent rows of $B$ appear in $M$.

Suppose these rows together with the previous rows are linearly dependent, i.e., there exist coefficients $k_{1},k_{2}$ such that

$$
k_{1}\left(\text{前 }s\text{ 行的线性组合}\right)+k_{2}\left(\text{后 }n\text{ 行的线性组合}\right)=0.
$$

Look at the last $m$ components:

$$
k_{2}\left(B\text{ 的行的线性组合}\right)=0.
$$

Since the rows of $B$ are linearly independent, $k_{2}=0$.

Then look at the first $s$ components:

$$
k_{1}\left(A\text{ 的行的线性组合}\right)=0.
$$

Since the rows of $A$ are linearly independent, $k_{1}=0$.

Therefore the rank of the row vectors of $M$ is at least $r_{1}+r_{2}$.

i.e.,

$$
\operatorname{rank}\left(M\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right).
$$

Combining the two inequalities:

$$
n+\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right).
$$

By the approach of **Theorem 1** (Canonical form under equivalence), i.e.,

$$
\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right)-n.
$$

$\blacksquare$
