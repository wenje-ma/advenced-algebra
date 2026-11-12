# week4

> **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**
> 
> A common factor of a row of a determinant can be pulled outside the determinant; in particular, if a row of a determinant is zero (all its entries are $0$), then the determinant is $0$.

> **Property 2.3.3 (Splitting When a Row Is a Sum of Two Groups)**
> 
> If a row of a determinant is the sum of two groups of numbers, then the determinant equals the sum of two determinants: in these two determinants that row is respectively the first group and the second group of numbers, while all other rows are the same as the corresponding rows of the original determinant.

> **Property 2.3.5 (Two Identical Rows Make the Determinant Zero)**
> 
> If a determinant has two identical rows, its value is $0$; consequently, if two rows are proportional, the determinant is also $0$.

> **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**
> 
> Adding a multiple of one row to another row leaves the value of the determinant unchanged.

> **Definition 2.4.1 (Minors and Cofactors)**
> 
> In the $n\times{n}$ determinant $\left|A\right|$, deleting row $i$ and column $j$, the $\left(n-1\right)$-determinant formed by the remaining entries in their original order is called the minor of the $\left(i,j\right)$-entry of $A$, denoted $M_{ij}$. Setting $A_{ij}=\left(-1\right)^{i+j}M_{ij}$, $A_{ij}$ is called the cofactor of the $\left(i,j\right)$-entry of $A$.

> **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**
> 
> The $n\times{n}$ determinant $\left|A\right|$ equals the sum of the products of the entries in its $i$-th row and their cofactors:

$$
\left|A\right|=a_{i1}A_{i1}+a_{i2}A_{i2}+\cdots+a_{in}A_{in}.
$$

## 2.3-3(1)

Prove that

$$
\left|\begin{array}{ccc}
a_{1}-b_{1}&b_{1}-c_{1}&c_{1}-a_{1}\\
a_{2}-b_{2}&b_{2}-c_{2}&c_{2}-a_{2}\\
a_{3}-b_{3}&b_{3}-c_{3}&c_{3}-a_{3}
\end{array}\right|=0.
$$

### Solution to 2.3-3(1)

Observe that columns $1$, $2$, and $3$ satisfy: column $1$ $+$ column $2$ $+$ column $3$ $=0$.

Precisely, in row $i$, column $1$ $+$ column $2$ $+$ column $3$

$$
=\left(a_{i}-b_{i}\right)+\left(b_{i}-c_{i}\right)+\left(c_{i}-a_{i}\right)=0.
$$

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, adding a multiple of one column to another leaves the determinant unchanged. Add both column $2$ and column $3$ to column $1$; then all entries of column $1$ become $0$.

By **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**, a determinant whose column is all zeros has value $0$.

Hence the original determinant $=0$. $\blacksquare$

## 2.3-4(1)

Compute the following $n\times{n}$ determinant:

$$
\left|\begin{array}{cccc}
a_{1}&a_{2}&\cdots&a_{n}\\
b_{2}&1&\cdots&0\\
\vdots&\vdots&&\vdots\\
b_{n}&0&\cdots&1
\end{array}\right|.
$$

### Solution to 2.3-4(1)

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, adding a multiple of one row to another leaves the determinant unchanged. Add $-a_{2}$ times row $2$ to row $1$, $-a_{3}$ times row $3$ to row $1$, $\cdots$, and $-a_{n}$ times row $n$ to row $1$; then columns $2$ through $n$ of row $1$ all become $0$:

$$
\left|\begin{array}{cccc}
a_{1}-\sum_{j=2}^{n}a_{j}b_{j}&0&\cdots&0\\
b_{2}&1&\cdots&0\\
\vdots&\vdots&&\vdots\\
b_{n}&0&\cdots&1
\end{array}\right|.
$$

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along row $1$; the minor is the $\left(n-1\right)$-identity matrix, whose determinant is $1$. Hence the determinant equals

$$
a_{1}-\sum_{j=2}^{n}a_{j}b_{j}.
$$

$\blacksquare$

## 2.3-4(2)

Compute the following $n\times{n}$ determinant:

$$
\left|\begin{array}{cccc}
a_{1}+b_{1}&a_{1}+b_{2}&\cdots&a_{1}+b_{n}\\
a_{2}+b_{1}&a_{2}+b_{2}&\cdots&a_{2}+b_{n}\\
\vdots&\vdots&&\vdots\\
a_{n}+b_{1}&a_{n}+b_{2}&\cdots&a_{n}+b_{n}
\end{array}\right|.
$$

### Solution to 2.3-4(2)

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, adding a multiple of one row to another leaves the determinant unchanged. Add $-1$ times row $1$ respectively to rows $2,3,\cdots,n$, giving

$$
\left|\begin{array}{cccc}
a_{1}+b_{1}&a_{1}+b_{2}&\cdots&a_{1}+b_{n}\\
a_{2}-a_{1}&a_{2}-a_{1}&\cdots&a_{2}-a_{1}\\
\vdots&\vdots&&\vdots\\
a_{n}-a_{1}&a_{n}-a_{1}&\cdots&a_{n}-a_{1}
\end{array}\right|.
$$

When $n\ge3$, every row from row $2$ to row $n$ has identical entries. By **Property 2.3.5 (Two Identical Rows Make the Determinant Zero)**, two identical rows make the determinant $0$. Hence for $n\ge3$ the determinant $=0$.

When $n=1$, the determinant $=a_{1}+b_{1}$.

When $n=2$, by **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, add $-1$ times row $1$ to row $2$, giving

$$
\left|\begin{array}{cc}
a_{1}+b_{1}&a_{1}+b_{2}\\
a_{2}-a_{1}&a_{2}-a_{1}
\end{array}\right|.
$$

By **Property 2.3.2 (A Common Factor of a Row Can Be Pulled Out)**, row $2$ has a common factor $a_{2}-a_{1}$; pulling it out gives

$$
\left(a_{2}-a_{1}\right)\times\left|\begin{array}{cc}
a_{1}+b_{1}&a_{1}+b_{2}\\
1&1
\end{array}\right|.
$$

By **Property 2.3.7 (Adding a Multiple of One Row to Another Leaves the Determinant Unchanged)**, add $-1$ times column $2$ to column $1$, giving

$$
\left(a_{2}-a_{1}\right)\times\left|\begin{array}{cc}
b_{1}-b_{2}&a_{1}+b_{2}\\
0&1
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
a_{1}+b_{1},&n=1,\\
\left(a_{1}-a_{2}\right)\left(b_{2}-b_{1}\right),&n=2,\\
0,&n\ge3.
\end{cases}
$$

$\blacksquare$

## 2.4-2

Compute the following $n\times{n}$ determinant $\left(n\ge2\right)$:

$$
\left|\begin{array}{cccccc}
a_{1}&a_{2}&a_{3}&\cdots&a_{n-1}&a_{n}\\
1&-1&0&\cdots&0&0\\
0&2&-2&\cdots&0&0\\
\vdots&\vdots&\vdots&&\vdots&\vdots\\
0&0&0&\cdots&n-1&1-n
\end{array}\right|.
$$

### Solution to 2.4-2

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
\left|A\right|=\left(a_{1}+a_{2}+\cdots+a_{n}\right)\cdot{A}_{11}.
$$

By **Definition 2.4.1 (Minors and Cofactors)**,

$$
A_{11}=\left(-1\right)^{1+1}M_{11}=M_{11},
$$

where $M_{11}$ is the $\left(n-1\right)$-determinant after deleting row $1$ and column $1$:

$$
M_{11}=\left|\begin{array}{cccc}
-1&0&\cdots&0\\
0&-2&\cdots&0\\
\vdots&\vdots&&\vdots\\
0&0&\cdots&1-n
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

## 2.4-4

Prove by mathematical induction that, for all $n\ge2$,

$$
\left|\begin{array}{cccccc}
x&0&0&\cdots&0&a_{0}\\
-1&x&0&\cdots&0&a_{1}\\
0&-1&x&\cdots&0&a_{2}\\
\vdots&\vdots&\vdots&&\vdots&\vdots\\
0&0&0&\cdots&x&a_{n-2}\\
0&0&0&\cdots&-1&x+a_{n-1}
\end{array}\right|=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{n}.
$$

### Solution to 2.4-4

Base case $n=2$:

$$
\left|\begin{array}{cc}x&a_{0}\\-1&x+a_{1}\end{array}\right|=x\left(x+a_{1}\right)-\left(-1\right)a_{0}=x^{2}+a_{1}x+a_{0}.
$$

It holds.

Inductive step: assume the conclusion holds for order $n-1$.

For the $n\times{n}$ determinant, by **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along row $1$:

$$
D_{n}=x\cdot{M}_{11}+\left(-1\right)^{1+n}a_{0}\cdot{M}_{1n}.
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

By mathematical induction, the conclusion holds for all $n\ge2$. $\blacksquare$

## 2.4-8

Compute the following $n\times{n}$ determinant $\left(n\ge2\right)$:

$$
\left|\begin{array}{cccccc}
1&2&2&\cdots&2&2\\
2&2&2&\cdots&2&2\\
2&2&3&\cdots&2&2\\
\vdots&\vdots&\vdots&&\vdots&\vdots\\
2&2&2&\cdots&n-1&2\\
2&2&2&\cdots&2&n
\end{array}\right|.
$$

### Solution to 2.4-8

Add $-1$ times row $2$ respectively to row $1$ and to row $i$ for $i=3,4,\cdots,n$:

row $1$ becomes $\left(-1,0,0,\cdots,0\right)$;

row $i$ $\left(i\ge3\right)$ becomes $\left(0,0,\cdots,i-2,\cdots,0\right)$, where $i-2$ lies in column $i$.

The determinant becomes

$$
\left|\begin{array}{cccccc}
-1&0&0&\cdots&0&0\\
2&2&2&\cdots&2&2\\
0&0&1&\cdots&0&0\\
\vdots&\vdots&\vdots&&\vdots&\vdots\\
0&0&0&\cdots&n-2&0\\
0&0&0&\cdots&0&n-2
\end{array}\right|.
$$

By **Theorem 2.4.1 (Expansion of a Determinant Along a Row (Column))**, expand along row $1$: $D=-1\cdot{M}_{11}$.

By **Definition 2.4.1 (Minors and Cofactors)**, $M_{11}$ is the $\left(n-1\right)$-determinant after deleting row $1$ and column $1$. Expanding along its row $2$ (the original row $3$), which has only entry $1$ in column $2$, gives

$$
M_{11}=1\cdot\left(-1\right)^{2+2}\cdot{M}'_{22}=M'_{22}.
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
