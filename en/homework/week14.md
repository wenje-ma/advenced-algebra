# week14

> **Basic Knowledge: Upper Bound on the Rank of a Union of Vector Groups**<br>If a vector group $A$ can be split into two subgroups $A_{1},A_{2}$, then $\text{rank}\left(A\right)\le\text{rank}\left(A_{1}\right)+\text{rank}\left(A_{2}\right)$.

> **Definition 3.5.1 (Rank of a Matrix)**<br>The row rank and column rank of a matrix $A$ are collectively called the rank of $A$, denoted $\text{rank}\left(A\right)$.

> **Theorem 3.5.4 (Row Rank Equals Column Rank)**<br>The row rank of any matrix equals its column rank.

> **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**<br>If a matrix $A$ is transformed by elementary row operations into a row-echelon matrix $J$, then the rank of $A$ equals the number of nonzero rows of $J$. If the pivot columns of $J$ are columns $j_{1},\cdots,j_{r}$, then columns $j_{1},\cdots,j_{r}$ of $A$ form a maximal linearly independent subset of the column group of $A$.

---

## 3.5-2(1)

Find the rank of the following vector group and a maximal linearly independent subset:

$$
\alpha_{1}=\begin{bmatrix}-1\\5\\3\\-2\end{bmatrix},
\alpha_{2}=\begin{bmatrix}4\\1\\-2\\9\end{bmatrix},
\alpha_{3}=\begin{bmatrix}2\\0\\-1\\4\end{bmatrix},
\alpha_{4}=\begin{bmatrix}0\\3\\4\\-5\end{bmatrix}.
$$

### Solution 3.5-2(1)

By **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**, arrange the vectors as columns into a matrix and perform elementary row operations:

$$
\left[\begin{array}{rrrr}
-1 & 4 & 2 & 0\\
5 & 1 & 0 & 3\\
3 & -2 & -1 & 4\\
-2 & 9 & 4 & -5
\end{array}\right]
\xrightarrow{\text{row ops}}
\left[\begin{array}{rrrr}
1 & -4 & -2 & 0\\
0 & 1 & 0 & -5\\
0 & 0 & 5 & 54\\
0 & 0 & 0 & 0
\end{array}\right].
$$

By **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**, the echelon matrix has $3$ nonzero rows, so the rank is $3$.

By **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**, the pivots are in columns $1,2,3$, so $\alpha_{1},\alpha_{2},\alpha_{3}$ are a maximal linearly independent subset. $\blacksquare$

---

## 3.5-3

Find a basis of the column space and the dimension of the row space of the following matrix $A$:

$$
A=\left[\begin{array}{rrrr}
1 & 3 & -2 & -7\\
0 & -1 & -3 & 4\\
5 & 2 & 0 & 1\\
1 & 4 & 1 & -11
\end{array}\right].
$$

### Solution 3.5-3

By **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**, perform elementary row operations:

$$
\left[\begin{array}{rrrr}
1 & 3 & -2 & -7\\
0 & -1 & -3 & 4\\
5 & 2 & 0 & 1\\
1 & 4 & 1 & -11
\end{array}\right]
\xrightarrow{\text{row ops}}
\left[\begin{array}{rrrr}
1 & 3 & -2 & -7\\
0 & 1 & 3 & -4\\
0 & 0 & 49 & -16\\
0 & 0 & 0 & 0
\end{array}\right].
$$

The echelon matrix has $3$ nonzero rows; by **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**, $\text{rank}\left(A\right)=3$.

By **Theorem 3.5.4 (Row Rank Equals Column Rank)**, the dimension of the row space equals the rank of the matrix, namely $3$.

By **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**, the pivots are in columns $1,2,3$, so columns $1,2,3$ of the original matrix $A$ form a basis of the column space:

$$
\alpha_{1}=\begin{bmatrix}1\\0\\5\\1\end{bmatrix},
\alpha_{2}=\begin{bmatrix}3\\-1\\2\\4\end{bmatrix},
\alpha_{3}=\begin{bmatrix}-2\\-3\\0\\1\end{bmatrix}.
$$

$\blacksquare$

---

## 3.5-4

For different values of $\lambda$, what are the ranks of the following matrix?

$$
\left[\begin{array}{rrrr}
1 & \lambda & -1 & 2\\
2 & -1 & \lambda & 5\\
1 & 10 & -6 & 1
\end{array}\right].
$$

### Solution 3.5-4

By **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**, perform elementary row operations to find the rank:

Row $2$ $-$ row $1$ $\times 2$: row $2$ $=\left(0,-1-2\lambda,\lambda+2,1\right)$.

Row $3$ $-$ row $1$: row $3$ $=\left(0,10-\lambda,-5,-1\right)$.

The matrix becomes

$$
\left[\begin{array}{rrrr}
1 & \lambda & -1 & 2\\
0 & -1-2\lambda & \lambda+2 & 1\\
0 & 10-\lambda & -5 & -1
\end{array}\right].
$$

Row $2$ $+$ row $3$: row $2$

$$
=\left(0,9-3\lambda,\lambda-3,0\right)=\left(0,3\left(3-\lambda\right),-\left(3-\lambda\right),0\right).
$$

**When $\lambda=3$**:

row $2$ $=\left(0,0,0,0\right)$, row $3$ $=\left(0,7,-5,-1\right)$.

The echelon matrix has $2$ nonzero rows, so the rank is $2$.

**When $\lambda\ne3$**:

row $2$ is nonzero. Row $3$ $-$ row $2$ $\times\frac{10-\lambda}{3\left(3-\lambda\right)}$: the $4$th column of row $3$ is still $-1\ne0$, so row $3$ is nonzero.

The echelon matrix has $3$ nonzero rows, so the rank is $3$.

In summary: when $\lambda=3$, by **Corollary 3.5.5 (Computing Rank by Elementary Row Operations)**, the echelon matrix has $2$ nonzero rows, so the rank is $2$; when $\lambda\ne3$, the echelon matrix has $3$ nonzero rows, so the rank is $3$. $\blacksquare$

---

## 3.5-8

Prove: if an $m\times n$ matrix $A$ has rank $r$, then the submatrix $A_{1}$ formed by any $s$ rows of $A$ has rank at least $r+s-m$.

### Solution 3.5-8

By **Definition 3.5.1 (Rank of a Matrix)**, the row rank and column rank of $A$ are collectively called the rank of $A$. We prove that the rank of $A_{1}$ is at least $r+s-m$.

Let $A_{2}$ be the submatrix formed by the remaining $m-s$ rows of $A$.

Viewing $A$ as a row vector group, the rank of the row group of $A$ is $r$.

The row group of $A$ $=$ the row group of $A_{1}$ $\cup$ the row group of $A_{2}$.

By **Basic Knowledge: Upper Bound on the Rank of a Union of Vector Groups**,

$$
\text{rank}\left(A\right)\le\text{rank}\left(A_{1}\right)+\text{rank}\left(A_{2}\right).
$$

Since $A_{2}$ has only $m-s$ rows, $\text{rank}\left(A_{2}\right)\le m-s$.

Hence

$$
r\le\text{rank}\left(A_{1}\right)+\left(m-s\right).
$$

Rearranging,

$$
\text{rank}\left(A_{1}\right)\ge r-\left(m-s\right)=r+s-m.
$$

$\blacksquare$

---

## 3.5-13

Let $A$ be an $s\times n$ matrix, $B$ an $l\times m$ matrix, and $C$ an $s\times m$ matrix. Prove:

$$
\text{rank}\left(\begin{array}{cc}A & C\\0 & B\end{array}\right)\ge\text{rank}\left(A\right)+\text{rank}\left(B\right).
$$

### Solution 3.5-13

By **Definition 3.5.1 (Rank of a Matrix)**, prove that the rank of the block matrix is at least the sum of the ranks of $A$ and $B$. Take bases of the column spaces of $A$ and $B$ to construct a linearly independent vector group.

Let $\text{rank}\left(A\right)=r_{1}$ and $\text{rank}\left(B\right)=r_{2}$.

Take a basis of the column space of $A$: $\alpha_{1},\cdots,\alpha_{r_{1}}$ ( $s$-dimensional vectors).

Take a basis of the column space of $B$: $\beta_{1},\cdots,\beta_{r_{2}}$ ( $l$-dimensional vectors).

Consider the following column vectors of the block matrix

$$
M=\left(\begin{array}{cc}A & C\\0 & B\end{array}\right):
$$

$$
\begin{bmatrix}\alpha_{1}\\0\end{bmatrix},\cdots,\begin{bmatrix}\alpha_{r_{1}}\\0\end{bmatrix},
\begin{bmatrix}c_{1}\\\beta_{1}\end{bmatrix},\cdots,\begin{bmatrix}c_{r_{2}}\\\beta_{r_{2}}\end{bmatrix},
$$

where $c_{i}$ are $s$-dimensional vectors suitably chosen from the columns of $C$ so that the lower half of the corresponding column of $M$ is $\beta_{i}$.

Prove that these $r_{1}+r_{2}$ vectors are linearly independent: set

$$
k_{1}\begin{bmatrix}\alpha_{1}\\0\end{bmatrix}+\cdots+k_{r_{1}}\begin{bmatrix}\alpha_{r_{1}}\\0\end{bmatrix}
+l_{1}\begin{bmatrix}c_{1}\\\beta_{1}\end{bmatrix}+\cdots+l_{r_{2}}\begin{bmatrix}c_{r_{2}}\\\beta_{r_{2}}\end{bmatrix}=0.
$$

Lower half: $l_{1}\beta_{1}+\cdots+l_{r_{2}}\beta_{r_{2}}=0$. Since $\beta_{1},\cdots,\beta_{r_{2}}$ are linearly independent, $l_{1}=\cdots=l_{r_{2}}=0$.

Upper half: $k_{1}\alpha_{1}+\cdots+k_{r_{1}}\alpha_{r_{1}}=0$. Since $\alpha_{1},\cdots,\alpha_{r_{1}}$ are linearly independent, $k_{1}=\cdots=k_{r_{1}}=0$.

Hence these $r_{1}+r_{2}$ vectors are linearly independent.

Therefore

$$
\text{rank}\left(M\right)\ge r_{1}+r_{2}=\text{rank}\left(A\right)+\text{rank}\left(B\right).
$$

$\blacksquare$
