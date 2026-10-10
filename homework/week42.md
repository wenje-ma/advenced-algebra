# 作业 42

> **定义1** (对称多项式)<br>设 $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ 是数域 $K$ 上的一个 $n$ 元多项式, 如果对于任意一个 $n$ 元排列 $j_{1}j_{2}\ldots j_{n}$, 都有 $f\left(x_{j_{1}},x_{j_{2}},\ldots,x_{j_{n}}\right)=f\left(x_{1},x_{2},\ldots,x_{n}\right)$, 那么称 $f\left(x_{1},x_{2},\ldots,x_{n}\right)$ 是数域 $K$ 上的一个 $n$ 元对称多项式.

> **初等对称多项式**<br>$$\begin{aligned}\sigma_{1}&=x_{1}+x_{2}+\ldots+x_{n}\\sigma_{2}&=x_{1}x_{2}+x_{1}x_{3}+\ldots+x_{n-1}x_{n}\\ldots&\\sigma_{n}&=x_{1}x_{2}\ldots x_{n}.\end{aligned}$$

> **牛顿公式** (幂和与初等对称多项式的关系)<br>设 $S_{k}=x_{1}^{k}+x_{2}^{k}+\ldots+x_{n}^{k}$, 则:<br>$$\begin{aligned}S_{1}&=\sigma_{1}\\S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\ldots+\left(-1\right)^{k-1}\sigma_{k-1}S_{1}+\left(-1\right)^{k}k\sigma_{k}&=0,\quad 1\le k\le n\\S_{k}-\sigma_{1}S_{k-1}+\sigma_{2}S_{k-2}-\ldots+\left(-1\right)^{n}\sigma_{n}S_{k-n}&=0,\quad k>n.\end{aligned}$$

### 习题一

(习题 7.10-5) 在 $K\left[x_{1},x_{2},x_{3}\right]$ 中, 利用牛顿公式把幂和 $S_{2},S_{3},S_{4}$ 用初等对称多项式表示.

### 解答 习题一

由**牛顿公式**(幂和与初等对称多项式的关系), 设 $S_{k}=x_{1}^{k}+x_{2}^{k}+x_{3}^{k}$. 初等对称多项式:

$$
\sigma_{1}=x_{1}+x_{2}+x_{3},
$$

$$
\sigma_{2}=x_{1}x_{2}+x_{1}x_{3}+x_{2}x_{3},
$$

$$
\sigma_{3}=x_{1}x_{2}x_{3}.
$$

**$S_{2}$**.

由牛顿公式:

$$
S_{2}-\sigma_{1}S_{1}+2\sigma_{2}=0.
$$

因为 $S_{1}=\sigma_{1}$, 所以

$$
S_{2}=\sigma_{1}S_{1}-2\sigma_{2}=\sigma_{1}^{2}-2\sigma_{2}.
$$

**$S_{3}$**.

由牛顿公式:

$$
S_{3}-\sigma_{1}S_{2}+\sigma_{2}S_{1}-3\sigma_{3}=0.
$$

所以

$$
\begin{aligned}
S_{3}
&=\sigma_{1}S_{2}-\sigma_{2}S_{1}+3\sigma_{3}\\
&=\sigma_{1}\left(\sigma_{1}^{2}-2\sigma_{2}\right)-\sigma_{2}\sigma_{1}+3\sigma_{3}\\
&=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}.
\end{aligned}
$$

**$S_{4}$**.

由牛顿公式 (因为 $n=3$, $k=4>n$):

$$
S_{4}-\sigma_{1}S_{3}+\sigma_{2}S_{2}-\sigma_{3}S_{1}=0.
$$

所以

$$
\begin{aligned}
S_{4}
&=\sigma_{1}S_{3}-\sigma_{2}S_{2}+\sigma_{3}S_{1}\\
&=\sigma_{1}\left(\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}\right)-\sigma_{2}\left(\sigma_{1}^{2}-2\sigma_{2}\right)+\sigma_{3}\sigma_{1}\\
&=\sigma_{1}^{4}-3\sigma_{1}^{2}\sigma_{2}+3\sigma_{1}\sigma_{3}-\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+\sigma_{1}\sigma_{3}\\
&=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}.
\end{aligned}
$$

$S_{2}=\sigma_{1}^{2}-2\sigma_{2}$, $S_{3}=\sigma_{1}^{3}-3\sigma_{1}\sigma_{2}+3\sigma_{3}$, $S_{4}=\sigma_{1}^{4}-4\sigma_{1}^{2}\sigma_{2}+2\sigma_{2}^{2}+4\sigma_{1}\sigma_{3}$. $\blacksquare$

### 习题二

(习题 7.10-7) 设 $f\left(x\right)\in K\left[x\right]$, 并且 $f\left(x\right)$ 的首项系数为 $1$, $a\in K$, $g\left(x\right)=\left(x-a\right)f\left(x\right)$, 证明: $D\left(g\right)=D\left(f\right)f\left(a\right)^{2}$.

### 解答 习题二

设

$$
f\left(x\right)=\left(x-r_{1}\right)\left(x-r_{2}\right)\ldots\left(x-r_{n}\right),
$$

其中 $r_{1},r_{2},\ldots,r_{n}$ 是 $f\left(x\right)$ 的全部根 (计重数).

则

$$
g\left(x\right)=\left(x-a\right)f\left(x\right)=\left(x-a\right)\left(x-r_{1}\right)\left(x-r_{2}\right)\ldots\left(x-r_{n}\right).
$$

记 $s_{0}=a$, $s_{1}=r_{1}$, $\ldots$, $s_{n}=r_{n}$.

判别式定义为:

$$
D\left(f\right)=\prod_{1\le i<j\le n}\left(r_{i}-r_{j}\right)^{2}.
$$

$$
D\left(g\right)=\prod_{0\le i<j\le n}\left(s_{i}-s_{j}\right)^{2}.
$$

因此

$$
\begin{aligned}
D\left(g\right)
&=\prod_{1\le i<j\le n}\left(r_{i}-r_{j}\right)^{2}\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}\\
&=D\left(f\right)\cdot\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}.
\end{aligned}
$$

而

$$
f\left(a\right)=\left(a-r_{1}\right)\left(a-r_{2}\right)\ldots\left(a-r_{n}\right).
$$

所以

$$
\prod_{i=1}^{n}\left(a-r_{i}\right)^{2}=f\left(a\right)^{2}.
$$

因此

$$
D\left(g\right)=D\left(f\right)\cdot f\left(a\right)^{2}.
$$

$\blacksquare$
