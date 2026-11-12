# week22

> **Definition 7.3.1 (Greatest Common Divisor)**
> 
> Let $f\left(x\right),g\left(x\right)\in{K}\left[x\right]$, and let $d\left(x\right)$ be a common divisor of $f\left(x\right)$ and $g\left(x\right)$. If every common divisor of $f\left(x\right)$ and $g\left(x\right)$ divides $d\left(x\right)$, then $d\left(x\right)$ is called a greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$.

> **Theorem 7.3.1 (Existence of the Greatest Common Divisor and Bezout Identity)**
> 
> For any two polynomials $f\left(x\right)$ and $g\left(x\right)$ in $K\left[x\right]$, there exists a greatest common divisor $d\left(x\right)$, and $d\left(x\right)$ can be expressed as a linear combination of $f\left(x\right)$ and $g\left(x\right)$, i.e. there exist $u\left(x\right),v\left(x\right)\in{K}\left[x\right]$ such that

> **Definition 7.3.2 (Coprime)**
> 
> In $K\left[x\right]$, if the greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$ is a zero-degree polynomial, then $f\left(x\right)$ and $g\left(x\right)$ are said to be coprime.

> **Definition 7.4.1 (Irreducible Polynomial)**
> 
> A polynomial $p\left(x\right)$ in $K\left[x\right]$ of positive degree is called irreducible over the number field $K$ if its only divisors in $K\left[x\right]$ are zero-degree polynomials and associates of $p\left(x\right)$.

> **Theorem 7.4.1 (Unique Factorization Theorem)**
> 
> Every polynomial in $K\left[x\right]$ of positive degree can be uniquely factored into a product of finitely many irreducible polynomials over $K$.

> **Property 7.4.1 (Property of Irreducible Polynomials)**
> 
> In $K\left[x\right]$, if $p\left(x\right)$ is irreducible and $p\left(x\right)\mid{f}\left(x\right)g\left(x\right)$, then $p\left(x\right)\mid{f}\left(x\right)$ or $p\left(x\right)\mid{g}\left(x\right)$.

> **Definition 7.5.1 (Multiple Factor)**
> 
> In $K\left[x\right]$, an irreducible polynomial $p\left(x\right)$ is called a $k$-fold factor of $f\left(x\right)$ if $p^{k}\left(x\right)\mid{f}\left(x\right)$ but $p^{k+1}\left(x\right)\nmid{f}\left(x\right)$.

> **Theorem 7.5.1 (Criterion for No Multiple Factors)**
> 
> Let $K$ be a number field. A polynomial $f\left(x\right)$ of positive degree in $K\left[x\right]$ has no multiple factors if and only if $f\left(x\right)$ is coprime to its derivative $f'\left(x\right)$.

## 7.3-12

Let $A\in{M}_{n}\left(K\right)$,

$$
f\left(x\right),f_{1}\left(x\right),f_{2}\left(x\right)\in{K}\left[x\right],
$$

and write $f\left(x\right)=f_{1}\left(x\right)f_{2}\left(x\right)$. Prove: if $\left(f_{1}\left(x\right),f_{2}\left(x\right)\right)=1$, then every solution of $f\left(A\right)X=0$ can be uniquely expressed as the sum of a solution of $f_{1}\left(A\right)X=0$ and a solution of $f_{2}\left(A\right)X=0$.

### Solution to 7.3-12

Existence.

Since $\left(f_{1},f_{2}\right)=1$, there exist $u,v$ such that $uf_{1}+vf_{2}=1$.

Let $X$ be a solution of $f\left(A\right)X=0$, i.e. $f_{1}\left(A\right)f_{2}\left(A\right)X=0$.

Set

$$
X_{1}=v\left(A\right)f_{2}\left(A\right)X,\quad{X}_{2}=u\left(A\right)f_{1}\left(A\right)X.
$$

Then

$$
X_{1}+X_{2}=\left[v\left(A\right)f_{2}\left(A\right)+u\left(A\right)f_{1}\left(A\right)\right]X=1\cdot{X}=X.
$$

Verify $X_{1}\in\ker{f}_{1}\left(A\right)$:

$$
f_{1}\left(A\right)X_{1}=f_{1}\left(A\right)v\left(A\right)f_{2}\left(A\right)X=v\left(A\right)f_{1}\left(A\right)f_{2}\left(A\right)X=v\left(A\right)f\left(A\right)X=0.
$$

Verify $X_{2}\in\ker{f}_{2}\left(A\right)$:

$$
f_{2}\left(A\right)X_{2}=f_{2}\left(A\right)u\left(A\right)f_{1}\left(A\right)X=u\left(A\right)f_{1}\left(A\right)f_{2}\left(A\right)X=u\left(A\right)f\left(A\right)X=0.
$$

Uniqueness.

Suppose $X=X_{1}+X_{2}=Y_{1}+Y_{2}$, where $X_{1},Y_{1}\in\ker{f}_{1}\left(A\right)$ and $X_{2},Y_{2}\in\ker{f}_{2}\left(A\right)$.

Then

$$
X_{1}-Y_{1}=Y_{2}-X_{2}.
$$

The left side $\in\ker{f}_{1}\left(A\right)$, the right side $\in\ker{f}_{2}\left(A\right)$.

Set $Z=X_{1}-Y_{1}=Y_{2}-X_{2}$.

Then $f_{1}\left(A\right)Z=0$ and $f_{2}\left(A\right)Z=0$.

Since $\left(f_{1},f_{2}\right)=1$, there exist $u,v$ such that $uf_{1}+vf_{2}=1$.

Therefore

$$
Z=u\left(A\right)f_{1}\left(A\right)Z+v\left(A\right)f_{2}\left(A\right)Z=0+0=0.
$$

Hence $X_{1}=Y_{1}$ and $X_{2}=Y_{2}$.

The decomposition is unique.

$\blacksquare$

## 7.4-2(2)

Factor the following polynomial into irreducible factors over the complex number field, the real number field, and the rational number field, respectively:

$$
x^{4}+4.
$$

### Solution to 7.4-2(2)

By **Theorem 7.4.1 (Unique Factorization Theorem)**, every polynomial in $K\left[x\right]$ of positive degree can be uniquely factored into irreducible factors.

Over the complex number field.

The roots of $x^{4}+4=0$ satisfy $x^{4}=-4=4e^{i\pi}$.

Hence

$$
x=4^{1/4}e^{i\left(\pi/4+k\pi/2\right)},k=0,1,2,3.
$$

$4^{1/4}=\sqrt{2}$.

Thus the four roots are:

$$
x_{1}=1+i,x_{2}=-1+i,x_{3}=-1-i,x_{4}=1-i.
$$

Therefore

$$
x^{4}+4=\left(x-1-i\right)\left(x+1-i\right)\left(x+1+i\right)\left(x-1+i\right).
$$

Over the real number field.

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

Over the rational number field.

The discriminant of $x^{2}-2x+2$ is $\Delta=4-8=-4<0$, so it is irreducible over $\mathbb{Q}$.

The discriminant of $x^{2}+2x+2$ is $\Delta=4-8=-4<0$, so it is irreducible over $\mathbb{Q}$.

Hence over $\mathbb{Q}$,

$$
x^{4}+4=\left(x^{2}-2x+2\right)\left(x^{2}+2x+2\right).
$$

All these factorizations are unique.

$\blacksquare$

## 7.4-3

Prove: in $K\left[x\right]$, $g^{2}\left(x\right)\mid{f}^{2}\left(x\right)$ if and only if $g\left(x\right)\mid{f}\left(x\right)$.

### Solution to 7.4-3

By **Property 7.4.1 (Property of Irreducible Polynomials)**, if $p\left(x\right)$ is irreducible and $p\left(x\right)\mid{f}\left(x\right)g\left(x\right)$, then $p\left(x\right)\mid{f}\left(x\right)$ or $p\left(x\right)\mid{g}\left(x\right)$.

Necessity. Suppose $g^{2}\mid{f}^{2}$; prove $g\mid{f}$.

Let $p$ be an irreducible factor of $g$ with multiplicity $k$.

Then $p^{2k}\mid{g}^{2}\mid{f}^{2}$.

Hence the multiplicity $m$ of $p$ in the factorization of $f$ satisfies $2m\ge2k$, i.e. $m\ge{k}$.

Therefore $p^{k}\mid{f}$.

Applying the same argument to every irreducible factor of $g$, we get $g\mid{f}$.

Sufficiency. Suppose $g\mid{f}$; prove $g^{2}\mid{f}^{2}$.

If $g\mid{f}$, there exists $h$ such that $f=gh$.

Hence

$$
f^{2}=g^{2}h^{2},
$$

i.e. $g^{2}\mid{f}^{2}$.

Thus $g^{2}\left(x\right)\mid{f}^{2}\left(x\right)$ if and only if $g\left(x\right)\mid{f}\left(x\right)$.

$\blacksquare$

## 7.4-7

In $K\left[x\right]$, let $\left(f,g_{i}\right)=1$ for $i=1,2$. Prove: $\left(f,g_{1}g_{2}\right)=1$.

### Solution to 7.4-7

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
f\cdot\left(u_{1}u_{2}f+u_{1}v_{2}g_{2}+v_{1}u_{2}g_{1}\right)+v_{1}v_{2}\cdot{g}_{1}g_{2}=1.
$$

This shows that a linear combination of $f$ and $g_{1}g_{2}$ equals $1$.

Hence $\left(f,g_{1}g_{2}\right)=1$.

$\blacksquare$

## 7.5-2

What conditions should $a,b$ satisfy for the following real-coefficient polynomial to have multiple factors:

$$
f\left(x\right)=x^{4}+2ax^{2}+b.
$$

### Solution to 7.5-2

By **Theorem 7.5.1 (Criterion for No Multiple Factors)**, $f\left(x\right)$ has no multiple factors if and only if $f\left(x\right)$ is coprime to its derivative $f'\left(x\right)$. Compute the derivative:

$$
f'\left(x\right)=4x^{3}+4ax=4x\left(x^{2}+a\right).
$$

$f$ has a multiple factor if and only if $\left(f,f'\right)\ne1$, i.e. $f$ and $f'$ have a common factor.

The factors of $f'$ are $x$ and $x^{2}+a$.

Case 1: $x\mid{f}$.

$f\left(0\right)=b=0$.

Hence when $b=0$, $x$ is a factor of $f$.

Then $f=x^{2}\left(x^{2}+2a\right)$, and $x$ is a double factor of $f$ (unless $a=0$, in which case $x$ is a quadruple factor).

Case 2: $x^{2}+a\mid{f}$.

Perform polynomial division:

$$
f\left(x\right)=x^{4}+2ax^{2}+b=\left(x^{2}+a\right)^{2}+\left(b-a^{2}\right).
$$

Hence $x^{2}+a\mid{f}$ if and only if $b-a^{2}=0$, i.e. $b=a^{2}$.

Then $f=\left(x^{2}+a\right)^{2}$, and $x^{2}+a$ is a double factor of $f$.

Combining the two cases, by **Theorem 7.5.1 (Criterion for No Multiple Factors)**, $f$ has a multiple factor if and only if

$$
b=0\text{~or~}b=a^{2}.
$$

$\blacksquare$

## 7.5-6

In $\mathbb{Q}\left[x\right]$, find a polynomial $g\left(x\right)$ with no multiple factors that contains exactly the same irreducible factors as $f\left(x\right)$ (ignoring multiplicity); then find the standard factorization of $f\left(x\right)$:

$$
f\left(x\right)=x^{5}-3x^{4}+2x^{3}+2x^{2}-3x+1.
$$

### Solution to 7.5-6

Compute the derivative:

$$
f'\left(x\right)=5x^{4}-12x^{3}+6x^{2}+4x-3.
$$

Use the Euclidean algorithm to find $\left(f,f'\right)$.

Step 1: Divide $f$ by $f'$.

Leading term of the quotient: $\frac{1}{5}x$.

$$
f-\frac{1}{5}xf'=-\frac{3}{5}x^{4}+\frac{4}{5}x^{3}+\frac{6}{5}x^{2}-\frac{12}{5}x+1.
$$

Multiply by $-\frac{5}{3}$ and set

$$
r_{1}\left(x\right)=x^{4}-\frac{4}{3}x^{3}-2x^{2}+4x-\frac{5}{3}.
$$

Step 2: Divide $f'$ by $r_{1}$.

Leading term of the quotient: $5$.

$$
f'-5r_{1}=-\frac{16}{3}x^{3}+16x^{2}-16x+\frac{16}{3}.
$$

Multiply by $-\frac{3}{16}$ and set

$$
r_{2}\left(x\right)=x^{3}-3x^{2}+3x-1=\left(x-1\right)^{3}.
$$

Step 3: Divide $r_{1}$ by $r_{2}$.

Leading term of the quotient: $x$.

$$
r_{1}-xr_{2}=\frac{5}{3}x^{3}-5x^{2}+5x-\frac{5}{3}=\frac{5}{3}\left(x-1\right)^{3}=\frac{5}{3}r_{2}.
$$

Hence

$$
r_{1}=\left(x+\frac{5}{3}\right)r_{2}.
$$

Therefore

$$
\left(f,f'\right)=r_{2}=\left(x-1\right)^{3}.
$$

The polynomial with no multiple factors:

$$
g\left(x\right)=\frac{f\left(x\right)}{\left(f\left(x\right),f'\left(x\right)\right)}=\frac{f\left(x\right)}{\left(x-1\right)^{3}}.
$$

Find the standard factorization.

Compute $f\left(1\right)$:

$$
f\left(1\right)=1-3+2+2-3+1=0.
$$

Compute $f'\left(1\right)$:

$$
f'\left(1\right)=5-12+6+4-3=0.
$$

Compute $f''\left(x\right)$:

$$
f''\left(x\right)=20x^{3}-36x^{2}+12x+4.
$$

$$
f''\left(1\right)=20-36+12+4=0.
$$

Compute $f'''\left(x\right)$:

$$
f'''\left(x\right)=60x^{2}-72x+12.
$$

$$
f'''\left(1\right)=60-72+12=0.
$$

Compute $f''''\left(x\right)$:

$$
f''''\left(x\right)=120x-72.
$$

$$
f''''\left(1\right)=120-72=48\ne0.
$$

Hence $x=1$ is a quadruple root of $f$.

Therefore

$$
f\left(x\right)=\left(x-1\right)^{4}\left(x+a\right).
$$

Expand:

$$
\left(x-1\right)^{4}\left(x+a\right)=x^{5}+\left(a-4\right)x^{4}+\left(-4a+6\right)x^{3}+\left(6a-4\right)x^{2}+\left(-4a+1\right)x+a.
$$

Compare with

$$
f\left(x\right)=x^{5}-3x^{4}+2x^{3}+2x^{2}-3x+1.
$$

$$
a-4=-3\Rightarrow{a}=1.
$$

Verify the other coefficients:

$$
-4a+6=-4+6=2,\quad6a-4=6-4=2,\quad-4a+1=-4+1=-3,\quad{a}=1.
$$

All match.

Hence the standard factorization:

$$
f\left(x\right)=\left(x-1\right)^{4}\left(x+1\right).
$$

The polynomial with no multiple factors:

$$
g\left(x\right)=\left(x-1\right)\left(x+1\right)=x^{2}-1.
$$

$\blacksquare$
