---
layout: post
title:  "Number Theory"
date:   2019-07-19 22:02:21 +0800
tags: Algebra, NumberTheory
color: rgb(255,90,90)
---

## Some Basics 
+ <a href="#1"> 1.Division Algorithm</a>


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
>  then $S(n)$ is true for all integers $n \geq m$ .

 proof
(反证法，设$C$为不满足归纳法的集合，它有一个最小数$k$，所以$k-1$不在$C$中，但由归纳法，$k$也不在$C$中，矛盾)
Let $C$ be the set of all integers $n \geq m$ for which $S(n)$ is false. If $C$ is empty, we are done. Otherwise, there is a smallest integer $k$ in $C$ . By $(i),$ we have $k>m,$ and so there is a statement $S(k-1) .$ But $k-1<k$ implies $k-1 \notin C,$ for $k$ is the smallest integer in C. Thus, $S(k-1)$ is true. But now (ii) says that $S(k)=S([k-1]+1)$ is true, and this contradicts $k \in C$ [which says that $S(k)$ is false].



