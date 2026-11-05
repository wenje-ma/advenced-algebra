# week23

> **Definition 7.6.1 (Root of a Polynomial)**
> 
> Let $K$ be a number field, and let $R$ be a commutative ring with identity that can be viewed as an extension ring of $K$. For a polynomial $f\left(x\right)$ in $K\left[x\right]$, if there is an element $c$ in $R$ such that $f\left(c\right)=0$, then $c$ is called a root of $f\left(x\right)$ in $R$.

> **Theorem 7.6.1 (Remainder Theorem)**
> 
> In $K\left[x\right]$, the remainder when $f\left(x\right)$ is divided by $x-a$ is $f\left(a\right)$.

> **Corollary 7.6.2 (Factor Theorem)**
> 
> In $K\left[x\right]$, $x-a$ divides $f\left(x\right)$ if and only if $f\left(a\right)=0$.

> **Property 7.7.1 (Conjugate Pairs of Nonreal Roots)**
> 
> The nonreal roots of a real-coefficient polynomial occur in conjugate pairs with the same multiplicity.

> **Theorem 7.7.1 (Unique Factorization Theorem for Real Polynomials)**
> 
> Every real-coefficient polynomial of positive degree can be uniquely factored over $\mathbb{R}$ into a product of linear factors and quadratic factors with negative discriminant.

> **Definition 7.8.1 (Primitive Polynomial)**
> 
> A nonzero polynomial with integer coefficients is called primitive if the greatest common divisor of its coefficients is $1$.

> **Lemma 7.8.1 (Gauss Lemma)**
> 
> The product of two primitive polynomials is again primitive.

> **Theorem 7.8.1 (Eisenstein Criterion)**
> 
> Let

$$
f\left(x\right)=a_{n}x^{n}+\cdots+a_{1}x+a_{0}
$$
be a polynomial with integer coefficients of degree $n> 0$. If there exists a prime $p$ such that (1) $p\mid a_{i}$ for $i=0,1,\ldots,n-1$; (2) $p\nmid a_{n}$; (3) $p^{2}\nmid a_{0}$, then $f\left(x\right)$ is irreducible over $\mathbb{Q}$.

## 7.6-1

Let

$$
f\left(x\right)=x^{5}+7x^{4}+19x^{3}+26x^{2}+20x+8\in\mathbb{Q}\left[x\right].
$$

Determine whether $-2$ is a root of $f\left(x\right)$, and if so, its multiplicity.

### Solution to 7.6-1

By **Corollary 7.6.2 (Factor Theorem)**, $x-a$ divides $f\left(x\right)$ if and only if $f\left(a\right)=0$. Compute $f\left(-2\right)$:

$$
f\left(-2\right)
=\left(-2\right)^{5}+7\left(-2\right)^{4}+19\left(-2\right)^{3}+26\left(-2\right)^{2}+20\left(-2\right)+8=-32+112-152+104-40+8=0.
$$

Hence $-2$ is a root of $f\left(x\right)$.

Use synthetic division to see how many times $x+2$ divides $f$.

First division:

$$
\begin{array}{r|rrrrrr}
-2 & 1 & 7 & 19 & 26 & 20 & 8\\
   &   & -2 & -10 & -18 & -16 & -8\\
\hline
   & 1 & 5 & 9 & 8 & 4 & 0
\end{array}
$$

Remainder $0$, quotient $x^{4}+5x^{3}+9x^{2}+8x+4$.

Second division:

$$
\begin{array}{r|rrrrr}
-2 & 1 & 5 & 9 & 8 & 4\\
   &   & -2 & -6 & -6 & -4\\
\hline
   & 1 & 3 & 3 & 2 & 0
\end{array}
$$

Remainder $0$, quotient $x^{3}+3x^{2}+3x+2$.

Third division:

$$
\begin{array}{r|rrrr}
-2 & 1 & 3 & 3 & 2\\
   &   & -2 & -2 & -2\\
\hline
   & 1 & 1 & 1 & 0
\end{array}
$$

Remainder $0$, quotient $x^{2}+x+1$.

Fourth division:

$$
\begin{array}{r|rrr}
-2 & 1 & 1 & 1\\
   &   & -2 & 2\\
\hline
   & 1 & -1 & 3
\end{array}
$$

Remainder $3\ne0$.

Hence $-2$ is a triple root of $f\left(x\right)$. $\blacksquare$

## 7.6-4

Let

$$
f\left(x\right)=x^{4}-5x^{3}+ax^{2}+bx+9\in\mathbb{Q}\left[x\right].
$$

If $3$ is a double root of $f\left(x\right)$, find $a,b$.

### Solution to 7.6-4

If $3$ is a double root of $f\left(x\right)$, then $f\left(3\right)=0$ and $f'\left(3\right)=0$.

Compute $f\left(3\right)$:

$$
f\left(3\right)
=3^{4}-5\cdot3^{3}+a\cdot3^{2}+b\cdot3+9=81-135+9a+3b+9=-45+9a+3b.
$$

Set $f\left(3\right)=0$:

$$
9a+3b=45\Rightarrow 3a+b=15. \tag{1}
$$

Compute the derivative:

$$
f'\left(x\right)=4x^{3}-15x^{2}+2ax+b.
$$

Compute $f'\left(3\right)$:

$$
f'\left(3\right)
=4\cdot3^{3}-15\cdot3^{2}+2a\cdot3+b=108-135+6a+b=-27+6a+b.
$$

Set $f'\left(3\right)=0$:

$$
6a+b=27. \tag{2}
$$

Subtract $\left(1\right)$ from $\left(2\right)$:

$$
3a=12\Rightarrow a=4.
$$

Substitute into $\left(1\right)$:

$$
3\cdot4+b=15\Rightarrow b=3.
$$

Hence $a=4$, $b=3$. $\blacksquare$

## 7.6-8

Find the standard factorization of the complex-coefficient polynomial $x^{n}-1$.

### Solution to 7.6-8

The roots of $x^{n}-1=0$ satisfy $x^{n}=1$.

The $n$-th roots of unity are:

$$
x_{k}=e^{2\pi i k/n}=\cos\frac{2\pi k}{n}+i\sin\frac{2\pi k}{n},\ k=0,1,\ldots,n-1.
$$

Therefore the standard factorization is:

$$
x^{n}-1=\prod_{k=0}^{n-1}\left(x-e^{2\pi i k/n}\right).
$$

$\blacksquare$

## 7.7-4

Prove: if two $n\times n$ real matrices $A$ and $B$ are not similar over $\mathbb{R}$, then they are still not similar when viewed as complex matrices.

### Solution to 7.7-4

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

## 7.8-2(4)

Is $x^{4}-2x^{3}+2x-3$ irreducible over $\mathbb{Q}$?

### Solution to 7.8-2(4)

By **Theorem 7.8.1 (Eisenstein Criterion)**, first check for rational roots.

Possible rational roots are $\pm1$, $\pm3$.

$$
f\left(1\right)=1-2+2-3=-2\ne0.
$$

$$
f\left(-1\right)=1+2-2-3=-2\ne0.
$$

$$
f\left(3\right)=81-54+6-3=30\ne0.
$$

$$
f\left(-3\right)=81+54-6-3=126\ne0.
$$

Hence there is no rational root.

Suppose it factors as a product of two integer-coefficient quadratics:

$$
x^{4}-2x^{3}+2x-3=\left(x^{2}+ax+b\right)\left(x^{2}+cx+d\right).
$$

Compare coefficients:

$$
a+c=-2, \tag{1}
$$

$$
ac+b+d=0, \tag{2}
$$

$$
ad+bc=2, \tag{3}
$$

$$
bd=-3. \tag{4}
$$

From $\left(4\right)$, the integer solutions of $bd=-3$ are:

$$
\left(b,d\right)=\left(1,-3\right),\left(-1,3\right),\left(3,-1\right),\left(-3,1\right).
$$

Check each:

- $b=1,d=-3$: from $\left(1\right)$, $c=-2-a$. Substitute into $\left(2\right)$:

  $$
  -2a-a^{2}+1-3=0\Rightarrow a^{2}+2a+2=0,
  $$

  no real roots.
- $b=-1,d=3$: substitute into $\left(2\right)$:

  $$
  -2a-a^{2}-1+3=0\Rightarrow a^{2}+2a-2=0,
  $$

  no integer roots.
- $b=3,d=-1$: substitute into $\left(2\right)$:

  $$
  -2a-a^{2}+3-1=0\Rightarrow a^{2}+2a-2=0,
  $$

  no integer roots.
- $b=-3,d=1$: substitute into $\left(2\right)$:

  $$
  -2a-a^{2}-3+1=0\Rightarrow a^{2}+2a+2=0,
  $$

  no real roots.

Hence it cannot be factored into two integer quadratics.

Therefore $x^{4}-2x^{3}+2x-3$ is irreducible over $\mathbb{Q}$. $\blacksquare$

## 7.8-2(5)

Is $x^{4}+px^{2}+1$ (where $p$ is an odd prime) irreducible over $\mathbb{Q}$?

### Solution to 7.8-2(5)

First check for rational roots.

Possible rational roots are $\pm1$.

$$
f\left(1\right)=1+p+1=p+2\ne0.
$$

$$
f\left(-1\right)=1+p+1=p+2\ne0.
$$

Hence there is no rational root.

Suppose it factors as a product of two integer quadratics:

$$
x^{4}+px^{2}+1=\left(x^{2}+ax+b\right)\left(x^{2}+cx+d\right).
$$

Compare coefficients:

$$
a+c=0, \tag{1}
$$

$$
ac+b+d=p, \tag{2}
$$

$$
ad+bc=0, \tag{3}
$$

$$
bd=1. \tag{4}
$$

From $\left(1\right)$, $c=-a$.

Substitute into $\left(3\right)$:

$$
ad+b\left(-a\right)=a\left(d-b\right)=0.
$$

Hence $a=0$ or $d=b$.

Case 1: $a=0$.

Then $c=0$.

From $\left(2\right)$: $b+d=p$.

From $\left(4\right)$: $bd=1$.

Thus $b=d=1$ or $b=d=-1$.

If $b=d=1$, then $b+d=2$, so $p=2$. But $p$ is odd, contradiction.

If $b=d=-1$, then $b+d=-2$, so $p=-2$. But $p$ is a positive prime, contradiction.

Case 2: $d=b$.

From $\left(4\right)$: $b^{2}=1$, so $b=1$ or $b=-1$.

If $b=1$, then $d=1$.

From $\left(2\right)$:

$$
-a^{2}+2=p\Rightarrow a^{2}=2-p.
$$

Since $p$ is odd and $p\ge3$, $2-p\le-1< 0$, no real root.

If $b=-1$, then $d=-1$.

From $\left(2\right)$:

$$
-a^{2}-2=p\Rightarrow a^{2}=-p-2< 0,
$$

no real root.

Hence it cannot be factored into two integer quadratics.

Therefore $x^{4}+px^{2}+1$ is irreducible over $\mathbb{Q}$. $\blacksquare$

## 7.8-2(7)

Is $2x^{3}-x^{2}+x+1$ irreducible over $\mathbb{Q}$?

### Solution to 7.8-2(7)

A cubic is reducible over $\mathbb{Q}$ if and only if it has a rational root.

Possible rational roots are $\pm1$, $\pm\frac{1}{2}$.

$$
f\left(1\right)=2-1+1+1=3\ne0.
$$

$$
f\left(-1\right)=-2-1-1+1=-3\ne0.
$$

$$
f\left(\frac{1}{2}\right)=2\cdot\frac{1}{8}-\frac{1}{4}+\frac{1}{2}+1=\frac{1}{4}-\frac{1}{4}+\frac{1}{2}+1=\frac{3}{2}\ne0.
$$

$$
f\left(-\frac{1}{2}\right)=2\cdot\left(-\frac{1}{8}\right)-\frac{1}{4}+\left(-\frac{1}{2}\right)+1=-\frac{1}{4}-\frac{1}{4}-\frac{1}{2}+1=0.
$$

Hence $-\frac{1}{2}$ is a rational root.

Therefore $f\left(x\right)$ is reducible over $\mathbb{Q}$. $\blacksquare$

## 7.8-2(8)

Is $x^{4}-5x^{2}+1$ irreducible over $\mathbb{Q}$?

### Solution to 7.8-2(8)

First check for rational roots.

Possible rational roots are $\pm1$.

$$
f\left(1\right)=1-5+1=-3\ne0.
$$

$$
f\left(-1\right)=1-5+1=-3\ne0.
$$

Hence there is no rational root.

Suppose it factors as a product of two integer quadratics:

$$
x^{4}-5x^{2}+1=\left(x^{2}+ax+b\right)\left(x^{2}+cx+d\right).
$$

Compare coefficients:

$$
a+c=0, \tag{1}
$$

$$
ac+b+d=-5, \tag{2}
$$

$$
ad+bc=0, \tag{3}
$$

$$
bd=1. \tag{4}
$$

From $\left(1\right)$, $c=-a$.

Substitute into $\left(3\right)$:

$$
ad+b\left(-a\right)=a\left(d-b\right)=0.
$$

Hence $a=0$ or $d=b$.

Case 1: $a=0$.

Then $c=0$.

From $\left(2\right)$: $b+d=-5$.

From $\left(4\right)$: $bd=1$.

Thus $b,d$ are roots of $t^{2}+5t+1=0$, not integers.

Case 2: $d=b$.

From $\left(4\right)$: $b^{2}=1$, so $b=1$ or $b=-1$.

If $b=1$, then $d=1$.

From $\left(2\right)$: $-a^{2}+2=-5\Rightarrow a^{2}=7$, not a perfect square.

If $b=-1$, then $d=-1$.

From $\left(2\right)$: $-a^{2}-2=-5\Rightarrow a^{2}=3$, not a perfect square.

Hence it cannot be factored into two integer quadratics.

Therefore $x^{4}-5x^{2}+1$ is irreducible over $\mathbb{Q}$. $\blacksquare$
