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





