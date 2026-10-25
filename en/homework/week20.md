# Assignment 20

> **Theorem 1** (Rank of matrix product)<br>Let $A=\left(a_{ij}\right)_{s\times n}$ and $B=\left(b_{ij}\right)_{n\times m}$. Then:
> 
> $$
> \text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}
> $$

> **Theorem 3** (Determinant of product)<br>Let $A,B$ both be $n$-th order matrices. Then $\left|AB\right|=\left|A\right|\left|B\right|$.

### Problem 1

(Problem 4.3-2) A matrix is called row-(column-)full-rank if its row (column) vectors are linearly independent. Prove: if an $s\times n$ matrix $A$ has rank $r$, then there exist an $s\times r$ column-full-rank matrix $B$ and an $r\times n$ row-full-rank matrix $C$ such that $A=BC$.

### Solution to Problem 1

Following the approach of **Theorem 1** (Rank of matrix product), transform $A$ by elementary row operations into reduced row echelon form $J$.

Since $\text{rank}\left(A\right)=r$, $J$ has $r$ nonzero rows.

Let

$$
J=\left[\begin{array}{c}C\\0\end{array}\right]
$$

where $C$ is an $r\times n$ matrix, and the row vectors of $C$ are linearly independent (since the nonzero rows of $J$ are linearly independent).

Thus $C$ is row-full-rank.

Let $A=PJ$, where $P$ is an $s\times s$ invertible matrix.

Then $A=P\left[\begin{array}{c}C\\0\end{array}\right]$.

Partition $P$ by columns: $P=\left(P_{1},P_{2}\right)$, where $P_{1}$ is an $s\times r$ matrix.

Then

$$
A=\left(P_{1},P_{2}\right)\left[\begin{array}{c}C\\0\end{array}\right]=P_{1}C
$$

Let $B=P_{1}$.

Since $P$ is invertible, the column vectors of $P$ are linearly independent; hence the column vectors of $P_{1}$ are also linearly independent.

Thus $B$ is column-full-rank.

Therefore $A=BC$, where $B$ is an $s\times r$ column-full-rank matrix and $C$ is an $r\times n$ row-full-rank matrix. $\blacksquare$

### Problem 2

(Problem 4.3-6) Prove: if $A$ is an $n$-th order matrix over $K$, $n$ is odd, and $AA^{T}=I$, $\left|A\right|=1$, then $\left|I-A\right|=0$.

### Solution to Problem 2

By **Theorem 3** (Determinant of product), $\left|AB\right|=\left|A\right|\left|B\right|$. We prove $\left|I-A\right|=0$.

$$
\left|I-A\right|=\left|\left(I-A\right)^{T}\right|=\left|I-A^{T}\right|.
$$

Since $AA^{T}=I$, $A^{T}=A^{-1}$.

Therefore

$$
\left|I-A^{T}\right|=\left|I-A^{-1}\right|=\left|A^{-1}\left(A-I\right)\right|=\left|A^{-1}\right|\left|A-I\right|.
$$

$$
\left|A^{-1}\right|=\frac{1}{\left|A\right|}=\frac{1}{1}=1.
$$

$$
\left|A-I\right|=\left|-\left(I-A\right)\right|=\left(-1\right)^{n}\left|I-A\right|.
$$

Since $n$ is odd, $\left(-1\right)^{n}=-1$.

Therefore

$$
\left|I-A\right|=1\times\left(-1\right)\times\left|I-A\right|=-\left|I-A\right|.
$$

Hence $2\left|I-A\right|=0$, i.e., $\left|I-A\right|=0$. $\blacksquare$

### Problem 3

(Problem 4.3-7) Let $s_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$, $k=0,1,2,\cdots$; let

$$
A=\left[\begin{array}{ccc}
s_{0} & s_{1} & s_{2}\\
s_{1} & s_{2} & s_{3}\\
s_{2} & s_{3} & s_{4}
\end{array}\right].
$$

Prove:

$$
\left|A\right|=\left(x_{1}-x_{2}\right)^{2}\left(x_{1}-x_{3}\right)^{2}\left(x_{2}-x_{3}\right)^{2}.
$$

### Solution to Problem 3

By **Theorem 3** (Determinant of product), $\left|AB\right|=\left|A\right|\left|B\right|$. Let

$$
B=\left[\begin{array}{ccc}
1 & 1 & 1\\
x_{1} & x_{2} & x_{3}\\
x_{1}^{2} & x_{2}^{2} & x_{3}^{2}
\end{array}\right].
$$

Compute the $\left(i,j\right)$-entry of $BB^{T}$:

$$
\left(BB^{T}\right)_{ij}=\sum_{k=1}^{3}B_{ik}B_{jk}=\sum_{k=1}^{3}x_{k}^{i-1}x_{k}^{j-1}=\sum_{k=1}^{3}x_{k}^{i+j-2}=s_{i+j-2}.
$$

Therefore

$$
BB^{T}=\left[\begin{array}{ccc}
s_{0} & s_{1} & s_{2}\\
s_{1} & s_{2} & s_{3}\\
s_{2} & s_{3} & s_{4}
\end{array}\right]=A.
$$

Therefore

By **Theorem 3** (Determinant of product),

$$
\left|A\right|=\left|BB^{T}\right|=\left|B\right|\left|B^{T}\right|=\left|B\right|^{2}.
$$

$B$ is a Vandermonde matrix,

$$
\left|B\right|=\left(x_{2}-x_{1}\right)\left(x_{3}-x_{1}\right)\left(x_{3}-x_{2}\right).
$$

Therefore

$$
\left|A\right|=\left|B\right|^{2}=\left(x_{1}-x_{2}\right)^{2}\left(x_{1}-x_{3}\right)^{2}\left(x_{2}-x_{3}\right)^{2}.
$$

$\blacksquare$

### Problem 4

(Problem 4.3-12) Prove: for any $s\times n$ matrix $A$ over the real field,

$$
\text{rank}\left(A^{T}AA^{T}\right)=\text{rank}\left(A\right).
$$

### Solution to Problem 4

By **Theorem 1** (Rank of matrix product),

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

Consider the homogeneous system $\left(A^{T}AA^{T}\right)y=0$, where $y$ is an $s$-dimensional column vector.

Let $y$ be a solution of $\left(A^{T}AA^{T}\right)y=0$. Then

$$
A^{T}A\left(A^{T}y\right)=0.
$$

Set $z=A^{T}y$; then $A^{T}Az=0$.

By Proposition $2$, over the real field, $A^{T}Az=0$ and $z=0$ have the same solutions.

Hence $z=0$, i.e., $A^{T}y=0$.

Conversely, if $A^{T}y=0$, then

$$
A^{T}AA^{T}y=A^{T}A\left(A^{T}y\right)=A^{T}A\times0=0.
$$

Therefore $\left(A^{T}AA^{T}\right)y=0$ and $A^{T}y=0$ have the same solutions.

Hence their solution spaces have the same dimension:

$$
s-\text{rank}\left(A^{T}AA^{T}\right)=s-\text{rank}\left(A^{T}\right).
$$

Therefore

$$
\text{rank}\left(A^{T}AA^{T}\right)=\text{rank}\left(A^{T}\right)=\text{rank}\left(A\right).
$$

$\blacksquare$
