## Diophantine Equations

If $d = \mathrm{gcd}(a,b)$ then $\exists s,t \in \mathbb{Z}$ s.t. $d = as + bt$. 

### Corollary

Let $a,b \in \mathbb{N} \backslash \\{0\\}$. Then the smallest positive linear combination $as + bt = \mathrm{gcd}(a,b)$. 

#### Proof 

Let $d = \mathrm{gcd}(a,b)$ and let $d'$ be the smallest positive value of $as + bt$ where $s,t \in \mathbb{Z}$. 

The number $d$ is a positive linear combination and $d'$ is the smallest linear combination, so $d' \leq d$. 

We know $\exists s', t' \in \mathbb{Z}$ s.t. $d' = as' + bt'$. We also know $d|a$ and $d|b$, therefore, $d|d'$. 

Then, $d \leq d'$. This implies $d=d'$. 

## Definition

We say $a$ and $b$ are relatively prime if $\mathrm{gcd}(a,b) = 1$. 

## Proposition

If $a$ and $b$ are relatively prime, and suppose that $a|(bc)$, then $a|c$. 

### Proof

By the corollary, $\exists s,t \in \mathbb{Z}$ s.t. $as+bt=1$. 

Multiplying both sides by $c$, we have $asc + bct = c$. Well, $a$ divides $a$ and $a$ divides $bc$ so $a$ divides $c$ as desired. 

## Corollary

If $p$ is prime and suppose 

$$p | \prod_{i=1}^{k} a_i$$

Then, there exists $i$ s.t. $p | a_i$. 

### Proof by Induction

For $k=1$, if $p|a_1$ then $p|a_1$. 

For $k=2$, we know $p|(a_1 a_2)$. 

Because $p$ is a prime, the gcd of $p$ and $a_1$ must be 1 or $p$. This is because the gcd divides $p$, and a prime number only has two positive divisors, 1 and $p$. 

If $\mathrm{gcd}(p, a_1) = 1$, then the proposition says that $p|a_2$. 
If $\mathrm{gcd}(p, a_1) = p$, then $p|a_1$. 

For $k > 2$, we use induction. Assume the $k-1$ case and prove the $k$ case. 

$$p | \prod_{i=1}^{k} a_i$$

We then know that:

$$p | \prod_{i=1}^{k-1} a_i \cdot a_k$$

Then, either $p|a_k$ or 

$$p | \prod_{i=1}^{k-1} a_i$$

If $p|a_k$, then we know $p|a_k$. Otherwise, then $p|a_i$ for some $i$. 

## Unique Factorization Theorem

Let $n$ be an integer and $n \geq 2$. Then $n$ factors uniquely into a product of positive primes. Then, $\exists p_i$ positive primes s.t. 

$$n = \prod_{i=1}^{r} p_i$$

Furthermore, if $q_j$ are positive primes with 

$$n = \prod_{j=1}^{s} q_j$$

Then $r=s$ and after reordering the $q_j$, then $p_i = q_i$. 

### Proof by Strong Induction

Suppose $\forall i$ where $2 \leq i < k$ then each integer $i$ has a unique positive prime factorization. WLOG, WMA $p_1 \leq q_1$ and $p_1 \leq p_2 \leq ... \leq p_r$ and $q_1 \leq q_2 \leq ... \leq q_s$. 

We know that $p_1 | n = \prod q_j$ then $p_1 | q_j$ for some $j$ (by the last proposition). By definition of a prime, therefore, $p_1$ is 1 or $q_j$. But $p_1$ is prime, so it cannot be 1. So $p_1 = q_j$. We know that $p_1 \leq q_1 \leq q_2 \leq ... \leq q_j = p_1$ by the assumption. Therefore, 

$$\prod_{i=2}^{r} p_i = \frac{n}{p_1} = \prod_{j=2}^{s} q_j$$

$n/p_1$ is less than $n$, so by the inductive hypothesis, both products are identical. This proves the unique factorization of the integers. 










