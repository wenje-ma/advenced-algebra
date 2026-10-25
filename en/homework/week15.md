# Assignment 15

> **Theorem 1** (Solvability criterion for linear systems)<br>A linear system
> $$
> x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
> $$
> is solvable if and only if its coefficient matrix and augmented matrix have the same rank.

> **Theorem 2** (Criterion for number of solutions)<br>If a linear system is solvable, then: if the rank of the coefficient matrix equals the number of unknowns $n$, the system has a unique solution; if the rank is less than $n$, the system has infinitely many solutions.

### Problem 1

(Problem 3.6-2) Determine whether the following linear system is solvable and how many solutions it has.

$$
\begin{cases}
x_{1}+ax_{2}+a^{2}x_{3}+\cdots+a^{n-1}x_{n}=b_{1},\\
x_{1}+a^{2}x_{2}+a^{4}x_{3}+\cdots+a^{2\left(n-1\right)}x_{n}=b_{2},\\
\cdots\cdots\cdots\cdots\\
x_{1}+a^{s}x_{2}+a^{2s}x_{3}+\cdots+a^{s\left(n-1\right)}x_{n}=b_{s},
\end{cases}
$$

where $s< n$, $a\ne0$, and when $0< r< s$, $a^{r}\ne1$.

### Solution to Problem 1

By **Theorem 1** (Solvability criterion) and **Theorem 2** (Criterion for number of solutions), we need to compare the ranks of the coefficient matrix and the augmented matrix.

The coefficient matrix $A$ is an $s\times n$ matrix. Take the $s$-th order minor formed by the first $s$ columns of $A$:

$$
D=\left|\begin{array}{cccc}
1 & a & a^{2} & \cdots & a^{s-1}\\
1 & a^{2} & a^{4} & \cdots & a^{2\left(s-1\right)}\\
\vdots & \vdots & \vdots & & \vdots\\
1 & a^{s} & a^{2s} & \cdots & a^{s\left(s-1\right)}
\end{array}\right|.
$$

This is a Vandermonde determinant,

$$
D=\prod_{1\le i< j\le s}\left(a^{j}-a^{i}\right).
$$

Since $a\ne 0$ and when $0< r< s$, $a^{r}\ne 1$, the values $a,a^{2},\cdots,a^{s}$ are all distinct, so $D\ne 0$.

Therefore $\text{rank}\left(A\right)\ge s$.

Also, $A$ has only $s$ rows, so $\text{rank}\left(A\right)\le s$.

Hence $\text{rank}\left(A\right)=s$.

The augmented matrix $\bar{A}$ is $A$ with one additional column, so $\text{rank}\left(\bar{A}\right)\ge\text{rank}\left(A\right)=s$.

Also, $\bar{A}$ has only $s$ rows, so $\text{rank}\left(\bar{A}\right)\le s$.

Hence $\text{rank}\left(\bar{A}\right)=s=\text{rank}\left(A\right)$.

Therefore the system is solvable.

Also, $\text{rank}\left(A\right)=s< n$ (number of unknowns), so the system has infinitely many solutions. $\blacksquare$

### Problem 2

(Problem 3.6-4) Given the linear system

$$
\begin{cases}
a_{11}x_{1}+a_{12}x_{2}+\cdots+a_{1n}x_{n}=b_{1},\\
a_{21}x_{1}+a_{22}x_{2}+\cdots+a_{2n}x_{n}=b_{2},\\
\cdots\cdots\cdots\cdots\\
a_{n1}x_{1}+a_{n2}x_{2}+\cdots+a_{nn}x_{n}=b_{n}
\end{cases}
$$

whose coefficient matrix $A$ has the same rank as the following matrix $B$:

$$
B=\left[\begin{array}{ccccc}
a_{11} & a_{12} & \cdots & a_{1n} & b_{1}\\
a_{21} & a_{22} & \cdots & a_{2n} & b_{2}\\
\vdots & \vdots & & \vdots & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn} & b_{n}\\
b_{1} & b_{2} & \cdots & b_{n} & 0
\end{array}\right].
$$

Prove that the above linear system is solvable.

### Solution to Problem 2

By **Theorem 1** (Solvability criterion), to prove the system is solvable, we need to show that the coefficient matrix $A$ and the augmented matrix $\bar{A}$ have the same rank.

Let the augmented matrix be $\bar{A}$, i.e., $\bar{A}=\left[A,b\right]$, where $b=\left(b_{1},b_{2},\cdots,b_{n}\right)^{T}$.

Note that $\bar{A}$ is the first $n$ rows of $B$, so $\bar{A}$ is a submatrix of $B$.

Therefore $\text{rank}\left(\bar{A}\right)\le\text{rank}\left(B\right)$.

Also, $A$ is a submatrix of $\bar{A}$, so $\text{rank}\left(A\right)\le\text{rank}\left(\bar{A}\right)$.

By the hypothesis $\text{rank}\left(A\right)=\text{rank}\left(B\right)$, we have

$$
\text{rank}\left(A\right)\le\text{rank}\left(\bar{A}\right)\le\text{rank}\left(B\right)=\text{rank}\left(A\right).
$$

Therefore $\text{rank}\left(\bar{A}\right)=\text{rank}\left(A\right)$.

The system is solvable. $\blacksquare$
