# week18

> **Basic Knowledge: Matrix Binomial Theorem**<br>If two matrices $P,Q$ commute ($PQ=QP$), then $\left(P+Q\right)^{n}=\sum_{k=0}^{n}\binom{n}{k}P^{n-k}Q^{k}$.

> **Definition 4.1.1 (Matrix Addition)**<br>Let $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ both be $s\times n$ matrices over a number field $K$, and set $C=\left(a_{ij}+b_{ij}\right)_{s\times n}$. Then $C$ is called the sum of the matrices $A$ and $B$, denoted $C=A+B$.

> **Definition 4.1.2 (Scalar Multiplication of Matrices)**<br>Let $k\in K$ and set $M=\left(ka_{ij}\right)_{s\times n}$. Then $M$ is called the scalar product of $k$ and the matrix $A$, denoted $M=kA$.

> **Definition 4.1.3 (Matrix Multiplication)**<br>Let $A=\left(a_{ij}\right)_{s\times n}$ and $B=\left(b_{ij}\right)_{n\times m}$, and set $C=\left(c_{ij}\right)_{s\times m}$ with $c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}$. Then $C$ is called the product of $A$ and $B$, denoted $C=AB$.

---

## 4.1-1

Let

$$
A=\left[\begin{array}{ccc}
\lambda & 0 & 0\\
0 & \lambda & 0\\
0 & 0 & \lambda
\end{array}\right],
B=\left[\begin{array}{ccc}
0 & 1 & 0\\
0 & 0 & 1\\
0 & 0 & 0
\end{array}\right].
$$

Find $A+B$.

### Solution 4.1-1

By **Definition 4.1.1 (Matrix Addition)**,

$$
A+B=\left[\begin{array}{ccc}
\lambda & 1 & 0\\
0 & \lambda & 1\\
0 & 0 & \lambda
\end{array}\right].
$$

$\blacksquare$

---

## 4.1-3

Let $I$ be the $n\times n$ identity matrix and $J$ be the $n\times n$ matrix all of whose entries are $1$. Let

$$
M=\left[\begin{array}{cccc}
k & \lambda & \cdots & \lambda\\
\lambda & k & \cdots & \lambda\\
\vdots & \vdots & & \vdots\\
\lambda & \lambda & \cdots & k
\end{array}\right]_{n\times n}.
$$

Express $M$ in the form $xI+yJ$, where $x,y$ are undetermined coefficients.

### Solution 4.1-3

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
M=\left(k-\lambda\right)I+\lambda J.
$$

$\blacksquare$

---

## 4.1-4(1)

Compute:

$$
\left[\begin{array}{rr}
7 & -1\\
-2 & 5\\
3 & -4
\end{array}\right]\left[\begin{array}{rr}
1 & 4\\
-5 & 2
\end{array}\right].
$$

### Solution 4.1-4(1)

By **Definition 4.1.3 (Matrix Multiplication)**, the $\left(i,j\right)$-entry of the product equals the inner product of row $i$ and column $j$:

$$
\left[\begin{array}{rr}
7 & -1\\
-2 & 5\\
3 & -4
\end{array}\right]\left[\begin{array}{rr}
1 & 4\\
-5 & 2
\end{array}\right]
=
\left[\begin{array}{rr}
7\times1+\left(-1\right)\times\left(-5\right) & 7\times4+\left(-1\right)\times2\\
\left(-2\right)\times1+5\times\left(-5\right) & \left(-2\right)\times4+5\times2\\
3\times1+\left(-4\right)\times\left(-5\right) & 3\times4+\left(-4\right)\times2
\end{array}\right]
=
\left[\begin{array}{rr}
12 & 26\\
-27 & 2\\
23 & 4
\end{array}\right].
$$

$\blacksquare$

---

## 4.1-4(2)

Compute:

$$
\left[\begin{array}{rr}
0 & 2\\
0 & 3
\end{array}\right]\left[\begin{array}{rr}
1 & 1\\
0 & 0
\end{array}\right].
$$

### Solution 4.1-4(2)

By **Definition 4.1.3 (Matrix Multiplication)**, the $\left(i,j\right)$-entry of the product equals the inner product of row $i$ and column $j$:

$$
\left[\begin{array}{rr}
0 & 2\\
0 & 3
\end{array}\right]\left[\begin{array}{rr}
1 & 1\\
0 & 0
\end{array}\right]
=
\left[\begin{array}{rr}
0\times1+2\times0 & 0\times1+2\times0\\
0\times1+3\times0 & 0\times1+3\times0
\end{array}\right]
=
\left[\begin{array}{rr}
0 & 0\\
0 & 0
\end{array}\right].
$$

$\blacksquare$

---

## 4.1-4(3)

Compute:

$$
\left[\begin{array}{rr}
1 & 1\\
0 & 0
\end{array}\right]\left[\begin{array}{rr}
0 & 2\\
0 & 3
\end{array}\right].
$$

### Solution 4.1-4(3)

By **Definition 4.1.3 (Matrix Multiplication)**, the $\left(i,j\right)$-entry of the product equals the inner product of row $i$ and column $j$:

$$
\left[\begin{array}{rr}
1 & 1\\
0 & 0
\end{array}\right]\left[\begin{array}{rr}
0 & 2\\
0 & 3
\end{array}\right]
=
\left[\begin{array}{rr}
1\times0+1\times0 & 1\times2+1\times3\\
0\times0+0\times0 & 0\times2+0\times3
\end{array}\right]
=
\left[\begin{array}{rr}
0 & 5\\
0 & 0
\end{array}\right].
$$

$\blacksquare$

---

## 4.1-4(8)

Compute:

$$
\left[\begin{array}{ccc}
d_{1} & 0 & 0\\
0 & d_{2} & 0\\
0 & 0 & d_{3}
\end{array}\right]\left[\begin{array}{ccc}
a_{1} & a_{2} & a_{3}\\
b_{1} & b_{2} & b_{3}\\
c_{1} & c_{2} & c_{3}
\end{array}\right].
$$

### Solution 4.1-4(8)

By **Definition 4.1.3 (Matrix Multiplication)**, left-multiplying by a diagonal matrix amounts to multiplying the corresponding rows by the diagonal entries:

$$
=
\left[\begin{array}{ccc}
d_{1}a_{1} & d_{1}a_{2} & d_{1}a_{3}\\
d_{2}b_{1} & d_{2}b_{2} & d_{2}b_{3}\\
d_{3}c_{1} & d_{3}c_{2} & d_{3}c_{3}
\end{array}\right].
$$

$\blacksquare$

---

## 4.1-4(9)

Compute:

$$
\left[\begin{array}{ccc}
a_{1} & a_{2} & a_{3}\\
b_{1} & b_{2} & b_{3}\\
c_{1} & c_{2} & c_{3}
\end{array}\right]\left[\begin{array}{ccc}
d_{1} & 0 & 0\\
0 & d_{2} & 0\\
0 & 0 & d_{3}
\end{array}\right].
$$

### Solution 4.1-4(9)

By **Definition 4.1.3 (Matrix Multiplication)**, right-multiplying by a diagonal matrix amounts to multiplying the corresponding columns by the diagonal entries:

$$
=
\left[\begin{array}{ccc}
d_{1}a_{1} & d_{2}a_{2} & d_{3}a_{3}\\
d_{1}b_{1} & d_{2}b_{2} & d_{3}b_{3}\\
d_{1}c_{1} & d_{2}c_{2} & d_{3}c_{3}
\end{array}\right].
$$

$\blacksquare$

---

## 4.1-4(13)

Compute:

$$
\left[\begin{array}{ccc}
0 & 1 & 0\\
1 & 0 & 0\\
0 & 0 & 1
\end{array}\right]\left[\begin{array}{cccc}
a_{1} & a_{2} & a_{3} & a_{4}\\
b_{1} & b_{2} & b_{3} & b_{4}\\
c_{1} & c_{2} & c_{3} & c_{4}
\end{array}\right].
$$

### Solution 4.1-4(13)

By **Definition 4.1.3 (Matrix Multiplication)**, this is left-multiplication by the elementary matrix that swaps rows $1$ and $2$:

$$
=
\left[\begin{array}{cccc}
b_{1} & b_{2} & b_{3} & b_{4}\\
a_{1} & a_{2} & a_{3} & a_{4}\\
c_{1} & c_{2} & c_{3} & c_{4}
\end{array}\right].
$$

$\blacksquare$

---

## 4.1-4(14)

Compute:

$$
\left[\begin{array}{ccc}
a_{1} & a_{2} & a_{3}\\
b_{1} & b_{2} & b_{3}\\
c_{1} & c_{2} & c_{3}
\end{array}\right]\left[\begin{array}{ccc}
0 & 1 & 0\\
1 & 0 & 0\\
0 & 0 & 1
\end{array}\right].
$$

### Solution 4.1-4(14)

By **Definition 4.1.3 (Matrix Multiplication)**, this is right-multiplication by the elementary matrix that swaps columns $1$ and $2$:

$$
=
\left[\begin{array}{ccc}
a_{2} & a_{1} & a_{3}\\
b_{2} & b_{1} & b_{3}\\
c_{2} & c_{1} & c_{3}
\end{array}\right].
$$

$\blacksquare$

---

## 4.1-6

Compute:

$$
\left(x,y,1\right)\left[\begin{array}{ccc}
a_{11} & a_{12} & a_{1}\\
a_{12} & a_{22} & a_{2}\\
a_{1} & a_{2} & a_{0}
\end{array}\right]\left[\begin{array}{c}
x\\
y\\
1
\end{array}\right].
$$

### Solution 4.1-6

By **Definition 4.1.3 (Matrix Multiplication)**, first multiply the row vector on the left by the matrix:

$$
\left(x,y,1\right)M
=
\left(a_{11}x+a_{12}y+a_{1},a_{12}x+a_{22}y+a_{2},a_{1}x+a_{2}y+a_{0}\right).
$$

Then multiply by the column vector:

$$
=\left(a_{11}x+a_{12}y+a_{1}\right)x+\left(a_{12}x+a_{22}y+a_{2}\right)y+\left(a_{1}x+a_{2}y+a_{0}\right)=a_{11}x^{2}+2a_{12}xy+a_{22}y^{2}+2a_{1}x+2a_{2}y+a_{0}.
$$

$\blacksquare$

---

## 4.1-7(5)

Compute:

$$
\left[\begin{array}{ccc}
0 & 1 & 0\\
0 & 0 & 1\\
0 & 0 & 0
\end{array}\right]^{n},\text{ where }n\text{ is a positive integer}.
$$

### Solution 4.1-7(5)

By **Definition 4.1.3 (Matrix Multiplication)**, write

$$
H=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right].
$$

$$
H^{2}=HH=\left[\begin{array}{ccc}
0 & 0 & 1\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

$$
H^{3}=H^{2}H=\left[\begin{array}{ccc}
0 & 0 & 0\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

Therefore:

- when $n=1$, $H^{n}=H=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right]$;
- when $n=2$, $H^{n}=\left[\begin{array}{ccc}0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]$;
- when $n\ge3$, $H^{n}=0$.

$\blacksquare$

---

## 4.1-7(6)

Compute:

$$
\left[\begin{array}{ccc}
\lambda & 1 & 0\\
0 & \lambda & 1\\
0 & 0 & \lambda
\end{array}\right]^{n},\text{ where }n\text{ is a positive integer}.
$$

### Solution 4.1-7(6)

By **Definition 4.1.3 (Matrix Multiplication)**, write $A=\lambda I+N$, where

$$
N=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right].
$$

Because $\lambda I$ and $N$ commute, by **Basic Knowledge: Matrix Binomial Theorem**,

$$
A^{n}=\sum_{k=0}^{n}\binom{n}{k}\left(\lambda I\right)^{n-k}N^{k}.
$$

Also $N^{0}=I$, $N^{1}=N$, $N^{2}=\left[\begin{array}{ccc}0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]$, $N^{3}=0$.

Hence

$$
A^{n}
=\lambda^{n}I+n\lambda^{n-1}N+\binom{n}{2}\lambda^{n-2}N^{2}=\left[\begin{array}{ccc}
\lambda^{n} & n\lambda^{n-1} & \dfrac{n\left(n-1\right)}{2}\lambda^{n-2}\\
0 & \lambda^{n} & n\lambda^{n-1}\\
0 & 0 & \lambda^{n}
\end{array}\right].
$$

When $n=1$, the above also holds (note $\lambda^{0}=1$, and the third term is $0$). $\blacksquare$

---

## 4.1-10

Prove: if $A=\frac{1}{2}\left(B+I\right)$, then $A^{2}=A$ if and only if $B^{2}=I$.

### Solution 4.1-10

$$
A^{2}=\left(\frac{1}{2}\left(B+I\right)\right)^{2}=\frac{1}{4}\left(B+I\right)^{2}=\frac{1}{4}\left(B^{2}+2B+I\right).
$$

$A^{2}=A$ is equivalent to

$$
\frac{1}{4}\left(B^{2}+2B+I\right)=\frac{1}{2}\left(B+I\right).
$$

Multiplying both sides by $4$:

$$
B^{2}+2B+I=2B+2I.
$$

Simplifying:

$$
B^{2}=I.
$$

Therefore $A^{2}=A$ if and only if $B^{2}=I$. $\blacksquare$
