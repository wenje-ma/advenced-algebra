# Assignment 22

> **Theorem 1** (Rank of matrix product)<br>Let $A=\left(a_{ij}\right)_{s\times n}$ and $B=\left(b_{ij}\right)_{n\times m}$. Then
> $$
> \text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
> $$

> **Proposition 2** (Rank identity over the real field)<br>Let $A$ be an $s\times n$ matrix over the real field. Then:
> 
> $$
> \text{rank}\left(A^{\top}A\right)=\text{rank}\left(AA^{\top}\right)=\text{rank}\left(A\right)
> $$

### Problem 1

(Problem 4.5-1) Prove: let $A,B$ be $s\times n$ and $n\times m$ matrices respectively. If $AB=0$, then $\text{rank}\left(A\right)+\text{rank}\left(B\right)\le n$.

### Solution to Problem 1

By **Theorem 1** (Rank of matrix product),

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

Let the column vectors of $B$ be $\beta_{1},\beta_{2},\cdots,\beta_{m}$.

$AB=0$ means $A\beta_{j}=0$ ( $j=1,2,\cdots,m$ ).

Thus each $\beta_{j}$ is a solution of the homogeneous system $Ax=0$.

Therefore the column space of $B$ $\subseteq Ax=0$ solution space $W$.

Hence

$$
\text{rank}\left(B\right)=\dim\left\langle\beta_{1},\cdots,\beta_{m}\right\rangle\le\dim W=n-\text{rank}\left(A\right).
$$

Therefore

By **Theorem 1** (Rank of matrix product),

$$
\text{rank}\left(A\right)+\text{rank}\left(B\right)\le n.
$$

$\blacksquare$

### Problem 2

(Problem 4.5-4) Prove: if an $n$-th order matrix $A$ satisfies $A^{2}=I$ (then $A$ is called an involutory matrix), then

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

### Solution to Problem 2

By **Theorem 1** (Rank of matrix product), since $A^{2}=I$,

$$
\left(I+A\right)\left(I-A\right)=I-A^{2}=I-I=0.
$$

By the result of Problem 4.5-1,

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)\le n.
$$

On the other hand,

$$
\left(I+A\right)+\left(I-A\right)=2I.
$$

By the rank inequality,

$$
\text{rank}\left(2I\right)\le\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right).
$$

$\text{rank}\left(2I\right)=n$, hence

$$
n\le\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right).
$$

Therefore

By **Theorem 1** (Rank of matrix product),

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

$\blacksquare$

### Problem 3

(Problem 4.5-5) Prove: if an $n$-th order matrix $A$ satisfies $A^{2}=A$ (then $A$ is called an idempotent matrix), then

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

### Solution to Problem 3

By **Theorem 1** (Rank of matrix product), since $A^{2}=A$,

$$
A\left(I-A\right)=A-A^{2}=A-A=0.
$$

By the result of Problem 4.5-1,

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)\le n.
$$

On the other hand,

$$
A+\left(I-A\right)=I.
$$

By the rank inequality,

$$
\text{rank}\left(I\right)\le\text{rank}\left(A\right)+\text{rank}\left(I-A\right).
$$

$\text{rank}\left(I\right)=n$, hence

$$
n\le\text{rank}\left(A\right)+\text{rank}\left(I-A\right).
$$

Therefore

By **Theorem 1** (Rank of matrix product),

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

$\blacksquare$

### Problem 4

(Problem 4.5-6) Let $A$ be an $s\times n$ matrix over the real field, and $\beta$ any column vector in $\mathbb{R}^{s}$. Prove: the $n$-unknown linear system $A^{\top}AX=A^{\top}\beta$ is always solvable.

### Solution to Problem 4

By **Proposition 2** (Rank identity over the real field), for matrices over the real field,

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

Therefore

$$
\text{rank}\left(A^{\top}A\right)\le\text{rank}\left(A^{\top}A,A^{\top}\beta\right)\le\text{rank}\left(A\right)=\text{rank}\left(A^{\top}A\right).
$$

Hence

$$
\text{rank}\left(A^{\top}A\right)=\text{rank}\left(A^{\top}A,A^{\top}\beta\right).
$$

The coefficient matrix and the augmented matrix have the same rank, so the system is solvable. $\blacksquare$

### Problem 5

(Problem 4.5-9) Let $A$ be an $n$-th order matrix ( $n\ge2$ ). Prove:

$$
\text{rank}\left(A^{*}\right)=
\begin{cases}
n, & \text{当 }\text{rank}\left(A\right)=n;\\
1, & \text{当 }\text{rank}\left(A\right)=n-1;\\
0, & \text{当 }\text{rank}\left(A\right)< n-1.
\end{cases}
$$

### Solution to Problem 5

By **Theorem 1** (Rank of matrix product),

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

Consider three cases.

**When $\text{rank}\left(A\right)=n$**: $\left|A\right|\ne0$.

From $AA^{*}=\left|A\right|I$, we get $\left|A\right|\left|A^{*}\right|=\left|A\right|^{n}$.

Hence $\left|A^{*}\right|=\left|A\right|^{n-1}\ne0$, so $\text{rank}\left(A^{*}\right)=n$.

**When $\text{rank}\left(A\right)=n-1$**: $\left|A\right|=0$.

Hence $AA^{*}=\left|A\right|I=0$.

By Problem 4.5-1, $\text{rank}\left(A\right)+\text{rank}\left(A^{*}\right)\le n$.

i.e., $\left(n-1\right)+\text{rank}\left(A^{*}\right)\le n$, so $\text{rank}\left(A^{*}\right)\le1$.

Also, since $\text{rank}\left(A\right)=n-1$, $A$ has a nonzero minor of order $n-1$. This $n-1$-th order minor is some cofactor, so $A^{*}\ne0$, hence $\text{rank}\left(A^{*}\right)\ge1$.

Therefore $\text{rank}\left(A^{*}\right)=1$.

**When $\text{rank}\left(A\right)< n-1$**: all minors of order $n-1$ of $A$ are zero.

Hence all cofactors are zero, i.e., $A^{*}=0$.

Therefore $\text{rank}\left(A^{*}\right)=0$.

$\blacksquare$

### Problem 6

(Problem 4.5-15) Let $A,B,C,D$ all be $n$-th order matrices, with $\left|A\right|\ne0$ and $AC=CA$. Prove:

$$
\left|\begin{array}{cc}A & B\\C & D\end{array}\right|=\left|AD-CB\right|.
$$

### Solution to Problem 6

Following the approach of **Theorem 1**, since $\left|A\right|\ne0$, $A$ is invertible.

Perform elementary row operations on the block matrix: left-multiply block row $1$ by $-CA^{-1}$ and add to block row $2$.

$$
\left|\begin{array}{cc}A & B\\C & D\end{array}\right|
=
\left|\begin{array}{cc}A & B\\0 & D-CA^{-1}B\end{array}\right|.
$$

This is a block upper triangular matrix; its determinant equals the product of the determinants of the diagonal submatrices:

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
