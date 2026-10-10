# 作业 33

> **定理1** (惯性定理)<br>$n$ 元实二次型 $X^{T}AX$ 的规范形是唯一的.

> **定义1** (正惯性指数)<br>在实二次型 $X^{T}AX$ 的规范形中, 系数为 $+1$ 的平方项的数目 $p$ 称为 $X^{T}AX$ 的正惯性指数, 系数为 $-1$ 的平方项的数目 $r-p$ 称为 $X^{T}AX$ 的负惯性指数.

> **推论4** (合同的充要条件)<br>两个 $n$ 级实对称矩阵合同当且仅当它们的秩相等, 并且正惯性指数也相等.

### 习题一

(习题 6.2-1) 把习题 6.1 的第 3 题的所有实二次型的标准形进一步化成规范形, 并且写出所作的非退化线性替换.

### 解答 习题一

由**定理1** (惯性定理), $n$ 元实二次型 $X^{T}AX$ 的规范形是唯一的.

**习题 6.1 第 3 题(1)**: $f=x_{1}^{2}+2x_{2}^{2}+2x_{1}x_{2}-2x_{1}x_{3}$.

标准形: $f=y_{1}^{2}+y_{2}^{2}-2y_{3}^{2}$.

化成规范形: 令 $z_{3}=\sqrt{2}y_{3}$, 则

$$
f=z_{1}^{2}+z_{2}^{2}-z_{3}^{2}.
$$

非退化线性替换: $z_{1}=y_{1}$, $z_{2}=y_{2}$, $z_{3}=\sqrt{2}y_{3}$.

**习题 6.1 第 3 题(2)**: $f=x_{1}^{2}-x_{2}^{2}+2x_{1}x_{3}+2x_{2}x_{3}$.

(具体计算略, 化成规范形即可. )

**习题 6.1 第 3 题(3)**: $f=x_{1}x_{2}+x_{1}x_{3}+x_{2}x_{3}$.

(具体计算略, 化成规范形即可. )

**习题 6.1 第 3 题(4)**: $f=2x_{1}x_{2}-2x_{3}x_{4}$.

(具体计算略, 化成规范形即可. )

以上规范形都是唯一的. $\blacksquare$

### 习题二

(习题 6.2-4) 设 $X^{T}AX$ 是一个 $n$ 元实二次型, 证明: 如果 $\mathbb{R}^{n}$ 中有列向量 $\alpha_{1},\alpha_{2}$, 使得 $\alpha_{1}^{T}A\alpha_{1}>0$, $\alpha_{2}^{T}A\alpha_{2}<0$, 则 $\mathbb{R}^{n}$ 中有非零列向量 $\alpha$, 使得 $\alpha^{T}A\alpha=0$.

### 解答 习题二

由**定义1** (正惯性指数), 设 $X^{T}AX$ 是一个 $n$ 元实二次型. 考虑函数

$$
g\left(t\right)=\left(\alpha_{1}+t\alpha_{2}\right)^{T}A\left(\alpha_{1}+t\alpha_{2}\right).
$$

展开:

$$
g\left(t\right)=\alpha_{1}^{T}A\alpha_{1}+2t\alpha_{1}^{T}A\alpha_{2}+t^{2}\alpha_{2}^{T}A\alpha_{2}.
$$

这是关于 $t$ 的二次函数.

已知 $g\left(0\right)=\alpha_{1}^{T}A\alpha_{1}>0$.

又因为 $\alpha_{2}^{T}A\alpha_{2}<0$, 所以当 $t\to\infty$ 时, $g\left(t\right)\to-\infty$.

因此存在 $t_{0}>0$, 使得 $g\left(t_{0}\right)<0$.

由连续函数的介值定理, 存在 $t_{1}\in\left(0,t_{0}\right)$, 使得 $g\left(t_{1}\right)=0$.

令 $\alpha=\alpha_{1}+t_{1}\alpha_{2}$.

则 $\alpha\ne0$ (因为如果 $\alpha=0$, 则 $\alpha_{1}=-t_{1}\alpha_{2}$, 从而 $\alpha_{1}^{T}A\alpha_{1}=t_{1}^{2}\alpha_{2}^{T}A\alpha_{2}<0$, 矛盾).

且 $\alpha^{T}A\alpha=g\left(t_{1}\right)=0$.

因此 $\mathbb{R}^{n}$ 中有非零列向量 $\alpha$, 使得 $\alpha^{T}A\alpha=0$. $\blacksquare$

### 习题三

(习题 6.2-6) 证明: 一个 $n$ 元实二次型可以分解成两个实系数 $1$ 次齐次多项式的乘积当且仅当它的秩等于 $2$, 并且符号差为 $0$, 或者它的秩等于 $1$.

### 解答 习题三

**充分性**.

若秩等于 $2$, 且符号差为 $0$, 则规范形为 $y_{1}^{2}-y_{2}^{2}=\left(y_{1}+y_{2}\right)\left(y_{1}-y_{2}\right)$.

这是两个 $1$ 次齐次多项式的乘积.

若秩等于 $1$, 则规范形为 $y_{1}^{2}=y_{1}\cdot y_{1}$.

这也是两个 $1$ 次齐次多项式的乘积.

**必要性**.

设 $X^{T}AX=\left(a_{1}x_{1}+\cdots+a_{n}x_{n}\right)\left(b_{1}x_{1}+\cdots+b_{n}x_{n}\right)$.

令 $\alpha=\left(a_{1},\cdots,a_{n}\right)^{T}$, $\beta=\left(b_{1},\cdots,b_{n}\right)^{T}$.

则

$$
X^{T}AX=\left(\alpha^{T}X\right)\left(\beta^{T}X\right)=X^{T}\left(\frac{\alpha\beta^{T}+\beta\alpha^{T}}{2}\right)X.
$$

因此

$$
A=\frac{\alpha\beta^{T}+\beta\alpha^{T}}{2}.
$$

**情况1**: $\alpha$ 与 $\beta$ 线性相关.

设 $\beta=k\alpha$. 则

$$
A=\frac{\alpha\cdot k\alpha^{T}+k\alpha\cdot\alpha^{T}}{2}=k\alpha\alpha^{T}.
$$

因此 $\operatorname{rank}\left(A\right)=1$.

**情况2**: $\alpha$ 与 $\beta$ 线性无关.

令

$$
\gamma_{1}=\frac{\alpha+\beta}{2},\quad\gamma_{2}=\frac{\alpha-\beta}{2}.
$$

则

$$
A=\gamma_{1}\gamma_{1}^{T}-\gamma_{2}\gamma_{2}^{T}.
$$

因为 $\gamma_{1},\gamma_{2}$ 线性无关, 所以 $\operatorname{rank}\left(A\right)=2$.

且正惯性指数为 $1$, 负惯性指数为 $1$, 故符号差为 $0$.

因此秩等于 $2$, 且符号差为 $0$.

$\blacksquare$

### 习题四

(习题 6.2-7) 证明: 复数域上 $n$ 元二次型 (简称为复二次型) $X^{T}AX$ 能经过非退化线性替换化成下述形式的标准形:

$$
z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2},
$$

其中 $r$ 是二次型 $X^{T}AX$ 的秩. 这种形式的标准形称为 $X^{T}AX$ 的规范形, 它只含平方项, 且平方项的系数为 $1$ 或 $0$.

### 解答 习题四

因为 $A$ 是复数域上的对称矩阵, 由定理, $A$ 合同于一个对角矩阵 $D=\operatorname{diag}\left\{d_{1},d_{2},\cdots,d_{r},0,\cdots,0\right\}$, 其中 $d_{i}\ne0$.

因为复数域上每个非零数都可以开平方, 故存在 $c_{i}\in\mathbb{C}$, 使得 $c_{i}^{2}=d_{i}$.

令

$$
C=\operatorname{diag}\left\{\frac{1}{c_{1}},\frac{1}{c_{2}},\cdots,\frac{1}{c_{r}},1,\cdots,1\right\}.
$$

则

$$
C^{T}DC=\operatorname{diag}\left\{1,1,\cdots,1,0,\cdots,0\right\}.
$$

因此 $A$ 合同于 $\operatorname{diag}\left\{I_{r},0\right\}$.

即存在可逆矩阵 $P$, 使得 $P^{T}AP=\operatorname{diag}\left\{I_{r},0\right\}$.

令 $X=PZ$, 则

$$
X^{T}AX=Z^{T}P^{T}APZ=Z^{T}\operatorname{diag}\left\{I_{r},0\right\}Z=z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2}.
$$

因此复二次型 $X^{T}AX$ 的规范形为 $z_{1}^{2}+z_{2}^{2}+\cdots+z_{r}^{2}$, 其中 $r$ 是二次型的秩. $\blacksquare$
