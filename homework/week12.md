# 作业 12

> **定义1** (极大线性无关组)<br>$K^{n}$ 中向量组的一个部分组称为一个极大线性无关组, 如果这个部分组本身是线性无关的, 但是从这个向量组的其余向量中任取一个添进去, 得到的新的部分组都线性相关.

> **定义3** (向量组的秩)<br>向量组的极大线性无关组所含向量的数目称为这个向量组的秩. 记作 $\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}$.

> **命题7** (秩的比较)<br>如果向量组 (I) 可以由向量组 (II) 线性表出, 则 (I) 的秩 $\le$ (II) 的秩.

### 习题一

(习题 3.3-1) 设向量组

$$
\alpha_{1}=\begin{bmatrix}2\\0\\0\end{bmatrix},\quad
\alpha_{2}=\begin{bmatrix}-1\\3\\0\end{bmatrix},\quad
\alpha_{3}=\begin{bmatrix}7\\-4\\0\end{bmatrix}.
$$

求 $\alpha_{1},\alpha_{2},\alpha_{3}$ 的一个极大线性无关组, 以及它的秩.

### 解答 习题一

由**定义1** (极大线性无关组)和**定义3** (向量组的秩), 首先判断 $\alpha_{1},\alpha_{2}$ 是否线性无关. 显然 $\alpha_{2}$ 不是 $\alpha_{1}$ 的倍数, 故 $\alpha_{1},\alpha_{2}$ 线性无关.

再判断 $\alpha_{3}$ 能否由 $\alpha_{1},\alpha_{2}$ 线性表出. 设 $\alpha_{3}=k_{1}\alpha_{1}+k_{2}\alpha_{2}$, 比较分量:

$$
\begin{cases}
2k_{1}-k_{2}=7,\\
3k_{2}=-4,\\
0=0.
\end{cases}
$$

由第 $2$ 式得 $k_{2}=-\frac{4}{3}$, 代入第 $1$ 式得 $k_{1}=\frac{17}{6}$.

故 $\alpha_{3}=\frac{17}{6}\alpha_{1}-\frac{4}{3}\alpha_{2}$.

由**定义1**, 因此 $\alpha_{1},\alpha_{2}$ 是一个极大线性无关组. 由**定义3**, 秩为 $2$. $\blacksquare$

### 习题二

(习题 3.3-7) 证明: 如果秩为 $r$ 的向量组可以由它的 $r$ 个向量线性表出, 则这 $r$ 个向量构成这向量组的一个极大线性无关组.

### 解答 习题二

设向量组 (I) 的秩为 $r$, 且 (I) 可以由它的 $r$ 个向量 $\alpha_{1},\cdots,\alpha_{r}$ 线性表出.

因为 $\alpha_{1},\cdots,\alpha_{r}$ 是 (I) 的一部分, 所以 $\alpha_{1},\cdots,\alpha_{r}$ 可以由 (I) 线性表出.

因此 (I) 与 $\alpha_{1},\cdots,\alpha_{r}$ 等价.

由推论 $8$, 等价的向量组有相同的秩, 故 $\text{rank}\left\{\alpha_{1},\cdots,\alpha_{r}\right\}=r$.

$r$ 个向量的秩为 $r$, 说明它们线性无关.

又因为 (I) 可以由 $\alpha_{1},\cdots,\alpha_{r}$ 线性表出, 所以从 (I) 的其余向量中任取一个添到 $\alpha_{1},\cdots,\alpha_{r}$ 中, 得到的新向量组必线性相关 (否则秩会超过 $r$).

因此 $\alpha_{1},\cdots,\alpha_{r}$ 是 (I) 的一个极大线性无关组. $\blacksquare$

### 习题三

(习题 3.3-8) 证明: 数域 $K$ 上的 $n$ 个方程的 $n$ 元线性方程组

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

对任何 $\beta\in K^{n}$ 都有解的充分必要条件是它的系数行列式 $\left|A\right|\ne0$.

### 解答 习题三

**必要性**. 设对任何 $\beta\in K^{n}$ 都有解.

取 $\beta=\varepsilon_{1},\varepsilon_{2},\cdots,\varepsilon_{n}$ (标准基), 则它们都可以由 $\alpha_{1},\cdots,\alpha_{n}$ 线性表出.

因此 $\alpha_{1},\cdots,\alpha_{n}$ 与 $\varepsilon_{1},\cdots,\varepsilon_{n}$ 等价 (因为 $\alpha_{1},\cdots,\alpha_{n}$ 可以由 $\varepsilon_{1},\cdots,\varepsilon_{n}$ 线性表出, 反之亦然).

由推论 $8$, $\text{rank}\left\{\alpha_{1},\cdots,\alpha_{n}\right\}=\text{rank}\left\{\varepsilon_{1},\cdots,\varepsilon_{n}\right\}=n$.

$n$ 个 $n$ 维向量的秩为 $n$, 说明它们线性无关, 故它们组成的矩阵的行列式 $\left|A\right|\ne0$.

**充分性**. 设 $\left|A\right|\ne0$, 则 $\alpha_{1},\cdots,\alpha_{n}$ 线性无关.

在 $K^{n}$ 中, $n$ 个线性无关的向量构成 $K^{n}$ 的一个基.

因此任何 $\beta\in K^{n}$ 都可以由 $\alpha_{1},\cdots,\alpha_{n}$ 线性表出, 即方程组有解.

$\blacksquare$

### 习题四

(习题 3.3-11) 证明: 两个向量组等价的充分必要条件是: 它们的秩相等, 并且其中一个向量组可以由另外一个向量组线性表出.

### 解答 习题四

**必要性**. 设两个向量组 (I) 和 (II) 等价.

由推论 $8$, 等价的向量组有相同的秩.

又因为等价意味着互相可以线性表出, 所以其中一个向量组可以由另外一个向量组线性表出.

**充分性**. 设 (I) 和 (II) 的秩相等, 且 (I) 可以由 (II) 线性表出.

设 (I) 的一个极大线性无关组为 $\alpha_{1},\cdots,\alpha_{r}$, (II) 的一个极大线性无关组为 $\beta_{1},\cdots,\beta_{r}$.

因为 (I) 可以由 (II) 线性表出, 所以 $\alpha_{1},\cdots,\alpha_{r}$ 可以由 $\beta_{1},\cdots,\beta_{r}$ 线性表出.

又因为 $\alpha_{1},\cdots,\alpha_{r}$ 线性无关, 且向量数目为 $r$, 而 $\beta_{1},\cdots,\beta_{r}$ 也是 $r$ 个线性无关的向量.

由习题 3.3 第 7 题, $r$ 个线性无关的向量可以线性表出一个 $r$ 维空间中的所有向量, 所以 $\beta_{1},\cdots,\beta_{r}$ 可以由 $\alpha_{1},\cdots,\alpha_{r}$ 线性表出.

因此 $\alpha_{1},\cdots,\alpha_{r}$ 与 $\beta_{1},\cdots,\beta_{r}$ 等价.

又因为 (I) 与 $\alpha_{1},\cdots,\alpha_{r}$ 等价, (II) 与 $\beta_{1},\cdots,\beta_{r}$ 等价, 由传递性得 (I) 与 (II) 等价.

$\blacksquare$
