---
layout: post
title:  "Number Theory"
date:   2019-07-19 22:02:21 +0800
tags: NumberTheory
color: rgb(255,90,90)
---

## Some Basics 
+ <a href="#1"> 1.Division Algorithm</a>
+ <a href="#2"> 2.Units and Primes</a>
+ <a href="#3"> 3.GDC</a>
### <a name="1"> 1.Division Algorithm</a>

>**Axiom**:[Well-ordering Principle]
>There is a smallest integer in every nonempty subset $C$ of $\mathbb{N}$ .


>**Theorem**:[Mathematical Induction]
>
>Let $S(n)$ be a family of statements, one for
each integer $n \geq m,$ where $m$ is some fixed integer. If
>
>1. $S(m)$ is true, and
>2. $S(n)$ is true implies $S(n+1)$ is true,
>
>  then $S(n)$ is true for all integers $n \geq m$ .


>**Theorem**:[Second Form of Induction]
>
>Let $S(n)$ be a family of statements, one for each integer $n \geq m,$ where $m$ is some fixed integer. If
>
>1. $S(m)$ is true, and
>2. $S(k)$ is true for all $k$ with $m\leq k < n$, then $S(n)$ is true,
> 
> then $S(n)$ is true for all integers $n \geq m$ .

>**Theorem**:[Division Algorithm]
>
>Given integers a and b with a $\neq$ 0, there exist unique integers q and r with $b=q a+r $ and $ 0 \leq r< \mid a \mid$
>

### <a name="2"> 2.Units and Primes</a>

>**Def** : We say that an integer $p$ is **irreducible** if it is not a unit, and if it has no factors other than $\pm 1, \pm p$.
>
>We say that an integer $p$ is **prime** if it is not a unit and if it has the following property: if $p \mid a b$ then either $p \mid a$ or $p \mid b .$

> **Prop**: An integer p is irreducible if and only if it is prime.

> **Prop**: Every integer $n \geq 2$ is either a prime or a product of primes

> **Cor**: There are infinitely many primes.

> **Thm**:[Fundamental Theorem of Arithmetic] Every integer other than zero and the units may be factored into primes in an essentially unique way.

### <a name="3">3.GDC</a>

> **Def**: If a, b are integers then the **greatest common divisor (GCD)** of a and b, written (a, b), is the greatest positive integer d such that $d\mid a$ and $d\mid  b$.

We have the following facts.
> $(a,b)=(|a|,|b|); (0,b)=|b|.$
> $(a,q)=1, (b,q)=1, then (ab,q)=1.$
> $(a,b)=1$, $b\mid ax$, then $b\mid x.$
> $ab=[a,b](a,b)$
> Suppose that $q_{1}, \ldots, q_{k}$ are pairwise coprime. Then $q_{1} \cdots q_{k}$ divides $x$ if and only if qi divides $x$ for $i=1, \ldots, k$
> a,b,c is nonzore integers, $a=bq+c$, then $(a,b)=(b,c)$

> **Thm**: [Euclid's Algorithm]
> Suppose that a, b are integers. Then there is an algorithm that finds the gcd, $d = (a, b)$, and there is an algorithm that finds a pair of integers s and t with$ d = sa + tb.$ 

> **Thm**:[Prime Factor Decomposition of n!]
> $$
> n!=\displaystyle\prod_{p\leq n}p^{\displaystyle\sum_{r=1}^\infty\left[\frac{n}{p^r}\right]}
> $$
> 
>

### <a name= "4">4.Diophantine Equations</a>

> **Thm**: Suppose that a, b, c are integers with $a, b \neq 0$. Then there is
> a solution to the equation $am + bn = c$ in integers $m, n$ if and only if $ (a, b)|c.$


> **Lemma**: 不定方程 $uv=w^2\ u,v,w>0; (u,v)=1$ 的一切正整数解可以写成$u:v:w=a^2:b^2:ab; a,b>0; (a,b)=1$ 

> **Thm**: Solution of $x^2+y^2=z^2$ with $x,y,z>0\ (x,y)=1, 2\mid x$ can be written by
> $$ x:y:z=2ab:a^2-b^2:a^2+b^2 \ a>b>0, (a,b)=1 ,\ a,b \text{ one odd one even}$$

> **Thm**: $x^4+y^4=z^4$没有正整数解。

