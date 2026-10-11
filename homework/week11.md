# 作业 11

> **定义1** (线性相关)<br>$K^{n}$ 中向量组 $\alpha_{1},\cdots,\alpha_{s}$ 称为是线性相关的, 如果有 $K$ 中不全为零的数 $k_{1},\cdots,k_{s}$ 使得 $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$.

> **定义2** (线性无关)<br>$K^{n}$ 中向量组 $\alpha_{1},\cdots,\alpha_{s}$ 如果不是线性相关的, 则称为线性无关的. 即如果从 $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$ 可以推出所有系数全为 $0$, 则称该向量组线性无关.

> **命题1** (线性表出与线性相关的关系)<br>设向量组 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关, 则向量 $\beta$ 可以由 $\alpha_{1},\cdots,\alpha_{s}$ 线性表出的充分必要条件是 $\alpha_{1},\cdots,\alpha_{s},\beta$ 线性相关.

### 习题一

(习题 3.2-2(1)) 判断下列向量组是线性相关还是线性无关. 如果线性相关, 试找出其中一个向量, 使得它可以由其余向量线性表出, 并且写出它的一种表达式.

$$
\alpha_{1}=\begin{bmatrix}3\\1\\2\\-4\end{bmatrix},\ 
\alpha_{2}=\begin{bmatrix}1\\0\\5\\2\end{bmatrix},\ 
\alpha_{3}=\begin{bmatrix}-1\\2\\0\\3\end{bmatrix}.
$$

### 解答 习题一

由**定义1** (线性相关)和**定义2** (线性无关), 考虑齐次线性方程组 $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}=0$. 写出系数矩阵, 作初等行变换:

$$
\left[\begin{array}{rrr}
3 & 1 & -1\\
1 & 0 & 2\\
2 & 5 & 0\\
-4 & 2 & 3
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrr}
1 & 0 & 2\\
0 & 1 & -7\\
0 & 0 & 31\\
0 & 0 & 0
\end{array}\right].
$$

阶梯形矩阵的非零行数目为 $3$, 等于未知量数目 $3$, 故齐次方程组只有零解.

由**定义2**, 因此 $\alpha_{1},\alpha_{2},\alpha_{3}$ 线性无关. $\blacksquare$

### 习题二

(习题 3.2-2(2)) 判断下列向量组是线性相关还是线性无关. 如果线性相关, 试找出其中一个向量, 使得它可以由其余向量线性表出, 并且写出它的一种表达式.

$$
\alpha_{1}=\begin{bmatrix}-2\\1\\0\\3\end{bmatrix},\ 
\alpha_{2}=\begin{bmatrix}1\\-3\\2\\4\end{bmatrix},\ 
\alpha_{3}=\begin{bmatrix}3\\0\\2\\-1\end{bmatrix},\ 
\alpha_{4}=\begin{bmatrix}2\\-2\\4\\6\end{bmatrix}.
$$

### 解答 习题二

由**定义1** (线性相关)和**定义2** (线性无关), 考虑齐次线性方程组 $x_{1}\alpha_{1}+x_{2}\alpha_{2}+x_{3}\alpha_{3}+x_{4}\alpha_{4}=0$. 写出系数矩阵, 作初等行变换:

$$
\left[\begin{array}{rrrr}
-2 & 1 & 3 & 2\\
1 & -3 & 0 & -2\\
0 & 2 & 2 & 4\\
3 & 4 & -1 & 6
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1 & -3 & 0 & -2\\
0 & -5 & 3 & -2\\
0 & 0 & 16/5 & 16/5\\
0 & 0 & 0 & 0
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

验证: $\alpha_{1}+\alpha_{2}+\alpha_{3}=\left(-2+1+3,1-3+0,0+2+2,3+4-1\right)^{T}=\left(2,-2,4,6\right)^{T}=\alpha_{4}$. 由**定义1** (线性相关), 齐次方程组有非零解, 故 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 线性相关. $\blacksquare$

### 习题三

(习题 3.2-6) 设向量组 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 线性无关, 判断向量组 $\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}$ 是否线性无关.

### 解答 习题三

由**定义2** (线性无关), 判断向量组 $\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}$ 是否线性无关, 即判断齐次线性方程组 $k_{1}\left(\alpha_{1}+\alpha_{2}\right)+k_{2}\left(\alpha_{2}+\alpha_{3}\right)+k_{3}\left(\alpha_{3}+\alpha_{4}\right)+k_{4}\left(\alpha_{4}+\alpha_{1}\right)=0$ 是否只有零解.

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
k_{3}+k_{4}=0.
\end{cases}
$$

解得 $k_{2}=-k_{1}$, $k_{3}=k_{1}$, $k_{4}=-k_{1}$, 其中 $k_{1}$ 自由.

令 $k_{1}=1$, 得 $k_{2}=-1$, $k_{3}=1$, $k_{4}=-1$, 这是一组非零解.

故向量组 $\alpha_{1}+\alpha_{2},\alpha_{2}+\alpha_{3},\alpha_{3}+\alpha_{4},\alpha_{4}+\alpha_{1}$ 线性相关.

具体地,

$$
\left(\alpha_{1}+\alpha_{2}\right)-\left(\alpha_{2}+\alpha_{3}\right)+\left(\alpha_{3}+\alpha_{4}\right)-\left(\alpha_{4}+\alpha_{1}\right)=0.
$$

存在不全为零的数 $1,-1,1,-1$ 使得上述等式成立, 故该向量组线性相关. $\blacksquare$

### 习题四

(习题 3.2-7) 证明: 如果向量 $\beta$ 可以由向量组 $\alpha_{1},\cdots,\alpha_{s}$ 线性表出, 则表出方式唯一的充分必要条件是 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关.

### 解答 习题四

由**定义2** (线性无关)和**定义1** (线性相关), 证明表出方式唯一的充分必要条件是 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关.

**充分性**. 设 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关. 假设有两种表出方式:

$$
\beta=k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s},
\beta=l_{1}\alpha_{1}+\cdots+l_{s}\alpha_{s}.
$$

两式相减得

$$
\left(k_{1}-l_{1}\right)\alpha_{1}+\cdots+\left(k_{s}-l_{s}\right)\alpha_{s}=0.
$$

因为 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关, 所以 $k_{i}-l_{i}=0$, 即 $k_{i}=l_{i}$. 表出方式唯一.

**必要性**. 设表出方式唯一. 反证: 假设 $\alpha_{1},\cdots,\alpha_{s}$ 线性相关, 则存在不全为零的数 $c_{1},\cdots,c_{s}$ 使得 $c_{1}\alpha_{1}+\cdots+c_{s}\alpha_{s}=0$.

设 $\beta=k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}$, 则

$$
\beta=\left(k_{1}+c_{1}\right)\alpha_{1}+\cdots+\left(k_{s}+c_{s}\right)\alpha_{s}.
$$

因为 $c_{i}$ 不全为零, 所以 $\left(k_{1}+c_{1},\cdots,k_{s}+c_{s}\right)\ne\left(k_{1},\cdots,k_{s}\right)$, 这与表出方式唯一矛盾.

假设不成立, 故 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关. $\blacksquare$

### 习题五

(习题 3.2-9) 证明: 由非零向量组成的向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ $\left(s\ge2\right)$ 线性无关的充分必要条件是: 每一个 $\alpha_{i}$ $\left(1<i\le s\right)$ 都不能用它前面的向量线性表出.

### 解答 习题五

由**定义2** (线性无关)和**定义1** (线性相关), 证明由非零向量组成的向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ $\left(s\ge2\right)$ 线性无关的充分必要条件是: 每一个 $\alpha_{i}$ $\left(1<i\le s\right)$ 都不能用它前面的向量线性表出.

**必要性**. 设 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关. 反证: 假设某个 $\alpha_{i}$ $\left(i>1\right)$ 可以用前面的向量线性表出, 即 $\alpha_{i}=k_{1}\alpha_{1}+\cdots+k_{i-1}\alpha_{i-1}$.

则

$$
k_{1}\alpha_{1}+\cdots+k_{i-1}\alpha_{i-1}-\alpha_{i}+0\cdot\alpha_{i+1}+\cdots+0\cdot\alpha_{s}=0.
$$

其中系数 $-1\ne0$, 故 $\alpha_{1},\cdots,\alpha_{s}$ 线性相关, 矛盾.

所以每一个 $\alpha_{i}$ $\left(i>1\right)$ 都不能用它前面的向量线性表出.

**充分性**. 设每一个 $\alpha_{i}$ $\left(i>1\right)$ 都不能用它前面的向量线性表出. 反证: 假设 $\alpha_{1},\cdots,\alpha_{s}$ 线性相关, 则存在不全为零的数 $c_{1},\cdots,c_{s}$ 使得 $c_{1}\alpha_{1}+\cdots+c_{s}\alpha_{s}=0$.

设 $c_{i}$ 是最后一个非零系数 $\left(c_{i}\ne0,\ c_{i+1}=\cdots=c_{s}=0\right)$.

若 $i=1$, 则 $c_{1}\alpha_{1}=0$. 因为 $\alpha_{1}\ne0$, 所以 $c_{1}=0$, 矛盾. 故 $i>1$.

由 $c_{1}\alpha_{1}+\cdots+c_{i}\alpha_{i}=0$ 得

$$
\alpha_{i}=-\frac{c_{1}}{c_{i}}\alpha_{1}-\cdots-\frac{c_{i-1}}{c_{i}}\alpha_{i-1}.
$$

这说明 $\alpha_{i}$ 可以用前面的向量线性表出, 与已知条件矛盾.

假设不成立, 故 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关. $\blacksquare$

### 习题六

(习题 3.2-11) 设 $a_{1},a_{2},\cdots,a_{r}$ 是两两不同的数, $r\le n$. 令

$$
\alpha_{1}=\begin{bmatrix}1\\a_{1}\\a_{1}^{2}\\\vdots\\a_{1}^{n-1}\end{bmatrix},\ 
\alpha_{2}=\begin{bmatrix}1\\a_{2}\\a_{2}^{2}\\\vdots\\a_{2}^{n-1}\end{bmatrix},\ \cdots,\ 
\alpha_{r}=\begin{bmatrix}1\\a_{r}\\a_{r}^{2}\\\vdots\\a_{r}^{n-1}\end{bmatrix}.
$$

证明: $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 是线性无关的.

### 解答 习题六

由**定义2** (线性无关), 要证明 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性无关, 即证明齐次线性方程组 $k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{r}\alpha_{r}=0$ 只有零解.

设 $k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{r}\alpha_{r}=0$.

取前 $r$ 个分量, 得齐次线性方程组:

$$
\begin{cases}
k_{1}+k_{2}+\cdots+k_{r}=0,\\
k_{1}a_{1}+k_{2}a_{2}+\cdots+k_{r}a_{r}=0,\\
\cdots\cdots\cdots\cdots\\
k_{1}a_{1}^{r-1}+k_{2}a_{2}^{r-1}+\cdots+k_{r}a_{r}^{r-1}=0.
\end{cases}
$$

其系数行列式为 $r$ 阶范德蒙行列式:

$$
\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{1} & a_{2} & \cdots & a_{r}\\
\vdots & \vdots & & \vdots\\
a_{1}^{r-1} & a_{2}^{r-1} & \cdots & a_{r}^{r-1}
\end{array}\right|=\prod_{1\le i<j\le r}\left(a_{j}-a_{i}\right).
$$

因为 $a_{1},a_{2},\cdots,a_{r}$ 两两不同, 所以行列式不等于 $0$.

故齐次方程组只有零解: $k_{1}=k_{2}=\cdots=k_{r}=0$.

因此 $\alpha_{1},\alpha_{2},\cdots,\alpha_{r}$ 线性无关. $\blacksquare$
