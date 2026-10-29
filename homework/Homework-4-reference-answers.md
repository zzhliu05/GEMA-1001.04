# Homework 4 参考答案

教材：《大学数学微积分 上册 第2版》
范围：第 2 章 22、24、25(4)(5)(11)、26(3)(8)、27(3)(5)、28(2)(8)、30(2)(4)。

## 第 2 章

### 第 22 题

设 $\lim_{x\to x_0}f(x)=A$，其中 $A>0$。任给 $\varepsilon>0$，取

$$
\delta=\min\left\{\frac A2,\,\varepsilon\sqrt A\right\}.
$$

当 $0<|x-x_0|<\delta$ 时，$|f(x)-A|<\delta\leq A/2$，所以 $f(x)>A/2>0$，且

$$
\left|\sqrt{f(x)}-\sqrt A\right|
=\frac{|f(x)-A|}{\sqrt{f(x)}+\sqrt A}
<\frac{|f(x)-A|}{\sqrt A}
<\varepsilon.
$$

故 $\displaystyle\lim_{x\to x_0}\sqrt{f(x)}=\sqrt A$。

### 第 24 题

函数 $f(x)=\dfrac1x\cos\dfrac1x$ 在任意去心邻域内无界。取

$$
x_n=\frac1{2\pi n},\qquad y_n=\frac1{(2n+1)\pi},
$$

则 $x_n,y_n\to0$，并且

$$
f(x_n)=2\pi n\to+\infty,\qquad
f(y_n)=-(2n+1)\pi\to-\infty.
$$

因此任意邻域内函数值均无界；同时沿趋于 $0$ 的数列，函数值分别趋于正无穷和负无穷，所以 $x\to0$ 时 $f(x)$ 既不趋于 $+\infty$，也不趋于 $-\infty$。

### 第 25 题

#### (4)

$$
\lim_{x\to\infty}\frac{(2x-3)^{20}(3x+2)^{30}}{(5x+1)^{50}}
=\frac{2^{20}3^{30}}{5^{50}}.
$$

#### (5)

$$
\lim_{x\to0}\frac{\sqrt{1+x}-1}{x}
=\lim_{x\to0}\frac{1}{\sqrt{1+x}+1}
=\boxed{\frac12}.
$$

#### (11)

令 $P(x)=x+x^2+\cdots+x^n-n$，则 $P(1)=0$，故

$$
\lim_{x\to1}\frac{x+x^2+\cdots+x^n-n}{x-1}
=P'(1)=1+2+\cdots+n
=\boxed{\frac{n(n+1)}2}.
$$

### 第 26 题

#### (3)

由导数定义，

$$
\lim_{x\to a}\frac{\sin x-\sin a}{x-a}
=(\sin x)'\big|_{x=a}
=\boxed{\cos a}.
$$

#### (8)

利用和差化积公式，

$$
\frac{\sqrt3}{2}-\cos x
=2\sin\left(\frac{x+\pi/6}{2}\right)
  \sin\left(\frac{x-\pi/6}{2}\right),
\qquad
\sin(x-\pi/6)
=2\sin\left(\frac{x-\pi/6}{2}\right)
  \cos\left(\frac{x-\pi/6}{2}\right).
$$

因此，当 $x\ne\pi/6$ 时，

$$
=\frac{\sin(x-\pi/6)}{\sqrt3/2-\cos x}
=\frac{\cos\left((x-\pi/6)/2\right)}
       {\sin\left((x+\pi/6)/2\right)}.
$$

故

$$
\lim_{x\to\pi/6}\frac{\sin(x-\pi/6)}{\sqrt3/2-\cos x}
=\frac{1}{\sin(\pi/6)}
=\boxed{2}.
$$

### 第 27 题

#### (3)

令 $L=\displaystyle\lim_{x\to0}(1+x^2)^{1/(1-\cos x)}$。取对数，

$$
\ln L=\lim_{x\to0}\frac{\ln(1+x^2)}{1-\cos x}
=\lim_{x\to0}\frac{x^2}{x^2/2}=2.
$$

故 $\boxed{L=e^2}$。

#### (5)

令 $L=\displaystyle\lim_{x\to0}(1+\tan x)^{\cot x}$。取对数，

$$
\ln L=\lim_{x\to0}\frac{\ln(1+\tan x)}{\tan x}
\cdot\cot x\tan x=1.
$$

故 $\boxed{L=e}$。

### 第 28 题

#### (2)

当 $x\to0^+$ 时，

$$
\sqrt[3]{x^2}-\sqrt x
=x^{2/3}-x^{1/2}
=x^{1/2}(x^{1/6}-1)\sim-\sqrt x.
$$

所以该无穷小关于 $x$ 的阶数为 $\boxed{1/2}$，主部为 $\boxed{-\sqrt x}$。

#### (8)

当 $x\to0$ 时，

$$
(\cos x)^x-1
=\exp(x\ln\cos x)-1.
$$

因为 $\ln\cos x\sim-x^2/2$，且 $e^u-1\sim u$（$u\to0$），所以

$$
(\cos x)^x-1\sim-\frac{x^3}{2}.
$$

所以该无穷小关于 $x$ 的阶数为 $\boxed{3}$，主部为 $\boxed{-x^3/2}$。

### 第 30 题

#### (2)

$$
\lim_{x\to0}\frac{1-\cos x}{(e^x-1)\ln(1+x)}
=\lim_{x\to0}\frac{x^2/2}{x\cdot x}
=\boxed{\frac12}.
$$

#### (4)

将分子、分母分别化简：

$$
\begin{aligned}
\ln(\sin^2x+e^x)-x
&=\ln\left(1+e^{-x}\sin^2x\right)\sim x^2,\\
\ln(e^{2x}-x^2)-2x
&=\ln\left(1-x^2e^{-2x}\right)\sim-x^2.
\end{aligned}
$$

因此

$$
\lim_{x\to0}\frac{\ln(\sin^2x+e^x)-x}{\ln(e^{2x}-x^2)-2x}
=\boxed{-1}.
$$
