# week15

> **Basic Knowledge: Formula for the Vandermonde Determinant**<br>The $s\times s$ Vandermonde determinant in $a_{1},a_{2},\cdots,a_{s}$

$$
\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{1} & a_{2} & \cdots & a_{s}\\
\vdots & \vdots & & \vdots\\
a_{1}^{s-1} & a_{2}^{s-1} & \cdots & a_{s}^{s-1}
\end{array}\right|=\prod_{1\le i< j\le s}\left(a_{j}-a_{i}\right).
$$

> **Theorem 3.6.1 (Solvability Criterion for a Linear System)**<br>The linear system

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

is solvable if and only if its coefficient matrix and its augmented matrix have the same rank.

> **Theorem 3.6.2 (Criterion for the Number of Solutions)**<br>Suppose a linear system is solvable. If the rank of the coefficient matrix equals the number $n$ of unknowns, the system has a unique solution; if the rank is less than $n$, the system has infinitely many solutions.

---

## 3.6-2

Determine whether the following linear system is solvable and how many solutions it has.

$$
\begin{cases}
x_{1}+ax_{2}+a^{2}x_{3}+\cdots+a^{n-1}x_{n}=b_{1},\\
x_{1}+a^{2}x_{2}+a^{4}x_{3}+\cdots+a^{2\left(n-1\right)}x_{n}=b_{2},\\
\cdots\cdots\cdots\cdots\\
x_{1}+a^{s}x_{2}+a^{2s}x_{3}+\cdots+a^{s\left(n-1\right)}x_{n}=b_{s},
\end{cases}
$$

where $s< n$, $a\ne0$, and $a^{r}\ne1$ whenever $0< r< s$.

### Solution 3.6-2

By **Theorem 3.6.1 (Solvability Criterion for a Linear System)** and **Theorem 3.6.2 (Criterion for the Number of Solutions)**, we compare the ranks of the coefficient matrix and the augmented matrix.

The coefficient matrix $A$ is an $s\times n$ matrix. Take the $s\times s$ minor formed by the first $s$ columns of $A$:

$$
D=\left|\begin{array}{cccc}
1 & a & a^{2} & \cdots & a^{s-1}\\
1 & a^{2} & a^{4} & \cdots & a^{2\left(s-1\right)}\\
\vdots & \vdots & \vdots & & \vdots\\
1 & a^{s} & a^{2s} & \cdots & a^{s\left(s-1\right)}
\end{array}\right|.
$$

By **Basic Knowledge: Formula for the Vandermonde Determinant**, this is a Vandermonde determinant,

$$
D=\prod_{1\le i< j\le s}\left(a^{j}-a^{i}\right).
$$

Because $a\ne 0$ and $a^{r}\ne 1$ whenever $0< r< s$, the numbers $a,a^{2},\cdots,a^{s}$ are pairwise distinct, so $D\ne 0$.

Hence $\text{rank}\left(A\right)\ge s$.

Also, $A$ has only $s$ rows, so $\text{rank}\left(A\right)\le s$.

Thus $\text{rank}\left(A\right)=s$.

The augmented matrix $\overline{A}$ is $A$ with one column added, so $\text{rank}\left(\overline{A}\right)\ge\text{rank}\left(A\right)=s$.

Also, $\overline{A}$ has only $s$ rows, so $\text{rank}\left(\overline{A}\right)\le s$.

Thus $\text{rank}\left(\overline{A}\right)=s=\text{rank}\left(A\right)$.

By **Theorem 3.6.1 (Solvability Criterion for a Linear System)**, the system is therefore solvable.

Also, $\text{rank}\left(A\right)=s< n$ (the number of unknowns); by **Theorem 3.6.2 (Criterion for the Number of Solutions)**, the system therefore has infinitely many solutions. $\blacksquare$

---

## 3.6-4

Given the linear system

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

### Solution 3.6-4

By **Theorem 3.6.1 (Solvability Criterion for a Linear System)**, to prove the system is solvable is to prove that the coefficient matrix $A$ and the augmented matrix $\overline{A}$ have the same rank.

Let the augmented matrix be $\overline{A}$, i.e. $\overline{A}=\left[A,b\right]$, where $b=\left(b_{1},b_{2},\cdots,b_{n}\right)^{\top}$.

Note that $\overline{A}$ is the first $n$ rows of $B$, so $\overline{A}$ is a submatrix of $B$.

Hence $\text{rank}\left(\overline{A}\right)\le\text{rank}\left(B\right)$.

Also, $A$ is a submatrix of $\overline{A}$, so $\text{rank}\left(A\right)\le\text{rank}\left(\overline{A}\right)$.

By hypothesis $\text{rank}\left(A\right)=\text{rank}\left(B\right)$, so

$$
\text{rank}\left(A\right)\le\text{rank}\left(\overline{A}\right)\le\text{rank}\left(B\right)=\text{rank}\left(A\right).
$$

Thus $\text{rank}\left(\overline{A}\right)=\text{rank}\left(A\right)$.

By **Theorem 3.6.1 (Solvability Criterion for a Linear System)**, the system is solvable. $\blacksquare$
