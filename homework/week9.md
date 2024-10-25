# week9

> **定理 3.6.1 (线性方程组有解判别定理)**
> 
> 线性方程组

> **定义 3.7.1 (基础解系)**
> 
> 齐次线性方程组有非零解时, 如果它的有限多个解 $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 满足: $1^{\circ}$ 线性无关; $2^{\circ}$ 方程组的每一个解都可以由它们线性表出, 则称它们是一个基础解系.

> **定理 3.7.1 (解空间的维数)**
> 
> 数域 $K$ 上 $n$ 元齐次线性方程组的解空间 $W$ 的维数为: $\dim{W}=n-\text{rank}\left(A\right)$ 其中 $A$ 是系数矩阵.

> **定理 3.8.1 (非齐次方程组的解集结构)**
> 
> 如果数域 $K$ 上 $n$ 元非齐次线性方程组有解, 则它的解集 $U=\gamma_{0}+W$, 其中 $\gamma_{0}$ 是一个特解, $W$ 是导出组的解空间.

## 3.5-8

证明: 如果 $m\times{n}$ 矩阵 $A$ 的秩为 $r$, 则它的任何 $s$ 行组成的子矩阵 $A_{1}$ 的秩不小于 $r+s-m$.

### 解答 3.5-8

由**定义 3.5.1 (矩阵的秩)**, 矩阵 $A$ 的行秩与列秩统称为 $A$ 的秩. 要证明 $A_{1}$ 的秩不小于 $r+s-m$.

设 $A_{2}$ 是 $A$ 的其余 $m-s$ 行组成的子矩阵.

把 $A$ 看作行向量组, $A$ 的行向量组的秩为 $r$.

$A$ 的行向量组 $=A_{1}$ 的行向量组 $\cup{A}_{2}$ 的行向量组.

由向量组之并的秩的上界,

$$
\text{rank}\left(A\right)\le\text{rank}\left(A_{1}\right)+\text{rank}\left(A_{2}\right).
$$

又 $A_{2}$ 只有 $m-s$ 行, 故 $\text{rank}\left(A_{2}\right)\le{m}-s$.

因此

$$
r\le\text{rank}\left(A_{1}\right)+\left(m-s\right).
$$

移项得

$$
\text{rank}\left(A_{1}\right)\ge{r}-\left(m-s\right)=r+s-m.
$$

$\blacksquare$

## 3.5-13

设 $A$ 是 $s\times{n}$ 矩阵, $B$ 是 $l\times{m}$ 矩阵, $C$ 是 $s\times{m}$ 矩阵, 证明:

$$
\text{rank}\left(\begin{array}{cc}A&C\\0&B\end{array}\right)\ge\text{rank}\left(A\right)+\text{rank}\left(B\right).
$$

### 解答 3.5-13

由**定义 3.5.1 (矩阵的秩)**, 要证明分块矩阵的秩不小于 $A$ 的秩与 $B$ 的秩之和. 取 $A$ 和 $B$ 的列空间的基来构造线性无关向量组.

设 $\text{rank}\left(A\right)=r_{1}$, $\text{rank}\left(B\right)=r_{2}$.

取 $A$ 的列空间的一个基: $\alpha_{1},\cdots,\alpha_{r_{1}}$ ( $s$ 维向量).

取 $B$ 的列空间的一个基: $\beta_{1},\cdots,\beta_{r_{2}}$ ( $l$ 维向量).

考虑分块矩阵

$$
M=\left(\begin{array}{cc}A&C\\0&B\end{array}\right)
$$

的以下列向量:

$$
\begin{bmatrix}\alpha_{1}\\0\end{bmatrix},\cdots,\begin{bmatrix}\alpha_{r_{1}}\\0\end{bmatrix},
\begin{bmatrix}c_{1}\\\beta_{1}\end{bmatrix},\cdots,\begin{bmatrix}c_{r_{2}}\\\beta_{r_{2}}\end{bmatrix},
$$

其中 $c_{i}$ 是从 $C$ 的列中适当选取的 $s$ 维向量, 使得对应 $M$ 的列的下半部分为 $\beta_{i}$.

证明这 $r_{1}+r_{2}$ 个向量线性无关: 设

$$
k_{1}\begin{bmatrix}\alpha_{1}\\0\end{bmatrix}+\cdots+k_{r_{1}}\begin{bmatrix}\alpha_{r_{1}}\\0\end{bmatrix}
+l_{1}\begin{bmatrix}c_{1}\\\beta_{1}\end{bmatrix}+\cdots+l_{r_{2}}\begin{bmatrix}c_{r_{2}}\\\beta_{r_{2}}\end{bmatrix}=0.
$$

下半部分: $l_{1}\beta_{1}+\cdots+l_{r_{2}}\beta_{r_{2}}=0$. 因为 $\beta_{1},\cdots,\beta_{r_{2}}$ 线性无关, 所以 $l_{1}=\cdots=l_{r_{2}}=0$.

上半部分: $k_{1}\alpha_{1}+\cdots+k_{r_{1}}\alpha_{r_{1}}=0$. 因为 $\alpha_{1},\cdots,\alpha_{r_{1}}$ 线性无关, 所以 $k_{1}=\cdots=k_{r_{1}}=0$.

故这 $r_{1}+r_{2}$ 个向量线性无关.

因此

$$
\text{rank}\left(M\right)\ge{r}_{1}+r_{2}=\text{rank}\left(A\right)+\text{rank}\left(B\right).
$$

$\blacksquare$

## 3.6-2

判断下述线性方程组有没有解, 有多少解.

$$
\begin{cases}
x_{1}+ax_{2}+a^{2}x_{3}+\cdots+a^{n-1}x_{n}=b_{1},\\
x_{1}+a^{2}x_{2}+a^{4}x_{3}+\cdots+a^{2\left(n-1\right)}x_{n}=b_{2},\\
\cdots\cdots\cdots\cdots\\
x_{1}+a^{s}x_{2}+a^{2s}x_{3}+\cdots+a^{s\left(n-1\right)}x_{n}=b_{s},
\end{cases}
$$

其中 $s<{}n$, $a\ne0$ 且当 $0<{}r<{}s$ 时, $a^{r}\ne1$.

### 解答 3.6-2

由**定理 3.6.1 (线性方程组有解判别定理)**和**定理 3.6.2 (解的个数判别)**, 需比较系数矩阵与增广矩阵的秩.

系数矩阵 $A$ 是 $s\times{n}$ 矩阵. 取 $A$ 的前 $s$ 列组成的 $s$ 阶子式:

$$
D=\left|\begin{array}{cccc}
1&a&a^{2}&\cdots&a^{s-1}\\
1&a^{2}&a^{4}&\cdots&a^{2\left(s-1\right)}\\
\vdots&\vdots&\vdots&&\vdots\\
1&a^{s}&a^{2s}&\cdots&a^{s\left(s-1\right)}
\end{array}\right|.
$$

由**范德蒙行列式**的计算公式, 这是范德蒙行列式,

$$
D=\prod_{1\le{i}<{}j\le{s}}\left(a^{j}-a^{i}\right).
$$

因为 $a\ne0$ 且当 $0<{}r<{}s$ 时 $a^{r}\ne1$, 所以 $a,a^{2},\cdots,a^{s}$ 两两不同, 故 $D\ne0$.

因此 $\text{rank}\left(A\right)\ge{s}$.

又 $A$ 只有 $s$ 行, 故 $\text{rank}\left(A\right)\le{s}$.

所以 $\text{rank}\left(A\right)=s$.

增广矩阵 $\overline{A}$ 是 $A$ 加了一列, 故 $\text{rank}\left(\overline{A}\right)\ge\text{rank}\left(A\right)=s$.

又 $\overline{A}$ 只有 $s$ 行, 故 $\text{rank}\left(\overline{A}\right)\le{s}$.

所以 $\text{rank}\left(\overline{A}\right)=s=\text{rank}\left(A\right)$.

由**定理 3.6.1 (线性方程组有解判别定理)**, 因此方程组有解.

又 $\text{rank}\left(A\right)=s<{}n$ (未知量数目), 由**定理 3.6.2 (解的个数判别)**, 故方程组有无穷多个解.

$\blacksquare$

## 3.6-4

已知线性方程组

$$
\begin{cases}
a_{11}x_{1}+a_{12}x_{2}+\cdots+a_{1n}x_{n}=b_{1},\\
a_{21}x_{1}+a_{22}x_{2}+\cdots+a_{2n}x_{n}=b_{2},\\
\cdots\cdots\cdots\cdots\\
a_{n1}x_{1}+a_{n2}x_{2}+\cdots+a_{nn}x_{n}=b_{n}
\end{cases}
$$

的系数矩阵 $A$ 的秩等于下述矩阵 $B$ 的秩:

$$
B=\left[\begin{array}{ccccc}
a_{11}&a_{12}&\cdots&a_{1n}&b_{1}\\
a_{21}&a_{22}&\cdots&a_{2n}&b_{2}\\
\vdots&\vdots&&\vdots&\vdots\\
a_{n1}&a_{n2}&\cdots&a_{nn}&b_{n}\\
b_{1}&b_{2}&\cdots&b_{n}&0
\end{array}\right].
$$

证明上述线性方程组有解.

### 解答 3.6-4

由**定理 3.6.1 (线性方程组有解判别定理)**, 要证明线性方程组有解, 即证明系数矩阵 $A$ 与增广矩阵 $\overline{A}$ 有相同的秩.

设增广矩阵为 $\overline{A}$, 即 $\overline{A}=\left[A,b\right]$, 其中 $b=\left(b_{1},b_{2},\cdots,b_{n}\right)^{\top}$.

注意到 $\overline{A}$ 是 $B$ 的前 $n$ 行, 故 $\overline{A}$ 是 $B$ 的子矩阵.

因此 $\text{rank}\left(\overline{A}\right)\le\text{rank}\left(B\right)$.

又 $A$ 是 $\overline{A}$ 的子矩阵, 故 $\text{rank}\left(A\right)\le\text{rank}\left(\overline{A}\right)$.

由题设 $\text{rank}\left(A\right)=\text{rank}\left(B\right)$, 故

$$
\text{rank}\left(A\right)\le\text{rank}\left(\overline{A}\right)\le\text{rank}\left(B\right)=\text{rank}\left(A\right).
$$

因此 $\text{rank}\left(\overline{A}\right)=\text{rank}\left(A\right)$.

由**定理 3.6.1 (线性方程组有解判别定理)**, 该方程组有解.

$\blacksquare$

## 3.7-1(1)

求下列数域 $K$ 上齐次线性方程组的一个基础解系, 并且写出它的解集.

$$
\begin{cases}
x_{1}-3x_{2}+x_{3}-2x_{4}=0,\\
-5x_{1}+x_{2}-2x_{3}+3x_{4}=0,\\
-x_{1}-11x_{2}+2x_{3}-5x_{4}=0,\\
3x_{1}+5x_{2}+x_{4}=0.
\end{cases}
$$

### 解答 3.7-1(1)

由**定义 3.7.1 (基础解系)**和**定理 3.7.1 (解空间的维数)**, 系数矩阵作初等行变换:

$$
\left[\begin{array}{rrrr}
1&-3&1&-2\\
-5&1&-2&3\\
-1&-11&2&-5\\
3&5&0&1
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1&-3&1&-2\\
0&-14&3&-7\\
0&0&0&0\\
0&0&0&0
\end{array}\right].
$$

秩为 $2$, 未知量数目为 $4$. 由**定理 3.7.1 (解空间的维数)**, 解空间的维数为 $4-2=2$, 故基础解系含 $2$ 个向量.

一般解:

$$
\begin{cases}
x_{1}=\frac{-5x_{3}+7x_{4}}{14},\\
x_{2}=\frac{3x_{3}-7x_{4}}{14},
\end{cases}
$$

其中 $x_{3},x_{4}$ 是自由未知量.

令 $x_{3}=14,x_{4}=0$, 得 $\eta_{1}=\left(-5,3,14,0\right)^{\top}$.

令 $x_{3}=0,x_{4}=14$, 得 $\eta_{2}=\left(7,-7,0,14\right)^{\top}$.

由**定义 3.7.1 (基础解系)**, $\eta_{1},\eta_{2}$ 线性无关, 且方程组的每一个解都可以由它们线性表出, 故它们是一个基础解系.

解集:

$$
W=\left\{k_{1}\eta_{1}+k_{2}\eta_{2}\mid{k}_{1},k_{2}\in{K}\right\}.
$$

$\blacksquare$

## 3.7-1(2)

求下列数域 $K$ 上齐次线性方程组的一个基础解系, 并且写出它的解集.

$$
\begin{cases}
3x_{1}-x_{2}+2x_{3}+x_{4}=0,\\
x_{1}+3x_{2}-x_{3}+2x_{4}=0,\\
-2x_{1}+5x_{2}+x_{3}-x_{4}=0,\\
3x_{1}+10x_{2}+x_{3}+4x_{4}=0,\\
-2x_{1}+15x_{2}-4x_{3}+4x_{4}=0.
\end{cases}
$$

### 解答 3.7-1(2)

由**定义 3.7.1 (基础解系)**和**定理 3.7.1 (解空间的维数)**, 系数矩阵作初等行变换:

$$
\left[\begin{array}{rrrr}
3&-1&2&1\\
1&3&-1&2\\
-2&5&1&-1\\
3&10&1&4\\
-2&15&-4&4
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1&3&-1&2\\
0&1&4&-2\\
0&0&-45&25\\
0&0&0&0\\
0&0&0&0
\end{array}\right].
$$

秩为 $3$, 未知量数目为 $4$, 故基础解系含 $4-3=1$ 个向量.

一般解:

$$
\begin{cases}
x_{1}=-\frac{7}{9}x_{4},\\
x_{2}=-\frac{2}{9}x_{4},\\
x_{3}=\frac{5}{9}x_{4},
\end{cases}
$$

其中 $x_{4}$ 是自由未知量.

令 $x_{4}=9$, 得 $\eta_{1}=\left(-7,-2,5,9\right)^{\top}$.

由**定义 3.7.1 (基础解系)**, $\eta_{1}$ 线性无关, 且方程组的每一个解都可以由它线性表出, 故它是一个基础解系.

解集:

$$
W=\left\{k\eta_{1}\mid{k}\in{K}\right\}.
$$

$\blacksquare$

## 3.7-4

证明: 设 $n$ 元齐次线性方程组的系数矩阵的秩为 $r$ $\left(r<{}n\right)$, 设 $\delta_{1},\delta_{2},\cdots,\delta_{m}$ 是方程组的解向量, 则

$$
\text{rank}\left\{\delta_{1},\delta_{2},\cdots,\delta_{m}\right\}\le{n}-r.
$$

### 解答 3.7-4

由**定理 3.7.1 (解空间的维数)**, 齐次线性方程组的解空间 $W$ 的维数为

$$
\dim{W}=n-\text{rank}\left(A\right)=n-r.
$$

$\delta_{1},\delta_{2},\cdots,\delta_{m}$ 都是 $W$ 中的向量, 故 $\left\langle\delta_{1},\delta_{2},\cdots,\delta_{m}\right\rangle\subseteq{W}$.

因此

$$
\text{rank}\left\{\delta_{1},\delta_{2},\cdots,\delta_{m}\right\}
=\dim\left\langle\delta_{1},\delta_{2},\cdots,\delta_{m}\right\rangle
\le\dim{W}=n-r.
$$

$\blacksquare$
