# week3

> **Basic Knowledge: Closure of the Rational Field under the Four Arithmetic Operations**<br>The set $\mathbb Q$ of rational numbers is closed under addition, subtraction, multiplication, and division (with nonzero divisor); that is, the sum, difference, product, and quotient (with nonzero divisor) of two rational numbers are still rational numbers.

> **Definition 1.3.1 (Number Field)**<br>Let $K$ be a subset of the set of complex numbers. If $K$ satisfies: (1) $0,1\in K$; (2) it is closed under addition, subtraction, multiplication, and division (with nonzero divisor), then $K$ is called a number field.

---

## 1.3-1

Let

$$
\mathbb Q\left(i\right)=\left\{a+bi\mid a,b\in\mathbb Q\right\},
$$

and prove that $\mathbb Q\left(i\right)$ is a number field.

### Solution 1.3-1

By the requirements of **Definition 1.3.1 (Number Field)**, we must verify that $\mathbb Q\left(i\right)$ satisfies $0,1\in K$ and is closed under addition, subtraction, multiplication, and division.

**Verify $0,1\in\mathbb Q\left(i\right)$**. By condition (1) of **Definition 1.3.1 (Number Field)**, clearly $0=0+0\cdot i\in\mathbb Q\left(i\right)$ and $1=1+0\cdot i\in\mathbb Q\left(i\right)$.

**Verify closure under addition**. By condition (2) of **Definition 1.3.1 (Number Field)**, take any

$$
\alpha=a+bi,\beta=c+di\in\mathbb Q\left(i\right),
$$

where $a,b,c,d\in\mathbb Q$; then

$$
\alpha+\beta=\left(a+c\right)+\left(b+d\right)i.
$$

Since the rationals are closed under addition (**Basic Knowledge: Closure of the Rational Field under the Four Arithmetic Operations**), $a+c\in\mathbb Q$ and $b+d\in\mathbb Q$, so $\alpha+\beta\in\mathbb Q\left(i\right)$.

**Verify closure under subtraction**. By condition (2) of **Definition 1.3.1 (Number Field)**, similarly,

$$
\alpha-\beta=\left(a-c\right)+\left(b-d\right)i,
$$

and $a-c\in\mathbb Q$, $b-d\in\mathbb Q$ (**Basic Knowledge: Closure of the Rational Field under the Four Arithmetic Operations**), so $\alpha-\beta\in\mathbb Q\left(i\right)$.

**Verify closure under multiplication**. By condition (2) of **Definition 1.3.1 (Number Field)**,

$$
\alpha\beta=\left(a+bi\right)\left(c+di\right)=\left(ac-bd\right)+\left(ad+bc\right)i.
$$

Since the rationals are closed under addition, subtraction, and multiplication (**Basic Knowledge: Closure of the Rational Field under the Four Arithmetic Operations**), $ac-bd\in\mathbb Q$ and $ad+bc\in\mathbb Q$, so $\alpha\beta\in\mathbb Q\left(i\right)$.

**Verify closure under division**. By condition (2) of **Definition 1.3.1 (Number Field)**, let $\beta=c+di\ne 0$; then $c^{2}+d^{2}\ne 0$, and

$$
\frac{\alpha}{\beta}=\frac{a+bi}{c+di}=\frac{\left(a+bi\right)\left(c-di\right)}{\left(c+di\right)\left(c-di\right)}=\frac{ac+bd}{c^{2}+d^{2}}+\frac{bc-ad}{c^{2}+d^{2}}i.
$$

Since the rationals are closed under addition, subtraction, multiplication, and division (with nonzero divisor) (**Basic Knowledge: Closure of the Rational Field under the Four Arithmetic Operations**), $\frac{ac+bd}{c^{2}+d^{2}}\in\mathbb Q$ and $\frac{bc-ad}{c^{2}+d^{2}}\in\mathbb Q$, so $\frac{\alpha}{\beta}\in\mathbb Q\left(i\right)$.

In summary, $\mathbb Q\left(i\right)$ satisfies all conditions of **Definition 1.3.1 (Number Field)**, so $\mathbb Q\left(i\right)$ is a number field. $\blacksquare$
