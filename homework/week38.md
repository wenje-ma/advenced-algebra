# 作业 38

> **定义1** (多项式的根)<br>设 $K$ 是一个数域, 设 $R$ 是一个有单位元的交换环, 且 $R$ 可看成是 $K$ 的一个扩环. 对于 $K\left[x\right]$ 中一个多项式 $f\left(x\right)$, 如果 $R$ 中有一个元素 $c$ 使得 $f\left(c\right)=0$, 则称 $c$ 是 $f\left(x\right)$ 在 $R$ 中的一个根.

> **定理1** (余数定理)<br>在 $K\left[x\right]$ 中, 用 $x-a$ 去除 $f\left(x\right)$ 所得的余式是 $f\left(a\right)$.

> **推论2** (因式定理)<br>在 $K\left[x\right]$ 中, $x-a$ 整除 $f\left(x\right)$ 当且仅当 $f\left(a\right)=0$.

### 习题一

(习题 7.6-1) 设 $f\left(x\right)=x^{5}+7x^{4}+19x^{3}+26x^{2}+20x+8\in Q\left[x\right]$, 判断 $-2$ 是不是多项式 $f\left(x\right)$ 的根, 如果是的话, 它是几重根?

### 解答 习题一

由**推论2** (因式定理), 在 $K\left[x\right]$ 中, $x-a$ 整除 $f\left(x\right)$ 当且仅当 $f\left(a\right)=0$. 计算 $f\left(-2\right)$:

$$
\begin{aligned}f\left(-2\right)
&=\left(-2\right)^{5}+7\left(-2\right)^{4}+19\left(-2\right)^{3}+26\left(-2\right)^{2}+20\left(-2\right)+8\\
&=-32+112-152+104-40+8\\
&=0.
\end{aligned}
$$

所以 $-2$ 是 $f\left(x\right)$ 的根.

用综合除法看 $x+2$ 能除几次.

**第一次**:

$$
\begin{array}{r|rrrrrr}
-2 & 1 & 7 & 19 & 26 & 20 & 8\\
   &   & -2 & -10 & -18 & -16 & -8\\
\hline
   & 1 & 5 & 9 & 8 & 4 & 0
\end{array}
$$

余式为 $0$, 商式是 $x^{4}+5x^{3}+9x^{2}+8x+4$.

**第二次**:

$$
\begin{array}{r|rrrrr}
-2 & 1 & 5 & 9 & 8 & 4\\
   &   & -2 & -6 & -6 & -4\\
\hline
   & 1 & 3 & 3 & 2 & 0
\end{array}
$$

余式为 $0$, 商式是 $x^{3}+3x^{2}+3x+2$.

**第三次**:

$$
\begin{array}{r|rrrr}
-2 & 1 & 3 & 3 & 2\\
   &   & -2 & -2 & -2\\
\hline
   & 1 & 1 & 1 & 0
\end{array}
$$

余式为 $0$, 商式是 $x^{2}+x+1$.

**第四次**:

$$
\begin{array}{r|rrr}
-2 & 1 & 1 & 1\\
   &   & -2 & 2\\
\hline
   & 1 & -1 & 3
\end{array}
$$

余式为 $3\ne0$.

因此 $-2$ 是 $f\left(x\right)$ 的 $3$ 重根. $\blacksquare$

### 习题二

(习题 7.6-4) 设 $f\left(x\right)=x^{4}-5x^{3}+ax^{2}+bx+9\in Q\left[x\right]$, 如果 $3$ 是 $f\left(x\right)$ 的二重根, 求 $a,b$.

### 解答 习题二

如果 $3$ 是 $f\left(x\right)$ 的二重根, 则 $f\left(3\right)=0$ 且 $f'\left(3\right)=0$.

计算 $f\left(3\right)$:

$$
\begin{aligned}f\left(3\right)
&=3^{4}-5\cdot3^{3}+a\cdot3^{2}+b\cdot3+9\\
&=81-135+9a+3b+9\\
&=-45+9a+3b.
\end{aligned}
$$

令 $f\left(3\right)=0$:

$$
9a+3b=45\quad\Rightarrow\quad 3a+b=15. \tag{1}
$$

求导数:

$$
f'\left(x\right)=4x^{3}-15x^{2}+2ax+b.
$$

计算 $f'\left(3\right)$:

$$
\begin{aligned}f'\left(3\right)
&=4\cdot3^{3}-15\cdot3^{2}+2a\cdot3+b\\
&=108-135+6a+b\\
&=-27+6a+b.
\end{aligned}
$$

令 $f'\left(3\right)=0$:

$$
6a+b=27. \tag{2}
$$

$\left(2\right)-\left(1\right)$ 得:

$$
3a=12\quad\Rightarrow\quad a=4.
$$

代入 $\left(1\right)$:

$$
3\cdot4+b=15\quad\Rightarrow\quad b=3.
$$

因此 $a=4$, $b=3$. $\blacksquare$

### 习题三

(习题 7.6-8) 求复系数多项式 $x^{n}-1$ 的标准分解式.

### 解答 习题三

$x^{n}-1=0$ 的根是 $x^{n}=1$.

$1$ 的 $n$ 次方根为:

$$
x_{k}=e^{2\pi i k/n}=\cos\frac{2\pi k}{n}+i\sin\frac{2\pi k}{n},\quad k=0,1,\ldots,n-1.
$$

因此标准分解式为:

$$
x^{n}-1=\prod_{k=0}^{n-1}\left(x-e^{2\pi i k/n}\right).
$$

$\blacksquare$
