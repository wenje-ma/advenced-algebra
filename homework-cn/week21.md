# week21

> **定义 7.2.1 (整除)**
> 
> 设 $f\left(x\right),g\left(x\right)\in K\left[x\right]$, 如果存在 $h\left(x\right)\in K\left[x\right]$, 使得 $f\left(x\right)=h\left(x\right)g\left(x\right)$, 则称 $g\left(x\right)$ 整除 $f\left(x\right)$, 记作 $g\left(x\right)\mid f\left(x\right)$.

> **定理 7.2.1 (带余除法)**
> 
> 在 $K\left[x\right]$ 中, 对于任意两个多项式 $f\left(x\right),g\left(x\right)$, 其中 $g\left(x\right)\ne0$, 存在唯一的一对多项式 $h\left(x\right),r\left(x\right)$, 使得

> **定义 7.3.1 (最大公因式)**
> 
> 设 $f\left(x\right),g\left(x\right)\in K\left[x\right]$, $d\left(x\right)$ 是 $f\left(x\right)$ 与 $g\left(x\right)$ 的一个公因式. 如果 $f\left(x\right)$ 与 $g\left(x\right)$ 的任一公因式都能整除 $d\left(x\right)$, 则称 $d\left(x\right)$ 是 $f\left(x\right)$ 与 $g\left(x\right)$ 的一个最大公因式.

> **定理 7.3.1 (最大公因式的存在性与倍式和)**
> 
> 对于 $K\left[x\right]$ 中任意两个多项式 $f\left(x\right)$ 与 $g\left(x\right)$, 存在它们的一个最大公因式 $d\left(x\right)$, 并且 $d\left(x\right)$ 可以表示成 $f\left(x\right)$ 与 $g\left(x\right)$ 的倍式和, 即有 $u\left(x\right),v\left(x\right)\in K\left[x\right]$, 使得

$$
d\left(x\right)=u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right).
$$

> **定义 7.3.2 (互素)**
> 
> 在 $K\left[x\right]$ 中, 如果 $f\left(x\right)$ 与 $g\left(x\right)$ 的最大公因式是零次多项式, 则称 $f\left(x\right)$ 与 $g\left(x\right)$ 互素.

## 7.2-4

设

$$
f\left(x\right)=x^{3}-3x^{2}+ax+a_{0},
$$

$g\left(x\right)=x^{2}-3x+1$, 求 $g\left(x\right)$ 整除 $f\left(x\right)$ 的充分必要条件.

### 解答 7.2-4

用 $g\left(x\right)$ 除 $f\left(x\right)$:

商式首项: $x^{3}/x^{2}=x$.

$$
x\cdot g\left(x\right)=x^{3}-3x^{2}+x.
$$

余式:

$$
f-x\cdot g=\left(a-1\right)x+a_{0}.
$$

余式次数 $< 2$, 停止.

因此 $g\left(x\right)\mid f\left(x\right)$ 当且仅当余式为零, 即

$$
\left(a-1\right)x+a_{0}=0.
$$

这对所有 $x$ 成立当且仅当

$$
a-1=0,\quad a_{0}=0.
$$

所以充分必要条件是 $a=1$, $a_{0}=0$. $\blacksquare$

## 7.2-5

用综合除法求一次多项式 $g\left(x\right)$ 除 $f\left(x\right)$ 所得的商式与余式.

(1)

$$
f\left(x\right)=3x^{4}-5x^{2}+2x-1,
$$

$g\left(x\right)=x-4$;

(2) $f\left(x\right)=5x^{3}-3x+4$, $g\left(x\right)=x+2$.

### 解答 7.2-5

**(1)** 综合除法:

$$
\begin{array}{r|rrrrr}
4 & 3 & 0 & -5 & 2 & -1\\
  &   & 12 & 48 & 172 & 776\\
\hline
  & 3 & 12 & 43 & 174 & 775
\end{array}
$$

因此

$$
\text{商式 }h\left(x\right)=3x^{3}+12x^{2}+43x+174.
$$

$$
\text{余式 }r\left(x\right)=775.
$$

**(2)** 综合除法:

$$
\begin{array}{r|rrrr}
-2 & 5 & 0 & -3 & 4\\
   &   & -10 & 20 & -34\\
\hline
   & 5 & -10 & 17 & -30
\end{array}
$$

因此

$$
\text{商式 }h\left(x\right)=5x^{2}-10x+17.
$$

$$
\text{余式 }r\left(x\right)=-30.
$$

$\blacksquare$

## 7.3-1(1)

求 $f\left(x\right)$ 与 $g\left(x\right)$ 的最大公因式, 并且把 $\left(f\left(x\right),g\left(x\right)\right)$ 表示成 $f\left(x\right)$ 与 $g\left(x\right)$ 的倍式和:

$$
f\left(x\right)=x^{4}+3x^{3}-x^{2}-4x-3,\quad g\left(x\right)=3x^{3}+10x^{2}+2x-3.
$$

### 解答 7.3-1(1)

由**定理 7.3.1 (最大公因式的存在性与倍式和)**, 存在最大公因式 $d\left(x\right)$, 并且 $d\left(x\right)$ 可以表示成 $f\left(x\right)$ 与 $g\left(x\right)$ 的倍式和. 用辗转相除法.

**第一步**: $f$ 除以 $g$.

商式首项: $\frac{1}{3}x$.

$$
f-\frac{1}{3}xg=-\frac{1}{3}x^{3}-\frac{5}{3}x^{2}-3x-3.
$$

乘以 $-3$, 令

$$
r_{1}\left(x\right)=x^{3}+5x^{2}+9x+9.
$$

**第二步**: $g$ 除以 $r_{1}$.

商式首项: $3$.

$$
g-3r_{1}=-5x^{2}-25x-30.
$$

乘以 $-\frac{1}{5}$, 令 $r_{2}\left(x\right)=x^{2}+5x+6$.

**第三步**: $r_{1}$ 除以 $r_{2}$.

商式首项: $x$.

$$
r_{1}-xr_{2}=3x+9=3\left(x+3\right).
$$

**第四步**: $r_{2}$ 除以 $x+3$.

$$
r_{2}=x^{2}+5x+6=\left(x+2\right)\left(x+3\right).
$$

因此最后一个非零余式是 $x+3$.

$$
\left(f\left(x\right),g\left(x\right)\right)=x+3.
$$

表示成倍式和:

由

$$
r_{2}=-\frac{1}{5}g+\frac{3}{5}r_{1}
$$

$r_{1}=-3f+xg$, 得

$$
r_{2}=-\frac{9}{5}f+\left(\frac{3x}{5}-\frac{1}{5}\right)g.
$$

由 $x+3=r_{1}-xr_{2}$, 得

$$
x+3
=-3f+xg-x\left[-\frac{9}{5}f+\left(\frac{3x}{5}-\frac{1}{5}\right)g\right]=\frac{9x-15}{5}f+\frac{-3x^{2}+6x}{5}g.
$$

因此, 由**定理 7.3.1 (最大公因式的存在性与倍式和)**,

$$
\left(f,g\right)=\frac{9x-15}{5}\cdot f\left(x\right)+\frac{-3x^{2}+6x}{5}\cdot g\left(x\right).
$$

$\blacksquare$

## 7.3-5

证明: 在 $K\left[x\right]$ 中, 如果 $f\left(x\right),g\left(x\right)$ 不全为零, 并且

$$
u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right)=\left(f\left(x\right),g\left(x\right)\right),
$$

则 $\left(u\left(x\right),v\left(x\right)\right)=1$.

### 解答 7.3-5

设 $d\left(x\right)=\left(f\left(x\right),g\left(x\right)\right)$.

则 $f\left(x\right)=d\left(x\right)f_{1}\left(x\right)$, $g\left(x\right)=d\left(x\right)g_{1}\left(x\right)$, 且 $\left(f_{1}\left(x\right),g_{1}\left(x\right)\right)=1$.

由题设,

$$
u\left(x\right)f\left(x\right)+v\left(x\right)g\left(x\right)=d\left(x\right).
$$

两边除以 $d\left(x\right)$:

$$
u\left(x\right)f_{1}\left(x\right)+v\left(x\right)g_{1}\left(x\right)=1.
$$

这说明 $u\left(x\right)$ 与 $v\left(x\right)$ 的一个倍式和等于 $1$.

因此 $\left(u\left(x\right),v\left(x\right)\right)=1$. $\blacksquare$

## 7.3-7

设 $f\left(x\right),g\left(x\right)\in K\left[x\right]$, 并且 $a,b,c,d\in K$, 使得 $ad-bc\ne0$. 证明:

$$
\left(af+bg,cf+dg\right)=\left(f,g\right).
$$

### 解答 7.3-7

设 $d_{1}=\left(af+bg,cf+dg\right)$, $d_{2}=\left(f,g\right)$.

因为 $d_{2}\mid f$ 且 $d_{2}\mid g$, 所以 $d_{2}\mid\left(af+bg\right)$ 且 $d_{2}\mid\left(cf+dg\right)$.

因此 $d_{2}\mid d_{1}$.

反过来, 因为 $ad-bc\ne0$, 我们可以解出 $f,g$ 用 $af+bg,cf+dg$ 表示:

$$
f=\frac{d}{ad-bc}\left(af+bg\right)-\frac{b}{ad-bc}\left(cf+dg\right).
$$

$$
g=-\frac{c}{ad-bc}\left(af+bg\right)+\frac{a}{ad-bc}\left(cf+dg\right).
$$

因为 $d_{1}\mid\left(af+bg\right)$ 且 $d_{1}\mid\left(cf+dg\right)$, 所以 $d_{1}\mid f$ 且 $d_{1}\mid g$.

因此 $d_{1}\mid d_{2}$.

所以 $d_{1}\sim d_{2}$.

首项系数都是 $1$, 故 $d_{1}=d_{2}$. $\blacksquare$

## 7.3-9

证明: $K\left[x\right]$ 中两个非零多项式 $f\left(x\right)$ 与 $g\left(x\right)$ 不互素的充分必要条件是, 存在两个非零多项式 $u\left(x\right),v\left(x\right)$, 使 $u\left(x\right)f\left(x\right)=v\left(x\right)g\left(x\right)$, $\deg u\left(x\right)< \deg g\left(x\right)$, $\deg v\left(x\right)< \deg f\left(x\right)$.

### 解答 7.3-9

**必要性**. 若 $f$ 与 $g$ 不互素, 设 $d\left(x\right)=\left(f,g\right)$, $\deg d> 0$.

令

$$
u\left(x\right)=\frac{g\left(x\right)}{d\left(x\right)},\quad v\left(x\right)=\frac{f\left(x\right)}{d\left(x\right)}.
$$

则

$$
u\left(x\right)f\left(x\right)=\frac{g\left(x\right)}{d\left(x\right)}\cdot f\left(x\right)=\frac{f\left(x\right)}{d\left(x\right)}\cdot g\left(x\right)=v\left(x\right)g\left(x\right).
$$

且

$$
\deg u=\deg g-\deg d< \deg g.
$$

$$
\deg v=\deg f-\deg d< \deg f.
$$

**充分性**. 若存在非零 $u,v$ 使得 $uf=vg$, 且 $\deg u< \deg g$, $\deg v< \deg f$.

假设 $f$ 与 $g$ 互素, 即 $\left(f,g\right)=1$.

由 $uf=vg$, 得 $g\mid uf$.

因为 $\left(f,g\right)=1$, 所以 $g\mid u$.

但 $\deg u< \deg g$, 所以只能 $u=0$, 矛盾.

因此 $f$ 与 $g$ 不互素. $\blacksquare$

## 7.3-11

设 $A\in M_{n}\left(K\right)$, $f\left(x\right),g\left(x\right)\in K\left[x\right]$. 证明: 如果 $d\left(x\right)$ 是 $f\left(x\right)$ 与 $g\left(x\right)$ 的一个最大公因式, 则 $d\left(A\right)$ 的核等于 $f\left(A\right)$ 的核与 $g\left(A\right)$ 的核的交.

### 解答 7.3-11

因为 $d$ 是 $f$ 与 $g$ 的最大公因式, 所以 $d\mid f$ 且 $d\mid g$.

即存在 $f_{1},g_{1}$ 使得 $f=df_{1}$, $g=dg_{1}$.

设 $X\in\ker d\left(A\right)$, 即 $d\left(A\right)X=0$.

则

$$
f\left(A\right)X=f_{1}\left(A\right)d\left(A\right)X=0,
$$

即 $X\in\ker f\left(A\right)$.

同理,

$$
g\left(A\right)X=g_{1}\left(A\right)d\left(A\right)X=0,
$$

即 $X\in\ker g\left(A\right)$.

因此

$$
\ker d\left(A\right)\subseteq\ker f\left(A\right)\cap\ker g\left(A\right).
$$

反过来, 设 $X\in\ker f\left(A\right)\cap\ker g\left(A\right)$, 即 $f\left(A\right)X=0$ 且 $g\left(A\right)X=0$.

因为 $d$ 是 $f$ 与 $g$ 的最大公因式, 所以存在 $u,v$ 使得 $uf+vg=d$.

因此

$$
d\left(A\right)X=u\left(A\right)f\left(A\right)X+v\left(A\right)g\left(A\right)X=0+0=0.
$$

即 $X\in\ker d\left(A\right)$.

因此

$$
\ker f\left(A\right)\cap\ker g\left(A\right)\subseteq\ker d\left(A\right).
$$

所以

$$
\ker d\left(A\right)=\ker f\left(A\right)\cap\ker g\left(A\right).
$$

$\blacksquare$
