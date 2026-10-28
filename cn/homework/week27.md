# week27

> **定义 5.3.1 (广义逆)**<br>设 $A$ 是数域 $K$ 上 $s\times n$ 矩阵. 如果矩阵 $G$ 满足 $AGA=A$, 则称 $G$ 是 $A$ 的一个广义逆, 记作 $A^{-}$.

> **定理 5.3.1 (广义逆的存在性)**<br>设 $A$ 是数域 $K$ 上 $s\times n$ 非零矩阵, 则矩阵方程 $AXA=A$ 一定有解.

---

## 5.3-1

设 $A$ 是数域 $K$ 上 $s\times n$ 矩阵. 证明: 如果 $A$ 行满秩, 则对于 $A$ 的任意一个广义逆 $A^{-}$, 都有 $AA^{-}=I_{s}$.

### 解答 5.3-1

由**定义 5.3.1 (广义逆)**, $A^{-}$ 是 $A$ 的广义逆, 即 $AA^{-}A=A$. 设 $A$ 行满秩, 即 $\operatorname{rank}\left(A\right)=s$.

令 $B=AA^{-}$. 则 $B$ 是 $s\times s$ 矩阵.

由 $AA^{-}A=A$, 两边右乘 $A^{-}$:

$$
\left(AA^{-}A\right)A^{-}=AA^{-}.
$$

即

$$
AA^{-}\left(AA^{-}\right)=AA^{-}.
$$

因此

$$
BB=B,
$$

即 $B$ 是幂等矩阵.

**求 $B$ 的秩**.

因为 $A$ 行满秩, $\operatorname{rank}\left(A\right)=s$.

又因为 $AA^{-}A=A$, 故

$$
\operatorname{rank}\left(A\right)=\operatorname{rank}\left(AA^{-}A\right)\le\operatorname{rank}\left(AA^{-}\right)\le\operatorname{rank}\left(A\right).
$$

因此

$$
\operatorname{rank}\left(B\right)=\operatorname{rank}\left(AA^{-}\right)=\operatorname{rank}\left(A\right)=s.
$$

所以 $B$ 是 $s\times s$ 矩阵, 且 $\operatorname{rank}\left(B\right)=s$, 即 $B$ 可逆.

由 $BB=B$, 两边左乘 $B^{-1}$:

$$
B=I_{s}.
$$

因此, 由**定义 5.3.1 (广义逆)**, 对于 $A$ 的任意一个广义逆 $A^{-}$, 都有

$$
AA^{-}=I_{s}.
$$

$\blacksquare$
