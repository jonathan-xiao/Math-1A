## Theorem

If $a_n$ is a Cauchy sequence with a convergent subsequence, then $a_n$ converges. 

### Proof

Suppose $a_n$ is Cauchy and $a_{n_k} \to L$. Fix $\epsilon > 0$. Now consider $N_1$ s.t. $\forall k > N_1$ $|a_{n_k} - L| <\frac{\epsilon}{2}$. 

Now consider $N_2$ s.t. $\forall n,m > N_2$, $|a_n - a_m| < \frac{\epsilon}{2}$ 

Let $N = \max(N_1, N_2)$. Then $N < N+1 \leq n_{N+1}$. This is because $n_i$ is a strictly increasing sequence of natural numbers, and must grow faster than any two consecutive natural numbers. 

Then,

$$\begin{aligned}
|a_n - L| &\leq |a_n - a_{n_{N+1}}| + |a_{n_{N+1}} - L| \\
&< \frac{\epsilon}{2} + \frac{\epsilon}{2} \\
&= \epsilon
\end{aligned}$$

Note that we used the triangle inequality, and we know that $a_{n_{N+1}}$ is beyond $a_N$, so we can apply both facts. 

## Theorem

TFAE:

1. $a_n \to L$
2. Every subsequence of $a_n$ converges to $L$
3. Every subsequence of $a_n$ has itself a subsequence that converges to $L$

### Proof

1 to 2. Suppose $a_n \to L$. Fix $\epsilon > 0$. Consider $N$ s.t. $\forall n > N$, $|a_n-L| < \epsilon$. 

Then we know that $\forall k > N$ since $k \leq n_k$ then $|a_{n_k} - L| < \epsilon$. If $k$ is beyond $N$, then $n_k$ is for sure. 

2 to 3. Any arbitrary subsequence of $a_{n_k}$ is also a subsequence of $a_n$. Therefore, such a subsequence converges to $L$.

3 to 1. Proof by contrapositive. Begin by supposing that $a_n$ does not converge to $L$. That is, $\exists \epsilon > 0$ s.t. $\forall N$, $\exists n > N$ s.t. $|a_n - l| \geq \epsilon$. 

For $N=1$, choose $n_1$ s.t. $|a_{n_1} - L| \geq \epsilon$. 
Strong induction. Suppose all the statements for $N = 1, ..., k-1$ are true. For $N=k$, there exists, and so we choose $n_{k+1} > n_k$ s.t. $|a_{n_{k+1}} - L| \geq \epsilon$. 

Hence for all $k$, $|a_{n_k}| \geq \epsilon$. This means that $a_{n_{k_j}}$ does not converge to $L$. Hence the contrapositive is true to 3 to 1 is true. 

## Theorem

$a_n \to \infty$ iff every subsequence of $a_n$ converges to $\infty$. A similar theorem holds for negative infinity. 

## Theorem

Every sequence has a monotonic subsequence

### Proof

Let $a_n$ be a sequence. Define $a_n$ as dominant if it is strictly greater than all remaining terms in the sequence. That is,

$$a_n > a_m \forall m > n$$

Suppose there are infinite dominant terms. Then each successive dominant term must be strictly less than the previous dominant term, so there is a monotonic decreasing subsequence. 

Suppose there are finite dominant terms. Consider $a_n$ which is beyond all the dominant terms. Then $a_{n_1}$ is not dominant, so there exists $a_{n_2}$ that is beyond it and larger than it. By induction, for every $a_{n_k}$ there is a term $a_{n_{k+1}}$ that is strictly greater than it. So there is a monotonic increasing subsequence. 

## Theorem

$\mathbb{R}$ is complete. 

### Proof

Suppose that $a_n$ is Cauchy. We know that $a_n$ has a monotonic subsequence. Such a subsequence must be Cauchy itself, and as such it is bounded. 

Every bounded subsequence that is Cauchy must converge. Therefore, if the subsequence converges, the $a_n$ converges. 

## Theorem

Every bounded sequence has a convergent subsequence

### Proof

Suppose $a_n$ is a bounded sequence. Then, $a_n$ has a monotonic subsequence that is also bounded. Every monotonic bounded sequence must converge. 

# Definition

A subsequential limit of $a_n$ is an $L$ s.t. some subsequence of $a_n$ has the limit $L$. This value can be infinite.

## Theorem

Let $a_n, b_n, c_n$ be sequences. If $a_n \leq b_n \leq c_n$ $\forall n$ and:

$$\lim_{n \to \infty} a_n = \lim_{n \to \infty} c_n = L$$ 

$$\implies \lim_{n \to \infty} b_n = L$$

### Proof

Fix $\epsilon > 0$. We know that then $\exists N_1$ s.t. $\forall n > N_1$ then $|a_n - L| < \epsilon$. 

Also, $\exists N_2$ s.t. $\forall n > N_2$ then $|c_n - L| < \epsilon$. 

Therefore pick $N = \max(N_1, N_2)$. We have $L - \epsilon < a_n \leq b_n \leq c_n < L + \epsilon$. 

Therefore, $b_n \in (L-\epsilon, L+\epsilon)$. So $b_n \to L$. 

## Theorem

$L$ is a subsequential limit of $a_n$ iff $\forall \epsilon > 0$ then the following set is infinite.

$$X_\epsilon = \\{ n \in \mathbb{N}: |a_n - L| < \epsilon\\}$$

### Proof

Forward. $L$ is a subsequential limit of $a_n$ so there are infinite values of $a_{n_k}$ s.t. $|a_{n_k} - L| < \epsilon$ for any $\epsilon > 0$. 

Backward. Suppose that $X_\epsilon$ is infinite for any $\epsilon$. Define $L - 1 < a_{n_1} < L+1$. 

Suppose that $a_{n_k}$ is defined so that 

$$L - \frac{1}{j} < a_{n_j} < L + \frac{1}{j}$$

Since $X_{\frac{1}{k+1}}$ is infinite, $\exists n_{k+1}$ larger than all the $n_j$ s.t. 

$$L - \frac{1}{k+1} < a_{n_{k+1}} < L + \frac{1}{k+1}$$

Both the right and left hand sides converge to $L$ as $k \to \infty$. Therefore, by the squeeze theorem, $a_{n_{k+1}}$ converges to $L$. 

## Theorem

If $a_n$ is not bounded above, it has a subsequence that converges to infinity.

### Proof

Define $a_{n_1} > 1$. Suppose we have a subsequence $a_{n_j}$ s.t. for each $j$, $a_{n_j} > j$. 

Then there exists a term larger than $k+1$ and every other $a_{n_j}$ terms before it. Call this term $a_{n_{k+1}}$ Then by induction, $a_{n_k} \to \infty$. 

## Theorem

Let $a_n$ be any sequence. There exists a subsequence whose limit is lim sup $a_n$. 

### Proof

If $a_n \to \infty$, then we know that if has a subsequence that converges to infinity. Then lim sup $a_n = \infty$, which is the limit of the subsequence.

If $a_n$ is bounded above, then lim sup $a_n = L$. 

Fix $\epsilon > 0$. Since $\sup T_N \to L$, then $\exists N_0$ s.t. $\forall N > N_0$, $|\sup T_N - L| < \epsilon$. 

Therefore, $\sup T_N < L+\epsilon$ for $n > N_0 + 1$ so $a_n < L+\epsilon$. 

Suppose that there are finite natural numbers $n$ where $|a_n - L| < \epsilon$. Then $\exists N_1 > N_0$ s.t. $\forall n > N_1$ we have $|a_n - L| \geq \epsilon$. We go past the last value where $|a_n - L| < \epsilon$ is true.

So $a_n \leq L + \epsilon$, rejecting the higher case. Therefore, $\sup T_N \leq L - \epsilon$ so $\lim \sup a_n \leq L - \epsilon$. This is a contradiction against $\lim \sup a_n = L$. 

## Theorem

Let $S$ denote the set of subsequence limits of $a_n$. 

1. $S$ is nonempty
2. $\sup S = \lim \sup a_n$ and $\inf S = \lim \inf a_n$
3. $S = \\{L\\}$ iff $a_n \to L$

### Proof

From earlier, $\lim \sup a_n$ is a subsequence limit of $a_n$ so $S$ cannot have nothing in it.

Let $L \in S$. Then $a_{n_k} \to L$. Note that the $N$-th tail $T'\_N$ of $a_{n_k}$ is a subset of the $N$-th tail $T_N$ of $a_n$. 

$$\inf T_N \leq \inf T'_N$$
$$\sup T'_N \leq \sup T_N$$

So we know that

$$\lim \inf a_n \leq \lim \inf a_{n_k} = L = \lim \sup a_{n_k} \leq \lim \sup a_n$$

We know this is true for any $L \in S$, so it must always be true that

$$\lim \inf a_n \leq \inf S \leq \sup S \leq \lim \sup a_n$$

But the lim sup and the lim inf are themselves in $S$. So the only way this is possible is if

$$\lim \inf a_n = \inf S$$ 
$$\lim \sup a_n = \sup S$$

Then from this fact, if $S = \\{L\\}$ then $\sup S = \lim \sup a_n = L = \lim \inf a_n = \inf S$. 

Therefore, $a_n$ must converge to $L$. 




