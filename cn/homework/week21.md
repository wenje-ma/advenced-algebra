# 作业 21

> **定义1** (可逆矩阵)<br>对于数域 $K$ 上的矩阵 $A$, 如果存在数域 $K$ 上的矩阵 $B$, 使得 $AB=BA=I$, 则称 $A$ 是可逆矩阵 (或非奇异矩阵).

> **定义2** (逆矩阵)<br>如果 $A$ 是可逆矩阵, 则适合 $AB=BA=I$ 的矩阵 $B$ 称为 $A$ 的逆矩阵, 记作 $A^{-1}$.

> **定理2** (可逆的充要条件)<br>数域 $K$ 上 $n$ 级矩阵 $A$ 可逆的充分必要条件为 $\left|A\right|\ne0$. 当 $A$ 可逆时:
> 
> $$
> A^{-1}=\frac{1}{\left|A\right|}A^{*}
> $$

### 习题一

(习题 4.4-4) 证明: 如果矩阵 $A$ 可逆, 则 $A^{*}$ 也可逆; 并且求 $\left(A^{*}\right)^{-1}$.

### 解答 习题一

由**定义1** (可逆矩阵)和**定义2** (逆矩阵), 因为 $A$ 可逆, 故 $\left|A\right|\ne 0$.

已知 $AA^{*}=\left|A\right|I$.

两边取行列式:

$$
\left|A\right|\left|A^{*}\right|=\left|A\right|^{n}.
$$

因为 $\left|A\right|\ne 0$, 故 $\left|A^{*}\right|=\left|A\right|^{n-1}\ne 0$.

由**定理2** (可逆的充要条件), 因此 $A^{*}$ 可逆.

由 $AA^{*}=\left|A\right|I$, 得

$$
A^{*}=\left|A\right|A^{-1}.
$$

所以

$$
\left(A^{*}\right)^{-1}=\left(\left|A\right|A^{-1}\right)^{-1}=\frac{1}{\left|A\right|}A.
$$

$\blacksquare$

### 习题二

(习题 4.4-5) 证明: 如果 $A^{3}=0$, 则 $I-A$ 可逆; 并且求 $\left(I-A\right)^{-1}$.

### 解答 习题二

由**定义1** (可逆矩阵), 要证明 $I-A$ 可逆, 即存在矩阵 $B$ 使得

$$
\left(I-A\right)B=B\left(I-A\right)=I.
$$

$$
\left(I-A\right)\left(I+A+A^{2}\right)=I+A+A^{2}-A-A^{2}-A^{3}=I-A^{3}=I-0=I.
$$

同理,

$$
\left(I+A+A^{2}\right)\left(I-A\right)=I.
$$

所以 $I-A$ 可逆, 且

由**定义2** (逆矩阵),

$$
\left(I-A\right)^{-1}=I+A+A^{2}.
$$

$\blacksquare$

### 习题三

(习题 4.4-9(4)) 求下列矩阵的逆矩阵:

$$
A=\left[\begin{array}{rrrr}
1 & 1 & 1 & 1\\
1 & 1 & -1 & -1\\
1 & -1 & 1 & -1\\
1 & -1 & -1 & 1
\end{array}\right].
$$

### 解答 习题三

由**定义1** (可逆矩阵)和**定义2** (逆矩阵), 计算 $A^{2}$:

$$
A^{2}=AA=\left[\begin{array}{rrrr}
4 & 0 & 0 & 0\\
0 & 4 & 0 & 0\\
0 & 0 & 4 & 0\\
0 & 0 & 0 & 4
\end{array}\right]=4I.
$$

因此

$$
A\times\frac{1}{4}A=I.
$$

由**定义2** (逆矩阵), 故

$$
A^{-1}=\frac{1}{4}A=\left[\begin{array}{rrrr}
1/4 & 1/4 & 1/4 & 1/4\\
1/4 & 1/4 & -1/4 & -1/4\\
1/4 & -1/4 & 1/4 & -1/4\\
1/4 & -1/4 & -1/4 & 1/4
\end{array}\right].
$$

$\blacksquare$

### 习题四

(习题 4.4-10(1)) 解下列矩阵方程:

$$
\left[\begin{array}{rrr}
1 & -2 & 0\\
4 & -2 & -1\\
-3 & 1 & 2
\end{array}\right]X=\left[\begin{array}{rr}
-1 & 4\\
2 & 5\\
1 & -3
\end{array}\right].
$$

### 解答 习题四

由**定理2** (可逆的充要条件), 先求 $A^{-1}$. 记

$$
A=\left[\begin{array}{rrr}1 & -2 & 0\\4 & -2 & -1\\-3 & 1 & 2\end{array}\right],;B=\left[\begin{array}{rr}-1 & 4\\2 & 5\\1 & -3\end{array}\right].
$$

先求 $A^{-1}$.

$$
\left|A\right|=1\times\left(-4+1\right)-\left(-2\right)\times\left(8-3\right)+0=-3+10=7.
$$

伴随矩阵:

$$
A^{*}=\left[\begin{array}{rrr}
-3 & 4 & 2\\
-5 & 2 & 1\\
-2 & 5 & 6
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
-3 & 4 & 2\\
-5 & 2 & 1\\
-2 & 5 & 6
\end{array}\right]\left[\begin{array}{rr}
-1 & 4\\
2 & 5\\
1 & -3
\end{array}\right]
=\left[\begin{array}{rr}
13 & 2\\
10 & -13\\
18 & -1
\end{array}\right].
$$

所以

由**定理2** (可逆的充要条件),

$$
A^{-1}=\frac{1}{\left|A\right|}A^{*}
$$

故

$$
X=\frac{1}{7}\left[\begin{array}{rr}
13 & 2\\
10 & -13\\
18 & -1
\end{array}\right].
$$

$\blacksquare$

### 习题五

(习题 4.4-11) 证明: 可逆的上 (下) 三角矩阵的逆矩阵仍是上 (下) 三角矩阵.

### 解答 习题五

由**定义1** (可逆矩阵)和**定义2** (逆矩阵), 设 $A$ 是 $n$ 级上三角矩阵, 且可逆. 设 $A^{-1}=B=\left(b_{ij}\right)$.

因为 $AB=I$, 故对任意 $i,j$,

$$
\sum_{k=1}^{n}a_{ik}b_{kj}=\delta_{ij}.
$$

**归纳证明 $b_{ij}=0$ (当 $i> j$)**.

对从下往上的行 $i=n,n-1,\cdots,2$ 归纳.

当 $i=n$ 时, 对任意 $j< n$:

$$
\sum_{k=1}^{n}a_{nk}b_{kj}=0.
$$

因为 $A$ 是上三角矩阵, 所以 $a_{nk}=0$ (当 $k< n$).

因此上式化为 $a_{nn}b_{nj}=0$.

因为 $A$ 可逆, 故 $a_{nn}\ne0$, 从而 $b_{nj}=0$ (对所有 $j< n$).

假设对所有 $i> m$ 的行, 结论已证 (即 $b_{ij}=0$, 当 $i> m$ 且 $i> j$).

考虑第 $m$ 行, 对任意 $j< m$:

$$
\sum_{k=1}^{n}a_{mk}b_{kj}=0.
$$

因为 $A$ 是上三角矩阵, 所以 $a_{mk}=0$ (当 $k> m$).

因此上式为

$$
\sum_{k=1}^{m}a_{mk}b_{kj}=0.
$$

其中

$$
a_{mm}b_{mj}+a_{m,m-1}b_{m-1,j}+\cdots+a_{m1}b_{1,j}=0.
$$

由归纳假设, 当 $k> m$ 时已证为 $0$. 对于 $k< m$ 的项, $a_{mk}=0$ (因为 $m> k$, 上三角矩阵).

因此只剩下 $a_{mm}b_{mj}=0$.

因为 $a_{mm}\ne0$, 故 $b_{mj}=0$.

归纳完成. 因此 $B$ 是上三角矩阵.

可逆的上 (下) 三角矩阵的逆矩阵仍是上 (下) 三角矩阵. 下三角矩阵的情形类似可证. $\blacksquare$
