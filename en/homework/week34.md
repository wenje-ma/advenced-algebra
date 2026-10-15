# Assignment 34

> **Definition 1** (Divisibility)<br>Let $f\left(x\right),g\left(x\right)\in K\left[x\right]$. If there exists $h\left(x\right)\in K\left[x\right]$ such that $f\left(x\right)=h\left(x\right)g\left(x\right)$, then $g\left(x\right)$ is said to divide $f\left(x\right)$, denoted $g\left(x\right)\mid f\left(x\right)$.

> **Theorem 1** (Division Algorithm)<br>In $K\left[x\right]$, for any two polynomials $f\left(x\right),g\left(x\right)$ with $g\left(x\right)\ne0$, there exists a unique pair of polynomials $h\left(x\right),r\left(x\right)$ such that

$$
f\left(x\right)=h\left(x\right)g\left(x\right)+r\left(x\right),\deg r\left(x\right)<\deg g\left(x\right).
$$

### Problem 1

(Problem 7.2-3(2)) Divide $f\left(x\right)$ by $g\left(x\right)$, and find the quotient and remainder:

$$
f\left(x\right)=x^{4}+x^{3}-2x+3, g\left(x\right)=3x^{2}-x+2.
$$

### Solution to Problem 1

By **Theorem 1** (Division Algorithm), in $K\left[x\right]$, for any two polynomials $f\left(x\right),g\left(x\right)$ with $g\left(x\right)\ne0$, there exists a unique pair of polynomials $h\left(x\right),r\left(x\right)$ such that $f\left(x\right)=h\left(x\right)g\left(x\right)+r\left(x\right)$. Perform polynomial long division:

$$
f\left(x\right)=x^{4}+x^{3}+0x^{2}-2x+3.
$$

Leading term of the quotient: $x^{4}/3x^{2}=\frac{1}{3}x^{2}$.

$$
\frac{1}{3}x^{2}\cdot g\left(x\right)=x^{4}-\frac{1}{3}x^{3}+\frac{2}{3}x^{2}.
$$

Remainder:

$$
f-\frac{1}{3}x^{2}g=\frac{4}{3}x^{3}-\frac{2}{3}x^{2}-2x+3.
$$

Second term of the quotient: $\frac{4}{3}x^{3}/3x^{2}=\frac{4}{9}x$.

$$
\frac{4}{9}x\cdot g=\frac{4}{3}x^{3}-\frac{4}{9}x^{2}+\frac{8}{9}x.
$$

Remainder:

$$
-\frac{2}{9}x^{2}-\frac{26}{9}x+3.
$$

Third term of the quotient: $-\frac{2}{9}x^{2}/3x^{2}=-\frac{2}{27}$.

$$
-\frac{2}{27}\cdot g=-\frac{2}{9}x^{2}+\frac{2}{27}x-\frac{4}{27}.
$$

Remainder:

$$
-\frac{80}{27}x+\frac{85}{27}.
$$

Therefore

By **Theorem 1** (Division Algorithm),

$$
\text{商式 }h\left(x\right)=\frac{1}{3}x^{2}+\frac{4}{9}x-\frac{2}{27}.
$$

$$
\text{余式 }r\left(x\right)=-\frac{80}{27}x+\frac{85}{27}.
$$

$\blacksquare$

### Problem 2

(Problem 7.2-4) Let

$$
f\left(x\right)=x^{3}-3x^{2}+ax+a_{0},
$$

$g\left(x\right)=x^{2}-3x+1$. Find the necessary and sufficient condition for $g\left(x\right)$ to divide $f\left(x\right)$.

### Solution to Problem 2

Divide $f\left(x\right)$ by $g\left(x\right)$:

Leading term of the quotient: $x^{3}/x^{2}=x$.

$$
x\cdot g\left(x\right)=x^{3}-3x^{2}+x.
$$

Remainder:

$$
f-x\cdot g=\left(a-1\right)x+a_{0}.
$$

The degree of the remainder is $<2$, so stop.

Therefore $g\left(x\right)\mid f\left(x\right)$ if and only if the remainder is zero, i.e.

$$
\left(a-1\right)x+a_{0}=0.
$$

This holds for all $x$ if and only if

$$
a-1=0, a_{0}=0.
$$

Hence the necessary and sufficient condition is $a=1$, $a_{0}=0$. $\blacksquare$

### Problem 3

(Problem 7.2-5) Use synthetic division to find the quotient and remainder when a linear polynomial $g\left(x\right)$ divides $f\left(x\right)$.

(1)

$$
f\left(x\right)=3x^{4}-5x^{2}+2x-1,
$$

$g\left(x\right)=x-4$;

(2) $f\left(x\right)=5x^{3}-3x+4$, $g\left(x\right)=x+2$.

### Solution to Problem 3

**(1)** Synthetic division:

$$
\begin{array}{r|rrrrr}
4 & 3 & 0 & -5 & 2 & -1\\
  &   & 12 & 48 & 172 & 776\\
\hline
  & 3 & 12 & 43 & 174 & 775
\end{array}
$$

Therefore

$$
\text{商式 }h\left(x\right)=3x^{3}+12x^{2}+43x+174.
$$

$$
\text{余式 }r\left(x\right)=775.
$$

**(2)** Synthetic division:

$$
\begin{array}{r|rrrr}
-2 & 5 & 0 & -3 & 4\\
   &   & -10 & 20 & -34\\
\hline
   & 5 & -10 & 17 & -30
\end{array}
$$

Therefore

$$
\text{商式 }h\left(x\right)=5x^{2}-10x+17.
$$

$$
\text{余式 }r\left(x\right)=-30.
$$

$\blacksquare$
