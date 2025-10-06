# Prime Number Forms

## $4k+3$

Assume there are a finite number of primes $p_i$ of form $4k+3$. Then, multiply all those primes together to get $\prod p_i$. Then consider $4\prod p_i - 1 = t$. We know that $\forall i$, $i \not| t$. However, $t$ much have a prime factorization $\prod q_j$ where none of the $q_j=p_i$. 

If $q_j \equiv 1 \mod 4$ then $t = 1 \mod 4$. This cannot be the case. But then there must exist a $q_j \equiv 3 \mod 4$, but then this $q_j = p_i$, another contradiction. Therefore there must be infinitely many primes of this form.

## $4k+1$

Assume there are a finite number of primes $p_i$ of form $4k+1$. Then, multiply all those primes together to get $\prod p_i$. Now consider $(2\prod p_i)^2 + 1=t$. $t$ must have a prime factorization, and so now suppose $q|t$. Note $p \neq p_i$ $\forall i$. Then:

$$\begin{aligned}
qk &= (2\prod p_i)^2+1 \\
\implies (2\prod p_i)^2 &\equiv -1 \mod q \\
2\prod p_i &\equiv (-1)^{\frac{1}{2}} \mod q \\
(2\prod p_i)^{q-1} &\equiv (-1)^{\frac{q-1}{2}} \mod q \\
\end{aligned}$$

Note that because $q|t$ and $q \neq p_i$ then $\gcd(q, 2\prod p_i)=1$. Using Fermat's Little Theorem, then:

$$(2\prod p_i)^{q-1} \equiv 1 \mod q \implies (-1)^{\frac{q-1}{2}} \equiv 1 \mod q$$

If $q \equiv 3 \mod 4$ then $\frac{q-1}{2}$ is odd which means because $(-1)^{2n+1} \equiv (-1)$ then we have a contradiction, because $q \neq 2$ and so we cannot have a modulo being 1 and -1 simultaneously. So there must be infinitely many primes of this form.

## $3k+1$

Assume there are finitely many primes $p_i$ of form $3k+1$. Consider $t = x^2 + x + 1$ where $x = 3\prod p_i$. Then we know that none of $3, p_i$ divides $t$ because of the $+1$. 

$t$ must have a prime factorization. Suppose $q \neq 3, p_i$ and $q |t$. Then $q$ cannot divide $x$. 

By Fermat's Little Theorem, we have $x^{q-1} \equiv 1 \mod q$. 

We know $x^3-1 = (x-1)(x^2+x+1) = (x-1)t$. This means that $x^3 \equiv 1 \mod q$. However, $x^0 \equiv 1 \mod q$ as well. So the order of $x \mod q$ must be less than or equal to $3$. 

Well the order cannot be $2$, otherwise $0$ and $3$ cannot both be the same. So suppose the order is $1$. That means $x \equiv 1 \mod q$. Then $t \equiv 1+1+1 \equiv 3 \mod q$. But then $q|t$ and $q|(t-3)$ so $q=3$ which is a contradiction. 

So we know the order of $x \mod 3$ is 3. Then $x^{q-1} \equiv 1 \mod q$ and $ x^3 \equiv 1 \mod 3$. Well, then $3|(q-1)$ so $3k=q-1$ and $3k+1=q$. But $q$ was not in the original list of $p_i$. Contradiction, and so we have infinitely many primes of form $3k+1$. 

# Dirichlet

## Euler Product

$$\sum_{n=1}^{\infty}\frac{1}{n} = \prod_{p \space \mathrm{prime}}^{\infty} \frac{1}{1-\frac{1}{p}}$$

## Proof

We know that $\frac{1}{1-x} = 1 + x + x^2 + x^3 + ...$. Then we can rewrite the right hand side as:

$$\prod_p (1 + \frac{1}{p} + \frac{1}{p^2} + ...)$$

Every single natural number has unique factorization. So for each number you select the unique factorization from this sum. For example $6 = 2^1 \cdot 3^1 \cdot 1 \cdot 1 \cdot 1 ... $

## Divergent Series 

$$\sum_p \frac{1}{p}$$

## Proof

We take the natural logarithm on both sides of the Euler Product.

$$\begin{aligned}
\ln \sum_{n=1}^{\infty}\frac{1}{n} &= \ln \prod_{p \space \mathrm{prime}}^{\infty} \frac{1}{1-\frac{1}{p}} \\
\infty &= \sum_p \ln \frac{1}{1-\frac{1}{p}} \\
&= \sum_p -\ln(1-\frac{1}{p}) \\
&= \sum_p (\frac{1}{p} + \frac{1}{2p^2} + \frac{1}{3p^3} + ... ) \\
&= \sum_p \frac{1}{p} + \sum_p \frac{1}{p^2}(\frac{1}{2} + \frac{1}{3p} + \frac{1}{4p^2} + ... ) \\
&< \sum_p \frac{1}{p} + \sum_p \frac{1}{2p(p-1)}
\end{aligned}$$

The second term converges by the integral test, and so the first term diverges. 

## Divergent Series

$$\sum_{p \equiv 1 \mod 3} \frac{1}{p}$$

Define 

$$\chi_0(n) = 
\begin{cases} 
      0 & n \equiv 0 \mod 3 \\
      1 & n \equiv 1,2 \mod 3
   \end{cases}
$$
$$\chi_1(n) = 
\begin{cases} 
      0 & n \equiv 0 \mod 3 \\
      1 & n \equiv 1 \mod 3 \\
      -1 & n \equiv 2 \mod 3
   \end{cases}
$$

We know that $\chi(mn) = \chi(m) \chi(n)$ (it is multiplicative).

$$\therefore \sum_{n \equiv 1 \mod 3} \frac{1}{n} =\frac{1}{2}\left(\sum_{n=1}^{\infty} \frac{\chi_0(n)}{n} + \sum_{n=1}^{\infty} \frac{\chi_1(n)}{n}\right)$$

By the Euler Product: (here $\chi(n)$ can refer to either $\chi_0$ or $\chi_1$. 

$$\begin{aligned}
\sum \frac{\chi(n)}{n} &= \prod_p \frac{1}{1-\frac{\chi(p)}{p}} \\
\ln \sum \frac{\chi(n)}{n} &= \ln \prod_p \frac{1}{1-\frac{\chi(p)}{p}} \\
\end{aligned}$$

The following function tells us when we have a prime $p \equiv 1 \mod 3$. 

$$\frac{1}{2}\left(\sum_{n=1}^{\infty} \frac{\chi_0(n)}{n} + \sum_{n=1}^{\infty} \frac{\chi_1(n)}{n}\right)$$

Therefore, 

$$\sum_{p \equiv 1 \mod 3} \frac{1}{p} = \frac{1}{2}\left(\sum_{p}^{\infty} \frac{\chi_0(n)}{n} + \sum_{p}^{\infty} \frac{\chi_1(n)}{n}\right)$$

Hence because the first term on the right diverges, the the left hand side diverges. An argument for $2 \mod 3$ is similar but takes the indicator:

$$\frac{1}{2}\left(\sum_{n=1}^{\infty} \frac{\chi_0(n)}{n} - \sum_{n=1}^{\infty} \frac{\chi_1(n)}{n}\right)$$

And similar arguments exist for all other arithmetic forms of primes that are nontrivial.








