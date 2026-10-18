ï»¿ï»¿# Assignment 12

> **Definition 1** (Maximal Linearly Independent Subsystem)<br>A subsystem of a vector system in $K^{n}$ is called a maximal linearly independent subsystem if the subsystem itself is linearly independent, but whenever any one of the remaining vectors of the vector system is adjoined, the resulting new subsystem is linearly dependent.

> **Definition 3** (Rank of a Vector System)<br>The number of vectors contained in a maximal linearly independent subsystem of a vector system is called the rank of the vector system. It is denoted by $\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}$.

> **Proposition 7** (Comparison of Ranks)<br>If vector system (I) can be linearly spanned by vector system (II), then the rank of (I) is $\le$ the rank of (II).

### Problem 1

(Problem 3.3-1) Let the vector system

$$
\alpha_{1}=\begin{bmatrix}2\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}-1\\3\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}7\\-4\\0\end{bmatrix}.
$$

Find a maximal linearly independent subsystem of $\alpha_{1},\alpha_{2},\alpha_{3}$, as well as its rank.

### Solution to Problem 1

By **Definition 1** (Maximal Linearly Independent Subsystem) and **Definition 3** (Rank of a Vector System), first determine whether $\alpha_{1},\alpha_{2}$ is linearly independent. Clearly $\alpha_{2}$ is not a multiple of $\alpha_{1}$, so $\alpha_{1},\alpha_{2}$ is linearly independent.

Next determine whether $\alpha_{3}$ can be linearly spanned by $\alpha_{1},\alpha_{2}$. Set $\alpha_{3}=k_{1}\alpha_{1}+k_{2}\alpha_{2}$; comparing the components:

$$
\begin{cases}
2k_{1}-k_{2}=7,\\
3k_{2}=-4,\\
0=0.
\end{cases}
$$

From the $2$nd equation we get $k_{2}=-\frac{4}{3}$; substituting into the $1$st equation gives $k_{1}=\frac{17}{6}$.

Hence

$$
\alpha_{3}=\frac{17}{6}\alpha_{1}-\frac{4}{3}\alpha_{2}
$$

By **Definition 1**, $\alpha_{1},\alpha_{2}$ is therefore a maximal linearly independent subsystem. By **Definition 3**, the rank is $2$. $\blacksquare$

### Problem 2

(Problem 3.3-7) Prove that if a vector system of rank $r$ can be linearly spanned by $r$ of its own vectors, then these $r$ vectors form a maximal linearly independent subsystem of the vector system.

### Solution to Problem 2

Let the rank of vector system (I) be $r$, and suppose (I) can be linearly spanned by its $r$ vectors $\alpha_{1},\cdots,\alpha_{r}$.

Since $\alpha_{1},\cdots,\alpha_{r}$ are a part of (I), $\alpha_{1},\cdots,\alpha_{r}$ can be linearly spanned by (I).

Hence (I) and $\alpha_{1},\cdots,\alpha_{r}$ are equivalent.

By Corollary $8$, equivalent vector systems have the same rank, hence $\text{rank}\left\{\alpha_{1},\cdots,\alpha_{r}\right\}=r$.

The rank of $r$ vectors being $r$ means that they are linearly independent.

Moreover, since (I) can be linearly spanned by $\alpha_{1},\cdots,\alpha_{r}$, whenever any one of the remaining vectors of (I) is adjoined to $\alpha_{1},\cdots,\alpha_{r}$, the resulting new vector system must be linearly dependent (otherwise the rank would exceed $r$).

Therefore $\alpha_{1},\cdots,\alpha_{r}$ is a maximal linearly independent subsystem of (I). $\blacksquare$

### Problem 3

(Problem 3.3-8) Prove that an $n$-variable system of $n$ linear equations over the number field $K$

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

has a solution for every $\beta\in K^{n}$ if and only if its coefficient determinant $\left|A\right|\ne0$.

### Solution to Problem 3

**Necessity**. Suppose there is a solution for every $\beta\in K^{n}$.

Take $\beta=\epsilon_{1},\epsilon_{2},\cdots,\epsilon_{n}$ (the standard basis); then they can all be linearly spanned by $\alpha_{1},\cdots,\alpha_{n}$.

Hence $\alpha_{1},\cdots,\alpha_{n}$ and $\epsilon_{1},\cdots,\epsilon_{n}$ are equivalent (because $\alpha_{1},\cdots,\alpha_{n}$ can be linearly spanned by $\epsilon_{1},\cdots,\epsilon_{n}$, and conversely).

By Corollary $8$,

$$
\text{rank}\left\{\alpha_{1},\cdots,\alpha_{n}\right\}=\text{rank}\left\{\epsilon_{1},\cdots,\epsilon_{n}\right\}=n.
$$

The rank of $n$ vectors in $n$ dimensions being $n$ means that they are linearly independent, so the determinant they form satisfies $\left|A\right|\ne0$.

**Sufficiency**. Suppose $\left|A\right|\ne0$; then $\alpha_{1},\cdots,\alpha_{n}$ is linearly independent.

In $K^{n}$, $n$ linearly independent vectors form a basis of $K^{n}$.

Therefore any $\beta\in K^{n}$ can be linearly spanned by $\alpha_{1},\cdots,\alpha_{n}$, i.e. the system has a solution.

$\blacksquare$

### Problem 4

(Problem 3.3-11) Prove that two vector systems are equivalent if and only if they have the same rank and one of the vector systems can be linearly spanned by the other.

### Solution to Problem 4

**Necessity**. Let the two vector systems (I) and (II) be equivalent.

By Corollary $8$, equivalent vector systems have the same rank.

Moreover, equivalence means that they can be linearly spanned by each other, so one of the vector systems can be linearly spanned by the other.

**Sufficiency**. Suppose (I) and (II) have the same rank, and (I) can be linearly spanned by (II).

Let a maximal linearly independent subsystem of (I) be $\alpha_{1},\cdots,\alpha_{r}$, and a maximal linearly independent subsystem of (II) be $\beta_{1},\cdots,\beta_{r}$.

Since (I) can be linearly spanned by (II), $\alpha_{1},\cdots,\alpha_{r}$ can be linearly spanned by $\beta_{1},\cdots,\beta_{r}$.

Moreover, $\alpha_{1},\cdots,\alpha_{r}$ is linearly independent and has $r$ vectors, while $\beta_{1},\cdots,\beta_{r}$ are also $r$ linearly independent vectors.

By Problem 7 of Exercise 3.3, $r$ linearly independent vectors can linearly span all vectors in an $r$-dimensional space, so $\beta_{1},\cdots,\beta_{r}$ can be linearly spanned by $\alpha_{1},\cdots,\alpha_{r}$.

Hence $\alpha_{1},\cdots,\alpha_{r}$ and $\beta_{1},\cdots,\beta_{r}$ are equivalent.

Moreover, (I) is equivalent to $\alpha_{1},\cdots,\alpha_{r}$, and (II) is equivalent to $\beta_{1},\cdots,\beta_{r}$; by transitivity, (I) and (II) are equivalent.

$\blacksquare$
