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

> [__Hasse-Minkowski theorem__]  If $F\left(x_{1}, \ldots, x_{n}\right)$ is a quadratic form with integral coefficients, then $(1)$ is solvable in integers if and only if it is solvable in $p$ -adic numbers for all $p$ and also in real numbers.

> We make one further remark. If $F$ is a form, then the solvability of $(1)$ in integers is equivalent to its solvability in rational numbers. 







