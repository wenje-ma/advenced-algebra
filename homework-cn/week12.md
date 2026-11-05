# week12

> **定义 4.1.1 (矩阵的加法)**
> 
> 设 $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ 都是数域 $K$ 上 $s\times n$ 矩阵, 令 $C=\left(a_{ij}+b_{ij}\right)_{s\times n}$, 则称 $C$ 是矩阵 $A$ 与 $B$ 的和, 记作 $C=A+B$.

> **定义 4.1.2 (矩阵的数量乘法)**
> 
> 设 $k\in K$, 令 $M=\left(ka_{ij}\right)_{s\times n}$, 则称 $M$ 是 $k$ 与矩阵 $A$ 的数量乘积, 记作 $M=kA$.

> **定义 4.1.3 (矩阵的乘法)**
> 
> 设 $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$, 令 $C=\left(c_{ij}\right)_{s\times m}$, 其中 $c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}$, 则称 $C$ 是 $A$ 与 $B$ 的乘积, 记作 $C=AB$.

> **定义 4.2.2 (上/下三角矩阵)**
> 
> 主对角线下 (上) 方元素全为零的方阵称为上 (下) 三角矩阵.

> **定义 4.2.3 (基本矩阵)**
> 
> 只有一个元素是 $1$, 其余元素全为零的矩阵称为基本矩阵. $\left(i,j\right)$ 元为 $1$ 的基本矩阵记作 $E_{ij}$.

> **定义 4.2.5 (对称矩阵)**
> 
> 一个矩阵 $A$ 如果满足 $A^{\top}=A$, 则称 $A$ 是对称矩阵.

> **定义 4.2.6 (斜对称矩阵)**
> 
> 一个矩阵 $A$ 如果满足 $A^{\top}=-A$, 则称 $A$ 是斜 (反) 对称矩阵.

$$
\left|\begin{array}{ccc}
1 & 1 & 1\\
x_{1} & x_{2} & x_{3}\\
x_{1}^{2} & x_{2}^{2} & x_{3}^{2}
\end{array}\right|=\left(x_{2}-x_{1}\right)\left(x_{3}-x_{1}\right)\left(x_{3}-x_{2}\right).
$$

> **定理 4.3.1 (矩阵乘积的秩)**
> 
> 设 $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$, 则

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

> **命题 4.3.2 (实矩阵 $A^{\top}Az=0$ 与 $z=0$ 同解)**
> 
> 设 $A$ 是实数域上的矩阵, 则齐次线性方程组 $A^{\top}Az=0$ 与 $z=0$ 同解.

> **定理 4.3.3 (乘积的行列式)**
> 
> 设 $A,B$ 都是 $n$ 级矩阵, 则 $\left|AB\right|=\left|A\right|\left|B\right|$.

## 4.1-6

计算:

$$
\left(x,y,1\right)\left[\begin{array}{ccc}
a_{11} & a_{12} & a_{1}\\
a_{12} & a_{22} & a_{2}\\
a_{1} & a_{2} & a_{0}
\end{array}\right]\left[\begin{array}{c}
x\\
y\\
1
\end{array}\right].
$$

### 解答 4.1-6

由**定义 4.1.3 (矩阵的乘法)**, 先算左边的行向量乘矩阵:

$$
\left(x,y,1\right)M
=
\left(a_{11}x+a_{12}y+a_{1},a_{12}x+a_{22}y+a_{2},a_{1}x+a_{2}y+a_{0}\right).
$$

再乘列向量:

$$
=\left(a_{11}x+a_{12}y+a_{1}\right)x+\left(a_{12}x+a_{22}y+a_{2}\right)y+\left(a_{1}x+a_{2}y+a_{0}\right)=a_{11}x^{2}+2a_{12}xy+a_{22}y^{2}+2a_{1}x+2a_{2}y+a_{0}.
$$

$\blacksquare$

## 4.1-7(5)

计算:

$$
\left[\begin{array}{ccc}
0 & 1 & 0\\
0 & 0 & 1\\
0 & 0 & 0
\end{array}\right]^{n},n\text{ 是正整数}.
$$

### 解答 4.1-7(5)

由**定义 4.1.3 (矩阵的乘法)**, 记

$$
H=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right].
$$

$$
H^{2}=HH=\left[\begin{array}{ccc}
0 & 0 & 1\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

$$
H^{3}=H^{2}H=\left[\begin{array}{ccc}
0 & 0 & 0\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

因此:

- 当 $n=1$ 时, $H^{n}=H=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right]$.
- 当 $n=2$ 时, $H^{n}=\left[\begin{array}{ccc}0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]$.
- 当 $n\ge3$ 时, $H^{n}=0$.

$\blacksquare$

## 4.1-7(6)

计算:

$$
\left[\begin{array}{ccc}
\lambda & 1 & 0\\
0 & \lambda & 1\\
0 & 0 & \lambda
\end{array}\right]^{n},n\text{ 是正整数}.
$$

### 解答 4.1-7(6)

由**定义 4.1.3 (矩阵的乘法)**, 记 $A=\lambda I+N$, 其中

$$
N=\left[\begin{array}{ccc}0 & 1 & 0\\0 & 0 & 1\\0 & 0 & 0\end{array}\right].
$$

因为 $\lambda I$ 与 $N$ 可交换, 由矩阵二项式定理:

$$
A^{n}=\sum_{k=0}^{n}\binom{n}{k}\left(\lambda I\right)^{n-k}N^{k}.
$$

又 $N^{0}=I$, $N^{1}=N$, $N^{2}=\left[\begin{array}{ccc}0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]$, $N^{3}=0$.

故

$$
A^{n}
=\lambda^{n}I+n\lambda^{n-1}N+\binom{n}{2}\lambda^{n-2}N^{2}=\left[\begin{array}{ccc}
\lambda^{n} & n\lambda^{n-1} & \frac{n\left(n-1\right)}{2}\lambda^{n-2}\\
0 & \lambda^{n} & n\lambda^{n-1}\\
0 & 0 & \lambda^{n}
\end{array}\right].
$$

当 $n=1$ 时, 上式也成立 (注意 $\lambda^{0}=1$, 第三项为 $0$). $\blacksquare$

## 4.1-10

证明: 如果 $A=\frac{1}{2}\left(B+I\right)$, 则 $A^{2}=A$ 当且仅当 $B^{2}=I$.

### 解答 4.1-10

$$
A^{2}=\left(\frac{1}{2}\left(B+I\right)\right)^{2}=\frac{1}{4}\left(B+I\right)^{2}=\frac{1}{4}\left(B^{2}+2B+I\right).
$$

$A^{2}=A$ 等价于:

$$
\frac{1}{4}\left(B^{2}+2B+I\right)=\frac{1}{2}\left(B+I\right).
$$

两边乘 $4$:

$$
B^{2}+2B+I=2B+2I.
$$

化简得:

$$
B^{2}=I.
$$

因此 $A^{2}=A$ 当且仅当 $B^{2}=I$. $\blacksquare$

## 4.2-2

证明: 两个 $n$ 级下三角矩阵的乘积仍是 $n$ 级下三角矩阵, 并且乘积矩阵的主对角元等于因子矩阵的相应主对角元的乘积.

### 解答 4.2-2

由**定义 4.2.2 (上/下三角矩阵)**, 设 $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ 都是 $n$ 级下三角矩阵, 即当 $i< j$ 时, $a_{ij}=0,b_{ij}=0$.

设 $C=AB=\left(c_{ij}\right)$, 则

$$
c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}.
$$

下三角性. 当 $i< j$ 时:

- 若 $k\le i< j$, 则 $k< j$, 故 $b_{kj}=0$.
- 若 $k> i$, 则 $a_{ik}=0$.

因此所有项均为 $0$, 故 $c_{ij}=0$ (当 $i< j$). 由**定义 4.2.2 (上/下三角矩阵)**, 所以 $C$ 是下三角矩阵.

主对角元. 当 $i=j$ 时:

- 若 $k< i$, 则 $b_{ki}=0$.
- 若 $k> i$, 则 $a_{ik}=0$.

因此只有 $k=i$ 这一项非零:

$$
c_{ii}=a_{ii}b_{ii}.
$$

$\blacksquare$

## 4.2-3

证明: 与所有 $n$ 级矩阵可交换的矩阵一定是 $n$ 级数量矩阵.

### 解答 4.2-3

设 $A=\left(a_{ij}\right)$ 与所有 $n$ 级矩阵可交换.

取**定义 4.2.3 (基本矩阵)**中的基本矩阵 $E_{ij}$ (第 $i$ 行第 $j$ 列为 $1$, 其余为 $0$). 则 $AE_{ij}=E_{ij}A$.

$AE_{ij}$ 的第 $j$ 列等于 $A$ 的第 $i$ 列, 其余列为 $0$.

$E_{ij}A$ 的第 $i$ 行等于 $A$ 的第 $j$ 行, 其余行为 $0$.

比较两者的 $\left(i,j\right)$ 元:

$AE_{ij}$ 的 $\left(i,j\right)$ 元 $=a_{ii}$.

$E_{ij}A$ 的 $\left(i,j\right)$ 元 $=a_{jj}$.

因此 $a_{ii}=a_{jj}$.

这对所有 $i,j$ 都成立, 故所有主对角元相等:

$$
a_{11}=a_{22}=\cdots=a_{nn}=k.
$$

再比较 $\left(k,j\right)$ 元 ( $k\ne i$ ):

$AE_{ij}$ 的 $\left(k,j\right)$ 元 $=a_{ki}$.

$E_{ij}A$ 的 $\left(k,j\right)$ 元 $=0$ (因为 $k\ne i$).

因此 $a_{ki}=0$ (当 $k\ne i$).

这对所有 $i$ 都成立, 故 $A$ 的非对角元全为 $0$.

因此 $A=kI$, 即 $A$ 是数量矩阵. $\blacksquare$

## 4.2-8

证明: 数域 $K$ 上任一 $n$ 级矩阵都可以表示成一个对称矩阵与一个斜对称矩阵之和, 并且表法唯一.

### 解答 4.2-8

设 $A$ 是任一 $n$ 级矩阵. 令

$$
S=\frac{1}{2}\left(A+A^{\top}\right),
K=\frac{1}{2}\left(A-A^{\top}\right).
$$

则 $A=S+K$.

$$
S^{\top}=\frac{1}{2}\left(A^{\top}+\left(A^{\top}\right)^{\top}\right)=\frac{1}{2}\left(A^{\top}+A\right)=S.
$$

由**定义 4.2.5 (对称矩阵)**, 故 $S$ 是对称矩阵.

$$
K^{\top}=\frac{1}{2}\left(A^{\top}-\left(A^{\top}\right)^{\top}\right)=\frac{1}{2}\left(A^{\top}-A\right)=-K.
$$

由**定义 4.2.6 (斜对称矩阵)**, 故 $K$ 是斜对称矩阵.

唯一性. 设 $A=S_{1}+K_{1}=S_{2}+K_{2}$, 其中 $S_{1},S_{2}$ 对称, $K_{1},K_{2}$ 斜对称.

则 $S_{1}-S_{2}=K_{2}-K_{1}$.

左边 $\left(S_{1}-S_{2}\right)^{\top}=S_{1}-S_{2}$, 是对称矩阵.

右边

$$
\left(K_{2}-K_{1}\right)^{\top}=-K_{2}+K_{1}=-\left(K_{2}-K_{1}\right),
$$

是斜对称矩阵.

一个矩阵既是对称的又是斜对称的, 故它必为零矩阵.

因此 $S_{1}-S_{2}=0$, $K_{2}-K_{1}=0$, 即 $S_{1}=S_{2}$, $K_{1}=K_{2}$.

表法唯一. $\blacksquare$

## 4.2-9

证明: 如果 $A$ 是实数域上的 $n$ 级对称矩阵, 并且 $A^{2}=0$, 则 $A=0$.

### 解答 4.2-9

设 $A=\left(a_{ij}\right)$ 是实对称矩阵, $A^{2}=0$.

考虑 $A^{2}$ 的主对角元:

$$
\left(A^{2}\right)_{ii}=\sum_{k=1}^{n}a_{ik}a_{ki}.
$$

由**定义 4.2.5 (对称矩阵)**, $A$ 对称, 所以 $a_{ki}=a_{ik}$.

故

$$
\left(A^{2}\right)_{ii}=\sum_{k=1}^{n}a_{ik}^{2}.
$$

因为 $A^{2}=0$, 所以 $\left(A^{2}\right)_{ii}=0$, 即

$$
\sum_{k=1}^{n}a_{ik}^{2}=0.
$$

因为 $a_{ik}$ 都是实数, 故 $a_{ik}^{2}\ge0$.

因此每个 $a_{ik}=0$, 即 $A=0$. $\blacksquare$

## 4.2-10

证明: 数域 $K$ 上奇数级斜对称矩阵的行列式等于零.

### 解答 4.2-10

设 $A$ 是 $n$ 级斜对称矩阵, $n$ 为奇数.

由**定义 4.2.6 (斜对称矩阵)**, 则 $A^{\top}=-A$.

$$
\left|A^{\top}\right|=\left|-A\right|.
$$

因为 $\left|A^{\top}\right|=\left|A\right|$, 且 $\left|-A\right|=\left(-1\right)^{n}\left|A\right|$.

所以

$$
\left|A\right|=\left(-1\right)^{n}\left|A\right|.
$$

因为 $n$ 为奇数, 故 $\left(-1\right)^{n}=-1$.

因此

$$
\left|A\right|=-\left|A\right|\Rightarrow 2\left|A\right|=0\Rightarrow \left|A\right|=0.
$$

$\blacksquare$

## 4.3-2

一个矩阵称为行 (列) 满秩矩阵, 如果它的行 (列) 向量组是线性无关的. 证明: 如果一个 $s\times n$ 矩阵 $A$ 的秩为 $r$, 则有 $s\times r$ 的列满秩矩阵 $B$ 和 $r\times n$ 的行满秩矩阵 $C$, 使得 $A=BC$.

### 解答 4.3-2

由**定理 4.3.1 (矩阵乘积的秩)**的思路, 把 $A$ 经过初等行变换化成简化行阶梯形矩阵 $J$.

因为 $\text{rank}\left(A\right)=r$, 所以 $J$ 有 $r$ 个非零行.

设

$$
J=\left[\begin{array}{c}C\\0\end{array}\right]
$$

其中 $C$ 是 $r\times n$ 矩阵, 且 $C$ 的行向量组线性无关 (因为 $J$ 的非零行线性无关).

故 $C$ 是行满秩矩阵.

设 $A=PJ$, 其中 $P$ 是 $s\times s$ 可逆矩阵.

则 $A=P\left[\begin{array}{c}C\\0\end{array}\right]$.

把 $P$ 按列分块: $P=\left(P_{1},P_{2}\right)$, 其中 $P_{1}$ 是 $s\times r$ 矩阵.

则

$$
A=\left(P_{1},P_{2}\right)\left[\begin{array}{c}C\\0\end{array}\right]=P_{1}C.
$$

令 $B=P_{1}$.

因为 $P$ 可逆, 所以 $P$ 的列向量组线性无关, 从而 $P_{1}$ 的列向量组也线性无关.

故 $B$ 是列满秩矩阵.

因此 $A=BC$, 其中 $B$ 是 $s\times r$ 列满秩矩阵, $C$ 是 $r\times n$ 行满秩矩阵. $\blacksquare$
