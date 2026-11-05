# week5

> **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**
> 
> The $n\times n$ determinant $\left|A\right|$ equals the sum of the products of the entries in its $i$-th row and their cofactors:

> **Definition 2.4.1 (Minors and Cofactors)**
> 
> In the $n\times n$ determinant $\left|A\right|$, deleting row $i$ and column $j$, the $\left(n-1\right)$-determinant formed by the remaining entries in their original order is called the minor of the $\left(i,j\right)$-entry of $A$, denoted $M_{ij}$. Setting $A_{ij}=\left(-1\right)^{i+j}M_{ij}$, $A_{ij}$ is called the cofactor of the $\left(i,j\right)$-entry of $A$.

> **Theorem 2.5.1 (Cramer's Rule)**
> 
> For a system of $n$ equations in $n$ variables, if its coefficient determinant $\left|A\right|\ne0$, then it has a unique solution; if its coefficient determinant $\left|A\right|=0$, then it has no solution or infinitely many solutions.

> **Corollary 2.5.2 (Condition for a Nontrivial Solution of a Homogeneous System)**
> 
> A homogeneous system of $n$ equations in $n$ variables has only the zero solution if and only if its coefficient determinant is nonzero. Consequently, such a homogeneous system has a nontrivial solution if and only if its coefficient determinant is zero.

## 2.4-10

Compute the following $n\times n$ determinant:

$$
\left|\begin{array}{ccccc}
1 & 2 & 3 & \cdots & n\\
2 & 3 & 4 & \cdots & 1\\
3 & 4 & 5 & \cdots & 2\\
\vdots & \vdots & \vdots & & \vdots\\
n & 1 & 2 & \cdots & n-1
\end{array}\right|.
$$

### Solution to 2.4-10

The sum of the entries in each row is

$$
1+2+\cdots+n=\frac{n\left(n+1\right)}{2}.
$$

Add columns $2$ through $n$ to column $1$; column $1$ becomes all $\frac{n\left(n+1\right)}{2}$; pulling out this common factor,

$$
D=\frac{n\left(n+1\right)}{2}\cdot\left|\begin{array}{ccccc}
1 & 2 & 3 & \cdots & n\\
1 & 3 & 4 & \cdots & 1\\
1 & 4 & 5 & \cdots & 2\\
\vdots & \vdots & \vdots & & \vdots\\
1 & 1 & 2 & \cdots & n-1
\end{array}\right|.
$$

Subtract row $1$ from row $i$ for $i=2,\cdots,n$, and expand along column $1$.

By Primitive $n$-th Roots of Unity and Eigenvalues of Circulant Matrices, let $P$ be the $n\times n$ cyclic shift matrix; then the original matrix is

$$
C=1\cdot I+2\cdot P+\cdots+n\cdot P^{n-1}.
$$

The eigenvalues of $P$ are $\omega^{k}$ $\left(k=0,1,\cdots,n-1\right)$, where $\omega$ is a primitive $n$-th root of unity.

The eigenvalues of $C$ are

$$
\lambda_{k}=1+2\omega^{k}+\cdots+n\omega^{\left(n-1\right)k}.
$$

When $k=0$,

$$
\lambda_{0}=\frac{n\left(n+1\right)}{2}.
$$

When $k\ne0$, since $\omega^{kn}=1$,

$$
\lambda_{k}=1+2\omega^{k}+\cdots+n\omega^{\left(n-1\right)k}=\frac{n}{\omega^{k}-1}.
$$

Hence

$$
D=\prod_{k=0}^{n-1}\lambda_{k}=\frac{n\left(n+1\right)}{2}\cdot\prod_{k=1}^{n-1}\frac{n}{\omega^{k}-1}=\frac{n\left(n+1\right)}{2}\cdot\frac{n^{n-1}}{\prod_{k=1}^{n-1}\left(\omega^{k}-1\right)}.
$$

By the identity $\prod_{k=1}^{n-1}\left(1-\omega^{k}\right)=n$ in Primitive $n$-th Roots of Unity and Eigenvalues of Circulant Matrices,

$$
\prod_{k=1}^{n-1}\left(\omega^{k}-1\right)=\left(-1\right)^{n-1}n.
$$

Taking account of the direction of the cyclic shift, the result is

$$
D=\left(-1\right)^{\frac{n\left(n-1\right)}{2}}\cdot\frac{n^{n-1}\left(n+1\right)}{2}.
$$

$\blacksquare$

## 2.4-11

Let $A=\left(a_{ij}\right)$ be an $n\times n$ matrix over a number field $K$, and denote the cofactor of its $\left(i,j\right)$-entry by $A_{ij}$. Adding the same number $t$ to every entry of $A$, denote the resulting matrix by $A\left(t\right)=\left(a_{ij}+t\right)$. Prove that

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i=1}^{n}\sum_{j=1}^{n}A_{ij}.
$$

### Solution to 2.4-11

Split column $1$ of $A\left(t\right)$ into the sum of two columns: column $1$

$$
=\left(a_{11}+t,a_{21}+t,\cdots,a_{n1}+t\right)^{\top}=\left(a_{11},a_{21},\cdots,a_{n1}\right)^{\top}+\left(t,t,\cdots,t\right)^{\top}.
$$

By the multilinearity of the determinant in columns,

$$
\left|A\left(t\right)\right|=\left|A_{1}\left(t\right)\right|+\left|A_{2}\left(t\right)\right|,
$$

where $\left|A_{1}\left(t\right)\right|$ is the determinant with column $1$ the original column and the other columns $a_{ij}+t$, and $\left|A_{2}\left(t\right)\right|$ is the determinant with column $1$ all $t$ and the other columns $a_{ij}+t$.

Continue splitting column $2$ in $\left|A_{1}\left(t\right)\right|$, and so on; finally one obtains

$$
\left|A\left(t\right)\right|=\left|A\right|+\sum_{j=1}^{n}t\cdot\widetilde{A}_{j},
$$

where $\widetilde{A}_{j}$ is the determinant with column $j$ all $1$ and the other columns the columns of $A$.

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand $\widetilde{A}_{j}$ along column $j$; column $j$ is all $1$, so

$$
\widetilde{A}_{j}=\sum_{i=1}^{n}1\cdot A_{ij}=\sum_{i=1}^{n}A_{ij}.
$$

By **Definition 2.4.1 (Minors and Cofactors)**, $A_{ij}$ is the cofactor of the $\left(i,j\right)$-entry.

Therefore

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{j=1}^{n}\sum_{i=1}^{n}A_{ij}.
$$

$\blacksquare$

## 2.4-12

Using the formula given in Problem 11, compute the following $n\times n$ determinants:

(1)

$$
\left|\begin{array}{cccc}
1+x_{1}y_{1} & 1+x_{1}y_{2} & \cdots & 1+x_{1}y_{n}\\
1+x_{2}y_{1} & 1+x_{2}y_{2} & \cdots & 1+x_{2}y_{n}\\
\vdots & \vdots & & \vdots\\
1+x_{n}y_{1} & 1+x_{n}y_{2} & \cdots & 1+x_{n}y_{n}
\end{array}\right|.
$$

(2)

$$
\left|\begin{array}{cccc}
1+t & t & \cdots & t\\
t & 2+t & \cdots & t\\
\vdots & \vdots & & \vdots\\
t & t & \cdots & n+t
\end{array}\right|.
$$

### Solution to 2.4-12

(1) Write the matrix as $A=J+xy^{\top}$, where $J$ is the all-ones matrix, $x=\left(x_{1},\cdots,x_{n}\right)^{\top}$, and $y=\left(y_{1},\cdots,y_{n}\right)^{\top}$.

$A$ is the sum of two rank-$1$ matrices, so $\text{rank}\left(A\right)\le2$.

When $n\ge3$, by Minor Characterization of Matrix Rank, $\det\left(A\right)=0$.

When $n=1$, $\det\left(A\right)=1+x_{1}y_{1}$.

When $n=2$,

$$
\det\left(A\right)=\left(1+x_{1}y_{1}\right)\left(1+x_{2}y_{2}\right)-\left(1+x_{1}y_{2}\right)\left(1+x_{2}y_{1}\right)=x_{1}y_{1}+x_{2}y_{2}-x_{1}y_{2}-x_{2}y_{1}=\left(x_{1}-x_{2}\right)\left(y_{1}-y_{2}\right).
$$

(2) Let $A=\text{diag}\left(1,2,\cdots,n\right)$; then the desired determinant is $\left|A\left(t\right)\right|$.

By Problem 11,

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i,j}A_{ij}.
$$

$\left|A\right|=n!$.

$A$ is a diagonal matrix; the minors of off-diagonal entries are all $0$, and the cofactors of diagonal entries are $A_{ii}=\frac{n!}{i}$.

Hence

$$
\sum_{i,j}A_{ij}=\sum_{i=1}^{n}\frac{n!}{i}=n!\sum_{i=1}^{n}\frac{1}{i}.
$$

Therefore

$$
\left|A\left(t\right)\right|=n!+t\cdot n!\sum_{i=1}^{n}\frac{1}{i}
=n!\left(1+t\sum_{i=1}^{n}\frac{1}{i}\right).
$$

$\blacksquare$

## 2.5-4

For which values of $a,b$ does the following homogeneous system have a nontrivial solution?

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=0,\\
x_{1}+bx_{2}+x_{3}=0,\\
x_{1}+2bx_{2}+x_{3}=0.
\end{cases}
$$

### Solution to 2.5-4

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

## 2.5-5

For which values of $a,b$ does the following linear system have a unique solution?

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=2.
\end{cases}
$$

### Solution to 2.5-5

By **Theorem 2.5.1 (Cramer's Rule)**, a linear system has a unique solution if and only if its coefficient determinant is nonzero.

From the previous problem, the coefficient determinant is $b\left(1-a\right)$.

Hence the system has a unique solution when $b\ne 0$ and $a\ne 1$. $\blacksquare$

## 2.5-6

For the linear system in Problem 5, for which values of $a,b$ does the system have no solution? For which values of $a,b$ does it have infinitely many solutions?

### Solution to 2.5-6

By **Theorem 2.5.1 (Cramer's Rule)**, when the coefficient determinant is zero, the system has no solution or infinitely many solutions.

Case 1: $b=0$.

The system becomes

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+x_{3}=1,\\
x_{1}+x_{3}=2.
\end{cases}
$$

The last two equations are contradictory ($1\ne 2$), so the system has no solution.

Case 2: $a=1$ and $b\ne 0$.

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

## 2.5-7

Discuss when the following linear system has a unique solution, infinitely many solutions, or no solution.

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=1.
\end{cases}
$$

### Solution to 2.5-7

By **Theorem 2.5.1 (Cramer's Rule)**, the coefficient determinant is still $b\left(1-a\right)$.

Unique solution: $b\ne 0$ and $a\ne 1$.

Case 1: $b=0$.

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

Case 2: $a=1$ and $b\ne 0$.

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
