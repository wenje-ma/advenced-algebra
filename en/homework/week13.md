# week13

> **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**<br>The vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ is linearly independent if and only if its rank equals the number $s$ of vectors it contains.

> **Definition 3.4.1 (Basis)**<br>Let $U$ be a subspace of $K^{n}$. A vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ in $U$ is called a basis of $U$ if it satisfies: $1^{\circ}$ it is linearly independent; $2^{\circ}$ every vector in $U$ can be linearly represented by it.

> **Theorem 3.4.8 (The Rank of a Vector Group Equals the Dimension of Its Spanning Subspace)**<br>A maximal linearly independent subset of the vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ in $K^{n}$ is a basis of the subspace $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\rangle$ spanned by this group, and hence

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}.
$$

---

## 3.4-2

Prove that the vector group in $K^{n}$

$$
\eta_{1}=\begin{bmatrix}1\\0\\0\\\vdots\\0\end{bmatrix},
\eta_{2}=\begin{bmatrix}1\\1\\0\\\vdots\\0\end{bmatrix},\cdots,
\eta_{n}=\begin{bmatrix}1\\1\\1\\\vdots\\1\end{bmatrix}
$$

is a basis of $K^{n}$.

### Solution 3.4-2

By the requirements of **Definition 3.4.1 (Basis)**, it suffices to verify two conditions: linear independence, and that it can linearly represent every vector in $K^{n}$.

**Verify linear independence.** Set

$$
k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{n}\eta_{n}=0.
$$

Comparing components (from the $1$st to the $n$th):

$1$st component: $k_{1}=0$.

$2$nd component: $k_{1}+k_{2}=0$; substituting $k_{1}=0$ gives $k_{2}=0$.

$3$rd component: $k_{1}+k_{2}+k_{3}=0$; substituting $k_{1}=k_{2}=0$ gives $k_{3}=0$.

Continuing, the $i$th component gives $k_{i}=0$.

Hence $\eta_{1},\eta_{2},\cdots,\eta_{n}$ are linearly independent.

**Verify representability.** Take any

$$
\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)^{\top}\in K^{n},
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

---

## 3.4-3(3)

Determine whether the following vector group is a basis of $K^{3}$:

$$
\alpha_{1}=\begin{bmatrix}1\\0\\1\end{bmatrix},
\alpha_{2}=\begin{bmatrix}0\\4\\-1\end{bmatrix},
\alpha_{3}=\begin{bmatrix}2\\-4\\3\end{bmatrix}.
$$

### Solution 3.4-3(3)

By the requirements of **Definition 3.4.1 (Basis)**, to determine whether three $3$-dimensional vectors form a basis of $K^{3}$ is equivalent to determining whether they are linearly independent, i.e. whether the determinant of the matrix they form is nonzero.

$$
\left|\begin{array}{rrr}
1 & 0 & 2\\
0 & 4 & -4\\
1 & -1 & 3
\end{array}\right|
=1\times\left(4\times3-\left(-4\right)\times\left(-1\right)\right)-0+2\times\left(0\times\left(-1\right)-4\times1\right)
$$

$$
=1\times\left(12-4\right)+2\times\left(-4\right)=8-8=0.
$$

The determinant is $0$; by **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**, $\alpha_{1},\alpha_{2},\alpha_{3}$ are therefore linearly dependent, failing the "linearly independent" requirement of **Definition 3.4.1 (Basis)**, and are not a basis of $K^{3}$. $\blacksquare$

---

## 3.4-4

Let $U$ be an $r$-dimensional subspace of $K^{n}$, and let $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ be $r$ vectors in $U$. Prove that if every vector in $U$ can be linearly represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$, then $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ is a basis of $U$.

### Solution 3.4-4

By the requirements of **Definition 3.4.1 (Basis)**, it suffices to verify two conditions: linear independence, and that every vector in $U$ can be represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$. The second condition is given, so only linear independence needs verification.

Because every vector in $U$ can be represented by $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$, we have $U\subseteq\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

Also, since $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\in U$ and $U$ is a subspace, $\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle\subseteq U$.

Hence $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

By **Theorem 3.4.8 (The Rank of a Vector Group Equals the Dimension of Its Spanning Subspace)**,

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}.
$$

Since $\dim U=r$,

$$
\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}=r.
$$

By **Proposition 3.3.6 (Linear Independence iff Rank Equals the Number of Vectors)**, the rank of $r$ vectors being $r$ shows they are linearly independent.

Thus $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ are linearly independent, and every vector in $U$ can be represented by them.

By **Definition 3.4.1 (Basis)**, $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ is a basis of $U$. $\blacksquare$
