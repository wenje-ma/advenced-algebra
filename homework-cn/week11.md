# week11

> **定理 3.8.1 (非齐次方程组的解集结构)**
> 
> 如果数域 $K$ 上 $n$ 元非齐次线性方程组有解, 则它的解集 $U=\gamma_{0}+W$, 其中 $\gamma_{0}$ 是一个特解, $W$ 是导出组的解空间.

> **定义 4.1.1 (矩阵的加法)**
> 
> 设 $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ 都是数域 $K$ 上 $s\times{n}$ 矩阵, 令 $C=\left(a_{ij}+b_{ij}\right)_{s\times{n}}$, 则称 $C$ 是矩阵 $A$ 与 $B$ 的和, 记作 $C=A+B$.

> **定义 4.1.2 (矩阵的数量乘法)**
> 
> 设 $k\in{K}$, 令 $M=\left(ka_{ij}\right)_{s\times{n}}$, 则称 $M$ 是 $k$ 与矩阵 $A$ 的数量乘积, 记作 $M=kA$.

> **定义 4.1.3 (矩阵的乘法)**
> 
> 设 $A=\left(a_{ij}\right)_{s\times{n}}$, $B=\left(b_{ij}\right)_{n\times{m}}$, 令 $C=\left(c_{ij}\right)_{s\times{m}}$, 其中 $c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}$, 则称 $C$ 是 $A$ 与 $B$ 的乘积, 记作 $C=AB$.

## 3.8-2

证明: $n$ 个方程的 $n$ 元非齐次线性方程组有唯一解当且仅当它的导出组只有零解.

### 解答 3.8-2

由**定理 3.8.1 (非齐次方程组的解集结构)**, 非齐次方程组的解集 $U=\gamma_{0}+W$, 其中 $W$ 是导出组的解空间. 要证明非齐次方程组有唯一解当且仅当它的导出组只有零解.

设非齐次线性方程组为 $Ax=\beta$, 其中 $A$ 是 $n\times{n}$ 矩阵; 导出组为 $Ax=0$.

必要性. 设非齐次方程组有唯一解, 则

$$
\text{rank}\left(A\right)=\text{rank}\left(\overline{A}\right)=n\;\text{(系数矩阵的秩等于未知量数目)}.
$$

导出组 $Ax=0$ 的系数矩阵秩为 $n$, 未知量数目为 $n$, 故只有零解.

充分性. 设导出组只有零解, 则 $\text{rank}\left(A\right)=n$.

$A$ 是 $n\times{n}$ 矩阵且 $\text{rank}\left(A\right)=n$, 故 $\left|A\right|\ne0$.

导出组只有零解意味着解空间 $W=\left\{0\right\}$, 故非齐次方程组的解集 $U=\gamma_{0}+W=\left\{\gamma_{0}\right\}$, 即有唯一解. $\blacksquare$

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

任取 $\gamma\in{U}$, 则 $\gamma-\gamma_{0}\in{W}$.

因为 $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 是 $W$ 的一个基, 所以存在 $k_{1},\cdots,k_{t}\in{K}$ 使得

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
\end{array}\right]_{n\times{n}}.
$$

把 $M$ 表示成 $xI+yJ$ 的形式, 其中 $x,y$ 是待定系数.

### 解答 4.1-3

由**定义 4.1.1 (矩阵的加法)**和**定义 4.1.2 (矩阵的数量乘法)**, $xI+yJ$ 的主对角元为 $x+y$, 其余元素为 $y$.

对比 $M$ 的主对角元为 $k$, 其余元素为 $\lambda$, 得

$$
\begin{cases}
x+y=k,\\
y=\lambda.
\end{cases}
$$

解得 $x=k-\lambda$, $y=\lambda$.

由**定义 4.1.1 (矩阵的加法)**和**定义 4.1.2 (矩阵的数量乘法)**, 故

$$
M=\left(k-\lambda\right)I+\lambda{J}.
$$

$\blacksquare$

## 4.1-4(1)

计算:

$$
\left[\begin{array}{rr}
7&-1\\
-2&5\\
3&-4
\end{array}\right]\left[\begin{array}{rr}
1&4\\
-5&2
\end{array}\right].
$$

### 解答 4.1-4(1)

由**定义 4.1.3 (矩阵的乘法)**, 矩阵乘积的第 $\left(i,j\right)$ 元等于第 $i$ 行与第 $j$ 列的内积:

$$
\left[\begin{array}{rr}
7&-1\\
-2&5\\
3&-4
\end{array}\right]\left[\begin{array}{rr}
1&4\\
-5&2
\end{array}\right]
=
\left[\begin{array}{rr}
7\times1+\left(-1\right)\times\left(-5\right)&7\times4+\left(-1\right)\times2\\
\left(-2\right)\times1+5\times\left(-5\right)&\left(-2\right)\times4+5\times2\\
3\times1+\left(-4\right)\times\left(-5\right)&3\times4+\left(-4\right)\times2
\end{array}\right]
=
\left[\begin{array}{rr}
12&26\\
-27&2\\
23&4
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(2)

计算:

$$
\left[\begin{array}{rr}
0&2\\
0&3
\end{array}\right]\left[\begin{array}{rr}
1&1\\
0&0
\end{array}\right].
$$

### 解答 4.1-4(2)

由**定义 4.1.3 (矩阵的乘法)**, 矩阵乘积的第 $\left(i,j\right)$ 元等于第 $i$ 行与第 $j$ 列的内积:

$$
\left[\begin{array}{rr}
0&2\\
0&3
\end{array}\right]\left[\begin{array}{rr}
1&1\\
0&0
\end{array}\right]
=
\left[\begin{array}{rr}
0\times1+2\times0&0\times1+2\times0\\
0\times1+3\times0&0\times1+3\times0
\end{array}\right]
=
\left[\begin{array}{rr}
0&0\\
0&0
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(3)

计算:

$$
\left[\begin{array}{rr}
1&1\\
0&0
\end{array}\right]\left[\begin{array}{rr}
0&2\\
0&3
\end{array}\right].
$$

### 解答 4.1-4(3)

由**定义 4.1.3 (矩阵的乘法)**, 矩阵乘积的第 $\left(i,j\right)$ 元等于第 $i$ 行与第 $j$ 列的内积:

$$
\left[\begin{array}{rr}
1&1\\
0&0
\end{array}\right]\left[\begin{array}{rr}
0&2\\
0&3
\end{array}\right]
=
\left[\begin{array}{rr}
1\times0+1\times0&1\times2+1\times3\\
0\times0+0\times0&0\times2+0\times3
\end{array}\right]
=
\left[\begin{array}{rr}
0&5\\
0&0
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(8)

计算:

$$
\left[\begin{array}{ccc}
d_{1}&0&0\\
0&d_{2}&0\\
0&0&d_{3}
\end{array}\right]\left[\begin{array}{ccc}
a_{1}&a_{2}&a_{3}\\
b_{1}&b_{2}&b_{3}\\
c_{1}&c_{2}&c_{3}
\end{array}\right].
$$

### 解答 4.1-4(8)

由**定义 4.1.3 (矩阵的乘法)**, 用对角矩阵左乘, 相当于用对角元分别乘相应的行:

$$
=
\left[\begin{array}{ccc}
d_{1}a_{1}&d_{1}a_{2}&d_{1}a_{3}\\
d_{2}b_{1}&d_{2}b_{2}&d_{2}b_{3}\\
d_{3}c_{1}&d_{3}c_{2}&d_{3}c_{3}
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(9)

计算:

$$
\left[\begin{array}{ccc}
a_{1}&a_{2}&a_{3}\\
b_{1}&b_{2}&b_{3}\\
c_{1}&c_{2}&c_{3}
\end{array}\right]\left[\begin{array}{ccc}
d_{1}&0&0\\
0&d_{2}&0\\
0&0&d_{3}
\end{array}\right].
$$

### 解答 4.1-4(9)

由**定义 4.1.3 (矩阵的乘法)**, 用对角矩阵右乘, 相当于用对角元分别乘相应的列:

$$
=
\left[\begin{array}{ccc}
d_{1}a_{1}&d_{2}a_{2}&d_{3}a_{3}\\
d_{1}b_{1}&d_{2}b_{2}&d_{3}b_{3}\\
d_{1}c_{1}&d_{2}c_{2}&d_{3}c_{3}
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(13)

计算:

$$
\left[\begin{array}{ccc}
0&1&0\\
1&0&0\\
0&0&1
\end{array}\right]\left[\begin{array}{cccc}
a_{1}&a_{2}&a_{3}&a_{4}\\
b_{1}&b_{2}&b_{3}&b_{4}\\
c_{1}&c_{2}&c_{3}&c_{4}
\end{array}\right].
$$

### 解答 4.1-4(13)

由**定义 4.1.3 (矩阵的乘法)**, 这是交换第 $1$ 行和第 $2$ 行的初等矩阵左乘:

$$
=
\left[\begin{array}{cccc}
b_{1}&b_{2}&b_{3}&b_{4}\\
a_{1}&a_{2}&a_{3}&a_{4}\\
c_{1}&c_{2}&c_{3}&c_{4}
\end{array}\right].
$$

$\blacksquare$

## 4.1-4(14)

计算:

$$
\left[\begin{array}{ccc}
a_{1}&a_{2}&a_{3}\\
b_{1}&b_{2}&b_{3}\\
c_{1}&c_{2}&c_{3}
\end{array}\right]\left[\begin{array}{ccc}
0&1&0\\
1&0&0\\
0&0&1
\end{array}\right].
$$

### 解答 4.1-4(14)

由**定义 4.1.3 (矩阵的乘法)**, 这是交换第 $1$ 列和第 $2$ 列的初等矩阵右乘:

$$
=
\left[\begin{array}{ccc}
a_{2}&a_{1}&a_{3}\\
b_{2}&b_{1}&b_{3}\\
c_{2}&c_{1}&c_{3}
\end{array}\right].
$$

$\blacksquare$
