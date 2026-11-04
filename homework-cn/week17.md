# week17

> **定义 5.4.1 (相似)**
> 
> 设 $A$ 与 $B$ 都是数域 $K$ 上 $n$ 级矩阵, 如果存在数域 $K$ 上的一个 $n$ 级可逆矩阵 $P$, 使得 $P^{-1}AP=B$, 则称 $A$ 与 $B$ 是相似的, 记作 $A\sim B$.

> **定理 5.4.2 (可对角化的充要条件)**
> 
> 数域 $K$ 上的 $n$ 级矩阵 $A$ 能够相似于对角矩阵的充分必要条件是: $K^{n}$ 中有 $n$ 个线性无关的列向量 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 以及 $K$ 中有 $n$ 个数 $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$, 使得 $A\alpha_{i}=\lambda_{i}\alpha_{i}$ ( $i=1,2,\cdots,n$ ).

> **定义 5.5.1 (特征值与特征向量)**
> 
> 设 $A$ 是数域 $K$ 上的 $n$ 级矩阵, 如果 $K^{n}$ 中有非零列向量 $\alpha$, 使得 $A\alpha=\lambda_{0}\alpha$, 且 $\lambda_{0}\in K$, 则称 $\lambda_{0}$ 是 $A$ 的一个特征值, 称 $\alpha$ 是 $A$ 的属于特征值 $\lambda_{0}$ 的一个特征向量.

## 5.4-3

证明: 如果 $A_{1}\sim B_{1}$, $A_{2}\sim B_{2}$, 则

$$
\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right].
$$

### 解答 5.4-3

由**定义 5.4.1 (相似)**, 因为 $A_{1}\sim B_{1}$, 故存在可逆矩阵 $P_{1}$, 使得 $P_{1}^{-1}A_{1}P_{1}=B_{1}$.

同理, 存在可逆矩阵 $P_{2}$, 使得 $P_{2}^{-1}A_{2}P_{2}=B_{2}$.

令

$$
P=\left[\begin{array}{cc}P_{1} & 0\\0 & P_{2}\end{array}\right].
$$

因为 $P_{1},P_{2}$ 可逆, 故 $P$ 可逆, 且

$$
P^{-1}=\left[\begin{array}{cc}P_{1}^{-1} & 0\\0 & P_{2}^{-1}\end{array}\right].
$$

计算:

$$
P^{-1}\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]P
=\left[\begin{array}{cc}P_{1}^{-1} & 0\\0 & P_{2}^{-1}\end{array}\right]\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\left[\begin{array}{cc}P_{1} & 0\\0 & P_{2}\end{array}\right]=\left[\begin{array}{cc}P_{1}^{-1}A_{1}P_{1} & 0\\0 & P_{2}^{-1}A_{2}P_{2}\end{array}\right]=\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right].
$$

因此由**定义 5.4.1 (相似)**,

$$
\left[\begin{array}{cc}A_{1} & 0\\0 & A_{2}\end{array}\right]\sim\left[\begin{array}{cc}B_{1} & 0\\0 & B_{2}\end{array}\right].
$$

$\blacksquare$

## 5.4-8

证明: 如果 $A$ 可对角化, 则 $A\sim A^{\top}$.

### 解答 5.4-8

由**定理 5.4.2 (可对角化的充要条件)**, 因为 $A$ 可对角化, 故存在可逆矩阵 $P$, 使得

$$
P^{-1}AP=D,
$$

其中 $D$ 是对角矩阵.

对角矩阵的转置仍是对角矩阵, 即 $D^{\top}=D$.

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
Q^{-1}A^{\top}Q=D.
$$

因此

$$
A^{\top}\sim D.
$$

又因为 $A\sim D$, 故由相似关系的对称性和传递性,

$$
A\sim A^{\top}.
$$

$\blacksquare$

## 5.4-9

证明: 如果数域 $K$ 上的 $n$ 级矩阵 $A,B$ 满足

$$
AB-BA=A,
$$

则 $A$ 不可逆.

### 解答 5.4-9

由相似矩阵的不变量, 相似的矩阵有相等的迹. 假设 $A$ 可逆.

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

另一方面, 由相似矩阵的不变量,

$$
\operatorname{tr}\left(C\right)=\operatorname{tr}\left(A^{-1}BA\right)=\operatorname{tr}\left(BAA^{-1}\right)=\operatorname{tr}\left(B\right).
$$

因此

$$
\operatorname{tr}\left(B-C\right)=\operatorname{tr}\left(B\right)-\operatorname{tr}\left(C\right)=0.
$$

矛盾.

因此假设不成立, 即 $A$ 不可逆. $\blacksquare$

## 5.4-12

方阵 $A$ 称为幂零矩阵, 如果 $A$ 的某个正整数次幂等于零矩阵, 使 $A^{l}=0$ 成立的最小正整数 $l$ 称为 $A$ 的幂零指数. 证明: 与幂零矩阵相似的矩阵仍是幂零矩阵, 并且它们的幂零指数相等.

### 解答 5.4-12

设 $A$ 是幂零矩阵, 幂零指数为 $l$, 即 $A^{l}=0$, 且 $A^{k}\ne0$ ( $k< l$ ).

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

## 5.5-1(2)

求下列数域 $K$ 上的矩阵 $A$ 的全部特征值和特征向量:

$$
A=\left[\begin{array}{rrr}
2 & 3 & 2\\
1 & 8 & 2\\
-2 & -14 & -3
\end{array}\right].
$$

### 解答 5.5-1(2)

由**定义 5.5.1 (特征值与特征向量)**, 求特征多项式:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-2 & -3 & -2\\
-1 & \lambda-8 & -2\\
2 & 14 & \lambda+3
\end{array}\right|.
$$

按第 $1$ 行展开:

$$
\left|\lambda I-A\right|
=\left(\lambda-2\right)\left[\left(\lambda-8\right)\left(\lambda+3\right)+28\right]+3\left[-\left(\lambda+3\right)+4\right]-2\left[-14-2\left(\lambda-8\right)\right]=\left(\lambda-2\right)\left(\lambda^{2}-5\lambda+4\right)+3\left(-\lambda+1\right)-2\left(2-2\lambda\right)=\left(\lambda-2\right)\left(\lambda-1\right)\left(\lambda-4\right)-3\lambda+3-4+4\lambda=\left(\lambda-1\right)\left[\left(\lambda-2\right)\left(\lambda-4\right)+1\right]=\left(\lambda-1\right)\left(\lambda^{2}-6\lambda+9\right)=\left(\lambda-1\right)\left(\lambda-3\right)^{2}.
$$

因此特征值为 $\lambda_{1}=1$, $\lambda_{2}=\lambda_{3}=3$.

**求 $\lambda=1$ 的特征向量**.

$$
I-A=\left[\begin{array}{rrr}
-1 & -3 & -2\\
-1 & -7 & -2\\
2 & 14 & 4
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
-1 & -3 & -2\\
0 & -4 & 0\\
0 & 0 & 0
\end{array}\right].
$$

解得 $x_{2}=0$, $x_{1}=-2x_{3}$.

基础解系: $\alpha_{1}=\left(-2,0,1\right)^{\top}$.

**求 $\lambda=3$ 的特征向量**.

$$
3I-A=\left[\begin{array}{rrr}
1 & -3 & -2\\
-1 & -5 & -2\\
2 & 14 & 6
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & -3 & -2\\
0 & -8 & -4\\
0 & 0 & 0
\end{array}\right].
$$

解得 $x_{2}=-\frac{1}{2}x_{3}$, $x_{1}=\frac{1}{2}x_{3}$.

基础解系: $\alpha_{2}=\left(1,-1,2\right)^{\top}$.

$\lambda_{1}=1$ 的特征向量为 $k_{1}\alpha_{1}$ ( $k_{1}\ne0$ ), $\lambda_{2}=\lambda_{3}=3$ 的特征向量为 $k_{2}\alpha_{2}$ ( $k_{2}\ne0$ ). $\blacksquare$

## 5.5-2(2)

求下列复数域上的矩阵 $A$ 的全部特征值和特征向量; 如果把 $A$ 看成实数域上的矩阵, 它有没有特征值? 有多少个特征值?

$$
A=\left[\begin{array}{rrr}
3 & 7 & -3\\
-2 & -5 & 2\\
-4 & -10 & 3
\end{array}\right].
$$

### 解答 5.5-2(2)

由**定义 5.5.1 (特征值与特征向量)**, 求特征多项式:

$$
\left|\lambda I-A\right|=\left|\begin{array}{rrr}
\lambda-3 & -7 & 3\\
2 & \lambda+5 & -2\\
4 & 10 & \lambda-3
\end{array}\right|.
$$

按第 $1$ 行展开:

$$
\left|\lambda I-A\right|
=\left(\lambda-3\right)\left[\left(\lambda+5\right)\left(\lambda-3\right)+20\right]+7\left[2\left(\lambda-3\right)+8\right]+3\left[20-4\left(\lambda+5\right)\right]=\left(\lambda-3\right)\left(\lambda^{2}+2\lambda+5\right)+7\left(2\lambda+2\right)+3\left(-4\lambda\right)=\lambda^{3}-3\lambda^{2}+2\lambda^{2}-6\lambda+5\lambda-15+14\lambda+14-12\lambda=\lambda^{3}-\lambda^{2}+\lambda-1=\left(\lambda-1\right)\left(\lambda^{2}+1\right).
$$

因此特征值为 $\lambda_{1}=1$, $\lambda_{2}=i$, $\lambda_{3}=-i$.

由**定义 5.5.1 (特征值与特征向量)**, 把 $A$ 看成实数域上的矩阵, 只有 $\lambda=1$ 是实数特征值, 故有 $1$ 个特征值.

$\blacksquare$

## 5.5-10

设 $A$ 是一个 $n$ 级正交矩阵, 证明:

(1) 如果 $A$ 有特征值, 则 $A$ 的特征值是 $1$ 或 $-1$;

(2) 如果 $n$ 是奇数, 且 $\left|A\right|=1$, 则 $1$ 是 $A$ 的一个特征值;

(3) 如果 $\left|A\right|=-1$, 则 $-1$ 是 $A$ 的一个特征值.

### 解答 5.5-10

**(1)** 设 $\lambda$ 是 $A$ 的一个特征值, $\alpha$ 是 $A$ 的属于 $\lambda$ 的特征向量, 即 $A\alpha=\lambda\alpha$.

两边取共轭转置: $\alpha^{\top}A^{\top}=\overline{\lambda}\alpha^{\top}$.

因为 $A$ 是正交矩阵, 故 $A^{\top}=A^{-1}$.

所以 $\alpha^{\top}A^{-1}=\overline{\lambda}\alpha^{\top}$.

两边右乘 $A\alpha$:

$$
\alpha^{\top}A^{-1}A\alpha=\overline{\lambda}\alpha^{\top}A\alpha.
$$

即

$$
\alpha^{\top}\alpha=\overline{\lambda}\lambda\alpha^{\top}\alpha.
$$

因为 $\alpha\ne0$, 故 $\alpha^{\top}\alpha\ne0$.

因此

$$
1=\overline{\lambda}\lambda=\left|\lambda\right|^{2}.
$$

所以 $\left|\lambda\right|=1$.

若 $\lambda$ 是实数特征值, 则 $\lambda=\pm1$.

**(2)** $A$ 是 $n$ 级正交矩阵, $n$ 是奇数.

复特征值共轭成对出现, 故复特征值的个数是偶数.

$n$ 是奇数, 故实数特征值的个数是奇数.

实数特征值只能是 $\pm1$.

设 $A$ 有 $k$ 个 $1$, $m$ 个 $-1$, 以及一些复特征值.

$$
\left|A\right|=1^{k}\cdot\left(-1\right)^{m}\cdot\left(\text{复特征值的乘积}\right).
$$

复特征值共轭成对, 每对的乘积是 $\left|\lambda\right|^{2}=1$.

故 $\left|A\right|=\left(-1\right)^{m}$.

已知 $\left|A\right|=1$, 故 $\left(-1\right)^{m}=1$, 即 $m$ 是偶数.

因为 $k+m$ 是奇数 (实数特征值个数), 且 $m$ 是偶数, 故 $k$ 是奇数, 即 $k\ge1$.

因此 $1$ 是 $A$ 的一个特征值.

**(3)** $\left|A\right|=\left(-1\right)^{m}=-1$, 故 $m$ 是奇数, 即 $m\ge1$.

因此 $-1$ 是 $A$ 的一个特征值.

$\blacksquare$
