# week21

> **Definition 4.4.1 (Invertible Matrix)**<br>For a matrix $A$ over a number field $K$, if there exists a matrix $B$ over $K$ such that $AB=BA=I$, then $A$ is called an invertible (or nonsingular) matrix.

> **Definition 4.4.2 (Inverse Matrix)**<br>If $A$ is invertible, the matrix $B$ satisfying $AB=BA=I$ is called the inverse matrix of $A$, denoted $A^{-1}$.

> **Theorem 4.4.2 (Necessary and Sufficient Condition for Invertibility)**<br>An $n\times n$ matrix $A$ over a number field $K$ is invertible if and only if $\left|A\right|\ne0$. When $A$ is invertible,

$$
A^{-1}=\frac{1}{\left|A\right|}A^{*}.
$$

---

## 4.4-4

Prove: if $A$ is invertible, then $A^{*}$ is also invertible; and find $\left(A^{*}\right)^{-1}$.

### Solution 4.4-4

By **Definition 4.4.1 (Invertible Matrix)** and **Definition 4.4.2 (Inverse Matrix)**, since $A$ is invertible, $\left|A\right|\ne 0$.

We know $AA^{*}=\left|A\right|I$.

Taking determinants on both sides:

$$
\left|A\right|\left|A^{*}\right|=\left|A\right|^{n}.
$$

Since $\left|A\right|\ne 0$, $\left|A^{*}\right|=\left|A\right|^{n-1}\ne 0$.

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

---

## 4.4-5

Prove: if $A^{3}=0$, then $I-A$ is invertible; and find $\left(I-A\right)^{-1}$.

### Solution 4.4-5

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

---

## 4.4-9(4)

Find the inverse of the following matrix:

$$
A=\left[\begin{array}{rrrr}
1 & 1 & 1 & 1\\
1 & 1 & -1 & -1\\
1 & -1 & 1 & -1\\
1 & -1 & -1 & 1
\end{array}\right].
$$

### Solution 4.4-9(4)

By **Definition 4.4.1 (Invertible Matrix)** and **Definition 4.4.2 (Inverse Matrix)**, compute $A^{2}$:

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

By **Definition 4.4.2 (Inverse Matrix)**,

$$
A^{-1}=\frac{1}{4}A=\left[\begin{array}{rrrr}
1/4 & 1/4 & 1/4 & 1/4\\
1/4 & 1/4 & -1/4 & -1/4\\
1/4 & -1/4 & 1/4 & -1/4\\
1/4 & -1/4 & -1/4 & 1/4
\end{array}\right].
$$

$\blacksquare$

---

## 4.4-10(1)

Solve the following matrix equation:

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

### Solution 4.4-10(1)

By **Theorem 4.4.2 (Necessary and Sufficient Condition for Invertibility)**, first find $A^{-1}$. Write

$$
A=\left[\begin{array}{rrr}1 & -2 & 0\\4 & -2 & -1\\-3 & 1 & 2\end{array}\right],
B=\left[\begin{array}{rr}-1 & 4\\2 & 5\\1 & -3\end{array}\right].
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

By **Theorem 4.4.2 (Necessary and Sufficient Condition for Invertibility)**, $A^{-1}=\frac{1}{\left|A\right|}A^{*}$, so

$$
X=\frac{1}{7}\left[\begin{array}{rr}
13 & 2\\
10 & -13\\
18 & -1
\end{array}\right].
$$

$\blacksquare$

---

## 4.4-11

Prove: the inverse of an invertible upper (lower) triangular matrix is still upper (lower) triangular.

### Solution 4.4-11

By **Definition 4.4.1 (Invertible Matrix)** and **Definition 4.4.2 (Inverse Matrix)**, let $A$ be an $n\times n$ upper triangular matrix that is invertible. Set $A^{-1}=B=\left(b_{ij}\right)$.

Since $AB=I$, for any $i,j$,

$$
\sum_{k=1}^{n}a_{ik}b_{kj}=\delta_{ij}.
$$

**Prove by induction that $b_{ij}=0$ when $i> j$.**

Induct on rows $i=n,n-1,\cdots,2$ from bottom to top.

When $i=n$, for any $j< n$:

$$
\sum_{k=1}^{n}a_{nk}b_{kj}=0.
$$

Since $A$ is upper triangular, $a_{nk}=0$ when $k< n$.

Thus the equation reduces to $a_{nn}b_{nj}=0$.

Since $A$ is invertible, $a_{nn}\ne0$, hence $b_{nj}=0$ (for all $j< n$).

Assume the conclusion holds for all rows $i> m$ (i.e. $b_{ij}=0$ when $i> m$ and $i> j$).

Consider row $m$, for any $j< m$:

$$
\sum_{k=1}^{n}a_{mk}b_{kj}=0.
$$

Since $A$ is upper triangular, $a_{mk}=0$ when $k> m$.

Thus the equation is

$$
\sum_{k=1}^{m}a_{mk}b_{kj}=0.
$$

Namely,

$$
a_{mm}b_{mj}+a_{m,m-1}b_{m-1,j}+\cdots+a_{m1}b_{1,j}=0.
$$

By the induction hypothesis, terms with $k> m$ are already $0$. For terms with $k< m$, $a_{mk}=0$ (because $m> k$, and $A$ is upper triangular).

Hence only $a_{mm}b_{mj}=0$ remains.

Since $a_{mm}\ne0$, $b_{mj}=0$.

The induction is complete. Therefore $B$ is upper triangular.

The inverse of an invertible upper (lower) triangular matrix is still upper (lower) triangular. The lower triangular case is proved analogously. $\blacksquare$
