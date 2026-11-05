# week8

> **定义 3.2.1 (线性相关)**
> 
> $K^{n}$ 中向量组 $\alpha_{1},\cdots,\alpha_{s}$ 称为是线性相关的, 如果有 $K$ 中不全为零的数 $k_{1},\cdots,k_{s}$ 使得 $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$.

> **命题 3.2.1 (线性表出与线性相关的关系)**
> 
> 设向量组 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关, 则向量 $\beta$ 可以由 $\alpha_{1},\cdots,\alpha_{s}$ 线性表出的充分必要条件是 $\alpha_{1},\cdots,\alpha_{s},\beta$ 线性相关.

> **定义 3.2.2 (线性无关)**
> 
> $K^{n}$ 中向量组 $\alpha_{1},\cdots,\alpha_{s}$ 如果不是线性相关的, 则称为线性无关的. 即如果从 $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$ 可以推出所有系数全为 $0$, 则称该向量组线性无关.

> **定义 3.3.1 (极大线性无关组)**
> 
> $K^{n}$ 中向量组的一个部分组称为一个极大线性无关组, 如果这个部分组本身是线性无关的, 但是从这个向量组的其余向量中任取一个添进去, 得到的新的部分组都线性相关.

> **定义 3.3.2 (向量组的等价)**
> 
> 如果向量组 $\alpha_{1},\cdots,\alpha_{s}$ 与向量组 $\beta_{1},\cdots,\beta_{t}$ 可以互相线性表出, 则称这两个向量组等价.

> **定义 3.3.3 (向量组的秩)**
> 
> 向量组的极大线性无关组所含向量的数目称为这个向量组的秩. 记作 $\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}$.

> **命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**
> 
> 向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 线性无关的充分必要条件是它的秩等于它所含向量的数目 $s$.

> **命题 3.3.7 (秩的比较)**
> 
> 如果向量组 (I) 可以由向量组 (II) 线性表出, 则 (I) 的秩 $\le$ (II) 的秩.

> **推论 3.3.8 (等价的向量组有相同的秩)**
> 
> 等价的向量组有相同的秩.

> **定义 3.4.1 (基)**
> 
> 设 $U$ 是 $K^{n}$ 的一个子空间, $U$ 中的向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 如果满足: $1^{\circ}$ 线性无关; $2^{\circ}$ $U$ 中每一个向量都可以由它线性表出, 则称它是 $U$ 的一个基.

> **定理 3.4.8 (向量组的秩等于其生成子空间的维数)**
> 
> $K^{n}$ 中向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 的一个极大线性无关组是由这个向量组生成的子空间 $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\rangle$ 的一个基, 从而

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}.
$$

## 3.2-11

设 $a_{1},a_{2},\cdots,a_{r}$ 是两两不同的数, $r\le n$. 令

$$
\alpha_{1}=\begin{bmatrix}1\\a_{1}\\a_{1}^{2}\\\vdots\\a_{1}^{n-1}\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\a_{2}\\a_{2}^{2}\\\vdots\\a_{2}^{n-1}\end{bmatrix},\cdots,
\alpha_{r}=\begin{bmatrix}1\\a_{r}\\a_{r}^{2}\\\vdots\\a_{r}^{n-1}\end{bmatrix}.
$$

证明: $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是线性无关的.

### 解答 3.2-11

由**定义 3.2.2 (线性无关)**, 要证明 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性无关, 即证明齐次线性方程组

$$
k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{r}\alpha_{r}=0
$$

只有零解.

设

$$
k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{r}\alpha_{r}=0.
$$

取前 $r$ 个分量, 得齐次线性方程组:

$$
\begin{cases}
k_{1}+k_{2}+\cdots+k_{r}=0,\\
k_{1}a_{1}+k_{2}a_{2}+\cdots+k_{r}a_{r}=0,\\
\cdots\cdots\cdots\cdots\\
k_{1}a_{1}^{r-1}+k_{2}a_{2}^{r-1}+\cdots+k_{r}a_{r}^{r-1}=0.
\end{cases}
$$

由范德蒙行列式的计算公式, 其系数行列式为 $r$ 阶范德蒙行列式:

$$
\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{1} & a_{2} & \cdots & a_{r}\\
\vdots & \vdots & & \vdots\\
a_{1}^{r-1} & a_{2}^{r-1} & \cdots & a_{r}^{r-1}
\end{array}\right|=\prod_{1\le i< j\le r}\left(a_{j}-a_{i}\right).
$$

因为 $a_{1},a_{2},\cdots,a_{r}$ 两两不同, 所以行列式不等于 $0$.

故齐次方程组只有零解: $k_{1}=k_{2}=\cdots=k_{r}=0$.

因此 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性无关. $\blacksquare$

## 3.3-1

设向量组

$$
\alpha_{1}=\begin{bmatrix}2\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}-1\\3\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}7\\-4\\0\end{bmatrix}.
$$

求 $\alpha_{1},\alpha_{2},\alpha_{3}$ 的一个极大线性无关组, 以及它的秩.

### 解答 3.3-1

由**定义 3.3.1 (极大线性无关组)**和**定义 3.3.3 (向量组的秩)**, 首先判断 $\alpha_{1},\alpha_{2}$ 是否线性无关. 显然 $\alpha_{2}$ 不是 $\alpha_{1}$ 的倍数, 故 $\alpha_{1},\alpha_{2}$ 线性无关.

再判断 $\alpha_{3}$ 能否由 $\alpha_{1},\alpha_{2}$ 线性表出. 设 $\alpha_{3}=k_{1}\alpha_{1}+k_{2}\alpha_{2}$, 比较分量:

$$
\begin{cases}
2k_{1}-k_{2}=7,\\
3k_{2}=-4,\\
0=0.
\end{cases}
$$

由第 $2$ 式得 $k_{2}=-\frac{4}{3}$, 代入第 $1$ 式得 $k_{1}=\frac{17}{6}$.

故

$$
\alpha_{3}=\frac{17}{6}\alpha_{1}-\frac{4}{3}\alpha_{2}.
$$

由**定义 3.3.1 (极大线性无关组)**, 因此 $\alpha_{1},\alpha_{2}$ 是一个极大线性无关组. 由**定义 3.3.3 (向量组的秩)**, 秩为 $2$. $\blacksquare$

## 3.3-7

证明: 如果秩为 $r$ 的向量组可以由它的 $r$ 个向量线性表出, 则这 $r$ 个向量构成这向量组的一个极大线性无关组.

### 解答 3.3-7

设向量组 (I) 的秩为 $r$, 且 (I) 可以由它的 $r$ 个向量 $\alpha_{1},\cdots,\alpha_{r}$ 线性表出.

因为 $\alpha_{1},\cdots,\alpha_{r}$ 是 (I) 的一部分, 所以 $\alpha_{1},\cdots,\alpha_{r}$ 可以由 (I) 线性表出.

由**定义 3.3.2 (向量组的等价)**, 因此 (I) 与 $\alpha_{1},\cdots,\alpha_{r}$ 等价.

由**推论 3.3.8 (等价的向量组有相同的秩)**, 等价的向量组有相同的秩, 故 $\text{rank}\left\{\alpha_{1},\cdots,\alpha_{r}\right\}=r$.

由**命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**, $r$ 个向量的秩为 $r$, 说明它们线性无关.

又因为 (I) 可以由 $\alpha_{1},\cdots,\alpha_{r}$ 线性表出, 所以从 (I) 的其余向量中任取一个添到 $\alpha_{1},\cdots,\alpha_{r}$ 中, 得到的新向量组必线性相关 (否则由**命题 3.3.7 (秩的比较)**, 秩会超过 $r$).

因此 $\alpha_{1},\cdots,\alpha_{r}$ 是 (I) 的一个极大线性无关组. $\blacksquare$

## 3.3-8

证明: 数域 $K$ 上的 $n$ 个方程的 $n$ 元线性方程组

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

对任何 $\beta\in K^{n}$ 都有解的充分必要条件是它的系数行列式 $\left|A\right|\ne0$.

### 解答 3.3-8

必要性. 设对任何 $\beta\in K^{n}$ 都有解.

取 $\beta=\varepsilon_{1},\varepsilon_{2},\cdots,\varepsilon_{n}$ (标准基), 则它们都可以由 $\alpha_{1},\cdots,\alpha_{n}$ 线性表出.

由**定义 3.3.2 (向量组的等价)**, 因此 $\alpha_{1},\cdots,\alpha_{n}$ 与 $\varepsilon_{1},\cdots,\varepsilon_{n}$ 等价 (因为 $\alpha_{1},\cdots,\alpha_{n}$ 可以由 $\varepsilon_{1},\cdots,\varepsilon_{n}$ 线性表出, 反之亦然).

由**推论 3.3.8 (等价的向量组有相同的秩)**,

$$
\text{rank}\left\{\alpha_{1},\cdots,\alpha_{n}\right\}=\text{rank}\left\{\varepsilon_{1},\cdots,\varepsilon_{n}\right\}=n.
$$

由**命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**, $n$ 个 $n$ 维向量的秩为 $n$, 说明它们线性无关, 故它们组成的矩阵的行列式 $\left|A\right|\ne0$.

充分性. 设 $\left|A\right|\ne0$, 则 $\alpha_{1},\cdots,\alpha_{n}$ 线性无关.

在 $K^{n}$ 中, $n$ 个线性无关的向量构成 $K^{n}$ 的一个基.

因此任何 $\beta\in K^{n}$ 都可以由 $\alpha_{1},\cdots,\alpha_{n}$ 线性表出, 即方程组有解.

$\blacksquare$

## 3.3-11

证明: 两个向量组等价的充分必要条件是: 它们的秩相等, 并且其中一个向量组可以由另外一个向量组线性表出.

### 解答 3.3-11

必要性. 设两个向量组 (I) 和 (II) 等价.

由**推论 3.3.8 (等价的向量组有相同的秩)**, 等价的向量组有相同的秩.

又因为等价意味着互相可以线性表出, 所以其中一个向量组可以由另外一个向量组线性表出.

充分性. 设 (I) 和 (II) 的秩相等, 且 (I) 可以由 (II) 线性表出.

设 (I) 的一个极大线性无关组为 $\alpha_{1},\cdots,\alpha_{r}$, (II) 的一个极大线性无关组为 $\beta_{1},\cdots,\beta_{r}$.

因为 (I) 可以由 (II) 线性表出, 所以 $\alpha_{1},\cdots,\alpha_{r}$ 可以由 $\beta_{1},\cdots,\beta_{r}$ 线性表出.

又因为 $\alpha_{1},\cdots,\alpha_{r}$ 线性无关, 且向量数目为 $r$, 而 $\beta_{1},\cdots,\beta_{r}$ 也是 $r$ 个线性无关的向量.

由习题 3.3 第 7 题, $r$ 个线性无关的向量可以线性表出一个 $r$ 维空间中的所有向量, 所以 $\beta_{1},\cdots,\beta_{r}$ 可以由 $\alpha_{1},\cdots,\alpha_{r}$ 线性表出.

由**定义 3.3.2 (向量组的等价)**, 因此 $\alpha_{1},\cdots,\alpha_{r}$ 与 $\beta_{1},\cdots,\beta_{r}$ 等价.

又因为 (I) 与 $\alpha_{1},\cdots,\alpha_{r}$ 等价, (II) 与 $\beta_{1},\cdots,\beta_{r}$ 等价, 由传递性得 (I) 与 (II) 等价.

$\blacksquare$

## 3.4-2

证明: $K^{n}$ 中的向量组

$$
\eta_{1}=\begin{bmatrix}1\\0\\0\\\vdots\\0\end{bmatrix},
\eta_{2}=\begin{bmatrix}1\\1\\0\\\vdots\\0\end{bmatrix},\cdots,
\eta_{n}=\begin{bmatrix}1\\1\\1\\\vdots\\1\end{bmatrix}
$$

是 $K^{n}$ 的一个基.

### 解答 3.4-2

由**定义 3.4.1 (基)**的要求, 需验证两个条件: 线性无关, 且能线性表出 $K^{n}$ 中每一个向量.

验证线性无关. 设

$$
k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{n}\eta_{n}=0.
$$

比较各分量 (从第 $1$ 分量到第 $n$ 分量):

第 $1$ 分量: $k_{1}=0$.

第 $2$ 分量: $k_{1}+k_{2}=0$, 代入 $k_{1}=0$ 得 $k_{2}=0$.

第 $3$ 分量: $k_{1}+k_{2}+k_{3}=0$, 代入 $k_{1}=k_{2}=0$ 得 $k_{3}=0$.

依此类推, 由第 $i$ 分量得 $k_{i}=0$.

故 $\eta_{1},\eta_{2},\cdots,\eta_{n}$ 线性无关.

验证可线性表出. 任取

$$
\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)^{\top}\in K^{n},
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

由**定义 3.4.1 (基)**, 因此 $\eta_{1},\eta_{2},\cdots,\eta_{n}$ 是 $K^{n}$ 的一个基. $\blacksquare$

## 3.4-3(3)

判断下述向量组是否为 $K^{3}$ 的一个基:

$$
\alpha_{1}=\begin{bmatrix}1\\0\\1\end{bmatrix},
\alpha_{2}=\begin{bmatrix}0\\4\\-1\end{bmatrix},
\alpha_{3}=\begin{bmatrix}2\\-4\\3\end{bmatrix}.
$$

### 解答 3.4-3(3)

由**定义 3.4.1 (基)**的要求, 判断三个 $3$ 维向量是否为 $K^{3}$ 的基, 等价于判断它们是否线性无关, 即判断它们组成的矩阵的行列式是否不等于 $0$.

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

行列式等于 $0$, 由**命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**, 故 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性相关, 不满足**定义 3.4.1 (基)**中"线性无关"的要求, 不是 $K^{3}$ 的一个基. $\blacksquare$

## 3.4-4

设 $U$ 是 $K^{n}$ 的一个 $r$ 维子空间, $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 中 $r$ 个向量. 证明: 如果 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出, 则 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 的一个基.

### 解答 3.4-4

由**定义 3.4.1 (基)**的要求, 需验证两个条件: 线性无关, 且 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出. 已知第二个条件成立, 只需验证线性无关.

因为 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出, 所以 $U\subseteq\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

又因为 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\in U$, 且 $U$ 是子空间, 所以 $\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle\subseteq U$.

因此 $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

由**定理 3.4.8 (向量组的秩等于其生成子空间的维数)**,

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}.
$$

又 $\dim U=r$, 故

$$
\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}=r.
$$

由**命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**, $r$ 个向量的秩为 $r$, 说明它们线性无关.

因此 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性无关, 并且 $U$ 中每一个向量都可以由它们线性表出.

由**定义 3.4.1 (基)**, $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 的一个基. $\blacksquare$
