# Assignment 17

> **Theorem 1** (Structure of solution set of inhomogeneous systems)<br>If an inhomogeneous linear system of $n$ unknowns over $K$ is solvable, then its solution set is $U=\gamma_{0}+W$, where $\gamma_{0}$ is a particular solution and $W$ is the solution space of the associated homogeneous system.

### Problem 1

(Problem 3.8-1(1)) Find the solution set of the following inhomogeneous linear system over $K$:

$$
\begin{cases}
x_{1}-5x_{2}+2x_{3}-3x_{4}=11,\\
-3x_{1}+x_{2}-4x_{3}+2x_{4}=-5,\\
-x_{1}-9x_{2}-4x_{4}=17,\\
5x_{1}+3x_{2}+6x_{3}-x_{4}=-1.
\end{cases}
$$

### Solution to Problem 1

By **Theorem 1** (Structure of solution set), perform elementary row operations on the augmented matrix:

$$
\left[\begin{array}{rrrr\left|r}
1 & -5 & 2 & -3 & 11\\
-3 & 1 & -4 & 2 & -5\\
-1 & -9 & 0 & -4 & 17\\
5 & 3 & 6 & -1 & -1
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr\right|r}
1 & -5 & 2 & -3 & 11\\
0 & -14 & 2 & -7 & 28\\
0 & 0 & 0 & 0 & 0\\
0 & 0 & 0 & 0 & 0
\end{array}\right].
$$

The rank is $2$, equal to the rank of the augmented matrix, so the system is solvable.

General solution:

$$
\begin{cases}
x_{1}=-\frac{9}{7}x_{3}+\frac{1}{2}x_{4}+1,\\
x_{2}=\frac{1}{7}x_{3}-\frac{1}{2}x_{4}-2,
\end{cases}
$$

where $x_{3},x_{4}$ are free variables.

Setting $x_{3}=x_{4}=0$, we get the particular solution $\gamma_{0}=\left(1,-2,0,0\right)^{T}$.

Fundamental system of the associated homogeneous system:

Setting $x_{3}=7,x_{4}=0$, we get $\eta_{1}=\left(-9,1,7,0\right)^{T}$.

Setting $x_{3}=0,x_{4}=2$, we get $\eta_{2}=\left(1,-1,0,2\right)^{T}$.

By **Theorem 1** (Structure of solution set), the solution set is the particular solution $\gamma_{0}$ plus the solution space $W$ of the associated homogeneous system:

$$
U=\left\{\gamma_{0}+k_{1}\eta_{1}+k_{2}\eta_{2}\middle|k_{1},k_{2}\in K\right\}.
$$

$\blacksquare$

### Problem 2

(Problem 3.8-2) Prove: an inhomogeneous system of $n$ equations in $n$ unknowns has a unique solution if and only if its associated homogeneous system has only the zero solution.

### Solution to Problem 2

By **Theorem 1** (Structure of solution set), the solution set of the inhomogeneous system is $U=\gamma_{0}+W$, where $W$ is the solution space of the associated homogeneous system. We prove that the inhomogeneous system has a unique solution iff the associated homogeneous system has only the zero solution.

Let the inhomogeneous system be $Ax=\beta$, where $A$ is an $n\times n$ matrix; the associated homogeneous system is $Ax=0$.

**Necessity.** Suppose the inhomogeneous system has a unique solution. Then

$$
\text{rank}\left(A\right)=\text{rank}\left(\bar{A}\right)=n\ \text{\left(系数矩阵的秩等于未知量数目\right)}.
$$

The coefficient matrix of the associated homogeneous system $Ax=0$ has rank $n$, and the number of unknowns is $n$, so it has only the zero solution.

**Sufficiency.** Suppose the associated homogeneous system has only the zero solution. Then $\text{rank}\left(A\right)=n$.

$A$ is an $n\times n$ matrix and $\text{rank}\left(A\right)=n$, so $\left|A\right|\ne0$.

That the associated homogeneous system has only the zero solution means $W=\left\{0\right\}$, so the solution set of the inhomogeneous system is $U=\gamma_{0}+W=\left\{\gamma_{0}\right\}$, i.e., it has a unique solution. $\blacksquare$

### Problem 3

(Problem 3.8-4) Prove: if $\gamma_{0}$ is a particular solution of the inhomogeneous linear system (1), and $\eta_{1},\eta_{2},\cdots,\eta_{t}$ is a fundamental system of its associated homogeneous system. Let

$$
\gamma_{1}=\gamma_{0}+\eta_{1},\gamma_{2}=\gamma_{0}+\eta_{2},\cdots,\gamma_{t}=\gamma_{0}+\eta_{t}.
$$

then any solution $\gamma$ of the inhomogeneous system (1) can be expressed as

$$
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},
$$

where

$$
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

### Solution to Problem 3

By **Theorem 1** (Structure of solution set), the solution set of the inhomogeneous system is $U=\gamma_{0}+W$, where $W$ is the solution space of the associated homogeneous system.

The solution set of the inhomogeneous system is $U=\gamma_{0}+W$, where $W$ is the solution space of the associated homogeneous system.

Take any $\gamma\in U$. Then $\gamma-\gamma_{0}\in W$.

Since $\eta_{1},\eta_{2},\cdots,\eta_{t}$ is a basis of $W$, there exist $k_{1},\cdots,k_{t}\in K$ such that

$$
\gamma-\gamma_{0}=k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{t}\eta_{t}.
$$

Substituting $\eta_{i}=\gamma_{i}-\gamma_{0}$:

$$
\gamma =\gamma_{0}+k_{1}\left(\gamma_{1}-\gamma_{0}\right)+k_{2}\left(\gamma_{2}-\gamma_{0}\right)+\cdots+k_{t}\left(\gamma_{t}-\gamma_{0}\right)=\left(1-k_{1}-k_{2}-\cdots-k_{t}\right)\gamma_{0}+k_{1}\gamma_{1}+k_{2}\gamma_{2}+\cdots+k_{t}\gamma_{t}.
$$

Let

$$
u_{0}=1-k_{1}-k_{2}-\cdots-k_{t},
$$

$u_{1}=k_{1}$, $\cdots$, $u_{t}=k_{t}$.

then

$$
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

Any solution of the inhomogeneous system can be expressed in the above form. Therefore

$$
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},\
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

$\blacksquare$
