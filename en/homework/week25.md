# week25

> **Definition 5.1.1 (Binary Relation)**<br>Let $S$ be a nonempty set. A subset $W$ of $S\times S$ is called a binary relation on $S$. If $\left(a,b\right)\in W$, we say $a$ and $b$ are in the relation $W$.

> **Definition 5.1.2 (Equivalence Relation)**<br>A binary relation $\sim$ on a set $S$ is called an equivalence relation if, for all $a,b,c\in S$: $1^{\circ}a\sim a$ (reflexivity); $2^{\circ}a\sim b\Rightarrow b\sim a$ (symmetry); $3^{\circ}a\sim b$ and $b\sim c\Rightarrow a\sim c$ (transitivity).

> **Definition 5.1.4 (Quotient Set)**<br>Let $\sim$ be an equivalence relation on a set $S$. The set consisting of all equivalence classes is called the quotient set of $S$ with respect to $\sim$, denoted $S/\sim$.

---

## 5.1-1

Define a binary relation on the plane $S$ (a set of points):

$$
P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)\overset{def}{\Leftrightarrow}x_{1}=x_{2}.
$$

Prove: $\sim$ is an equivalence relation on $S$.

### Solution 5.1-1

By **Definition 5.1.2 (Equivalence Relation)**, we verify reflexivity, symmetry and transitivity.

**Reflexivity**: for any $P\left(x,y\right)\in S$, clearly $x=x$, so $P\sim P$.

**Symmetry**: if $P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)$, then $x_{1}=x_{2}$, hence $x_{2}=x_{1}$, and so $P\left(x_{2},y_{2}\right)\sim P\left(x_{1},y_{1}\right)$.

**Transitivity**: if $P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)$ and $P\left(x_{2},y_{2}\right)\sim P\left(x_{3},y_{3}\right)$, then $x_{1}=x_{2}$ and $x_{2}=x_{3}$, hence $x_{1}=x_{3}$, and so $P\left(x_{1},y_{1}\right)\sim P\left(x_{3},y_{3}\right)$.

Therefore $\sim$ satisfies all conditions of **Definition 5.1.2 (Equivalence Relation)**, and hence is an equivalence relation on $S$. $\blacksquare$

---

## 5.1-4

Write out the quotient set $\mathbb{Z}/\left(3\right)$ of $\mathbb{Z}$ with respect to the congruence relation modulo $3$.

### Solution 5.1-4

By **Definition 5.1.4 (Quotient Set)**, congruence modulo $3$ means: $a\sim b\overset{def}{\Leftrightarrow}a$ and $b$ have the same remainder upon division by $3$.

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
