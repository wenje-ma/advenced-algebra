# week9

> **Basic Knowledge: Block Upper-Triangular Determinant**<br>Here $A,B$ are both square matrices:

$$
\left|\begin{array}{cc}A & 0\\C & B\end{array}\right|=\left|A\right|\left|B\right|.
$$

> **Basic Knowledge: Formula for the Vandermonde Determinant**<br>The $n\times n$ Vandermonde determinant in $a_{1},a_{2},\cdots,a_{n}$

$$
\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{1} & a_{2} & \cdots & a_{n}\\
a_{1}^{2} & a_{2}^{2} & \cdots & a_{n}^{2}\\
\vdots & \vdots & & \vdots\\
a_{1}^{n-1} & a_{2}^{n-1} & \cdots & a_{n}^{n-1}
\end{array}\right|=\prod_{1\le i< j\le n}\left(a_{j}-a_{i}\right).
$$

> **Theorem 2.6.1 (Laplace Expansion Theorem)**<br>In an $n\times n$ determinant $\left|A\right|$, fix $k$ rows; then the sum of the products of all $k$-minors formed by the entries in these $k$ rows and their own cofactors equals $\left|A\right|$.

---

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

### Solution 2.6-3

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

---

## 2.6-4(1)

Let $\left|A\right|$ be the Vandermonde determinant in the $n$ numbers $1,2,\cdots,n$. Compute

$$
A\begin{bmatrix}1,2,\cdots,n-1\\2,3,\cdots,n\end{bmatrix}.
$$

### Solution 2.6-4(1)

By **Basic Knowledge: Formula for the Vandermonde Determinant**, the Vandermonde determinant is

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

This is the $\left(n-1\right)$-Vandermonde determinant in $a_{2},a_{3},\cdots,a_{n}$; by **Basic Knowledge: Formula for the Vandermonde Determinant**, its value is

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
