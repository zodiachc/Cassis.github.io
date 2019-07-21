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
>Given integers a and b with a $\neq$ 0, there exist unique integers q and r with $b=q a+r $ and $ 0 \leq r<\|a\|$
>

### <a name="2"> 2.Units and Primes</a>

>**Def** : We say that an integer $p$ is **irreducible** if it is not a unit, and if it has no factors other than $\pm 1, \pm p$.
>
>We say that an integer $p$ is **prime** if it is not a unit and if it has the following property: if $p \| a b$ then either $p \| a$ or $p \| b .$

> **Prop**: An integer p is irreducible if and only if it is prime.





> **Lemma**: 不定方程 $uv=w^2\ u,v,w>0; (u,v)=1$ 的一切正整数解可以写成$u:v:w=a^2:b^2:ab; a,b>0; (a,b)=1$ 

> **Thm**: Solution of $x^2+y^2=z^2$ with $x,y,z>0\ (x,y)=1, 2|x$ can be written by
> $$ x:y:z=2ab:a^2-b^2:a^2+b^2 \ a>b>0, (a,b)=1 ,\ a,b \text{ one odd one even}$$

> **Thm**: $x^4+y^4=z^4$没有正整数解。

Proof: 只需证明$x^4+y^4=z^2$没有正整数解。

反证法，若存在正整数解，设$z$的解集中$u$是最小一个，此时 $$x^4+y^4=u^2, (x,y)=1, x\text{偶}，y\text{奇}$$
thm
$$x^2=2ab,y^2=a^2-b^2,u^2=a^2+b^2$$
$$a>b>0, (a,b)=1, a\text{奇}，b\text{偶}$$ 
{不然设$b=2b_1+1, a=2a_1$,$y^2$mod$4=(4(a_1^2-b_1^2-b_1)-1)${mod}$4=3$, 与$y$奇数矛盾}

设$b=2c$，有
$$(x/2)^2=ac$$
lemma
$$a=d^2, c=f^2$$
代入可知$y^2=d^4-4f^4$
$$(2f^2)^2+(y^2)^2=(d^2)^2$$
thm
$$2f^2=2lm, d^2=l^2+m^2$$
lemma
$$l=r^2, m=s^2$$
所以有
$$d^2=r^4+s^4$$
但 $d<u$ 矛盾。