# week20

> **定义 6.1.1 (二次型)**
> 
> 系数在数域 $K$ 中的 $n$ 个变量 $x_{1},x_{2},\cdots,x_{n}$ 的一个二次齐次多项式, 称为数域 $K$ 上的一个 $n$ 元二次型.

> **定义 6.1.2 (规范形)**
> 
> 实二次型 $X^{\top}AX$ 的规范形为

> **定理 6.1.3 (二次型的标准形)**
> 
> 数域 $K$ 上任意一个二次型都等价于一个只含平方项的二次型.

> **定义 6.2.1 (正惯性指数)**
> 
> 在实二次型 $X^{\top}AX$ 的规范形中, 系数为 $+1$ 的平方项的数目 $p$ 称为 $X^{\top}AX$ 的正惯性指数, 系数为 $-1$ 的平方项的数目 $r-p$ 称为 $X^{\top}AX$ 的负惯性指数.

> **定理 6.2.1 (惯性定理)**
> 
> $n$ 元实二次型 $X^{\top}AX$ 的规范形是唯一的.

> **推论 6.2.4 (合同的充要条件)**
> 
> 两个 $n$ 级实对称矩阵合同当且仅当它们的秩相等, 并且正惯性指数也相等.

> **定义 7.2.1 (整除)**
> 
> 设 $f\left(x\right),g\left(x\right)\in{K}\left[x\right]$, 如果存在 $h\left(x\right)\in{K}\left[x\right]$, 使得 $f\left(x\right)=h\left(x\right)g\left(x\right)$, 则称 $g\left(x\right)$ 整除 $f\left(x\right)$, 记作 $g\left(x\right)\mid{f}\left(x\right)$.

> **定理 7.2.1 (带余除法)**
> 
> 在 $K\left[x\right]$ 中, 对于任意两个多项式 $f\left(x\right),g\left(x\right)$, 其中 $g\left(x\right)\ne0$, 存在唯一的一对多项式 $h\left(x\right),r\left(x\right)$, 使得

$$
f\left(x\right)=h\left(x\right)g\left(x\right)+r\left(x\right),\deg{r}\left(x\right)<\deg{g}\left(x\right).
$$

## 6.1-8(1)

用矩阵的成对初等行, 列变换法把数域 $K$ 上的下述二次型化成标准形, 并且写出所作的非退化线性替换:

$$
f\left(x_{1},x_{2},x_{3}\right)=x_{1}^{2}-2x_{2}^{2}+x_{3}^{2}-2x_{1}x_{3}+4x_{2}x_{3}.
$$

### 解答 6.1-8(1)

用配方法:

$$
f
=x_{1}^{2}-2x_{1}x_{3}+x_{3}^{2}-2x_{2}^{2}+4x_{2}x_{3}=\left(x_{1}-x_{3}\right)^{2}-2x_{2}^{2}+4x_{2}x_{3}=\left(x_{1}-x_{3}\right)^{2}-2\left(x_{2}^{2}-2x_{2}x_{3}\right)=\left(x_{1}-x_{3}\right)^{2}-2\left(x_{2}-x_{3}\right)^{2}+2x_{3}^{2}.
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
1&0&1\\
0&1&1\\
0&0&1
\end{array}\right].
$$

$\blacksquare$

## 6.1-11

设 $n$ 级实对称矩阵 $A$ 的全部特征值按大小顺序排成: $\lambda_{1}\ge\lambda_{2}\ge\cdots\ge\lambda_{n}$. 证明: 对于 $\mathbb{R}^{n}$ 中任一列向量 $\alpha\ne0$, 都有

$$
\lambda_{1}\ge\frac{\alpha^{\top}A\alpha}{\alpha^{\top}\alpha}\ge\lambda_{n}.
$$

### 解答 6.1-11

因为 $A$ 是实对称矩阵, 故存在正交矩阵 $T$, 使得

$$
T^{\top}AT=\operatorname{diag}\left\{\lambda_{1},\lambda_{2},\cdots,\lambda_{n}\right\}.
$$

令 $\alpha=T\beta$, 则

$$
\alpha^{\top}\alpha=\beta^{\top}T^{\top}T\beta=\beta^{\top}\beta.
$$

$$
\alpha^{\top}A\alpha=\beta^{\top}T^{\top}AT\beta=\beta^{\top}\operatorname{diag}\left\{\lambda_{1},\cdots,\lambda_{n}\right\}\beta=\lambda_{1}\beta_{1}^{2}+\lambda_{2}\beta_{2}^{2}+\cdots+\lambda_{n}\beta_{n}^{2}.
$$

因为 $\lambda_{1}\ge\lambda_{2}\ge\cdots\ge\lambda_{n}$, 所以

$$
\lambda_{1}\left(\beta_{1}^{2}+\beta_{2}^{2}+\cdots+\beta_{n}^{2}\right)\ge\lambda_{1}\beta_{1}^{2}+\lambda_{2}\beta_{2}^{2}+\cdots+\lambda_{n}\beta_{n}^{2}\ge\lambda_{n}\left(\beta_{1}^{2}+\beta_{2}^{2}+\cdots+\beta_{n}^{2}\right).
$$

即

$$
\lambda_{1}\alpha^{\top}\alpha\ge\alpha^{\top}A\alpha\ge\lambda_{n}\alpha^{\top}\alpha.
$$

因为 $\alpha\ne0$, 故 $\alpha^{\top}\alpha>0$.

两边除以 $\alpha^{\top}\alpha$:

$$
\lambda_{1}\ge\frac{\alpha^{\top}A\alpha}{\alpha^{\top}\alpha}\ge\lambda_{n}.
$$

$\blacksquare$

## 6.2-1

把习题 6.1 的第 3 题的所有实二次型的标准形进一步化成规范形, 并且写出所作的非退化线性替换.

### 解答 6.2-1

由**定理 6.2.1 (惯性定理)**, $n$ 元实二次型 $X^{\top}AX$ 的规范形是唯一的.

**习题 6.1 第 3 题(1)**:

$$
f=x_{1}^{2}+2x_{2}^{2}+2x_{1}x_{2}-2x_{1}x_{3}.
$$

标准形: $f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}$.

化成规范形: 令 $z_{3}=\sqrt{2}y_{3}$, 则

$$
f=z_{1}^{2}+z_{2}^{2}-z_{3}^{2}.
$$

非退化线性替换: $z_{1}=y_{1}$, $z_{2}=y_{2}$, $z_{3}=\sqrt{2}y_{3}$.

**习题 6.1 第 3 题(2)**:

$$
f=x_{1}^{2}-x_{2}^{2}+2x_{1}x_{3}+2x_{2}x_{3}.
$$

化成规范形即可.

**习题 6.1 第 3 题(3)**: $f=x_{1}x_{2}+x_{1}x_{3}+x_{2}x_{3}$.

化成规范形即可.

**习题 6.1 第 3 题(4)**: $f=2x_{1}x_{2}-2x_{3}x_{4}$.

化成规范形即可.

以上规范形都是唯一的. $\blacksquare$

## 6.2-4

设 $X^{\top}AX$ 是一个 $n$ 元实二次型, 证明: 如果 $\mathbb{R}^{n}$ 中有列向量 $\alpha_{1},\alpha_{2}$, 使得 $\alpha_{1}^{\top}A\alpha_{1}>0$, $\alpha_{2}^{\top}A\alpha_{2}<0$, 则 $\mathbb{R}^{n}$ 中有非零列向量 $\alpha$, 使得 $\alpha^{\top}A\alpha=0$.

### 解答 6.2-4

由**定义 6.2.1 (正惯性指数)**, 设 $X^{\top}AX$ 是一个 $n$ 元实二次型. 考虑函数

$$
g\left(t\right)=\left(\alpha_{1}+t\alpha_{2}\right)^{\top}A\left(\alpha_{1}+t\alpha_{2}\right).
$$

展开:

$$
g\left(t\right)=\alpha_{1}^{\top}A\alpha_{1}+2t\alpha_{1}^{\top}A\alpha_{2}+t^{2}\alpha_{2}^{\top}A\alpha_{2}.
$$

这是关于 $t$ 的二次函数.

已知 $g\left(0\right)=\alpha_{1}^{\top}A\alpha_{1}>0$.

又因为 $\alpha_{2}^{\top}A\alpha_{2}<0$, 所以当 $t\to\infty$ 时, $g\left(t\right)\to-\infty$.

因此存在 $t_{0}>0$, 使得 $g\left(t_{0}\right)<0$.

由连续函数的介值定理, 存在 $t_{1}\in\left(0,t_{0}\right)$, 使得 $g\left(t_{1}\right)=0$.

令 $\alpha=\alpha_{1}+t_{1}\alpha_{2}$.

则 $\alpha\ne0$ (因为如果 $\alpha=0$, 则 $\alpha_{1}=-t_{1}\alpha_{2}$, 从而 $\alpha_{1}^{\top}A\alpha_{1}=t_{1}^{2}\alpha_{2}^{\top}A\alpha_{2}<0$, 矛盾).

且 $\alpha^{\top}A\alpha=g\left(t_{1}\right)=0$.

因此 $\mathbb{R}^{n}$ 中有非零列向量 $\alpha$, 使得 $\alpha^{\top}A\alpha=0$. $\blacksquare$

## 6.2-6

证明: 一个 $n$ 元实二次型可以分解成两个实系数 $1$ 次齐次多项式的乘积当且仅当它的秩等于 $2$, 并且符号差为 $0$, 或者它的秩等于 $1$.

### 解答 6.2-6

充分性.

若秩等于 $2$, 且符号差为 $0$, 则规范形为

$$
y_{1}^{2}-y_{2}^{2}=\left(y_{1}+y_{2}\right)\left(y_{1}-y_{2}\right).
$$

这是两个 $1$ 次齐次多项式的乘积.

若秩等于 $1$, 则规范形为 $y_{1}^{2}=y_{1}\cdot{y}_{1}$.

这也是两个 $1$ 次齐次多项式的乘积.

必要性.

设

$$
X^{\top}AX=\left(a_{1}x_{1}+\cdots+a_{n}x_{n}\right)\left(b_{1}x_{1}+\cdots+b_{n}x_{n}\right).
$$

令 $\alpha=\left(a_{1},\cdots,a_{n}\right)^{\top}$, $\beta=\left(b_{1},\cdots,b_{n}\right)^{\top}$.

则

$$
X^{\top}AX=\left(\alpha^{\top}X\right)\left(\beta^{\top}X\right)=X^{\top}\left(\frac{\alpha\beta^{\top}+\beta\alpha^{\top}}{2}\right)X.
$$

因此

$$
A=\frac{\alpha\beta^{\top}+\beta\alpha^{\top}}{2}.
$$

情况1: $\alpha$ 与 $\beta$ 线性相关.

设 $\beta=k\alpha$. 则

$$
A=\frac{\alpha\cdot{k}\alpha^{\top}+k\alpha\cdot\alpha^{\top}}{2}=k\alpha\alpha^{\top}.
$$

因此 $\operatorname{rank}\left(A\right)=1$.

情况2: $\alpha$ 与 $\beta$ 线性无关.

令

$$
\gamma_{1}=\frac{\alpha+\beta}{2},\gamma_{2}=\frac{\alpha-\beta}{2}.
$$

则

$$
A=\gamma_{1}\gamma_{1}^{\top}-\gamma_{2}\gamma_{2}^{\top}.
$$

因为 $\gamma_{1},\gamma_{2}$ 线性无关, 所以 $\operatorname{rank}\left(A\right)=2$.

且正惯性指数为 $1$, 负惯性指数为 $1$, 故符号差为 $0$.

因此秩等于 $2$, 且符号差为 $0$.

$\blacksquare$

## 6.2-7

证明: 复数域上 $n$ 元二次型 (简称为复二次型) $X^{\top}AX$ 能经过非退化线性替换化成下述形式的标准形:

$$
z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2},
$$

其中 $r$ 是二次型 $X^{\top}AX$ 的秩. 这种形式的标准形称为 $X^{\top}AX$ 的规范形, 它只含平方项, 且平方项的系数为 $1$ 或 $0$.

### 解答 6.2-7

因为 $A$ 是复数域上的对称矩阵, 故 $A$ 合同于一个对角矩阵

$$
D=\operatorname{diag}\left\{d_{1},d_{2},\cdots,d_{r},0,\cdots,0\right\},
$$

其中 $d_{i}\ne0$.

因为复数域上每个非零数都可以开平方, 故存在 $c_{i}\in\mathbb{C}$, 使得 $c_{i}^{2}=d_{i}$.

令

$$
C=\operatorname{diag}\left\{\frac{1}{c_{1}},\frac{1}{c_{2}},\cdots,\frac{1}{c_{r}},1,\cdots,1\right\}.
$$

则

$$
C^{\top}DC=\operatorname{diag}\left\{1,1,\cdots,1,0,\cdots,0\right\}.
$$

因此 $A$ 合同于 $\operatorname{diag}\left\{I_{r},0\right\}$.

即存在可逆矩阵 $P$, 使得 $P^{\top}AP=\operatorname{diag}\left\{I_{r},0\right\}$.

令 $X=PZ$, 则

$$
X^{\top}AX=Z^{\top}P^{\top}APZ=Z^{\top}\operatorname{diag}\left\{I_{r},0\right\}Z=z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2}.
$$

因此复二次型 $X^{\top}AX$ 的规范形为 $z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2}$, 其中 $r$ 是二次型的秩. $\blacksquare$

## 7.2-3(2)

用 $g\left(x\right)$ 除 $f\left(x\right)$, 求商式与余式:

$$
f\left(x\right)=x^{4}+x^{3}-2x+3,\quad{g}\left(x\right)=3x^{2}-x+2.
$$

### 解答 7.2-3(2)

由**定理 7.2.1 (带余除法)**, 作多项式除法:

$$
f\left(x\right)=x^{4}+x^{3}+0x^{2}-2x+3.
$$

商式首项: $x^{4}/3x^{2}=\frac{1}{3}x^{2}$.

$$
\frac{1}{3}x^{2}\cdot{g}\left(x\right)=x^{4}-\frac{1}{3}x^{3}+\frac{2}{3}x^{2}.
$$

余式:

$$
f-\frac{1}{3}x^{2}g=\frac{4}{3}x^{3}-\frac{2}{3}x^{2}-2x+3.
$$

商式第二项: $\frac{4}{3}x^{3}/3x^{2}=\frac{4}{9}x$.

$$
\frac{4}{9}x\cdot{g}=\frac{4}{3}x^{3}-\frac{4}{9}x^{2}+\frac{8}{9}x.
$$

余式:

$$
-\frac{2}{9}x^{2}-\frac{26}{9}x+3.
$$

商式第三项: $-\frac{2}{9}x^{2}/3x^{2}=-\frac{2}{27}$.

$$
-\frac{2}{27}\cdot{g}=-\frac{2}{9}x^{2}+\frac{2}{27}x-\frac{4}{27}.
$$

余式:

$$
-\frac{80}{27}x+\frac{85}{27}.
$$

因此, 由**定理 7.2.1 (带余除法)**,

$$
\text{商式~}h\left(x\right)=\frac{1}{3}x^{2}+\frac{4}{9}x-\frac{2}{27}.
$$

$$
\text{余式~}r\left(x\right)=-\frac{80}{27}x+\frac{85}{27}.
$$

$\blacksquare$
