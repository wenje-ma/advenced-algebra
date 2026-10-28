# week39

> **Property 7.7.1 (Conjugate Pairs of Nonreal Roots)**<br>The nonreal roots of a real-coefficient polynomial occur in conjugate pairs with the same multiplicity.

> **Theorem 7.7.1 (Unique Factorization Theorem for Real Polynomials)**<br>Every real-coefficient polynomial of positive degree can be uniquely factored over $\mathbb{R}$ into a product of linear factors and quadratic factors with negative discriminant.

---

## 7.7-4

Prove: if two $n\times n$ real matrices $A$ and $B$ are not similar over $\mathbb{R}$, then they are still not similar when viewed as complex matrices.

### Solution 7.7-4

By **Property 7.7.1 (Conjugate Pairs of Nonreal Roots)**, nonreal roots of a real polynomial come in conjugate pairs. Use proof by contradiction.

Assume $A$ and $B$ are similar over $\mathbb{C}$, i.e. there exists an invertible complex matrix $P$ such that

$$
B=P^{-1}AP.
$$

We show that $A$ and $B$ are also similar over $\mathbb{R}$.

Write $P=P_{1}+iP_{2}$, where $P_{1},P_{2}$ are real matrices.

From $B=P^{-1}AP$,

$$
BP=PA.
$$

Substitute $P=P_{1}+iP_{2}$:

$$
B\left(P_{1}+iP_{2}\right)=\left(P_{1}+iP_{2}\right)A.
$$

Compare real and imaginary parts:

$$
BP_{1}=P_{1}A,
$$

$$
BP_{2}=P_{2}A.
$$

Therefore, for every real number $t$,

$$
B\left(P_{1}+tP_{2}\right)=\left(P_{1}+tP_{2}\right)A.
$$

Consider the polynomial $\det\left(P_{1}+xP_{2}\right)$ in $x$ with real coefficients.

Since $P=P_{1}+iP_{2}$ is invertible, $\det\left(P\right)\ne0$, i.e. $\det\left(P_{1}+iP_{2}\right)\ne0$.

Hence $\det\left(P_{1}+xP_{2}\right)$ is not the zero polynomial and has only finitely many real roots.

Therefore there exists a real number $t$ such that

$$
\det\left(P_{1}+tP_{2}\right)\ne0.
$$

That is, $P_{1}+tP_{2}$ is invertible.

Set $Q=P_{1}+tP_{2}$, an invertible real matrix.

Then

$$
BQ=QA,
$$

i.e.

$$
B=Q^{-1}AQ.
$$

Hence $A$ and $B$ are similar as real matrices.

This contradicts the assumption.

Therefore, if $A$ and $B$ are not similar as real matrices, they are not similar as complex matrices either. $\blacksquare$
