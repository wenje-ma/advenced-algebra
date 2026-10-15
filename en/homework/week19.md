# Assignment 19

> **Definition 2** (Upper/lower triangular matrix)<br>A square matrix whose entries below (above) the main diagonal are all zero is called an upper (lower) triangular matrix.

### Problem 1

(Problem 4.2-2) Prove: the product of two $n$-th order lower triangular matrices is again an $n$-th order lower triangular matrix, and the diagonal entries of the product equal the product of the corresponding diagonal entries of the factors.

### Solution to Problem 1

By **Definition 2** (Upper/lower triangular matrix), let $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ both be $n$-th order lower triangular matrices, i.e., when $i<j$, $a_{ij}=0,b_{ij}=0$.

Let $C=AB=\left(c_{ij}\right)$. Then

$$
c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}
$$

**Lower triangular property.** When $i<j$:

- If $k\le i<j$, then $k<j$, so $b_{kj}=0$.
- If $k>i$, then $a_{ik}=0$.

Therefore all terms are $0$, so $c_{ij}=0$ (when $i<j$). By **Definition 2**, $C$ is a lower triangular matrix.

**Diagonal entries.** When $i=j$:

- If $k<i$, then $b_{ki}=0$.
- If $k>i$, then $a_{ik}=0$.

Thus only the term $k=i$ is nonzero:

$$
c_{ii}=a_{ii}b_{ii}.
$$

$\blacksquare$

### Problem 2

(Problem 4.2-3) Prove: any matrix that commutes with all $n$-th order matrices must be an $n$-th order scalar matrix.

### Solution to Problem 2

Following the approach of **Definition 2**, use elementary matrices to test commutativity. Let $A=\left(a_{ij}\right)$ commute with all $n$-th order matrices.

Take the elementary matrix $E_{ij}$ (entry in row $i$, column $j$ is $1$, all others are $0$). Then $AE_{ij}=E_{ij}A$.

The $j$-th column of $AE_{ij}$ equals the $i$-th column of $A$, and all other columns are $0$.

The $i$-th row of $E_{ij}A$ equals the $j$-th row of $A$, and all other rows are $0$.

Comparing the $\left(i,j\right)$-entry of both:

The $\left(i,j\right)$-entry of $AE_{ij}$ $=a_{ii}$.

The $\left(i,j\right)$-entry of $E_{ij}A$ $=a_{jj}$.

Therefore $a_{ii}=a_{jj}$.

This holds for all $i,j$, so all diagonal entries are equal:

$$
a_{11}=a_{22}=\cdots=a_{nn}=k.
$$

Now compare the $\left(k,j\right)$-entry ( $k\ne i$ ):

The $\left(k,j\right)$-entry of $AE_{ij}$ $=a_{ki}$.

The $\left(k,j\right)$-entry of $E_{ij}A$ $=0$ (since $k\ne i$).

Therefore $a_{ki}=0$ (when $k\ne i$).

This holds for all $i$, so all off-diagonal entries of $A$ are $0$.

Therefore $A=kI$, i.e., $A$ is a scalar matrix. $\blacksquare$

### Problem 3

(Problem 4.2-8) Prove: over a field $K$, any $n$-th order matrix can be expressed as the sum of a symmetric matrix and a skew-symmetric matrix, and this decomposition is unique.

### Solution to Problem 3

Let $A$ be any $n$-th order matrix. Set

$$
S=\frac{1}{2}\left(A+A^{T}\right),
K=\frac{1}{2}\left(A-A^{T}\right).
$$

Then $A=S+K$.

$$
S^{T}=\frac{1}{2}\left(A^{T}+\left(A^{T}\right)^{T}\right)=\frac{1}{2}\left(A^{T}+A\right)=S.
$$

Thus $S$ is a symmetric matrix.

$$
K^{T}=\frac{1}{2}\left(A^{T}-\left(A^{T}\right)^{T}\right)=\frac{1}{2}\left(A^{T}-A\right)=-K.
$$

Thus $K$ is a skew-symmetric matrix.

**Uniqueness.** Suppose $A=S_{1}+K_{1}=S_{2}+K_{2}$, where $S_{1},S_{2}$ are symmetric and $K_{1},K_{2}$ are skew-symmetric.

Then $S_{1}-S_{2}=K_{2}-K_{1}$.

The left side $\left(S_{1}-S_{2}\right)^{T}=S_{1}-S_{2}$ is symmetric.

The right side

$$
\left(K_{2}-K_{1}\right)^{T}=-K_{2}+K_{1}=-\left(K_{2}-K_{1}\right),
$$

is skew-symmetric.

A matrix that is both symmetric and skew-symmetric must be the zero matrix.

Therefore $S_{1}-S_{2}=0$, $K_{2}-K_{1}=0$, i.e., $S_{1}=S_{2}$, $K_{1}=K_{2}$.

The decomposition is unique. $\blacksquare$

### Problem 4

(Problem 4.2-9) Prove: if $A$ is an $n$-th order symmetric matrix over the real field and $A^{2}=0$, then $A=0$.

### Solution to Problem 4

Let $A=\left(a_{ij}\right)$ be a real symmetric matrix with $A^{2}=0$.

Consider the diagonal entries of $A^{2}$:

$$
\left(A^{2}\right)_{ii}=\sum_{k=1}^{n}a_{ik}a_{ki}.
$$

Since $A$ is symmetric, $a_{ki}=a_{ik}$.

Thus

$$
\left(A^{2}\right)_{ii}=\sum_{k=1}^{n}a_{ik}^{2}.
$$

Since $A^{2}=0$, $\left(A^{2}\right)_{ii}=0$, i.e.,

$$
\sum_{k=1}^{n}a_{ik}^{2}=0.
$$

Since all $a_{ik}$ are real, $a_{ik}^{2}\ge0$.

Therefore each $a_{ik}=0$, i.e., $A=0$. $\blacksquare$

### Problem 5

(Problem 4.2-10) Prove: the determinant of an odd-order skew-symmetric matrix over a field $K$ is zero.

### Solution to Problem 5

Let $A$ be an $n$-th order skew-symmetric matrix, with $n$ odd.

Then $A^{T}=-A$.

$$
\left|A^{T}\right|=\left|-A\right|.
$$

Since $\left|A^{T}\right|=\left|A\right|$ and $\left|-A\right|=\left(-1\right)^{n}\left|A\right|$.

Therefore

$$
\left|A\right|=\left(-1\right)^{n}\left|A\right|.
$$

Since $n$ is odd, $\left(-1\right)^{n}=-1$.

Therefore

$$
\left|A\right|=-\left|A\right|\Rightarrow 2\left|A\right|=0\Rightarrow \left|A\right|=0.
$$

$\blacksquare$
