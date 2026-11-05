# week3

> **定义 2.2.1 ($n$ 阶行列式)**
> 
> $n$ 阶行列式是 $n!$ 项的代数和, 其中每一项都是位于不同行, 不同列的 $n$ 个元素的乘积, 把这 $n$ 个元素按照行指标成自然序排好位置, 当列指标所成排列是偶排列时, 该项带正号; 奇排列时, 该项带负号. 即

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

## 2.2-1(4)

按定义计算下列行列式:

$$
\left|\begin{array}{ccccc}
0&\cdots&0&a_{1}&0\\
0&\cdots&a_{2}&0&0\\
\vdots&&\vdots&\vdots&\vdots\\
a_{n-1}&\cdots&0&0&0\\
0&\cdots&0&0&a_{n}
\end{array}\right|.
$$

### 解答 2.2-1(4)

由**定义 2.2.1 ($n$ 阶行列式)**, 行列式的每一项都是取自不同行, 不同列的 $n$ 个元素的乘积.

由**定义 2.2.1 ($n$ 阶行列式)**, 逐行确定唯一可取的非零元素: 第 $1$ 行只有第 $n-1$ 列的 $a_{1}$ 非零, 第 $2$ 行只有第 $n-2$ 列的 $a_{2}$ 非零, $\cdots$, 第 $n-1$ 行只有第 $1$ 列的 $a_{n-1}$ 非零, 第 $n$ 行只有第 $n$ 列的 $a_{n}$ 非零. 因此唯一非零项为 $a_{1}a_{2}\cdots{a}_{n}$.

由**定义 2.2.1 ($n$ 阶行列式)**, 该非零项的列指标排列为 $n-1,n-2,\cdots,1,n$, 其逆序数为

$$
\tau=\left(n-2\right)+\left(n-3\right)+\cdots+1+0=\frac{\left(n-1\right)\left(n-2\right)}{2}.
$$

由**定义 2.2.1 ($n$ 阶行列式)** 中正负号的规定, 故行列式值为

$$
\left(-1\right)^{\frac{\left(n-1\right)\left(n-2\right)}{2}}a_{1}a_{2}\cdots{a}_{n}.
$$

$\blacksquare$

## 2.2-1(5)

按定义计算下列行列式:

$$
\left|\begin{array}{ccccc}
0&0&0&1&0\\
0&0&2&0&0\\
0&3&8&0&0\\
4&9&0&7&0\\
6&0&0&0&5
\end{array}\right|.
$$

### 解答 2.2-1(5)

由**定义 2.2.1 ($n$ 阶行列式)**, 行列式的每一项都是取自不同行, 不同列的 $n$ 个元素的乘积.

由**定义 2.2.1 ($n$ 阶行列式)**, 逐行确定唯一可取的非零元素:

- 第 $1$ 行: 只有第 $4$ 列的 $1$ 非零, 故取 $\left(1,4\right)=1$;
- 第 $2$ 行: 只有第 $3$ 列的 $2$ 非零, 故取 $\left(2,3\right)=2$;
- 第 $3$ 行: 第 $3$ 列已被占用, 只能取 $\left(3,2\right)=3$;
- 第 $4$ 行: 第 $2$ 列, 第 $4$ 列已被占用, 只能取 $\left(4,1\right)=4$;
- 第 $5$ 行: 第 $1$ 列已被占用, 只能取 $\left(5,5\right)=5$.

因此唯一非零项为 $1\times2\times3\times4\times5=120$.

由**定义 2.2.1 ($n$ 阶行列式)**, 该非零项的列指标排列为 $4,3,2,1,5$, 其逆序数为

$$
\tau\left(4,3,2,1,5\right)=3+2+1+0+0=6.
$$

由**定义 2.2.1 ($n$ 阶行列式)** 中正负号的规定, 偶排列带正号, 故行列式值为

$$
\left(-1\right)^{6}\times120=120.
$$

$\blacksquare$

## 2.2-3

用行列式定义计算:

$$
\left|\begin{array}{ccccc}
a_{1}&a_{2}&a_{3}&a_{4}&a_{5}\\
b_{1}&b_{2}&b_{3}&b_{4}&b_{5}\\
c_{1}&c_{2}&0&0&0\\
d_{1}&d_{2}&0&0&0\\
e_{1}&e_{2}&0&0&0
\end{array}\right|.
$$

### 解答 2.2-3

由**定义 2.2.1 ($n$ 阶行列式)**, 行列式的每一项都是取自不同行, 不同列的 $n$ 个元素的乘积.

由**定义 2.2.1 ($n$ 阶行列式)**, 第 $3,4,5$ 行只有第 $1,2$ 列的元素非零. 按**定义 2.2.1 ($n$ 阶行列式)**, 这三行的元素必须取自不同列, 但只有 $2$ 列可供选择, 要取 $3$ 个不同列的元素, 由抽屉原理, 必有两行取到同一列, 与**定义 2.2.1 ($n$ 阶行列式)** 中"不同列"的要求矛盾.

因此不存在满足条件的非零项, 行列式值为 $0$.

$\blacksquare$

## 2.2-5

写出下述行列式中 $x^{4}$ 的项与 $x^{3}$ 的项:

$$
\left|\begin{array}{rrrr}
5x&x&1&x\\
1&x&1&-1\\
3&2&x&1\\
3&1&1&x
\end{array}\right|.
$$

### 解答 2.2-5

由**定义 2.2.1 ($n$ 阶行列式)**, 行列式的每一项都是取自不同行, 不同列的 $n$ 个元素的乘积, 项的符号由列指标排列的逆序数决定.

$x^{4}$ 的项. 要得到 $x^{4}$, 需要 $4$ 个元素都含 $x$. 含 $x$ 的位置为

$$
\left(1,1\right)=5x,\left(1,2\right)=x,\left(1,4\right)=x,\left(2,2\right)=x,\left(3,3\right)=x,\left(4,4\right)=x.
$$

第 $2,3,4$ 行各只有一个含 $x$ 的位置, 即 $\left(2,2\right),\left(3,3\right),\left(4,4\right)$, 按**定义 2.2.1 ($n$ 阶行列式)** 必须全取. 此时已用列 $2,3,4$, 第 $1$ 行只能取 $\left(1,1\right)=5x$. 列指标排列为 $1,2,3,4$, 逆序数 $\tau=0$, 偶排列带正号.

故 $x^{4}$ 的项为 $5x^{4}$.

$x^{3}$ 的项. 要得到 $x^{3}$, 需要 $3$ 个含 $x$ 的元素和 $1$ 个不含 $x$ 的元素. 枚举所有满足条件的组合:

(1) 取

$$
\left(1,2\right)=x,\left(3,3\right)=x,\left(4,4\right)=x,
$$

第 $2$ 行取不含 $x$ 的 $\left(2,1\right)=1$. 列指标为 $2,1,3,4$, 逆序数 $\tau=1$, 奇排列带负号, 项为 $-x^{3}$.

(2) 取

$$
\left(1,4\right)=x,\left(2,2\right)=x,\left(3,3\right)=x,
$$

第 $4$ 行取不含 $x$ 的 $\left(4,1\right)=3$. 列指标为 $4,2,3,1$, 逆序数 $\tau=5$, 奇排列带负号, 项为 $-3x^{3}$.

其余组合均因列冲突而无效, 不满足**定义 2.2.1 ($n$ 阶行列式)** 中"不同列"的要求.

故 $x^{3}$ 的项为 $-x^{3}-3x^{3}=-4x^{3}$.

$\blacksquare$

## 2.3-1(2)

计算下列行列式:

$$
\left|\begin{array}{rrr}
-1&203&1/3\\
3&298&1/2\\
5&399&2/3
\end{array}\right|.
$$

### 解答 2.3-1(2)

观察到第 $2$ 列的元素 $203,298,399$ 可以拆成两个数之和, 即 $203=200+3$, $298=300-2$, $399=400-1$. 由**性质 2.3.3 (某行为两组数之和则可拆分)**, 行列式某一列的所有元素都是两项之和, 则行列式可拆成两个行列式之和:

$$
\left|\begin{array}{rrr}
-1&203&1/3\\
3&298&1/2\\
5&399&2/3
\end{array}\right|
=
\left|\begin{array}{rrr}
-1&200&1/3\\
3&300&1/2\\
5&400&2/3
\end{array}\right|
+
\left|\begin{array}{rrr}
-1&3&1/3\\
3&-2&1/2\\
5&-1&2/3
\end{array}\right|.
$$

由**性质 2.3.2 (一行的公因子可以提出去)**, 行列式某一列的公因子可以提到行列式符号外面. 第一个行列式的第 $2$ 列有公因子 $100$, 提出得:

$$
D_{1}=100\times\left|\begin{array}{rrr}
-1&2&1/3\\
3&3&1/2\\
5&4&2/3
\end{array}\right|.
$$

直接展开计算:

$$
\left|\begin{array}{rrr}
-1&2&1/3\\
3&3&1/2\\
5&4&2/3
\end{array}\right|=-1\times\left(3\times\frac{2}{3}-\frac{1}{2}\times4\right)-2\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times4-3\times5\right)=-1\times\left(2-2\right)-2\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(12-15\right)=0-2\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times\left(-3\right)=1-1=0.
$$

故 $D_{1}=100\times0=0$.

计算第二个行列式 $D_{2}$:

$$
D_{2}=\left|\begin{array}{rrr}
-1&3&1/3\\
3&-2&1/2\\
5&-1&2/3
\end{array}\right|=-1\times\left(-2\times\frac{2}{3}-\frac{1}{2}\times\left(-1\right)\right)-3\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times\left(-1\right)-\left(-2\right)\times5\right)=-1\times\left(-\frac{4}{3}+\frac{1}{2}\right)-3\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(-3+10\right)=-1\times\left(-\frac{5}{6}\right)-3\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times7=\frac{5}{6}+\frac{3}{2}+\frac{7}{3}=\frac{5}{6}+\frac{9}{6}+\frac{14}{6}=\frac{28}{6}=\frac{14}{3}.
$$

故原行列式

$$
D=D_{1}+D_{2}=0+\frac{14}{3}=\frac{14}{3}.
$$

$\blacksquare$

## 2.3-2(2)

计算下列 $n$ 阶行列式:

$$
\left|\begin{array}{cccc}
a_{1}-b&a_{2}&\cdots&a_{n}\\
a_{1}&a_{2}-b&\cdots&a_{n}\\
\vdots&\vdots&&\vdots\\
a_{1}&a_{2}&\cdots&a_{n}-b
\end{array}\right|.
$$

### 解答 2.3-2(2)

由**性质 2.3.7 (把一行的倍数加到另一行上值不变)**, 把某一行的倍数加到另一行上, 行列式的值不变. 将第 $n$ 行的 $-1$ 倍分别加到第 $1,2,\cdots,n-1$ 行上, 得

$$
\left|\begin{array}{rrrrr}
-b&0&\cdots&0&b\\
0&-b&\cdots&0&b\\
\vdots&\vdots&&\vdots&\vdots\\
0&0&\cdots&-b&b\\
a_{1}&a_{2}&\cdots&a_{n-1}&a_{n}-b
\end{array}\right|.
$$

由**定理 2.4.1 (行列式按一行(列)展开)**, 按最后一列展开. 最后一列的元素为 $\left(b,b,\cdots,b,a_{n}-b\right)$.

对于 $j<{}n$, 代数余子式 $A_{jn}=\left(-1\right)^{j+n}M_{jn}$, 其中 $M_{jn}$ 是去掉第 $j$ 行第 $n$ 列后的 $\left(n-1\right)$ 阶行列式. 该行列式中第 $j$ 行(原第 $j$ 行去掉第 $n$ 列后)只有第 $1$ 列为 $b_{j}$, 其余全为 $0$, 按此行展开后余子式为对角行列式, 可得 $M_{jn}=\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}$.

于是

$$
\text{行列式}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{j+n}\cdot\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-1\right)^{2n}\left(-b\right)^{n-1}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{2j+n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\left(-1\right)^{n-1}b^{n-1}\sum_{j=1}^{n-1}a_{j}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\left(-b\right)^{n-1}\left(\sum_{j=1}^{n}a_{j}-b\right).
$$

$\blacksquare$
