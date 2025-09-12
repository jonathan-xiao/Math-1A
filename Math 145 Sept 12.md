## Diophantine Equations

If $d = \mathrm{gcd}(a,b)$ then $\exists s,t \in \mathbb{Z}$ s.t. $d = as + bt$. 

### Corollary

Let $a,b \in \mathbb{N} \backslash \\{0\\}$. Then the smallest positive linear combination $as + bt = \mathrm{gcd}(a,b)$. 

#### Proof 

Let $d = \mathrm{gcd}(a,b)$ and let $d'$ be the smallest positive value of $as + bt$ where $s,t \in \mathbb{Z}$. 

The number $d$ is a positive linear combination and $d'$ is the smallest linear combination, so $d' \leq d$. 

We know $\exists s', t' \in \mathbb{Z}$ s.t. $d' = as' + bt'$. We also know $d|a$ and $d|b$, therefore, $d|d'$. 

Then, $d \leq d'$. This implies $d=d'$. 

## Definition

We say $a$ and $b$ are relatively prime if $\mathrm{gcd}(a,b) = 1$. 

## Proposition

If $a$ and $b$ are relatively prime, and suppose that $a|(bc)$, then $a|c$. 

### Proof

By the corollary, $\exists s,t \in \mathbb{Z}$ s.t. $as+bt=1$. 

Multiplying both sides by $c$, we have $asc + bct = c$. Well, $a$ divides $a$ and $a$ divides $bc$ so $a$ divides $c$ as desired. 











