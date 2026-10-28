# week40

> **Definition 7.8.1 (Primitive Polynomial)**<br>A nonzero polynomial with integer coefficients is called primitive if the greatest common divisor of its coefficients is $1$.

> **Lemma 7.8.1 (Gauss Lemma)**<br>The product of two primitive polynomials is again primitive.

> **Theorem 7.8.1 (Eisenstein Criterion)**<br>Let

$$
f\left(x\right)=a_{n}x^{n}+\cdots+a_{1}x+a_{0}
$$

be a polynomial with integer coefficients of degree $n> 0$. If there exists a prime $p$ such that (1) $p\mid a_{i}$ for $i=0,1,\ldots,n-1$; (2) $p\nmid a_{n}$; (3) $p^{2}\nmid a_{0}$, then $f\left(x\right)$ is irreducible over $\mathbb{Q}$.

---

## 7.8-2(4)

Is $x^{4}-2x^{3}+2x-3$ irreducible over $\mathbb{Q}$?

### Solution 7.8-2(4)

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

---

## 7.8-2(5)

Is $x^{4}+px^{2}+1$ (where $p$ is an odd prime) irreducible over $\mathbb{Q}$?

### Solution 7.8-2(5)

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

**Case 1**: $a=0$.

Then $c=0$.

From $\left(2\right)$: $b+d=p$.

From $\left(4\right)$: $bd=1$.

Thus $b=d=1$ or $b=d=-1$.

If $b=d=1$, then $b+d=2$, so $p=2$. But $p$ is odd, contradiction.

If $b=d=-1$, then $b+d=-2$, so $p=-2$. But $p$ is a positive prime, contradiction.

**Case 2**: $d=b$.

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

---

## 7.8-2(7)

Is $2x^{3}-x^{2}+x+1$ irreducible over $\mathbb{Q}$?

### Solution 7.8-2(7)

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

---

## 7.8-2(8)

Is $x^{4}-5x^{2}+1$ irreducible over $\mathbb{Q}$?

### Solution 7.8-2(8)

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

**Case 1**: $a=0$.

Then $c=0$.

From $\left(2\right)$: $b+d=-5$.

From $\left(4\right)$: $bd=1$.

Thus $b,d$ are roots of $t^{2}+5t+1=0$, not integers.

**Case 2**: $d=b$.

From $\left(4\right)$: $b^{2}=1$, so $b=1$ or $b=-1$.

If $b=1$, then $d=1$.

From $\left(2\right)$: $-a^{2}+2=-5\Rightarrow a^{2}=7$, not a perfect square.

If $b=-1$, then $d=-1$.

From $\left(2\right)$: $-a^{2}-2=-5\Rightarrow a^{2}=3$, not a perfect square.

Hence it cannot be factored into two integer quadratics.

Therefore $x^{4}-5x^{2}+1$ is irreducible over $\mathbb{Q}$. $\blacksquare$

---

## 7.8-5

Let $f\left(x\right)$ be a monic polynomial with integer coefficients of positive degree. Prove: if $f\left(0\right)$ and $f\left(1\right)$ are both odd, then $f\left(x\right)$ has no rational root.

### Solution 7.8-5

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

---

## 7.8-6

Let

$$
f\left(x\right)=x^{3}+ax^{2}+bx+c
$$

be a polynomial with integer coefficients. Prove: if $\left(a+b\right)c$ is odd, then $f\left(x\right)$ is irreducible over $\mathbb{Q}$.

### Solution 7.8-6

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
