# week8

> **Theorem 2.5.1 (Cramer's Rule)**<br>For a system of $n$ equations in $n$ variables, if its coefficient determinant $\left|A\right|\ne0$, then it has a unique solution; if its coefficient determinant $\left|A\right|=0$, then it has no solution or infinitely many solutions.

> **Corollary 2.5.2 (Condition for a Nontrivial Solution of a Homogeneous System)**<br>A homogeneous system of $n$ equations in $n$ variables has only the zero solution if and only if its coefficient determinant is nonzero. Consequently, such a homogeneous system has a nontrivial solution if and only if its coefficient determinant is zero.

---

## 2.5-4

For which values of $a,b$ does the following homogeneous system have a nontrivial solution?

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=0,\\
x_{1}+bx_{2}+x_{3}=0,\\
x_{1}+2bx_{2}+x_{3}=0.
\end{cases}
$$

### Solution 2.5-4

By **Corollary 2.5.2 (Condition for a Nontrivial Solution of a Homogeneous System)**, a homogeneous system has a nontrivial solution if and only if its coefficient determinant is zero.

The coefficient determinant is

$$
\left|\begin{array}{ccc}
a & 1 & 1\\
1 & b & 1\\
1 & 2b & 1
\end{array}\right|=a\left(b\cdot1-1\cdot2b\right)-1\left(1\cdot1-1\cdot1\right)+1\left(1\cdot2b-b\cdot1\right)=a\left(-b\right)-0+b=b\left(1-a\right).
$$

Setting it equal to $0$ gives $b\left(1-a\right)=0$, i.e. $b=0$ or $a=1$.

Hence the homogeneous system has a nontrivial solution when $b=0$ or $a=1$. $\blacksquare$

---

## 2.5-5

For which values of $a,b$ does the following linear system have a unique solution?

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=2.
\end{cases}
$$

### Solution 2.5-5

By **Theorem 2.5.1 (Cramer's Rule)**, a linear system has a unique solution if and only if its coefficient determinant is nonzero.

From the previous problem, the coefficient determinant is $b\left(1-a\right)$.

Hence the system has a unique solution when $b\ne 0$ and $a\ne 1$. $\blacksquare$

---

## 2.5-6

For the linear system in Problem 5, for which values of $a,b$ does the system have no solution? For which values of $a,b$ does it have infinitely many solutions?

### Solution 2.5-6

By **Theorem 2.5.1 (Cramer's Rule)**, when the coefficient determinant is zero, the system has no solution or infinitely many solutions.

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

Subtract row $1$ from row $2$: $\left(b-1\right)x_{2}=-1$.

Subtract row $1$ from row $3$: $\left(2b-1\right)x_{2}=0$.

If $2b-1\ne 0$, i.e. $b\ne\frac{1}{2}$, then row $3$ gives $x_{2}=0$, and substituting into row $2$ gives $0=-1$, a contradiction. No solution.

If $2b-1=0$, i.e. $b=\frac{1}{2}$, then row $3$ becomes an identity. Row $2$ gives $\left(\frac{1}{2}-1\right)x_{2}=-1$, i.e. $x_{2}=2$. Substituting into row $1$ gives $x_{1}+x_{3}=0$.

Hence there are infinitely many solutions: $x_{2}=2$, $x_{1}+x_{3}=0$.

In summary:

- No solution: $b=0$, or $a=1$ and $b\ne\frac{1}{2}$.
- Infinitely many solutions: $a=1$ and $b=\frac{1}{2}$.

$\blacksquare$

---

## 2.5-7

Discuss when the following linear system has a unique solution, infinitely many solutions, or no solution.

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=1.
\end{cases}
$$

### Solution 2.5-7

By **Theorem 2.5.1 (Cramer's Rule)**, the coefficient determinant is still $b\left(1-a\right)$.

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

The last two equations are identical. Substituting into row $1$: $ax_{1}+x_{2}+\left(1-x_{1}\right)=2$, i.e. $\left(a-1\right)x_{1}+x_{2}=1$.

Regardless of $a$, $x_{1}$ is free, with $x_{2}=1-\left(a-1\right)x_{1}$ and $x_{3}=1-x_{1}$. There are infinitely many solutions.

**Case 2: $a=1$ and $b\ne 0$**.

The system becomes

$$
\begin{cases}
x_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=1.
\end{cases}
$$

Subtract row $1$ from row $2$: $\left(b-1\right)x_{2}=-1$.

Subtract row $1$ from row $3$: $\left(2b-1\right)x_{2}=-1$.

If $b\ne 1$ and $b\ne\frac{1}{2}$, then

$$
x_{2}=\frac{1}{1-b}=\frac{1}{1-2b},
$$

which gives $b=0$, a contradiction.

If $b=1$, then subtracting row $1$ from row $2$ gives $0=-1$, a contradiction.

If $b=\frac{1}{2}$, then subtracting row $1$ from row $3$ gives $0=-1$, a contradiction.

Hence when $a=1$ and $b\ne 0$, there is no solution.

In summary:

- Unique solution: $b\ne 0$ and $a\ne 1$.
- Infinitely many solutions: $b=0$.
- No solution: $a=1$ and $b\ne 0$.

$\blacksquare$
