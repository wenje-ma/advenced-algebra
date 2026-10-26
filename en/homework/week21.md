# Assignment 21

> **Definition 1** (Invertible matrix)<br>A matrix $A$ over a field $K$ is called invertible (or nonsingular) if there exists a matrix $B$ over $K$ such that $AB=BA=I$.

> **Definition 2** (Inverse matrix)<br>If $A$ is invertible, the matrix $B$ satisfying $AB=BA=I$ is called the inverse of $A$, denoted $A^{-1}$.

> **Theorem 2** (Necessary and sufficient condition for invertibility)<br>An $n$-th order matrix $A$ over $K$ is invertible if and only if $\left|A\right|\ne0$. When $A$ is invertible:
> 
> $$
> A^{-1}=\frac{1}{\left|A\right|}A^{*}
> $$

### Problem 1

(Problem 4.4-4) Prove: if $A$ is invertible, then $A^{*}$ is also invertible; and find $\left(A^{*}\right)^{-1}$.

### Solution to Problem 1

By **Definition 1** (Invertible matrix) and **Definition 2** (Inverse matrix), since $A$ is invertible, $\left|A\right|\ne 0$.

We know $AA^{*}=\left|A\right|I$.

Taking determinants on both sides:

$$
\left|A\right|\left|A^{*}\right|=\left|A\right|^{n}.
$$

Since $\left|A\right|\ne 0$, $\left|A^{*}\right|=\left|A\right|^{n-1}\ne 0$.

By **Theorem 2** (Necessary and sufficient condition), $A^{*}$ is invertible.

From $AA^{*}=\left|A\right|I$, we get

$$
A^{*}=\left|A\right|A^{-1}.
$$

Therefore

$$
\left(A^{*}\right)^{-1}=\left(\left|A\right|A^{-1}\right)^{-1}=\frac{1}{\left|A\right|}A.
$$

$\blacksquare$

### Problem 2

(Problem 4.4-5) Prove: if $A^{3}=0$, then $I-A$ is invertible; and find $\left(I-A\right)^{-1}$.

### Solution to Problem 2

By **Definition 1** (Invertible matrix), to prove $I-A$ is invertible, we need a matrix $B$ such that

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

Thus $I-A$ is invertible, and

By **Definition 2** (Inverse matrix),

$$
\left(I-A\right)^{-1}=I+A+A^{2}.
$$

$\blacksquare$

### Problem 3

(Problem 4.4-9(4)) Find the inverse of the following matrix:

$$
A=\left[\begin{array}{rrrr}
1 & 1 & 1 & 1\\
1 & 1 & -1 & -1\\
1 & -1 & 1 & -1\\
1 & -1 & -1 & 1
\end{array}\right].
$$

### Solution to Problem 3

By **Definition 1** and **Definition 2**, compute $A^{2}$:

$$
A^{2}=AA=\left[\begin{array}{rrrr}
4 & 0 & 0 & 0\\
0 & 4 & 0 & 0\\
0 & 0 & 4 & 0\\
0 & 0 & 0 & 4
\end{array}\right]=4I.
$$

Therefore

$$
A\times\frac{1}{4}A=I.
$$

By **Definition 2** (Inverse matrix),

$$
A^{-1}=\frac{1}{4}A=\left[\begin{array}{rrrr}
1/4 & 1/4 & 1/4 & 1/4\\
1/4 & 1/4 & -1/4 & -1/4\\
1/4 & -1/4 & 1/4 & -1/4\\
1/4 & -1/4 & -1/4 & 1/4
\end{array}\right].
$$

$\blacksquare$

### Problem 4

(Problem 4.4-10(1)) Solve the following matrix equation:

$$
\left[\begin{array}{rrr}
1 & -2 & 0\\
4 & -2 & -1\\
-3 & 1 & 2
\end{array}\right]X=\left[\begin{array}{rr}
-1 & 4\\
2 & 5\\
1 & -3
\end{array}\right].
$$

### Solution to Problem 4

By **Theorem 2** (Necessary and sufficient condition), first find $A^{-1}$. Let

$$
A=\left[\begin{array}{rrr}1 & -2 & 0\\4 & -2 & -1\\-3 & 1 & 2\end{array}\right],;B=\left[\begin{array}{rr}-1 & 4\\2 & 5\\1 & -3\end{array}\right].
$$

First find $A^{-1}$.

$$
\left|A\right|=1\times\left(-4+1\right)-\left(-2\right)\times\left(8-3\right)+0=-3+10=7.
$$

Adjugate matrix:

$$
A^{*}=\left[\begin{array}{rrr}
-3 & 4 & 2\\
-5 & 2 & 1\\
-2 & 5 & 6
\end{array}\right].
$$

Thus

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
-3 & 4 & 2\\
-5 & 2 & 1\\
-2 & 5 & 6
\end{array}\right]\left[\begin{array}{rr}
-1 & 4\\
2 & 5\\
1 & -3
\end{array}\right]
=\left[\begin{array}{rr}
13 & 2\\
10 & -13\\
18 & -1
\end{array}\right].
$$

Therefore

By **Theorem 2** (Necessary and sufficient condition),

$$
A^{-1}=\frac{1}{\left|A\right|}A^{*}
$$

Thus

$$
X=\frac{1}{7}\left[\begin{array}{rr}
13 & 2\\
10 & -13\\
18 & -1
\end{array}\right].
$$

$\blacksquare$

### Problem 5

(Problem 4.4-11) Prove: the inverse of an invertible upper (lower) triangular matrix is also upper (lower) triangular.

### Solution to Problem 5

By **Definition 1** and **Definition 2**, let $A$ be an invertible $n$-th order upper triangular matrix. Let $A^{-1}=B=\left(b_{ij}\right)$.

Since $AB=I$, for any $i,j$,

$$
\sum_{k=1}^{n}a_{ik}b_{kj}=\delta_{ij}.
$$

**Inductively prove $b_{ij}=0$ (when $i> j$).**

Induct on $i=n,n-1,\cdots,2$ from bottom to top.

When $i=n$, for any $j< n$:

$$
\sum_{k=1}^{n}a_{nk}b_{kj}=0.
$$

Since $A$ is upper triangular, $a_{nk}=0$ (when $k< n$).

Thus the above reduces to $a_{nn}b_{nj}=0$.

Since $A$ is invertible, $a_{nn}\ne0$, hence $b_{nj}=0$ (for all $j< n$).

Assume the conclusion holds for all rows $i> m$ (i.e., $b_{ij}=0$ when $i> m$ and $i> j$).

Consider row $m$, for any $j< m$:

$$
\sum_{k=1}^{n}a_{mk}b_{kj}=0.
$$

Since $A$ is upper triangular, $a_{mk}=0$ (when $k> m$).

Thus the above is

$$
\sum_{k=1}^{m}a_{mk}b_{kj}=0.
$$

where

$$
a_{mm}b_{mj}+a_{m,m-1}b_{m-1,j}+\cdots+a_{m1}b_{1,j}=0.
$$

By the induction hypothesis, terms with $k> m$ are already proved to be $0$. For terms with $k< m$, $a_{mk}=0$ (since $m> k$, and $A$ is upper triangular).

Thus only $a_{mm}b_{mj}=0$ remains.

Since $a_{mm}\ne0$, $b_{mj}=0$.

Induction complete. Thus $B$ is upper triangular.

The inverse of an invertible upper (lower) triangular matrix is also upper (lower) triangular. The lower triangular case is proved similarly. $\blacksquare$
