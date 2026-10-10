# 作业 31

> **定理1** (实对称矩阵的特征值)<br>实对称矩阵的特征多项式在复数域中的每一个根都是实数.

> **定理3** (实对称矩阵可正交对角化)<br>对于任意 $n$ 级实对称矩阵 $A$, 一定存在一个 $n$ 级正交矩阵 $T$, 使得 $T^{-1}AT$ 为对角矩阵.

### 习题一

(习题 5.7-1(1)) 对于下列实对称矩阵 $A$, 求正交矩阵 $T$, 使 $T^{T}AT$ 为对角矩阵:

$$
A=\left[\begin{array}{rrr}
0 & -2 & 2\\
-2 & -3 & 4\\
2 & 4 & -3
\end{array}\right].
$$

### 解答 习题一

由**定理3**(实对称矩阵可正交对角化), 一定存在正交矩阵 $T$, 使 $T^{T}AT$ 为对角矩阵. 求特征多项式:

$$
|\lambda I-A|=\left|\begin{array}{rrr}
\lambda & 2 & -2\\
2 & \lambda+3 & -4\\
-2 & -4 & \lambda+3
\end{array}\right|=(\lambda-1)^{2}(\lambda+8).
$$

因此特征值为 $\lambda_{1}=\lambda_{2}=1$, $\lambda_{3}=-8$.

**求 $\lambda=1$ 的特征向量**.

$$
I-A=\left[\begin{array}{rrr}
1 & 2 & -2\\
2 & 4 & -4\\
-2 & -4 & 4
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & 2 & -2\\
0 & 0 & 0\\
0 & 0 & 0
\end{array}\right].
$$

基础解系: $\alpha_{1}=\left(-2,1,0\right)^{T}$, $\alpha_{2}=\left(2,0,1\right)^{T}$.

施密特正交化:

$$
\beta_{1}=\alpha_{1}=\left(-2,1,0\right)^{T}.
$$

$$
\beta_{2}=\alpha_{2}-\frac{\left(\alpha_{2},\beta_{1}\right)}{\left(\beta_{1},\beta_{1}\right)}\beta_{1}
=\left(2,0,1\right)^{T}-\frac{-4}{5}\left(-2,1,0\right)^{T}
=\left(\frac{2}{5},\frac{4}{5},1\right)^{T}.
$$

单位化:

$$
\eta_{1}=\left(-\frac{2}{\sqrt{5}},\frac{1}{\sqrt{5}},0\right)^{T}.
$$

$$
\eta_{2}=\left(\frac{2}{3\sqrt{5}},\frac{4}{3\sqrt{5}},\frac{\sqrt{5}}{3}\right)^{T}.
$$

**求 $\lambda=-8$ 的特征向量**.

$$
-8I-A=\left[\begin{array}{rrr}
-8 & 2 & -2\\
2 & -5 & -4\\
-2 & -4 & -5
\end{array}\right]\rightarrow
\left[\begin{array}{rrr}
1 & 0 & 1/2\\
0 & 1 & 1\\
0 & 0 & 0
\end{array}\right].
$$

基础解系: $\alpha_{3}=\left(-1,2,-4\right)^{T}$.

单位化:

$$
\eta_{3}=\left(-\frac{1}{\sqrt{21}},\frac{2}{\sqrt{21}},-\frac{4}{\sqrt{21}}\right)^{T}.
$$

因此正交矩阵为

$$
T=\left[\begin{array}{ccc}
-2/\sqrt{5} & 2/(3\sqrt{5}) & -1/\sqrt{21}\\
1/\sqrt{5} & 4/(3\sqrt{5}) & 2/\sqrt{21}\\
0 & \sqrt{5}/3 & -4/\sqrt{21}
\end{array}\right].
$$

由**定理3**(实对称矩阵可正交对角化),

$$
T^{T}AT=\operatorname{diag}\left\{1,1,-8\right\}.
$$

$\blacksquare$

### 习题二

(习题 5.7-1(3)) 对于下列实对称矩阵 $A$, 求正交矩阵 $T$, 使 $T^{T}AT$ 为对角矩阵:

$$
A=\left[\begin{array}{rrr}
3 & -2 & 0\\
-2 & 2 & -2\\
0 & -2 & 1
\end{array}\right].
$$

### 解答 习题二

求特征多项式:

$$
|\lambda I-A|=\left|\begin{array}{rrr}
\lambda-3 & 2 & 0\\
2 & \lambda-2 & 2\\
0 & 2 & \lambda-1
\end{array}\right|=(\lambda+1)(\lambda-2)(\lambda-5).
$$

因此特征值为 $\lambda_{1}=-1$, $\lambda_{2}=2$, $\lambda_{3}=5$.

**求 $\lambda=-1$ 的特征向量**.

基础解系: $\alpha_{1}=\left(1,2,2\right)^{T}$.

**求 $\lambda=2$ 的特征向量**.

基础解系: $\alpha_{2}=\left(2,1,-2\right)^{T}$.

**求 $\lambda=5$ 的特征向量**.

基础解系: $\alpha_{3}=\left(-2,2,-1\right)^{T}$.

验证正交性: $\left(\alpha_{1},\alpha_{2}\right)=0$, $\left(\alpha_{1},\alpha_{3}\right)=0$, $\left(\alpha_{2},\alpha_{3}\right)=0$.

单位化:

$$
\eta_{1}=\left(\frac{1}{3},\frac{2}{3},\frac{2}{3}\right)^{T}.
$$

$$
\eta_{2}=\left(\frac{2}{3},\frac{1}{3},-\frac{2}{3}\right)^{T}.
$$

$$
\eta_{3}=\left(-\frac{2}{3},\frac{2}{3},-\frac{1}{3}\right)^{T}.
$$

因此正交矩阵为

$$
T=\left[\begin{array}{rrr}
1/3 & 2/3 & -2/3\\
2/3 & 1/3 & 2/3\\
2/3 & -2/3 & -1/3
\end{array}\right].
$$

$$
T^{T}AT=\operatorname{diag}\left\{-1,2,5\right\}.
$$

$\blacksquare$

### 习题三

(习题 5.7-2) 证明: 如果 $n$ 级实对称矩阵 $A,B$ 有相同的特征多项式, 则 $A$ 与 $B$ 相似.

### 解答 习题三

因为 $A$ 是实对称矩阵, 故 $A$ 正交相似于对角矩阵 $D_{A}$, 且 $D_{A}$ 的主对角元是 $A$ 的全部特征值 (计重数).

同理, $B$ 正交相似于对角矩阵 $D_{B}$, 且 $D_{B}$ 的主对角元是 $B$ 的全部特征值 (计重数).

因为 $A,B$ 有相同的特征多项式, 所以它们有相同的特征值 (计重数).

因此 $D_{A}$ 与 $D_{B}$ 的主对角元相同 (至多排列次序不同).

通过交换 $D_{B}$ 的主对角元的次序, 可使 $D_{A}=D_{B}$.

交换主对角元的次序相当于用一个正交矩阵 $Q$ 作相似变换: $Q^{T}D_{B}Q=D_{A}$.

因此

$$
A\sim D_{A}=D_{B}\sim B.
$$

所以 $A$ 与 $B$ 相似. $\blacksquare$

### 习题四

(习题 5.7-3) 证明: 如果实矩阵 $A$ 正交相似于对角矩阵, 则 $A$ 一定是对称矩阵.

### 解答 习题四

设 $A$ 正交相似于对角矩阵 $D$, 即存在正交矩阵 $T$, 使得

$$
T^{T}AT=D.
$$

则

$$
A=TDT^{T}.
$$

因为 $D$ 是对角矩阵, 故 $D^{T}=D$.

因此

$$
A^{T}=\left(TDT^{T}\right)^{T}=TD^{T}T^{T}=TDT^{T}=A.
$$

所以 $A$ 是对称矩阵. $\blacksquare$
