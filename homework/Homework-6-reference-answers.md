# Homework 6 参考答案

教材：《大学数学微积分 上册 第2版》
范围：第 3 章 4(3)、8、13、17、19(1)(2)(9)、22(10)(11)、24(4)。

## 第 3 章

### 第 4 题 (3)

$$
y=\cos(ax+b)
\quad\Longrightarrow\quad
\boxed{y'=-a\sin(ax+b)}.
$$

### 第 8 题

#### (1) 可导偶函数的导函数为奇函数

由 $f(-x)=f(x)$ 两边对 $x$ 求导，得

$$
-f'(-x)=f'(x),
$$

故 $f'(-x)=-f'(x)$，所以 $f'$ 是奇函数。

#### (2) 可导奇函数的导函数为偶函数

由 $f(-x)=-f(x)$ 两边对 $x$ 求导，得

$$
-f'(-x)=-f'(x),
$$

故 $f'(-x)=f'(x)$，所以 $f'$ 是偶函数。

### 第 13 题

设双曲线 $xy=a^2$ 上任一点为 $P(u,v)$，则 $uv=a^2$。对方程隐式求导：

$$
y+xy'=0,
\qquad y'(u,v)=-\frac vu.
$$

因此 $P$ 点切线为

$$
y-v=-\frac vu(x-u).
$$

令 $y=0$，得横截距 $x=2u$；令 $x=0$，得纵截距 $y=2v$。切线与两坐标轴围成的三角形面积为

$$
S=\frac12|2u\cdot2v|=2|uv|=\boxed{2a^2},
$$

为常数。

### 第 17 题

$$
f(x)=\begin{cases}
x^2,&x\leq x_0,\\
ax+b,&x>x_0.
\end{cases}
$$

在 $x_0$ 连续要求

$$
ax_0+b=x_0^2.
$$

左右导数分别为 $2x_0$ 与 $a$。可导要求 $a=2x_0$，代入连续条件得 $b=-x_0^2$。所以

$$
\boxed{a=2x_0,\qquad b=-x_0^2}.
$$

### 第 19 题

#### (1) $y=a^x x^a$

其中 $a>0$ 为常数，且 $x>0$。对数求导：$\ln y=x\ln a+a\ln x$，因此

$$
\boxed{y'=a^x x^a\left(\ln a+\frac{a}{x}\right)}\qquad(x>0).
$$

#### (2) $y=x\sin x\ln x$

用乘积法则：

$$
\boxed{y'=\sin x\ln x+x\cos x\ln x+\sin x}\qquad(x>0).
$$

#### (9) $\displaystyle y=x\sec x+\frac{\arctan x}{e^x}$

写成 $y=x\sec x+e^{-x}\arctan x$，则

$$
\boxed{y'=\sec x+x\sec x\tan x
+e^{-x}\left(\frac1{1+x^2}-\arctan x\right)}.
$$

### 第 22 题

#### (10)

$$
y=\cos^2\left(\frac{1-\sqrt{x}}{1+\sqrt{x}}\right).
$$

令 $u=(1-\sqrt{x})/(1+\sqrt{x})$，则

$$
u'=-\frac1{\sqrt{x}(1+\sqrt{x})^2}.
$$

由链式法则，

$$
\boxed{y'=-\sin(2u)u'
=\frac{\sin\!\left(2\dfrac{1-\sqrt{x}}{1+\sqrt{x}}\right)}
{\sqrt{x}(1+\sqrt{x})^2}}\qquad(x>0).
$$

#### (11)

$$
y=\sin\bigl(\sin(\sin 2x)\bigr).
$$

连续使用链式法则：

$$
\boxed{y'=2\cos\bigl(\sin(\sin 2x)\bigr)
\cos(\sin 2x)\cos 2x}.
$$

### 第 24 题 (4)

$$
y=\left(\frac{x}{1+x}\right)^x\qquad(x>0).
$$

取对数：$\ln y=x\ln\frac{x}{1+x}$。于是

$$
\frac{y'}y=\ln\frac{x}{1+x}
+x\left(\frac1x-\frac1{1+x}\right)
=\ln\frac{x}{1+x}+\frac1{1+x}.
$$

故

$$
\boxed{y'=\left(\frac{x}{1+x}\right)^x
\left(\ln\frac{x}{1+x}+\frac1{1+x}\right)}.
$$
