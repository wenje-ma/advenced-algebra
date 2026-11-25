# week10

> **定理 3.8.1 (非齐次方程组的解集结构)**
> 
> 如果数域 $K$ 上 $n$ 元非齐次线性方程组有解, 则它的解集 $U=\gamma_{0}+W$, 其中 $\gamma_{0}$ 是一个特解, $W$ 是导出组的解空间.

> **定义 4.1.1 (矩阵的加法)**
> 
> 设 $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ 都是数域 $K$ 上 $s\times{}n$ 矩阵, 令 $C=\left(a_{ij}+b_{ij}\right)_{s\times{}n}$, 则称 $C$ 是矩阵 $A$ 与 $B$ 的和, 记作 $C=A+B$.

> **定义 4.1.2 (矩阵的数量乘法)**
> 
> 设 $k\in{}K$, 令 $M=\left(ka_{ij}\right)_{s\times{}n}$, 则称 $M$ 是 $k$ 与矩阵 $A$ 的数量乘积, 记作 $M=kA$.

> **定义 4.1.3 (矩阵的乘法)**
> 
> 设 $A=\left(a_{ij}\right)_{s\times{}n}$, $B=\left(b_{ij}\right)_{n\times{}m}$, 令 $C=\left(c_{ij}\right)_{s\times{}m}$, 其中 $c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}$, 则称 $C$ 是 $A$ 与 $B$ 的乘积, 记作 $C=AB$.

## 3.7-5

设 $n$ 个方程的 $n$ 元齐次线性方程组的系数矩阵 $A$ 的行列式等于零, 并且 $A$ 的 $\left(k,l\right)$ 元的代数余子式 $A_{kl}\ne0$. 证明:

$$
\eta_{1}=\begin{bmatrix}A_{k1}\\A_{k2}\\\vdots\\A_{kn}\end{bmatrix}
$$

是这个齐次线性方程组的一个基础解系.

### 解答 3.7-5

由**定义 3.7.1 (基础解系)**和**定理 3.7.1 (解空间的维数)**, 要证明 $\eta_{1}$ 是齐次线性方程组的一个基础解系, 需验证三个条件: $\eta_{1}$ 是解, $\eta_{1}\ne0$, 且解空间的维数为 $1$.

验证 $\eta_{1}$ 是解. 对每个 $i=1,2,\cdots,n$, 计算

$$
a_{i1}A_{k1}+a_{i2}A_{k2}+\cdots+a_{in}A_{kn}.
$$

当 $i=k$ 时, 这是 $\left|A\right|=0$ (题设).

当 $i\ne{}k$ 时, 这是把 $A$ 的第 $k$ 行换成第 $i$ 行后的行列式, 由于有两行相同, 故行列式为 $0$.

因此对所有 $i$, 上式都为 $0$, 即 $A\eta_{1}=0$.

验证 $\eta_{1}\ne0$. 因为 $A_{kl}\ne0$, 所以 $\eta_{1}$ 的第 $l$ 个分量非零, 故 $\eta_{1}\ne0$.

验证解空间维数为 $1$. 因为 $\left|A\right|=0$, 故 $\text{rank}\left(A\right)<{}n$.

又因为 $A_{kl}\ne0$, 说明 $A$ 有一个 $n-1$ 阶子式非零 (划去第 $k$ 行第 $l$ 列后的子式), 故 $\text{rank}\left(A\right)\ge{}n-1$.

因此 $\text{rank}\left(A\right)=n-1$.

由**定理 3.7.1 (解空间的维数)**, 解空间维数 $=n-\text{rank}\left(A\right)=1$.

$\eta_{1}$ 是一个非零解, 它本身就构成解空间的一个基, 即基础解系.

$\blacksquare$

## 3.7-7

设 $A_{1}$ 是 $s\times{}n$ 矩阵 $A=\left(a_{ij}\right)$ 的前 $s-1$ 行组成的子矩阵. 证明: 如果以 $A_{1}$ 为系数矩阵的齐次线性方程组的解都是方程

$$
a_{s1}x_{1}+a_{s2}x_{2}+\cdots+a_{sn}x_{n}=0
$$

的解, 则 $A$ 的第 $s$ 行可以由 $A$ 的前 $s-1$ 行线性表出.

### 解答 3.7-7

由**定理 3.7.1 (解空间的维数)**, 齐次线性方程组的解空间是系数矩阵行空间的正交补. 设 $A_{1}$ 的行空间为 $V_{1}$, 则以 $A_{1}$ 为系数矩阵的齐次线性方程组的解空间 $W_{1}=V_{1}^{\perp}$ ( $V_{1}$ 的正交补).

题设: $W_{1}$ 中的每个 $x$ 都满足 $a_{s1}x_{1}+\cdots+a_{sn}x_{n}=0$.

即第 $s$ 行的行向量 $\gamma_{s}=\left(a_{s1},\cdots,a_{sn}\right)$ 与 $W_{1}$ 中的每个向量正交.

因此 $\gamma_{s}\in\left(W_{1}\right)^{\perp}=V_{1}$.

所以 $\gamma_{s}$ 可以由 $A_{1}$ 的行向量线性表出, 即 $A$ 的第 $s$ 行可以由 $A$ 的前 $s-1$ 行线性表出.

$\blacksquare$

## 3.8-1(1)

求下述数域 $K$ 上非齐次线性方程组的解集:

$$
\begin{cases}
x_{1}-5x_{2}+2x_{3}-3x_{4}=11,\\
-3x_{1}+x_{2}-4x_{3}+2x_{4}=-5,\\
-x_{1}-9x_{2}-4x_{4}=17,\\
5x_{1}+3x_{2}+6x_{3}-x_{4}=-1.
\end{cases}
$$

### 解答 3.8-1(1)

由**定理 3.8.1 (非齐次方程组的解集结构)**, 增广矩阵作初等行变换:

$$
\left[\begin{array}{rrrr\left|r}
1&-5&2&-3&11\\
-3&1&-4&2&-5\\
-1&-9&0&-4&17\\
5&3&6&-1&-1
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr\right|r}
1&-5&2&-3&11\\
0&-14&2&-7&28\\
0&0&0&0&0\\
0&0&0&0&0
\end{array}\right].
$$

秩为 $2$, 等于增广矩阵的秩, 故方程组有解.

一般解:

$$
\begin{cases}
x_{1}=-\frac{9}{7}x_{3}+\frac{1}{2}x_{4}+1,\\
x_{2}=\frac{1}{7}x_{3}-\frac{1}{2}x_{4}-2,
\end{cases}
$$

其中 $x_{3},x_{4}$ 是自由未知量.

令 $x_{3}=x_{4}=0$, 得特解 $\gamma_{0}=\left(1,-2,0,0\right)^{\top}$.

导出组的基础解系:

令 $x_{3}=7,x_{4}=0$, 得 $\eta_{1}=\left(-9,1,7,0\right)^{\top}$.

令 $x_{3}=0,x_{4}=2$, 得 $\eta_{2}=\left(1,-1,0,2\right)^{\top}$.

由**定理 3.8.1 (非齐次方程组的解集结构)**, 解集为特解 $\gamma_{0}$ 加上导出组的解空间 $W$:

$$
U=\left\{\gamma_{0}+k_{1}\eta_{1}+k_{2}\eta_{2}\mid{}k_{1},k_{2}\in{}K\right\}.
$$

$\blacksquare$

## 3.8-2

证明: $n$ 个方程的 $n$ 元非齐次线性方程组有唯一解当且仅当它的导出组只有零解.

### 解答 3.8-2

由**定理 3.8.1 (非齐次方程组的解集结构)**, 非齐次方程组的解集 $U=\gamma_{0}+W$, 其中 $W$ 是导出组的解空间. 要证明非齐次方程组有唯一解当且仅当它的导出组只有零解.

设非齐次线性方程组为 $Ax=\beta$, 其中 $A$ 是 $n\times{}n$ 矩阵; 导出组为 $Ax=0$.

必要性. 设非齐次方程组有唯一解, 则

$$
\text{rank}\left(A\right)=\text{rank}\left(\overline{A}\right)=n\;\text{(系数矩阵的秩等于未知量数目)}.
$$

导出组 $Ax=0$ 的系数矩阵秩为 $n$, 未知量数目为 $n$, 故只有零解.

充分性. 设导出组只有零解, 则 $\text{rank}\left(A\right)=n$.

$A$ 是 $n\times{}n$ 矩阵且 $\text{rank}\left(A\right)=n$, 故 $\left|A\right|\ne0$.

导出组只有零解意味着解空间 $W=\left\{0\right\}$, 故非齐次方程组的解集 $U=\gamma_{0}+W=\left\{\gamma_{0}\right\}$, 即有唯一解.

$\blacksquare$

## 3.8-4

证明: 如果 $\gamma_{0}$ 是非齐次线性方程组 (1) 的一个特解, $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 是它的导出组的一个基础解系. 令

$$
\gamma_{1}=\gamma_{0}+\eta_{1},\gamma_{2}=\gamma_{0}+\eta_{2},\cdots,\gamma_{t}=\gamma_{0}+\eta_{t}.
$$

则非齐次线性方程组 (1) 的任意一个解 $\gamma$ 可以表示成

$$
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},
$$

其中

$$
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

### 解答 3.8-4

由**定理 3.8.1 (非齐次方程组的解集结构)**, 非齐次方程组的解集 $U=\gamma_{0}+W$, 其中 $W$ 是导出组的解空间.

任取 $\gamma\in{}U$, 则 $\gamma-\gamma_{0}\in{}W$.

因为 $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 是 $W$ 的一个基, 所以存在 $k_{1},\cdots,k_{t}\in{}K$ 使得

$$
\gamma-\gamma_{0}=k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{t}\eta_{t}.
$$

将 $\eta_{i}=\gamma_{i}-\gamma_{0}$ 代入:

$$
\gamma=\gamma_{0}+k_{1}\left(\gamma_{1}-\gamma_{0}\right)+k_{2}\left(\gamma_{2}-\gamma_{0}\right)+\cdots+k_{t}\left(\gamma_{t}-\gamma_{0}\right)=\left(1-k_{1}-k_{2}-\cdots-k_{t}\right)\gamma_{0}+k_{1}\gamma_{1}+k_{2}\gamma_{2}+\cdots+k_{t}\gamma_{t}.
$$

令

$$
u_{0}=1-k_{1}-k_{2}-\cdots-k_{t},
$$

$u_{1}=k_{1}$, $\cdots$, $u_{t}=k_{t}$.

则

$$
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

非齐次方程组的任意一个解都可以表示成上述形式. 因此

$$
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},\quad
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

$\blacksquare$

## 4.1-1

设

$$
A=\left[\begin{array}{ccc}
\lambda&0&0\\
0&\lambda&0\\
0&0&\lambda
\end{array}\right],
B=\left[\begin{array}{ccc}
0&1&0\\
0&0&1\\
0&0&0
\end{array}\right].
$$

求 $A+B$.

### 解答 4.1-1

由**定义 4.1.1 (矩阵的加法)**,

$$
A+B=\left[\begin{array}{ccc}
\lambda&1&0\\
0&\lambda&1\\
0&0&\lambda
\end{array}\right].
$$

$\blacksquare$

## 4.1-3

设 $I$ 是 $n$ 级单位矩阵, $J$ 是元素全为 $1$ 的 $n$ 级矩阵. 设

$$
M=\left[\begin{array}{cccc}
k&\lambda&\cdots&\lambda\\
\lambda&k&\cdots&\lambda\\
\vdots&\vdots&&\vdots\\
\lambda&\lambda&\cdots&k
\end{array}\right]_{n\times{}n}.
$$

把 $M$ 表示成 $xI+yJ$ 的形式, 其中 $x,y$ 是待定系数.

### 解答 4.1-3

由**定义 4.1.1 (矩阵的加法)**和**定义 4.1.2 (矩阵的数量乘法)**, $xI+yJ$ 的主对角元为 $x+y$, 其余元素为 $y$.

对比 $M$ 的主对角元为 $k$, 其余元素为 $\lambda$, 得

$$
\begin{cases}
x+y=k,\\
y=\lambda.\end{case
s}
$$

解得 $x=k-\lambda$, $y=\lambda$.

由**定义 4.1.1 (矩阵的加法)**和**定义 4.1.2 (矩阵的数量乘法)**, 故

$$
M=\left(k-\lambda\right)I+\lambda{}J.
$$

$\blacksquare$
