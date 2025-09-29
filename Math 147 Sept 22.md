## Theorem

$$\lim_{n \to \infty} \frac{2n-7}{3n^3-2}=0$$

### Proof

Fix $\epsilon > 0$. We want:

$$|\frac{2n-7}{3n^3-2}-0|<\epsilon$$

Note that when $n > 7$ then 

$$\frac{2n-7}{3n^3-2}>0$$

Therefore, the absolute value brackets can come off. Also, for $n \geq 1$, we have $2n-7 \leq 2n$ and $3n^3-2 \geq 3n^3-2n^3 = n^3$. This means we can replace the numerator with a larger term and the denominator with a smaller term. We have:

$$\frac{2n-7}{3n^3-2} \leq \frac{2n}{n^3}$$

Let $\frac{2n}{n^3} < \epsilon$, which means that $n > \sqrt{\frac{2}{\epsilon}}$. Now let $N = \max\\{7, \sqrt{\frac{2}{\epsilon}}\\}$ and work forwards. 

Fix $\epsilon>0$. Then choose:

$$N = \max\\{7, \sqrt{\frac{2}{\epsilon}}\\}$$

So that we have for all $n>N$,

$$n > \sqrt{\frac{2}{\epsilon}}$$

This means that 

$$\epsilon > \frac{2n}{n^3} \geq \frac{2n-7}{n^3-2} = |\frac{2n-7}{n^3-2}-0|$$

Therefore, $L=0$. 

## Theorem

If a sequence $a_n$ converges to a limit, the limit is unique.

### Proof

Suppose the sequence converges. Then assume we have two limits, $L$ and $L'$. Fix $\epsilon > 0$. 

Since $a_n \rightarrow L$, $\exists N_1$ s.t. $\forall n > N_1$, we have $|a_n - L| < \frac{\epsilon}{2}$.
Since $a_n \rightarrow L'$, $\exists N_2$ s.t. $\forall n > N_2$, we have $|a_n - L'| < \frac{\epsilon}{2}$.

Consider $n$ as the maximum of $(N_1, N_2)$. We have:

$$\begin{aligned}
|L-L'| &= |L-a_n - (L'-a_n)| \\
&\leq |L-a_n| + |L'-a_n| \\
&< \frac{\epsilon}{2}+\frac{\epsilon}{2} \\
&= \epsilon
\end{aligned}$$

By theorem 1.19, $|L-L'| = 0$ so $L = L'$. 

## Theorem

$a_n = (-1)^n$ diverges.

Let $L$ be a potential limit. Consider $\epsilon = 1$. Pick an arbitrary $N \in \mathbb{R}$. 

Case 1: $L \geq 0$. Here, choose $n > N$ that is odd, which means $|L - a_n| = |L-(-1)| \geq 1$.

Case 2: $L < 0$. Here, choose $n > N$ that is even, which means $|L - a_n| = |L-1| \geq 1$.

This means there is no $N$ for $\epsilon = 1$, so this limit diverges. 

## Definition

Let $I = \mathbb{N}$. A sequence $(a_n)_{n \in I}$ is said to be bounded if $\\{a_n, n \in I\\}$ is a bounded set. 

## Theorem

Any convergent sequence is bounded.

### Proof

Suppose that $a_n \rightarrow L$. For $\epsilon = 1$ we have $\exists N$ s.t. $\forall n>N$, $|a_n-L|<1$. 

Therefore, $a_n \in (L-1, L+1)$, which is to say $L-1 < a_n < L+1$. 

Let:

$$B = \max(\\{a_n: n\leq N \\} \cup \\{L+1\\})$$
$$C = \min(\\{a_n: n\leq N \\} \cup \\{L-1\\})$$

This means $\forall n$, $C \leq a_n \leq B$. Hence the set and the limit are bounded.

## Theorem

If $a_n \rightarrow L$ and $t \in \mathbb{R}$ then $ta_n \rightarrow tL$. 

### Proof

If $t=0$ then $a_nt = 0$ $\forall n$. This is trivial.

If $t \neq 0$ we then want $|ta_n-tL|<\epsilon$. 

Fix $\epsilon>0$. Since $a_n \rightarrow L$ then $\exists N$ s.t. $\forall n > N$, we have $|a_n-L|<\frac{\epsilon}{|t|}$. Therefore,

$$\begin{aligned}
|ta_n-tL| &\leq |t||a_n-L| \\
&< |t|\frac{\epsilon}{|t|} \\
&= \epsilon
\end{aligned}$$

Hence, proved.



