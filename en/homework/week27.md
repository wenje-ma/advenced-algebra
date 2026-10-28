# week27

> **Definition 5.3.1 (Generalized Inverse)**<br>Let $A$ be an $s\times n$ matrix over a number field $K$. If a matrix $G$ satisfies $AGA=A$, then $G$ is called a generalized inverse of $A$, denoted $A^{-}$.

> **Theorem 5.3.1 (Existence of a Generalized Inverse)**<br>Let $A$ be a nonzero $s\times n$ matrix over a number field $K$. Then the matrix equation $AXA=A$ always has a solution.

---

## 5.3-1

Let $A$ be an $s\times n$ matrix over a number field $K$. Prove: if $A$ is row full-rank, then for every generalized inverse $A^{-}$ of $A$, $AA^{-}=I_{s}$.

### Solution 5.3-1

By **Definition 5.3.1 (Generalized Inverse)**, $A^{-}$ is a generalized inverse of $A$, i.e. $AA^{-}A=A$. Suppose $A$ is row full-rank, i.e. $\operatorname{rank}\left(A\right)=s$.

Set $B=AA^{-}$. Then $B$ is an $s\times s$ matrix.

From $AA^{-}A=A$, multiply on the right by $A^{-}$:

$$
\left(AA^{-}A\right)A^{-}=AA^{-}.
$$

Namely,

$$
AA^{-}\left(AA^{-}\right)=AA^{-}.
$$

Therefore

$$
BB=B,
$$

i.e. $B$ is idempotent.

**Find the rank of $B$.**

Since $A$ is row full-rank, $\operatorname{rank}\left(A\right)=s$.

Since $AA^{-}A=A$,

$$
\operatorname{rank}\left(A\right)=\operatorname{rank}\left(AA^{-}A\right)\le\operatorname{rank}\left(AA^{-}\right)\le\operatorname{rank}\left(A\right).
$$

Hence

$$
\operatorname{rank}\left(B\right)=\operatorname{rank}\left(AA^{-}\right)=\operatorname{rank}\left(A\right)=s.
$$

Thus $B$ is an $s\times s$ matrix with $\operatorname{rank}\left(B\right)=s$, i.e. $B$ is invertible.

From $BB=B$, multiply on the left by $B^{-1}$:

$$
B=I_{s}.
$$

Therefore, by **Definition 5.3.1 (Generalized Inverse)**, for every generalized inverse $A^{-}$ of $A$,

$$
AA^{-}=I_{s}.
$$

$\blacksquare$
