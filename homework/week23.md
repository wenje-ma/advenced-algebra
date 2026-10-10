# 作业 23

> **定义1** (正交矩阵)<br>实数域上的方阵 $A$ 如果满足 $A^{T}A=I$, 则称 $A$ 是正交矩阵.

> **定义2** (内积)<br>在 $\mathbb{R}^{n}$ 中, 任给 $\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)$, $\beta=\left(b_{1},b_{2},\cdots,b_{n}\right)$, 规定 $\left(\alpha,\beta\right)=a_{1}b_{1}+a_{2}b_{2}+\cdots+a_{n}b_{n}$, 称为 $\mathbb{R}^{n}$ 的标准内积.

> **命题2** (正交向量组线性无关)<br>欧几里得空间 $\mathbb{R}^{n}$ 中, 正交向量组一定是线性无关的.

### 习题一

(习题 4.6-1(3)) 判断下列矩阵是否为正交矩阵:

$$
A=\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right].
$$

### 解答 习题一

由**定义1**(正交矩阵), 计算 $A^{T}A$:

$$
A^{T}A=\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right]\left[\begin{array}{rr}
\sqrt{3}/2 & 1/2\\
1/2 & -\sqrt{3}/2
\end{array}\right].
$$

$\left(1,1\right)$ 元: $\left(\frac{\sqrt{3}}{2}\right)^{2}+\left(\frac{1}{2}\right)^{2}=\frac{3}{4}+\frac{1}{4}=1$.

$\left(1,2\right)$ 元: $\frac{\sqrt{3}}{2}\cdot\frac{1}{2}+\frac{1}{2}\cdot\left(-\frac{\sqrt{3}}{2}\right)=\frac{\sqrt{3}}{4}-\frac{\sqrt{3}}{4}=0$.

$\left(2,1\right)$ 元: $\frac{1}{2}\cdot\frac{\sqrt{3}}{2}+\left(-\frac{\sqrt{3}}{2}\right)\cdot\frac{1}{2}=\frac{\sqrt{3}}{4}-\frac{\sqrt{3}}{4}=0$.

$\left(2,2\right)$ 元: $\left(\frac{1}{2}\right)^{2}+\left(-\frac{\sqrt{3}}{2}\right)^{2}=\frac{1}{4}+\frac{3}{4}=1$.

因此 $A^{T}A=I$, 由**定义1**(正交矩阵), 故 $A$ 是正交矩阵. $\blacksquare$

### 习题二

(习题 4.6-1(8)) 判断下列矩阵是否为正交矩阵:

$$
A=\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right].
$$

### 解答 习题二

由**定义1**(正交矩阵), 计算 $A^{T}A$:

$$
A^{T}A=\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right]\left[\begin{array}{rr}
1 & 1\\
1 & -1
\end{array}\right]
=\left[\begin{array}{rr}
2 & 0\\
0 & 2
\end{array}\right].
$$

显然 $A^{T}A\ne I$, 由**定义1**(正交矩阵), 故 $A$ 不是正交矩阵. $\blacksquare$

### 习题三

(习题 4.6-3) 证明: 如果 $A$ 是实数域上 $n$ 级对称矩阵, $T$ 是 $n$ 级正交矩阵, 则 $T^{-1}AT$ 是对称矩阵.

### 解答 习题三

由**定义1**(正交矩阵), 因为 $T$ 是正交矩阵, 故 $T^{-1}=T^{T}$.

$$
\left(T^{-1}AT\right)^{T}=T^{T}A^{T}\left(T^{-1}\right)^{T}.
$$

因为 $T$ 是正交矩阵, 故 $T^{-1}=T^{T}$, 从而 $\left(T^{-1}\right)^{T}=\left(T^{T}\right)^{T}=T$.

因此

$$
\left(T^{-1}AT\right)^{T}=T^{T}A^{T}T.
$$

因为 $A$ 是对称矩阵, 故 $A^{T}=A$.

所以

$$
\left(T^{-1}AT\right)^{T}=T^{T}AT=T^{-1}AT.
$$

因此 $T^{-1}AT$ 是对称矩阵. $\blacksquare$

### 习题四

(习题 4.6-5) 证明: 如果正交矩阵 $A$ 是上三角矩阵, 则 $A$ 一定是对角矩阵, 并且其主对角元是 $1$ 或 $-1$.

### 解答 习题四

由**定义1**(正交矩阵), 设 $A$ 是 $n$ 级上三角矩阵, 且 $A^{T}A=I$.

因为 $A$ 是上三角矩阵, 故 $A^{T}$ 是下三角矩阵.

$A^{T}A=I$ 是对角矩阵.

**归纳证明 $A$ 的非对角元都为零**.

当 $i=1,\ j=2$ 时, 考虑 $A^{T}A$ 的 $\left(1,2\right)$ 元:

$$
\sum_{k=1}^{n}\left(A^{T}\right)_{1k}A_{k2}=\sum_{k=1}^{n}A_{k1}A_{k2}=0.
$$

因为 $A$ 是上三角矩阵, 所以当 $k>1$ 时 $A_{k1}=0$. 故上式化为 $A_{11}A_{12}=0$.

因为 $A$ 可逆, 故 $A_{11}\ne0$, 从而 $A_{12}=0$.

同理可证 $A_{1j}=0$ ( $j>1$ ).

假设第 $1,\cdots,i-1$ 行的非对角元都已证明为零.

考虑 $A^{T}A$ 的 $\left(i,j\right)$ 元 ( $i<j$ ):

$$
\sum_{k=1}^{i}A_{ki}A_{kj}=0.
$$

由归纳假设, 当 $k<i$ 时 $A_{ki}=0$. 故上式化为 $A_{ii}A_{ij}=0$.

因为 $A_{ii}\ne0$, 故 $A_{ij}=0$.

归纳完成. 因此 $A$ 是对角矩阵.

$A^{T}A=I$, 得 $A_{ii}^{2}=1$, 故 $A_{ii}=\pm1$. $\blacksquare$

### 习题五

(习题 4.6-12) 在欧几里得空间 $\mathbb{R}^{4}$ 中, 设向量组

$$
\alpha_{1}=\begin{bmatrix}1\\1\\0\\0\end{bmatrix},\quad
\alpha_{2}=\begin{bmatrix}1\\0\\1\\0\end{bmatrix},\quad
\alpha_{3}=\begin{bmatrix}1\\0\\0\\-1\end{bmatrix}.
$$

求与 $\alpha_{1},\alpha_{2},\alpha_{3}$ 等价的正交单位向量组.

### 解答 习题五

用施密特正交化方法.

令 $\beta_{1}=\alpha_{1}=\left(1,1,0,0\right)^{T}$.

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}.
$$

$\left(\alpha_{2},\beta_{1}\right)=1$, $\left(\beta_{1},\beta_{1}\right)=2$.

故

$$
\beta_{2}=\left(1,0,1,0\right)^{T}-\frac{1}{2}\left(1,1,0,0\right)^{T}=\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{T}.
$$

$$
\beta_{3}=\alpha_{3}-\frac{\left(\alpha_{3},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}-\frac{\left(\alpha_{3},\beta_{2}\right)}{\left(\beta_{2},\beta_{2}\right)}\beta_{2}.
$$

$\left(\alpha_{3},\beta_{1}\right)=1$, $\left(\alpha_{3},\beta_{2}\right)=\frac{1}{2}$, $\left(\beta_{2},\beta_{2}\right)=\frac{3}{2}$.

故

$$
\begin{aligned}
\beta_{3}
&=\left(1,0,0,-1\right)^{T}-\frac{1}{2}\left(1,1,0,0\right)^{T}-\frac{1}{3}\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{T}\\
&=\left(\frac{1}{3},-\frac{1}{3},-\frac{1}{3},-1\right)^{T}.
\end{aligned}
$$

验证正交性: $\left(\beta_{1},\beta_{2}\right)=0$, $\left(\beta_{1},\beta_{3}\right)=0$, $\left(\beta_{2},\beta_{3}\right)=0$.

单位化:

$$
\eta_{1}=\frac{\beta_{1}}{|\beta_{1}|}=\left(\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}},0,0\right)^{T}.
$$

$$
\eta_{2}=\frac{\beta_{2}}{|\beta_{2}|}=\left(\frac{1}{\sqrt{6}},-\frac{1}{\sqrt{6}},\frac{2}{\sqrt{6}},0\right)^{T}.
$$

$$
\eta_{3}=\frac{\beta_{3}}{|\beta_{3}|}=\left(\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{\sqrt{3}}{2}\right)^{T}.
$$

$\blacksquare$

### 习题六

(习题 4.6-14) 设 $A$ 是实数域上的 $n$ 级可逆矩阵, 证明: $A$ 可以分解成

$$
A=TB,
$$

其中 $T$ 是正交矩阵, $B$ 是上三角矩阵, 并且 $B$ 的主对角元都为正数; 证明这种分解是唯一的.

### 解答 习题六

**存在性**. 设 $A$ 的列向量组为 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$.

因为 $A$ 可逆, 故 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 线性无关.

对 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 作施密特正交化, 得到正交向量组 $\beta_{1},\beta_{2},\cdots,\beta_{n}$, 其中 $\beta_{i}$ 是 $\alpha_{1},\cdots,\alpha_{i}$ 的线性组合, 且 $\alpha_{i}$ 是 $\beta_{1},\cdots,\beta_{i}$ 的线性组合.

把 $\beta_{1},\beta_{2},\cdots,\beta_{n}$ 单位化, 得到正交单位向量组 $\eta_{1},\eta_{2},\cdots,\eta_{n}$.

令 $T=\left(\eta_{1},\eta_{2},\cdots,\eta_{n}\right)$, 则 $T$ 是正交矩阵.

因为 $\alpha_{i}$ 是 $\eta_{1},\cdots,\eta_{i}$ 的线性组合, 所以 $A=TB$, 其中 $B$ 是上三角矩阵.

$B$ 的主对角元为 $|\beta_{1}|,|\beta_{2}|,\cdots,|\beta_{n}|$, 都是正数.

**唯一性**. 设 $A=T_{1}B_{1}=T_{2}B_{2}$, 其中 $T_{1},T_{2}$ 是正交矩阵, $B_{1},B_{2}$ 是主对角元为正数的上三角矩阵.

则 $T_{2}^{-1}T_{1}=B_{2}B_{1}^{-1}$.

左边 $T_{2}^{-1}T_{1}$ 是正交矩阵 (正交矩阵的乘积仍为正交矩阵).

右边 $B_{2}B_{1}^{-1}$ 是上三角矩阵 (上三角矩阵的乘积仍为上三角矩阵).

由习题 4.6 第 5 题的结论, 既是正交矩阵又是上三角矩阵的矩阵一定是对角矩阵, 且主对角元为 $\pm1$.

故 $B_{2}B_{1}^{-1}$ 是对角矩阵, 主对角元为 $\pm1$.

又因为 $B_{1},B_{2}$ 的主对角元都是正数, 故 $B_{2}B_{1}^{-1}$ 的主对角元为正数.

因此主对角元只能为 $+1$, 即 $B_{2}B_{1}^{-1}=I$.

故 $B_{2}=B_{1}$, 从而 $T_{2}=T_{1}$.

分解唯一. $\blacksquare$
