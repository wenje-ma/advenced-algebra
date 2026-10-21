# 作业 3

> **定义1** (数域)<br>设 $K$ 是复数集的一个子集, 如果 $K$ 满足:
> (1) $0,1\in K$;
>
> (2) 对加, 减, 乘, 除(除数不为 $0$) 四种运算封闭,
> 那么称 $K$ 是一个数域.

### 习题一

(习题 1.3-1) 令

$$
\mathbb Q\left(i\right)=\left\{a+bi\mid a,b\in\mathbb Q\right\},
$$

证明: $\mathbb Q\left(i\right)$ 是一个数域.

### 解答 习题一

由**定义1** (数域)的要求, 需验证 $\mathbb Q\left(i\right)$ 满足 $0,1\in K$ 且对加, 减, 乘, 除四种运算封闭.

**验证 $0,1\in\mathbb Q\left(i\right)$**. 由**定义1**第(1)条, 显然 $0=0+0\cdot i\in\mathbb Q\left(i\right)$, $1=1+0\cdot i\in\mathbb Q\left(i\right)$.

**验证对加法封闭**. 由**定义1**第(2)条, 任取

$$
\alpha=a+bi,\beta=c+di\in\mathbb Q\left(i\right),
$$

其中 $a,b,c,d\in\mathbb Q$, 则

$$
\alpha+\beta=\left(a+c\right)+\left(b+d\right)i.
$$

由于有理数对加法封闭, $a+c\in\mathbb Q$, $b+d\in\mathbb Q$, 故 $\alpha+\beta\in\mathbb Q\left(i\right)$.

**验证对减法封闭**. 由**定义1**第(2)条, 同上,

$$
\alpha-\beta=\left(a-c\right)+\left(b-d\right)i,
$$

且 $a-c\in\mathbb Q$, $b-d\in\mathbb Q$, 故 $\alpha-\beta\in\mathbb Q\left(i\right)$.

**验证对乘法封闭**. 由**定义1**第(2)条,

$$
\begin{aligned}\alpha\beta&=\left(a+bi\right)\left(c+di\right)\\
&=\left(ac-bd\right)+\left(ad+bc\right)i.
\end{aligned}
$$

由于有理数对加, 减, 乘封闭, $ac-bd\in\mathbb Q$, $ad+bc\in\mathbb Q$, 故 $\alpha\beta\in\mathbb Q\left(i\right)$.

**验证对除法封闭**. 由**定义1**第(2)条, 设 $\beta=c+di\ne 0$, 则 $c^{2}+d^{2}\ne 0$, 且

$$
\begin{aligned}\frac{\alpha}{\beta}&=\frac{a+bi}{c+di}\\
&=\frac{\left(a+bi\right)\left(c-di\right)}{\left(c+di\right)\left(c-di\right)}\\
&=\frac{ac+bd}{c^{2}+d^{2}}+\frac{bc-ad}{c^{2}+d^{2}}i.
\end{aligned}
$$

由于有理数对加, 减, 乘, 除(除数不为 $0$) 封闭, $\frac{ac+bd}{c^{2}+d^{2}}\in\mathbb Q$, $\frac{bc-ad}{c^{2}+d^{2}}\in\mathbb Q$, 故 $\frac{\alpha}{\beta}\in\mathbb Q\left(i\right)$.

综上, $\mathbb Q\left(i\right)$ 满足**定义1** (数域)的全部条件, 故 $\mathbb Q\left(i\right)$ 是一个数域. $\blacksquare$
