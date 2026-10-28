# week10

> **Basic Knowledge: Criterion for a Subspace**<br>A nonempty subset $W$ of $K^{n}$ is a subspace if and only if it is closed under addition and scalar multiplication: namely, for any $\alpha,\beta\in W$ and $k\in K$, $\alpha+\beta\in W$ and $k\alpha\in W$.

> **Definition 3.1.1 (Linear Combination and Linear Representation)**<br>In $K^{n}$, given a vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ and any numbers $k_{1},k_{2},\cdots,k_{s}$ in $K$, we call $k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s}$ a linear combination of the vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$. If

$$
\beta=k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s},
$$

then we say that $\beta$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$.

> **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**<br>An $n$-variable linear system over a number field $K$

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

is solvable $\Leftrightarrow$ $\beta$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ $\Leftrightarrow$ $\beta\in\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\right\rangle$.

---

## 3.1-3(1)

In $K^{4}$, determine whether the vector $\beta$ can be linearly represented by the vector group $\alpha_{1},\alpha_{2},\alpha_{3}$. If so, write down one way of representing it.

$$
\alpha_{1}=\begin{bmatrix}-1\\3\\0\\-5\end{bmatrix},
\alpha_{2}=\begin{bmatrix}2\\0\\7\\-3\end{bmatrix},
\alpha_{3}=\begin{bmatrix}-4\\1\\-2\\6\end{bmatrix},
\beta=\begin{bmatrix}8\\3\\-1\\-25\end{bmatrix}.
$$

### Solution 3.1-3(1)

By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, to determine whether $\beta$ can be represented by $\alpha_{1},\alpha_{2},\alpha_{3}$ is to determine whether the linear system $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=\beta$ is solvable.

Write down the augmented matrix and perform elementary row operations:

$$
\left[\begin{array}{rrr|r}
-1 & 2 & -4 & 8\\
3 & 0 & 1 & 3\\
0 & 7 & -2 & -1\\
-5 & -3 & 6 & -25
\end{array}\right]
\xrightarrow{\substack{②+①\times3\\④-①\times5}}
\left[\begin{array}{rrr|r}
-1 & 2 & -4 & 8\\
0 & 6 & -11 & 27\\
0 & 7 & -2 & -1\\
0 & -13 & 26 & 15
\end{array}\right].
$$

Continuing the row operations, the last row becomes a contradictory row $0=80$, so the system has no solution.

By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, $\beta$ therefore cannot be linearly represented by $\alpha_{1},\alpha_{2},\alpha_{3}$. $\blacksquare$

---

## 3.1-3(3)

In $K^{4}$, determine whether the vector $\beta$ can be linearly represented by the vector group $\alpha_{1},\alpha_{2},\alpha_{3}$. If so, write down one way of representing it.

$$
\alpha_{1}=\begin{bmatrix}3\\-5\\2\\-4\end{bmatrix},
\alpha_{2}=\begin{bmatrix}-1\\7\\-3\\6\end{bmatrix},
\alpha_{3}=\begin{bmatrix}3\\11\\-5\\10\end{bmatrix},
\beta=\begin{bmatrix}2\\-30\\13\\-26\end{bmatrix}.
$$

### Solution 3.1-3(3)

By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, to determine whether $\beta$ can be represented by $\alpha_{1},\alpha_{2},\alpha_{3}$ is to determine whether the linear system $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=\beta$ is solvable.

Write down the augmented matrix and perform elementary row operations:

$$
\left[\begin{array}{rrr|r}
3 & -1 & 3 & 2\\
-5 & 7 & 11 & -30\\
2 & -3 & -5 & 13\\
-4 & 6 & 10 & -26
\end{array}\right]
\xrightarrow{\substack{②+①\times5/3\\③-①\times2/3\\④+①\times4/3}}
\left[\begin{array}{rrr|r}
3 & -1 & 3 & 2\\
0 & 16/3 & 16 & -80/3\\
0 & -7/3 & -7 & 35/3\\
0 & 14/3 & 14 & -70/3
\end{array}\right].
$$

Note that rows $2,3,4$ are proportional; after elimination the echelon matrix has only two rows:

$$
\left[\begin{array}{rrr|r}
3 & -1 & 3 & 2\\
0 & 16/3 & 16 & -80/3
\end{array}\right].
$$

From row $2$:

$$
\frac{16}{3}x_{2}+16x_{3}=-\frac{80}{3},
$$

i.e. $x_{2}+3x_{3}=-5$, so $x_{2}=-5-3x_{3}$.

From row $1$: $3x_{1}-x_{2}+3x_{3}=2$; substituting $x_{2}$ gives $3x_{1}+6x_{3}=-3$, so $x_{1}=-1-2x_{3}$.

Setting $x_{3}=0$ gives $x_{1}=-1$, $x_{2}=-5$.

Verify:

$$
-\alpha_{1}-5\alpha_{2}=\begin{bmatrix}-3+5\\5-35\\-2+15\\4-30\end{bmatrix}=\begin{bmatrix}2\\-30\\13\\-26\end{bmatrix}=\beta.
$$

Hence $\beta=-\alpha_{1}-5\alpha_{2}$. By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, the system is solvable, so $\beta$ can be linearly represented by $\alpha_{1},\alpha_{2},\alpha_{3}$. $\blacksquare$

---

## 3.1-5

In $K^{4}$, let

$$
\alpha_{1}=\begin{bmatrix}1\\0\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}1\\1\\1\\0\end{bmatrix},
\alpha_{4}=\begin{bmatrix}1\\1\\1\\1\end{bmatrix}.
$$

Prove that every vector $\alpha=\left(a_{1},a_{2},a_{3},a_{4}\right)^{\top}$ in $K^{4}$ can be linearly represented by the vector group $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$, that this representation is unique, and write it down.

### Solution 3.1-5

By **Proposition 3.1.1 (Relation Between Linear Representability and Solvability of a System)**, to prove that every vector $\alpha$ in $K^{4}$ can be represented by $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ is to prove that the linear system

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}=\alpha
$$

is solvable.

Set

$$
\alpha=x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}.
$$

Comparing components:

$4$th component: $x_{4}=a_{4}$.

$3$rd component: $x_{3}+x_{4}=a_{3}$, so $x_{3}=a_{3}-a_{4}$.

$2$nd component: $x_{2}+x_{3}+x_{4}=a_{2}$, so $x_{2}=a_{2}-a_{3}$.

$1$st component: $x_{1}+x_{2}+x_{3}+x_{4}=a_{1}$, so $x_{1}=a_{1}-a_{2}$.

The above solving process is uniquely determined from bottom to top, so the representation is unique.

The representation is

$$
\alpha=\left(a_{1}-a_{2}\right)\alpha_{1}+\left(a_{2}-a_{3}\right)\alpha_{2}+\left(a_{3}-a_{4}\right)\alpha_{3}+a_{4}\alpha_{4}.
$$

The system has a unique solution, so $\alpha$ can be uniquely linearly represented by $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$. $\blacksquare$

---

## 3.1-8

Let $r< n$. Prove that the following subset $W$ of $K^{n}$ is a subspace:

$$
W=\left\{\left(a_{1},a_{2},\cdots,a_{r},0,\cdots,0\right)\mid a_{i}\in K,i=1,2,\cdots,r\right\}.
$$

### Solution 3.1-8

By **Basic Knowledge: Criterion for a Subspace**, it suffices to verify that $W$ is nonempty and closed under addition and scalar multiplication.

**Verify closure under addition.** Take any

$$
\alpha=\left(a_{1},\cdots,a_{r},0,\cdots,0\right),
\beta=\left(b_{1},\cdots,b_{r},0,\cdots,0\right)\in W.
$$

Then

$$
\alpha+\beta=\left(a_{1}+b_{1},\cdots,a_{r}+b_{r},0,\cdots,0\right)\in W.
$$

**Verify closure under scalar multiplication.** Take any

$$
\alpha=\left(a_{1},\cdots,a_{r},0,\cdots,0\right)\in W
$$

and $k\in K$.

Then

$$
k\alpha=\left(ka_{1},\cdots,ka_{r},0,\cdots,0\right)\in W.
$$

$W$ is nonempty (e.g. the zero vector $\left(0,\cdots,0\right)\in W$).

By **Basic Knowledge: Criterion for a Subspace**, $W$ is a subspace of $K^{n}$. $\blacksquare$
