# week19

> **Definition 4.2.2 (Upper/Lower Triangular Matrix)**<br>A square matrix whose entries below (above) the main diagonal are all zero is called an upper (lower) triangular matrix.

> **Definition 4.2.3 (Elementary Matrix Unit)**<br>A matrix with exactly one entry equal to $1$ and all other entries equal to $0$ is called a matrix unit. The matrix unit whose $\left(i,j\right)$-entry is $1$ is denoted $E_{ij}$.

> **Definition 4.2.5 (Symmetric Matrix)**<br>A matrix $A$ satisfying $A^{\top}=A$ is called a symmetric matrix.

> **Definition 4.2.6 (Skew-Symmetric Matrix)**<br>A matrix $A$ satisfying $A^{\top}=-A$ is called a skew-symmetric matrix.

---

## 4.2-2

Prove: the product of two $n\times n$ lower triangular matrices is still an $n\times n$ lower triangular matrix, and the diagonal entries of the product equal the products of the corresponding diagonal entries of the factors.

### Solution 4.2-2

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

---

## 4.2-3

Prove: a matrix that commutes with every $n\times n$ matrix must be an $n\times n$ scalar matrix.

### Solution 4.2-3

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

---

## 4.2-8

Prove: over a number field $K$, every $n\times n$ matrix can be written as the sum of a symmetric matrix and a skew-symmetric matrix, and this representation is unique.

### Solution 4.2-8

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

---

## 4.2-9

Prove: if $A$ is an $n\times n$ real symmetric matrix and $A^{2}=0$, then $A=0$.

### Solution 4.2-9

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

---

## 4.2-10

Prove: the determinant of an odd-order skew-symmetric matrix over a number field $K$ is zero.

### Solution 4.2-10

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
