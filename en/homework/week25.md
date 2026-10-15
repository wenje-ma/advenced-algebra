# Assignment 25

> **Definition 1** (Binary relation)<br>Let $S$ be a nonempty set. A subset $W$ of $S\times S$ is called a binary relation on $S$. If $\left(a,b\right)\in W$, then $a$ and $b$ are said to be in the relation $W$.

> **Definition 2** (Equivalence relation)<br>If a binary relation $\sim$ on a set $S$ satisfies the following properties: $\forall a,b,c\in S$, $1^{\circ}a\sim a$ (reflexivity); $2^{\circ}a\sim b\Rightarrow b\sim a$ (symmetry); $3^{\circ}a\sim b$ and $b\sim c\Rightarrow a\sim c$ (transitivity), then $\sim$ is called an equivalence relation on $S$.

> **Definition 4** (Quotient set)<br>Let $\sim$ be an equivalence relation on a set $S$. The set of all equivalence classes is called the quotient set of $S$ by the relation $\sim$, denoted $S/\sim$.

### Problem 1

(Problem 5.1-1) Define a binary relation on the plane $S$ (set of points):

$$
P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)\overset{def}{\Leftrightarrow}x_{1}=x_{2}.
$$

Prove: $\sim$ is an equivalence relation on $S$.

### Solution to Problem 1

By **Definition 2** (Equivalence relation), we verify reflexivity, symmetry, and transitivity.

**Reflexivity**: For any $P\left(x,y\right)\in S$, clearly $x=x$, so $P\sim P$.

**Symmetry**: If $P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)$, then $x_{1}=x_{2}$, hence $x_{2}=x_{1}$, so $P\left(x_{2},y_{2}\right)\sim P\left(x_{1},y_{1}\right)$.

**Transitivity**: If $P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)$ and $P\left(x_{2},y_{2}\right)\sim P\left(x_{3},y_{3}\right)$, then $x_{1}=x_{2}$ and $x_{2}=x_{3}$, hence $x_{1}=x_{3}$, so $P\left(x_{1},y_{1}\right)\sim P\left(x_{3},y_{3}\right)$.

Therefore $\sim$ satisfies all conditions of **Definition 2** (Equivalence relation), so $\sim$ is an equivalence relation on $S$. $\blacksquare$

### Problem 2

(Problem 5.1-4) Write the quotient set $\mathbb{Z}/\left(3\right)$ of $\mathbb{Z}$ under the congruence mod $3$ relation.

### Solution to Problem 2

By **Definition 4** (Quotient set), congruence mod $3$: $a\sim b\overset{def}{\Leftrightarrow}a$ and $b$ have the same remainder when divided by $3$.

There are $3$ equivalence classes:

$$
\left[0\right]=\left\{\cdots,-6,-3,0,3,6,\cdots\right\}=\left\{3k\mid k\in\mathbb{Z}\right\}.
$$

$$
\left[1\right]=\left\{\cdots,-5,-2,1,4,7,\cdots\right\}=\left\{3k+1\mid k\in\mathbb{Z}\right\}.
$$

$$
\left[2\right]=\left\{\cdots,-4,-1,2,5,8,\cdots\right\}=\left\{3k+2\mid k\in\mathbb{Z}\right\}.
$$

Therefore

$$
\mathbb{Z}/\left(3\right)=\left\{\left[0\right],\left[1\right],\left[2\right]\right\}.
$$

$\blacksquare$
