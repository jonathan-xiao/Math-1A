# Comparison Test

Let $\sum a_k$ be a series with non-negative terms.

1. If $\sum a_k$ converges and $|b_k|\leq a_k$ $\forall k$ then $\sum b_k$ converges
2. If $\sum a_k = \infty$ and $b_k \geq a_k$ $\forall k$ then $\sum b_k = \infty$

## Proof

Suppose that $\sum a_k$ converges and $|b_k| \leq a_k$ $\forall k$. By the triangle inequality, 

$$\left| \sum_{k=m}^n b_k\right| \leq \sum_{k=m}^n |b_k|$$

Then: term by term, we have:

$$\sum_{k=m}^n |b_k| \leq \sum_{k=m}^n a_k \leq \left| \sum_{k=m}^n a_k\right|$$

## Theorem (P-series)

$\sum \frac{1}{n^p}$ converges iff $p > 1$

## Example

Consider $\sum \frac{n}{n^2+3}$

We know that $\frac{n}{n^2+3} \leq \frac{n}{n^3} = \frac{1}{n^2}$. We know that $\sum \frac{1}{n^2}$ converges, so then $\sum \frac{n}{n^2+3}$ converges. 

## Definition

A series $\sum a_n$ is absolutely convergent if $\sum |a_n|$ converges. 

## Corollary

An absolutely convergent series is convergent

### Proof

If $\sum |a_n|$ converges then $|b_n| \leq |a_n|$ for $b_n = a_n$ so $\sum b_n = \sum a_n$. Both of these converge. 

## Definition

$${{n}\choose{k}} = \frac{n!}{k!(n-k)!}$$

## Theorem

$$(1+y)^n = \sum_{k=0}^n {{n}\choose{k}}y^k$$

## Theorem

The following are infinite limits.

1. $\lim \frac{1}{n^p} = 0$ where $p > 0$
2. $\lim n^{\frac{1}{n}} = 1$
3. $\lim a^{\frac{1}{n}} = 1$ when $a > 0$

### Proof 1

Fix $\epsilon > 0$. Choose $N = (\frac{1}{\epsilon})^{\frac{1}{p}}$. Then, $\forall n > N$, $\epsilon > \frac{1}{n^p}$. Therefore:

$$\left| \frac{1}{n^p} - 0 \right| < \epsilon$$

### Proof 2

Consider $b_n = n^{\frac{1}{n}} - 1$. Since $n \geq 1$ we have $b_n \geq 0$ $\forall n$. 

This means that $n = (1+b_n)^n$. Each term in the binomial expansion on the right is positive. This means that $n$ is smaller than each term individually.

$$n > \frac{n(n-1)b_n^2}{2}$$

Therefore, we solve for $b_n < \sqrt{\frac{2}{n-1}}$. 

This means that $0 \leq b_n \leq \sqrt{\frac{2}{n-1}}$. By the squeeze theorem, $b_n \to 0$ and so $n^{\frac{1}{n}} \to 1$. 

### Proof 3

Consider the case $a \geq 1$. For $n \geq a$ we have $1 \leq a^{\frac{1}{n}} \leq n^{\frac{1}{n}}$. By the squeeze theorem, then $a^{\frac{1}{n}} \to 1$. 

Consider the case $0 < a < 1$. Then:

$$\lim_{n \to \infty} \left(\frac{1}{a}\right)^{\frac{1}{n}} = 1$$

We know that $a_n \to L$ iff $\frac{1}{a_n} \to \frac{1}{L}$. This means that:

$$\lim_{n \to \infty} a^{\frac{1}{n}} = 1$$

# Root Test

Let $\sum a_n$ be a series. Let $\alpha = \lim \sup |a_n|^{\frac{1}{n}}$. Then, the series:

1. Converges if $\alpha < 1$
2. Diverges if $\alpha > 1$
3. And the test gives no information when $\alpha =1 $

## Proof 1

Suppose that $\alpha < 1$. Then fix $\epsilon > 0$ with $\alpha + \epsilon < 1$. Let $T_N$ be the $N$-th tail. Then $\exists N$ s.t. $|\sup(T_N) - \alpha| < \epsilon$. 

This means that $\sup(T_N) \in (\alpha - \epsilon, \alpha + \epsilon)$. So $\alpha + \epsilon$ is an upper bound for $|a_n|^{\frac{1}{n}}$. Taking the $n$-th power to both sides yields:

$$|a_n| < (\alpha + \epsilon)^n$$

Since $\alpha + \epsilon < 1$, then so is $(\alpha + \epsilon)^n$. Then this converges, so $\sum |a_n|$ converges also. Any absolutely convergent series converges. 

## Proof 2

If $\alpha = \lim \sup |a_n|^{\frac{1}{n}} > 1$ then there is a subset of $|a_n|^{\frac{1}{n}}$ with limit $\alpha > 1$. 

Let $\alpha = 1+a$ and let $\epsilon < a$. Then, for a subsequence:

$$||a_n|^{\frac{1}{n}}-\alpha|<\epsilon$$

We have $1 < \alpha - \epsilon$ because $|a_n|^{\frac{1}{n}} > 1$. This means:

$$1 < \alpha - \epsilon = 1 + a - \epsilon < |a_n|^{\frac{1}{n}}$$

So in comparison, $1 < |a_n|$ for infinitely many $|a_n|$ in the subsequence. Since $a_n \not\to 0$, then $\sum a_n$ diverges by the divergence test.

## Proof 3

By counterexample, we just analyse $\alpha$ for the series $\sum \frac{1}{n}$ and $\sum \frac{1}{n^2}$.

# Ratio Test

Let $\sum a_n$ be a series of nonzero terms. Then $\sum a_n$: 

1. Converges absolutely if $\lim \sup |\frac{a_{n+1}}{a_n}| < 1$
2. Diverges if $\lim \inf |\frac{a_{n+1}}{a_n}| > 1$
3. Else, the test gives no information



