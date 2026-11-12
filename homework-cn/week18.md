# week18

> **定义 5.5.1 (特征值与特征向量)**
> 
> 设 $A$ 是数域 $K$ 上的 $n$ 级矩阵, 如果 $K^{n}$ 中有非零列向量 $\alpha$, 使得 $A\alpha=\lambda_{0}\alpha$, 且 $\lambda_{0}\in{K}$, 则称 $\lambda_{0}$ 是 $A$ 的一个特征值, 称 $\alpha$ 是 $A$ 的属于特征值 $\lambda_{0}$ 的一个特征向量.

> **定理 5.6.1 (可对角化的充要条件)**
> 
> 数域 $K$ 上 $n$ 级矩阵 $A$ 可对角化的充分必要条件是 $A$ 有 $n$ 个线性无关的特征向量.

> **推论 5.6.6 (有 $n$ 个不同特征值则可对角化)**
> 
> 如果数域 $K$ 上 $n$ 级矩阵 $A$ 有 $n$ 个不同的特征值, 则 $A$ 可对角化.

## 5.5-12(1)

求下列复数域上矩阵的全部特征值和特征向量:

$$
P=\left[\begin{array}{ccc}
0&1&0\\
0&0&1\\
1&0&0
\end{array}\right].
$$

### 解答 5.5-12(1)

求特征多项式:

$$
\left|\lambda{I}-P\right|=\left|\begin{array}{rrr}
\lambda&-1&0\\
0&\lambda&-1\\
-1&0&\lambda
\end{array}\right|=\lambda^{3}-1.
$$

因此特征值为 $\lambda_{1}=1$, $\lambda_{2}=\omega$, $\lambda_{3}=\omega^{2}$, 其中

$$
\omega=e^{2\pi{i}/3}=-\frac{1}{2}+\frac{\sqrt{3}}{2}i.
$$

求 $\lambda=1$ 的特征向量.

$$
I-P=\left[\begin{array}{rrr}
1&-1&0\\
0&1&-1\\
-1&0&1
\end{array}\right]arrow
\left[\begin{array}{rrr}
1&-1&0\\
0&1&-1\\
0&0&0
\end{array}\right].
$$

解得 $x_{1}=x_{2}=x_{3}$.

基础解系: $\alpha_{1}=\left(1,1,1\right)^{\top}$.

求 $\lambda=\omega$ 的特征向量.

由第 $1$ 行: $\omega{x}_{1}-x_{2}=0$, 即 $x_{2}=\omega{x}_{1}$.

由第 $2$ 行: $\omega{x}_{2}-x_{3}=0$, 即 $x_{3}=\omega{x}_{2}=\omega^{2}x_{1}$.

基础解系: $\alpha_{2}=\left(1,\omega,\omega^{2}\right)^{\top}$.

求 $\lambda=\omega^{2}$ 的特征向量.

同理, 基础解系: $\alpha_{3}=\left(1,\omega^{2},\omega\right)^{\top}$.

$\blacksquare$

## 5.5-13

设 $A,B$ 分别是数域 $K$ 上 $s\times{n}$, $n\times{s}$ 矩阵, 证明: $AB$ 与 $BA$ 有相同的非零特征值.

### 解答 5.5-13

设 $\lambda\ne0$ 是 $AB$ 的一个特征值, $\alpha$ 是 $AB$ 的属于 $\lambda$ 的特征向量, 即

$$
AB\alpha=\lambda\alpha.
$$

令 $\beta=B\alpha$.

则

$$
BA\beta=BA\left(B\alpha\right)=B\left(AB\alpha\right)=B\left(\lambda\alpha\right)=\lambda\left(B\alpha\right)=\lambda\beta.
$$

证明 $\beta\ne0$.

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

因此 $AB$ 与 $BA$ 有相同的非零特征值.

$\blacksquare$

## 5.6-1

习题 5.5 的第 1, 2 题中, 哪些矩阵可对角化? 哪些矩阵不可对角化? 对于可对角化的矩阵 $A$, 求可逆矩阵 $P$, 使得 $P^{-1}AP$ 为对角矩阵, 并且写出这个对角矩阵.

### 解答 5.6-1

由**定理 5.6.1 (可对角化的充要条件)**, 数域 $K$ 上 $n$ 级矩阵 $A$ 可对角化的充分必要条件是 $A$ 有 $n$ 个线性无关的特征向量.

**习题 5.5 第 1 题(1)**: $A=\left[\begin{array}{rrr}2&2&-2\\2&5&-4\\-2&-4&5\end{array}\right]$.

特征值: $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=10$.

求 $\lambda=10$ 的特征向量:

$$
10I-A=\left[\begin{array}{rrr}
8&-2&2\\
-2&5&4\\
2&4&5
\end{array}\right]arrow
\left[\begin{array}{rrr}
2&4&5\\
0&9&9\\
0&0&0
\end{array}\right].
$$

解得 $x_{2}=-x_{3}$, $x_{1}=\frac{1}{2}x_{3}$.

基础解系: $\alpha_{1}=\left(1,-2,2\right)^{\top}$.

特征值 $\lambda=1$ 的特征向量:

$$
I-A=\left[\begin{array}{rrr}
-1&-2&2\\
-2&-4&4\\
2&4&-4
\end{array}\right]arrow
\left[\begin{array}{rrr}
1&2&-2\\
0&0&0\\
0&0&0
\end{array}\right].
$$

解得 $x_{1}=-2x_{2}+2x_{3}$.

基础解系: $\alpha_{2}=\left(-2,1,0\right)^{\top}$, $\alpha_{3}=\left(2,0,1\right)^{\top}$.

三个特征向量线性无关, 故 $A$ 可对角化.

$$
P=\left[\begin{array}{rrr}
1&-2&2\\
-2&1&0\\
2&0&1
\end{array}\right],
P^{-1}AP=\left[\begin{array}{rrr}
10&0&0\\
0&1&0\\
0&0&1
\end{array}\right].
$$

**习题 5.5 第 1 题(2)**: $A=\left[\begin{array}{rrr}2&3&2\\1&8&2\\-2&-14&-3\end{array}\right]$.

特征值: $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=3$.

$\lambda=3$ 的特征子空间维数为 $1$ (几何重数), 而代数重数为 $2$.

几何重数 $<$ 代数重数, 故 $A$ 不可对角化.

**习题 5.5 第 1 题(3)**: $A=\left[\begin{array}{rrr}6&2&4\\2&3&2\\4&2&6\end{array}\right]$.

特征值: $\lambda_{1}=2$, $\lambda_{2}=11$.

有两个不同的特征值, 且 $3$ 级矩阵有 $3$ 个线性无关的特征向量, 故可对角化.

**习题 5.5 第 1 题(4)**: $A=\left[\begin{array}{rrr}2&-1&2\\5&-3&3\\-1&0&-2\end{array}\right]$.

特征值: $\lambda=-1$ (三重根).

几何重数 $<3$, 故不可对角化.

**习题 5.5 第 1 题(5)**: $A=\left[\begin{array}{rrr}0&1/2&1/2\\1&-1/2&1/2\\1&-1/2&1/2\end{array}\right]$.

特征值: $\lambda_{1}=0$, $\lambda_{2}=1$, $\lambda_{3}=-1$.

三个不同的特征值, 故可对角化.

**习题 5.5 第 2 题(1)**: $A=\left[\begin{array}{rr}1&-\sqrt{3}\\\sqrt{3}&1\end{array}\right]$.

看成实数域上的矩阵, 没有实特征值, 故不可对角化.

看成复数域上的矩阵, 有两个不同的特征值, 故可对角化.

**习题 5.5 第 2 题(2)**: $A=\left[\begin{array}{rrr}3&7&-3\\-2&-5&2\\-4&-10&3\end{array}\right]$.

看成实数域上的矩阵, 只有 $1$ 个实特征值, 故不可对角化.

看成复数域上的矩阵, 有三个不同的特征值, 故可对角化.

以上判断均基于矩阵是否有 $n$ 个线性无关的特征向量.

$\blacksquare$

## 5.6-5

设 $A$ 是数域 $K$ 上的 $n$ 级矩阵. 证明: 如果 $K^{n}$ 中任意非零列向量都是 $A$ 的特征向量, 则 $A$ 一定是数量矩阵.

### 解答 5.6-5

假设 $A$ 不是数量矩阵.

则 $A$ 至少有两个不同的特征值 $\lambda_{1}\ne\lambda_{2}$.

设 $\alpha$ 是属于 $\lambda_{1}$ 的特征向量, $\beta$ 是属于 $\lambda_{2}$ 的特征向量.

不同特征值的特征向量线性无关.

因此 $\alpha+\beta\ne0$.

由题设, $\alpha+\beta$ 也是 $A$ 的特征向量.

设 $\alpha+\beta$ 属于特征值 $\lambda_{3}$.

则

$$
A\left(\alpha+\beta\right)=\lambda_{3}\left(\alpha+\beta\right).
$$

另一方面,

$$
A\left(\alpha+\beta\right)=A\alpha+A\beta=\lambda_{1}\alpha+\lambda_{2}\beta.
$$

因此

$$
\lambda_{1}\alpha+\lambda_{2}\beta=\lambda_{3}\alpha+\lambda_{3}\beta.
$$

即

$$
\left(\lambda_{1}-\lambda_{3}\right)\alpha+\left(\lambda_{2}-\lambda_{3}\right)\beta=0.
$$

因为 $\alpha,\beta$ 线性无关, 故

$$
\lambda_{1}-\lambda_{3}=0,\quad\lambda_{2}-\lambda_{3}=0.
$$

即 $\lambda_{1}=\lambda_{2}=\lambda_{3}$.

矛盾.

因此假设不成立, 即 $A$ 是数量矩阵.

$\blacksquare$

## 5.6-7

证明: 数域 $K$ 上 $n$ 级幂等矩阵 $A$ 一定可对角化, 并且 $A$ 的相似标准形是 $\operatorname{diag}\left\{I_{r},0\right\}$, 其中 $r=\operatorname{rank}\left(A\right)$.

### 解答 5.6-7

因为 $A^{2}=A$, 故 $A$ 的特征值只能是 $0$ 或 $1$.

证明 $A$ 可对角化.

$\ker\left(A\right)=\left\{x\mid{A}x=0\right\}$ 是属于特征值 $0$ 的特征子空间.

$$
\ker\left(I-A\right)=\left\{x\mid\left(I-A\right)x=0\right\}=\left\{x\mid{A}x=x\right\}
$$

是属于特征值 $1$ 的特征子空间.

我们证明

$$
K^{n}=\ker\left(A\right)\oplus\ker\left(I-A\right).
$$

对任意 $x\in{K}^{n}$,

$$
x=Ax+\left(I-A\right)x.
$$

因为 $A\left(Ax\right)=A^{2}x=Ax$, 故 $Ax\in\ker\left(I-A\right)$.

因为

$$
A\left(\left(I-A\right)x\right)=\left(A-A^{2}\right)x=0,
$$

故 $\left(I-A\right)x\in\ker\left(A\right)$.

因此

$$
K^{n}=\ker\left(A\right)+\ker\left(I-A\right).
$$

又因为

$$
\ker\left(A\right)\cap\ker\left(I-A\right)=\left\{0\right\}\,\left(\text{若~}Ax=0\text{~且~}Ax=x\text{,~则~}x=0\right).
$$

故

$$
K^{n}=\ker\left(A\right)\oplus\ker\left(I-A\right).
$$

因此 $A$ 有 $n$ 个线性无关的特征向量, 即可对角化.

求相似标准形.

$$
\dim\ker\left(A\right)=n-\operatorname{rank}\left(A\right).
$$

$$
\dim\ker\left(I-A\right)=\operatorname{rank}\left(A\right)=r.
$$

故 $A$ 有 $r$ 个特征值 $1$, $n-r$ 个特征值 $0$.

因此 $A$ 的相似标准形是 $\operatorname{diag}\left\{I_{r},0\right\}$, 其中 $r=\operatorname{rank}\left(A\right)$.

$\blacksquare$
