# Assignment 40

> **Definition 1** (Primitive Polynomial)<br>A nonzero polynomial with integer coefficients is called primitive if the greatest common divisor of all its coefficients is $1$.

> **Lemma 2** (Gauss's Lemma)<br>The product of two primitive polynomials is still primitive.

> **Theorem 5** (Eisenstein's Criterion)<br>Let
> $$
> f\left(x\right)=a_{n}x^{n}+\ldots+a_{1}x+a_{0}
> $$
> be a polynomial with integer coefficients of degree $n$ greater than zero. If there exists a prime number $p$ such that
> (1) $p\mid a_{i}$, $i=0,1,\ldots,n-1$;
>
> (2) $p\nmid a_{n}$;
>
> (3) $p^{2}\nmid a_{0}$.
> then $f\left(x\right)$ is irreducible over the rational number field.

### Problem 1

(Problem 7.8-2(4)) Is $x^{4}-2x^{3}+2x-3$ irreducible over the rational number field?

### Solution to Problem 1

By **Theorem 5** (Eisenstein's Criterion), let

$$
f\left(x\right)=a_{n}x^{n}+\ldots+a_{1}x+a_{0}
$$

be a polynomial with integer coefficients of degree $n$ greater than zero. If there exists a prime number $p$ such that $p\mid a_{i}$ ( $i=0,1,\ldots,n-1$ ), $p\nmid a_{n}$, and $p^{2}\nmid a_{0}$, then $f\left(x\right)$ is irreducible over the rational number field.

First check for rational roots.

The possible rational roots are $\pm1$, $\pm3$.

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

So there are no rational roots.

Suppose it can be factored as a product of two quadratic polynomials with integer coefficients:

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

From $\left(4\right)$, the integer solutions to $bd=-3$ are:

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

Therefore it cannot be factored as a product of two quadratic polynomials with integer coefficients.

Hence $x^{4}-2x^{3}+2x-3$ is irreducible over the rational number field. $\blacksquare$

### Problem 2

(Problem 7.8-2(5)) Is $x^{4}+px^{2}+1$, where $p$ is an odd prime, irreducible over the rational number field?

### Solution to Problem 2

First check for rational roots.

The possible rational roots are $\pm1$.

$$
f\left(1\right)=1+p+1=p+2\ne0.
$$

$$
f\left(-1\right)=1+p+1=p+2\ne0.
$$

So there are no rational roots.

Suppose it can be factored as a product of two quadratic polynomials with integer coefficients:

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

Therefore $a=0$ or $d=b$.

**Case 1**: $a=0$.

Then $c=0$.

From $\left(2\right)$: $b+d=p$.

From $\left(4\right)$: $bd=1$.

Therefore $b=d=1$ or $b=d=-1$.

If $b=d=1$, then $b+d=2$, so $p=2$. But $p$ is an odd prime, a contradiction.

If $b=d=-1$, then $b+d=-2$, so $p=-2$. But $p$ is a positive prime, a contradiction.

**Case 2**: $d=b$.

From $\left(4\right)$: $b^{2}=1$, so $b=1$ or $b=-1$.

If $b=1$, then $d=1$.

From $\left(2\right)$:

$$
-a^{2}+2=p\Rightarrow a^{2}=2-p.
$$

Since $p$ is an odd prime, $p\ge3$, so $2-p\le-1<0$, no real roots.

If $b=-1$, then $d=-1$.

From $\left(2\right)$:

$$
-a^{2}-2=p\Rightarrow a^{2}=-p-2<0,
$$

no real roots.

Therefore it cannot be factored as a product of two quadratic polynomials with integer coefficients.

Hence $x^{4}+px^{2}+1$ is irreducible over the rational number field. $\blacksquare$

### Problem 3

(Problem 7.8-2(7)) Is $2x^{3}-x^{2}+x+1$ irreducible over the rational number field?

### Solution to Problem 3

A cubic polynomial is reducible over the rational number field if and only if it has a rational root.

The possible rational roots are $\pm1$, $\pm\frac{1}{2}$.

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

Therefore $-\frac{1}{2}$ is a rational root of $f\left(x\right)$.

Hence $f\left(x\right)$ is reducible over the rational number field. $\blacksquare$

### Problem 4

(Problem 7.8-2(8)) Is $x^{4}-5x^{2}+1$ irreducible over the rational number field?

### Solution to Problem 4

First check for rational roots.

The possible rational roots are $\pm1$.

$$
f\left(1\right)=1-5+1=-3\ne0.
$$

$$
f\left(-1\right)=1-5+1=-3\ne0.
$$

So there are no rational roots.

Suppose it can be factored as a product of two quadratic polynomials with integer coefficients:

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

Therefore $a=0$ or $d=b$.

**Case 1**: $a=0$.

Then $c=0$.

From $\left(2\right)$: $b+d=-5$.

From $\left(4\right)$: $bd=1$.

Therefore $b,d$ are the roots of $t^{2}+5t+1=0$, which are not integers.

**Case 2**: $d=b$.

From $\left(4\right)$: $b^{2}=1$, so $b=1$ or $b=-1$.

If $b=1$, then $d=1$.

From $\left(2\right)$: $-a^{2}+2=-5\Rightarrow a^{2}=7$, which is not a perfect square.

If $b=-1$, then $d=-1$.

From $\left(2\right)$: $-a^{2}-2=-5\Rightarrow a^{2}=3$, which is not a perfect square.

Therefore it cannot be factored as a product of two quadratic polynomials with integer coefficients.

Hence $x^{4}-5x^{2}+1$ is irreducible over the rational number field. $\blacksquare$

### Problem 5

(Problem 7.8-5) Let $f\left(x\right)$ be a polynomial with integer coefficients of positive degree and leading coefficient $1$. Prove: if both $f\left(0\right)$ and $f\left(1\right)$ are odd, then $f\left(x\right)$ has no rational roots.

### Solution to Problem 5

Let

$$
f\left(x\right)=x^{n}+a_{n-1}x^{n-1}+\ldots+a_{1}x+a_{0},
$$

where all $a_{i}$ are integers.

$f\left(0\right)=a_{0}$, so $a_{0}$ is odd.

$$
f\left(1\right)=1+a_{n-1}+\ldots+a_{1}+a_{0}
$$

is odd.

Suppose, for contradiction, that $f\left(x\right)$ has a rational root $r=\frac{p}{q}$, where $p,q$ are coprime integers and $q>0$.

Since the leading coefficient is $1$, we have $q=1$, i.e. $r$ is an integer.

Moreover, $r\mid a_{0}$, so $r$ is odd (since $a_{0}$ is odd).

Consider $f\left(r\right)\bmod 2$.

Since $r$ is odd, $r\equiv1\pmod2$.

Therefore

$$
f\left(r\right)\equiv1^{n}+a_{n-1}\cdot1^{n-1}+\ldots+a_{1}\cdot1+a_{0}=f\left(1\right)\pmod2.
$$

Since $f\left(1\right)$ is odd, $f\left(r\right)\equiv1\pmod2$, i.e. $f\left(r\right)\ne0$.

This is a contradiction.

Therefore $f\left(x\right)$ has no rational roots. $\blacksquare$

### Problem 6

(Problem 7.8-6) Let

$$
f\left(x\right)=x^{3}+ax^{2}+bx+c
$$

be a polynomial with integer coefficients. Prove: if $\left(a+b\right)c$ is odd, then $f\left(x\right)$ is irreducible over the rational number field.

### Solution to Problem 6

$f\left(x\right)$ is a cubic polynomial. A cubic polynomial is reducible over the rational number field if and only if it has a rational root.

Since the leading coefficient is $1$, any rational root is an integer root and divides the constant term $c$.

Suppose, for contradiction, that $f\left(x\right)$ has a rational root $r$; then $r$ is an integer and $r\mid c$.

Since $\left(a+b\right)c$ is odd, both $a+b$ and $c$ are odd.

Therefore $r$ is odd.

Consider $f\left(r\right)\bmod 2$.

Since $r$ is odd, $r\equiv1\pmod2$.

Therefore

$$
f\left(r\right)\equiv1+a\cdot1+b\cdot1+c=1+a+b+c\pmod2.
$$

Since $a+b$ is odd and $c$ is odd, $a+b+c$ is even.

Therefore $1+a+b+c$ is odd.

Hence $f\left(r\right)\equiv1\pmod2$, i.e. $f\left(r\right)\ne0$.

This is a contradiction.

Therefore $f\left(x\right)$ has no rational roots.

Hence $f\left(x\right)$ is irreducible over the rational number field. $\blacksquare$
