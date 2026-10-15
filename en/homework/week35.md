# Assignment 35

> **Definition 1** (Greatest Common Divisor)<br>Let $f\left(x\right),g\left(x\right)\in K\left[x\right]$, and let $d\left(x\right)$ be a common divisor of $f\left(x\right)$ and $g\left(x\right)$. If every common divisor of $f\left(x\right)$ and $g\left(x\right)$ divides $d\left(x\right)$, then $d\left(x\right)$ is called a greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$.

> **Theorem 3** (Existence of the Greatest Common Divisor and Bezout's Identity)<br>For any two polynomials $f\left(x\right)$ and $g\left(x\right)$ in $K\left[x\right]$, there exists a greatest common divisor $d\left(x\right)$ of them, and $d\left(x\right)$ can be expressed as a linear combination of $f\left(x\right)$ and $g\left(x\right)$; that is, there exist $u\left(x\right),v\left(x\right)\in K\left[x\right]$ such that
> $$
> d\left(x\right)=u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right).
> $$

> **Definition 3** (Coprime)<br>In $K\left[x\right]$, if the greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$ is a constant polynomial, then $f\left(x\right)$ and $g\left(x\right)$ are said to be coprime.

### Problem 1

(Problem 7.3-1) Find the greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$, and express $\left(f\left(x\right),g\left(x\right)\right)$ as a linear combination of $f\left(x\right)$ and $g\left(x\right)$:

(1)

$$
\begin{aligned}
f\left(x\right)&=x^{4}+3x^{3}-x^{2}-4x-3,\
g\left(x\right)&=3x^{3}+10x^{2}+2x-3.
\end{aligned}
$$

### Solution to Problem 1

By **Theorem 3** (Existence of the Greatest Common Divisor and Bezout's Identity), there exists a greatest common divisor $d\left(x\right)$, and $d\left(x\right)$ can be expressed as a linear combination of $f\left(x\right)$ and $g\left(x\right)$. Use the Euclidean algorithm.

**Step 1**: divide $f$ by $g$.

Leading term of the quotient: $\frac{1}{3}x$.

$$
f-\frac{1}{3}xg=-\frac{1}{3}x^{3}-\frac{5}{3}x^{2}-3x-3.
$$

Multiply by $-3$, and let

$$
r_{1}\left(x\right)=x^{3}+5x^{2}+9x+9.
$$

**Step 2**: divide $g$ by $r_{1}$.

Leading term of the quotient: $3$.

$$
g-3r_{1}=-5x^{2}-25x-30.
$$

Multiply by $-\frac{1}{5}$, and let $r_{2}\left(x\right)=x^{2}+5x+6$.

**Step 3**: divide $r_{1}$ by $r_{2}$.

Leading term of the quotient: $x$.

$$
r_{1}-xr_{2}=3x+9=3\left(x+3\right).
$$

**Step 4**: divide $r_{2}$ by $x+3$.

$$
r_{2}=x^{2}+5x+6=\left(x+2\right)\left(x+3\right).
$$

Therefore the last nonzero remainder is $x+3$.

$$
\left(f\left(x\right),g\left(x\right)\right)=x+3.
$$

Express as a linear combination:

From

$$
r_{2}=-\frac{1}{5}g+\frac{3}{5}r_{1}
$$

and $r_{1}=-3f+xg$, we get

$$
r_{2}=-\frac{9}{5}f+\left(\frac{3x}{5}-\frac{1}{5}\right)g.
$$

From $x+3=r_{1}-xr_{2}$, we get

$$
\begin{aligned}x+3
&=-3f+xg-x\left[-\frac{9}{5}f+\left(\frac{3x}{5}-\frac{1}{5}\right)g\right]\\
&=\frac{9x-15}{5}f+\frac{-3x^{2}+6x}{5}g.
\end{aligned}
$$

Therefore

By **Theorem 3** (Existence of the Greatest Common Divisor and Bezout's Identity),

$$
\left(f,g\right)=\frac{9x-15}{5}\cdot f\left(x\right)+\frac{-3x^{2}+6x}{5}\cdot g\left(x\right).
$$

$\blacksquare$

### Problem 2

(Problem 7.3-5) Prove: in $K\left[x\right]$, if $f\left(x\right),g\left(x\right)$ are not both zero and

$$
u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right)=\left(f\left(x\right),g\left(x\right)\right),
$$

then $\left(u\left(x\right),v\left(x\right)\right)=1$.

### Solution to Problem 2

Let $d\left(x\right)=\left(f\left(x\right),g\left(x\right)\right)$.

Then $f\left(x\right)=d\left(x\right)f_{1}\left(x\right)$, $g\left(x\right)=d\left(x\right)g_{1}\left(x\right)$, and $\left(f_{1}\left(x\right),g_{1}\left(x\right)\right)=1$.

By the hypothesis,

$$
u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right)=d\left(x\right).
$$

Divide both sides by $d\left(x\right)$:

$$
u\left(x\right)f_{1}\left(x\right)+v\left(x\right)g_{1}\left(x\right)=1.
$$

This shows that a linear combination of $u\left(x\right)$ and $v\left(x\right)$ equals $1$.

Therefore $\left(u\left(x\right),v\left(x\right)\right)=1$. $\blacksquare$

### Problem 3

(Problem 7.3-7) Let $f\left(x\right),g\left(x\right)\in K\left[x\right]$, and let $a,b,c,d\in K$ satisfy $ad-bc\ne0$. Prove:

$$
\left(af+bg,cf+dg\right)=\left(f,g\right).
$$

### Solution to Problem 3

Let $d_{1}=\left(af+bg,cf+dg\right)$, $d_{2}=\left(f,g\right)$.

Since $d_{2}\mid f$ and $d_{2}\mid g$, we have $d_{2}\mid\left(af+bg\right)$ and $d_{2}\mid\left(cf+dg\right)$.

Therefore $d_{2}\mid d_{1}$.

Conversely, since $ad-bc\ne0$, we can solve for $f,g$ in terms of $af+bg,cf+dg$:

$$
f=\frac{d}{ad-bc}\left(af+bg\right)-\frac{b}{ad-bc}\left(cf+dg\right).
$$

$$
g=-\frac{c}{ad-bc}\left(af+bg\right)+\frac{a}{ad-bc}\left(cf+dg\right).
$$

Since $d_{1}\mid\left(af+bg\right)$ and $d_{1}\mid\left(cf+dg\right)$, we have $d_{1}\mid f$ and $d_{1}\mid g$.

Therefore $d_{1}\mid d_{2}$.

Hence $d_{1}\sim d_{2}$.

Both have leading coefficient $1$, so $d_{1}=d_{2}$. $\blacksquare$

### Problem 4

(Problem 7.3-9) Prove: two nonzero polynomials $f\left(x\right)$ and $g\left(x\right)$ in $K\left[x\right]$ are not coprime if and only if there exist two nonzero polynomials $u\left(x\right),v\left(x\right)$ such that $u\left(x\right)f\left(x\right)=v\left(x\right)g\left(x\right)$, $\deg u\left(x\right)<\deg g\left(x\right)$, and $\deg v\left(x\right)<\deg f\left(x\right)$.

### Solution to Problem 4

**Necessity**. If $f$ and $g$ are not coprime, let $d\left(x\right)=\left(f,g\right)$ with $\deg d>0$.

Let

$$
u\left(x\right)=\frac{g\left(x\right)}{d\left(x\right)}, v\left(x\right)=\frac{f\left(x\right)}{d\left(x\right)}.
$$

Then

$$
u\left(x\right)f\left(x\right)=\frac{g\left(x\right)}{d\left(x\right)}\cdot f\left(x\right)=\frac{f\left(x\right)}{d\left(x\right)}\cdot g\left(x\right)=v\left(x\right)g\left(x\right).
$$

And

$$
\deg u=\deg g-\deg d<\deg g.
$$

$$
\deg v=\deg f-\deg d<\deg f.
$$

**Sufficiency**. Suppose there exist nonzero $u,v$ such that $uf=vg$, with $\deg u<\deg g$ and $\deg v<\deg f$.

Suppose, for contradiction, that $f$ and $g$ are coprime, i.e. $\left(f,g\right)=1$.

From $uf=vg$, we get $g\mid uf$.

Since $\left(f,g\right)=1$, we have $g\mid u$.

But $\deg u<\deg g$, so this forces $u=0$, a contradiction.

Therefore $f$ and $g$ are not coprime. $\blacksquare$

### Problem 5

(Problem 7.3-11) Let $A\in M_{n}\left(K\right)$, $f\left(x\right),g\left(x\right)\in K\left[x\right]$. Prove: if $d\left(x\right)$ is a greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$, then the kernel of $d\left(A\right)$ equals the intersection of the kernel of $f\left(A\right)$ and the kernel of $g\left(A\right)$.

### Solution to Problem 5

Since $d$ is a greatest common divisor of $f$ and $g$, we have $d\mid f$ and $d\mid g$.

That is, there exist $f_{1},g_{1}$ such that $f=df_{1}$, $g=dg_{1}$.

Let $X\in\ker d\left(A\right)$, i.e. $d\left(A\right)X=0$.

Then

$$
f\left(A\right)X=f_{1}\left(A\right)d\left(A\right)X=0,
$$

i.e. $X\in\ker f\left(A\right)$.

Similarly,

$$
g\left(A\right)X=g_{1}\left(A\right)d\left(A\right)X=0,
$$

i.e. $X\in\ker g\left(A\right)$.

Therefore

$$
\ker d\left(A\right)\subseteq\ker f\left(A\right)\cap\ker g\left(A\right).
$$

Conversely, let $X\in\ker f\left(A\right)\cap\ker g\left(A\right)$, i.e. $f\left(A\right)X=0$ and $g\left(A\right)X=0$.

Since $d$ is a greatest common divisor of $f$ and $g$, there exist $u,v$ such that $uf+vg=d$.

Therefore

$$
d\left(A\right)X=u\left(A\right)f\left(A\right)X+v\left(A\right)g\left(A\right)X=0+0=0.
$$

That is, $X\in\ker d\left(A\right)$.

Therefore

$$
\ker f\left(A\right)\cap\ker g\left(A\right)\subseteq\ker d\left(A\right).
$$

Hence

$$
\ker d\left(A\right)=\ker f\left(A\right)\cap\ker g\left(A\right).
$$

$\blacksquare$

### Problem 6

(Problem 7.3-12) Let $A\in M_{n}\left(K\right)$,

$$
f\left(x\right),f_{1}\left(x\right),f_{2}\left(x\right)\in K\left[x\right],
$$

and write $f\left(x\right)=f_{1}\left(x\right)f_{2}\left(x\right)$. Prove: if $\left(f_{1}\left(x\right),f_{2}\left(x\right)\right)=1$, then every solution of $f\left(A\right)X=0$ can be uniquely expressed as the sum of a solution of $f_{1}\left(A\right)X=0$ and a solution of $f_{2}\left(A\right)X=0$.

### Solution to Problem 6

**Existence**.

Since $\left(f_{1},f_{2}\right)=1$, there exist $u,v$ such that $uf_{1}+vf_{2}=1$.

Let $X$ be a solution of $f\left(A\right)X=0$, i.e. $f_{1}\left(A\right)f_{2}\left(A\right)X=0$.

Let

$$
X_{1}=v\left(A\right)f_{2}\left(A\right)X, X_{2}=u\left(A\right)f_{1}\left(A\right)X.
$$

Then

$$
X_{1}+X_{2}=\left[v\left(A\right)f_{2}\left(A\right)+u\left(A\right)f_{1}\left(A\right)\right]X=1\cdot X=X.
$$

Verify that $X_{1}\in\ker f_{1}\left(A\right)$:

$$
f_{1}\left(A\right)X_{1}=f_{1}\left(A\right)v\left(A\right)f_{2}\left(A\right)X=v\left(A\right)f_{1}\left(A\right)f_{2}\left(A\right)X=v\left(A\right)f\left(A\right)X=0.
$$

Verify that $X_{2}\in\ker f_{2}\left(A\right)$:

$$
f_{2}\left(A\right)X_{2}=f_{2}\left(A\right)u\left(A\right)f_{1}\left(A\right)X=u\left(A\right)f_{1}\left(A\right)f_{2}\left(A\right)X=u\left(A\right)f\left(A\right)X=0.
$$

**Uniqueness**.

Suppose $X=X_{1}+X_{2}=Y_{1}+Y_{2}$, where $X_{1},Y_{1}\in\ker f_{1}\left(A\right)$ and $X_{2},Y_{2}\in\ker f_{2}\left(A\right)$.

Then

$$
X_{1}-Y_{1}=Y_{2}-X_{2}.
$$

The left-hand side $\in\ker f_{1}\left(A\right)$, and the right-hand side $\in\ker f_{2}\left(A\right)$.

Let $Z=X_{1}-Y_{1}=Y_{2}-X_{2}$.

Then $f_{1}\left(A\right)Z=0$ and $f_{2}\left(A\right)Z=0$.

Since $\left(f_{1},f_{2}\right)=1$, there exist $u,v$ such that $uf_{1}+vf_{2}=1$.

Therefore

$$
Z=u\left(A\right)f_{1}\left(A\right)Z+v\left(A\right)f_{2}\left(A\right)Z=0+0=0.
$$

Hence $X_{1}=Y_{1}$ and $X_{2}=Y_{2}$.

The decomposition is unique. $\blacksquare$
