## Theorem

Let $\sum a_n$ be an absolutely convergent series of real numbers and let $\sum a_{\pi(n)}$ be a rearrangement of $\sum a_n$. Then both series converge to the same limit.

## Proof

Suppose $\sum a_n = L$ and let $s_n$ be the sequence of partial sums. 

Consider $N_1$ s.t. $\forall n > N_1$, $|s_n - L| < \frac{\epsilon}{2}$. Consider $N_2$ s.t. $N_2 > N_1$ and $\forall i \geq j > N_2$,

$$\sum_{n=j}^i |a_n| < \frac{\epsilon}{2}$$

Now consider an $N_3$ where $\\{0,1,2,...,N_2\\} \subseteq \\{\pi(0),\pi(1),\pi(2),...,\pi(N_2)\\}$. Note that this is possible because $\pi(n)$ is bijective and we will have $N_3 \geq N_2$. Now fix $n > N_3$. Set $T = \max\\{\pi(k): k \neq n\\}$, which means $T > N_2$. Then:

$$\begin{aligned}
\left|\sum_{k=0}^n a_{\pi(k)}-L\right| &= \left| \sum_{k=0}^{N_2}a_k-L+\sum_{k\leq n \land \pi(k)>N_2} a_{\pi(k)}\right| \\
&\leq \left| \sum_{k=0}^{N_2}a_k-L\right|+\sum_{k\leq n \land \pi(k)>N_2} |a_{\pi(k)}| \\
&< \frac{\epsilon}{2} + \sum_{k=N_2+1}^T |a_k| \\
&< \frac{\epsilon}{2} + \frac{\epsilon}{2} \\
&= \epsilon
\end{aligned}$$

# Limit Point

Let $K \subseteq \mathbb{R}$. A limit point of $K$ is a point $a \in \mathbb{R}$ s.t. there exists a sequence $a_n$ of distinct elements of $K$ converging to $a$. 

## Theorem

Let $K \subseteq \mathbb{R}$. TFAE:

1. There is a sequence of points in $K - \\{a\\}$ converging to $a$
2. There is a sequence of distinct points in $K$ converging to $a$
3. $\forall r > 0$ the interval $(a-r, a+r)$ of radius $r$ centered at $a$ contains infinitely many points of $K$
4. $\forall r > 0$ the interval $(a-r, a+r)$ of radius $r$ centered at $a$ contains at least one point of $K-\\{a\\}$

### Proof 1 -> 2

Let $a_n$ be a sequence in $K - \\{a\\}$ converging to $a$. Either $a_n$ has a constant subsequence, or a subsequence of distinct terms. It is not possible for $a_n$ to have a constant subsequence because such a subsequence must converge to $a$, and the sequence cannot have $a$ in it (because the set difference). So there must be a subsequence of distinct terms which converges to $a$.

### Proof 2 -> 3

Suppose $a_n \to a$ where $a_n \in K$ and $r>0$. Then there exists $N$ s.t. $\forall n > N$, $|a_n-a|<r$ and so $\forall n > N$, $a_n \in (a-r,a+r)$. 

### Proof 3 -> 4

There are infinitely many points of $a_n$ in the interval, so also infinitely many in the interval that are not actually $a$ itself, which is but a singular point.

### Proof 4 -> 1

It is know that the interval contains a point of the set difference. Now $\forall n \in \mathbb{N}$, let $a_n \in (a-\frac{1}{n}, a+\frac{1}{n})$. Fix $\epsilon > 0$. Now choose $N$ s.t. $0 < \frac{1}{N} < \epsilon$ and $\forall n > N$, $|a_n - n| < \frac{1}{n} < \frac{1}{N} < \epsilon$. 

# The limit of a function

Let $K \subseteq \mathbb{R}$ and let $f: K \to \mathbb{R}$ be a function. Let $a$ be a limit point of $K$. Then:

$$\lim_{x \to a} f(x)=L$$ 

iff $\forall \epsilon > 0$ $\exists \delta > 0$ s.t. $x \in K \land 0 < |x-a| < \delta \implies |f(x)-L|<\epsilon$.

## Negating If/Then

$$\neg (p \to q) \equiv p \land \neg q$$

## Theorem

Let $K \subseteq \mathbb{R}$. Let $a$ be a limit point of $K$ and let $f: K \to \mathbb{R}$. TFAE:

1. $\lim_{x \to a} f(x) = L$
2. For each sequence $x_n$ with $x_n \neq a$ and $x_n \to a$ then $\lim_{n \to \infty} f(x_n) = L$
3. For each sequence $x_n$ of distinct points in $K$ and $x_n \to a$ then $\lim_{n \to \infty} f(x_n) = L$

### Proof 1 -> 2

Suppose $x_n$ is a sequence of values in $K$ with $x_n \neq a$ and $x_n \to a$. Fix $\epsilon > 0$. Then $\exists \delta > 0$ s.t. if $0 < |x-a| < \delta$ then $|f(x)-L|<\epsilon$. Since $x_n \to a$ then $\exists N$ s.t. $\forall n > N$ we have $0 < |x_n - a| < \delta$. Now $|f(x_n) - L| < \epsilon$. 

### Proof 2 -> 1

Assume the inverse of 1. That is, the limit does tend to $L$ as $x \to a$ for $f(x)$. Consider $\delta_n = \frac{1}{n}$ and choose $x_n \in K$ s.t. $0 < |x_n - a| < \delta_n$ but $|f(x_n) - L| \geq \epsilon$ here. So we get the inverse of 2 and so the relationship holds by contraposition.

### Proof 2 -> 3

Assume premise 2. Then $a$ appears as a term in $x_n$ at most once. Consider $x_{n_k}$ that omits $a$. Then this is still an infinite sequence of distinct points that converges to $a$.

### Proof 3 -> 2

Assume premise 3. If the subsequence limit tends to $L$ then so does the overall limit. 

## Theorem

Let $f,g$ be functions with domain $K$. Let $a \in \mathbb{R}$. Assume 

$$\lim_{x \to a} f(x) = L$$
$$\lim_{x \to a} g(x) = M$$

Then:

1. If $f(x)=c$ $\forall x \in \mathbb{R}$ then $\lim_{x \to a} f(x) = c$
2. $\forall c \in \mathbb{R}$ $\lim_{x \to a} cf(x) = cL$
3. $\lim_{x \to a} (f(x)+g(x)) = L+M$
4.  $\lim_{x \to a} (f(x) \cdot g(x)) = LM$

## Theorem

Let $f$ have domain $K$ and let $g$ have domain $K'$. Let $a$ be a limit point of the domain of $\frac{f}{g}$. Assume:

$$\lim_{x \to a} f(x) = L$$
$$\lim_{x \to a} g(x) = M$$

If $M \neq 0$ then:

$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M}$$




