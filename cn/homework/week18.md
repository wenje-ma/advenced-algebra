# 作业 18

> **定义1** (矩阵的加法)<br>设 $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ 都是数域 $K$ 上 $s\times n$ 矩阵, 令 $C=\left(a_{ij}+b_{ij}\right)_{s\times n}$, 则称 $C$ 是矩阵 $A$ 与 $B$ 的和, 记作 $C=A+B$.

> **定义2** (矩阵的数量乘法)<br>设 $k\in K$, 令 $M=\left(ka_{ij}\right)_{s\times n}$, 则称 $M$ 是 $k$ 与矩阵 $A$ 的数量乘积, 记作 $M=kA$.

> **定义3** (矩阵的乘法)<br>设 $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$, 令 $C=\left(c_{ij}\right)_{s\times m}$, 其中 $c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}$, 则称 $C$ 是 $A$ 与 $B$ 的乘积, 记作 $C=AB$.

### 习题一

(习题 4.1-1) 设

$$
A=\left[\begin{array}{ccc}
\lambda & 0 & 0\\
0 & \lambda & 0\\
0 & 0 & \lambda
\end{array}\right],
B=\left[\begin{array}{ccc}
0 & 1 & 0\\
0 & 0 & 1\\
0 & 0 & 0
\end{array}\right].
$$

求 $A+B$.

### 解答 习题一

由**定义1** (矩阵的加法),

$$
A+B=\left[\begin{array}{ccc}
\lambda & 1 & 0\\
0 & \lambda & 1\\
0 & 0 & \lambda
\end{array}\right].
$$

$\blacksquare$

### 习题二

(习题 4.1-3) 设 $I$ 是 $n$ 级单位矩阵, $J$ 是元素全为 $1$ 的 $n$ 级矩阵. 设

$$
M=\left[\begin{array}{cccc}
k & \lambda & \cdots & \lambda\\
\lambda & k & \cdots & \lambda\\
\vdots & \vdots & & \vdots\\
\lambda & \lambda & \cdots & k
\end{array}\right]_{n\times n}.
$$

把 $M$ 表示成 $xI+yJ$ 的形式, 其中 $x,y$ 是待定系数.

### 解答 习题二

由**定义1** (矩阵的加法)和**定义2** (矩阵的数量乘法), $xI+yJ$ 的主对角元为 $x+y$, 其余元素为 $y$.

对比 $M$ 的主对角元为 $k$, 其余元素为 $\lambda$, 得

$$
\begin{cases}
x+y=k,\\
y=\lambda.
\end{cases}
$$

解得 $x=k-\lambda$, $y=\lambda$.

由**定义1** (矩阵的加法)和**定义2** (矩阵的数量乘法), 故

$$
M=\left(k-\lambda\right)I+\lambda J.
$$

$\blacksquare$

### 习题三

(习题 4.1-4(1)) 计算:

$$
\left[\begin{array}{rr}
7 & -1\\
-2 & 5\\
3 & -4
\end{array}\right]\left[\begin{array}{rr}
1 & 4\\
-5 & 2
\end{array}\right].
$$

### 解答 习题三

由**定义3** (矩阵的乘法), 矩阵乘积的第 $\left(i,j\right)$ 元等于第 $i$ 行与第 $j$ 列的内积:

$$
\left[\begin{array}{rr}
7 & -1\\
-2 & 5\\
3 & -4
\end{array}\right]\left[\begin{array}{rr}
1 & 4\\
-5 & 2
\end{array}\right]
=
\left[\begin{array}{rr}
7\times1+\left(-1\right)\times\left(-5\right) & 7\times4+\left(-1\right)\times2\\
\left(-2\right)\times1+5\times\left(-5\right) & \left(-2\right)\times4+5\times2\\
3\times1+\left(-4\right)\times\left(-5\right) & 3\times4+\left(-4\right)\times2
\end{array}\right]
=
\left[\begin{array}{rr}
12 & 26\\
-27 & 2\\
23 & 4
\end{array}\right].
$$

$\blacksquare$

### 习题四

(习题 4.1-4(2)) 计算:

$$
\left[\begin{array}{rr}
0 & 2\\
0 & 3
\end{array}\right]\left[\begin{array}{rr}
1 & 1\\
0 & 0
\end{array}\right].
$$

### 解答 习题四

由**定义3** (矩阵的乘法), 矩阵乘积的第 $\left(i,j\right)$ 元等于第 $i$ 行与第 $j$ 列的内积:

$$
\left[\begin{array}{rr}
0 & 2\\
0 & 3
\end{array}\right]\left[\begin{array}{rr}
1 & 1\\
0 & 0
\end{array}\right]
=
\left[\begin{array}{rr}
0\times1+2\times0 & 0\times1+2\times0\\
0\times1+3\times0 & 0\times1+3\times0
\end{array}\right]
=
\left[\begin{array}{rr}
0 & 0\\
0 & 0
\end{array}\right].
$$

$\blacksquare$

### 习题五

(习题 4.1-4(3)) 计算:

$$
\left[\begin{array}{rr}
1 & 1\\
0 & 0
\end{array}\right]\left[\begin{array}{rr}
0 & 2\\
0 & 3
\end{array}\right].
$$

### 解答 习题五

由**定义3** (矩阵的乘法), 矩阵乘积的第 $\left(i,j\right)$ 元等于第 $i$ 行与第 $j$ 列的内积:

$$
\left[\begin{array}{rr}
1 & 1\\
0 & 0
\end{array}\right]\left[\begin{array}{rr}
0 & 2\\
0 & 3
\end{array}\right]
=
\left[\begin{array}{rr}
1\times0+1\times0 & 1\times2+1\times3\\
0\times0+0\times0 & 0\times2+0\times3
\end{array}\right]
=
\left[\begin{array}{rr}
0 & 5\\
0 & 0
\end{array}\right].
$$

$\blacksquare$

### 习题六

(习题 4.1-4(8)) 计算:

$$
\left[\begin{array}{ccc}
d_{1} & 0 & 0\\
0 & d_{2} & 0\\
0 & 0 & d_{3}
\end{array}\right]\left[\begin{array}{ccc}
a_{1} & a_{2} & a_{3}\\
b_{1} & b_{2} & b_{3}\\
c_{1} & c_{2} & c_{3}
\end{array}\right].
$$

### 解答 习题六

由**定义3** (矩阵的乘法), 用对角矩阵左乘, 相当于用对角元分别乘相应的行:

$$
=
\left[\begin{array}{ccc}
d_{1}a_{1} & d_{1}a_{2} & d_{1}a_{3}\\
d_{2}b_{1} & d_{2}b_{2} & d_{2}b_{3}\\
d_{3}c_{1} & d_{3}c_{2} & d_{3}c_{3}
\end{array}\right].
$$

$\blacksquare$

### 习题七

(习题 4.1-4(9)) 计算:

$$
\left[\begin{array}{ccc}
a_{1} & a_{2} & a_{3}\\
b_{1} & b_{2} & b_{3}\\
c_{1} & c_{2} & c_{3}
\end{array}\right]\left[\begin{array}{ccc}
d_{1} & 0 & 0\\
0 & d_{2} & 0\\
0 & 0 & d_{3}
\end{array}\right].
$$

### 解答 习题七

由**定义3** (矩阵的乘法), 用对角矩阵右乘, 相当于用对角元分别乘相应的列:

$$
=
\left[\begin{array}{ccc}
d_{1}a_{1} & d_{2}a_{2} & d_{3}a_{3}\\
d_{1}b_{1} & d_{2}b_{2} & d_{3}b_{3}\\
d_{1}c_{1} & d_{2}c_{2} & d_{3}c_{3}
\end{array}\right].
$$

$\blacksquare$

### 习题八

(习题 4.1-4(13)) 计算:

$$
\left[\begin{array}{ccc}
0 & 1 & 0\\
1 & 0 & 0\\
0 & 0 & 1
\end{array}\right]\left[\begin{array}{cccc}
a_{1} & a_{2} & a_{3} & a_{4}\\
b_{1} & b_{2} & b_{3} & b_{4}\\
c_{1} & c_{2} & c_{3} & c_{4}
\end{array}\right].
$$

### 解答 习题八

由**定义3** (矩阵的乘法), 这是交换第 $1$ 行和第 $2$ 行的初等矩阵左乘:

$$
=
\left[\begin{array}{cccc}
b_{1} & b_{2} & b_{3} & b_{4}\\
a_{1} & a_{2} & a_{3} & a_{4}\\
c_{1} & c_{2} & c_{3} & c_{4}
\end{array}\right].
$$

$\blacksquare$

### 习题九

(习题 4.1-4(14)) 计算:

$$
\left[\begin{array}{ccc}
a_{1} & a_{2} & a_{3}\\
b_{1} & b_{2} & b_{3}\\
c_{1} & c_{2} & c_{3}
\end{array}\right]\left[\begin{array}{ccc}
0 & 1 & 0\\
1 & 0 & 0\\
0 & 0 & 1
\end{array}\right].
$$

### 解答 习题九

由**定义3** (矩阵的乘法), 这是交换第 $1$ 列和第 $2$ 列的初等矩阵右乘:

$$
=
\left[\begin{array}{ccc}
a_{2} & a_{1} & a_{3}\\
b_{2} & b_{1} & b_{3}\\
c_{2} & c_{1} & c_{3}
\end{array}\right].
$$

$\blacksquare$

### 习题十

(习题 4.1-6) 计算:

$$
\left(x,y,1\right)\left[\begin{array}{ccc}
a_{11} & a_{12} & a_{1}\\
a_{12} & a_{22} & a_{2}\\
a_{1} & a_{2} & a_{0}
\end{array}\right]\left[\begin{array}{c}
x\\
y\\
1
\end{array}\right].
$$

### 解答 习题十

由**定义3** (矩阵的乘法), 先算右边的行向量乘矩阵:

$$
\left(x,y,1\right)M
=
\left(a_{11}x+a_{12}y+a_{1},a_{12}x+a_{22}y+a_{2},a_{1}x+a_{2}y+a_{0}\right).
$$

再乘列向量:

$$
=\left(a_{11}x+a_{12}y+a_{1}\right)x+\left(a_{12}x+a_{22}y+a_{2}\right)y+\left(a_{1}x+a_{2}y+a_{0}\right)=a_{11}x^{2}+a_{12}xy+a_{1}x+a_{12}xy+a_{22}y^{2}+a_{2}y+a_{1}x+a_{2}y+a_{0}=a_{11}x^{2}+2a_{12}xy+a_{22}y^{2}+2a_{1}x+2a_{2}y+a_{0}.
$$

$\blacksquare$

### 习题十一

(习题 4.1-7(5)) 计算:

$$
\left[\begin{array}{ccc}
0 & 1 & 0\\
0 & 0 & 1\\
0 & 0 & 0
\end{array}\right]^{n},n\text{ 是正整数}.
$$

### 解答 习题十一

由**定义3** (矩阵的乘法), 记

$$
H=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right]
$$

$$
H^{2}=HH=\left[\begin{array}{ccc}
0 & 0 & 1\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

$$
H^{3}=H^{2}H=\left[\begin{array}{ccc}
0 & 0 & 0\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

因此:

- 当 $n=1$ 时, $H^{n}=H=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right]$.
- 当 $n=2$ 时, $H^{n}=\left[\begin{array}{ccc}0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]$.
- 当 $n\ge3$ 时, $H^{n}=0$.

$\blacksquare$

### 习题十二

(习题 4.1-7(6)) 计算:

$$
\left[\begin{array}{ccc}
\lambda & 1 & 0\\
0 & \lambda & 1\\
0 & 0 & \lambda
\end{array}\right]^{n},n\text{ 是正整数}.
$$

### 解答 习题十二

由**定义3** (矩阵的乘法), 记 $A=\lambda I+N$, 其中

$$
N=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right]
$$

因为 $\lambda I$ 与 $N$ 可交换, 由二项式定理:

$$
A^{n}=\sum_{k=0}^{n}\binom{n}{k}\left(\lambda I\right)^{n-k}N^{k}.
$$

又 $N^{0}=I$, $N^{1}=N$, $N^{2}=\left[\begin{array}{ccc}0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]$, $N^{3}=0$.

故当 $n\ge2$ 时,

$$
A^{n}
=\lambda^{n}I+n\lambda^{n-1}N+\binom{n}{2}\lambda^{n-2}N^{2}=\left[\begin{array}{ccc}
\lambda^{n} & n\lambda^{n-1} & n\left(n-1\right)/2 \cdot \lambda^{n-2}\\
0 & \lambda^{n} & n\lambda^{n-1}\\
0 & 0 & \lambda^{n}
\end{array}\right].
$$

当 $n=1$ 时, 上式也成立 (注意 $\lambda^{0}=1$, 第三项为 $0$). $\blacksquare$

### 习题十三

(习题 4.1-10) 证明: 如果 $A=\frac{1}{2}\left(B+I\right)$, 则 $A^{2}=A$ 当且仅当 $B^{2}=I$.

### 解答 习题十三

$$
A^{2}=\left(\frac{1}{2}\left(B+I\right)\right)^{2}=\frac{1}{4}\left(B+I\right)^{2}=\frac{1}{4}\left(B^{2}+2B+I\right).
$$

$A^{2}=A$ 等价于:

$$
\frac{1}{4}\left(B^{2}+2B+I\right)=\frac{1}{2}\left(B+I\right).
$$

两边乘 $4$:

$$
B^{2}+2B+I=2B+2I.
$$

化简得:

$$
B^{2}=I.
$$

因此 $A^{2}=A$ 当且仅当 $B^{2}=I$. $\blacksquare$
