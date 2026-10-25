# Assignment 3

> **Definition 1** (Number Field)<br>Let $K$ be a subset of the set of complex numbers. If $K$ satisfies:
> (1) $0,1\in K$;
> 
> (2) it is closed under the four operations of addition, subtraction, multiplication, and division (the divisor being not $0$),
> then $K$ is called a number field.

### Problem 1

(Problem 1.3-1) Let

$$
\mathbb Q\left(i\right)=\left\{a+bi\mid a,b\in\mathbb Q\right\},
$$

Prove that $\mathbb Q\left(i\right)$ is a number field.

### Solution to Problem 1

According to the requirements of **Definition 1** (Number Field), we need to verify that $\mathbb Q\left(i\right)$ satisfies $0,1\in K$ and is closed under the four operations of addition, subtraction, multiplication, and division.

**Verify $0,1\in\mathbb Q\left(i\right)$**. By item (1) of **Definition 1**, clearly $0=0+0\cdot i\in\mathbb Q\left(i\right)$ and $1=1+0\cdot i\in\mathbb Q\left(i\right)$.

**Verify closure under addition**. By item (2) of **Definition 1**, take any

$$
\alpha=a+bi,\beta=c+di\in\mathbb Q\left(i\right),
$$

where $a,b,c,d\in\mathbb Q$; then

$$
\alpha+\beta=\left(a+c\right)+\left(b+d\right)i.
$$

Since the rational numbers are closed under addition, $a+c\in\mathbb Q$ and $b+d\in\mathbb Q$, hence $\alpha+\beta\in\mathbb Q\left(i\right)$.

**Verify closure under subtraction**. By item (2) of **Definition 1**, similarly,

$$
\alpha-\beta=\left(a-c\right)+\left(b-d\right)i,
$$

and $a-c\in\mathbb Q$, $b-d\in\mathbb Q$, hence $\alpha-\beta\in\mathbb Q\left(i\right)$.

**Verify closure under multiplication**. By item (2) of **Definition 1**,

$$
\begin{aligned}\alpha\beta&=\left(a+bi\right)\left(c+di\right)\\
&=\left(ac-bd\right)+\left(ad+bc\right)i.
\end{aligned}
$$

Since the rational numbers are closed under addition, subtraction, and multiplication, $ac-bd\in\mathbb Q$ and $ad+bc\in\mathbb Q$, hence $\alpha\beta\in\mathbb Q\left(i\right)$.

**Verify closure under division**. By item (2) of **Definition 1**, let $\beta=c+di\ne 0$; then $c^{2}+d^{2}\ne 0$, and

$$
\begin{aligned}\frac{\alpha}{\beta}&=\frac{a+bi}{c+di}\\
&=\frac{\left(a+bi\right)\left(c-di\right)}{\left(c+di\right)\left(c-di\right)}\\
&=\frac{ac+bd}{c^{2}+d^{2}}+\frac{bc-ad}{c^{2}+d^{2}}i.
\end{aligned}
$$

Since the rational numbers are closed under addition, subtraction, multiplication, and division (the divisor being not $0$), $\frac{ac+bd}{c^{2}+d^{2}}\in\mathbb Q$ and $\frac{bc-ad}{c^{2}+d^{2}}\in\mathbb Q$, hence $\frac{\alpha}{\beta}\in\mathbb Q\left(i\right)$.

In summary, $\mathbb Q\left(i\right)$ satisfies all the conditions of **Definition 1** (Number Field), so $\mathbb Q\left(i\right)$ is a number field. $\blacksquare$
