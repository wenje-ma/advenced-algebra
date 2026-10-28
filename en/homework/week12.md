# week12

> **Definition 3.3.1 (Maximal Linearly Independent Subset)**<br>A subset of a vector group in $K^{n}$ is called a maximal linearly independent subset if it is itself linearly independent, yet adding any one vector from the remaining vectors of the group yields a linearly dependent subset.

> **Definition 3.3.2 (Equivalence of Vector Groups)**<br>If the vector group $\alpha_{1},\cdots,\alpha_{s}$ and the vector group $\beta_{1},\cdots,\beta_{t}$ can be linearly represented by each other, then the two groups are called equivalent.

> **Definition 3.3.3 (Rank of a Vector Group)**<br>The number of vectors contained in a maximal linearly independent subset of a vector group is called the rank of that vector group, denoted $\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}$.

> **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**<br>The vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ is linearly independent if and only if its rank equals the number $s$ of vectors it contains.

> **Proposition 3.3.7 (Comparison of Ranks)**<br>If vector group (I) can be linearly represented by vector group (II), then the rank of (I) is at most the rank of (II).

> **Corollary 3.3.8 (Equivalent Vector Groups Have the Same Rank)**<br>Equivalent vector groups have the same rank.

---

## 3.3-1

Given the vector group

$$
\alpha_{1}=\begin{bmatrix}2\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}-1\\3\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}7\\-4\\0\end{bmatrix}.
$$

Find a maximal linearly independent subset of $\alpha_{1},\alpha_{2},\alpha_{3}$, and its rank.

### Solution 3.3-1

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

---

## 3.3-7

Prove: if a vector group of rank $r$ can be linearly represented by $r$ of its own vectors, then these $r$ vectors form a maximal linearly independent subset of the group.

### Solution 3.3-7

Let the rank of vector group (I) be $r$, and suppose (I) can be linearly represented by its $r$ vectors $\alpha_{1},\cdots,\alpha_{r}$.

Because $\alpha_{1},\cdots,\alpha_{r}$ are part of (I), they can be represented by (I).

By **Definition 3.3.2 (Equivalence of Vector Groups)**, (I) and $\alpha_{1},\cdots,\alpha_{r}$ are therefore equivalent.

By **Corollary 3.3.8 (Equivalent Vector Groups Have the Same Rank)**, equivalent groups have the same rank, so $\text{rank}\left\{\alpha_{1},\cdots,\alpha_{r}\right\}=r$.

By **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**, the rank of $r$ vectors being $r$ shows that they are linearly independent.

Also, since (I) can be represented by $\alpha_{1},\cdots,\alpha_{r}$, adding any one remaining vector of (I) to $\alpha_{1},\cdots,\alpha_{r}$ gives a linearly dependent group (otherwise, by **Proposition 3.3.7 (Comparison of Ranks)**, the rank would exceed $r$).

Hence $\alpha_{1},\cdots,\alpha_{r}$ is a maximal linearly independent subset of (I). $\blacksquare$

---

## 3.3-8

Prove: the $n$-variable linear system of $n$ equations over a number field $K$

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

is solvable for every $\beta\in K^{n}$ if and only if its coefficient determinant $\left|A\right|\ne0$.

### Solution 3.3-8

**Necessity.** Suppose the system is solvable for every $\beta\in K^{n}$.

Take $\beta=\varepsilon_{1},\varepsilon_{2},\cdots,\varepsilon_{n}$ (the standard basis); then they can all be represented by $\alpha_{1},\cdots,\alpha_{n}$.

By **Definition 3.3.2 (Equivalence of Vector Groups)**, $\alpha_{1},\cdots,\alpha_{n}$ and $\varepsilon_{1},\cdots,\varepsilon_{n}$ are therefore equivalent (since $\alpha_{1},\cdots,\alpha_{n}$ can be represented by $\varepsilon_{1},\cdots,\varepsilon_{n}$ and vice versa).

By **Corollary 3.3.8 (Equivalent Vector Groups Have the Same Rank)**,

$$
\text{rank}\left\{\alpha_{1},\cdots,\alpha_{n}\right\}=\text{rank}\left\{\varepsilon_{1},\cdots,\varepsilon_{n}\right\}=n.
$$

By **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**, $n$ vectors in $K^{n}$ having rank $n$ shows they are linearly independent, so the determinant of the matrix they form is $\left|A\right|\ne0$.

**Sufficiency.** Suppose $\left|A\right|\ne0$; then $\alpha_{1},\cdots,\alpha_{n}$ are linearly independent.

In $K^{n}$, $n$ linearly independent vectors form a basis of $K^{n}$.

Hence every $\beta\in K^{n}$ can be represented by $\alpha_{1},\cdots,\alpha_{n}$, i.e. the system is solvable.

$\blacksquare$

---

## 3.3-11

Prove: two vector groups are equivalent if and only if they have the same rank and one of them can be linearly represented by the other.

### Solution 3.3-11

**Necessity.** Suppose the two vector groups (I) and (II) are equivalent.

By **Corollary 3.3.8 (Equivalent Vector Groups Have the Same Rank)**, equivalent groups have the same rank.

Moreover, equivalence means they can represent each other, so one group can be represented by the other.

**Sufficiency.** Suppose (I) and (II) have the same rank and (I) can be represented by (II).

Let a maximal linearly independent subset of (I) be $\alpha_{1},\cdots,\alpha_{r}$, and a maximal linearly independent subset of (II) be $\beta_{1},\cdots,\beta_{r}$.

Because (I) can be represented by (II), $\alpha_{1},\cdots,\alpha_{r}$ can be represented by $\beta_{1},\cdots,\beta_{r}$.

Also, $\alpha_{1},\cdots,\alpha_{r}$ are linearly independent with $r$ vectors, and $\beta_{1},\cdots,\beta_{r}$ are likewise $r$ linearly independent vectors.

By Problem 7 of Exercises 3.3, $r$ linearly independent vectors can represent all vectors in an $r$-dimensional space, so $\beta_{1},\cdots,\beta_{r}$ can be represented by $\alpha_{1},\cdots,\alpha_{r}$.

By **Definition 3.3.2 (Equivalence of Vector Groups)**, $\alpha_{1},\cdots,\alpha_{r}$ and $\beta_{1},\cdots,\beta_{r}$ are therefore equivalent.

Moreover, (I) is equivalent to $\alpha_{1},\cdots,\alpha_{r}$ and (II) is equivalent to $\beta_{1},\cdots,\beta_{r}$; by transitivity, (I) and (II) are equivalent.

$\blacksquare$
