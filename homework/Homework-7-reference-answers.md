# Homework 7 参考答案

教材：《大学数学微积分 上册 第2版》，第 3 章习题 3，教材印刷页 144—149。范围：21(1)(2)、24(1)、30、37(2)、40、43(2)、53、57(1)、60(1)、62(2)。

## 21(1)(2)：反函数的导数

**(1)** $y=x+\ln x$，$x>0$。因 $dy/dx=1+1/x>0$，反函数存在。若 $x=F(y)$，则

$$
\boxed{F'(y)=\frac{1}{1+1/x}=\frac{x}{x+1},\quad x=F(y)>0.}
$$

**(2)** $y=2x-\cos(x/2)$。因 $dy/dx=2+\tfrac12\sin(x/2)>0$，反函数存在。若 $x=G(y)$，则

$$
\boxed{G'(y)=\frac{1}{2+\tfrac12\sin(x/2)},\quad x=G(y).}
$$

## 24(1)：对数求导

题设 $y=\dfrac{(x+1)^2\sqrt[3]{3x-2}}{\sqrt[3]{(x-3)^2}}$。在 $x\ne-1,\,2/3,\,3$ 处，

$$
\ln|y|=2\ln|x+1|+\frac13\ln|3x-2|-\frac23\ln|x-3|.
$$

故

$$
\boxed{y'=y\left(\frac{2}{x+1}+\frac{1}{3x-2}-\frac{2}{3(x-3)}\right).}
$$

$x=-1$ 时由原函数直接可得 $y'(-1)=0$；$x=2/3$ 处导数不存在，$x=3$ 不在定义域。

## 30：隐函数及复合函数

由 $xy+\ln y=1$（$y>0$）求导：

$$
y+xy'+\frac{y'}y=0,\qquad
\boxed{f'(x)=-\frac{y^2}{xy+1},\quad y=f(x).}
$$

在 $x=0$ 时 $f(0)=e$、$f'(0)=-e^2$；在 $x=1$ 时 $f(1)=1$、$f'(1)=-1/2$。对 $g(x)=f(\ln x)e^{f(x)}$ 求导得

$$
g'(x)=e^{f(x)}\left[\frac{f'(\ln x)}x+f(\ln x)f'(x)\right],
$$

因此 $\boxed{g'(1)=-e^3-\tfrac12e^2}$。

## 37(2)：极坐标曲线的切线与法线

$r=a\sin2\theta$，$a>0$。在 $\theta=\pi/4$，$r=a$、$r'=2a\cos2\theta=0$，对应点 $P=(a/\sqrt2,a/\sqrt2)$。由 $x=r\cos\theta$、$y=r\sin\theta$，

$$
\left.\frac{dy}{dx}\right|_P
=\left.\frac{r'\sin\theta+r\cos\theta}{r'\cos\theta-r\sin\theta}\right|_{\theta=\pi/4}=-1.
$$

故切线为 $\boxed{x+y=\sqrt2a}$，法线为 $\boxed{y=x}$。

## 40：漏斗与水桶

设漏斗内水深为 $h$，由相似三角形知水面半径 $r=h/3$，故水量

$$
V=\frac13\pi r^2h=\frac{\pi h^3}{27},\qquad
\frac{dV}{dt}=\frac{\pi h^2}{9}\frac{dh}{dt}.
$$

在 $h=12$ cm、$dh/dt=-1$ cm/s 时，$dV/dt=-16\pi$ cm³/s。水桶半径为 $5$ cm；若桶内水深为 $H$，体积守恒给出 $25\pi\,dH/dt=-dV/dt$。因此

$$
\boxed{\frac{dH}{dt}=\frac{16}{25}\ \mathrm{cm/s}.}
$$

## 43(2)：微分

设 $y=\dfrac{\arcsin x}{\arccos x}$，则利用 $\arcsin x+\arccos x=\pi/2$，

$$
\boxed{dy=\frac{\pi}{2\sqrt{1-x^2}(\arccos x)^2}\,dx}\qquad(-1<x<1).
$$

## 53：变量替换

原方程为 $y_{xx}-\dfrac{x}{1-x^2}y_x+\dfrac{y}{1-x^2}=0$。令 $x=\cos t$，在 $\sin t\ne0$ 的区间内，

$$
y_x=-\frac{y_t}{\sin t},\qquad
y_{xx}=\frac{y_{tt}}{\sin^2t}-\frac{\cos t}{\sin^3t}y_t.
$$

代入并约去 $y_t$ 项，得 $\boxed{y_{tt}+y=0}$。

## 57(1)：隐函数的二阶导数

对 $e^{x+y}=xy$ 求导。记 $E=e^{x+y}=xy$，则

$$
E(1+y')=y+xy',\qquad
y'=\frac{y-E}{E-x}=\frac{y(1-x)}{x(y-1)}.
$$

再求导，或用 $F(x,y)=e^{x+y}-xy=0$ 的二阶隐函数公式，得

$$
\boxed{y''=-\frac{E(1+(y')^2)+2(E-1)y'}{E-x},
\quad E=xy,\quad y'=\frac{y(1-x)}{x(y-1)}.}
$$

此式适用于 $E-x\ne0$ 的可微分支。

## 60(1)：参数方程的二阶导数

$x=a\cos^3t$、$y=a\sin^3t$。在 $dx/dt\ne0$ 处，

$$
\frac{dy}{dx}=\frac{3a\sin^2t\cos t}{-3a\cos^2t\sin t}=-\tan t,
$$

所以

$$
\boxed{\frac{d^2y}{dx^2}
=\frac{d(-\tan t)/dt}{dx/dt}
=\frac{1}{3a\sin t\cos^4t}.}
$$

## 62(2)：一百阶导数

$y=(x+1)^2e^{2x}$。由 Leibniz 公式，只有多项式的前两阶导数非零，故

$$
\begin{aligned}
y^{(100)}
&=e^{2x}\left[2^{100}(x+1)^2
+\binom{100}{1}2^{99}\cdot2(x+1)
+\binom{100}{2}2^{98}\cdot2\right]\\
&=\boxed{2^{100}e^{2x}\left[(x+1)^2+100(x+1)+2475\right]}.
\end{aligned}
$$
