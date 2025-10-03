# Sequences

Let $(a_n)$ be a sequence. Define a new sequence:

$$s_n = \sum_{k=m}^n a_k$$

This is known as the sequence of partial sums. If $s_n \to L$ then:

$$\sum_{k=m}^{\infty} a_k = L$$

This is known as a series. If $L$ is finite then the series is convergent. Otherwise, the series is divergent. 

## Telescoping

The sum:

$$\begin{aligned}
\sum_{n=1}^{\infty} \frac{1}{n^2+n} &= \sum_{n=1}^{\infty} \frac{1}{n} - \frac{1}{n+1} \\
\end{aligned}$$

Then we have:

$$s_k = (1 - \frac{1}{2}) + (\frac{1}{2} - \frac{1}{3}) + ... + (\frac{1}{k} - \frac{1}{k+1}) \\$$

Note that $s_k$ is finite, so using associativity is allowed. On an infinite series, using arithmetic laws must be done with caution. Note the cancellation of terms. 

$$s_k = 1 - \frac{1}{k+1}$$

This means $s_k \to 1$ and so the sum tends to 1. Due the cancellation of terms, this series is known as a telescoping sum. 

## Lemma

$(x^n)$ diverges if $x \notin (0, 1)$ and converges to 0 if $x \in (0,1)$. 

## Definition

A geometric series is of the form:

$$\sum_{n=0}^{\infty} r^n = 1 + r + r^2 + ...$$

The value $r$ is known as the common ratio. 

## Theorem

The geometric series converges iff $|r|<1$ so that the infinite sum evaluates to $\frac{1}{1-r}$.

### Proof

If $r=1$ then $s_k = k$ so $s_k \to \infty$. Trivial

Else, if $r \neq 1$ then:

$$\begin{aligned}
s_k &= 1 + r + r^2 + ... + r^k \\
rs^k &= r + r^2 + r^3 + ... + r^{k+1} \\
s_k - rs_k &= 1 - r^{k+1} \\
(1-r)s_k &= 1- r^{k+1} \\
s_k &= \frac{1-r^{k+1}}{1-r} \\
\end{aligned}$$

If $|r|<1$, then $s_k \to \frac{1}{1-r}$. 

# Cauchy Criterion

$\sum a_k$ satisfies the Cauchy Criterion if $\forall \epsilon > 0$ $\exists N$ s.t. $\forall n \geq m > N$, 

$$\left| \sum_{k=m}^n a_k \right| < \epsilon$$

## Theorem

A series converges iff it satisfies the Cauchy Criterion

### Proof

A series $\sum a_k$ converges iff
The series $s_n$ of partial sums converges iff
The series $s_n$ of partial sums is Cauchy iff
$\forall \epsilon > 0$ $\exists N$ s.t. $\forall n,m > N$ then $|s_n - s_m| < \epsilon$ iff
$\forall \epsilon > 0$ $\exists N$ s.t. $\forall n \geq m > N$ then $|s_n - s_{m-1}| < \epsilon$ iff
$\forall \epsilon > 0$ $\exists N$ s.t. $\forall n \geq m > N$ then:

$$\left| \sum_{k=m}^n a_k \right| < \epsilon$$

## Corollary

If $\sum a_k$ converges then $a_k \to 0$. 

### Proof

If $\sum a_k$ converges, it must satisfy the Cauchy Criterion. 

$\forall \epsilon > 0$ $\exists N$ s.t. $\forall n \geq m > N$ we have:

$$\left| \sum_{k=m}^n a_k \right| < \epsilon$$

This is true in particular when $n = m$ Therefore, $|a_n| = |a_n-0| < \epsilon$. 

So $a_n \to 0$. 

# Divergence Test

If $a_k \nrightarrow 0$ then $\sum a_k$ diverges.

# Well-Ordering

Every nonempty subset of $\mathbb{N}$ has a least element.

## Theorem

Let $p(x)$ be a statement with scope in the natural numbers. If both of:

1. $p(1)$ is true
2. $p(k) \implies p(k+1)$

Then $\forall n \in \mathbb{N}$, $p(n)$ is true. 





