# week5

> **定义 2.4.1 (余子式与代数余子式)**
> 
> $n$ 阶行列式 $\left|A\right|$ 中, 划去第 $i$ 行和第 $j$ 列, 剩下的元素按原来次序组成的 $n-1$ 阶行列式称为 $A$ 的 $\left(i,j\right)$ 元的余子式, 记作 $M_{ij}$. 令 $A_{ij}=\left(-1\right)^{i+j}M_{ij}$, 称 $A_{ij}$ 是 $A$ 的 $\left(i,j\right)$ 元的代数余子式.

> **定理 2.4.1 (行列式按一行(列)展开)**
> 
> $n$ 阶行列式 $\left|A\right|$ 等于它的第 $i$ 行元素与自己的代数余子式的乘积之和:

> **定理 2.5.1 (克拉默法则)**
> 
> $n$ 个方程的 $n$ 元线性方程组如果它的系数行列式 $\left|A\right|\ne0$, 则它有唯一解; 如果它的系数行列式 $\left|A\right|=0$, 则它无解或者有无穷多个解.

> **推论 2.5.2 (齐次方程组有非零解的条件)**
> 
> $n$ 个方程的 $n$ 元齐次线性方程组只有零解的充分必要条件是它的系数行列式不等于 $0$. 从而, $n$ 个方程的 $n$ 元齐次线性方程组有非零解的充分必要条件是它的系数行列式等于 $0$.

## 2.4-11

设数域 $K$ 上 $n$ 级矩阵 $A=\left(a_{ij}\right)$, 它的 $\left(i,j\right)$ 元的代数余子式记作 $A_{ij}$. 把 $A$ 的每个元素都加上同一个数 $t$, 得到的矩阵记作 $A\left(t\right)=\left(a_{ij}+t\right)$. 证明:

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i=1}^{n}\sum_{j=1}^{n}A_{ij}.
$$

### 解答 2.4-11

将 $A\left(t\right)$ 的第 $1$ 列拆成两个列之和: 第 $1$ 列

$$
=\left(a_{11}+t,a_{21}+t,\cdots,a_{n1}+t\right)^{\top}=\left(a_{11},a_{21},\cdots,a_{n1}\right)^{\top}+\left(t,t,\cdots,t\right)^{\top}.
$$

由行列式对列的多重线性,

$$
\left|A\left(t\right)\right|=\left|A_{1}\left(t\right)\right|+\left|A_{2}\left(t\right)\right|,
$$

其中 $\left|A_{1}\left(t\right)\right|$ 是第 $1$ 列为原列, 其余列为 $a_{ij}+t$ 的行列式, $\left|A_{2}\left(t\right)\right|$ 是第 $1$ 列为全 $t$, 其余列为 $a_{ij}+t$ 的行列式.

对 $\left|A_{1}\left(t\right)\right|$ 继续拆第 $2$ 列, 依此类推, 最后得到:

$$
\left|A\left(t\right)\right|=\left|A\right|+\sum_{j=1}^{n}t\cdot\widetilde{A}_{j},
$$

其中 $\widetilde{A}_{j}$ 是第 $j$ 列为全 $1$, 其余列为 $A$ 的列的行列式.

由**定理 2.4.1 (行列式按一行(列)展开)**, 把 $\widetilde{A}_{j}$ 按第 $j$ 列展开, 第 $j$ 列全为 $1$, 故

$$
\widetilde{A}_{j}=\sum_{i=1}^{n}1\cdot{}A_{ij}=\sum_{i=1}^{n}A_{ij}.
$$

由**定义 2.4.1 (余子式与代数余子式)**, $A_{ij}$ 是 $\left(i,j\right)$ 元的代数余子式.

因此

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{j=1}^{n}\sum_{i=1}^{n}A_{ij}.
$$

$\blacksquare$

## 2.4-12

用第 11 题给出的公式, 计算下列 $n$ 阶行列式:

(1)

$$
\left|\begin{array}{cccc}
1+x_{1}y_{1}&1+x_{1}y_{2}&\cdots&1+x_{1}y_{n}\\
1+x_{2}y_{1}&1+x_{2}y_{2}&\cdots&1+x_{2}y_{n}\\
\vdots&\vdots&&\vdots\\
1+x_{n}y_{1}&1+x_{n}y_{2}&\cdots&1+x_{n}y_{n}
\end{array}\right|.
$$

(2)

$$
\left|\begin{array}{cccc}
1+t&t&\cdots&t\\
t&2+t&\cdots&t\\
\vdots&\vdots&&\vdots\\
t&t&\cdots&n+t
\end{array}\right|.
$$

### 解答 2.4-12

(1) 把矩阵写成 $A=J+xy^{\top}$, 其中 $J$ 是全 $1$ 矩阵, $x=\left(x_{1},\cdots,x_{n}\right)^{\top}$, $y=\left(y_{1},\cdots,y_{n}\right)^{\top}$.

$A$ 是两个秩 $1$ 矩阵之和, 故 $\text{rank}\left(A\right)\le2$.

当 $n\ge3$ 时, 由矩阵秩的子式刻画, $\det\left(A\right)=0$.

当 $n=1$ 时, $\det\left(A\right)=1+x_{1}y_{1}$.

当 $n=2$ 时,

$$
\det\left(A\right)=\left(1+x_{1}y_{1}\right)\left(1+x_{2}y_{2}\right)-\left(1+x_{1}y_{2}\right)\left(1+x_{2}y_{1}\right)=x_{1}y_{1}+x_{2}y_{2}-x_{1}y_{2}-x_{2}y_{1}=\left(x_{1}-x_{2}\right)\left(y_{1}-y_{2}\right).
$$

(2) 设 $A=\text{diag}\left(1,2,\cdots,n\right)$, 则所求行列式为 $\left|A\left(t\right)\right|$.

由第 11 题,

$$
\left|A\left(t\right)\right|=\left|A\right|+t\sum_{i,j}A_{ij}.
$$

$\left|A\right|=n!$.

$A$ 是对角矩阵, 非对角元的余子式均为 $0$, 对角元的代数余子式 $A_{ii}=\frac{n!}{i}$.

故

$$
\sum_{i,j}A_{ij}=\sum_{i=1}^{n}\frac{n!}{i}=n!\sum_{i=1}^{n}\frac{1}{i}.
$$

因此

$$
\left|A\left(t\right)\right|=n!+t\cdot{}n!\sum_{i=1}^{n}\frac{1}{i}
=n!\left(1+t\sum_{i=1}^{n}\frac{1}{i}\right).
$$

$\blacksquare$

## 2.5-4

当 $a,b$ 取什么值时, 下述齐次线性方程组有非零解?

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=0,\\
x_{1}+bx_{2}+x_{3}=0,\\
x_{1}+2bx_{2}+x_{3}=0.
\end{cases}
$$

### 解答 2.5-4

由**推论 2.5.2 (齐次方程组有非零解的条件)**, 齐次线性方程组有非零解的充分必要条件是系数行列式等于 $0$.

系数行列式为

$$
\left|\begin{array}{ccc}
a&1&1\\
1&b&1\\
1&2b&1
\end{array}\right|=a\left(b\cdot1-1\cdot2b\right)-1\left(1\cdot1-1\cdot1\right)+1\left(1\cdot2b-b\cdot1\right)=a\left(-b\right)-0+b=b\left(1-a\right).
$$

令其等于 $0$, 得 $b\left(1-a\right)=0$, 即 $b=0$ 或 $a=1$.

故当 $b=0$ 或 $a=1$ 时, 该齐次线性方程组有非零解.

$\blacksquare$

## 2.5-5

当 $a,b$ 取什么值时, 下述线性方程组有唯一解?

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=2.
\end{cases}
$$

### 解答 2.5-5

由**定理 2.5.1 (克拉默法则)**, 线性方程组有唯一解的充分必要条件是系数行列式不等于 $0$.

由上题, 系数行列式为 $b\left(1-a\right)$.

故当 $b\ne0$ 且 $a\ne1$ 时, 方程组有唯一解.

$\blacksquare$

## 2.5-6

对于第 5 题中的线性方程组, 当 $a,b$ 为何值时, 方程组无解? 当 $a,b$ 为何值时, 方程组有无穷多个解?

### 解答 2.5-6

由**定理 2.5.1 (克拉默法则)**, 当系数行列式等于 $0$ 时, 方程组无解或者有无穷多个解.

情况 1: $b=0$.

方程组变为

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+x_{3}=1,\\
x_{1}+x_{3}=2.\end{
cases}
$$

后两个方程矛盾 ($1\ne2$), 故方程组无解.

情况 2: $a=1$ 且 $b\ne0$.

方程组变为

$$
\begin{cases}
x_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=2.
\end{cases}
$$

第 $2$ 行减第 $1$ 行: $\left(b-1\right)x_{2}=-1$.

第 $3$ 行减第 $1$ 行: $\left(2b-1\right)x_{2}=0$.

若 $2b-1\ne0$, 即 $b\ne\frac{1}{2}$, 则由第 $3$ 行得 $x_{2}=0$, 代入第 $2$ 行得 $0=-1$, 矛盾. 无解.

若 $2b-1=0$, 即 $b=\frac{1}{2}$, 则第 $3$ 行变为恒等式. 由第 $2$ 行得 $\left(\frac{1}{2}-1\right)x_{2}=-1$, 即 $x_{2}=2$. 代入第 $1$ 行得 $x_{1}+x_{3}=0$.

故有无穷多解: $x_{2}=2$, $x_{1}+x_{3}=0$.

综上:

- 无解: $b=0$, 或 $a=1$ 且 $b\ne\frac{1}{2}$.

- 无穷多解: $a=1$ 且 $b=\frac{1}{2}$.

$\blacksquare$

## 2.5-7

讨论下述线性方程组何时有唯一解, 有无穷多个解, 无解.

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=1.
\end{cases}
$$

### 解答 2.5-7

由**定理 2.5.1 (克拉默法则)**, 系数行列式仍为 $b\left(1-a\right)$.

唯一解: $b\ne0$ 且 $a\ne1$.

情况 1: $b=0$.

方程组变为

$$
\begin{cases}
ax_{1}+x_{2}+x_{3}=2,\\
x_{1}+x_{3}=1,\\
x_{1}+x_{3}=1.\end{
cases}
$$

后两个方程相同. 代入第 $1$ 行: $ax_{1}+x_{2}+\left(1-x_{1}\right)=2$, 即 $\left(a-1\right)x_{1}+x_{2}=1$.

无论 $a$ 取何值, $x_{1}$ 自由, $x_{2}=1-\left(a-1\right)x_{1}$, $x_{3}=1-x_{1}$. 有无穷多解.

情况 2: $a=1$ 且 $b\ne0$.

方程组变为

$$
\begin{cases}
x_{1}+x_{2}+x_{3}=2,\\
x_{1}+bx_{2}+x_{3}=1,\\
x_{1}+2bx_{2}+x_{3}=1.
\end{cases}
$$

第 $2$ 行减第 $1$ 行: $\left(b-1\right)x_{2}=-1$.

第 $3$ 行减第 $1$ 行: $\left(2b-1\right)x_{2}=-1$.

若 $b\ne1$ 且 $b\ne\frac{1}{2}$, 则

$$
x_{2}=\frac{1}{1-b}=\frac{1}{1-2b}
$$

得 $b=0$, 矛盾.

若 $b=1$, 则第 $2$ 行减第 $1$ 行得 $0=-1$, 矛盾.

若 $b=\frac{1}{2}$, 则第 $3$ 行减第 $1$ 行得 $0=-1$, 矛盾.

故 $a=1$ 且 $b\ne0$ 时, 无解.

综上:

- 唯一解: $b\ne0$ 且 $a\ne1$.

- 无穷多解: $b=0$. - 无解:

$a=1$ 且 $b\ne0$. $\blacksquare$

## 2.6-3

计算下述行列式:

$$
\left|\begin{array}{cccccc}
0&\cdots&0&a_{11}&\cdots&a_{1k}\\
\vdots&&\vdots&\vdots&&\vdots\\
0&\cdots&0&a_{k1}&\cdots&a_{kk}\\
b_{11}&\cdots&b_{1r}&c_{11}&\cdots&c_{1k}\\
\vdots&&\vdots&\vdots&&\vdots\\
b_{r1}&\cdots&b_{rr}&c_{r1}&\cdots&c_{rk}
\end{array}\right|.
$$

### 解答 2.6-3

由**定理 2.6.1 (拉普拉斯定理)**, 按前 $k$ 行展开. 前 $k$ 行的所有 $k$ 阶子式中, 只有右上角的 $k$ 阶子式 $A=\left(a_{ij}\right)_{k\times{}k}$ 可能不为零 (因为前 $k$ 行的前 $r$ 列全为 $0$).

右上角的 $k$ 阶子式 $A$ 的代数余子式: 行指标为 $1,2,\cdots,k$, 列指标为 $r+1,r+2,\cdots,r+k$.

由**定理 2.6.1 (拉普拉斯定理)**, 余子式是去掉前 $k$ 行和后 $k$ 列后的 $r$ 阶行列式, 即 $B=\left(b_{ij}\right)_{r\times{}r}$.

代数余子式为

$$
\left(-1\right)^{\left(1+2+\cdots+k\right)+\left(r+1+r+2+\cdots+r+k\right)}\cdot\left|B\right|
=\left(-1\right)^{\frac{k\left(k+1\right)}{2}+kr+\frac{k\left(k+1\right)}{2}}\cdot\left|B\right|
=\left(-1\right)^{k\left(k+1+r\right)}\cdot\left|B\right|.
$$

故行列式值为

$$
\left|A\right|\cdot\left(-1\right)^{k\left(k+1+r\right)}\cdot\left|B\right|
=\left(-1\right)^{k\left(r+k+1\right)}\left|A\right|\left|B\right|.
$$

$\blacksquare$
