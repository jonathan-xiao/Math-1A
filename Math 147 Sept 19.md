# Archimedean Property

## Corollary 

Let $a,b \in \mathbb{R}$. If $a,b > 0$ then for some $n \in \mathbb{N}$, $na > b$. 

### Proof

By theorem 1.16, there exists a natural number $n$ s.t. $n > \frac{b}{a}$. Then, it follows that $na > b$. 

## Theorem

There are no real infinitesimals. Let $r \in \mathbb{R}$, where $r>0$. If $r \leq \epsilon$ $\forall \epsilon > 0$ then $r = 0$. 

### Lemma

For every $\epsilon \in \mathbb{R}$ where $\epsilon > 0$, there exists $n \in \mathbb{N}$ s.t. $\frac{1}{n} < \epsilon$. 

#### Proof Lemma

$\forall a,b \in F$, if $a > b > 0$ then $b^{-1} > a^{-1} > 0$ by theorem 1.8.7. Suppose that $\epsilon > 0$. By theorem 1.16, there exists $n \in \mathbb{N}$ s.t. $n > \frac{1}{\epsilon} > 0$. By theorem 1.8.7, this implies that $\epsilon > 1/n$. 

### Proof

Now let $r \in \mathbb{R}$ where $r \geq 0$. Suppose that $r \leq \epsilon$ $\forall \epsilon > 0$. Now suppose $r \neq 0$. 

This would mean $r > 0$, so by corollary 1.17, $\exists n \in \mathbb{N}$ s.t. $\frac{1}{r}<n$ which is the same as $\frac{1}{n}<r$. Then, choose $\epsilon = \frac{1}{n}$. Then we would have $\epsilon < r$, which is a contradiction. Hence $r=0$ so there are no infinitesimals. 

## Theorem

Let $x, y \in \mathbb{R}$. Suppose that for all positive real numbers $\epsilon$, $x < y + \epsilon$. Then $x \leq y$. 

### Proof

Fix $x,y \in \mathbb{R}$ and suppose that $x < y + \epsilon$ where $\epsilon > 0$. Assume that $x > y$. Then we know that $x - y > 0$. Since $\epsilon > 0$, let $\epsilon = x-y$. Then $x < y + x -y \implies x < x$.

Contradiction. Therefore $x \leq y$. 

## Theorem

Let $t$ be a positive real number and $S$ be a nonempty subset of the real numbers, bounded above. Define:

$$tS = \\{ts : s \in S\\}$$

Then $tS$ is nonempty bounded above and $\mathrm{sup}(tS) = t\mathrm{sup}(S)$. 

### Proof

Suppose that $t \in \mathbb{R}^+$ and $S \subseteq \mathbb{R}$ be bounded and nonempty. By the completeness axiom, $r = \mathrm{sup}(S)$ exists. 

Let $y \in tS$. Therefore, we have $y = ts$ for some $s \in S$. For this $s$, we know $s \leq r$. 

Since $t > 0$, we have $ts \leq tr$ which means since $S$ is nonempty, $tS$ must also be nonempty. Then we can conclude that $tS$ is bounded above by $tr$. 

Let $u$ another upper bound of $tS$. We know that $u \geq ts \implies \frac{u}{t} \geq s$. So $\frac{u}{t}$ is another upper bound of $S$. 

Since $r = \mathrm{sup}(S)$, we know $r \leq \frac{u}{t}$. This means $rt \leq u$. This shows that $\mathrm{sup}(tS) = t\mathrm{sup}(S)$. 

# Indexing

Let $I$ be an indexing set and let $X$ be a set. A function $f: I \rightarrow X$ is an indexing of elements $X$ by $I$. 

For $i \in I$, we write $f(i) = x_i$. The range of $f$ is $(x_i)_{i \in I}$ and is called the family of elements indexed by $I$. 

Let $(A_i)_{i \in I}$ be a collection of sets indexed by $I$. The union over $i \in I$ of the $A_i$ sets is:

$$\bigcup_{i \in I} A_i = \\{ x: \exists i \in I \space \mathrm{s.t.} \space x \in A_i\\}$$

The intersection over $i \in I$ of the $A_i$ sets is:

$$\bigcap_{i \in I} A_i = \\{ x: \forall i \in I \space \mathrm{s.t.} \space x \in A_i\\}$$

A descending chain is a family of sets $(A_i)_{i \in \mathbb{N}}$ s.t.

$$... \subseteq A_3 \subseteq A_2 \subseteq A_1$$

## Theorem

Let $(C_i)_{i \in \mathbb{N}}$ be a descending chain of nonempty closed intervals in $\mathbb{R}$. Then the intersection of the $(C_i)$ is nonempty. 

### Proof

Let $(C_i)_{i \in \mathbb{N}}$ be a nonempty closed interval $C_i = \[a_i, b_i\]$ where $a_i \leq b_i$. For each $i$, it is known that $a_i \leq a\_{i+1}$ and $b_i \geq b\_{i+1}$. 

Define $A = \\{a_i : i \in \mathbb{N}\\}$. For each $i$, $a_i \leq b_i \leq b_1$. This means that $b_1$ is an upper bound for $A$. By the completeness axiom, it must then have a supremum. Let this supremum be $r$. 

Fix an arbitrary $k$. Since $r$ is an upper bound of $A$, $r \geq a_k$. Take any $a_i \in A$. 

If $i \leq k$ then $a_i \leq a_k \leq b_k$. If $i > k$ then $a_i \leq b_i \leq b_k$. Either way, $b_k$ is an upper bound for $A$. Since $r$ is the supremum of $A$, then $r \leq b_k$. 

Therefore, $r \in \[a_k, b_k\]$, a nonempty closed interval. 

# Sequences

An infinite sequence is a collection $(a_n)_{n \in \mathbb{N}}$ of elements indexed by the natural numbers. Each $a_i$ is called a term. Usually, we are given a general expression on $n$ to give us $a_n$.

## Convergence

A sequence of real numbers $a_n$ converges to $L$ provided that $\forall \epsilon > 0$ $\exists N$ s.t. $\forall n > N$, 

$$|a_n - L| < \epsilon$$

If $a_n$ converges to a limit $L$, we say the sequence converges. Otherwise, it is divergent. For a convergent series, we can write:

$$\lim_{n \to \infty} a_n = L$$

## Theorem

$$(\frac{1}{n^2})_{n \in \mathbb{N}}$$

converges to $L=0$. 

### Proof

Fix an arbitrary $\epsilon > 0$. We work backwards to find a good value of $N$. We want to prove that $|\frac{1}{n^2} - 0| < \epsilon$. So solve for $n$ and we get $n > \frac{1}{\sqrt{\epsilon}}$, which is what we pick for $N$. 

Now we work the other way. 

$$n > \frac{1}{\sqrt{\epsilon}}$$
$$n^2 > \frac{1}{\epsilon}$$
$$\epsilon > \frac{1}{n^2} = |\frac{1}{n^2}-0|$$

Therefore, $L = 0$. 























 

