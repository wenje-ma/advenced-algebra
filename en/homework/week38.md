# week38

> **Definition 7.6.1 (Root of a Polynomial)**<br>Let $K$ be a number field, and let $R$ be a commutative ring with identity that can be viewed as an extension ring of $K$. For a polynomial $f\left(x\right)$ in $K\left[x\right]$, if there is an element $c$ in $R$ such that $f\left(c\right)=0$, then $c$ is called a root of $f\left(x\right)$ in $R$.

> **Theorem 7.6.1 (Remainder Theorem)**<br>In $K\left[x\right]$, the remainder when $f\left(x\right)$ is divided by $x-a$ is $f\left(a\right)$.

> **Corollary 7.6.2 (Factor Theorem)**<br>In $K\left[x\right]$, $x-a$ divides $f\left(x\right)$ if and only if $f\left(a\right)=0$.

---

## 7.6-1

Let

$$
f\left(x\right)=x^{5}+7x^{4}+19x^{3}+26x^{2}+20x+8\in\mathbb{Q}\left[x\right].
$$

Determine whether $-2$ is a root of $f\left(x\right)$, and if so, its multiplicity.

### Solution 7.6-1

By **Corollary 7.6.2 (Factor Theorem)**, $x-a$ divides $f\left(x\right)$ if and only if $f\left(a\right)=0$. Compute $f\left(-2\right)$:

$$
f\left(-2\right)
=\left(-2\right)^{5}+7\left(-2\right)^{4}+19\left(-2\right)^{3}+26\left(-2\right)^{2}+20\left(-2\right)+8=-32+112-152+104-40+8=0.
$$

Hence $-2$ is a root of $f\left(x\right)$.

Use synthetic division to see how many times $x+2$ divides $f$.

**First division**:

$$
\begin{array}{r|rrrrrr}
-2 & 1 & 7 & 19 & 26 & 20 & 8\\
   &   & -2 & -10 & -18 & -16 & -8\\
\hline
   & 1 & 5 & 9 & 8 & 4 & 0
\end{array}
$$

Remainder $0$, quotient $x^{4}+5x^{3}+9x^{2}+8x+4$.

**Second division**:

$$
\begin{array}{r|rrrrr}
-2 & 1 & 5 & 9 & 8 & 4\\
   &   & -2 & -6 & -6 & -4\\
\hline
   & 1 & 3 & 3 & 2 & 0
\end{array}
$$

Remainder $0$, quotient $x^{3}+3x^{2}+3x+2$.

**Third division**:

$$
\begin{array}{r|rrrr}
-2 & 1 & 3 & 3 & 2\\
   &   & -2 & -2 & -2\\
\hline
   & 1 & 1 & 1 & 0
\end{array}
$$

Remainder $0$, quotient $x^{2}+x+1$.

**Fourth division**:

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

---

## 7.6-4

Let

$$
f\left(x\right)=x^{4}-5x^{3}+ax^{2}+bx+9\in\mathbb{Q}\left[x\right].
$$

If $3$ is a double root of $f\left(x\right)$, find $a,b$.

### Solution 7.6-4

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

---

## 7.6-8

Find the standard factorization of the complex-coefficient polynomial $x^{n}-1$.

### Solution 7.6-8

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
