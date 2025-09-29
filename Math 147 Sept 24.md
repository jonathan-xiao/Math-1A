## Theorem

If $a_n \rightarrow L$ and $b_n \rightarrow L'$ then $(a_n+b_n) \rightarrow L+L'$. 

### Proof

Fix $\epsilon > 0$. Since $a_n \rightarrow L$ then $\exists N_1$ s.t. $\forall n > N_1$, $|a_n-L| \leq \frac{\epsilon}{2}$. Since $b_n \rightarrow L'$ then $\exists N_2$ s.t. $\forall n > N_2$, $|b_n-L'| \leq \frac{\epsilon}{2}$. 

Let $N = \max(N_1, N_2)$. Then $\forall n > N$ we have:

$$\begin{aligned}
|a_n+b_n-(L+L')| &= |(a_n-L)+(b_n-L')| \\
&\leq |a_n-L|+|b_n-L'| \\
&< \frac{\epsilon}{2}+\frac{\epsilon}{2} \\
&= \epsilon
\end{aligned}$$

## Theorem

If $a_n \rightarrow L$ and $b_n \rightarrow L'$ then $(a_nb_n) \rightarrow LL'$.

### Proof

We want to end up with $|a_nb_n-LL'|<\epsilon$ by the very end. So we need a way to connect this to what we are given. 

$$\begin{aligned}
|a_nb_n-LL'| &= |a_nb_n-a_nL'+a_nL'-LL'| \\
&\leq |a_nb_n-a_nL'|+|a_nL'-LL'| \\
&= |a_n||b_n-L'|+|L'||a_n-L|
\end{aligned}$$

Now we can see it. We want each of them to end up with some kind of $\frac{\epsilon}{2}$ so that we add to $\epsilon$. 

For the first part, we want $|a_n||b_n-L'| < \frac{\epsilon}{2}$ which means we want $|b_n-L'|<\frac{\epsilon}{2|a_n|}$. 

Note that because $a_n$ approaches a limit $L$, it is bounded. So $|a_n|$ is a sequence bounded above. There must exist $M$ such that $|a_n|<M$ for all $n$. This means we want $|b_n-L'|<\frac{\epsilon}{2M}$.

Remember we also want the other part, $|L'||a_n-L| < \frac{\epsilon}{2}$. But here it is possible that $L'=0$. So we just need to add 1 to force it positive. 

We need $|a_n-L|<\frac{\epsilon}{2(|L'|+1)}$. 

Therefore, we just write it all backwards.

Fix an arbitrary $\epsilon >0$. Then there exists $M$ s.t. $|a_n|<M$. 

Since $a_n \rightarrow L$ then $\exists N_1$ s.t. $\forall n > N_1$, $|a_n-L| \leq \frac{\epsilon}{2(|L'|+1)}$. Since $b_n \rightarrow L'$ then $\exists N_2$ s.t. $\forall n > N_2$, $|b_n-L'| \leq \frac{\epsilon}{2M}$

Then let $N = \max(N_1, N_2)$. Hence for all $n > N$. 

$$\begin{aligned}
|a_n-b_n-LL'| &\leq |a_nb_n-a_nL'|+|a_nL'-LL'| \\
&= |a_n||b_n-L'|+|L'||a_n-L| \\
&< M\frac{\epsilon}{2M} + |L'|\frac{\epsilon}{2(|L'|+1)} \\
&\leq \frac{\epsilon}{2}+\frac{\epsilon}{2} \\
&= \epsilon
\end{aligned}$$

## Lemma

Let $a_n \rightarrow L$. Suppose that for all $n$, $a_n \neq 0$ and $L \neq 0$. Then $\inf\\{|a_n| : n \in \mathbb{N}\\}>0$. 

### Proof

Since $a_n \rightarrow L$ then $\exists N$ s.t. $\forall n > N$ we have $|a_n-L| \leq \frac{|L|}{2}$. 

Assume that $\forall n >N$, that $|a_n| \leq \frac{|L|}{2}$. Then we have:

$$\begin{aligned}
|L| = |L-a_n+a_n| &\leq |L-a_n|+|a_n| \\
&< \frac{|L|}{2} + \frac{|L|}{2} \\
&= |L|
\end{aligned}$$

This is a contradiction, so $\forall n >N$, we have that $|a_n| > \frac{|L|}{2}$.

Now consider $m = \min(\\{|a_n|:n \leq N\\} \cup \\{\frac{|L|}{2}\\})$. 

Well $|a_n|$ is larger than $\frac{|L|}{2}$ so this $m$ is smaller than every $|a_n|$. Since $a_n \neq 0$ then $m \neq 0$. Every $|a_n|$ is positive, and so $m$ is positive also.

Well if $m$ is a minimum and greater than zero, we have: $\inf\\{|a_n| : n \in \mathbb{N}\\} \geq m >0$.

## Theorem

If $a_n \rightarrow L$ and $a_n \neq 0$ and $L \neq 0$ then $\frac{1}{a_n} \rightarrow \frac{1}{L}$. 

### Proof

Fix $\epsilon > 0$. By the lemma, there exists $m > 0$ s.t. $|a_n|\geq m$ for all $n$. (This $m$ is now the infimum).

Since $a_n \rightarrow L$ then $\exists N$ s.t. $\forall n > N$ we have:

$$|L-a_n| < m|L|\epsilon$$

$$|\frac{1}{a_n}-\frac{1}{L}| = |\frac{L-a_n}{a_nL}| \leq \frac{|L-a_n|}{m|L|} < \epsilon$$

## Definition

For a sequence $a_n$ we write 

$$\lim_{n \to \infty} a_n = \infty$$

if for all $m > 0$ $\exists N$ s.t. $\forall n > N$ we have $a_n > M$. 

## Theorem

Let $a_n, b_n$ be sequences s.t. 

$$\lim_{n \to \infty} a_n = \infty$$
$$\lim_{n \to \infty} b_n > 0$$

Then:

$$\lim_{n \to \infty} a_nb_n = \infty$$

### Proof

Let $M>0$ be arbitrary. Pick some $0 < m < L$. Since $b_n \rightarrow L$ and $b_n > 0$, then $\exists N_1$ s.t. $\forall n > N_1$, $b_n > m$. Since $a_n \rightarrow \infty$, then $\exists N_2$ s.t. $\forall n > N_2$, $a_n > \frac{M}{m}$. 

Let $N = \max(N_1, N_2)$. Then $\forall n > N$ we have $a_nb_n > \frac{M}{m} \cdot m = M$. 

## Theorem

For a sequence $a_n$ where $a_n > 0$, then $a_n \rightarrow \infty$ iff $\frac{1}{a_n} \rightarrow 0$. 

### Proof

Forward. Assume $a_n \rightarrow \infty$. Fix $\epsilon > 0$. Consider $N$ s.t. $\forall n>N$, then $a_n > \frac{1}{\epsilon}$. Then, $\epsilon > \frac{1}{a_n} = |\frac{1}{a_n}-0|$. 

Backward. Assume $\frac{1}{a_n} \rightarrow 0$. Fix $M>0$. Consider $N$ s.t. $\forall n > N$, $|\frac{1}{a_n}-0| < \frac{1}{M}$. Then $a_n > M$ $\forall n > N$. 

## Definition

A sequence $a_n$ is increasing if $a_n \leq a_m$ if $n < m$. A sequence $a_n$ is decreasing if $a_n \geq a_m$ if $n < m$. Both cases are considered monotonic. 

## Theorem

Every bounded monotonic sequence converges.

### Proof

Let $(a_n)_{n \in \mathbb{N}}$ be a increasing bounded sequence. Now let $X = \\{a_n : n \in \mathbb{N}\\}$. $X$ is nonempty and bounded above. Therefore, $\sup(X)$ exists. 

Fix $\epsilon > 0$. By theorem 1.14, there exists $\exists a_N \in X$ s.t. $|a_N - \sup(X)| < \epsilon$. 

Then $\forall n > N$ we have $a_N \leq a_n \leq \sup(X)$. 

There $|a_n - \sup(X)| \leq |a_N -\sup(X)| < \epsilon$

The proof is similar for a decreasing sequence. 

## Theorem

If $a_n$ is unbounded increasing, $a_n \rightarrow \infty$. If $a_n$ is unbounded decreasing, $a_n \rightarrow -\infty$. 

If $A \subseteq B$ then we know:

$$\inf(A) \geq \inf(B)$$
$$\sup(A) \leq \sup(B)$$

Consider $s_N = \sup\\{a_n : a > N\\}$. 

This is a set of sequences of elements in the sequence where the index is after a particular $N$ ("tails"). 

Well,

$s_N$ is a monotonic decreasing sequence itself. We say the supremum of set of $s_N$ is the lim sup of $a_n$. 

$$\lim \sup a_n = \lim_{N \to \infty} \sup\\{a_n:n > N\\}$$

And if $a_n$ is not bounded above, then the lim sup is infinity. Similarly, the lim inf is the limit of all the infimums of the tails.

$$\lim \inf a_n = \lim_{N \to \infty} \inf\\{a_n:n > N\\}$$




