# week6

> **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**<br>A common factor of a row of a determinant can be pulled outside the determinant; in particular, if a row of a determinant is zero (all its entries are $0$), then the determinant is $0$.

> **Property 2.3.3 (Splitting When a Row Is a Sum of Two Groups)**<br>If a row of a determinant is the sum of two groups of numbers, then the determinant equals the sum of two determinants: in these two determinants that row is respectively the first group and the second group of numbers, while all other rows are the same as the corresponding rows of the original determinant.

> **Property 2.3.5 (Two Identical Rows Make the Determinant Zero)**<br>If a determinant has two identical rows, its value is $0$; consequently, if two rows are proportional, the determinant is also $0$.

> **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**<br>Adding a multiple of one row to another row leaves the value of the determinant unchanged.

> **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**<br>The $n\times n$ determinant $|A|$ equals the sum of the products of the entries in its $i$-th row and their cofactors, and also the sum of the products of the entries in its $j$-th column and their cofactors, i.e. $|A|=\sum_{k=1}^{n}a_{ik}A_{ik}=\sum_{k=1}^{n}a_{kj}A_{kj}$, where $A_{kj}=\left(-1\right)^{k+j}M_{kj}$ is the cofactor.

---

## 2.3-1(2)

Compute the following determinant:

$$
\left|\begin{array}{rrr}
-1 & 203 & 1/3\\
3 & 298 & 1/2\\
5 & 399 & 2/3
\end{array}\right|.
$$

### Solution 2.3-1(2)

Observe that the entries $203,298,399$ of the $2$nd column can be split into sums of two numbers, namely $203=200+3$, $298=300-2$, $399=400-1$. By **Property 2.3.3 (Splitting When a Row Is a Sum of Two Groups)**, when all entries of a column are sums of two terms, the determinant can be split into the sum of two determinants:

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

By **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**, a common factor of a column can be moved outside the determinant. The $2$nd column of the first determinant has a common factor $100$; pulling it out gives

$$
D_{1}=100\times\left|\begin{array}{rrr}
-1 & 2 & 1/3\\
3 & 3 & 1/2\\
5 & 4 & 2/3
\end{array}\right|.
$$

Expanding directly,

$$
\left|\begin{array}{rrr}
-1 & 2 & 1/3\\
3 & 3 & 1/2\\
5 & 4 & 2/3
\end{array}\right|=-1\times\left(3\times\frac{2}{3}-\frac{1}{2}\times4\right)-2\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times4-3\times5\right)=-1\times\left(2-2\right)-2\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(12-15\right)=0-2\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times\left(-3\right)=1-1=0.
$$

Hence $D_{1}=100\times0=0$.

Compute the second determinant $D_{2}$:

$$
D_{2}=\left|\begin{array}{rrr}
-1 & 3 & 1/3\\
3 & -2 & 1/2\\
5 & -1 & 2/3
\end{array}\right|=-1\times\left(-2\times\frac{2}{3}-\frac{1}{2}\times\left(-1\right)\right)-3\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times\left(-1\right)-\left(-2\right)\times5\right)=-1\times\left(-\frac{4}{3}+\frac{1}{2}\right)-3\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(-3+10\right)=-1\times\left(-\frac{5}{6}\right)-3\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times7=\frac{5}{6}+\frac{3}{2}+\frac{7}{3}=\frac{5}{6}+\frac{9}{6}+\frac{14}{6}=\frac{28}{6}=\frac{14}{3}.
$$

Hence the original determinant is

$$
D=D_{1}+D_{2}=0+\frac{14}{3}=\frac{14}{3}.
$$

$\blacksquare$

---

## 2.3-2(2)

Compute the following $n\times n$ determinant:

$$
\left|\begin{array}{cccc}
a_{1}-b & a_{2} & \cdots & a_{n}\\
a_{1} & a_{2}-b & \cdots & a_{n}\\
\vdots & \vdots & & \vdots\\
a_{1} & a_{2} & \cdots & a_{n}-b
\end{array}\right|.
$$

### Solution 2.3-2(2)

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, adding a multiple of one row to another leaves the determinant unchanged. Add $-1$ times the $n$-th row respectively to rows $1,2,\cdots,n-1$, giving

$$
\left|\begin{array}{rrrrr}
-b & 0 & \cdots & 0 & b\\
0 & -b & \cdots & 0 & b\\
\vdots & \vdots & & \vdots & \vdots\\
0 & 0 & \cdots & -b & b\\
a_{1} & a_{2} & \cdots & a_{n-1} & a_{n}-b
\end{array}\right|.
$$

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along the last column. The entries of the last column are $\left(b,b,\cdots,b,a_{n}-b\right)$.

For $j< n$, the cofactor is $A_{jn}=\left(-1\right)^{j+n}M_{jn}$, where $M_{jn}$ is the $\left(n-1\right)$-determinant obtained by deleting row $j$ and column $n$. In that determinant, row $j$ (the original row $j$ with column $n$ removed) has only its first entry $b_{j}$ nonzero and all others $0$; expanding along that row, the minor is a diagonal determinant, giving $M_{jn}=\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}$.

Hence

$$
\text{determinant}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{j+n}\cdot\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-1\right)^{2n}\left(-b\right)^{n-1}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{2j+n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\left(-1\right)^{n-1}b^{n-1}\sum_{j=1}^{n-1}a_{j}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\left(-b\right)^{n-1}\left(\sum_{j=1}^{n}a_{j}-b\right).
$$

$\blacksquare$

---

## 2.3-3(1)

Prove that

$$
\left|\begin{array}{ccc}
a_{1}-b_{1} & b_{1}-c_{1} & c_{1}-a_{1}\\
a_{2}-b_{2} & b_{2}-c_{2} & c_{2}-a_{2}\\
a_{3}-b_{3} & b_{3}-c_{3} & c_{3}-a_{3}
\end{array}\right|=0.
$$

### Solution 2.3-3(1)

Observe that columns $1$, $2$, and $3$ satisfy: column $1$ $+$ column $2$ $+$ column $3$ $=0$.

Precisely, in row $i$, column $1$ $+$ column $2$ $+$ column $3$

$$
=\left(a_{i}-b_{i}\right)+\left(b_{i}-c_{i}\right)+\left(c_{i}-a_{i}\right)=0.
$$

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, adding a multiple of one column to another leaves the determinant unchanged. Add both column $2$ and column $3$ to column $1$; then all entries of column $1$ become $0$.

By **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**, a determinant whose column is all zeros has value $0$.

Hence the original determinant $=0$. $\blacksquare$

---

## 2.3-4(1)

Compute the following $n\times n$ determinant:

$$
\left|\begin{array}{cccc}
a_{1} & a_{2} & \cdots & a_{n}\\
b_{2} & 1 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
b_{n} & 0 & \cdots & 1
\end{array}\right|.
$$

### Solution 2.3-4(1)

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, adding a multiple of one row to another leaves the determinant unchanged. Add $-a_{2}$ times row $2$ to row $1$, $-a_{3}$ times row $3$ to row $1$, $\cdots$, and $-a_{n}$ times row $n$ to row $1$; then columns $2$ through $n$ of row $1$ all become $0$:

$$
\left|\begin{array}{cccc}
a_{1}-\sum_{j=2}^{n}a_{j}b_{j} & 0 & \cdots & 0\\
b_{2} & 1 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
b_{n} & 0 & \cdots & 1
\end{array}\right|.
$$

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along row $1$; the minor is the $\left(n-1\right)$-identity matrix, whose determinant is $1$. Hence the determinant equals

$$
a_{1}-\sum_{j=2}^{n}a_{j}b_{j}.
$$

$\blacksquare$

---

## 2.3-4(2)

Compute the following $n\times n$ determinant:

$$
\left|\begin{array}{cccc}
a_{1}+b_{1} & a_{1}+b_{2} & \cdots & a_{1}+b_{n}\\
a_{2}+b_{1} & a_{2}+b_{2} & \cdots & a_{2}+b_{n}\\
\vdots & \vdots & & \vdots\\
a_{n}+b_{1} & a_{n}+b_{2} & \cdots & a_{n}+b_{n}
\end{array}\right|.
$$

### Solution 2.3-4(2)

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, adding a multiple of one row to another leaves the determinant unchanged. Add $-1$ times row $1$ respectively to rows $2,3,\cdots,n$, giving

$$
\left|\begin{array}{cccc}
a_{1}+b_{1} & a_{1}+b_{2} & \cdots & a_{1}+b_{n}\\
a_{2}-a_{1} & a_{2}-a_{1} & \cdots & a_{2}-a_{1}\\
\vdots & \vdots & & \vdots\\
a_{n}-a_{1} & a_{n}-a_{1} & \cdots & a_{n}-a_{1}
\end{array}\right|.
$$

When $n\ge3$, every row from row $2$ to row $n$ has identical entries. By **Property 2.3.5 (Two Identical Rows Make the Determinant Zero)**, two identical rows make the determinant $0$. Hence for $n\ge3$ the determinant $=0$.

When $n=1$, the determinant $=a_{1}+b_{1}$.

When $n=2$, by **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, add $-1$ times row $1$ to row $2$, giving

$$
\left|\begin{array}{cc}
a_{1}+b_{1} & a_{1}+b_{2}\\
a_{2}-a_{1} & a_{2}-a_{1}
\end{array}\right|.
$$

By **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**, row $2$ has a common factor $a_{2}-a_{1}$; pulling it out gives

$$
\left(a_{2}-a_{1}\right)\times\left|\begin{array}{cc}
a_{1}+b_{1} & a_{1}+b_{2}\\
1 & 1
\end{array}\right|.
$$

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, add $-1$ times column $2$ to column $1$, giving

$$
\left(a_{2}-a_{1}\right)\times\left|\begin{array}{cc}
b_{1}-b_{2} & a_{1}+b_{2}\\
0 & 1
\end{array}\right|.
$$

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along column $2$, obtaining

$$
\left(a_{2}-a_{1}\right)\times\left(b_{1}-b_{2}\right)=\left(a_{1}-a_{2}\right)\left(b_{2}-b_{1}\right).
$$

In summary,

$$
\det\left(A\right)=
\begin{cases}
a_{1}+b_{1}, & n=1,\\
\left(a_{1}-a_{2}\right)\left(b_{2}-b_{1}\right), & n=2,\\
0, & n\ge3.
\end{cases}
$$

$\blacksquare$
