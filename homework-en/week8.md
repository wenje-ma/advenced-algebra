# week8

> **Definition 3.2.1 (Linear Dependence)**
> 
> A vector group $\alpha_{1},\cdots,\alpha_{s}$ in $K^{n}$ is called linearly dependent if there exist numbers $k_{1},\cdots,k_{s}$ in $K$, not all zero, such that $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$.

> **Proposition 3.2.1 (Relation Between Linear Representability and Linear Dependence)**
> 
> Suppose the vector group $\alpha_{1},\cdots,\alpha_{s}$ is linearly independent. Then the vector $\beta$ can be linearly represented by $\alpha_{1},\cdots,\alpha_{s}$ if and only if $\alpha_{1},\cdots,\alpha_{s},\beta$ is linearly dependent.

> **Definition 3.2.2 (Linear Independence)**
> 
> A vector group $\alpha_{1},\cdots,\alpha_{s}$ in $K^{n}$ is called linearly independent if it is not linearly dependent. That is, if from $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$ one can deduce that all coefficients are $0$, then the vector group is linearly independent.

> **Definition 3.3.1 (Maximal Linearly Independent Subset)**
> 
> A subset of a vector group in $K^{n}$ is called a maximal linearly independent subset if it is itself linearly independent, yet adding any one vector from the remaining vectors of the group yields a linearly dependent subset.

> **Definition 3.3.2 (Equivalence of Vector Groups)**
> 
> If the vector group $\alpha_{1},\cdots,\alpha_{s}$ and the vector group $\beta_{1},\cdots,\beta_{t}$ can be linearly represented by each other, then the two groups are called equivalent.

> **Definition 3.3.3 (Rank of a Vector Group)**
> 
> The number of vectors contained in a maximal linearly independent subset of a vector group is called the rank of that vector group, denoted $\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}$.

> **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**
> 
> The vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ is linearly independent if and only if its rank equals the number $s$ of vectors it contains.

> **Proposition 3.3.7 (Comparison of Ranks)**
> 
> If vector group (I) can be linearly represented by vector group (II), then the rank of (I) is at most the rank of (II).

> **Corollary 3.3.8 (Equivalent Vector Groups Have the Same Rank)**
> 
> Equivalent vector groups have the same rank.

> **Definition 3.4.1 (Basis)**
> 
> Let $U$ be a subspace of $K^{n}$. A vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ in $U$ is called a basis of $U$ if it satisfies: $1^{\circ}$ it is linearly independent; $2^{\circ}$ every vector in $U$ can be linearly represented by it.

> **Theorem 3.4.8 (The Rank of a Vector Group Equals the Dimension of Its Spanning Subspace)**
> 
> A maximal linearly independent subset of the vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ in $K^{n}$ is a basis of the subspace $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\rangle$ spanned by this group, and hence

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}.
$$

## 3.2-11

Let $a_{1},a_{2},\cdots,a_{r}$ be pairwise distinct numbers with $r\le{n}$. Set

$$
\alpha_{1}=\begin{bmatrix}1\\a_{1}\\a_{1}^{2}\\\vdots\\a_{1}^{n-1}\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\a_{2}\\a_{2}^{2}\\\vdots\\a_{2}^{n-1}\end{bmatrix},\cdots,
\alpha_{r}=\begin{bmatrix}1\\a_{r}\\a_{r}^{2}\\\vdots\\a_{r}^{n-1}\end{bmatrix}.
$$

Prove that $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ are linearly independent.

### Solution to 3.2-11

By **Definition 3.2.2 (Linear Independence)**, to prove that $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ are linearly independent is to prove that the homogeneous system

$$
k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{r}\alpha_{r}=0
$$

has only the zero solution.

Set

$$
k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{r}\alpha_{r}=0.
$$

Taking the first $r$ components gives the homogeneous system:

$$
\begin{cases}
k_{1}+k_{2}+\cdots+k_{r}=0,\\
k_{1}a_{1}+k_{2}a_{2}+\cdots+k_{r}a_{r}=0,\\
\cdots\cdots\cdots\cdots\\
k_{1}a_{1}^{r-1}+k_{2}a_{2}^{r-1}+\cdots+k_{r}a_{r}^{r-1}=0.
\end{cases}
$$

By Formula for the Vandermonde Determinant, its coefficient determinant is the $r\times{r}$ Vandermonde determinant:

$$
\left|\begin{array}{cccc}
1&1&\cdots&1\\
a_{1}&a_{2}&\cdots&a_{r}\\
\vdots&\vdots&&\vdots\\
a_{1}^{r-1}&a_{2}^{r-1}&\cdots&a_{r}^{r-1}
\end{array}\right|=\prod_{1\le{i}<{}j\le{r}}\left(a_{j}-a_{i}\right).
$$

Because $a_{1},a_{2},\cdots,a_{r}$ are pairwise distinct, the determinant is nonzero.

Hence the homogeneous system has only the zero solution: $k_{1}=k_{2}=\cdots=k_{r}=0$.

Therefore $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ are linearly independent. $\blacksquare$

## 3.3-1

Given the vector group

$$
\alpha_{1}=\begin{bmatrix}2\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}-1\\3\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}7\\-4\\0\end{bmatrix}.
$$

Find a maximal linearly independent subset of $\alpha_{1},\alpha_{2},\alpha_{3}$, and its rank.

### Solution to 3.3-1

By **Definition 3.3.1 (Maximal Linearly Independent Subset)** and **Definition 3.3.3 (Rank of a Vector Group)**, first determine whether $\alpha_{1},\alpha_{2}$ are linearly independent. Clearly $\alpha_{2}$ is not a scalar multiple of $\alpha_{1}$, so $\alpha_{1},\alpha_{2}$ are linearly independent.

Next determine whether $\alpha_{3}$ can be represented by $\alpha_{1},\alpha_{2}$. Set $\alpha_{3}=k_{1}\alpha_{1}+k_{2}\alpha_{2}$ and compare components:

$$
\begin{cases}
2k_{1}-k_{2}=7,\\
3k_{2}=-4,\\
0=0.
\end{cases}
$$

From the second equation $k_{2}=-\frac{4}{3}$; substituting into the first gives $k_{1}=\frac{17}{6}$.

Hence

$$
\alpha_{3}=\frac{17}{6}\alpha_{1}-\frac{4}{3}\alpha_{2}.
$$

By **Definition 3.3.1 (Maximal Linearly Independent Subset)**, $\alpha_{1},\alpha_{2}$ are therefore a maximal linearly independent subset. By **Definition 3.3.3 (Rank of a Vector Group)**, the rank is $2$. $\blacksquare$

## 3.3-7

Prove: if a vector group of rank $r$ can be linearly represented by $r$ of its own vectors, then these $r$ vectors form a maximal linearly independent subset of the group.

### Solution to 3.3-7

Let the rank of vector group (I) be $r$, and suppose (I) can be linearly represented by its $r$ vectors $\alpha_{1},\cdots,\alpha_{r}$.

Because $\alpha_{1},\cdots,\alpha_{r}$ are part of (I), they can be represented by (I).

By **Definition 3.3.2 (Equivalence of Vector Groups)**, (I) and $\alpha_{1},\cdots,\alpha_{r}$ are therefore equivalent.

By **Corollary 3.3.8 (Equivalent Vector Groups Have the Same Rank)**, equivalent groups have the same rank, so $\text{rank}\left\{\alpha_{1},\cdots,\alpha_{r}\right\}=r$.

By **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**, the rank of $r$ vectors being $r$ shows that they are linearly independent.

Also, since (I) can be represented by $\alpha_{1},\cdots,\alpha_{r}$, adding any one remaining vector of (I) to $\alpha_{1},\cdots,\alpha_{r}$ gives a linearly dependent group (otherwise, by **Proposition 3.3.7 (Comparison of Ranks)**, the rank would exceed $r$).

Hence $\alpha_{1},\cdots,\alpha_{r}$ is a maximal linearly independent subset of (I). $\blacksquare$

## 3.3-8

Prove: the $n$-variable linear system of $n$ equations over a number field $K$

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

is solvable for every $\beta\in{K}^{n}$ if and only if its coefficient determinant $\left|A\right|\ne0$.

### Solution to 3.3-8

Necessity. Suppose the system is solvable for every $\beta\in{K}^{n}$.

Take $\beta=\varepsilon_{1},\varepsilon_{2},\cdots,\varepsilon_{n}$ (the standard basis); then they can all be represented by $\alpha_{1},\cdots,\alpha_{n}$.

By **Definition 3.3.2 (Equivalence of Vector Groups)**, $\alpha_{1},\cdots,\alpha_{n}$ and $\varepsilon_{1},\cdots,\varepsilon_{n}$ are therefore equivalent (since $\alpha_{1},\cdots,\alpha_{n}$ can be represented by $\varepsilon_{1},\cdots,\varepsilon_{n}$ and vice versa).

By **Corollary 3.3.8 (Equivalent Vector Groups Have the Same Rank)**,

$$
\text{rank}\left\{\alpha_{1},\cdots,\alpha_{n}\right\}=\text{rank}\left\{\varepsilon_{1},\cdots,\varepsilon_{n}\right\}=n.
$$

By **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**, $n$ vectors in $K^{n}$ having rank $n$ shows they are linearly independent, so the determinant of the matrix they form is $\left|A\right|\ne0$.

Sufficiency. Suppose $\left|A\right|\ne0$; then $\alpha_{1},\cdots,\alpha_{n}$ are linearly independent.

In $K^{n}$, $n$ linearly independent vectors form a basis of $K^{n}$.

Hence every $\beta\in{K}^{n}$ can be represented by $\alpha_{1},\cdots,\alpha_{n}$, i.e. the system is solvable.

$\blacksquare$

## 3.3-11

Prove: two vector groups are equivalent if and only if they have the same rank and one of them can be linearly represented by the other.

### Solution to 3.3-11

Necessity. Suppose the two vector groups (I) and (II) are equivalent.

By **Corollary 3.3.8 (Equivalent Vector Groups Have the Same Rank)**, equivalent groups have the same rank.

Moreover, equivalence means they can represent each other, so one group can be represented by the other.

Sufficiency. Suppose (I) and (II) have the same rank and (I) can be represented by (II).

Let a maximal linearly independent subset of (I) be $\alpha_{1},\cdots,\alpha_{r}$, and a maximal linearly independent subset of (II) be $\beta_{1},\cdots,\beta_{r}$.

Because (I) can be represented by (II), $\alpha_{1},\cdots,\alpha_{r}$ can be represented by $\beta_{1},\cdots,\beta_{r}$.

Also, $\alpha_{1},\cdots,\alpha_{r}$ are linearly independent with $r$ vectors, and $\beta_{1},\cdots,\beta_{r}$ are likewise $r$ linearly independent vectors.

By Problem 7 of Exercises 3.3, $r$ linearly independent vectors can represent all vectors in an $r$-dimensional space, so $\beta_{1},\cdots,\beta_{r}$ can be represented by $\alpha_{1},\cdots,\alpha_{r}$.

By **Definition 3.3.2 (Equivalence of Vector Groups)**, $\alpha_{1},\cdots,\alpha_{r}$ and $\beta_{1},\cdots,\beta_{r}$ are therefore equivalent.

Moreover, (I) is equivalent to $\alpha_{1},\cdots,\alpha_{r}$ and (II) is equivalent to $\beta_{1},\cdots,\beta_{r}$; by transitivity, (I) and (II) are equivalent.

$\blacksquare$

## 3.4-2

Prove that the vector group in $K^{n}$

$$
\eta_{1}=\begin{bmatrix}1\\0\\0\\\vdots\\0\end{bmatrix},
\eta_{2}=\begin{bmatrix}1\\1\\0\\\vdots\\0\end{bmatrix},\cdots,
\eta_{n}=\begin{bmatrix}1\\1\\1\\\vdots\\1\end{bmatrix}
$$

is a basis of $K^{n}$.

### Solution to 3.4-2

By the requirements of **Definition 3.4.1 (Basis)**, it suffices to verify two conditions: linear independence, and that it can linearly represent every vector in $K^{n}$.

Verify linear independence. Set

$$
k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{n}\eta_{n}=0.
$$

Comparing components (from the $1$st to the $n$th):

$1$st component: $k_{1}=0$.

$2$nd component: $k_{1}+k_{2}=0$; substituting $k_{1}=0$ gives $k_{2}=0$.

$3$rd component: $k_{1}+k_{2}+k_{3}=0$; substituting $k_{1}=k_{2}=0$ gives $k_{3}=0$.

Continuing, the $i$th component gives $k_{i}=0$.

Hence $\eta_{1},\eta_{2},\cdots,\eta_{n}$ are linearly independent.

Verify representability. Take any

$$
\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)^{\top}\in{K}^{n},
$$

and set

$$
\alpha=x_{1}\eta_{1}+x_{2}\eta_{2}+\cdots+x_{n}\eta_{n}.
$$

Comparing components:

$1$st component: $x_{1}=a_{1}$.

$2$nd component: $x_{1}+x_{2}=a_{2}$, so $x_{2}=a_{2}-a_{1}$.

$3$rd component: $x_{1}+x_{2}+x_{3}=a_{3}$, so $x_{3}=a_{3}-a_{2}$.

Continuing, $x_{i}=a_{i}-a_{i-1}$ $\left(i=2,\cdots,n\right)$.

The representation exists and is unique.

By **Definition 3.4.1 (Basis)**, $\eta_{1},\eta_{2},\cdots,\eta_{n}$ is therefore a basis of $K^{n}$. $\blacksquare$

## 3.4-3(3)

Determine whether the following vector group is a basis of $K^{3}$:

$$
\alpha_{1}=\begin{bmatrix}1\\0\\1\end{bmatrix},
\alpha_{2}=\begin{bmatrix}0\\4\\-1\end{bmatrix},
\alpha_{3}=\begin{bmatrix}2\\-4\\3\end{bmatrix}.
$$

### Solution to 3.4-3(3)

By the requirements of **Definition 3.4.1 (Basis)**, to determine whether three $3$-dimensional vectors form a basis of $K^{3}$ is equivalent to determining whether they are linearly independent, i.e. whether the determinant of the matrix they form is nonzero.

$$
\left|\begin{array}{rrr}
1&0&2\\
0&4&-4\\
1&-1&3
\end{array}\right|
=1\times\left(4\times3-\left(-4\right)\times\left(-1\right)\right)-0+2\times\left(0\times\left(-1\right)-4\times1\right)
$$

$$
=1\times\left(12-4\right)+2\times\left(-4\right)=8-8=0.
$$

The determinant is $0$; by **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**, $\alpha_{1},\alpha_{2},\alpha_{3}$ are therefore linearly dependent, failing the "linearly independent" requirement of **Definition 3.4.1 (Basis)**, and are not a basis of $K^{3}$. $\blacksquare$

## 3.4-4

Let $U$ be an $r$-dimensional subspace of $K^{n}$, and let $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ be $r$ vectors in $U$. Prove that if every vector in $U$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$, then $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ is a basis of $U$.

### Solution to 3.4-4

By the requirements of **Definition 3.4.1 (Basis)**, it suffices to verify two conditions: linear independence, and that every vector in $U$ can be represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$. The second condition is given, so only linear independence needs verification.

Because every vector in $U$ can be represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$, we have $U\subseteq\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

Also, since $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\in{U}$ and $U$ is a subspace, $\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle\subseteq{U}$.

Hence $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

By **Theorem 3.4.8 (The Rank of a Vector Group Equals the Dimension of Its Spanning Subspace)**,

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}.
$$

Since $\dim{U}=r$,

$$
\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}=r.
$$

By **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**, the rank of $r$ vectors being $r$ shows they are linearly independent.

Thus $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ are linearly independent, and every vector in $U$ can be represented by them.

By **Definition 3.4.1 (Basis)**, $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ is a basis of $U$. $\blacksquare$
