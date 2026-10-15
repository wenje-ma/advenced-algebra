# Assignment 2

> **Theorem 1** (Criterion for the Solutions of a System of Linear Equations)<br>By applying elementary row operations to the augmented matrix of an $n$-variable system of linear equations and reducing it to a row echelon matrix:
> (1) if the corresponding echelon system exhibits $0=d$($d\ne 0$), then the original system has no solution;
>
> (2) if $0=d$ does not occur, then there is a solution, and when the number of nonzero rows of the echelon matrix equals the number $n$ of unknowns there is a unique solution, while when the number of nonzero rows is $r<n$ there are infinitely many solutions.

### Problem 1

(Problem 1.2-2) For what value of $a$ does the following system of linear equations have a unique solution? For what value of $a$ does this system have no solution?

$$
\begin{cases}
x_{1}+x_{2}+x_{3}=3,\\
x_{1}+2x_{2}-ax_{3}=9,\\
2x_{1}-x_{2}+3x_{3}=6.
\end{cases}
$$

### Solution to Problem 1

By **Theorem 1** (Criterion for the Solutions of a System of Linear Equations), apply elementary row operations to the augmented matrix to reduce it to row echelon form:

$$
\left[\begin{array}{rrr|r}
1 & 1 & 1 & 3\\
1 & 2 & -a & 9\\
2 & -1 & 3 & 6
\end{array}\right]
\xrightarrow{\left(2\right)-\left(1\right),\left(3\right)-2\left(1\right)}
\left[\begin{array}{rrr|r}
1 & 1 & 1 & 3\\
0 & 1 & -a-1 & 6\\
0 & -3 & 1 & 0
\end{array}\right]
\xrightarrow{\left(3\right)+3\left(2\right)}
\left[\begin{array}{rrr|r}
1 & 1 & 1 & 3\\
0 & 1 & -a-1 & 6\\
0 & 0 & -3a-2 & 18
\end{array}\right].
$$

By **Theorem 1**, when $-3a-2\ne 0$, i.e. $a\ne-\frac{2}{3}$, the echelon matrix has $3$ nonzero rows, equal to the number $3$ of unknowns, and the system has a unique solution.

By **Theorem 1**, when $-3a-2=0$, i.e. $a=-\frac{2}{3}$, the $3$rd row becomes $0=18$, exhibiting $0=d$($d\ne 0$), and the system has no solution.

In summary, there is a unique solution when $a\ne-\frac{2}{3}$, and no solution when $a=-\frac{2}{3}$. $\blacksquare$

### Problem 2

(Problem 1.2-5) For what values of $c$ and $d$ does the following system of linear equations have a solution? When it has a solution, find all its solutions.

$$
\begin{cases}
x_{1}+x_{2}+x_{3}+x_{4}+x_{5}=1,\\
3x_{1}+2x_{2}+x_{3}+x_{4}-3x_{5}=c,\\
x_{2}+2x_{3}+2x_{4}+6x_{5}=3,\\
5x_{1}+4x_{2}+3x_{3}+3x_{4}-x_{5}=d.
\end{cases}
$$

### Solution to Problem 2

By **Theorem 1** (Criterion for the Solutions of a System of Linear Equations), apply elementary row operations to the augmented matrix to reduce it to row echelon form:

$$
\left[\begin{array}{rrrrr\left|r}
1 & 1 & 1 & 1 & 1 & 1\\
3 & 2 & 1 & 1 & -3 & c\\
0 & 1 & 2 & 2 & 6 & 3\\
5 & 4 & 3 & 3 & -1 & d
\end{array}\right]
\xrightarrow{\left(2\right)-3\left(1\right),\left(4\right)-5\left(1\right)}
\left[\begin{array}{rrrrr\right|r}
1 & 1 & 1 & 1 & 1 & 1\\
0 & -1 & -2 & -2 & -6 & c-3\\
0 & 1 & 2 & 2 & 6 & 3\\
0 & -1 & -2 & -2 & -6 & d-5
\end{array}\right].
$$

By **Theorem 1**, continue with elementary row operations: perform (2) $\times\left(-1\right)$, and replace (4) by (4) $-$(2) [the replaced row]:

$$
\left[\begin{array}{rrrrr\left|r}
1 & 1 & 1 & 1 & 1 & 1\\
0 & 1 & 2 & 2 & 6 & 3-c\\
0 & 1 & 2 & 2 & 6 & 3\\
0 & -1 & -2 & -2 & -6 & d-5
\end{array}\right]
\xrightarrow{\left(3\right)-\left(2\right),\left(4\right)+\left(2\right)}
\left[\begin{array}{rrrrr\right|r}
1 & 1 & 1 & 1 & 1 & 1\\
0 & 1 & 2 & 2 & 6 & 3-c\\
0 & 0 & 0 & 0 & 0 & c\\
0 & 0 & 0 & 0 & 0 & d-c-2
\end{array}\right].
$$

By **Theorem 1**, the system has a solution if and only if $0=d$ does not occur, i.e. $c=0$ and $d-c-2=0$, namely $c=0$ and $d=2$.

When $c=0,d=2$, by **Theorem 1**, the echelon matrix has $2$ nonzero rows, less than the number $5$ of unknowns, and there are infinitely many solutions. Continue reducing to reduced row echelon form:

From (2):

$$
x_{2}+2x_{3}+2x_{4}+6x_{5}=3.
$$

From (1) $-$(2): $x_{1}-x_{3}-x_{4}-5x_{5}=-2$.

Let $x_{3}=c_{1},x_{4}=c_{2},x_{5}=c_{3}$ be free unknowns; then

$$
\begin{cases}
x_{1}=-2+c_{1}+c_{2}+5c_{3},\\
x_{2}=3-2c_{1}-2c_{2}-6c_{3},\\
x_{3}=c_{1},\\
x_{4}=c_{2},\\
x_{5}=c_{3},
\end{cases}
$$

where $c_{1},c_{2},c_{3}$ are arbitrary constants. $\blacksquare$

### Problem 3

(Problem 1.2-6) Is there a quadratic function $f\left(x\right)=ax^{2}+bx+c$ whose graph passes through the following $4$ points:

$$
P\left(1,2\right),Q\left(-1,3\right),M\left(-4,5\right),N\left(0,2\right)
$$

?

### Solution to Problem 3

If the graph of the quadratic function $f\left(x\right)=ax^{2}+bx+c$ passes through these $4$ points, then $a,b,c$ should satisfy the system:

$$
\begin{cases}
a+b+c=2,\\
a-b+c=3,\\
16a-4b+c=5,\\
c=2.
\end{cases}
$$

From the $4$th equation $c=2$, substituting into the first two equations:

$$
\begin{cases}
a+b=0,\\
a-b=1,
\end{cases}
$$

solving gives $a=\frac{1}{2},b=-\frac{1}{2}$.

Substituting into the $3$rd equation to verify:

$$
16\times\frac{1}{2}-4\times\left(-\frac{1}{2}\right)+2=8+2+2=12\ne 5.
$$

Hence the $3$rd equation is not satisfied. Therefore no such quadratic function exists. $\blacksquare$

### Problem 4

(Problem 1.2-8) An investor wants to invest $1$ ten-thousand yuan in $3$ enterprises $A_{1},A_{2},A_{3}$, with profit rates of $12\%,15\%,22\%$, respectively. If the amount he invests in $A_{1}$ equals the sum of the amounts invested in $A_{2}$ and $A_{3}$, find the maximum and minimum values of the total profit $l$ (in thousands of yuan). At that time, how many thousands of yuan are invested in $A_{1},A_{2},A_{3}$, respectively?

### Solution to Problem 4

Let the amounts invested in $A_{1},A_{2},A_{3}$ be $x_{1},x_{2},x_{3}$, respectively (in thousands of yuan). The total investment is $10$ thousand yuan, and $x_{1}=x_{2}+x_{3}$.

From $x_{1}=x_{2}+x_{3}$ and $x_{1}+x_{2}+x_{3}=10$, we get

$$
2x_{1}=10\Rightarrow x_{1}=5, x_{2}+x_{3}=5.
$$

The total profit

$$
\begin{aligned}l&=0.12x_{1}+0.15x_{2}+0.22x_{3}\\
&=0.12\times5+0.15x_{2}+0.22x_{3}\\
&=0.6+0.15x_{2}+0.22x_{3}.
\end{aligned}
$$

From $x_{2}=5-x_{3}$, substituting:

$$
\begin{aligned}l&=0.6+0.15\left(5-x_{3}\right)+0.22x_{3}\\
&=0.6+0.75-0.15x_{3}+0.22x_{3}\\
&=1.35+0.07x_{3}.
\end{aligned}
$$

Since the investment amounts are nonnegative: $x_{2}\ge 0,x_{3}\ge 0$, hence $0\le x_{3}\le 5$.

When $x_{3}=0$, $l$ takes its minimum value $1.35$, and then $x_{1}=5,x_{2}=5,x_{3}=0$.

When $x_{3}=5$, $l$ takes its maximum value $1.35+0.07\times5=1.7$, and then $x_{1}=5,x_{2}=0,x_{3}=5$.

Hence the minimum value of the total profit $l$ is $1.35$ thousand yuan (investing five thousand in $A_{1}$, five thousand in $A_{2}$, and zero in $A_{3}$), and the maximum value is $1.7$ thousand yuan (investing five thousand in $A_{1}$, zero in $A_{2}$, and five thousand in $A_{3}$). $\blacksquare$
