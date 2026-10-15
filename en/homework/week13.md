# Assignment 13

> **Definition 1** (Basis)<br>Let $U$ be a subspace of $K^{n}$. A family of vectors $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ in $U$ is called a **basis** of $U$ if it satisfies: $1^{\circ}$ linearly independent; $2^{\circ}$ every vector in $U$ can be linearly represented by them.

### Problem 1

(Problem 3.4-2) Prove that the vectors in $K^{n}$

$$
\eta_{1}=\begin{bmatrix}1\\0\\0\\\vdots\\0\end{bmatrix},
\eta_{2}=\begin{bmatrix}1\\1\\0\\\vdots\\0\end{bmatrix},\cdots,
\eta_{n}=\begin{bmatrix}1\\1\\1\\\vdots\\1\end{bmatrix}
$$

form a basis of $K^{n}$.

### Solution to Problem 1

By the requirements of **Definition 1** (Basis), we need to verify two conditions: linear independence, and that every vector in $K^{n}$ can be linearly represented.

**Verify linear independence.** Let

$$
k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{n}\eta_{n}=0.
$$

Comparing the components (from the $1$st to the $n$-th):

$1$st component: $k_{1}=0$.

$2$nd component: $k_{1}+k_{2}=0$; substituting $k_{1}=0$ gives $k_{2}=0$.

$3$rd component: $k_{1}+k_{2}+k_{3}=0$; substituting $k_{1}=k_{2}=0$ gives $k_{3}=0$.

And so on; from the $i$-th component we get $k_{i}=0$.

Thus $\eta_{1},\eta_{2},\cdots,\eta_{n}$ are linearly independent.

**Verify linear representability.** Take any

$$
\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)^{T}\in K^{n},
$$
and set

$$
\alpha=x_{1}\eta_{1}+x_{2}\eta_{2}+\cdots+x_{n}\eta_{n}.
$$

Comparing the components:

$1$st component: $x_{1}=a_{1}$.

$2$nd component: $x_{1}+x_{2}=a_{2}$, hence $x_{2}=a_{2}-a_{1}$.

$3$rd component: $x_{1}+x_{2}+x_{3}=a_{3}$, hence $x_{3}=a_{3}-a_{2}$.

And so on, $x_{i}=a_{i}-a_{i-1}$ $\left(i=2,\cdots,n\right)$.

The representation exists and is unique.

By **Definition 1**, $\eta_{1},\eta_{2},\cdots,\eta_{n}$ form a basis of $K^{n}$. $\blacksquare$

### Problem 2

(Problem 3.4-3(3)) Determine whether the following vectors form a basis of $K^{3}$:

$$
\alpha_{1}=\begin{bmatrix}1\\0\\1\end{bmatrix},
\alpha_{2}=\begin{bmatrix}0\\4\\-1\end{bmatrix},
\alpha_{3}=\begin{bmatrix}2\\-4\\3\end{bmatrix}.
$$

### Solution to Problem 2

By the requirements of **Definition 1** (Basis), determining whether three $3$-dimensional vectors form a basis of $K^{3}$ is equivalent to determining whether they are linearly independent, i.e., whether the determinant of the matrix they form is not equal to $0$.

$$
\left|\begin{array}{rrr}
1 & 0 & 2\\
0 & 4 & -4\\
1 & -1 & 3
\end{array}\right|
=1\times\left(4\times3-\left(-4\right)\times\left(-1\right)\right)-0+2\times\left(0\times\left(-1\right)-4\times1\right)
$$

$$
=1\times\left(12-4\right)+2\times\left(-4\right)=8-8=0.
$$

The determinant equals $0$, so $\alpha_{1},\alpha_{2},\alpha_{3}$ are linearly dependent. They do not satisfy the "linearly independent" requirement of **Definition 1** (Basis), and are not a basis of $K^{3}$. $\blacksquare$

### Problem 3

(Problem 3.4-4) Let $U$ be an $r$-dimensional subspace of $K^{n}$, and let $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ be $r$ vectors in $U$. Prove that if every vector in $U$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$, then $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ form a basis of $U$.

### Solution to Problem 3

By the requirements of **Definition 1** (Basis), we need to verify two conditions: linear independence, and that every vector in $U$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$. The second condition is given, so we only need to verify linear independence.

Since every vector in $U$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$, we have $U\subseteq\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

Since $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\in U$ and $U$ is a subspace, we have $\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle\subseteq U$.

Therefore $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

By Theorem $8$,

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}.
$$

Also $\dim U=r$, hence

$$
\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}=r.
$$

The rank of $r$ vectors being $r$ means they are linearly independent.

Therefore $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ are linearly independent, and every vector in $U$ can be linearly represented by them.

$\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ form a basis of $U$. $\blacksquare$
