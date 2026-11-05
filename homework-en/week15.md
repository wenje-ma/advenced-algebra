# week15

> **Definition 4.6.1 (Orthogonal Matrix)**
> 
> A real square matrix $A$ satisfying $A^{\top}A=I$ is called an orthogonal matrix.

> **Definition 4.6.2 (Standard Inner Product)**
> 
> In $\mathbb{R}^{n}$, for any $\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)$ and $\beta=\left(b_{1},b_{2},\cdots,b_{n}\right)$, define

> **Proposition 4.6.2 (An Orthogonal Vector Group Is Linearly Independent)**
> 
> In the Euclidean space $\mathbb{R}^{n}$, an orthogonal vector group is always linearly independent.

> **Definition 4.7.1 (Mapping)**
> 
> Let $S$ and $S'$ be two sets. If there is a rule $f$ such that to every element $a$ of $S$ there corresponds a unique element $b$ of $S'$, then $f$ is called a mapping from $S$ to $S'$.

> **Theorem 4.7.1 (Dimension Formula for Kernel and Image)**
> 
> Let $\mathcal{A}:K^{n}\to K^{s}$ be a linear map. The sum of the dimension of the kernel (the solution space of the homogeneous system) and the dimension of the image equals the dimension of the domain:

$$
\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=\dim\left(K^{n}\right)=n.
$$

> **Definition 4.7.5 (Linear Map)**
> 
> A mapping $\mathcal{A}$ from $K^{n}$ to $K^{s}$ is called a linear map if it preserves addition and scalar multiplication, i.e. for all $\alpha,\beta\in K^{n}$ and $k\in K$,

$$
\mathcal{A}\left(\alpha+\beta\right)=\mathcal{A}\left(\alpha\right)+\mathcal{A}\left(\beta\right),
$$
and $\mathcal{A}\left(k\alpha\right)=k\mathcal{A}\left(\alpha\right)$.

## 4.6-5

Prove: if an orthogonal matrix $A$ is upper triangular, then $A$ must be diagonal, and its diagonal entries are $1$ or $-1$.

### Solution to 4.6-5

By **Definition 4.6.1 (Orthogonal Matrix)**, let $A$ be an $n\times n$ upper triangular matrix with $A^{\top}A=I$.

Since $A$ is upper triangular, $A^{\top}$ is lower triangular.

$A^{\top}A=I$ is a diagonal matrix.

Prove by induction that all off-diagonal entries of $A$ are zero.

When $i=1,j=2$, consider the $\left(1,2\right)$-entry of $A^{\top}A$:

$$
\sum_{k=1}^{n}\left(A^{\top}\right)_{1k}A_{k2}=\sum_{k=1}^{n}A_{k1}A_{k2}=0.
$$

Since $A$ is upper triangular, $A_{k1}=0$ when $k> 1$. Thus the equation reduces to $A_{11}A_{12}=0$.

Since $A$ is invertible, $A_{11}\ne0$, hence $A_{12}=0$.

Similarly one proves $A_{1j}=0$ ( $j> 1$ ).

Assume the off-diagonal entries of rows $1,\cdots,i-1$ have already been proved to be zero.

Consider the $\left(i,j\right)$-entry of $A^{\top}A$ ( $i< j$ ):

$$
\sum_{k=1}^{i}A_{ki}A_{kj}=0.
$$

By the induction hypothesis, $A_{ki}=0$ when $k< i$. Thus the equation reduces to $A_{ii}A_{ij}=0$.

Since $A_{ii}\ne0$, $A_{ij}=0$.

The induction is complete. Therefore $A$ is diagonal.

From $A^{\top}A=I$, $A_{ii}^{2}=1$, hence $A_{ii}=\pm1$. $\blacksquare$

## 4.6-12

In the Euclidean space $\mathbb{R}^{4}$, let

$$
\alpha_{1}=\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\0\\1\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}1\\0\\0\\-1\end{bmatrix}.
$$

Find an orthonormal vector group equivalent to $\alpha_{1},\alpha_{2},\alpha_{3}$.

### Solution to 4.6-12

By The Schmidt Orthogonalization Process.

Set $\beta_{1}=\alpha_{1}=\left(1,1,0,0\right)^{\top}$.

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}.
$$

$\left(\alpha_{2},\beta_{1}\right)=1$, $\left(\beta_{1},\beta_{1}\right)=2$.

Hence

$$
\beta_{2}=\left(1,0,1,0\right)^{\top}-\frac{1}{2}\left(1,1,0,0\right)^{\top}=\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{\top}.
$$

$$
\beta_{3}=\alpha_{3}-\frac{\left(\alpha_{3},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}-\frac{\left(\alpha_{3},\beta_{2}\right)}{\left(\beta_{2},\beta_{2}\right)}\beta_{2}.
$$

$\left(\alpha_{3},\beta_{1}\right)=1$, $\left(\alpha_{3},\beta_{2}\right)=\frac{1}{2}$, $\left(\beta_{2},\beta_{2}\right)=\frac{3}{2}$.

Hence

$$
\beta_{3}
=\left(1,0,0,-1\right)^{\top}-\frac{1}{2}\left(1,1,0,0\right)^{\top}-\frac{1}{3}\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{\top}=\left(\frac{1}{3},-\frac{1}{3},-\frac{1}{3},-1\right)^{\top}.
$$

Verify orthogonality: $\left(\beta_{1},\beta_{2}\right)=0$, $\left(\beta_{1},\beta_{3}\right)=0$, $\left(\beta_{2},\beta_{3}\right)=0$.

Normalize:

$$
\eta_{1}=\frac{\beta_{1}}{\left|\beta_{1}\right|}=\left(\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}},0,0\right)^{\top}.
$$

$$
\eta_{2}=\frac{\beta_{2}}{\left|\beta_{2}\right|}=\left(\frac{1}{\sqrt{6}},-\frac{1}{\sqrt{6}},\frac{2}{\sqrt{6}},0\right)^{\top}.
$$

$$
\eta_{3}=\frac{\beta_{3}}{\left|\beta_{3}\right|}=\left(\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{\sqrt{3}}{2}\right)^{\top}.
$$

$\blacksquare$

## 4.6-14

Let $A$ be an $n\times n$ real invertible matrix. Prove: $A$ can be decomposed as

$$
A=TB,
$$

where $T$ is orthogonal and $B$ is upper triangular with all diagonal entries positive; prove that this decomposition is unique.

### Solution to 4.6-14

Existence. Let the column group of $A$ be $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$.

Since $A$ is invertible, $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ are linearly independent.

By The Schmidt Orthogonalization Process, apply it to $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ to obtain an orthogonal group $\beta_{1},\beta_{2},\cdots,\beta_{n}$, where $\beta_{i}$ is a linear combination of $\alpha_{1},\cdots,\alpha_{i}$ and $\alpha_{i}$ is a linear combination of $\beta_{1},\cdots,\beta_{i}$.

Normalize $\beta_{1},\beta_{2},\cdots,\beta_{n}$ to obtain an orthonormal group $\eta_{1},\eta_{2},\cdots,\eta_{n}$.

Set $T=\left(\eta_{1},\eta_{2},\cdots,\eta_{n}\right)$; then $T$ is orthogonal.

Since each $\alpha_{i}$ is a linear combination of $\eta_{1},\cdots,\eta_{i}$, $A=TB$, where $B$ is upper triangular.

The diagonal entries of $B$ are $\left|\beta_{1}\right|,\left|\beta_{2}\right|,\cdots,\left|\beta_{n}\right|$, all positive.

Uniqueness. Suppose $A=T_{1}B_{1}=T_{2}B_{2}$, where $T_{1},T_{2}$ are orthogonal and $B_{1},B_{2}$ are upper triangular with positive diagonal entries.

Then $T_{2}^{-1}T_{1}=B_{2}B_{1}^{-1}$.

The left side $T_{2}^{-1}T_{1}$ is orthogonal (a product of orthogonal matrices is orthogonal).

The right side $B_{2}B_{1}^{-1}$ is upper triangular (a product of upper triangular matrices is upper triangular).

By the conclusion of 4.6-5, a matrix that is both orthogonal and upper triangular must be diagonal with diagonal entries $\pm1$.

Hence $B_{2}B_{1}^{-1}$ is diagonal with diagonal entries $\pm1$.

Since the diagonal entries of $B_{1},B_{2}$ are all positive, those of $B_{2}B_{1}^{-1}$ are positive.

Therefore each diagonal entry can only be $+1$, i.e. $B_{2}B_{1}^{-1}=I$.

Hence $B_{2}=B_{1}$, and consequently $T_{2}=T_{1}$.

The decomposition is unique. $\blacksquare$

## 4.7-1

Determine whether the following rules are mappings from $\mathbb{R}$ to itself, and whether they are injective or surjective:

(1) $x\mapsto x^{3}$;

(2) $x\mapsto x^{2}-x$;

(3) $x\mapsto 2^{x}$;

(4) $x\mapsto\ln x$.

### Solution to 4.7-1

By **Definition 4.7.1 (Mapping)**, determine whether each rule is a mapping from $\mathbb{R}$ to itself, and whether it is injective or surjective.

(1) $f\left(x\right)=x^{3}$.

It is a mapping. For every $x\in\mathbb{R}$, $x^{3}$ is defined and unique.

Injective:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow x_{1}^{3}=x_{2}^{3}\Rightarrow x_{1}=x_{2}.
$$

Hence it is injective.

Surjective: for every $y\in\mathbb{R}$, there is $x=\sqrt\left[3\right]{y}$ such that $f\left(x\right)=y$. Hence it is surjective.

Therefore it is both injective and surjective (bijective).

(2) $f\left(x\right)=x^{2}-x$.

It is a mapping.

Injective: $f\left(0\right)=0$ and $f\left(1\right)=0$, but $0\ne1$. Hence it is not injective.

Surjective:

$$
f\left(x\right)=x^{2}-x=\left(x-\frac{1}{2}\right)^{2}-\frac{1}{4}\ge-\frac{1}{4}.
$$

For example, $-1$ has no preimage. Hence it is not surjective.

Therefore it is neither injective nor surjective.

(3) $f\left(x\right)=2^{x}$.

It is a mapping.

Injective:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow 2^{x_{1}}=2^{x_{2}}\Rightarrow x_{1}=x_{2}.
$$

Hence it is injective.

Surjective: $2^{x}> 0$. For example, $-1$ has no preimage. Hence it is not surjective.

Therefore it is injective but not surjective.

(4) $f\left(x\right)=\ln x$.

It is not a mapping. Because for $x\le0$, $\ln x$ is not defined, so not every $x\in\mathbb{R}$ has a corresponding value.

$\blacksquare$

## 4.7-4

Let $S$ be a finite set. Prove: if a mapping $f:S\to S$ is injective, then $f$ must be bijective.

### Solution to 4.7-4

By **Definition 4.7.1 (Mapping)**, suppose $S$ has $n$ elements.

Since $f$ is injective, distinct elements of $S$ have distinct images. Hence the number of elements in $f\left(S\right)$ equals $\left|S\right|=n$.

Since $f\left(S\right)\subseteq S$ and $\left|f\left(S\right)\right|=n=\left|S\right|$, we have $f\left(S\right)=S$.

That is, $f$ is surjective.

Therefore $f$ is both injective and surjective, i.e. $f$ is bijective. $\blacksquare$

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

### Solution to 4.7-7

By **Definition 4.7.5 (Linear Map)** and **Theorem 4.7.1 (Dimension Formula for Kernel and Image)**, $\mathcal{A}\left(\alpha\right)=A\alpha$ is a linear map.

(1) $\operatorname{Im}\mathcal{A}$ is the column space of $A$.

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

(2) $\ker\mathcal{A}$ is the solution space of $Ax=0$.

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
