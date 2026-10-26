# 作业 22

> **定理1** (矩阵乘积的秩)<br>设 $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$, 则
> $$
> \text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
> $$

> **命题2** (实数域上秩的等式)<br>设 $A$ 是实数域上 $s\times n$ 矩阵, 则:
> 
> $$
> \text{rank}\left(A^{\top}A\right)=\text{rank}\left(AA^{\top}\right)=\text{rank}\left(A\right)
> $$

### 习题一

(习题 4.5-1) 证明: 设 $A,B$ 分别是 $s\times n$, $n\times m$ 矩阵. 如果 $AB=0$, 则 $\text{rank}\left(A\right)+\text{rank}\left(B\right)\le n$.

### 解答 习题一

由**定理1** (矩阵乘积的秩),

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

设 $B$ 的列向量组为 $\beta_{1},\beta_{2},\cdots,\beta_{m}$.

$AB=0$ 意味着 $A\beta_{j}=0$ ( $j=1,2,\cdots,m$ ).

所以每个 $\beta_{j}$ 都是齐次线性方程组 $Ax=0$ 的解.

因此 $B$ 的列空间 $\subseteq Ax=0$ 的解空间 $W$.

故

$$
\text{rank}\left(B\right)=\dim\left\langle\beta_{1},\cdots,\beta_{m}\right\rangle\le\dim W=n-\text{rank}\left(A\right).
$$

因此

由**定理1** (矩阵乘积的秩),

$$
\text{rank}\left(A\right)+\text{rank}\left(B\right)\le n.
$$

$\blacksquare$

### 习题二

(习题 4.5-4) 证明: 如果 $n$ 级矩阵 $A$ 满足 $A^{2}=I$ (此时称 $A$ 是对合矩阵), 则

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

### 解答 习题二

由**定理1** (矩阵乘积的秩), 因为 $A^{2}=I$, 所以

$$
\left(I+A\right)\left(I-A\right)=I-A^{2}=I-I=0.
$$

由习题 4.5 第 1 题的结论,

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)\le n.
$$

另一方面,

$$
\left(I+A\right)+\left(I-A\right)=2I.
$$

由秩的不等式,

$$
\text{rank}\left(2I\right)\le\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right).
$$

$\text{rank}\left(2I\right)=n$, 故

$$
n\le\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right).
$$

因此

由**定理1** (矩阵乘积的秩),

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

$\blacksquare$

### 习题三

(习题 4.5-5) 证明: 如果 $n$ 级矩阵 $A$ 满足 $A^{2}=A$ (此时称 $A$ 是幂等矩阵), 则

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

### 解答 习题三

由**定理1** (矩阵乘积的秩), 因为 $A^{2}=A$, 所以

$$
A\left(I-A\right)=A-A^{2}=A-A=0.
$$

由习题 4.5 第 1 题的结论,

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)\le n.
$$

另一方面,

$$
A+\left(I-A\right)=I.
$$

由秩的不等式,

$$
\text{rank}\left(I\right)\le\text{rank}\left(A\right)+\text{rank}\left(I-A\right).
$$

$\text{rank}\left(I\right)=n$, 故

$$
n\le\text{rank}\left(A\right)+\text{rank}\left(I-A\right).
$$

因此

由**定理1** (矩阵乘积的秩),

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

$\blacksquare$

### 习题四

(习题 4.5-6) 设 $A$ 是实数域上的 $s\times n$ 矩阵, $\beta$ 是 $\mathbb{R}^{s}$ 的任意一个列向量. 证明: $n$ 元线性方程组 $A^{\top}AX=A^{\top}\beta$ 一定有解.

### 解答 习题四

由**命题2** (实数域上秩的等式), 对于实数域上的矩阵,

$$
\text{rank}\left(A^{\top}A\right)=\text{rank}\left(A\right).
$$

增广矩阵为 $\left(A^{\top}A,A^{\top}\beta\right)=A^{\top}\left(A,\beta\right)$.

因此

$$
\text{rank}\left(A^{\top}A,A^{\top}\beta\right)=\text{rank}\left(A^{\top}\left(A,\beta\right)\right)\le\text{rank}\left(A^{\top}\right)=\text{rank}\left(A\right).
$$

另一方面, $A^{\top}A$ 是 $\left(A^{\top}A,A^{\top}\beta\right)$ 的子矩阵, 故

$$
\text{rank}\left(A^{\top}A\right)\le\text{rank}\left(A^{\top}A,A^{\top}\beta\right).
$$

因此

$$
\text{rank}\left(A^{\top}A\right)\le\text{rank}\left(A^{\top}A,A^{\top}\beta\right)\le\text{rank}\left(A\right)=\text{rank}\left(A^{\top}A\right).
$$

所以

$$
\text{rank}\left(A^{\top}A\right)=\text{rank}\left(A^{\top}A,A^{\top}\beta\right).
$$

系数矩阵与增广矩阵有相同的秩, 故该方程组有解. $\blacksquare$

### 习题五

(习题 4.5-9) 设 $A$ 是 $n$ 级矩阵 ( $n\ge2$ ), 证明:

$$
\text{rank}\left(A^{*}\right)=
\begin{cases}
n, & \text{当 }\text{rank}\left(A\right)=n;\\
1, & \text{当 }\text{rank}\left(A\right)=n-1;\\
0, & \text{当 }\text{rank}\left(A\right)< n-1.
\end{cases}
$$

### 解答 习题五

由**定理1** (矩阵乘积的秩),

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

分三种情况讨论.

**当 $\text{rank}\left(A\right)=n$ 时**: $\left|A\right|\ne0$.

由 $AA^{*}=\left|A\right|I$, 得 $\left|A\right|\left|A^{*}\right|=\left|A\right|^{n}$.

故 $\left|A^{*}\right|=\left|A\right|^{n-1}\ne0$, 因此 $\text{rank}\left(A^{*}\right)=n$.

**当 $\text{rank}\left(A\right)=n-1$ 时**: $\left|A\right|=0$.

故 $AA^{*}=\left|A\right|I=0$.

由习题 4.5 第 1 题, $\text{rank}\left(A\right)+\text{rank}\left(A^{*}\right)\le n$.

即 $\left(n-1\right)+\text{rank}\left(A^{*}\right)\le n$, 故 $\text{rank}\left(A^{*}\right)\le1$.

又因为 $\text{rank}\left(A\right)=n-1$, 所以 $A$ 有一个 $n-1$ 阶子式非零. 这个 $n-1$ 阶子式就是某个代数余子式, 故 $A^{*}\ne0$, 从而 $\text{rank}\left(A^{*}\right)\ge1$.

因此 $\text{rank}\left(A^{*}\right)=1$.

**当 $\text{rank}\left(A\right)< n-1$ 时**: $A$ 的所有 $n-1$ 阶子式都为零.

故所有代数余子式都为零, 即 $A^{*}=0$.

因此 $\text{rank}\left(A^{*}\right)=0$.

$\blacksquare$

### 习题六

(习题 4.5-15) 设 $A,B,C,D$ 都是 $n$ 级矩阵, 并且 $\left|A\right|\ne0$, $AC=CA$. 证明:

$$
\left|\begin{array}{cc}A & B\\C & D\end{array}\right|=\left|AD-CB\right|.
$$

### 解答 习题六

由**定理1** (矩阵乘积的秩)的思路, 因为 $\left|A\right|\ne0$, 所以 $A$ 可逆.

作分块矩阵的初等行变换: 用 $-CA^{-1}$ 左乘第 $1$ 块行, 加到第 $2$ 块行上.

$$
\left|\begin{array}{cc}A & B\\C & D\end{array}\right|
=
\left|\begin{array}{cc}A & B\\0 & D-CA^{-1}B\end{array}\right|.
$$

这是分块上三角矩阵, 行列式等于主对角线上子矩阵行列式的乘积:

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
