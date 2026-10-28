# week31

> **Basic Knowledge: The Schmidt Orthogonalization Process**<br>For a linearly independent vector group $\alpha_{1},\alpha_{2},\cdots,\alpha_{m}$, set $\beta_{1}=\alpha_{1}$ and, for $i\ge2$, recursively define

$$
\beta_{i}=\alpha_{i}-\sum_{k=1}^{i-1}\frac{\left(\alpha_{i},\beta_{k}\right)}{\left(\beta_{k},\beta_{k}\right)}\beta_{k}.
$$

Then $\beta_{1},\beta_{2},\cdots,\beta_{m}$ is an orthogonal vector group equivalent to the original one.

> **Theorem 5.7.1 (Eigenvalues of a Real Symmetric Matrix)**<br>Every root of the characteristic polynomial of a real symmetric matrix, over the complex number field, is a real number.

> **Theorem 5.7.3 (A Real Symmetric Matrix Is Orthogonally Diagonalizable)**<br>For any $n\times n$ real symmetric matrix $A$, there exists an $n\times n$ orthogonal matrix $T$ such that $T^{-1}AT$ is a diagonal matrix.

---

## 5.7-1(1)

For the following real symmetric matrix $A$, find an orthogonal matrix $T$ such that $T^{\top}AT$ is diagonal:

$$
A=\left[\begin{array}{rrr}
0 & -2 & 2\\
-2 & -3 & 4\\
2 & 4 & -3
\end{array}\right].
$$

### Solution 5.7-1(1)

By **Theorem 5.7.3 (A Real Symmetric Matrix Is Orthogonally Diagonalizable)**, there is an orthogonal matrix $T$ such that $T^{\top}AT$ is diagonal. Compute the characteristic polynomial:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda & 2 & -2\\
2 & \lambda+3 & -4\\
-2 & -4 & \lambda+3
\end{array}\right|=\left(\lambda-1\right)^{2}\left(\lambda+8\right).
$$

Thus the eigenvalues are $\lambda_{1}=\lambda_{2}=1$ and $\lambda_{3}=-8$.

**Find the eigenvectors for $\lambda=1$.**

$$
I-A=\left[\begin{array}{rrr}
1 & 2 & -2\\
2 & 4 & -4\\
-2 & -4 & 4
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & 2 & -2\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

A fundamental solution system: $\alpha_{1}=\left(-2,1,0\right)^{\top}$, $\alpha_{2}=\left(2,0,1\right)^{\top}$.

By **Basic Knowledge: The Schmidt Orthogonalization Process**:

$$
\beta_{1}=\alpha_{1}=\left(-2,1,0\right)^{\top}.
$$

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}
=\left(2,0,1\right)^{\top}-\frac{-4}{5}\left(-2,1,0\right)^{\top}
=\left(\frac{2}{5},\frac{4}{5},1\right)^{\top}.
$$

Normalize:

$$
\eta_{1}=\left(-\frac{2}{\sqrt{5}},\frac{1}{\sqrt{5}},0\right)^{\top}.
$$

$$
\eta_{2}=\left(\frac{2}{3\sqrt{5}},\frac{4}{3\sqrt{5}},\frac{\sqrt{5}}{3}\right)^{\top}.
$$

**Find the eigenvectors for $\lambda=-8$.**

$$
-8I-A=\left[\begin{array}{rrr}
-8 & 2 & -2\\
2 & -5 & -4\\
-2 & -4 & -5
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & 0 & 1/2\\
0 & 1 & 1\\
0 & 0 & 0
\end{array}\right].
$$

A fundamental solution system: $\alpha_{3}=\left(-1,2,-4\right)^{\top}$.

Normalize:

$$
\eta_{3}=\left(-\frac{1}{\sqrt{21}},\frac{2}{\sqrt{21}},-\frac{4}{\sqrt{21}}\right)^{\top}.
$$

Thus the orthogonal matrix is

$$
T=\left[\begin{array}{ccc}
-2/\sqrt{5} & 2/\left(3\sqrt{5}\right) & -1/\sqrt{21}\\
1/\sqrt{5} & 4/\left(3\sqrt{5}\right) & 2/\sqrt{21}\\
0 & \sqrt{5}/3 & -4/\sqrt{21}
\end{array}\right].
$$

By **Theorem 5.7.3 (A Real Symmetric Matrix Is Orthogonally Diagonalizable)**,

$$
T^{\top}AT=\operatorname{diag}\left\{1,1,-8\right\}.
$$

$\blacksquare$

---

## 5.7-1(3)

For the following real symmetric matrix $A$, find an orthogonal matrix $T$ such that $T^{\top}AT$ is diagonal:

$$
A=\left[\begin{array}{rrr}
3 & -2 & 0\\
-2 & 2 & -2\\
0 & -2 & 1
\end{array}\right].
$$

### Solution 5.7-1(3)

Compute the characteristic polynomial:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-3 & 2 & 0\\
2 & \lambda-2 & 2\\
0 & 2 & \lambda-1
\end{array}\right|=\left(\lambda+1\right)\left(\lambda-2\right)\left(\lambda-5\right).
$$

Thus the eigenvalues are $\lambda_{1}=-1$, $\lambda_{2}=2$ and $\lambda_{3}=5$.

**Find the eigenvectors for $\lambda=-1$.**

A fundamental solution system: $\alpha_{1}=\left(1,2,2\right)^{\top}$.

**Find the eigenvectors for $\lambda=2$.**

A fundamental solution system: $\alpha_{2}=\left(2,1,-2\right)^{\top}$.

**Find the eigenvectors for $\lambda=5$.**

A fundamental solution system: $\alpha_{3}=\left(-2,2,-1\right)^{\top}$.

Verify orthogonality: $\left(\alpha_{1},\alpha_{2}\right)=0$, $\left(\alpha_{1},\alpha_{3}\right)=0$, $\left(\alpha_{2},\alpha_{3}\right)=0$.

Normalize:

$$
\eta_{1}=\left(\frac{1}{3},\frac{2}{3},\frac{2}{3}\right)^{\top}.
$$

$$
\eta_{2}=\left(\frac{2}{3},\frac{1}{3},-\frac{2}{3}\right)^{\top}.
$$

$$
\eta_{3}=\left(-\frac{2}{3},\frac{2}{3},-\frac{1}{3}\right)^{\top}.
$$

Thus the orthogonal matrix is

$$
T=\left[\begin{array}{rrr}
1/3 & 2/3 & -2/3\\
2/3 & 1/3 & 2/3\\
2/3 & -2/3 & -1/3
\end{array}\right].
$$

$$
T^{\top}AT=\operatorname{diag}\left\{-1,2,5\right\}.
$$

$\blacksquare$

---

## 5.7-2

Prove: if $n\times n$ real symmetric matrices $A,B$ have the same characteristic polynomial, then $A$ and $B$ are similar.

### Solution 5.7-2

Since $A$ is real symmetric, by **Theorem 5.7.3 (A Real Symmetric Matrix Is Orthogonally Diagonalizable)**, $A$ is orthogonally similar to a diagonal matrix $D_{A}$, whose diagonal entries are all eigenvalues of $A$ (with multiplicity).

Similarly, $B$ is orthogonally similar to a diagonal matrix $D_{B}$, whose diagonal entries are all eigenvalues of $B$ (with multiplicity).

Since $A,B$ have the same characteristic polynomial, they have the same eigenvalues (with multiplicity).

Hence the diagonal entries of $D_{A}$ and $D_{B}$ agree (up to order).

By permuting the diagonal entries of $D_{B}$, we can make $D_{A}=D_{B}$.

Permuting the diagonal entries amounts to a similarity transformation by an orthogonal matrix $Q$: $Q^{\top}D_{B}Q=D_{A}$.

Therefore

$$
A\sim D_{A}=D_{B}\sim B.
$$

Hence $A$ and $B$ are similar. $\blacksquare$

---

## 5.7-3

Prove: if a real matrix $A$ is orthogonally similar to a diagonal matrix, then $A$ must be symmetric.

### Solution 5.7-3

Suppose $A$ is orthogonally similar to a diagonal matrix $D$, i.e. there is an orthogonal matrix $T$ such that

$$
T^{\top}AT=D.
$$

Then

$$
A=TDT^{\top}.
$$

Since $D$ is diagonal, $D^{\top}=D$.

Therefore

$$
A^{\top}=\left(TDT^{\top}\right)^{\top}=TD^{\top}T^{\top}=TDT^{\top}=A.
$$

Hence $A$ is symmetric. $\blacksquare$
