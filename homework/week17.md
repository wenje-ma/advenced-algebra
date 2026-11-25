# week17

> **定义 5.1.1 (二元关系)**
> 
> 设 $S$ 是一个非空集合, 我们把 $S\times{}S$ 的一个子集 $W$ 叫做 $S$ 上的一个二元关系. 如果 $\left(a,b\right)\in{}W$, 则称 $a$ 与 $b$ 有 $W$ 关系.

> **定义 5.1.2 (等价关系)**
> 
> 集合 $S$ 上的一个二元关系 $\sim$ 如果具有下述性质: $\forall{}a,b,c\in{}S$, 有 $1^{\circ}a\sim{}a$ (反身性); $2^{\circ}a\sim{}b\Rightarrow{}b\sim{}a$ (对称性); $3^{\circ}a\sim{}b$ 且 $b\sim{}c\Rightarrow{}a\sim{}c$ (传递性), 则称 $\sim$ 是 $S$ 上的一个等价关系.

> **定义 5.1.4 (商集)**
> 
> 设 $\sim$ 是集合 $S$ 上的一个等价关系. 由所有等价类组成的集合称为 $S$ 对于关系 $\sim$ 的商集, 记作 $S/\sim$.

> **定义 5.2.1 (相抵)**
> 
> 数域 $K$ 上的矩阵 $A$ 如果经过一系列初等行变换和初等列变换变成矩阵 $B$, 则称 $A$ 与 $B$ 是相抵的, 记作 $A\overset{\text{相抵}}{\sim}B$.

> **定理 5.2.1 (相抵标准形)**
> 
> 设数域 $K$ 上 $s\times{}n$ 矩阵 $A$ 的秩为 $r$. 如果 $r>0$, 则 $A$ 相抵于下述形式的矩阵: $\left[\begin{array}{cc}I_{r}&0\\0&0\end{array}\right]$.

> **定义 5.3.1 (广义逆)**
> 
> 设 $A$ 是数域 $K$ 上 $s\times{}n$ 矩阵. 如果矩阵 $G$ 满足 $AGA=A$, 则称 $G$ 是 $A$ 的一个广义逆, 记作 $A^{-}$. ## 5.1-1 在平面 $S$ (点集) 上定义一个二元关系: $$P\left(x_{1},y_{1}\right)\sim{}P\left(x_{2},y_{2}\right)\overset{def}{\Leftrightarrow}x_{1}=x_{2}.$$ 证明: $\sim$ 是 $S$ 上的一个等价关系. 按**定义 5.1.1 (二元关系)**, **定义 5.1.2 (等价关系)**, 需验证反身性, 对称性和传递性. 反身性: 对任意 $P\left(x,y\right)\in{}S$, 显然 $x=x$, 故 $P\sim{}P$. 对称性: 若 $P\left(x_{1},y_{1}\right)\sim{}P\left(x_{2},y_{2}\right)$, 则 $x_{1}=x_{2}$, 从而 $x_{2}=x_{1}$, 故 $P\left(x_{2},y_{2}\right)\sim{}P\left(x_{1},y_{1}\right)$. 传递性: 若 $P\left(x_{1},y_{1}\right)\sim{}P\left(x_{2},y_{2}\right)$ 且 $P\left(x_{2},y_{2}\right)\sim{}P\left(x_{3},y_{3}\right)$, 则 $x_{1}=x_{2}$ 且 $x_{2}=x_{3}$, 从而 $x_{1}=x_{3}$, 故 $P\left(x_{1},y_{1}\right)\sim{}P\left(x_{3},y_{3}\right)$. 因此 $\sim$ 满足**定义 5.1.2 (等价关系)**的全部条件, 故 $\sim$ 是 $S$ 上的等价关系. $\blacksquare$

## 5.2-1(3)

求下列矩阵的相抵标准形:

$$
A=\left[\begin{array}{rr}
1&-2\\
-3&-6\\
2&-4
\end{array}\right].
$$

### 解答 5.2-1(3)

由**定理 5.2.1 (相抵标准形)**, 对 $A$ 作初等行变换:

$$
A=\left[\begin{array}{rr}
1&-2\\
-3&-6\\
2&-4
\end{array}\right]
arrow
\left[\begin{array}{rr}
1&-2\\
0&-12\\
0&0
\end{array}\right]
arrow
\left[\begin{array}{rr}
1&-2\\
0&1\\
0&0
\end{array}\right]
arrow
\left[\begin{array}{rr}
1&0\\
0&1\\
0&0
\end{array}\right].
$$

因此由**定理 5.2.1 (相抵标准形)**, 相抵标准形为

$$
\left[\begin{array}{c}I_{2}\\0\end{array}\right].
$$

$\blacksquare$

## 5.2-4

证明: 任意一个秩为 $r$ ( $r>0$ ) 的矩阵都可以表示成 $r$ 个秩为 $1$ 的矩阵之和.

### 解答 5.2-4

由**定理 5.2.1 (相抵标准形)**, 设 $A$ 是 $s\times{}n$ 矩阵, $\operatorname{rank}\left(A\right)=r>0$. 由**定义 5.2.1 (相抵)**标准形定理, 存在 $s$ 级可逆矩阵 $P$ 和 $n$ 级可逆矩阵 $Q$, 使得

$$
A=P\left[\begin{array}{cc}I_{r}&0\\0&0\end{array}\right]Q.
$$

把中间的矩阵写成 $r$ 个矩阵之和:

$$
\left[\begin{array}{cc}I_{r}&0\\0&0\end{array}\right]=E_{11}+E_{22}+\cdots+E_{rr},
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

因此 $A$ 可以表示成 $r$ 个秩为 $1$ 的矩阵之和.

$\blacksquare$

## 5.2-5

设 $A,B$ 分别是 $s\times{}n$, $n\times{}m$ 矩阵, 证明西尔维斯特秩不等式:

$$
\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right)-n.
$$

### 解答 5.2-5

由**定理 5.2.1 (相抵标准形)**的思路, 考虑分块矩阵

$$
M=\left[\begin{array}{cc}A&0\\I_{n}&B\end{array}\right].
$$

求 $\operatorname{rank}\left(M\right)$ 的上界.

作分块矩阵的初等列变换: 用 $-B$ 右乘第 $1$ 块列, 加到第 $2$ 块列上.

$$
M=\left[\begin{array}{cc}A&0\\I_{n}&B\end{array}\right]
arrow
\left[\begin{array}{cc}A&-AB\\I_{n}&0\end{array}\right].
$$

再作分块矩阵的初等行变换: 交换第 $1$ 块行和第 $2$ 块行.

$$
arrow
\left[\begin{array}{cc}I_{n}&0\\A&-AB\end{array}\right].
$$

这是分块上三角矩阵, 故

$$
\operatorname{rank}\left(M\right)=\operatorname{rank}\left(I_{n}\right)+\operatorname{rank}\left(-AB\right)=n+\operatorname{rank}\left(AB\right).
$$

求 $\operatorname{rank}\left(M\right)$ 的下界.

设 $\operatorname{rank}\left(A\right)=r_{1}$, $\operatorname{rank}\left(B\right)=r_{2}$.

$A$ 有 $r_{1}$ 个线性无关的行, $B$ 有 $r_{2}$ 个线性无关的行.

$M$ 的前 $s$ 行中, $A$ 的 $r_{1}$ 个线性无关行对应到 $M$ 中也是线性无关的 (因为右边的 $0$ 不影响).

$M$ 的后 $n$ 行中, $B$ 的 $r_{2}$ 个线性无关行对应到 $M$ 中.

假设这些行与前面的行合起来线性相关, 即存在系数 $k_{1},k_{2}$ 使得

$$
k_{1}\left(\text{前~}s\text{~行的线性组合}\right)+k_{2}\left(\text{后~}n\text{~行的线性组合}\right)=0.
$$

看后 $m$ 个分量:

$$
k_{2}\left(B\text{~的行的线性组合}\right)=0.
$$

因为 $B$ 的行线性无关, 故 $k_{2}=0$.

再看前 $s$ 个分量:

$$
k_{1}\left(A\text{~的行的线性组合}\right)=0.
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

即

$$
\operatorname{rank}\left(AB\right)\ge\operatorname{rank}\left(A\right)+\operatorname{rank}\left(B\right)-n.
$$

$\blacksquare$

## 5.3-1

设 $A$ 是数域 $K$ 上 $s\times{}n$ 矩阵. 证明: 如果 $A$ 行满秩, 则对于 $A$ 的任意一个广义逆 $A^{-}$, 都有 $AA^{-}=I_{s}$.

### 解答 5.3-1

由**定义 5.3.1 (广义逆)**, $A^{-}$ 是 $A$ 的广义逆, 即 $AA^{-}A=A$. 设 $A$ 行满秩, 即 $\operatorname{rank}\left(A\right)=s$.

令 $B=AA^{-}$. 则 $B$ 是 $s\times{}s$ 矩阵.

由 $AA^{-}A=A$, 两边右乘 $A^{-}$:

$$
\left(AA^{-}A\right)A^{-}=AA^{-}.
$$

即

$$
AA^{-}\left(AA^{-}\right)=AA^{-}.
$$

因此

$$
BB=B,
$$

即 $B$ 是幂等矩阵.

求 $B$ 的秩.

因为 $A$ 行满秩, $\operatorname{rank}\left(A\right)=s$.

又因为 $AA^{-}A=A$, 故

$$
\operatorname{rank}\left(A\right)=\operatorname{rank}\left(AA^{-}A\right)\le\operatorname{rank}\left(AA^{-}\right)\le\operatorname{rank}\left(A\right).
$$

因此

$$
\operatorname{rank}\left(B\right)=\operatorname{rank}\left(AA^{-}\right)=\operatorname{rank}\left(A\right)=s.
$$

所以 $B$ 是 $s\times{}s$ 矩阵, 且 $\operatorname{rank}\left(B\right)=s$, 即 $B$ 可逆.

由 $BB=B$, 两边左乘 $B^{-1}$:

$$
B=I_{s}.
$$

因此, 由**定义 5.3.1 (广义逆)**, 对于 $A$ 的任意一个广义逆 $A^{-}$, 都有

$$
AA^{-}=I_{s}.
$$

$\blacksquare$

## 5.4-3

证明: 如果 $A_{1}\sim{}B_{1}$, $A_{2}\sim{}B_{2}$, 则

$$
\left[\begin{array}{cc}A_{1}&0\\0&A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1}&0\\0&B_{2}\end{array}\right].
$$

### 解答 5.4-3

由**定义 5.4.1 (相似)**, 因为 $A_{1}\sim{}B_{1}$, 故存在可逆矩阵 $P_{1}$, 使得 $P_{1}^{-1}A_{1}P_{1}=B_{1}$.

同理, 存在可逆矩阵 $P_{2}$, 使得 $P_{2}^{-1}A_{2}P_{2}=B_{2}$.

令

$$
P=\left[\begin{array}{cc}P_{1}&0\\0&P_{2}\end{array}\right].
$$

因为 $P_{1},P_{2}$ 可逆, 故 $P$ 可逆, 且

$$
P^{-1}=\left[\begin{array}{cc}P_{1}^{-1}&0\\0&P_{2}^{-1}\end{array}\right].
$$

计算:

$$
P^{-1}\left[\begin{array}{cc}A_{1}&0\\0&A_{2}\end{array}\right]P
=\left[\begin{array}{cc}P_{1}^{-1}&0\\0&P_{2}^{-1}\end{array}\right]\left[\begin{array}{cc}A_{1}&0\\0&A_{2}\end{array}\right]\left[\begin{array}{cc}P_{1}&0\\0&P_{2}\end{array}\right]=\left[\begin{array}{cc}P_{1}^{-1}A_{1}P_{1}&0\\0&P_{2}^{-1}A_{2}P_{2}\end{array}\right]=\left[\begin{array}{cc}B_{1}&0\\0&B_{2}\end{array}\right].
$$

因此由**定义 5.4.1 (相似)**,

$$
\left[\begin{array}{cc}A_{1}&0\\0&A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1}&0\\0&B_{2}\end{array}\right].
$$

$\blacksquare$

## 5.4-8

证明: 如果 $A$ 可对角化, 则 $A\sim{}A^{\top}$.

### 解答 5.4-8

由**定理 5.4.2 (可对角化的充要条件)**, 因为 $A$ 可对角化, 故存在可逆矩阵 $P$, 使得

$$
P^{-1}AP=D,
$$

其中 $

D$ 是对角矩阵. 对角矩阵的转置仍是对角矩阵, 即 $D^{\top}=D$.

两边取转置:

$$
\left(P^{-1}AP\right)^{\top}=D^{\top}=D.
$$

即

$$
P^{\top}A^{\top}\left(P^{-1}\right)^{\top}=D.
$$

令 $Q=\left(P^{\top}\right)^{-1}$. 则 $Q^{-1}=P^{\top}$.

上式化为

$$
Q^{-1}A^{\top}Q=D.$
$
因此
$$

A^{\top}\sim{D}.

$$
又因为$A\sim{}D$,故由相似关系的对称性和传递性,
$$

A\sim{A}^{\top}.

$$
$\blacksquare$

##5.4-9
证明:如果数域$K$上的$n$级矩阵$A,B$满足
$$

AB-BA=A,

$$
则$A$不
可逆.
###解答5.4-9
由相似矩阵的不变量,相似的矩阵有相等的迹.假设$A$可逆.
由$AB-BA=A$,两边左乘$A^{-1}$:
$$

A^{-1}AB-A^{-1}BA=A^{-1}A.

$$
即
$$

B-A^{-1}BA=I.

$$
令
$C=A^{-1}BA$.则$B-C=I$.
两边取迹:
$$

\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(I\right)=n.

$$
另一方面,由相似矩阵的不变量,
$$

\operatorname{tr}\left(C\right)=\operatorname{tr}\left(A^{-1}BA\right)=\operatorname{tr}\left(BAA^{-1}\right)=\operatorname{tr}\left(B\right).

$$
因此
$$

\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(B\right)-\operatorname{tr}\left(C\right)=0.

$$
矛盾.
因此假设不成立, 即 $A$ 不可逆.
$\blacksquare$
