# Assignment 31

> **Theorem 1** (Eigenvalues of Real Symmetric Matrices)<br>Every root in the complex number field of the characteristic polynomial of a real symmetric matrix is a real number.

> **Theorem 3** (Real Symmetric Matrices Are Orthogonally Diagonalizable)<br>For any real symmetric matrix $A$ of order $n$, there always exists an orthogonal matrix $T$ of order $n$ such that $T^{-1}AT$ is a diagonal matrix.

### Problem 1

(Problem 5.7-1(1)) For the following real symmetric matrix $A$, find an orthogonal matrix $T$ such that $T^{T}AT$ is a diagonal matrix:

$$
A=\left[\begin{array}{rrr}
0 & -2 & 2\\
-2 & -3 & 4\\
2 & 4 & -3
\end{array}\right].
$$

### Solution to Problem 1

By **Theorem 3** (Real Symmetric Matrices Are Orthogonally Diagonalizable), there always exists an orthogonal matrix $T$ such that $T^{T}AT$ is a diagonal matrix. Find the characteristic polynomial:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda & 2 & -2\\
2 & \lambda+3 & -4\\
-2 & -4 & \lambda+3
\end{array}\right|=\left(\lambda-1\right)^{2}\left(\lambda+8\right).
$$

Therefore the eigenvalues are $\lambda_{1}=\lambda_{2}=1$, $\lambda_{3}=-8$.

**Find eigenvectors for $\lambda=1$**.

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

A fundamental system of solutions: $\alpha_{1}=\left(-2,1,0\right)^{T}$, $\alpha_{2}=\left(2,0,1\right)^{T}$.

Apply the Gram–Schmidt orthogonalization:

$$
\beta_{1}=\alpha_{1}=\left(-2,1,0\right)^{T}.
$$

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}
=\left(2,0,1\right)^{T}-\frac{-4}{5}\left(-2,1,0\right)^{T}
=\left(\frac{2}{5},\frac{4}{5},1\right)^{T}.
$$

Normalize:

$$
\eta_{1}=\left(-\frac{2}{\sqrt{5}},\frac{1}{\sqrt{5}},0\right)^{T}.
$$

$$
\eta_{2}=\left(\frac{2}{3\sqrt{5}},\frac{4}{3\sqrt{5}},\frac{\sqrt{5}}{3}\right)^{T}.
$$

**Find eigenvectors for $\lambda=-8$**.

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

A fundamental system of solutions: $\alpha_{3}=\left(-1,2,-4\right)^{T}$.

Normalize:

$$
\eta_{3}=\left(-\frac{1}{\sqrt{21}},\frac{2}{\sqrt{21}},-\frac{4}{\sqrt{21}}\right)^{T}.
$$

Therefore the orthogonal matrix is

$$
T=\left[\begin{array}{ccc}
-2/\sqrt{5} & 2/\left(3\sqrt{5}\right) & -1/\sqrt{21}\\
1/\sqrt{5} & 4/\left(3\sqrt{5}\right) & 2/\sqrt{21}\\
0 & \sqrt{5}/3 & -4/\sqrt{21}
\end{array}\right].
$$

By **Theorem 3** (Real Symmetric Matrices Are Orthogonally Diagonalizable),

$$
T^{T}AT=\operatorname{diag}\left\{1,1,-8\right\}.
$$

$\blacksquare$

### Problem 2

(Problem 5.7-1(3)) For the following real symmetric matrix $A$, find an orthogonal matrix $T$ such that $T^{T}AT$ is a diagonal matrix:

$$
A=\left[\begin{array}{rrr}
3 & -2 & 0\\
-2 & 2 & -2\\
0 & -2 & 1
\end{array}\right].
$$

### Solution to Problem 2

Find the characteristic polynomial:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-3 & 2 & 0\\
2 & \lambda-2 & 2\\
0 & 2 & \lambda-1
\end{array}\right|=\left(\lambda+1\right)\left(\lambda-2\right)\left(\lambda-5\right).
$$

Therefore the eigenvalues are $\lambda_{1}=-1$, $\lambda_{2}=2$, $\lambda_{3}=5$.

**Find eigenvectors for $\lambda=-1$**.

A fundamental system of solutions: $\alpha_{1}=\left(1,2,2\right)^{T}$.

**Find eigenvectors for $\lambda=2$**.

A fundamental system of solutions: $\alpha_{2}=\left(2,1,-2\right)^{T}$.

**Find eigenvectors for $\lambda=5$**.

A fundamental system of solutions: $\alpha_{3}=\left(-2,2,-1\right)^{T}$.

Verify orthogonality: $\left(\alpha_{1},\alpha_{2}\right)=0$, $\left(\alpha_{1},\alpha_{3}\right)=0$, $\left(\alpha_{2},\alpha_{3}\right)=0$.

Normalize:

$$
\eta_{1}=\left(\frac{1}{3},\frac{2}{3},\frac{2}{3}\right)^{T}.
$$

$$
\eta_{2}=\left(\frac{2}{3},\frac{1}{3},-\frac{2}{3}\right)^{T}.
$$

$$
\eta_{3}=\left(-\frac{2}{3},\frac{2}{3},-\frac{1}{3}\right)^{T}.
$$

Therefore the orthogonal matrix is

$$
T=\left[\begin{array}{rrr}
1/3 & 2/3 & -2/3\\
2/3 & 1/3 & 2/3\\
2/3 & -2/3 & -1/3
\end{array}\right].
$$

$$
T^{T}AT=\operatorname{diag}\left\{-1,2,5\right\}.
$$

$\blacksquare$

### Problem 3

(Problem 5.7-2) Prove: if two real symmetric matrices $A,B$ of order $n$ have the same characteristic polynomial, then $A$ and $B$ are similar.

### Solution to Problem 3

Since $A$ is a real symmetric matrix, $A$ is orthogonally similar to a diagonal matrix $D_{A}$, and the diagonal entries of $D_{A}$ are all the eigenvalues of $A$ (counting multiplicities).

Similarly, $B$ is orthogonally similar to a diagonal matrix $D_{B}$, and the diagonal entries of $D_{B}$ are all the eigenvalues of $B$ (counting multiplicities).

Since $A,B$ have the same characteristic polynomial, they have the same eigenvalues (counting multiplicities).

Therefore the diagonal entries of $D_{A}$ and $D_{B}$ are the same (up to ordering).

By permuting the order of the diagonal entries of $D_{B}$, we can make $D_{A}=D_{B}$.

Permuting the diagonal entries amounts to a similarity transformation by an orthogonal matrix $Q$: $Q^{T}D_{B}Q=D_{A}$.

Therefore

$$
A\sim D_{A}=D_{B}\sim B.
$$

Hence $A$ and $B$ are similar. $\blacksquare$

### Problem 4

(Problem 5.7-3) Prove: if a real matrix $A$ is orthogonally similar to a diagonal matrix, then $A$ must be a symmetric matrix.

### Solution to Problem 4

Let $A$ be orthogonally similar to a diagonal matrix $D$, i.e. there exists an orthogonal matrix $T$ such that

$$
T^{T}AT=D.
$$

Then

$$
A=TDT^{T}.
$$

Since $D$ is a diagonal matrix, $D^{T}=D$.

Therefore

$$
A^{T}=\left(TDT^{T}\right)^{T}=TD^{T}T^{T}=TDT^{T}=A.
$$

Hence $A$ is a symmetric matrix. $\blacksquare$
