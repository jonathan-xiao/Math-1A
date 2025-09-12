## Ordering

Let $A$ be a set. We define $P(A)$ to be the set of all subsets of $A$. 

### Example

Let $A = \\{1,2\\}$. Then:

$$P(A) = \\{ \emptyset, \\{1\\}, \\{2\\}, \\{1,2\\}\\}$$

Note that no matter what $A$ is, $\emptyset \subseteq A$. 

The ordering $(P(A), \subseteq)$ is a partial ordering and not a total ordering. Show this with a lattice diagram with $\emptyset$ on the bottom and $\\{1,2\\}$ on the top. 

## Trichotomy

Let $L$ be a partially ordering set under $\leq$. The partial order $L$ is said to obey the law of trichotomy if for every $a,b \in L$ exactly one of the following is true:

1. $a < b$
2. $a = b$
3. $b < a$


## Theorem

If $L$ is a partial order and $L$ obeys the law of trichotomy, then $L$ is a total order.

### Proof by Cases

Split the proof into cases that exhaust all the possibilities. Then prove each case holds up the statement. 

Suppose that $(L, \leq)$ obeys the law of trichotomy. Let $a,b$ be arbitrary elements. Then, you will have cases:

1. Assume that $a<b$. Then $a \leq b$ by the definition of $<$.
2. Assume that $a=b$. Then $a\leq b$ by the reflexivity axiom.
3. Assume that $b<a$. Then $b \leq a$ by the definition of $<$.

## Theorem Converse

If $L$ is a total order, then $L$ obeys the law of trichotomy.

### Proof

The converse of $p \rightarrow q$ is $q \rightarrow p$ and they are different statements. So each has to be proved separately. 

Assume that $L$ is a total order. Note that since any two elements are comparable in a total order, then either $a \leq b$ or $b \leq a$. 

1. Case 1: Suppose that $a \leq b$.
   - If $a=b$ then (2) holds.
   - If $a \neq b$ then (1) holds.
  
2. Case 2: Suppose that $b \leq a$.
   - If $b=a$ then (2) holds.
   - If $b \neq a$ then (3) holds.

Now we have to prove that they are disjoint, ie, only one of the law of trichotomy parts holds.

Assume (1), so $a<b$. Then (2) is false by the definition of $<$. If (3) is true, then $a leq b$ and $b \leq a$, which means by the antisymmetry property, then $a=b$, which cannot be true. Therefore, (3) must be false too.
The arugument that if (3) is true then (1) and (2) are false is similar. 

If (2) is true, then $a=b$. Then by the definition of $<$, then $a<b$ and $b<a$ are both false. That means (1) and (3) are both false in this case. 

Since we proved both sides of the theorem, then we can conclude the following:

If $p \rightarrow q$ is true and $q \rightarrow p$ then $p \leftrightarrow q$. 


## Ordered Fields

### Ordered Fields Axioms

Let $F$ be a field and let $\leq$ be a total ordering on $F$. We say that $(F, \leq)$ is an ordered field if the following are true $\forall a,b,c \in F$. 

1. If $a \leq b$ then $a + c \leq b + c$
2. If $a \leq b$ and $0 \leq c$ then $ac \leq bc$

For example, $\mathbb{Q}$ is an ordered fields. 

### Positive and Negative

Let $F$ is an ordered fields. We define:

$$F^+ = \\{x : x > 0\\}$$
$$F^- = \\{x : x < 0\\}$$

We say $x$ is positive if $x \in F^+$ and $x$ is negative if $x \in F^-$. For any $x$ is exactly one of the following: either positive, negative, or 0. 





