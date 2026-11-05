# week16

> **Definition 5.1.1 (Binary Relation)**
> 
> Let $S$ be a nonempty set. A subset $W$ of $S\times{S}$ is called a binary relation on $S$. If $\left(a,b\right)\in{W}$, we say $a$ and $b$ are in the relation $W$.

> **Definition 5.1.2 (Equivalence Relation)**
> 
> A binary relation $\sim$ on a set $S$ is called an equivalence relation if, for all $a,b,c\in{S}$: $1^{\circ}a\sim{a}$ (reflexivity); $2^{\circ}a\sim{b}\Rightarrow{b}\sim{a}$ (symmetry); $3^{\circ}a\sim{b}$ and $b\sim{c}\Rightarrow{a}\sim{c}$ (transitivity).

> **Definition 5.1.4 (Quotient Set)**
> 
> Let $\sim$ be an equivalence relation on a set $S$. The set consisting of all equivalence classes is called the quotient set of $S$ with respect to $\sim$, denoted $S/\sim$.

> **Definition 5.2.1 (Equivalence)**
> 
> A matrix $A$ over a number field $K$ is equivalent to a matrix $B$ if $A$ can be transformed into $B$ by a sequence of elementary row and column operations, denoted $A\sim{B}$.

> **Theorem 5.2.1 (Canonical Form under Equivalence)**
> 
> Let $A$ be an $s\times{n}$ matrix over a number field $K$ with rank $r$. If $r>0$, then $A$ is equivalent to a matrix of the form

$$
\left[\begin{array}{cc}I_{r}&0\\0&0\end{array}\right].
$$

> **Theorem 5.2.2 (Necessary and Sufficient Condition for Equivalence)**
> 
> Two $s\times{n}$ matrices $A$ and $B$ over a number field $K$ are equivalent if and only if they have the same rank.

> **Definition 5.3.1 (Generalized Inverse)**
> 
> Let $A$ be an $s\times{n}$ matrix over a number field $K$. If a matrix $G$ satisfies $AGA=A$, then $G$ is called a generalized inverse of $A$, denoted $A^{-}$.

> **Theorem 5.3.1 (Existence of a Generalized Inverse)**
> 
> Let $A$ be a nonzero $s\times{n}$ matrix over a number field $K$. Then the matrix equation $AXA=A$ always has a solution.

## 5.1-1

Define a binary relation on the plane $S$ (a set of points):

$$
P\left(x_{1},y_{1}\right)\sim{P}\left(x_{2},y_{2}\right)\overset{def}{\Leftrightarrow}x_{1}=x_{2}.
$$

Prove: $\sim$ is an equivalence relation on $S$.

### Solution to 5.1-1

By **Definition 5.1.2 (Equivalence Relation)**, we verify reflexivity, symmetry and transitivity.

Reflexivity: for any $P\left(x,y\right)\in{S}$, clearly $x=x$, so $P\sim{P}$.

Symmetry: if $P\left(x_{1},y_{1}\right)\sim{P}\left(x_{2},y_{2}\right)$, then $x_{1}=x_{2}$, hence $x_{2}=x_{1}$, and so $P\left(x_{2},y_{2}\right)\sim{P}\left(x_{1},y_{1}\right)$.

Transitivity: if $P\left(x_{1},y_{1}\right)\sim{P}\left(x_{2},y_{2}\right)$ and $P\left(x_{2},y_{2}\right)\sim{P}\left(x_{3},y_{3}\right)$, then $x_{1}=x_{2}$ and $x_{2}=x_{3}$, hence $x_{1}=x_{3}$, and so $P\left(x_{1},y_{1}\right)\sim{P}\left(x_{3},y_{3}\right)$.

Therefore $\sim$ satisfies all conditions of **Definition 5.1.2 (Equivalence Relation)**, and hence is an equivalence relation on $S$. $\blacksquare$

## 5.1-4

Write out the quotient set $\mathbb{Z}/\left(3\right)$ of $\mathbb{Z}$ with respect to the congruence relation modulo $3$.

### Solution to 5.1-4

By **Definition 5.1.4 (Quotient Set)**, congruence modulo $3$ means: $a\sim{b}\overset{def}{\Leftrightarrow}a$ and $b$ have the same remainder upon division by $3$.

There are $3$ equivalence classes:

$$
\left[0\right]=\left\{\cdots,-6,-3,0,3,6,\cdots\right\}=\left\{3k\mid{k}\in\mathbb{Z}\right\}.
$$

$$
\left[1\right]=\left\{\cdots,-5,-2,1,4,7,\cdots\right\}=\left\{3k+1\mid{k}\in\mathbb{Z}\right\}.
$$

$$
\left[2\right]=\left\{\cdots,-4,-1,2,5,8,\cdots\right\}=\left\{3k+2\mid{k}\in\mathbb{Z}\right\}.
$$

Therefore

$$
\mathbb{Z}/\left(3\right)=\left\{\left[0\right],\left[1\right],\left[2\right]\right\}.
$$

$\blacksquare$

## 5.2-1(1)

Find the canonical form under equivalence of the following matrix:

$$
A=\left[\begin{array}{rrr}
1&-1&3\\
-2&3&-11\\
4&-5&17
\end{array}\right].
$$

### Solution to 5.2-1(1)

By **Theorem 5.2.1 (Canonical Form under Equivalence)**, apply elementary row operations to $A$:

$$
A=\left[\begin{array}{rrr}
1&-1&3\\
-2&3&-11\\
4&-5&17
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1&-1&3\\
0&1&-5\\
0&-1&5
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1&-1&3\\
0&1&-5\\
0&0&0
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1&0&-2\\
0&1&-5\\
0&0&0
\end{array}\right].
$$

Now apply elementary column operations: column $3$ $+2\times$ column $1$, column $3$ $+5\times$ column $2$.

$$
A\rightarrow\left[\begin{array}{rrr}
1&0&0\\
0&1&0\\
0&0&0
\end{array}\right].
$$

Thus, by **Theorem 5.2.1 (Canonical Form under Equivalence)**, the canonical form under equivalence is

$$
\left[\begin{array}{cc}I_{2}&0\\0&0\end{array}\right].
$$

$\blacksquare$

## 5.2-1(3)

Find the canonical form under equivalence of the following matrix:

$$
A=\left[\begin{array}{rr}
1&-2\\
-3&-6\\
2&-4
\end{array}\right].
$$

### Solution to 5.2-1(3)

By **Theorem 5.2.1 (Canonical Form under Equivalence)**, apply elementary row operations to $A$:

$$
A=\left[\begin{array}{rr}
1&-2\\
-3&-6\\
2&-4
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1&-2\\
0&-12\\
0&0
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1&-2\\
0&1\\
0&0
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1&0\\
0&1\\
0&0
\end{array}\right].
$$

Thus, by **Theorem 5.2.1 (Canonical Form under Equivalence)**, the canonical form under equivalence is

$$
\left[\begin{array}{c}I_{2}\\0\end{array}\right].
$$

$\blacksquare$

## 5.2-4

Prove: every matrix of rank $r$ ( $r>0$ ) can be written as the sum of $r$ matrices of rank $1$.

### Solution to 5.2-4

By **Theorem 5.2.1 (Canonical Form under Equivalence)**, let $A$ be an $s\times{n}$ matrix with $\operatorname{rank}\left(A\right)=r>0$.

By the canonical form theorem, there exist an $s\times{s}$ invertible matrix $P$ and an $n\times{n}$ invertible matrix $Q$ such that

$$
A=P\left[\begin{array}{cc}I_{r}&0\\0&0\end{array}\right]Q.
$$

Write the middle matrix as the sum of $r$ matrices:

$$
\left[\begin{array}{cc}I_{r}&0\\0&0\end{array}\right]=E_{11}+E_{22}+\cdots+E_{rr},
$$

where $E_{ii}$ is the matrix whose $\left(i,i\right)$-entry is $1$ and all other entries are $0$.

Each $E_{ii}$ has rank $1$.

Therefore

$$
A=P\left(E_{11}+E_{22}+\cdots+E_{rr}\right)Q=PE_{11}Q+PE_{22}Q+\cdots+PE_{rr}Q.
$$

Set $A_{i}=PE_{ii}Q$.

Since $P$ and $Q$ are invertible,

$$
\operatorname{rank}\left(A_{i}\right)=\operatorname{rank}\left(E_{ii}\right)=1.
$$

Therefore $A$ can be written as the sum of $r$ matrices of rank $1$. $\blacksquare$

## 5.2-5

Let $A,B$ be $s\times{n}$ and $n\times{m}$ matrices, respectively. Prove the Sylvester rank inequality:

$$
\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right)-n.
$$

### Solution to 5.2-5

Following the idea of **Theorem 5.2.1 (Canonical Form under Equivalence)**, consider the block matrix

$$
M=\left[\begin{array}{cc}A&0\\I_{n}&B\end{array}\right].
$$

Find an upper bound for $\operatorname{rank}\left(M\right)$.

Perform an elementary block column operation: add $-B$ times the first block column to the second block column.

$$
M=\left[\begin{array}{cc}A&0\\I_{n}&B\end{array}\right]
\rightarrow
\left[\begin{array}{cc}A&-AB\\I_{n}&0\end{array}\right].
$$

Now perform an elementary block row operation: swap the first and second block rows.

$$
\rightarrow
\left[\begin{array}{cc}I_{n}&0\\A&-AB\end{array}\right].
$$

This is block upper triangular, so

$$
\operatorname{rank}\left(M\right)=\operatorname{rank}\left(I_{n}\right)+\operatorname{rank}\left(-AB\right)=n+\operatorname{rank}\left(AB\right).
$$

Find a lower bound for $\operatorname{rank}\left(M\right)$.

Let $\operatorname{rank}\left(A\right)=r_{1}$ and $\operatorname{rank}\left(B\right)=r_{2}$.

$A$ has $r_{1}$ linearly independent rows, and $B$ has $r_{2}$ linearly independent rows.

Among the first $s$ rows of $M$, the $r_{1}$ independent rows of $A$ remain independent in $M$ (the $0$ on the right does not affect them).

Among the last $n$ rows of $M$, the $r_{2}$ independent rows of $B$ correspond to rows of $M$.

Suppose these rows are linearly dependent together with the preceding rows, i.e. there are coefficients $k_{1},k_{2}$ such that

$$
k_{1}\left(\text{a~linear~combination~of~the~first~}s\text{~rows}\right)+k_{2}\left(\text{a~linear~combination~of~the~last~}n\text{~rows}\right)=0.
$$

Look at the last $m$ components:

$$
k_{2}\left(\text{a~linear~combination~of~the~rows~of~}B\right)=0.
$$

Since the rows of $B$ are independent, $k_{2}=0$.

Now look at the first $s$ components:

$$
k_{1}\left(\text{a~linear~combination~of~the~rows~of~}A\right)=0.
$$

Since the rows of $A$ are independent, $k_{1}=0$.

Therefore the row group of $M$ has rank at least $r_{1}+r_{2}$.

That is,

$$
\operatorname{rank}\left(M\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right).
$$

Combining the two inequalities:

$$
n+\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right).
$$

That is,

$$
\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right)-n.
$$

$\blacksquare$

## 5.3-1

Let $A$ be an $s\times{n}$ matrix over a number field $K$. Prove: if $A$ is row full-rank, then for every generalized inverse $A^{-}$ of $A$, $AA^{-}=I_{s}$.

### Solution to 5.3-1

By **Definition 5.3.1 (Generalized Inverse)**, $A^{-}$ is a generalized inverse of $A$, i.e. $AA^{-}A=A$. Suppose $A$ is row full-rank, i.e. $\operatorname{rank}\left(A\right)=s$.

Set $B=AA^{-}$. Then $B$ is an $s\times{s}$ matrix.

From $AA^{-}A=A$, multiply on the right by $A^{-}$:

$$
\left(AA^{-}A\right)A^{-}=AA^{-}.
$$

Namely,

$$
AA^{-}\left(AA^{-}\right)=AA^{-}.
$$

Therefore

$$
BB=B,
$$

i.e. $B$ is idempotent.

Find the rank of $B$.

Since $A$ is row full-rank, $\operatorname{rank}\left(A\right)=s$.

Since $AA^{-}A=A$,

$$
\operatorname{rank}\left(A\right)=\operatorname{rank}\left(AA^{-}A\right)\le\operatorname{rank}\left(AA^{-}\right)\le\operatorname{rank}\left(A\right).
$$

Hence

$$
\operatorname{rank}\left(B\right)=\operatorname{rank}\left(AA^{-}\right)=\operatorname{rank}\left(A\right)=s.
$$

Thus $B$ is an $s\times{s}$ matrix with $\operatorname{rank}\left(B\right)=s$, i.e. $B$ is invertible.

From $BB=B$, multiply on the left by $B^{-1}$:

$$
B=I_{s}.
$$

Therefore, by **Definition 5.3.1 (Generalized Inverse)**, for every generalized inverse $A^{-}$ of $A$,

$$
AA^{-}=I_{s}.
$$

$\blacksquare$
