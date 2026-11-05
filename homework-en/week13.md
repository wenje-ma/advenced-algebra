# week13

> **Theorem 4.3.1 (Rank of a Matrix Product)**
> 
> Let $A=\left(a_{ij}\right)_{s\times{n}}$ and $B=\left(b_{ij}\right)_{n\times{m}}$. Then

> **Proposition 4.3.2 (Over $\mathbb{R}$, $A^{\top}Az=0$ Has the Same Solutions as $z=0$)**
> 
> Let $A$ be a matrix over the real number field. Then the homogeneous system $A^{\top}Az=0$ and $z=0$ have the same solutions.

> **Theorem 4.3.3 (Determinant of a Product)**
> 
> Let $A,B$ both be $n\times{n}$ matrices. Then $\left|AB\right|=\left|A\right|\left|B\right|$.

> **Definition 4.4.1 (Invertible Matrix)**
> 
> For a matrix $A$ over a number field $K$, if there exists a matrix $B$ over $K$ such that $AB=BA=I$, then $A$ is called an invertible (or nonsingular) matrix.

> **Definition 4.4.2 (Inverse Matrix)**
> 
> If $A$ is invertible, the matrix $B$ satisfying $AB=BA=I$ is called the inverse matrix of $A$, denoted $A^{-1}$.

> **Theorem 4.4.2 (Necessary and Sufficient Condition for Invertibility)**
> 
> An $n\times{n}$ matrix $A$ over a number field $K$ is invertible if and only if $\left|A\right|\ne0$. When $A$ is invertible,

$$
A^{-1}=\frac{1}{\left|A\right|}A^{*}.
$$

## 4.3-6

Prove: if $A$ is an $n\times{n}$ matrix over a number field $K$, $n$ is odd, and $AA^{\top}=I$ with $\left|A\right|=1$, then $\left|I-A\right|=0$.

### Solution to 4.3-6

By **Theorem 4.3.3 (Determinant of a Product)**, $\left|AB\right|=\left|A\right|\left|B\right|$. We prove $\left|I-A\right|=0$.

$$
\left|I-A\right|=\left|\left(I-A\right)^{\top}\right|=\left|I-A^{\top}\right|.
$$

Since $AA^{\top}=I$, we have $A^{\top}=A^{-1}$.

Therefore

$$
\left|I-A^{\top}\right|=\left|I-A^{-1}\right|=\left|A^{-1}\left(A-I\right)\right|=\left|A^{-1}\right|\left|A-I\right|.
$$

$$
\left|A^{-1}\right|=\frac{1}{\left|A\right|}=\frac{1}{1}=1.
$$

$$
\left|A-I\right|=\left|-\left(I-A\right)\right|=\left(-1\right)^{n}\left|I-A\right|.
$$

Since $n$ is odd, $\left(-1\right)^{n}=-1$.

Therefore

$$
\left|I-A\right|=1\times\left(-1\right)\times\left|I-A\right|=-\left|I-A\right|.
$$

Hence $2\left|I-A\right|=0$, i.e. $\left|I-A\right|=0$. $\blacksquare$

## 4.3-7

Let $s_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$ for $k=0,1,2,\cdots$; and let

$$
A=\left[\begin{array}{ccc}
s_{0}&s_{1}&s_{2}\\
s_{1}&s_{2}&s_{3}\\
s_{2}&s_{3}&s_{4}
\end{array}\right].
$$

Prove:

$$
\left|A\right|=\left(x_{1}-x_{2}\right)^{2}\left(x_{1}-x_{3}\right)^{2}\left(x_{2}-x_{3}\right)^{2}.
$$

### Solution to 4.3-7

By **Theorem 4.3.3 (Determinant of a Product)**, $\left|AB\right|=\left|A\right|\left|B\right|$. Set

$$
B=\left[\begin{array}{ccc}
1&1&1\\
x_{1}&x_{2}&x_{3}\\
x_{1}^{2}&x_{2}^{2}&x_{3}^{2}
\end{array}\right].
$$

Compute the $\left(i,j\right)$-entry of $BB^{\top}$:

$$
\left(BB^{\top}\right)_{ij}=\sum_{k=1}^{3}B_{ik}B_{jk}=\sum_{k=1}^{3}x_{k}^{i-1}x_{k}^{j-1}=\sum_{k=1}^{3}x_{k}^{i+j-2}=s_{i+j-2}.
$$

Therefore

$$
BB^{\top}=\left[\begin{array}{ccc}
s_{0}&s_{1}&s_{2}\\
s_{1}&s_{2}&s_{3}\\
s_{2}&s_{3}&s_{4}
\end{array}\right]=A.
$$

By **Theorem 4.3.3 (Determinant of a Product)**,

$$
\left|A\right|=\left|BB^{\top}\right|=\left|B\right|\left|B^{\top}\right|=\left|B\right|^{2}.
$$

By Formula for the Vandermonde Determinant, $B$ is a Vandermonde matrix,

$$
\left|B\right|=\left(x_{2}-x_{1}\right)\left(x_{3}-x_{1}\right)\left(x_{3}-x_{2}\right).
$$

Therefore

$$
\left|A\right|=\left|B\right|^{2}=\left(x_{1}-x_{2}\right)^{2}\left(x_{1}-x_{3}\right)^{2}\left(x_{2}-x_{3}\right)^{2}.
$$

$\blacksquare$

## 4.3-12

Prove: for any $s\times{n}$ matrix $A$ over the real number field,

$$
\text{rank}\left(A^{\top}AA^{\top}\right)=\text{rank}\left(A\right).
$$

### Solution to 4.3-12

By **Theorem 4.3.1 (Rank of a Matrix Product)**,

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

Consider the homogeneous system $\left(A^{\top}AA^{\top}\right)y=0$, where $y$ is an $s$-dimensional column vector.

Suppose $y$ solves $\left(A^{\top}AA^{\top}\right)y=0$; then

$$
A^{\top}A\left(A^{\top}y\right)=0.
$$

Set $z=A^{\top}y$; then $A^{\top}Az=0$.

By **Proposition 4.3.2 (Over $\mathbb{R}$, $A^{\top}Az=0$ Has the Same Solutions as $z=0$)**, over the real number field $A^{\top}Az=0$ and $z=0$ have the same solutions.

Hence $z=0$, i.e. $A^{\top}y=0$.

Conversely, if $A^{\top}y=0$, then

$$
A^{\top}AA^{\top}y=A^{\top}A\left(A^{\top}y\right)=A^{\top}A\times0=0.
$$

Thus $\left(A^{\top}AA^{\top}\right)y=0$ and $A^{\top}y=0$ have the same solutions.

Hence their solution spaces have the same dimension:

$$
s-\text{rank}\left(A^{\top}AA^{\top}\right)=s-\text{rank}\left(A^{\top}\right).
$$

Therefore

$$
\text{rank}\left(A^{\top}AA^{\top}\right)=\text{rank}\left(A^{\top}\right)=\text{rank}\left(A\right).
$$

$\blacksquare$

## 4.4-4

Prove: if $A$ is invertible, then $A^{*}$ is also invertible; and find $\left(A^{*}\right)^{-1}$.

### Solution to 4.4-4

By **Definition 4.4.1 (Invertible Matrix)** and **Definition 4.4.2 (Inverse Matrix)**, since $A$ is invertible, $\left|A\right|\ne0$.

We know $AA^{*}=\left|A\right|I$.

Taking determinants on both sides:

$$
\left|A\right|\left|A^{*}\right|=\left|A\right|^{n}.
$$

Since $\left|A\right|\ne0$, $\left|A^{*}\right|=\left|A\right|^{n-1}\ne0$.

By **Theorem 4.4.2 (Necessary and Sufficient Condition for Invertibility)**, $A^{*}$ is therefore invertible.

From $AA^{*}=\left|A\right|I$,

$$
A^{*}=\left|A\right|A^{-1}.
$$

Hence

$$
\left(A^{*}\right)^{-1}=\left(\left|A\right|A^{-1}\right)^{-1}=\frac{1}{\left|A\right|}A.
$$

$\blacksquare$

## 4.4-5

Prove: if $A^{3}=0$, then $I-A$ is invertible; and find $\left(I-A\right)^{-1}$.

### Solution to 4.4-5

By **Definition 4.4.1 (Invertible Matrix)**, to prove $I-A$ invertible is to find a matrix $B$ such that

$$
\left(I-A\right)B=B\left(I-A\right)=I.
$$

$$
\left(I-A\right)\left(I+A+A^{2}\right)=I+A+A^{2}-A-A^{2}-A^{3}=I-A^{3}=I-0=I.
$$

Similarly,

$$
\left(I+A+A^{2}\right)\left(I-A\right)=I.
$$

Hence $I-A$ is invertible, and by **Definition 4.4.2 (Inverse Matrix)**,

$$
\left(I-A\right)^{-1}=I+A+A^{2}.
$$

$\blacksquare$

## 4.4-9(4)

Find the inverse of the following matrix:

$$
A=\left[\begin{array}{rrrr}
1&1&1&1\\
1&1&-1&-1\\
1&-1&1&-1\\
1&-1&-1&1
\end{array}\right].
$$

### Solution to 4.4-9(4)

By **Definition 4.4.1 (Invertible Matrix)** and **Definition 4.4.2 (Inverse Matrix)**, compute $A^{2}$:

$$
A^{2}=AA=\left[\begin{array}{rrrr}
4&0&0&0\\
0&4&0&0\\
0&0&4&0\\
0&0&0&4
\end{array}\right]=4I.
$$

Therefore

$$
A\times\frac{1}{4}A=I.
$$

By **Definition 4.4.2 (Inverse Matrix)**,

$$
A^{-1}=\frac{1}{4}A=\left[\begin{array}{rrrr}
1/4&1/4&1/4&1/4\\
1/4&1/4&-1/4&-1/4\\
1/4&-1/4&1/4&-1/4\\
1/4&-1/4&-1/4&1/4
\end{array}\right].
$$

$\blacksquare$

## 4.4-10(1)

Solve the following matrix equation:

$$
\left[\begin{array}{rrr}
1&-2&0\\
4&-2&-1\\
-3&1&2
\end{array}\right]X=\left[\begin{array}{rr}
-1&4\\
2&5\\
1&-3
\end{array}\right].
$$

### Solution to 4.4-10(1)

By **Theorem 4.4.2 (Necessary and Sufficient Condition for Invertibility)**, first find $A^{-1}$. Write

$$
A=\left[\begin{array}{rrr}1&-2&0\\4&-2&-1\\-3&1&2\end{array}\right],
B=\left[\begin{array}{rr}-1&4\\2&5\\1&-3\end{array}\right].
$$

First find $A^{-1}$.

$$
\left|A\right|=1\times\left(-4+1\right)-\left(-2\right)\times\left(8-3\right)+0=-3+10=7.
$$

Adjugate matrix:

$$
A^{*}=\left[\begin{array}{rrr}
-3&4&2\\
-5&2&1\\
-2&5&6
\end{array}\right].
$$

Hence

$$
A^{-1}=\frac{1}{7}A^{*}.
$$

Therefore

$$
X=A^{-1}B=\frac{1}{7}A^{*}B.
$$

Compute $A^{*}B$:

$$
A^{*}B=\left[\begin{array}{rrr}
-3&4&2\\
-5&2&1\\
-2&5&6
\end{array}\right]\left[\begin{array}{rr}
-1&4\\
2&5\\
1&-3
\end{array}\right]
=\left[\begin{array}{rr}
13&2\\
10&-13\\
18&-1
\end{array}\right].
$$

By **Theorem 4.4.2 (Necessary and Sufficient Condition for Invertibility)**, $A^{-1}=\frac{1}{\left|A\right|}A^{*}$, so

$$
X=\frac{1}{7}\left[\begin{array}{rr}
13&2\\
10&-13\\
18&-1
\end{array}\right].
$$

$\blacksquare$

## 4.4-11

Prove: the inverse of an invertible upper (lower) triangular matrix is still upper (lower) triangular.

### Solution to 4.4-11

By **Definition 4.4.1 (Invertible Matrix)** and **Definition 4.4.2 (Inverse Matrix)**, let $A$ be an $n\times{n}$ upper triangular matrix that is invertible. Set $A^{-1}=B=\left(b_{ij}\right)$.

Since $AB=I$, for any $i,j$,

$$
\sum_{k=1}^{n}a_{ik}b_{kj}=\delta_{ij}.
$$

Prove by induction that $b_{ij}=0$ when $i>{}j$.

Induct on rows $i=n,n-1,\cdots,2$ from bottom to top.

When $i=n$, for any $j<{}n$:

$$
\sum_{k=1}^{n}a_{nk}b_{kj}=0.
$$

Since $A$ is upper triangular, $a_{nk}=0$ when $k<{}n$.

Thus the equation reduces to $a_{nn}b_{nj}=0$.

Since $A$ is invertible, $a_{nn}\ne0$, hence $b_{nj}=0$ (for all $j<{}n$).

Assume the conclusion holds for all rows $i>{}m$ (i.e. $b_{ij}=0$ when $i>{}m$ and $i>{}j$).

Consider row $m$, for any $j<{}m$:

$$
\sum_{k=1}^{n}a_{mk}b_{kj}=0.
$$

Since $A$ is upper triangular, $a_{mk}=0$ when $k>{}m$.

Thus the equation is

$$
\sum_{k=1}^{m}a_{mk}b_{kj}=0.
$$

Namely,

$$
a_{mm}b_{mj}+a_{m,m-1}b_{m-1,j}+\cdots+a_{m1}b_{1,j}=0.
$$

By the induction hypothesis, terms with $k>{}m$ are already $0$. For terms with $k<{}m$, $a_{mk}=0$ (because $m>{}k$, and $A$ is upper triangular).

Hence only $a_{mm}b_{mj}=0$ remains.

Since $a_{mm}\ne0$, $b_{mj}=0$.

The induction is complete. Therefore $B$ is upper triangular.

The inverse of an invertible upper (lower) triangular matrix is still upper (lower) triangular. The lower triangular case is proved analogously. $\blacksquare$
