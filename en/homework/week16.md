# week16

> **Definition 3.7.1 (Fundamental System of Solutions)**<br>When a homogeneous linear system has a nontrivial solution, if finitely many of its solutions $\eta_{1},\eta_{2},\cdots,\eta_{t}$ satisfy: $1^{\circ}$ they are linearly independent; $2^{\circ}$ every solution of the system can be linearly represented by them, then they are called a fundamental system of solutions.

> **Theorem 3.7.1 (Dimension of the Solution Space)**<br>The dimension of the solution space $W$ of an $n$-variable homogeneous linear system over a number field $K$ is

$$
\dim W=n-\text{rank}\left(A\right),
$$

where $A$ is the coefficient matrix.

---

## 3.7-1(1)

Find a fundamental system of solutions of the following homogeneous linear system over a number field $K$, and write down its solution set.

$$
\begin{cases}
x_{1}-3x_{2}+x_{3}-2x_{4}=0,\\
-5x_{1}+x_{2}-2x_{3}+3x_{4}=0,\\
-x_{1}-11x_{2}+2x_{3}-5x_{4}=0,\\
3x_{1}+5x_{2}+x_{4}=0.
\end{cases}
$$

### Solution 3.7-1(1)

By **Definition 3.7.1 (Fundamental System of Solutions)** and **Theorem 3.7.1 (Dimension of the Solution Space)**, perform elementary row operations on the coefficient matrix:

$$
\left[\begin{array}{rrrr}
1 & -3 & 1 & -2\\
-5 & 1 & -2 & 3\\
-1 & -11 & 2 & -5\\
3 & 5 & 0 & 1
\end{array}\right]
\xrightarrow{\text{row ops}}
\left[\begin{array}{rrrr}
1 & -3 & 1 & -2\\
0 & -14 & 3 & -7\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0
\end{array}\right].
$$

The rank is $2$ and the number of unknowns is $4$. By **Theorem 3.7.1 (Dimension of the Solution Space)**, the solution space has dimension $4-2=2$, so the fundamental system contains $2$ vectors.

The general solution:

$$
\begin{cases}
x_{1}=\dfrac{-5x_{3}+7x_{4}}{14},\\
x_{2}=\dfrac{3x_{3}-7x_{4}}{14},
\end{cases}
$$

where $x_{3},x_{4}$ are free variables.

Set $x_{3}=14,x_{4}=0$ to get $\eta_{1}=\left(-5,3,14,0\right)^{\top}$.

Set $x_{3}=0,x_{4}=14$ to get $\eta_{2}=\left(7,-7,0,14\right)^{\top}$.

By **Definition 3.7.1 (Fundamental System of Solutions)**, $\eta_{1},\eta_{2}$ are linearly independent and every solution can be represented by them, so they form a fundamental system.

The solution set:

$$
W=\left\{k_{1}\eta_{1}+k_{2}\eta_{2}\mid k_{1},k_{2}\in K\right\}.
$$

$\blacksquare$

---

## 3.7-1(2)

Find a fundamental system of solutions of the following homogeneous linear system over a number field $K$, and write down its solution set.

$$
\begin{cases}
3x_{1}-x_{2}+2x_{3}+x_{4}=0,\\
x_{1}+3x_{2}-x_{3}+2x_{4}=0,\\
-2x_{1}+5x_{2}+x_{3}-x_{4}=0,\\
3x_{1}+10x_{2}+x_{3}+4x_{4}=0,\\
-2x_{1}+15x_{2}-4x_{3}+4x_{4}=0.
\end{cases}
$$

### Solution 3.7-1(2)

By **Definition 3.7.1 (Fundamental System of Solutions)** and **Theorem 3.7.1 (Dimension of the Solution Space)**, perform elementary row operations on the coefficient matrix:

$$
\left[\begin{array}{rrrr}
3 & -1 & 2 & 1\\
1 & 3 & -1 & 2\\
-2 & 5 & 1 & -1\\
3 & 10 & 1 & 4\\
-2 & 15 & -4 & 4
\end{array}\right]
\xrightarrow{\text{row ops}}
\left[\begin{array}{rrrr}
1 & 3 & -1 & 2\\
0 & 1 & 4 & -2\\
0 & 0 & -45 & 25\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0
\end{array}\right].
$$

The rank is $3$ and the number of unknowns is $4$, so the fundamental system contains $4-3=1$ vector.

The general solution:

$$
\begin{cases}
x_{1}=-\dfrac{7}{9}x_{4},\\
x_{2}=-\dfrac{2}{9}x_{4},\\
x_{3}=\dfrac{5}{9}x_{4},
\end{cases}
$$

where $x_{4}$ is a free variable.

Set $x_{4}=9$ to get $\eta_{1}=\left(-7,-2,5,9\right)^{\top}$.

By **Definition 3.7.1 (Fundamental System of Solutions)**, $\eta_{1}$ is linearly independent and every solution can be represented by it, so it forms a fundamental system.

The solution set:

$$
W=\left\{k\eta_{1}\mid k\in K\right\}.
$$

$\blacksquare$

---

## 3.7-4

Prove: let the coefficient matrix of an $n$-variable homogeneous linear system have rank $r$ $\left(r< n\right)$, and let $\delta_{1},\delta_{2},\cdots,\delta_{m}$ be solution vectors of the system. Then

$$
\text{rank}\left\{\delta_{1},\delta_{2},\cdots,\delta_{m}\right\}\le n-r.
$$

### Solution 3.7-4

By **Theorem 3.7.1 (Dimension of the Solution Space)**, the solution space $W$ of the homogeneous system has dimension

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

---

## 3.7-5

Let the determinant of the coefficient matrix $A$ of an $n$-variable homogeneous linear system of $n$ equations be zero, and let the cofactor $A_{kl}$ of the $\left(k,l\right)$-entry of $A$ be nonzero. Prove that

$$
\eta_{1}=\begin{bmatrix}A_{k1}\\A_{k2}\\\vdots\\A_{kn}\end{bmatrix}
$$

is a fundamental system of solutions of this homogeneous system.

### Solution 3.7-5

By **Definition 3.7.1 (Fundamental System of Solutions)** and **Theorem 3.7.1 (Dimension of the Solution Space)**, to prove that $\eta_{1}$ is a fundamental system we verify three conditions: $\eta_{1}$ is a solution, $\eta_{1}\ne0$, and the solution space has dimension $1$.

**Verify that $\eta_{1}$ is a solution.** For each $i=1,2,\cdots,n$, compute

$$
a_{i1}A_{k1}+a_{i2}A_{k2}+\cdots+a_{in}A_{kn}.
$$

When $i=k$, this is $\left|A\right|=0$ (by hypothesis).

When $i\ne k$, this is the determinant obtained by replacing row $k$ of $A$ with row $i$; since two rows are identical, the determinant is $0$.

Hence for all $i$ the above is $0$, i.e. $A\eta_{1}=0$.

**Verify that $\eta_{1}\ne0$.** Because $A_{kl}\ne0$, the $l$th component of $\eta_{1}$ is nonzero, so $\eta_{1}\ne0$.

**Verify that the solution space has dimension $1$.** Since $\left|A\right|=0$, $\text{rank}\left(A\right)< n$.

Also, since $A_{kl}\ne0$, $A$ has a nonzero $\left(n-1\right)$-minor (the minor after deleting row $k$ and column $l$), so $\text{rank}\left(A\right)\ge n-1$.

Thus $\text{rank}\left(A\right)=n-1$.

By **Theorem 3.7.1 (Dimension of the Solution Space)**, the solution space has dimension $n-\text{rank}\left(A\right)=1$.

$\eta_{1}$ is a nonzero solution, and by itself forms a basis of the solution space, i.e. a fundamental system. $\blacksquare$

---

## 3.7-7

Let $A_{1}$ be the submatrix of the $s\times n$ matrix $A=\left(a_{ij}\right)$ formed by its first $s-1$ rows. Prove: if every solution of the homogeneous system with coefficient matrix $A_{1}$ is also a solution of the equation

$$
a_{s1}x_{1}+a_{s2}x_{2}+\cdots+a_{sn}x_{n}=0,
$$

then the $s$th row of $A$ can be linearly represented by the first $s-1$ rows of $A$.

### Solution 3.7-7

By **Theorem 3.7.1 (Dimension of the Solution Space)**, the solution space of a homogeneous system is the orthogonal complement of the row space of the coefficient matrix. Let $V_{1}$ be the row space of $A_{1}$; then the solution space $W_{1}$ of the homogeneous system with coefficient matrix $A_{1}$ is $W_{1}=V_{1}^{\perp}$ (the orthogonal complement of $V_{1}$).

By hypothesis, every $x$ in $W_{1}$ satisfies $a_{s1}x_{1}+\cdots+a_{sn}x_{n}=0$.

That is, the row vector of the $s$th row $\gamma_{s}=\left(a_{s1},\cdots,a_{sn}\right)$ is orthogonal to every vector in $W_{1}$.

Hence $\gamma_{s}\in\left(W_{1}\right)^{\perp}=V_{1}$.

Therefore $\gamma_{s}$ can be linearly represented by the row vectors of $A_{1}$, i.e. the $s$th row of $A$ can be linearly represented by the first $s-1$ rows of $A$. $\blacksquare$
