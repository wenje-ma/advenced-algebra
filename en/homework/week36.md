# week36

> **Definition 7.4.1 (Irreducible Polynomial)**<br>A polynomial $p\left(x\right)$ in $K\left[x\right]$ of positive degree is called irreducible over the number field $K$ if its only divisors in $K\left[x\right]$ are zero-degree polynomials and associates of $p\left(x\right)$.

> **Property 7.4.1 (Property of Irreducible Polynomials)**<br>In $K\left[x\right]$, if $p\left(x\right)$ is irreducible and $p\left(x\right)\mid f\left(x\right)g\left(x\right)$, then $p\left(x\right)\mid f\left(x\right)$ or $p\left(x\right)\mid g\left(x\right)$.

> **Theorem 7.4.1 (Unique Factorization Theorem)**<br>Every polynomial in $K\left[x\right]$ of positive degree can be uniquely factored into a product of finitely many irreducible polynomials over $K$.

---

## 7.4-2(2)

Factor the following polynomial into irreducible factors over the complex number field, the real number field, and the rational number field, respectively:

$$
x^{4}+4.
$$

### Solution 7.4-2(2)

By **Theorem 7.4.1 (Unique Factorization Theorem)**, every polynomial in $K\left[x\right]$ of positive degree can be uniquely factored into irreducible factors.

**Over the complex number field.**

The roots of $x^{4}+4=0$ satisfy $x^{4}=-4=4e^{i\pi}$.

Hence

$$
x=4^{1/4}e^{i\left(\pi/4+k\pi/2\right)},\ k=0,1,2,3.
$$

$4^{1/4}=\sqrt{2}$.

Thus the four roots are:

$$
x_{1}=1+i,\ x_{2}=-1+i,\ x_{3}=-1-i,\ x_{4}=1-i.
$$

Therefore

$$
x^{4}+4=\left(x-1-i\right)\left(x+1-i\right)\left(x+1+i\right)\left(x-1+i\right).
$$

**Over the real number field.**

Pair the conjugate roots:

$$
\left(x-1-i\right)\left(x-1+i\right)=\left(x-1\right)^{2}+1=x^{2}-2x+2.
$$

$$
\left(x+1-i\right)\left(x+1+i\right)=\left(x+1\right)^{2}+1=x^{2}+2x+2.
$$

Hence

$$
x^{4}+4=\left(x^{2}-2x+2\right)\left(x^{2}+2x+2\right).
$$

**Over the rational number field.**

The discriminant of $x^{2}-2x+2$ is $\Delta=4-8=-4< 0$, so it is irreducible over $\mathbb{Q}$.

The discriminant of $x^{2}+2x+2$ is $\Delta=4-8=-4< 0$, so it is irreducible over $\mathbb{Q}$.

Hence over $\mathbb{Q}$,

$$
x^{4}+4=\left(x^{2}-2x+2\right)\left(x^{2}+2x+2\right).
$$

All these factorizations are unique. $\blacksquare$

---

## 7.4-3

Prove: in $K\left[x\right]$, $g^{2}\left(x\right)\mid f^{2}\left(x\right)$ if and only if $g\left(x\right)\mid f\left(x\right)$.

### Solution 7.4-3

By **Property 7.4.1 (Property of Irreducible Polynomials)**, if $p\left(x\right)$ is irreducible and $p\left(x\right)\mid f\left(x\right)g\left(x\right)$, then $p\left(x\right)\mid f\left(x\right)$ or $p\left(x\right)\mid g\left(x\right)$.

**Necessity.** Suppose $g^{2}\mid f^{2}$; prove $g\mid f$.

Let $p$ be an irreducible factor of $g$ with multiplicity $k$.

Then $p^{2k}\mid g^{2}\mid f^{2}$.

Hence the multiplicity $m$ of $p$ in the factorization of $f$ satisfies $2m\ge2k$, i.e. $m\ge k$.

Therefore $p^{k}\mid f$.

Applying the same argument to every irreducible factor of $g$, we get $g\mid f$.

**Sufficiency.** Suppose $g\mid f$; prove $g^{2}\mid f^{2}$.

If $g\mid f$, there exists $h$ such that $f=gh$.

Hence

$$
f^{2}=g^{2}h^{2},
$$

i.e. $g^{2}\mid f^{2}$.

Thus $g^{2}\left(x\right)\mid f^{2}\left(x\right)$ if and only if $g\left(x\right)\mid f\left(x\right)$. $\blacksquare$

---

## 7.4-7

In $K\left[x\right]$, let $\left(f,g_{i}\right)=1$ for $i=1,2$. Prove: $\left(f,g_{1}g_{2}\right)=1$.

### Solution 7.4-7

Since $\left(f,g_{1}\right)=1$, there exist $u_{1},v_{1}$ such that

$$
u_{1}f+v_{1}g_{1}=1.
$$

Since $\left(f,g_{2}\right)=1$, there exist $u_{2},v_{2}$ such that

$$
u_{2}f+v_{2}g_{2}=1.
$$

Multiply the two equations:

$$
\left(u_{1}f+v_{1}g_{1}\right)\left(u_{2}f+v_{2}g_{2}\right)=1.
$$

Expanding:

$$
u_{1}u_{2}f^{2}+u_{1}v_{2}fg_{2}+v_{1}u_{2}g_{1}f+v_{1}v_{2}g_{1}g_{2}=1.
$$

The first three terms all contain $f$, so we can write:

$$
f\cdot\left(u_{1}u_{2}f+u_{1}v_{2}g_{2}+v_{1}u_{2}g_{1}\right)+v_{1}v_{2}\cdot g_{1}g_{2}=1.
$$

This shows that a linear combination of $f$ and $g_{1}g_{2}$ equals $1$.

Hence $\left(f,g_{1}g_{2}\right)=1$. $\blacksquare$
