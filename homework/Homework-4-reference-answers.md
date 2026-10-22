# Homework 4 参考答案

教材：《大学数学微积分 上册 第2版》

范围：第 2 章 33(7)、37、39(2)、40、46；第 3 章 3(2)(3)。

## 第 2 章

### 第 33 题 (7)

函数为 $y=\lfloor x\rfloor$。

若 $x\notin\mathbb Z$，则 $x$ 的某个邻域内 $\lfloor x\rfloor$ 为常数，故函数在这些点连续。

对任意整数 $m$，

$$
\lim_{x\to m^-}\lfloor x\rfloor=m-1,
\qquad
\lim_{x\to m^+}\lfloor x\rfloor=m,
\qquad
\lfloor m\rfloor=m.
$$

左右极限均存在但不相等，因此每个整数点都是第一类跳跃间断点，跳跃量为 $1$。改变整数点处函数值不能使左右极限相等，故这些间断点均不能通过补定义或改值去掉。

### 第 37 题

#### (1)

$$
f(x)=
\begin{cases}
\dfrac{\sin(ax)}{x},&x<0,\\[4pt]
1,&x=0,\\[4pt]
\dfrac{b(\sqrt{1+x}-1)}{x},&x>0.
\end{cases}
$$

连续性要求左右极限都等于 $f(0)=1$。左极限为

$$
\lim_{x\to0^-}\frac{\sin(ax)}x=a,
$$

右极限有理化得

$$
\lim_{x\to0^+}\frac{b(\sqrt{1+x}-1)}x
=\lim_{x\to0^+}\frac{b}{\sqrt{1+x}+1}=\frac b2.
$$

故 $a=1$ 且 $b=2$。

#### (2)

$$
f(x)=\lim_{n\to\infty}
\frac{x^{2n-1}+ax^2+bx}{x^{2n}+1}.
$$

逐区间求出 $f$：

$$
f(x)=
\begin{cases}
ax^2+bx,&|x|<1,\\[2pt]
\dfrac{1+a+b}{2},&x=1,\\[4pt]
\dfrac{-1+a-b}{2},&x=-1,\\[4pt]
\dfrac1x,&|x|>1.
\end{cases}
$$

在 $x=1$ 连续要求 $a+b=1$；在 $x=-1$ 连续要求 $a-b=-1$。解得

$$
\boxed{a=0,\qquad b=1}.
$$

这时 $f(x)=x$（$|x|\le1$），$f(x)=1/x$（$|x|>1$），在 $x=\pm1$ 处也连续。

### 第 39 题 (2)

证明方程

$$
x=a\sin x+b\qquad(0<a<1,\ b>0)
$$

至少有一正根，且不超过 $a+b$。

令 $F(x)=x-a\sin x-b$。$F$ 在 $[0,a+b]$ 上连续，并且

$$
F(0)=-b<0,
\qquad
F(a+b)=a\bigl(1-\sin(a+b)\bigr)\ge0.
$$

由介值定理，存在 $\xi\in(0,a+b]$ 使 $F(\xi)=0$。因此 $\xi$ 是方程的正根，且 $\xi\le a+b$。

### 第 40 题

设 $f\in C[0,1]$ 且 $0<f(x)<1$。令 $g(x)=f(x)-x$，则 $g$ 在 $[0,1]$ 上连续，且

$$
g(0)=f(0)>0,\qquad g(1)=f(1)-1<0.
$$

由介值定理，存在 $\xi\in(0,1)$ 使 $g(\xi)=0$，即 $f(\xi)=\xi$。

\newpage

### 第 46 题

教材扫描件给出的条件是仅有

$$
f\in C(\mathbb R),\qquad \lim_{x\to+\infty}f(x)=+\infty.
$$

按此条件结论不成立：取 $f(x)=e^x$，则满足条件，但在 $\mathbb R$ 上不取到最小值。

若原题意为

$$
f\in C(\mathbb R),\qquad \lim_{|x|\to\infty}f(x)=+\infty,
$$

则可证明结论如下。取 $R>0$，使得 $|x|>R$ 时 $f(x)>f(0)$。由 $f$ 在紧区间 $[-R,R]$ 上连续，存在 $x_0\in[-R,R]$ 使

$$
f(x_0)=\min_{x\in[-R,R]}f(x)\le f(0).
$$

而区间外 $f(x)>f(0)\ge f(x_0)$，所以 $f(x_0)=\min_{x\in\mathbb R}f(x)$。

## 第 3 章

### 第 3 题 (2)

设 $f$ 在 $x_0$ 处可导。令 $h=-\Delta x$，则

$$
\begin{aligned}
\lim_{\Delta x\to0}
\frac{f(x_0-\Delta x)-f(x_0)}{\Delta x}
&=-\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}h\\
&=\boxed{-f'(x_0)}.
\end{aligned}
$$

### 第 3 题 (3)

$$
\begin{aligned}
\lim_{h\to0}\frac{f(x_0+h)-f(x_0-h)}h
&=\lim_{h\to0}\left[
\frac{f(x_0+h)-f(x_0)}h+
\frac{f(x_0)-f(x_0-h)}h\right]\\
&=f'(x_0)+f'(x_0)\\
&=\boxed{2f'(x_0)}.
\end{aligned}
$$
