# week8

> **定义 3.2.1 (线性相关)**
> 
> $K^{n}$ 中向量组 $\alpha_{1},\cdots,\alpha_{s}$ 称为是线性相关的, 如果有 $K$ 中不全为零的数 $k_{1},\cdots,k_{s}$ 使得 $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$.

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
> $K^{n}$ 中向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 的一个极大线性无关组是由这个向量组生成的子空间 $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\rangle$ 的一个基, 从而 $\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}$.

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
\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)^{\top}\in{}K^{n},
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

由**定义 3.4.1 (基)**, 因此 $\eta_{1},\eta_{2},\cdots,\eta_{n}$ 是 $K^{n}$ 的一个基.

$\blacksquare$

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
1&0&2\\
0&4&-4\\
1&-1&3
\end{array}\right|
=1\times\left(4\times3-\left(-4\right)\times\left(-1\right)\right)-0+2\times\left(0\times\left(-1\right)-4\times1\right)
$$

$$
=1\times\left(12-4\right)+2\times\left(-4\right)=8-8=0.
$$

行列式等于 $0$, 由**命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**, 故 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性相关, 不满足**定义 3.4.1 (基)**中"线性无关"的要求, 不是 $K^{3}$ 的一个基.

$\blacksquare$

## 3.4-4

设 $U$ 是 $K^{n}$ 的一个 $r$ 维子空间, $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 中 $r$ 个向量. 证明: 如果 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出, 则 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 的一个基.

### 解答 3.4-4

由**定义 3.4.1 (基)**的要求, 需验证两个条件: 线性无关, 且 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出. 已知第二个条件成立, 只需验证线性无关.

因为 $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性表出, 所以 $U\subseteq\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

又因为 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\in{}U$, 且 $U$ 是子空间, 所以 $\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle\subseteq{}U$.

因此 $U=\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle$.

由**定理 3.4.8 (向量组的秩等于其生成子空间的维数)**,

$$
\dim\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\rangle=\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}.
$$

又 $\dim{}U=r$, 故

$$
\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{r}\right\}=r.
$$

由**命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**, $r$ 个向量的秩为 $r$, 说明它们线性无关.

因此 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性无关, 并且 $U$ 中每一个向量都可以由它们线性表出.

由**定义 3.4.1 (基)**, $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是 $U$ 的一个基.

$\blacksquare$

## 3.5-2(1)

求下列向量组的秩以及它的一个极大线性无关组:

$$
\alpha_{1}=\begin{bmatrix}-1\\5\\3\\-2\end{bmatrix},
\alpha_{2}=\begin{bmatrix}4\\1\\-2\\9\end{bmatrix},
\alpha_{3}=\begin{bmatrix}2\\0\\-1\\4\end{bmatrix},
\alpha_{4}=\begin{bmatrix}0\\3\\4\\-5\end{bmatrix}.
$$

### 解答 3.5-2(1)

由**推论 3.5.5 (用初等行变换求秩)**, 把向量按列排成矩阵, 作初等行变换:

$$
\left[\begin{array}{rrrr}
-1&4&2&0\\
5&1&0&3\\
3&-2&-1&4\\
-2&9&4&-5
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1&-4&-2&0\\
0&1&0&-5\\
0&0&5&54\\
0&0&0&0
\end{array}\right].
$$

由**推论 3.5.5 (用初等行变换求秩)**, 阶梯形矩阵有 $3$ 个非零行, 故秩为 $3$.

由**推论 3.5.5 (用初等行变换求秩)**, 主元在第 $1,2,3$ 列, 故 $\alpha_{1},\alpha_{2},\alpha_{3}$ 是一个极大线性无关组.

$\blacksquare$

## 3.5-3

求下述矩阵 $A$ 的列空间的一个基和行空间的维数:

$$
A=\left[\begin{array}{rrrr}
1&3&-2&-7\\
0&-1&-3&4\\
5&2&0&1\\
1&4&1&-11
\end{array}\right].
$$

### 解答 3.5-3

由**推论 3.5.5 (用初等行变换求秩)**, 作初等行变换:

$$
\left[\begin{array}{rrrr}
1&3&-2&-7\\
0&-1&-3&4\\
5&2&0&1\\
1&4&1&-11
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1&3&-2&-7\\
0&1&3&-4\\
0&0&49&-16\\
0&0&0&0
\end{array}\right].
$$

阶梯形矩阵有 $3$ 个非零行, 由**推论 3.5.5 (用初等行变换求秩)**, 故 $\text{rank}\left(A\right)=3$.

由**定理 3.5.4 (行秩等于列秩)**, 行空间的维数等于矩阵的秩, 即 $3$.

由**推论 3.5.5 (用初等行变换求秩)**, 主元在第 $1,2,3$ 列, 故原矩阵 $A$ 的第 $1,2,3$ 列构成列空间的一个基:

$$
\alpha_{1}=\begin{bmatrix}1\\0\\5\\1\end{bmatrix},
\alpha_{2}=\begin{bmatrix}3\\-1\\2\\4\end{bmatrix},
\alpha_{3}=\begin{bmatrix}-2\\-3\\0\\1\end{bmatrix}.
$$

$\blacksquare$

## 3.5-4

对于 $\lambda$ 的不同的值, 下述矩阵的秩分别是多少?

$$
\left[\begin{array}{rrrr}
1&\lambda&-1&2\\
2&-1&\lambda&5\\
1&10&-6&1
\end{array}\right].
$$

### 解答 3.5-4

由**推论 3.5.5 (用初等行变换求秩)**, 作初等行变换求矩阵的秩:

第 $2$ 行 $-$ 第 $1$ 行 $\times2$: 第 $2$ 行 $=\left(0,-1-2\lambda,\lambda+2,1\right)$.

第 $3$ 行 $-$ 第 $1$ 行: 第 $3$ 行 $=\left(0,10-\lambda,-5,-1\right)$.

矩阵化为:

$$
\left[\begin{array}{rrrr}
1&\lambda&-1&2\\
0&-1-2\lambda&\lambda+2&1\\
0&10-\lambda&-5&-1
\end{array}\right].
$$

第 $2$ 行 $+$ 第 $3$ 行: 第 $2$ 行

$$
=\left(0,9-3\lambda,\lambda-3,0\right)=\left(0,3\left(3-\lambda\right),-\left(3-\lambda\right),0\right).
$$

当 $\lambda=3$ 时:

第 $2$ 行 $=\left(0,0,0,0\right)$, 第 $3$ 行 $=\left(0,7,-5,-1\right)$.

阶梯形矩阵有 $2$ 个非零行, 故秩为 $2$.

当 $\lambda\ne3$ 时:

第 $2$ 行非零. 第 $3$ 行 $-$ 第 $2$ 行 $\times\frac{10-\lambda}{3\left(3-\lambda\right)}$, 第 $3$ 行的第 $4$ 列仍为 $-1\ne0$, 故第 $3$ 行非零.

阶梯形矩阵有 $3$ 个非零行, 故秩为 $3$.

综上: 当 $\lambda=3$ 时, 由**推论 3.5.5 (用初等行变换求秩)**, 阶梯形矩阵有 $2$ 个非零行, 故秩为 $2$; 当 $\lambda\ne3$ 时, 阶梯形矩阵有 $3$ 个非零行, 故秩为 $3$.

$\blacksquare$
