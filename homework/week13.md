# 作业 13

> **定义1** (基)<br>设 $U$ 是 $K^{n}$ 的一个子空间, $U$ 中的向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 如果满足: $1^{\circ}$ 线性无关; $2^{\circ}$ $U$ 中每一个向量都可以由它线性表出, 则称它是 $U$ 的一个基.

### 习题一

(习题 3.4-2) 证明: $K^{n}$ 中的向量组

$$
\eta_{1}=\begin{bmatrix}1\\0\\0\\\vdots\\0\end{bmatrix},
\eta_{2}=\begin{bmatrix}1\\1\\0\\\vdots\\0\end{bmatrix},\cdots,
\eta_{n}=\begin{bmatrix}1\\1\\1\\\vdots\\1\end{bmatrix}
$$

是 $K^{n}$ 的一个基.

### 解答 习题一

由**定义1** (基)的要求, 需验证两个条件: 线性无关, 且能线性表出 $K^{n}$ 中每一个向量.

**验证线性无关**. 设

$$
k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{n}\eta_{n}=0.
$$

比较各分量 (从第 $1$ 分量到第 $n$ 分量):

第 $1$ 分量: $k_{1}=0$.

第 $2$ 分量: $k_{1}+k_{2}=0$, 代入 $k_{1}=0$ 得 $k_{2}=0$.

第 $3$ 分量: $k_{1}+k_{2}+k_{3}=0$, 代入 $k_{1}=k_{2}=0$ 得 $k_{3}=0$.

依此类推, 由第 $i$ 分量得 $k_{i}=0$.

故 $\eta_{1},\eta_{2},\cdots,\eta_{n}$ 线性无关.

**验证可线性表出**. 任取

$$
\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)^{T}\in K^{n},
$$
设

$$
\alpha=x_{1}\eta_{1}+x_{2}\eta_{2}+\cdots+x_{n}\eta_{n}.
$$

比较各分量:

第 $1$ 分量: $x_{1}=a_{1}$.

第 $2$ 分量: $x_{1}+x_{2}=a_{2}$, 故 $x_{2}=a_{2}-a_{1}$.

第 $3$ 分量: $x_{1}+x_{2}+x_{3}=a_{3}$, 故 $x_{3}=a_{3}-a_{2}$.

依此类推, $x_{i}=a_{i}-a_{i-1}$ $\left(i=2,\cdots,n\right)$.

表出方式存在且唯一.

由**定义1**, 因此 $\eta_{1},\eta_{2},\cdots,\eta_{n}$ 是 $K^{n}$ 的一个基. $\blacksquare$

### 习题二

(习题 3.4-3(3)) 判断下述向量组是否为 $K^{3}$ 的一个基:

$$
\alpha_{1}=\begin{bmatrix}1\\0\\1\end{bmatrix},
\alpha_{2}=\begin{bmatrix}0\\4\\-1\end{bmatrix},
\alpha_{3}=\begin{bmatrix}2\\-4\\3\end{bmatrix}.
$$

### 解答 习题二

由**定义1** (基)的要求, 判断三个 $3$ 维向量是否为 $K^{3}$ 的基, 等价于判断它们是否线性无关, 即判断它们组成的矩阵的行列式是否不等于 $0$.

$$
\left|\begin{array}{rrr}
1 & 0 & 2\\
0 & 4 & -4\\
1 & -1 & 3
\end{array}\right|
=1\times\left(4\times3-\left(-4\right)\times\left(-1\right)\right)-0+2\times\left(0\times\left(-1\right)-4\times1\right)
$$

$$
=1\times\left(12-4\right)+2\times\left(-4\right)=8-8=0.
$$

行列式等于 $0$, 故 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性相关, 不满足**定义1** (基)中"线性无关"的要求, 不是 $K^{3}$ 的一个基. $\blacksquare$

### 习题三

(习题 3.4-4) 设 $U$ 是 $K^{n}$ 的一个 $r$ 维子空间, $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 中 $r$ 个向量. 证明: 如果 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出, 则 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 的一个基.

### 解答 习题三

由**定义1** (基)的要求, 需验证两个条件: 线性无关, 且 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出. 已知第二个条件成立, 只需验证线性无关.

因为 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出, 所以 $U\subseteq\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

又因为 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\in U$, 且 $U$ 是子空间, 所以 $\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle\subseteq U$.

因此 $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

由定理 $8$,

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}.
$$

又 $\dim U=r$, 故

$$
\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}=r.
$$

$r$ 个向量的秩为 $r$, 说明它们线性无关.

因此 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性无关, 并且 $U$ 中每一个向量都可以由它们线性表出.

$\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 的一个基. $\blacksquare$
