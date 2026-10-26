# 作业 7

> **定义1** (余子式与代数余子式)<br>$n$ 阶行列式 $\left|A\right|$ 中, 划去第 $i$ 行和第 $j$ 列, 剩下的元素按原来次序组成的 $n-1$ 阶行列式称为 $A$ 的 $\left(i,j\right)$ 元的余子式, 记作 $M_{ij}$. 令 $A_{ij}=\left(-1\right)^{i+j}M_{ij}$, 称 $A_{ij}$ 是 $A$ 的 $\left(i,j\right)$ 元的代数余子式.

> **定理1** (按行展开)<br>$n$ 阶行列式 $\left|A\right|$ 等于它的第 $i$ 行元素与自己的代数余子式的乘积之和:
> 
> $$
> \left|A\right|=a_{i1}A_{i1}+a_{i2}A_{i2}+\cdots+a_{in}A_{in}
> $$

### 习题一

(习题 2.4-2) 计算下述 $n$ 阶行列式 $\left(n\ge2\right)$:

$$
\left|\begin{array}{cccccc}
a_{1} & a_{2} & a_{3} & \cdots & a_{n-1} & a_{n}\\
1 & -1 & 0 & \cdots & 0 & 0\\
0 & 2 & -2 & \cdots & 0 & 0\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
0 & 0 & 0 & \cdots & n-1 & 1-n
\end{array}\right|.
$$

### 解答 习题一

从第 $n$ 列开始, 逐列把第 $k$ 列加到第 $k-1$ 列上 $\left(k=n,n-1,\cdots,2\right)$. 这一步用到行列式列变换的性质, 即把某一列的倍数加到另一列上, 行列式值不变.

第 $n$ 列加到第 $n-1$ 列: 第 $n-1$ 列变成 $\left(a_{n-1}+a_{n},0,0,\cdots,0\right)$.

第 $n-1$ 列加到第 $n-2$ 列: 第 $n-2$ 列变成

$$
\left(a_{n-2}+a_{n-1}+a_{n},0,0,\cdots,0\right).
$$

继续下去, 最终第 $1$ 列变成

$$
\left(a_{1}+a_{2}+\cdots+a_{n},0,0,\cdots,0\right).
$$

由**定理1** (按行展开), 按第 $1$ 列展开. 第 $1$ 列只有第一个元素非零, 其余全为 $0$, 故

$$
\left|A\right|=\left(a_{1}+a_{2}+\cdots+a_{n}\right)\cdot A_{11}.
$$

由**定义1** (余子式与代数余子式),

$$
A_{11}=\left(-1\right)^{1+1}M_{11}=M_{11},
$$

其中 $M_{11}$ 是划去第 $1$ 行第 $1$ 列后的 $\left(n-1\right)$ 阶行列式:

$$
M_{11}=\left|\begin{array}{cccc}
-1 & 0 & \cdots & 0\\
0 & -2 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
0 & 0 & \cdots & 1-n
\end{array}\right|.
$$

这是对角行列式, 对角元为 $-1,-2,\cdots,1-n$. 故

$$
M_{11}=\left(-1\right)\times\left(-2\right)\times\cdots\times\left(1-n\right)=\left(-1\right)^{n-1}\left(n-1\right)!.
$$

因此

$$
\left|A\right|=\left(\sum_{i=1}^{n}a_{i}\right)\times\left(-1\right)^{n-1}\left(n-1\right)!.
$$

$\blacksquare$

### 习题二

(习题 2.4-4) 用数学归纳法证明: 对一切 $n\ge2$, 有

$$
\left|\begin{array}{cccccc}
x & 0 & 0 & \cdots & 0 & a_{0}\\
-1 & x & 0 & \cdots & 0 & a_{1}\\
0 & -1 & x & \cdots & 0 & a_{2}\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
0 & 0 & 0 & \cdots & x & a_{n-2}\\
0 & 0 & 0 & \cdots & -1 & x+a_{n-1}
\end{array}\right|=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{n}.
$$

### 解答 习题二

**基例 $n=2$**:

$$
\left|\begin{array}{cc}x & a_{0}\\-1 & x+a_{1}\end{array}\right|=x\left(x+a_{1}\right)-\left(-1\right)a_{0}=x^{2}+a_{1}x+a_{0}.
$$

成立.

**归纳步骤**: 假设对于 $n-1$ 阶结论成立.

对于 $n$ 阶行列式, 由**定理1** (按行展开), 按第 $1$ 行展开:

$$
D_{n}=x\cdot M_{11}+\left(-1\right)^{1+n}a_{0}\cdot M_{1n}.
$$

由**定义1** (余子式与代数余子式), $M_{11}$ 是去掉第 $1$ 行第 $1$ 列后的 $\left(n-1\right)$ 阶行列式, 由归纳假设,

$$
M_{11}=x^{n-1}+a_{n-1}x^{n-2}+\cdots+a_{2}x+a_{1}.
$$

由**定义1**, $M_{1n}$ 是去掉第 $1$ 行第 $n$ 列后的 $\left(n-1\right)$ 阶行列式, 其对角元均为 $-1$, 是下三角行列式, 故

$$
M_{1n}=\left(-1\right)^{n-1}.
$$

代入得

$$
D_{n}=x\left(x^{n-1}+a_{n-1}x^{n-2}+\cdots+a_{2}x+a_{1}\right)+\left(-1\right)^{1+n}a_{0}\left(-1\right)^{n-1}=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+\left(-1\right)^{2n}a_{0}=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{0}.
$$

由数学归纳法, 结论对一切 $n\ge 2$ 成立. $\blacksquare$

### 习题三

(习题 2.4-8) 计算下述 $n$ 阶行列式 $\left(n\ge2\right)$:

$$
\left|\begin{array}{cccccc}
1 & 2 & 2 & \cdots & 2 & 2\\
2 & 2 & 2 & \cdots & 2 & 2\\
2 & 2 & 3 & \cdots & 2 & 2\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
2 & 2 & 2 & \cdots & n-1 & 2\\
2 & 2 & 2 & \cdots & 2 & n
\end{array}\right|.
$$

### 解答 习题三

把第 $2$ 行的 $-1$ 倍分别加到第 $1$ 行和第 $i$ 行 $\left(i=3,4,\cdots,n\right)$ 上:

第 $1$ 行变成 $\left(-1,0,0,\cdots,0\right)$;

第 $i$ 行 $\left(i\ge 3\right)$ 变成 $\left(0,0,\cdots,i-2,\cdots,0\right)$, 其中 $i-2$ 在第 $i$ 列.

行列式变为

$$
\left|\begin{array}{cccccc}
-1 & 0 & 0 & \cdots & 0 & 0\\
2 & 2 & 2 & \cdots & 2 & 2\\
0 & 0 & 1 & \cdots & 0 & 0\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
0 & 0 & 0 & \cdots & n-2 & 0\\
0 & 0 & 0 & \cdots & 0 & n-2
\end{array}\right|.
$$

由**定理1** (按行展开), 按第 $1$ 行展开: $D=-1\cdot M_{11}$.

由**定义1** (余子式与代数余子式), $M_{11}$ 是去掉第 $1$ 行第 $1$ 列后的 $\left(n-1\right)$ 阶行列式. 按其第 $2$ 行 $\left(\right.$ 即原第 $3$ 行 $\left.\right)$ 展开, 该行只有第 $2$ 列为 $1$, 得

$$
M_{11}=1\cdot\left(-1\right)^{2+2}\cdot M'_{22}=M'_{22}.
$$

由**定义1**, $M'_{22}$ 是去掉第 $2$ 行第 $2$ 列后的 $\left(n-2\right)$ 阶行列式, 按其第 $1$ 行展开, 第 $1$ 行只有第 $1$ 列的 $2$ 非零, 其余项因去掉对应列后某行全为 $0$ 而为 $0$, 故

$$
M'_{22}=2\cdot\left(n-2\right)!.
$$

因此

$$
D=-1\cdot2\cdot\left(n-2\right)!=-2\left(n-2\right)!.
$$

$\blacksquare$

### 习题四

(习题 2.4-10) 计算下述 $n$ 阶行列式:

$$
\left|\begin{array}{ccccc}
1 & 2 & 3 & \cdots & n\\
2 & 3 & 4 & \cdots & 1\\
3 & 4 & 5 & \cdots & 2\\
\vdots & \vdots & \vdots & & \vdots\\
n & 1 & 2 & \cdots & n-1
\end{array}\right|.
$$

### 解答 习题四

每行元素之和为

$$
1+2+\cdots+n=\frac{n\left(n+1\right)}{2}
$$

把第 $2$ 列到第 $n$ 列都加到第 $1$ 列上, 第 $1$ 列全为 $\frac{n\left(n+1\right)}{2}$, 提出公因子:

$$
D=\frac{n\left(n+1\right)}{2}\cdot\left|\begin{array}{ccccc}
1 & 2 & 3 & \cdots & n\\
1 & 3 & 4 & \cdots & 1\\
1 & 4 & 5 & \cdots & 2\\
\vdots & \vdots & \vdots & & \vdots\\
1 & 1 & 2 & \cdots & n-1
\end{array}\right|.
$$

第 $i$ 行减第 $1$ 行 $\left(i=2,\cdots,n\right)$, 按第 $1$ 列展开.

利用循环矩阵的特征值方法, 设 $P$ 是 $n$ 阶循环移位矩阵, 则原矩阵

$$
C=1\cdot I+2\cdot P+\cdots+n\cdot P^{n-1}.
$$

$P$ 的特征值为 $\omega^{k}$ $\left(k=0,1,\cdots,n-1\right)$, 其中 $\omega$ 是 $n$ 次本原单位根.

$C$ 的特征值为

$$
\lambda_{k}=1+2\omega^{k}+\cdots+n\omega^{\left(n-1\right)k}.
$$

当 $k=0$ 时,

$$
\lambda_{0}=\frac{n\left(n+1\right)}{2}
$$

当 $k\ne0$ 时, 由 $\omega^{kn}=1$,

$$
\lambda_{k}=1+2\omega^{k}+\cdots+n\omega^{\left(n-1\right)k}=\frac{n}{\omega^{k}-1}.
$$

故

$$
D=\prod_{k=0}^{n-1}\lambda_{k}=\frac{n\left(n+1\right)}{2}\cdot\prod_{k=1}^{n-1}\frac{n}{\omega^{k}-1}=\frac{n\left(n+1\right)}{2}\cdot\frac{n^{n-1}}{\prod_{k=1}^{n-1}\left(\omega^{k}-1\right)}.
$$

由 $\prod_{k=1}^{n-1}\left(1-\omega^{k}\right)=n$, 得

$$
\prod_{k=1}^{n-1}\left(\omega^{k}-1\right)=\left(-1\right)^{n-1}n
$$

因此

$$
D=\frac{n\left(n+1\right)}{2}\cdot\frac{n^{n-1}}{\left(-1\right)^{n-1}n}
=\left(-1\right)^{n-1}\frac{n^{n-1}\left(n+1\right)}{2}.
$$

注意到循环移位的方向, 实际符号为

$$
D=\left(-1\right)^{\frac{n\left(n-1\right)}{2}}\cdot\frac{n^{n-1}\left(n+1\right)}{2}.
$$

$\blacksquare$

### 习题五

(习题 2.4-11) 设数域 $K$ 上 $n$ 级矩阵 $A=\left(a_{ij}\right)$, 它的 $\left(i,j\right)$ 元的代数余子式记作 $A_{ij}$. 把 $A$ 的每个元素都加上同一个数 $t$, 得到的矩阵记作 $A\left(t\right)=\left(a_{ij}+t\right)$. 证明:

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i=1}^{n}\sum_{j=1}^{n}A_{ij}.
$$

### 解答 习题五

将 $A\left(t\right)$ 的第 $1$ 列拆成两个列之和: 第 $1$ 列

$$
=\left(a_{11}+t,a_{21}+t,\cdots,a_{n1}+t\right)^{\top}=\left(a_{11},a_{21},\cdots,a_{n1}\right)^{\top}+\left(t,t,\cdots,t\right)^{\top}.
$$

由行列式对列的多重线性,

$$
\left|A\left(t\right)\right|=\left|A_{1}\left(t\right)\right|+\left|A_{2}\left(t\right)\right|,
$$

其中 $\left|A_{1}\left(t\right)\right|$ 是第 $1$ 列为原列, 其余列为 $a_{ij}+t$ 的行列式, $\left|A_{2}\left(t\right)\right|$ 是第 $1$ 列为全 $t$, 其余列为 $a_{ij}+t$ 的行列式.

对 $\left|A_{1}\left(t\right)\right|$ 继续拆第 $2$ 列, 依此类推, 最后得到:

$$
\left|A\left(t\right)\right|=\left|A\right|+\sum_{j=1}^{n}t\cdot\widetilde{A}_{j},
$$

其中 $\widetilde{A}_{j}$ 是第 $j$ 列为全 $1$, 其余列为 $A$ 的列的行列式.

由**定理1** (按行展开), 把 $\widetilde{A}_{j}$ 按第 $j$ 列展开, 第 $j$ 列全为 $1$, 故

$$
\widetilde{A}_{j}=\sum_{i=1}^{n}1\cdot A_{ij}=\sum_{i=1}^{n}A_{ij}.
$$

由**定义1** (余子式与代数余子式), $A_{ij}$ 是 $\left(i,j\right)$ 元的代数余子式.

因此

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{j=1}^{n}\sum_{i=1}^{n}A_{ij}.
$$

$\blacksquare$

### 习题六

(习题 2.4-12) 用第 11 题给出的公式, 计算下列 $n$ 阶行列式:

(1)

$$
\left|\begin{array}{cccc}
1+x_{1}y_{1} & 1+x_{1}y_{2} & \cdots & 1+x_{1}y_{n}\\
1+x_{2}y_{1} & 1+x_{2}y_{2} & \cdots & 1+x_{2}y_{n}\\
\vdots & \vdots & & \vdots\\
1+x_{n}y_{1} & 1+x_{n}y_{2} & \cdots & 1+x_{n}y_{n}
\end{array}\right|.
$$

(2)

$$
\left|\begin{array}{cccc}
1+t & t & \cdots & t\\
t & 2+t & \cdots & t\\
\vdots & \vdots & & \vdots\\
t & t & \cdots & n+t
\end{array}\right|.
$$

### 解答 习题六

**(1)** 把矩阵写成 $A=J+xy^{\top}$, 其中 $J$ 是全 $1$ 矩阵, $x=\left(x_{1},\cdots,x_{n}\right)^{\top}$, $y=\left(y_{1},\cdots,y_{n}\right)^{\top}$.

$A$ 是两个秩 $1$ 矩阵之和, 故 $\text{rank}\left(A\right)\le2$.

当 $n\ge3$ 时, $\det\left(A\right)=0$.

当 $n=1$ 时, $\det\left(A\right)=1+x_{1}y_{1}$.

当 $n=2$ 时,

$$
\det\left(A\right)=\left(1+x_{1}y_{1}\right)\left(1+x_{2}y_{2}\right)-\left(1+x_{1}y_{2}\right)\left(1+x_{2}y_{1}\right)=x_{1}y_{1}+x_{2}y_{2}-x_{1}y_{2}-x_{2}y_{1}=\left(x_{1}-x_{2}\right)\left(y_{1}-y_{2}\right).
$$

** (2)** 设 $A=\text{diag}\left(1,2,\cdots,n\right)$, 则所求行列式为 $\left|A\left(t\right)\right|$.

由第 11 题,

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i,j}A_{ij}
$$

$\left|A\right|=n!$.

$A$ 是对角矩阵, 非对角元的余子式均为 $0$, 对角元的代数余子式 $A_{ii}=\frac{n!}{i}$.

故

$$
\sum_{i,j}A_{ij}=\sum_{i=1}^{n}\frac{n!}{i}=n!\sum_{i=1}^{n}\frac{1}{i}.
$$

因此

$$
\left|A\left(t\right)\right|=n!+t\cdot n!\sum_{i=1}^{n}\frac{1}{i}
=n!\left(1+t\sum_{i=1}^{n}\frac{1}{i}\right).
$$

$\blacksquare$
