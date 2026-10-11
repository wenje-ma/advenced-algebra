# 作业 40

> **定义1** (本原多项式)<br>一个非零整系数多项式如果它的各项系数的最大公因数是 $1$, 则称它为本原多项式.

> **引理2** (高斯引理)<br>两个本原多项式的乘积还是本原多项式.

> **定理5** (艾森斯坦判别法)<br>设
> $$
> f\left(x\right)=a_{n}x^{n}+\ldots+a_{1}x+a_{0}
> $$
> 是一个次数 $n$ 大于零的整系数多项式, 如果存在一个素数 $p$, 使得
> (1) $p\mid a_{i}$, $i=0,1,\ldots,n-1$;
>
> (2) $p\nmid a_{n}$;
>
> (3) $p^{2}\nmid a_{0}$.
> 则 $f\left(x\right)$ 在有理数域上是不可约的.

### 习题一

(习题 7.8-2(4)) $x^{4}-2x^{3}+2x-3$ 在有理数域上是否不可约?

### 解答 习题一

由**定理5** (艾森斯坦判别法), 设

$$
f\left(x\right)=a_{n}x^{n}+\ldots+a_{1}x+a_{0}
$$

是一个次数 $n$ 大于零的整系数多项式, 如果存在一个素数 $p$, 使得 $p\mid a_{i}$ ( $i=0,1,\ldots,n-1$ ), $p\nmid a_{n}$, $p^{2}\nmid a_{0}$, 则 $f\left(x\right)$ 在有理数域上是不可约的.

先看有没有有理根.

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
a+c=-2, \tag{1}
$$

$$
ac+b+d=0, \tag{2}
$$

$$
ad+bc=2, \tag{3}
$$

$$
bd=-3. \tag{4}
$$

由 $\left(4\right)$, $bd=-3$ 的整数解有:

$$
\left(b,d\right)=\left(1,-3\right),\left(-1,3\right),\left(3,-1\right),\left(-3,1\right).
$$

逐一验证:

- $b=1,d=-3$: 由 $\left(1\right)$, $c=-2-a$. 代入 $\left(2\right)$:

  $$
  -2a-a^{2}+1-3=0\Rightarrow a^{2}+2a+2=0,
  $$

  无实根.
- $b=-1,d=3$: 代入 $\left(2\right)$:

  $$
  -2a-a^{2}-1+3=0\Rightarrow a^{2}+2a-2=0,
  $$

  无整数根.
- $b=3,d=-1$: 代入 $\left(2\right)$:

  $$
  -2a-a^{2}+3-1=0\Rightarrow a^{2}+2a-2=0,
  $$

  无整数根.
- $b=-3,d=1$: 代入 $\left(2\right)$:

  $$
  -2a-a^{2}-3+1=0\Rightarrow a^{2}+2a+2=0,
  $$

  无实根.

因此不能分解成两个整系数二次多项式的乘积.

所以 $x^{4}-2x^{3}+2x-3$ 在有理数域上不可约. $\blacksquare$

### 习题二

(习题 7.8-2(5)) $x^{4}+px^{2}+1$, $p$ 为奇素数, 在有理数域上是否不可约?

### 解答 习题二

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
a+c=0, \tag{1}
$$

$$
ac+b+d=p, \tag{2}
$$

$$
ad+bc=0, \tag{3}
$$

$$
bd=1. \tag{4}
$$

由 $\left(1\right)$, $c=-a$.

代入 $\left(3\right)$:

$$
ad+b\left(-a\right)=a\left(d-b\right)=0.
$$

所以 $a=0$ 或 $d=b$.

**情况1**: $a=0$.

则 $c=0$.

由 $\left(2\right)$: $b+d=p$.

由 $\left(4\right)$: $bd=1$.

所以 $b=d=1$ 或 $b=d=-1$.

若 $b=d=1$, 则 $b+d=2$, 故 $p=2$. 但 $p$ 是奇素数, 矛盾.

若 $b=d=-1$, 则 $b+d=-2$, 故 $p=-2$. 但 $p$ 是正素数, 矛盾.

**情况2**: $d=b$.

由 $\left(4\right)$: $b^{2}=1$, 所以 $b=1$ 或 $b=-1$.

若 $b=1$, 则 $d=1$.

由 $\left(2\right)$:

$$
-a^{2}+2=p\Rightarrow a^{2}=2-p.
$$

因为 $p$ 是奇素数, $p\ge3$, 所以 $2-p\le-1<0$, 无实根.

若 $b=-1$, 则 $d=-1$.

由 $\left(2\right)$:

$$
-a^{2}-2=p\Rightarrow a^{2}=-p-2<0,
$$

无实根.

因此不能分解成两个整系数二次多项式的乘积.

所以 $x^{4}+px^{2}+1$ 在有理数域上不可约. $\blacksquare$

### 习题三

(习题 7.8-2(7)) $2x^{3}-x^{2}+x+1$ 在有理数域上是否不可约?

### 解答 习题三

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

因此 $f\left(x\right)$ 在有理数域上可约. $\blacksquare$

### 习题四

(习题 7.8-2(8)) $x^{4}-5x^{2}+1$ 在有理数域上是否不可约?

### 解答 习题四

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
a+c=0, \tag{1}
$$

$$
ac+b+d=-5, \tag{2}
$$

$$
ad+bc=0, \tag{3}
$$

$$
bd=1. \tag{4}
$$

由 $\left(1\right)$, $c=-a$.

代入 $\left(3\right)$:

$$
ad+b\left(-a\right)=a\left(d-b\right)=0.
$$

所以 $a=0$ 或 $d=b$.

**情况1**: $a=0$.

则 $c=0$.

由 $\left(2\right)$: $b+d=-5$.

由 $\left(4\right)$: $bd=1$.

所以 $b,d$ 是方程 $t^{2}+5t+1=0$ 的根, 不是整数.

**情况2**: $d=b$.

由 $\left(4\right)$: $b^{2}=1$, 所以 $b=1$ 或 $b=-1$.

若 $b=1$, 则 $d=1$.

由 $\left(2\right)$: $-a^{2}+2=-5\Rightarrow a^{2}=7$, 不是完全平方数.

若 $b=-1$, 则 $d=-1$.

由 $\left(2\right)$: $-a^{2}-2=-5\Rightarrow a^{2}=3$, 不是完全平方数.

因此不能分解成两个整系数二次多项式的乘积.

所以 $x^{4}-5x^{2}+1$ 在有理数域上不可约. $\blacksquare$

### 习题五

(习题 7.8-5) 设 $f\left(x\right)$ 是一个次数大于零且首项系数为 $1$ 的整系数多项式, 证明: 如果 $f\left(0\right)$ 与 $f\left(1\right)$ 都是奇数, 则 $f\left(x\right)$ 没有有理根.

### 解答 习题五

设

$$
f\left(x\right)=x^{n}+a_{n-1}x^{n-1}+\ldots+a_{1}x+a_{0},
$$

其中 $a_{i}$ 都是整数.

$f\left(0\right)=a_{0}$, 所以 $a_{0}$ 是奇数.


$$
f\left(1\right)=1+a_{n-1}+\ldots+a_{1}+a_{0}
$$

是奇数.

假设 $f\left(x\right)$ 有有理根 $r=\frac{p}{q}$, 其中 $p,q$ 是互素的整数, $q>0$.

因为首项系数是 $1$, 所以 $q=1$, 即 $r$ 是整数.

而且 $r\mid a_{0}$, 所以 $r$ 是奇数 (因为 $a_{0}$ 是奇数).

考虑 $f\left(r\right)\bmod 2$.

因为 $r$ 是奇数, 所以 $r\equiv1\pmod2$.

因此

$$
f\left(r\right)\equiv1^{n}+a_{n-1}\cdot1^{n-1}+\ldots+a_{1}\cdot1+a_{0}=f\left(1\right)\pmod2.
$$

因为 $f\left(1\right)$ 是奇数, 所以 $f\left(r\right)\equiv1\pmod2$, 即 $f\left(r\right)\ne0$.

矛盾.

因此 $f\left(x\right)$ 没有有理根. $\blacksquare$

### 习题六

(习题 7.8-6) 设

$$
f\left(x\right)=x^{3}+ax^{2}+bx+c
$$

是整系数多项式, 证明: 如果 $\left(a+b\right)c$ 是奇数, 则 $f\left(x\right)$ 在有理数域上不可约.

### 解答 习题六

$f\left(x\right)$ 是三次多项式. 三次多项式在有理数域上可约当且仅当它有有理根.

因为首项系数是 $1$, 所以任何有理根都是整数根, 且整除常数项 $c$.

假设 $f\left(x\right)$ 有有理根 $r$, 则 $r$ 是整数, 且 $r\mid c$.

因为 $\left(a+b\right)c$ 是奇数, 所以 $a+b$ 是奇数, $c$ 是奇数.

因此 $r$ 是奇数.

考虑 $f\left(r\right)\bmod 2$.

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

所以 $f\left(x\right)$ 在有理数域上不可约. $\blacksquare$
