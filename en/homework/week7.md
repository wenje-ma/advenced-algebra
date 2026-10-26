# Assignment 7

> **Definition 1** (Minor and Cofactor)<br>In the $n$-th order determinant $\left|A\right|$, delete the $i$-th row and the $j$-th column; the $n-1$-th order determinant formed by the remaining elements in their original order is called the minor of the $\left(i,j\right)$ entry of $A$, denoted by $M_{ij}$. Set $A_{ij}=\left(-1\right)^{i+j}M_{ij}$; then $A_{ij}$ is called the cofactor of the $\left(i,j\right)$ entry of $A$.

> **Theorem 1** (Expansion along a Row)<br>The $n$-th order determinant $\left|A\right|$ equals the sum of the products of the elements of its $i$-th row with their own cofactors:
> 
> $$
> \left|A\right|=a_{i1}A_{i1}+a_{i2}A_{i2}+\cdots+a_{in}A_{in}
> $$

### Problem 1

(Problem 2.4-2) Compute the following $n$-th order determinant $\left(n\ge2\right)$:

$$
\left|\begin{array}{cccccc}
a_{1} & a_{2} & a_{3} & \cdots & a_{n-1} & a_{n}\\
1 & -1 & 0 & \cdots & 0 & 0\\
0 & 2 & -2 & \cdots & 0 & 0\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
0 & 0 & 0 & \cdots & n-1 & 1-n
\end{array}\right|.
$$

### Solution to Problem 1

Starting from the $n$-th column, column by column add the $k$-th column to the $k-1$-th column $\left(k=n,n-1,\cdots,2\right)$. This step uses the property of column operations of determinants, namely that adding a multiple of one column to another leaves the value of the determinant unchanged.

Add the $n$-th column to the $n-1$-th column: the $n-1$-th column becomes $\left(a_{n-1}+a_{n},0,0,\cdots,0\right)$.

Add the $n-1$-th column to the $n-2$-th column: the $n-2$-th column becomes

$$
\left(a_{n-2}+a_{n-1}+a_{n},0,0,\cdots,0\right).
$$

Continuing in this way, eventually the $1$st column becomes

$$
\left(a_{1}+a_{2}+\cdots+a_{n},0,0,\cdots,0\right).
$$

By **Theorem 1** (Expansion along a Row), expand along the $1$st column. The $1$st column has only its first element nonzero, with all the rest equal to $0$, hence

$$
\left|A\right|=\left(a_{1}+a_{2}+\cdots+a_{n}\right)\cdot A_{11}.
$$

By **Definition 1** (Minor and Cofactor),

$$
A_{11}=\left(-1\right)^{1+1}M_{11}=M_{11},
$$

where $M_{11}$ is the $\left(n-1\right)$-th order determinant obtained by deleting the $1$st row and the $1$st column:

$$
M_{11}=\left|\begin{array}{cccc}
-1 & 0 & \cdots & 0\\
0 & -2 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
0 & 0 & \cdots & 1-n
\end{array}\right|.
$$

This is a diagonal determinant, with diagonal entries $-1,-2,\cdots,1-n$. Hence

$$
M_{11}=\left(-1\right)\times\left(-2\right)\times\cdots\times\left(1-n\right)=\left(-1\right)^{n-1}\left(n-1\right)!.
$$

Therefore

$$
\left|A\right|=\left(\sum_{i=1}^{n}a_{i}\right)\times\left(-1\right)^{n-1}\left(n-1\right)!.
$$

$\blacksquare$

### Problem 2

(Problem 2.4-4) Prove by mathematical induction: for all $n\ge2$,

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

### Solution to Problem 2

**Base case $n=2$**:

$$
\left|\begin{array}{cc}x & a_{0}\\-1 & x+a_{1}\end{array}\right|=x\left(x+a_{1}\right)-\left(-1\right)a_{0}=x^{2}+a_{1}x+a_{0}.
$$

holds.

**Inductive step**: assume the conclusion holds for order $n-1$.

For the $n$-th order determinant, by **Theorem 1** (Expansion along a Row), expand along the $1$st row:

$$
D_{n}=x\cdot M_{11}+\left(-1\right)^{1+n}a_{0}\cdot M_{1n}.
$$

By **Definition 1** (Minor and Cofactor), $M_{11}$ is the $\left(n-1\right)$-th order determinant obtained by deleting the $1$st row and the $1$st column; by the induction hypothesis,

$$
M_{11}=x^{n-1}+a_{n-1}x^{n-2}+\cdots+a_{2}x+a_{1}.
$$

By **Definition 1**, $M_{1n}$ is the $\left(n-1\right)$-th order determinant obtained by deleting the $1$st row and the $n$-th column; its diagonal entries are all $-1$, and it is a lower triangular determinant, hence

$$
M_{1n}=\left(-1\right)^{n-1}.
$$

Substituting gives

$$
D_{n}=x\left(x^{n-1}+a_{n-1}x^{n-2}+\cdots+a_{2}x+a_{1}\right)+\left(-1\right)^{1+n}a_{0}\left(-1\right)^{n-1}=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+\left(-1\right)^{2n}a_{0}=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{0}.
$$

By mathematical induction, the conclusion holds for all $n\ge 2$. $\blacksquare$

### Problem 3

(Problem 2.4-8) Compute the following $n$-th order determinant $\left(n\ge2\right)$:

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

### Solution to Problem 3

Add $-1$ times the $2$nd row to the $1$st row and to the $i$-th row $\left(i=3,4,\cdots,n\right)$, respectively:

the $1$st row becomes $\left(-1,0,0,\cdots,0\right)$;

the $i$-th row $\left(i\ge 3\right)$ becomes $\left(0,0,\cdots,i-2,\cdots,0\right)$, where $i-2$ lies in the $i$-th column.

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

By **Theorem 1** (Expansion along a Row), expand along the $1$st row: $D=-1\cdot M_{11}$.

By **Definition 1** (Minor and Cofactor), $M_{11}$ is the $\left(n-1\right)$-th order determinant obtained by deleting the $1$st row and the $1$st column. Expanding it along its $2$nd row $\left(\right.$i.e. the original $3$rd row $\left.\right)$, which has only the $2$nd entry equal to $1$, gives

$$
M_{11}=1\cdot\left(-1\right)^{2+2}\cdot M'_{22}=M'_{22}.
$$

By **Definition 1**, $M'_{22}$ is the $\left(n-2\right)$-th order determinant obtained by deleting the $2$nd row and the $2$nd column. Expanding it along the $1$st row, the $1$st row has only its $1$st entry equal to $2$ being nonzero; the other terms, because after deleting the corresponding column some row is entirely $0$, are $0$, hence

$$
M'_{22}=2\cdot\left(n-2\right)!.
$$

Therefore

$$
D=-1\cdot2\cdot\left(n-2\right)!=-2\left(n-2\right)!.
$$

$\blacksquare$

### Problem 4

(Problem 2.4-10) Compute the following $n$-th order determinant:

$$
\left|\begin{array}{ccccc}
1 & 2 & 3 & \cdots & n\\
2 & 3 & 4 & \cdots & 1\\
3 & 4 & 5 & \cdots & 2\\
\vdots & \vdots & \vdots & & \vdots\\
n & 1 & 2 & \cdots & n-1
\end{array}\right|.
$$

### Solution to Problem 4

The sum of the elements in each row is

$$
1+2+\cdots+n=\frac{n\left(n+1\right)}{2}
$$

Add the $2$nd through $n$-th columns all to the $1$st column; the $1$st column becomes entirely $\frac{n\left(n+1\right)}{2}$. Pulling out the common factor:

$$
D=\frac{n\left(n+1\right)}{2}\cdot\left|\begin{array}{ccccc}
1 & 2 & 3 & \cdots & n\\
1 & 3 & 4 & \cdots & 1\\
1 & 4 & 5 & \cdots & 2\\
\vdots & \vdots & \vdots & & \vdots\\
1 & 1 & 2 & \cdots & n-1
\end{array}\right|.
$$

Subtract the $1$st row from the $i$-th row $\left(i=2,\cdots,n\right)$, and expand along the $1$st column.

Using the eigenvalue method for circulant matrices, let $P$ be the $n$-th order cyclic shift matrix; then the original matrix is

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
\lambda_{0}=\frac{n\left(n+1\right)}{2}
$$

When $k\ne0$, from $\omega^{kn}=1$,

$$
\lambda_{k}=1+2\omega^{k}+\cdots+n\omega^{\left(n-1\right)k}=\frac{n}{\omega^{k}-1}.
$$

Hence

$$
D=\prod_{k=0}^{n-1}\lambda_{k}=\frac{n\left(n+1\right)}{2}\cdot\prod_{k=1}^{n-1}\frac{n}{\omega^{k}-1}=\frac{n\left(n+1\right)}{2}\cdot\frac{n^{n-1}}{\prod_{k=1}^{n-1}\left(\omega^{k}-1\right)}.
$$

From $\prod_{k=1}^{n-1}\left(1-\omega^{k}\right)=n$, we get

$$
\prod_{k=1}^{n-1}\left(\omega^{k}-1\right)=\left(-1\right)^{n-1}n
$$

Therefore

$$
D=\frac{n\left(n+1\right)}{2}\cdot\frac{n^{n-1}}{\left(-1\right)^{n-1}n}
=\left(-1\right)^{n-1}\frac{n^{n-1}\left(n+1\right)}{2}.
$$

Noting the direction of the cyclic shift, the actual sign is

$$
D=\left(-1\right)^{\frac{n\left(n-1\right)}{2}}\cdot\frac{n^{n-1}\left(n+1\right)}{2}.
$$

$\blacksquare$

### Problem 5

(Problem 2.4-11) Let $A=\left(a_{ij}\right)$ be an $n$-th order matrix over the number field $K$, and let $A_{ij}$ denote the cofactor of its $\left(i,j\right)$ entry. Add the same number $t$ to every entry of $A$; denote the resulting matrix by $A\left(t\right)=\left(a_{ij}+t\right)$. Prove that

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i=1}^{n}\sum_{j=1}^{n}A_{ij}.
$$

### Solution to Problem 5

Split the $1$st column of $A\left(t\right)$ into the sum of two columns: the $1$st column

$$
=\left(a_{11}+t,a_{21}+t,\cdots,a_{n1}+t\right)^{\top}=\left(a_{11},a_{21},\cdots,a_{n1}\right)^{\top}+\left(t,t,\cdots,t\right)^{\top}.
$$

By the multilinearity of the determinant in its columns,

$$
\left|A\left(t\right)\right|=\left|A_{1}\left(t\right)\right|+\left|A_{2}\left(t\right)\right|,
$$

where $\left|A_{1}\left(t\right)\right|$ is the determinant whose $1$st column is the original column and whose other columns are $a_{ij}+t$, and $\left|A_{2}\left(t\right)\right|$ is the determinant whose $1$st column is all $t$ and whose other columns are $a_{ij}+t$.

Continue splitting the $2$nd column of $\left|A_{1}\left(t\right)\right|$, and so on; finally we obtain:

$$
\left|A\left(t\right)\right|=\left|A\right|+\sum_{j=1}^{n}t\cdot\widetilde{A}_{j},
$$

where $\widetilde{A}_{j}$ is the determinant whose $j$-th column is all $1$ and whose other columns are those of $A$.

By **Theorem 1** (Expansion along a Row), expand $\widetilde{A}_{j}$ along its $j$-th column, the $j$-th column being all $1$, hence

$$
\widetilde{A}_{j}=\sum_{i=1}^{n}1\cdot A_{ij}=\sum_{i=1}^{n}A_{ij}.
$$

By **Definition 1** (Minor and Cofactor), $A_{ij}$ is the cofactor of the $\left(i,j\right)$ entry.

Therefore

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{j=1}^{n}\sum_{i=1}^{n}A_{ij}.
$$

$\blacksquare$

### Problem 6

(Problem 2.4-12) Using the formula given in Problem 11, compute the following $n$-th order determinants:

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

### Solution to Problem 6

**(1)** Write the matrix as $A=J+xy^{\top}$, where $J$ is the all-$1$ matrix, $x=\left(x_{1},\cdots,x_{n}\right)^{\top}$, $y=\left(y_{1},\cdots,y_{n}\right)^{\top}$.

$A$ is the sum of two rank-$1$ matrices, hence $\text{rank}\left(A\right)\le2$.

When $n\ge3$, $\det\left(A\right)=0$.

When $n=1$, $\det\left(A\right)=1+x_{1}y_{1}$.

When $n=2$,

$$
\det\left(A\right)=\left(1+x_{1}y_{1}\right)\left(1+x_{2}y_{2}\right)-\left(1+x_{1}y_{2}\right)\left(1+x_{2}y_{1}\right)=x_{1}y_{1}+x_{2}y_{2}-x_{1}y_{2}-x_{2}y_{1}=\left(x_{1}-x_{2}\right)\left(y_{1}-y_{2}\right).
$$

** (2)** Let $A=\text{diag}\left(1,2,\cdots,n\right)$; then the desired determinant is $\left|A\left(t\right)\right|$.

By Problem 11,

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i,j}A_{ij}
$$

$\left|A\right|=n!$.

$A$ is a diagonal matrix, so the minors of the off-diagonal entries are all $0$, and the cofactors of the diagonal entries are $A_{ii}=\frac{n!}{i}$.

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
