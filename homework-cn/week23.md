# week23

> **定义 7.6.1 (多项式的根)**
> 
> 设 $K$ 是一个数域, 设 $R$ 是一个有单位元的交换环, 且 $R$ 可看成是 $K$ 的一个扩环. 对于 $K\left[x\right]$ 中一个多项式 $f\left(x\right)$, 如果 $R$ 中有一个元素 $c$ 使得 $f\left(c\right)=0$, 则称 $c$ 是 $f\left(x\right)$ 在 $R$ 中的一个根.

> **定理 7.6.1 (余数定理)**
> 
> 在 $K\left[x\right]$ 中, 用 $x-a$ 去除 $f\left(x\right)$ 所得的余式是 $f\left(a\right)$.

> **推论 7.6.2 (因式定理)**
> 
> 在 $K\left[x\right]$ 中, $x-a$ 整除 $f\left(x\right)$ 当且仅当 $f\left(a\right)=0$.

> **定理 7.7.1 (实系数多项式唯一因式分解定理)**
> 
> 每个次数大于零的实系数多项式在实数域上都可以唯一地分解成一次因式与判别式小于零的二次因式的乘积.

> **性质 7.7.1 (虚根共轭成对)**
> 
> 实系数多项式的虚根共轭成对出现, 且重数相同.

> **定义 7.8.1 (本原多项式)**
> 
> 一个非零整系数多项式如果它的各项系数的最大公因数是 $1$, 则称它为本原多项式.

> **引理 7.8.1 (高斯引理)**
> 
> 两个本原多项式的乘积还是本原多项式.

> **定理 7.8.1 (艾森斯坦判别法)**
> 
> 设

$$
f\left(x\right)=a_{n}x^{n}+\cdots+a_{1}x+a_{0}
$$
是一个次数 $n$ 大于零的整系数多项式, 如果存在一个素数 $p$, 使得 (1) $p\mid{a}_{i}$, $i=0,1,\ldots,n-1$; (2) $p\nmid{a}_{n}$; (3) $p^{2}\nmid{a}_{0}$, 则 $f\left(x\right)$ 在有理数域上是不可约的.

## 7.6-1

设

$$
f\left(x\right)=x^{5}+7x^{4}+19x^{3}+26x^{2}+20x+8\in\mathbb{Q}\left[x\right],
$$

判断 $-2$ 是不是多项式 $f\left(x\right)$ 的根, 如果是的话, 它是几重根?

### 解答 7.6-1

由**推论 7.6.2 (因式定理)**, 在 $K\left[x\right]$ 中, $x-a$ 整除 $f\left(x\right)$ 当且仅当 $f\left(a\right)=0$. 计算 $f\left(-2\right)$:

$$
f\left(-2\right)
=\left(-2\right)^{5}+7\left(-2\right)^{4}+19\left(-2\right)^{3}+26\left(-2\right)^{2}+20\left(-2\right)+8=-32+112-152+104-40+8=0.
$$

所以 $-2$ 是 $f\left(x\right)$ 的根.

用综合除法看 $x+2$ 能除几次.

第一次:

$$
\begin{array}{r|rrrrrr}
-2&1&7&19&26&20&8\\
&&-2&-10&-18&-16&-8\\
\hline
&1&5&9&8&4&0
\end{array}
$$

余式为 $0$, 商式是 $x^{4}+5x^{3}+9x^{2}+8x+4$.

第二次:

$$
\begin{array}{r|rrrrr}
-2&1&5&9&8&4\\
&&-2&-6&-6&-4\\
\hline
&1&3&3&2&0
\end{array}
$$

余式为 $0$, 商式是 $x^{3}+3x^{2}+3x+2$.

第三次:

$$
\begin{array}{r|rrrr}
-2&1&3&3&2\\
&&-2&-2&-2\\
\hline
&1&1&1&0
\end{array}
$$

余式为 $0$, 商式是 $x^{2}+x+1$.

第四次:

$$
\begin{array}{r|rrr}
-2&1&1&1\\
&&-2&2\\
\hline
&1&-1&3
\end{array}
$$

余式为 $3\ne0$.

因此 $-2$ 是 $f\left(x\right)$ 的 $3$ 重根.

$\blacksquare$

## 7.6-4

设

$$
f\left(x\right)=x^{4}-5x^{3}+ax^{2}+bx+9\in\mathbb{Q}\left[x\right],
$$

如果 $3$ 是 $f\left(x\right)$ 的二重根, 求 $a,b$.

### 解答 7.6-4

如果 $3$ 是 $f\left(x\right)$ 的二重根, 则 $f\left(3\right)=0$ 且 $f'\left(3\right)=0$.

计算 $f\left(3\right)$:

$$
f\left(3\right)
=3^{4}-5\cdot3^{3}+a\cdot3^{2}+b\cdot3+9=81-135+9a+3b+9=-45+9a+3b.
$$

令 $f\left(3\right)=0$:

$$
9a+3b=45\Rightarrow3a+b=15.\tag{1}
$$

求导数:

$$
f'\left(x\right)=4x^{3}-15x^{2}+2ax+b.
$$

计算 $f'\left(3\right)$:

$$
f'\left(3\right)
=4\cdot3^{3}-15\cdot3^{2}+2a\cdot3+b=108-135+6a+b=-27+6a+b.
$$

令 $f'\left(3\right)=0$:

$$
6a+b=27.\tag{2}
$$

$\left(2\right)-\left(1\right)$ 得:

$$
3a=12\Rightarrow{a}=4.
$$

代入 $\left(1\right)$:

$$
3\cdot4+b=15\Rightarrow{b}=3.
$$

因此 $a=4$, $b=3$.

$\blacksquare$

## 7.6-8

求复系数多项式 $x^{n}-1$ 的标准分解式.

### 解答 7.6-8

$x^{n}-1=0$ 的根是 $x^{n}=1$.

$1$ 的 $n$ 次方根为:

$$
x_{k}=e^{2\pi{i}k/n}=\cos\frac{2\pi{k}}{n}+i\sin\frac{2\pi{k}}{n},k=0,1,\ldots,n-1.
$$

因此标准分解式为:

$$
x^{n}-1=\prod_{k=0}^{n-1}\left(x-e^{2\pi{i}k/n}\right).
$$

$\blacksquare$

## 7.7-4

证明: 如果 $n$ 级实矩阵 $A$ 与 $B$ 不相似, 则把它们看成复矩阵后仍然不相似.

### 解答 7.7-4

由**性质 7.7.1 (虚根共轭成对)**, 实系数多项式的虚根共轭成对出现. 用反证法.

假设 $A$ 与 $B$ 作为复矩阵相似, 即存在可逆复矩阵 $P$ 使得

$$
B=P^{-1}AP.
$$

我们需要证明 $A$ 与 $B$ 作为实矩阵也相似.

设 $P=P_{1}+iP_{2}$, 其中 $P_{1},P_{2}$ 是实矩阵.

由 $B=P^{-1}AP$ 得

$$
BP=PA.
$$

代入 $P=P_{1}+iP_{2}$:

$$
B\left(P_{1}+iP_{2}\right)=\left(P_{1}+iP_{2}\right)A.
$$

比较实部和虚部:

$$
BP_{1}=P_{1}A,
$$

$$
BP_{2}=P_{2}A.
$$

因此对于任意实数 $t$, 都有

$$
B\left(P_{1}+tP_{2}\right)=\left(P_{1}+tP_{2}\right)A.
$$

考虑多项式 $\det\left(P_{1}+xP_{2}\right)$, 这是一个关于 $x$ 的实系数多项式.

因为 $P=P_{1}+iP_{2}$ 可逆, 所以 $\det\left(P\right)\ne0$, 即 $\det\left(P_{1}+iP_{2}\right)\ne0$.

因此 $\det\left(P_{1}+xP_{2}\right)$ 不是零多项式, 它只有有限多个实根.

所以存在实数 $t$, 使得

$$
\det\left(P_{1}+tP_{2}\right)\ne0.
$$

即 $P_{1}+tP_{2}$ 可逆.

令 $Q=P_{1}+tP_{2}$, 这是一个可逆实矩阵.

则

$$
BQ=QA,
$$

即

$$
B=Q^{-1}AQ.
$$

所以 $A$ 与 $B$ 作为实矩阵也相似.

这与已知条件矛盾.

因此如果 $A$ 与 $B$ 作为实矩阵不相似, 则作为复矩阵也不相似.

$\blacksquare$

## 7.8-2(4)

$x^{4}-2x^{3}+2x-3$ 在有理数域上是否不可约?

### 解答 7.8-2(4)

由**定理 7.8.1 (艾森斯坦判别法)**, 先看有没有有理根.

可能的有理根是 $\pm1$, $\pm3$.

$$
f\left(1\right)=1-2+2-3=-2\ne0.
$$

$$
f\left(-1\right)=1+2-2-3=-2\ne0.
$$

$$
f\left(3\right)=81-54+6-3=30\ne0.
$$

$$
f\left(-3\right)=81+54-6-3=126\ne0.
$$

所以没有有理根.

假设能分解成两个整系数二次多项式的乘积:

$$
x^{4}-2x^{3}+2x-3=\left(x^{2}+ax+b\right)\left(x^{2}+cx+d\right).
$$

比较系数:

$$
a+c=-2,\tag{1}
$$

$$
ac+b+d=0,\tag{2}
$$

$$
ad+bc=2,\tag{3}
$$

$$
bd=-3.\tag{4}
$$

由 $\left(4\right)$, $bd=-3$ 的整数解有:

$$
\left(b,d\right)=\left(1,-3\right),\left(-1,3\right),\left(3,-1\right),\left(-3,1\right).
$$

逐一验证:

- $b=1,d=-3$: 由 $\left(1\right)$, $c=-2-a$. 代入 $\left(2\right)$:

  $$
-2a-a^{2}+1-3=0\Rightarrow{a}^{2}+2a+2=0,
$$

  无实根.
- $b=-1,d=3$: 代入 $\left(2\right)$:

  $$
-2a-a^{2}-1+3=0\Rightarrow{a}^{2}+2a-2=0,
$$

  无整数根.
- $b=3,d=-1$: 代入 $\left(2\right)$:

  $$
-2a-a^{2}+3-1=0\Rightarrow{a}^{2}+2a-2=0,
$$

  无整数根.
- $b=-3,d=1$: 代入 $\left(2\right)$:

  $$
-2a-a^{2}-3+1=0\Rightarrow{a}^{2}+2a+2=0,
$$

  无实根.

因此不能分解成两个整系数二次多项式的乘积.

所以 $x^{4}-2x^{3}+2x-3$ 在有理数域上不可约.

$\blacksquare$

## 7.8-2(5)

$x^{4}+px^{2}+1$, $p$ 为奇素数, 在有理数域上是否不可约?

### 解答 7.8-2(5)

先看有没有有理根.

可能的有理根是 $\pm1$.

$$
f\left(1\right)=1+p+1=p+2\ne0.
$$

$$
f\left(-1\right)=1+p+1=p+2\ne0.
$$

所以没有有理根.

假设能分解成两个整系数二次多项式的乘积:

$$
x^{4}+px^{2}+1=\left(x^{2}+ax+b\right)\left(x^{2}+cx+d\right).
$$

比较系数:

$$
a+c=0,\tag{1}
$$

$$
ac+b+d=p,\tag{2}
$$

$$
ad+bc=0,\tag{3}
$$

$$
bd=1.\tag{4}
$$

由 $\left(1\right)$, $c=-a$.

代入 $\left(3\right)$:

$$
ad+b\left(-a\right)=a\left(d-b\right)=0.
$$

所以 $a=0$ 或 $d=b$.

情况1: $a=0$.

则 $c=0$.

由 $\left(2\right)$: $b+d=p$.

由 $\left(4\right)$: $bd=1$.

所以 $b=d=1$ 或 $b=d=-1$.

若 $b=d=1$, 则 $b+d=2$, 故 $p=2$. 但 $p$ 是奇素数, 矛盾.

若 $b=d=-1$, 则 $b+d=-2$, 故 $p=-2$. 但 $p$ 是正素数, 矛盾.

情况2: $d=b$.

由 $\left(4\right)$: $b^{2}=1$, 所以 $b=1$ 或 $b=-1$.

若 $b=1$, 则 $d=1$.

由 $\left(2\right)$:

$$
-a^{2}+2=p\Rightarrow{a}^{2}=2-p.
$$

因为 $p$ 是奇素数, $p\ge3$, 所以 $2-p\le-1<0$, 无实根.

若 $b=-1$, 则 $d=-1$.

由 $\left(2\right)$:

$$
-a^{2}-2=p\Rightarrow{a}^{2}=-p-2<0,
$$

无实根.

因此不能分解成两个整系数二次多项式的乘积.

所以 $x^{4}+px^{2}+1$ 在有理数域上不可约.

$\blacksquare$

## 7.8-2(7)

$2x^{3}-x^{2}+x+1$ 在有理数域上是否不可约?

### 解答 7.8-2(7)

三次多项式在有理数域上可约当且仅当它有有理根.

可能的有理根是 $\pm1$, $\pm\frac{1}{2}$.

$$
f\left(1\right)=2-1+1+1=3\ne0.
$$

$$
f\left(-1\right)=-2-1-1+1=-3\ne0.
$$

$$
f\left(\frac{1}{2}\right)=2\cdot\frac{1}{8}-\frac{1}{4}+\frac{1}{2}+1=\frac{1}{4}-\frac{1}{4}+\frac{1}{2}+1=\frac{3}{2}\ne0.
$$

$$
f\left(-\frac{1}{2}\right)=2\cdot\left(-\frac{1}{8}\right)-\frac{1}{4}+\left(-\frac{1}{2}\right)+1=-\frac{1}{4}-\frac{1}{4}-\frac{1}{2}+1=0.
$$

所以 $-\frac{1}{2}$ 是 $f\left(x\right)$ 的有理根.

因此 $f\left(x\right)$ 在有理数域上可约.

$\blacksquare$

## 7.8-2(8)

$x^{4}-5x^{2}+1$ 在有理数域上是否不可约?

### 解答 7.8-2(8)

先看有没有有理根.

可能的有理根是 $\pm1$.

$$
f\left(1\right)=1-5+1=-3\ne0.
$$

$$
f\left(-1\right)=1-5+1=-3\ne0.
$$

所以没有有理根.

假设能分解成两个整系数二次多项式的乘积:

$$
x^{4}-5x^{2}+1=\left(x^{2}+ax+b\right)\left(x^{2}+cx+d\right).
$$

比较系数:

$$
a+c=0,\tag{1}
$$

$$
ac+b+d=-5,\tag{2}
$$

$$
ad+bc=0,\tag{3}
$$

$$
bd=1.\tag{4}
$$

由 $\left(1\right)$, $c=-a$.

代入 $\left(3\right)$:

$$
ad+b\left(-a\right)=a\left(d-b\right)=0.
$$

所以 $a=0$ 或 $d=b$.

情况1: $a=0$.

则 $c=0$.

由 $\left(2\right)$: $b+d=-5$.

由 $\left(4\right)$: $bd=1$.

所以 $b,d$ 是方程 $t^{2}+5t+1=0$ 的根, 不是整数.

情况2: $d=b$.

由 $\left(4\right)$: $b^{2}=1$, 所以 $b=1$ 或 $b=-1$.

若 $b=1$, 则 $d=1$.

由 $\left(2\right)$: $-a^{2}+2=-5\Rightarrow{a}^{2}=7$, 不是完全平方数.

若 $b=-1$, 则 $d=-1$.

由 $\left(2\right)$: $-a^{2}-2=-5\Rightarrow{a}^{2}=3$, 不是完全平方数.

因此不能分解成两个整系数二次多项式的乘积.

所以 $x^{4}-5x^{2}+1$ 在有理数域上不可约.

$\blacksquare$
