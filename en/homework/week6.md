# Assignment 6

> **Basic Knowledge 1** (Properties of Determinants)<br>
> (1) interchanging the rows and columns of a determinant (transposition) leaves its value unchanged;
>
> (2) a common factor of a row (column) of a determinant can be pulled outside the determinant sign;
>
> (3) if all elements of a row (column) of a determinant are sums of two terms, then the determinant can be split into the sum of two determinants;
>
> (4) adding a multiple of one row (column) to another row (column) leaves the value of the determinant unchanged;
>
> (5) interchanging two rows (columns) of a determinant changes its sign;
>
> (6) if two rows (columns) of a determinant are identical or proportional, then the determinant is $0$.

### Problem 1

(Problem 2.3-1(2)) Compute the following determinant:

$$
\left|\begin{array}{rrr}
-1 & 203 & 1/3\\
3 & 298 & 1/2\\
5 & 399 & 2/3
\end{array}\right|.
$$

### Solution to Problem 1

Observe that the elements $203,298,399$ in the $2$nd column can be split into sums of two numbers, namely $203=200+3$, $298=300-2$, $399=400-1$. By **Basic Knowledge 1** (Properties of Determinants)(3), if all elements of a column of a determinant are sums of two terms, then the determinant can be split into the sum of two determinants:

$$
\left|\begin{array}{rrr}
-1 & 203 & 1/3\\
3 & 298 & 1/2\\
5 & 399 & 2/3
\end{array}\right|
=
\left|\begin{array}{rrr}
-1 & 200 & 1/3\\
3 & 300 & 1/2\\
5 & 400 & 2/3
\end{array}\right|
+
\left|\begin{array}{rrr}
-1 & 3 & 1/3\\
3 & -2 & 1/2\\
5 & -1 & 2/3
\end{array}\right|.
$$

By **Basic Knowledge 1** (2), a common factor of a column of a determinant can be pulled outside the determinant sign. The $2$nd column of the first determinant has a common factor $100$; pulling it out gives:

$$
D_{1}=100\times\left|\begin{array}{rrr}
-1 & 2 & 1/3\\
3 & 3 & 1/2\\
5 & 4 & 2/3
\end{array}\right|.
$$

By **Basic Knowledge 1** (2), the $3$rd column has a common factor $1/6$ (after putting over a common denominator); to simplify the computation, expand directly:

$$
\begin{aligned}\left|\begin{array}{rrr}
-1 & 2 & 1/3\\
3 & 3 & 1/2\\
5 & 4 & 2/3
\end{array}\right|&=-1\times\left(3\times\frac{2}{3}-\frac{1}{2}\times4\right)-2\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times4-3\times5\right)\\
&=-1\times\left(2-2\right)-2\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(12-15\right)\\
&=0-2\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times\left(-3\right)\\
&=1-1\\
&=0.
\end{aligned}
$$

Hence $D_{1}=100\times0=0$.

Compute the second determinant $D_{2}$:

$$
\begin{aligned}D_{2}&=\left|\begin{array}{rrr}
-1 & 3 & 1/3\\
3 & -2 & 1/2\\
5 & -1 & 2/3
\end{array}\right|\\
&=-1\times\left(-2\times\frac{2}{3}-\frac{1}{2}\times\left(-1\right)\right)-3\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times\left(-1\right)-\left(-2\right)\times5\right)\\
&=-1\times\left(-\frac{4}{3}+\frac{1}{2}\right)-3\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(-3+10\right)\\
&=-1\times\left(-\frac{5}{6}\right)-3\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times7\\
&=\frac{5}{6}+\frac{3}{2}+\frac{7}{3}\\
&=\frac{5}{6}+\frac{9}{6}+\frac{14}{6}\\
&=\frac{28}{6}\\
&=\frac{14}{3}.
\end{aligned}
$$

Hence the original determinant

$$
D=D_{1}+D_{2}=0+\frac{14}{3}=\frac{14}{3}
$$

$\blacksquare$

### Problem 2

(Problem 2.3-2(2)) Compute the following $n$-th order determinant:

$$
\left|\begin{array}{cccc}
a_{1}-b & a_{2} & \cdots & a_{n}\\
a_{1} & a_{2}-b & \cdots & a_{n}\\
\vdots & \vdots & & \vdots\\
a_{1} & a_{2} & \cdots & a_{n}-b
\end{array}\right|.
$$

### Solution to Problem 2

By **Basic Knowledge 1** (Properties of Determinants)(4), adding a multiple of one row to another leaves the value of the determinant unchanged. Add $-1$ times the $n$-th row to rows $1,2,\cdots,n-1$, respectively, giving

$$
\left|\begin{array}{rrrrr}
-b & 0 & \cdots & 0 & b\\
0 & -b & \cdots & 0 & b\\
\vdots & \vdots & & \vdots & \vdots\\
0 & 0 & \cdots & -b & b\\
a_{1} & a_{2} & \cdots & a_{n-1} & a_{n}-b
\end{array}\right|.
$$

Expand along the last column. The elements of the last column are $\left(b,b,\cdots,b,a_{n}-b\right)$.

For $j<n$, the cofactor is $A_{jn}=\left(-1\right)^{j+n}M_{jn}$, where $M_{jn}$ is the $\left(n-1\right)$-th order determinant obtained by deleting the $j$-th row and the $n$-th column. In that determinant, the $j$-th row (the original $j$-th row with the $n$-th column removed) has only the $1$st entry equal to $b_{j}$, with all the rest equal to $0$; expanding along this row, the minor is a diagonal determinant, giving $M_{jn}=\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}$.

Hence

$$
\begin{aligned}\text{行列式}&=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{j+n}\cdot\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-1\right)^{2n}\left(-b\right)^{n-1}\\
&=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{2j+n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}\\
&=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}\\
&=\left(-1\right)^{n-1}b^{n-1}\sum_{j=1}^{n-1}a_{j}+\left(a_{n}-b\right)\left(-b\right)^{n-1}\\
&=\left(-b\right)^{n-1}\left(\sum_{j=1}^{n}a_{j}-b\right).
\end{aligned}
$$

$\blacksquare$

### Problem 3

(Problem 2.3-3(1)) Prove that

$$
\left|\begin{array}{ccc}
a_{1}-b_{1} & b_{1}-c_{1} & c_{1}-a_{1}\\
a_{2}-b_{2} & b_{2}-c_{2} & c_{2}-a_{2}\\
a_{3}-b_{3} & b_{3}-c_{3} & c_{3}-a_{3}
\end{array}\right|=0.
$$

### Solution to Problem 3

Note that the $1$st, $2$nd, and $3$rd columns of the determinant satisfy: the $1$st column + the $2$nd column + the $3$rd column $=0$.

Specifically, for the $i$-th row: the $1$-st column + the $i$-th column + the $i$-th column

$$
=\left(a_{i}-b_{i}\right)+\left(b_{i}-c_{i}\right)+\left(c_{i}-a_{i}\right)=0.
$$

By **Basic Knowledge 1** (Properties of Determinants)(4), adding a multiple of one column to another leaves the value of the determinant unchanged. Add both the $2$nd and $3$rd columns to the $1$st column; then all elements of the $1$st column become $0$.

By **Basic Knowledge 1** (Properties of Determinants), a determinant in which one column is entirely $0$ has value $0$.

Hence the original determinant $=0$. $\blacksquare$

### Problem 4

(Problem 2.3-4(1)) Compute the following $n$-th order determinant:

$$
\left|\begin{array}{cccc}
a_{1} & a_{2} & \cdots & a_{n}\\
b_{2} & 1 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
b_{n} & 0 & \cdots & 1
\end{array}\right|.
$$

### Solution to Problem 4

By **Basic Knowledge 1** (Properties of Determinants)(4), adding a multiple of one row to another leaves the value of the determinant unchanged. Add $-a_{2}$ times the $2$nd row to the $1$st row, $-a_{3}$ times the $3$rd row to the $1$st row, $\cdots$, and $-a_{n}$ times the $n$-th row to the $1$st row; then the $2$nd through $n$-th entries of the $1$st row all become $0$:

$$
\left|\begin{array}{cccc}
a_{1}-\sum_{j=2}^{n}a_{j}b_{j} & 0 & \cdots & 0\\
b_{2} & 1 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
b_{n} & 0 & \cdots & 1
\end{array}\right|.
$$

Expanding along the $1$st row, the minor is the $\left(n-1\right)$-th order identity matrix, whose determinant is $1$. Hence the value of the determinant is

$$
a_{1}-\sum_{j=2}^{n}a_{j}b_{j}.
$$

$\blacksquare$

### Problem 5

(Problem 2.3-4(2)) Compute the following $n$-th order determinant:

$$
\left|\begin{array}{cccc}
a_{1}+b_{1} & a_{1}+b_{2} & \cdots & a_{1}+b_{n}\\
a_{2}+b_{1} & a_{2}+b_{2} & \cdots & a_{2}+b_{n}\\
\vdots & \vdots & & \vdots\\
a_{n}+b_{1} & a_{n}+b_{2} & \cdots & a_{n}+b_{n}
\end{array}\right|.
$$

### Solution to Problem 5

By **Basic Knowledge 1** (Properties of Determinants)(4), adding a multiple of one row to another leaves the value of the determinant unchanged. Add $-1$ times the $1$-st row to rows $2,3,\cdots,n$, respectively, giving

$$
\left|\begin{array}{cccc}
a_{1}+b_{1} & a_{1}+b_{2} & \cdots & a_{1}+b_{n}\\
a_{2}-a_{1} & a_{2}-a_{1} & \cdots & a_{2}-a_{1}\\
\vdots & \vdots & & \vdots\\
a_{n}-a_{1} & a_{n}-a_{1} & \cdots & a_{n}-a_{1}
\end{array}\right|.
$$

When $n\ge3$, the elements of every row from the $2$nd to the $n$-th are identical. By **Basic Knowledge 1** (6), if two rows of a determinant are identical, the determinant is $0$. Hence when $n\ge3$ the determinant $=0$.

When $n=1$, the determinant $=a_{1}+b_{1}$.

When $n=2$, by **Basic Knowledge 1** (4), add $-1$ times the $1$st row to the $2$nd row, giving

$$
\left|\begin{array}{cc}
a_{1}+b_{1} & a_{1}+b_{2}\\
a_{2}-a_{1} & a_{2}-a_{1}
\end{array}\right|.
$$

By **Basic Knowledge 1** (2), the $2$nd row has a common factor $a_{2}-a_{1}$; pulling it out gives:

$$
\left(a_{2}-a_{1}\right)\times\left|\begin{array}{cc}
a_{1}+b_{1} & a_{1}+b_{2}\\
1 & 1
\end{array}\right|.
$$

By **Basic Knowledge 1** (4), add $-1$ times the $2$nd column to the $1$st column, giving

$$
\left(a_{2}-a_{1}\right)\times\left|\begin{array}{cc}
b_{1}-b_{2} & a_{1}+b_{2}\\
0 & 1
\end{array}\right|.
$$

Expanding along the $2$nd column gives

$$
\left(a_{2}-a_{1}\right)\times\left(b_{1}-b_{2}\right)=\left(a_{1}-a_{2}\right)\left(b_{2}-b_{1}\right).
$$

In summary:

$$
\det\left(A\right)=
\begin{cases}
a_{1}+b_{1}, & n=1,\\
\left(a_{1}-a_{2}\right)\left(b_{2}-b_{1}\right), & n=2,\\
0, & n\ge3.
\end{cases}
$$

$\blacksquare$
