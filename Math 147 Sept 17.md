## Bounded Sets

Let $L$ be a totally ordered set where $A \subseteq L$. Then we have $x \in A$ is the maximum if $x \geq y \space \forall y \in A$. Also, $x \in A$ is the minimum if $x \leq y \space \forall y \in A$. 

These are notated as $\mathrm{max}(A)$ and $\mathrm{min}(A)$. 

### Interval Notation

Interval notation helps us shorten the set builder notation for sets. We have:

$$\[a,b\] = \\{x \in L: a \leq x \leq b\\}$$
$$(a,b) = \\{x \in L: a < x < b\\}$$
$$\[a,\infty) = \\{x \in L: a \leq x \\}$$

Et cetera. A few special remarks: 

If $b > a$ then we have $\[a,b\] = \emptyset$. Then $a \leq b$ iff $\[a,b\] \neq \emptyset$ so that $b = \mathrm{max}(\[a,b\])$. 

With a set in $\mathbb{Q}$ like $\[0, 1)$, there is no maximum. For every rational $x$ in the interval, a larger rational in the interval is $x+\frac{1-x}{2}$. 

### Supremum

Let $L$ be a total order. Suppose that $A \subseteq L$. Then, we have:

1. The element $x \in L$ is an upper bound for $A$ if $\forall a \in A$, $x \geq a$. This element does not need to be in $A$.
2. If an upper bound exists, then $A$ is bounded above by $x$.
3. Define the set:

$$U = \\{ x \in L: x \mathrm{is \space an \space upper \space bound \space of} \space A\\}$$

The least element of $U$ is guaranteed by the well-ordering principle and is called the least upper bound (supremum) of $A$ and is written $\mathrm{sup}(A)$. 

The lower bound is defined similarly. The greatest lower bound is called the infimum of $A$. 

### Theorem

Let $L$ be a total order and $A \subseteq L$. 

1. If $A$ has a maximum, it is unique. If $A$ has a minimum, it is unique.
2. The element $x$ is the maximum of $A$ iff $x = \mathrm{sup}(A)$ and $x \in A$. Similar statement for minimum.

#### Proof 1

Suppose that $A$ has maxima $a,b$ where $a,b \in A$. Then, for all elements $x \in A$, it is true that $a \geq x$ and $b \geq x$. Hence, we have $a \geq b$ and $b \geq a$. By antisymmetry, then $a=b$. Similar argument for minimum. 

#### Proof 2

Forward direction. Assume that $x$ is the maximum of $A$. Then we know that $\forall a \in A$, $x \geq a$, which means it is an upper bound. Let $U$ be the set of all upper bounds. Since $x \in A$, then it is the smallest element of the set. Therefore $x = \mathrm{sup}(A)$.

Backward direction. Assume that $x$ is the least upper bound of $A$ and $x \in A$. By the definition of an upper bound, then $\forall a \in A$, $x \geq a$. Since $x \in A$ this means that $x$ is the maximum of $A$. 

Similar argument for minimum. 

### Theorem

Let $F$ be an ordered field. Let $a,b,r \in F$ with $r>0$. Then $|a-b|<r$ iff $b \in (a-r, a+r)$. 

#### Proof

Forward. Suppose that $|a-b|<r$. From theorem 1.10.2, we have $\pm (a-b) < r$. Splitting these up, we have $b > a+r$ and $b < a+r$. 

This means that $a-r < b < a+r$ and so $b \in (a-r, a+r)$. 

Backward. Suppose that $b \in (a-r, a+r)$. So then $a-r < b < a+r$. Either $|a-b| = a-b$ or $|a-b|=b-a$. 

The first case gives $a-r < b$ so $a-b = |a-b| < r$. The second gives $b<a+r$ so $b-a = |a-b| < r$. In both cases, then $|a-b|<r$ is true. 

### Theorem

Let $F$ be an ordered field and let $B \subseteq F$ be a nonempty set that is bounded above by $b$. The following are equivalent (TFAE):

1. $b = \mathrm{sup}(B)$
2. For each $\epsilon > 0$, $\exists x \in B$ s.t. $|x-b|<\epsilon$
3. For each $\epsilon > 0$, $\exists x \in B$ s.t. $x \in (b - \epsilon, b\]$

#### Proof

1 to 2. Suppose that $b = \mathrm{sup}(B)$. Assume the negation of (2), which is that 

$$\exists \epsilon > 0 \space \mathrm{s.t.} \space \forall x \in B, \space |x-b| \geq \epsilon$$

Then no element $x \in B$ is in the range $(b-\epsilon, b+\epsilon)$. 

Since $b = \mathrm{sup}(B)$ and no element in $B$ is in $(b-\epsilon, b+\epsilon)$, then $b - \epsilon$ is also an upper bound and so there is an upper bound smaller than the supremum. This is a contradiction.

2 to 3. Assume (2) is true. Let $\epsilon > 0$ and consider $x \in B$ s.t. $|x-b|<\epsilon$. Then $x \in (b-\epsilon, b+\epsilon)$. Since $B$ is bounded above by $b$, then we can cut out the extraneous range and we have $x \in (b - \epsilon, b\]$. 

3 to 1. Assume (3) is true. Suppose $b \neq \mathrm{sup}(B)$. Since $b$ is an upper bound, then there is a lower upper bound $u < b$. Let $\epsilon = |b-u| > 0$. So $\epsilon = b-u$ or $u = b -\epsilon$. 

By (3), then $\exists x \in B$ s.t. $x \in (b-\epsilon, b\]$ or $x \in u, b$. But $u$ cannot be an upper bound if there is an element larger than it. Contradiction. 

### Definition

Define $\mathbb{R}$, the set of real numbers, to be the unique ordered field satisfying the completeness axiom:

- Every nonempty subset of $\mathbb{R}$ has a supremum

This is called the categoricity of the real numbers. 

### Theorem

Every nonempty subset of $\mathbb{R}$ that is bounded below has a greatest lower bound.

#### Proof

Let $K$ be the nonempty subset of $\mathbb{R}$ that is bounded below. Then let $L$ be the set of all lower bounds of $K$. Since $K$ is known to be bounded below, $L$ is nonempty. 

Let $k \in K$. Every element in $L$ is a lower bound of $K$, so for all $l \in L, l \leq k$. Therefore, $k$ is an upper bound of $L$. Since $K$ is also nonempty then there must exist a $k \in K$ that is the upper bound of $L$. 

$L$ is a nonempty set of $R$ and is bounded above. By the completeness axiom, then $L$ has a supremum. Let this supremum be $\mathrm{sup}(L) = b$. 

I want to show that $b$ is the maximum of $L$. Suppose that $b$ is not a lower bound of $K$. Then $\exists a \in K$ s.t. $a < b$. Since $b$ is the supremum and $a<b$, then $a$ cannot be an upper bound for $L$. We previously showed that every element of $K$ must be an upper bound of $L$, and so we have a contradiction.

Therefore, $b = \mathrm{sup}(L)$ is the greatest lower bound of $K$.  

### Real Numbers

Let $x \in \mathbb{R}$ and $n \in \mathbb{N}$. Then we have 

$$n \cdot a = a + a + ... + a \space (n \space \mathrm{times})$$
$$n = 1 + 1 + ... + 1 \space (n \space \mathrm{times})$$

### Archimedean Property

If $x > 0$ and $x \in \mathbb{R}$, for some $n \in \mathbb{N}$ we have $n > x$. 

#### Proof

Suppose $\exists x \in \mathbb{R}$ where $x$ is greater than every real number. So $\mathbb{N}$ is also bounded above by $x$ and is nonempty, so $\mathbb{N}$ also has a least upper bound. Let $r = \mathrm{sup}\mathbb{N}$. 

By theorem 1.14.2, $\exists n \in \mathbb{N}$ s.t. $|r-n|<1$. This means $n-1 < r < n+1$. 

But $n+1 \in \mathbb{N}$ and $n+1>r$ which is a contradiction. 











