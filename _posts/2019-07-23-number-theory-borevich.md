# Congruences

**This chapter is devoted to the theory of congruences and to its application
to equations in several variables. **

>The connection between congruences and equations is based on the simple remark that if the equation
>$$
>F\left(x_{1}, \ldots, x_{n}\right)=0
>$$
>where $F$ is a polynomial with integral coefficients, has a solution in integers, then the congruence
>$$
>F\left(x_{1}, \ldots, x_{n}\right) \equiv 0(\bmod m)
>$$
>is solvable for any value of the modulus $m$ . 

so we have a sequence of **necessary conditions** for the solvability of (1) in integers. 

The question of the **sufficiency** of these conditions is much more difficult. In this chapter, we shall prove it in the case where $F$ is a **quadratic form** which satisfies the additional condition, clearly necessary, that $(1)$ be solvable in real numbers.

From the elementary theory of numbers it is known that if the congruences
$$
\begin{equation*}
F\left(x_{1}, \ldots, x_{n}\right) \equiv 0\left(\bmod p_{i}^{k_{i}}\right)
\end{equation*}
$$
are solvable for $i=1, \ldots, r,$ where $p_{1}, \ldots, p_{r}$ are distinct primes, then the congruence $(2)$ is solvable modulo $m,$ where $m=p_{1}^{k_{1}} \ldots p_{r}^{k_{1}} .$ The solvbility of the congruence $(2)$ for all $m$ is equivalent to its solvability modulo
all powers of primes. 

We fix a prime $p$ and ask whether the congruencea
$$
F\left(x_{1}, \ldots, x_{n}\right) \equiv 0\left(\bmod p^{k}\right)
$$
is solvable for all natural numbers $k$ .

Hensel showed that the solvability of $(3)$ for all $k$ was equivalent to the solvability of $(1)$ in $p$ -adic numbers. Hence we may say that the solvability of the congruence $(2)$ for all $m$ is equivalent to the solvability of $(1)$ in $p$ -adic numbers for all prime numbers $p$ .

> [__Hasse-Minkowski theorem__]  If $F\left(x_{1}, \ldots, x_{n}\right)$ is a **quadratic form** with integral coefficients, then $(1)$ is solvable in integers if and only if it is solvable in $p$ -adic numbers for all $p$ and also in real numbers.

> We make one further remark. If $F$ is a form, then the solvability of $(1)$ in integers is equivalent to its solvability in rational numbers. 

### Congruence with prime modulus

#### Equivalence of Polynomials

We first consider congruences with prime modulus $p .$ The residue classes modulo $p$ form a finite field with $p$ elements, and a conguence with modulus $p$ can be considered as an equation in this field. 

We write
$$
\begin{equation*}	
F\left(x_{1}, \ldots, x_{n}\right) \equiv G\left(x_{1}, \ldots, x_{n}\right)(\bmod p)
\end{equation*}
$$
and call the polynomials $F$ and $G$ **congrent**, if the coefficients of corresponding terms on the right and left sides are congruent modulo $p .$ If for any set of values $c_{1}, \ldots, c_{n}$ we have
$$
\begin{equation*}
F\left(c_{1}, \ldots, c_{n}\right) \equiv G\left(c_{1}, \ldots, c_{n}\right)(\bmod p) 
\end{equation*}
$$
then we write $F \sim G$ and call $F$ and $G$ **equivalent**. It is clear that if $F \equiv G$ then $F \sim G,$ but the example of the polynomials $x^{p}$ and $x$ shows that the converse is, in general, false. Since, if $F \sim G,$ the congruences $F \equiv 0(\bmod p)$ and $G \equiv 0(\bmod p)$ have the same solutions, it is natural that in the theory of congruences one needs to be able to replace a polynomial $F$ by a polynomial which is equivalent to it but is possibly in a simpler form.

> **Theorem** 1. Every polynomial $F$ is equivalent to a reduced polynomial $F^{*},$ whose total degree is not greater than that of $F .$

> **Theorem** 2. If two <u>reduced polynomials</u> are equivalent, then they are congruent.

#### Theorems on the Number of Solutions of Congruences

> **Theorem** 3. If the congruence $F\left(x_{1}, \ldots, x_{n}\right) \equiv 0(\bmod p)$ has at least one solution, and the <u>total degree</u> of the polynomial $F$ is less than the number of variables, then the congruence has at least two solutions.

> **Corollary** (Chevalley's Theorem). If $F\left(x_{1}, \ldots, x_{n}\right)$ is a form of degree less than $n,$ then the congruence
> $$
> \begin{equation*}
> F\left(x_{1}, \ldots, x_{n}\right) \equiv 0(\bmod p)
> \end{equation*}
> $$
> has a nonzero solution.

> **Theorem** 4 (Warning's Theorem). The number of solutions of the congruence $F\left(x_{1}, \ldots, x_{n}\right) \equiv 0(\bmod p)$ is divisible by $p,$ provided that the degree of the polynomial $F\left(x_{1}, \ldots, x_{n}\right)$ is less than $n$

#### Quadratic Form Modulo a Prime

We now apply the above results to the case of quadratic forms.

> **Theorem** 5. Let $f\left(x_{1}, \ldots, x_{n}\right)$ be a quadratic form with integer coefficients.
> If $n \geqslant 3,$ then the congruence
> $$
> \begin{equation*}
> f\left(x_{1}, \ldots, x_{n}\right) \equiv 0(\bmod p)
> \end{equation*}
> $$
> has a nonzero solution.

The case of quadratic forms in one variable is trivial, We shall consider the remaining case of binary quadratic forms.($p\neq 2$)
$$
\begin{equation*}
	f(x, y)=a x^{2}+2 b x y+c y^{2}
\end{equation*}
$$
Its discriminant $a c-b^{2}$ we denote by $d$.

> **Theorem** 6. The congruence
> $$
> f(x, y) \equiv 0(\bmod p) \quad(p \neq 2)
> $$
> has a nonzero solution if and only if $-d$ is either divisible by $p$ or is a quadratic residue modulo $p$ . i.e. $\left(\frac{-d}{p}\right)=0\ or 1$

### Trigonometirc Sums

#### Congruences and Trigonometric Sums

We first note that for the equation $F\left(x_{1}, \ldots, x_{n}\right)=0$ to have a solution, it is necessary that for all $m$ the congruence $F \equiv 0$ (mod $m )$ have a solution. Even if we limit our considerations to prime values of $m,$ we still have an infinite number of necessary conditions . It can be shown that for a very important class of polynomials a finite method  exists.

> **Definition**. A polynomial $F\left(x_{1}, \ldots, x_{n}\right)$ with rational coefficients is called **absolutely irreducible** if it cannot be factored in a nontrivial manner in any extension of the field of rational numbers.

> **Theorem** A. If $F\left(x_{1}, \ldots, x_{n}\right)$ is an absolutely irreducible polynomial
> with integer coefficients, then the congruence
> $$
> F\left(x_{1}, \ldots, x_{n}\right) \equiv 0(\bmod p)
> $$
> is solvable for all prime numbers $p,$ larger than some bound which depends
> only on the polynomial $F $ .

### $p$-Adic Numbers

#### $p$-Adic Integers

#### The Ring of $p$ -Adic Integers

#### Fractional $p$-Adic Numbers

#### Convergence in the Field of $p$-Adic Numbers

### An Axiomatic Characterization of the Field of $p$ -Adic Numbers



### Quadratic Forms with $p$ - Adic coefficients

### Rational Quadratic Forms

#### The Hasse-Minkowski Theorem

> **Theorem** 1 (Hasse-Minkowski). A quadratic form with rational coefficients represents zero in the field of rational numbers if and only if it represents zero in the field of real numbers and in all fields of $p$ -adic numbers.











