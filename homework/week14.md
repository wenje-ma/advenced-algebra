# 作业 14

> **定义1** (矩阵的秩)<br>矩阵 $A$ 的行秩与列秩统称为 $A$ 的秩, 记作 $\text{rank}\left(A\right)$.

> **定理4** (行秩等于列秩)<br>任一矩阵的行秩等于它的列秩.

> **推论5** (用初等行变换求秩)<br>设矩阵 $A$ 经过初等行变换化成阶梯形矩阵 $J$, 则 $A$ 的秩等于 $J$ 的非零行的数目. 设 $J$ 的主元所在的列是第 $j_{1},\cdots,j_{r}$ 列, 则 $A$ 的第 $j_{1},\cdots,j_{r}$ 列构成 $A$ 的列向量组的一个极大线性无关组.

### 习题一

(习题 3.5-2(1)) 求下列向量组的秩以及它的一个极大线性无关组:

$$
\alpha_{1}=\begin{bmatrix}-1\\5\\3\\-2\end{bmatrix},\ 
\alpha_{2}=\begin{bmatrix}4\\1\\-2\\9\end{bmatrix},\ 
\alpha_{3}=\begin{bmatrix}2\\0\\-1\\4\end{bmatrix},\ 
\alpha_{4}=\begin{bmatrix}0\\3\\4\\-5\end{bmatrix}.
$$

### 解答 习题一

由**推论5** (用初等行变换求秩), 把向量按列排成矩阵, 作初等行变换:

$$
\left[\begin{array}{rrrr}
-1 & 4 & 2 & 0\\
5 & 1 & 0 & 3\\
3 & -2 & -1 & 4\\
-2 & 9 & 4 & -5
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1 & -4 & -2 & 0\\
0 & 1 & 0 & -5\\
0 & 0 & 5 & 54\\
0 & 0 & 0 & 0
\end{array}\right].
$$

由**推论5**, 阶梯形矩阵有 $3$ 个非零行, 故秩为 $3$.

由**推论5**, 主元在第 $1,2,3$ 列, 故 $\alpha_{1},\alpha_{2},\alpha_{3}$ 是一个极大线性无关组. $\blacksquare$

### 习题二

(习题 3.5-3) 求下述矩阵 $A$ 的列空间的一个基和行空间的维数:

$$
A=\left[\begin{array}{rrrr}
1 & 3 & -2 & -7\\
0 & -1 & -3 & 4\\
5 & 2 & 0 & 1\\
1 & 4 & 1 & -11
\end{array}\right].
$$

### 解答 习题二

由**推论5** (用初等行变换求秩), 作初等行变换:

$$
\left[\begin{array}{rrrr}
1 & 3 & -2 & -7\\
0 & -1 & -3 & 4\\
5 & 2 & 0 & 1\\
1 & 4 & 1 & -11
\end{array}\right]
\xrightarrow{\text{行变换}}
\left[\begin{array}{rrrr}
1 & 3 & -2 & -7\\
0 & 1 & 3 & -4\\
0 & 0 & 49 & -16\\
0 & 0 & 0 & 0
\end{array}\right].
$$

阶梯形矩阵有 $3$ 个非零行, 由**推论5** (用初等行变换求秩), 故 $\text{rank}\left(A\right)=3$.

由**定理4** (行秩等于列秩), 行空间的维数等于矩阵的秩, 即 $3$.

由**推论5**, 主元在第 $1,2,3$ 列, 故原矩阵 $A$ 的第 $1,2,3$ 列构成列空间的一个基:

$$
\alpha_{1}=\begin{bmatrix}1\\0\\5\\1\end{bmatrix},\ 
\alpha_{2}=\begin{bmatrix}3\\-1\\2\\4\end{bmatrix},\ 
\alpha_{3}=\begin{bmatrix}-2\\-3\\0\\1\end{bmatrix}.
$$

$\blacksquare$

### 习题三

(习题 3.5-4) 对于 $\lambda$ 的不同的值, 下述矩阵的秩分别是多少?

$$
\left[\begin{array}{rrrr}
1 & \lambda & -1 & 2\\
2 & -1 & \lambda & 5\\
1 & 10 & -6 & 1
\end{array}\right].
$$

### 解答 习题三

由**推论5** (用初等行变换求秩), 作初等行变换求矩阵的秩:

第 $2$ 行 $-$ 第 $1$ 行 $\times 2$: 第 $2$ 行 $=\left(0,-1-2\lambda,\lambda+2,1\right)$.

第 $3$ 行 $-$ 第 $1$ 行: 第 $3$ 行 $=\left(0,10-\lambda,-5,-1\right)$.

矩阵化为:

$$
\left[\begin{array}{rrrr}
1 & \lambda & -1 & 2\\
0 & -1-2\lambda & \lambda+2 & 1\\
0 & 10-\lambda & -5 & -1
\end{array}\right].
$$

第 $2$ 行 $+$ 第 $3$ 行: 第 $2$ 行 $=\left(0,9-3\lambda,\lambda-3,0\right)=\left(0,3\left(3-\lambda\right),-\left(3-\lambda\right),0\right)$.

**当 $\lambda=3$ 时**:

第 $2$ 行 $=\left(0,0,0,0\right)$, 第 $3$ 行 $=\left(0,7,-5,-1\right)$.

阶梯形矩阵有 $2$ 个非零行, 故秩为 $2$.

**当 $\lambda\ne3$ 时**:

第 $2$ 行非零. 第 $3$ 行 $-$ 第 $2$ 行 $\times\frac{10-\lambda}{3\left(3-\lambda\right)}$, 第 $3$ 行的第 $4$ 列仍为 $-1\ne0$, 故第 $3$ 行非零.

阶梯形矩阵有 $3$ 个非零行, 故秩为 $3$.

综上: 当 $\lambda=3$ 时, 由**推论5** (用初等行变换求秩), 阶梯形矩阵有 $2$ 个非零行, 故秩为 $2$; 当 $\lambda\ne3$ 时, 阶梯形矩阵有 $3$ 个非零行, 故秩为 $3$. $\blacksquare$

### 习题四

(习题 3.5-8) 证明: 如果 $m\times n$ 矩阵 $A$ 的秩为 $r$, 则它的任何 $s$ 行组成的子矩阵 $A_{1}$ 的秩不小于 $r+s-m$.

### 解答 习题四

由**定义1** (矩阵的秩), 矩阵 $A$ 的行秩与列秩统称为 $A$ 的秩. 要证明 $A_{1}$ 的秩不小于 $r+s-m$.

设 $A_{2}$ 是 $A$ 的其余 $m-s$ 行组成的子矩阵.

把 $A$ 看作行向量组, $A$ 的行向量组的秩为 $r$.

$A$ 的行向量组 $=A_{1}$ 的行向量组 $\cup A_{2}$ 的行向量组.

由秩的不等式:

$$
\text{rank}\left(A\right)\le\text{rank}\left(A_{1}\right)+\text{rank}\left(A_{2}\right).
$$

又 $A_{2}$ 只有 $m-s$ 行, 故 $\text{rank}\left(A_{2}\right)\le m-s$.

因此

$$
r\le\text{rank}\left(A_{1}\right)+\left(m-s\right).
$$

移项得

$$
\text{rank}\left(A_{1}\right)\ge r-\left(m-s\right)=r+s-m.
$$

$\blacksquare$

### 习题五

(习题 3.5-13) 设 $A$ 是 $s\times n$ 矩阵, $B$ 是 $l\times m$ 矩阵, $C$ 是 $s\times m$ 矩阵, 证明:

$$
\text{rank}\left(\begin{array}{cc}A & C\\0 & B\end{array}\right)\ge\text{rank}\left(A\right)+\text{rank}\left(B\right).
$$

### 解答 习题五

由**定义1** (矩阵的秩), 要证明分块矩阵的秩不小于 $A$ 的秩与 $B$ 的秩之和. 取 $A$ 和 $B$ 的列空间的基来构造线性无关向量组.

设 $\text{rank}\left(A\right)=r_{1}$, $\text{rank}\left(B\right)=r_{2}$.

取 $A$ 的列空间的一个基: $\alpha_{1},\cdots,\alpha_{r_{1}}$ ( $s$ 维向量).

取 $B$ 的列空间的一个基: $\beta_{1},\cdots,\beta_{r_{2}}$ ( $l$ 维向量).

考虑分块矩阵 $M=\left(\begin{array}{cc}A & C\\0 & B\end{array}\right)$ 的以下列向量:

$$
\begin{bmatrix}\alpha_{1}\\0\end{bmatrix},\ \cdots,\ \begin{bmatrix}\alpha_{r_{1}}\\0\end{bmatrix},\ 
\begin{bmatrix}c_{1}\\\beta_{1}\end{bmatrix},\ \cdots,\ \begin{bmatrix}c_{r_{2}}\\\beta_{r_{2}}\end{bmatrix},
$$

其中 $c_{i}$ 是从 $C$ 的列中适当选取的 $s$ 维向量, 使得对应 $M$ 的列的下半部分为 $\beta_{i}$.

证明这 $r_{1}+r_{2}$ 个向量线性无关: 设

$$
k_{1}\begin{bmatrix}\alpha_{1}\\0\end{bmatrix}+\cdots+k_{r_{1}}\begin{bmatrix}\alpha_{r_{1}}\\0\end{bmatrix}
+l_{1}\begin{bmatrix}c_{1}\\\beta_{1}\end{bmatrix}+\cdots+l_{r_{2}}\begin{bmatrix}c_{r_{2}}\\\beta_{r_{2}}\end{bmatrix}=0.
$$

下半部分: $l_{1}\beta_{1}+\cdots+l_{r_{2}}\beta_{r_{2}}=0$. 因为 $\beta_{1},\cdots,\beta_{r_{2}}$ 线性无关, 所以 $l_{1}=\cdots=l_{r_{2}}=0$.

上半部分: $k_{1}\alpha_{1}+\cdots+k_{r_{1}}\alpha_{r_{1}}=0$. 因为 $\alpha_{1},\cdots,\alpha_{r_{1}}$ 线性无关, 所以 $k_{1}=\cdots=k_{r_{1}}=0$.

故这 $r_{1}+r_{2}$ 个向量线性无关.

因此 $\text{rank}\left(M\right)\ge r_{1}+r_{2}=\text{rank}\left(A\right)+\text{rank}\left(B\right)$. $\blacksquare$
