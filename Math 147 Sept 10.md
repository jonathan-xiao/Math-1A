## Theorem 1.5

Let $F$ be a field. For all $a,b,c \in F$, then:

1. If $a+c=b+c$ then $a=b$
2. $(-a)b = -(ab) = a(-b)$
3. $(-a)(-b)=ab$
4. If $ac=bc$ and $c \neq 0$ then $a=b$

Remember that to prove $\forall x \in S, p(x)$ start with a let statement. 

### Proof 1.5.1

Let $a,b,c$ be arbitrary elements of $F$. Assume that $a+c=b+c$. 

By a field axiom, there exists an additive inverse $-c$ for $c$. Therefore, 

$$ 
\begin{aligned}
a+c+(-c) &= b + c + (-c) \\
a + 0 &= c + 0 \\
a &= b
\end{aligned} $$

Hence, proved.

### Proof 1.5.2

Let $a, b$ be arbitrary elements of $F$. By theorem 1.4, we have:

$$ \begin{aligned}
-a &= (-1)(a) &= a(-1) \\
-ab &= (-1)(a)(b) &= a(-1)b \\
-ab &= (-a)b &= a(-b)
\end{aligned} $$

Hence, proved.

### Proof 1.5.3

Let $a, b$ be arbitrary elements of $F$. 

$$ \begin{aligned}
(-a)(b+(-b)) &= 0 \\
(-a)b + (-a)(-b) &= 0 \\
(-ab) + (-a)(-b) &= 0 \\
\end{aligned} $$

The last step follows from theorem 1.5.2. Therefore, $-ab$ and $(-a)(-b)$ are additive inverses. Hence $(-a)(-b) = -ab$. 

### Proof 1.5.4

Let $a,b,c$ be arbitrary elements of $F$. Assume that $ac=bc$ and $c \neq 0$. 

Since $c \neq 0$ then by the field axioms, $c^{-1}$ exists. Then:

$$ \begin{aligned}
acc^{-1} &= bcc^{-1} \\
a1 &= b1 \\
a &= b
\end{aligned} $$

## Note about contradiction

Statements $p$ and $q$ are said to be logically equivalent if they always have the same truth values. We write:

$$p \equiv q \space \mathrm{or} \space p \Longleftrightarrow q$$

Let $p$ be a statement. $p \land \neg p$ always returns false. This is a contradiction. We have:

| $p$ | $\neg$ $p$ |$\neg$ $p$ $\rightarrow$ ($q$ $\land$ $\neg$ $q$)|
|---|---|:---:|
|T|F|T|
|F|T|F|

$p$ and $\neg p \rightarrow (q \land \neg q)$ have the same truth values. 

## Theorem 1.6

Let $F$ be a field. For all $x,y \in F$,

1. If $x \neq 0$ then $x^{-1} \neq 0$ and $(x^{-1})^{-1} = x$
2. If $x,y \neq 0$ then $x/y \neq 0$ and $1/(x/y) = y/x$
3. $-(-x) = x$

### Proof of 1.6.1 

Let $x \in F$ and $x \neq 0$. Assume that $x^{-1} = 0$

$$x(x \cdot x^{-1}) = 1 \cdot x = x$$

But also, 

$$ \begin{aligned}
x(x \cdot x^{-1} &= x(x \cdot 0) \\
&= x(0) \\
&= 0
\end{aligned} $$

Then $x = 0$, which is a contradiction. Therefore, $x^{-1} \neq 0$. 

Next we have that $x \cdot x^{-1} = 1$ by the field axioms. Therefore, $(x^{-1})^{-1} = x$. 

## Uniqueness

To prove that there is a unique element satisfying property $p$:

1. SHow that $\exists z$ where $p(z)$ is true
2. Assume that there are two objects $x,y$ s.t. $p(x)$ and $p(y)$ are true. Then prove $x=y$.

$$\forall x,y \space (p(x) \land q(x)) \rightarrow x = y$$

## Proof of 1.1.1

By the field axioms, an additive identity element exists. 

Suppose that $a,b$ are two additive identity elements of $F$. Then,

$$\forall x \in F, x+a=x$$
$$\forall x \in F, x+b=x$$

are both true statements. Therefore, we can substitute $x = b$ and $x=a$ respectively to get:

$$b+a=b$$
$$a+b=a$$

Therefore, $a=b$ so the additive identity element is unique. 

## Proof of 1.1.3

Let $x$ be an arbitrary element of $F$. The existence of the additive inverse of $x$ is guaranteed by 
the field axioms. Suppose $a,b$ are both additive inverses of $x$. 

$$x+a=0$$
$$x+b=0$$

are both true. Therefore, 

$$ \begin{aligned}
x+a &= x+b \\
a + x + a &= a + x + b \\
0 + a &= 0 + b \\
a &= b
\end{aligned} $$

Therefore, there is a unique additive inverse of $x$. 

## Partial Ordering

A partial order is a set $L$ and a relation $\leq$ on $L \times L$ that satisfies the following:

1. The relation $\leq$ is reflexive
   - This means $\forall a \in L$, $a \leq a$
  
2. The relation $\leq$ is transitive
   - This means $\forall a,b,c \in L$, if $a \leq b$ and $b \leq c$ then $a \leq c$

3. The relation $\leq$ is anti-symmetric
   - This means $\forall a,b \in L$, if $a \leq b$ and $b \leq a$ then $a=b$

### Total Order

Let $(L, \leq)$ be a partial order. We say $\leq$ is a total order if 

4. Any two elements are comparable
   - This means $\forall a,b \in L$, either $a \leq b$ or $b \leq a$
  
### Example

Let $L = \\{1,2,3,6,14 \\}$. Define $\leq = \\{(a,b): \exists x \in \mathbb{Z} \space \mathrm{s.t.} \space ax = b \\}$

It is not a total order because there is no comparison from 6 to 14. You can draw a lattice diagram to check this, larger numbers on top, smaller numbers on bottom. 










































































