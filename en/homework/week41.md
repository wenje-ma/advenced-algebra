# Assignment 41

> **Definition 1** (Polynomial in $n$ Variables)<br>Let $K$ be a number field. Using $n$ symbols $x_{1},x_{2},\ldots,x_{n}$ not belonging to $K$, form the expression

$$
\sum_{i_{1},i_{2},\ldots,i_{n}}a_{i_{1}i_{2}\ldots i_{n}}x_{1}^{i_{1}}x_{2}^{i_{2}}\cdots x_{n}^{i_{n}},
$$

where $a_{i_{1}i_{2}\ldots i_{n}}\in K$ and $i_{1},i_{2},\ldots,i_{n}$ are nonnegative integers. Only finitely many monomials have coefficients not equal to $0$. Such an expression is called a polynomial in $n$ variables over the number field $K$.

> **Theorem 1** (Leading Term Theorem)<br>In $K\left[x_{1},x_{2},\ldots,x_{n}\right]$, the leading term of the product of two nonzero polynomials equals the product of their leading terms. Hence the product of two nonzero polynomials is again a nonzero polynomial; that is, $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ is a ring without zero divisors.

### Problem 1

(Problem 7.9-3) Let $f,g\in K\left[x_{1},\ldots,x_{n}\right]$ with $g\ne0$. Prove: if for every tuple of elements $c_{1},\ldots,c_{n}\in K$ such that $g\left(c_{1},\ldots,c_{n}\right)\ne0$, we have $f\left(c_{1},\ldots,c_{n}\right)=0$, then $f\left(x_{1},\ldots,x_{n}\right)=0$.

### Solution to Problem 1

By **Theorem 1** (Leading Term Theorem), in $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ the product of two nonzero polynomials is again a nonzero polynomial. Use mathematical induction.

**When $n=1$**.

$f\left(x\right)$ is a polynomial in $K\left[x\right]$. If $f\left(x\right)=0$ for infinitely many $x$, then $f\left(x\right)=0$.

This is because the number of roots of a nonzero polynomial does not exceed its degree.

**Inductive step**.

Assume the conclusion holds for polynomials in $n-1$ variables.

Now consider the polynomial $f\left(x_{1},\ldots,x_{n}\right)$ in $n$ variables.

Write $f$ as a polynomial in $x_{n}$:

$$
f\left(x_{1},\ldots,x_{n}\right)=u_{0}\left(x_{1},\ldots,x_{n-1}\right)+u_{1}\left(x_{1},\ldots,x_{n-1}\right)x_{n}+\ldots+u_{s}\left(x_{1},\ldots,x_{n-1}\right)x_{n}^{s}.
$$

where

$$
u_{i}\left(x_{1},\ldots,x_{n-1}\right)\in K\left[x_{1},\ldots,x_{n-1}\right].
$$

By the inductive hypothesis, there exist $c_{1},\ldots,c_{n-1}\in K$ such that:

1. $g\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ is not the zero polynomial;
2.

   $$
   u_{0}\left(c_{1},\ldots,c_{n-1}\right),\ldots,u_{s}\left(c_{1},\ldots,c_{n-1}\right)
   $$

   are not all zero (if $f$ is not the zero polynomial).

For such $c_{1},\ldots,c_{n-1}$, consider the univariate polynomial in $x_{n}$:

$$
f\left(c_{1},\ldots,c_{n-1},x_{n}\right)=u_{0}\left(c_{1},\ldots,c_{n-1}\right)+\ldots+u_{s}\left(c_{1},\ldots,c_{n-1}\right)x_{n}^{s}.
$$

If $f$ is not the zero polynomial, then this univariate polynomial is also not the zero polynomial.

Therefore it has only finitely many roots.

But the hypothesis says that for all $c_{n}$ such that $g\left(c_{1},\ldots,c_{n}\right)\ne0$, we have $f\left(c_{1},\ldots,c_{n}\right)=0$.

And $g\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ is not the zero polynomial, so it has only finitely many roots.

Therefore there are infinitely many $c_{n}$ such that $g\left(c_{1},\ldots,c_{n}\right)\ne0$.

For all such $c_{n}$, $f\left(c_{1},\ldots,c_{n}\right)=0$.

Therefore $f\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ has infinitely many roots.

But $f\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ is a nonzero univariate polynomial with only finitely many roots. This is a contradiction.

Therefore $f\left(x_{1},\ldots,x_{n}\right)=0$. $\blacksquare$

### Problem 2

(Problem 7.9-4(2)) $f\in K\left[x_{1},\ldots,x_{n}\right]$ is called irreducible if the only divisors of $f$ are constant polynomials and associates of $f$; otherwise it is called reducible. Prove: in $K\left[x,y\right]$, the polynomial $x-y$ is irreducible.

### Solution to Problem 2

Suppose, for contradiction, that $x-y$ is reducible, i.e. there exist two polynomials $g\left(x,y\right),h\left(x,y\right)$ of positive degree such that:

$$
x-y=g\left(x,y\right)h\left(x,y\right).
$$

Consider the degrees.

The degree of the left-hand side $x-y$ is $1$.

The degree of the right-hand side $g\left(x,y\right)h\left(x,y\right)$ is $\deg g+\deg h$.

Since $\deg g> 0$ and $\deg h> 0$,

$$
\deg g+\deg h\ge2.
$$

This is a contradiction.

Therefore $x-y$ is irreducible. $\blacksquare$
