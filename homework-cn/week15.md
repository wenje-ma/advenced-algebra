# week15

> **定义 4.6.1 (正交矩阵)**
> 
> 实数域上的方阵 $A$ 如果满足 $A^{\top}A=I$, 则称 $A$ 是正交矩阵.

> **定义 4.6.2 (标准内积)**
> 
> 在 $\mathbb{R}^{n}$ 中, 任给 $\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)$, $\beta=\left(b_{1},b_{2},\cdots,b_{n}\right)$, 规定

> **命题 4.6.2 (正交向量组线性无关)**
> 
> 欧几里得空间 $\mathbb{R}^{n}$ 中, 正交向量组一定是线性无关的.

> **定义 4.7.1 (映射)**
> 
> 设 $S$ 和 $S'$ 是两个集合, 如果存在一个法则 $f$, 使得集合 $S$ 中每一个元素 $a$, 都有集合 $S'$ 中唯一确定的元素 $b$ 与它对应, 则称 $f$ 是 $S$ 到 $S'$ 的一个映射.

> **定理 4.7.1 (核与象的维数公式)**
> 
> 设 $\mathcal{A}:K^{n}\to K^{s}$ 是线性映射, 则核 (即齐次线性方程组的解空间) 的维数与象的维数之和等于定义域的维数, 即

$$
\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=\dim\left(K^{n}\right)=n.
$$

> **定义 4.7.5 (线性映射)**
> 
> $K^{n}$ 到 $K^{s}$ 的一个映射 $\mathcal{A}$ 如果保持加法和数量乘法, 即 $\forall\alpha,\beta\in K^{n},k\in K$, 有

$$
\mathcal{A}\left(\alpha+\beta\right)=\mathcal{A}\left(\alpha\right)+\mathcal{A}\left(\beta\right),
$$
$\mathcal{A}\left(k\alpha\right)=k\mathcal{A}\left(\alpha\right)$, 则称 $\mathcal{A}$ 是 $K^{n}$ 到 $K^{s}$ 的一个线性映射.

## 4.6-5

证明: 如果正交矩阵 $A$ 是上三角矩阵, 则 $A$ 一定是对角矩阵, 并且其主对角元是 $1$ 或 $-1$.

### 解答 4.6-5

由**定义 4.6.1 (正交矩阵)**, 设 $A$ 是 $n$ 级上三角矩阵, 且 $A^{\top}A=I$.

因为 $A$ 是上三角矩阵, 故 $A^{\top}$ 是下三角矩阵.

$A^{\top}A=I$ 是对角矩阵.

归纳证明 $A$ 的非对角元都为零.

当 $i=1,j=2$ 时, 考虑 $A^{\top}A$ 的 $\left(1,2\right)$ 元:

$$
\sum_{k=1}^{n}\left(A^{\top}\right)_{1k}A_{k2}=\sum_{k=1}^{n}A_{k1}A_{k2}=0.
$$

因为 $A$ 是上三角矩阵, 所以当 $k> 1$ 时 $A_{k1}=0$. 故上式化为 $A_{11}A_{12}=0$.

因为 $A$ 可逆, 故 $A_{11}\ne0$, 从而 $A_{12}=0$.

同理可证 $A_{1j}=0$ ( $j> 1$ ).

假设第 $1,\cdots,i-1$ 行的非对角元都已证明为零.

考虑 $A^{\top}A$ 的 $\left(i,j\right)$ 元 ( $i< j$ ):

$$
\sum_{k=1}^{i}A_{ki}A_{kj}=0.
$$

由归纳假设, 当 $k< i$ 时 $A_{ki}=0$. 故上式化为 $A_{ii}A_{ij}=0$.

因为 $A_{ii}\ne0$, 故 $A_{ij}=0$.

归纳完成. 因此 $A$ 是对角矩阵.

$A^{\top}A=I$, 得 $A_{ii}^{2}=1$, 故 $A_{ii}=\pm1$. $\blacksquare$

## 4.6-12

在欧几里得空间 $\mathbb{R}^{4}$ 中, 设向量组

$$
\alpha_{1}=\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\0\\1\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}1\\0\\0\\-1\end{bmatrix}.
$$

求与 $\alpha_{1},\alpha_{2},\alpha_{3}$ 等价的正交单位向量组.

### 解答 4.6-12

由施密特正交化方法.

令 $\beta_{1}=\alpha_{1}=\left(1,1,0,0\right)^{\top}$.

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}.
$$

$\left(\alpha_{2},\beta_{1}\right)=1$, $\left(\beta_{1},\beta_{1}\right)=2$.

故

$$
\beta_{2}=\left(1,0,1,0\right)^{\top}-\frac{1}{2}\left(1,1,0,0\right)^{\top}=\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{\top}.
$$

$$
\beta_{3}=\alpha_{3}-\frac{\left(\alpha_{3},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}-\frac{\left(\alpha_{3},\beta_{2}\right)}{\left(\beta_{2},\beta_{2}\right)}\beta_{2}.
$$

$\left(\alpha_{3},\beta_{1}\right)=1$, $\left(\alpha_{3},\beta_{2}\right)=\frac{1}{2}$, $\left(\beta_{2},\beta_{2}\right)=\frac{3}{2}$.

故

$$
\beta_{3}
=\left(1,0,0,-1\right)^{\top}-\frac{1}{2}\left(1,1,0,0\right)^{\top}-\frac{1}{3}\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{\top}=\left(\frac{1}{3},-\frac{1}{3},-\frac{1}{3},-1\right)^{\top}.
$$

验证正交性: $\left(\beta_{1},\beta_{2}\right)=0$, $\left(\beta_{1},\beta_{3}\right)=0$, $\left(\beta_{2},\beta_{3}\right)=0$.

单位化:

$$
\eta_{1}=\frac{\beta_{1}}{\left|\beta_{1}\right|}=\left(\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}},0,0\right)^{\top}.
$$

$$
\eta_{2}=\frac{\beta_{2}}{\left|\beta_{2}\right|}=\left(\frac{1}{\sqrt{6}},-\frac{1}{\sqrt{6}},\frac{2}{\sqrt{6}},0\right)^{\top}.
$$

$$
\eta_{3}=\frac{\beta_{3}}{\left|\beta_{3}\right|}=\left(\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{\sqrt{3}}{2}\right)^{\top}.
$$

$\blacksquare$

## 4.6-14

设 $A$ 是实数域上的 $n$ 级可逆矩阵, 证明: $A$ 可以分解成

$$
A=TB,
$$

其中 $T$ 是正交矩阵, $B$ 是上三角矩阵, 并且 $B$ 的主对角元都为正数; 证明这种分解是唯一的.

### 解答 4.6-14

存在性. 设 $A$ 的列向量组为 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$.

因为 $A$ 可逆, 故 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 线性无关.

由施密特正交化方法, 对 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 作施密特正交化, 得到正交向量组 $\beta_{1},\beta_{2},\cdots,\beta_{n}$, 其中 $\beta_{i}$ 是 $\alpha_{1},\cdots,\alpha_{i}$ 的线性组合, 且 $\alpha_{i}$ 是 $\beta_{1},\cdots,\beta_{i}$ 的线性组合.

把 $\beta_{1},\beta_{2},\cdots,\beta_{n}$ 单位化, 得到正交单位向量组 $\eta_{1},\eta_{2},\cdots,\eta_{n}$.

令 $T=\left(\eta_{1},\eta_{2},\cdots,\eta_{n}\right)$, 则 $T$ 是正交矩阵.

因为 $\alpha_{i}$ 是 $\eta_{1},\cdots,\eta_{i}$ 的线性组合, 所以 $A=TB$, 其中 $B$ 是上三角矩阵.

$B$ 的主对角元为 $\left|\beta_{1}\right|,\left|\beta_{2}\right|,\cdots,\left|\beta_{n}\right|$, 都是正数.

唯一性. 设 $A=T_{1}B_{1}=T_{2}B_{2}$, 其中 $T_{1},T_{2}$ 是正交矩阵, $B_{1},B_{2}$ 是主对角元为正数的上三角矩阵.

则 $T_{2}^{-1}T_{1}=B_{2}B_{1}^{-1}$.

左边 $T_{2}^{-1}T_{1}$ 是正交矩阵 (正交矩阵的乘积仍为正交矩阵).

右边 $B_{2}B_{1}^{-1}$ 是上三角矩阵 (上三角矩阵的乘积仍为上三角矩阵).

由4.6-5的结论, 既是正交矩阵又是上三角矩阵的矩阵一定是对角矩阵, 且主对角元为 $\pm1$.

故 $B_{2}B_{1}^{-1}$ 是对角矩阵, 主对角元为 $\pm1$.

又因为 $B_{1},B_{2}$ 的主对角元都是正数, 故 $B_{2}B_{1}^{-1}$ 的主对角元为正数.

因此主对角元只能为 $+1$, 即 $B_{2}B_{1}^{-1}=I$.

故 $B_{2}=B_{1}$, 从而 $T_{2}=T_{1}$.

分解唯一. $\blacksquare$

## 4.7-1

判别下列对应法则是否为 $\mathbb{R}$ 到自身的映射, 是否为单射, 是否为满射:

(1) $x\mapsto x^{3}$;

(2) $x\mapsto x^{2}-x$;

(3) $x\mapsto 2^{x}$;

(4) $x\mapsto\ln x$.

### 解答 4.7-1

由**定义 4.7.1 (映射)**, 判别下列对应法则是否为 $\mathbb{R}$ 到自身的映射, 是否为单射, 是否为满射.

(1) $f\left(x\right)=x^{3}$.

是映射. 对任意 $x\in\mathbb{R}$, $x^{3}$ 都有定义且唯一.

单射:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow x_{1}^{3}=x_{2}^{3}\Rightarrow x_{1}=x_{2}.
$$

故是单射.

满射: 对任意 $y\in\mathbb{R}$, 存在 $x=\sqrt\left[3\right]{y}$ 使得 $f\left(x\right)=y$. 故是满射.

因此既是单射又是满射 (双射).

(2) $f\left(x\right)=x^{2}-x$.

是映射.

单射: $f\left(0\right)=0$, $f\left(1\right)=0$, 但 $0\ne1$. 故不是单射.

满射:

$$
f\left(x\right)=x^{2}-x=\left(x-\frac{1}{2}\right)^{2}-\frac{1}{4}\ge-\frac{1}{4}.
$$

例如 $-1$ 没有原象. 故不是满射.

因此既不是单射也不是满射.

(3) $f\left(x\right)=2^{x}$.

是映射.

单射:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow 2^{x_{1}}=2^{x_{2}}\Rightarrow x_{1}=x_{2}.
$$

故是单射.

满射: $2^{x}> 0$. 例如 $-1$ 没有原象. 故不是满射.

因此是单射但不是满射.

(4) $f\left(x\right)=\ln x$.

不是映射. 因为对 $x\le0$, $\ln x$ 没有定义, 不是对所有 $x\in\mathbb{R}$ 都有对应.

$\blacksquare$

## 4.7-4

设 $S$ 是一个有限集合. 证明: 如果映射 $f:S\to S$ 是单射, 则 $f$ 一定是双射.

### 解答 4.7-4

由**定义 4.7.1 (映射)**, 设 $S$ 有 $n$ 个元素.

$f$ 是单射, 故 $S$ 中不同元素的象也不同. 因此 $f\left(S\right)$ 的元素个数等于 $\left|S\right|=n$.

又因为 $f\left(S\right)\subseteq S$, 且 $\left|f\left(S\right)\right|=n=\left|S\right|$, 所以 $f\left(S\right)=S$.

即 $f$ 是满射.

因此 $f$ 既是单射又是满射, 即 $f$ 是双射. $\blacksquare$

## 4.7-7

设

$$
A=\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
-1 & 2 & 1 & 3\\
1 & 2 & 5 & 5
\end{array}\right].
$$

令 $\mathcal{A}\left(\alpha\right)=A\alpha$, $\forall\alpha\in K^{4}$.

(1) 求 $\operatorname{Im}\mathcal{A}$ 的维数和一个基;

(2) 求 $\ker\mathcal{A}$ 的维数和一个基.

### 解答 4.7-7

由**定义 4.7.5 (线性映射)**和**定理 4.7.1 (核与象的维数公式)**, $\mathcal{A}\left(\alpha\right)=A\alpha$ 是线性映射.

(1) $\operatorname{Im}\mathcal{A}$ 等于 $A$ 的列空间.

对 $A$ 作初等行变换:

$$
A=\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
-1 & 2 & 1 & 3\\
1 & 2 & 5 & 5
\end{array}\right]
\rightarrow
\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
0 & 2 & 3 & 4\\
0 & 2 & 3 & 4
\end{array}\right]
\rightarrow
\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
0 & 2 & 3 & 4\\
0 & 0 & 0 & 0
\end{array}\right].
$$

因此 $\operatorname{rank}\left(A\right)=2$.

主元列为第 $1$ 列和第 $2$ 列, 故 $\operatorname{Im}\mathcal{A}$ 的一个基为

$$
\alpha_{1}=\left(1,-1,1\right)^{\top},\alpha_{2}=\left(0,2,2\right)^{\top}.
$$

$$
\dim\left(\operatorname{Im}\mathcal{A}\right)=\operatorname{rank}\left(A\right)=2.
$$

(2) $\ker\mathcal{A}$ 是 $Ax=0$ 的解空间.

由行阶梯形得同解方程组:

$$
\begin{cases}
x_{1}+2x_{3}+x_{4}=0,\\
2x_{2}+3x_{3}+4x_{4}=0.
\end{cases}
$$

自由未知量为 $x_{3},x_{4}$.

$$
x_{1}=-2x_{3}-x_{4},\quad x_{2}=-\frac{3}{2}x_{3}-2x_{4}.
$$

令 $x_{3}=1,x_{4}=0$:

$$
\xi_{1}=\left(-2,-\frac{3}{2},1,0\right)^{\top}.
$$

令 $x_{3}=0,x_{4}=1$:

$$
\xi_{2}=\left(-1,-2,0,1\right)^{\top}.
$$

因此 $\ker\mathcal{A}$ 的一个基为 $\xi_{1},\xi_{2}$.

$$
\dim\left(\ker\mathcal{A}\right)=4-\operatorname{rank}\left(A\right)=2.
$$

由**定理 4.7.1 (核与象的维数公式)**, 验证:

$$
\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=2+2=4=\dim\left(K^{4}\right).
$$

$\blacksquare$
