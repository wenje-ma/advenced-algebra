# 作业 15

> **定理1** (线性方程组有解判别定理)<br>线性方程组
> $$
> x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
> $$
> 有解的充分必要条件是: 它的系数矩阵与增广矩阵有相同的秩.

> **定理2** (解的个数判别)<br>设线性方程组有解, 如果系数矩阵的秩等于未知量数目 $n$, 则方程组有唯一解; 如果系数矩阵的秩小于 $n$, 则方程组有无穷多个解.

### 习题一

(习题 3.6-2) 判断下述线性方程组有没有解, 有多少解.

$$
\begin{cases}
x_{1}+ax_{2}+a^{2}x_{3}+\cdots+a^{n-1}x_{n}=b_{1},\\
x_{1}+a^{2}x_{2}+a^{4}x_{3}+\cdots+a^{2\left(n-1\right)}x_{n}=b_{2},\\
\cdots\cdots\cdots\cdots\\
x_{1}+a^{s}x_{2}+a^{2s}x_{3}+\cdots+a^{s\left(n-1\right)}x_{n}=b_{s},
\end{cases}
$$

其中 $s< n$, $a\ne0$ 且当 $0< r< s$ 时, $a^{r}\ne1$.

### 解答 习题一

由**定理1** (线性方程组有解判别定理)和**定理2** (解的个数判别), 需比较系数矩阵与增广矩阵的秩.

系数矩阵 $A$ 是 $s\times n$ 矩阵. 取 $A$ 的前 $s$ 列组成的 $s$ 阶子式:

$$
D=\left|\begin{array}{cccc}
1 & a & a^{2} & \cdots & a^{s-1}\\
1 & a^{2} & a^{4} & \cdots & a^{2\left(s-1\right)}\\
\vdots & \vdots & \vdots & & \vdots\\
1 & a^{s} & a^{2s} & \cdots & a^{s\left(s-1\right)}
\end{array}\right|.
$$

这是范德蒙行列式,

$$
D=\prod_{1\le i< j\le s}\left(a^{j}-a^{i}\right).
$$

因为 $a\ne 0$ 且当 $0< r< s$ 时 $a^{r}\ne 1$, 所以 $a,a^{2},\cdots,a^{s}$ 两两不同, 故 $D\ne 0$.

因此 $\text{rank}\left(A\right)\ge s$.

又 $A$ 只有 $s$ 行, 故 $\text{rank}\left(A\right)\le s$.

所以 $\text{rank}\left(A\right)=s$.

增广矩阵 $\overline{A}$ 是 $A$ 加了一列, 故 $\text{rank}\left(\overline{A}\right)\ge\text{rank}\left(A\right)=s$.

又 $\overline{A}$ 只有 $s$ 行, 故 $\text{rank}\left(\overline{A}\right)\le s$.

所以 $\text{rank}\left(\overline{A}\right)=s=\text{rank}\left(A\right)$.

因此方程组有解.

又 $\text{rank}\left(A\right)=s< n$ (未知量数目), 故方程组有无穷多个解. $\blacksquare$

### 习题二

(习题 3.6-4) 已知线性方程组

$$
\begin{cases}
a_{11}x_{1}+a_{12}x_{2}+\cdots+a_{1n}x_{n}=b_{1},\\
a_{21}x_{1}+a_{22}x_{2}+\cdots+a_{2n}x_{n}=b_{2},\\
\cdots\cdots\cdots\cdots\\
a_{n1}x_{1}+a_{n2}x_{2}+\cdots+a_{nn}x_{n}=b_{n}
\end{cases}
$$

的系数矩阵 $A$ 的秩等于下述矩阵 $B$ 的秩:

$$
B=\left[\begin{array}{ccccc}
a_{11} & a_{12} & \cdots & a_{1n} & b_{1}\\
a_{21} & a_{22} & \cdots & a_{2n} & b_{2}\\
\vdots & \vdots & & \vdots & \vdots\\
a_{n1} & a_{n2} & \cdots & a_{nn} & b_{n}\\
b_{1} & b_{2} & \cdots & b_{n} & 0
\end{array}\right].
$$

证明上述线性方程组有解.

### 解答 习题二

由**定理1** (线性方程组有解判别定理), 要证明线性方程组有解, 即证明系数矩阵 $A$ 与增广矩阵 $\overline{A}$ 有相同的秩.

设增广矩阵为 $\overline{A}$, 即 $\overline{A}=\left[A,b\right]$, 其中 $b=\left(b_{1},b_{2},\cdots,b_{n}\right)^{\top}$.

注意到 $\overline{A}$ 是 $B$ 的前 $n$ 行, 故 $\overline{A}$ 是 $B$ 的子矩阵.

因此 $\text{rank}\left(\overline{A}\right)\le\text{rank}\left(B\right)$.

又 $A$ 是 $\overline{A}$ 的子矩阵, 故 $\text{rank}\left(A\right)\le\text{rank}\left(\overline{A}\right)$.

由题设 $\text{rank}\left(A\right)=\text{rank}\left(B\right)$, 故

$$
\text{rank}\left(A\right)\le\text{rank}\left(\overline{A}\right)\le\text{rank}\left(B\right)=\text{rank}\left(A\right).
$$

因此 $\text{rank}\left(\overline{A}\right)=\text{rank}\left(A\right)$.

该方程组有解. $\blacksquare$
