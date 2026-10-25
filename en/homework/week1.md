# Assignment 1

> **Definition 1** (Elementary Operations on Systems of Linear Equations)<br>The following three operations are performed on a system of linear equations:
> (1) add a multiple of one equation to another;
> 
> (2) interchange the positions of two equations;
> 
> (3) multiply an equation by a nonzero scalar. These three operations are collectively called the elementary operations on systems of linear equations. A system obtained by elementary operations has the same solution set as the original system.

> **Definition 2** (Row Echelon Matrix)<br>In a matrix, rows whose elements are all $0$ (zero rows) lie below; in a row whose elements are not all $0$ (nonzero row), the first element not equal to $0$ counted from the left is called the pivot, and the column index of the pivot of each nonzero row strictly increases as the row index increases.

> **Definition 3** (Reduced Row Echelon Matrix)<br>On the basis of a row echelon matrix, the pivot of each nonzero row is $1$, and all other elements in the column containing each pivot are $0$.

> **Basic Knowledge 1** (Gauss–Jordan Algorithm)<br>By applying elementary row operations to the augmented matrix of a system of linear equations and reducing it to a reduced row echelon matrix, one can write down the solution directly. If the corresponding echelon system exhibits $0=d$($d\ne 0$), then the original system has no solution.

### Problem 1

(Problem 1.1-1(4)) Solve the following system of linear equations:

$$
\begin{cases}
x_{1}+3x_{2}-7x_{3}=-8,\\
2x_{1}+5x_{2}+4x_{3}=4,\\
-3x_{1}-7x_{2}-2x_{3}=-3,\\
x_{1}+4x_{2}-12x_{3}=-15.
\end{cases}
$$

### Solution to Problem 1

By **Basic Knowledge 1** (Gauss–Jordan Algorithm), apply elementary row operations to the augmented matrix to reduce it to row echelon form. The augmented matrix is

$$
\left[\begin{array}{rrr|r}
1 & 3 & -7 & -8\\
2 & 5 & 4 & 4\\
-3 & -7 & -2 & -3\\
1 & 4 & -12 & -15
\end{array}\right].
$$

By the (1)-th operation of **Definition 1** (Elementary Operations on Systems of Linear Equations), perform the row operations in turn: (2) $-2\times$(1), (3) $+3\times$(1), (4) $-$(1), giving

$$
\left[\begin{array}{rrr|r}
1 & 3 & -7 & -8\\
0 & -1 & 18 & 20\\
0 & 2 & -23 & -27\\
0 & 1 & -5 & -7
\end{array}\right].
$$

By **Definition 1**, elementary operations do not change the solutions of the system, so we can back-substitute from the echelon system. From (4) we get $x_{2}=5x_{3}-7$. Substituting into (2): $-\left(5x_{3}-7\right)+18x_{3}=20$, solving gives $x_{3}=1$. Hence $x_{2}=-2$. Substituting into (1):

$$
x_{1}+3\times\left(-2\right)-7\times1=-8,
$$

solving gives $x_{1}=5$.

Substituting into (3) to verify:

$$
-3\times5-7\times\left(-2\right)-2\times1=-15+14-2=-3,
$$

which holds.

By **Basic Knowledge 1**, the original system therefore has the unique solution

$$
\left(x_{1},x_{2},x_{3}\right)=\left(5,-2,1\right).\blacksquare
$$

### Problem 2

(Problem 1.1-2) An investor wants to invest $1$ ten-thousand yuan in $3$ enterprises $A_{1},A_{2},A_{3}$, with profit rates of $12\%,15\%,22\%$, respectively. He wants to obtain a profit of $2000$ yuan.

(1) If the amount invested in $A_{1}$ is $2$ times that invested in $A_{2}$, how much should be invested in $A_{1},A_{2},A_{3}$, respectively?

(2) Is it possible to make the amount invested in $A_{3}$ equal to the sum of the amounts invested in $A_{1}$ and $A_{2}$?

### Solution to Problem 2

Let the amounts invested in $A_{1},A_{2},A_{3}$ be $x_{1},x_{2},x_{3}$, respectively (unit: yuan). Based on the total investment and the total profit, set up the system

$$
\begin{cases}
x_{1}+x_{2}+x_{3}=10000,\\
0.12x_{1}+0.15x_{2}+0.22x_{3}=2000.
\end{cases}
$$

(1) From the condition $x_{1}=2x_{2}$, substituting into the system gives

$$
\begin{cases}
3x_{2}+x_{3}=10000,\\
0.39x_{2}+0.22x_{3}=2000.
\end{cases}
$$

From the first equation $x_{3}=10000-3x_{2}$, substituting into the second equation:

$$
\begin{aligned}0.39x_{2}+0.22\left(10000-3x_{2}\right)&=2000\\
0.39x_{2}+2200-0.66x_{2}&=2000\\
-0.27x_{2}&=-200\\
x_{2}&=\frac{20000}{27}.
\end{aligned}
$$

Hence

$$
x_{1}=2x_{2}=\frac{40000}{27}, x_{3}=10000-3x_{2}=\frac{70000}{9}.
$$

i.e. one should invest $\frac{40000}{27}$ yuan, $\frac{20000}{27}$ yuan, and $\frac{70000}{9}$ yuan, respectively (approximately $1481.48$ yuan, $740.74$ yuan, and $7777.78$ yuan).

(2) From the condition $x_{3}=x_{1}+x_{2}$, substituting into the total-investment equation:

$$
\begin{aligned}x_{1}+x_{2}+\left(x_{1}+x_{2}\right)&=10000\\
2\left(x_{1}+x_{2}\right)&=10000\\
x_{1}+x_{2}&=5000.
\end{aligned}
$$

Hence $x_{3}=5000$. Substituting into the total-profit equation:

$$
\begin{aligned}0.12x_{1}+0.15x_{2}+0.22\times5000&=2000\\
0.12x_{1}+0.15x_{2}+1100&=2000\\
0.12x_{1}+0.15x_{2}&=900.
\end{aligned}
$$

Also $x_{2}=5000-x_{1}$; substituting gives

$$
\begin{aligned}0.12x_{1}+0.15\left(5000-x_{1}\right)&=900\\
0.12x_{1}+750-0.15x_{1}&=900\\
-0.03x_{1}&=150\\
x_{1}&=-5000.
\end{aligned}
$$

Then $x_{2}=10000$. Since an investment cannot be negative, $x_{1}=-5000< 0$ has no practical meaning. Hence it is not possible to make the amount invested in $A_{3}$ equal to the sum of the amounts invested in $A_{1}$ and $A_{2}$. $\blacksquare$

### Problem 3

(Problem 1.1-3(2)) Solve the following system of linear equations:

$$
\begin{cases}
2x_{1}-3x_{2}+x_{3}+5x_{4}=6,\\
-3x_{1}+x_{2}+2x_{3}-4x_{4}=5,\\
-x_{1}-2x_{2}+3x_{3}+x_{4}=11.
\end{cases}
$$

### Solution to Problem 3

By **Basic Knowledge 1** (Gauss–Jordan Algorithm), apply elementary row operations to the augmented matrix. The augmented matrix is

$$
\left[\begin{array}{rrrr|r}
2 & -3 & 1 & 5 & 6\\
-3 & 1 & 2 & -4 & 5\\
-1 & -2 & 3 & 1 & 11
\end{array}\right].
$$

By the (2)-th operation of **Definition 1** (Elementary Operations on Systems of Linear Equations), interchange rows $1,3$, giving

$$
\left[\begin{array}{rrrr|r}
-1 & -2 & 3 & 1 & 11\\
-3 & 1 & 2 & -4 & 5\\
2 & -3 & 1 & 5 & 6
\end{array}\right].
$$

By the (1)-th operation of **Definition 1**, perform (2) $-3\times$(1), (3) $+2\times$(1):

$$
\left[\begin{array}{rrrr|r}
-1 & -2 & 3 & 1 & 11\\
0 & -5 & -7 & -7 & -28\\
0 & -7 & 7 & 7 & 28
\end{array}\right].
$$

By **Definition 1**, elementary operations do not change the solutions of the system, so we back-substitute from the echelon system. From the $3$rd row we get $-7x_{2}+7x_{3}+7x_{4}=28$, i.e. $-x_{2}+x_{3}+x_{4}=4$, hence $x_{2}=x_{3}+x_{4}-4$.

Substituting into the $2$nd row:

$$
\begin{aligned}-5\left(x_{3}+x_{4}-4\right)-7x_{3}-7x_{4}&=-28\\
-5x_{3}-5x_{4}+20-7x_{3}-7x_{4}&=-28\\
-12x_{3}-12x_{4}&=-48\\
x_{3}+x_{4}&=4.
\end{aligned}
$$

Let $x_{4}=c$ (a free unknown); then $x_{3}=4-c$. Hence

$$
x_{2}=\left(4-c\right)+c-4=0.
$$

Substituting into the $1$st row:

$$
\begin{aligned}-x_{1}-2\times0+3\left(4-c\right)+c&=11\\
-x_{1}+12-3c+c&=11\\
-x_{1}&=-1+2c\\
x_{1}&=1-2c.
\end{aligned}
$$

By **Basic Knowledge 1**, the original system therefore has infinitely many solutions, and the general solution is

$$
\begin{cases}
x_{1}=1-2c,\\
x_{2}=0,\\
x_{3}=4-c,\\
x_{4}=c,
\end{cases}
$$

where $c$ is an arbitrary constant. $\blacksquare$

### Problem 4

(Problem 1.1-3(3)) Solve the following system of linear equations:

$$
\begin{cases}
x_{1}-5x_{2}-2x_{3}=4,\\
2x_{1}-3x_{2}+x_{3}=7,\\
-x_{1}+12x_{2}+7x_{3}=-5,\\
x_{1}+16x_{2}+13x_{3}=-1.
\end{cases}
$$

### Solution to Problem 4

By **Basic Knowledge 1** (Gauss–Jordan Algorithm), apply elementary row operations to the augmented matrix. The augmented matrix is

$$
\left[\begin{array}{rrr|r}
1 & -5 & -2 & 4\\
2 & -3 & 1 & 7\\
-1 & 12 & 7 & -5\\
1 & 16 & 13 & -1
\end{array}\right].
$$

By the (1)-th operation of **Definition 1** (Elementary Operations on Systems of Linear Equations), perform (2) $-2\times$(1), (3) $+$(1), (4) $-$(1):

$$
\left[\begin{array}{rrr|r}
1 & -5 & -2 & 4\\
0 & 7 & 5 & -1\\
0 & 7 & 5 & -1\\
0 & 21 & 15 & -5
\end{array}\right].
$$

By **Definition 1**, elementary operations do not change the solutions of the system, so we can determine whether there is a solution from the echelon system. From the $2$nd row we get $7x_{2}+5x_{3}=-1$. The $4$th row is $21x_{2}+15x_{3}=-5$.

Note that the left-hand side of the $4$th row is exactly $3$ times the left-hand side of the $2$nd row, whereas the right-hand side $3\times\left(-1\right)=-3\ne-5$. That is,

$$
3\times\left(7x_{2}+5x_{3}\right)=3\times\left(-1\right)\Rightarrow21x_{2}+15x_{3}=-3,
$$

which contradicts the $4$th row $21x_{2}+15x_{3}=-5$, yielding $0=-2$.

By **Basic Knowledge 1**, the corresponding echelon system exhibits the case $0=d$($d\ne 0$), so the original system has no solution. $\blacksquare$
