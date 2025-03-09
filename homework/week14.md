# week14

> **定理 3.7.1 (齐次线性方程组解空间的维数)**
> 
> 数域 $K$ 上 $n$ 元齐次线性方程组 $Ax=0$ 的解空间 $W$ 的维数为 $\dim{W}=n-\text{rank}\left(A\right)$.

> **定理 4.3.1 (矩阵乘积的秩)**
> 
> 设 $A=\left(a_{ij}\right)_{s\times{n}}$, $B=\left(b_{ij}\right)_{n\times{m}}$, 则 $\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}$.

> **命题 4.5.2 (实数域上秩的等式)**
> 
> 设 $A$ 是实数域上 $s\times{n}$ 矩阵, 则 $\text{rank}\left(A^{\top}A\right)=\text{rank}\left(AA^{\top}\right)=\text{rank}\left(A\right)$. $\beta_{i}=\alpha_{i}-\sum_{k=1}^{i-1}\frac{\left(\alpha_{i},\beta_{k}\right)}{\left(\beta_{k},\beta_{k}\right)}\beta_{k}$, 则 $\beta_{1},\beta_{2},\cdots,\beta_{m}$ 是正交向量组, 且与原向量组等价.

> **定义 4.6.1 (正交矩阵)**
> 
> 实数域上的方阵 $A$ 如果满足 $A^{\top}A=I$, 则称 $A$ 是正交矩阵. ## 4.5-1 证明: 设 $A,B$ 分别是 $s\times{n}$, $n\times{m}$ 矩阵. 如果 $AB=0$, 则 $\text{rank}\left(A\right)+\text{rank}\left(B\right)\le{n}$. 设 $B$ 的列向量组为 $\beta_{1},\beta_{2},\cdots,\beta_{m}$. $AB=0$ 意味着 $A\beta_{j}=0$ ( $j=1,2,\cdots,m$ ). 所以每个 $\beta_{j}$ 都是齐次线性方程组 $Ax=0$ 的解. 因此 $B$ 的列空间 $\subseteq{A}x=0$ 的解空间 $W$. 由**定理 3.7.1 (齐次线性方程组解空间的维数)**, $$ \text{rank}\left(B\right)=\dim\left\langle\beta_{1},\cdots,\beta_{m}\right\rangle\le\dim{W}=n-\text{rank}\left(A\right). $$ 因此 $$ \text{rank}\left(A\right)+\text{rank}\left(B\right)\le{n}. $$ $\blacksquare$

## 4.4-10(1)

解下列矩阵方程:

$$
\left[\begin{array}{rrr}
1&-2&0\\
4&-2&-1\\
-3&1&2
\end{array}\right]X=\left[\begin{array}{rr}
-1&4\\
2&5\\
1&-3
\end{array}\right].
$$

### 解答 4.4-10(1)

由**定理 4.4.2 (可逆的充要条件)**, 先求 $A^{-1}$. 记

$$
A=\left[\begin{array}{rrr}1&-2&0\\4&-2&-1\\-3&1&2\end{array}\right],
B=\left[\begin{array}{rr}-1&4\\2&5\\1&-3\end{array}\right].
$$

先求 $A^{-1}$.

$$
\left|A\right|=1\times\left(-4+1\right)-\left(-2\right)\times\left(8-3\right)+0=-3+10=7.
$$

伴随矩阵:

$$
A^{*}=\left[\begin{array}{rrr}
-3&4&2\\
-5&2&1\\
-2&5&6
\end{array}\right].
$$

故

$$
A^{-1}=\frac{1}{7}A^{*}.
$$

因此

$$
X=A^{-1}B=\frac{1}{7}A^{*}B.
$$

计算 $A^{*}B$:

$$
A^{*}B=\left[\begin{array}{rrr}
-3&4&2\\
-5&2&1\\
-2&5&6
\end{array}\right]\left[\begin{array}{rr}
-1&4\\
2&5\\
1&-3
\end{array}\right]
=\left[\begin{array}{rr}
13&2\\
10&-13\\
18&-1
\end{array}\right].
$$

由**定理 4.4.2 (可逆的充要条件)**, $A^{-1}=\frac{1}{\left|A\right|}A^{*}$, 故

$$
X=\frac{1}{7}\left[\begin{array}{rr}
13&2\\
10&-13\\
18&-1
\end{array}\right].
$$

$\blacksquare$

## 4.4-11

证明: 可逆的上 (下) 三角矩阵的逆矩阵仍是上 (下) 三角矩阵.

### 解答 4.4-11

由**定义 4.4.1 (可逆矩阵)**和**定义 4.4.2 (逆矩阵)**, 设 $A$ 是 $n$ 级上三角矩阵, 且可逆. 设 $A^{-1}=B=\left(b_{ij}\right)$.

因为 $AB=I$, 故对任意 $i,j$,

$$
\sum_{k=1}^{n}a_{ik}b_{kj}=\delta_{ij}.
$$

归纳证明 $b_{ij}=0$ (当 $i>j$).

对从下往上的行 $i=n,n-1,\cdots,2$ 归纳.

当 $i=n$ 时, 对任意 $j<{}n$:

$$
\sum_{k=1}^{n}a_{nk}b_{kj}=0.
$$

因为 $A$ 是上三角矩阵, 所以 $a_{nk}=0$ (当 $k<{}n$).

因此上式化为 $a_{nn}b_{nj}=0$.

因为 $A$ 可逆, 故 $a_{nn}\ne0$, 从而 $b_{nj}=0$ (对所有 $j<{}n$).

假设对所有 $i>m$ 的行, 结论已证 (即 $b_{ij}=0$, 当 $i>m$ 且 $i>j$).

考虑第 $m$ 行, 对任意 $j<{}m$:

$$
\sum_{k=1}^{n}a_{mk}b_{kj}=0.
$$

因为 $A$ 是上三角矩阵, 所以 $a_{mk}=0$ (当 $k>m$).

因此上式为

$$
\sum_{k=1}^{m}a_{mk}b_{kj}=0.
$$

其中

$$
a_{mm}b_{mj}+a_{m,m-1}b_{m-1,j}+\cdots+a_{m1}b_{1,j}=0.
$$

由归纳假设, 当 $k>m$ 时已证为 $0$. 对于 $k<{}m$ 的项, $a_{mk}=0$ (因为 $m>k$, 上三角矩阵).

因此只剩下 $a_{mm}b_{mj}=0$.

因为 $a_{mm}\ne0$, 故 $b_{mj}=0$.

归纳完成. 因此 $B$ 是上三角矩阵.

可逆的上 (下) 三角矩阵的逆矩阵仍是上 (下) 三角矩阵. 下三角矩阵的情形类似可证.

$\blacksquare$

## 4.5-4

证明: 如果 $n$ 级矩阵 $A$ 满足 $A^{2}=I$ (此时称 $A$ 是对合矩阵), 则

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

### 解答 4.5-4

因为 $A^{2}=I$, 所以

$$
\left(I+A\right)\left(I-A\right)=I-A^{2}=I-I=0.
$$

由4.5-1的结论,

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)\le{n}.
$$

另一方面,

$$
\left(I+A\right)+\left(I-A\right)=2I.
$$

由秩的子加性,

$$
\text{rank}\left(2I\right)\le\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right).
$$

$\text{rank}\left(2I\right)=n$, 故

$$
n\le\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right).
$$

因此

$$
\text{rank}\left(I+A\right)+\text{rank}\left(I-A\right)=n.
$$

$\blacksquare$

## 4.5-5

证明: 如果 $n$ 级矩阵 $A$ 满足 $A^{2}=A$ (此时称 $A$ 是幂等矩阵), 则

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

### 解答 4.5-5

因为 $A^{2}=A$, 所以

$$
A\left(I-A\right)=A-A^{2}=A-A=0.
$$

由4.5-1的结论,

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)\le{n}.
$$

另一方面,

$$
A+\left(I-A\right)=I.
$$

由秩的子加性,

$$
\text{rank}\left(I\right)\le\text{rank}\left(A\right)+\text{rank}\left(I-A\right).
$$

$\text{rank}\left(I\right)=n$, 故

$$
n\le\text{rank}\left(A\right)+\text{rank}\left(I-A\right).
$$

因此

$$
\text{rank}\left(A\right)+\text{rank}\left(I-A\right)=n.
$$

$\blacksquare$

## 4.5-6

设 $A$ 是实数域上的 $s\times{n}$ 矩阵, $\beta$ 是 $\mathbb{R}^{s}$ 的任意一个列向量. 证明: $n$ 元线性方程组 $A^{\top}AX=A^{\top}\beta$ 一定有解.

### 解答 4.5-6

由**命题 4.5.2 (实数域上秩的等式)**, 对于实数域上的矩阵,

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

系数矩阵与增广矩阵有相同的秩, 故该方程组有解.

$\blacksquare$

## 4.5-9

设 $A$ 是 $n$ 级矩阵 ( $n\ge2$ ), 证明:

$$
\text{rank}\left(A^{*}\right)=
\begin{cases}
n,&\text{当~}\text{rank}\left(A\right)=n;\\
1,&\text{当~}\text{rank}\left(A\right)=n-1;\\
0,&\text{当~}\text{rank}\left(A\right)<{}n-1.
\end{cases}
$$

### 解答 4.5-9

由**定理 4.3.1 (矩阵乘积的秩)**,

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

分三种情况讨论.

当 $\text{rank}\left(A\right)=n$ 时: $\left|A\right|\ne0$.

由 $AA^{*}=\left|A\right|I$, 得 $\left|A\right|\left|A^{*}\right|=\left|A\right|^{n}$.

故 $\left|A^{*}\right|=\left|A\right|^{n-1}\ne0$, 因此 $\text{rank}\left(A^{*}\right)=n$.

当 $\text{rank}\left(A\right)=n-1$ 时: $\left|A\right|=0$.

故 $AA^{*}=\left|A\right|I=0$.

由4.5-1, $\text{rank}\left(A\right)+\text{rank}\left(A^{*}\right)\le{n}$.

即 $\left(n-1\right)+\text{rank}\left(A^{*}\right)\le{n}$, 故 $\text{rank}\left(A^{*}\right)\le1$.

又因为 $\text{rank}\left(A\right)=n-1$, 所以 $A$ 有一个 $n-1$ 阶子式非零. 这个 $n-1$ 阶子式就是某个代数余子式, 故 $A^{*}\ne0$, 从而 $\text{rank}\left(A^{*}\right)\ge1$.

因此 $\text{rank}\left(A^{*}\right)=1$.

当 $\text{rank}\left(A\right)<{}n-1$ 时: $A$ 的所有 $n-1$ 阶子式都为零.

故所有代数余子式都为零, 即 $A^{*}=0$.

因此 $\text{rank}\left(A^{*}\right)=0$.

$\blacksquare$
