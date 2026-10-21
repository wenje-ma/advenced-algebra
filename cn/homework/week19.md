# 作业 19

> **定义2** (上/下三角矩阵)<br>主对角线下 (上) 方元素全为零的方阵称为上 (下) 三角矩阵.

### 习题一

(习题 4.2-2) 证明: 两个 $n$ 级下三角矩阵的乘积仍是 $n$ 级下三角矩阵, 并且乘积矩阵的主对角元等于因子矩阵的相应主对角元的乘积.

### 解答 习题一

由**定义2** (上/下三角矩阵), 设 $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ 都是 $n$ 级下三角矩阵, 即当 $i<j$ 时, $a_{ij}=0,b_{ij}=0$.

设 $C=AB=\left(c_{ij}\right)$, 则

$$
c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}
$$

**下三角性**. 当 $i<j$ 时:

- 若 $k\le i<j$, 则 $k<j$, 故 $b_{kj}=0$.
- 若 $k>i$, 则 $a_{ik}=0$.

因此所有项均为 $0$, 故 $c_{ij}=0$ (当 $i<j$). 由**定义2**, 所以 $C$ 是下三角矩阵.

**主对角元**. 当 $i=j$ 时:

- 若 $k<i$, 则 $b_{ki}=0$.
- 若 $k>i$, 则 $a_{ik}=0$.

因此只有 $k=i$ 这一项非零:

$$
c_{ii}=a_{ii}b_{ii}.
$$

$\blacksquare$

### 习题二

(习题 4.2-3) 证明: 与所有 $n$ 级矩阵可交换的矩阵一定是 $n$ 级数量矩阵.

### 解答 习题二

由**定义2** (上/下三角矩阵)的思路, 用基本矩阵测试可交换性. 设 $A=\left(a_{ij}\right)$ 与所有 $n$ 级矩阵可交换.

取基本矩阵 $E_{ij}$ (第 $i$ 行第 $j$ 列为 $1$, 其余为 $0$). 则 $AE_{ij}=E_{ij}A$.

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

### 习题三

(习题 4.2-8) 证明: 数域 $K$ 上任一 $n$ 级矩阵都可以表示成一个对称矩阵与一个斜对称矩阵之和, 并且表法唯一.

### 解答 习题三

设 $A$ 是任一 $n$ 级矩阵. 令

$$
S=\frac{1}{2}\left(A+A^{T}\right),
K=\frac{1}{2}\left(A-A^{T}\right).
$$

则 $A=S+K$.

$$
S^{T}=\frac{1}{2}\left(A^{T}+\left(A^{T}\right)^{T}\right)=\frac{1}{2}\left(A^{T}+A\right)=S.
$$

故 $S$ 是对称矩阵.

$$
K^{T}=\frac{1}{2}\left(A^{T}-\left(A^{T}\right)^{T}\right)=\frac{1}{2}\left(A^{T}-A\right)=-K.
$$

故 $K$ 是斜对称矩阵.

**唯一性**. 设 $A=S_{1}+K_{1}=S_{2}+K_{2}$, 其中 $S_{1},S_{2}$ 对称, $K_{1},K_{2}$ 斜对称.

则 $S_{1}-S_{2}=K_{2}-K_{1}$.

左边 $\left(S_{1}-S_{2}\right)^{T}=S_{1}-S_{2}$, 是对称矩阵.

右边

$$
\left(K_{2}-K_{1}\right)^{T}=-K_{2}+K_{1}=-\left(K_{2}-K_{1}\right),
$$

是斜对称矩阵.

一个矩阵既是对称的又是斜对称的, 故它必为零矩阵.

因此 $S_{1}-S_{2}=0$, $K_{2}-K_{1}=0$, 即 $S_{1}=S_{2}$, $K_{1}=K_{2}$.

表法唯一. $\blacksquare$

### 习题四

(习题 4.2-9) 证明: 如果 $A$ 是实数域上的 $n$ 级对称矩阵, 并且 $A^{2}=0$, 则 $A=0$.

### 解答 习题四

设 $A=\left(a_{ij}\right)$ 是实对称矩阵, $A^{2}=0$.

考虑 $A^{2}$ 的主对角元:

$$
\left(A^{2}\right)_{ii}=\sum_{k=1}^{n}a_{ik}a_{ki}.
$$

因为 $A$ 对称, 所以 $a_{ki}=a_{ik}$.

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

### 习题五

(习题 4.2-10) 证明: 数域 $K$ 上奇数级斜对称矩阵的行列式等于零.

### 解答 习题五

设 $A$ 是 $n$ 级斜对称矩阵, $n$ 为奇数.

则 $A^{T}=-A$.

$$
\left|A^{T}\right|=\left|-A\right|.
$$

因为 $\left|A^{T}\right|=\left|A\right|$, 且 $\left|-A\right|=\left(-1\right)^{n}\left|A\right|$.

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
