# week7

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

## 3.2-6

设向量组 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 线性无关, 判断向量组

$$
\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}
$$

是否线性无关.

### 解答 3.2-6

由**定义 3.2.2 (线性无关)**, 判断向量组

$$
\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}
$$

是否线性无关, 即判断齐次线性方程组

$$
k_{1}\left(\alpha_{1}+\alpha_{2}\right)+k_{2}\left(\alpha_{2}+\alpha_{3}\right)+k_{3}\left(\alpha_{3}+\alpha_{4}\right)+k_{4}\left(\alpha_{4}+\alpha_{1}\right)=0
$$

是否只有零解.

设

$$
k_{1}\left(\alpha_{1}+\alpha_{2}\right)+k_{2}\left(\alpha_{2}+\alpha_{3}\right)+k_{3}\left(\alpha_{3}+\alpha_{4}\right)+k_{4}\left(\alpha_{4}+\alpha_{1}\right)=0.
$$

整理得

$$
\left(k_{1}+k_{4}\right)\alpha_{1}+\left(k_{1}+k_{2}\right)\alpha_{2}+\left(k_{2}+k_{3}\right)\alpha_{3}+\left(k_{3}+k_{4}\right)\alpha_{4}=0.
$$

因为 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 线性无关, 所以

$$
\begin{cases}
k_{1}+k_{4}=0,\\
k_{1}+k_{2}=0,\\
k_{2}+k_{3}=0,\\
k_{3}+k_{4}=0. \end{
cases}
$$

解得 $k_{2}=-k_{1}$, $k_{3}=k_{1}$, $k_{4}=-k_{1}$, 其中 $k_{1}$ 自由.

令 $k_{1}=1$, 得 $k_{2}=-1$, $k_{3}=1$, $k_{4}=-1$, 这是一组非零解.

故向量组

$$
\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}
$$

线性相关.

具体地,

$$
\left(\alpha_{1}+\alpha_{2}\right)-\left(\alpha_{2}+\alpha_{3}\right)+\left(\alpha_{3}+\alpha_{4}\right)-\left(\alpha_{4}+\alpha_{1}\right)=0.
$$

存在不全为零的数 $1,-1,1,-1$ 使得上述等式成立, 故该向量组线性相关.

$\blacksquare$

## 3.2-7

证明: 如果向量 $\beta$ 可以由向量组 $\alpha_{1},\cdots,\alpha_{s}$ 线性表出, 则表出方式唯一的充分必要条件是 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关.

### 解答 3.2-7

由**定义 3.2.2 (线性无关)**和**定义 3.2.1 (线性相关)**, 证明表出方式唯一的充分必要条件是 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关.

充分性. 设 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关. 假设有两种表出方式:

$$
\beta=k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s},
\beta=l_{1}\alpha_{1}+\cdots+l_{s}\alpha_{s}.
$$

两式相减得

$$
\left(k_{1}-l_{1}\right)\alpha_{1}+\cdots+\left(k_{s}-l_{s}\right)\alpha_{s}=0.
$$

因为 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关, 所以 $k_{i}-l_{i}=0$, 即 $k_{i}=l_{i}$. 表出方式唯一.

必要性. 设表出方式唯一. 反证: 假设 $\alpha_{1},\cdots,\alpha_{s}$ 线性相关, 则存在不全为零的数 $c_{1},\cdots,c_{s}$ 使得 $c_{1}\alpha_{1}+\cdots+c_{s}\alpha_{s}=0$.

设 $\beta=k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}$, 则

$$
\beta=\left(k_{1}+c_{1}\right)\alpha_{1}+\cdots+\left(k_{s}+c_{s}\right)\alpha_{s}.
$$

因为 $c_{i}$ 不全为零, 所以

$$
\left(k_{1}+c_{1},\cdots,k_{s}+c_{s}\right)\ne\left(k_{1},\cdots,k_{s}\right),
$$

这与表出方式唯一矛盾.

假设不成立, 故 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关.

$\blacksquare$

## 3.2-9

证明: 由非零向量组成的向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ $\left(s\ge2\right)$ 线性无关的充分必要条件是: 每一个 $\alpha_{i}$ $\left(1<{}i\le{s}\right)$ 都不能用它前面的向量线性表出.

### 解答 3.2-9

由**定义 3.2.2 (线性无关)**和**定义 3.2.1 (线性相关)**, 证明由非零向量组成的向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ $\left(s\ge2\right)$ 线性无关的充分必要条件是: 每一个 $\alpha_{i}$ $\left(1<{}i\le{s}\right)$ 都不能用它前面的向量线性表出.

必要性. 设 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关. 反证: 假设某个 $\alpha_{i}$ $\left(i>1\right)$ 可以用前面的向量线性表出, 即

$$
\alpha_{i}=k_{1}\alpha_{1}+\cdots+k_{i-1}\alpha_{i-1}.
$$

则

$$
k_{1}\alpha_{1}+\cdots+k_{i-1}\alpha_{i-1}-\alpha_{i}+0\cdot\alpha_{i+1}+\cdots+0\cdot\alpha_{s}=0.
$$

其中系数 $-1\ne0$, 故 $\alpha_{1},\cdots,\alpha_{s}$ 线性相关, 矛盾.

所以每一个 $\alpha_{i}$ $\left(i>1\right)$ 都不能用它前面的向量线性表出.

充分性. 设每一个 $\alpha_{i}$ $\left(i>1\right)$ 都不能用它前面的向量线性表出. 反证: 假设 $\alpha_{1},\cdots,\alpha_{s}$ 线性相关, 则存在不全为零的数 $c_{1},\cdots,c_{s}$ 使得 $c_{1}\alpha_{1}+\cdots+c_{s}\alpha_{s}=0$.

设 $c_{i}$ 是最后一个非零系数

$$
\left(c_{i}\ne0,c_{i+1}=\cdots=c_{s}=0\right).
$$

若 $i=1$, 则 $c_{1}\alpha_{1}=0$. 因为 $\alpha_{1}\ne0$, 所以 $c_{1}=0$, 矛盾. 故 $i>1$.

由 $c_{1}\alpha_{1}+\cdots+c_{i}\alpha_{i}=0$ 得

$$
\alpha_{i}=-\frac{c_{1}}{c_{i}}\alpha_{1}-\cdots-\frac{c_{i-1}}{c_{i}}\alpha_{i-1}.
$$

这说明 $\alpha_{i}$ 可以用前面的向量线性表出, 与已知条件矛盾.

假设不成立, 故 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关.

$\blacksquare$

## 3.2-11

设 $a_{1},a_{2},\cdots,a_{r}$ 是两两不同的数, $r\le{n}$. 令

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
1&1&\cdots&1\\
a_{1}&a_{2}&\cdots&a_{r}\\
\vdots&\vdots&&\vdots\\
a_{1}^{r-1}&a_{2}^{r-1}&\cdots&a_{r}^{r-1}
\end{array}\right|=\prod_{1\le{i}<{}j\le{r}}\left(a_{j}-a_{i}\right).
$$

因为 $a_{1},a_{2},\cdots,a_{r}$ 两两不同, 所以行列式不等于 $0$.

故齐次方程组只有零解: $k_{1}=k_{2}=\cdots=k_{r}=0$.

因此 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性无关.

$\blacksquare$

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

由**定义 3.3.1 (极大线性无关组)**, 因此 $\alpha_{1},\alpha_{2}$ 是一个极大线性无关组. 由**定义 3.3.3 (向量组的秩)**, 秩为 $2$.

$\blacksquare$

## 3.3-7

证明: 如果秩为 $r$ 的向量组可以由它的 $r$ 个向量线性表出, 则这 $r$ 个向量构成这向量组的一个极大线性无关组.

### 解答 3.3-7

按**定义 3.2.1 (线性相关)**, 设向量组 (I) 的秩为 $r$, 且 (I) 可以由它的 $r$ 个向量 $\alpha_{1},\cdots,\alpha_{r}$ 线性表出.

因为 $\alpha_{1},\cdots,\alpha_{r}$ 是 (I) 的一部分, 所以 $\alpha_{1},\cdots,\alpha_{r}$ 可以由 (I) 线性表出.

由**定义 3.3.2 (向量组的等价)**, 因此 (I) 与 $\alpha_{1},\cdots,\alpha_{r}$ 等价.

由**推论 3.3.8 (等价的向量组有相同的秩)**, 等价的向量组有相同的秩, 故 $\text{rank}\left\{\alpha_{1},\cdots,\alpha_{r}\right\}=r$.

由**命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**, $r$ 个向量的秩为 $r$, 说明它们线性无关.

又因为 (I) 可以由 $\alpha_{1},\cdots,\alpha_{r}$ 线性表出, 所以从 (I) 的其余向量中任取一个添到 $\alpha_{1},\cdots,\alpha_{r}$ 中, 得到的新向量组必线性相关 (否则由**命题 3.3.7 (秩的比较)**, 秩会超过 $r$).

因此 $\alpha_{1},\cdots,\alpha_{r}$ 是 (I) 的一个极大线性无关组.

$\blacksquare$

## 3.3-8

证明: 数域 $K$ 上的 $n$ 个方程的 $n$ 元线性方程组

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

对任何 $\beta\in{K}^{n}$ 都有解的充分必要条件是它的系数行列式 $\left|A\right|\ne0$.

### 解答 3.3-8

必要性. 设对任何 $\beta\in{K}^{n}$ 都有解.

取 $\beta=\varepsilon_{1},\varepsilon_{2},\cdots,\varepsilon_{n}$ (标准基), 则它们都可以由 $\alpha_{1},\cdots,\alpha_{n}$ 线性表出.

由**定义 3.3.2 (向量组的等价)**, 因此 $\alpha_{1},\cdots,\alpha_{n}$ 与 $\varepsilon_{1},\cdots,\varepsilon_{n}$ 等价 (因为 $\alpha_{1},\cdots,\alpha_{n}$ 可以由 $\varepsilon_{1},\cdots,\varepsilon_{n}$ 线性表出, 反之亦然).

由**推论 3.3.8 (等价的向量组有相同的秩)**,

$$
\text{rank}\left\{\alpha_{1},\cdots,\alpha_{n}\right\}=\text{rank}\left\{\varepsilon_{1},\cdots,\varepsilon_{n}\right\}=n.
$$

由**命题 3.3.6 (线性无关的充要条件是秩等于所含向量数目)**, $n$ 个 $n$ 维向量的秩为 $n$, 说明它们线性无关, 故它们组成的矩阵的行列式 $\left|A\right|\ne0$.

充分性. 设 $\left|A\right|\ne0$, 则 $\alpha_{1},\cdots,\alpha_{n}$ 线性无关.

在 $K^{n}$ 中, $n$ 个线性无关的向量构成 $K^{n}$ 的一个基.

因此任何 $\beta\in{K}^{n}$ 都可以由 $\alpha_{1},\cdots,\alpha_{n}$ 线性表出, 即方程组有解.

$\blacksquare$
