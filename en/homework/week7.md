# week7

> **Basic Knowledge: Minor Characterization of Matrix Rank**<br>If the rank of a matrix is at most $2$, then all its minors of order $3$ and higher are $0$; in particular, when $n\ge3$, the $n\times n$ determinant is $0$.

> **Basic Knowledge: Primitive $n$-th Roots of Unity and Eigenvalues of Circulant Matrices**<br>Let $\omega$ be a primitive $n$-th root of unity. The eigenvalues of the cyclic shift matrix $P$ are $\omega^{k}$ $\left(k=0,1,\cdots,n-1\right)$, and the identity $\prod_{k=1}^{n-1}\left(1-\omega^{k}\right)=n$ holds.

> **Definition 2.4.1 (Minors and Cofactors)**<br>In the $n\times n$ determinant $\left|A\right|$, deleting row $i$ and column $j$, the $(n-1)$-determinant formed by the remaining entries in their original order is called the minor of the $\left(i,j\right)$-entry of $A$, denoted $M_{ij}$. Setting $A_{ij}=\left(-1\right)^{i+j}M_{ij}$, $A_{ij}$ is called the cofactor of the $\left(i,j\right)$-entry of $A$.

> **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**<br>The $n\times n$ determinant $\left|A\right|$ equals the sum of the products of the entries in its $i$-th row and their cofactors:

$$
\left|A\right|=a_{i1}A_{i1}+a_{i2}A_{i2}+\cdots+a_{in}A_{in}.
$$

---

## 2.4-2

Compute the following $n\times n$ determinant $\left(n\ge2\right)$:

$$
\left|\begin{array}{cccccc}
a_{1} & a_{2} & a_{3} & \cdots & a_{n-1} & a_{n}\\
1 & -1 & 0 & \cdots & 0 & 0\\
0 & 2 & -2 & \cdots & 0 & 0\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
0 & 0 & 0 & \cdots & n-1 & 1-n
\end{array}\right|.
$$

### Solution 2.4-2

Starting from the $n$-th column, successively add column $k$ to column $k-1$ for $k=n,n-1,\cdots,2$. This step uses the column-operation property of a determinant: adding a multiple of one column to another leaves the determinant unchanged.

Adding column $n$ to column $n-1$: column $n-1$ becomes $\left(a_{n-1}+a_{n},0,0,\cdots,0\right)$.

Adding column $n-1$ to column $n-2$: column $n-2$ becomes

$$
\left(a_{n-2}+a_{n-1}+a_{n},0,0,\cdots,0\right).
$$

Continuing, column $1$ eventually becomes

$$
\left(a_{1}+a_{2}+\cdots+a_{n},0,0,\cdots,0\right).
$$

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along column $1$. Column $1$ has only its first entry nonzero and all others $0$, so

$$
\left|A\right|=\left(a_{1}+a_{2}+\cdots+a_{n}\right)\cdot A_{11}.
$$

By **Definition 2.4.1 (Minors and Cofactors)**,

$$
A_{11}=\left(-1\right)^{1+1}M_{11}=M_{11},
$$

where $M_{11}$ is the $\left(n-1\right)$-determinant after deleting row $1$ and column $1$:

$$
M_{11}=\left|\begin{array}{cccc}
-1 & 0 & \cdots & 0\\
0 & -2 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
0 & 0 & \cdots & 1-n
\end{array}\right|.
$$

This is a diagonal determinant with diagonal entries $-1,-2,\cdots,1-n$. Hence

$$
M_{11}=\left(-1\right)\times\left(-2\right)\times\cdots\times\left(1-n\right)=\left(-1\right)^{n-1}\left(n-1\right)!.
$$

Therefore

$$
\left|A\right|=\left(\sum_{i=1}^{n}a_{i}\right)\times\left(-1\right)^{n-1}\left(n-1\right)!.
$$

$\blacksquare$

---

## 2.4-4

Prove by mathematical induction that, for all $n\ge2$,

$$
\left|\begin{array}{cccccc}
x & 0 & 0 & \cdots & 0 & a_{0}\\
-1 & x & 0 & \cdots & 0 & a_{1}\\
0 & -1 & x & \cdots & 0 & a_{2}\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
0 & 0 & 0 & \cdots & x & a_{n-2}\\
0 & 0 & 0 & \cdots & -1 & x+a_{n-1}
\end{array}\right|=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{n}.
$$

### Solution 2.4-4

**Base case $n=2$**:

$$
\left|\begin{array}{cc}x & a_{0}\\-1 & x+a_{1}\end{array}\right|=x\left(x+a_{1}\right)-\left(-1\right)a_{0}=x^{2}+a_{1}x+a_{0}.
$$

It holds.

**Inductive step**: assume the conclusion holds for order $n-1$.

For the $n\times n$ determinant, by **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along row $1$:

$$
D_{n}=x\cdot M_{11}+\left(-1\right)^{1+n}a_{0}\cdot M_{1n}.
$$

By **Definition 2.4.1 (Minors and Cofactors)**, $M_{11}$ is the $\left(n-1\right)$-determinant after deleting row $1$ and column $1$; by the induction hypothesis,

$$
M_{11}=x^{n-1}+a_{n-1}x^{n-2}+\cdots+a_{2}x+a_{1}.
$$

By **Definition 2.4.1 (Minors and Cofactors)**, $M_{1n}$ is the $\left(n-1\right)$-determinant after deleting row $1$ and column $n$; its diagonal entries are all $-1$, making it a lower triangular determinant, so

$$
M_{1n}=\left(-1\right)^{n-1}.
$$

Substituting,

$$
D_{n}=x\left(x^{n-1}+a_{n-1}x^{n-2}+\cdots+a_{2}x+a_{1}\right)+\left(-1\right)^{1+n}a_{0}\left(-1\right)^{n-1}=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+\left(-1\right)^{2n}a_{0}=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{0}.
$$

By mathematical induction, the conclusion holds for all $n\ge 2$. $\blacksquare$

---

## 2.4-8

Compute the following $n\times n$ determinant $\left(n\ge2\right)$:

$$
\left|\begin{array}{cccccc}
1 & 2 & 2 & \cdots & 2 & 2\\
2 & 2 & 2 & \cdots & 2 & 2\\
2 & 2 & 3 & \cdots & 2 & 2\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
2 & 2 & 2 & \cdots & n-1 & 2\\
2 & 2 & 2 & \cdots & 2 & n
\end{array}\right|.
$$

### Solution 2.4-8

Add $-1$ times row $2$ respectively to row $1$ and to row $i$ for $i=3,4,\cdots,n$:

row $1$ becomes $\left(-1,0,0,\cdots,0\right)$;

row $i$ $\left(i\ge 3\right)$ becomes $\left(0,0,\cdots,i-2,\cdots,0\right)$, where $i-2$ lies in column $i$.

The determinant becomes

$$
\left|\begin{array}{cccccc}
-1 & 0 & 0 & \cdots & 0 & 0\\
2 & 2 & 2 & \cdots & 2 & 2\\
0 & 0 & 1 & \cdots & 0 & 0\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
0 & 0 & 0 & \cdots & n-2 & 0\\
0 & 0 & 0 & \cdots & 0 & n-2
\end{array}\right|.
$$

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along row $1$: $D=-1\cdot M_{11}$.

By **Definition 2.4.1 (Minors and Cofactors)**, $M_{11}$ is the $\left(n-1\right)$-determinant after deleting row $1$ and column $1$. Expanding along its row $2$ (the original row $3$), which has only entry $1$ in column $2$, gives

$$
M_{11}=1\cdot\left(-1\right)^{2+2}\cdot M'_{22}=M'_{22}.
$$

By **Definition 2.4.1 (Minors and Cofactors)**, $M'_{22}$ is the $\left(n-2\right)$-determinant after deleting row $2$ and column $2$; expanding along its row $1$, which has only entry $2$ in column $1$ nonzero, all other terms vanish because after deleting the corresponding column some row becomes all zeros, so

$$
M'_{22}=2\cdot\left(n-2\right)!.
$$

Therefore

$$
D=-1\cdot2\cdot\left(n-2\right)!=-2\left(n-2\right)!.
$$

$\blacksquare$

---

## 2.4-10

Compute the following $n\times n$ determinant:

$$
\left|\begin{array}{ccccc}
1 & 2 & 3 & \cdots & n\\
2 & 3 & 4 & \cdots & 1\\
3 & 4 & 5 & \cdots & 2\\
\vdots & \vdots & \vdots & & \vdots\\
n & 1 & 2 & \cdots & n-1
\end{array}\right|.
$$

### Solution 2.4-10

The sum of the entries in each row is

$$
1+2+\cdots+n=\frac{n\left(n+1\right)}{2}.
$$

Add columns $2$ through $n$ to column $1$; column $1$ becomes all $\frac{n\left(n+1\right)}{2}$; pulling out this common factor,

$$
D=\frac{n\left(n+1\right)}{2}\cdot\left|\begin{array}{ccccc}
1 & 2 & 3 & \cdots & n\\
1 & 3 & 4 & \cdots & 1\\
1 & 4 & 5 & \cdots & 2\\
\vdots & \vdots & \vdots & & \vdots\\
1 & 1 & 2 & \cdots & n-1
\end{array}\right|.
$$

Subtract row $1$ from row $i$ for $i=2,\cdots,n$, and expand along column $1$.

By **Basic Knowledge: Primitive $n$-th Roots of Unity and Eigenvalues of Circulant Matrices**, let $P$ be the $n\times n$ cyclic shift matrix; then the original matrix is

$$
C=1\cdot I+2\cdot P+\cdots+n\cdot P^{n-1}.
$$

The eigenvalues of $P$ are $\omega^{k}$ $\left(k=0,1,\cdots,n-1\right)$, where $\omega$ is a primitive $n$-th root of unity.

The eigenvalues of $C$ are

$$
\lambda_{k}=1+2\omega^{k}+\cdots+n\omega^{\left(n-1\right)k}.
$$

When $k=0$,

$$
\lambda_{0}=\frac{n\left(n+1\right)}{2}.
$$

When $k\ne0$, since $\omega^{kn}=1$,

$$
\lambda_{k}=1+2\omega^{k}+\cdots+n\omega^{\left(n-1\right)k}=\frac{n}{\omega^{k}-1}.
$$

Hence

$$
D=\prod_{k=0}^{n-1}\lambda_{k}=\frac{n\left(n+1\right)}{2}\cdot\prod_{k=1}^{n-1}\frac{n}{\omega^{k}-1}=\frac{n\left(n+1\right)}{2}\cdot\frac{n^{n-1}}{\prod_{k=1}^{n-1}\left(\omega^{k}-1\right)}.
$$

By the identity $\prod_{k=1}^{n-1}\left(1-\omega^{k}\right)=n$ in **Basic Knowledge: Primitive $n$-th Roots of Unity and Eigenvalues of Circulant Matrices**,

$$
\prod_{k=1}^{n-1}\left(\omega^{k}-1\right)=\left(-1\right)^{n-1}n.
$$

Taking account of the direction of the cyclic shift, the result is

$$
D=\left(-1\right)^{\frac{n\left(n-1\right)}{2}}\cdot\frac{n^{n-1}\left(n+1\right)}{2}.
$$

$\blacksquare$

---

## 2.4-11

Let $A=\left(a_{ij}\right)$ be an $n\times n$ matrix over a number field $K$, and denote the cofactor of its $\left(i,j\right)$-entry by $A_{ij}$. Adding the same number $t$ to every entry of $A$, denote the resulting matrix by $A\left(t\right)=\left(a_{ij}+t\right)$. Prove that

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i=1}^{n}\sum_{j=1}^{n}A_{ij}.
$$

### Solution 2.4-11

Split column $1$ of $A\left(t\right)$ into the sum of two columns: column $1$

$$
=\left(a_{11}+t,a_{21}+t,\cdots,a_{n1}+t\right)^{\top}=\left(a_{11},a_{21},\cdots,a_{n1}\right)^{\top}+\left(t,t,\cdots,t\right)^{\top}.
$$

By the multilinearity of the determinant in columns,

$$
\left|A\left(t\right)\right|=\left|A_{1}\left(t\right)\right|+\left|A_{2}\left(t\right)\right|,
$$

where $\left|A_{1}\left(t\right)\right|$ is the determinant with column $1$ the original column and the other columns $a_{ij}+t$, and $\left|A_{2}\left(t\right)\right|$ is the determinant with column $1$ all $t$ and the other columns $a_{ij}+t$.

Continue splitting column $2$ in $\left|A_{1}\left(t\right)\right|$, and so on; finally one obtains

$$
\left|A\left(t\right)\right|=\left|A\right|+\sum_{j=1}^{n}t\cdot\widetilde{A}_{j},
$$

where $\widetilde{A}_{j}$ is the determinant with column $j$ all $1$ and the other columns the columns of $A$.

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand $\widetilde{A}_{j}$ along column $j$; column $j$ is all $1$, so

$$
\widetilde{A}_{j}=\sum_{i=1}^{n}1\cdot A_{ij}=\sum_{i=1}^{n}A_{ij}.
$$

By **Definition 2.4.1 (Minors and Cofactors)**, $A_{ij}$ is the cofactor of the $\left(i,j\right)$-entry.

Therefore

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{j=1}^{n}\sum_{i=1}^{n}A_{ij}.
$$

$\blacksquare$

---

## 2.4-12

Using the formula given in Problem 11, compute the following $n\times n$ determinants:

(1)

$$
\left|\begin{array}{cccc}
1+x_{1}y_{1} & 1+x_{1}y_{2} & \cdots & 1+x_{1}y_{n}\\
1+x_{2}y_{1} & 1+x_{2}y_{2} & \cdots & 1+x_{2}y_{n}\\
\vdots & \vdots & & \vdots\\
1+x_{n}y_{1} & 1+x_{n}y_{2} & \cdots & 1+x_{n}y_{n}
\end{array}\right|.
$$

(2)

$$
\left|\begin{array}{cccc}
1+t & t & \cdots & t\\
t & 2+t & \cdots & t\\
\vdots & \vdots & & \vdots\\
t & t & \cdots & n+t
\end{array}\right|.
$$

### Solution 2.4-12

**(1)** Write the matrix as $A=J+xy^{\top}$, where $J$ is the all-ones matrix, $x=\left(x_{1},\cdots,x_{n}\right)^{\top}$, and $y=\left(y_{1},\cdots,y_{n}\right)^{\top}$.

$A$ is the sum of two rank-$1$ matrices, so $\text{rank}\left(A\right)\le2$.

When $n\ge3$, by **Basic Knowledge: Minor Characterization of Matrix Rank**, $\det\left(A\right)=0$.

When $n=1$, $\det\left(A\right)=1+x_{1}y_{1}$.

When $n=2$,

$$
\det\left(A\right)=\left(1+x_{1}y_{1}\right)\left(1+x_{2}y_{2}\right)-\left(1+x_{1}y_{2}\right)\left(1+x_{2}y_{1}\right)=x_{1}y_{1}+x_{2}y_{2}-x_{1}y_{2}-x_{2}y_{1}=\left(x_{1}-x_{2}\right)\left(y_{1}-y_{2}\right).
$$

**(2)** Let $A=\text{diag}\left(1,2,\cdots,n\right)$; then the desired determinant is $\left|A\left(t\right)\right|$.

By Problem 11,

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i,j}A_{ij}.
$$

$\left|A\right|=n!$.

$A$ is a diagonal matrix; the minors of off-diagonal entries are all $0$, and the cofactors of diagonal entries are $A_{ii}=\frac{n!}{i}$.

Hence

$$
\sum_{i,j}A_{ij}=\sum_{i=1}^{n}\frac{n!}{i}=n!\sum_{i=1}^{n}\frac{1}{i}.
$$

Therefore

$$
\left|A\left(t\right)\right|=n!+t\cdot n!\sum_{i=1}^{n}\frac{1}{i}
=n!\left(1+t\sum_{i=1}^{n}\frac{1}{i}\right).
$$

$\blacksquare$
