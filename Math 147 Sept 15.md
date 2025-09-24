## Theorem 1.9

Let $(L, \leq)$ be an ordered field. For all $a,b,c,d \in F$, if $a \leq b$ then $c \leq d$ then $a+c \leq b+d$. 

### Proof

$a \leq b$ and $c \leq b$. By the properties of ordering, we have $a+c \leq b+c$ and $b+c \leq b+d$. By transitivity, $a+c \leq b+d$. 

## Definition

Let $F$ be an ordered field. Then the absolute value of an element $a$ is defined as 

$$|a| = \begin{cases} 
      a & a \geq 0 \\
      -a & a \leq 0
   \end{cases}
$$

This double counting is permitted because $-0 = 0$. 

## Theorem

Let $F$ be an ordered field. For all $a,b \in F$:

1. $0 \leq |a|$
2. $\pm \leq |a|$
3. $|ab| = |a||b|$
4. $|a+b \leq |a| + |b|$

### Proof

1. Let $a \in F$.

If $a \geq 0$ then $|a| = a \geq 0$. If $a \leq 0$ then $-0 \leq -a$ therefore $0 \leq -a = |a|$.

2. Let $a \in F$. 

  If $a \geq 0$ then $-a \leq 0 \leq a = |a|$. If $a \leq 0$ then $a \leq 0 \leq -a = |a|$. 

3. Let $a, b \in F$.
  
If $a,b \geq 0$ then $ab \geq 0$ (1.8.3).
   
$$|a||b| = ab = |ab|$$

If $a,b \leq 0$ then $-a, -b \geq 0$ so $(-a)(-b) \geq 0$. 

$$|a||b| = (-a)(-b) = ab = |ab|$$

If $a \geq 0$ and $b \leq 0$ then $a \geq 0$, $-b \geq 0$ which means $(-a)b = -(ab) \geq 0$ which means $ab \leq 0$. 

$$|a||b| = (-a)b = -(ab) = |ab|$$

By symmetry, the last case follows the previous. 

4. Let $a,b \in F$.
  
We have $a \leq |a|$ and $b \leq |b|$ by part 2. This means $a+b \leq |a|+|b|$. For $a+b \geq 0$, then the property holds.

Also $-a \leq |a|$ and $-b \leq |b|$ by part 2. This means $-a+(-b) \leq |a|+|b|$. For $a+b \geq 0$, then the property holds. Therefore:

$$|a+b| \leq |a|+|b|$$

## Triangle Inequality

Let $F$ be an ordered field (meaning it obeys total order). For all $a,b,c \in F$ 

$$|a-c| \leq |a-b| + |b-c|$$

### Proof

$$
\begin{aligned}
|(a-b) + (b-c)| &\leq |a-b| + |b-c| \\
|a-c| &\leq |a-b| + |b-c|
\end{aligned}$$

## Quantifiers

To prove that $\exists x \in X, \space p(x)$ provide some value $x \in X$ and show $p(x)$ is true for that value. We can show a discovery process to illustrate the method to find that $x$. 

We have nested quantifiers, which may appear as:

$$ \exists x \in X, \forall y \in Y, p(x,y)$$
$$ \forall x \in X, \exists y \in Y, p(x,y)$$

For there exists, give a specific example. For for all, introduce an arbitrary element and prove without using any specific properties of that element, that the statement holds.

### Negation

$$ \neg \exists x \in X, \forall y \in Y, p(x,y) \equiv \forall x \in X, \exists y \in Y, \neg p(x,y)$$

Change the quantifiers and negate the statement as you go along.







    









