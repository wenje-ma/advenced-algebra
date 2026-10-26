ï»¿ï»¿# Assignment 11

> **Definition 1** (Linearly Dependent)<br>A vector system $\alpha_{1},\cdots,\alpha_{s}$ in $K^{n}$ is called linearly dependent if there exist scalars $k_{1},\cdots,k_{s}$ in $K$, not all zero, such that $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$.

> **Definition 2** (Linearly Independent)<br>A vector system $\alpha_{1},\cdots,\alpha_{s}$ in $K^{n}$ is called linearly independent if it is not linearly dependent. That is, if from $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$ one can deduce that all the coefficients are $0$, then the vector system is called linearly independent.

> **Proposition 1** (Relationship between Linear Spanning and Linear Dependence)<br>Let the vector system $\alpha_{1},\cdots,\alpha_{s}$ be linearly independent. Then the vector $\beta$ can be linearly spanned by $\alpha_{1},\cdots,\alpha_{s}$ if and only if $\alpha_{1},\cdots,\alpha_{s},\beta$ is linearly dependent.

### Problem 1

(Problem 3.2-2(1)) Determine whether the following vector system is linearly dependent or linearly independent. If it is linearly dependent, find one of its vectors that can be linearly spanned by the rest, and write down one such expression.

$$
\alpha_{1}=\begin{bmatrix}3\\1\\2\\-4\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\0\\5\\2\end{bmatrix},
\alpha_{3}=\begin{bmatrix}-1\\2\\0\\3\end{bmatrix}.
$$

### Solution to Problem 1

By **Definition 1** (Linearly Dependent) and **Definition 2** (Linearly Independent), consider the homogeneous system of linear equations $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=0$. Write down the coefficient matrix and perform elementary row operations:

$$
\left[\begin{array}{rrr}
3 & 1 & -1\\
1 & 0 & 2\\
2 & 5 & 0\\
-4 & 2 & 3
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrr}
1 & 0 & 2\\
0 & 1 & -7\\
0 & 0 & 31\\
0 & 0 & 0
\end{array}\right].
$$

The echelon matrix has $3$ nonzero rows, equal to the number $3$ of unknowns, so the homogeneous system has only the zero solution.

By **Definition 2**, $\alpha_{1},\alpha_{2},\alpha_{3}$ is therefore linearly independent. $\blacksquare$

### Problem 2

(Problem 3.2-2(2)) Determine whether the following vector system is linearly dependent or linearly independent. If it is linearly dependent, find one of its vectors that can be linearly spanned by the rest, and write down one such expression.

$$
\alpha_{1}=\begin{bmatrix}-2\\1\\0\\3\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\-3\\2\\4\end{bmatrix},
\alpha_{3}=\begin{bmatrix}3\\0\\2\\-1\end{bmatrix},
\alpha_{4}=\begin{bmatrix}2\\-2\\4\\6\end{bmatrix}.
$$

### Solution to Problem 2

By **Definition 1** (Linearly Dependent) and **Definition 2** (Linearly Independent), consider the homogeneous system of linear equations

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}=0.
$$

Write down the coefficient matrix and perform elementary row operations:

$$
\left[\begin{array}{rrrr}
-2 & 1 & 3 & 2\\
1 & -3 & 0 & -2\\
0 & 2 & 2 & 4\\
3 & 4 & -1 & 6
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1 & -3 & 0 & -2\\
0 & -5 & 3 & -2\\
0 & 0 & 16/5 & 16/5\\
0 & 0 & 0 & 0
\end{array}\right].
$$

The echelon matrix has $3$ nonzero rows, less than the number $4$ of unknowns, so the homogeneous system has a nontrivial solution.

Hence $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ is linearly dependent.

Solve for the general solution:

From the $3$rd row: $x_{3}+x_{4}=0$, hence $x_{3}=-x_{4}$.

From the $2$nd row: $-5x_{2}+3x_{3}-2x_{4}=0$; substituting $x_{3}=-x_{4}$ gives $x_{2}=-x_{4}$.

From the $1$st row: $x_{1}-3x_{2}-2x_{4}=0$; substituting $x_{2}=-x_{4}$ gives $x_{1}=-x_{4}$.

Letting $x_{4}=1$, we get $x_{1}=-1$, $x_{2}=-1$, $x_{3}=-1$.

Hence $-\alpha_{1}-\alpha_{2}-\alpha_{3}+\alpha_{4}=0$, i.e.

$$
\alpha_{4}=\alpha_{1}+\alpha_{2}+\alpha_{3}.
$$

Verification:

$$
\alpha_{1}+\alpha_{2}+\alpha_{3}=\left(-2+1+3,1-3+0,0+2+2,3+4-1\right)^{\top}=\left(2,-2,4,6\right)^{\top}=\alpha_{4}.
$$

By **Definition 1** (Linearly Dependent), the homogeneous system has a nontrivial solution, so $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ is linearly dependent. $\blacksquare$

### Problem 3

(Problem 3.2-6) Let the vector system $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ be linearly independent. Determine whether the vector system

$$
\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}
$$

is linearly independent.

### Solution to Problem 3

By **Definition 2** (Linearly Independent), to determine whether the vector system

$$
\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}
$$
is linearly independent is to determine whether the homogeneous system of linear equations

$$
k_{1}\left(\alpha_{1}+\alpha_{2}\right)+k_{2}\left(\alpha_{2}+\alpha_{3}\right)+k_{3}\left(\alpha_{3}+\alpha_{4}\right)+k_{4}\left(\alpha_{4}+\alpha_{1}\right)=0
$$

has only the zero solution.

Set

$$
k_{1}\left(\alpha_{1}+\alpha_{2}\right)+k_{2}\left(\alpha_{2}+\alpha_{3}\right)+k_{3}\left(\alpha_{3}+\alpha_{4}\right)+k_{4}\left(\alpha_{4}+\alpha_{1}\right)=0.
$$

Rearranging gives

$$
\left(k_{1}+k_{4}\right)\alpha_{1}+\left(k_{1}+k_{2}\right)\alpha_{2}+\left(k_{2}+k_{3}\right)\alpha_{3}+\left(k_{3}+k_{4}\right)\alpha_{4}=0.
$$

Since $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ is linearly independent,

$$
\begin{cases}
k_{1}+k_{4}=0,\\
k_{1}+k_{2}=0,\\
k_{2}+k_{3}=0,\\
k_{3}+k_{4}=0.
\end{cases}
$$

Solving gives $k_{2}=-k_{1}$, $k_{3}=k_{1}$, $k_{4}=-k_{1}$, where $k_{1}$ is free.

Letting $k_{1}=1$, we get $k_{2}=-1$, $k_{3}=1$, $k_{4}=-1$, which is a nontrivial solution.

Hence the vector system

$$
\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}
$$

is linearly dependent.

Specifically,

$$
\left(\alpha_{1}+\alpha_{2}\right)-\left(\alpha_{2}+\alpha_{3}\right)+\left(\alpha_{3}+\alpha_{4}\right)-\left(\alpha_{4}+\alpha_{1}\right)=0.
$$

There exist scalars $1,-1,1,-1$, not all zero, such that the above equality holds, so the vector system is linearly dependent. $\blacksquare$

### Problem 4

(Problem 3.2-7) Prove that if the vector $\beta$ can be linearly spanned by the vector system $\alpha_{1},\cdots,\alpha_{s}$, then the representation is unique if and only if $\alpha_{1},\cdots,\alpha_{s}$ is linearly independent.

### Solution to Problem 4

By **Definition 2** (Linearly Independent) and **Definition 1** (Linearly Dependent), prove that the representation is unique if and only if $\alpha_{1},\cdots,\alpha_{s}$ is linearly independent.

**Sufficiency**. Let $\alpha_{1},\cdots,\alpha_{s}$ be linearly independent. Suppose there are two representations:

$$
\beta=k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s},
\beta=l_{1}\alpha_{1}+\cdots+l_{s}\alpha_{s}.
$$

Subtracting the two equations gives

$$
\left(k_{1}-l_{1}\right)\alpha_{1}+\cdots+\left(k_{s}-l_{s}\right)\alpha_{s}=0.
$$

Since $\alpha_{1},\cdots,\alpha_{s}$ is linearly independent, $k_{i}-l_{i}=0$, i.e. $k_{i}=l_{i}$. The representation is unique.

**Necessity**. Let the representation be unique. By contradiction: suppose $\alpha_{1},\cdots,\alpha_{s}$ is linearly dependent; then there exist scalars $c_{1},\cdots,c_{s}$, not all zero, such that $c_{1}\alpha_{1}+\cdots+c_{s}\alpha_{s}=0$.

Let $\beta=k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}$; then

$$
\beta=\left(k_{1}+c_{1}\right)\alpha_{1}+\cdots+\left(k_{s}+c_{s}\right)\alpha_{s}.
$$

Since the $c_{i}$ are not all zero,

$$
\left(k_{1}+c_{1},\cdots,k_{s}+c_{s}\right)\ne\left(k_{1},\cdots,k_{s}\right),
$$

which contradicts the uniqueness of the representation.

The supposition is false, so $\alpha_{1},\cdots,\alpha_{s}$ is linearly independent. $\blacksquare$

### Problem 5

(Problem 3.2-9) Prove that a vector system $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ $\left(s\ge2\right)$ consisting of nonzero vectors is linearly independent if and only if every $\alpha_{i}$ $\left(1< i\le s\right)$ cannot be linearly spanned by the vectors preceding it.

### Solution to Problem 5

By **Definition 2** (Linearly Independent) and **Definition 1** (Linearly Dependent), prove that a vector system $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ $\left(s\ge2\right)$ consisting of nonzero vectors is linearly independent if and only if every $\alpha_{i}$ $\left(1< i\le s\right)$ cannot be linearly spanned by the vectors preceding it.

**Necessity**. Let $\alpha_{1},\cdots,\alpha_{s}$ be linearly independent. By contradiction: suppose some $\alpha_{i}$ $\left(i> 1\right)$ can be linearly spanned by the preceding vectors, i.e.

$$
\alpha_{i}=k_{1}\alpha_{1}+\cdots+k_{i-1}\alpha_{i-1}.
$$

Then

$$
k_{1}\alpha_{1}+\cdots+k_{i-1}\alpha_{i-1}-\alpha_{i}+0\cdot\alpha_{i+1}+\cdots+0\cdot\alpha_{s}=0.
$$

Here the coefficient $-1\ne0$, so $\alpha_{1},\cdots,\alpha_{s}$ is linearly dependent, a contradiction.

Therefore every $\alpha_{i}$ $\left(i> 1\right)$ cannot be linearly spanned by the vectors preceding it.

**Sufficiency**. Let every $\alpha_{i}$ $\left(i> 1\right)$ cannot be linearly spanned by the vectors preceding it. By contradiction: suppose $\alpha_{1},\cdots,\alpha_{s}$ is linearly dependent; then there exist scalars $c_{1},\cdots,c_{s}$, not all zero, such that $c_{1}\alpha_{1}+\cdots+c_{s}\alpha_{s}=0$.

Let $c_{i}$ be the last nonzero coefficient

$$
\left(c_{i}\ne0,c_{i+1}=\cdots=c_{s}=0\right).
$$

If $i=1$, then $c_{1}\alpha_{1}=0$. Since $\alpha_{1}\ne0$, we have $c_{1}=0$, a contradiction. Hence $i> 1$.

From $c_{1}\alpha_{1}+\cdots+c_{i}\alpha_{i}=0$ we get

$$
\alpha_{i}=-\frac{c_{1}}{c_{i}}\alpha_{1}-\cdots-\frac{c_{i-1}}{c_{i}}\alpha_{i-1}.
$$

This shows that $\alpha_{i}$ can be linearly spanned by the preceding vectors, contradicting the hypothesis.

The supposition is false, so $\alpha_{1},\cdots,\alpha_{s}$ is linearly independent. $\blacksquare$

### Problem 6

(Problem 3.2-11) Let $a_{1},a_{2},\cdots,a_{r}$ be pairwise distinct numbers, $r\le n$. Let

$$
\alpha_{1}=\begin{bmatrix}1\\a_{1}\\a_{1}^{2}\\\vdots\\a_{1}^{n-1}\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\a_{2}\\a_{2}^{2}\\\vdots\\a_{2}^{n-1}\end{bmatrix},\cdots,
\alpha_{r}=\begin{bmatrix}1\\a_{r}\\a_{r}^{2}\\\vdots\\a_{r}^{n-1}\end{bmatrix}.
$$

Prove that $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ is linearly independent.

### Solution to Problem 6

By **Definition 2** (Linearly Independent), to prove that $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ is linearly independent is to prove that the homogeneous system of linear equations

$$
k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{r}\alpha_{r}=0
$$

has only the zero solution.

Set

$$
k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{r}\alpha_{r}=0.
$$

Taking the first $r$ components, we obtain the homogeneous system:

$$
\begin{cases}
k_{1}+k_{2}+\cdots+k_{r}=0,\\
k_{1}a_{1}+k_{2}a_{2}+\cdots+k_{r}a_{r}=0,\\
\cdots\cdots\cdots\cdots\\
k_{1}a_{1}^{r-1}+k_{2}a_{2}^{r-1}+\cdots+k_{r}a_{r}^{r-1}=0.
\end{cases}
$$

Its coefficient determinant is the $r$-th order Vandermonde determinant:

$$
\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{1} & a_{2} & \cdots & a_{r}\\
\vdots & \vdots & & \vdots\\
a_{1}^{r-1} & a_{2}^{r-1} & \cdots & a_{r}^{r-1}
\end{array}\right|=\prod_{1\le i< j\le r}\left(a_{j}-a_{i}\right).
$$

Since $a_{1},a_{2},\cdots,a_{r}$ are pairwise distinct, the determinant is not equal to $0$.

Hence the homogeneous system has only the zero solution: $k_{1}=k_{2}=\cdots=k_{r}=0$.

Therefore $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ is linearly independent. $\blacksquare$
