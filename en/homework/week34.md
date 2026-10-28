# week34

> **Definition 7.2.1 (Divisibility)**<br>Let $f\left(x\right),g\left(x\right)\in K\left[x\right]$. If there exists $h\left(x\right)\in K\left[x\right]$ such that $f\left(x\right)=h\left(x\right)g\left(x\right)$, then $g\left(x\right)$ divides $f\left(x\right)$, written $g\left(x\right)\mid f\left(x\right)$.

> **Theorem 7.2.1 (Division with Remainder)**<br>In $K\left[x\right]$, for any two polynomials $f\left(x\right),g\left(x\right)$ with $g\left(x\right)\ne0$, there exists a unique pair of polynomials $h\left(x\right),r\left(x\right)$ such that

$$
f\left(x\right)=h\left(x\right)g\left(x\right)+r\left(x\right),\deg r\left(x\right)< \deg g\left(x\right).
$$

---

## 7.2-3(2)

Divide $f\left(x\right)$ by $g\left(x\right)$ and find the quotient and remainder:

$$
f\left(x\right)=x^{4}+x^{3}-2x+3,\quad g\left(x\right)=3x^{2}-x+2.
$$

### Solution 7.2-3(2)

By **Theorem 7.2.1 (Division with Remainder)**, perform polynomial long division:

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

Therefore, by **Theorem 7.2.1 (Division with Remainder)**,

$$
\text{quotient }h\left(x\right)=\frac{1}{3}x^{2}+\frac{4}{9}x-\frac{2}{27}.
$$

$$
\text{remainder }r\left(x\right)=-\frac{80}{27}x+\frac{85}{27}.
$$

$\blacksquare$

---

## 7.2-4

Let

$$
f\left(x\right)=x^{3}-3x^{2}+ax+a_{0},
$$

$g\left(x\right)=x^{2}-3x+1$. Find the necessary and sufficient condition for $g\left(x\right)$ to divide $f\left(x\right)$.

### Solution 7.2-4

Divide $f\left(x\right)$ by $g\left(x\right)$:

Leading term of the quotient: $x^{3}/x^{2}=x$.

$$
x\cdot g\left(x\right)=x^{3}-3x^{2}+x.
$$

Remainder:

$$
f-x\cdot g=\left(a-1\right)x+a_{0}.
$$

The degree of the remainder is $< 2$, so stop.

Therefore $g\left(x\right)\mid f\left(x\right)$ if and only if the remainder is zero, i.e.

$$
\left(a-1\right)x+a_{0}=0.
$$

This holds for all $x$ if and only if

$$
a-1=0,\quad a_{0}=0.
$$

Hence the necessary and sufficient condition is $a=1$, $a_{0}=0$. $\blacksquare$

---

## 7.2-5

Use synthetic division to find the quotient and remainder when $f\left(x\right)$ is divided by the linear polynomial $g\left(x\right)$.

(1)

$$
f\left(x\right)=3x^{4}-5x^{2}+2x-1,
$$

$g\left(x\right)=x-4$;

(2) $f\left(x\right)=5x^{3}-3x+4$, $g\left(x\right)=x+2$.

### Solution 7.2-5

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
\text{quotient }h\left(x\right)=3x^{3}+12x^{2}+43x+174.
$$

$$
\text{remainder }r\left(x\right)=775.
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
\text{quotient }h\left(x\right)=5x^{2}-10x+17.
$$

$$
\text{remainder }r\left(x\right)=-30.
$$

$\blacksquare$
