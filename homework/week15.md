# week15

> **定理 3.7.1 (齐次线性方程组解空间的维数)**
> 
> 数域 $K$ 上 $n$ 元齐次线性方程组 $Ax=0$ 的解空间 $W$ 的维数为 $\dim{}W=n-\text{rank}\left(A\right)$.

> **定理 4.3.1 (矩阵乘积的秩)**
> 
> 设 $A=\left(a_{ij}\right)_{s\times{}n}$, $B=\left(b_{ij}\right)_{n\times{}m}$, 则 $\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}$.

> **命题 4.5.2 (实数域上秩的等式)**
> 
> 设 $A$ 是实数域上 $s\times{}n$ 矩阵, 则 $\text{rank}\left(A^{\top}A\right)=\text{rank}\left(AA^{\top}\right)=\text{rank}\left(A\right)$. $\beta_{i}=\alpha_{i}-\sum_{k=1}^{i-1}\frac{\left(\alpha_{i},\beta_{k}\right)}{\left(\beta_{k},\beta_{k}\right)}\beta_{k}$, 则 $\beta_{1},\beta_{2},\cdots,\beta_{m}$ 是正交向量组, 且与原向量组等价.

> **定义 4.6.1 (正交矩阵)**
> 
> 实数域上的方阵 $A$ 如果满足 $A^{\top}A=I$, 则称 $A$ 是正交矩阵. ## 4.5-1 证明: 设 $A,B$ 分别是 $s\times{}n$, $n\times{}m$ 矩阵. 如果 $AB=0$, 则 $\text{rank}\left(A\right)+\text{rank}\left(B\right)\le{}n$. 设 $B$ 的列向量组为 $\beta_{1},\beta_{2},\cdots,\beta_{m}$. $AB=0$ 意味着 $A\beta_{j}=0$ ( $j=1,2,\cdots,m$ ). 所以每个 $\beta_{j}$ 都是齐次线性方程组 $Ax=0$ 的解. 因此 $B$ 的列空间 $\subseteq{}Ax=0$ 的解空间 $W$. 由**定理 3.7.1 (齐次线性方程组解空间的维数)**, $$\text{rank}\left(B\right)=\dim\left\langle\beta_{1},\cdots,\beta_{m}\right\rangle\le\dim{}W=n-\text{rank}\left(A\right).$$ 因此 $$\text{rank}\left(A\right)+\text{rank}\left(B\right)\le{}n.$$ $\blacksquare$

## 4.5-15

设 $A,B,C,D$ 都是 $n$ 级矩阵, 并且 $\left|A\right|\ne0$, $AC=CA$. 证明:

$$
\left|\begin{array}{cc}A&B\\C&D\end{array}\right|=\left|AD-CB\right|.
$$

### 解答 4.5-15

因为 $\left|A\right|\ne0$, 所以 $A$ 可逆.

作分块矩阵的初等行变换: 用 $-CA^{-1}$ 左乘第 $1$ 块行, 加到第 $2$ 块行上.

$$
\left|\begin{array}{cc}A&B\\C&D\end{array}\right|
=
\left|\begin{array}{cc}A&B\\0&D-CA^{-1}B\end{array}\right|.
$$

这是分块上三角矩阵, 由分块上三角矩阵的行列式, 行列式等于主对角线上子矩阵行列式的乘积:

$$
=\left|A\right|\cdot\left|D-CA^{-1}B\right|.
$$

因为 $AC=CA$, 所以 $CA^{-1}=A^{-1}C$.

故

$$
D-CA^{-1}B=D-A^{-1}CB.
$$

因此

$$
\left|D-CA^{-1}B\right|
=\left|D-A^{-1}CB\right|
=\left|A^{-1}\left(AD-CB\right)\right|
=\left|A^{-1}\right|\cdot\left|AD-CB\right|
=\frac{1}{\left|A\right|}\cdot\left|AD-CB\right|.
$$

所以

$$
\left|A\right|\cdot\left|D-CA^{-1}B\right|
=\left|A\right|\cdot\frac{1}{\left|A\right|}\cdot\left|AD-CB\right|
=\left|AD-CB\right|.
$$

$\blacksquare$

## 4.6-1(3)

判断下列矩阵是否为正交矩阵:

$$
A=\left[\begin{array}{rr}
\sqrt{3}/2&1/2\\
1/2&-\sqrt{3}/2
\end{array}\right].
$$

### 解答 4.6-1(3)

由**定义 4.6.1 (正交矩阵)**, 计算 $A^{\top}A$:

$$
A^{\top}A=\left[\begin{array}{rr}
\sqrt{3}/2&1/2\\
1/2&-\sqrt{3}/2
\end{array}\right]\left[\begin{array}{rr}
\sqrt{3}/2&1/2\\
1/2&-\sqrt{3}/2
\end{array}\right].
$$

$\left(1,1\right)$ 元:

$$
\left(\frac{\sqrt{3}}{2}\right)^{2}+\left(\frac{1}{2}\right)^{2}=\frac{3}{4}+\frac{1}{4}=1.
$$

$\left(1,2\right)$ 元:

$$
\frac{\sqrt{3}}{2}\cdot\frac{1}{2}+\frac{1}{2}\cdot\left(-\frac{\sqrt{3}}{2}\right)=\frac{\sqrt{3}}{4}-\frac{\sqrt{3}}{4}=0.
$$

$\left(2,1\right)$ 元:

$$
\frac{1}{2}\cdot\frac{\sqrt{3}}{2}+\left(-\frac{\sqrt{3}}{2}\right)\cdot\frac{1}{2}=\frac{\sqrt{3}}{4}-\frac{\sqrt{3}}{4}=0.
$$

$\left(2,2\right)$ 元:

$$
\left(\frac{1}{2}\right)^{2}+\left(-\frac{\sqrt{3}}{2}\right)^{2}=\frac{1}{4}+\frac{3}{4}=1.
$$

因此 $A^{\top}A=I$, 由**定义 4.6.1 (正交矩阵)**, 故 $A$ 是正交矩阵.

$\blacksquare$

## 4.6-1(8)

判断下列矩阵是否为正交矩阵:

$$
A=\left[\begin{array}{rr}
1&1\\
1&-1
\end{array}\right].
$$

### 解答 4.6-1(8)

由**定义 4.6.1 (正交矩阵)**, 计算 $A^{\top}A$:

$$
A^{\top}A=\left[\begin{array}{rr}
1&1\\
1&-1
\end{array}\right]\left[\begin{array}{rr}
1&1\\
1&-1
\end{array}\right]
=\left[\begin{array}{rr}
2&0\\
0&2
\end{array}\right].
$$

显然 $A^{\top}A\ne{}I$, 由**定义 4.6.1 (正交矩阵)**, 故 $A$ 不是正交矩阵.

$\blacksquare$

## 4.6-3

证明: 如果 $A$ 是实数域上 $n$ 级对称矩阵, $T$ 是 $n$ 级正交矩阵, 则 $T^{-1}AT$ 是对称矩阵.

### 解答 4.6-3

由**定义 4.6.1 (正交矩阵)**, 因为 $T$ 是正交矩阵, 故 $T^{-1}=T^{\top}$.

$$
\left(T^{-1}AT\right)^{\top}=T^{\top}A^{\top}\left(T^{-1}\right)^{\top}.
$$

因为 $T$ 是正交矩阵, 故 $T^{-1}=T^{\top}$, 从而 $\left(T^{-1}\right)^{\top}=\left(T^{\top}\right)^{\top}=T$.

因此

$$
\left(T^{-1}AT\right)^{\top}=T^{\top}A^{\top}T.
$$

因为 $A$ 是对称矩阵, 故 $A^{\top}=A$.

所以

$$
\left(T^{-1}AT\right)^{\top}=T^{\top}AT=T^{-1}AT.
$$

因此 $T^{-1}AT$ 是对称矩阵.

$\blacksquare$

## 4.6-5

证明: 如果正交矩阵 $A$ 是上三角矩阵, 则 $A$ 一定是对角矩阵, 并且其主对角元是 $1$ 或 $-1$.

### 解答 4.6-5

由**定义 4.6.1 (正交矩阵)**, 设 $A$ 是 $n$ 级上三角矩阵, 且 $A^{\top}A=I$.

因为 $A$ 是上三角矩阵, 故 $A^{\top}$ 是下三角矩阵.

$A^{\top}A=I$ 是对角矩阵.

归纳证明 $A$ 的非对角元都为零.

当 $i=1,j=2$ 时, 考虑 $A^{\top}A$ 的 $\left(1,2\right)$ 元:

$$
\sum_{k=1}^{n}\left(A^{\top}\right)_{1k}A_{k2}=\sum_{k=1}^{n}A_{k1}A_{k2}=0.
$$

因为 $A$ 是上三角矩阵, 所以当 $k>1$ 时 $A_{k1}=0$. 故上式化为 $A_{11}A_{12}=0$.

因为 $A$ 可逆, 故 $A_{11}\ne0$, 从而 $A_{12}=0$.

同理可证 $A_{1j}=0$ ( $j>1$ ).

假设第 $1,\cdots,i-1$ 行的非对角元都已证明为零.

考虑 $A^{\top}A$ 的 $\left(i,j\right)$ 元 ( $i<{}j$ ):

$$
\sum_{k=1}^{i}A_{ki}A_{kj}=0.
$$

由归纳假设, 当 $k<{}i$ 时 $A_{ki}=0$. 故上式化为 $A_{ii}A_{ij}=0$.

因为 $A_{ii}\ne0$, 故 $A_{ij}=0$.

归纳完成. 因此 $A$ 是对角矩阵.

$A^{\top}A=I$, 得 $A_{ii}^{2}=1$, 故 $A_{ii}=\pm1$.

$\blacksquare$

## 4.6-12

在欧几里得空间 $\mathbb{R}^{4}$ 中, 设向量组

$$
\alpha_{1}=\begin{bmatrix}1\\1\\0\\0\end{bmatrix},
\alpha_{2}=\begin{bmatrix}1\\0\\1\\0\end{bmatrix},
\alpha_{3}=\begin{bmatrix}1\\0\\0\\-1\end{bmatrix}.
$$

求与 $\alpha_{1},\alpha_{2},\alpha_{3}$ 等价的正交单位向量组.

### 解答 4.6-12

由施密特正交化方法.

令 $\beta_{1}=\alpha_{1}=\left(1,1,0,0\right)^{\top}$.

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}.
$$

$\left(\alpha_{2},\beta_{1}\right)=1$, $\left(\beta_{1},\beta_{1}\right)=2$.

故

$$
\beta_{2}=\left(1,0,1,0\right)^{\top}-\frac{1}{2}\left(1,1,0,0\right)^{\top}=\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{\top}.
$$

$$
\beta_{3}=\alpha_{3}-\frac{\left(\alpha_{3},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}-\frac{\left(\alpha_{3},\beta_{2}\right)}{\left(\beta_{2},\beta_{2}\right)}\beta_{2}.
$$

$\left(\alpha_{3},\beta_{1}\right)=1$, $\left(\alpha_{3},\beta_{2}\right)=\frac{1}{2}$, $\left(\beta_{2},\beta_{2}\right)=\frac{3}{2}$.

故

$$
\beta_{3}
=\left(1,0,0,-1\right)^{\top}-\frac{1}{2}\left(1,1,0,0\right)^{\top}-\frac{1}{3}\left(\frac{1}{2},-\frac{1}{2},1,0\right)^{\top}=\left(\frac{1}{3},-\frac{1}{3},-\frac{1}{3},-1\right)^{\top}.
$$

验证正交性: $\left(\beta_{1},\beta_{2}\right)=0$, $\left(\beta_{1},\beta_{3}\right)=0$, $\left(\beta_{2},\beta_{3}\right)=0$.

单位化:

$$
\eta_{1}=\frac{\beta_{1}}{\left|\beta_{1}\right|}=\left(\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}},0,0\right)^{\top}.
$$

$$
\eta_{2}=\frac{\beta_{2}}{\left|\beta_{2}\right|}=\left(\frac{1}{\sqrt{6}},-\frac{1}{\sqrt{6}},\frac{2}{\sqrt{6}},0\right)^{\top}.
$$

$$
\eta_{3}=\frac{\beta_{3}}{\left|\beta_{3}\right|}=\left(\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{1}{2\sqrt{3}},-\frac{\sqrt{3}}{2}\right)^{\top}.
$$

$\blacksquare$
