# week24

> **定义 7.8.1 (本原多项式)**
> 
> 一个非零整系数多项式如果它的各项系数的最大公因数是 $1$, 则称它为本原多项式.

> **引理 7.8.1 (高斯引理)**
> 
> 两个本原多项式的乘积还是本原多项式.

> **定理 7.8.1 (艾森斯坦判别法)**
> 
> 设

> **定义 7.9.1 ($n$ 元多项式)**
> 
> 设 $K$ 是一个数域, 用不属于 $K$ 的 $n$ 个符号 $x_{1},x_{2},\ldots,x_{n}$ 作表达式

$$
\sum_{i_{1},i_{2},\ldots,i_{n}}a_{i_{1}i_{2}\ldots{i}_{n}}x_{1}^{i_{1}}x_{2}^{i_{2}}\cdots{x}_{n}^{i_{n}},
$$
其中 $a_{i_{1}i_{2}\ldots{i}_{n}}\in{K}$, $i_{1},i_{2},\ldots,i_{n}$ 是非负整数. 只有有限多个单项式的系数不为 $0$. 这种表达式称为数域 $K$ 上的 $n$ 元多项式.

> **定理 7.9.1 (首项定理)**
> 
> 在 $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ 中两个非零多项式的乘积的首项等于它们的首项的乘积. 从而两个非零多项式的乘积仍是非零多项式, 即 $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ 是无零因子环.

$$
\sigma_{1}=x_{1}+x_{2}+\cdots+x_{n},
$$
$$
\sigma_{2}=x_{1}x_{2}+x_{1}x_{3}+\cdots+x_{n-1}x_{n},
$$
$$
\cdots\cdots
$$
$$
\sigma_{n}=x_{1}x_{2}\cdots{x}_{n}.
$$
$$
S_{1}=\sigma_{1},
$$
$$
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\cdots+\left(-1\right)^{k-1}\sigma_{k-1}S_{1}+\left(-1\right)^{k}k\sigma_{k}=0,\quad1\le{k}\le{n},
$$
$$
S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\cdots+\left(-1\right)^{n}\sigma_{n}S_{k-n}=0,\quad{k}>n.
$$

> **定义 7.10.1 (对称多项式)**
> 
> 设 $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ 是数域 $K$ 上的一个 $n$ 元多项式, 如果对于任意一个 $n$ 元排列 $j_{1}j_{2}\ldots{j}_{n}$, 都有

$$
f\left(x_{j_{1}},x_{j_{2}},\ldots,x_{j_{n}}\right)=f\left(x_{1},x_{2},\ldots,x_{n}\right),
$$
那么称 $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ 是数域 $K$ 上的一个 $n$ 元对称多项式.

## 7.8-5

设 $f\left(x\right)$ 是一个次数大于零且首项系数为 $1$ 的整系数多项式, 证明: 如果 $f\left(0\right)$ 与 $f\left(1\right)$ 都是奇数, 则 $f\left(x\right)$ 没有有理根.

### 解答 7.8-5

设

$$
f\left(x\right)=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{1}x+a_{0},
$$

其中 $a_{i}$ 都是整数.

$f\left(0\right)=a_{0}$, 所以 $a_{0}$ 是奇数.

$$
f\left(1\right)=1+a_{n-1}+\cdots+a_{1}+a_{0}
$$

是奇数.

假设 $f\left(x\right)$ 有有理根 $r=\frac{p}{q}$, 其中 $p,q$ 是互素的整数, $q>0$.

因为首项系数是 $1$, 所以 $q=1$, 即 $r$ 是整数.

而且 $r\mid{a}_{0}$, 所以 $r$ 是奇数 (因为 $a_{0}$ 是奇数).

考虑 $f\left(r\right)\bmod2$.

因为 $r$ 是奇数, 所以 $r\equiv1\pmod2$.

因此

$$
f\left(r\right)\equiv1^{n}+a_{n-1}\cdot1^{n-1}+\cdots+a_{1}\cdot1+a_{0}=f\left(1\right)\pmod2.
$$

因为 $f\left(1\right)$ 是奇数, 所以 $f\left(r\right)\equiv1\pmod2$, 即 $f\left(r\right)\ne0$.

矛盾.

因此 $f\left(x\right)$ 没有有理根.

$\blacksquare$

## 7.8-6

设

$$
f\left(x\right)=x^{3}+ax^{2}+bx+c
$$

是整系数多项式, 证明: 如果 $\left(a+b\right)c$ 是奇数, 则 $f\left(x\right)$ 在有理数域上不可约.

### 解答 7.8-6

$f\left(x\right)$ 是三次多项式. 三次多项式在有理数域上可约当且仅当它有有理根.

因为首项系数是 $1$, 所以任何有理根都是整数根, 且整除常数项 $c$.

假设 $f\left(x\right)$ 有有理根 $r$, 则 $r$ 是整数, 且 $r\mid{c}$.

因为 $\left(a+b\right)c$ 是奇数, 所以 $a+b$ 是奇数, $c$ 是奇数.

因此 $r$ 是奇数.

考虑 $f\left(r\right)\bmod2$.

因为 $r$ 是奇数, 所以 $r\equiv1\pmod2$.

因此

$$
f\left(r\right)\equiv1+a\cdot1+b\cdot1+c=1+a+b+c\pmod2.
$$

因为 $a+b$ 是奇数, $c$ 是奇数, 所以 $a+b+c$ 是偶数.

因此 $1+a+b+c$ 是奇数.

所以 $f\left(r\right)\equiv1\pmod2$, 即 $f\left(r\right)\ne0$.

矛盾.

因此 $f\left(x\right)$ 没有有理根.

所以 $f\left(x\right)$ 在有理数域上不可约.

$\blacksquare$

## 7.9-3

设 $f,g\in{K}\left[x_{1},\ldots,x_{n}\right]$, 且 $g\ne0$. 证明: 如果对于使 $g\left(c_{1},\ldots,c_{n}\right)\ne0$ 的任意一组元素 $c_{1},\ldots,c_{n}\in{K}$, 都有 $f\left(c_{1},\ldots,c_{n}\right)=0$, 则 $f\left(x_{1},\ldots,x_{n}\right)=0$.

### 解答 7.9-3

由**定理 7.9.1 (首项定理)**, 在 $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ 中两个非零多项式的乘积仍是非零多项式. 用数学归纳法.

当 $n=1$ 时.

$f\left(x\right)$ 是 $K\left[x\right]$ 中的多项式. 如果对于无穷多个 $x$ 都有 $f\left(x\right)=0$, 则 $f\left(x\right)=0$.

这是因为一个非零多项式的根的个数不超过它的次数.

归纳步骤.

假设对于 $n-1$ 元多项式结论成立.

现在看 $n$ 元多项式 $f\left(x_{1},\ldots,x_{n}\right)$.

把 $f$ 写成关于 $x_{n}$ 的多项式:

$$
f\left(x_{1},\ldots,x_{n}\right)=u_{0}\left(x_{1},\ldots,x_{n-1}\right)+u_{1}\left(x_{1},\ldots,x_{n-1}\right)x_{n}+\cdots+u_{s}\left(x_{1},\ldots,x_{n-1}\right)x_{n}^{s}.
$$

其中

$$
u_{i}\left(x_{1},\ldots,x_{n-1}\right)\in{K}\left[x_{1},\ldots,x_{n-1}\right].
$$

由归纳假设, 存在 $c_{1},\ldots,c_{n-1}\in{K}$, 使得:

1. $g\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ 不是零多项式;
2.

   $$
u_{0}\left(c_{1},\ldots,c_{n-1}\right),\ldots,u_{s}\left(c_{1},\ldots,c_{n-1}\right)
$$

   不全为零 (如果 $f$ 不是零多项式的话).

对于这样的 $c_{1},\ldots,c_{n-1}$, 考虑关于 $x_{n}$ 的一元多项式:

$$
f\left(c_{1},\ldots,c_{n-1},x_{n}\right)=u_{0}\left(c_{1},\ldots,c_{n-1}\right)+\cdots+u_{s}\left(c_{1},\ldots,c_{n-1}\right)x_{n}^{s}.
$$

如果 $f$ 不是零多项式, 则这个一元多项式也不是零多项式.

因此它只有有限多个根.

但题设说, 对于所有使得 $g\left(c_{1},\ldots,c_{n}\right)\ne0$ 的 $c_{n}$, 都有 $f\left(c_{1},\ldots,c_{n}\right)=0$.

而 $g\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ 不是零多项式, 所以它只有有限多个根.

因此存在无穷多个 $c_{n}$ 使得 $g\left(c_{1},\ldots,c_{n}\right)\ne0$.

在这些 $c_{n}$ 中, $f\left(c_{1},\ldots,c_{n}\right)=0$.

所以 $f\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ 有无穷多个根.

但 $f\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ 是一个非零一元多项式, 只有有限多个根. 矛盾.

因此 $f\left(x_{1},\ldots,x_{n}\right)=0$.

$\blacksquare$

## 7.9-4(2)

$f\in{K}\left[x_{1},\ldots,x_{n}\right]$ 称为不可约的, 如果 $f$ 的因式只有零次多项式以及 $f$ 的相伴元. 否则称为可约的. 证明: 在 $K\left[x,y\right]$ 中, 多项式 $x-y$ 是不可约的.

### 解答 7.9-4(2)

假设 $x-y$ 可约, 即存在两个次数大于零的多项式 $g\left(x,y\right),h\left(x,y\right)$ 使得:

$$
x-y=g\left(x,y\right)h\left(x,y\right).
$$

考虑次数.

左边 $x-y$ 的次数是 $1$.

右边 $g\left(x,y\right)h\left(x,y\right)$ 的次数是 $\deg{g}+\deg{h}$.

因为 $\deg{g}>0$, $\deg{h}>0$, 所以

$$
\deg{g}+\deg{h}\ge2.
$$

矛盾.

因此 $x-y$ 不可约.

$\blacksquare$

## 7.10-5

在 $K\left[x_{1},x_{2},x_{3}\right]$ 中, 利用牛顿公式把幂和 $S_{2},S_{3},S_{4}$ 用初等对称多项式表示.

### 解答 7.10-5

由牛顿公式, 设 $S_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$. 初等对称多项式:

$$
\sigma_{1}=x_{1}+x_{2}+x_{3},
$$

$$
\sigma_{2}=x_{1}x_{2}+x_{1}x_{3}+x_{2}x_{3},
$$

$$
\sigma_{3}=x_{1}x_{2}x_{3}.
$$

$S_{2}$.

由牛顿公式:

$$
S_{2}-\sigma_{1}S_{1}+2\sigma_{2}=0.
$$

因为 $S_{1}=\sigma_{1}$, 所以

$$
S_{2}=\sigma_{1}S_{1}-2\sigma_{2}=\sigma_{1}^{2}-2\sigma_{2}.
$$

$S_{3}$.

由牛顿公式:

$$
S_{3}-\sigma_{1}S_{2}+\sigma_{2}S_{1}-3\sigma_{3}=0.
$$

所以

$$
S_{3}
=\sigma_{1}S_{2}-\sigma_{2}S_{1}+3\sigma_{3}=\sigma_{1}\left(\sigma_{1}^{2}-2\sigma_{2}\right)-\sigma_{2}\sigma_{1}+3\sigma_{3}=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}.
$$

$S_{4}$.

由牛顿公式 (因为 $n=3$, $k=4>n$):

$$
S_{4}-\sigma_{1}S_{3}+\sigma_{2}S_{2}-\sigma_{3}S_{1}=0.
$$

所以

$$
S_{4}
=\sigma_{1}S_{3}-\sigma_{2}S_{2}+\sigma_{3}S_{1}=\sigma_{1}\left(\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}\right)-\sigma_{2}\left(\sigma_{1}^{2}-2\sigma_{2}\right)+\sigma_{3}\sigma_{1}=\sigma_{1}^{4}-3\sigma_{1}^{2}\sigma_{2}+3\sigma_{1}\sigma_{3}-\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+\sigma_{1}\sigma_{3}=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
$$

$S_{2}=\sigma_{1}^{2}-2\sigma_{2}$, $S_{3}=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}$,

$$
S_{4}=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
$$

$\blacksquare$

## 7.10-7

设 $f\left(x\right)\in{K}\left[x\right]$, 并且 $f\left(x\right)$ 的首项系数为 $1$, $a\in{K}$, $g\left(x\right)=\left(x-a\right)f\left(x\right)$, 证明: $D\left(g\right)=D\left(f\right)f\left(a\right)^{2}$.

### 解答 7.10-7

设

$$
f\left(x\right)=\left(x-r_{1}\right)\left(x-r_{2}\right)\cdots\left(x-r_{n}\right),
$$

其中 $r_{1},r_{2},\ldots,r_{n}$ 是 $f\left(x\right)$ 的全部根 (计重数).

则

$$
g\left(x\right)=\left(x-a\right)f\left(x\right)=\left(x-a\right)\left(x-r_{1}\right)\left(x-r_{2}\right)\cdots\left(x-r_{n}\right).
$$

记 $s_{0}=a$, $s_{1}=r_{1}$, $\ldots$, $s_{n}=r_{n}$.

判别式定义为:

$$
D\left(f\right)=\prod_{1\le{i}<{}j\le{n}}\left(r_{i}-r_{j}\right)^{2}.
$$

$$
D\left(g\right)=\prod_{0\le{i}<{}j\le{n}}\left(s_{i}-s_{j}\right)^{2}.
$$

因此

$$
D\left(g\right)
=\prod_{1\le{i}<{}j\le{n}}\left(r_{i}-r_{j}\right)^{2}\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}=D\left(f\right)\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}.
$$

而

$$
f\left(a\right)=\left(a-r_{1}\right)\left(a-r_{2}\right)\cdots\left(a-r_{n}\right).
$$

所以

$$
\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}=f\left(a\right)^{2}.
$$

因此

$$
D\left(g\right)=D\left(f\right)\cdot{f}\left(a\right)^{2}.
$$

$\blacksquare$
