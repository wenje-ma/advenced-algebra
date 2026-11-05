# week4

> **性质 2.3.2 (一行的公因子可以提出去)**
> 
> 行列式一行的公因子可以提出去; 特别地, 若行列式中有一行为零(该行元素全为 $0$), 则行列式的值为 $0$.

> **性质 2.3.3 (某行为两组数之和则可拆分)**
> 
> 行列式中若有某一行是两组数的和, 则此行列式等于两个行列式的和, 这两个行列式的这一行分别是第一组数和第二组数, 而其余各行与原来行列式的相应各行相同.

> **性质 2.3.5 (两行相同则行列式为零)**
> 
> 行列式中有两行相同, 则行列式的值为 $0$; 进而若两行成比例, 行列式的值也为 $0$.

> **性质 2.3.7 (把一行的倍数加到另一行上值不变)**
> 
> 把一行的倍数加到另一行上, 行列式的值不变.

> **定理 2.4.1 (行列式按一行(列)展开)**
> 
> $n$ 阶行列式 $\left|A\right|$ 等于它的第 $i$ 行元素与自己的代数余子式的乘积之和:

$$
\left|A\right|=a_{i1}A_{i1}+a_{i2}A_{i2}+\cdots+a_{in}A_{in}.
$$

> **定义 2.4.1 (余子式与代数余子式)**
> 
> $n$ 阶行列式 $\left|A\right|$ 中, 划去第 $i$ 行和第 $j$ 列, 剩下的元素按原来次序组成的 $n-1$ 阶行列式称为 $A$ 的 $\left(i,j\right)$ 元的余子式, 记作 $M_{ij}$. 令 $A_{ij}=\left(-1\right)^{i+j}M_{ij}$, 称 $A_{ij}$ 是 $A$ 的 $\left(i,j\right)$ 元的代数余子式.

## 2.3-3(1)

证明:

$$
\left|\begin{array}{ccc}
a_{1}-b_{1} & b_{1}-c_{1} & c_{1}-a_{1}\\
a_{2}-b_{2} & b_{2}-c_{2} & c_{2}-a_{2}\\
a_{3}-b_{3} & b_{3}-c_{3} & c_{3}-a_{3}
\end{array}\right|=0.
$$

### 解答 2.3-3(1)

注意到行列式的第 $1$ 列, 第 $2$ 列, 第 $3$ 列满足: 第 $1$ 列 + 第 $2$ 列 + 第 $3$ 列 $=0$.

具体地, 第 $i$ 行第 $1$ 列 + 第 $i$ 行第 $2$ 列 + 第 $i$ 行第 $3$ 列

$$
=\left(a_{i}-b_{i}\right)+\left(b_{i}-c_{i}\right)+\left(c_{i}-a_{i}\right)=0.
$$

由**性质 2.3.7 (把一行的倍数加到另一行上值不变)**, 把某一列的倍数加到另一列上, 行列式的值不变. 将第 $2$ 列和第 $3$ 列都加到第 $1$ 列上, 第 $1$ 列的所有元素都变成 $0$.

由**性质 2.3.2 (一行的公因子可以提出去)**, 某一列全为 $0$ 的行列式值为 $0$.

故原行列式 $=0$. $\blacksquare$

## 2.3-4(1)

计算下列 $n$ 阶行列式:

$$
\left|\begin{array}{cccc}
a_{1} & a_{2} & \cdots & a_{n}\\
b_{2} & 1 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
b_{n} & 0 & \cdots & 1
\end{array}\right|.
$$

### 解答 2.3-4(1)

由**性质 2.3.7 (把一行的倍数加到另一行上值不变)**, 把某一行的倍数加到另一行上, 行列式的值不变. 把第 $2$ 行的 $-a_{2}$ 倍加到第 $1$ 行, 第 $3$ 行的 $-a_{3}$ 倍加到第 $1$ 行, $\cdots$, 第 $n$ 行的 $-a_{n}$ 倍加到第 $1$ 行, 则第 $1$ 行的第 $2$ 列到第 $n$ 列全部变成 $0$:

$$
\left|\begin{array}{cccc}
a_{1}-\sum_{j=2}^{n}a_{j}b_{j} & 0 & \cdots & 0\\
b_{2} & 1 & \cdots & 0\\
\vdots & \vdots & & \vdots\\
b_{n} & 0 & \cdots & 1
\end{array}\right|.
$$

由**定理 2.4.1 (行列式按一行(列)展开)**, 按第 $1$ 行展开, 余子式为 $\left(n-1\right)$ 阶单位矩阵, 其行列式为 $1$. 故行列式值为

$$
a_{1}-\sum_{j=2}^{n}a_{j}b_{j}.
$$

$\blacksquare$

## 2.3-4(2)

计算下列 $n$ 阶行列式:

$$
\left|\begin{array}{cccc}
a_{1}+b_{1} & a_{1}+b_{2} & \cdots & a_{1}+b_{n}\\
a_{2}+b_{1} & a_{2}+b_{2} & \cdots & a_{2}+b_{n}\\
\vdots & \vdots & & \vdots\\
a_{n}+b_{1} & a_{n}+b_{2} & \cdots & a_{n}+b_{n}
\end{array}\right|.
$$

### 解答 2.3-4(2)

由**性质 2.3.7 (把一行的倍数加到另一行上值不变)**, 把某一行的倍数加到另一行上, 行列式的值不变. 把第 $1$ 行的 $-1$ 倍分别加到第 $2,3,\cdots,n$ 行上, 得

$$
\left|\begin{array}{cccc}
a_{1}+b_{1} & a_{1}+b_{2} & \cdots & a_{1}+b_{n}\\
a_{2}-a_{1} & a_{2}-a_{1} & \cdots & a_{2}-a_{1}\\
\vdots & \vdots & & \vdots\\
a_{n}-a_{1} & a_{n}-a_{1} & \cdots & a_{n}-a_{1}
\end{array}\right|.
$$

当 $n\ge3$ 时, 第 $2$ 行到第 $n$ 行的每一行元素都相同. 由**性质 2.3.5 (两行相同则行列式为零)**, 行列式某两行相同, 则行列式为 $0$. 故 $n\ge3$ 时行列式 $=0$.

当 $n=1$ 时, 行列式 $=a_{1}+b_{1}$.

当 $n=2$ 时, 由**性质 2.3.7 (把一行的倍数加到另一行上值不变)**, 把第 $1$ 行的 $-1$ 倍加到第 $2$ 行, 得

$$
\left|\begin{array}{cc}
a_{1}+b_{1} & a_{1}+b_{2}\\
a_{2}-a_{1} & a_{2}-a_{1}
\end{array}\right|.
$$

由**性质 2.3.2 (一行的公因子可以提出去)**, 第 $2$ 行有公因子 $a_{2}-a_{1}$, 提出得:

$$
\left(a_{2}-a_{1}\right)\times\left|\begin{array}{cc}
a_{1}+b_{1} & a_{1}+b_{2}\\
1 & 1
\end{array}\right|.
$$

由**性质 2.3.7 (把一行的倍数加到另一行上值不变)**, 把第 $2$ 列的 $-1$ 倍加到第 $1$ 列, 得

$$
\left(a_{2}-a_{1}\right)\times\left|\begin{array}{cc}
b_{1}-b_{2} & a_{1}+b_{2}\\
0 & 1
\end{array}\right|.
$$

由**定理 2.4.1 (行列式按一行(列)展开)**, 按第 $2$ 列展开, 得

$$
\left(a_{2}-a_{1}\right)\times\left(b_{1}-b_{2}\right)=\left(a_{1}-a_{2}\right)\left(b_{2}-b_{1}\right).
$$

综上:

$$
\det\left(A\right)=
\begin{cases}
a_{1}+b_{1}, & n=1,\\
\left(a_{1}-a_{2}\right)\left(b_{2}-b_{1}\right), & n=2,\\
0, & n\ge3.
\end{cases}
$$

$\blacksquare$

## 2.4-2

计算下述 $n$ 阶行列式 $\left(n\ge2\right)$:

$$
\left|\begin{array}{cccccc}
a_{1} & a_{2} & a_{3} & \cdots & a_{n-1} & a_{n}\\
1 & -1 & 0 & \cdots & 0 & 0\\
0 & 2 & -2 & \cdots & 0 & 0\\
\vdots & \vdots & \vdots & & \vdots & \vdots\\
0 & 0 & 0 & \cdots & n-1 & 1-n
\end{array}\right|.
$$

### 解答 2.4-2

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

由**定理 2.4.1 (行列式按一行(列)展开)**, 按第 $1$ 列展开. 第 $1$ 列只有第一个元素非零, 其余全为 $0$, 故

$$
\left|A\right|=\left(a_{1}+a_{2}+\cdots+a_{n}\right)\cdot A_{11}.
$$

由**定义 2.4.1 (余子式与代数余子式)**,

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

## 2.4-4

用数学归纳法证明: 对一切 $n\ge2$, 有

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

### 解答 2.4-4

基例 $n=2$:

$$
\left|\begin{array}{cc}x & a_{0}\\-1 & x+a_{1}\end{array}\right|=x\left(x+a_{1}\right)-\left(-1\right)a_{0}=x^{2}+a_{1}x+a_{0}.
$$

成立.

归纳步骤: 假设对于 $n-1$ 阶结论成立.

对于 $n$ 阶行列式, 由**定理 2.4.1 (行列式按一行(列)展开)**, 按第 $1$ 行展开:

$$
D_{n}=x\cdot M_{11}+\left(-1\right)^{1+n}a_{0}\cdot M_{1n}.
$$

由**定义 2.4.1 (余子式与代数余子式)**, $M_{11}$ 是去掉第 $1$ 行第 $1$ 列后的 $\left(n-1\right)$ 阶行列式, 由归纳假设,

$$
M_{11}=x^{n-1}+a_{n-1}x^{n-2}+\cdots+a_{2}x+a_{1}.
$$

由**定义 2.4.1 (余子式与代数余子式)**, $M_{1n}$ 是去掉第 $1$ 行第 $n$ 列后的 $\left(n-1\right)$ 阶行列式, 其对角元均为 $-1$, 是下三角行列式, 故

$$
M_{1n}=\left(-1\right)^{n-1}.
$$

代入得

$$
D_{n}=x\left(x^{n-1}+a_{n-1}x^{n-2}+\cdots+a_{2}x+a_{1}\right)+\left(-1\right)^{1+n}a_{0}\left(-1\right)^{n-1}=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+\left(-1\right)^{2n}a_{0}=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{0}.
$$

由数学归纳法, 结论对一切 $n\ge 2$ 成立. $\blacksquare$

## 2.4-8

计算下述 $n$ 阶行列式 $\left(n\ge2\right)$:

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

### 解答 2.4-8

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

由**定理 2.4.1 (行列式按一行(列)展开)**, 按第 $1$ 行展开: $D=-1\cdot M_{11}$.

由**定义 2.4.1 (余子式与代数余子式)**, $M_{11}$ 是去掉第 $1$ 行第 $1$ 列后的 $\left(n-1\right)$ 阶行列式. 按其第 $2$ 行(即原第 $3$ 行)展开, 该行只有第 $2$ 列为 $1$, 得

$$
M_{11}=1\cdot\left(-1\right)^{2+2}\cdot M'_{22}=M'_{22}.
$$

由**定义 2.4.1 (余子式与代数余子式)**, $M'_{22}$ 是去掉第 $2$ 行第 $2$ 列后的 $\left(n-2\right)$ 阶行列式, 按其第 $1$ 行展开, 第 $1$ 行只有第 $1$ 列的 $2$ 非零, 其余项因去掉对应列后某行全为 $0$ 而为 $0$, 故

$$
M'_{22}=2\cdot\left(n-2\right)!.
$$

因此

$$
D=-1\cdot2\cdot\left(n-2\right)!=-2\left(n-2\right)!.
$$

$\blacksquare$
