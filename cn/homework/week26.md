# 作业 26

> **定义1** (相抵)<br>数域 $K$ 上的矩阵 $A$ 如果经过一系列初等行变换和初等列变换变成矩阵 $B$, 则称 $A$ 与 $B$ 是相抵的, 记作 $A\overset{\text{相抵}}{\sim}B$.

> **定理1** (相抵标准形)<br>设数域 $K$ 上 $s\times n$ 矩阵 $A$ 的秩为 $r$. 如果 $r>0$, 则 $A$ 相抵于下述形式的矩阵:

$$
\left[\begin{array}{cc}I_{r} & 0\\0 & 0\end{array}\right].
$$

> **定理2** (相抵的充要条件)<br>数域 $K$ 上两个 $s\times n$ 矩阵 $A$ 与 $B$ 相抵当且仅当它们的秩相等.

### 习题一

(习题 5.2-1(1)) 求下列矩阵的相抵标准形:

$$
A=\left[\begin{array}{rrr}
1 & -1 & 3\\
-2 & 3 & -11\\
4 & -5 & 17
\end{array}\right].
$$

### 解答 习题一

由**定理1** (相抵标准形), 对 $A$ 作初等行变换:

$$
A=\left[\begin{array}{rrr}
1 & -1 & 3\\
-2 & 3 & -11\\
4 & -5 & 17
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1 & -1 & 3\\
0 & 1 & -5\\
0 & -1 & 5
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1 & -1 & 3\\
0 & 1 & -5\\
0 & 0 & 0
\end{array}\right]
\rightarrow
\left[\begin{array}{rrr}
1 & 0 & -2\\
0 & 1 & -5\\
0 & 0 & 0
\end{array}\right].
$$

再作初等列变换: 第 $3$ 列 $+2\times$ 第 $1$ 列, 第 $3$ 列 $+5\times$ 第 $2$ 列.

$$
A\rightarrow\left[\begin{array}{rrr}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 0
\end{array}\right].
$$

因此由**定理1** (相抵标准形), 相抵标准形为

$$
\left[\begin{array}{cc}I_{2} & 0\\0 & 0\end{array}\right]
$$

$\blacksquare$

### 习题二

(习题 5.2-1(3)) 求下列矩阵的相抵标准形:

$$
A=\left[\begin{array}{rr}
1 & -2\\
-3 & -6\\
2 & -4
\end{array}\right].
$$

### 解答 习题二

由**定理1** (相抵标准形), 对 $A$ 作初等行变换:

$$
A=\left[\begin{array}{rr}
1 & -2\\
-3 & -6\\
2 & -4
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1 & -2\\
0 & -12\\
0 & 0
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1 & -2\\
0 & 1\\
0 & 0
\end{array}\right]
\rightarrow
\left[\begin{array}{rr}
1 & 0\\
0 & 1\\
0 & 0
\end{array}\right].
$$

因此由**定理1** (相抵标准形), 相抵标准形为

$$
\left[\begin{array}{c}I_{2}\\0\end{array}\right]
$$

$\blacksquare$

### 习题三

(习题 5.2-4) 证明: 任意一个秩为 $r$ ( $r>0$ ) 的矩阵都可以表示成 $r$ 个秩为 $1$ 的矩阵之和.

### 解答 习题三

由**定理1** (相抵标准形), 设 $A$ 是 $s\times n$ 矩阵, $\operatorname{rank}\left(A\right)=r>0$.

由相抵标准形定理, 存在 $s$ 级可逆矩阵 $P$ 和 $n$ 级可逆矩阵 $Q$, 使得

$$
A=P\left[\begin{array}{cc}I_{r} & 0\\0 & 0\end{array}\right]Q.
$$

把中间的矩阵写成 $r$ 个矩阵之和:

$$
\left[\begin{array}{cc}I_{r} & 0\\0 & 0\end{array}\right]=E_{11}+E_{22}+\cdots+E_{rr},
$$

其中 $E_{ii}$ 是第 $i$ 行第 $i$ 列为 $1$, 其余元素为 $0$ 的矩阵.

每个 $E_{ii}$ 的秩都是 $1$.

因此

$$
A=P\left(E_{11}+E_{22}+\cdots+E_{rr}\right)Q=PE_{11}Q+PE_{22}Q+\cdots+PE_{rr}Q.
$$

令 $A_{i}=PE_{ii}Q$.

因为 $P$ 和 $Q$ 可逆, 故

$$
\operatorname{rank}\left(A_{i}\right)=\operatorname{rank}\left(E_{ii}\right)=1.
$$

因此 $A$ 可以表示成 $r$ 个秩为 $1$ 的矩阵之和. $\blacksquare$

### 习题四

(习题 5.2-5) 设 $A,B$ 分别是 $s\times n$, $n\times m$ 矩阵, 证明 Sylvester (西尔维斯特) 秩不等式:

$$
\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right)-n.
$$

### 解答 习题四

由**定理1** (相抵标准形)的思路, 考虑分块矩阵

$$
M=\left[\begin{array}{cc}A & 0\\I_{n} & B\end{array}\right].
$$

**求 $\operatorname{rank}\left(M\right)$ 的上界**.

作分块矩阵的初等列变换: 用 $-B$ 右乘第 $1$ 块列, 加到第 $2$ 块列上.

$$
M=\left[\begin{array}{cc}A & 0\\I_{n} & B\end{array}\right]
\rightarrow
\left[\begin{array}{cc}A & -AB\\I_{n} & 0\end{array}\right].
$$

再作分块矩阵的初等行变换: 交换第 $1$ 块行和第 $2$ 块行.

$$
\rightarrow
\left[\begin{array}{cc}I_{n} & 0\\A & -AB\end{array}\right].
$$

这是分块上三角矩阵, 故

$$
\operatorname{rank}\left(M\right)=\operatorname{rank}\left(I_{n}\right)+\operatorname{rank}\left(-AB\right)=n+\operatorname{rank}\left(AB\right).
$$

**求 $\operatorname{rank}\left(M\right)$ 的下界**.

设 $\operatorname{rank}\left(A\right)=r_{1}$, $\operatorname{rank}\left(B\right)=r_{2}$.

$A$ 有 $r_{1}$ 个线性无关的行, $B$ 有 $r_{2}$ 个线性无关的行.

$M$ 的前 $s$ 行中, $A$ 的 $r_{1}$ 个线性无关行对应到 $M$ 中也是线性无关的 (因为右边的 $0$ 不影响).

$M$ 的后 $n$ 行中, $B$ 的 $r_{2}$ 个线性无关行对应到 $M$ 中.

假设这些行与前面的行合起来线性相关, 即存在系数 $k_{1},k_{2}$ 使得

$$
k_{1}\left(\text{前 }s\text{ 行的线性组合}\right)+k_{2}\left(\text{后 }n\text{ 行的线性组合}\right)=0.
$$

看后 $m$ 个分量:

$$
k_{2}\left(B\text{ 的行的线性组合}\right)=0.
$$

因为 $B$ 的行线性无关, 故 $k_{2}=0$.

再看前 $s$ 个分量:

$$
k_{1}\left(A\text{ 的行的线性组合}\right)=0.
$$

因为 $A$ 的行线性无关, 故 $k_{1}=0$.

因此 $M$ 的行向量组的秩至少为 $r_{1}+r_{2}$.

即

$$
\operatorname{rank}\left(M\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right).
$$

综合两式:

$$
n+\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right).
$$

由**定理1** (相抵标准形)的思路, 即

$$
\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right)-n.
$$

$\blacksquare$
