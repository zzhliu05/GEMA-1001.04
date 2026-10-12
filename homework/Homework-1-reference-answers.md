# Homework 1 参考答案

课程：Gradescope 1391123  
作业：Homework 1（assignment 8661120）  
教材：《大学数学微积分 上册 第2版》，习题 1，第 31--35 页

> 本文是供助教核对的参考解答。等价推导、等价区间写法和合理省略步骤均可接受。

## Question 1：习题 1，第 2 题

已知

$$
A=\{x\mid x^2\le 1\},\qquad B=\{x\mid |x-1|<1\}.
$$

先化为区间：

$$
A=[-1,1],\qquad B=(0,2).
$$

所以

$$
\boxed{A\cup B=[-1,2)},
$$

$$
\boxed{A\cap B=(0,1]},
$$

$$
\boxed{A-B=[-1,0]},
$$

$$
\boxed{B-A=(1,2)}.
$$

## Question 2：习题 1，第 4 题 (1)(2)

### (1)

$$
E=\left\{1,\frac12,\frac13,\ldots,\frac1n,\ldots\right\}.
$$

对任意 $n\in\mathbb N_+$，有 $0<1/n\le 1$，而且 $1\in E$，故

$$
\boxed{\sup E=1}.
$$

数 $0$ 是 $E$ 的下界。对任意 $\varepsilon>0$，取正整数 $n>1/\varepsilon$，则

$$
0<\frac1n<\varepsilon.
$$

因此不存在大于 $0$ 的下界，故

$$
\boxed{\inf E=0}.
$$

### (2)

$$
E=\{x\in\mathbb Q\mid x^2<9\}=(-3,3)\cap\mathbb Q.
$$

显然 $-3<x<3$，所以 $3$ 是上界，$-3$ 是下界。利用有理数在实数中的稠密性，对任意 $\varepsilon>0$，都能分别在 $(3-\varepsilon,3)$ 和 $(-3,-3+\varepsilon)$ 中取到有理数。因此

$$
\boxed{\sup E=3,\qquad \inf E=-3}.
$$

## Question 3：习题 1，第 5 题 (2)(3)

### (2) 证明 $|\sin nx|\le n|\sin x|$

对 $n$ 作归纳。$n=1$ 时结论显然成立。假设

$$
|\sin nx|\le n|\sin x|.
$$

则

$$
\begin{aligned}
|\sin((n+1)x)|
&=|\sin nx\cos x+\cos nx\sin x|\\
&\le |\sin nx|\,|\cos x|+|\cos nx|\,|\sin x|\\
&\le |\sin nx|+|\sin x|\\
&\le (n+1)|\sin x|.
\end{aligned}
$$

所以对所有 $n\in\mathbb N_+$ 都有

$$
\boxed{|\sin nx|\le n|\sin x|}.
$$

若教材约定 $0\in\mathbb N$，则 $n=0$ 时两边均为 $0$，结论同样成立。

### (3) 证明 Bernoulli 不等式

要证：当 $x>-1$、$x\ne0$、$n\ge2$ 时，

$$
(1+x)^n>1+nx.
$$

$n=2$ 时，

$$
(1+x)^2-(1+2x)=x^2>0.
$$

假设对某个 $n\ge2$ 有 $(1+x)^n>1+nx$。因为 $1+x>0$，所以

$$
\begin{aligned}
(1+x)^{n+1}
&>(1+x)(1+nx)\\
&=1+(n+1)x+nx^2\\
&>1+(n+1)x.
\end{aligned}
$$

由数学归纳法，

$$
\boxed{(1+x)^n>1+nx\quad(x>-1,\ x\ne0,\ n\ge2)}.
$$

## Question 4：习题 1，第 9 题 (2)(3)

已知 $D_f=[0,1]$。

### (2) $f(\sin x)$ 的定义域

要求 $0\le\sin x\le1$。由于 $\sin x\le1$ 恒成立，只需 $\sin x\ge0$，故

$$
\boxed{D_{f(\sin x)}=\bigcup_{k\in\mathbb Z}[2k\pi,(2k+1)\pi]}.
$$

### (3) $f(x+a)$ 的定义域

要求 $0\le x+a\le1$，所以

$$
\boxed{D_{f(x+a)}=[-a,1-a]}.
$$

## Question 5：习题 1，第 14 题 (3)

已知

$$
f\!\left(\sin\frac x2\right)=1+\cos x.
$$

利用 $\cos x=1-2\sin^2(x/2)$，得

$$
f\!\left(\sin\frac x2\right)=2-2\sin^2\frac x2.
$$

由于 $\sin(x/2)$ 可取遍 $[-1,1]$，所以对 $t\in[-1,1]$，

$$
f(t)=2-2t^2.
$$

又因为 $\cos(x/2)\in[-1,1]$，于是

$$
\begin{aligned}
f\!\left(\cos\frac x2\right)
&=2-2\cos^2\frac x2\\
&=1-\cos x\\
&=2\sin^2\frac x2.
\end{aligned}
$$

因此

$$
\boxed{f\!\left(\cos\frac x2\right)=1-\cos x=2\sin^2\frac x2}.
$$

## Question 6：习题 1，第 15 题 (3)

已知

$$
f(x)=
\begin{cases}
2x,&0\le x\le1,\\
x^2,&1<x\le2,
\end{cases}
\qquad g(x)=\ln x.
$$

### $f\circ g$

必须有 $\ln x\in[0,2]$，即 $x\in[1,e^2]$。因此

$$
\boxed{
f(g(x))=
\begin{cases}
2\ln x,&1\le x\le e,\\
(\ln x)^2,&e<x\le e^2.
\end{cases}}
$$

### $g\circ f$

必须有 $x\in[0,2]$ 且 $f(x)>0$，故定义域为 $(0,2]$。因此

$$
\boxed{
g(f(x))=
\begin{cases}
\ln(2x),&0<x\le1,\\
\ln(x^2)=2\ln x,&1<x\le2.
\end{cases}}
$$

## Question 7：习题 1，第 16 题

设 $f$ 为奇函数，$g$ 为偶函数，并假定相应复合函数的定义域关于原点对称。

### (1) $f(g(x))$

$$
f(g(-x))=f(g(x)),
$$

所以 $f\circ g$ 是

$$
\boxed{\text{偶函数}}.
$$

### (2) $g(f(x))$

$$
g(f(-x))=g(-f(x))=g(f(x)),
$$

所以 $g\circ f$ 是

$$
\boxed{\text{偶函数}}.
$$

### (3) $f(f(x))$

$$
f(f(-x))=f(-f(x))=-f(f(x)),
$$

所以 $f\circ f$ 是

$$
\boxed{\text{奇函数}}.
$$

### (4) $g(g(x))$

$$
g(g(-x))=g(g(x)),
$$

所以 $g\circ g$ 是

$$
\boxed{\text{偶函数}}.
$$

## Question 8：习题 1，第 19 题

圆柱形容器底面半径为 $r$，总高度为 $H$。液面高度为 $h$ 时，体积为

$$
V=\pi r^2h.
$$

所以

$$
\boxed{h(V)=\frac{V}{\pi r^2}}.
$$

由 $0\le h\le H$，可得 $0\le V\le\pi r^2H$，故 $h$ 作为 $V$ 的函数时，其定义域为

$$
\boxed{D_h=[0,\pi r^2H]}.
$$

## Question 9：补充题第 3 题

设 $A,B$ 都是非空有界数集，$\sup A=a$、$\sup B=b$，且

$$
A+B=\{x\mid x=x_1+x_2,\ x_1\in A,\ x_2\in B\}.
$$

证明 $\sup(A+B)=a+b$。

对任意 $x_1\in A$、$x_2\in B$，由上确界的定义有

$$
x_1\le a,\qquad x_2\le b.
$$

所以

$$
x_1+x_2\le a+b,
$$

即 $a+b$ 是 $A+B$ 的上界。

另一方面，任取 $\varepsilon>0$。因为 $a=\sup A$、$b=\sup B$，存在 $x_1\in A$、$x_2\in B$，使得

$$
x_1>a-\frac{\varepsilon}{2},\qquad
x_2>b-\frac{\varepsilon}{2}.
$$

于是

$$
x_1+x_2>a+b-\varepsilon.
$$

因此 $a+b$ 以下的任何数都不可能是 $A+B$ 的上界。结合 $a+b$ 本身是上界，得到

$$
\boxed{\sup(A+B)=a+b}.
$$

