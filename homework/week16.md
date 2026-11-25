# week16

> **定义 4.6.1 (正交矩阵)**
> 
> 实数域上的方阵 $A$ 如果满足 $A^{\top}A=I$, 则称 $A$ 是正交矩阵.

> **定义 4.7.1 (映射)**
> 
> 设 $S$ 和 $S'$ 是两个集合, 如果存在一个法则 $f$, 使得集合 $S$ 中每一个元素 $a$, 都有集合 $S'$ 中唯一确定的元素 $b$ 与它对应, 则称 $f$ 是 $S$ 到 $S'$ 的一个映射.

> **定理 4.7.1 (核与象的维数公式)**
> 
> 设 $\mathcal{A}:K^{n}\to{}K^{s}$ 是线性映射, 则核 (即齐次线性方程组的解空间) 的维数与象的维数之和等于定义域的维数, 即 $\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=\dim\left(K^{n}\right)=n$.

> **定义 4.7.5 (线性映射)**
> 
> $K^{n}$ 到 $K^{s}$ 的一个映射 $\mathcal{A}$ 如果保持加法和数量乘法, 即 $\forall\alpha,\beta\in{}K^{n},k\in{}K$, 有 $\mathcal{A}\left(\alpha+\beta\right)=\mathcal{A}\left(\alpha\right)+\mathcal{A}\left(\beta\right)$, $\mathcal{A}\left(k\alpha\right)=k\mathcal{A}\left(\alpha\right)$, 则称 $\mathcal{A}$ 是 $K^{n}$ 到 $K^{s}$ 的一个线性映射.

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

分解唯一.

$\blacksquare$

## 4.7-1

判别下列对应法则是否为 $\mathbb{R}$ 到自身的映射, 是否为单射, 是否为满射:

(1) $x\mapsto{}x^{3}$;

(2) $x\mapsto{}x^{2}-x$;

(3) $x\mapsto2^{x}$;

(4) $x\mapsto\ln{}x$.

### 解答 4.7-1

由**定义 4.7.1 (映射)**, 判别下列对应法则是否为 $\mathbb{R}$ 到自身的映射, 是否为单射, 是否为满射.

(1) $f\left(x\right)=x^{3}$.

是映射. 对任意 $x\in\mathbb{R}$, $x^{3}$ 都有定义且唯一.

单射:

$$
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow{}x_{1}^{3}=x_{2}^{3}\Rightarrow{}x_{1}=x_{2}.
$$

故是单射.

满射: 对任意 $y\in\mathbb{R}$, 存在 $x=\sqrt[3]{y}$ 使得 $f\left(x\right)=y$. 故是满射.

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
f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow2^{x_{1}}=2^{x_{2}}\Rightarrow{}x_{1}=x_{2}.
$$

故是单射.

满射: $2^{x}>0$. 例如 $-1$ 没有原象. 故不是满射.

因此是单射但不是满射.

(4) $f\left(x\right)=\ln{}x$.

不是映射. 因为对 $x\le0$, $\ln{}x$ 没有定义, 不是对所有 $x\in\mathbb{R}$ 都有对应.

$\blacksquare$

## 4.7-4

设 $S$ 是一个有限集合. 证明: 如果映射 $f:S\to{}S$ 是单射, 则 $f$ 一定是双射.

### 解答 4.7-4

由**定义 4.7.1 (映射)**, 设 $S$ 有 $n$ 个元素.

$f$ 是单射, 故 $S$ 中不同元素的象也不同. 因此 $f\left(S\right)$ 的元素个数等于 $\left|S\right|=n$.

又因为 $f\left(S\right)\subseteq{}S$, 且 $\left|f\left(S\right)\right|=n=\left|S\right|$, 所以 $f\left(S\right)=S$.

即 $f$ 是满射.

因此 $f$ 既是单射又是满射, 即 $f$ 是双射.

$\blacksquare$

## 4.7-7

设

$$
A=\left[\begin{array}{rrrr}
1&0&2&1\\
-1&2&1&3\\
1&2&5&5
\end{array}\right].
$$

令 $\mathcal{A}\left(\alpha\right)=A\alpha$, $\forall\alpha\in{}K^{4}$.

(1) 求 $\operatorname{Im}\mathcal{A}$ 的维数和一个基;

(2) 求 $\ker\mathcal{A}$ 的维数和一个基.

### 解答 4.7-7

由**定义 4.7.5 (线性映射)**和**定理 4.7.1 (核与象的维数公式)**, $\mathcal{A}\left(\alpha\right)=A\alpha$ 是线性映射.

(1) $\operatorname{Im}\mathcal{A}$ 等于 $A$ 的列空间.

对 $A$ 作初等行变换:

$$
A=\left[\begin{array}{rrrr}
1&0&2&1\\
-1&2&1&3\\
1&2&5&5
\end{array}\right]
arrow
\left[\begin{array}{rrrr}
1&0&2&1\\
0&2&3&4\\
0&2&3&4
\end{array}\right]
arrow
\left[\begin{array}{rrrr}
1&0&2&1\\
0&2&3&4\\
0&0&0&0
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
x_{1}=-2x_{3}-x_{4},\quad{}x_{2}=-\frac{3}{2}x_{3}-2x_{4}.
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

## 5.1-4

写出 $\mathbb{Z}$ 对于模 $3$ 同余关系的商集 $\mathbb{Z}/\left(3\right)$.

### 解答 5.1-4

由**定义 5.1.4 (商集)**, 模 $3$ 同余: $a\sim{}b\overset{def}{\Leftrightarrow}a$ 与 $b$ 被 $3$ 除所得余数相同.

共有 $3$ 个等价类:

$$
\left[0\right]=\left\{\cdots,-6,-3,0,3,6,\cdots\right\}=\left\{3k\mid{}k\in\mathbb{Z}\right\}.
$$

$$
\left[1\right]=\left\{\cdots,-5,-2,1,4,7,\cdots\right\}=\left\{3k+1\mid{}k\in\mathbb{Z}\right\}.
$$

$$
\left[2\right]=\left\{\cdots,-4,-1,2,5,8,\cdots\right\}=\left\{3k+2\mid{}k\in\mathbb{Z}\right\}.
$$

因此

$$
\mathbb{Z}/\left(3\right)=\left\{\left[0\right],\left[1\right],\left[2\right]\right\}.
$$

$\blacksquare$

## 5.2-1(1)

求下列矩阵的相抵标准形:

$$
A=\left[\begin{array}{rrr}
1&-1&3\\
-2&3&-11\\
4&-5&17
\end{array}\right].
$$

### 解答 5.2-1(1)

由**定理 5.2.1 (相抵标准形)**, 对 $A$ 作初等行变换:

$$
A=\left[\begin{array}{rrr}
1&-1&3\\
-2&3&-11\\
4&-5&17
\end{array}\right]
arrow
\left[\begin{array}{rrr}
1&-1&3\\
0&1&-5\\
0&-1&5
\end{array}\right]
arrow
\left[\begin{array}{rrr}
1&-1&3\\
0&1&-5\\
0&0&0
\end{array}\right]
arrow
\left[\begin{array}{rrr}
1&0&-2\\
0&1&-5\\
0&0&0
\end{array}\right].
$$

再作初等列变换: 第 $3$ 列 $+2\times$ 第 $1$ 列, 第 $3$ 列 $+5\times$ 第 $2$ 列.

$$
Aarrow\left[\begin{array}{rrr}
1&0&0\\
0&1&0\\
0&0&0
\end{array}\right].
$$

因此由**定理 5.2.1 (相抵标准形)**, 相抵标准形为

$$
\left[\begin{array}{cc}I_{2}&0\\0&0\end{array}\right].
$$

$\blacksquare$
