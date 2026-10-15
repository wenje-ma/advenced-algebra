# Assignment 5

> **Definition 1** ($n$-th Order Determinant)<br>An $n$-th order determinant is the algebraic sum of $n!$ terms, each being the product of $n$ elements lying in distinct rows and distinct columns. When these $n$ elements are placed in natural order according to their row indices, the term carries a positive sign if the permutation formed by the column indices is even, and a negative sign if it is odd. That is,

$$
\left|\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{array}\right|=\sum_{j_{1}j_{2}\cdots j_{n}}\left(-1\right)^{\tau\left(j_{1}j_{2}\cdots j_{n}\right)}a_{1j_{1}}a_{2j_{2}}\cdots a_{nj_{n}}.
$$

### Problem 1

(Problem 2.2-1(3)) Compute the following determinant according to the definition:

$$
\left|\begin{array}{ccccc}
0 & b_{1} & 0 & \cdots & 0\\
0 & 0 & b_{2} & \cdots & 0\\
\vdots & \vdots & \vdots & & \vdots\\
0 & 0 & 0 & \cdots & b_{n-1}\\
b_{n} & 0 & 0 & \cdots & 0
\end{array}\right|.
$$

### Solution to Problem 1

By **Definition 1** ($n$-th Order Determinant), each term of the determinant is the product of $n$ elements taken from distinct rows and distinct columns.

By **Definition 1**, determine the unique nonzero element that can be chosen row by row: in the $1$st row only $b_{1}$ in the $2$nd column is nonzero, in the $2$nd row only $b_{2}$ in the $3$rd column is nonzero, $\cdots$, in the $n-1$-th row only $b_{n-1}$ in the $n$-th column is nonzero, and in the $n$-th row only $b_{n}$ in the $1$st column is nonzero. Hence the only nonzero term is $b_{1}b_{2}\cdots b_{n}$.

By **Definition 1**, the column-index permutation of this nonzero term is $2,3,\cdots,n,1$, and its number of inversions is

$$
\tau\left(2,3,\cdots,n,1\right)=n-1.
$$

By the sign convention in **Definition 1**, an even permutation carries a positive sign and an odd permutation carries a negative sign, so the value of the determinant is

$$
\left(-1\right)^{n-1}b_{1}b_{2}\cdots b_{n}.
$$

$\blacksquare$

### Problem 2

(Problem 2.2-1(4)) Compute the following determinant according to the definition:

$$
\left|\begin{array}{ccccc}
0 & \cdots & 0 & a_{1} & 0\\
0 & \cdots & a_{2} & 0 & 0\\
\vdots & & \vdots & \vdots & \vdots\\
a_{n-1} & \cdots & 0 & 0 & 0\\
0 & \cdots & 0 & 0 & a_{n}
\end{array}\right|.
$$

### Solution to Problem 2

By **Definition 1** ($n$-th Order Determinant), each term of the determinant is the product of $n$ elements taken from distinct rows and distinct columns.

By **Definition 1**, determine the unique nonzero element that can be chosen row by row: in the $1$st row only $a_{1}$ in the $n-1$-th column is nonzero, in the $2$nd row only $a_{2}$ in the $n-2$-th column is nonzero, $\cdots$, in the $n-1$-th row only $a_{n-1}$ in the $1$st column is nonzero, and in the $n$-th row only $a_{n}$ in the $n$-th column is nonzero. Hence the only nonzero term is $a_{1}a_{2}\cdots a_{n}$.

By **Definition 1**, the column-index permutation of this nonzero term is $n-1,n-2,\cdots,1,n$, and its number of inversions is

$$
\tau=\left(n-2\right)+\left(n-3\right)+\cdots+1+0=\frac{\left(n-1\right)\left(n-2\right)}{2}.
$$

By the sign convention in **Definition 1**, the value of the determinant is

$$
\left(-1\right)^{\frac{\left(n-1\right)\left(n-2\right)}{2}}a_{1}a_{2}\cdots a_{n}.
$$

$\blacksquare$

### Problem 3

(Problem 2.2-1(5)) Compute the following determinant according to the definition:

$$
\left|\begin{array}{ccccc}
0 & 0 & 0 & 1 & 0\\
0 & 0 & 2 & 0 & 0\\
0 & 3 & 8 & 0 & 0\\
4 & 9 & 0 & 7 & 0\\
6 & 0 & 0 & 0 & 5
\end{array}\right|.
$$

### Solution to Problem 3

By **Definition 1** ($n$-th Order Determinant), each term of the determinant is the product of $n$ elements taken from distinct rows and distinct columns.

By **Definition 1**, determine the unique nonzero element that can be chosen row by row:

- $1$st row: only $1$ in the $4$th column is nonzero, so take $\left(1,4\right)=1$;
- $2$nd row: only $2$ in the $3$rd column is nonzero, so take $\left(2,3\right)=2$;
- $3$rd row: the $3$rd column is already occupied, so the only choice is $\left(3,2\right)=3$;
- $4$th row: the $2$nd and $4$th columns are already occupied, so the only choice is $\left(4,1\right)=4$;
- $5$th row: the $1$st column is already occupied, so the only choice is $\left(5,5\right)=5$.

Hence the only nonzero term is $1\times2\times3\times4\times5=120$.

By **Definition 1**, the column-index permutation of this nonzero term is $4,3,2,1,5$, and its number of inversions is

$$
\tau\left(4,3,2,1,5\right)=3+2+1+0+0=6.
$$

By the sign convention in **Definition 1**, an even permutation carries a positive sign, so the value of the determinant is

$$
\left(-1\right)^{6}\times120=120.
$$

$\blacksquare$

### Problem 4

(Problem 2.2-3) Compute using the definition of the determinant:

$$
\left|\begin{array}{ccccc}
a_{1} & a_{2} & a_{3} & a_{4} & a_{5}\\
b_{1} & b_{2} & b_{3} & b_{4} & b_{5}\\
c_{1} & c_{2} & 0 & 0 & 0\\
d_{1} & d_{2} & 0 & 0 & 0\\
e_{1} & e_{2} & 0 & 0 & 0
\end{array}\right|.
$$

### Solution to Problem 4

By **Definition 1** ($n$-th Order Determinant), each term of the determinant is the product of $n$ elements taken from distinct rows and distinct columns.

By **Definition 1**, in rows $3,4,5$ only the elements in columns $1,2$ are nonzero. According to **Definition 1**, the elements of these three rows must be taken from distinct columns, but only $2$ columns are available; since $3$ elements must be taken from distinct columns, by the pigeonhole principle two rows must necessarily draw from the same column, contradicting the "distinct columns" requirement in **Definition 1**.

Therefore there is no nonzero term satisfying the conditions, and the value of the determinant is $0$.

$\blacksquare$

### Problem 5

(Problem 2.2-5) Write down the terms in the following determinant that contain $x^{4}$ and those that contain $x^{3}$:

$$
\left|\begin{array}{rrrr}
5x & x & 1 & x\\
1 & x & 1 & -1\\
3 & 2 & x & 1\\
3 & 1 & 1 & x
\end{array}\right|.
$$

### Solution to Problem 5

By **Definition 1** ($n$-th Order Determinant), each term of the determinant is the product of $n$ elements taken from distinct rows and distinct columns, and the sign of a term is determined by the number of inversions of the column-index permutation.

**Terms containing $x^{4}$**. To obtain $x^{4}$, all $4$ elements must contain $x$. The positions containing $x$ are

$$
\left(1,1\right)=5x,\left(1,2\right)=x,\left(1,4\right)=x,\left(2,2\right)=x,\left(3,3\right)=x,\left(4,4\right)=x.
$$

Each of rows $2,3,4$ has only one position containing $x$, namely $\left(2,2\right),\left(3,3\right),\left(4,4\right)$, which by **Definition 1** must all be taken. Then columns $2,3,4$ are already used, and row $1$ can only take $\left(1,1\right)=5x$. The column-index permutation is $1,2,3,4$, with $\tau=0$ inversions; an even permutation carries a positive sign.

Hence the term containing $x^{4}$ is $5x^{4}$.

**Terms containing $x^{3}$**. To obtain $x^{3}$, we need $3$ elements containing $x$ and $1$ element not containing $x$. Enumerate all combinations satisfying the conditions:

(1) Take

$$
\left(1,2\right)=x,\left(3,3\right)=x,\left(4,4\right)=x,
$$

and row $2$ takes $\left(2,1\right)=1$, which does not contain $x$. The column indices are $2,1,3,4$, with $\tau=1$ inversion; an odd permutation carries a negative sign, so the term is $-x^{3}$.

(2) Take

$$
\left(1,4\right)=x,\left(2,2\right)=x,\left(3,3\right)=x,
$$

and row $4$ takes $\left(4,1\right)=3$, which does not contain $x$. The column indices are $4,2,3,1$, with $\tau=5$ inversions; an odd permutation carries a negative sign, so the term is $-3x^{3}$.

All other combinations are invalid due to column conflicts and do not satisfy the "distinct columns" requirement in **Definition 1**.

Hence the terms containing $x^{3}$ are $-x^{3}-3x^{3}=-4x^{3}$.

$\blacksquare$
