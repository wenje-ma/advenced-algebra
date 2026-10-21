# Assignment 24

> **Definition 1** (Map)<br>Let $S$ and $S'$ be two sets. If there exists a rule $f$ such that for every element $a$ in $S$, there is a unique element $b$ in $S'$ corresponding to it, then $f$ is called a map from $S$ to $S'$.

> **Definition 5** (Linear map)<br>A map $\mathcal{A}$ from $K^{n}$ to $K^{s}$ that preserves addition and scalar multiplication, i.e., $\forall\alpha,\beta\in K^{n},k\in K$, satisfies
> $$
> \mathcal{A}\left(\alpha+\beta\right)=\mathcal{A}\left(\alpha\right)+\mathcal{A}\left(\beta\right),
> $$
> $\mathcal{A}\left(k\alpha\right)=k\mathcal{A}\left(\alpha\right)$, then $\mathcal{A}$ is called a linear map from $K^{n}$ to $K^{s}$.

> **Theorem** (Dimension formula for kernel and image)<br>
>
> $$
> \dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=\dim\left(K^{n}\right)
> $$

### Problem 1

(Problem 4.7-1) Determine whether the following rules are maps from $\mathbb{R}$ to itself, whether they are injective, and whether they are surjective:

(1) $x\mapsto x^{3}$;

(2) $x\mapsto x^{2}-x$;

(3) $x\mapsto 2^{x}$;

(4) $x\mapsto\ln x$.

### Solution to Problem 1

By **Definition 1** (Map), determine whether the following rules are maps from $\mathbb{R}$ to itself, whether they are injective, and whether they are surjective.

**(1)** $f\left(x\right)=x^{3}$.

It is a map. For any $x\in\mathbb{R}$, $x^{3}$ is well-defined and unique.

Injective:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow x_{1}^{3}=x_{2}^{3}\Rightarrow x_{1}=x_{2}.
$$

Hence it is injective.

Surjective: for any $y\in\mathbb{R}$, there exists

$$
x=\sqrt\left[3\right]{y}
$$

such that $f\left(x\right)=y$. Hence it is surjective.

Therefore it is both injective and surjective (bijective).

** (2)** $f\left(x\right)=x^{2}-x$.

It is a map.

Injective: $f\left(0\right)=0$, $f\left(1\right)=0$, but $0\ne1$. Hence it is not injective.

Surjective:

$$
f\left(x\right)=x^{2}-x=\left(x-\frac{1}{2}\right)^{2}-\frac{1}{4}\ge-\frac{1}{4}
$$
For example, $-1$ has no preimage. Hence it is not surjective.

Therefore it is neither injective nor surjective.

** (3)** $f\left(x\right)=2^{x}$.

It is a map.

Injective:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow 2^{x_{1}}=2^{x_{2}}\Rightarrow x_{1}=x_{2}.
$$

Hence it is injective.

Surjective: $2^{x}>0$. For example, $-1$ has no preimage. Hence it is not surjective.

Therefore it is injective but not surjective.

** (4)** $f\left(x\right)=\ln x$.

It is not a map. Because for $x\le0$, $\ln x$ is not defined; not every $x\in\mathbb{R}$ has a corresponding value.

$\blacksquare$

### Problem 2

(Problem 4.7-4) Let $S$ be a finite set. Prove: if a map $f:S\to S$ is injective, then $f$ must be bijective.

### Solution to Problem 2

By **Definition 1** (Map), let $S$ have $n$ elements.

$f$ is injective, so the images of distinct elements in $S$ are also distinct. Hence the number of elements in $f\left(S\right)$ equals $\left|S\right|=n$.

Also, since $f\left(S\right)\subseteq S$, and $\left|f\left(S\right)\right|=n=\left|S\right|$, we have $f\left(S\right)=S$.

i.e., $f$ is surjective.

Therefore $f$ is both injective and surjective, i.e., $f$ is bijective. $\blacksquare$

### Problem 3

(Problem 4.7-7) Let

$$
A=\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
-1 & 2 & 1 & 3\\
1 & 2 & 5 & 5
\end{array}\right].
$$

Define $\mathcal{A}\left(\alpha\right)=A\alpha$, $\forall\alpha\in K^{4}$.

(1) Find the dimension of $\operatorname{Im}\mathcal{A}$ and a basis;

(2) Find the dimension of $\ker\mathcal{A}$ and a basis.

### Solution to Problem 3

By **Definition 5** (Linear map) and the **Theorem** (Dimension formula for kernel and image), $\mathcal{A}\left(\alpha\right)=A\alpha$ is a linear map.

**(1)** $\operatorname{Im}\mathcal{A}$ equals the column space of $A$.

Perform elementary row operations on $A$:

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

Therefore $\operatorname{rank}\left(A\right)=2$.

The pivot columns are column $1$ and column $2$, so a basis for $\operatorname{Im}\mathcal{A}$ is

$$
\alpha_{1}=\left(1,-1,1\right)^{T},\alpha_{2}=\left(0,2,2\right)^{T}.
$$

$$
\dim\left(\operatorname{Im}\mathcal{A}\right)=\operatorname{rank}\left(A\right)=2.
$$

**(2)** $\ker\mathcal{A}$ is the solution space of $Ax=0$.

The row echelon form gives the equivalent system:

$$
\begin{cases}
x_{1}+2x_{3}+x_{4}=0,\\
2x_{2}+3x_{3}+4x_{4}=0.
\end{cases}
$$

The free variables are $x_{3},x_{4}$.

$$
x_{1}=-2x_{3}-x_{4}, x_{2}=-\frac{3}{2}x_{3}-2x_{4}.
$$

Set $x_{3}=1,x_{4}=0$:

$$
\xi_{1}=\left(-2,-\frac{3}{2},1,0\right)^{T}.
$$

Set $x_{3}=0,x_{4}=1$:

$$
\xi_{2}=\left(-1,-2,0,1\right)^{T}.
$$

Therefore a basis for $\ker\mathcal{A}$ is $\xi_{1},\xi_{2}$.

$$
\dim\left(\ker\mathcal{A}\right)=4-\operatorname{rank}\left(A\right)=2.
$$

By the **Theorem** (Dimension formula for kernel and image), verify:

$$
\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=2+2=4=\dim\left(K^{4}\right).
$$

$\blacksquare$
