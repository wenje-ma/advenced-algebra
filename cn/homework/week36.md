# week36

> **定义 7.4.1 (不可约多项式)**<br>$K\left[x\right]$ 中一个次数大于零的多项式 $p\left(x\right)$, 如果它在 $K\left[x\right]$ 中的因式只有零次多项式和 $p\left(x\right)$ 的相伴元, 则称 $p\left(x\right)$ 是数域 $K$ 上的一个不可约多项式.

> **性质 7.4.1 (不可约多项式的性质)**<br>在 $K\left[x\right]$ 中, 如果 $p\left(x\right)$ 不可约, 且 $p\left(x\right)\mid f\left(x\right)g\left(x\right)$, 则 $p\left(x\right)\mid f\left(x\right)$ 或 $p\left(x\right)\mid g\left(x\right)$.

> **定理 7.4.1 (唯一因式分解定理)**<br>$K\left[x\right]$ 中每一个次数大于零的多项式都能唯一地分解成数域 $K$ 上有限多个不可约多项式的乘积.

---

## 7.4-2(2)

分别在复数域, 实数域和有理数域上分解下列多项式为不可约因式的乘积:

$$
x^{4}+4.
$$

### 解答 7.4-2(2)

由**定理 7.4.1 (唯一因式分解定理)**, $K\left[x\right]$ 中每一个次数大于零的多项式都能唯一地分解成数域 $K$ 上有限多个不可约多项式的乘积.

**复数域**.

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

**实数域**.

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

**有理数域**.

$x^{2}-2x+2$ 的判别式 $\Delta=4-8=-4< 0$, 在有理数域上不可约.

$x^{2}+2x+2$ 的判别式 $\Delta=4-8=-4< 0$, 在有理数域上不可约.

因此在有理数域上,

$$
x^{4}+4=\left(x^{2}-2x+2\right)\left(x^{2}+2x+2\right).
$$

以上分解都是唯一的. $\blacksquare$

---

## 7.4-3

证明: 在 $K\left[x\right]$ 中, $g^{2}\left(x\right)\mid f^{2}\left(x\right)$ 当且仅当 $g\left(x\right)\mid f\left(x\right)$.

### 解答 7.4-3

由**性质 7.4.1 (不可约多项式的性质)**, 在 $K\left[x\right]$ 中, 如果 $p\left(x\right)$ 不可约, 且 $p\left(x\right)\mid f\left(x\right)g\left(x\right)$, 则 $p\left(x\right)\mid f\left(x\right)$ 或 $p\left(x\right)\mid g\left(x\right)$.

**必要性**. 若 $g^{2}\mid f^{2}$, 证明 $g\mid f$.

设 $p$ 是 $g$ 的一个不可约因式, 重数为 $k$.

则 $p^{2k}\mid g^{2}\mid f^{2}$.

所以 $p$ 在 $f$ 的标准分解式中的重数 $m$ 满足 $2m\ge2k$, 即 $m\ge k$.

因此 $p^{k}\mid f$.

对 $g$ 的所有不可约因式都作此推理, 得 $g\mid f$.

**充分性**. 若 $g\mid f$, 证明 $g^{2}\mid f^{2}$.

若 $g\mid f$, 则存在 $h$ 使得 $f=gh$.

所以

$$
f^{2}=g^{2}h^{2},
$$

即 $g^{2}\mid f^{2}$.

$g^{2}\left(x\right)\mid f^{2}\left(x\right)$ 当且仅当 $g\left(x\right)\mid f\left(x\right)$. $\blacksquare$

---

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
