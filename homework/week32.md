# 作业 32

> **定义1** (二次型)<br>系数在数域 $K$ 中的 $n$ 个变量 $x_{1},x_{2},\cdots,x_{n}$ 的一个二次齐次多项式, 称为数域 $K$ 上的一个 $n$ 元二次型.

> **定理3** (二次型的标准形)<br>数域 $K$ 上任意一个二次型都等价于一个只含平方项的二次型.

> **定义1** (规范形)<br>实二次型 $X^{T}AX$ 的规范形为
> $$
> z_{1}^{2}+\cdots+z_{p}^{2}-z_{p+1}^{2}-\cdots-z_{r}^{2},
> $$
> 其中 $p$ 是正惯性指数, $r$ 是二次型的秩.

### 习题一

(习题 6.1-3(1)) 作非退化线性替换把下列数域 $K$ 上二次型化成标准形, 并且写出所作的非退化线性替换:

$$
f\left(x_{1},x_{2},x_{3}\right)=x_{1}^{2}+2x_{2}^{2}+2x_{1}x_{2}-2x_{1}x_{3}.
$$

### 解答 习题一

由**定理3** (二次型的标准形), 用配方法:

$$
\begin{aligned}f
&=x_{1}^{2}+2x_{1}x_{2}-2x_{1}x_{3}+2x_{2}^{2}\\
&=\left(x_{1}+x_{2}-x_{3}\right)^{2}-\left(x_{2}-x_{3}\right)^{2}+2x_{2}^{2}\\
&=\left(x_{1}+x_{2}-x_{3}\right)^{2}+x_{2}^{2}+2x_{2}x_{3}-x_{3}^{2}\\
&=\left(x_{1}+x_{2}-x_{3}\right)^{2}+\left(x_{2}+x_{3}\right)^{2}-2x_{3}^{2}.
\end{aligned}
$$

令

$$
\begin{cases}
y_{1}=x_{1}+x_{2}-x_{3},\\
y_{2}=x_{2}+x_{3},\\
y_{3}=x_{3}.
\end{cases}
$$

则

$$
\begin{cases}
x_{1}=y_{1}-y_{2}+2y_{3},\\
x_{2}=y_{2}-y_{3},\\
x_{3}=y_{3}.
\end{cases}
$$

因此

$$
f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}.
$$

非退化线性替换 $X=CY$, 其中

$$
C=\left[\begin{array}{rrr}
1 & -1 & 2\\
0 & 1 & -1\\
0 & 0 & 1
\end{array}\right].
$$

$f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}$ 是标准形. $\blacksquare$

### 习题二

(习题 6.1-5) 设 $A$ 是数域 $K$ 上的 $n$ 级矩阵, 证明: $A$ 是斜对称矩阵当且仅当对于 $K^{n}$ 中任一列向量 $\alpha$, 有 $\alpha^{T}A\alpha=0$.

### 解答 习题二

由**定义1** (二次型), $A$ 是数域 $K$ 上的 $n$ 级矩阵.

**必要性**. 若 $A$ 是斜对称矩阵, 即 $A^{T}=-A$.

则 $\alpha^{T}A\alpha$ 是一个数, 其转置等于自身:

$$
\left(\alpha^{T}A\alpha\right)^{T}=\alpha^{T}A^{T}\alpha=\alpha^{T}\left(-A\right)\alpha=-\alpha^{T}A\alpha.
$$

但 $\left(\alpha^{T}A\alpha\right)^{T}=\alpha^{T}A\alpha$ (因为它是一个数).

因此

$$
\alpha^{T}A\alpha=-\alpha^{T}A\alpha,
$$

即 $2\alpha^{T}A\alpha=0$, 故 $\alpha^{T}A\alpha=0$.

**充分性**. 若对于任一列向量 $\alpha$, $\alpha^{T}A\alpha=0$.

要证明 $A$ 是斜对称矩阵, 即 $A^{T}=-A$, 即 $A+A^{T}=0$.

因为 $\left(A+A^{T}\right)$ 是对称矩阵.

对于任一列向量 $\alpha$,

$$
\alpha^{T}\left(A+A^{T}\right)\alpha=\alpha^{T}A\alpha+\alpha^{T}A^{T}\alpha=0+\left(\alpha^{T}A\alpha\right)^{T}=0+0=0.
$$

即对于任一列向量 $\alpha$, $\alpha^{T}\left(A+A^{T}\right)\alpha=0$.

因为 $\left(A+A^{T}\right)$ 是对称矩阵, 且对于任一列向量 $\alpha$, $\alpha^{T}\left(A+A^{T}\right)\alpha=0$.

由对称矩阵的性质 (对称矩阵如果对任意 $\alpha$ 都有 $\alpha^{T}A\alpha=0$, 则 $A=0$ ), 可知 $A+A^{T}=0$.

因此 $A^{T}=-A$, 即 $A$ 是斜对称矩阵. $\blacksquare$

### 习题三

(习题 6.1-8(1)) 用矩阵的成对初等行, 列变换法把数域 $K$ 上的下述二次型化成标准形, 并且写出所作的非退化线性替换:

$$
f\left(x_{1},x_{2},x_{3}\right)=x_{1}^{2}-2x_{2}^{2}+x_{3}^{2}-2x_{1}x_{3}+4x_{2}x_{3}.
$$

### 解答 习题三

用配方法:

$$
\begin{aligned}f
&=x_{1}^{2}-2x_{1}x_{3}+x_{3}^{2}-2x_{2}^{2}+4x_{2}x_{3}\\
&=\left(x_{1}-x_{3}\right)^{2}-2x_{2}^{2}+4x_{2}x_{3}\\
&=\left(x_{1}-x_{3}\right)^{2}-2\left(x_{2}^{2}-2x_{2}x_{3}\right)\\
&=\left(x_{1}-x_{3}\right)^{2}-2\left(x_{2}-x_{3}\right)^{2}+2x_{3}^{2}.
\end{aligned}
$$

令

$$
\begin{cases}
y_{1}=x_{1}-x_{3},\\
y_{2}=x_{2}-x_{3},\\
y_{3}=x_{3}.
\end{cases}
$$

则

$$
\begin{cases}
x_{1}=y_{1}+y_{3},\\
x_{2}=y_{2}+y_{3},\\
x_{3}=y_{3}.
\end{cases}
$$

因此

$$
f=y_{1}^{2}-2y_{2}^{2}+2y_{3}^{2}.
$$

非退化线性替换 $X=CY$, 其中

$$
C=\left[\begin{array}{rrr}
1 & 0 & 1\\
0 & 1 & 1\\
0 & 0 & 1
\end{array}\right].
$$

$\blacksquare$

### 习题四

(习题 6.1-11) 设 $n$ 级实对称矩阵 $A$ 的全部特征值按大小顺序排成: $\lambda_{1}\ge\lambda_{2}\ge\cdots\ge\lambda_{n}$. 证明: 对于 $\mathbb{R}^{n}$ 中任一列向量 $\alpha\ne0$, 都有

$$
\lambda_{1}\ge\frac{\alpha^{T}A\alpha}{\alpha^{T}\alpha}\ge\lambda_{n}.
$$

### 解答 习题四

因为 $A$ 是实对称矩阵, 故存在正交矩阵 $T$, 使得

$$
T^{T}AT=\operatorname{diag}\left\{\lambda_{1},\lambda_{2},\cdots,\lambda_{n}\right\}.
$$

令 $\alpha=T\beta$, 则

$$
\alpha^{T}\alpha=\beta^{T}T^{T}T\beta=\beta^{T}\beta.
$$

$$
\alpha^{T}A\alpha=\beta^{T}T^{T}AT\beta=\beta^{T}\operatorname{diag}\left\{\lambda_{1},\cdots,\lambda_{n}\right\}\beta=\lambda_{1}\beta_{1}^{2}+\lambda_{2}\beta_{2}^{2}+\cdots+\lambda_{n}\beta_{n}^{2}.
$$

因为 $\lambda_{1}\ge\lambda_{2}\ge\cdots\ge\lambda_{n}$, 所以

$$
\lambda_{1}\left(\beta_{1}^{2}+\beta_{2}^{2}+\cdots+\beta_{n}^{2}\right)\ge\lambda_{1}\beta_{1}^{2}+\lambda_{2}\beta_{2}^{2}+\cdots+\lambda_{n}\beta_{n}^{2}\ge\lambda_{n}\left(\beta_{1}^{2}+\beta_{2}^{2}+\cdots+\beta_{n}^{2}\right).
$$

即

$$
\lambda_{1}\alpha^{T}\alpha\ge\alpha^{T}A\alpha\ge\lambda_{n}\alpha^{T}\alpha.
$$

因为 $\alpha\ne0$, 故 $\alpha^{T}\alpha>0$.

两边除以 $\alpha^{T}\alpha$:

$$
\lambda_{1}\ge\frac{\alpha^{T}A\alpha}{\alpha^{T}\alpha}\ge\lambda_{n}.
$$

$\blacksquare$
