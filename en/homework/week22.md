# week22

> **Basic Knowledge: Subadditivity of Rank**<br>For any two matrices $A,B$ with the same number of rows and columns,

$$
\text{rank}\left(A+B\right)\le\text{rank}\left(A\right)+\text{rank}\left(B\right).
$$

> **Basic Knowledge: Determinant of a Block Upper Triangular Matrix**<br>For a block upper triangular matrix $\left[\begin{array}{cc}A & B\\0 & D\end{array}\right]$, where $A,D$ are square,

$$
\left|\begin{array}{cc}A & B\\0 & D\end{array}\right|=\left|A\right|\cdot\left|D\right|.
$$

> **Theorem 3.7.1 (Dimension of the Solution Space of a Homogeneous System)**<br>For an $n$-variable homogeneous system $Ax=0$ over a number field $K$, the solution space $W$ has dimension

$$
\dim W=n-\text{rank}\left(A\right).
$$

> **Theorem 4.3.1 (Rank of a Matrix Product)**<br>Let $A=\left(a_{ij}\right)_{s\times n}$ and $B=\left(b_{ij}\right)_{n\times m}$. Then

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

> **Proposition 4.5.2 (Rank Identity over the Real Number Field)**<br>Let $A$ be an $s\times n$ matrix over the real number field. Then

$$
\text{rank}\left(A^{\top}A\right)=\text{rank}\left(AA^{\top}\right)=\text{rank}\left(A\right).
$$

---

## 4.5-1

Prove: let $A,B$ be $s\times n$ and $n\times m$ matrices, respectively. If $AB=0$, then $\text{rank}\left(A\right)+\text{rank}\left(B\right)\le n$.

### Solution 4.5-1

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

---

## 4.5-4

Prove: if an $n\times n$ matrix $A$ satisfies $A^{2}=I$ (then $A$ is called an involutory matrix), then

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

### Solution 4.5-4

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

By **Basic Knowledge: Subadditivity of Rank**,

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

---

## 4.5-5

Prove: if an $n\times n$ matrix $A$ satisfies $A^{2}=A$ (then $A$ is called an idempotent matrix), then

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

### Solution 4.5-5

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

By **Basic Knowledge: Subadditivity of Rank**,

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

---

## 4.5-6

Let $A$ be an $s\times n$ matrix over the real number field, and $\beta$ any column vector in $\mathbb{R}^{s}$. Prove: the $n$-variable system $A^{\top}AX=A^{\top}\beta$ always has a solution.

### Solution 4.5-6

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

---

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

### Solution 4.5-9

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

---

## 4.5-15

Let $A,B,C,D$ all be $n\times n$ matrices, with $\left|A\right|\ne0$ and $AC=CA$. Prove:

$$
\left|\begin{array}{cc}A & B\\C & D\end{array}\right|=\left|AD-CB\right|.
$$

### Solution 4.5-15

Since $\left|A\right|\ne0$, $A$ is invertible.

Perform an elementary block row operation: add $-CA^{-1}$ times the first block row to the second block row.

$$
\left|\begin{array}{cc}A & B\\C & D\end{array}\right|
=
\left|\begin{array}{cc}A & B\\0 & D-CA^{-1}B\end{array}\right|.
$$

This is a block upper triangular matrix. By **Basic Knowledge: Determinant of a Block Upper Triangular Matrix**, its determinant equals the product of the determinants of the diagonal block submatrices:

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
