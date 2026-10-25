# Assignment 42

> **Definition 1** (Symmetric Polynomial)<br>Let $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ be a polynomial in $n$ variables over a number field $K$. If for any $n$-element permutation $j_{1}j_{2}\ldots j_{n}$,
> $$
> f\left(x_{j_{1}},x_{j_{2}},\ldots,x_{j_{n}}\right)=f\left(x_{1},x_{2},\ldots,x_{n}\right),
> $$
> then $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ is called a symmetric polynomial in $n$ variables over the number field $K$.

> **Elementary Symmetric Polynomials**<br>
> 
> $$
> \begin{aligned}
> \sigma_{1}&=x_{1}+x_{2}+\ldots+x_{n},\\
> \sigma_{2}&=x_{1}x_{2}+x_{1}x_{3}+\ldots+x_{n-1}x_{n},\\
> \ldots&\\
> \sigma_{n}&=x_{1}x_{2}\ldots x_{n}
> \end{aligned}
> $$

> **Newton's Identities** (Relation Between Power Sums and Elementary Symmetric Polynomials)<br>Let $S_{k}=x_{1}^{k}+x_{2}^{k}+\ldots+x_{n}^{k}$. Then:
> 
> $$
> \begin{aligned}
> S_{1}&=\sigma_{1},\\
> S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\ldots+\left(-1\right)^{k-1}\sigma_{k-1}S_{1}+\left(-1\right)^{k}k\sigma_{k}&=0, \ 1\le k\le n,\\
> S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\ldots+\left(-1\right)^{n}\sigma_{n}S_{k-n}&=0, \ k> n
> \end{aligned}
> $$

### Problem 1

(Problem 7.10-5) In $K\left[x_{1},x_{2},x_{3}\right]$, use Newton's identities to express the power sums $S_{2},S_{3},S_{4}$ in terms of the elementary symmetric polynomials.

### Solution to Problem 1

By **Newton's Identities** (Relation Between Power Sums and Elementary Symmetric Polynomials), let $S_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$. The elementary symmetric polynomials are:

$$
\sigma_{1}=x_{1}+x_{2}+x_{3},
$$

$$
\sigma_{2}=x_{1}x_{2}+x_{1}x_{3}+x_{2}x_{3},
$$

$$
\sigma_{3}=x_{1}x_{2}x_{3}.
$$

**$S_{2}$**.

By Newton's identities:

$$
S_{2}-\sigma_{1}S_{1}+2\sigma_{2}=0.
$$

Since $S_{1}=\sigma_{1}$,

$$
S_{2}=\sigma_{1}S_{1}-2\sigma_{2}=\sigma_{1}^{2}-2\sigma_{2}.
$$

**$S_{3}$**.

By Newton's identities:

$$
S_{3}-\sigma_{1}S_{2}+\sigma_{2}S_{1}-3\sigma_{3}=0.
$$

Therefore

$$
\begin{aligned}S_{3}
&=\sigma_{1}S_{2}-\sigma_{2}S_{1}+3\sigma_{3}\\
&=\sigma_{1}\left(\sigma_{1}^{2}-2\sigma_{2}\right)-\sigma_{2}\sigma_{1}+3\sigma_{3}\\
&=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}.
\end{aligned}
$$

**$S_{4}$**.

By Newton's identities (since $n=3$ and $k=4> n$):

$$
S_{4}-\sigma_{1}S_{3}+\sigma_{2}S_{2}-\sigma_{3}S_{1}=0.
$$

Therefore

$$
\begin{aligned}S_{4}
&=\sigma_{1}S_{3}-\sigma_{2}S_{2}+\sigma_{3}S_{1}\\
&=\sigma_{1}\left(\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}\right)-\sigma_{2}\left(\sigma_{1}^{2}-2\sigma_{2}\right)+\sigma_{3}\sigma_{1}\\
&=\sigma_{1}^{4}-3\sigma_{1}^{2}\sigma_{2}+3\sigma_{1}\sigma_{3}-\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+\sigma_{1}\sigma_{3}\\
&=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
\end{aligned}
$$

$S_{2}=\sigma_{1}^{2}-2\sigma_{2}$, $S_{3}=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}$,

$$
S_{4}=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
$$

$\blacksquare$

### Problem 2

(Problem 7.10-7) Let $f\left(x\right)\in K\left[x\right]$, and let the leading coefficient of $f\left(x\right)$ be $1$, let $a\in K$, and let $g\left(x\right)=\left(x-a\right)f\left(x\right)$. Prove: $D\left(g\right)=D\left(f\right)f\left(a\right)^{2}$.

### Solution to Problem 2

Let

$$
f\left(x\right)=\left(x-r_{1}\right)\left(x-r_{2}\right)\ldots\left(x-r_{n}\right),
$$

where $r_{1},r_{2},\ldots,r_{n}$ are all the roots of $f\left(x\right)$ (counting multiplicities).

Then

$$
g\left(x\right)=\left(x-a\right)f\left(x\right)=\left(x-a\right)\left(x-r_{1}\right)\left(x-r_{2}\right)\ldots\left(x-r_{n}\right).
$$

Write $s_{0}=a$, $s_{1}=r_{1}$, $\ldots$, $s_{n}=r_{n}$.

The discriminant is defined as:

$$
D\left(f\right)=\prod_{1\le i< j\le n}\left(r_{i}-r_{j}\right)^{2}.
$$

$$
D\left(g\right)=\prod_{0\le i< j\le n}\left(s_{i}-s_{j}\right)^{2}.
$$

Therefore

$$
\begin{aligned}D\left(g\right)
&=\prod_{1\le i< j\le n}\left(r_{i}-r_{j}\right)^{2}\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}\\
&=D\left(f\right)\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}.
\end{aligned}
$$

And

$$
f\left(a\right)=\left(a-r_{1}\right)\left(a-r_{2}\right)\ldots\left(a-r_{n}\right).
$$

Therefore

$$
\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}=f\left(a\right)^{2}.
$$

Hence

$$
D\left(g\right)=D\left(f\right)\cdot f\left(a\right)^{2}.
$$

$\blacksquare$
