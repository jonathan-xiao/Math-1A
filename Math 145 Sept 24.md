## Chinese Remainder Theorem 

Suppose $m_1, m_2, ..., m_k$ are all pairwise relatively prime. Then the system:

$$x \equiv a_1 \mod m_1$$
$$...$$
$$x \equiv a_k \mod m_k$$

has a unique solution mod $m_1 m_2 m_3 ... m_k$. 

### Example

$$x \equiv 8 \mod 5$$
$$x \equiv -8 \mod 13$$

1. $x = 8 + 5k = -8 + 13j$ which means $5k - 13j = -16$.

2. Use Euclid's Algorithm

Because $5$ and $13$ are relatively prime, their gcd is 1, and so by Euclid's Algorithm there is a solution to 

$$5k-13j=1$$

Then you find that solution and multiply both sides by -16. So $k = 8(-16)$ and $j = 3(-16)$. 

So $x = 8+5k = -632$. This means $x \equiv -632 \mod 65$.

$x \equiv 18 \mod 65$. 

### Proof

Proof by strong induction. Assume every case below the $k$ case. 

Then we have a unique solution for the system of equations:

$$x = a_i \mod m_i$$

where $i > 1$ (so we disclude one case, so there are $k-1$ cases). 

Then we have a new system, where we have that unique solution and the $i=1$ case. 

$$x \equiv b \mod \prod_{i>1} m_i$$
$$x \equiv a \mod m_1$$

This is another system of equations, which should have a unique solution. So the general case has a unique solution. 

### Example

Solve $x^2 + 1 \equiv 0 \mod 65$. 

We know that $\mathbb{Z}/65$ is not a field (nor an integral domain) because there are 0 divisors. This is because 65 is composite. But by the Chinese Remainder Theorem, we can split this into prime factors.

$$x^2+1 \mod 5$$
$$x^2+1 \mod 13$$

And since $5$ and $13$ are prime numbers, their mod integers are integral domains (and fields). 

By an eye test, we see that $\pm 8$ are solutions. So we just solve 4 systems of equations. 

$$x = \pm 8 \mod 5$$
$$x = \pm 8 \mod 13$$

And so we get the roots are $\pm 8, \pm 18$. 

## Proposition

$ax \equiv b \mod n$ has a solution iff $\gcd(a,n)|b$ (and let the gcd be $d$). In this case, the solution is unique mod $\frac{n}{d}$. 

### Proof

$ax \equiv b \mod n \Longleftrightarrow ax + yn = b$. There is a solution only if $d|b$, and all solutions take the form:

$$x = x_0 + \frac{n}{d}k$$
$$y = y_0 - \frac{a}{d}k$$

In the first, we can see that $x$ will be a unique solution mod $\frac{n}{d}$. 

## Fermat's Little Theorem

Suppose $p$ is prime and $p$ does not divide $a$. Then $a^{p-1} \equiv 1 \mod p$. Also, for all $b \in \mathbb{Z}$, $b^p \equiv b \mod p$. 

### Proof 

The function $f: \mathbb{Z}/p \rightarrow \mathbb{Z}/p$ where $[x] \rightarrow [ax]$ is a bijection. 

$\\{[1], [2], ..., [p-1]\\}$ = $\\{[a], [2a], ..., [a(p-1)]\\}$ up to a rearranging of terms (same number of terms). 

Then:

$$\begin{aligned}
(p-1)! &\equiv \prod_{i=1}^{p-1}a_i \\
(p-1)! &\equiv a^{p-1}(p-1)! \\
1 &\equiv a^{p-1}
\end{aligned}$$

Therefore the statement is proved.




