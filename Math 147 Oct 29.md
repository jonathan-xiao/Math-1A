# Uniform Continuity

Let $f$ be a real valued function on a set $S$. Then $f$ is uniformly continuous on $S$ if $\forall \epsilon > 0$ $\exists \delta > 0$ s.t. if $a,b \in S$ and $|a-b|<\delta$ then $|f(a)-f(b)|<\epsilon$. 
Every function that is uniformly continuous on $S$ is continuous on $S$. It is a stronger condition.

"Steepness" is somewhat related to uniform continuity. Certainly $3x+1$ is uniformly continuous everywhere, but $\frac{1}{x^2}$ is not. However, a steep function is not necessarily not uniformly continuous. That is, $\sqrt{x}$ gets steep but is still uniformly continuous. 

## Theorem

If $f$ is uniformly continuous on $S$ and $a_n$ is a Cauchy sequence in $S$ then $f(a_n)$ is also a Cauchy sequence.

### Proof

Let $a_n$ be Cauchy and in $S$ and assume $f$ is uniformly continuous. Fix $\epsilon > 0$.

Since $f$ is uniformly continuous then $\exists \delta >0$ where if $x,y \in S$ and $|x-y|<\delta$ then $|f(x)-f(y)|<\epsilon$.

Since $a_n$ is Cauchy then $\exists N$ s.t. $\forall m,n > N$ then $|a_n-a_m|<\delta$. Then $m,n > N$ means $|f(a_n)-f(a_m)|<\epsilon$ and so $f(a_n)$ is Cauchy.

The takeaway is this: Many of our basic theorems which are true about continuous functions are only true about uniformly continuous functions after modification, OR simply not true at all.

The inverse of a uniformly continuous function may not be uniformly continuous. 

## Theorem

Let $f: K \to \mathbb{R}$ be a function and $S \subseteq K$. Then $f$ fails to be uniformly continuous on $S$ iff $\exists \epsilon >0$ and $x_n, y_n \in S$ s.t. $|x_n-y_n| \to 0$ and yet for all natural numbers $n$, $|f(x_n)-f(y_n)|\geq \epsilon$.

### Proof

Forward. If $f$ fails to be uniformly continuous on $S$ then $\exists \epsilon > 0$ s.t. $\forall \delta > 0$ $\exists x,y \in S$ with $|x-y|<\delta$ but $|f(x)-f(y)|\geq \epsilon$. So then for $\delta=\frac{1}{n}$ then $\exists x_n, y_n \in S$ where $|x_n-y_n|<\frac{1}{n}$ and yet $|f(x_n)-f(y_n)|\geq \epsilon$. 

Backward. Suppose the backward premise. Then consider $\epsilon > 0$ and $x_n, y_n$. Fix $\delta > 0$ and consider $N$ large enough where $|x_N-y_N|<\delta$. Then $x=x_N$ and $y=y_N$ are points in $S$ where $|x-y|<\delta$ but $|f(x)-f(y)|\geq\epsilon$ and so $f$ is not uniformly continuous. 




