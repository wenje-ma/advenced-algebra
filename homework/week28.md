# 作业 28

> **定义1** (相似)<br>设 $A$ 与 $B$ 都是数域 $K$ 上 $n$ 级矩阵, 如果存在数域 $K$ 上的一个 $n$ 级可逆矩阵 $P$, 使得 $P^{-1}AP=B$, 则称 $A$ 与 $B$ 是相似的, 记作 $A\sim B$.

> **性质** (相似的不变量)<br>相似的矩阵有相等的行列式、相等的秩、相等的迹.

> **定理2** (可对角化的充要条件)<br>数域 $K$ 上的 $n$ 级矩阵 $A$ 能够相似于对角矩阵的充分必要条件是: $K^{n}$ 中有 $n$ 个线性无关的列向量 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 以及 $K$ 中有 $n$ 个数 $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$, 使得 $A\alpha_{i}=\lambda_{i}\alpha_{i}$ ( $i=1,2,\cdots,n$ ).

### 习题一

(习题 5.4-3) 证明: 如果 $A_{1}\sim B_{1}$, $A_{2}\sim B_{2}$, 则

$$
\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right].
$$

### 解答 习题一

由**定义1**(相似), 因为 $A_{1}\sim B_{1}$, 故存在可逆矩阵 $P_{1}$, 使得 $P_{1}^{-1}A_{1}P_{1}=B_{1}$.

令 $P=\left[\begin{array}{cc}P_{1} & 0\\0 & P_{2}\end{array}\right]$.

因为 $P_{1},P_{2}$ 可逆, 故 $P$ 可逆, 且 $P^{-1}=\left[\begin{array}{cc}P_{1}^{-1} & 0\\0 & P_{2}^{-1}\end{array}\right]$.

计算:

$$
\begin{aligned}
P^{-1}\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]P
&=\left[\begin{array}{cc}P_{1}^{-1} & 0\\0 & P_{2}^{-1}\end{array}\right]\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\left[\begin{array}{cc}P_{1} & 0\\0 & P_{2}\end{array}\right]\\
&=\left[\begin{array}{cc}P_{1}^{-1}A_{1}P_{1} & 0\\0 & P_{2}^{-1}A_{2}P_{2}\end{array}\right]\\
&=\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right].
\end{aligned}
$$

因此由**定义1**(相似), $\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right]$. $\blacksquare$

### 习题二

(习题 5.4-8) 证明: 如果 $A$ 可对角化, 则 $A\sim A^{T}$.

### 解答 习题二

由**定理2**(可对角化的充要条件), 因为 $A$ 可对角化, 故存在可逆矩阵 $P$, 使得

$$
P^{-1}AP=D,
$$

其中 $D$ 是对角矩阵.

对角矩阵的转置仍是对角矩阵, 即 $D^{T}=D$.

两边取转置:

$$
\left(P^{-1}AP\right)^{T}=D^{T}=D.
$$

即

$$
P^{T}A^{T}\left(P^{-1}\right)^{T}=D.
$$

令 $Q=\left(P^{T}\right)^{-1}$. 则 $Q^{-1}=P^{T}$.

上式化为

$$
Q^{-1}A^{T}Q=D.
$$

因此

$$
A^{T}\sim D.
$$

又因为 $A\sim D$, 故由相似关系的对称性和传递性,

$$
A\sim A^{T}.
$$

因此 $A\sim A^{T}$. $\blacksquare$

### 习题三

(习题 5.4-9) 证明: 如果数域 $K$ 上的 $n$ 级矩阵 $A,B$ 满足

$$
AB-BA=A,
$$

则 $A$ 不可逆.

### 解答 习题三

由**性质**(相似的不变量), 相似的矩阵有相等的迹. 假设 $A$ 可逆.

由 $AB-BA=A$, 两边左乘 $A^{-1}$:

$$
A^{-1}AB-A^{-1}BA=A^{-1}A.
$$

即

$$
B-A^{-1}BA=I.
$$

令 $C=A^{-1}BA$. 则 $B-C=I$.

两边取迹:

$$
\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(I\right)=n.
$$

另一方面,

$$
\operatorname{tr}\left(C\right)=\operatorname{tr}\left(A^{-1}BA\right)=\operatorname{tr}\left(BAA^{-1}\right)=\operatorname{tr}\left(B\right).
$$

因此

$$
\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(B\right)-\operatorname{tr}\left(C\right)=0.
$$

矛盾.

相似的矩阵有相等的迹, 因此假设不成立, 即 $A$ 不可逆. $\blacksquare$

### 习题四

(习题 5.4-12) 方阵 $A$ 称为幂零矩阵, 如果 $A$ 的某个正整数次幂等于零矩阵, 使 $A^{l}=0$ 成立的最小正整数 $l$ 称为 $A$ 的幂零指数. 证明: 与幂零矩阵相似的矩阵仍是幂零矩阵, 并且它们的幂零指数相等.

### 解答 习题四

设 $A$ 是幂零矩阵, 幂零指数为 $l$, 即 $A^{l}=0$, 且 $A^{k}\ne0$ ( $k<l$ ).

设 $B\sim A$, 即存在可逆矩阵 $P$, 使得 $B=P^{-1}AP$.

**证明 $B$ 是幂零矩阵**.

$$
B^{l}=\left(P^{-1}AP\right)^{l}=P^{-1}A^{l}P=P^{-1}0P=0.
$$

因此 $B$ 是幂零矩阵.

**证明 $B$ 的幂零指数等于 $l$**.

设 $B$ 的幂零指数为 $m$, 即 $B^{m}=0$.

则

$$
B^{m}=\left(P^{-1}AP\right)^{m}=P^{-1}A^{m}P=0.
$$

两边左乘 $P$, 右乘 $P^{-1}$:

$$
A^{m}=0.
$$

因为 $A$ 的幂零指数为 $l$, 故 $m\ge l$.

另一方面, $A^{l}=0$, 故

$$
B^{l}=P^{-1}A^{l}P=0.
$$

因为 $B$ 的幂零指数为 $m$, 故 $l\ge m$.

因此 $m=l$.

所以与幂零矩阵相似的矩阵仍是幂零矩阵, 且幂零指数相等. $\blacksquare$
