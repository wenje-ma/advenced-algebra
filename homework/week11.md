# week11

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

## 4.1-7(5)

计算:

$$
\left[\begin{array}{ccc}
0&1&0\\
0&0&1\\
0&0&0
\end{array}\right]^{n},n\text{~是正整数}.
$$

### 解答 4.1-7(5)

由**定义 4.1.3 (矩阵的乘法)**, 记

$$
H=\left[\begin{array}{ccc}0&1&0\\0&0&1\\0&0&0\end{array}\right].
$$

$$
H^{2}=HH=\left[\begin{array}{ccc}
0&0&1\\
0&0&0\\
0&0&0
\end{array}\right].
$$

$$
H^{3}=H^{2}H=\left[\begin{array}{ccc}
0&0&0\\
0&0&0\\
0&0&0
\end{array}\right].
$$

因此:

- 当 $n=1$ 时, $H^{n}=H=\left[\begin{array}{ccc}0&1&0\\0&0&1\\0&0&0\end{array}\right]$.
- 当 $n=2$ 时, $H^{n}=\left[\begin{array}{ccc}0&0&1\\0&0&0\\0&0&0\end{array}\right]$.
- 当 $n\ge3$ 时, $H^{n}=0$.

$\blacksquare$
