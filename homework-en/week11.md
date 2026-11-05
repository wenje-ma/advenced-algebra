# week11

> **Theorem 3.8.1 (Solution Set Structure of an Inhomogeneous System)**
> 
> If an $n$-variable inhomogeneous linear system over a number field $K$ is solvable, then its solution set is $U=\gamma_{0}+W$, where $\gamma_{0}$ is a particular solution and $W$ is the solution space of the derived homogeneous system.

> **Definition 4.1.1 (Matrix Addition)**
> 
> Let $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ both be $s\times{n}$ matrices over a number field $K$, and set $C=\left(a_{ij}+b_{ij}\right)_{s\times{n}}$. Then $C$ is called the sum of the matrices $A$ and $B$, denoted $C=A+B$.

> **Definition 4.1.2 (Scalar Multiplication of Matrices)**
> 
> Let $k\in{K}$ and set $M=\left(ka_{ij}\right)_{s\times{n}}$. Then $M$ is called the scalar product of $k$ and the matrix $A$, denoted $M=kA$.

> **Definition 4.1.3 (Matrix Multiplication)**
> 
> Let $A=\left(a_{ij}\right)_{s\times{n}}$ and $B=\left(b_{ij}\right)_{n\times{m}}$, and set $C=\left(c_{ij}\right)_{s\times{m}}$ with $c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}$. Then $C$ is called the product of $A$ and $B$, denoted $C=AB$.

## 3.8-2

Prove: an inhomogeneous linear system of $n$ equations in $n$ variables has a unique solution if and only if its derived homogeneous system has only the zero solution.

### Solution to 3.8-2

By **Theorem 3.8.1 (Solution Set Structure of an Inhomogeneous System)**, the solution set of the inhomogeneous system is $U=\gamma_{0}+W$, where $W$ is the solution space of the derived homogeneous system. We prove that the inhomogeneous system has a unique solution if and only if its derived system has only the zero solution.

Let the inhomogeneous system be $Ax=\beta$, where $A$ is an $n\times{n}$ matrix; the derived system is $Ax=0$.

Necessity. Suppose the inhomogeneous system has a unique solution; then

$$
\text{rank}\left(A\right)=\text{rank}\left(\overline{A}\right)=n\,\text{\left(the~rank~of~the~coefficient~matrix~equals~the~number~of~unknowns\right)}.
$$

The derived system $Ax=0$ has coefficient matrix of rank $n$ and $n$ unknowns, so it has only the zero solution.

Sufficiency. Suppose the derived system has only the zero solution; then $\text{rank}\left(A\right)=n$.

$A$ is an $n\times{n}$ matrix with $\text{rank}\left(A\right)=n$, so $\left|A\right|\ne0$.

The derived system having only the zero solution means the solution space $W=\left\{0\right\}$, so the inhomogeneous system's solution set $U=\gamma_{0}+W=\left\{\gamma_{0}\right\}$, i.e. it has a unique solution. $\blacksquare$

## 3.8-4

Prove: if $\gamma_{0}$ is a particular solution of inhomogeneous linear system (1), and $\eta_{1},\eta_{2},\cdots,\eta_{t}$ is a fundamental system of its derived homogeneous system. Set

$$
\gamma_{1}=\gamma_{0}+\eta_{1},\gamma_{2}=\gamma_{0}+\eta_{2},\cdots,\gamma_{t}=\gamma_{0}+\eta_{t}.
$$

Then any solution $\gamma$ of inhomogeneous linear system (1) can be expressed as

$$
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},
$$

where

$$
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

### Solution to 3.8-4

By **Theorem 3.8.1 (Solution Set Structure of an Inhomogeneous System)**, the solution set of the inhomogeneous system is $U=\gamma_{0}+W$, where $W$ is the solution space of the derived homogeneous system.

Take any $\gamma\in{U}$; then $\gamma-\gamma_{0}\in{W}$.

Because $\eta_{1},\eta_{2},\cdots,\eta_{t}$ is a basis of $W$, there exist $k_{1},\cdots,k_{t}\in{K}$ such that

$$
\gamma-\gamma_{0}=k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{t}\eta_{t}.
$$

Substituting $\eta_{i}=\gamma_{i}-\gamma_{0}$:

$$
\gamma=\gamma_{0}+k_{1}\left(\gamma_{1}-\gamma_{0}\right)+k_{2}\left(\gamma_{2}-\gamma_{0}\right)+\cdots+k_{t}\left(\gamma_{t}-\gamma_{0}\right)=\left(1-k_{1}-k_{2}-\cdots-k_{t}\right)\gamma_{0}+k_{1}\gamma_{1}+k_{2}\gamma_{2}+\cdots+k_{t}\gamma_{t}.
$$

Set

$$
u_{0}=1-k_{1}-k_{2}-\cdots-k_{t},
$$

$u_{1}=k_{1}$, $\cdots$, $u_{t}=k_{t}$.

Then

$$
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

Any solution of the inhomogeneous system can be expressed in the above form. Hence

$$
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},\quad
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

$\blacksquare$

## 4.1-1

Let

$$
A=\left[\begin{array}{ccc}
\lambda&0&0\\
0&\lambda&0\\
0&0&\lambda
\end{array}\right],
B=\left[\begin{array}{ccc}
0&1&0\\
0&0&1\\
0&0&0
\end{array}\right].
$$

Find $A+B$.

### Solution to 4.1-1

By **Definition 4.1.1 (Matrix Addition)**,

$$
A+B=\left[\begin{array}{ccc}
\lambda&1&0\\
0&\lambda&1\\
0&0&\lambda
\end{array}\right].
$$

$\blacksquare$

## 4.1-3

Let $I$ be the $n\times{n}$ identity matrix and $J$ be the $n\times{n}$ matrix all of whose entries are $1$. Let

$$
M=\left[\begin{array}{cccc}
k&\lambda&\cdots&\lambda\\
\lambda&k&\cdots&\lambda\\
\vdots&\vdots&&\vdots\\
\lambda&\lambda&\cdots&k
\end{array}\right]_{n\times{n}}.
$$

Express $M$ in the form $xI+yJ$, where $x,y$ are undetermined coefficients.

### Solution to 4.1-3

By **Definition 4.1.1 (Matrix Addition)** and **Definition 4.1.2 (Scalar Multiplication of Matrices)**, the diagonal entries of $xI+yJ$ are $x+y$ and the off-diagonal entries are $y$.

Comparing with $M$, whose diagonal entries are $k$ and off-diagonal entries are $\lambda$, gives

$$
\begin{cases}
x+y=k,\\
y=\lambda.
\end{cases}
$$

Solving gives $x=k-\lambda$, $y=\lambda$.

By **Definition 4.1.1 (Matrix Addition)** and **Definition 4.1.2 (Scalar Multiplication of Matrices)**,

$$
M=\left(k-\lambda\right)I+\lambda{J}.
$$

$\blacksquare$

## 4.1-4(1)

Compute:

$$
\left[\begin{array}{rr}
7&-1\\
-2&5\\
3&-4
\end{array}\right]\left[\begin{array}{rr}
1&4\\
-5&2
\end{array}\right].
$$

### Solution to 4.1-4(1)

By **Definition 4.1.3 (Matrix Multiplication)**, the $\left(i,j\right)$-entry of the product equals the inner product of row $i$ and column $j$:

$$
\left[\begin{array}{rr}
7&-1\\
-2&5\\
3&-4
\end{array}\right]\left[\begin{array}{rr}
1&4\\
-5&2
\end{array}\right]
=
\left[\begin{array}{rr}
7\times1+\left(-1\right)\times\left(-5\right)&7\times4+\left(-1\right)\times2\\
\left(-2\right)\times1+5\times\left(-5\right)&\left(-2\right)\times4+5\times2\\
3\times1+\left(-4\right)\times\left(-5\right)&3\times4+\left(-4\right)\times2
\end{array}\right]
=
\left[\begin{array}{rr}
12&26\\
-27&2\\
23&4
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(2)

Compute:

$$
\left[\begin{array}{rr}
0&2\\
0&3
\end{array}\right]\left[\begin{array}{rr}
1&1\\
0&0
\end{array}\right].
$$

### Solution to 4.1-4(2)

By **Definition 4.1.3 (Matrix Multiplication)**, the $\left(i,j\right)$-entry of the product equals the inner product of row $i$ and column $j$:

$$
\left[\begin{array}{rr}
0&2\\
0&3
\end{array}\right]\left[\begin{array}{rr}
1&1\\
0&0
\end{array}\right]
=
\left[\begin{array}{rr}
0\times1+2\times0&0\times1+2\times0\\
0\times1+3\times0&0\times1+3\times0
\end{array}\right]
=
\left[\begin{array}{rr}
0&0\\
0&0
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(3)

Compute:

$$
\left[\begin{array}{rr}
1&1\\
0&0
\end{array}\right]\left[\begin{array}{rr}
0&2\\
0&3
\end{array}\right].
$$

### Solution to 4.1-4(3)

By **Definition 4.1.3 (Matrix Multiplication)**, the $\left(i,j\right)$-entry of the product equals the inner product of row $i$ and column $j$:

$$
\left[\begin{array}{rr}
1&1\\
0&0
\end{array}\right]\left[\begin{array}{rr}
0&2\\
0&3
\end{array}\right]
=
\left[\begin{array}{rr}
1\times0+1\times0&1\times2+1\times3\\
0\times0+0\times0&0\times2+0\times3
\end{array}\right]
=
\left[\begin{array}{rr}
0&5\\
0&0
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(8)

Compute:

$$
\left[\begin{array}{ccc}
d_{1}&0&0\\
0&d_{2}&0\\
0&0&d_{3}
\end{array}\right]\left[\begin{array}{ccc}
a_{1}&a_{2}&a_{3}\\
b_{1}&b_{2}&b_{3}\\
c_{1}&c_{2}&c_{3}
\end{array}\right].
$$

### Solution to 4.1-4(8)

By **Definition 4.1.3 (Matrix Multiplication)**, left-multiplying by a diagonal matrix amounts to multiplying the corresponding rows by the diagonal entries:

$$
=
\left[\begin{array}{ccc}
d_{1}a_{1}&d_{1}a_{2}&d_{1}a_{3}\\
d_{2}b_{1}&d_{2}b_{2}&d_{2}b_{3}\\
d_{3}c_{1}&d_{3}c_{2}&d_{3}c_{3}
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(9)

Compute:

$$
\left[\begin{array}{ccc}
a_{1}&a_{2}&a_{3}\\
b_{1}&b_{2}&b_{3}\\
c_{1}&c_{2}&c_{3}
\end{array}\right]\left[\begin{array}{ccc}
d_{1}&0&0\\
0&d_{2}&0\\
0&0&d_{3}
\end{array}\right].
$$

### Solution to 4.1-4(9)

By **Definition 4.1.3 (Matrix Multiplication)**, right-multiplying by a diagonal matrix amounts to multiplying the corresponding columns by the diagonal entries:

$$
=
\left[\begin{array}{ccc}
d_{1}a_{1}&d_{2}a_{2}&d_{3}a_{3}\\
d_{1}b_{1}&d_{2}b_{2}&d_{3}b_{3}\\
d_{1}c_{1}&d_{2}c_{2}&d_{3}c_{3}
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(13)

Compute:

$$
\left[\begin{array}{ccc}
0&1&0\\
1&0&0\\
0&0&1
\end{array}\right]\left[\begin{array}{cccc}
a_{1}&a_{2}&a_{3}&a_{4}\\
b_{1}&b_{2}&b_{3}&b_{4}\\
c_{1}&c_{2}&c_{3}&c_{4}
\end{array}\right].
$$

### Solution to 4.1-4(13)

By **Definition 4.1.3 (Matrix Multiplication)**, this is left-multiplication by the elementary matrix that swaps rows $1$ and $2$:

$$
=
\left[\begin{array}{cccc}
b_{1}&b_{2}&b_{3}&b_{4}\\
a_{1}&a_{2}&a_{3}&a_{4}\\
c_{1}&c_{2}&c_{3}&c_{4}
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(14)

Compute:

$$
\left[\begin{array}{ccc}
a_{1}&a_{2}&a_{3}\\
b_{1}&b_{2}&b_{3}\\
c_{1}&c_{2}&c_{3}
\end{array}\right]\left[\begin{array}{ccc}
0&1&0\\
1&0&0\\
0&0&1
\end{array}\right].
$$

### Solution to 4.1-4(14)

By **Definition 4.1.3 (Matrix Multiplication)**, this is right-multiplication by the elementary matrix that swaps columns $1$ and $2$:

$$
=
\left[\begin{array}{ccc}
a_{2}&a_{1}&a_{3}\\
b_{2}&b_{1}&b_{3}\\
c_{2}&c_{1}&c_{3}
\end{array}\right].
$$

$\blacksquare$
