# Assignment 27

> **Definition 1** (Generalized inverse)<br>Let $A$ be an $s\times n$ matrix over a field $K$. If a matrix $G$ satisfies $AGA=A$, then $G$ is called a generalized inverse of $A$, denoted $A^{-}$.

> **Theorem 1** (Existence of generalized inverse)<br>Let $A$ be a nonzero $s\times n$ matrix over $K$. Then the matrix equation $AXA=A$ always has a solution.

### Problem 1

(Problem 5.3-1) Let $A$ be an $s\times n$ matrix over $K$. Prove: if $A$ has full row rank, then for any generalized inverse $A^{-}$ of $A$, we have $AA^{-}=I_{s}$.

### Solution to Problem 1

By **Definition 1** (Generalized inverse), $A^{-}$ is a generalized inverse of $A$, i.e., $AA^{-}A=A$. Suppose $A$ has full row rank, i.e., $\operatorname{rank}\left(A\right)=s$.

Let $B=AA^{-}$. Then $B$ is an $s\times s$ matrix.

From $AA^{-}A=A$, right-multiply both sides by $A^{-}$:

$$
\left(AA^{-}A\right)A^{-}=AA^{-}.
$$

i.e.,

$$
AA^{-}\left(AA^{-}\right)=AA^{-}.
$$

Therefore

$$
BB=B,
$$

i.e., $B$ is an idempotent matrix.

**Find the rank of $B$**.

Since $A$ has full row rank, $\operatorname{rank}\left(A\right)=s$.

Also, since $AA^{-}A=A$,

$$
\operatorname{rank}\left(A\right)=\operatorname{rank}\left(AA^{-}A\right)\le\operatorname{rank}\left(AA^{-}\right)\le\operatorname{rank}\left(A\right).
$$

Therefore

$$
\operatorname{rank}\left(B\right)=\operatorname{rank}\left(AA^{-}\right)=\operatorname{rank}\left(A\right)=s.
$$

Hence $B$ is an $s\times s$ matrix with $\operatorname{rank}\left(B\right)=s$, i.e., $B$ is invertible.

From $BB=B$, left-multiply both sides by $B^{-1}$:

$$
B=I_{s}.
$$

Therefore

By **Definition 1** (Generalized inverse), for any generalized inverse $A^{-}$ of $A$, we have

$$
AA^{-}=I_{s}.
$$

$\blacksquare$
