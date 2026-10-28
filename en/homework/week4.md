# week4

> **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**<br>In an $n$-permutation, if a pair of numbers has its order reversed relative to its size (i.e. the number in front is larger than the one behind), then the pair is called an inversion. The total number of inversions in a permutation is called its inversion number, denoted $\tau$. A permutation with odd inversion number is called an odd permutation, and one with even inversion number is called an even permutation.

> **Proposition 2.1.1 (Criterion for a Unique Solution of a Two-Variable Linear System)**<br>A two-equation linear system in two variables has a unique solution if and only if its coefficient determinant is nonzero; in that case the unique solution is given by the Cramer formula, i.e. two fractions whose numerators are the $2\times2$ determinants obtained by replacing the $1$st and $2$nd columns of the coefficient determinant by the constant terms of the system.

---

## 2.1-1(1)

Find the inversion number of the permutation $315462$ and determine its parity.

### Solution 2.1-1(1)

By **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**, count the inversions digit by digit:

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

By **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**, $\tau=6$ is even, so $315462$ is an even permutation. $\blacksquare$

---

## 2.1-1(4)

Find the inversion number of the permutation $7654321$ and determine its parity.

### Solution 2.1-1(4)

By **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**, this is the fully reversed $7$-permutation, whose inversion number is

$$
\tau\left(7654321\right)=6+5+4+3+2+1+0=21.
$$

By **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**, $\tau=21$ is odd, so $7654321$ is an odd permutation. $\blacksquare$

---

## 2.1-1(7)

Find the inversion number of the permutation $123456789$ and determine its parity.

### Solution 2.1-1(7)

By **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**, this is the natural-order permutation, which has no inversions, so

$$
\tau\left(123456789\right)=0.
$$

By **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**, $\tau=0$ is even, so $123456789$ is an even permutation. $\blacksquare$

---

## 2.1-2

Find the inversion number of the following $n$-permutations:

(1) $\left(n-1\right)\left(n-2\right)\cdots 21n$;

(2) $23\cdots\left(n-1\right)n1$.

### Solution 2.1-2

By **Basic Knowledge: Inversions, the Number of Inversions, and Even/Odd Permutations**:

(1) In the permutation $\left(n-1\right)\left(n-2\right)\cdots 21n$, the first $n-1$ numbers are in fully reversed order, and the last number $n$ is the largest, producing no inversion. The inversion number of the first $n-1$ numbers is

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

---

## 2.1-8

Using $2\times2$ determinants, determine whether the following two-variable linear system has a unique solution, and when it does, find that solution:

$$
\begin{cases}
2x_{1}-3x_{2}=7,\\
5x_{1}+4x_{2}=6.
\end{cases}
$$

### Solution 2.1-8

The coefficient determinant is

$$
\left|\begin{array}{rr}
2 & -3\\
5 & 4
\end{array}\right|=2\times4-\left(-3\right)\times5=8+15=23\ne 0.
$$

By **Proposition 2.1.1 (Criterion for a Unique Solution of a Two-Variable Linear System)**, the system has a unique solution.

By the Cramer formula given in that proposition:

$$
x_{1}=\frac{\left|\begin{array}{rr}7 & -3\\6 & 4\end{array}\right|}{23}=\frac{7\times4-\left(-3\right)\times6}{23}=\frac{28+18}{23}=\frac{46}{23}=2,
$$

$$
x_{2}=\frac{\left|\begin{array}{rr}2 & 7\\5 & 6\end{array}\right|}{23}=\frac{2\times6-7\times5}{23}=\frac{12-35}{23}=\frac{-23}{23}=-1.
$$

Hence the unique solution is $\left(x_{1},x_{2}\right)=\left(2,-1\right)$. $\blacksquare$
