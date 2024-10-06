# week6

> **定理 2.6.1 (拉普拉斯定理)**
> 
> 在 $n$ 阶行列式 $\left|A\right|$ 中, 取定 $k$ 行, 则这 $k$ 行元素形成的所有 $k$ 阶子式与它们自己的代数余子式的乘积之和等于 $\left|A\right|$.

> **命题 3.1.1 (线性表出与方程组有解的关系)**
> 
> 数域 $K$ 上 $n$ 元线性方程组 $x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta$ 有解 $\Leftrightarrow$ $\beta$ 可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 线性表出 $\Leftrightarrow$ $\beta\in\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\right\rangle$.

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

## 3.2-2(1)

判断下列向量组是线性相关还是线性无关. 如果线性相关, 试找出其中一个向量, 使得它可以由其余向量线性表出, 并且写出它的一种表达式.

$$
\alpha_{1}=\begin{bmatrix}3\\1\\2\\-4\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\0\\5\\2\end{bmatrix},
\alpha_{3}=\begin{bmatrix}-1\\2\\0\\3\end{bmatrix}.
$$

### 解答 3.2-2(1)

由**定义 3.2.1 (线性相关)**和**定义 3.2.2 (线性无关)**, 考虑齐次线性方程组 $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=0$. 写出系数矩阵, 作初等行变换:

$$
\left[\begin{array}{rrr}
3&1&-1\\
1&0&2\\
2&5&0\\
-4&2&3
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrr}
1&0&2\\
0&1&-7\\
0&0&31\\
0&0&0
\end{array}\right].
$$

阶梯形矩阵的非零行数目为 $3$, 等于未知量数目 $3$, 故齐次方程组只有零解.

由**定义 3.2.2 (线性无关)**, 因此 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性无关.

$\blacksquare$

## 3.2-2(2)

判断下列向量组是线性相关还是线性无关. 如果线性相关, 试找出其中一个向量, 使得它可以由其余向量线性表出, 并且写出它的一种表达式.

$$
\alpha_{1}=\begin{bmatrix}-2\\1\\0\\3\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\-3\\2\\4\end{bmatrix},
\alpha_{3}=\begin{bmatrix}3\\0\\2\\-1\end{bmatrix},
\alpha_{4}=\begin{bmatrix}2\\-2\\4\\6\end{bmatrix}.
$$

### 解答 3.2-2(2)

由**定义 3.2.1 (线性相关)**和**定义 3.2.2 (线性无关)**, 考虑齐次线性方程组

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}=0.
$$

写出系数矩阵, 作初等行变换:

$$
\left[\begin{array}{rrrr}
-2&1&3&2\\
1&-3&0&-2\\
0&2&2&4\\
3&4&-1&6
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1&-3&0&-2\\
0&-5&3&-2\\
0&0&16/5&16/5\\
0&0&0&0
\end{array}\right].
$$

阶梯形矩阵的非零行数目为 $3$, 小于未知量数目 $4$, 故齐次方程组有非零解.

因此 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 线性相关.

求解一般解:

由第 $3$ 行: $x_{3}+x_{4}=0$, 故 $x_{3}=-x_{4}$.

由第 $2$ 行: $-5x_{2}+3x_{3}-2x_{4}=0$, 代入 $x_{3}=-x_{4}$ 得 $x_{2}=-x_{4}$.

由第 $1$ 行: $x_{1}-3x_{2}-2x_{4}=0$, 代入 $x_{2}=-x_{4}$ 得 $x_{1}=-x_{4}$.

令 $x_{4}=1$, 得 $x_{1}=-1$, $x_{2}=-1$, $x_{3}=-1$.

故 $-\alpha_{1}-\alpha_{2}-\alpha_{3}+\alpha_{4}=0$, 即

$$
\alpha_{4}=\alpha_{1}+\alpha_{2}+\alpha_{3}.
$$

验证:

$$
\alpha_{1}+\alpha_{2}+\alpha_{3}=\left(-2+1+3,1-3+0,0+2+2,3+4-1\right)^{\top}=\left(2,-2,4,6\right)^{\top}=\alpha_{4}.
$$

由**定义 3.2.1 (线性相关)**, 齐次方程组有非零解, 故 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 线性相关.

$\blacksquare$
