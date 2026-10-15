ï»¿ï»¿# Assignment 9

> **Theorem 1** (Laplace's Theorem)<br>In the $n$-th order determinant $\left|A\right|$, fix $k$ rows; then the sum of the products of all $k$-th order minors formed by the elements of these $k$ rows with their own cofactors equals $\left|A\right|$.

> **Basic Knowledge 1** (Block Determinants)<br>where $A,B$ are both square matrices:
>
> $$
> \left|\begin{array}{cc}A & 0\\C & B\end{array}\right|=\left|A\right|\left|B\right|
> $$

### Problem 1

(Problem 2.6-3) Compute the following determinant:

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

### Solution to Problem 1

By **Theorem 1** (Laplace's Theorem), expand along the first $k$ rows. Among all the $k$-th order minors of the first $k$ rows, only the upper-right $k$-th order minor $A=\left(a_{ij}\right)_{k\times k}$ can be nonzero (because the first $r$ columns of the first $k$ rows are all $0$).

The cofactor of the upper-right $k$-th order minor $A$: the row indices are $1,2,\cdots,k$, and the column indices are $r+1,r+2,\cdots,r+k$.

By **Theorem 1**, the minor is the $r$-th order determinant obtained by deleting the first $k$ rows and the last $k$ columns, namely $B=\left(b_{ij}\right)_{r\times r}$.

The cofactor is

$$
\left(-1\right)^{\left(1+2+\cdots+k\right)+\left(r+1+r+2+\cdots+r+k\right)}\cdot\left|B\right|
=\left(-1\right)^{\frac{k\left(k+1\right)}{2}+kr+\frac{k\left(k+1\right)}{2}}\cdot\left|B\right|
=\left(-1\right)^{k\left(k+1+r\right)}\cdot\left|B\right|.
$$

Hence the value of the determinant is

$$
\left|A\right|\cdot\left(-1\right)^{k\left(k+1+r\right)}\cdot\left|B\right|
=\left(-1\right)^{k\left(r+k+1\right)}\left|A\right|\left|B\right|.
$$

$\blacksquare$

### Problem 2

(Problem 2.6-4(1)) Let $\left|A\right|$ be the Vandermonde determinant of the $n$ numbers $1,2,\cdots,n$. Compute:

$$
A\begin{bmatrix}1,2,\cdots,n-1\\2,3,\cdots,n\end{bmatrix}.
$$

### Solution to Problem 2

The Vandermonde determinant is

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

Taking the $1,2,\cdots,n-1$-th rows (namely the rows of powers $0$ through $n-2$) and the $2,3,\cdots,n$-th columns (namely the columns $a_{2},a_{3},\cdots,a_{n}$), the resulting $n-1$-th order minor is

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

This is the $n-1$-th order Vandermonde determinant of $a_{2},a_{3},\cdots,a_{n}$, and its value is

$$
\prod_{2\le i<j\le n}\left(a_{j}-a_{i}\right)=\prod_{2\le i<j\le n}\left(j-i\right).
$$

Let $d=j-i$; then $d=1,2,\cdots,n-2$, and for each $d$ there are $n-1-d$ pairs $\left(i,j\right)$ satisfying $j-i=d$.

Hence

$$
\prod_{2\le i<j\le n}\left(j-i\right)=\prod_{d=1}^{n-2}d^{n-1-d}
=1^{n-2}\cdot2^{n-3}\cdot\cdots\cdot\left(n-2\right)^{1}.
$$

$\blacksquare$
