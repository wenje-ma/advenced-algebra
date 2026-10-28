# week42

> **Basic Knowledge: Elementary Symmetric Polynomials**<br>The elementary symmetric polynomials in $n$ variables are

$$
\sigma_{1}=x_{1}+x_{2}+\cdots+x_{n},
$$

$$
\sigma_{2}=x_{1}x_{2}+x_{1}x_{3}+\cdots+x_{n-1}x_{n},
$$

$$
\cdots\cdots
$$

$$
\sigma_{n}=x_{1}x_{2}\cdots x_{n}.
$$

> **Basic Knowledge: Newton's Identities**<br>Let $S_{k}=x_{1}^{k}+x_{2}^{k}+\cdots+x_{n}^{k}$; then:

$$
S_{1}=\sigma_{1},
$$

$$
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\cdots+\left(-1\right)^{k-1}\sigma_{k-1}S_{1}+\left(-1\right)^{k}k\sigma_{k}=0,\quad 1\le k\le n,
$$

$$
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\cdots+\left(-1\right)^{n}\sigma_{n}S_{k-n}=0,\quad k> n.
$$

> **Definition 7.10.1 (Symmetric Polynomial)**<br>Let $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ be a polynomial over $K$. If for every permutation $j_{1}j_{2}\ldots j_{n}$ of $1,2,\ldots,n$,

$$
f\left(x_{j_{1}},x_{j_{2}},\ldots,x_{j_{n}}\right)=f\left(x_{1},x_{2},\ldots,x_{n}\right),
$$

then $f$ is called a symmetric polynomial over $K$.

---

## 7.10-5

In $K\left[x_{1},x_{2},x_{3}\right]$, use Newton's identities to express the power sums $S_{2},S_{3},S_{4}$ in terms of elementary symmetric polynomials.

### Solution 7.10-5

By **Basic Knowledge: Newton's Identities**, let $S_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$. The elementary symmetric polynomials:

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

Hence

$$
S_{3}
=\sigma_{1}S_{2}-\sigma_{2}S_{1}+3\sigma_{3}=\sigma_{1}\left(\sigma_{1}^{2}-2\sigma_{2}\right)-\sigma_{2}\sigma_{1}+3\sigma_{3}=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}.
$$

**$S_{4}$**.

By Newton's identities (since $n=3$, $k=4> n$):

$$
S_{4}-\sigma_{1}S_{3}+\sigma_{2}S_{2}-\sigma_{3}S_{1}=0.
$$

Hence

$$
S_{4}
=\sigma_{1}S_{3}-\sigma_{2}S_{2}+\sigma_{3}S_{1}=\sigma_{1}\left(\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}\right)-\sigma_{2}\left(\sigma_{1}^{2}-2\sigma_{2}\right)+\sigma_{3}\sigma_{1}=\sigma_{1}^{4}-3\sigma_{1}^{2}\sigma_{2}+3\sigma_{1}\sigma_{3}-\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+\sigma_{1}\sigma_{3}=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
$$

$S_{2}=\sigma_{1}^{2}-2\sigma_{2}$, $S_{3}=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}$,

$$
S_{4}=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
$$

$\blacksquare$

---

## 7.10-7

Let $f\left(x\right)\in K\left[x\right]$ be monic, $a\in K$, and $g\left(x\right)=\left(x-a\right)f\left(x\right)$. Prove: $D\left(g\right)=D\left(f\right)f\left(a\right)^{2}$.

### Solution 7.10-7

Write

$$
f\left(x\right)=\left(x-r_{1}\right)\left(x-r_{2}\right)\cdots\left(x-r_{n}\right),
$$

where $r_{1},r_{2},\ldots,r_{n}$ are all roots of $f\left(x\right)$ (with multiplicity).

Then

$$
g\left(x\right)=\left(x-a\right)f\left(x\right)=\left(x-a\right)\left(x-r_{1}\right)\left(x-r_{2}\right)\cdots\left(x-r_{n}\right).
$$

Set $s_{0}=a$, $s_{1}=r_{1}$, $\ldots$, $s_{n}=r_{n}$.

The discriminant is defined as:

$$
D\left(f\right)=\prod_{1\le i< j\le n}\left(r_{i}-r_{j}\right)^{2}.
$$

$$
D\left(g\right)=\prod_{0\le i< j\le n}\left(s_{i}-s_{j}\right)^{2}.
$$

Therefore

$$
D\left(g\right)
=\prod_{1\le i< j\le n}\left(r_{i}-r_{j}\right)^{2}\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}=D\left(f\right)\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}.
$$

And

$$
f\left(a\right)=\left(a-r_{1}\right)\left(a-r_{2}\right)\cdots\left(a-r_{n}\right).
$$

Hence

$$
\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}=f\left(a\right)^{2}.
$$

Therefore

$$
D\left(g\right)=D\left(f\right)\cdot f\left(a\right)^{2}.
$$

$\blacksquare$
