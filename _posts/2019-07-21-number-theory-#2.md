---
layout: post
title:  "Number Theory #2"
date:   2019-07-21 22:02:21 +0800
tags: NumberTheory
color: rgb(255,90,90)

---

## Congruence Equation

+ General Congruence 
+ Linear Congruence
+ Chinese Remainder Theorem
+ Congrugence mod p

### General Congruence

> **Def**: 设 $f(x)=a_nx^n+\ldots +a_1x+a_0$ 是整系数多项式，称 $f(x)\equiv0(\bmod m)$ 是关于未知数x的模m 的同余方程。

若$x_0$是方程的解，则$x\equiv x_0(\bmod m)$ 都是方程的解。因此只需在模m的完全剩余系中来解模m的同余方程，显然解的个数不超过m个。

为了解代数方程我们需要对代数方程进行恒等变换，一样，对于同余方程，我们利用同余式的性质进行恒等变换，变成同解方程。

（1）若$f(x)\equiv g(x)(\bmod m)$, 则$f(x)\equiv0(\bmod m)$ 与 $g(x)\equiv0(\bmod m)$ 同解。

（2）若$s(x)$是整系数多项式，则$f(x)\equiv0(\bmod m)$与$f(x)+s(x)\equiv s(x)(\bmod m)$同解。

（3）若$(a,m)=1$, 则$f(x)\equiv0(\bmod m)$与$af(x)\equiv 0(\bmod m)$同解。

（4）若$h(x)\equiv0(\bmod m)$是恒等同余式（解数为m），且$f(x) \equiv q(x) h(x)+r(x)(\bmod m)$，则原方程与$r(x) \equiv 0(\bmod m)$同解。

> **Thm**: 若$(a_n,m)=1$ 及 $a_n^{-1}a_n\equiv1(\bmod m)$ 则原方程与$x^{n}+a_{n}^{-1} a_{n-1} x^{n-1}+\cdots+a_{n}^{-1} a_{1} x+a_{n}^{-1} a_{0} \equiv 0(\bmod m)$ 同解。

### Linear Congruence

设$m \nmid a$，本节讨论最简单的模$m$一次同余方程 $ax\equiv b(\bmod m)$

> **Thm**: $ax\equiv b(\bmod m)$有解的充要条件为$(a,m)\vert b$, 且解的个数为$d=(a,m)$

> **Prop**: $(a,m)=1$时，$$a_{1} x \equiv-b\left[\frac{m}{a}\right](\bmod m)$$

### Chinese Remainder Theorem

这一节要考虑同余方程组
$$
\left\{\begin{array}{c}{x \equiv a_{1}\left(\bmod m_{1}\right)} \\ {x=a_{2}\left(\bmod m_{2}\right)} \\ {\ldots \ldots} \\ {x=a_{k}\left(\bmod m_{k}\right)}\end{array}\right.
$$

> **Thm**: 设$m_1, m_2, ... ,m_k$是正整数数，$(m_i,m_j)=1$, \\ 记$m=m_1m_2...m_k, M_i=\frac{m}{m_i}$, 则存在整数$M_i', st$
> 	$$M_iM_i'\equiv1(\bmod m_i)$$
> 	$$M_iM_i'\equiv0(\bmod m_j)$$
> 	且 $$x_0\equiv \sum_{i=1}^{k} a_{i} M_{i} M_{i}^{\prime}(\bmod m)$$是同余方程组对模$m$的唯一解。

> **Thm**: 同余方程组有解的充要条件为 $a_{i} \equiv a_{j}\left(\bmod \left(m_{i}, m_{j}\right)\right), 1 \leqslant i, j \leqslant n$

### Congruence mod $p^a$

> **Prop**: $p$是素数，$f(x)$是整系数多项式，c是 $f(x) \equiv 0\left(\bmod p^{a-1}\right)$的解，那么对于同余方程$f(x) \equiv 0\left(\bmod p^{a}\right)$, 若
>
> + $p\nmid f'(c)$，此时解数唯一，$x=c+pt_1$ 代入方程，Taylor 公式 $f(c)+pt_1f'(c)\equiv (mod p^a)$.
> + $p\vert f'(c), p^a\nmid f(c)$，无解。
> + $p\vert f'(c), p^a\vert f(c)$，$p$个解.

### Congrugence mod p

在上节中我们证明了对于素数$p$，模$p^a$ 的同余方程可以转化为求解模$p$的同余方程，本节要对素数模的同余方程做初步研究。

以下设$f(x)=a_nx^n+\ldots+a_1x+a_0$ 是整系数多项式，$p$是素数且$p\nmid a_n$.

> **Thm**: 设$k\leq n$, 方程$f(x)\equiv0(\bmod p)$ 有$k$个解$x_1, x_2, ... ,x_k$, 则对任意的$x$有
> $$f(x)=\left(x-x_{1}\right)\left(x-x_{2}\right) \cdots\left(x-x_{k}\right) f_{k}(x)(\bmod p)$$
> 其中$f_k(x)$是$n-k$次多项式，首项系数为$a_n$.

> **Thm**: 同余方程$f(x)\equiv0(\bmod p)$的解数$\leq n$.

> **Thm**: 设$n\leq p$，则同余方程$f(x)=x^n+\ldots+a_1x+a_0\equiv 0(mod p)$有$n$个解的充要条件是存在整系数多项式$q(x)，r(x)$，使得
> 	$$x^{p}-x=f(x) q(x)+p \cdot r(x)$$

> **Thm**: 若$p$是素数，$n\mid p-1, p\nmid a$ 则 $x^n\equiv a(\bmod p)$ 有解的充要条件为 $a^{\frac{p-1}{n}}\equiv1(\bmod p)$ ; 有解时，解数为$n$.

> **Cor**: 设$n$是正整数，$p$为素数，$(n,p-1)=k$, 则同余方程$x^n\equiv 1(\bmod p)$有$k$个解

### Quadratic residues

$p$为素数，我们来研究模$p$的二次同余方程
$$
ax^2+bx+c\equiv0(\bmod p)
$$
只需考虑$p>2, (n,p)=1$ 的情形。进而可以归结为讨论
$$
x^2\equiv n(\bmod p)		 
$$

> **Def**: 给定整数$p$ , 对于任意的整数$n$ ,