# week24

> **Definition 4.7.1 (Mapping)**<br>Let $S$ and $S'$ be two sets. If there is a rule $f$ such that to every element $a$ of $S$ there corresponds a unique element $b$ of $S'$, then $f$ is called a mapping from $S$ to $S'$.

> **Theorem 4.7.1 (Dimension Formula for Kernel and Image)**<br>Let $\mathcal{A}:K^{n}\to K^{s}$ be a linear map. The sum of the dimension of the kernel (the solution space of the homogeneous system) and the dimension of the image equals the dimension of the domain:

$$
\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=\dim\left(K^{n}\right)=n.
$$

> **Definition 4.7.5 (Linear Map)**<br>A mapping $\mathcal{A}$ from $K^{n}$ to $K^{s}$ is called a linear map if it preserves addition and scalar multiplication, i.e. for all $\alpha,\beta\in K^{n}$ and $k\in K$,

$$
\mathcal{A}\left(\alpha+\beta\right)=\mathcal{A}\left(\alpha\right)+\mathcal{A}\left(\beta\right),
$$

and $\mathcal{A}\left(k\alpha\right)=k\mathcal{A}\left(\alpha\right)$.

---

## 4.7-1

Determine whether the following rules are mappings from $\mathbb{R}$ to itself, and whether they are injective or surjective:

(1) $x\mapsto x^{3}$;

(2) $x\mapsto x^{2}-x$;

(3) $x\mapsto 2^{x}$;

(4) $x\mapsto\ln x$.

### Solution 4.7-1

By **Definition 4.7.1 (Mapping)**, determine whether each rule is a mapping from $\mathbb{R}$ to itself, and whether it is injective or surjective.

**(1)** $f\left(x\right)=x^{3}$.

It is a mapping. For every $x\in\mathbb{R}$, $x^{3}$ is defined and unique.

Injective:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow x_{1}^{3}=x_{2}^{3}\Rightarrow x_{1}=x_{2}.
$$

Hence it is injective.

Surjective: for every $y\in\mathbb{R}$, there is $x=\sqrt[3]{y}$ such that $f\left(x\right)=y$. Hence it is surjective.

Therefore it is both injective and surjective (bijective).

**(2)** $f\left(x\right)=x^{2}-x$.

It is a mapping.

Injective: $f\left(0\right)=0$ and $f\left(1\right)=0$, but $0\ne1$. Hence it is not injective.

Surjective:

$$
f\left(x\right)=x^{2}-x=\left(x-\frac{1}{2}\right)^{2}-\frac{1}{4}\ge-\frac{1}{4}.
$$

For example, $-1$ has no preimage. Hence it is not surjective.

Therefore it is neither injective nor surjective.

**(3)** $f\left(x\right)=2^{x}$.

It is a mapping.

Injective:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow 2^{x_{1}}=2^{x_{2}}\Rightarrow x_{1}=x_{2}.
$$

Hence it is injective.

Surjective: $2^{x}> 0$. For example, $-1$ has no preimage. Hence it is not surjective.

Therefore it is injective but not surjective.

**(4)** $f\left(x\right)=\ln x$.

It is not a mapping. Because for $x\le0$, $\ln x$ is not defined, so not every $x\in\mathbb{R}$ has a corresponding value.

$\blacksquare$

---

## 4.7-4

Let $S$ be a finite set. Prove: if a mapping $f:S\to S$ is injective, then $f$ must be bijective.

### Solution 4.7-4

By **Definition 4.7.1 (Mapping)**, suppose $S$ has $n$ elements.

Since $f$ is injective, distinct elements of $S$ have distinct images. Hence the number of elements in $f\left(S\right)$ equals $\left|S\right|=n$.

Since $f\left(S\right)\subseteq S$ and $\left|f\left(S\right)\right|=n=\left|S\right|$, we have $f\left(S\right)=S$.

That is, $f$ is surjective.

Therefore $f$ is both injective and surjective, i.e. $f$ is bijective. $\blacksquare$

---

## 4.7-7

Let

$$
A=\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
-1 & 2 & 1 & 3\\
1 & 2 & 5 & 5
\end{array}\right].
$$

Define $\mathcal{A}\left(\alpha\right)=A\alpha$ for all $\alpha\in K^{4}$.

(1) Find the dimension and a basis of $\operatorname{Im}\mathcal{A}$;

(2) Find the dimension and a basis of $\ker\mathcal{A}$.

### Solution 4.7-7

By **Definition 4.7.5 (Linear Map)** and **Theorem 4.7.1 (Dimension Formula for Kernel and Image)**, $\mathcal{A}\left(\alpha\right)=A\alpha$ is a linear map.

**(1)** $\operatorname{Im}\mathcal{A}$ is the column space of $A$.

Apply elementary row operations to $A$:

$$
A=\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
-1 & 2 & 1 & 3\\
1 & 2 & 5 & 5
\end{array}\right]
\rightarrow
\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
0 & 2 & 3 & 4\\
0 & 2 & 3 & 4
\end{array}\right]
\rightarrow
\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
0 & 2 & 3 & 4\\
0 & 0 & 0 & 0
\end{array}\right].
$$

Hence $\operatorname{rank}\left(A\right)=2$.

The pivot columns are column $1$ and column $2$, so a basis of $\operatorname{Im}\mathcal{A}$ is

$$
\alpha_{1}=\left(1,-1,1\right)^{\top},\alpha_{2}=\left(0,2,2\right)^{\top}.
$$

$$
\dim\left(\operatorname{Im}\mathcal{A}\right)=\operatorname{rank}\left(A\right)=2.
$$

**(2)** $\ker\mathcal{A}$ is the solution space of $Ax=0$.

From the row echelon form, the equivalent system is

$$
\begin{cases}
x_{1}+2x_{3}+x_{4}=0,\\
2x_{2}+3x_{3}+4x_{4}=0.
\end{cases}
$$

The free variables are $x_{3},x_{4}$.

$$
x_{1}=-2x_{3}-x_{4},\quad x_{2}=-\frac{3}{2}x_{3}-2x_{4}.
$$

Set $x_{3}=1,x_{4}=0$:

$$
\xi_{1}=\left(-2,-\frac{3}{2},1,0\right)^{\top}.
$$

Set $x_{3}=0,x_{4}=1$:

$$
\xi_{2}=\left(-1,-2,0,1\right)^{\top}.
$$

Hence a basis of $\ker\mathcal{A}$ is $\xi_{1},\xi_{2}$.

$$
\dim\left(\ker\mathcal{A}\right)=4-\operatorname{rank}\left(A\right)=2.
$$

By **Theorem 4.7.1 (Dimension Formula for Kernel and Image)**, verify:

$$
\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=2+2=4=\dim\left(K^{4}\right).
$$

$\blacksquare$
