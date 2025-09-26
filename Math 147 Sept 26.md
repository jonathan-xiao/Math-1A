# Bounded Sequences

If $a_n$ is bounded, then $\sup T_N$ and $\inf T_N$ (the tails of the sequence after $N$) are finite and bounded. Both the supremum and the infimum of the tails of $a_n$ are bounded and monotonic. This means that $\lim \sup a_n$ and $\lim \inf a_n$ are finite and bounded. 

If $a_n$ is not bounded above, then $\sup T_N = \infty$ so $\lim sup a_n = \infty$. Then $\lim inf a_n = \infty$ also. The same situation applies oppositely for $a_n$ not bounded below.

## Theorem

If $\lim \inf a_n = \lim \sup a_n$ then $\lim a_n$ is defined and $\lim \sup a_n = \lim a_n = \lim \inf a_n$. 

### Proof

The proof is trivial if both the lim inf and lim sup go to infinity. So suppose they do not.

Fix $\epsilon > 0$. Since $s_N \rightarrow L$ then there is a $N_1$ s.t. $\forall n > N_1$, $|L-s_N|<\epsilon$. 

Therefore, past this number $N_1$, the terms of the sequence should be even closer to $L$. So $|L-\sup T_{N_1+1}| < \epsilon$. This means that $\sup T_{N_1+1}$ is at most $\epsilon$ away from $L$, so $\sup T_{N_1+1} < L + \epsilon$. This means $L + \epsilon$ is an upper bound for $T_{N_1+1}$. 
Similarly, we can find a $N_2$ so that $L-\epsilon$ is a lower bound for $T_{N_2+1}$. 

Take $N = \max(N_1, N_2)$. Then past this, we must have both an upper and a lower bound. So then $\forall n > N$ we have $L-\epsilon < a_n < L+\epsilon$. 

This means $|L-a_n|<\epsilon$, so $a_n \to L$. 

# Cauchy Sequences

A sequence is said to be Cauchy if $\forall \epsilon > 0$ $\exists N$ s.t. $\forall n,m > N$ we have $|a_n - a_m| < \epsilon$. 

## Theorem

In the real numbers, every convergent sequence is Cauchy.

### Proof

Suppose $a_n \to L$. Fix $\epsilon > 0$. Then $\exists N$ s.t. $\forall n > N$, $|a_n-L| < \frac{\epsilon}{2}$. 

Let $n,m > N$. By the triangle inequality:

$$\begin{aligned}
|a_n-a_m| $\leq |a_n-L|+|a_m-L| \\
&< \frac{\epsilon}{2} + \frac{\epsilon}{2} \\
&= \epsilon
\end{aligned}$$

Completes the proof.

## Theorem

Every Cauchy sequence is bounded.

### Proof

Let $a_n$ be a Cauchy sequence. For $\epsilon=1$ in particular, $\exists N$ s.t. $\forall n, m >N$, $|a_n-a_m|<1$. 

Let $a = a_{N+1}$ (a term after this point). Then $\forall n > N$, $|a_n-a|<1$ which means $a-1 < a_n < a+1$. 

Then:

$$B = \max(\\{a_n: n \leq N\\} \cup \\{a+1\\})$$
$$C = \min(\\{a_n: n \leq N\\} \cup \\{a-1\\})$$

are bounds for $a_n$. 

## Theorem 

In the real numbers, every Cauchy sequence converges.

### Proof

Let $a_n$ be a Cauchy sequence, which we know is bounded by before. Therefore, both the lim sup and the lim inf are bounded also. 

Fix $\epsilon > 0$. Consider $N$ s.t. $\forall n,m > N$, then $|a_n-a_m|<\epsilon$. 

Fix $m > N$. Then $a_m + \epsilon$ is an upper bound for the $N$th tail. The supremum of the $N$th tail is the smallest upper bound, so:

$$s_N = \sup T_N \leq a_m + \epsilon$$

Then, we know that $s_N - \epsilon \leq a_m$ for all $m > N$. So $s_N - \epsilon$ is a lower bound for this tail. 

$$s_N - \epsilon \leq \inf T_N = b_N$$ 

This means $s_N \leq b_N + \epsilon$. In a comparison across, we have

$$\lim \sup a_n \leq s_N \leq b_N + \epsilon \leq \lim \inf + \epsilon$$

The supremum must be larger than the infimum, so we have both $\lim \sup a_n \leq \lim \inf a_n$ and $\lim \inf a_n \leq \lim \sup a_n$.

Therefore they are equal and so $a_n$ converges. 

# Subsequence

Suppose $a_n$ is a sequence. If $a_k$ is a strictly increasing sequence of natural numbers, then $t_k = a_{n_k}$. 

## Theorem

If $a_n$ is a Cauchy sequence, then every subsequence is also Cauchy.

### Proof

If $n_k$ is a strictly increasing sequence of natural numbers, then $k \leq n_k$ because $k$ is the slowest growing sequence of natural numbers (the consecutive ones). 

Let $a_n$ be Cauchy and $a_{n_k}$ be a subsequence. Fix $\epsilon > 0$. Consider $N$ s.t. $\forall n,m > N$, $|a_n-a_m| < \epsilon$. 

Let $k,j$ be natural numbers such that $N < k \leq m_k$ and $N < j \leq n_j$. Since they are past $N$, then $|a_{m_k} - a_{n_j}| < \epsilon$. 



