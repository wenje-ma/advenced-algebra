# Assignment 28

> **Definition 1** (Similarity)<br>Let $A$ and $B$ both be matrices of order $n$ over a number field $K$. If there exists an invertible matrix of order $n$ $P$ over $K$ such that $P^{-1}AP=B$, then $A$ and $B$ are said to be similar, denoted $A\sim B$.

> **Property** (Similarity Invariants)<br>Similar matrices have equal determinants, equal ranks, and equal traces.

> **Theorem 2** (Necessary and Sufficient Condition for Diagonalizability)<br>An matrix of order $n$ $A$ over a number field $K$ is similar to a diagonal matrix if and only if there exist $n$ linearly independent column vectors $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ in $K^{n}$ and $n$ scalars $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ in $K$ such that $A\alpha_{i}=\lambda_{i}\alpha_{i}$ ( $i=1,2,\cdots,n$ ).

### Problem 1

(Problem 5.4-3) Prove: if $A_{1}\sim B_{1}$ and $A_{2}\sim B_{2}$, then

$$
\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right].
$$

### Solution to Problem 1

By **Definition 1** (Similarity), since $A_{1}\sim B_{1}$, there exists an invertible matrix $P_{1}$ such that $P_{1}^{-1}A_{1}P_{1}=B_{1}$.

Let

$$
P=\left[\begin{array}{cc}P_{1} & 0\\0 & P_{2}\end{array}\right]
$$

Since $P_{1},P_{2}$ are invertible, $P$ is invertible, and

$$
P^{-1}=\left[\begin{array}{cc}P_{1}^{-1} & 0\\0 & P_{2}^{-1}\end{array}\right]
$$

Compute:

$$
\begin{aligned}P^{-1}\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]P
&=\left[\begin{array}{cc}P_{1}^{-1} & 0\\0 & P_{2}^{-1}\end{array}\right]\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\left[\begin{array}{cc}P_{1} & 0\\0 & P_{2}\end{array}\right]\\
&=\left[\begin{array}{cc}P_{1}^{-1}A_{1}P_{1} & 0\\0 & P_{2}^{-1}A_{2}P_{2}\end{array}\right]\\
&=\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right].
\end{aligned}
$$

Therefore by **Definition 1** (Similarity),

$$
\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right]
$$

$\blacksquare$

### Problem 2

(Problem 5.4-8) Prove: if $A$ is diagonalizable, then $A\sim A^{T}$.

### Solution to Problem 2

By **Theorem 2** (Necessary and Sufficient Condition for Diagonalizability), since $A$ is diagonalizable, there exists an invertible matrix $P$ such that

$$
P^{-1}AP=D,
$$

where $D$ is a diagonal matrix.

The transpose of a diagonal matrix is still a diagonal matrix, i.e. $D^{T}=D$.

Take the transpose of both sides:

$$
\left(P^{-1}AP\right)^{T}=D^{T}=D.
$$

That is,

$$
P^{T}A^{T}\left(P^{-1}\right)^{T}=D.
$$

Let $Q=\left(P^{T}\right)^{-1}$. Then $Q^{-1}=P^{T}$.

The above becomes

$$
Q^{-1}A^{T}Q=D.
$$

Therefore

$$
A^{T}\sim D.
$$

Since also $A\sim D$, by the symmetry and transitivity of similarity,

$$
A\sim A^{T}.
$$

Thus $A\sim A^{T}$. $\blacksquare$

### Problem 3

(Problem 5.4-9) Prove: if matrices of order $n$ $A,B$ over a number field $K$ satisfy

$$
AB-BA=A,
$$

then $A$ is not invertible.

### Solution to Problem 3

By **Property** (Similarity Invariants), similar matrices have equal traces. Suppose, for contradiction, that $A$ is invertible.

From $AB-BA=A$, left-multiply both sides by $A^{-1}$:

$$
A^{-1}AB-A^{-1}BA=A^{-1}A.
$$

That is,

$$
B-A^{-1}BA=I.
$$

Let $C=A^{-1}BA$. Then $B-C=I$.

Take the trace of both sides:

$$
\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(I\right)=n.
$$

On the other hand,

$$
\operatorname{tr}\left(C\right)=\operatorname{tr}\left(A^{-1}BA\right)=\operatorname{tr}\left(BAA^{-1}\right)=\operatorname{tr}\left(B\right).
$$

Therefore

$$
\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(B\right)-\operatorname{tr}\left(C\right)=0.
$$

This is a contradiction.

Similar matrices have equal traces, so the supposition is false; namely, $A$ is not invertible. $\blacksquare$

### Problem 4

(Problem 5.4-12) A square matrix $A$ is called nilpotent if some positive integer power of $A$ equals the zero matrix; the smallest positive integer $l$ such that $A^{l}=0$ is called the nilpotency index of $A$. Prove: any matrix similar to a nilpotent matrix is also nilpotent, and their nilpotency indices are equal.

### Solution to Problem 4

Let $A$ be a nilpotent matrix with nilpotency index $l$, i.e. $A^{l}=0$ and $A^{k}\ne0$ ( $k< l$ ).

Let $B\sim A$, i.e. there exists an invertible matrix $P$ such that $B=P^{-1}AP$.

**Prove that $B$ is nilpotent**.

$$
B^{l}=\left(P^{-1}AP\right)^{l}=P^{-1}A^{l}P=P^{-1}0P=0.
$$

Therefore $B$ is nilpotent.

**Prove that the nilpotency index of $B$ equals $l$**.

Let the nilpotency index of $B$ be $m$, i.e. $B^{m}=0$.

Then

$$
B^{m}=\left(P^{-1}AP\right)^{m}=P^{-1}A^{m}P=0.
$$

Left-multiply by $P$ and right-multiply by $P^{-1}$:

$$
A^{m}=0.
$$

Since the nilpotency index of $A$ is $l$, we have $m\ge l$.

On the other hand, $A^{l}=0$, so

$$
B^{l}=P^{-1}A^{l}P=0.
$$

Since the nilpotency index of $B$ is $m$, we have $l\ge m$.

Therefore $m=l$.

Hence any matrix similar to a nilpotent matrix is also nilpotent, and their nilpotency indices are equal. $\blacksquare$
