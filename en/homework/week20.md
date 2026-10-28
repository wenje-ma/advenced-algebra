# week20

> **Basic Knowledge: Formula for the Vandermonde Determinant**<br>The $3\times 3$ Vandermonde determinant in $x_{1},x_{2},x_{3}$

$$
\left|\begin{array}{ccc}
1 & 1 & 1\\
x_{1} & x_{2} & x_{3}\\
x_{1}^{2} & x_{2}^{2} & x_{3}^{2}
\end{array}\right|=\left(x_{2}-x_{1}\right)\left(x_{3}-x_{1}\right)\left(x_{3}-x_{2}\right).
$$

> **Theorem 4.3.1 (Rank of a Matrix Product)**<br>Let $A=\left(a_{ij}\right)_{s\times n}$ and $B=\left(b_{ij}\right)_{n\times m}$. Then

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

> **Proposition 4.3.2 (Over $\mathbb{R}$, $A^{\top}Az=0$ Has the Same Solutions as $z=0$)**<br>Let $A$ be a matrix over the real number field. Then the homogeneous system $A^{\top}Az=0$ and $z=0$ have the same solutions.

> **Theorem 4.3.3 (Determinant of a Product)**<br>Let $A,B$ both be $n\times n$ matrices. Then $\left|AB\right|=\left|A\right|\left|B\right|$.

---

## 4.3-2

A matrix is called row (column) full-rank if its row (column) vector group is linearly independent. Prove: if an $s\times n$ matrix $A$ has rank $r$, then there exist an $s\times r$ column full-rank matrix $B$ and an $r\times n$ row full-rank matrix $C$ such that $A=BC$.

### Solution 4.3-2

Following the idea of **Theorem 4.3.1 (Rank of a Matrix Product)**, transform $A$ by elementary row operations into a reduced row-echelon matrix $J$.

Since $\text{rank}\left(A\right)=r$, $J$ has $r$ nonzero rows.

Set

$$
J=\left[\begin{array}{c}C\\0\end{array}\right],
$$

where $C$ is an $r\times n$ matrix whose row vector group is linearly independent (because the nonzero rows of $J$ are linearly independent).

Hence $C$ is row full-rank.

Write $A=PJ$, where $P$ is an $s\times s$ invertible matrix.

Then $A=P\left[\begin{array}{c}C\\0\end{array}\right]$.

Block $P$ by columns: $P=\left(P_{1},P_{2}\right)$, where $P_{1}$ is an $s\times r$ matrix.

Then

$$
A=\left(P_{1},P_{2}\right)\left[\begin{array}{c}C\\0\end{array}\right]=P_{1}C.
$$

Set $B=P_{1}$.

Since $P$ is invertible, its column group is linearly independent, and hence the column group of $P_{1}$ is also linearly independent.

Thus $B$ is column full-rank.

Therefore $A=BC$, where $B$ is an $s\times r$ column full-rank matrix and $C$ is an $r\times n$ row full-rank matrix. $\blacksquare$

---

## 4.3-6

Prove: if $A$ is an $n\times n$ matrix over a number field $K$, $n$ is odd, and $AA^{\top}=I$ with $\left|A\right|=1$, then $\left|I-A\right|=0$.

### Solution 4.3-6

By **Theorem 4.3.3 (Determinant of a Product)**, $\left|AB\right|=\left|A\right|\left|B\right|$. We prove $\left|I-A\right|=0$.

$$
\left|I-A\right|=\left|\left(I-A\right)^{\top}\right|=\left|I-A^{\top}\right|.
$$

Since $AA^{\top}=I$, we have $A^{\top}=A^{-1}$.

Therefore

$$
\left|I-A^{\top}\right|=\left|I-A^{-1}\right|=\left|A^{-1}\left(A-I\right)\right|=\left|A^{-1}\right|\left|A-I\right|.
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

Hence $2\left|I-A\right|=0$, i.e. $\left|I-A\right|=0$. $\blacksquare$

---

## 4.3-7

Let $s_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$ for $k=0,1,2,\cdots$; and let

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

### Solution 4.3-7

By **Theorem 4.3.3 (Determinant of a Product)**, $\left|AB\right|=\left|A\right|\left|B\right|$. Set

$$
B=\left[\begin{array}{ccc}
1 & 1 & 1\\
x_{1} & x_{2} & x_{3}\\
x_{1}^{2} & x_{2}^{2} & x_{3}^{2}
\end{array}\right].
$$

Compute the $\left(i,j\right)$-entry of $BB^{\top}$:

$$
\left(BB^{\top}\right)_{ij}=\sum_{k=1}^{3}B_{ik}B_{jk}=\sum_{k=1}^{3}x_{k}^{i-1}x_{k}^{j-1}=\sum_{k=1}^{3}x_{k}^{i+j-2}=s_{i+j-2}.
$$

Therefore

$$
BB^{\top}=\left[\begin{array}{ccc}
s_{0} & s_{1} & s_{2}\\
s_{1} & s_{2} & s_{3}\\
s_{2} & s_{3} & s_{4}
\end{array}\right]=A.
$$

By **Theorem 4.3.3 (Determinant of a Product)**,

$$
\left|A\right|=\left|BB^{\top}\right|=\left|B\right|\left|B^{\top}\right|=\left|B\right|^{2}.
$$

By **Basic Knowledge: Formula for the Vandermonde Determinant**, $B$ is a Vandermonde matrix,

$$
\left|B\right|=\left(x_{2}-x_{1}\right)\left(x_{3}-x_{1}\right)\left(x_{3}-x_{2}\right).
$$

Therefore

$$
\left|A\right|=\left|B\right|^{2}=\left(x_{1}-x_{2}\right)^{2}\left(x_{1}-x_{3}\right)^{2}\left(x_{2}-x_{3}\right)^{2}.
$$

$\blacksquare$

---

## 4.3-12

Prove: for any $s\times n$ matrix $A$ over the real number field,

$$
\text{rank}\left(A^{\top}AA^{\top}\right)=\text{rank}\left(A\right).
$$

### Solution 4.3-12

By **Theorem 4.3.1 (Rank of a Matrix Product)**,

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

Consider the homogeneous system $\left(A^{\top}AA^{\top}\right)y=0$, where $y$ is an $s$-dimensional column vector.

Suppose $y$ solves $\left(A^{\top}AA^{\top}\right)y=0$; then

$$
A^{\top}A\left(A^{\top}y\right)=0.
$$

Set $z=A^{\top}y$; then $A^{\top}Az=0$.

By **Proposition 4.3.2 (Over $\mathbb{R}$, $A^{\top}Az=0$ Has the Same Solutions as $z=0$)**, over the real number field $A^{\top}Az=0$ and $z=0$ have the same solutions.

Hence $z=0$, i.e. $A^{\top}y=0$.

Conversely, if $A^{\top}y=0$, then

$$
A^{\top}AA^{\top}y=A^{\top}A\left(A^{\top}y\right)=A^{\top}A\times0=0.
$$

Thus $\left(A^{\top}AA^{\top}\right)y=0$ and $A^{\top}y=0$ have the same solutions.

Hence their solution spaces have the same dimension:

$$
s-\text{rank}\left(A^{\top}AA^{\top}\right)=s-\text{rank}\left(A^{\top}\right).
$$

Therefore

$$
\text{rank}\left(A^{\top}AA^{\top}\right)=\text{rank}\left(A^{\top}\right)=\text{rank}\left(A\right).
$$

$\blacksquare$
