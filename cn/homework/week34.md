# week34

> **定义 7.2.1 (整除)**<br>设 $f\left(x\right),g\left(x\right)\in K\left[x\right]$, 如果存在 $h\left(x\right)\in K\left[x\right]$, 使得 $f\left(x\right)=h\left(x\right)g\left(x\right)$, 则称 $g\left(x\right)$ 整除 $f\left(x\right)$, 记作 $g\left(x\right)\mid f\left(x\right)$.

> **定理 7.2.1 (带余除法)**<br>在 $K\left[x\right]$ 中, 对于任意两个多项式 $f\left(x\right),g\left(x\right)$, 其中 $g\left(x\right)\ne0$, 存在唯一的一对多项式 $h\left(x\right),r\left(x\right)$, 使得

$$
f\left(x\right)=h\left(x\right)g\left(x\right)+r\left(x\right),\deg r\left(x\right)< \deg g\left(x\right).
$$

---

## 7.2-3(2)

用 $g\left(x\right)$ 除 $f\left(x\right)$, 求商式与余式:

$$
f\left(x\right)=x^{4}+x^{3}-2x+3,\quad g\left(x\right)=3x^{2}-x+2.
$$

### 解答 7.2-3(2)

由**定理 7.2.1 (带余除法)**, 作多项式除法:

$$
f\left(x\right)=x^{4}+x^{3}+0x^{2}-2x+3.
$$

商式首项: $x^{4}/3x^{2}=\frac{1}{3}x^{2}$.

$$
\frac{1}{3}x^{2}\cdot g\left(x\right)=x^{4}-\frac{1}{3}x^{3}+\frac{2}{3}x^{2}.
$$

余式:

$$
f-\frac{1}{3}x^{2}g=\frac{4}{3}x^{3}-\frac{2}{3}x^{2}-2x+3.
$$

商式第二项: $\frac{4}{3}x^{3}/3x^{2}=\frac{4}{9}x$.

$$
\frac{4}{9}x\cdot g=\frac{4}{3}x^{3}-\frac{4}{9}x^{2}+\frac{8}{9}x.
$$

余式:

$$
-\frac{2}{9}x^{2}-\frac{26}{9}x+3.
$$

商式第三项: $-\frac{2}{9}x^{2}/3x^{2}=-\frac{2}{27}$.

$$
-\frac{2}{27}\cdot g=-\frac{2}{9}x^{2}+\frac{2}{27}x-\frac{4}{27}.
$$

余式:

$$
-\frac{80}{27}x+\frac{85}{27}.
$$

因此, 由**定理 7.2.1 (带余除法)**,

$$
\text{商式 }h\left(x\right)=\frac{1}{3}x^{2}+\frac{4}{9}x-\frac{2}{27}.
$$

$$
\text{余式 }r\left(x\right)=-\frac{80}{27}x+\frac{85}{27}.
$$

$\blacksquare$

---

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

---

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
