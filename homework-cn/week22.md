# week22

> **定义 7.3.1 (最大公因式)**
> 
> 设 $f\left(x\right),g\left(x\right)\in K\left[x\right]$, $d\left(x\right)$ 是 $f\left(x\right)$ 与 $g\left(x\right)$ 的一个公因式. 如果 $f\left(x\right)$ 与 $g\left(x\right)$ 的任一公因式都能整除 $d\left(x\right)$, 则称 $d\left(x\right)$ 是 $f\left(x\right)$ 与 $g\left(x\right)$ 的一个最大公因式.

> **定理 7.3.1 (最大公因式的存在性与倍式和)**
> 
> 对于 $K\left[x\right]$ 中任意两个多项式 $f\left(x\right)$ 与 $g\left(x\right)$, 存在它们的一个最大公因式 $d\left(x\right)$, 并且 $d\left(x\right)$ 可以表示成 $f\left(x\right)$ 与 $g\left(x\right)$ 的倍式和, 即有 $u\left(x\right),v\left(x\right)\in K\left[x\right]$, 使得

> **定义 7.3.2 (互素)**
> 
> 在 $K\left[x\right]$ 中, 如果 $f\left(x\right)$ 与 $g\left(x\right)$ 的最大公因式是零次多项式, 则称 $f\left(x\right)$ 与 $g\left(x\right)$ 互素.

> **定义 7.4.1 (不可约多项式)**
> 
> $K\left[x\right]$ 中一个次数大于零的多项式 $p\left(x\right)$, 如果它在 $K\left[x\right]$ 中的因式只有零次多项式和 $p\left(x\right)$ 的相伴元, 则称 $p\left(x\right)$ 是数域 $K$ 上的一个不可约多项式.

> **性质 7.4.1 (不可约多项式的性质)**
> 
> 在 $K\left[x\right]$ 中, 如果 $p\left(x\right)$ 不可约, 且 $p\left(x\right)\mid f\left(x\right)g\left(x\right)$, 则 $p\left(x\right)\mid f\left(x\right)$ 或 $p\left(x\right)\mid g\left(x\right)$.

> **定理 7.4.1 (唯一因式分解定理)**
> 
> $K\left[x\right]$ 中每一个次数大于零的多项式都能唯一地分解成数域 $K$ 上有限多个不可约多项式的乘积.

> **定义 7.5.1 (重因式)**
> 
> 在 $K\left[x\right]$ 中, 不可约多项式 $p\left(x\right)$ 称为多项式 $f\left(x\right)$ 的 $k$ 重因式, 如果 $p^{k}\left(x\right)\mid f\left(x\right)$, 而 $p^{k+1}\left(x\right)\nmid f\left(x\right)$.

> **定理 7.5.1 (无重因式的判别)**
> 
> 设 $K$ 是数域, $K\left[x\right]$ 中次数大于零的多项式 $f\left(x\right)$ 没有重因式的充分必要条件是 $f\left(x\right)$ 与它的导数 $f'\left(x\right)$ 互素.

## 7.3-12

设 $A\in M_{n}\left(K\right)$,

$$
f\left(x\right),f_{1}\left(x\right),f_{2}\left(x\right)\in K\left[x\right],
$$

记 $f\left(x\right)=f_{1}\left(x\right)f_{2}\left(x\right)$. 证明: 如果 $\left(f_{1}\left(x\right),f_{2}\left(x\right)\right)=1$, 则 $f\left(A\right)X=0$ 的任一个解可以唯一地表示成 $f_{1}\left(A\right)X=0$ 的一个解与 $f_{2}\left(A\right)X=0$ 的一个解的和.

### 解答 7.3-12

存在性.

因为 $\left(f_{1},f_{2}\right)=1$, 所以存在 $u,v$ 使得 $uf_{1}+vf_{2}=1$.

设 $X$ 是 $f\left(A\right)X=0$ 的解, 即 $f_{1}\left(A\right)f_{2}\left(A\right)X=0$.

令

$$
X_{1}=v\left(A\right)f_{2}\left(A\right)X,\quad X_{2}=u\left(A\right)f_{1}\left(A\right)X.
$$

则

$$
X_{1}+X_{2}=\left[v\left(A\right)f_{2}\left(A\right)+u\left(A\right)f_{1}\left(A\right)\right]X=1\cdot X=X.
$$

验证 $X_{1}\in\ker f_{1}\left(A\right)$:

$$
f_{1}\left(A\right)X_{1}=f_{1}\left(A\right)v\left(A\right)f_{2}\left(A\right)X=v\left(A\right)f_{1}\left(A\right)f_{2}\left(A\right)X=v\left(A\right)f\left(A\right)X=0.
$$

验证 $X_{2}\in\ker f_{2}\left(A\right)$:

$$
f_{2}\left(A\right)X_{2}=f_{2}\left(A\right)u\left(A\right)f_{1}\left(A\right)X=u\left(A\right)f_{1}\left(A\right)f_{2}\left(A\right)X=u\left(A\right)f\left(A\right)X=0.
$$

唯一性.

设 $X=X_{1}+X_{2}=Y_{1}+Y_{2}$, 其中 $X_{1},Y_{1}\in\ker f_{1}\left(A\right)$, $X_{2},Y_{2}\in\ker f_{2}\left(A\right)$.

则

$$
X_{1}-Y_{1}=Y_{2}-X_{2}.
$$

左边 $\in\ker f_{1}\left(A\right)$, 右边 $\in\ker f_{2}\left(A\right)$.

设 $Z=X_{1}-Y_{1}=Y_{2}-X_{2}$.

则 $f_{1}\left(A\right)Z=0$ 且 $f_{2}\left(A\right)Z=0$.

因为 $\left(f_{1},f_{2}\right)=1$, 所以存在 $u,v$ 使得 $uf_{1}+vf_{2}=1$.

因此

$$
Z=u\left(A\right)f_{1}\left(A\right)Z+v\left(A\right)f_{2}\left(A\right)Z=0+0=0.
$$

所以 $X_{1}=Y_{1}$, $X_{2}=Y_{2}$.

分解唯一. $\blacksquare$

## 7.4-2(2)

分别在复数域, 实数域和有理数域上分解下列多项式为不可约因式的乘积:

$$
x^{4}+4.
$$

### 解答 7.4-2(2)

由**定理 7.4.1 (唯一因式分解定理)**, $K\left[x\right]$ 中每一个次数大于零的多项式都能唯一地分解成数域 $K$ 上有限多个不可约多项式的乘积.

复数域.

$x^{4}+4=0$ 的根是 $x^{4}=-4=4e^{i\pi}$.

因此

$$
x=4^{1/4}e^{i\left(\pi/4+k\pi/2\right)},\ k=0,1,2,3.
$$

$4^{1/4}=\sqrt{2}$.

所以四个根为:

$$
x_{1}=1+i,\ x_{2}=-1+i,\ x_{3}=-1-i,\ x_{4}=1-i.
$$

因此

$$
x^{4}+4=\left(x-1-i\right)\left(x+1-i\right)\left(x+1+i\right)\left(x-1+i\right).
$$

实数域.

把共轭的根配对:

$$
\left(x-1-i\right)\left(x-1+i\right)=\left(x-1\right)^{2}+1=x^{2}-2x+2.
$$

$$
\left(x+1-i\right)\left(x+1+i\right)=\left(x+1\right)^{2}+1=x^{2}+2x+2.
$$

因此

$$
x^{4}+4=\left(x^{2}-2x+2\right)\left(x^{2}+2x+2\right).
$$

有理数域.

$x^{2}-2x+2$ 的判别式 $\Delta=4-8=-4< 0$, 在有理数域上不可约.

$x^{2}+2x+2$ 的判别式 $\Delta=4-8=-4< 0$, 在有理数域上不可约.

因此在有理数域上,

$$
x^{4}+4=\left(x^{2}-2x+2\right)\left(x^{2}+2x+2\right).
$$

以上分解都是唯一的. $\blacksquare$

## 7.4-3

证明: 在 $K\left[x\right]$ 中, $g^{2}\left(x\right)\mid f^{2}\left(x\right)$ 当且仅当 $g\left(x\right)\mid f\left(x\right)$.

### 解答 7.4-3

由**性质 7.4.1 (不可约多项式的性质)**, 在 $K\left[x\right]$ 中, 如果 $p\left(x\right)$ 不可约, 且 $p\left(x\right)\mid f\left(x\right)g\left(x\right)$, 则 $p\left(x\right)\mid f\left(x\right)$ 或 $p\left(x\right)\mid g\left(x\right)$.

必要性. 若 $g^{2}\mid f^{2}$, 证明 $g\mid f$.

设 $p$ 是 $g$ 的一个不可约因式, 重数为 $k$.

则 $p^{2k}\mid g^{2}\mid f^{2}$.

所以 $p$ 在 $f$ 的标准分解式中的重数 $m$ 满足 $2m\ge2k$, 即 $m\ge k$.

因此 $p^{k}\mid f$.

对 $g$ 的所有不可约因式都作此推理, 得 $g\mid f$.

充分性. 若 $g\mid f$, 证明 $g^{2}\mid f^{2}$.

若 $g\mid f$, 则存在 $h$ 使得 $f=gh$.

所以

$$
f^{2}=g^{2}h^{2},
$$

即 $g^{2}\mid f^{2}$.

$g^{2}\left(x\right)\mid f^{2}\left(x\right)$ 当且仅当 $g\left(x\right)\mid f\left(x\right)$. $\blacksquare$

## 7.4-7

在 $K\left[x\right]$ 中, 设 $\left(f,g_{i}\right)=1$, $i=1,2$, 证明: $\left(f,g_{1}g_{2}\right)=1$.

### 解答 7.4-7

因为 $\left(f,g_{1}\right)=1$, 所以存在 $u_{1},v_{1}$ 使得

$$
u_{1}f+v_{1}g_{1}=1.
$$

因为 $\left(f,g_{2}\right)=1$, 所以存在 $u_{2},v_{2}$ 使得

$$
u_{2}f+v_{2}g_{2}=1.
$$

两式相乘:

$$
\left(u_{1}f+v_{1}g_{1}\right)\left(u_{2}f+v_{2}g_{2}\right)=1.
$$

展开:

$$
u_{1}u_{2}f^{2}+u_{1}v_{2}fg_{2}+v_{1}u_{2}g_{1}f+v_{1}v_{2}g_{1}g_{2}=1.
$$

前三项都有 $f$, 可以写成:

$$
f\cdot\left(u_{1}u_{2}f+u_{1}v_{2}g_{2}+v_{1}u_{2}g_{1}\right)+v_{1}v_{2}\cdot g_{1}g_{2}=1.
$$

这说明 $f$ 与 $g_{1}g_{2}$ 的一个倍式和等于 $1$.

因此 $\left(f,g_{1}g_{2}\right)=1$. $\blacksquare$

## 7.5-2

$a,b$ 应该满足什么条件, 下述实系数多项式才能有重因式:

$$
f\left(x\right)=x^{4}+2ax^{2}+b.
$$

### 解答 7.5-2

由**定理 7.5.1 (无重因式的判别)**, $f\left(x\right)$ 没有重因式的充分必要条件是 $f\left(x\right)$ 与它的导数 $f'\left(x\right)$ 互素. 求导数:

$$
f'\left(x\right)=4x^{3}+4ax=4x\left(x^{2}+a\right).
$$

$f$ 有重因式的充分必要条件是 $\left(f,f'\right)\ne1$, 即 $f$ 与 $f'$ 有公共因式.

$f'$ 的因式是 $x$ 和 $x^{2}+a$.

情况1: $x\mid f$.

$f\left(0\right)=b=0$.

所以当 $b=0$ 时, $x$ 是 $f$ 的因式.

此时 $f=x^{2}\left(x^{2}+2a\right)$, $x$ 是 $f$ 的 $2$ 重因式 (除非 $a=0$, 此时 $x$ 是 $4$ 重因式).

情况2: $x^{2}+a\mid f$.

作多项式除法:

$$
f\left(x\right)=x^{4}+2ax^{2}+b=\left(x^{2}+a\right)^{2}+\left(b-a^{2}\right).
$$

所以 $x^{2}+a\mid f$ 当且仅当 $b-a^{2}=0$, 即 $b=a^{2}$.

此时 $f=\left(x^{2}+a\right)^{2}$, $x^{2}+a$ 是 $f$ 的 $2$ 重因式.

综合两种情况, 由**定理 7.5.1 (无重因式的判别)**, $f$ 有重因式的充分必要条件是

$$
b=0\text{ 或 } b=a^{2}.
$$

$\blacksquare$

## 7.5-6

在 $\mathbb{Q}\left[x\right]$ 中求一个没有重因式的多项式 $g\left(x\right)$, 使它与 $f\left(x\right)$ 含有完全相同的不可约因式 (不计重数); 然后求 $f\left(x\right)$ 的标准分解式:

$$
f\left(x\right)=x^{5}-3x^{4}+2x^{3}+2x^{2}-3x+1.
$$

### 解答 7.5-6

求导数:

$$
f'\left(x\right)=5x^{4}-12x^{3}+6x^{2}+4x-3.
$$

用辗转相除法求 $\left(f,f'\right)$.

第一步: $f$ 除以 $f'$.

商式首项: $\frac{1}{5}x$.

$$
f-\frac{1}{5}xf'=-\frac{3}{5}x^{4}+\frac{4}{5}x^{3}+\frac{6}{5}x^{2}-\frac{12}{5}x+1.
$$

乘以 $-\frac{5}{3}$, 令

$$
r_{1}\left(x\right)=x^{4}-\frac{4}{3}x^{3}-2x^{2}+4x-\frac{5}{3}.
$$

第二步: $f'$ 除以 $r_{1}$.

商式首项: $5$.

$$
f'-5r_{1}=-\frac{16}{3}x^{3}+16x^{2}-16x+\frac{16}{3}.
$$

乘以 $-\frac{3}{16}$, 令

$$
r_{2}\left(x\right)=x^{3}-3x^{2}+3x-1=\left(x-1\right)^{3}.
$$

第三步: $r_{1}$ 除以 $r_{2}$.

商式首项: $x$.

$$
r_{1}-xr_{2}=\frac{5}{3}x^{3}-5x^{2}+5x-\frac{5}{3}=\frac{5}{3}\left(x-1\right)^{3}=\frac{5}{3}r_{2}.
$$

所以

$$
r_{1}=\left(x+\frac{5}{3}\right)r_{2}.
$$

因此

$$
\left(f,f'\right)=r_{2}=\left(x-1\right)^{3}.
$$

没有重因式的多项式:

$$
g\left(x\right)=\frac{f\left(x\right)}{\left(f\left(x\right),f'\left(x\right)\right)}=\frac{f\left(x\right)}{\left(x-1\right)^{3}}.
$$

求标准分解式.

计算 $f\left(1\right)$:

$$
f\left(1\right)=1-3+2+2-3+1=0.
$$

计算 $f'\left(1\right)$:

$$
f'\left(1\right)=5-12+6+4-3=0.
$$

计算 $f''\left(x\right)$:

$$
f''\left(x\right)=20x^{3}-36x^{2}+12x+4.
$$

$$
f''\left(1\right)=20-36+12+4=0.
$$

计算 $f'''\left(x\right)$:

$$
f'''\left(x\right)=60x^{2}-72x+12.
$$

$$
f'''\left(1\right)=60-72+12=0.
$$

计算 $f''''\left(x\right)$:

$$
f''''\left(x\right)=120x-72.
$$

$$
f''''\left(1\right)=120-72=48\ne0.
$$

所以 $x=1$ 是 $f$ 的 $4$ 重根.

因此

$$
f\left(x\right)=\left(x-1\right)^{4}\left(x+a\right).
$$

展开:

$$
\left(x-1\right)^{4}\left(x+a\right)=x^{5}+\left(a-4\right)x^{4}+\left(-4a+6\right)x^{3}+\left(6a-4\right)x^{2}+\left(-4a+1\right)x+a.
$$

与

$$
f\left(x\right)=x^{5}-3x^{4}+2x^{3}+2x^{2}-3x+1
$$

比较:

$$
a-4=-3\Rightarrow a=1.
$$

验证其余系数:

$$
-4a+6=-4+6=2,\quad 6a-4=6-4=2,\quad -4a+1=-4+1=-3,\quad a=1.
$$

全部符合.

因此标准分解式:

$$
f\left(x\right)=\left(x-1\right)^{4}\left(x+1\right).
$$

没有重因式的多项式:

$$
g\left(x\right)=\left(x-1\right)\left(x+1\right)=x^{2}-1.
$$

$\blacksquare$
