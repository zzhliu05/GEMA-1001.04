# Homework 4 参考答案

教材：《大学数学微积分 上册 第2版》
范围：第 2 章 33(7)、37、39(2)、40、46；第 3 章 3(2)(3)。

## 第 2 章

### 第 33 题 (7)

函数 $y=[x]$（取不超过 $x$ 的最大整数）在每个整数 $k\in\mathbb Z$ 处不连续。其左、右极限分别为

$$
\lim_{x\to k^-}[x]=k-1,\qquad \lim_{x\to k^+}[x]=k.
$$

两侧极限均存在但不相等，因此每个整数点都是第一类跳跃间断点。由于左右极限不相等，仅改变 $f(k)$ 的值不能使函数在 $k$ 处连续，故这些间断点都不可去。

### 第 37 题

#### (1)

$$
f(x)=\begin{cases}
\dfrac{\sin ax}{x},&x<0,\\
1,&x=0,\\
\dfrac{b(\sqrt{1+x}-1)}{x},&x>0.
\end{cases}
$$

在 $x=0$ 连续要求左右极限都等于 $f(0)=1$。有

$$
\lim_{x\to0^-}\frac{\sin ax}{x}=a,\qquad
\lim_{x\to0^+}\frac{b(\sqrt{1+x}-1)}{x}
=\lim_{x\to0^+}\frac{b}{\sqrt{1+x}+1}=\frac b2.
$$

故 $a=1$ 且 $b=2$。

#### (2)

$$
f(x)=\lim_{n\to\infty}\frac{x^{2n-1}+ax^2+bx}{x^{2n}+1}.
$$

逐点计算得

$$
f(x)=\begin{cases}
ax^2+bx,&|x|<1,\\[2pt]
\dfrac{1+a+b}{2},&x=1,\\[4pt]
\dfrac{-1+a-b}{2},&x=-1,\\[4pt]
\dfrac1x,&|x|>1.
\end{cases}
$$

在 $x=1$ 连续要求 $a+b=1$；在 $x=-1$ 连续要求 $a-b=-1$。解得

$$
a=0,\qquad b=1.
$$

此时 $f(x)=x$（$|x|\leq1$），$f(x)=1/x$（$|x|>1$），在 $x=\pm1$ 的函数值与左右极限分别相等，故 $f$ 连续。

### 第 39 题 (2)

令

$$
g(x)=x-a\sin x-b.
$$

则 $g(0)=-b<0$，且

$$
g(a+b)=a\bigl(1-\sin(a+b)\bigr)\geq0.
$$

由介值定理，存在 $\xi\in(0,a+b]$ 使 $g(\xi)=0$，即

$$
\xi=a\sin\xi+b.
$$

因此至少有一个正根，且该正根不超过 $a+b$。

### 第 40 题

令 $g(x)=f(x)-x$。由 $0<f(x)<1$（$0\leq x\leq1$），得

$$
g(0)=f(0)>0,\qquad g(1)=f(1)-1<0.
$$

函数 $g$ 在 $[0,1]$ 上连续，故由介值定理，存在 $\xi\in(0,1)$ 使 $g(\xi)=0$，即 $f(\xi)=\xi$。

### 第 46 题

题目印出的条件是 $\lim_{x\to+\infty}f(x)=+\infty$，单凭此条件结论不成立。例如 $f(x)=e^x$ 满足该条件，但在 $\mathbb R$ 上不取到最小值。

若题意为 $\lim_{x\to\pm\infty}f(x)=+\infty$，则取 $R>0$ 充分大，使 $|x|>R$ 时 $f(x)>f(0)$。连续函数 $f$ 在紧区间 $[-R,R]$ 上取得最小值，设在 $x=\xi$ 处取得。因 $0\in[-R,R]$，有 $f(\xi)\leq f(0)$；而区间外 $f(x)>f(0)\geq f(\xi)$。故 $f(\xi)$ 即为 $f$ 在 $\mathbb R$ 上的最小值。

## 第 3 章

### 第 3 题

设 $f$ 在 $x_0$ 处可导。

#### (2)

令 $h=-\Delta x$，则

$$
\lim_{\Delta x\to0}\frac{f(x_0-\Delta x)-f(x_0)}{\Delta x}
=-\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}
=\boxed{-f'(x_0)}.
$$

#### (3)

$$
\begin{aligned}
\lim_{h\to0}\frac{f(x_0+h)-f(x_0-h)}{h}
&=\lim_{h\to0}\left[
\frac{f(x_0+h)-f(x_0)}{h}
+\frac{f(x_0)-f(x_0-h)}{h}\right]\\
&=f'(x_0)+f'(x_0)\\
&=\boxed{2f'(x_0)}.
\end{aligned}
$$
