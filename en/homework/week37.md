# Assignment 37

> **Definition 1** (Multiple Factor)<br>In $K\left[x\right]$, an irreducible polynomial $p\left(x\right)$ is called a $k$-fold factor of a polynomial $f\left(x\right)$ if $p^{k}\left(x\right)\mid f\left(x\right)$ but $p^{k+1}\left(x\right)\nmid f\left(x\right)$.

> **Theorem 3** (Criterion for Having No Multiple Factors)<br>Let $K$ be a number field. A polynomial $f\left(x\right)$ of positive degree in $K\left[x\right]$ has no multiple factors if and only if $f\left(x\right)$ and its derivative $f'\left(x\right)$ are coprime.

### Problem 1

(Problem 7.5-2) What conditions must $a,b$ satisfy for the following polynomial with real coefficients to have a multiple factor?

$$
f\left(x\right)=x^{4}+2ax^{2}+b.
$$

### Solution to Problem 1

By **Theorem 3** (Criterion for Having No Multiple Factors), $f\left(x\right)$ has no multiple factors if and only if $f\left(x\right)$ and its derivative $f'\left(x\right)$ are coprime. Compute the derivative:

$$
f'\left(x\right)=4x^{3}+4ax=4x\left(x^{2}+a\right).
$$

$f$ has a multiple factor if and only if $\left(f,f'\right)\ne1$, i.e. $f$ and $f'$ have a common factor.

The factors of $f'$ are $x$ and $x^{2}+a$.

**Case 1**: $x\mid f$.

$f\left(0\right)=b=0$.

Therefore when $b=0$, $x$ is a factor of $f$.

In this case $f=x^{2}\left(x^{2}+2a\right)$, and $x$ is a $2$-fold factor of $f$ (unless $a=0$, in which case $x$ is a $4$-fold factor).

**Case 2**: $x^{2}+a\mid f$.

Perform polynomial division:

$$
\begin{aligned}f\left(x\right)&=x^{4}+2ax^{2}+b\\
&=\left(x^{2}+a\right)^{2}+\left(b-a^{2}\right).
\end{aligned}
$$

Therefore $x^{2}+a\mid f$ if and only if $b-a^{2}=0$, i.e. $b=a^{2}$.

In this case $f=\left(x^{2}+a\right)^{2}$, and $x^{2}+a$ is a $2$-fold factor of $f$.

Combining the two cases, by **Theorem 3** (Criterion for Having No Multiple Factors), $f$ has a multiple factor if and only if

$$
b=0\text{或} b=a^{2}.
$$

$\blacksquare$

### Problem 2

(Problem 7.5-6) Find a polynomial $g\left(x\right)$ in $Q\left[x\right]$ that has no multiple factors and contains exactly the same irreducible factors as $f\left(x\right)$ (ignoring multiplicities); then find the standard factorization of $f\left(x\right)$:

$$
f\left(x\right)=x^{5}-3x^{4}+2x^{3}+2x^{2}-3x+1.
$$

### Solution to Problem 2

Compute the derivative:

$$
f'\left(x\right)=5x^{4}-12x^{3}+6x^{2}+4x-3.
$$

Use the Euclidean algorithm to find $\left(f,f'\right)$.

**Step 1**: divide $f$ by $f'$.

Leading term of the quotient: $\frac{1}{5}x$.

$$
f-\frac{1}{5}xf'=-\frac{3}{5}x^{4}+\frac{4}{5}x^{3}+\frac{6}{5}x^{2}-\frac{12}{5}x+1.
$$

Multiply by $-\frac{5}{3}$, and let

$$
r_{1}\left(x\right)=x^{4}-\frac{4}{3}x^{3}-2x^{2}+4x-\frac{5}{3}.
$$

**Step 2**: divide $f'$ by $r_{1}$.

Leading term of the quotient: $5$.

$$
f'-5r_{1}=-\frac{16}{3}x^{3}+16x^{2}-16x+\frac{16}{3}.
$$

Multiply by $-\frac{3}{16}$, and let

$$
\begin{aligned}r_{2}\left(x\right)&=x^{3}-3x^{2}+3x-1\\
&=\left(x-1\right)^{3}.
\end{aligned}
$$

**Step 3**: divide $r_{1}$ by $r_{2}$.

Leading term of the quotient: $x$.

$$
\begin{aligned}r_{1}-xr_{2}&=\frac{5}{3}x^{3}-5x^{2}+5x-\frac{5}{3}\\
&=\frac{5}{3}\left(x-1\right)^{3}\\
&=\frac{5}{3}r_{2}.
\end{aligned}
$$

Therefore

$$
r_{1}=\left(x+\frac{5}{3}\right)r_{2}.
$$

Hence

$$
\begin{aligned}\left(f,f'\right)&=r_{2}\\
&=\left(x-1\right)^{3}.
\end{aligned}
$$

The polynomial with no multiple factors:

$$
\begin{aligned}g\left(x\right)&=\frac{f\left(x\right)}{\left(f\left(x\right),f'\left(x\right)\right)}\\
&=\frac{f\left(x\right)}{\left(x-1\right)^{3}}.
\end{aligned}
$$

**Find the standard factorization**.

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

Therefore $x=1$ is a root of $f$ of multiplicity $4$.

Hence

$$
f\left(x\right)=\left(x-1\right)^{4}\left(x+a\right).
$$

Expand:

$$
\left(x-1\right)^{4}\left(x+a\right)=x^{5}+\left(a-4\right)x^{4}+\left(-4a+6\right)x^{3}+\left(6a-4\right)x^{2}+\left(-4a+1\right)x+a.
$$

Compare with

$$
f\left(x\right)=x^{5}-3x^{4}+2x^{3}+2x^{2}-3x+1
$$

Coefficients:

$$
a-4=-3\Rightarrow a=1.
$$

Verify the remaining coefficients:

$$
\begin{aligned}-4a+6&=-4+6=2,\\
6a-4&=6-4=2,\\
-4a+1&=-4+1=-3,\\
a&=1.
\end{aligned}
$$

All match.

Therefore the standard factorization is:

$$
f\left(x\right)=\left(x-1\right)^{4}\left(x+1\right).
$$

The polynomial with no multiple factors:

$$
\begin{aligned}g\left(x\right)&=\left(x-1\right)\left(x+1\right)\\
&=x^{2}-1.
\end{aligned}
$$

$\blacksquare$
