# 作业 17

> **定理1** (非齐次方程组的解集结构)<br>如果数域 $K$ 上 $n$ 元非齐次线性方程组有解, 则它的解集 $U=\gamma_{0}+W$, 其中 $\gamma_{0}$ 是一个特解, $W$ 是导出组的解空间.

### 习题一

(习题 3.8-1(1)) 求下述数域 $K$ 上非齐次线性方程组的解集:

$$
\begin{cases}
x_{1}-5x_{2}+2x_{3}-3x_{4}=11,\\
-3x_{1}+x_{2}-4x_{3}+2x_{4}=-5,\\
-x_{1}-9x_{2}-4x_{4}=17,\\
5x_{1}+3x_{2}+6x_{3}-x_{4}=-1.
\end{cases}
$$

### 解答 习题一

由**定理1** (非齐次方程组的解集结构), 增广矩阵作初等行变换:

$$
\left[\begin{array}{rrrr\left|r}
1 & -5 & 2 & -3 & 11\\
-3 & 1 & -4 & 2 & -5\\
-1 & -9 & 0 & -4 & 17\\
5 & 3 & 6 & -1 & -1
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr\right|r}
1 & -5 & 2 & -3 & 11\\
0 & -14 & 2 & -7 & 28\\
0 & 0 & 0 & 0 & 0\\
0 & 0 & 0 & 0 & 0
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

令 $x_{3}=x_{4}=0$, 得特解 $\gamma_{0}=\left(1,-2,0,0\right)^{T}$.

导出组的基础解系:

令 $x_{3}=7,x_{4}=0$, 得 $\eta_{1}=\left(-9,1,7,0\right)^{T}$.

令 $x_{3}=0,x_{4}=2$, 得 $\eta_{2}=\left(1,-1,0,2\right)^{T}$.

由**定理1** (非齐次方程组的解集结构), 解集为特解 $\gamma_{0}$ 加上导出组的解空间 $W$:

$$
U=\left\{\gamma_{0}+k_{1}\eta_{1}+k_{2}\eta_{2}\middle|k_{1},k_{2}\in K\right\}.
$$

$\blacksquare$

### 习题二

(习题 3.8-2) 证明: $n$ 个方程的 $n$ 元非齐次线性方程组有唯一解当且仅当它的导出组只有零解.

### 解答 习题二

由**定理1** (非齐次方程组的解集结构), 非齐次方程组的解集 $U=\gamma_{0}+W$, 其中 $W$ 是导出组的解空间. 要证明非齐次方程组有唯一解当且仅当它的导出组只有零解.

设非齐次线性方程组为 $Ax=\beta$, 其中 $A$ 是 $n\times n$ 矩阵; 导出组为 $Ax=0$.

**必要性**. 设非齐次方程组有唯一解, 则

$$
\text{rank}\left(A\right)=\text{rank}\left(\bar{A}\right)=n\ \text{\left(系数矩阵的秩等于未知量数目\right)}.
$$

导出组 $Ax=0$ 的系数矩阵秩为 $n$, 未知量数目为 $n$, 故只有零解.

**充分性**. 设导出组只有零解, 则 $\text{rank}\left(A\right)=n$.

$A$ 是 $n\times n$ 矩阵且 $\text{rank}\left(A\right)=n$, 故 $\left|A\right|\ne0$.

导出组只有零解意味着解空间 $W=\left\{0\right\}$, 故非齐次方程组的解集 $U=\gamma_{0}+W=\left\{\gamma_{0}\right\}$, 即有唯一解. $\blacksquare$

### 习题三

(习题 3.8-4) 证明: 如果 $\gamma_{0}$ 是非齐次线性方程组 (1) 的一个特解, $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 是它的导出组的一个基础解系. 令

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

### 解答 习题三

由**定理1** (非齐次方程组的解集结构), 非齐次方程组的解集 $U=\gamma_{0}+W$, 其中 $W$ 是导出组的解空间.

非齐次方程组的解集 $U=\gamma_{0}+W$, 其中 $W$ 是导出组的解空间.

任取 $\gamma\in U$, 则 $\gamma-\gamma_{0}\in W$.

因为 $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 是 $W$ 的一个基, 所以存在 $k_{1},\cdots,k_{t}\in K$ 使得

$$
\gamma-\gamma_{0}=k_{1}\eta_{1}+k_{2}\eta_{2}+\cdots+k_{t}\eta_{t}.
$$

将 $\eta_{i}=\gamma_{i}-\gamma_{0}$ 代入:

$$
\gamma =\gamma_{0}+k_{1}\left(\gamma_{1}-\gamma_{0}\right)+k_{2}\left(\gamma_{2}-\gamma_{0}\right)+\cdots+k_{t}\left(\gamma_{t}-\gamma_{0}\right)=\left(1-k_{1}-k_{2}-\cdots-k_{t}\right)\gamma_{0}+k_{1}\gamma_{1}+k_{2}\gamma_{2}+\cdots+k_{t}\gamma_{t}.
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
\gamma=u_{0}\gamma_{0}+u_{1}\gamma_{1}+u_{2}\gamma_{2}+\cdots+u_{t}\gamma_{t},\
u_{0}+u_{1}+u_{2}+\cdots+u_{t}=1.
$$

$\blacksquare$
