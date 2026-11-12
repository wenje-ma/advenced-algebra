# week6

$$
\left|\begin{array}{cc}A&0\\C&B\end{array}\right|=\left|A\right|\left|B\right|.
$$
$$
\left|\begin{array}{cccc}
1&1&\cdots&1\\
a_{1}&a_{2}&\cdots&a_{n}\\
a_{1}^{2}&a_{2}^{2}&\cdots&a_{n}^{2}\\
\vdots&\vdots&&\vdots\\
a_{1}^{n-1}&a_{2}^{n-1}&\cdots&a_{n}^{n-1}
\end{array}\right|=\prod_{1\le{i}<{}j\le{n}}\left(a_{j}-a_{i}\right).
$$

> **定理 2.6.1 (拉普拉斯定理)**
> 
> 在 $n$ 阶行列式 $\left|A\right|$ 中, 取定 $k$ 行, 则这 $k$ 行元素形成的所有 $k$ 阶子式与它们自己的代数余子式的乘积之和等于 $\left|A\right|$.

> **定义 3.1.1 (线性组合与线性表出)**
> 
> $K^{n}$ 中, 给定向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$, 任给 $K$ 中一组数 $k_{1},k_{2},\cdots,k_{s}$, 称 $k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s}$ 为向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 的一个线性组合. 如果

$$
\beta=k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s},
$$
则称 $\beta$ 可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 线性表出.

> **命题 3.1.1 (线性表出与方程组有解的关系)**
> 
> 数域 $K$ 上 $n$ 元线性方程组

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$
有解 $\Leftrightarrow$ $\beta$ 可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 线性表出 $\Leftrightarrow$ $\beta\in\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\right\rangle$.

## 2.6-3

计算下述行列式:

$$
\left|\begin{array}{cccccc}
0&\cdots&0&a_{11}&\cdots&a_{1k}\\
\vdots&&\vdots&\vdots&&\vdots\\
0&\cdots&0&a_{k1}&\cdots&a_{kk}\\
b_{11}&\cdots&b_{1r}&c_{11}&\cdots&c_{1k}\\
\vdots&&\vdots&\vdots&&\vdots\\
b_{r1}&\cdots&b_{rr}&c_{r1}&\cdots&c_{rk}
\end{array}\right|.
$$

### 解答 2.6-3

由**定理 2.6.1 (拉普拉斯定理)**, 按前 $k$ 行展开. 前 $k$ 行的所有 $k$ 阶子式中, 只有右上角的 $k$ 阶子式 $A=\left(a_{ij}\right)_{k\times{k}}$ 可能不为零 (因为前 $k$ 行的前 $r$ 列全为 $0$).

右上角的 $k$ 阶子式 $A$ 的代数余子式: 行指标为 $1,2,\cdots,k$, 列指标为 $r+1,r+2,\cdots,r+k$.

由**定理 2.6.1 (拉普拉斯定理)**, 余子式是去掉前 $k$ 行和后 $k$ 列后的 $r$ 阶行列式, 即 $B=\left(b_{ij}\right)_{r\times{r}}$.

代数余子式为

$$
\left(-1\right)^{\left(1+2+\cdots+k\right)+\left(r+1+r+2+\cdots+r+k\right)}\cdot\left|B\right|
=\left(-1\right)^{\frac{k\left(k+1\right)}{2}+kr+\frac{k\left(k+1\right)}{2}}\cdot\left|B\right|
=\left(-1\right)^{k\left(k+1+r\right)}\cdot\left|B\right|.
$$

故行列式值为

$$
\left|A\right|\cdot\left(-1\right)^{k\left(k+1+r\right)}\cdot\left|B\right|
=\left(-1\right)^{k\left(r+k+1\right)}\left|A\right|\left|B\right|.
$$

$\blacksquare$

## 2.6-4(1)

设 $\left|A\right|$ 是关于 $1,2,\cdots,n$ 这 $n$ 个数的范德蒙行列式. 计算:

$$
A\begin{bmatrix}1,2,\cdots,n-1\\2,3,\cdots,n\end{bmatrix}.
$$

### 解答 2.6-4(1)

由范德蒙行列式的计算公式, 范德蒙行列式为

$$
\left|A\right|=\left|\begin{array}{cccc}
1&1&\cdots&1\\
a_{1}&a_{2}&\cdots&a_{n}\\
a_{1}^{2}&a_{2}^{2}&\cdots&a_{n}^{2}\\
\vdots&\vdots&&\vdots\\
a_{1}^{n-1}&a_{2}^{n-1}&\cdots&a_{n}^{n-1}
\end{array}\right|,
$$

其中 $a_{i}=i$.

取第 $1,2,\cdots,n-1$ 行 (即 $0$ 次幂到 $n-2$ 次幂行) 和第 $2,3,\cdots,n$ 列 (即 $a_{2},a_{3},\cdots,a_{n}$ 列), 得到的 $n-1$ 阶子式为

$$
A\begin{bmatrix}1,2,\cdots,n-1\\2,3,\cdots,n\end{bmatrix}
=\left|\begin{array}{cccc}
1&1&\cdots&1\\
a_{2}&a_{3}&\cdots&a_{n}\\
a_{2}^{2}&a_{3}^{2}&\cdots&a_{n}^{2}\\
\vdots&\vdots&&\vdots\\
a_{2}^{n-2}&a_{3}^{n-2}&\cdots&a_{n}^{n-2}
\end{array}\right|.
$$

这是关于 $a_{2},a_{3},\cdots,a_{n}$ 的 $n-1$ 阶范德蒙行列式, 由范德蒙行列式的计算公式, 其值为

$$
\prod_{2\le{i}<{}j\le{n}}\left(a_{j}-a_{i}\right)=\prod_{2\le{i}<{}j\le{n}}\left(j-i\right).
$$

令 $d=j-i$, 则 $d=1,2,\cdots,n-2$, 对于每个 $d$, 有 $n-1-d$ 对 $\left(i,j\right)$ 满足 $j-i=d$.

故

$$
\prod_{2\le{i}<{}j\le{n}}\left(j-i\right)=\prod_{d=1}^{n-2}d^{n-1-d}
=1^{n-2}\cdot2^{n-3}\cdot\cdots\cdot\left(n-2\right)^{1}.
$$

$\blacksquare$

## 3.1-3(1)

在 $K^{4}$ 中, 判断向量 $\beta$ 能否由向量组 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性表出. 若能, 写出它的一种表示方式.

$$
\alpha_{1}=\begin{bmatrix}-1\\3\\0\\-5\end{bmatrix},
\alpha_{2}=\begin{bmatrix}2\\0\\7\\-3\end{bmatrix},
\alpha_{3}=\begin{bmatrix}-4\\1\\-2\\6\end{bmatrix},
\beta=\begin{bmatrix}8\\3\\-1\\-25\end{bmatrix}.
$$

### 解答 3.1-3(1)

由**命题 3.1.1 (线性表出与方程组有解的关系)**, 判断 $\beta$ 能否由 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性表出, 即判断线性方程组 $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=\beta$ 是否有解.

写出增广矩阵, 作初等行变换:

$$
\left[\begin{array}{rrr\left|r}
-1&2&-4&8\\
3&0&1&3\\
0&7&-2&-1\\
-5&-3&6&-25
\end{array}\right]
\xrightarrow{\substack{②+①\times3\\④-①\times5}}
\left[\begin{array}{rrr\right|r}
-1&2&-4&8\\
0&6&-11&27\\
0&7&-2&-1\\
0&-13&26&15
\end{array}\right].
$$

继续作行变换, 最后一行出现矛盾行 $0=80$, 故方程组无解.

由**命题 3.1.1 (线性表出与方程组有解的关系)**, 因此 $\beta$ 不能由 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性表出.

$\blacksquare$

## 3.1-3(3)

在 $K^{4}$ 中, 判断向量 $\beta$ 能否由向量组 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性表出. 若能, 写出它的一种表示方式.

$$
\alpha_{1}=\begin{bmatrix}3\\-5\\2\\-4\end{bmatrix},
\alpha_{2}=\begin{bmatrix}-1\\7\\-3\\6\end{bmatrix},
\alpha_{3}=\begin{bmatrix}3\\11\\-5\\10\end{bmatrix},
\beta=\begin{bmatrix}2\\-30\\13\\-26\end{bmatrix}.
$$

### 解答 3.1-3(3)

由**命题 3.1.1 (线性表出与方程组有解的关系)**, 判断 $\beta$ 能否由 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性表出, 即判断线性方程组 $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=\beta$ 是否有解.

写出增广矩阵, 作初等行变换:

$$
\left[\begin{array}{rrr\left|r}
3&-1&3&2\\
-5&7&11&-30\\
2&-3&-5&13\\
-4&6&10&-26
\end{array}\right]
\xrightarrow{\substack{②+①\times5/3\\③-①\times2/3\\④+①\times4/3}}
\left[\begin{array}{rrr\right|r}
3&-1&3&2\\
0&16/3&16&-80/3\\
0&-7/3&-7&35/3\\
0&14/3&14&-70/3
\end{array}\right].
$$

注意到第 $2,3,4$ 行成比例, 消去后得阶梯形矩阵只有两行:

$$
\left[\begin{array}{rrr|r}
3&-1&3&2\\
0&16/3&16&-80/3
\end{array}\right].
$$

由第 $2$ 行:

$$
\frac{16}{3}x_{2}+16x_{3}=-\frac{80}{3}
$$

即 $x_{2}+3x_{3}=-5$, 故 $x_{2}=-5-3x_{3}$.

由第 $1$ 行: $3x_{1}-x_{2}+3x_{3}=2$, 代入 $x_{2}$ 得 $3x_{1}+6x_{3}=-3$, 故 $x_{1}=-1-2x_{3}$.

令 $x_{3}=0$, 得 $x_{1}=-1$, $x_{2}=-5$.

验证:

$$
-\alpha_{1}-5\alpha_{2}=\begin{bmatrix}-3+5\\5-35\\-2+15\\4-30\end{bmatrix}=\begin{bmatrix}2\\-30\\13\\-26\end{bmatrix}=\beta.
$$

故 $\beta=-\alpha_{1}-5\alpha_{2}$. 由**命题 3.1.1 (线性表出与方程组有解的关系)**, 方程组有解, 故 $\beta$ 可以由 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性表出.

$\blacksquare$

## 3.1-5

在 $K^{4}$ 中, 设

$$
\alpha_{1}=\begin{bmatrix}1\\0\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}1\\1\\1\\0\end{bmatrix},
\alpha_{4}=\begin{bmatrix}1\\1\\1\\1\end{bmatrix}.
$$

证明: $K^{4}$ 中任一向量 $\alpha=\left(a_{1},a_{2},a_{3},a_{4}\right)^{\top}$ 可以由向量组 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 线性表出, 并且表出方式唯一, 写出这种表出方式.

### 解答 3.1-5

由**命题 3.1.1 (线性表出与方程组有解的关系)**, 要证明 $K^{4}$ 中任一向量 $\alpha$ 可以由 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 线性表出, 即证明线性方程组

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}=\alpha
$$

有解.

设

$$
\alpha=x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}.
$$

比较各分量:

第 $4$ 分量: $x_{4}=a_{4}$.

第 $3$ 分量: $x_{3}+x_{4}=a_{3}$, 故 $x_{3}=a_{3}-a_{4}$.

第 $2$ 分量: $x_{2}+x_{3}+x_{4}=a_{2}$, 故 $x_{2}=a_{2}-a_{3}$.

第 $1$ 分量: $x_{1}+x_{2}+x_{3}+x_{4}=a_{1}$, 故 $x_{1}=a_{1}-a_{2}$.

上述求解过程是从下到上唯一确定的, 故表出方式唯一.

表出方式为:

$$
\alpha=\left(a_{1}-a_{2}\right)\alpha_{1}+\left(a_{2}-a_{3}\right)\alpha_{2}+\left(a_{3}-a_{4}\right)\alpha_{3}+a_{4}\alpha_{4}.
$$

方程组有唯一解, 故 $\alpha$ 可以由 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 唯一线性表出.

$\blacksquare$

## 3.1-8

设 $r<{}n$, 证明 $K^{n}$ 的下述子集 $W$ 是一个子空间:

$$
W=\left\{\left(a_{1},a_{2},\cdots,a_{r},0,\cdots,0\right)\mid{a}_{i}\in{K},i=1,2,\cdots,r\right\}.
$$

### 解答 3.1-8

由子空间的判别, 只需验证 $W$ 非空且对加法和数量乘法封闭.

验证加法封闭. 任取

$$
\alpha=\left(a_{1},\cdots,a_{r},0,\cdots,0\right),
\beta=\left(b_{1},\cdots,b_{r},0,\cdots,0\right)\in{W}.
$$

则

$$
\alpha+\beta=\left(a_{1}+b_{1},\cdots,a_{r}+b_{r},0,\cdots,0\right)\in{W}.
$$

验证数量乘法封闭. 任取

$$
\alpha=\left(a_{1},\cdots,a_{r},0,\cdots,0\right)\in{W},
$$

$k\in{K}$.

则

$$
k\alpha=\left(ka_{1},\cdots,ka_{r},0,\cdots,0\right)\in{W}.
$$

$W$ 非空 (例如零向量 $\left(0,\cdots,0\right)\in{W}$).

由子空间的判别, $W$ 是 $K^{n}$ 的一个子空间.

$\blacksquare$
