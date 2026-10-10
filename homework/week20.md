# 作业 20

> **定理1** (矩阵乘积的秩)<br>设 $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$, 则:<br>$$\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.$$

> **定理3** (乘积的行列式)<br>设 $A,B$ 都是 $n$ 级矩阵, 则 $|AB|=|A||B|$.

### 习题一

(习题 4.3-2) 一个矩阵称为行 (列) 满秩矩阵, 如果它的行 (列) 向量组是线性无关的. 证明: 如果一个 $s\times n$ 矩阵 $A$ 的秩为 $r$, 则有 $s\times r$ 的列满秩矩阵 $B$ 和 $r\times n$ 的行满秩矩阵 $C$, 使得 $A=BC$.

### 解答 习题一

由**定理1**(矩阵乘积的秩)的思路, 把 $A$ 经过初等行变换化成简化行阶梯形矩阵 $J$.

因为 $\text{rank}\left(A\right)=r$, 所以 $J$ 有 $r$ 个非零行.

设 $J=\left[\begin{array}{c}C\\0\end{array}\right]$, 其中 $C$ 是 $r\times n$ 矩阵, 且 $C$ 的行向量组线性无关 (因为 $J$ 的非零行线性无关).

故 $C$ 是行满秩矩阵.

设 $A=PJ$, 其中 $P$ 是 $s\times s$ 可逆矩阵.

则 $A=P\left[\begin{array}{c}C\\0\end{array}\right]$.

把 $P$ 按列分块: $P=\left(P_{1},P_{2}\right)$, 其中 $P_{1}$ 是 $s\times r$ 矩阵.

则 $A=\left(P_{1},P_{2}\right)\left[\begin{array}{c}C\\0\end{array}\right]=P_{1}C$.

令 $B=P_{1}$.

因为 $P$ 可逆, 所以 $P$ 的列向量组线性无关, 从而 $P_{1}$ 的列向量组也线性无关.

故 $B$ 是列满秩矩阵.

因此 $A=BC$, 其中 $B$ 是 $s\times r$ 列满秩矩阵, $C$ 是 $r\times n$ 行满秩矩阵. $\blacksquare$

### 习题二

(习题 4.3-6) 证明: 如果 $A$ 是数域 $K$ 上 $n$ 级矩阵, $n$ 是奇数, 且满足 $AA^{T}=I$, $|A|=1$, 则 $|I-A|=0$.

### 解答 习题二

由**定理3**(乘积的行列式), $|AB|=|A||B|$. 要证明 $|I-A|=0$.

$$
|I-A|=\left|\left(I-A\right)^{T}\right|=\left|I-A^{T}\right|.
$$

因为 $AA^{T}=I$, 故 $A^{T}=A^{-1}$.

因此

$$
|I-A^{T}|=|I-A^{-1}|=|A^{-1}\left(A-I\right)|=|A^{-1}||A-I|.
$$

$$
|A^{-1}|=\frac{1}{|A|}=\frac{1}{1}=1.
$$

$$
|A-I|=|-\left(I-A\right)|=\left(-1\right)^{n}|I-A|.
$$

因为 $n$ 是奇数, 故 $\left(-1\right)^{n}=-1$.

因此

$$
|I-A|=1\times\left(-1\right)\times|I-A|=-|I-A|.
$$

所以 $2|I-A|=0$, 即 $|I-A|=0$. $\blacksquare$

### 习题三

(习题 4.3-7) 设 $s_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$, $k=0,1,2,\cdots$; 设

$$
A=\left[\begin{array}{ccc}
s_{0} & s_{1} & s_{2}\\
s_{1} & s_{2} & s_{3}\\
s_{2} & s_{3} & s_{4}
\end{array}\right].
$$

证明: $|A|=\left(x_{1}-x_{2}\right)^{2}\left(x_{1}-x_{3}\right)^{2}\left(x_{2}-x_{3}\right)^{2}$.

### 解答 习题三

由**定理3**(乘积的行列式), $|AB|=|A||B|$. 令

$$
B=\left[\begin{array}{ccc}
1 & 1 & 1\\
x_{1} & x_{2} & x_{3}\\
x_{1}^{2} & x_{2}^{2} & x_{3}^{2}
\end{array}\right].
$$

计算 $BB^{T}$ 的 $\left(i,j\right)$ 元:

$$
\left(BB^{T}\right)_{ij}=\sum_{k=1}^{3}B_{ik}B_{jk}=\sum_{k=1}^{3}x_{k}^{i-1}x_{k}^{j-1}=\sum_{k=1}^{3}x_{k}^{i+j-2}=s_{i+j-2}.
$$

因此

$$
BB^{T}=\left[\begin{array}{ccc}
s_{0} & s_{1} & s_{2}\\
s_{1} & s_{2} & s_{3}\\
s_{2} & s_{3} & s_{4}
\end{array}\right]=A.
$$

所以

由**定理3**(乘积的行列式),

$$
|A|=|BB^{T}|=|B||B^{T}|=|B|^{2}.
$$

$B$ 是范德蒙矩阵,

$$
|B|=\left(x_{2}-x_{1}\right)\left(x_{3}-x_{1}\right)\left(x_{3}-x_{2}\right).
$$

因此

$$
|A|=|B|^{2}=\left(x_{1}-x_{2}\right)^{2}\left(x_{1}-x_{3}\right)^{2}\left(x_{2}-x_{3}\right)^{2}.
$$

$\blacksquare$

### 习题四

(习题 4.3-12) 证明: 对于实数域上任一 $s\times n$ 矩阵 $A$, 都有 $\text{rank}\left(A^{T}AA^{T}\right)=\text{rank}\left(A\right)$.

### 解答 习题四

由**定理1**(矩阵乘积的秩), $\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}$. 考虑齐次线性方程组 $\left(A^{T}AA^{T}\right)y=0$, 其中 $y$ 是 $s$ 维列向量.

设 $y$ 是 $\left(A^{T}AA^{T}\right)y=0$ 的解, 则

$$
A^{T}A\left(A^{T}y\right)=0.
$$

令 $z=A^{T}y$, 则 $A^{T}Az=0$.

由命题 $2$, 实数域上 $A^{T}Az=0$ 与 $z=0$ 同解.

故 $z=0$, 即 $A^{T}y=0$.

反之, 若 $A^{T}y=0$, 则

$$
A^{T}AA^{T}y=A^{T}A\left(A^{T}y\right)=A^{T}A\times0=0.
$$

因此 $\left(A^{T}AA^{T}\right)y=0$ 与 $A^{T}y=0$ 同解.

故它们的解空间维数相同:

$$
s-\text{rank}\left(A^{T}AA^{T}\right)=s-\text{rank}\left(A^{T}\right).
$$

所以

$$
\text{rank}\left(A^{T}AA^{T}\right)=\text{rank}\left(A^{T}\right)=\text{rank}\left(A\right).
$$

$\blacksquare$
