---
layout: post
title:  "Number Theory #2"
date:   2019-07-21 22:02:21 +0800
tags: NumberTheory
color: rgb(255,90,90)
---

##  Modular Arithmetic and $\mathbb{Z}/p\mathbb{Z}$



> **Def**: [Congruent]
>
> Let $q \geq$ 1 be an integer. Then we write $a \equiv b(mod q)$ if and only if $q$ divides $a - b$.

> **Prop**: Suppose that $x \equiv a(\bmod q)$ and that $y \equiv b(\bmod q) .$ Then $x+y \equiv$
> $a+b(\bmod q)$ and $x y \equiv a b(\bmod q)$

The fact that “(mod q)” works well with regard to both addition and multiplication is really asserting some properties of a natural ring homomorphism from the
integers Z to a ring called $\mathbb{Z}/p\mathbb{Z}$.

> $a\equiv b(\bmod m), d\mid m, d>0 \implies a\equiv b(\bmod d)$
> $a\equiv b(\bmod m), k>0, k\in \mathbb{N} \implies ak\equiv bk(\bmod mk)$
> $a\equiv b(\bmod m_i) \implies a\equiv b(\bmod [m_1,\ldots m_k])$
> $a\equiv b(\bmod m) \implies (a,m)=(b,m)$
> $ac\equiv bc(\bmod m), (c,m)=1 \implies a\equiv b(\bmod m)$

> **Def**: $(\mathbb{Z} / q \mathbb{Z})^{ \times} :=\{x+q \mathbb{Z} \in \mathbb{Z} / q \mathbb{Z} :(x, q)=1\}$

We can see $|(\mathbb{Z} / q \mathbb{Z})^{ \times}|=\varphi(q)$, where $q=p_1^{a_1}p_2^{a_2}\ldots p_k^{a_k}. \varphi(q)=q\left(1-\frac{1}{p_1}\right)\left(1-\frac{1}{p_2}\right)\ldots\left(1-\frac{1}{p_k}\right).$

One of our main aims is to prove the following result.

> **Thm**: Let p be a prime. Then there is an element $g \in(\mathbb{Z} / p \mathbb{Z})^{ \times}$ with ord$_{p}(g)=p-1 .$ Equivalently, $(\mathbb{Z} / p \mathbb{Z})^{ \times}$ is a cyclic group.

Here are some theorems.

> **Thm**: [Euler's Theorem]
> If a is an integer prime to the positive integer m, then $a^{\varphi(m)}\equiv1(\bmod m)$

> **Thm**: [Fermat’s Little Theorem]
> If $p$ is a prime and $a$ is an integer not divisible by $p$, then $a^{p-1}\equiv1(\bmod p)$

> **Thm**: [Wilson's Theorem]
> $p$ is a prime $\Leftrightarrow$ $(p-1)!\equiv-1(\bmod p)$











