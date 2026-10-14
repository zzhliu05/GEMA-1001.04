# Homework 3 参考答案

教材：《大学数学微积分 上册 第2版》
范围：第 2 章 12(6)(7)(8)、13(1)(3)、14、16(1)(4)、17(2)(4)、18(4)(5)、20(2)。

> 以下给出主要推导。数列极限存在性题按题意证明存在即可；若同时写出极限值，也一并注明。

## 第 12 题：计算数列极限

### (6)

求

$$
\lim_{n\to\infty}\frac{1^2+3^2+\cdots +(2n-1)^2}{n^3}.
$$

利用奇数平方和公式

$$
\sum_{k=1}^n(2k-1)^2=\frac{n(4n^2-1)}{3},
$$

可得

$$
\frac{1^2+3^2+\cdots +(2n-1)^2}{n^3}
=\frac{4n^3-n}{3n^3}
=\frac43-\frac{1}{3n^2}\longrightarrow\boxed{\frac43}.
$$

### (7)

$$
\prod_{k=2}^n\left(1-\frac1{k^2}\right)
=\prod_{k=2}^n\frac{(k-1)(k+1)}{k^2}
=\left(\prod_{k=2}^n\frac{k-1}{k}\right)
 \left(\prod_{k=2}^n\frac{k+1}{k}\right)
=\frac1n\cdot\frac{n+1}{2}.
$$

因此

$$
\lim_{n\to\infty}\prod_{k=2}^n\left(1-\frac1{k^2}\right)
=\boxed{\frac12}.
$$

### (8)

令 $x=1/2$。由恒等式

$$
\prod_{j=0}^{n}(1+x^{2^j})=\frac{1-x^{2^{n+1}}}{1-x}
$$

（将分子分母逐次使用 $1-y^2=(1-y)(1+y)$ 即得），题中乘积为

$$
\prod_{j=0}^{n}\left(1+\frac1{2^{2^j}}\right)
=\frac{1-(1/2)^{2^{n+1}}}{1-1/2}\longrightarrow\boxed{2}.
$$

## 第 13 题：利用夹逼定理

### (1)

题中和式有 $n+1$ 项，且每一项满足

$$
\frac1{(2n)^2}\leq\frac1{k^2}\leq\frac1{n^2}
\qquad(n\leq k\leq 2n).
$$

于是

$$
0\leq\sum_{k=n}^{2n}\frac1{k^2}
\leq\frac{n+1}{n^2}\longrightarrow0,
$$

故所求极限为 $\boxed{0}$。

### (3)

将双阶乘比写为乘积：

$$
\frac{(2n-1)!!}{(2n)!!}
=\prod_{k=1}^n\frac{2k-1}{2k}
=\prod_{k=1}^n\left(1-\frac1{2k}\right).
$$

利用 $\ln(1-t)\leq -t$（$0<t<1$），有

$$
0<\frac{(2n-1)!!}{(2n)!!}
\leq\exp\left(-\frac12\sum_{k=1}^n\frac1k\right).
$$

调和级数发散，故右端趋于 $0$。由夹逼定理，极限为 $\boxed{0}$。

## 第 14 题：幂和的 $n$ 次方根

设 $A=\max\{a_1,\ldots,a_m\}$，其中每个 $a_i>0$。因为至少有一个 $a_i=A$，且所有 $a_i\leq A$，所以

$$
A^n\leq a_1^n+\cdots+a_m^n\leq mA^n.
$$

取 $n$ 次方根：

$$
A\leq\sqrt[n]{a_1^n+\cdots+a_m^n}
\leq m^{1/n}A.
$$

由于 $m^{1/n}\to1$，夹逼得

$$
\boxed{\lim_{n\to\infty}\sqrt[n]{a_1^n+\cdots+a_m^n}=A}.
$$

## 第 16 题：证明数列极限存在

### (1)

$$
a_n=\sum_{k=1}^n\frac1{3^k+1}.
$$

每一项为正，因此 $\{a_n\}$ 单调递增。又因为

$$
0<a_n<\sum_{k=1}^n\frac1{3^k}
<\sum_{k=1}^{\infty}\frac1{3^k}=\frac12,
$$

故数列单调有界，极限存在。

### (4)

$$
a_n=1+\sum_{k=2}^n\frac1{k^2}.
$$

数列单调递增。对 $k\geq2$，有

$$
\frac1{k^2}<\frac1{k(k-1)}=\frac1{k-1}-\frac1k.
$$

故

$$
1\leq a_n<1+\sum_{k=2}^n\left(\frac1{k-1}-\frac1k\right)
=2-\frac1n<2.
$$

数列单调有界，极限存在。（事实上它是 $\sum_{k=1}^n1/k^2$，其极限为 $\pi^2/6$。）

\newpage

## 第 17 题：递归数列

### (2)

递推式为

$$
a_{n+1}=\frac12\left(a_n+\frac1{a_n}\right),\qquad a_1>0.
$$

对任意 $a_n>0$，由平方非负可知 $a_{n+1}\geq1$。并且

$$
a_{n+1}-a_n=\frac{1-a_n^2}{2a_n}.
$$

所以从 $a_2$ 起，$a_n\geq1$ 且数列单调不增；它下有界于 $1$，因此收敛。设极限为 $L$，对递推式取极限得

$$
L=\frac12\left(L+\frac1L\right),
$$

即 $L^2=1$。又 $L\geq1$，故 $\boxed{L=1}$。

### (4)

$$
a_1=1,\qquad a_{n+1}=1+\frac{a_n}{1+a_n}.
$$

令 $\varphi=(1+\sqrt5)/2$，则 $\varphi=1+\varphi/(1+\varphi)$。函数 $f(x)=1+x/(1+x)$ 在 $x>0$ 上递增。由 $a_1=1<\varphi$ 归纳得 $a_n<\varphi$。同时

$$
a_{n+1}-a_n=\frac{1+a_n-a_n^2}{1+a_n}>0,
$$

因为 $0<a_n<\varphi$ 且 $\varphi^2=\varphi+1$。所以 $\{a_n\}$ 单调递增且以上界 $\varphi$ 有界，极限存在。设为 $L$，取极限得

$$
L=1+\frac{L}{1+L},\qquad L^2-L-1=0.
$$

因 $L>0$，得到 $\boxed{L=(1+\sqrt5)/2}$。

## 第 18 题：用 $\varepsilon$-$\delta$ 定义证明

### (4)

证明 $\displaystyle\lim_{x\to3}\frac{x-3}{x}=0$。任给 $\varepsilon>0$，取

$$
\delta=\min\{1,2\varepsilon\}.
$$

若 $0<|x-3|<\delta$，则 $|x|>2$，从而

$$
\left|\frac{x-3}{x}-0\right|
=\frac{|x-3|}{|x|}
<\frac{|x-3|}{2}
<\frac{\delta}{2}\leq\varepsilon.
$$

故极限为 $0$。

### (5)

证明 $\displaystyle\lim_{x\to\pi/4}\sin x=\sqrt2/2$。利用恒等式及 $|\sin t|\leq|t|$，有

$$
\left|\sin x-\sin\frac\pi4\right|
=2\left|\sin\frac{x-\pi/4}{2}\right|
 \left|\cos\frac{x+\pi/4}{2}\right|
\leq |x-\pi/4|.
$$

任给 $\varepsilon>0$，取 $\delta=\varepsilon$。当 $0<|x-\pi/4|<\delta$ 时，上式小于 $\varepsilon$，故极限为 $\sin(\pi/4)=\boxed{\sqrt2/2}$。

## 第 20 题：单侧极限与双侧极限

### (2)

$$
f(x)=\begin{cases}
x+2,&x\leq2,\\[2pt]
\dfrac1{x-2},&x>2.
\end{cases}
$$

当 $x\to2^-$ 时，使用第一段表达式：

$$
\lim_{x\to2^-}f(x)=\lim_{x\to2^-}(x+2)=4.
$$

当 $x\to2^+$ 时，$x-2\to0^+$，因此

$$
\lim_{x\to2^+}f(x)=\lim_{x\to2^+}\frac1{x-2}=+\infty.
$$

右极限不是有限值，所以 $f$ 在 $x_0=2$ 处不存在有限的双侧极限。
