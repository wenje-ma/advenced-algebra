# week3

> **Definition 2.2.1 ($n\times n$ Determinant)**
> 
> An $n\times n$ determinant is an algebraic sum of $n!$ terms, each term being a product of $n$ entries from distinct rows and distinct columns; after these $n$ entries are arranged so that their row indices are in natural order, the term carries a plus sign when the permutation formed by the column indices is even and a minus sign when it is odd. Namely,

> **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**
> 
> A common factor of a row of a determinant can be pulled outside the determinant; in particular, if a row of a determinant is zero (all its entries are $0$), then the determinant is $0$.

> **Property 2.3.3 (Splitting When a Row Is a Sum of Two Groups)**
> 
> If a row of a determinant is the sum of two groups of numbers, then the determinant equals the sum of two determinants: in these two determinants that row is respectively the first group and the second group of numbers, while all other rows are the same as the corresponding rows of the original determinant.

> **Property 2.3.5 (Two Identical Rows Make the Determinant Zero)**
> 
> If a determinant has two identical rows, its value is $0$; consequently, if two rows are proportional, the determinant is also $0$.

> **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**
> 
> Adding a multiple of one row to another row leaves the value of the determinant unchanged.

> **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**
> 
> The $n\times n$ determinant $\left|A\right|$ equals the sum of the products of the entries in its $i$-th row and their cofactors:

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

### Solution to 2.2-1(4)

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

### Solution to 2.2-1(5)

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

### Solution to 2.2-3

By **Definition 2.2.1 ($n\times n$ Determinant)**, each term of the determinant is a product of $n$ entries from distinct rows and distinct columns.

By **Definition 2.2.1 ($n\times n$ Determinant)**, in rows $3,4,5$ only the entries in columns $1$ and $2$ are nonzero. According to **Definition 2.2.1 ($n\times n$ Determinant)**, the entries chosen from these three rows must come from distinct columns, but there are only $2$ columns available; to choose $3$ entries from distinct columns, by The Pigeonhole Principle, two rows must choose entries from the same column, contradicting the requirement of "distinct columns" in **Definition 2.2.1 ($n\times n$ Determinant)**.

Therefore there is no nonzero term satisfying the conditions, and the determinant equals $0$.

$\blacksquare$

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

### Solution to 2.2-5

By **Definition 2.2.1 ($n\times n$ Determinant)**, each term of the determinant is a product of $n$ entries from distinct rows and distinct columns, and the sign of a term is determined by the inversion number of its column-index permutation.

The term containing $x^{4}$. To obtain $x^{4}$, all $4$ entries must contain $x$. The positions containing $x$ are

$$
\left(1,1\right)=5x,\left(1,2\right)=x,\left(1,4\right)=x,\left(2,2\right)=x,\left(3,3\right)=x,\left(4,4\right)=x.
$$

Each of rows $2,3,4$ has only one position containing $x$, namely $\left(2,2\right),\left(3,3\right),\left(4,4\right)$, which by **Definition 2.2.1 ($n\times n$ Determinant)** must all be taken. Then columns $2,3,4$ are already used, so row $1$ can only take $\left(1,1\right)=5x$. The column-index permutation is $1,2,3,4$, with inversion number $\tau=0$, an even permutation carrying a plus sign.

Hence the term containing $x^{4}$ is $5x^{4}$.

The term containing $x^{3}$. To obtain $x^{3}$, one needs $3$ entries containing $x$ and $1$ entry not containing $x$. Enumerate all valid combinations:

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

## 2.3-1(2)

Compute the following determinant:

$$
\left|\begin{array}{rrr}
-1 & 203 & 1/3\\
3 & 298 & 1/2\\
5 & 399 & 2/3
\end{array}\right|.
$$

### Solution to 2.3-1(2)

Observe that the entries $203,298,399$ of the $2$nd column can be split into sums of two numbers, namely $203=200+3$, $298=300-2$, $399=400-1$. By **Property 2.3.3 (Splitting When a Row Is a Sum of Two Groups)**, when all entries of a column are sums of two terms, the determinant can be split into the sum of two determinants:

$$
\left|\begin{array}{rrr}
-1 & 203 & 1/3\\
3 & 298 & 1/2\\
5 & 399 & 2/3
\end{array}\right|
=
\left|\begin{array}{rrr}
-1 & 200 & 1/3\\
3 & 300 & 1/2\\
5 & 400 & 2/3
\end{array}\right|
+
\left|\begin{array}{rrr}
-1 & 3 & 1/3\\
3 & -2 & 1/2\\
5 & -1 & 2/3
\end{array}\right|.
$$

By **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**, a common factor of a column can be moved outside the determinant. The $2$nd column of the first determinant has a common factor $100$; pulling it out gives

$$
D_{1}=100\times\left|\begin{array}{rrr}
-1 & 2 & 1/3\\
3 & 3 & 1/2\\
5 & 4 & 2/3
\end{array}\right|.
$$

Expanding directly,

$$
\left|\begin{array}{rrr}
-1 & 2 & 1/3\\
3 & 3 & 1/2\\
5 & 4 & 2/3
\end{array}\right|=-1\times\left(3\times\frac{2}{3}-\frac{1}{2}\times4\right)-2\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times4-3\times5\right)=-1\times\left(2-2\right)-2\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(12-15\right)=0-2\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times\left(-3\right)=1-1=0.
$$

Hence $D_{1}=100\times0=0$.

Compute the second determinant $D_{2}$:

$$
D_{2}=\left|\begin{array}{rrr}
-1 & 3 & 1/3\\
3 & -2 & 1/2\\
5 & -1 & 2/3
\end{array}\right|=-1\times\left(-2\times\frac{2}{3}-\frac{1}{2}\times\left(-1\right)\right)-3\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times\left(-1\right)-\left(-2\right)\times5\right)=-1\times\left(-\frac{4}{3}+\frac{1}{2}\right)-3\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(-3+10\right)=-1\times\left(-\frac{5}{6}\right)-3\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times7=\frac{5}{6}+\frac{3}{2}+\frac{7}{3}=\frac{5}{6}+\frac{9}{6}+\frac{14}{6}=\frac{28}{6}=\frac{14}{3}.
$$

Hence the original determinant is

$$
D=D_{1}+D_{2}=0+\frac{14}{3}=\frac{14}{3}.
$$

$\blacksquare$

## 2.3-2(2)

Compute the following $n\times n$ determinant:

$$
\left|\begin{array}{cccc}
a_{1}-b & a_{2} & \cdots & a_{n}\\
a_{1} & a_{2}-b & \cdots & a_{n}\\
\vdots & \vdots & & \vdots\\
a_{1} & a_{2} & \cdots & a_{n}-b
\end{array}\right|.
$$

### Solution to 2.3-2(2)

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, adding a multiple of one row to another leaves the determinant unchanged. Add $-1$ times the $n$-th row respectively to rows $1,2,\cdots,n-1$, giving

$$
\left|\begin{array}{rrrrr}
-b & 0 & \cdots & 0 & b\\
0 & -b & \cdots & 0 & b\\
\vdots & \vdots & & \vdots & \vdots\\
0 & 0 & \cdots & -b & b\\
a_{1} & a_{2} & \cdots & a_{n-1} & a_{n}-b
\end{array}\right|.
$$

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along the last column. The entries of the last column are $\left(b,b,\cdots,b,a_{n}-b\right)$.

For $j< n$, the cofactor is $A_{jn}=\left(-1\right)^{j+n}M_{jn}$, where $M_{jn}$ is the $\left(n-1\right)$-determinant obtained by deleting row $j$ and column $n$. In that determinant, row $j$ (the original row $j$ with column $n$ removed) has only its first entry $b_{j}$ nonzero and all others $0$; expanding along that row, the minor is a diagonal determinant, giving $M_{jn}=\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}$.

Hence

$$
\text{determinant}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{j+n}\cdot\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-1\right)^{2n}\left(-b\right)^{n-1}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{2j+n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\left(-1\right)^{n-1}b^{n-1}\sum_{j=1}^{n-1}a_{j}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\left(-b\right)^{n-1}\left(\sum_{j=1}^{n}a_{j}-b\right).
$$

$\blacksquare$
