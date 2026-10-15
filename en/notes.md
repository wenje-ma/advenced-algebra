# Advanced Algebra

## Systems of Linear Equations

**Definition 1** (Elementary Operations on Systems of Linear Equations)

The following three operations are performed on a system of linear equations:

(1) add a multiple of one equation to another;

(2) interchange the positions of two equations;

(3) multiply an equation by a nonzero scalar. These three operations are collectively called the elementary operations on systems of linear equations. A system obtained by elementary operations has the same solution set as the original system.

**Definition 2** (Row Echelon Matrix)

In a matrix, rows whose elements are all $0$ (zero rows) lie below; in a row whose elements are not all $0$ (nonzero row), the first element not equal to $0$ counted from the left is called the pivot, and the column index of the pivot of each nonzero row strictly increases as the row index increases.

**Definition 3** (Reduced Row Echelon Matrix)

On the basis of a row echelon matrix, the pivot of each nonzero row is $1$, and all other elements in the column containing each pivot are $0$.

**Basic Knowledge 1** (Gauss–Jordan Algorithm)

By applying elementary row operations to the augmented matrix of a system of linear equations and reducing it to a reduced row echelon matrix, one can write down the solution directly. If the corresponding echelon system exhibits $0=d$($d\ne 0$), then the original system has no solution.

**Theorem 1** (Criterion for the Solutions of a System of Linear Equations)

By applying elementary row operations to the augmented matrix of an $n$-variable system of linear equations and reducing it to a row echelon matrix:

(1) if the corresponding echelon system exhibits $0=d$($d\ne 0$), then the original system has no solution;

(2) if $0=d$ does not occur, then there is a solution, and when the number of nonzero rows equals the number of unknowns there is a unique solution, while when the number of nonzero rows is less than the number of unknowns there are infinitely many solutions.

**Definition 4** (Number Field)

Let $K$ be a subset of the set of complex numbers. If $K$ satisfies:

(1) $0,1\in K$;

(2) it is closed under the four operations of addition, subtraction, multiplication, and division (the divisor being not $0$),
then $K$ is called a number field.

## Determinants

**Definition 5** (Number of Inversions of a Permutation of $n$ Elements)

In a permutation of $n$ elements, if a pair of numbers appears in reverse order with respect to their size (i.e. the number in front is greater than the number behind), then the pair is called an inversion. The total number of inversions in a permutation is called its number of inversions, denoted by $\tau\left(j_{1}j_{2}\cdots j_{n}\right)$.

**Proposition 1** (Criterion for a Two-Variable Linear System to Have a Unique Solution)

A two-variable system of two linear equations has a unique solution if and only if its coefficient determinant is not equal to $0$.

**Definition 6** ($n$-th Order Determinant)

An $n$-th order determinant is the algebraic sum of $n!$ terms, each being the product of $n$ elements lying in distinct rows and distinct columns. When these $n$ elements are placed in natural order according to their row indices, the term carries a positive sign if the permutation formed by the column indices is even, and a negative sign if it is odd.

**Basic Knowledge 2** (Properties of Determinants)

(1) interchanging the rows and columns of a determinant (transposition) leaves its value unchanged;

(2) a common factor of a row (column) of a determinant can be pulled outside the determinant sign;

(3) if all elements of a row (column) of a determinant are sums of two terms, then the determinant can be split into the sum of two determinants;

(4) interchanging two rows (columns) changes the sign of the determinant;

(5) if two rows (columns) are proportional, the determinant is zero;

(6) adding a multiple of one row (column) to another row (column) leaves the value of the determinant unchanged.

**Definition 7** (Minor and Cofactor)

In the $n$-th order determinant $\left|A\right|$, delete the $i$-th row and the $j$-th column; the $n-1$-th order determinant formed by the remaining elements in their original order is called the $\left(i,j\right)$ minor of $A$, denoted by $M_{ij}$. Set $A_{ij}=\left(-1\right)^{i+j}M_{ij}$; then $A_{ij}$ is called the $\left(i,j\right)$ cofactor of $A$.

**Theorem 2** (Expansion along a Row)

The $n$-th order determinant $\left|A\right|$ equals the sum of the products of the elements of its $i$-th row with their own cofactors:

$$
\left|A\right|=a_{i1}A_{i1}+a_{i2}A_{i2}+\cdots+a_{in}A_{in}.
$$

Similarly, expansion along a column:

$$
\left|A\right|=a_{1j}A_{1j}+a_{2j}A_{2j}+\cdots+a_{nj}A_{nj}.
$$

**Theorem 3** (Cramer's Rule)

For an $n$-variable system of $n$ linear equations, if its coefficient determinant $\left|A\right|\ne0$, then it has a unique solution; if its coefficient determinant $\left|A\right|=0$, then it has no solution or infinitely many solutions.

**Corollary 1** (Condition for a Homogeneous System to Have a Nontrivial Solution)

An $n$-variable homogeneous system of $n$ linear equations has only the zero solution if and only if its coefficient determinant is not equal to $0$. Hence, an $n$-variable homogeneous system of $n$ linear equations has a nontrivial solution if and only if its coefficient determinant is equal to $0$.

**Theorem 4** (Laplace's Theorem)

In the $n$-th order determinant $\left|A\right|$, fix $k$ rows; then the sum of the products of all $k$-th order minors formed by the elements of these $k$ rows with their own cofactors equals $\left|A\right|$.

**Basic Knowledge 3** (Block Determinants)

where $A,B$ are both square matrices:

$$
\left|\begin{array}{cc}A & 0\\C & B\end{array}\right|=\left|A\right|\left|B\right|.
$$

## Vector Spaces and Systems of Linear Equations

**Definition 8** (Linear Combination and Linear Spanning)

In $K^{n}$, given a vector system $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$, for any scalars $k_{1},k_{2},\cdots,k_{s}$ in $K$, the expression $k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s}$ is called a linear combination of the vector system $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$. If

$$
\beta=k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s},
$$

then $\beta$ is said to be linearly spanned by $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$.

**Proposition 2** (Relationship between Linear Spanning and the Existence of a Solution)

An $n$-variable system of linear equations over the number field $K$

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

has a solution $\Leftrightarrow$ $\beta$ can be linearly spanned by $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ $\Leftrightarrow$ $\beta\in\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\right\rangle$.

**Definition 9** (Linearly Dependent)

A vector system $\alpha_{1},\cdots,\alpha_{s}$ in $K^{n}$ is called linearly dependent if there exist scalars $k_{1},\cdots,k_{s}$ in $K$, not all zero, such that $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$.

**Definition 10** (Linearly Independent)

A vector system $\alpha_{1},\cdots,\alpha_{s}$ in $K^{n}$ is called linearly independent if it is not linearly dependent. That is, if from $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$ one can deduce that all $k_{1}=\cdots=k_{s}=0$, then the vector system is called linearly independent.

**Proposition 3** (Relationship between Linear Spanning and Linear Dependence)

Let the vector system $\alpha_{1},\cdots,\alpha_{s}$ be linearly independent. Then the vector $\beta$ can be linearly spanned by $\alpha_{1},\cdots,\alpha_{s}$ if and only if $\alpha_{1},\cdots,\alpha_{s},\beta$ is linearly dependent.

**Definition 11** (Maximal Linearly Independent Subsystem)

A subsystem of a vector system in $K^{n}$ is called a maximal linearly independent subsystem if the subsystem itself is linearly independent, but whenever any one of the remaining vectors of the vector system is adjoined, the resulting new subsystem is linearly dependent.

**Definition 12** (Rank of a Vector System)

The number of vectors contained in a maximal linearly independent subsystem of a vector system is called the rank of the vector system. It is denoted by

$$
\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}.
$$

**Proposition 4** (Comparison of Ranks)

If vector system (I) can be linearly spanned by vector system (II), then the rank of (I) is $\le$ the rank of (II).

**Definition 13** (Basis)

Let $U$ be a subspace of $K^{n}$. If a vector system $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ in $U$ satisfies: $1^{\circ}$ $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ is linearly independent; $2^{\circ}$ every vector in $U$ can be linearly spanned by $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$, then $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ is called a basis of $U$.

**Definition 14** (Rank of a Matrix)

The row rank and column rank of a matrix $A$ are collectively called the rank of $A$, denoted by $\text{rank}\left(A\right)$.

**Theorem 5** (Row Rank Equals Column Rank)

The row rank of any matrix equals its column rank.

**Corollary 2** (Finding the Rank by Elementary Row Operations)

Let a matrix $A$ be reduced by elementary row operations to a row echelon matrix $J$; then the rank of $A$ equals the number of nonzero rows of $J$. Let the columns containing the pivots of $J$ be the $j_{1},\cdots,j_{r}$-th columns; then the $j_{1},\cdots,j_{r}$-th columns of $A$ form a maximal linearly independent subsystem of the column vector system of $A$.

**Theorem 6** (Criterion for the Existence of a Solution of a System of Linear Equations)

The system of linear equations

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

has a solution if and only if its coefficient matrix and its augmented matrix have the same rank.

**Theorem 7** (Determining the Number of Solutions)

Suppose a system of linear equations has a solution. If the rank of the coefficient matrix equals the number $n$ of unknowns, then the system has a unique solution; if the rank of the coefficient matrix is less than $n$, then the system has infinitely many solutions.

**Definition 15** (Fundamental System of Solutions)

When a homogeneous system of linear equations has nontrivial solutions, if finitely many of its solutions $\eta_{1},\eta_{2},\cdots,\eta_{t}$ satisfy: $1^{\circ}$ they are linearly independent; $2^{\circ}$ every solution of the system can be linearly spanned by $\eta_{1},\eta_{2},\cdots,\eta_{t}$, then $\eta_{1},\eta_{2},\cdots,\eta_{t}$ is called a fundamental system of solutions of the homogeneous system.

**Theorem 8** (Dimension of the Solution Space)

The dimension of the solution space $W$ of an $n$-variable homogeneous system of linear equations over the number field $K$ is:

$$
\dim W=n-\text{rank}\left(A\right),
$$

where $A$ is the coefficient matrix.

**Theorem 9** (Structure of the Solution Set of an Inhomogeneous System)

If an $n$-variable inhomogeneous system of linear equations over the number field $K$ has a solution, then its solution set is $U=\gamma_{0}+W$, where $\gamma_{0}$ is a particular solution and $W$ is the solution space of the derived homogeneous system.

## Matrix Operations

**Definition 16** (Addition of Matrices)

Let $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ both be $s\times n$ matrices over the number field $K$, and set $C=\left(a_{ij}+b_{ij}\right)_{s\times n}$; then $C$ is called the sum of $A$ and $B$, denoted by $C=A+B$.

**Definition 17** (Scalar Multiplication of Matrices)

Let $k\in K$ and set $M=\left(ka_{ij}\right)_{s\times n}$; then $M$ is called the scalar product of $k$ and the matrix $A$, denoted by $M=kA$.

**Definition 18** (Multiplication of Matrices)

Let $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$, and set $C=\left(c_{ij}\right)_{s\times m}$, where

$$
c_{ij}=a_{i1}b_{1j}+a_{i2}b_{2j}+\cdots+a_{in}b_{nj},
$$

then $C$ is called the product of $A$ and $B$, denoted by $C=AB$.

**Definition 19** (Upper/Lower Triangular Matrix)

A square matrix whose elements below (above) the main diagonal are all zero is called an upper (lower) triangular matrix.

**Theorem 10** (Rank of a Product of Matrices)

Let $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$. Then:

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

**Theorem 11** (Determinant of a Product)

Let $A,B$ both be $n$-th order matrices. Then $\left|AB\right|=\left|A\right|\left|B\right|$.


**Definition 20** (Invertible Matrix)

For a matrix $A$ over the number field $K$, if there exists a matrix $B$ over $K$ such that $AB=BA=I$, then $A$ is called an invertible matrix (or a nonsingular matrix).

**Definition 21** (Inverse Matrix)

If $A$ is an invertible matrix, then the matrix $B$ satisfying $AB=BA=I$ is called the inverse matrix of $A$, denoted by $A^{-1}$.

**Theorem 12** (Necessary and Sufficient Condition for Invertibility)

An $n$-th order matrix $A$ over the number field $K$ is invertible if and only if $\left|A\right|\ne0$. When $A$ is invertible:

$$
A^{-1}=\frac{1}{\left|A\right|}A^{*}.
$$

**Proposition 5** (Rank Identity over the Real Field)

Let $A$ be an $s\times n$ matrix over the real field. Then:

$$
\text{rank}\left(A^{T}A\right)=\text{rank}\left(AA^{T}\right)=\text{rank}\left(A\right).
$$

**Definition 22** (Orthogonal Matrix)

A square matrix $A$ over the real field, if it satisfies $A^{T}A=I$, then $A$ is called an orthogonal matrix.

**Definition 23** (Inner Product)

In $\mathbb{R}^{n}$, for any $\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)$ and $\beta=\left(b_{1},b_{2},\cdots,b_{n}\right)$, define

$$
\left(\alpha,\beta\right)=a_{1}b_{1}+a_{2}b_{2}+\cdots+a_{n}b_{n},
$$

which is called the standard inner product of $\mathbb{R}^{n}$.

**Proposition 6** (An Orthogonal Vector System Is Linearly Independent)

In the Euclidean space $\mathbb{R}^{n}$, an orthogonal vector system is always linearly independent.

**Definition 24** (Mapping)

Let $S$ and $S'$ be two sets. If there exists a rule $f$ such that to every element $a$ in the set $S$ there corresponds a uniquely determined element $b$ in the set $S'$, then $f$ is called a mapping from $S$ to $S'$.

**Definition 25** (Linear Mapping)

A mapping $\mathcal{A}$ from $K^{n}$ to $K^{s}$ is called a linear mapping if it preserves addition and scalar multiplication, i.e. for $\forall\alpha,\beta\in K^{n},k\in K$, we have

$$
\mathcal{A}\left(\alpha+\beta\right)=\mathcal{A}\left(\alpha\right)+\mathcal{A}\left(\beta\right),
$$

$\mathcal{A}\left(k\alpha\right)=k\mathcal{A}\left(\alpha\right)$; then $\mathcal{A}$ is called a linear mapping from $K^{n}$ to $K^{s}$.

**Theorem** (Dimension Formula for the Kernel and Image)

$$
\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=\dim\left(K^{n}\right).
$$

## Canonical Forms under Similarity

**Definition 26** (Binary Relation)

Let $S$ be a nonempty set. A subset $W$ of $S\times S$ is called a binary relation on $S$. If $\left(a,b\right)\in W$, then $a$ and $b$ are said to stand in the relation $W$.

**Definition 27** (Equivalence Relation)

A binary relation $\sim$ on a set $S$, if it has the following properties: for $\forall a,b,c\in S$, we have $1^{\circ}a\sim a$ (reflexivity); $2^{\circ}a\sim b\Rightarrow b\sim a$ (symmetry); $3^{\circ}a\sim b$ and $b\sim c\Rightarrow a\sim c$ (transitivity), then $\sim$ is called an equivalence relation on $S$.

**Definition 28** (Quotient Set)

Let $\sim$ be an equivalence relation on a set $S$. The set consisting of all equivalence classes is called the quotient set of $S$ with respect to the relation $\sim$, denoted by $S/\sim$.

**Definition 29** (Equivalence of Matrices)

If a matrix $A$ over the number field $K$ is transformed into a matrix $B$ through a sequence of elementary row operations and elementary column operations, then $A$ and $B$ are said to be equivalent, denoted by $A\overset{\text{相抵}}{\sim}B$.

**Theorem 13** (Canonical Form under Equivalence)

Let the rank of an $s\times n$ matrix $A$ over the number field $K$ be $r$. If $r>0$, then $A$ is equivalent to a matrix of the following form:

$$
\left[\begin{array}{cc}I_{r} & 0\\0 & 0\end{array}\right].
$$

**Theorem 14** (Necessary and Sufficient Condition for Equivalence)

Two $s\times n$ matrices $A$ and $B$ over the number field $K$ are equivalent if and only if they have the same rank.

**Definition 30** (Generalized Inverse)

Let $A$ be an $s\times n$ matrix over the number field $K$. If a matrix $G$ satisfies $AGA=A$, then $G$ is called a generalized inverse of $A$, denoted by $A^{-}$.

**Theorem 15** (Existence of a Generalized Inverse)

Let $A$ be a nonzero $s\times n$ matrix over the number field $K$. Then the matrix equation $AXA=A$ always has a solution.

**Definition 31** (Similarity)

Let $A$ and $B$ both be $n$-th order matrices over the number field $K$. If there exists an $n$-th order invertible matrix $P$ over $K$ such that $P^{-1}AP=B$, then $A$ and $B$ are said to be similar, denoted by $A\sim B$.

**Property** (Invariants under Similarity)

Similar matrices have equal determinants, equal ranks, and equal traces.

**Theorem 16** (Necessary and Sufficient Condition for Diagonalizability)

An $n$-th order matrix $A$ over the number field $K$ can be similar to a diagonal matrix if and only if there exist $n$ linearly independent column vectors $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ in $K^{n}$ and $n$ scalars $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ in $K$ such that $A\alpha_{i}=\lambda_{i}\alpha_{i}$($i=1,2,\cdots,n$).

**Definition 32** (Eigenvalue and Eigenvector)

Let $A$ be an $n$-th order matrix over the number field $K$. If there is a nonzero column vector $\alpha$ in $K^{n}$ such that $A\alpha=\lambda_{0}\alpha$ with $\lambda_{0}\in K$, then $\lambda_{0}$ is called an eigenvalue of $A$, and $\alpha$ is called an eigenvector of $A$ belonging to the eigenvalue $\lambda_{0}$.

**Property** (Similarity Invariants)

Similar matrices have the same determinant, the same rank, the same trace, the same characteristic polynomial, and the same eigenvalues.

**Theorem 17** (Necessary and Sufficient Condition for Diagonalizability)

An $n$-th order matrix $A$ over the number field $K$ is diagonalizable if and only if $A$ has $n$ linearly independent eigenvectors.

**Corollary 3** (Having $n$ Distinct Eigenvalues Implies Diagonalizability)

If an $n$-th order matrix $A$ over the number field $K$ has $n$ distinct eigenvalues, then $A$ is diagonalizable.

**Theorem 18** (Eigenvalues of a Real Symmetric Matrix)

Every root in the complex field of the characteristic polynomial of a real symmetric matrix is a real number.

**Theorem 19** (A Real Symmetric Matrix Is Orthogonally Diagonalizable)

For any $n$-th order real symmetric matrix $A$, there always exists an $n$-th order orthogonal matrix $T$ such that $T^{-1}AT$ is a diagonal matrix.

## Quadratic Forms

**Definition 33** (Quadratic Form)

A homogeneous quadratic polynomial in $n$ variables $x_{1},x_{2},\cdots,x_{n}$ with coefficients in a number field $K$ is called an $n$-variable quadratic form over $K$.

**Theorem 20** (Canonical Form of a Quadratic Form)

Any quadratic form over a number field $K$ is equivalent to a quadratic form containing only square terms.

**Definition 34** (Normal Form)

The normal form of the real quadratic form $X^{T}AX$ is

$$
z_{1}^{2}+\cdots+z_{p}^{2}-z_{p+1}^{2}-\cdots-z_{r}^{2},
$$

where $p$ is the positive index of inertia and $r$ is the rank of the quadratic form.

**Theorem 21** (Inertia Theorem)

The normal form of an $n$-variable real quadratic form $X^{T}AX$ is unique.

**Definition 35** (Positive Index of Inertia)

In the normal form of the real quadratic form $X^{T}AX$, the number $p$ of square terms with coefficient $+1$ is called the positive index of inertia of $X^{T}AX$, and the number $r-p$ of square terms with coefficient $-1$ is called the negative index of inertia of $X^{T}AX$.

**Corollary 4** (Necessary and Sufficient Condition for Congruence)

Two $n$-th order real symmetric matrices are congruent if and only if they have the same rank and the same positive index of inertia.

## Polynomials in One Variable

**Definition 36** (Divisibility)

Let $f\left(x\right),g\left(x\right)\in K\left[x\right]$. If there exists $h\left(x\right)\in K\left[x\right]$ such that $f\left(x\right)=h\left(x\right)g\left(x\right)$, then $g\left(x\right)$ is said to divide $f\left(x\right)$, denoted by $g\left(x\right)\mid f\left(x\right)$.

**Theorem 22** (Division Algorithm)

In $K\left[x\right]$, for any two polynomials $f\left(x\right),g\left(x\right)$ with $g\left(x\right)\ne0$, there exists a unique pair of polynomials $h\left(x\right),r\left(x\right)$ such that $f\left(x\right)=h\left(x\right)g\left(x\right)+r\left(x\right)$ and $\deg r\left(x\right)<\deg g\left(x\right)$.

**Definition 37** (Greatest Common Divisor)

Let $f\left(x\right),g\left(x\right)\in K\left[x\right]$, and let $d\left(x\right)$ be a common divisor of $f\left(x\right)$ and $g\left(x\right)$. If every common divisor of $f\left(x\right)$ and $g\left(x\right)$ divides $d\left(x\right)$, then $d\left(x\right)$ is called a greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$.

**Theorem 23** (Existence of the Greatest Common Divisor and the Bézout Representation)

For any two polynomials $f\left(x\right)$ and $g\left(x\right)$ in $K\left[x\right]$, there exists a greatest common divisor $d\left(x\right)$ of them, and $d\left(x\right)$ can be expressed as a linear combination of $f\left(x\right)$ and $g\left(x\right)$, i.e. there exist $u\left(x\right),v\left(x\right)\in K\left[x\right]$ such that

$$
d\left(x\right)=u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right).
$$

**Definition 38** (Coprime)

In $K\left[x\right]$, if the greatest common divisor of $f\left(x\right)$ and $g\left(x\right)$ is a constant polynomial, then $f\left(x\right)$ and $g\left(x\right)$ are said to be coprime.

**Definition 39** (Irreducible Polynomial)

A polynomial $p\left(x\right)$ in $K\left[x\right]$ of degree greater than zero: if its only divisors in $K\left[x\right]$ are the constant polynomials and the associates of $p\left(x\right)$, then $p\left(x\right)$ is called an irreducible polynomial over the number field $K$.

**Property 2** (Property of Irreducible Polynomials)

In $K\left[x\right]$, if $p\left(x\right)$ is irreducible and $p\left(x\right)\mid f\left(x\right)g\left(x\right)$, then $p\left(x\right)\mid f\left(x\right)$ or $p\left(x\right)\mid g\left(x\right)$.

**Theorem 24** (Unique Factorization Theorem)

Every polynomial in $K\left[x\right]$ of degree greater than zero can be uniquely factored into a finite product of irreducible polynomials over the number field $K$.

**Definition 40** (Multiple Factor)

In $K\left[x\right]$, an irreducible polynomial $p\left(x\right)$ is called a $k$-fold factor of the polynomial $f\left(x\right)$ if $p^{k}\left(x\right)\mid f\left(x\right)$ but $p^{k+1}\left(x\right)\nmid f\left(x\right)$.

**Theorem 25** (Criterion for Having No Multiple Factors)

Let $K$ be a number field. A polynomial $f\left(x\right)$ in $K\left[x\right]$ of degree greater than zero has no multiple factors if and only if $f\left(x\right)$ and its derivative $f'\left(x\right)$ are coprime.

**Definition 41** (Root of a Polynomial)

Let $K$ be a number field, and let $R$ be a commutative ring with identity, and $R$ can be regarded as an extension ring of $K$. For a polynomial $f\left(x\right)$ in $K\left[x\right]$, if there is an element $c$ in $R$ such that $f\left(c\right)=0$, then $c$ is called a root of $f\left(x\right)$ in $R$.

**Theorem 26** (Remainder Theorem)

In $K\left[x\right]$, the remainder obtained by dividing $f\left(x\right)$ by $x-a$ is $f\left(a\right)$.

**Corollary 5** (Factor Theorem)

In $K\left[x\right]$, $x-a$ divides $f\left(x\right)$ if and only if $f\left(a\right)=0$.

**Theorem 27** (Unique Factorization Theorem for Real-Coefficient Polynomials)

Every real-coefficient polynomial of degree greater than zero can be uniquely factored over the real field into a product of linear factors and quadratic factors with negative discriminant.

**Property** (Complex Roots Occur in Conjugate Pairs)

The non-real roots of a real-coefficient polynomial occur in conjugate pairs with the same multiplicity.

**Definition 42** (Primitive Polynomial)

A nonzero integer-coefficient polynomial is called primitive if the greatest common divisor of all its coefficients is $1$.

**Lemma 1** (Gauss's Lemma)

The product of two primitive polynomials is again a primitive polynomial.

**Theorem 28** (Eisenstein's Criterion)

Let

$$
f\left(x\right)=a_{n}x^{n}+\ldots+a_{1}x+a_{0}
$$

be an integer-coefficient polynomial of degree $n$ greater than zero. If there exists a prime number $p$ such that

(1) $p\mid a_{i}$, $i=0,1,\ldots,n-1$;

(2) $p\nmid a_{n}$;

(3) $p^{2}\nmid a_{0}$.
then $f\left(x\right)$ is irreducible over the rational field.

## Polynomials in $n$ Variables

**Definition 43** (Polynomial in $n$ Variables)

Let $K$ be a number field. Using $n$ symbols $x_{1},x_{2},\ldots,x_{n}$ not belonging to $K$, form the expression

$$
\sum_{i_{1},i_{2},\ldots,i_{n}}a_{i_{1}i_{2}\ldots i_{n}}x_{1}^{i_{1}}x_{2}^{i_{2}}\cdots x_{n}^{i_{n}}
$$

where $a_{i_{1}i_{2}\ldots i_{n}}\in K$, and $i_{1},i_{2},\ldots,i_{n}$ are nonnegative integers. Only finitely many monomials have coefficients not equal to $0$. Such an expression is called a polynomial in $n$ variables over the number field $K$.

**Theorem 29** (Leading Term Theorem)

In $K\left[x_{1},x_{2},\ldots,x_{n}\right]$, the leading term of the product of two nonzero polynomials equals the product of their leading terms. Hence the product of two nonzero polynomials is again a nonzero polynomial, i.e. $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ is a ring without zero divisors.

**Definition 44** (Symmetric Polynomial)

Let $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ be a polynomial in $n$ variables over the number field $K$. If for every permutation $j_{1}j_{2}\ldots j_{n}$ of $n$ elements we have

$$
f\left(x_{j_{1}},x_{j_{2}},\ldots,x_{j_{n}}\right)=f\left(x_{1},x_{2},\ldots,x_{n}\right),
$$

then $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ is called a symmetric polynomial in $n$ variables over the number field $K$.

**Elementary Symmetric Polynomials**

$$
\begin{aligned}\sigma_{1}&=x_{1}+x_{2}+\ldots+x_{n}\\
\sigma_{2}&=x_{1}x_{2}+x_{1}x_{3}+\ldots+x_{n-1}x_{n}\\
\ldots&\\
\sigma_{n}&=x_{1}x_{2}\ldots x_{n}.
\end{aligned}
$$

**Newton's Formulas** (Relationship between Power Sums and Elementary Symmetric Polynomials)

Let $S_{k}=x_{1}^{k}+x_{2}^{k}+\ldots+x_{n}^{k}$. Then:

$$
\begin{aligned}S_{1}&=\sigma_{1}\\
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\ldots+\left(-1\right)^{k-1}\sigma_{k-1}S_{1}+\left(-1\right)^{k}k\sigma_{k}&=0, 1\le k\le n\\
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\ldots+\left(-1\right)^{n}\sigma_{n}S_{k-n}&=0, k>n.
\end{aligned}
$$
