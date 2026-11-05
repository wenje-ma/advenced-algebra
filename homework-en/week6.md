# week6

$$
\left|\begin{array}{cc}A & 0\\C & B\end{array}\right|=\left|A\right|\left|B\right|.
$$
$$
\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{1} & a_{2} & \cdots & a_{n}\\
a_{1}^{2} & a_{2}^{2} & \cdots & a_{n}^{2}\\
\vdots & \vdots & & \vdots\\
a_{1}^{n-1} & a_{2}^{n-1} & \cdots & a_{n}^{n-1}
\end{array}\right|=\prod_{1\le i< j\le n}\left(a_{j}-a_{i}\right).
$$

> **Theorem 2.6.1 (Laplace Expansion Theorem)**
> 
> In an $n\times n$ determinant $\left|A\right|$, fix $k$ rows; then the sum of the products of all $k$-minors formed by the entries in these $k$ rows and their own cofactors equals $\left|A\right|$.

> **Definition 3.1.1 (Linear Combination and Linear Representation)**
> 
> In $K^{n}$, given a vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ and any numbers $k_{1},k_{2},\cdots,k_{s}$ in $K$, we call $k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s}$ a linear combination of the vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$. If

$$
\beta=k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s},
$$
then we say that $\beta$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$.

> **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**
> 
> An $n$-variable linear system over a number field $K$

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$
is solvable $\Leftrightarrow$ $\beta$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ $\Leftrightarrow$ $\beta\in\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\right\rangle$.

## 2.6-3

Compute the following determinant:

$$
\left|\begin{array}{cccccc}
0 & \cdots & 0 & a_{11} & \cdots & a_{1k}\\
\vdots & & \vdots & \vdots & & \vdots\\
0 & \cdots & 0 & a_{k1} & \cdots & a_{kk}\\
b_{11} & \cdots & b_{1r} & c_{11} & \cdots & c_{1k}\\
\vdots & & \vdots & \vdots & & \vdots\\
b_{r1} & \cdots & b_{rr} & c_{r1} & \cdots & c_{rk}
\end{array}\right|.
$$

### Solution to 2.6-3

By **Theorem 2.6.1 (Laplace Expansion Theorem)**, expand along the first $k$ rows. Among all $k$-minors of the first $k$ rows, only the upper-right $k$-minor $A=\left(a_{ij}\right)_{k\times k}$ can be nonzero (because the first $r$ columns of the first $k$ rows are all $0$).

The cofactor of the upper-right $k$-minor $A$: its row indices are $1,2,\cdots,k$ and its column indices are $r+1,r+2,\cdots,r+k$.

By **Theorem 2.6.1 (Laplace Expansion Theorem)**, the minor is the $r$-determinant after deleting the first $k$ rows and the last $k$ columns, namely $B=\left(b_{ij}\right)_{r\times r}$.

The cofactor is

$$
\left(-1\right)^{\left(1+2+\cdots+k\right)+\left(r+1+r+2+\cdots+r+k\right)}\cdot\left|B\right|
=\left(-1\right)^{\frac{k\left(k+1\right)}{2}+kr+\frac{k\left(k+1\right)}{2}}\cdot\left|B\right|
=\left(-1\right)^{k\left(k+1+r\right)}\cdot\left|B\right|.
$$

Hence the determinant equals

$$
\left|A\right|\cdot\left(-1\right)^{k\left(k+1+r\right)}\cdot\left|B\right|
=\left(-1\right)^{k\left(r+k+1\right)}\left|A\right|\left|B\right|.
$$

$\blacksquare$

## 2.6-4(1)

Let $\left|A\right|$ be the Vandermonde determinant in the $n$ numbers $1,2,\cdots,n$. Compute

$$
A\begin{bmatrix}1,2,\cdots,n-1\\2,3,\cdots,n\end{bmatrix}.
$$

### Solution to 2.6-4(1)

By Formula for the Vandermonde Determinant, the Vandermonde determinant is

$$
\left|A\right|=\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{1} & a_{2} & \cdots & a_{n}\\
a_{1}^{2} & a_{2}^{2} & \cdots & a_{n}^{2}\\
\vdots & \vdots & & \vdots\\
a_{1}^{n-1} & a_{2}^{n-1} & \cdots & a_{n}^{n-1}
\end{array}\right|,
$$

where $a_{i}=i$.

Taking rows $1,2,\cdots,n-1$ (namely the rows of powers $0$ through $n-2$) and columns $2,3,\cdots,n$ (namely the columns of $a_{2},a_{3},\cdots,a_{n}$), the resulting $\left(n-1\right)$-minor is

$$
A\begin{bmatrix}1,2,\cdots,n-1\\2,3,\cdots,n\end{bmatrix}
=\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{2} & a_{3} & \cdots & a_{n}\\
a_{2}^{2} & a_{3}^{2} & \cdots & a_{n}^{2}\\
\vdots & \vdots & & \vdots\\
a_{2}^{n-2} & a_{3}^{n-2} & \cdots & a_{n}^{n-2}
\end{array}\right|.
$$

This is the $\left(n-1\right)$-Vandermonde determinant in $a_{2},a_{3},\cdots,a_{n}$; by Formula for the Vandermonde Determinant, its value is

$$
\prod_{2\le i< j\le n}\left(a_{j}-a_{i}\right)=\prod_{2\le i< j\le n}\left(j-i\right).
$$

Let $d=j-i$; then $d=1,2,\cdots,n-2$, and for each $d$ there are $n-1-d$ pairs $\left(i,j\right)$ with $j-i=d$.

Hence

$$
\prod_{2\le i< j\le n}\left(j-i\right)=\prod_{d=1}^{n-2}d^{n-1-d}
=1^{n-2}\cdot2^{n-3}\cdot\cdots\cdot\left(n-2\right)^{1}.
$$

$\blacksquare$

## 3.1-3(1)

In $K^{4}$, determine whether the vector $\beta$ can be linearly represented by the vector group $\alpha_{1},\alpha_{2},\alpha_{3}$. If so, write down one way of representing it.

$$
\alpha_{1}=\begin{bmatrix}-1\\3\\0\\-5\end{bmatrix},
\alpha_{2}=\begin{bmatrix}2\\0\\7\\-3\end{bmatrix},
\alpha_{3}=\begin{bmatrix}-4\\1\\-2\\6\end{bmatrix},
\beta=\begin{bmatrix}8\\3\\-1\\-25\end{bmatrix}.
$$

### Solution to 3.1-3(1)

By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, to determine whether $\beta$ can be represented by $\alpha_{1},\alpha_{2},\alpha_{3}$ is to determine whether the linear system $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=\beta$ is solvable.

Write down the augmented matrix and perform elementary row operations:

$$
\left[\begin{array}{rrr\left|r}
-1 & 2 & -4 & 8\\
3 & 0 & 1 & 3\\
0 & 7 & -2 & -1\\
-5 & -3 & 6 & -25
\end{array}\right]
\xrightarrow{\substack{②+①\times3\\④-①\times5}}
\left[\begin{array}{rrr\right|r}
-1 & 2 & -4 & 8\\
0 & 6 & -11 & 27\\
0 & 7 & -2 & -1\\
0 & -13 & 26 & 15
\end{array}\right].
$$

Continuing the row operations, the last row becomes a contradictory row $0=80$, so the system has no solution.

By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, $\beta$ therefore cannot be linearly represented by $\alpha_{1},\alpha_{2},\alpha_{3}$. $\blacksquare$

## 3.1-3(3)

In $K^{4}$, determine whether the vector $\beta$ can be linearly represented by the vector group $\alpha_{1},\alpha_{2},\alpha_{3}$. If so, write down one way of representing it.

$$
\alpha_{1}=\begin{bmatrix}3\\-5\\2\\-4\end{bmatrix},
\alpha_{2}=\begin{bmatrix}-1\\7\\-3\\6\end{bmatrix},
\alpha_{3}=\begin{bmatrix}3\\11\\-5\\10\end{bmatrix},
\beta=\begin{bmatrix}2\\-30\\13\\-26\end{bmatrix}.
$$

### Solution to 3.1-3(3)

By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, to determine whether $\beta$ can be represented by $\alpha_{1},\alpha_{2},\alpha_{3}$ is to determine whether the linear system $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=\beta$ is solvable.

Write down the augmented matrix and perform elementary row operations:

$$
\left[\begin{array}{rrr\left|r}
3 & -1 & 3 & 2\\
-5 & 7 & 11 & -30\\
2 & -3 & -5 & 13\\
-4 & 6 & 10 & -26
\end{array}\right]
\xrightarrow{\substack{②+①\times5/3\\③-①\times2/3\\④+①\times4/3}}
\left[\begin{array}{rrr\right|r}
3 & -1 & 3 & 2\\
0 & 16/3 & 16 & -80/3\\
0 & -7/3 & -7 & 35/3\\
0 & 14/3 & 14 & -70/3
\end{array}\right].
$$

Note that rows $2,3,4$ are proportional; after elimination the echelon matrix has only two rows:

$$
\left[\begin{array}{rrr|r}
3 & -1 & 3 & 2\\
0 & 16/3 & 16 & -80/3
\end{array}\right].
$$

From row $2$:

$$
\frac{16}{3}x_{2}+16x_{3}=-\frac{80}{3},
$$

i.e. $x_{2}+3x_{3}=-5$, so $x_{2}=-5-3x_{3}$.

From row $1$: $3x_{1}-x_{2}+3x_{3}=2$; substituting $x_{2}$ gives $3x_{1}+6x_{3}=-3$, so $x_{1}=-1-2x_{3}$.

Setting $x_{3}=0$ gives $x_{1}=-1$, $x_{2}=-5$.

Verify:

$$
-\alpha_{1}-5\alpha_{2}=\begin{bmatrix}-3+5\\5-35\\-2+15\\4-30\end{bmatrix}=\begin{bmatrix}2\\-30\\13\\-26\end{bmatrix}=\beta.
$$

Hence $\beta=-\alpha_{1}-5\alpha_{2}$. By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, the system is solvable, so $\beta$ can be linearly represented by $\alpha_{1},\alpha_{2},\alpha_{3}$. $\blacksquare$

## 3.1-5

In $K^{4}$, let

$$
\alpha_{1}=\begin{bmatrix}1\\0\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}1\\1\\1\\0\end{bmatrix},
\alpha_{4}=\begin{bmatrix}1\\1\\1\\1\end{bmatrix}.
$$

Prove that every vector $\alpha=\left(a_{1},a_{2},a_{3},a_{4}\right)^{\top}$ in $K^{4}$ can be linearly represented by the vector group $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$, that this representation is unique, and write it down.

### Solution to 3.1-5

By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, to prove that every vector $\alpha$ in $K^{4}$ can be represented by $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ is to prove that the linear system

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}=\alpha
$$

is solvable.

Set

$$
\alpha=x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}.
$$

Comparing components:

$4$th component: $x_{4}=a_{4}$.

$3$rd component: $x_{3}+x_{4}=a_{3}$, so $x_{3}=a_{3}-a_{4}$.

$2$nd component: $x_{2}+x_{3}+x_{4}=a_{2}$, so $x_{2}=a_{2}-a_{3}$.

$1$st component: $x_{1}+x_{2}+x_{3}+x_{4}=a_{1}$, so $x_{1}=a_{1}-a_{2}$.

The above solving process is uniquely determined from bottom to top, so the representation is unique.

The representation is

$$
\alpha=\left(a_{1}-a_{2}\right)\alpha_{1}+\left(a_{2}-a_{3}\right)\alpha_{2}+\left(a_{3}-a_{4}\right)\alpha_{3}+a_{4}\alpha_{4}.
$$

The system has a unique solution, so $\alpha$ can be uniquely linearly represented by $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$. $\blacksquare$

## 3.1-8

Let $r< n$. Prove that the following subset $W$ of $K^{n}$ is a subspace:

$$
W=\left\{\left(a_{1},a_{2},\cdots,a_{r},0,\cdots,0\right)\mid a_{i}\in K,i=1,2,\cdots,r\right\}.
$$

### Solution to 3.1-8

By Criterion for a Subspace, it suffices to verify that $W$ is nonempty and closed under addition and scalar multiplication.

Verify closure under addition. Take any

$$
\alpha=\left(a_{1},\cdots,a_{r},0,\cdots,0\right),
\beta=\left(b_{1},\cdots,b_{r},0,\cdots,0\right)\in W.
$$

Then

$$
\alpha+\beta=\left(a_{1}+b_{1},\cdots,a_{r}+b_{r},0,\cdots,0\right)\in W.
$$

Verify closure under scalar multiplication. Take any

$$
\alpha=\left(a_{1},\cdots,a_{r},0,\cdots,0\right)\in W
$$

and $k\in K$.

Then

$$
k\alpha=\left(ka_{1},\cdots,ka_{r},0,\cdots,0\right)\in W.
$$

$W$ is nonempty (e.g. the zero vector $\left(0,\cdots,0\right)\in W$).

By Criterion for a Subspace, $W$ is a subspace of $K^{n}$. $\blacksquare$
