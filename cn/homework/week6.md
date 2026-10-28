# week6

> **性质 2.3.2 (一行的公因子可以提出去)**<br>行列式一行的公因子可以提出去; 特别地, 若行列式中有一行为零(该行元素全为 $0$), 则行列式的值为 $0$.

> **性质 2.3.3 (某行为两组数之和则可拆分)**<br>行列式中若有某一行是两组数的和, 则此行列式等于两个行列式的和, 这两个行列式的这一行分别是第一组数和第二组数, 而其余各行与原来行列式的相应各行相同.

> **性质 2.3.5 (两行相同则行列式为零)**<br>行列式中有两行相同, 则行列式的值为 $0$; 进而若两行成比例, 行列式的值也为 $0$.

> **性质 2.3.7 (把一行的倍数加到另一行上值不变)**<br>把一行的倍数加到另一行上, 行列式的值不变.

> **定理 2.4.1 (行列式按一行(列)展开)**<br>$n$ 阶行列式 $|A|$ 等于它的第 $i$ 行元素与自己的代数余子式的乘积之和, 也等于它的第 $j$ 列元素与自己的代数余子式的乘积之和, 即 $|A|=\sum_{k=1}^{n}a_{ik}A_{ik}=\sum_{k=1}^{n}a_{kj}A_{kj}$, 其中 $A_{kj}=\left(-1\right)^{k+j}M_{kj}$ 为代数余子式.

---

## 2.3-1(2)

计算下列行列式:

$$
\left|\begin{array}{rrr}
-1 & 203 & 1/3\\
3 & 298 & 1/2\\
5 & 399 & 2/3
\end{array}\right|.
$$

### 解答 2.3-1(2)

观察到第 $2$ 列的元素 $203,298,399$ 可以拆成两个数之和, 即 $203=200+3$, $298=300-2$, $399=400-1$. 由**性质 2.3.3 (某行为两组数之和则可拆分)**, 行列式某一列的所有元素都是两项之和, 则行列式可拆成两个行列式之和:

$$
\left|\begin{array}{rrr}
-1 & 203 & 1/3\\
3 & 298 & 1/2\\
5 & 399 & 2/3
\end{array}\right|
=
\left|\begin{array}{rrr}
-1 & 200 & 1/3\\
3 & 300 & 1/2\\
5 & 400 & 2/3
\end{array}\right|
+
\left|\begin{array}{rrr}
-1 & 3 & 1/3\\
3 & -2 & 1/2\\
5 & -1 & 2/3
\end{array}\right|.
$$

由**性质 2.3.2 (一行的公因子可以提出去)**, 行列式某一列的公因子可以提到行列式符号外面. 第一个行列式的第 $2$ 列有公因子 $100$, 提出得:

$$
D_{1}=100\times\left|\begin{array}{rrr}
-1 & 2 & 1/3\\
3 & 3 & 1/2\\
5 & 4 & 2/3
\end{array}\right|.
$$

直接展开计算:

$$
\left|\begin{array}{rrr}
-1 & 2 & 1/3\\
3 & 3 & 1/2\\
5 & 4 & 2/3
\end{array}\right|=-1\times\left(3\times\frac{2}{3}-\frac{1}{2}\times4\right)-2\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times4-3\times5\right)=-1\times\left(2-2\right)-2\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(12-15\right)=0-2\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times\left(-3\right)=1-1=0.
$$

故 $D_{1}=100\times0=0$.

计算第二个行列式 $D_{2}$:

$$
D_{2}=\left|\begin{array}{rrr}
-1 & 3 & 1/3\\
3 & -2 & 1/2\\
5 & -1 & 2/3
\end{array}\right|=-1\times\left(-2\times\frac{2}{3}-\frac{1}{2}\times\left(-1\right)\right)-3\times\left(3\times\frac{2}{3}-\frac{1}{2}\times5\right)+\frac{1}{3}\times\left(3\times\left(-1\right)-\left(-2\right)\times5\right)=-1\times\left(-\frac{4}{3}+\frac{1}{2}\right)-3\times\left(2-\frac{5}{2}\right)+\frac{1}{3}\times\left(-3+10\right)=-1\times\left(-\frac{5}{6}\right)-3\times\left(-\frac{1}{2}\right)+\frac{1}{3}\times7=\frac{5}{6}+\frac{3}{2}+\frac{7}{3}=\frac{5}{6}+\frac{9}{6}+\frac{14}{6}=\frac{28}{6}=\frac{14}{3}.
$$

故原行列式

$$
D=D_{1}+D_{2}=0+\frac{14}{3}=\frac{14}{3}.
$$

$\blacksquare$

---

## 2.3-2(2)

计算下列 $n$ 阶行列式:

$$
\left|\begin{array}{cccc}
a_{1}-b & a_{2} & \cdots & a_{n}\\
a_{1} & a_{2}-b & \cdots & a_{n}\\
\vdots & \vdots & & \vdots\\
a_{1} & a_{2} & \cdots & a_{n}-b
\end{array}\right|.
$$

### 解答 2.3-2(2)

由**性质 2.3.7 (把一行的倍数加到另一行上值不变)**, 把某一行的倍数加到另一行上, 行列式的值不变. 将第 $n$ 行的 $-1$ 倍分别加到第 $1,2,\cdots,n-1$ 行上, 得

$$
\left|\begin{array}{rrrrr}
-b & 0 & \cdots & 0 & b\\
0 & -b & \cdots & 0 & b\\
\vdots & \vdots & & \vdots & \vdots\\
0 & 0 & \cdots & -b & b\\
a_{1} & a_{2} & \cdots & a_{n-1} & a_{n}-b
\end{array}\right|.
$$

由**定理 2.4.1 (行列式按一行(列)展开)**, 按最后一列展开. 最后一列的元素为 $\left(b,b,\cdots,b,a_{n}-b\right)$.

对于 $j< n$, 代数余子式 $A_{jn}=\left(-1\right)^{j+n}M_{jn}$, 其中 $M_{jn}$ 是去掉第 $j$ 行第 $n$ 列后的 $\left(n-1\right)$ 阶行列式. 该行列式中第 $j$ 行(原第 $j$ 行去掉第 $n$ 列后)只有第 $1$ 列为 $b_{j}$, 其余全为 $0$, 按此行展开后余子式为对角行列式, 可得 $M_{jn}=\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}$.

于是

$$
\text{行列式}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{j+n}\cdot\left(-1\right)^{j-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-1\right)^{2n}\left(-b\right)^{n-1}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{2j+n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\sum_{j=1}^{n-1}b\cdot\left(-1\right)^{n-1}a_{j}\left(-b\right)^{n-2}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\left(-1\right)^{n-1}b^{n-1}\sum_{j=1}^{n-1}a_{j}+\left(a_{n}-b\right)\left(-b\right)^{n-1}=\left(-b\right)^{n-1}\left(\sum_{j=1}^{n}a_{j}-b\right).
$$

$\blacksquare$

---

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

---

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

---

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
