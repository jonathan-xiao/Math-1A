## Proposition

Suppose that $n,k \in \mathbb{Z}^+$ and $\sqrt[k]{n}$ is rational. Then $\sqrt[k]{n} \in \mathbb{Z}^+$. 

### Proof

Let $\sqrt[k]{n} = a/b$ where $a,b \in \mathbb{Z}^+$. Suppose that $\mathrm{gcd}(a,b)=1$. 

We have that $nb^k = a^k$. If $b \neq 1$, let $p | b$. Then $p|a^k \implies p|a$. Then we have $p | \mathrm{gcd}(a,b)$ so $p|1$ which is impossible so $b=1$. 

That means that $a/b$ is an integer, so $\sqrt[k]{n}$ is an integer. 

## Proposition

$e$ is irrational. 

### Proof

$$e = \sum_{n=0}^{\infty} \frac{1}{n!}$$

Suppose that $e=a/k$ where $a,k \in \mathbb{Z}^+$. Then we have:

$$\begin{aligned}
a(k-1)! &= ek! \\
&= k! \sum_{n=0}^{\infty} \frac{1}{n!} \\
&= \sum_{n=0}^{k} \frac{k!}{n!} + \sum_{n=k+1}^{\infty} \frac{k!}{n!}
\end{aligned}$$

Both the left hand side and the first term on the right are integers. Therefore, the last term is an integer. 

We have 

$$
\begin{aligned}
0 &< \sum_{n=k+1}^{\infty} \frac{k!}{n!} \\
&= \frac{1}{k+1} + \frac{1}{(k+1)(k+2)} + ... \\
&< \frac{1}{1+k} + \frac{1}{(k+1)^2} + ... \\
&= \frac{(1+k)^{-1}}{1-(1+k)^{-1}} \\
&\leq 1
\end{aligned}$$

No integer exists between 0 and 1, exclusive, so we have a contradiction, and hence $e$ is irrational. 

## Integral Domains

A commutative ring $R$ is an integral domain if $\forall a,b \in R$, if $ab=0$ then $a=0$ or $b=0$. 

### Proposition

If $R$ is an integral domain, then $\forall a,b,c \in R$, if $a \neq 0$ and $ac=ab$ then $b=c$. 

#### Proof

We have then $ac - ab = a(c-b) = 0$. Since $a \neq 0$ then $c-b = 0$ so $c=b$. 

### Definition

An element $a \in R$ is a unit if $a | 1$. We say $R^* = \\{\mathrm{units}\\}$. 

For the integers, the units are $\pm 1$. For the rationals, the units are any element besides 0.

### Definition

An element $p \in R$ is irreducible if $p \notin R^\*$ and if $ab=p$ then $a \in R^*$ then $b \in R^\*$. 

## Euclidean Domain

$R$ is a Euclidean Domain if $\exists f: R \rightarrow \mathbb{N}$ s.t. 

1. $f(a) \leq f(ab)$ where $b$ is nonzero
2. $\forall a,b \in R$ and $b$ is nonzero, $\exists q,r \in R$ s.t. $a = bq+r$ and $f(r)<f(b)$.

### Examples

We have the integers, where $f(x) = |x|$. 

We have $\mathbb{Z}\[i\]$, where $f(x+yi) = x^2+y^2$. 








