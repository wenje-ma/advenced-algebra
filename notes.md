# 高等代数

## 线性方程组

**定义 1** (线性方程组的初等变换)

对线性方程组施行以下三种变换: (1) 把一个方程的倍数加到另一个方程上; (2) 互换两个方程的位置; (3) 用一个非零数乘某一个方程. 这三种变换统称为线性方程组的初等变换. 经过初等变换得到的方程组与原方程组同解.

**定义 2** (阶梯形矩阵)

矩阵中元素全为 $0$ 的行(零行)在下方; 元素不全为 $0$ 的行(非零行)从左边数起第一个不为 $0$ 的元素称为主元, 各非零行主元的列指标随行指标递增而严格增大.

**定义 3** (简化行阶梯形矩阵)

在阶梯形矩阵基础上, 每个非零行的主元都是 $1$, 且每个主元所在列的其余元素都是 $0$.

**基础知识 1** (高斯-若尔当算法)

把线性方程组的增广矩阵经过初等行变换化成简化行阶梯形矩阵, 从而直接写出解. 若相应阶梯形方程组出现 $0=d$($d\ne 0$), 则原方程组无解.

**定理 1** (线性方程组解的判别准则)

把 $n$ 元线性方程组的增广矩阵经过初等行变换化成阶梯形矩阵: (1) 若相应的阶梯形方程组出现 $0=d$($d\ne 0$), 则原方程组无解; (2) 若不出现 $0=d$, 则有解, 且当非零行数目等于未知量数目时有唯一解, 当非零行数目小于未知量数目时有无穷多个解.

**定义 4** (数域)

设 $K$ 是复数集的一个子集, 如果 $K$ 满足: (1) $0,1\in K$; (2) 对加, 减, 乘, 除(除数不为 $0$)四种运算封闭, 那么称 $K$ 是一个数域.

## 行列式

**定义 5** ($n$ 元排列的逆序数)

在一个 $n$ 元排列中, 若一对数的前后位置与大小顺序相反(即前面的数大于后面的数), 则称它们为一个逆序. 一个排列中逆序的总数称为该排列的逆序数, 记作 $\tau\left(j_{1}j_{2}\cdots j_{n}\right)$.

**命题 1** (二元一次方程组有唯一解的判别)

两个方程的二元一次方程组有唯一解的充分必要条件是它的系数行列式不等于 $0$.

**定义 6** ($n$ 阶行列式)

$n$ 阶行列式是 $n!$ 项的代数和, 其中每一项都是位于不同行, 不同列的 $n$ 个元素的乘积, 把这 $n$ 个元素按照行指标成自然序排好位置, 当列指标所成排列是偶排列时, 该项带正号; 奇排列时, 该项带负号.

**基础知识 2** (行列式的性质)

(1) 行列式的行与列互换(转置), 其值不变; (2) 行列式某一行(列)的公因子可以提到行列式符号外面; (3) 行列式某一行(列)的所有元素都是两项之和, 则行列式可以拆成两个行列式之和; (4) 两行(列)互换, 行列式变号; (5) 两行(列)成比例, 行列式为零; (6) 把一行(列)的倍数加到另一行(列)上, 行列式的值不变.

**定义 7** (余子式与代数余子式)

$n$ 阶行列式 $\left|A\right|$ 中, 划去第 $i$ 行和第 $j$ 列, 剩下的元素按原来次序组成的 $n-1$ 阶行列式称为 $A$ 的 $\left(i,j\right)$ 余子式, 记作 $M_{ij}$. 令 $A_{ij}=\left(-1\right)^{i+j}M_{ij}$, 称 $A_{ij}$ 是 $A$ 的 $\left(i,j\right)$ 代数余子式.

**定理 2** (按行展开)

$n$ 阶行列式 $\left|A\right|$ 等于它的第 $i$ 行元素与自己的代数余子式的乘积之和:

$$
\left|A\right|=a_{i1}A_{i1}+a_{i2}A_{i2}+\cdots+a_{in}A_{in}.
$$

类似地, 按列展开:

$$
\left|A\right|=a_{1j}A_{1j}+a_{2j}A_{2j}+\cdots+a_{nj}A_{nj}.
$$

**定理 3** (克拉默法则)

$n$ 个方程的 $n$ 元线性方程组如果它的系数行列式 $\left|A\right|\ne0$, 则它有唯一解; 如果它的系数行列式 $\left|A\right|=0$, 则它无解或者有无穷多个解.

**推论 1** (齐次方程组有非零解的条件)

$n$ 个方程的 $n$ 元齐次线性方程组只有零解的充分必要条件是它的系数行列式不等于 $0$. 从而, $n$ 个方程的 $n$ 元齐次线性方程组有非零解的充分必要条件是它的系数行列式等于 $0$.

**定理 4** (拉普拉斯定理)

在 $n$ 阶行列式 $\left|A\right|$ 中, 取定 $k$ 行, 则这 $k$ 行元素形成的所有 $k$ 阶子式与它们自己的代数余子式的乘积之和等于 $\left|A\right|$.

**基础知识 3** (分块行列式)

其中 $A,B$ 都是方阵:

$$
\left|\begin{array}{cc}A & 0\\C & B\end{array}\right|=\left|A\right|\left|B\right|.
$$

## 向量空间与线性方程组

**定义 8** (线性组合与线性表出)

$K^{n}$ 中, 给定向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$, 任给 $K$ 中一组数 $k_{1},k_{2},\cdots,k_{s}$, 称 $k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s}$ 为向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 的一个线性组合. 如果 $\beta=k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{s}\alpha_{s}$, 则称 $\beta$ 可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 线性表出.

**命题 2** (线性表出与方程组有解的关系)

数域 $K$ 上 $n$ 元线性方程组 $x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta$ 有解 $\Leftrightarrow$ $\beta$ 可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 线性表出 $\Leftrightarrow$ $\beta\in\left\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\right\rangle$.

**定义 9** (线性相关)

$K^{n}$ 中向量组 $\alpha_{1},\cdots,\alpha_{s}$ 称为是线性相关的, 如果有 $K$ 中不全为零的数 $k_{1},\cdots,k_{s}$ 使得 $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$.

**定义 10** (线性无关)

$K^{n}$ 中向量组 $\alpha_{1},\cdots,\alpha_{s}$ 如果不是线性相关的, 则称为线性无关的. 即如果从 $k_{1}\alpha_{1}+\cdots+k_{s}\alpha_{s}=0$ 可以推出所有 $k_{1}=\cdots=k_{s}=0$, 则称这个向量组线性无关.

**命题 3** (线性表出与线性相关的关系)

设向量组 $\alpha_{1},\cdots,\alpha_{s}$ 线性无关, 则向量 $\beta$ 可以由 $\alpha_{1},\cdots,\alpha_{s}$ 线性表出当且仅当 $\alpha_{1},\cdots,\alpha_{s},\beta$ 线性相关.

**定义 11** (极大线性无关组)

$K^{n}$ 中向量组的一个部分组称为一个极大线性无关组, 如果这个部分组本身是线性无关的, 但是从这个向量组的其余向量中任取一个添进去, 得到的新的部分组都线性相关.

**定义 12** (向量组的秩)

向量组的极大线性无关组所含向量的数目称为这个向量组的秩. 记作

$$
\text{rank}\left\{\alpha_{1},\alpha_{2},\cdots,\alpha_{s}\right\}.
$$

**命题 4** (秩的比较)

如果向量组(I)可以由向量组(II)线性表出, 则(I)的秩 $\le$(II)的秩.

**定义 13** (基)

设 $U$ 是 $K^{n}$ 的一个子空间, $U$ 中的向量组 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 如果满足: $1^{\circ}$ $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 线性无关; $2^{\circ}$ $U$ 中每一个向量都可以由 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 线性表出, 则称 $\alpha_{1},\alpha_{2},\cdots,\alpha_{s}$ 是 $U$ 的一个基.

**定义 14** (矩阵的秩)

矩阵 $A$ 的行秩与列秩统称为 $A$ 的秩, 记作 $\text{rank}\left(A\right)$.

**定理 5** (行秩等于列秩)

任一矩阵的行秩等于它的列秩.

**推论 2** (用初等行变换求秩)

设矩阵 $A$ 经过初等行变换化成阶梯形矩阵 $J$, 则 $A$ 的秩等于 $J$ 的非零行的数目. 设 $J$ 的主元所在的列是第 $j_{1},\cdots,j_{r}$ 列, 则 $A$ 的第 $j_{1},\cdots,j_{r}$ 列构成 $A$ 的列向量组的一个极大线性无关组.

**定理 6** (线性方程组有解判别定理)

线性方程组

$$
x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n}=\beta
$$

有解的充分必要条件是: 它的系数矩阵与增广矩阵有相同的秩.

**定理 7** (解的个数判别)

设线性方程组有解, 如果系数矩阵的秩等于未知量数目 $n$, 则方程组有唯一解; 如果系数矩阵的秩小于 $n$, 则方程组有无穷多个解.

**定义 15** (基础解系)

齐次线性方程组有非零解时, 如果它的有限多个解 $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 满足: $1^{\circ}$ 线性无关; $2^{\circ}$ 方程组的每一个解都可以由 $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 线性表出, 则称 $\eta_{1},\eta_{2},\cdots,\eta_{t}$ 是齐次线性方程组的一个基础解系.

**定理 8** (解空间的维数)

数域 $K$ 上 $n$ 元齐次线性方程组的解空间 $W$ 的维数为:

$$
\dim W=n-\text{rank}\left(A\right),
$$

其中 $A$ 是系数矩阵.

**定理 9** (非齐次方程组的解集结构)

如果数域 $K$ 上 $n$ 元非齐次线性方程组有解, 则它的解集 $U=\gamma_{0}+W$, 其中 $\gamma_{0}$ 是一个特解, $W$ 是导出组的解空间.

## 矩阵的运算

**定义 16** (矩阵的加法)

设 $A=\left(a_{ij}\right),B=\left(b_{ij}\right)$ 都是数域 $K$ 上 $s\times n$ 矩阵, 令 $C=\left(a_{ij}+b_{ij}\right)_{s\times n}$, 则称 $C$ 是 $A$ 与 $B$ 的和, 记作 $C=A+B$.

**定义 17** (矩阵的数量乘法)

设 $k\in K$, 令 $M=\left(ka_{ij}\right)_{s\times n}$, 则称 $M$ 是 $k$ 与矩阵 $A$ 的数量乘积, 记作 $M=kA$.

**定义 18** (矩阵的乘法)

设 $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$, 令 $C=\left(c_{ij}\right)_{s\times m}$, 其中

$$
c_{ij}=a_{i1}b_{1j}+a_{i2}b_{2j}+\cdots+a_{in}b_{nj},
$$

则称 $C$ 是 $A$ 与 $B$ 的乘积, 记作 $C=AB$.

**定义 19** (上/下三角矩阵)

主对角线下(上)方元素全为零的方阵称为上(下)三角矩阵.

**定理 10** (矩阵乘积的秩)

设 $A=\left(a_{ij}\right)_{s\times n}$, $B=\left(b_{ij}\right)_{n\times m}$, 则:

$$
\text{rank}\left(AB\right)\le\min\left\{\text{rank}\left(A\right),\text{rank}\left(B\right)\right\}.
$$

**定理 11** (乘积的行列式)

设 $A,B$ 都是 $n$ 级矩阵, 则 $\left|AB\right|=\left|A\right|\left|B\right|$.


**定义 20** (可逆矩阵)

对于数域 $K$ 上的矩阵 $A$, 如果存在数域 $K$ 上的矩阵 $B$, 使得 $AB=BA=I$, 则称 $A$ 是可逆矩阵(或非奇异矩阵).

**定义 21** (逆矩阵)

如果 $A$ 是可逆矩阵, 则适合 $AB=BA=I$ 的矩阵 $B$ 称为 $A$ 的逆矩阵, 记作 $A^{-1}$.

**定理 12** (可逆的充要条件)

数域 $K$ 上 $n$ 级矩阵 $A$ 可逆的充分必要条件为 $\left|A\right|\ne0$. 当 $A$ 可逆时:

$$
A^{-1}=\frac{1}{\left|A\right|}A^{*}.
$$

**命题 5** (实数域上秩的等式)

设 $A$ 是实数域上 $s\times n$ 矩阵, 则:

$$
\text{rank}\left(A^{T}A\right)=\text{rank}\left(AA^{T}\right)=\text{rank}\left(A\right).
$$

**定义 22** (正交矩阵)

实数域上的方阵 $A$ 如果满足 $A^{T}A=I$, 则称 $A$ 是正交矩阵.

**定义 23** (内积)

在 $\mathbb{R}^{n}$ 中, 任给 $\alpha=\left(a_{1},a_{2},\cdots,a_{n}\right)$, $\beta=\left(b_{1},b_{2},\cdots,b_{n}\right)$, 规定

$$
\left(\alpha,\beta\right)=a_{1}b_{1}+a_{2}b_{2}+\cdots+a_{n}b_{n},
$$

称为 $\mathbb{R}^{n}$ 的标准内积.

**命题 6** (正交向量组线性无关)

欧几里得空间 $\mathbb{R}^{n}$ 中, 正交向量组一定是线性无关的.

**定义 24** (映射)

设 $S$ 和 $S'$ 是两个集合, 如果存在一个法则 $f$, 使得集合 $S$ 中每一个元素 $a$, 都有集合 $S'$ 中唯一确定的元素 $b$ 与它对应, 则称 $f$ 是 $S$ 到 $S'$ 的一个映射.

**定义 25** (线性映射)

$K^{n}$ 到 $K^{s}$ 的一个映射 $\mathcal{A}$ 如果保持加法和数量乘法, 即 $\forall\alpha,\beta\in K^{n},\ k\in K$, 有 $\mathcal{A}\left(\alpha+\beta\right)=\mathcal{A}\left(\alpha\right)+\mathcal{A}\left(\beta\right)$, $\mathcal{A}\left(k\alpha\right)=k\mathcal{A}\left(\alpha\right)$, 则称 $\mathcal{A}$ 是 $K^{n}$ 到 $K^{s}$ 的一个线性映射.

**定理** (核与象的维数公式)

$$
\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=\dim\left(K^{n}\right).
$$

## 相似标准形

**定义 26** (二元关系)

设 $S$ 是一个非空集合, 我们把 $S\times S$ 的一个子集 $W$ 叫做 $S$ 上的一个二元关系. 如果 $\left(a,b\right)\in W$, 则称 $a$ 与 $b$ 有 $W$ 关系.

**定义 27** (等价关系)

集合 $S$ 上的一个二元关系 $\sim$ 如果具有下述性质: $\forall a,b,c\in S$, 有 $1^{\circ}\ a\sim a$(反身性); $2^{\circ}\ a\sim b\Rightarrow b\sim a$(对称性); $3^{\circ}\ a\sim b$ 且 $b\sim c\Rightarrow a\sim c$(传递性), 则称 $\sim$ 是 $S$ 上的一个等价关系.

**定义 28** (商集)

设 $\sim$ 是集合 $S$ 上的一个等价关系. 由所有等价类组成的集合称为 $S$ 对于关系 $\sim$ 的商集, 记作 $S/\sim$.

**定义 29** (相抵)

数域 $K$ 上的矩阵 $A$ 如果经过一系列初等行变换和初等列变换变成矩阵 $B$, 则称 $A$ 与 $B$ 是相抵的, 记作 $A\overset{\text{相抵}}{\sim}B$.

**定理 13** (相抵标准形)

设数域 $K$ 上 $s\times n$ 矩阵 $A$ 的秩为 $r$. 如果 $r>0$, 则 $A$ 相抵于下述形式的矩阵:

$$
\left[\begin{array}{cc}I_{r} & 0\\0 & 0\end{array}\right].
$$

**定理 14** (相抵的充要条件)

数域 $K$ 上两个 $s\times n$ 矩阵 $A$ 与 $B$ 相抵当且仅当它们的秩相等.

**定义 30** (广义逆)

设 $A$ 是数域 $K$ 上 $s\times n$ 矩阵. 如果矩阵 $G$ 满足 $AGA=A$, 则称 $G$ 是 $A$ 的一个广义逆, 记作 $A^{-}$.

**定理 15** (广义逆的存在性)

设 $A$ 是数域 $K$ 上 $s\times n$ 非零矩阵, 则矩阵方程 $AXA=A$ 一定有解.

**定义 31** (相似)

设 $A$ 与 $B$ 都是数域 $K$ 上 $n$ 级矩阵, 如果存在数域 $K$ 上的一个 $n$ 级可逆矩阵 $P$, 使得 $P^{-1}AP=B$, 则称 $A$ 与 $B$ 是相似的, 记作 $A\sim B$.

**性质** (相似的不变量)

相似的矩阵有相等的行列式, 相等的秩, 相等的迹.

**定理 16** (可对角化的充要条件)

数域 $K$ 上的 $n$ 级矩阵 $A$ 能够相似于对角矩阵的充分必要条件是: $K^{n}$ 中有 $n$ 个线性无关的列向量 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 以及 $K$ 中有 $n$ 个数 $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$, 使得 $A\alpha_{i}=\lambda_{i}\alpha_{i}$($i=1,2,\cdots,n$).

**定义 32** (特征值与特征向量)

设 $A$ 是数域 $K$ 上的 $n$ 级矩阵, 如果 $K^{n}$ 中有非零列向量 $\alpha$, 使得 $A\alpha=\lambda_{0}\alpha$, 且 $\lambda_{0}\in K$, 则称 $\lambda_{0}$ 是 $A$ 的一个特征值, 称 $\alpha$ 是 $A$ 的属于特征值 $\lambda_{0}$ 的一个特征向量.

**性质** (相似不变量)

相似的矩阵有相同的行列式, 相同的秩, 相同的迹, 相同的特征多项式, 相同的特征值.

**定理 17** (可对角化的充要条件)

数域 $K$ 上 $n$ 级矩阵 $A$ 可对角化的充分必要条件是 $A$ 有 $n$ 个线性无关的特征向量.

**推论 3** (有 $n$ 个不同特征值则可对角化)

如果数域 $K$ 上 $n$ 级矩阵 $A$ 有 $n$ 个不同的特征值, 则 $A$ 可对角化.

**定理 18** (实对称矩阵的特征值)

实对称矩阵的特征多项式在复数域中的每一个根都是实数.

**定理 19** (实对称矩阵可正交对角化)

对于任意 $n$ 级实对称矩阵 $A$, 一定存在一个 $n$ 级正交矩阵 $T$, 使得 $T^{-1}AT$ 为对角矩阵.

## 二次型

**定义 33** (二次型)

系数在数域 $K$ 中的 $n$ 个变量 $x_{1},x_{2},\cdots,x_{n}$ 的一个二次齐次多项式, 称为数域 $K$ 上的一个 $n$ 元二次型.

**定理 20** (二次型的标准形)

数域 $K$ 上任意一个二次型都等价于一个只含平方项的二次型.

**定义 34** (规范形)

实二次型 $X^{T}AX$ 的规范形为 $z_{1}^{2}+\cdots+z_{p}^{2}-z_{p+1}^{2}-\cdots-z_{r}^{2}$, 其中 $p$ 是正惯性指数, $r$ 是二次型的秩.

**定理 21** (惯性定理)

$n$ 元实二次型 $X^{T}AX$ 的规范形是唯一的.

**定义 35** (正惯性指数)

在实二次型 $X^{T}AX$ 的规范形中, 系数为 $+1$ 的平方项的数目 $p$ 称为 $X^{T}AX$ 的正惯性指数, 系数为 $-1$ 的平方项的数目 $r-p$ 称为 $X^{T}AX$ 的负惯性指数.

**推论 4** (合同的充要条件)

两个 $n$ 级实对称矩阵合同当且仅当它们的秩相等, 并且正惯性指数也相等.

## 一元多项式

**定义 36** (整除)

设 $f\left(x\right),g\left(x\right)\in K\left[x\right]$, 如果存在 $h\left(x\right)\in K\left[x\right]$, 使得 $f\left(x\right)=h\left(x\right)g\left(x\right)$, 则称 $g\left(x\right)$ 整除 $f\left(x\right)$, 记作 $g\left(x\right)\mid f\left(x\right)$.

**定理 22** (带余除法)

在 $K\left[x\right]$ 中, 对于任意两个多项式 $f\left(x\right),g\left(x\right)$, 其中 $g\left(x\right)\ne0$, 存在唯一的一对多项式 $h\left(x\right),r\left(x\right)$, 使得 $f\left(x\right)=h\left(x\right)g\left(x\right)+r\left(x\right)$, $\deg r\left(x\right)<\deg g\left(x\right)$.

**定义 37** (最大公因式)

设 $f\left(x\right),g\left(x\right)\in K\left[x\right]$, $d\left(x\right)$ 是 $f\left(x\right)$ 与 $g\left(x\right)$ 的一个公因式. 如果 $f\left(x\right)$ 与 $g\left(x\right)$ 的任一公因式都能整除 $d\left(x\right)$, 则称 $d\left(x\right)$ 是 $f\left(x\right)$ 与 $g\left(x\right)$ 的一个最大公因式.

**定理 23** (最大公因式的存在性与倍式和)

对于 $K\left[x\right]$ 中任意两个多项式 $f\left(x\right)$ 与 $g\left(x\right)$, 存在它们的一个最大公因式 $d\left(x\right)$, 并且 $d\left(x\right)$ 可以表示成 $f\left(x\right)$ 与 $g\left(x\right)$ 的倍式和, 即有 $u\left(x\right),v\left(x\right)\in K\left[x\right]$, 使得 $d\left(x\right)=u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right)$.

**定义 38** (互素)

在 $K\left[x\right]$ 中, 如果 $f\left(x\right)$ 与 $g\left(x\right)$ 的最大公因式是零次多项式, 则称 $f\left(x\right)$ 与 $g\left(x\right)$ 互素.

**定义 39** (不可约多项式)

$K\left[x\right]$ 中一个次数大于零的多项式 $p\left(x\right)$, 如果它在 $K\left[x\right]$ 中的因式只有零次多项式和 $p\left(x\right)$ 的相伴元, 则称 $p\left(x\right)$ 是数域 $K$ 上的一个不可约多项式.

**性质 2** (不可约多项式的性质)

在 $K\left[x\right]$ 中, 如果 $p\left(x\right)$ 不可约, 且 $p\left(x\right)\mid f\left(x\right)g\left(x\right)$, 则 $p\left(x\right)\mid f\left(x\right)$ 或 $p\left(x\right)\mid g\left(x\right)$.

**定理 24** (唯一因式分解定理)

$K\left[x\right]$ 中每一个次数大于零的多项式都能唯一地分解成数域 $K$ 上有限多个不可约多项式的乘积.

**定义 40** (重因式)

在 $K\left[x\right]$ 中, 不可约多项式 $p\left(x\right)$ 称为多项式 $f\left(x\right)$ 的 $k$ 重因式, 如果 $p^{k}\left(x\right)\mid f\left(x\right)$, 而 $p^{k+1}\left(x\right)\nmid f\left(x\right)$.

**定理 25** (无重因式的判别)

设 $K$ 是数域, $K\left[x\right]$ 中次数大于零的多项式 $f\left(x\right)$ 没有重因式的充分必要条件是 $f\left(x\right)$ 与它的导数 $f'\left(x\right)$ 互素.

**定义 41** (多项式的根)

设 $K$ 是一个数域, 设 $R$ 是一个有单位元的交换环, 且 $R$ 可看成是 $K$ 的一个扩环. 对于 $K\left[x\right]$ 中一个多项式 $f\left(x\right)$, 如果 $R$ 中有一个元素 $c$ 使得 $f\left(c\right)=0$, 则称 $c$ 是 $f\left(x\right)$ 在 $R$ 中的一个根.

**定理 26** (余数定理)

在 $K\left[x\right]$ 中, 用 $x-a$ 去除 $f\left(x\right)$ 所得的余式是 $f\left(a\right)$.

**推论 5** (因式定理)

在 $K\left[x\right]$ 中, $x-a$ 整除 $f\left(x\right)$ 当且仅当 $f\left(a\right)=0$.

**定理 27** (实系数多项式唯一因式分解定理)

每个次数大于零的实系数多项式在实数域上都可以唯一地分解成一次因式与判别式小于零的二次因式的乘积.

**性质** (虚根共轭成对)

实系数多项式的虚根共轭成对出现, 且重数相同.

**定义 42** (本原多项式)

一个非零整系数多项式如果它的各项系数的最大公因数是 $1$, 则称它为本原多项式.

**引理 1** (高斯引理)

两个本原多项式的乘积还是本原多项式.

**定理 28** (艾森斯坦判别法)

设 $f\left(x\right)=a_{n}x^{n}+\ldots+a_{1}x+a_{0}$ 是一个次数 $n$ 大于零的整系数多项式, 如果存在一个素数 $p$, 使得 (1) $p\mid a_{i}$, $i=0,1,\ldots,n-1$; (2) $p\nmid a_{n}$; (3) $p^{2}\nmid a_{0}$. 则 $f\left(x\right)$ 在有理数域上是不可约的.

## $n$ 元多项式

**定义 43** ($n$ 元多项式)

设 $K$ 是一个数域, 用不属于 $K$ 的 $n$ 个符号 $x_{1},x_{2},\ldots,x_{n}$ 作表达式 $\sum_{i_{1},i_{2},\ldots,i_{n}}a_{i_{1}i_{2}\ldots i_{n}}x_{1}^{i_{1}}x_{2}^{i_{2}}\cdots x_{n}^{i_{n}}$, 其中 $a_{i_{1}i_{2}\ldots i_{n}}\in K$, $i_{1},i_{2},\ldots,i_{n}$ 是非负整数. 只有有限多个单项式的系数不为 $0$. 这种表达式称为数域 $K$ 上的 $n$ 元多项式.

**定理 29** (首项定理)

在 $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ 中两个非零多项式的乘积的首项等于它们的首项的乘积. 从而两个非零多项式的乘积仍是非零多项式, 即 $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ 是无零因子环.

**定义 44** (对称多项式)

设 $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ 是数域 $K$ 上的一个 $n$ 元多项式, 如果对于任意一个 $n$ 元排列 $j_{1}j_{2}\ldots j_{n}$, 都有

$$
f\left(x_{j_{1}},x_{j_{2}},\ldots,x_{j_{n}}\right)=f\left(x_{1},x_{2},\ldots,x_{n}\right),
$$

那么称 $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ 是数域 $K$ 上的一个 $n$ 元对称多项式.

**初等对称多项式**

$$
\begin{aligned}
\sigma_{1}&=x_{1}+x_{2}+\ldots+x_{n}\\
\sigma_{2}&=x_{1}x_{2}+x_{1}x_{3}+\ldots+x_{n-1}x_{n}\\
\ldots&\\
\sigma_{n}&=x_{1}x_{2}\ldots x_{n}.
\end{aligned}
$$

**牛顿公式** (幂和与初等对称多项式的关系)

设 $S_{k}=x_{1}^{k}+x_{2}^{k}+\ldots+x_{n}^{k}$, 则:

$$
\begin{aligned}
S_{1}&=\sigma_{1}\\
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\ldots+\left(-1\right)^{k-1}\sigma_{k-1}S_{1}+\left(-1\right)^{k}k\sigma_{k}&=0,\quad 1\le k\le n\\
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\ldots+\left(-1\right)^{n}\sigma_{n}S_{k-n}&=0,\quad k>n.
\end{aligned}
$$
