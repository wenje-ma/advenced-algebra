# 作业 37

> **定义1** (重因式)<br>在 $K\left[x\right]$ 中, 不可约多项式 $p\left(x\right)$ 称为多项式 $f\left(x\right)$ 的 $k$ 重因式, 如果 $p^{k}\left(x\right)\mid f\left(x\right)$, 而 $p^{k+1}\left(x\right)\nmid f\left(x\right)$.

> **定理3** (无重因式的判别)<br>设 $K$ 是数域, $K\left[x\right]$ 中次数大于零的多项式 $f\left(x\right)$ 没有重因式的充分必要条件是 $f\left(x\right)$ 与它的导数 $f'\left(x\right)$ 互素.

### 习题一

(习题 7.5-2) $a,b$ 应该满足什么条件, 下述实系数多项式才能有重因式:

$$
f\left(x\right)=x^{4}+2ax^{2}+b.
$$

### 解答 习题一

由**定理3** (无重因式的判别), $f\left(x\right)$ 没有重因式的充分必要条件是 $f\left(x\right)$ 与它的导数 $f'\left(x\right)$ 互素. 求导数:

$$
f'\left(x\right)=4x^{3}+4ax=4x\left(x^{2}+a\right).
$$

$f$ 有重因式的充分必要条件是 $\left(f,f'\right)\ne1$, 即 $f$ 与 $f'$ 有公共因式.

$f'$ 的因式是 $x$ 和 $x^{2}+a$.

**情况1**: $x\mid f$.

$f\left(0\right)=b=0$.

所以当 $b=0$ 时, $x$ 是 $f$ 的因式.

此时 $f=x^{2}\left(x^{2}+2a\right)$, $x$ 是 $f$ 的 $2$ 重因式 (除非 $a=0$, 此时 $x$ 是 $4$ 重因式).

**情况2**: $x^{2}+a\mid f$.

作多项式除法:

$$
f\left(x\right)=x^{4}+2ax^{2}+b=\left(x^{2}+a\right)^{2}+\left(b-a^{2}\right).
$$

所以 $x^{2}+a\mid f$ 当且仅当 $b-a^{2}=0$, 即 $b=a^{2}$.

此时 $f=\left(x^{2}+a\right)^{2}$, $x^{2}+a$ 是 $f$ 的 $2$ 重因式.

综合两种情况, 由**定理3** (无重因式的判别), $f$ 有重因式的充分必要条件是

$$
b=0\text{或} b=a^{2}.
$$

$\blacksquare$

### 习题二

(习题 7.5-6) 在 $Q\left[x\right]$ 中求一个没有重因式的多项式 $g\left(x\right)$, 使它与 $f\left(x\right)$ 含有完全相同的不可约因式 (不计重数); 然后求 $f\left(x\right)$ 的标准分解式:

$$
f\left(x\right)=x^{5}-3x^{4}+2x^{3}+2x^{2}-3x+1.
$$

### 解答 习题二

求导数:

$$
f'\left(x\right)=5x^{4}-12x^{3}+6x^{2}+4x-3.
$$

用辗转相除法求 $\left(f,f'\right)$.

**第一步**: $f$ 除以 $f'$.

商式首项: $\frac{1}{5}x$.

$$
f-\frac{1}{5}xf'=-\frac{3}{5}x^{4}+\frac{4}{5}x^{3}+\frac{6}{5}x^{2}-\frac{12}{5}x+1.
$$

乘以 $-\frac{5}{3}$, 令

$$
r_{1}\left(x\right)=x^{4}-\frac{4}{3}x^{3}-2x^{2}+4x-\frac{5}{3}.
$$

**第二步**: $f'$ 除以 $r_{1}$.

商式首项: $5$.

$$
f'-5r_{1}=-\frac{16}{3}x^{3}+16x^{2}-16x+\frac{16}{3}.
$$

乘以 $-\frac{3}{16}$, 令

$$
r_{2}\left(x\right)=x^{3}-3x^{2}+3x-1=\left(x-1\right)^{3}.
$$

**第三步**: $r_{1}$ 除以 $r_{2}$.

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

**求标准分解式**.

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
-4a+6=-4+6=2,;6a-4=6-4=2,-4a+1=-4+1=-3,;a=1.
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
