# week14

$$
\text{rank}\left(A+B\right)\le\text{rank}\left(A\right)+\text{rank}\left(B\right).
$$
$$
\left|\begin{array}{cc}A & B\\0 & D\end{array}\right|=\left|A\right|\cdot\left|D\right|.
$$

> **Theorem 3.7.1 (Dimension of the Solution Space of a Homogeneous System)**
> 
> For an $n$-variable homogeneous system $Ax=0$ over a number field $K$, the solution space $W$ has dimension

$$
\dim W=n-\text{rank}\left(A\right).
$$

> **Theorem 4.3.1 (Rank of a Matrix Product)**
> 
> Let $A=\left(a_{ij}\right)_{s\times n}$ and $B=\left(b_{ij}\right)_{n\times m}$. Then

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

> **Proposition 4.5.2 (Rank Identity over the Real Number Field)**
> 
> Let $A$ be an $s\times n$ matrix over the real number field. Then

$$
\text{rank}\left(A^{\top}A\right)=\text{rank}\left(AA^{\top}\right)=\text{rank}\left(A\right).
$$

$$
\beta_{i}=\alpha_{i}-\sum_{k=1}^{i-1}\frac{\left(\alpha_{i},\beta_{k}\right)}{\left(\beta_{k},\beta_{k}\right)}\beta_{k}.
$$
Then $\beta_{1},\beta_{2},\cdots,\beta_{m}$ is an orthogonal vector group equivalent to the original one.

> **Definition 4.6.1 (Orthogonal Matrix)**
> 
> A real square matrix $A$ satisfying $A^{\top}A=I$ is called an orthogonal matrix.

> **Definition 4.6.2 (Standard Inner Product)**
> 
> In $\mathbb{R}^{n}$, for any $\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)$ and $\beta=\left(b_{1},b_{2},\cdots,b_{n}\right)$, define

$$
\left(\alpha,\beta\right)=a_{1}b_{1}+a_{2}b_{2}+\cdots+a_{n}b_{n},
$$
which is called the standard inner product on $\mathbb{R}^{n}$.

> **Proposition 4.6.2 (An Orthogonal Vector Group Is Linearly Independent)**
> 
> In the Euclidean space $\mathbb{R}^{n}$, an orthogonal vector group is always linearly independent.

## 4.5-1

Prove: let $A,B$ be $s\times n$ and $n\times m$ matrices, respectively. If $AB=0$, then $\text{rank}\left(A\right)+\text{rank}\left(B\right)\le n$.

### Solution to 4.5-1

Let the column group of $B$ be $\beta_{1},\beta_{2},\cdots,\beta_{m}$.

$AB=0$ means $A\beta_{j}=0$ ( $j=1,2,\cdots,m$ ).

Hence each $\beta_{j}$ is a solution of the homogeneous system $Ax=0$.

Therefore the column space of $B$ is contained in the solution space $W$ of $Ax=0$.

By **Theorem 3.7.1 (Dimension of the Solution Space of a Homogeneous System)**,

$$
\text{rank}\left(B\right)=\dim\left\langle\beta_{1},\cdots,\beta_{m}\right\rangle\le\dim W=n-\text{rank}\left(A\right).
$$

Hence

$$
\text{rank}\left(A\right)+\text{rank}\left(B\right)\le n.
$$

$\blacksquare$

## 4.5-4

Prove: if an $n\times n$ matrix $A$ satisfies $A^{2}=I$ (then $A$ is called an involutory matrix), then

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

### Solution to 4.5-4

Since $A^{2}=I$,

$$
\left(I+A\right)\left(I-A\right)=I-A^{2}=I-I=0.
$$

By the conclusion of **4.5-1**,

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)\le n.
$$

On the other hand,

$$
\left(I+A\right)+\left(I-A\right)=2I.
$$

By Subadditivity of Rank,

$$
\text{rank}\left(2I\right)\le\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right).
$$

Since $\text{rank}\left(2I\right)=n$,

$$
n\le\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right).
$$

Therefore

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

$\blacksquare$

## 4.5-5

Prove: if an $n\times n$ matrix $A$ satisfies $A^{2}=A$ (then $A$ is called an idempotent matrix), then

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

### Solution to 4.5-5

Since $A^{2}=A$,

$$
A\left(I-A\right)=A-A^{2}=A-A=0.
$$

By the conclusion of **4.5-1**,

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)\le n.
$$

On the other hand,

$$
A+\left(I-A\right)=I.
$$

By Subadditivity of Rank,

$$
\text{rank}\left(I\right)\le\text{rank}\left(A\right)+\text{rank}\left(I-A\right).
$$

Since $\text{rank}\left(I\right)=n$,

$$
n\le\text{rank}\left(A\right)+\text{rank}\left(I-A\right).
$$

Therefore

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

$\blacksquare$

## 4.5-6

Let $A$ be an $s\times n$ matrix over the real number field, and $\beta$ any column vector in $\mathbb{R}^{s}$. Prove: the $n$-variable system $A^{\top}AX=A^{\top}\beta$ always has a solution.

### Solution to 4.5-6

By **Proposition 4.5.2 (Rank Identity over the Real Number Field)**, for a matrix over the real number field,

$$
\text{rank}\left(A^{\top}A\right)=\text{rank}\left(A\right).
$$

The augmented matrix is $\left(A^{\top}A,A^{\top}\beta\right)=A^{\top}\left(A,\beta\right)$.

Therefore

$$
\text{rank}\left(A^{\top}A,A^{\top}\beta\right)=\text{rank}\left(A^{\top}\left(A,\beta\right)\right)\le\text{rank}\left(A^{\top}\right)=\text{rank}\left(A\right).
$$

On the other hand, $A^{\top}A$ is a submatrix of $\left(A^{\top}A,A^{\top}\beta\right)$, so

$$
\text{rank}\left(A^{\top}A\right)\le\text{rank}\left(A^{\top}A,A^{\top}\beta\right).
$$

Hence

$$
\text{rank}\left(A^{\top}A\right)\le\text{rank}\left(A^{\top}A,A^{\top}\beta\right)\le\text{rank}\left(A\right)=\text{rank}\left(A^{\top}A\right).
$$

Therefore

$$
\text{rank}\left(A^{\top}A\right)=\text{rank}\left(A^{\top}A,A^{\top}\beta\right).
$$

The coefficient matrix and the augmented matrix have the same rank, so the system has a solution. $\blacksquare$

## 4.5-9

Let $A$ be an $n\times n$ matrix ( $n\ge2$ ). Prove:

$$
\text{rank}\left(A^{*}\right)=
\begin{cases}
n, & \text{when }\text{rank}\left(A\right)=n;\\
1, & \text{when }\text{rank}\left(A\right)=n-1;\\
0, & \text{when }\text{rank}\left(A\right)< n-1.
\end{cases}
$$

### Solution to 4.5-9

By **Theorem 4.3.1 (Rank of a Matrix Product)**,

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

Consider three cases.

**When $\text{rank}\left(A\right)=n$**: $\left|A\right|\ne0$.

From $AA^{*}=\left|A\right|I$, $\left|A\right|\left|A^{*}\right|=\left|A\right|^{n}$.

Hence $\left|A^{*}\right|=\left|A\right|^{n-1}\ne0$, so $\text{rank}\left(A^{*}\right)=n$.

**When $\text{rank}\left(A\right)=n-1$**: $\left|A\right|=0$.

Thus $AA^{*}=\left|A\right|I=0$.

By **4.5-1**, $\text{rank}\left(A\right)+\text{rank}\left(A^{*}\right)\le n$.

Namely $\left(n-1\right)+\text{rank}\left(A^{*}\right)\le n$, so $\text{rank}\left(A^{*}\right)\le1$.

Since $\text{rank}\left(A\right)=n-1$, $A$ has a nonzero $\left(n-1\right)$-minor. This $\left(n-1\right)$-minor is some cofactor, so $A^{*}\ne0$, and hence $\text{rank}\left(A^{*}\right)\ge1$.

Therefore $\text{rank}\left(A^{*}\right)=1$.

**When $\text{rank}\left(A\right)< n-1$**: all $\left(n-1\right)$-minors of $A$ are zero.

Hence all cofactors are zero, i.e. $A^{*}=0$.

Therefore $\text{rank}\left(A^{*}\right)=0$.

$\blacksquare$

## 4.5-15

Let $A,B,C,D$ all be $n\times n$ matrices, with $\left|A\right|\ne0$ and $AC=CA$. Prove:

$$
\left|\begin{array}{cc}A & B\\C & D\end{array}\right|=\left|AD-CB\right|.
$$

### Solution to 4.5-15

Since $\left|A\right|\ne0$, $A$ is invertible.

Perform an elementary block row operation: add $-CA^{-1}$ times the first block row to the second block row.

$$
\left|\begin{array}{cc}A & B\\C & D\end{array}\right|
=
\left|\begin{array}{cc}A & B\\0 & D-CA^{-1}B\end{array}\right|.
$$

This is a block upper triangular matrix. By Determinant of a Block Upper Triangular Matrix, its determinant equals the product of the determinants of the diagonal block submatrices:

$$
=\left|A\right|\cdot\left|D-CA^{-1}B\right|.
$$

Since $AC=CA$, $CA^{-1}=A^{-1}C$.

Hence

$$
D-CA^{-1}B=D-A^{-1}CB.
$$

Therefore

$$
\left|D-CA^{-1}B\right|
=\left|D-A^{-1}CB\right|
=\left|A^{-1}\left(AD-CB\right)\right|
=\left|A^{-1}\right|\cdot\left|AD-CB\right|
=\frac{1}{\left|A\right|}\cdot\left|AD-CB\right|.
$$

Hence

$$
\left|A\right|\cdot\left|D-CA^{-1}B\right|
=\left|A\right|\cdot\frac{1}{\left|A\right|}\cdot\left|AD-CB\right|
=\left|AD-CB\right|.
$$

$\blacksquare$

## 4.6-1(3)

Determine whether the following matrix is orthogonal:

$$
A=\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right].
$$

### Solution to 4.6-1(3)

By **Definition 4.6.1 (Orthogonal Matrix)**, compute $A^{\top}A$:

$$
A^{\top}A=\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right]\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right].
$$

The $\left(1,1\right)$-entry:

$$
\left(\frac{\sqrt{3}}{2}\right)^{2}+\left(\frac{1}{2}\right)^{2}=\frac{3}{4}+\frac{1}{4}=1.
$$

The $\left(1,2\right)$-entry:

$$
\frac{\sqrt{3}}{2}\cdot\frac{1}{2}+\frac{1}{2}\cdot\left(-\frac{\sqrt{3}}{2}\right)=\frac{\sqrt{3}}{4}-\frac{\sqrt{3}}{4}=0.
$$

The $\left(2,1\right)$-entry:

$$
\frac{1}{2}\cdot\frac{\sqrt{3}}{2}+\left(-\frac{\sqrt{3}}{2}\right)\cdot\frac{1}{2}=\frac{\sqrt{3}}{4}-\frac{\sqrt{3}}{4}=0.
$$

The $\left(2,2\right)$-entry:

$$
\left(\frac{1}{2}\right)^{2}+\left(-\frac{\sqrt{3}}{2}\right)^{2}=\frac{1}{4}+\frac{3}{4}=1.
$$

Hence $A^{\top}A=I$, and by **Definition 4.6.1 (Orthogonal Matrix)**, $A$ is orthogonal. $\blacksquare$

## 4.6-1(8)

Determine whether the following matrix is orthogonal:

$$
A=\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right].
$$

### Solution to 4.6-1(8)

By **Definition 4.6.1 (Orthogonal Matrix)**, compute $A^{\top}A$:

$$
A^{\top}A=\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right]\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right]
=\left[\begin{array}{rr}
2 & 0\\
0 & 2
\end{array}\right].
$$

Clearly $A^{\top}A\ne I$, and by **Definition 4.6.1 (Orthogonal Matrix)**, $A$ is not orthogonal. $\blacksquare$

## 4.6-3

Prove: if $A$ is an $n\times n$ real symmetric matrix and $T$ is an $n\times n$ orthogonal matrix, then $T^{-1}AT$ is symmetric.

### Solution to 4.6-3

By **Definition 4.6.1 (Orthogonal Matrix)**, since $T$ is orthogonal, $T^{-1}=T^{\top}$.

$$
\left(T^{-1}AT\right)^{\top}=T^{\top}A^{\top}\left(T^{-1}\right)^{\top}.
$$

Since $T$ is orthogonal, $T^{-1}=T^{\top}$, and hence $\left(T^{-1}\right)^{\top}=\left(T^{\top}\right)^{\top}=T$.

Therefore

$$
\left(T^{-1}AT\right)^{\top}=T^{\top}A^{\top}T.
$$

Since $A$ is symmetric, $A^{\top}=A$.

Thus

$$
\left(T^{-1}AT\right)^{\top}=T^{\top}AT=T^{-1}AT.
$$

Therefore $T^{-1}AT$ is symmetric. $\blacksquare$
