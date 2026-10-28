# week41

> **Definition 7.9.1 (Polynomial in $n$ Variables)**<br>Let $K$ be a number field. Using $n$ symbols $x_{1},x_{2},\ldots,x_{n}$ not in $K$, form the expression

$$
\sum_{i_{1},i_{2},\ldots,i_{n}}a_{i_{1}i_{2}\ldots i_{n}}x_{1}^{i_{1}}x_{2}^{i_{2}}\cdots x_{n}^{i_{n}},
$$

where $a_{i_{1}i_{2}\ldots i_{n}}\in K$ and $i_{1},i_{2},\ldots,i_{n}$ are nonnegative integers. Only finitely many monomials have nonzero coefficients. Such an expression is called a polynomial in $n$ variables over $K$.

> **Theorem 7.9.1 (Leading Term Theorem)**<br>In $K\left[x_{1},x_{2},\ldots,x_{n}\right]$, the leading term of the product of two nonzero polynomials equals the product of their leading terms. Hence the product of two nonzero polynomials is again nonzero, i.e. $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ has no zero divisors.

---

## 7.9-3

Let $f,g\in K\left[x_{1},\ldots,x_{n}\right]$ with $g\ne0$. Prove: if for every tuple $c_{1},\ldots,c_{n}\in K$ with $g\left(c_{1},\ldots,c_{n}\right)\ne0$ we have $f\left(c_{1},\ldots,c_{n}\right)=0$, then $f\left(x_{1},\ldots,x_{n}\right)=0$.

### Solution 7.9-3

By **Theorem 7.9.1 (Leading Term Theorem)**, the product of two nonzero polynomials in $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ is nonzero. Use induction on $n$.

**Base case $n=1$**.

$f\left(x\right)$ is a polynomial in $K\left[x\right]$. If $f\left(x\right)=0$ for infinitely many $x$, then $f\left(x\right)=0$.

This is because the number of roots of a nonzero polynomial does not exceed its degree.

**Inductive step**.

Assume the claim holds for polynomials in $n-1$ variables.

Now consider an $n$-variable polynomial $f\left(x_{1},\ldots,x_{n}\right)$.

Write $f$ as a polynomial in $x_{n}$:

$$
f\left(x_{1},\ldots,x_{n}\right)=u_{0}\left(x_{1},\ldots,x_{n-1}\right)+u_{1}\left(x_{1},\ldots,x_{n-1}\right)x_{n}+\cdots+u_{s}\left(x_{1},\ldots,x_{n-1}\right)x_{n}^{s}.
$$

where

$$
u_{i}\left(x_{1},\ldots,x_{n-1}\right)\in K\left[x_{1},\ldots,x_{n-1}\right].
$$

By the induction hypothesis, there exist $c_{1},\ldots,c_{n-1}\in K$ such that:

1. $g\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ is not the zero polynomial;
2.

   $$
   u_{0}\left(c_{1},\ldots,c_{n-1}\right),\ldots,u_{s}\left(c_{1},\ldots,c_{n-1}\right)
   $$

   are not all zero (if $f$ is not the zero polynomial).

For such $c_{1},\ldots,c_{n-1}$, consider the univariate polynomial in $x_{n}$:

$$
f\left(c_{1},\ldots,c_{n-1},x_{n}\right)=u_{0}\left(c_{1},\ldots,c_{n-1}\right)+\cdots+u_{s}\left(c_{1},\ldots,c_{n-1}\right)x_{n}^{s}.
$$

If $f$ is nonzero, this univariate polynomial is also nonzero.

Hence it has only finitely many roots.

But the hypothesis says that for all $c_{n}$ with $g\left(c_{1},\ldots,c_{n}\right)\ne0$, we have $f\left(c_{1},\ldots,c_{n}\right)=0$.

Since $g\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ is nonzero, it has only finitely many roots.

Hence there are infinitely many $c_{n}$ with $g\left(c_{1},\ldots,c_{n}\right)\ne0$.

For all these $c_{n}$, $f\left(c_{1},\ldots,c_{n}\right)=0$.

So $f\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ has infinitely many roots.

But $f\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ is a nonzero univariate polynomial and has only finitely many roots. Contradiction.

Therefore $f\left(x_{1},\ldots,x_{n}\right)=0$. $\blacksquare$

---

## 7.9-4(2)

A polynomial $f\in K\left[x_{1},\ldots,x_{n}\right]$ is called irreducible if its only divisors are constants and associates of $f$; otherwise it is reducible. Prove: in $K\left[x,y\right]$, the polynomial $x-y$ is irreducible.

### Solution 7.9-4(2)

Suppose $x-y$ is reducible, i.e. there exist two polynomials $g\left(x,y\right),h\left(x,y\right)$ of positive degree such that:

$$
x-y=g\left(x,y\right)h\left(x,y\right).
$$

Consider degrees.

The degree of the left side $x-y$ is $1$.

The degree of the right side $g\left(x,y\right)h\left(x,y\right)$ is $\deg g+\deg h$.

Since $\deg g> 0$ and $\deg h> 0$,

$$
\deg g+\deg h\ge2.
$$

Contradiction.

Therefore $x-y$ is irreducible. $\blacksquare$
