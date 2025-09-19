# Diophantine Equations

This is a system of polynomial equations with integer coefficients that we seek to find integer solutions for. 

## Proposition

Suppose $a,b,c \in \mathbb{Z}$. 

The equation $ax + by = c$ has integer solutions iff $d = \mathrm{gcd}(a,b)|c$.

### Proof

Forward. We know $d | a$ and $d | b$, which means that $d|c$ if there is a solution.

Backward. If $d|c$, then there exists $x', y'$ s.t. $ax' + by' = d$. (Think of Euclid's Algorithm and $s$ and $t$).

This means that, after dividing both sides by $d$ and multiplying both sides by $c$, 

$$a(\frac{c}{d}x') + b(\frac{c}{d}y') = c$$

Since $d|c$ then $\frac{d}{c}$ is an integer. 

## Proposition, Cont'd

If $(x_0, y_0)$ is a solution to $ax + by = c$, then all solutions are given by:

$$x = x_0 + \frac{kb}{d}$$
$$y = y_0 - \frac{ka}{d}$$

### Proof

Forward. If $(x_0, y_0)$ is a solution then:

$$a(x_0 + \frac{kb}{d}) + b(y_0 - \frac{ka}{d}) = ax_0 + by_0 - 0 = c$$

Backward. If $(x,y)$ is a solution, we know that $ax+by+c$ is a solution and that $ax_0 + by_0 =c$ is some other solution. Stacking the two equations:

$$a(x-x_0)+b(y-y_0) = 0$$

We divide both sides by $d$. If $d$ is the gcd of $a,b$ then $\frac{a}{d}$ and ${b}{d}$ are coprime, so their gcd is 1. 

$$\frac{a}{d}(x-x_0) = -\frac{b}{d}(y-y_0)$$

Since $\frac{a}{d}$ divdes the right side because $x-x_0$ is an integer, by the lemma, $\frac{a}{d}$ divides $y-y_0$. Therefore, for some integer $k$, 

$$y = y_0 - \frac{a}{d}k$$

This means $\frac{a}{d}(x-x_0) = \frac{b}{d}(-\frac{a}{d}k)$.

Thus, $x - x_0 = -\frac{b}{d}k$. 

It then follows that $y-y_0 = -\frac{a}{b}(x-x_0)$, so the second equation follows. 

# Congruences

If $n$ is an integer, we say $a \equiv b \mod n$ if $n | (a-b)$.

## Proposition

If $a_i, b_i, n \in \mathbb{Z}$, and if $a_1 \equiv b_1 \mod n and $a_2 \equiv b_2 \mod n$, then $a_1+a_2 \equiv b_1+b_2 \mod n$ and $a_1a_2 \equiv b_1b_2 \mod n$. 

### Proof

We have $n|(a_1-b_1)$ and $n|(a_2-b_2)$. Then, $n|(a_1-b_1+a_2-b_2)$. So $n|(a_1+a_2-(b_1+b_2))$. This means $a_1 + a_2 \equiv b_1 + b_2 \mod n$. 

Also, we have $a_1a_2 - b_1b_2 = (a_1-b_1)a_2 + b_1(a_2-b_2)$. $n$ divides both $a_1-b_1$ and $a_2-b_2$. This means $n | (a_1a_2 - b_1b_2)$ and the proposition follows. 

## Remark

Modulo can be used to prove several divisibility rules, most commonly $3$, $9$, and $11$. You can also do it in a slightly harder way for other numbers, like $7$. 

## Equivalence relation

$\sim$ is an ER on a set $S$ if for all $a,b,c \in S$:

1. It is reflexive. $a \sim a$
2. It is symmetric. $a \sim b \implies b \sim a$
3. It is transitive. $a \sim b$ and $b \sim c$ means $a \sim c$

## Equivalence Class

If $\sim$ is an ER and $a \in S$, the equivalence class of $a$ is 

$$\[a\] = \\{b \in S | b \sim a\\}$$

We have $S \mod \sim = \\{ \[a\] | a \in S \\}$. 






















