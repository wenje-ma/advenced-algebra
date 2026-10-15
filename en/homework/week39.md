# Assignment 39

> **Theorem 3** (Unique Factorization Theorem for Real Polynomials)<br>Every real polynomial of positive degree can be uniquely factored over the real number field as a product of linear factors and quadratic factors with negative discriminant.

> **Property** (Complex Roots Occur in Conjugate Pairs)<br>The non-real roots of a real polynomial occur in conjugate pairs, and with the same multiplicities.

### Problem 1

(Problem 7.7-4) Prove: if two real matrices $A$ and $B$ of order $n$ are not similar, then they are still not similar when regarded as complex matrices.

### Solution to Problem 1

By **Property** (Complex Roots Occur in Conjugate Pairs), the non-real roots of a real polynomial occur in conjugate pairs with the same multiplicities. Use proof by contradiction.

Suppose, for contradiction, that $A$ and $B$ are similar as complex matrices, i.e. there exists an invertible complex matrix $P$ such that

$$
B=P^{-1}AP.
$$

We need to prove that $A$ and $B$ are also similar as real matrices.

Write $P=P_{1}+iP_{2}$, where $P_{1},P_{2}$ are real matrices.

From $B=P^{-1}AP$ we get

$$
BP=PA.
$$

Substitute $P=P_{1}+iP_{2}$:

$$
B\left(P_{1}+iP_{2}\right)=\left(P_{1}+iP_{2}\right)A.
$$

Compare the real and imaginary parts:

$$
BP_{1}=P_{1}A,
$$

$$
BP_{2}=P_{2}A.
$$

Therefore for any real number $t$,

$$
B\left(P_{1}+tP_{2}\right)=\left(P_{1}+tP_{2}\right)A.
$$

Consider the polynomial $\det\left(P_{1}+xP_{2}\right)$; this is a real polynomial in $x$.

Since $P=P_{1}+iP_{2}$ is invertible, $\det\left(P\right)\ne0$, i.e. $\det\left(P_{1}+iP_{2}\right)\ne0$.

Therefore $\det\left(P_{1}+xP_{2}\right)$ is not the zero polynomial, and it has only finitely many real roots.

Hence there exists a real number $t$ such that

$$
\det\left(P_{1}+tP_{2}\right)\ne0.
$$

That is, $P_{1}+tP_{2}$ is invertible.

Let $Q=P_{1}+tP_{2}$; this is an invertible real matrix.

Then

$$
BQ=QA,
$$

i.e.

$$
B=Q^{-1}AQ.
$$

Therefore $A$ and $B$ are also similar as real matrices.

This contradicts the hypothesis.

Therefore if $A$ and $B$ are not similar as real matrices, they are also not similar as complex matrices. $\blacksquare$
