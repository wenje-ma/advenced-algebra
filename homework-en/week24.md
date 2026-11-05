# week24

> **Definition 7.8.1 (Primitive Polynomial)**
> 
> A nonzero polynomial with integer coefficients is called primitive if the greatest common divisor of its coefficients is $1$.

> **Lemma 7.8.1 (Gauss Lemma)**
> 
> The product of two primitive polynomials is again primitive.

> **Theorem 7.8.1 (Eisenstein Criterion)**
> 
> Let

> **Definition 7.9.1 (Polynomial in $n$ Variables)**
> 
> Let $K$ be a number field. Using $n$ symbols $x_{1},x_{2},\ldots,x_{n}$ not in $K$, form the expression

$$
\sum_{i_{1},i_{2},\ldots,i_{n}}a_{i_{1}i_{2}\ldots i_{n}}x_{1}^{i_{1}}x_{2}^{i_{2}}\cdots x_{n}^{i_{n}},
$$
where $a_{i_{1}i_{2}\ldots i_{n}}\in K$ and $i_{1},i_{2},\ldots,i_{n}$ are nonnegative integers. Only finitely many monomials have nonzero coefficients. Such an expression is called a polynomial in $n$ variables over $K$.

> **Theorem 7.9.1 (Leading Term Theorem)**
> 
> In $K\left[x_{1},x_{2},\ldots,x_{n}\right]$, the leading term of the product of two nonzero polynomials equals the product of their leading terms. Hence the product of two nonzero polynomials is again nonzero, i.e. $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ has no zero divisors.

$$
\sigma_{1}=x_{1}+x_{2}+\cdots+x_{n},
$$
$$
\sigma_{2}=x_{1}x_{2}+x_{1}x_{3}+\cdots+x_{n-1}x_{n},
$$
$$
\cdots\cdots
$$
$$
\sigma_{n}=x_{1}x_{2}\cdots x_{n}.
$$
$$
S_{1}=\sigma_{1},
$$
$$
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\cdots+\left(-1\right)^{k-1}\sigma_{k-1}S_{1}+\left(-1\right)^{k}k\sigma_{k}=0,\quad 1\le k\le n,
$$
$$
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\cdots+\left(-1\right)^{n}\sigma_{n}S_{k-n}=0,\quad k> n.
$$

> **Definition 7.10.1 (Symmetric Polynomial)**
> 
> Let $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ be a polynomial over $K$. If for every permutation $j_{1}j_{2}\ldots j_{n}$ of $1,2,\ldots,n$,

$$
f\left(x_{j_{1}},x_{j_{2}},\ldots,x_{j_{n}}\right)=f\left(x_{1},x_{2},\ldots,x_{n}\right),
$$
then $f$ is called a symmetric polynomial over $K$.

## 7.8-5

Let $f\left(x\right)$ be a monic polynomial with integer coefficients of positive degree. Prove: if $f\left(0\right)$ and $f\left(1\right)$ are both odd, then $f\left(x\right)$ has no rational root.

### Solution to 7.8-5

Write

$$
f\left(x\right)=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{0},
$$

with all $a_{i}$ integers.

$f\left(0\right)=a_{0}$, so $a_{0}$ is odd.

$$
f\left(1\right)=1+a_{n-1}+\cdots+a_{1}+a_{0}
$$

is odd.

Suppose $f\left(x\right)$ has a rational root $r=\frac{p}{q}$, where $p,q$ are coprime integers, $q> 0$.

Since the leading coefficient is $1$, $q=1$, i.e. $r$ is an integer.

Moreover $r\mid a_{0}$, so $r$ is odd (since $a_{0}$ is odd).

Consider $f\left(r\right)\bmod 2$.

Since $r$ is odd, $r\equiv1\pmod2$.

Therefore

$$
f\left(r\right)\equiv1^{n}+a_{n-1}\cdot1^{n-1}+\cdots+a_{1}\cdot1+a_{0}=f\left(1\right)\pmod2.
$$

Since $f\left(1\right)$ is odd, $f\left(r\right)\equiv1\pmod2$, i.e. $f\left(r\right)\ne0$.

Contradiction.

Therefore $f\left(x\right)$ has no rational root. $\blacksquare$

## 7.8-6

Let

$$
f\left(x\right)=x^{3}+ax^{2}+bx+c
$$

be a polynomial with integer coefficients. Prove: if $\left(a+b\right)c$ is odd, then $f\left(x\right)$ is irreducible over $\mathbb{Q}$.

### Solution to 7.8-6

$f\left(x\right)$ is a cubic. A cubic is reducible over $\mathbb{Q}$ if and only if it has a rational root.

Since the leading coefficient is $1$, any rational root is an integer dividing the constant term $c$.

Suppose $f\left(x\right)$ has a rational root $r$; then $r$ is an integer and $r\mid c$.

Since $\left(a+b\right)c$ is odd, $a+b$ is odd and $c$ is odd.

Hence $r$ is odd.

Consider $f\left(r\right)\bmod 2$.

Since $r$ is odd, $r\equiv1\pmod2$.

Therefore

$$
f\left(r\right)\equiv1+a\cdot1+b\cdot1+c=1+a+b+c\pmod2.
$$

Since $a+b$ is odd and $c$ is odd, $a+b+c$ is even.

Hence $1+a+b+c$ is odd.

Therefore $f\left(r\right)\equiv1\pmod2$, i.e. $f\left(r\right)\ne0$.

Contradiction.

Hence $f\left(x\right)$ has no rational root.

Therefore $f\left(x\right)$ is irreducible over $\mathbb{Q}$. $\blacksquare$

## 7.9-3

Let $f,g\in K\left[x_{1},\ldots,x_{n}\right]$ with $g\ne0$. Prove: if for every tuple $c_{1},\ldots,c_{n}\in K$ with $g\left(c_{1},\ldots,c_{n}\right)\ne0$ we have $f\left(c_{1},\ldots,c_{n}\right)=0$, then $f\left(x_{1},\ldots,x_{n}\right)=0$.

### Solution to 7.9-3

By **Theorem 7.9.1 (Leading Term Theorem)**, the product of two nonzero polynomials in $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ is nonzero. Use induction on $n$.

Base case $n=1$.

$f\left(x\right)$ is a polynomial in $K\left[x\right]$. If $f\left(x\right)=0$ for infinitely many $x$, then $f\left(x\right)=0$.

This is because the number of roots of a nonzero polynomial does not exceed its degree.

Inductive step.

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

## 7.9-4(2)

A polynomial $f\in K\left[x_{1},\ldots,x_{n}\right]$ is called irreducible if its only divisors are constants and associates of $f$; otherwise it is reducible. Prove: in $K\left[x,y\right]$, the polynomial $x-y$ is irreducible.

### Solution to 7.9-4(2)

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

## 7.10-5

In $K\left[x_{1},x_{2},x_{3}\right]$, use Newton's identities to express the power sums $S_{2},S_{3},S_{4}$ in terms of elementary symmetric polynomials.

### Solution to 7.10-5

By Newton's Identities, let $S_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$. The elementary symmetric polynomials:

$$
\sigma_{1}=x_{1}+x_{2}+x_{3},
$$

$$
\sigma_{2}=x_{1}x_{2}+x_{1}x_{3}+x_{2}x_{3},
$$

$$
\sigma_{3}=x_{1}x_{2}x_{3}.
$$

$S_{2}$.

By Newton's identities:

$$
S_{2}-\sigma_{1}S_{1}+2\sigma_{2}=0.
$$

Since $S_{1}=\sigma_{1}$,

$$
S_{2}=\sigma_{1}S_{1}-2\sigma_{2}=\sigma_{1}^{2}-2\sigma_{2}.
$$

$S_{3}$.

By Newton's identities:

$$
S_{3}-\sigma_{1}S_{2}+\sigma_{2}S_{1}-3\sigma_{3}=0.
$$

Hence

$$
S_{3}
=\sigma_{1}S_{2}-\sigma_{2}S_{1}+3\sigma_{3}=\sigma_{1}\left(\sigma_{1}^{2}-2\sigma_{2}\right)-\sigma_{2}\sigma_{1}+3\sigma_{3}=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}.
$$

$S_{4}$.

By Newton's identities (since $n=3$, $k=4> n$):

$$
S_{4}-\sigma_{1}S_{3}+\sigma_{2}S_{2}-\sigma_{3}S_{1}=0.
$$

Hence

$$
S_{4}
=\sigma_{1}S_{3}-\sigma_{2}S_{2}+\sigma_{3}S_{1}=\sigma_{1}\left(\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}\right)-\sigma_{2}\left(\sigma_{1}^{2}-2\sigma_{2}\right)+\sigma_{3}\sigma_{1}=\sigma_{1}^{4}-3\sigma_{1}^{2}\sigma_{2}+3\sigma_{1}\sigma_{3}-\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+\sigma_{1}\sigma_{3}=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
$$

$S_{2}=\sigma_{1}^{2}-2\sigma_{2}$, $S_{3}=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}$,

$$
S_{4}=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
$$

$\blacksquare$

## 7.10-7

Let $f\left(x\right)\in K\left[x\right]$ be monic, $a\in K$, and $g\left(x\right)=\left(x-a\right)f\left(x\right)$. Prove: $D\left(g\right)=D\left(f\right)f\left(a\right)^{2}$.

### Solution to 7.10-7

Write

$$
f\left(x\right)=\left(x-r_{1}\right)\left(x-r_{2}\right)\cdots\left(x-r_{n}\right),
$$

where $r_{1},r_{2},\ldots,r_{n}$ are all roots of $f\left(x\right)$ (with multiplicity).

Then

$$
g\left(x\right)=\left(x-a\right)f\left(x\right)=\left(x-a\right)\left(x-r_{1}\right)\left(x-r_{2}\right)\cdots\left(x-r_{n}\right).
$$

Set $s_{0}=a$, $s_{1}=r_{1}$, $\ldots$, $s_{n}=r_{n}$.

The discriminant is defined as:

$$
D\left(f\right)=\prod_{1\le i< j\le n}\left(r_{i}-r_{j}\right)^{2}.
$$

$$
D\left(g\right)=\prod_{0\le i< j\le n}\left(s_{i}-s_{j}\right)^{2}.
$$

Therefore

$$
D\left(g\right)
=\prod_{1\le i< j\le n}\left(r_{i}-r_{j}\right)^{2}\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}=D\left(f\right)\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}.
$$

And

$$
f\left(a\right)=\left(a-r_{1}\right)\left(a-r_{2}\right)\cdots\left(a-r_{n}\right).
$$

Hence

$$
\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}=f\left(a\right)^{2}.
$$

Therefore

$$
D\left(g\right)=D\left(f\right)\cdot f\left(a\right)^{2}.
$$

$\blacksquare$
