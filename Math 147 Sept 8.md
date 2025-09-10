## Binary Operation

Let $S$ be a set. A function * from $S \times S \rightarrow S$ is called a binary operation on $S$. For $x, y \in S$, the output $*(x,y) = x * y$. 

It must obey the following conditions

1. It must be associative. $\forall x,y,z \in S$, $x * (y * z) = (z * y) * z$.
2. It must be commutative. $\forall x,y \in S$, $x * y = y * x$.
3. Identity element. An element $e \in S$ is called the identity element if $\forall x \in S$, $x * e = e * x = x$.
4. Inverse element. $x^{-1} \in S$ is an inverse of $x$ if $x^{-1} * x = x * x^{-1} = e$. 

For example, the distance operation $xDy = |x-y|$ for $x.y \in \mathbb{R}$. 

It is commutative but not associative. The identity element $e=0$ and $x^{-1} = x$. 

## Fields

Definition: A field is a triple $(F, +, \cdot)$ with a set $F$ and two binary operations $+$ and $\cdot$. The field must satisfy:

1. $+$ and $\cdot$ are associative
2. $+$ and $\cdot$ are commutative
3. There exist additive and multiplicative identity elements

   - $\exists 0 \in F$ s.t. $\forall x \in F$, $x+0=x$.
   - $\exists 1 \in F$ s.t. $\forall x \in F$, $x \cdot 1=x$.
  
4. Every element except 0 has an additive and multiplicative inverse.

   - $\forall a \in F$, $\exists -a \in F$ s.t. $a + (-a) = 0$.
   - $\forall a \in F$, $\exists a^{-1} \in F$ s.t. $a \cdot a^{-1} = 1$.

5. Multiplication is distributive over additions

   - $\forall a,b,c \in F$, $a(b+c) = ab + ac$.

6. $F$ is nontrivial. There must be at least 2 elements in $F$.


## Writing a Proof

Every statement in a proof must either be:

- An axiom
- A previously proven statement
- A statement that follows by logical rules from the previous
- A substitution upon an appeal to a definition

## Theorem 1.1

Let $F$ be a field. Then:

i. The additive identity element 0 is unique
ii. The multiplicative identity element 1 is unique
iii. $\forall x \in F$, $-x$ is unique
iv. $\forall x \neq 0, x \in F$, $x^{-1}$ is unique

## Theorem 1.2

Let $F$ be a field. If 0 is the additive identity of $F$, then $-0 = 0$. 

### Proof

For if - then proofs, always assume the "if" portion is a true statement to begin. 

Assume that 0 is the additive identity element of $F$. 

$\forall x \in F$, $x + 0 = x$

Therefore, for a particular $x=0$, we have $0+0=0$

That means that 0 is the additive inverse of 0.

This means we can conclude that $-0 = 0$. 

## Theorem 1.3

For all $x \in F$, $x(0)=0$. 

### Proof

$$\begin{aligned}
0 &= 0 + 0 \\
0(x) &= (0+0)x \\
0(x) &= 0(x) + 0(x) \\
0(x) + (-0(x)) &= 0(x) + 0(x) +(-0(x)) \\
0 &= 0(x)
\end{aligned}$$

## Theorem 1.4

Let $F$ be a field. For any $x \in F$, $-x = (-1)x = x(-1)$. 

### Proof

For $\forall$ statements, let $c \in S$ be an arbitrary but particular element of $S$. Show that $p(c)$ is true by using only the fact that $c \in S$. 

Let $c$ be an arbitrary element in $F$. 

Since 1 is the multiplicative identity, then $c = 1 \cdot c$. 

Thus, $-1(c) + c = -1(c) + 1(c)$ because $+$ is well-defined. Therefore,

$$\begin{aligned}
-1(c)  + c &= -1(c)+1(c) \\
&= c(-1)+c(1) \\
&= c(-1+1) \\
&= c(0)
\end{aligned}$$

Now we make use of Theorem 1.3.

Therefore, $-1(c) + c = 0$. So, $-1(c)$ is the additive inverse of $c$, meaning that $-c = (-1)c = c(-1)$. Since $c$ is an arbitrary number in $F$, then the theorem is proved. 














