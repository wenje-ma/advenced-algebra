# Assignment 16

> **Definition 1** (Fundamental system of solutions)<br>When a homogeneous linear system has nonzero solutions, a finite set of solutions $\eta_{1},\eta_{2},\cdots,\eta_{t}$ is called a **fundamental system of solutions** if: $1^{\circ}$ they are linearly independent; $2^{\circ}$ every solution of the system can be linearly represented by them.

> **Theorem 1** (Dimension of solution space)<br>The dimension of the solution space $W$ of a homogeneous linear system of $n$ unknowns over the field $K$ is:
> 
> $$
> \dim W=n-\text{rank}\left(A\right)
> $$
> 
where $A$ is the coefficient matrix.

### Problem 1

(Problem 3.7-1(1)) Find a fundamental system of solutions for the following homogeneous linear system over $K$, and write out its solution set.

$$
\begin{cases}
x_{1}-3x_{2}+x_{3}-2x_{4}=0,\\
-5x_{1}+x_{2}-2x_{3}+3x_{4}=0,\\
-x_{1}-11x_{2}+2x_{3}-5x_{4}=0,\\
3x_{1}+5x_{2}+x_{4}=0.
\end{cases}
$$

### Solution to Problem 1

By **Definition 1** (Fundamental system) and **Theorem 1** (Dimension of solution space), perform elementary row operations on the coefficient matrix:

$$
\left[\begin{array}{rrrr}
1 & -3 & 1 & -2\\
-5 & 1 & -2 & 3\\
-1 & -11 & 2 & -5\\
3 & 5 & 0 & 1
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1 & -3 & 1 & -2\\
0 & -14 & 3 & -7\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0
\end{array}\right].
$$

The rank is $2$, and the number of unknowns is $4$. By **Theorem 1**, the dimension of the solution space is $4-2=2$, so the fundamental system contains $2$ vectors.

General solution:

$$
\begin{cases}
x_{1}=\frac{-5x_{3}+7x_{4}}{14},\\
x_{2}=\frac{3x_{3}-7x_{4}}{14},
\end{cases}
$$

where $x_{3},x_{4}$ are free variables.

Setting $x_{3}=14,x_{4}=0$, we get $\eta_{1}=\left(-5,3,14,0\right)^{\top}$.

Setting $x_{3}=0,x_{4}=14$, we get $\eta_{2}=\left(7,-7,0,14\right)^{\top}$.

By **Definition 1** (Fundamental system), $\eta_{1},\eta_{2}$ are linearly independent, and every solution can be linearly represented by them, so they form a fundamental system of solutions.

Solution set:

$$
W=\left\{k_{1}\eta_{1}+k_{2}\eta_{2}\middle|k_{1},k_{2}\in K\right\}.
$$

$\blacksquare$

### Problem 2

(Problem 3.7-1(2)) Find a fundamental system of solutions for the following homogeneous linear system over $K$, and write out its solution set.

$$
\begin{cases}
3x_{1}-x_{2}+2x_{3}+x_{4}=0,\\
x_{1}+3x_{2}-x_{3}+2x_{4}=0,\\
-2x_{1}+5x_{2}+x_{3}-x_{4}=0,\\
3x_{1}+10x_{2}+x_{3}+4x_{4}=0,\\
-2x_{1}+15x_{2}-4x_{3}+4x_{4}=0.
\end{cases}
$$

### Solution to Problem 2

By **Definition 1** (Fundamental system) and **Theorem 1** (Dimension of solution space), perform elementary row operations on the coefficient matrix:

$$
\left[\begin{array}{rrrr}
3 & -1 & 2 & 1\\
1 & 3 & -1 & 2\\
-2 & 5 & 1 & -1\\
3 & 10 & 1 & 4\\
-2 & 15 & -4 & 4
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1 & 3 & -1 & 2\\
0 & 1 & 4 & -2\\
0 & 0 & -45 & 25\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0
\end{array}\right].
$$

The rank is $3$, and the number of unknowns is $4$, so the fundamental system contains $4-3=1$ vector.

General solution:

$$
\begin{cases}
x_{1}=-\frac{7}{9}x_{4},\\
x_{2}=-\frac{2}{9}x_{4},\\
x_{3}=\frac{5}{9}x_{4},
\end{cases}
$$

where $x_{4}$ is a free variable.

Setting $x_{4}=9$, we get $\eta_{1}=\left(-7,-2,5,9\right)^{\top}$.

By **Definition 1** (Fundamental system), $\eta_{1}$ is linearly independent, and every solution can be linearly represented by it, so it forms a fundamental system of solutions.

Solution set:

$$
W=\left\{k\eta_{1}\middle|k\in K\right\}.
$$

$\blacksquare$

### Problem 3

(Problem 3.7-4) Prove: let the rank of the coefficient matrix of a homogeneous system of $n$ unknowns be $r$ $\left(r< n\right)$, and let $\delta_{1},\delta_{2},\cdots,\delta_{m}$ be solution vectors of the system. Then

$$
\text{rank}\left\{\delta_{1},\delta_{2},\cdots,\delta_{m}\right\}\le n-r.
$$

### Solution to Problem 3

By **Theorem 1** (Dimension of solution space), the dimension of the solution space $W$ is

$$
\dim W=n-\text{rank}\left(A\right)=n-r.
$$

$\delta_{1},\delta_{2},\cdots,\delta_{m}$ are all vectors in $W$, so $\left\langle\delta_{1},\delta_{2},\cdots,\delta_{m}\right\rangle\subseteq W$.

Therefore

$$
\text{rank}\left\{\delta_{1},\delta_{2},\cdots,\delta_{m}\right\}
=\dim\left\langle\delta_{1},\delta_{2},\cdots,\delta_{m}\right\rangle
\le\dim W=n-r.
$$

$\blacksquare$

### Problem 4

(Problem 3.7-5) Let the coefficient matrix $A$ of a homogeneous system of $n$ equations in $n$ unknowns have determinant equal to zero, and let the cofactor of the $\left(k,l\right)$-entry of $A$ satisfy $A_{kl}\ne0$. Prove:

$$
\eta_{1}=\begin{bmatrix}A_{k1}\\A_{k2}\\\vdots\\A_{kn}\end{bmatrix}
$$

is a fundamental system of solutions for this homogeneous linear system.

### Solution to Problem 4

By **Definition 1** (Fundamental system) and **Theorem 1** (Dimension of solution space), to prove that $\eta_{1}$ is a fundamental system of solutions, we need to verify three conditions: $\eta_{1}$ is a solution, $\eta_{1}\ne0$, and the dimension of the solution space is $1$.

**Verify that $\eta_{1}$ is a solution.** For each $i=1,2,\cdots,n$, compute

$$
a_{i1}A_{k1}+a_{i2}A_{k2}+\cdots+a_{in}A_{kn}.
$$

When $i=k$, this is $\left|A\right|=0$ (given).

When $i\ne k$, this is the determinant obtained by replacing the $k$-th row of $A$ with the $i$-th row; since two rows are identical, the determinant is $0$.

Therefore for all $i$, the above equals $0$, i.e., $A\eta_{1}=0$.

**Verify that $\eta_{1}\ne0$.** Since $A_{kl}\ne0$, the $l$-th component of $\eta_{1}$ is nonzero, so $\eta_{1}\ne0$.

**Verify that the solution space has dimension $1$.** Since $\left|A\right|=0$, $\text{rank}\left(A\right)< n$.

Also, since $A_{kl}\ne0$, this shows that $A$ has a nonzero minor of order $n-1$ (the minor after deleting row $k$ and column $l$), so $\text{rank}\left(A\right)\ge n-1$.

Therefore $\text{rank}\left(A\right)=n-1$.

By **Theorem 1** (Dimension of solution space), the dimension of the solution space $=n-\text{rank}\left(A\right)=1$.

$\eta_{1}$ is a nonzero solution, and by itself forms a basis of the solution space, i.e., a fundamental system of solutions. $\blacksquare$

### Problem 5

(Problem 3.7-7) Let $A_{1}$ be the submatrix formed by the first $s-1$ rows of the $s\times n$ matrix $A=\left(a_{ij}\right)$. Prove: if every solution of the homogeneous system with coefficient matrix $A_{1}$ is also a solution of the equation

$$
a_{s1}x_{1}+a_{s2}x_{2}+\cdots+a_{sn}x_{n}=0
$$

then the $s$-th row of $A$ can be linearly represented by the first $s-1$ rows of $A$.

### Solution to Problem 5

By **Theorem 1** (Dimension of solution space), the solution space of a homogeneous system is the orthogonal complement of the row space of the coefficient matrix. Let $V_{1}$ be the row space of $A_{1}$; then the solution space of the homogeneous system with coefficient matrix $A_{1}$ is $W_{1}=V_{1}^{\perp}$ (the orthogonal complement of $V_{1}$).

Hypothesis: every $x$ in $W_{1}$ satisfies $a_{s1}x_{1}+\cdots+a_{sn}x_{n}=0$.

That is, the row vector $\gamma_{s}=\left(a_{s1},\cdots,a_{sn}\right)$ of the $s$-th row is orthogonal to every vector in $W_{1}$.

Therefore $\gamma_{s}\in\left(W_{1}\right)^{\perp}=V_{1}$.

Hence $\gamma_{s}$ can be linearly represented by the row vectors of $A_{1}$, i.e., the $s$-th row of $A$ can be linearly represented by the first $s-1$ rows of $A$. $\blacksquare$
