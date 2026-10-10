# 作业 9

> **定理1** (拉普拉斯定理)<br>在 $n$ 阶行列式 $\left|A\right|$ 中, 取定 $k$ 行, 则这 $k$ 行元素形成的所有 $k$ 阶子式与它们自己的代数余子式的乘积之和等于 $\left|A\right|$.

> **基础知识1** (分块行列式)<br>其中 $A,B$ 都是方阵: <br>$$\left|\begin{array}{cc}A & 0\\C & B\end{array}\right|=\left|A\right|\left|B\right|.$$

### 习题一

(习题 2.6-3) 计算下述行列式:

$$
\left|\begin{array}{cccccc}
0 & \cdots & 0 & a_{11} & \cdots & a_{1k}\\
\vdots & & \vdots & \vdots & & \vdots\\
0 & \cdots & 0 & a_{k1} & \cdots & a_{kk}\\
b_{11} & \cdots & b_{1r} & c_{11} & \cdots & c_{1k}\\
\vdots & & \vdots & \vdots & & \vdots\\
b_{r1} & \cdots & b_{rr} & c_{r1} & \cdots & c_{rk}
\end{array}\right|.
$$

### 解答 习题一

由**定理1** (拉普拉斯定理), 按前 $k$ 行展开. 前 $k$ 行的所有 $k$ 阶子式中, 只有右上角的 $k$ 阶子式 $A=\left(a_{ij}\right)_{k\times k}$ 可能不为零 (因为前 $k$ 行的前 $r$ 列全为 $0$).

右上角的 $k$ 阶子式 $A$ 的代数余子式: 行指标为 $1,2,\cdots,k$, 列指标为 $r+1,r+2,\cdots,r+k$.

由**定理1**, 余子式是去掉前 $k$ 行和后 $k$ 列后的 $r$ 阶行列式, 即 $B=\left(b_{ij}\right)_{r\times r}$.

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

### 习题二

(习题 2.6-4(1)) 设 $\left|A\right|$ 是关于 $1,2,\cdots,n$ 这 $n$ 个数的范德蒙行列式. 计算:

$$
A\begin{bmatrix}1,2,\cdots,n-1\\2,3,\cdots,n\end{bmatrix}.
$$

### 解答 习题二

范德蒙行列式为

$$
\left|A\right|=\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{1} & a_{2} & \cdots & a_{n}\\
a_{1}^{2} & a_{2}^{2} & \cdots & a_{n}^{2}\\
\vdots & \vdots & & \vdots\\
a_{1}^{n-1} & a_{2}^{n-1} & \cdots & a_{n}^{n-1}
\end{array}\right|,
$$

其中 $a_{i}=i$.

取第 $1,2,\cdots,n-1$ 行 (即 $0$ 次幂到 $n-2$ 次幂行) 和第 $2,3,\cdots,n$ 列 (即 $a_{2},a_{3},\cdots,a_{n}$ 列), 得到的 $n-1$ 阶子式为

$$
A\begin{bmatrix}1,2,\cdots,n-1\\2,3,\cdots,n\end{bmatrix}
=\left|\begin{array}{cccc}
1 & 1 & \cdots & 1\\
a_{2} & a_{3} & \cdots & a_{n}\\
a_{2}^{2} & a_{3}^{2} & \cdots & a_{n}^{2}\\
\vdots & \vdots & & \vdots\\
a_{2}^{n-2} & a_{3}^{n-2} & \cdots & a_{n}^{n-2}
\end{array}\right|.
$$

这是关于 $a_{2},a_{3},\cdots,a_{n}$ 的 $n-1$ 阶范德蒙行列式, 其值为

$$
\prod_{2\le i<j\le n}\left(a_{j}-a_{i}\right)=\prod_{2\le i<j\le n}\left(j-i\right).
$$

令 $d=j-i$, 则 $d=1,2,\cdots,n-2$, 对于每个 $d$, 有 $n-1-d$ 对 $\left(i,j\right)$ 满足 $j-i=d$.

故

$$
\prod_{2\le i<j\le n}\left(j-i\right)=\prod_{d=1}^{n-2}d^{n-1-d}
=1^{n-2}\cdot2^{n-3}\cdot\cdots\cdot\left(n-2\right)^{1}.
$$

$\blacksquare$
