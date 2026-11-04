# week12

> **Definition 4.1.1 (Matrix Addition)**
> 
> Let $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ both be $s\times n$ matrices over a number field $K$, and set $C=\left(a_{ij}+b_{ij}\right)_{s\times n}$. Then $C$ is called the sum of the matrices $A$ and $B$, denoted $C=A+B$.

> **Definition 4.1.2 (Scalar Multiplication of Matrices)**
> 
> Let $k\in K$ and set $M=\left(ka_{ij}\right)_{s\times n}$. Then $M$ is called the scalar product of $k$ and the matrix $A$, denoted $M=kA$.

> **Definition 4.1.3 (Matrix Multiplication)**
> 
> Let $A=\left(a_{ij}\right)_{s\times n}$ and $B=\left(b_{ij}\right)_{n\times m}$, and set $C=\left(c_{ij}\right)_{s\times m}$ with $c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}$. Then $C$ is called the product of $A$ and $B$, denoted $C=AB$.

> **Definition 4.2.2 (Upper/Lower Triangular Matrix)**
> 
> A square matrix whose entries below (above) the main diagonal are all zero is called an upper (lower) triangular matrix.

> **Definition 4.2.3 (Elementary Matrix Unit)**
> 
> A matrix with exactly one entry equal to $1$ and all other entries equal to $0$ is called a matrix unit. The matrix unit whose $\left(i,j\right)$-entry is $1$ is denoted $E_{ij}$.

> **Definition 4.2.5 (Symmetric Matrix)**
> 
> A matrix $A$ satisfying $A^{\top}=A$ is called a symmetric matrix.

> **Definition 4.2.6 (Skew-Symmetric Matrix)**
> 
> A matrix $A$ satisfying $A^{\top}=-A$ is called a skew-symmetric matrix.

$$
\left|\begin{array}{ccc}
1 & 1 & 1\\
x_{1} & x_{2} & x_{3}\\
x_{1}^{2} & x_{2}^{2} & x_{3}^{2}
\end{array}\right|=\left(x_{2}-x_{1}\right)\left(x_{3}-x_{1}\right)\left(x_{3}-x_{2}\right).
$$

> **Theorem 4.3.1 (Rank of a Matrix Product)**
> 
> Let $A=\left(a_{ij}\right)_{s\times n}$ and $B=\left(b_{ij}\right)_{n\times m}$. Then

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

> **Proposition 4.3.2 (Over $\mathbb{R}$, $A^{\top}Az=0$ Has the Same Solutions as $z=0$)**
> 
> Let $A$ be a matrix over the real number field. Then the homogeneous system $A^{\top}Az=0$ and $z=0$ have the same solutions.

> **Theorem 4.3.3 (Determinant of a Product)**
> 
> Let $A,B$ both be $n\times n$ matrices. Then $\left|AB\right|=\left|A\right|\left|B\right|$.

## 4.1-6

Compute:

$$
\left(x,y,1\right)\left[\begin{array}{ccc}
a_{11} & a_{12} & a_{1}\\
a_{12} & a_{22} & a_{2}\\
a_{1} & a_{2} & a_{0}
\end{array}\right]\left[\begin{array}{c}
x\\
y\\
1
\end{array}\right].
$$

### Solution to 4.1-6

By **Definition 4.1.3 (Matrix Multiplication)**, first multiply the row vector on the left by the matrix:

$$
\left(x,y,1\right)M
=
\left(a_{11}x+a_{12}y+a_{1},a_{12}x+a_{22}y+a_{2},a_{1}x+a_{2}y+a_{0}\right).
$$

Then multiply by the column vector:

$$
=\left(a_{11}x+a_{12}y+a_{1}\right)x+\left(a_{12}x+a_{22}y+a_{2}\right)y+\left(a_{1}x+a_{2}y+a_{0}\right)=a_{11}x^{2}+2a_{12}xy+a_{22}y^{2}+2a_{1}x+2a_{2}y+a_{0}.
$$

$\blacksquare$

## 4.1-7(5)

Compute:

$$
\left[\begin{array}{ccc}
0 & 1 & 0\\
0 & 0 & 1\\
0 & 0 & 0
\end{array}\right]^{n},\text{ where }n\text{ is a positive integer}.
$$

### Solution to 4.1-7(5)

By **Definition 4.1.3 (Matrix Multiplication)**, write

$$
H=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right].
$$

$$
H^{2}=HH=\left[\begin{array}{ccc}
0 & 0 & 1\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

$$
H^{3}=H^{2}H=\left[\begin{array}{ccc}
0 & 0 & 0\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

Therefore:

- when $n=1$, $H^{n}=H=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right]$;
- when $n=2$, $H^{n}=\left[\begin{array}{ccc}0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]$;
- when $n\ge3$, $H^{n}=0$.

$\blacksquare$

## 4.1-7(6)

Compute:

$$
\left[\begin{array}{ccc}
\lambda & 1 & 0\\
0 & \lambda & 1\\
0 & 0 & \lambda
\end{array}\right]^{n},\text{ where }n\text{ is a positive integer}.
$$

### Solution to 4.1-7(6)

By **Definition 4.1.3 (Matrix Multiplication)**, write $A=\lambda I+N$, where

$$
N=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right].
$$

Because $\lambda I$ and $N$ commute, by Matrix Binomial Theorem,

$$
A^{n}=\sum_{k=0}^{n}\binom{n}{k}\left(\lambda I\right)^{n-k}N^{k}.
$$

Also $N^{0}=I$, $N^{1}=N$, $N^{2}=\left[\begin{array}{ccc}0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]$, $N^{3}=0$.

Hence

$$
A^{n}
=\lambda^{n}I+n\lambda^{n-1}N+\binom{n}{2}\lambda^{n-2}N^{2}=\left[\begin{array}{ccc}
\lambda^{n} & n\lambda^{n-1} & \frac{n\left(n-1\right)}{2}\lambda^{n-2}\\
0 & \lambda^{n} & n\lambda^{n-1}\\
0 & 0 & \lambda^{n}
\end{array}\right].
$$

When $n=1$, the above also holds (note $\lambda^{0}=1$, and the third term is $0$). $\blacksquare$

## 4.1-10

Prove: if $A=\frac{1}{2}\left(B+I\right)$, then $A^{2}=A$ if and only if $B^{2}=I$.

### Solution to 4.1-10

$$
A^{2}=\left(\frac{1}{2}\left(B+I\right)\right)^{2}=\frac{1}{4}\left(B+I\right)^{2}=\frac{1}{4}\left(B^{2}+2B+I\right).
$$

$A^{2}=A$ is equivalent to

$$
\frac{1}{4}\left(B^{2}+2B+I\right)=\frac{1}{2}\left(B+I\right).
$$

Multiplying both sides by $4$:

$$
B^{2}+2B+I=2B+2I.
$$

Simplifying:

$$
B^{2}=I.
$$

Therefore $A^{2}=A$ if and only if $B^{2}=I$. $\blacksquare$

## 4.2-2

Prove: the product of two $n\times n$ lower triangular matrices is still an $n\times n$ lower triangular matrix, and the diagonal entries of the product equal the products of the corresponding diagonal entries of the factors.

### Solution to 4.2-2

By **Definition 4.2.2 (Upper/Lower Triangular Matrix)**, let $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ both be $n\times n$ lower triangular matrices, i.e. $a_{ij}=0,b_{ij}=0$ whenever $i< j$.

Set $C=AB=\left(c_{ij}\right)$; then

$$
c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}.
$$

**Lower triangularity.** When $i< j$:

- if $k\le i< j$, then $k< j$, so $b_{kj}=0$;
- if $k> i$, then $a_{ik}=0$.

Hence every term is $0$, so $c_{ij}=0$ (when $i< j$). By **Definition 4.2.2 (Upper/Lower Triangular Matrix)**, $C$ is therefore a lower triangular matrix.

**Diagonal entries.** When $i=j$:

- if $k< i$, then $b_{ki}=0$;
- if $k> i$, then $a_{ik}=0$.

Hence only the term $k=i$ is nonzero:

$$
c_{ii}=a_{ii}b_{ii}.
$$

$\blacksquare$

## 4.2-3

Prove: a matrix that commutes with every $n\times n$ matrix must be an $n\times n$ scalar matrix.

### Solution to 4.2-3

Let $A=\left(a_{ij}\right)$ commute with every $n\times n$ matrix.

Take the matrix unit $E_{ij}$ of **Definition 4.2.3 (Elementary Matrix Unit)** (its $\left(i,j\right)$-entry is $1$ and all others are $0$). Then $AE_{ij}=E_{ij}A$.

Column $j$ of $AE_{ij}$ equals column $i$ of $A$, and its other columns are $0$.

Row $i$ of $E_{ij}A$ equals row $j$ of $A$, and its other rows are $0$.

Comparing their $\left(i,j\right)$-entries:

the $\left(i,j\right)$-entry of $AE_{ij}$ $=a_{ii}$;

the $\left(i,j\right)$-entry of $E_{ij}A$ $=a_{jj}$.

Hence $a_{ii}=a_{jj}$.

This holds for all $i,j$, so all diagonal entries are equal:

$$
a_{11}=a_{22}=\cdots=a_{nn}=k.
$$

Now compare the $\left(k,j\right)$-entry (with $k\ne i$):

the $\left(k,j\right)$-entry of $AE_{ij}$ $=a_{ki}$;

the $\left(k,j\right)$-entry of $E_{ij}A$ $=0$ (because $k\ne i$).

Hence $a_{ki}=0$ (when $k\ne i$).

This holds for all $i$, so all off-diagonal entries of $A$ are $0$.

Therefore $A=kI$, i.e. $A$ is a scalar matrix. $\blacksquare$

## 4.2-8

Prove: over a number field $K$, every $n\times n$ matrix can be written as the sum of a symmetric matrix and a skew-symmetric matrix, and this representation is unique.

### Solution to 4.2-8

Let $A$ be any $n\times n$ matrix. Set

$$
S=\frac{1}{2}\left(A+A^{\top}\right),
K=\frac{1}{2}\left(A-A^{\top}\right).
$$

Then $A=S+K$.

$$
S^{\top}=\frac{1}{2}\left(A^{\top}+\left(A^{\top}\right)^{\top}\right)=\frac{1}{2}\left(A^{\top}+A\right)=S.
$$

By **Definition 4.2.5 (Symmetric Matrix)**, $S$ is therefore symmetric.

$$
K^{\top}=\frac{1}{2}\left(A^{\top}-\left(A^{\top}\right)^{\top}\right)=\frac{1}{2}\left(A^{\top}-A\right)=-K.
$$

By **Definition 4.2.6 (Skew-Symmetric Matrix)**, $K$ is therefore skew-symmetric.

**Uniqueness.** Suppose $A=S_{1}+K_{1}=S_{2}+K_{2}$, where $S_{1},S_{2}$ are symmetric and $K_{1},K_{2}$ are skew-symmetric.

Then $S_{1}-S_{2}=K_{2}-K_{1}$.

The left side $\left(S_{1}-S_{2}\right)^{\top}=S_{1}-S_{2}$ is symmetric.

The right side

$$
\left(K_{2}-K_{1}\right)^{\top}=-K_{2}+K_{1}=-\left(K_{2}-K_{1}\right)
$$

is skew-symmetric.

A matrix that is both symmetric and skew-symmetric must be the zero matrix.

Hence $S_{1}-S_{2}=0$ and $K_{2}-K_{1}=0$, i.e. $S_{1}=S_{2}$ and $K_{1}=K_{2}$.

The representation is unique. $\blacksquare$

## 4.2-9

Prove: if $A$ is an $n\times n$ real symmetric matrix and $A^{2}=0$, then $A=0$.

### Solution to 4.2-9

Let $A=\left(a_{ij}\right)$ be a real symmetric matrix with $A^{2}=0$.

Consider the diagonal entries of $A^{2}$:

$$
\left(A^{2}\right)_{ii}=\sum_{k=1}^{n}a_{ik}a_{ki}.
$$

By **Definition 4.2.5 (Symmetric Matrix)**, $A$ is symmetric, so $a_{ki}=a_{ik}$.

Hence

$$
\left(A^{2}\right)_{ii}=\sum_{k=1}^{n}a_{ik}^{2}.
$$

Since $A^{2}=0$, $\left(A^{2}\right)_{ii}=0$, i.e.

$$
\sum_{k=1}^{n}a_{ik}^{2}=0.
$$

Since the $a_{ik}$ are all real, $a_{ik}^{2}\ge0$.

Therefore each $a_{ik}=0$, i.e. $A=0$. $\blacksquare$

## 4.2-10

Prove: the determinant of an odd-order skew-symmetric matrix over a number field $K$ is zero.

### Solution to 4.2-10

Let $A$ be an $n\times n$ skew-symmetric matrix with $n$ odd.

By **Definition 4.2.6 (Skew-Symmetric Matrix)**, $A^{\top}=-A$.

$$
\left|A^{\top}\right|=\left|-A\right|.
$$

Since $\left|A^{\top}\right|=\left|A\right|$ and $\left|-A\right|=\left(-1\right)^{n}\left|A\right|$,

$$
\left|A\right|=\left(-1\right)^{n}\left|A\right|.
$$

Since $n$ is odd, $\left(-1\right)^{n}=-1$.

Therefore

$$
\left|A\right|=-\left|A\right|\Rightarrow 2\left|A\right|=0\Rightarrow \left|A\right|=0.
$$

$\blacksquare$

## 4.3-2

A matrix is called row (column) full-rank if its row (column) vector group is linearly independent. Prove: if an $s\times n$ matrix $A$ has rank $r$, then there exist an $s\times r$ column full-rank matrix $B$ and an $r\times n$ row full-rank matrix $C$ such that $A=BC$.

### Solution to 4.3-2

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
