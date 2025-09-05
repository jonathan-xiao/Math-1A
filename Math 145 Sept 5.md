## The Well-Ordering Principle

Needs no proof, as it is an axiom. It states:

For $\mathbb{N} = \\{0, 1, 2, ... \\}$, every nonempty subset $S \subseteq \mathbb{N}$ has a least element. 

## Induction Theorem

Suppose $P(n)$ is a mathematical statement $\forall n \in \mathbb{N}$. Suppose $P(0)$ is true and $P(n) \implies P(n+1)$. Then $P(n)$ is true $\forall n \in \mathbb{N}$

### Proof 

Let $S$ be a set $S = \\{n: P(n)$ is false}. Assume that $S \neq \emptyset$. Then, by the WOP, $\exists$ a least element $n \in S$. 

We know that $P(0)$ is true because it is assumed. Therefore $0 \notin S$ so $n > 0$.

Then, $n-1 \in \mathbb{N}$ and $n-1 \notin S$ since $n$ was the least value in $S$. Therefore:

$P(n-1)$ is true $\implies P(n)$ is true $\implies n \notin S$ which is a contradiction. 

Therefore $S$ must be empty and so $P(n)$ is true $\forall n \in \mathbb{Z}$

### Example

Prove that:  

$$\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$$

Let $p(n)$ denote $\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$

$p(1)$ is true. Suppose $\sum_{i=1}^{k} i = \frac{k(k+1)}{2}$. Then,

$$
\begin{align}
\sum_{i=1}^{k+1} i &= \sum_{i=1}^{k} i + k + 1 \\
&= \frac{k(k+1)}{2} + k + 1 \\
&= \frac{k^2 + 3k + 2}{2} \\
&= \frac{(k+1)(k+2)}{2} 
\end{align}
$$

Therefore $p(k+1)$ is true of $p(k)$ is true. By the theorem, $p(n)$ is true $\forall n \in \mathbb{N}$.


## Strong Induction Theorem

Suppose $P(n)$ is a mathematical statement $\forall n \in \mathbb{N}$. Then $\forall n \in \mathbb{N}$, if $P(k)$ is true $\forall k \in \mathbb{N}, k < n$ then $P(n)$ is true.

### Proof

Let $S$ be a set $S = \\{n: P(n)$ is false}. Assume that $S \neq \emptyset$. Then, by the WOP, $\exists$ a least element $n \in S$. 

For $n = 0$, $\nexists k \in \mathbb{N}$ s.t. $k < n$. Therefore, $P(0)$ is vacuously true. Therefore $0 \notin S$ so $n > 0$.

Then, any $k < n$, where $k \in \mathbb{N}$ has $k \notin S$ since $n$ was the least value in $S$. Therefore:

Any $P(k)$ is true where $k < n, k \in \mathbb{N}$ $\implies P(n)$ is true $\implies n \notin S$ which is a contradiction. 

Therefore $S$ must be empty and so $P(n)$ is true $\forall n \in \mathbb{Z}$


## Divisibility

For $a, b \in \mathbb{Z}$, we say $a$ divides $b$ if $\exists c \in \mathbb{Z}$ s.t. $ac = b$. We write $a | b$. 

A number $p$ is prime if $a | p \implies a = \pm 1$ or $\pm p$ where $p \neq \pm 1$. 

## Proposition

If $a, b \in \mathbb{N} \textbackslash \\{0 \\}$ and $n = ab$ then $a \leq n$. If $b>1$ then $a<n$. 

### Proof

For $b \geq 1$ then $ab \geq a \implies n \geq a$

For $b > 1$ then $ab > a \implies n > a$

## Theorem

$\forall n \in \mathbb{N}$ with $n > 1$ then $n$ is a product of finitely many primes. 

### Proof by strong induction

If $n$ is prime, then the theorem holds. 

If $n$ is composite, then $n = ab$ where $a,b > 1$ and $a,b \in \mathbb{N}$. 

By the proposition, $a, b < n$. By strong induction hypothesis, $a$ and $b$ are the products of finitely many primes themselves. Therefore, $n$ is the product of finitely many primes. 










