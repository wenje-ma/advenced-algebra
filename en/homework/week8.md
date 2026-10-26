# Assignment 8

> **Theorem 1** (Cramer's Rule)<br>For an $n$-variable system of $n$ linear equations, if its coefficient determinant $\left|A\right|\ne0$, then it has a unique solution; if its coefficient determinant $\left|A\right|=0$, then it has no solution or infinitely many solutions.

> **Corollary 2** (Condition for a Homogeneous System to Have a Nontrivial Solution)<br>An $n$-variable homogeneous system of $n$ linear equations has only the zero solution if and only if its coefficient determinant is not equal to $0$. Hence, an $n$-variable homogeneous system of $n$ linear equations has a nontrivial solution if and only if its coefficient determinant is equal to $0$.

### Problem 1

(Problem 2.5-4) For what values of $a,b$ does the following homogeneous system of linear equations have a nontrivial solution?

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=0,\\
x_{1}+bx_{2}+x_{3}=0,\\
x_{1}+2bx_{2}+x_{3}=0.
\end{cases}
$$

### Solution to Problem 1

By **Corollary 2** (Condition for a Homogeneous System to Have a Nontrivial Solution), a homogeneous system of linear equations has a nontrivial solution if and only if its coefficient determinant equals $0$.

The coefficient determinant is

$$
\left|\begin{array}{ccc}
a & 1 & 1\\
1 & b & 1\\
1 & 2b & 1
\end{array}\right|=a\left(b\cdot1-1\cdot2b\right)-1\left(1\cdot1-1\cdot1\right)+1\left(1\cdot2b-b\cdot1\right)=a\left(-b\right)-0+b=b\left(1-a\right).
$$

Setting it equal to $0$, we get $b\left(1-a\right)=0$, i.e. $b=0$ or $a=1$.

Hence when $b=0$ or $a=1$, this homogeneous system of linear equations has a nontrivial solution. $\blacksquare$

### Problem 2

(Problem 2.5-5) For what values of $a,b$ does the following system of linear equations have a unique solution?

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=2.
\end{cases}
$$

### Solution to Problem 2

By **Theorem 1** (Cramer's Rule), a system of linear equations has a unique solution if and only if its coefficient determinant is not equal to $0$.

From the previous problem, the coefficient determinant is $b\left(1-a\right)$.

Hence when $b\ne 0$ and $a\ne 1$, the system has a unique solution. $\blacksquare$

### Problem 3

(Problem 2.5-6) For the system of linear equations in Problem 5, for what values of $a,b$ does the system have no solution? For what values of $a,b$ does the system have infinitely many solutions?

### Solution to Problem 3

By **Theorem 1** (Cramer's Rule), when the coefficient determinant equals $0$, the system has no solution or infinitely many solutions.

**Case 1: $b=0$**.

The system becomes

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+x_{3}=1,\\
x_{1}+x_{3}=2.
\end{cases}
$$

The last two equations are contradictory ($1\ne 2$), so the system has no solution.

**Case 2: $a=1$ and $b\ne 0$**.

The system becomes

$$
\begin{cases}
x_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=2.
\end{cases}
$$

Subtracting the $1$st row from the $2$nd row: $\left(b-1\right)x_{2}=-1$.

Subtracting the $1$st row from the $3$rd row: $\left(2b-1\right)x_{2}=0$.

If $2b-1\ne 0$, i.e. $b\ne\frac{1}{2}$, then from the $3$rd row we get $x_{2}=0$, and substituting into the $2$nd row gives $0=-1$, a contradiction. No solution.

If $2b-1=0$, i.e. $b=\frac{1}{2}$, then the $3$rd row becomes an identity. From the $2$nd row we get $\left(\frac{1}{2}-1\right)x_{2}=-1$, i.e. $x_{2}=2$. Substituting into the $1$st row gives $x_{1}+x_{3}=0$.

Hence there are infinitely many solutions: $x_{2}=2$, $x_{1}+x_{3}=0$.

In summary:

- No solution: $b=0$, or $a=1$ and $b\ne\frac{1}{2}$.
- Infinitely many solutions: $a=1$ and $b=\frac{1}{2}$.

$\blacksquare$

### Problem 4

(Problem 2.5-7) Discuss when the following system of linear equations has a unique solution, infinitely many solutions, or no solution.

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=1.
\end{cases}
$$

### Solution to Problem 4

By **Theorem 1** (Cramer's Rule), the coefficient determinant is still $b\left(1-a\right)$.

**Unique solution**: $b\ne 0$ and $a\ne 1$.

**Case 1: $b=0$**.

The system becomes

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+x_{3}=1,\\
x_{1}+x_{3}=1.
\end{cases}
$$

The last two equations are identical. Substituting into the $1$st row: $ax_{1}+x_{2}+\left(1-x_{1}\right)=2$, i.e. $\left(a-1\right)x_{1}+x_{2}=1$.

Regardless of the value of $a$, $x_{1}$ is free, $x_{2}=1-\left(a-1\right)x_{1}$, $x_{3}=1-x_{1}$. There are infinitely many solutions.

**Case 2: $a=1$ and $b\ne 0$**.

The system becomes

$$
\begin{cases}
x_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=1.
\end{cases}
$$

Subtracting the $1$st row from the $2$nd row: $\left(b-1\right)x_{2}=-1$.

Subtracting the $1$st row from the $3$rd row: $\left(2b-1\right)x_{2}=-1$.

If $b\ne 1$ and $b\ne\frac{1}{2}$, then

$$
x_{2}=\frac{1}{1-b}=\frac{1}{1-2b}
$$

which gives $b=0$, a contradiction.

If $b=1$, then subtracting the $1$st row from the $2$nd row gives $0=-1$, a contradiction.

If $b=\frac{1}{2}$, then subtracting the $1$st row from the $3$rd row gives $0=-1$, a contradiction.

Hence when $a=1$ and $b\ne 0$, there is no solution.

In summary:

- Unique solution: $b\ne 0$ and $a\ne 1$.
- Infinitely many solutions: $b=0$.
- No solution: $a=1$ and $b\ne 0$.

$\blacksquare$
