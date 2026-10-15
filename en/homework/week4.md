# Assignment 4

> **Definition 1** (Number of Inversions of a Permutation of $n$ Elements)<br>In a permutation of $n$ elements, if a pair of numbers appears in reverse order with respect to their size (i.e. the number in front is greater than the number behind), then the pair is called an inversion. The total number of inversions in a permutation is called its number of inversions, denoted by $\tau$.

> **Proposition 1** (Criterion for a Two-Variable Linear System to Have a Unique Solution)<br>A two-variable system of two linear equations has a unique solution if and only if its coefficient determinant is not equal to $0$.

### Problem 1

(Problem 2.1-1(1)) Find the number of inversions of the permutation $315462$, and state whether it is even or odd.

### Solution to Problem 1

By **Definition 1** (Number of Inversions of a Permutation of $n$ Elements), count the inversions position by position:

- after $3$, the numbers smaller than $3$ are $1,2$, contributing $2$ inversions;
- after $1$, there is no number smaller than $1$, contributing $0$;
- after $5$, the numbers smaller than $5$ are $4,2$, contributing $2$;
- after $4$, the numbers smaller than $4$ are $2$, contributing $1$;
- after $6$, the numbers smaller than $6$ are $2$, contributing $1$;
- after $2$, there is no number smaller than $2$, contributing $0$.

Hence

$$
\tau\left(315462\right)=2+0+2+1+1+0=6.
$$

By **Definition 1**, $\tau=6$ is even, so $315462$ is an even permutation. $\blacksquare$

### Problem 2

(Problem 2.1-1(4)) Find the number of inversions of the permutation $7654321$, and state whether it is even or odd.

### Solution to Problem 2

By **Definition 1** (Number of Inversions of a Permutation of $n$ Elements), this is the completely reversed permutation of $7$ elements, and its number of inversions is

$$
\tau\left(7654321\right)=6+5+4+3+2+1+0=21.
$$

By **Definition 1**, $\tau=21$ is odd, so $7654321$ is an odd permutation. $\blacksquare$

### Problem 3

(Problem 2.1-1(7)) Find the number of inversions of the permutation $123456789$, and state whether it is even or odd.

### Solution to Problem 3

By **Definition 1** (Number of Inversions of a Permutation of $n$ Elements), this is the permutation in natural order, with no inversions, hence

$$
\tau\left(123456789\right)=0.
$$

By **Definition 1**, $\tau=0$ is even, so $123456789$ is an even permutation. $\blacksquare$

### Problem 4

(Problem 2.1-2) Find the number of inversions of the following permutations of $n$ elements:

(1) $\left(n-1\right)\left(n-2\right)\cdots 21n$;

(2) $23\cdots\left(n-1\right)n1$.

### Solution to Problem 4

By **Definition 1** (Number of Inversions of a Permutation of $n$ Elements):

(1) In the permutation $\left(n-1\right)\left(n-2\right)\cdots 21n$, the first $n-1$ numbers are in completely reversed order, and the last number $n$ is the largest, producing no inversions. The number of inversions of the first $n-1$ numbers is

$$
\left(n-2\right)+\left(n-3\right)+\cdots+1+0=\frac{\left(n-2\right)\left(n-1\right)}{2}.
$$

Hence

$$
\tau=\frac{\left(n-1\right)\left(n-2\right)}{2}
$$

(2) In the permutation $23\cdots\left(n-1\right)n1$, the number $1$ is placed last; the preceding $n-1$ numbers $2,3,\cdots,n$ are all greater than $1$, and each forms an inversion with $1$. The remaining numbers are all in natural order, producing no inversions. Hence

$$
\tau=n-1.
$$

$\blacksquare$

### Problem 5

(Problem 2.1-8) Using a $2$-nd order determinant, determine whether the following two-variable system of linear equations has a unique solution, and when it has a unique solution, find that solution:

$$
\begin{cases}
2x_{1}-3x_{2}=7,\\
5x_{1}+4x_{2}=6.
\end{cases}
$$

### Solution to Problem 5

The coefficient determinant is

$$
\left|\begin{array}{rr}
2 & -3\\
5 & 4
\end{array}\right|=2\times4-\left(-3\right)\times5=8+15=23\ne 0.
$$

By **Proposition 1** (Criterion for a Two-Variable Linear System to Have a Unique Solution), the system has a unique solution.

By Cramer's rule:

$$
x_{1}=\frac{\left|\begin{array}{rr}7 & -3\\6 & 4\end{array}\right|}{23}=\frac{7\times4-\left(-3\right)\times6}{23}=\frac{28+18}{23}=\frac{46}{23}=2,
$$

$$
x_{2}=\frac{\left|\begin{array}{rr}2 & 7\\5 & 6\end{array}\right|}{23}=\frac{2\times6-7\times5}{23}=\frac{12-35}{23}=\frac{-23}{23}=-1.
$$

Hence the unique solution is $\left(x_{1},x_{2}\right)=\left(2,-1\right)$. $\blacksquare$
