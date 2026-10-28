# week25

> **定义 5.1.1 (二元关系)**<br>设 $S$ 是一个非空集合, 我们把 $S\times S$ 的一个子集 $W$ 叫做 $S$ 上的一个二元关系. 如果 $\left(a,b\right)\in W$, 则称 $a$ 与 $b$ 有 $W$ 关系.

> **定义 5.1.2 (等价关系)**<br>集合 $S$ 上的一个二元关系 $\sim$ 如果具有下述性质: $\forall a,b,c\in S$, 有 $1^{\circ}a\sim a$ (反身性); $2^{\circ}a\sim b\Rightarrow b\sim a$ (对称性); $3^{\circ}a\sim b$ 且 $b\sim c\Rightarrow a\sim c$ (传递性), 则称 $\sim$ 是 $S$ 上的一个等价关系.

> **定义 5.1.4 (商集)**<br>设 $\sim$ 是集合 $S$ 上的一个等价关系. 由所有等价类组成的集合称为 $S$ 对于关系 $\sim$ 的商集, 记作 $S/\sim$.

---

## 5.1-1

在平面 $S$ (点集) 上定义一个二元关系:

$$
P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)\overset{def}{\Leftrightarrow}x_{1}=x_{2}.
$$

证明: $\sim$ 是 $S$ 上的一个等价关系.

### 解答 5.1-1

由**定义 5.1.2 (等价关系)**, 需验证反身性, 对称性和传递性.

**反身性**: 对任意 $P\left(x,y\right)\in S$, 显然 $x=x$, 故 $P\sim P$.

**对称性**: 若 $P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)$, 则 $x_{1}=x_{2}$, 从而 $x_{2}=x_{1}$, 故 $P\left(x_{2},y_{2}\right)\sim P\left(x_{1},y_{1}\right)$.

**传递性**: 若 $P\left(x_{1},y_{1}\right)\sim P\left(x_{2},y_{2}\right)$ 且 $P\left(x_{2},y_{2}\right)\sim P\left(x_{3},y_{3}\right)$, 则 $x_{1}=x_{2}$ 且 $x_{2}=x_{3}$, 从而 $x_{1}=x_{3}$, 故 $P\left(x_{1},y_{1}\right)\sim P\left(x_{3},y_{3}\right)$.

因此 $\sim$ 满足**定义 5.1.2 (等价关系)**的全部条件, 故 $\sim$ 是 $S$ 上的等价关系. $\blacksquare$

---

## 5.1-4

写出 $\mathbb{Z}$ 对于模 $3$ 同余关系的商集 $\mathbb{Z}/\left(3\right)$.

### 解答 5.1-4

由**定义 5.1.4 (商集)**, 模 $3$ 同余: $a\sim b\overset{def}{\Leftrightarrow}a$ 与 $b$ 被 $3$ 除所得余数相同.

共有 $3$ 个等价类:

$$
\left[0\right]=\left\{\cdots,-6,-3,0,3,6,\cdots\right\}=\left\{3k\mid k\in\mathbb{Z}\right\}.
$$

$$
\left[1\right]=\left\{\cdots,-5,-2,1,4,7,\cdots\right\}=\left\{3k+1\mid k\in\mathbb{Z}\right\}.
$$

$$
\left[2\right]=\left\{\cdots,-4,-1,2,5,8,\cdots\right\}=\left\{3k+2\mid k\in\mathbb{Z}\right\}.
$$

因此

$$
\mathbb{Z}/\left(3\right)=\left\{\left[0\right],\left[1\right],\left[2\right]\right\}.
$$

$\blacksquare$
