# week21

> **Definition 7.2.1 (Divisibility)**
> 
> Let $f\left(x\right),g\left(x\right)\in{K}\left[x\right]$. If there exists $h\left(x\right)\in{K}\left[x\right]$ such that $f\left(x\right)=h\left(x\right)g\left(x\right)$, then $g\left(x\right)$ divides $f\left(x\right)$, written $g\left(x\right)\mid{f}\left(x\right)$.

> **Theorem 7.2.1 (Division with Remainder)**
> 
> In $K\left[x\right]$, for any two polynomials $f\left(x\right),g\left(x\right)$ with $g\left(x\right)\ne0$, there exists a unique pair of polynomials $h\left(x\right),r\left(x\right)$ such that

> **Definition 7.3.1 (Greatest Common Divisor)**
> 
> Let $f\left(x\right),g\left(x\right)\in{K}\left[x\right]$, and let $d\left(x\right)$ be a common divisor of $f\left(x\right)$ and $g\left(x\right)$. If every common divisor of $f\left(x\right)$ and $g\left(x\right)$ divides $d\left(x\right)$, then $d\left(x\right)$ is called a greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$.

> **Theorem 7.3.1 (Existence of the Greatest Common Divisor and Bezout Identity)**
> 
> For any two polynomials $f\left(x\right)$ and $g\left(x\right)$ in $K\left[x\right]$, there exists a greatest common divisor $d\left(x\right)$, and $d\left(x\right)$ can be expressed as a linear combination of $f\left(x\right)$ and $g\left(x\right)$, i.e. there exist $u\left(x\right),v\left(x\right)\in{K}\left[x\right]$ such that

$$
d\left(x\right)=u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right).
$$

> **Definition 7.3.2 (Coprime)**
> 
> In $K\left[x\right]$, if the greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$ is a zero-degree polynomial, then $f\left(x\right)$ and $g\left(x\right)$ are said to be coprime.

## 7.2-4

Let

$$
f\left(x\right)=x^{3}-3x^{2}+ax+a_{0},
$$

$g\left(x\right)=x^{2}-3x+1$. Find the necessary and sufficient condition for $g\left(x\right)$ to divide $f\left(x\right)$.

### Solution to 7.2-4

Divide $f\left(x\right)$ by $g\left(x\right)$:

Leading term of the quotient: $x^{3}/x^{2}=x$.

$$
x\cdot{g}\left(x\right)=x^{3}-3x^{2}+x.
$$

Remainder:

$$
f-x\cdot{g}=\left(a-1\right)x+a_{0}.
$$

The degree of the remainder is $<2$, so stop.

Therefore $g\left(x\right)\mid{f}\left(x\right)$ if and only if the remainder is zero, i.e.

$$
\left(a-1\right)x+a_{0}=0.
$$

This holds for all $x$ if and only if

$$
a-1=0,\quad{a}_{0}=0.
$$

Hence the necessary and sufficient condition is $a=1$, $a_{0}=0$. $\blacksquare$

## 7.2-5

Use synthetic division to find the quotient and remainder when $f\left(x\right)$ is divided by the linear polynomial $g\left(x\right)$.

(1)

$$
f\left(x\right)=3x^{4}-5x^{2}+2x-1,
$$

$g\left(x\right)=x-4$;

(2) $f\left(x\right)=5x^{3}-3x+4$, $g\left(x\right)=x+2$.

### Solution to 7.2-5

(1) Synthetic division:

$$
\begin{array}{r|rrrrr}
4&3&0&-5&2&-1\\
&&12&48&172&776\\
\hline
&3&12&43&174&775
\end{array}
$$

Therefore

$$
\text{quotient~}h\left(x\right)=3x^{3}+12x^{2}+43x+174.
$$

$$
\text{remainder~}r\left(x\right)=775.
$$

(2) Synthetic division:

$$
\begin{array}{r|rrrr}
-2&5&0&-3&4\\
&&-10&20&-34\\
\hline
&5&-10&17&-30
\end{array}
$$

Therefore

$$
\text{quotient~}h\left(x\right)=5x^{2}-10x+17.
$$

$$
\text{remainder~}r\left(x\right)=-30.
$$

$\blacksquare$

## 7.3-1(1)

Find the greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$, and express $\left(f\left(x\right),g\left(x\right)\right)$ as a linear combination of $f\left(x\right)$ and $g\left(x\right)$:

$$
f\left(x\right)=x^{4}+3x^{3}-x^{2}-4x-3,\quad{g}\left(x\right)=3x^{3}+10x^{2}+2x-3.
$$

### Solution to 7.3-1(1)

By **Theorem 7.3.1 (Existence of the Greatest Common Divisor and Bezout Identity)**, there is a greatest common divisor $d\left(x\right)$, and it can be expressed as a linear combination. Use the Euclidean algorithm.

Step 1: Divide $f$ by $g$.

Leading term of the quotient: $\frac{1}{3}x$.

$$
f-\frac{1}{3}xg=-\frac{1}{3}x^{3}-\frac{5}{3}x^{2}-3x-3.
$$

Multiply by $-3$ and set

$$
r_{1}\left(x\right)=x^{3}+5x^{2}+9x+9.
$$

Step 2: Divide $g$ by $r_{1}$.

Leading term of the quotient: $3$.

$$
g-3r_{1}=-5x^{2}-25x-30.
$$

Multiply by $-\frac{1}{5}$ and set $r_{2}\left(x\right)=x^{2}+5x+6$.

Step 3: Divide $r_{1}$ by $r_{2}$.

Leading term of the quotient: $x$.

$$
r_{1}-xr_{2}=3x+9=3\left(x+3\right).
$$

Step 4: Divide $r_{2}$ by $x+3$.

$$
r_{2}=x^{2}+5x+6=\left(x+2\right)\left(x+3\right).
$$

Hence the last nonzero remainder is $x+3$.

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

From $x+3=r_{1}-xr_{2}$,

$$
x+3
=-3f+xg-x\left[-\frac{9}{5}f+\left(\frac{3x}{5}-\frac{1}{5}\right)g\right]=\frac{9x-15}{5}f+\frac{-3x^{2}+6x}{5}g.
$$

Therefore, by **Theorem 7.3.1 (Existence of the Greatest Common Divisor and Bezout Identity)**,

$$
\left(f,g\right)=\frac{9x-15}{5}\cdot{f}\left(x\right)+\frac{-3x^{2}+6x}{5}\cdot{g}\left(x\right).
$$

$\blacksquare$

## 7.3-5

Prove: in $K\left[x\right]$, if $f\left(x\right),g\left(x\right)$ are not both zero and

$$
u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right)=\left(f\left(x\right),g\left(x\right)\right),
$$

then $\left(u\left(x\right),v\left(x\right)\right)=1$.

### Solution to 7.3-5

Set $d\left(x\right)=\left(f\left(x\right),g\left(x\right)\right)$.

Then $f\left(x\right)=d\left(x\right)f_{1}\left(x\right)$, $g\left(x\right)=d\left(x\right)g_{1}\left(x\right)$, and $\left(f_{1}\left(x\right),g_{1}\left(x\right)\right)=1$.

By assumption,

$$
u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right)=d\left(x\right).
$$

Divide by $d\left(x\right)$:

$$
u\left(x\right)f_{1}\left(x\right)+v\left(x\right)g_{1}\left(x\right)=1.
$$

This shows that a linear combination of $u\left(x\right)$ and $v\left(x\right)$ equals $1$.

Hence $\left(u\left(x\right),v\left(x\right)\right)=1$. $\blacksquare$

## 7.3-7

Let $f\left(x\right),g\left(x\right)\in{K}\left[x\right]$, and let $a,b,c,d\in{K}$ with $ad-bc\ne0$. Prove:

$$
\left(af+bg,cf+dg\right)=\left(f,g\right).
$$

### Solution to 7.3-7

Set $d_{1}=\left(af+bg,cf+dg\right)$, $d_{2}=\left(f,g\right)$.

Since $d_{2}\mid{f}$ and $d_{2}\mid{g}$, we have $d_{2}\mid\left(af+bg\right)$ and $d_{2}\mid\left(cf+dg\right)$.

Hence $d_{2}\mid{d}_{1}$.

Conversely, since $ad-bc\ne0$, we can solve for $f,g$ in terms of $af+bg,cf+dg$:

$$
f=\frac{d}{ad-bc}\left(af+bg\right)-\frac{b}{ad-bc}\left(cf+dg\right).
$$

$$
g=-\frac{c}{ad-bc}\left(af+bg\right)+\frac{a}{ad-bc}\left(cf+dg\right).
$$

Since $d_{1}\mid\left(af+bg\right)$ and $d_{1}\mid\left(cf+dg\right)$, we have $d_{1}\mid{f}$ and $d_{1}\mid{g}$.

Hence $d_{1}\mid{d}_{2}$.

Therefore $d_{1}\sim{d}_{2}$.

Both are monic, so $d_{1}=d_{2}$. $\blacksquare$

## 7.3-9

Prove: two nonzero polynomials $f\left(x\right)$ and $g\left(x\right)$ in $K\left[x\right]$ are not coprime if and only if there exist two nonzero polynomials $u\left(x\right),v\left(x\right)$ such that $u\left(x\right)f\left(x\right)=v\left(x\right)g\left(x\right)$, $\deg{u}\left(x\right)<\deg{g}\left(x\right)$, $\deg{v}\left(x\right)<\deg{f}\left(x\right)$.

### Solution to 7.3-9

Necessity. If $f$ and $g$ are not coprime, set $d\left(x\right)=\left(f,g\right)$ with $\deg{d}>0$.

Set

$$
u\left(x\right)=\frac{g\left(x\right)}{d\left(x\right)},\quad{v}\left(x\right)=\frac{f\left(x\right)}{d\left(x\right)}.
$$

Then

$$
u\left(x\right)f\left(x\right)=\frac{g\left(x\right)}{d\left(x\right)}\cdot{f}\left(x\right)=\frac{f\left(x\right)}{d\left(x\right)}\cdot{g}\left(x\right)=v\left(x\right)g\left(x\right).
$$

And

$$
\deg{u}=\deg{g}-\deg{d}<\deg{g}.
$$

$$
\deg{v}=\deg{f}-\deg{d}<\deg{f}.
$$

Sufficiency. Suppose there exist nonzero $u,v$ such that $uf=vg$, with $\deg{u}<\deg{g}$ and $\deg{v}<\deg{f}$.

Assume $f$ and $g$ are coprime, i.e. $\left(f,g\right)=1$.

From $uf=vg$, we get $g\mid{u}f$.

Since $\left(f,g\right)=1$, we have $g\mid{u}$.

But $\deg{u}<\deg{g}$, so $u=0$, a contradiction.

Therefore $f$ and $g$ are not coprime. $\blacksquare$

## 7.3-11

Let $A\in{M}_{n}\left(K\right)$, $f\left(x\right),g\left(x\right)\in{K}\left[x\right]$. Prove: if $d\left(x\right)$ is a greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$, then the kernel of $d\left(A\right)$ equals the intersection of the kernels of $f\left(A\right)$ and $g\left(A\right)$.

### Solution to 7.3-11

Since $d$ is the greatest common divisor of $f$ and $g$, we have $d\mid{f}$ and $d\mid{g}$.

That is, there exist $f_{1},g_{1}$ such that $f=df_{1}$, $g=dg_{1}$.

Let $X\in\ker{d}\left(A\right)$, i.e. $d\left(A\right)X=0$.

Then

$$
f\left(A\right)X=f_{1}\left(A\right)d\left(A\right)X=0,
$$

i.e. $X\in\ker{f}\left(A\right)$.

Similarly,

$$
g\left(A\right)X=g_{1}\left(A\right)d\left(A\right)X=0,
$$

i.e. $X\in\ker{g}\left(A\right)$.

Therefore

$$
\ker{d}\left(A\right)\subseteq\ker{f}\left(A\right)\cap\ker{g}\left(A\right).
$$

Conversely, let $X\in\ker{f}\left(A\right)\cap\ker{g}\left(A\right)$, i.e. $f\left(A\right)X=0$ and $g\left(A\right)X=0$.

Since $d$ is the greatest common divisor of $f$ and $g$, there exist $u,v$ such that $uf+vg=d$.

Therefore

$$
d\left(A\right)X=u\left(A\right)f\left(A\right)X+v\left(A\right)g\left(A\right)X=0+0=0.
$$

i.e. $X\in\ker{d}\left(A\right)$.

Therefore

$$
\ker{f}\left(A\right)\cap\ker{g}\left(A\right)\subseteq\ker{d}\left(A\right).
$$

Hence

$$
\ker{d}\left(A\right)=\ker{f}\left(A\right)\cap\ker{g}\left(A\right).
$$

$\blacksquare$
