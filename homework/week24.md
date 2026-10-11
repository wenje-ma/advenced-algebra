# 作业 24

> **定义1** (映射)<br>设 $S$ 和 $S'$ 是两个集合, 如果存在一个法则 $f$, 使得集合 $S$ 中每一个元素 $a$, 都有集合 $S'$ 中唯一确定的元素 $b$ 与它对应, 则称 $f$ 是 $S$ 到 $S'$ 的一个映射.

> **定义5** (线性映射)<br>$K^{n}$ 到 $K^{s}$ 的一个映射 $\mathcal{A}$ 如果保持加法和数量乘法, 即 $\forall\alpha,\beta\in K^{n},\ k\in K$, 有 $\mathcal{A}\left(\alpha+\beta\right)=\mathcal{A}\left(\alpha\right)+\mathcal{A}\left(\beta\right)$, $\mathcal{A}\left(k\alpha\right)=k\mathcal{A}\left(\alpha\right)$, 则称 $\mathcal{A}$ 是 $K^{n}$ 到 $K^{s}$ 的一个线性映射.

> **定理** (核与象的维数公式)<br>$$\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=\dim\left(K^{n}\right).$$

### 习题一

(习题 4.7-1) 判别下列对应法则是否为 $\mathbb{R}$ 到自身的映射, 是否为单射, 是否为满射:

(1) $x\mapsto x^{3}$;

(2) $x\mapsto x^{2}-x$;

(3) $x\mapsto 2^{x}$;

(4) $x\mapsto\ln x$.

### 解答 习题一

由**定义1** (映射), 判别下列对应法则是否为 $\mathbb{R}$ 到自身的映射, 是否为单射, 是否为满射.

**(1)** $f\left(x\right)=x^{3}$.

是映射. 对任意 $x\in\mathbb{R}$, $x^{3}$ 都有定义且唯一.

单射: $f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow x_{1}^{3}=x_{2}^{3}\Rightarrow x_{1}=x_{2}$. 故是单射.

满射: 对任意 $y\in\mathbb{R}$, 存在 $x=\sqrt\left[3\right]{y}$ 使得 $f\left(x\right)=y$. 故是满射.

因此既是单射又是满射 (双射).

** (2)** $f\left(x\right)=x^{2}-x$.

是映射.

单射: $f\left(0\right)=0$, $f\left(1\right)=0$, 但 $0\ne1$. 故不是单射.

满射: $f\left(x\right)=x^{2}-x=\left(x-\frac{1}{2}\right)^{2}-\frac{1}{4}\ge-\frac{1}{4}$. 例如 $-1$ 没有原象. 故不是满射.

因此既不是单射也不是满射.

** (3)** $f\left(x\right)=2^{x}$.

是映射.

单射: $f\left(x_{1}\right)=f\left(x_{2}\right)\Rightarrow 2^{x_{1}}=2^{x_{2}}\Rightarrow x_{1}=x_{2}$. 故是单射.

满射: $2^{x}>0$. 例如 $-1$ 没有原象. 故不是满射.

因此是单射但不是满射.

** (4)** $f\left(x\right)=\ln x$.

不是映射. 因为对 $x\le0$, $\ln x$ 没有定义, 不是对所有 $x\in\mathbb{R}$ 都有对应.

$\blacksquare$

### 习题二

(习题 4.7-4) 设 $S$ 是一个有限集合. 证明: 如果映射 $f:S\to S$ 是单射, 则 $f$ 一定是双射.

### 解答 习题二

由**定义1** (映射), 设 $S$ 有 $n$ 个元素.

$f$ 是单射, 故 $S$ 中不同元素的象也不同. 因此 $f\left(S\right)$ 的元素个数等于 $\left|S\right|=n$.

又因为 $f\left(S\right)\subseteq S$, 且 $\left|f\left(S\right)\right|=n=\left|S\right|$, 所以 $f\left(S\right)=S$.

即 $f$ 是满射.

因此 $f$ 既是单射又是满射, 即 $f$ 是双射. $\blacksquare$

### 习题三

(习题 4.7-7) 设

$$
A=\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
-1 & 2 & 1 & 3\\
1 & 2 & 5 & 5
\end{array}\right].
$$

令 $\mathcal{A}\left(\alpha\right)=A\alpha$, $\forall\alpha\in K^{4}$.

(1) 求 $\operatorname{Im}\mathcal{A}$ 的维数和一个基;

(2) 求 $\ker\mathcal{A}$ 的维数和一个基.

### 解答 习题三

由**定义5** (线性映射)和**定理** (核与象的维数公式), $\mathcal{A}\left(\alpha\right)=A\alpha$ 是线性映射.

**(1)** $\operatorname{Im}\mathcal{A}$ 等于 $A$ 的列空间.

对 $A$ 作初等行变换:

$$
A=\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
-1 & 2 & 1 & 3\\
1 & 2 & 5 & 5
\end{array}\right]
\rightarrow
\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
0 & 2 & 3 & 4\\
0 & 2 & 3 & 4
\end{array}\right]
\rightarrow
\left[\begin{array}{rrrr}
1 & 0 & 2 & 1\\
0 & 2 & 3 & 4\\
0 & 0 & 0 & 0
\end{array}\right].
$$

因此 $\operatorname{rank}\left(A\right)=2$.

主元列为第 $1$ 列和第 $2$ 列, 故 $\operatorname{Im}\mathcal{A}$ 的一个基为

$$
\alpha_{1}=\left(1,-1,1\right)^{T},\ \alpha_{2}=\left(0,2,2\right)^{T}.
$$

$\dim\left(\operatorname{Im}\mathcal{A}\right)=\operatorname{rank}\left(A\right)=2$.

** (2)** $\ker\mathcal{A}$ 是 $Ax=0$ 的解空间.

由行阶梯形得同解方程组:

$$
\begin{cases}
x_{1}+2x_{3}+x_{4}=0,\\
2x_{2}+3x_{3}+4x_{4}=0.
\end{cases}
$$

自由未知量为 $x_{3},x_{4}$.

$$
x_{1}=-2x_{3}-x_{4},\  x_{2}=-\frac{3}{2}x_{3}-2x_{4}.
$$

令 $x_{3}=1,\ x_{4}=0$:

$$
\xi_{1}=\left(-2,-\frac{3}{2},1,0\right)^{T}.
$$

令 $x_{3}=0,\ x_{4}=1$:

$$
\xi_{2}=\left(-1,-2,0,1\right)^{T}.
$$

因此 $\ker\mathcal{A}$ 的一个基为 $\xi_{1},\xi_{2}$.

$\dim\left(\ker\mathcal{A}\right)=4-\operatorname{rank}\left(A\right)=2$.

由**定理** (核与象的维数公式), 验证: $\dim\left(\ker\mathcal{A}\right)+\dim\left(\operatorname{Im}\mathcal{A}\right)=2+2=4=\dim\left(K^{4}\right)$.

$\blacksquare$
