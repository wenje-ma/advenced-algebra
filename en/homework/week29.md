# Assignment 29

> **Definition 1** (Eigenvalues and Eigenvectors)<br>Let $A$ be an matrix of order $n$ over a number field $K$. If there exists a nonzero column vector $\alpha$ in $K^{n}$ such that $A\alpha=\lambda_{0}\alpha$ with $\lambda_{0}\in K$, then $\lambda_{0}$ is called an eigenvalue of $A$, and $\alpha$ is called an eigenvector of $A$ belonging to the eigenvalue $\lambda_{0}$.

> **Property** (Similarity Invariants)<br>Similar matrices have the same determinant, the same rank, the same trace, the same characteristic polynomial, and the same eigenvalues.

### Problem 1

(Problem 5.5-1(2)) Find all eigenvalues and eigenvectors of the following matrix $A$ over a number field $K$:

$$
A=\left[\begin{array}{rrr}
2 & 3 & 2\\
1 & 8 & 2\\
-2 & -14 & -3
\end{array}\right].
$$

### Solution to Problem 1

By **Definition 1** (Eigenvalues and Eigenvectors), find the characteristic polynomial:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-2 & -3 & -2\\
-1 & \lambda-8 & -2\\
2 & 14 & \lambda+3
\end{array}\right|.
$$

Expand along row $1$:

$$
\left|\lambda I-A\right|
=\left(\lambda-2\right)\left[\left(\lambda-8\right)\left(\lambda+3\right)+28\right]+3\left[-\left(\lambda+3\right)+4\right]-2\left[-14-2\left(\lambda-8\right)\right]=\left(\lambda-2\right)\left(\lambda^{2}-5\lambda+4\right)+3\left(-\lambda+1\right)-2\left(2-2\lambda\right)=\left(\lambda-2\right)\left(\lambda-1\right)\left(\lambda-4\right)-3\lambda+3-4+4\lambda=\left(\lambda-1\right)\left[\left(\lambda-2\right)\left(\lambda-4\right)+1\right]=\left(\lambda-1\right)\left(\lambda^{2}-6\lambda+9\right)=\left(\lambda-1\right)\left(\lambda-3\right)^{2}.
$$

Therefore the eigenvalues are $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=3$.

**Find eigenvectors for $\lambda=1$**.

$$
I-A=\left[\begin{array}{rrr}
-1 & -3 & -2\\
-1 & -7 & -2\\
2 & 14 & 4
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
-1 & -3 & -2\\
0 & -4 & 0\\
0 & 0 & 0
\end{array}\right].
$$

Solving gives $x_{2}=0$, $x_{1}=-2x_{3}$.

A fundamental system of solutions: $\alpha_{1}=\left(-2,0,1\right)^{T}$.

**Find eigenvectors for $\lambda=3$**.

$$
3I-A=\left[\begin{array}{rrr}
1 & -3 & -2\\
-1 & -5 & -2\\
2 & 14 & 6
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & -3 & -2\\
0 & -8 & -4\\
0 & 0 & 0
\end{array}\right].
$$

Solving gives $x_{2}=-\frac{1}{2}x_{3}$, $x_{1}=\frac{1}{2}x_{3}$.

A fundamental system of solutions: $\alpha_{2}=\left(1,-1,2\right)^{T}$.

The eigenvectors for $\lambda_{1}=1$ are $k_{1}\alpha_{1}$ ( $k_{1}\ne0$ ); the eigenvectors for $\lambda_{2}=\lambda_{3}=3$ are $k_{2}\alpha_{2}$ ( $k_{2}\ne0$ ). $\blacksquare$

### Problem 2

(Problem 5.5-2(2)) Find all eigenvalues and eigenvectors of the following matrix $A$ over the complex number field; if $A$ is regarded as a matrix over the real number field, does it have eigenvalues? How many?

$$
A=\left[\begin{array}{rrr}
3 & 7 & -3\\
-2 & -5 & 2\\
-4 & -10 & 3
\end{array}\right].
$$

### Solution to Problem 2

By **Definition 1** (Eigenvalues and Eigenvectors), find the characteristic polynomial:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-3 & -7 & 3\\
2 & \lambda+5 & -2\\
4 & 10 & \lambda-3
\end{array}\right|.
$$

Expand along row $1$:

$$
\left|\lambda I-A\right|
=\left(\lambda-3\right)\left[\left(\lambda+5\right)\left(\lambda-3\right)+20\right]+7\left[2\left(\lambda-3\right)+8\right]+3\left[20-4\left(\lambda+5\right)\right]=\left(\lambda-3\right)\left(\lambda^{2}+2\lambda+5\right)+7\left(2\lambda+2\right)+3\left(-4\lambda\right)=\lambda^{3}-3\lambda^{2}+2\lambda^{2}-6\lambda+5\lambda-15+14\lambda+14-12\lambda=\lambda^{3}-\lambda^{2}+\lambda-1=\left(\lambda-1\right)\left(\lambda^{2}+1\right).
$$

Therefore the eigenvalues are $\lambda_{1}=1$, $\lambda_{2}=i$, $\lambda_{3}=-i$.

By **Definition 1** (Eigenvalues and Eigenvectors), when $A$ is regarded as a matrix over the real number field, only $\lambda=1$ is a real eigenvalue, so there is $1$ eigenvalue.

$\blacksquare$

### Problem 3

(Problem 5.5-10) Let $A$ be an orthogonal matrix of order $n$. Prove:

(1) if $A$ has eigenvalues, then the eigenvalues of $A$ are $1$ or $-1$;

(2) if $n$ is odd and $\left|A\right|=1$, then $1$ is an eigenvalue of $A$;

(3) if $\left|A\right|=-1$, then $-1$ is an eigenvalue of $A$.

### Solution to Problem 3

**(1)** Let $\lambda$ be an eigenvalue of $A$, and let $\alpha$ be an eigenvector of $A$ belonging to $\lambda$, i.e. $A\alpha=\lambda\alpha$.

Take the conjugate transpose of both sides: $\alpha^{T}A^{T}=\overline{\lambda}\alpha^{T}$.

Since $A$ is orthogonal, $A^{T}=A^{-1}$.

Therefore $\alpha^{T}A^{-1}=\overline{\lambda}\alpha^{T}$.

Right-multiply both sides by $A\alpha$:

$$
\alpha^{T}A^{-1}A\alpha=\overline{\lambda}\alpha^{T}A\alpha.
$$

That is,

$$
\alpha^{T}\alpha=\overline{\lambda}\lambda\alpha^{T}\alpha.
$$

Since $\alpha\ne0$, we have $\alpha^{T}\alpha\ne0$.

Therefore

$$
1=\overline{\lambda}\lambda=\left|\lambda\right|^{2}.
$$

Hence $\left|\lambda\right|=1$.

If $\lambda$ is a real eigenvalue, then $\lambda=\pm1$.

**(2)** $A$ is an orthogonal matrix of order $n$ and $n$ is odd.

Complex eigenvalues occur in conjugate pairs, so the number of complex eigenvalues is even.

Since $n$ is odd, the number of real eigenvalues is odd.

Real eigenvalues can only be $\pm1$.

Suppose $A$ has $k$ copies of $1$, $m$ copies of $-1$, and some complex eigenvalues.

$$
\left|A\right|=1^{k}\cdot\left(-1\right)^{m}\cdot\left(\text{复特征值的乘积}\right).
$$

Complex eigenvalues come in conjugate pairs, and the product of each pair is $\left|\lambda\right|^{2}=1$.

Hence $\left|A\right|=\left(-1\right)^{m}$.

Given $\left|A\right|=1$, we have $\left(-1\right)^{m}=1$, i.e. $m$ is even.

Since $k+m$ is odd (the number of real eigenvalues) and $m$ is even, $k$ is odd, i.e. $k\ge1$.

Therefore $1$ is an eigenvalue of $A$.

**(3)** $\left|A\right|=\left(-1\right)^{m}=-1$, so $m$ is odd, i.e. $m\ge1$.

Therefore $-1$ is an eigenvalue of $A$.

$\blacksquare$

### Problem 4

(Problem 5.5-12(1)) Find all eigenvalues and eigenvectors of the following matrix over the complex number field:

$$
P=\left[\begin{array}{ccc}
0 & 1 & 0\\
0 & 0 & 1\\
1 & 0 & 0
\end{array}\right].
$$

### Solution to Problem 4

Find the characteristic polynomial:

$$
\left|\lambda I-P\right|=\left|\begin{array}{rrr}
\lambda & -1 & 0\\
0 & \lambda & -1\\
-1 & 0 & \lambda
\end{array}\right|=\lambda^{3}-1.
$$

Therefore the eigenvalues are $\lambda_{1}=1$, $\lambda_{2}=\omega$, $\lambda_{3}=\omega^{2}$, where

$$
\omega=e^{2\pi i/3}=-\frac{1}{2}+\frac{\sqrt{3}}{2}i
$$

**Find eigenvectors for $\lambda=1$**.

$$
I-P=\left[\begin{array}{rrr}
1 & -1 & 0\\
0 & 1 & -1\\
-1 & 0 & 1
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & -1 & 0\\
0 & 1 & -1\\
0 & 0 & 0
\end{array}\right].
$$

Solving gives $x_{1}=x_{2}=x_{3}$.

A fundamental system of solutions: $\alpha_{1}=\left(1,1,1\right)^{T}$.

**Find eigenvectors for $\lambda=\omega$**.

From row $1$: $\omega x_{1}-x_{2}=0$, i.e. $x_{2}=\omega x_{1}$.

From row $2$: $\omega x_{2}-x_{3}=0$, i.e. $x_{3}=\omega x_{2}=\omega^{2}x_{1}$.

A fundamental system of solutions: $\alpha_{2}=\left(1,\omega,\omega^{2}\right)^{T}$.

**Find eigenvectors for $\lambda=\omega^{2}$**.

Similarly, a fundamental system of solutions: $\alpha_{3}=\left(1,\omega^{2},\omega\right)^{T}$.

$\blacksquare$

### Problem 5

(Problem 5.5-13) Let $A,B$ be $s\times n$ and $n\times s$ matrices over a number field $K$, respectively. Prove: $AB$ and $BA$ have the same nonzero eigenvalues.

### Solution to Problem 5

Let $\lambda\ne0$ be an eigenvalue of $AB$, and let $\alpha$ be an eigenvector of $AB$ belonging to $\lambda$, i.e.

$$
AB\alpha=\lambda\alpha.
$$

Let $\beta=B\alpha$.

Then

$$
BA\beta=BA\left(B\alpha\right)=B\left(AB\alpha\right)=B\left(\lambda\alpha\right)=\lambda\left(B\alpha\right)=\lambda\beta.
$$

**Prove that $\beta\ne0$**.

If $\beta=0$, then $B\alpha=0$.

Then

$$
AB\alpha=A\left(0\right)=0.
$$

But $AB\alpha=\lambda\alpha$ with $\lambda\ne0$, so $\lambda\alpha=0$, and hence $\alpha=0$.

This is a contradiction, since $\alpha$ is an eigenvector and $\alpha\ne0$.

Therefore $\beta\ne0$.

Thus $\beta$ is an eigenvector of $BA$ belonging to $\lambda$.

Therefore $\lambda$ is an eigenvalue of $BA$.

By the same argument, every nonzero eigenvalue of $BA$ is also an eigenvalue of $AB$.

Therefore $AB$ and $BA$ have the same nonzero eigenvalues. $\blacksquare$
