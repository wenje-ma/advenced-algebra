# Assignment 23

> **Definition 1** (Orthogonal matrix)<br>A square matrix $A$ over the real field, if $A^{T}A=I$, then $A$ is called an orthogonal matrix.

> **Definition 2** (Inner product)<br>In $\mathbb{R}^{n}$, for any $\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)$ and $\beta=\left(b_{1},b_{2},\cdots,b_{n}\right)$, define
> $$
> \left(\alpha,\beta\right)=a_{1}b_{1}+a_{2}b_{2}+\cdots+a_{n}b_{n},
> $$
> as the standard inner product of $\mathbb{R}^{n}$.

> **Proposition 2** (Orthogonal vectors are linearly independent)<br>In the Euclidean space $\mathbb{R}^{n}$, an orthogonal set of vectors is always linearly independent.

### Problem 1

(Problem 4.6-1(3)) Determine whether the following matrix is orthogonal:

$$
A=\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right].
$$

### Solution to Problem 1

By **Definition 1** (Orthogonal matrix), compute $A^{T}A$:

$$
A^{T}A=\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right]\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right].
$$

$\left(1,1\right)$-entry:

$$
\left(\frac{\sqrt{3}}{2}\right)^{2}+\left(\frac{1}{2}\right)^{2}=\frac{3}{4}+\frac{1}{4}=1
$$

$\left(1,2\right)$-entry:

$$
\frac{\sqrt{3}}{2}\cdot\frac{1}{2}+\frac{1}{2}\cdot\left(-\frac{\sqrt{3}}{2}\right)=\frac{\sqrt{3}}{4}-\frac{\sqrt{3}}{4}=0.
$$

$\left(2,1\right)$-entry:

$$
\frac{1}{2}\cdot\frac{\sqrt{3}}{2}+\left(-\frac{\sqrt{3}}{2}\right)\cdot\frac{1}{2}=\frac{\sqrt{3}}{4}-\frac{\sqrt{3}}{4}=0
$$

$\left(2,2\right)$-entry:

$$
\left(\frac{1}{2}\right)^{2}+\left(-\frac{\sqrt{3}}{2}\right)^{2}=\frac{1}{4}+\frac{3}{4}=1
$$

Therefore $A^{T}A=I$. By **Definition 1** (Orthogonal matrix), $A$ is orthogonal. $\blacksquare$

### Problem 2

(Problem 4.6-1(8)) Determine whether the following matrix is orthogonal:

$$
A=\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right].
$$

### Solution to Problem 2

By **Definition 1** (Orthogonal matrix), compute $A^{T}A$:

$$
A^{T}A=\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right]\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right]
=\left[\begin{array}{rr}
2 & 0\\
0 & 2
\end{array}\right].
$$

Clearly $A^{T}A\ne I$. By **Definition 1** (Orthogonal matrix), $A$ is not orthogonal. $\blacksquare$

### Problem 3

(Problem 4.6-3) Prove: if $A$ is an $n$-th order symmetric matrix over the real field and $T$ is an $n$-th order orthogonal matrix, then $T^{-1}AT$ is symmetric.

### Solution to Problem 3

By **Definition 1** (Orthogonal matrix), since $T$ is orthogonal, $T^{-1}=T^{T}$.

$$
\left(T^{-1}AT\right)^{T}=T^{T}A^{T}\left(T^{-1}\right)^{T}.
$$

Since $T$ is orthogonal, $T^{-1}=T^{T}$, hence $\left(T^{-1}\right)^{T}=\left(T^{T}\right)^{T}=T$.

Therefore

$$
\left(T^{-1}AT\right)^{T}=T^{T}A^{T}T.
$$

Since $A$ is symmetric, $A^{T}=A$.

Thus

$$
\left(T^{-1}AT\right)^{T}=T^{T}AT=T^{-1}AT.
$$

Therefore $T^{-1}AT$ is symmetric. $\blacksquare$

### Problem 4

(Problem 4.6-5) Prove: if an orthogonal matrix $A$ is upper triangular, then $A$ must be diagonal, and its diagonal entries are $1$ or $-1$.

### Solution to Problem 4

By **Definition 1** (Orthogonal matrix), let $A$ be an $n$-th order upper triangular matrix with $A^{T}A=I$.

Since $A$ is upper triangular, $A^{T}$ is lower triangular.

$A^{T}A=I$ is a diagonal matrix.

**Inductively prove that all off-diagonal entries of $A$ are zero.**

When $i=1,j=2$, consider the $\left(1,2\right)$-entry of $A^{T}A$:

$$
\sum_{k=1}^{n}\left(A^{T}\right)_{1k}A_{k2}=\sum_{k=1}^{n}A_{k1}A_{k2}=0.
$$

Since $A$ is upper triangular, when $k>1$, $A_{k1}=0$. Thus the above reduces to $A_{11}A_{12}=0$.

Since $A$ is invertible, $A_{11}\ne0$, hence $A_{12}=0$.

Similarly, $A_{1j}=0$ ( $j>1$ ).

Assume the off-diagonal entries of rows $1,\cdots,i-1$ have already been proved to be zero.

Consider the $\left(i,j\right)$-entry of $A^{T}A$ ( $i<j$ ):

$$
\sum_{k=1}^{i}A_{ki}A_{kj}=0.
$$

By the induction hypothesis, when $k<i$, $A_{ki}=0$. Thus the above reduces to $A_{ii}A_{ij}=0$.

Since $A_{ii}\ne0$, $A_{ij}=0$.

Induction complete. Thus $A$ is diagonal.

From $A^{T}A=I$, we get $A_{ii}^{2}=1$, hence $A_{ii}=\pm1$. $\blacksquare$

### Problem 5

(Problem 4.6-12) In the Euclidean space $\mathbb{R}^{4}$, let the vectors

$$
\alpha_{1}=\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\0\\1\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}1\\0\\0\\-1\end{bmatrix}.
$$

Find an orthonormal set equivalent to $\alpha_{1},\alpha_{2},\alpha_{3}$.

### Solution to Problem 5

Use the Gram-Schmidt orthogonalization process.

Set $\beta_{1}=\alpha_{1}=\left(1,1,0,0\right)^{T}$.

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}.
$$

$\left(\alpha_{2},\beta_{1}\right)=1$, $\left(\beta_{1},\beta_{1}\right)=2$.

Thus

$$
\beta_{2}=\left(1,0,1,0\right)^{T}-\frac{1}{2}\left(1,1,0,0\right)^{T}=\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{T}.
$$

$$
\beta_{3}=\alpha_{3}-\frac{\left(\alpha_{3},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}-\frac{\left(\alpha_{3},\beta_{2}\right)}{\left(\beta_{2},\beta_{2}\right)}\beta_{2}.
$$

$\left(\alpha_{3},\beta_{1}\right)=1$, $\left(\alpha_{3},\beta_{2}\right)=\frac{1}{2}$, $\left(\beta_{2},\beta_{2}\right)=\frac{3}{2}$.

Thus

$$
\begin{aligned}\beta_{3}
&=\left(1,0,0,-1\right)^{T}-\frac{1}{2}\left(1,1,0,0\right)^{T}-\frac{1}{3}\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{T}\\
&=\left(\frac{1}{3},-\frac{1}{3},-\frac{1}{3},-1\right)^{T}.
\end{aligned}
$$

Verify orthogonality: $\left(\beta_{1},\beta_{2}\right)=0$, $\left(\beta_{1},\beta_{3}\right)=0$, $\left(\beta_{2},\beta_{3}\right)=0$.

Normalize:

$$
\eta_{1}=\frac{\beta_{1}}{\left|\beta_{1}\right|}=\left(\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}},0,0\right)^{T}.
$$

$$
\eta_{2}=\frac{\beta_{2}}{\left|\beta_{2}\right|}=\left(\frac{1}{\sqrt{6}},-\frac{1}{\sqrt{6}},\frac{2}{\sqrt{6}},0\right)^{T}.
$$

$$
\eta_{3}=\frac{\beta_{3}}{\left|\beta_{3}\right|}=\left(\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{\sqrt{3}}{2}\right)^{T}.
$$

$\blacksquare$

### Problem 6

(Problem 4.6-14) Let $A$ be an invertible $n$-th order matrix over the real field. Prove that $A$ can be decomposed as

$$
A=TB,
$$

where $T$ is orthogonal, $B$ is upper triangular, and the diagonal entries of $B$ are all positive; and prove that this decomposition is unique.

### Solution to Problem 6

**Existence.** Let the column vectors of $A$ be $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$.

Since $A$ is invertible, $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ are linearly independent.

Apply Gram-Schmidt orthogonalization to $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ to obtain the orthogonal set $\beta_{1},\beta_{2},\cdots,\beta_{n}$, where each $\beta_{i}$ is a linear combination of $\alpha_{1},\cdots,\alpha_{i}$, and $\alpha_{i}$ is a linear combination of $\beta_{1},\cdots,\beta_{i}$.

Normalize $\beta_{1},\beta_{2},\cdots,\beta_{n}$ to obtain the orthonormal set $\eta_{1},\eta_{2},\cdots,\eta_{n}$.

Set $T=\left(\eta_{1},\eta_{2},\cdots,\eta_{n}\right)$; then $T$ is orthogonal.

Since $\alpha_{i}$ is a linear combination of $\eta_{1},\cdots,\eta_{i}$, we have $A=TB$, where $B$ is upper triangular.

The diagonal entries of $B$ are $\left|\beta_{1}\right|,\left|\beta_{2}\right|,\cdots,\left|\beta_{n}\right|$, all positive.

**Uniqueness.** Suppose $A=T_{1}B_{1}=T_{2}B_{2}$, where $T_{1},T_{2}$ are orthogonal and $B_{1},B_{2}$ are upper triangular with positive diagonal entries.

Then $T_{2}^{-1}T_{1}=B_{2}B_{1}^{-1}$.

The left side $T_{2}^{-1}T_{1}$ is orthogonal (the product of orthogonal matrices is orthogonal).

The right side $B_{2}B_{1}^{-1}$ is upper triangular (the product of upper triangular matrices is upper triangular).

By the result of Problem 4.6-5, a matrix that is both orthogonal and upper triangular must be diagonal with diagonal entries $\pm1$.

Hence $B_{2}B_{1}^{-1}$ is diagonal with diagonal entries $\pm1$.

Since the diagonal entries of $B_{1},B_{2}$ are all positive, the diagonal entries of $B_{2}B_{1}^{-1}$ are positive.

Therefore the diagonal entries must be $+1$, i.e., $B_{2}B_{1}^{-1}=I$.

Hence $B_{2}=B_{1}$, and therefore $T_{2}=T_{1}$.

The decomposition is unique. $\blacksquare$
