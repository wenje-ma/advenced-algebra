# week17

> **Theorem 3.8.1 (Solution Set Structure of an Inhomogeneous System)**<br>If an $n$-variable inhomogeneous linear system over a number field $K$ is solvable, then its solution set is $U=\gamma_{0}+W$, where $\gamma_{0}$ is a particular solution and $W$ is the solution space of the derived homogeneous system.

---

## 3.8-1(1)

Find the solution set of the following inhomogeneous linear system over a number field $K$:

$$
\begin{cases}
x_{1}-5x_{2}+2x_{3}-3x_{4}=11,\\
-3x_{1}+x_{2}-4x_{3}+2x_{4}=-5,\\
-x_{1}-9x_{2}-4x_{4}=17,\\
5x_{1}+3x_{2}+6x_{3}-x_{4}=-1.
\end{cases}
$$

### Solution 3.8-1(1)

By **Theorem 3.8.1 (Solution Set Structure of an Inhomogeneous System)**, perform elementary row operations on the augmented matrix:

$$
\left[\begin{array}{rrrr|r}
1 & -5 & 2 & -3 & 11\\
-3 & 1 & -4 & 2 & -5\\
-1 & -9 & 0 & -4 & 17\\
5 & 3 & 6 & -1 & -1
\end{array}\right]
\xrightarrow{\text{row ops}}
\left[\begin{array}{rrrr|r}
1 & -5 & 2 & -3 & 11\\
0 & -14 & 2 & -7 & 28\\
0 & 0 & 0 & 0 & 0\\
0 & 0 & 0 & 0 & 0
\end{array}\right].
$$

The rank is $2$, equal to the rank of the augmented matrix, so the system is solvable.

The general solution:

$$
\begin{cases}
x_{1}=-\dfrac{9}{7}x_{3}+\dfrac{1}{2}x_{4}+1,\\
x_{2}=\dfrac{1}{7}x_{3}-\dfrac{1}{2}x_{4}-2,
\end{cases}
$$

where $x_{3},x_{4}$ are free variables.

Set $x_{3}=x_{4}=0$ to get the particular solution $\gamma_{0}=\left(1,-2,0,0\right)^{\top}$.

Fundamental system of the derived homogeneous system:

Set $x_{3}=7,x_{4}=0$ to get $\eta_{1}=\left(-9,1,7,0\right)^{\top}$.

Set $x_{3}=0,x_{4}=2$ to get $\eta_{2}=\left(1,-1,0,2\right)^{\top}$.

By **Theorem 3.8.1 (Solution Set Structure of an Inhomogeneous System)**, the solution set is the particular solution $\gamma_{0}$ plus the solution space $W$ of the derived system:

$$
U=\left\{\gamma_{0}+k_{1}\eta_{1}+k_{2}\eta_{2}\mid k_{1},k_{2}\in K\right\}.
$$

$\blacksquare$

---

## 3.8-2

Prove: an inhomogeneous linear system of $n$ equations in $n$ variables has a unique solution if and only if its derived homogeneous system has only the zero solution.

### Solution 3.8-2

By **Theorem 3.8.1 (Solution Set Structure of an Inhomogeneous System)**, the solution set of the inhomogeneous system is $U=\gamma_{0}+W$, where $W$ is the solution space of the derived homogeneous system. We prove that the inhomogeneous system has a unique solution if and only if its derived system has only the zero solution.

Let the inhomogeneous system be $Ax=\beta$, where $A$ is an $n\times n$ matrix; the derived system is $Ax=0$.

**Necessity.** Suppose the inhomogeneous system has a unique solution; then

$$
\text{rank}\left(A\right)=\text{rank}\left(\overline{A}\right)=n\ \text{(the rank of the coefficient matrix equals the number of unknowns)}.
$$

The derived system $Ax=0$ has coefficient matrix of rank $n$ and $n$ unknowns, so it has only the zero solution.

**Sufficiency.** Suppose the derived system has only the zero solution; then $\text{rank}\left(A\right)=n$.

$A$ is an $n\times n$ matrix with $\text{rank}\left(A\right)=n$, so $\left|A\right|\ne0$.

The derived system having only the zero solution means the solution space $W=\left\{0\right\}$, so the inhomogeneous system's solution set $U=\gamma_{0}+W=\left\{\gamma_{0}\right\}$, i.e. it has a unique solution. $\blacksquare$

---

## 3.8-4

Prove: if $\gamma_{0}$ is a particular solution of inhomogeneous linear system (1), and $\eta_{1},\eta_{2},\cdots,\eta_{t}$ is a fundamental system of its derived homogeneous system. Set

$$
\gamma_{1}=\gamma_{0}+\eta_{1},\gamma_{2}=\gamma_{0}+\eta_{2},\cdots,\gamma_{t}=\gamma_{0}+\eta_{t}.
$$

Then any solution $\gamma$ of inhomogeneous linear system (1) can be expressed as

$$
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},
$$

where

$$
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

### Solution 3.8-4

By **Theorem 3.8.1 (Solution Set Structure of an Inhomogeneous System)**, the solution set of the inhomogeneous system is $U=\gamma_{0}+W$, where $W$ is the solution space of the derived homogeneous system.

Take any $\gamma\in U$; then $\gamma-\gamma_{0}\in W$.

Because $\eta_{1},\eta_{2},\cdots,\eta_{t}$ is a basis of $W$, there exist $k_{1},\cdots,k_{t}\in K$ such that

$$
\gamma-\gamma_{0}=k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{t}\eta_{t}.
$$

Substituting $\eta_{i}=\gamma_{i}-\gamma_{0}$:

$$
\gamma=\gamma_{0}+k_{1}\left(\gamma_{1}-\gamma_{0}\right)+k_{2}\left(\gamma_{2}-\gamma_{0}\right)+\cdots+k_{t}\left(\gamma_{t}-\gamma_{0}\right)=\left(1-k_{1}-k_{2}-\cdots-k_{t}\right)\gamma_{0}+k_{1}\gamma_{1}+k_{2}\gamma_{2}+\cdots+k_{t}\gamma_{t}.
$$

Set

$$
u_{0}=1-k_{1}-k_{2}-\cdots-k_{t},
$$

$u_{1}=k_{1}$, $\cdots$, $u_{t}=k_{t}$.

Then

$$
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

Any solution of the inhomogeneous system can be expressed in the above form. Hence

$$
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},\quad
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

$\blacksquare$
