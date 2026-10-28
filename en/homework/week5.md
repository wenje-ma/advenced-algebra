# week5

> **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**<br>In an $n$-permutation, if a pair of numbers has its order reversed relative to its size (i.e. the number in front is larger than the one behind), then the pair is called an inversion. The total number of inversions in a permutation is called its inversion number, denoted $\tau$. A permutation with odd inversion number is called an odd permutation, and one with even inversion number is called an even permutation.

> **Basic Knowledge: The Pigeonhole Principle**<br>If $n+1$ (or more) objects are placed into $n$ boxes, then at least one box contains at least two objects.

> **Definition 2.2.1 ($n\times n$ Determinant)**<br>An $n\times n$ determinant is an algebraic sum of $n!$ terms, each term being a product of $n$ entries from distinct rows and distinct columns; after these $n$ entries are arranged so that their row indices are in natural order, the term carries a plus sign when the permutation formed by the column indices is even and a minus sign when it is odd. Namely,

$$
\left|\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{array}\right|=\sum_{j_{1}j_{2}\cdots j_{n}}\left(-1\right)^{\tau\left(j_{1}j_{2}\cdots j_{n}\right)}a_{1j_{1}}a_{2j_{2}}\cdots a_{nj_{n}}.
$$

---

## 2.2-1(3)

Compute the following determinant by the definition:

$$
\left|\begin{array}{ccccc}
0 & b_{1} & 0 & \cdots & 0\\
0 & 0 & b_{2} & \cdots & 0\\
\vdots & \vdots & \vdots & & \vdots\\
0 & 0 & 0 & \cdots & b_{n-1}\\
b_{n} & 0 & 0 & \cdots & 0
\end{array}\right|.
$$

### Solution 2.2-1(3)

By **Definition 2.2.1 ($n\times n$ Determinant)**, each term of the determinant is a product of $n$ entries from distinct rows and distinct columns.

By **Definition 2.2.1 ($n\times n$ Determinant)**, determine the unique nonzero entry row by row: row $1$ has only $b_{1}$ in column $2$ nonzero, row $2$ has only $b_{2}$ in column $3$ nonzero, $\cdots$, row $n-1$ has only $b_{n-1}$ in column $n$ nonzero, and row $n$ has only $b_{n}$ in column $1$ nonzero. Hence the only nonzero term is $b_{1}b_{2}\cdots b_{n}$.

By **Definition 2.2.1 ($n\times n$ Determinant)**, the column-index permutation of this nonzero term is $2,3,\cdots,n,1$, whose inversion number is

$$
\tau\left(2,3,\cdots,n,1\right)=n-1.
$$

By the sign convention in **Definition 2.2.1 ($n\times n$ Determinant)**, even permutations carry a plus sign and odd permutations a minus sign, so the determinant equals

$$
\left(-1\right)^{n-1}b_{1}b_{2}\cdots b_{n}.
$$

$\blacksquare$

---

## 2.2-1(4)

Compute the following determinant by the definition:

$$
\left|\begin{array}{ccccc}
0 & \cdots & 0 & a_{1} & 0\\
0 & \cdots & a_{2} & 0 & 0\\
\vdots & & \vdots & \vdots & \vdots\\
a_{n-1} & \cdots & 0 & 0 & 0\\
0 & \cdots & 0 & 0 & a_{n}
\end{array}\right|.
$$

### Solution 2.2-1(4)

By **Definition 2.2.1 ($n\times n$ Determinant)**, each term of the determinant is a product of $n$ entries from distinct rows and distinct columns.

By **Definition 2.2.1 ($n\times n$ Determinant)**, determine the unique nonzero entry row by row: row $1$ has only $a_{1}$ in column $n-1$ nonzero, row $2$ has only $a_{2}$ in column $n-2$ nonzero, $\cdots$, row $n-1$ has only $a_{n-1}$ in column $1$ nonzero, and row $n$ has only $a_{n}$ in column $n$ nonzero. Hence the only nonzero term is $a_{1}a_{2}\cdots a_{n}$.

By **Definition 2.2.1 ($n\times n$ Determinant)**, the column-index permutation of this nonzero term is $n-1,n-2,\cdots,1,n$, whose inversion number is

$$
\tau=\left(n-2\right)+\left(n-3\right)+\cdots+1+0=\frac{\left(n-1\right)\left(n-2\right)}{2}.
$$

By the sign convention in **Definition 2.2.1 ($n\times n$ Determinant)**, the determinant equals

$$
\left(-1\right)^{\frac{\left(n-1\right)\left(n-2\right)}{2}}a_{1}a_{2}\cdots a_{n}.
$$

$\blacksquare$

---

## 2.2-1(5)

Compute the following determinant by the definition:

$$
\left|\begin{array}{ccccc}
0 & 0 & 0 & 1 & 0\\
0 & 0 & 2 & 0 & 0\\
0 & 3 & 8 & 0 & 0\\
4 & 9 & 0 & 7 & 0\\
6 & 0 & 0 & 0 & 5
\end{array}\right|.
$$

### Solution 2.2-1(5)

By **Definition 2.2.1 ($n\times n$ Determinant)**, each term of the determinant is a product of $n$ entries from distinct rows and distinct columns.

By **Definition 2.2.1 ($n\times n$ Determinant)**, determine the unique nonzero entry row by row:

- row $1$: only the entry $1$ in column $4$ is nonzero, so take $\left(1,4\right)=1$;
- row $2$: only the entry $2$ in column $3$ is nonzero, so take $\left(2,3\right)=2$;
- row $3$: column $3$ is already taken, so one can only take $\left(3,2\right)=3$;
- row $4$: columns $2$ and $4$ are already taken, so one can only take $\left(4,1\right)=4$;
- row $5$: column $1$ is already taken, so one can only take $\left(5,5\right)=5$.

Hence the only nonzero term is $1\times2\times3\times4\times5=120$.

By **Definition 2.2.1 ($n\times n$ Determinant)**, the column-index permutation of this nonzero term is $4,3,2,1,5$, whose inversion number is

$$
\tau\left(4,3,2,1,5\right)=3+2+1+0+0=6.
$$

By the sign convention in **Definition 2.2.1 ($n\times n$ Determinant)**, an even permutation carries a plus sign, so the determinant equals

$$
\left(-1\right)^{6}\times120=120.
$$

$\blacksquare$

---

## 2.2-3

Compute by the definition of the determinant:

$$
\left|\begin{array}{ccccc}
a_{1} & a_{2} & a_{3} & a_{4} & a_{5}\\
b_{1} & b_{2} & b_{3} & b_{4} & b_{5}\\
c_{1} & c_{2} & 0 & 0 & 0\\
d_{1} & d_{2} & 0 & 0 & 0\\
e_{1} & e_{2} & 0 & 0 & 0
\end{array}\right|.
$$

### Solution 2.2-3

By **Definition 2.2.1 ($n\times n$ Determinant)**, each term of the determinant is a product of $n$ entries from distinct rows and distinct columns.

By **Definition 2.2.1 ($n\times n$ Determinant)**, in rows $3,4,5$ only the entries in columns $1$ and $2$ are nonzero. According to **Definition 2.2.1 ($n\times n$ Determinant)**, the entries chosen from these three rows must come from distinct columns, but there are only $2$ columns available; to choose $3$ entries from distinct columns, by **Basic Knowledge: The Pigeonhole Principle**, two rows must choose entries from the same column, contradicting the requirement of "distinct columns" in **Definition 2.2.1 ($n\times n$ Determinant)**.

Therefore there is no nonzero term satisfying the conditions, and the determinant equals $0$.

$\blacksquare$

---

## 2.2-5

Write out the term containing $x^{4}$ and the term containing $x^{3}$ in the following determinant:

$$
\left|\begin{array}{rrrr}
5x & x & 1 & x\\
1 & x & 1 & -1\\
3 & 2 & x & 1\\
3 & 1 & 1 & x
\end{array}\right|.
$$

### Solution 2.2-5

By **Definition 2.2.1 ($n\times n$ Determinant)**, each term of the determinant is a product of $n$ entries from distinct rows and distinct columns, and the sign of a term is determined by the inversion number of its column-index permutation.

**The term containing $x^{4}$.** To obtain $x^{4}$, all $4$ entries must contain $x$. The positions containing $x$ are

$$
\left(1,1\right)=5x,\left(1,2\right)=x,\left(1,4\right)=x,\left(2,2\right)=x,\left(3,3\right)=x,\left(4,4\right)=x.
$$

Each of rows $2,3,4$ has only one position containing $x$, namely $\left(2,2\right),\left(3,3\right),\left(4,4\right)$, which by **Definition 2.2.1 ($n\times n$ Determinant)** must all be taken. Then columns $2,3,4$ are already used, so row $1$ can only take $\left(1,1\right)=5x$. The column-index permutation is $1,2,3,4$, with inversion number $\tau=0$, an even permutation carrying a plus sign.

Hence the term containing $x^{4}$ is $5x^{4}$.

**The term containing $x^{3}$.** To obtain $x^{3}$, one needs $3$ entries containing $x$ and $1$ entry not containing $x$. Enumerate all valid combinations:

(1) Take

$$
\left(1,2\right)=x,\left(3,3\right)=x,\left(4,4\right)=x,
$$

and take the entry not containing $x$, namely $\left(2,1\right)=1$, from row $2$. The column indices are $2,1,3,4$, with inversion number $\tau=1$, an odd permutation carrying a minus sign, so the term is $-x^{3}$.

(2) Take

$$
\left(1,4\right)=x,\left(2,2\right)=x,\left(3,3\right)=x,
$$

and take the entry not containing $x$, namely $\left(4,1\right)=3$, from row $4$. The column indices are $4,2,3,1$, with inversion number $\tau=5$, an odd permutation carrying a minus sign, so the term is $-3x^{3}$.

All other combinations are invalid due to column conflicts, failing the "distinct columns" requirement in **Definition 2.2.1 ($n\times n$ Determinant)**.

Hence the terms containing $x^{3}$ are $-x^{3}-3x^{3}=-4x^{3}$.

$\blacksquare$
