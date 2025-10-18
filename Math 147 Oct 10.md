# Problem

Consider:

$$f(x) = \begin{cases} 
      1, & x > 0 \\
      -1, & x < 0
   \end{cases}$$

Note the domain $K = (-\infty, 0) \cup (0, \infty)$. 

## Part
Prove 

$$\lim_{x \to \frac{1}{2}} f(x) = 1$$

Fix $\epsilon > 0$. Consider $\delta = \frac{1}{4}$. Then fix an arbitrary $x \in K$ with $0<|x - \frac{1}{2}| < \frac{1}{4}. Now note that since this is true, $x > 0$. Therefore $\forall x$,

$$|f(x) - 1| = |1-1| = 0 < \epsilon$$

## Part

Prove the limit of $f(x)$ at 0 does not exist.

Suppose the limit exists and is equal to $L$. Consider two sequences $a_n = \frac{1}{n}$ and $b_n = -\frac{1}{n}$. These are both sequences of distinct nonzero terms. Therefore:

$$\lim_{n \to \infty} f(a_n) = 1 = L = -1 = \lim_{n \to \infty} f(b_n)$$

This is a contradiction.

# Continuity

## Definition

Let $K$ be the domain of $f$ and let $a \in K$. If $a$ is a limit point of $K$ then $f$ is continuous at the point $a$ if:

$$\lim_{x \to a} f(x) = f(a)$$

If $a$ is not a limit point of $K$ and $a \in K$ then $f$ is continuous at $a$.

A function $f$ is continuous (on its domain) if it is continuous at every point in $K$. 

## Theorem

Let $f: K \to \mathbb{R}$. Let $a \in K$. TFAE

1. $f$ is continuous at $a$
2. $\forall \epsilon > 0$, $\exists \delta > 0$ s.t. if $x \in K$ and $|x-a|<\delta$ then $|f(x)-f(a)| < \epsilon$
3. $\forall x_n \in K$ where $x_n \to a$ then $f(x_n) = f(a)$

## Theorem

$f(x)=x$ is continuous.

### Proof

Let $a \in \mathbb{R}$. FIx $\epsilon > 0$. Choose $\delta = \epsilon$. Assume $|x-a|<\delta$. Then $|f(x)-f(a)| = |x-a| < \delta = \epsilon$. 

## Theorem

If $f$ is continuous at $a$ and $g$ is continuous at $f(a)$ then $(g \circ f)$ is continuous at $a$. 

### Proof

Note the domain of $(g \circ f)$ is:

$$K = \\{x: x \in dom(f) \land f(x) \in dom(g)\\}$$

Since $f$ is continuous at $a$:

$$\lim_{n \to \infty} f(x_n) = f(a)$$

Since $g$ is continuous at $f(a)$ then:

$$\lim_{n \to \infty} g(f(x_n)) = g(f(a))$$

## Theorem

Let $f$ and $g$ be real-valued functions that are continuous at a real number $a$. 

1. Let $k \in \mathbb{R}$. Then $kf$ is continuous at $a$
2. $f+g$ is continuous at $a$
3. $fg$ is continuous at $a$
4. $f/g$ is continuous at $a$ if $a \in dom(f/g)$

## Corollary

Every polynomial is continuous.

## Example

Consider:

$$\lim_{x \to 0} \sin(\frac{1}{x})$$

As $x \to 0$ we know $\frac{1}{x} \to \infty$. Recall that $\sin(2n\pi)=0$ if $n \in \mathbb{N}$. Therefore, consider a sequence $x_n = \frac{1}{2n\pi}$. Note $x_n \to 0$. Then:

$$\sin(\frac{1}{x_n} = 0 \implies \lim_{n \to \infty} \sin(\frac{1}{x_n} = 0$$

## Theorem

Let $I$ be an interval containing $a$ and let $f,g,h$ be functions defined on $I$ except possibly at $a$. Suppose $\forall x \in I - \\{a\\}$, both of the following hold:

$$g(x) \leq f(x) \leq h(x)$$
$$\lim_{x \to a} g(x) = L = \lim_{x \to a} h(x)$$

Then:

$$ \lim_{x \to a} f(x) = L$$

## Theorem

If $f$ is continuous at $a$ then $|f|$ is continuous at $a$.

### Proof

Let $x_n$ be an arbitrary sequence of values in the domain of $f$ where $x_n \to a$. Fix $\epsilon > 0$. Then:

$$||f(x_n)| - |f(a)|| \leq |f(x_n) - f(a)|$$

Therefore, 

$$\lim_{n \to \infty} f(x_n) = f(a) \implies \exists N \space \mathrm{s.t.} \space |f(x_n) - f(a)| < \epsilon$$

Then it is clear $||f(x_n)| - |f(a)|| < \epsilon$. 

# Union

## Definition

An open interval is of the form $(a,b)$ where $a,b$ are real numbers. A subset $U$ of $\mathbb{R}$ is open if it is a union of open intervals. Also:

$$(a, \infty) = \bigcup_{n \in \mathbb{N}} (a, n)$$

## Theorem

Let $(A_i)_{i \in I}$ be an indexed collection of sets. Then $\forall i$,

$$A_i \in \bigcup_{i \in I} A_i$$

## Theorem

Let $U \subseteq \mathbb{R}$. TFAE

1. $U$ is open
2. $\forall a \in U$ $\exists r > 0$ s.t. $(a-r, a+r) \in U$


