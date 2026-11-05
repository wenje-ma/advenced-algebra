# week19

> **定理 5.6.1 (可对角化的充要条件)**
> 
> 数域 $K$ 上 $n$ 级矩阵 $A$ 可对角化的充分必要条件是 $A$ 有 $n$ 个线性无关的特征向量.

> **推论 5.6.6 (有 $n$ 个不同特征值则可对角化)**
> 
> 如果数域 $K$ 上 $n$ 级矩阵 $A$ 有 $n$ 个不同的特征值, 则 $A$ 可对角化.

$$
\beta_{i}=\alpha_{i}-\sum_{k=1}^{i-1}\frac{\left(\alpha_{i},\beta_{k}\right)}{\left(\beta_{k},\beta_{k}\right)}\beta_{k},
$$
则 $\beta_{1},\beta_{2},\cdots,\beta_{m}$ 是正交向量组, 且与原向量组等价.

> **定理 5.7.1 (实对称矩阵的特征值)**
> 
> 实对称矩阵的特征多项式在复数域中的每一个根都是实数.

> **定理 5.7.3 (实对称矩阵可正交对角化)**
> 
> 对于任意 $n$ 级实对称矩阵 $A$, 一定存在一个 $n$ 级正交矩阵 $T$, 使得 $T^{-1}AT$ 为对角矩阵.

> **定义 6.1.1 (二次型)**
> 
> 系数在数域 $K$ 中的 $n$ 个变量 $x_{1},x_{2},\cdots,x_{n}$ 的一个二次齐次多项式, 称为数域 $K$ 上的一个 $n$ 元二次型.

> **定义 6.1.2 (规范形)**
> 
> 实二次型 $X^{\top}AX$ 的规范形为

$$
z_{1}^{2}+\cdots+z_{p}^{2}-z_{p+1}^{2}-\cdots-z_{r}^{2},
$$
其中 $p$ 是正惯性指数, $r$ 是二次型的秩.

> **定理 6.1.3 (二次型的标准形)**
> 
> 数域 $K$ 上任意一个二次型都等价于一个只含平方项的二次型.

## 5.6-10

设 $A=\left(a_{ij}\right)$ 是数域 $K$ 上一个 $n$ 级上三角矩阵, 证明: 如果 $a_{11}=a_{22}=\cdots=a_{nn}$, 并且至少有一个 $a_{kl}\ne0$ ( $k< l$ ), 则 $A$ 一定不能对角化.

### 解答 5.6-10

因为 $A$ 是上三角矩阵, 故特征值就是主对角元 $a_{11},a_{22},\cdots,a_{nn}$.

已知

$$
a_{11}=a_{22}=\cdots=a_{nn}=\lambda_{0}.
$$

即 $\lambda_{0}$ 是 $A$ 的 $n$ 重特征值 (代数重数为 $n$ ).

求特征子空间的维数.

$$
\lambda_{0}I-A=\left[\begin{array}{cccc}
0 & -a_{12} & \cdots & -a_{1n}\\
0 & 0 & \cdots & -a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
0 & 0 & \cdots & 0
\end{array}\right].
$$

因为至少有一个 $a_{kl}\ne0$ ( $k< l$ ), 故 $\lambda_{0}I-A$ 不是零矩阵.

因此 $\operatorname{rank}\left(\lambda_{0}I-A\right)\ge1$.

故特征子空间的维数为

$$
n-\operatorname{rank}\left(\lambda_{0}I-A\right)\le n-1.
$$

即几何重数 $\le n-1< n=$ 代数重数.

因此 $A$ 不能对角化. $\blacksquare$

## 5.7-1(1)

对于下列实对称矩阵 $A$, 求正交矩阵 $T$, 使 $T^{\top}AT$ 为对角矩阵:

$$
A=\left[\begin{array}{rrr}
0 & -2 & 2\\
-2 & -3 & 4\\
2 & 4 & -3
\end{array}\right].
$$

### 解答 5.7-1(1)

由**定理 5.7.3 (实对称矩阵可正交对角化)**, 一定存在正交矩阵 $T$, 使 $T^{\top}AT$ 为对角矩阵. 求特征多项式:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda & 2 & -2\\
2 & \lambda+3 & -4\\
-2 & -4 & \lambda+3
\end{array}\right|=\left(\lambda-1\right)^{2}\left(\lambda+8\right).
$$

因此特征值为 $\lambda_{1}=\lambda_{2}=1$, $\lambda_{3}=-8$.

求 $\lambda=1$ 的特征向量.

$$
I-A=\left[\begin{array}{rrr}
1 & 2 & -2\\
2 & 4 & -4\\
-2 & -4 & 4
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & 2 & -2\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

基础解系: $\alpha_{1}=\left(-2,1,0\right)^{\top}$, $\alpha_{2}=\left(2,0,1\right)^{\top}$.

由施密特正交化方法:

$$
\beta_{1}=\alpha_{1}=\left(-2,1,0\right)^{\top}.
$$

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}
=\left(2,0,1\right)^{\top}-\frac{-4}{5}\left(-2,1,0\right)^{\top}
=\left(\frac{2}{5},\frac{4}{5},1\right)^{\top}.
$$

单位化:

$$
\eta_{1}=\left(-\frac{2}{\sqrt{5}},\frac{1}{\sqrt{5}},0\right)^{\top}.
$$

$$
\eta_{2}=\left(\frac{2}{3\sqrt{5}},\frac{4}{3\sqrt{5}},\frac{\sqrt{5}}{3}\right)^{\top}.
$$

求 $\lambda=-8$ 的特征向量.

$$
-8I-A=\left[\begin{array}{rrr}
-8 & 2 & -2\\
2 & -5 & -4\\
-2 & -4 & -5
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & 0 & 1/2\\
0 & 1 & 1\\
0 & 0 & 0
\end{array}\right].
$$

基础解系: $\alpha_{3}=\left(-1,2,-4\right)^{\top}$.

单位化:

$$
\eta_{3}=\left(-\frac{1}{\sqrt{21}},\frac{2}{\sqrt{21}},-\frac{4}{\sqrt{21}}\right)^{\top}.
$$

因此正交矩阵为

$$
T=\left[\begin{array}{ccc}
-2/\sqrt{5} & 2/\left(3\sqrt{5}\right) & -1/\sqrt{21}\\
1/\sqrt{5} & 4/\left(3\sqrt{5}\right) & 2/\sqrt{21}\\
0 & \sqrt{5}/3 & -4/\sqrt{21}
\end{array}\right].
$$

由**定理 5.7.3 (实对称矩阵可正交对角化)**,

$$
T^{\top}AT=\operatorname{diag}\left\{1,1,-8\right\}.
$$

$\blacksquare$

## 5.7-1(3)

对于下列实对称矩阵 $A$, 求正交矩阵 $T$, 使 $T^{\top}AT$ 为对角矩阵:

$$
A=\left[\begin{array}{rrr}
3 & -2 & 0\\
-2 & 2 & -2\\
0 & -2 & 1
\end{array}\right].
$$

### 解答 5.7-1(3)

求特征多项式:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-3 & 2 & 0\\
2 & \lambda-2 & 2\\
0 & 2 & \lambda-1
\end{array}\right|=\left(\lambda+1\right)\left(\lambda-2\right)\left(\lambda-5\right).
$$

因此特征值为 $\lambda_{1}=-1$, $\lambda_{2}=2$, $\lambda_{3}=5$.

求 $\lambda=-1$ 的特征向量.

基础解系: $\alpha_{1}=\left(1,2,2\right)^{\top}$.

求 $\lambda=2$ 的特征向量.

基础解系: $\alpha_{2}=\left(2,1,-2\right)^{\top}$.

求 $\lambda=5$ 的特征向量.

基础解系: $\alpha_{3}=\left(-2,2,-1\right)^{\top}$.

验证正交性: $\left(\alpha_{1},\alpha_{2}\right)=0$, $\left(\alpha_{1},\alpha_{3}\right)=0$, $\left(\alpha_{2},\alpha_{3}\right)=0$.

单位化:

$$
\eta_{1}=\left(\frac{1}{3},\frac{2}{3},\frac{2}{3}\right)^{\top}.
$$

$$
\eta_{2}=\left(\frac{2}{3},\frac{1}{3},-\frac{2}{3}\right)^{\top}.
$$

$$
\eta_{3}=\left(-\frac{2}{3},\frac{2}{3},-\frac{1}{3}\right)^{\top}.
$$

因此正交矩阵为

$$
T=\left[\begin{array}{rrr}
1/3 & 2/3 & -2/3\\
2/3 & 1/3 & 2/3\\
2/3 & -2/3 & -1/3
\end{array}\right].
$$

$$
T^{\top}AT=\operatorname{diag}\left\{-1,2,5\right\}.
$$

$\blacksquare$

## 5.7-2

证明: 如果 $n$ 级实对称矩阵 $A,B$ 有相同的特征多项式, 则 $A$ 与 $B$ 相似.

### 解答 5.7-2

因为 $A$ 是实对称矩阵, 故由**定理 5.7.3 (实对称矩阵可正交对角化)**, $A$ 正交相似于对角矩阵 $D_{A}$, 且 $D_{A}$ 的主对角元是 $A$ 的全部特征值 (计重数).

同理, $B$ 正交相似于对角矩阵 $D_{B}$, 且 $D_{B}$ 的主对角元是 $B$ 的全部特征值 (计重数).

因为 $A,B$ 有相同的特征多项式, 所以它们有相同的特征值 (计重数).

因此 $D_{A}$ 与 $D_{B}$ 的主对角元相同 (至多排列次序不同).

通过交换 $D_{B}$ 的主对角元的次序, 可使 $D_{A}=D_{B}$.

交换主对角元的次序相当于用一个正交矩阵 $Q$ 作相似变换: $Q^{\top}D_{B}Q=D_{A}$.

因此

$$
A\sim D_{A}=D_{B}\sim B.
$$

所以 $A$ 与 $B$ 相似. $\blacksquare$

## 5.7-3

证明: 如果实矩阵 $A$ 正交相似于对角矩阵, 则 $A$ 一定是对称矩阵.

### 解答 5.7-3

设 $A$ 正交相似于对角矩阵 $D$, 即存在正交矩阵 $T$, 使得

$$
T^{\top}AT=D.
$$

则

$$
A=TDT^{\top}.
$$

因为 $D$ 是对角矩阵, 故 $D^{\top}=D$.

因此

$$
A^{\top}=\left(TDT^{\top}\right)^{\top}=TD^{\top}T^{\top}=TDT^{\top}=A.
$$

所以 $A$ 是对称矩阵. $\blacksquare$

## 6.1-3(1)

作非退化线性替换把下列数域 $K$ 上二次型化成标准形, 并且写出所作的非退化线性替换:

$$
f\left(x_{1},x_{2},x_{3}\right)=x_{1}^{2}+2x_{2}^{2}+2x_{1}x_{2}-2x_{1}x_{3}.
$$

### 解答 6.1-3(1)

由**定理 6.1.3 (二次型的标准形)**, 用配方法:

$$
f
=x_{1}^{2}+2x_{1}x_{2}-2x_{1}x_{3}+2x_{2}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}-\left(x_{2}-x_{3}\right)^{2}+2x_{2}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}+x_{2}^{2}+2x_{2}x_{3}-x_{3}^{2}=\left(x_{1}+x_{2}-x_{3}\right)^{2}+\left(x_{2}+x_{3}\right)^{2}-2x_{3}^{2}.
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

## 6.1-5

设 $A$ 是数域 $K$ 上的 $n$ 级矩阵, 证明: $A$ 是斜对称矩阵当且仅当对于 $K^{n}$ 中任一列向量 $\alpha$, 有 $\alpha^{\top}A\alpha=0$.

### 解答 6.1-5

由**定义 6.1.1 (二次型)**, $A$ 是数域 $K$ 上的 $n$ 级矩阵.

必要性. 若 $A$ 是斜对称矩阵, 即 $A^{\top}=-A$.

则 $\alpha^{\top}A\alpha$ 是一个数, 其转置等于自身:

$$
\left(\alpha^{\top}A\alpha\right)^{\top}=\alpha^{\top}A^{\top}\alpha=\alpha^{\top}\left(-A\right)\alpha=-\alpha^{\top}A\alpha.
$$

但 $\left(\alpha^{\top}A\alpha\right)^{\top}=\alpha^{\top}A\alpha$ (因为它是一个数).

因此

$$
\alpha^{\top}A\alpha=-\alpha^{\top}A\alpha,
$$

即 $2\alpha^{\top}A\alpha=0$, 故 $\alpha^{\top}A\alpha=0$.

充分性. 若对于任一列向量 $\alpha$, $\alpha^{\top}A\alpha=0$.

要证明 $A$ 是斜对称矩阵, 即 $A^{\top}=-A$, 即 $A+A^{\top}=0$.

因为 $\left(A+A^{\top}\right)$ 是对称矩阵.

对于任一列向量 $\alpha$,

$$
\alpha^{\top}\left(A+A^{\top}\right)\alpha=\alpha^{\top}A\alpha+\alpha^{\top}A^{\top}\alpha=0+\left(\alpha^{\top}A\alpha\right)^{\top}=0+0=0.
$$

即对于任一列向量 $\alpha$, $\alpha^{\top}\left(A+A^{\top}\right)\alpha=0$.

因为 $\left(A+A^{\top}\right)$ 是对称矩阵, 且对于任一列向量 $\alpha$, $\alpha^{\top}\left(A+A^{\top}\right)\alpha=0$.

由对称矩阵的性质 (对称矩阵如果对任意 $\alpha$ 都有 $\alpha^{\top}A\alpha=0$, 则 $A=0$ ), 可知 $A+A^{\top}=0$.

因此 $A^{\top}=-A$, 即 $A$ 是斜对称矩阵. $\blacksquare$
