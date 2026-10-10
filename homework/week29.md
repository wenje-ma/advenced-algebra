# 作业 29

> **定义1** (特征值与特征向量)<br>设 $A$ 是数域 $K$ 上的 $n$ 级矩阵, 如果 $K^{n}$ 中有非零列向量 $\alpha$, 使得 $A\alpha=\lambda_{0}\alpha$, 且 $\lambda_{0}\in K$, 则称 $\lambda_{0}$ 是 $A$ 的一个特征值, 称 $\alpha$ 是 $A$ 的属于特征值 $\lambda_{0}$ 的一个特征向量.

> **性质** (相似不变量)<br>相似的矩阵有相同的行列式, 相同的秩, 相同的迹, 相同的特征多项式, 相同的特征值.

### 习题一

(习题 5.5-1(2)) 求下列数域 $K$ 上的矩阵 $A$ 的全部特征值和特征向量:

$$
A=\left[\begin{array}{rrr}
2 & 3 & 2\\
1 & 8 & 2\\
-2 & -14 & -3
\end{array}\right].
$$

### 解答 习题一

由**定义1** (特征值与特征向量), 求特征多项式:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-2 & -3 & -2\\
-1 & \lambda-8 & -2\\
2 & 14 & \lambda+3
\end{array}\right|.
$$

按第 $1$ 行展开:

$$
\begin{aligned}
\left|\lambda I-A\right|
&=\left(\lambda-2\right)\left[\left(\lambda-8\right)\left(\lambda+3\right)+28\right]+3\left[-\left(\lambda+3\right)+4\right]-2\left[-14-2\left(\lambda-8\right)\right]\\
&=\left(\lambda-2\right)\left(\lambda^{2}-5\lambda+4\right)+3\left(-\lambda+1\right)-2\left(2-2\lambda\right)\\
&=\left(\lambda-2\right)\left(\lambda-1\right)\left(\lambda-4\right)-3\lambda+3-4+4\lambda\\
&=\left(\lambda-1\right)\left[\left(\lambda-2\right)\left(\lambda-4\right)+1\right]\\
&=\left(\lambda-1\right)\left(\lambda^{2}-6\lambda+9\right)\\
&=\left(\lambda-1\right)\left(\lambda-3\right)^{2}.
\end{aligned}
$$

因此特征值为 $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=3$.

**求 $\lambda=1$ 的特征向量**.

$$
I-A=\left[\begin{array}{rrr}
-1 & -3 & -2\\
-1 & -7 & -2\\
2 & 14 & 4
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
-1 & -3 & -2\\
0 & -4 & 0\\
0 & 0 & 0
\end{array}\right].
$$

解得 $x_{2}=0$, $x_{1}=-2x_{3}$.

基础解系: $\alpha_{1}=\left(-2,0,1\right)^{T}$.

**求 $\lambda=3$ 的特征向量**.

$$
3I-A=\left[\begin{array}{rrr}
1 & -3 & -2\\
-1 & -5 & -2\\
2 & 14 & 6
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & -3 & -2\\
0 & -8 & -4\\
0 & 0 & 0
\end{array}\right].
$$

解得 $x_{2}=-\frac{1}{2}x_{3}$, $x_{1}=\frac{1}{2}x_{3}$.

基础解系: $\alpha_{2}=\left(1,-1,2\right)^{T}$.

$\lambda_{1}=1$ 的特征向量为 $k_{1}\alpha_{1}$ ( $k_{1}\ne0$ ), $\lambda_{2}=\lambda_{3}=3$ 的特征向量为 $k_{2}\alpha_{2}$ ( $k_{2}\ne0$ ). $\blacksquare$

### 习题二

(习题 5.5-2(2)) 求下列复数域上的矩阵 $A$ 的全部特征值和特征向量; 如果把 $A$ 看成实数域上的矩阵, 它有没有特征值? 有多少个特征值?

$$
A=\left[\begin{array}{rrr}
3 & 7 & -3\\
-2 & -5 & 2\\
-4 & -10 & 3
\end{array}\right].
$$

### 解答 习题二

由**定义1** (特征值与特征向量), 求特征多项式:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-3 & -7 & 3\\
2 & \lambda+5 & -2\\
4 & 10 & \lambda-3
\end{array}\right|.
$$

按第 $1$ 行展开:

$$
\begin{aligned}
\left|\lambda I-A\right|
&=\left(\lambda-3\right)\left[\left(\lambda+5\right)\left(\lambda-3\right)+20\right]+7\left[2\left(\lambda-3\right)+8\right]+3\left[20-4\left(\lambda+5\right)\right]\\
&=\left(\lambda-3\right)\left(\lambda^{2}+2\lambda+5\right)+7\left(2\lambda+2\right)+3\left(-4\lambda\right)\\
&=\lambda^{3}-3\lambda^{2}+2\lambda^{2}-6\lambda+5\lambda-15+14\lambda+14-12\lambda\\
&=\lambda^{3}-\lambda^{2}+\lambda-1\\
&=\left(\lambda-1\right)\left(\lambda^{2}+1\right).
\end{aligned}
$$

因此特征值为 $\lambda_{1}=1$, $\lambda_{2}=i$, $\lambda_{3}=-i$.

由**定义1** (特征值与特征向量), 把 $A$ 看成实数域上的矩阵, 只有 $\lambda=1$ 是实数特征值, 故有 $1$ 个特征值.

$\blacksquare$

### 习题三

(习题 5.5-10) 设 $A$ 是一个 $n$ 级正交矩阵, 证明:

(1) 如果 $A$ 有特征值, 则 $A$ 的特征值是 $1$ 或 $-1$;

(2) 如果 $n$ 是奇数, 且 $\left|A\right|=1$, 则 $1$ 是 $A$ 的一个特征值;

(3) 如果 $\left|A\right|=-1$, 则 $-1$ 是 $A$ 的一个特征值.

### 解答 习题三

**(1)** 设 $\lambda$ 是 $A$ 的一个特征值, $\alpha$ 是 $A$ 的属于 $\lambda$ 的特征向量, 即 $A\alpha=\lambda\alpha$.

两边取共轭转置: $\alpha^{T}A^{T}=\bar{\lambda}\alpha^{T}$.

因为 $A$ 是正交矩阵, 故 $A^{T}=A^{-1}$.

所以 $\alpha^{T}A^{-1}=\bar{\lambda}\alpha^{T}$.

两边右乘 $A\alpha$:

$$
\alpha^{T}A^{-1}A\alpha=\bar{\lambda}\alpha^{T}A\alpha.
$$

即

$$
\alpha^{T}\alpha=\bar{\lambda}\lambda\alpha^{T}\alpha.
$$

因为 $\alpha\ne0$, 故 $\alpha^{T}\alpha\ne0$.

因此

$$
1=\bar{\lambda}\lambda=\left|\lambda\right|^{2}.
$$

所以 $\left|\lambda\right|=1$.

若 $\lambda$ 是实数特征值, 则 $\lambda=\pm1$.

** (2)** $A$ 是 $n$ 级正交矩阵, $n$ 是奇数.

复特征值共轭成对出现, 故复特征值的个数是偶数.

$n$ 是奇数, 故实数特征值的个数是奇数.

实数特征值只能是 $\pm1$.

设 $A$ 有 $k$ 个 $1$, $m$ 个 $-1$, 以及一些复特征值.

$$
\left|A\right|=1^{k}\cdot\left(-1\right)^{m}\cdot\left(\text{复特征值的乘积}\right).
$$

复特征值共轭成对, 每对的乘积是 $\left|\lambda\right|^{2}=1$.

故 $\left|A\right|=\left(-1\right)^{m}$.

已知 $\left|A\right|=1$, 故 $\left(-1\right)^{m}=1$, 即 $m$ 是偶数.

因为 $k+m$ 是奇数 (实数特征值个数), 且 $m$ 是偶数, 故 $k$ 是奇数, 即 $k\ge1$.

因此 $1$ 是 $A$ 的一个特征值.

** (3)** $\left|A\right|=\left(-1\right)^{m}=-1$, 故 $m$ 是奇数, 即 $m\ge1$.

因此 $-1$ 是 $A$ 的一个特征值.

$\blacksquare$

### 习题四

(习题 5.5-12(1)) 求下列复数域上矩阵的全部特征值和特征向量:

$$
P=\left[\begin{array}{ccc}
0 & 1 & 0\\
0 & 0 & 1\\
1 & 0 & 0
\end{array}\right].
$$

### 解答 习题四

求特征多项式:

$$
\left|\lambda I-P\right|=\left|\begin{array}{rrr}
\lambda & -1 & 0\\
0 & \lambda & -1\\
-1 & 0 & \lambda
\end{array}\right|=\lambda^{3}-1.
$$

因此特征值为 $\lambda_{1}=1$, $\lambda_{2}=\omega$, $\lambda_{3}=\omega^{2}$, 其中 $\omega=e^{2\pi i/3}=-\frac{1}{2}+\frac{\sqrt{3}}{2}i$.

**求 $\lambda=1$ 的特征向量**.

$$
I-P=\left[\begin{array}{rrr}
1 & -1 & 0\\
0 & 1 & -1\\
-1 & 0 & 1
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & -1 & 0\\
0 & 1 & -1\\
0 & 0 & 0
\end{array}\right].
$$

解得 $x_{1}=x_{2}=x_{3}$.

基础解系: $\alpha_{1}=\left(1,1,1\right)^{T}$.

**求 $\lambda=\omega$ 的特征向量**.

由第 $1$ 行: $\omega x_{1}-x_{2}=0$, 即 $x_{2}=\omega x_{1}$.

由第 $2$ 行: $\omega x_{2}-x_{3}=0$, 即 $x_{3}=\omega x_{2}=\omega^{2}x_{1}$.

基础解系: $\alpha_{2}=\left(1,\omega,\omega^{2}\right)^{T}$.

**求 $\lambda=\omega^{2}$ 的特征向量**.

同理, 基础解系: $\alpha_{3}=\left(1,\omega^{2},\omega\right)^{T}$.

$\blacksquare$

### 习题五

(习题 5.5-13) 设 $A,B$ 分别是数域 $K$ 上 $s\times n$, $n\times s$ 矩阵, 证明: $AB$ 与 $BA$ 有相同的非零特征值.

### 解答 习题五

设 $\lambda\ne0$ 是 $AB$ 的一个特征值, $\alpha$ 是 $AB$ 的属于 $\lambda$ 的特征向量, 即

$$
AB\alpha=\lambda\alpha.
$$

令 $\beta=B\alpha$.

则

$$
BA\beta=BA\left(B\alpha\right)=B\left(AB\alpha\right)=B\left(\lambda\alpha\right)=\lambda\left(B\alpha\right)=\lambda\beta.
$$

**证明 $\beta\ne0$**.

如果 $\beta=0$, 则 $B\alpha=0$.

那么

$$
AB\alpha=A\left(0\right)=0.
$$

但 $AB\alpha=\lambda\alpha$, 且 $\lambda\ne0$, 故 $\lambda\alpha=0$, 从而 $\alpha=0$.

矛盾, 因为 $\alpha$ 是特征向量, $\alpha\ne0$.

因此 $\beta\ne0$.

所以 $\beta$ 是 $BA$ 的属于 $\lambda$ 的特征向量.

因此 $\lambda$ 是 $BA$ 的一个特征值.

同理可证, $BA$ 的非零特征值也是 $AB$ 的特征值.

因此 $AB$ 与 $BA$ 有相同的非零特征值. $\blacksquare$
