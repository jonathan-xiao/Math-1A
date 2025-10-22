# Open and Closed Intervals

## Definition

Open intervals are of the form $(a,b)$ for real numbers $a,b$. A subset $U \subseteq \mathbb{R}$ is open if it is the union of open sets.

## Theorem

Let $U \subseteq \mathbb{R}$. TFAE:

1. $U$ is open
2. $\forall a \in U$ $\exists r > 0$ s.t. $(a-r,a+r) \subseteq U$

### Proof

(1 -> 2). Suppose $U$ is open. Then:

$$U = \bigcup_{i \in I} (a_i, b_i)$$

Consider an arbitrary element $a \in U$. Then $a$ belongs in some $(a_i, b_i)$ where $i \in I$. Let $r = \min(a-a_i, b_i-a)$. We know $r > 0$. 

Fix an arbitrary $x \in (a-r, a+r)$. Then $x < a+r \leq a+b_i-a = b_i$ so $x < b_i$. Similarly, we get $a_i < x$. This means that $(a-r, a+r) \subseteq (a_i, b_i) \subseteq U$. 

(2 -> 1). For every $a \in U$, let $r_a >0$ be defined such that $(a-r_a, a+r_a) \subseteq U$. We claim that:

$$U = \bigcup_{a \in U}(a-r_a, a+r_a)$$

For an arbitrary $x \in U$, then 

$$x \in (x-r_x, x+r_x) \subseteq \bigcup_{a \in U} (a-r_a, a+r_a)$$

By transitivity, then:

$$x \in \bigcup_{a \in U} (a-r_a, a+r_a)$$

For an arbitrary 

$$x \in \bigcup_{a \in U} (a-r_a, a+r_a)$$

then $x \in (a-r_a, a+r_a)$ for some $a$. So $x \in U$. This means that:

$$U = \bigcup_{a \in U}(a-r_a, a+r_a)$$

So $U$ is the union of open sets, and so $U$ is open. 

## Theorem

Every union of open sets is open. Every finite intersection of open sets is open.

### Proof

First. Definition. 

Second. Let $U_1 ... U_n$ be open sets. Take an arbitrary $x \in X$ where:

$$X = \bigcap_{i = i}^n U_i$$

Then $\forall i$, $x \in U_i$. This means that $\forall i$, $\exists r_i > 0$ where $(x-r_i, x+r_i) \subseteq U$. 

Let $r = \min(r_i ... r_n)$. $\forall i$ $(x-r, x+r) \subseteq (x-r_i, x+r_i) \subseteq U_i$. 

Therefore, if $a \in (x-r, x+r)$ then $a \in U_i$ which means that 

$$(x-r, x+r) = \bigcap_{i = i}^n U_i$$

So the intersection is also a union of open sets, and so it itself is open.

## Definition

A subset $C \subseteq \mathbb{R}$ is closed if it contains all of its limit points.

## Definition

Let $U$ be the universe. Let $S \subseteq U$ then $S^c = \\{x \in U : x \not\in S\\}$ is the complement. 

## Theorem

Let $S \subseteq R$. TFAE

1. If $x_n$ is a sequence of points in $S$ converging to $x$ then $x \in S$
2. $S$ is closed
3. $S^c$ is open

### Proof

Suppose 1. Let $x$ be a limit point of $S$. Then $\exists$ a sequence of distinct points in $S$ converging to $S$. This means that $x \in S$ and so $S$ is closed.

Suppose 2. Let $a \in S^c$ so $a$ is not a limit point of $S$. Then $\exists$ an interval $(a-r, a+r)$ which contains no points in $S$. This means that $(a-r, a+r) \in S^c$ and so $S^c$ is open. 

Suppose 3. Assume 1 is false. Since $x \in S^c$ and $S^c$ is open. Then $\exists r > 0$ s.t. $(x-r, x+r) \subseteq S^c$. Since $x_n \to x$ $\exists n$ where $|x_n - x| < r$. This means $x_n \in (x-r, x+r)$ and so $x_n \in S$ and so $x \in S^c$ which is a contradiction. 

# De Morgan

$$\neg(p \land q) \equiv \neg p \lor \neg q$$
$$\neg(p \lor q) \equiv \neg p \land \neg q$$

Also:

$$(A \cup B)^c = A^c \cap B^c$$
$$(A \cap B)^c = A^c \cup B^c$$

$$(\bigcup_{i \in I} A_i)^c = \bigcap_{i \in I} A_i^c$$
$$(\bigcap_{i \in I} A_i)^c = \bigcup_{i \in I} A_i^c$$

## Theorem

The intersection of closed sets is closed. The finite union of closed sets is closed.

### Proof

$$(\bigcap_{i \in I} S_i)^c = \bigcup_{i \in I} S_i^c$$

This means $S_i$ is closed so $S_i^c$ is open, and so the union of all $S_i^c$ is open and so the intersection is closed.

## Theorem

$[a,b]$ is closed.

### Proof

$$\begin{aligned}
[a,b]^c &= \\{x: \neg(a \leq x \leq b)\\} \\
&= \\{x: x<a\\} \cup \\{x: x> b\\} \\
&=(-\infty, a) \cup (b, \infty) \\
\end{aligned}$$

This is open and so $[a,b]$ is closed.

# Definition

Let $f: A \to B$ be a function. Define

$$f^{-1}(T) = \\{x \in A: f(x) \in T\\}$$

The set $f^{-1}(T)$ is the inverse image of $T$ under $f$. 

We have $x \in f^{-1}(T)$ iff $f(x) \in T$. 

## Theorem

$f: \mathbb{R} \to \mathbb{R}$ is continuous iff the inverse image of every open set is open. 

### Proof

Suppose $f$ is continuous and $U$ is open. Let $x \in f^{-1}(U)$ and therefore $f(x) \in U$. Then $\exists \epsilon > 0$ s.t. $(f(x)-\epsilon, f(x)+\epsilon) \subseteq U$. Therefore, if $\forall z$ $|f(x)-z| < \epsilon$ then $z \in U$. 

Since $f$ is continuous, $\exists \delta > 0$ s.t. if $|x-y|<\delta$ then $|f(x)-f(y)|<\epsilon$. 

Suppose $y \in (x - \delta, x+\delta)$. Then $|f(x)-f(y)|<\epsilon$ so $f(y) \in U$. Therefore, $y \in f^{-1}(U)$ and since $y$ is open, then $f^{-1}(U)$ is open. 

Suppose $f: \mathbb{R} \to \mathbb{R}$ is a function where the inverse image of every open set is open. 

Let $x$ be an arbitrary real number. Fix $\epsilon >0$. Then $B = (f(x) - \epsilon, f(x)+\epsilon)$ is open and so $f^{-1}(B)$ is open. Therefore since $x \in f^{-1}(B)$ so $\exists$ s.t. $(x-\delta, x+\delta) \subseteq f^{-1}(B)$. 

$\forall y$ if $|x-y|<\delta$ then $y \in (x-\delta, x+\delta)$ therefore $y \in f^{-1}(B)$. Then $|f(x)-f(y)|<\epsilon$ and so $f$ is continuous. 

# Definition

Let $f: A \to B$ be a function. Let $S \subseteq A$. We define 

$$f(s) = \\{x \in B: x = f(s)\\}$$

$S$ is the image of $S$ under $f$. $f(A)$ is the image of $f$. 









