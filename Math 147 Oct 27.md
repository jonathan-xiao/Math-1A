# Intermediate Value Theorem

Let $f: K \to \mathbb{R}$ be a function and let $[a,b] \subseteq K$. Then if $y$ is a value strictly between $f(a)$ and $f(b)$ then there exists $c \in (a,b)$ where $f(c)=y$. 

## Proof

Assume that $f(a) < y < f(b)$ and let $S = \\{ x \in [a,b]: f(x)<y\\}$. We know that $S \subseteq [a,b]$ so $S$ is bounded, and since $a \in S$, it is nonempty. Hence it has a supremum.

Consider $c = \sup(S)$. Since $b$ is another upper bound of $S$, $c \leq b$. And since $a \in S$, $a \leq c$. Note that $f(a) < y < f(b)$ meaning $c \in (a,b)$. 

Let $x_n$ be a sequence of elements in $S$ converging to $\sup(S)$. Since $f$ is continuous, $f(x_n) \to f(c)$ and since each $f(x_n)<y$ then $f(c) \leq y$. 

Consider $T = \\{x: c < x \leq b\\}$. We know that $b \in T$ so $T$ is nonempty, and it is bounded below by $c$ which means $\inf(T) = c$ exists. Let $a_n$ be a sequence of points in $T$ converging to $c$. $\forall n$, $a_n > c$ which means $a_n \not\in S$. 

But $f(a_n) \to f(c)$. Since $a_n \not\in S$ then $f(a_n) \geq y$ $\forall n$ so $f(c) \geq y$. Well $y \leq f(c) \leq y$ so $f(c) = y$. 

The other case is similar. 

# Intervals

An interval is a set that is either open or closed (or open on one side and closed on the other). 

A set $I$ of real numbers is an interval iff $\forall a,b \in I$, if $a < c < b$ then $c \in I$. 

## Proof

Forwards. By definition.

Backwards. Suppose $I$ is nonempty and meets the reverse conditions. We show that $I$ is the interval between the infimum and supremum, where the two endpoints are included only if they are in $I$. Let this interval be $J$.

We know that $I \subseteq J$. But take an arbitrary $j \in J$. If $j$ is the supremum or infimum of $I$ then it is clear that $j \in I$. Otherwise, we have $\inf(I)<j<\sup(I)$. 

By theorem 1.14, $\exists a,b \in I$ where $\inf(I)<a<j$ and $j<b<\sup(I)$ and so $a<j<b$ and so $j \in I$ and so $J \subseteq I$ so $J=I$. Done.

## Theorem

If $f$ is a continuous real-valued function on an interval $I$ , then $f(I)$ is also an interval. In other words, the continuous image of an interval is an interval.

### Proof

Suppose $y_1, y_2 \in f(I)$. Let $y_1 = f(x_1)$ and $y_2 = f(x_2)$. Suppose that $f(x_1) < y < f(x_2)$. We use the IVT to conclude $y = f(x)$ for some $x \in (x_1,x_2) \subseteq I$ so $y \in f(I)$. 

# Intermediate Value Property

A function $f$ is said to have the intermediate value property if whenever $[a,b] \subseteq dom(f)$ and $f(a) < y < f(b)$ $\exists c \in (a,b)$ s.t. $f(c) = y$. 

$f$ has the intermediate value property iff the image of every interval under $f$ is an interval. 

## Definition

$f$ is injective if $\forall x,y \in dom(f)$ if $f(x) = f(y)$ then $x=y$. Equivalently, if $x \neq y$ then $f(x) \neq f(y)$. 

## Definition

A function $f$ is said to be strictly increasing if $a < b \implies f (a) < f (b)$. A function $f$ is said to be strictly decreasing if $a < b \implies f(a) > f(b)$. A function which is either strictly increasing or strictly decreasing is called strictly monotonic.

Every strictly monotonic function is injective.

## Theorem

Let $f$ be an injective continuous function whose domain is an interval $I$. Then $f$ is strictly monotonic.

### Proof

We first show $f$ has the following property: If $a < b < c \in I$ then $f(b)$ lies strictly between $f(a)$ and $f(c)$. If not, then $f(b)$ is either strictly greater than both $f(a)$ and $f(c)$ or strictly smaller than both. 

Let’s consider the case where $f(b) > \max\\{f (a), f (c)\\}$. Select $y$ between these two values: $\max\\{f (a), f (c)\\} < y < f (b)$. Then $y \in [f (a), f (b)]$ and $y \in [f (c), f (b)]$. 
By the intermediate value theorem, there exists $x_1 \in (a, b)$ and $x_2 \in (b, c)$ such that $f(x_1 ) = y = f (x_2 )$. Note $x_1 \neq x_2$ so this contradicts the fact that $f$ is injective.

Pick two specific $a,b \in I$ with $a<b$. Since $f$ is injective, $f(a) \neq f(b)$. Assume $f(a) < f(b)$. $\forall x \in I$, 

$$x < a < b \implies f(x) < f(a) < f(b)$$
$$a < x < b \implies f(a) < f(x) < f(b)$$
$$a < b < x \implies f(a) < f(b) < f(x)$$

Consider arbitrary $x_1, x_2 \in I$ with $x_1 < x_2$. If $x_1 < a < x_2$ we can use the facts to show $f(x_1)<f(a)<f(x_2)$ and the rest of the cases are similar. So $f$ is monotonic increasing. 

## Theorem

An injective function with the intermediate value property is continuous on any interval $J \in dom(f)$.

## Proof

First, the injective function is strictly monotonic on $J$. Suppose $f$ is strictly increasing on $J$. Since $f$ has the IVP, $f(J)$ is also an interval. Let $x_0 \in J$. Consider the case where $x_0$ is not an endpoint of $J$ (endpoint case is similar).

Then $f(x_0)$ is not an endpoint of $f(J)$. Let $\epsilon_0 > 0$ s.t. $(f(x_0)-\epsilon_0, f(x_0)+\epsilon_0) \in J$. Fix $\epsilon > 0$.

Assume $\epsilon < \epsilon_0$. Then $\exists x_1, x_2 \in J$ where $f(x_1) = f(x_0) - \epsilon$ and $f(x_2) = f(x_0) + \epsilon$. When $x_1 < x < x_2$ then $|f(x)-f(x_0)|<\epsilon$. 

Let $\delta = \min(x_2-x_0, x_0-x_1)$. So then $|x-x_0|<\delta \implies |f(x)-f(x_0)|<\epsilon$. 

## Theorem

Let $f$ be an injective continuous function, and suppose $dom(f)$ is an interval $J$.
Then it can be shown that $f^{-1} : f(J) \to J$ exists, has the intermediate value property, and is injective - therefore is continuous.



