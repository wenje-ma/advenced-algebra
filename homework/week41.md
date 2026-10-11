# 作业 41

> **定义1** ($n$ 元多项式)<br>设 $K$ 是一个数域, 用不属于 $K$ 的 $n$ 个符号 $x_{1},x_{2},\ldots,x_{n}$ 作表达式

$$
\sum_{i_{1},i_{2},\ldots,i_{n}}a_{i_{1}i_{2}\ldots i_{n}}x_{1}^{i_{1}}x_{2}^{i_{2}}\cdots x_{n}^{i_{n}},
$$

其中 $a_{i_{1}i_{2}\ldots i_{n}}\in K$, $i_{1},i_{2},\ldots,i_{n}$ 是非负整数. 只有有限多个单项式的系数不为 $0$. 这种表达式称为数域 $K$ 上的 $n$ 元多项式.

> **定理1** (首项定理)<br>在 $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ 中两个非零多项式的乘积的首项等于它们的首项的乘积. 从而两个非零多项式的乘积仍是非零多项式, 即 $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ 是无零因子环.

### 习题一

(习题 7.9-3) 设 $f,g\in K\left[x_{1},\ldots,x_{n}\right]$, 且 $g\ne0$. 证明: 如果对于使 $g\left(c_{1},\ldots,c_{n}\right)\ne0$ 的任意一组元素 $c_{1},\ldots,c_{n}\in K$, 都有 $f\left(c_{1},\ldots,c_{n}\right)=0$, 则 $f\left(x_{1},\ldots,x_{n}\right)=0$.

### 解答 习题一

由**定理1** (首项定理), 在 $K\left[x_{1},x_{2},\ldots,x_{n}\right]$ 中两个非零多项式的乘积仍是非零多项式. 用数学归纳法.

**当 $n=1$ 时**.

$f\left(x\right)$ 是 $K\left[x\right]$ 中的多项式. 如果对于无穷多个 $x$ 都有 $f\left(x\right)=0$, 则 $f\left(x\right)=0$.

这是因为一个非零多项式的根的个数不超过它的次数.

**归纳步骤**.

假设对于 $n-1$ 元多项式结论成立.

现在看 $n$ 元多项式 $f\left(x_{1},\ldots,x_{n}\right)$.

把 $f$ 写成关于 $x_{n}$ 的多项式:

$$
f\left(x_{1},\ldots,x_{n}\right)=u_{0}\left(x_{1},\ldots,x_{n-1}\right)+u_{1}\left(x_{1},\ldots,x_{n-1}\right)x_{n}+\ldots+u_{s}\left(x_{1},\ldots,x_{n-1}\right)x_{n}^{s}.
$$

其中

$$
u_{i}\left(x_{1},\ldots,x_{n-1}\right)\in K\left[x_{1},\ldots,x_{n-1}\right].
$$

由归纳假设, 存在 $c_{1},\ldots,c_{n-1}\in K$, 使得:

1. $g\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ 不是零多项式;
2.

   $$
   u_{0}\left(c_{1},\ldots,c_{n-1}\right),\ldots,u_{s}\left(c_{1},\ldots,c_{n-1}\right)
   $$

   不全为零 (如果 $f$ 不是零多项式的话).

对于这样的 $c_{1},\ldots,c_{n-1}$, 考虑关于 $x_{n}$ 的一元多项式:

$$
f\left(c_{1},\ldots,c_{n-1},x_{n}\right)=u_{0}\left(c_{1},\ldots,c_{n-1}\right)+\ldots+u_{s}\left(c_{1},\ldots,c_{n-1}\right)x_{n}^{s}.
$$

如果 $f$ 不是零多项式, 则这个一元多项式也不是零多项式.

因此它只有有限多个根.

但题设说, 对于所有使得 $g\left(c_{1},\ldots,c_{n}\right)\ne0$ 的 $c_{n}$, 都有 $f\left(c_{1},\ldots,c_{n}\right)=0$.

而 $g\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ 不是零多项式, 所以它只有有限多个根.

因此存在无穷多个 $c_{n}$ 使得 $g\left(c_{1},\ldots,c_{n}\right)\ne0$.

在这些 $c_{n}$ 中, $f\left(c_{1},\ldots,c_{n}\right)=0$.

所以 $f\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ 有无穷多个根.

但 $f\left(c_{1},\ldots,c_{n-1},x_{n}\right)$ 是一个非零一元多项式, 只有有限多个根. 矛盾.

因此 $f\left(x_{1},\ldots,x_{n}\right)=0$. $\blacksquare$

### 习题二

(习题 7.9-4(2)) $f\in K\left[x_{1},\ldots,x_{n}\right]$ 称为不可约的, 如果 $f$ 的因式只有零次多项式以及 $f$ 的相伴元. 否则称为可约的. 证明: 在 $K\left[x,y\right]$ 中, 多项式 $x-y$ 是不可约的.

### 解答 习题二

假设 $x-y$ 可约, 即存在两个次数大于零的多项式 $g\left(x,y\right),h\left(x,y\right)$ 使得:

$$
x-y=g\left(x,y\right)h\left(x,y\right).
$$

考虑次数.

左边 $x-y$ 的次数是 $1$.

右边 $g\left(x,y\right)h\left(x,y\right)$ 的次数是 $\deg g+\deg h$.

因为 $\deg g>0$, $\deg h>0$, 所以

$$
\deg g+\deg h\ge2.
$$

矛盾.

因此 $x-y$ 不可约. $\blacksquare$
