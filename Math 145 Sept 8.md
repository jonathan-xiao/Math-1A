## Many Primes Proposition

There are infinitely many primes.

### Proof

We will show that $\forall n \in \mathbb{N}$, $\exists p_n > n$ where $p_n$ is prime. 

Consider $x = n! + 1$ where $n \geq 1$. 

Then, $\exists p_n$ s.t. $p_n | x$. So, $p_n \leq n \implies p_n | n!$.

### Lemma

If $a,b,c \in \mathbb{Z}$ and $a | b$ and $a | c$ then $a | (b \pm c)$.

#### Proof

We know that $b = an$ and $c = am$ where $n,m \in \mathbb{Z}$. This implies that $b \pm c = a(n \pm m)$. This means that $a | (b \pm c)$ is true.

### Proof, Continued

By the lemma, then if $p_n | n!$, $p_n | (x - n!)$ or $p_n | 1$. This is impossible, since all positive primes are larger than 1. 

This means that for any $n$, then $\exists p > n!$. The list of primes is infinite. 

## Density of Primes

Suppose now we want to figure out how often primes occur. Let $\pi(n)$ be the number of positive primes less than of equal to $n$.

It is known that:

$$\lim_{n \to \infty} \space {\frac{\pi(n)}{n  \space \ln{(n)}}} = 1$$

It appears that as $n$ grows, the density of primes approximately grows by $n \space \ln{(n)}$. 

## Theorem

$$\sum_{p \space \mathrm{prime}} \frac{1}{p} = \infty$$ 

### Proof

Let us order the primes $p_1 < p_2 < ...$ Assume that the sum converges. The terms then must get arbitrarily small, so that there must exist $k$ such that:

$$\sum_{i = k+1}^{\infty} \frac{1}{p_i} < \frac{1}{2}$$

Let $N = 4^{k+1}$. For $S = \\{1, 2, 3, ..., N\\}$ and any large $p_i$, where $i > k$, there are at most $\frac{N}{p_i}$ numbers in $S$ with $p_i$ as a factor. 

Let the number of elements in $S$ with any $p_i$ as a factor where $i > k$ be called $n$. Then we have:

$$n = \sum_{i = k+1}^{\infty} \frac{N}{p_i} < \frac{N}{2}$$

This is from the first sum, multiplying each side by $N$. 

Every number that has not been counted yet in $S$ can be denoted as $a = p_1^{n_1} \cdot p_2^{n_2} \cdot ... \cdot p_k^{n_k}$. Every prime factor here has $i \leq k$. 

Let us factor out the largest possible square from each $a$. Therefore, 

$$a = p_1^{m_1} \cdot p_2^{m_2} \cdot ... \cdot p_k^{m_k} \cdot \prod_{i = 1}^{k} p_i^{e_i}$$ 

where $e_i \in \\{0, 1\\}$. Hence the left side can take at most $\sqrt{N}$ values, and the right side $2^k$ values. So the maximum number of elements in $S$ with a small prime factor is $m = \sqrt{N} 2^k$. 

Therefore, we have:

$$\begin{aligned}
4^{k+1} &= N \\
&\leq n + m \\
&< \frac{N}{2}+2^k \sqrt{N} \\
&= 2^{2k+1} + 2^k 2^{k+1} \\
&= 4^{k+1}
\end{aligned}$$

This is a contradiction. Therefore the original sum must diverge!




