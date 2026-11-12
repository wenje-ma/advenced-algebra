# week2

> **Theorem 1.2.1 (Criterion for the Number of Solutions of a Linear System)**
> 
> Reduce the augmented matrix of an $n$-variable linear system to a row echelon matrix by elementary row operations: (1) if the corresponding echelon system exhibits $0=d$ ($d\ne0$), then the original system has no solution; (2) if $0=d$ does not appear, then there is a solution: when the number of nonzero rows of the echelon matrix equals the number $n$ of unknowns there is a unique solution, and when the number of nonzero rows is $r<{}n$ there are infinitely many solutions.

> **Definition 1.3.1 (Number Field)**
> 
> Let $K$ be a subset of the set of complex numbers. If $K$ satisfies: (1) $0,1\in{K}$; (2) it is closed under addition, subtraction, multiplication, and division (with nonzero divisor), then $K$ is called a number field.

> **Proposition 2.1.1 (Criterion for a Unique Solution of a Two-Variable Linear System)**
> 
> A two-equation linear system in two variables has a unique solution if and only if its coefficient determinant is nonzero; in that case the unique solution is given by the Cramer formula, i.e. two fractions whose numerators are the $2\times2$ determinants obtained by replacing the $1$st and $2$nd columns of the coefficient determinant by the constant terms of the system.

> **Definition 2.2.1 ($n\times{n}$ Determinant)**
> 
> An $n\times{n}$ determinant is an algebraic sum of $n!$ terms, each term being a product of $n$ entries from distinct rows and distinct columns; after these $n$ entries are arranged so that their row indices are in natural order, the term carries a plus sign when the permutation formed by the column indices is even and a minus sign when it is odd. Namely,

$$
\left|\begin{array}{cccc}
a_{11}&a_{12}&\cdots&a_{1n}\\
a_{21}&a_{22}&\cdots&a_{2n}\\
\vdots&\vdots&&\vdots\\
a_{n1}&a_{n2}&\cdots&a_{nn}
\end{array}\right|=\sum_{j_{1}j_{2}\cdots{j}_{n}}\left(-1\right)^{\tau\left(j_{1}j_{2}\cdots{j}_{n}\right)}a_{1j_{1}}a_{2j_{2}}\cdots{a}_{nj_{n}}.
$$

## 1.2-6

Does there exist a quadratic function $f\left(x\right)=ax^{2}+bx+c$ whose graph passes through the following $4$ points:

$$
P\left(1,2\right),Q\left(-1,3\right),M\left(-4,5\right),N\left(0,2\right)
$$

?

### Solution to 1.2-6

If the graph of the quadratic function $f\left(x\right)=ax^{2}+bx+c$ passes through these $4$ points, then $a,b,c$ must satisfy the system:

$$
\begin{cases}
a+b+c=2,\\
a-b+c=3,\\
16a-4b+c=5,\\
c=2.
\end{cases}
$$

From the $4$th equation $c=2$, substitute into the first two:

$$
\begin{cases}
a+b=0,\\
a-b=1,
\end{cases}
$$

which gives $a=\frac{1}{2},b=-\frac{1}{2}$.

Substitute into the $3$rd equation to verify:

$$
16\times\frac{1}{2}-4\times\left(-\frac{1}{2}\right)+2=8+2+2=12\ne5.
$$

Hence the $3$rd equation is not satisfied. Therefore no such quadratic function exists.

$\blacksquare$

## 1.2-8

An investor wants to invest $1$ ten-thousand yuan in $3$ enterprises $A_{1},A_{2},A_{3}$, with profit rates of $12\%,15\%,22\%$, respectively. If the amount he invests in $A_{1}$ equals the sum of the amounts invested in $A_{2}$ and $A_{3}$, find the maximum and minimum values of the total profit $l$ (in thousand yuan). How much (in thousand yuan) should be invested in $A_{1},A_{2},A_{3}$ in each case?

### Solution to 1.2-8

Let the amounts invested in $A_{1},A_{2},A_{3}$ be $x_{1},x_{2},x_{3}$ (in thousand yuan). The total investment is $10$ thousand yuan, and $x_{1}=x_{2}+x_{3}$.

From $x_{1}=x_{2}+x_{3}$ and $x_{1}+x_{2}+x_{3}=10$, we get

$$
2x_{1}=10\Rightarrow{x}_{1}=5,x_{2}+x_{3}=5.
$$

The total profit is

$$
l=0.12x_{1}+0.15x_{2}+0.22x_{3}=0.12\times5+0.15x_{2}+0.22x_{3}=0.6+0.15x_{2}+0.22x_{3}.
$$

From $x_{2}=5-x_{3}$, substitute:

$$
l=0.6+0.15\left(5-x_{3}\right)+0.22x_{3}=0.6+0.75-0.15x_{3}+0.22x_{3}=1.35+0.07x_{3}.
$$

Since the investment amounts are nonnegative: $x_{2}\ge0,x_{3}\ge0$, we have $0\le{x}_{3}\le5$.

When $x_{3}=0$, $l$ attains its minimum $1.35$, at which point $x_{1}=5,x_{2}=5,x_{3}=0$.

When $x_{3}=5$, $l$ attains its maximum $1.35+0.07\times5=1.7$, at which point $x_{1}=5,x_{2}=0,x_{3}=5$.

Hence the minimum total profit $l$ is $1.35$ thousand yuan (investing $5$ thousand in $A_{1}$, $5$ thousand in $A_{2}$, and $0$ in $A_{3}$), and the maximum is $1.7$ thousand yuan (investing $5$ thousand in $A_{1}$, $0$ in $A_{2}$, and $5$ thousand in $A_{3}$).

$\blacksquare$

## 1.3-1

Let

$$
\mathbb{Q}\left(i\right)=\left\{a+bi\mid{a},b\in\mathbb{Q}\right\},
$$

and prove that $\mathbb{Q}\left(i\right)$ is a number field.

### Solution to 1.3-1

By the requirements of **Definition 1.3.1 (Number Field)**, we must verify that $\mathbb{Q}\left(i\right)$ satisfies $0,1\in{K}$ and is closed under addition, subtraction, multiplication, and division.

Verify $0,1\in\mathbb{Q}\left(i\right)$. By condition (1) of **Definition 1.3.1 (Number Field)**, clearly $0=0+0\cdot{i}\in\mathbb{Q}\left(i\right)$ and $1=1+0\cdot{i}\in\mathbb{Q}\left(i\right)$.

Verify closure under addition. By condition (2) of **Definition 1.3.1 (Number Field)**, take any

$$
\alpha=a+bi,\beta=c+di\in\mathbb{Q}\left(i\right),
$$

where $a,b,c,d\in\mathbb{Q}$; then

$$
\alpha+\beta=\left(a+c\right)+\left(b+d\right)i.
$$

Since the rationals are closed under addition (Closure of the Rational Field under the Four Arithmetic Operations), $a+c\in\mathbb{Q}$ and $b+d\in\mathbb{Q}$, so $\alpha+\beta\in\mathbb{Q}\left(i\right)$.

Verify closure under subtraction. By condition (2) of **Definition 1.3.1 (Number Field)**, similarly,

$$
\alpha-\beta=\left(a-c\right)+\left(b-d\right)i,
$$

and $a-c\in\mathbb{Q}$, $b-d\in\mathbb{Q}$ (Closure of the Rational Field under the Four Arithmetic Operations), so $\alpha-\beta\in\mathbb{Q}\left(i\right)$.

Verify closure under multiplication. By condition (2) of **Definition 1.3.1 (Number Field)**,

$$
\alpha\beta=\left(a+bi\right)\left(c+di\right)=\left(ac-bd\right)+\left(ad+bc\right)i.
$$

Since the rationals are closed under addition, subtraction, and multiplication (Closure of the Rational Field under the Four Arithmetic Operations), $ac-bd\in\mathbb{Q}$ and $ad+bc\in\mathbb{Q}$, so $\alpha\beta\in\mathbb{Q}\left(i\right)$.

Verify closure under division. By condition (2) of **Definition 1.3.1 (Number Field)**, let $\beta=c+di\ne0$; then $c^{2}+d^{2}\ne0$, and

$$
\frac{\alpha}{\beta}=\frac{a+bi}{c+di}=\frac{\left(a+bi\right)\left(c-di\right)}{\left(c+di\right)\left(c-di\right)}=\frac{ac+bd}{c^{2}+d^{2}}+\frac{bc-ad}{c^{2}+d^{2}}i.
$$

Since the rationals are closed under addition, subtraction, multiplication, and division (with nonzero divisor) (Closure of the Rational Field under the Four Arithmetic Operations), $\frac{ac+bd}{c^{2}+d^{2}}\in\mathbb{Q}$ and $\frac{bc-ad}{c^{2}+d^{2}}\in\mathbb{Q}$, so $\frac{\alpha}{\beta}\in\mathbb{Q}\left(i\right)$.

In summary, $\mathbb{Q}\left(i\right)$ satisfies all conditions of **Definition 1.3.1 (Number Field)**, so $\mathbb{Q}\left(i\right)$ is a number field.

$\blacksquare$

## 2.1-1(1)

Find the inversion number of the permutation $315462$ and determine its parity.

### Solution to 2.1-1(1)

By Inversions, the Number of Inversions, and Even/Odd Permutations, count the inversions digit by digit:

- after $3$, the numbers smaller than $3$ are $1,2$, contributing $2$ inversions;
- after $1$, there is no number smaller than $1$, contributing $0$;
- after $5$, the numbers smaller than $5$ are $4,2$, contributing $2$;
- after $4$, the number smaller than $4$ is $2$, contributing $1$;
- after $6$, the number smaller than $6$ is $2$, contributing $1$;
- after $2$, there is no number smaller than $2$, contributing $0$.

Hence

$$
\tau\left(315462\right)=2+0+2+1+1+0=6.
$$

By Inversions, the Number of Inversions, and Even/Odd Permutations, $\tau=6$ is even, so $315462$ is an even permutation.

$\blacksquare$

## 2.1-1(4)

Find the inversion number of the permutation $7654321$ and determine its parity.

### Solution to 2.1-1(4)

By Inversions, the Number of Inversions, and Even/Odd Permutations, this is the fully reversed $7$-permutation, whose inversion number is

$$
\tau\left(7654321\right)=6+5+4+3+2+1+0=21.
$$

By Inversions, the Number of Inversions, and Even/Odd Permutations, $\tau=21$ is odd, so $7654321$ is an odd permutation.

$\blacksquare$

## 2.1-1(7)

Find the inversion number of the permutation $123456789$ and determine its parity.

### Solution to 2.1-1(7)

By Inversions, the Number of Inversions, and Even/Odd Permutations, this is the natural-order permutation, which has no inversions, so

$$
\tau\left(123456789\right)=0.
$$

By Inversions, the Number of Inversions, and Even/Odd Permutations, $\tau=0$ is even, so $123456789$ is an even permutation.

$\blacksquare$

## 2.1-2

Find the inversion number of the following $n$-permutations:

(1) $\left(n-1\right)\left(n-2\right)\cdots21n$;

(2) $23\cdots\left(n-1\right)n1$.

### Solution to 2.1-2

By Inversions, the Number of Inversions, and Even/Odd Permutations:

(1) In the permutation $\left(n-1\right)\left(n-2\right)\cdots21n$, the first $n-1$ numbers are in fully reversed order, and the last number $n$ is the largest, producing no inversion. The inversion number of the first $n-1$ numbers is

$$
\left(n-2\right)+\left(n-3\right)+\cdots+1+0=\frac{\left(n-2\right)\left(n-1\right)}{2}.
$$

Hence

$$
\tau=\frac{\left(n-1\right)\left(n-2\right)}{2}.
$$

(2) In the permutation $23\cdots\left(n-1\right)n1$, the number $1$ is at the end, and the preceding $n-1$ numbers $2,3,\cdots,n$ are all larger than $1$, each forming an inversion with $1$. Between the remaining numbers the order is natural, producing no inversion. Hence

$$
\tau=n-1.
$$

$\blacksquare$

## 2.1-8

Using $2\times2$ determinants, determine whether the following two-variable linear system has a unique solution, and when it does, find that solution:

$$
\begin{cases}
2x_{1}-3x_{2}=7,\\
5x_{1}+4x_{2}=6.
\end{cases}
$$

### Solution to 2.1-8

The coefficient determinant is

$$
\left|\begin{array}{rr}
2&-3\\
5&4
\end{array}\right|=2\times4-\left(-3\right)\times5=8+15=23\ne0.
$$

By **Proposition 2.1.1 (Criterion for a Unique Solution of a Two-Variable Linear System)**, the system has a unique solution.

By the Cramer formula given in that proposition:

$$
x_{1}=\frac{\left|\begin{array}{rr}7&-3\\6&4\end{array}\right|}{23}=\frac{7\times4-\left(-3\right)\times6}{23}=\frac{28+18}{23}=\frac{46}{23}=2,
$$

$$
x_{2}=\frac{\left|\begin{array}{rr}2&7\\5&6\end{array}\right|}{23}=\frac{2\times6-7\times5}{23}=\frac{12-35}{23}=\frac{-23}{23}=-1.
$$

Hence the unique solution is $\left(x_{1},x_{2}\right)=\left(2,-1\right)$.

$\blacksquare$

## 2.2-1(3)

Compute the following determinant by the definition:

$$
\left|\begin{array}{ccccc}
0&b_{1}&0&\cdots&0\\
0&0&b_{2}&\cdots&0\\
\vdots&\vdots&\vdots&&\vdots\\
0&0&0&\cdots&b_{n-1}\\
b_{n}&0&0&\cdots&0
\end{array}\right|.
$$

### Solution to 2.2-1(3)

By **Definition 2.2.1 ($n\times{n}$ Determinant)**, each term of the determinant is a product of $n$ entries from distinct rows and distinct columns.

By **Definition 2.2.1 ($n\times{n}$ Determinant)**, determine the unique nonzero entry row by row: row $1$ has only $b_{1}$ in column $2$ nonzero, row $2$ has only $b_{2}$ in column $3$ nonzero, $\cdots$, row $n-1$ has only $b_{n-1}$ in column $n$ nonzero, and row $n$ has only $b_{n}$ in column $1$ nonzero. Hence the only nonzero term is $b_{1}b_{2}\cdots{b}_{n}$.

By **Definition 2.2.1 ($n\times{n}$ Determinant)**, the column-index permutation of this nonzero term is $2,3,\cdots,n,1$, whose inversion number is

$$
\tau\left(2,3,\cdots,n,1\right)=n-1.
$$

By the sign convention in **Definition 2.2.1 ($n\times{n}$ Determinant)**, even permutations carry a plus sign and odd permutations a minus sign, so the determinant equals

$$
\left(-1\right)^{n-1}b_{1}b_{2}\cdots{b}_{n}.
$$

$\blacksquare$
