# week17

> **Definition 5.4.1 (Similarity)**
> 
> Let $A$ and $B$ both be $n\times{n}$ matrices over a number field $K$. If there exists an $n\times{n}$ invertible matrix $P$ over $K$ such that $P^{-1}AP=B$, then $A$ and $B$ are called similar, denoted $A\sim{B}$.

> **Theorem 5.4.2 (Necessary and Sufficient Condition for Diagonalizability)**
> 
> An $n\times{n}$ matrix $A$ over a number field $K$ is similar to a diagonal matrix if and only if there are $n$ linearly independent column vectors $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ in $K^{n}$ and $n$ scalars $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ in $K$ such that $A\alpha_{i}=\lambda_{i}\alpha_{i}$ ( $i=1,2,\cdots,n$ ).

> **Definition 5.5.1 (Eigenvalue and Eigenvector)**
> 
> Let $A$ be an $n\times{n}$ matrix over a number field $K$. If there is a nonzero column vector $\alpha$ in $K^{n}$ such that $A\alpha=\lambda_{0}\alpha$ with $\lambda_{0}\in{K}$, then $\lambda_{0}$ is called an eigenvalue of $A$, and $\alpha$ is called an eigenvector of $A$ belonging to the eigenvalue $\lambda_{0}$.

## 5.4-3

Prove: if $A_{1}\sim{B}_{1}$ and $A_{2}\sim{B}_{2}$, then

$$
\left[\begin{array}{cc}A_{1}&0\\0&A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1}&0\\0&B_{2}\end{array}\right].
$$

### Solution to 5.4-3

By **Definition 5.4.1 (Similarity)**, since $A_{1}\sim{B}_{1}$, there is an invertible matrix $P_{1}$ such that $P_{1}^{-1}A_{1}P_{1}=B_{1}$.

Similarly, there is an invertible matrix $P_{2}$ such that $P_{2}^{-1}A_{2}P_{2}=B_{2}$.

Set

$$
P=\left[\begin{array}{cc}P_{1}&0\\0&P_{2}\end{array}\right].
$$

Since $P_{1},P_{2}$ are invertible, $P$ is invertible and

$$
P^{-1}=\left[\begin{array}{cc}P_{1}^{-1}&0\\0&P_{2}^{-1}\end{array}\right].
$$

Compute:

$$
P^{-1}\left[\begin{array}{cc}A_{1}&0\\0&A_{2}\end{array}\right]P
=\left[\begin{array}{cc}P_{1}^{-1}&0\\0&P_{2}^{-1}\end{array}\right]\left[\begin{array}{cc}A_{1}&0\\0&A_{2}\end{array}\right]\left[\begin{array}{cc}P_{1}&0\\0&P_{2}\end{array}\right]=\left[\begin{array}{cc}P_{1}^{-1}A_{1}P_{1}&0\\0&P_{2}^{-1}A_{2}P_{2}\end{array}\right]=\left[\begin{array}{cc}B_{1}&0\\0&B_{2}\end{array}\right].
$$

Thus, by **Definition 5.4.1 (Similarity)**,

$$
\left[\begin{array}{cc}A_{1}&0\\0&A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1}&0\\0&B_{2}\end{array}\right].
$$

$\blacksquare$

## 5.4-8

Prove: if $A$ is diagonalizable, then $A\sim{A}^{\top}$.

### Solution to 5.4-8

By **Theorem 5.4.2 (Necessary and Sufficient Condition for Diagonalizability)**, since $A$ is diagonalizable, there is an invertible matrix $P$ such that

$$
P^{-1}AP=D,
$$

where $D$ is diagonal.

The transpose of a diagonal matrix is still diagonal, i.e. $D^{\top}=D$.

Taking transposes on both sides:

$$
\left(P^{-1}AP\right)^{\top}=D^{\top}=D.
$$

That is,

$$
P^{\top}A^{\top}\left(P^{-1}\right)^{\top}=D.
$$

Set $Q=\left(P^{\top}\right)^{-1}$. Then $Q^{-1}=P^{\top}$.

The equation becomes

$$
Q^{-1}A^{\top}Q=D.
$$

Therefore

$$
A^{\top}\sim{D}.
$$

Since also $A\sim{D}$, by symmetry and transitivity of similarity,

$$
A\sim{A}^{\top}.
$$

$\blacksquare$

## 5.4-9

Prove: if $n\times{n}$ matrices $A,B$ over a number field $K$ satisfy

$$
AB-BA=A,
$$

then $A$ is not invertible.

### Solution to 5.4-9

By Invariants of Similar Matrices, similar matrices have equal traces. Suppose, for contradiction, that $A$ is invertible.

From $AB-BA=A$, multiply on the left by $A^{-1}$:

$$
A^{-1}AB-A^{-1}BA=A^{-1}A.
$$

That is,

$$
B-A^{-1}BA=I.
$$

Set $C=A^{-1}BA$. Then $B-C=I$.

Taking traces on both sides:

$$
\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(I\right)=n.
$$

On the other hand, by Invariants of Similar Matrices,

$$
\operatorname{tr}\left(C\right)=\operatorname{tr}\left(A^{-1}BA\right)=\operatorname{tr}\left(BAA^{-1}\right)=\operatorname{tr}\left(B\right).
$$

Therefore

$$
\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(B\right)-\operatorname{tr}\left(C\right)=0.
$$

This is a contradiction.

Hence the assumption fails, and $A$ is not invertible. $\blacksquare$

## 5.4-12

A square matrix $A$ is called nilpotent if some positive integral power of $A$ is the zero matrix; the smallest positive integer $l$ such that $A^{l}=0$ is called the nilpotent index of $A$. Prove: a matrix similar to a nilpotent matrix is also nilpotent, and their nilpotent indices are equal.

### Solution to 5.4-12

Let $A$ be nilpotent with nilpotent index $l$, i.e. $A^{l}=0$ and $A^{k}\ne0$ for $k<{}l$.

Let $B\sim{A}$, i.e. there is an invertible matrix $P$ such that $B=P^{-1}AP$.

Prove that $B$ is nilpotent.

$$
B^{l}=\left(P^{-1}AP\right)^{l}=P^{-1}A^{l}P=P^{-1}0P=0.
$$

Therefore $B$ is nilpotent.

Prove that the nilpotent index of $B$ equals $l$.

Let the nilpotent index of $B$ be $m$, i.e. $B^{m}=0$.

Then

$$
B^{m}=\left(P^{-1}AP\right)^{m}=P^{-1}A^{m}P=0.
$$

Multiply on the left by $P$ and on the right by $P^{-1}$:

$$
A^{m}=0.
$$

Since the nilpotent index of $A$ is $l$, $m\ge{l}$.

On the other hand, $A^{l}=0$, so

$$
B^{l}=P^{-1}A^{l}P=0.
$$

Since the nilpotent index of $B$ is $m$, $l\ge{m}$.

Therefore $m=l$.

Thus a matrix similar to a nilpotent matrix is also nilpotent, and their nilpotent indices are equal. $\blacksquare$

## 5.5-1(2)

Find all eigenvalues and eigenvectors of the following matrix $A$ over a number field $K$:

$$
A=\left[\begin{array}{rrr}
2&3&2\\
1&8&2\\
-2&-14&-3
\end{array}\right].
$$

### Solution to 5.5-1(2)

By **Definition 5.5.1 (Eigenvalue and Eigenvector)**, compute the characteristic polynomial:

$$
\left|\lambda{I}-A\right|=\left|\begin{array}{rrr}
\lambda-2&-3&-2\\
-1&\lambda-8&-2\\
2&14&\lambda+3
\end{array}\right|.
$$

Expanding along the first row:

$$
\left|\lambda{I}-A\right|
=\left(\lambda-2\right)\left[\left(\lambda-8\right)\left(\lambda+3\right)+28\right]+3\left[-\left(\lambda+3\right)+4\right]-2\left[-14-2\left(\lambda-8\right)\right]=\left(\lambda-2\right)\left(\lambda^{2}-5\lambda+4\right)+3\left(-\lambda+1\right)-2\left(2-2\lambda\right)=\left(\lambda-2\right)\left(\lambda-1\right)\left(\lambda-4\right)-3\lambda+3-4+4\lambda=\left(\lambda-1\right)\left[\left(\lambda-2\right)\left(\lambda-4\right)+1\right]=\left(\lambda-1\right)\left(\lambda^{2}-6\lambda+9\right)=\left(\lambda-1\right)\left(\lambda-3\right)^{2}.
$$

Thus the eigenvalues are $\lambda_{1}=1$ and $\lambda_{2}=\lambda_{3}=3$.

Find the eigenvectors for $\lambda=1$.

$$
I-A=\left[\begin{array}{rrr}
-1&-3&-2\\
-1&-7&-2\\
2&14&4
\end{array}\right]arrow
\left[\begin{array}{rrr}
-1&-3&-2\\
0&-4&0\\
0&0&0
\end{array}\right].
$$

Solving gives $x_{2}=0$ and $x_{1}=-2x_{3}$.

A fundamental solution system: $\alpha_{1}=\left(-2,0,1\right)^{\top}$.

Find the eigenvectors for $\lambda=3$.

$$
3I-A=\left[\begin{array}{rrr}
1&-3&-2\\
-1&-5&-2\\
2&14&6
\end{array}\right]arrow
\left[\begin{array}{rrr}
1&-3&-2\\
0&-8&-4\\
0&0&0
\end{array}\right].
$$

Solving gives $x_{2}=-\frac{1}{2}x_{3}$ and $x_{1}=\frac{1}{2}x_{3}$.

A fundamental solution system: $\alpha_{2}=\left(1,-1,2\right)^{\top}$.

The eigenvectors for $\lambda_{1}=1$ are $k_{1}\alpha_{1}$ ( $k_{1}\ne0$ ), and those for $\lambda_{2}=\lambda_{3}=3$ are $k_{2}\alpha_{2}$ ( $k_{2}\ne0$ ). $\blacksquare$

## 5.5-2(2)

Find all eigenvalues and eigenvectors of the following matrix $A$ over the complex number field. If $A$ is regarded as a matrix over the real number field, does it have eigenvalues? How many?

$$
A=\left[\begin{array}{rrr}
3&7&-3\\
-2&-5&2\\
-4&-10&3
\end{array}\right].
$$

### Solution to 5.5-2(2)

By **Definition 5.5.1 (Eigenvalue and Eigenvector)**, compute the characteristic polynomial:

$$
\left|\lambda{I}-A\right|=\left|\begin{array}{rrr}
\lambda-3&-7&3\\
2&\lambda+5&-2\\
4&10&\lambda-3
\end{array}\right|.
$$

Expanding along the first row:

$$
\left|\lambda{I}-A\right|
=\left(\lambda-3\right)\left[\left(\lambda+5\right)\left(\lambda-3\right)+20\right]+7\left[2\left(\lambda-3\right)+8\right]+3\left[20-4\left(\lambda+5\right)\right]=\left(\lambda-3\right)\left(\lambda^{2}+2\lambda+5\right)+7\left(2\lambda+2\right)+3\left(-4\lambda\right)=\lambda^{3}-3\lambda^{2}+2\lambda^{2}-6\lambda+5\lambda-15+14\lambda+14-12\lambda=\lambda^{3}-\lambda^{2}+\lambda-1=\left(\lambda-1\right)\left(\lambda^{2}+1\right).
$$

Thus the eigenvalues are $\lambda_{1}=1$, $\lambda_{2}=i$ and $\lambda_{3}=-i$.

By **Definition 5.5.1 (Eigenvalue and Eigenvector)**, regarding $A$ as a real matrix, only $\lambda=1$ is a real eigenvalue, so it has $1$ eigenvalue.

$\blacksquare$

## 5.5-10

Let $A$ be an $n\times{n}$ orthogonal matrix. Prove:

(1) if $A$ has eigenvalues, they are $1$ or $-1$;

(2) if $n$ is odd and $\left|A\right|=1$, then $1$ is an eigenvalue of $A$;

(3) if $\left|A\right|=-1$, then $-1$ is an eigenvalue of $A$.

### Solution to 5.5-10

(1) Let $\lambda$ be an eigenvalue of $A$ and $\alpha$ an eigenvector of $A$ belonging to $\lambda$, i.e. $A\alpha=\lambda\alpha$.

Taking the conjugate transpose on both sides: $\alpha^{\top}A^{\top}=\overline{\lambda}\alpha^{\top}$.

Since $A$ is orthogonal, $A^{\top}=A^{-1}$.

Hence $\alpha^{\top}A^{-1}=\overline{\lambda}\alpha^{\top}$.

Multiply on the right by $A\alpha$:

$$
\alpha^{\top}A^{-1}A\alpha=\overline{\lambda}\alpha^{\top}A\alpha.
$$

That is,

$$
\alpha^{\top}\alpha=\overline{\lambda}\lambda\alpha^{\top}\alpha.
$$

Since $\alpha\ne0$, $\alpha^{\top}\alpha\ne0$.

Therefore

$$
1=\overline{\lambda}\lambda=\left|\lambda\right|^{2}.
$$

Hence $\left|\lambda\right|=1$.

If $\lambda$ is a real eigenvalue, then $\lambda=\pm1$.

(2) $A$ is an $n\times{n}$ orthogonal matrix and $n$ is odd.

Complex eigenvalues occur in conjugate pairs, so the number of complex eigenvalues is even.

Since $n$ is odd, the number of real eigenvalues is odd.

Real eigenvalues can only be $\pm1$.

Suppose $A$ has $k$ copies of $1$, $m$ copies of $-1$, and some complex eigenvalues.

$$
\left|A\right|=1^{k}\cdot\left(-1\right)^{m}\cdot\left(\text{product~of~complex~eigenvalues}\right).
$$

Complex eigenvalues occur in conjugate pairs, and each pair has product $\left|\lambda\right|^{2}=1$.

Thus $\left|A\right|=\left(-1\right)^{m}$.

Given $\left|A\right|=1$, $\left(-1\right)^{m}=1$, i.e. $m$ is even.

Since $k+m$ is odd (the number of real eigenvalues) and $m$ is even, $k$ is odd, i.e. $k\ge1$.

Therefore $1$ is an eigenvalue of $A$.

(3) $\left|A\right|=\left(-1\right)^{m}=-1$, so $m$ is odd, i.e. $m\ge1$.

Therefore $-1$ is an eigenvalue of $A$.

$\blacksquare$
