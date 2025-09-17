## Euclidean Domains

### Definition

$R$ is a Euclidean Domain (ED) if $\exists f: R \leftarrow \mathbb{N}$ s.t. 

1. $f(a) \leq f(ab)$ where $b \neq 0$
2. $\forall a,b \in R$, $b \neq 0$ then $\exists q,r \in R$ s.t. $a = bq+r$ and $f(r) < f(b)$. $q$ and $r$ do not have to be unique.

### Lemma

Let $(R, f)$ be ED. 

1. $f(0) < f(1) \leq f(a) \space \forall a \neq 0$
2. If $a,b \neq 0$ then $f(a)=f(ab)$ iff $b \in R^*$
3. If $a \neq 0$ then $f(a) = f(1)$ iff $a \in R^*$

#### Proof 1

By axiom 1, becase $1 | a$ then $f(1) \leq f(a \cdot 1)$. Let $1 = 1 \cdot q + r$ where $f(r)<f(1)$. 

If $r \neq 0$ then $f(r) \geq f(1)$. This is a contradiction, meaning $r=0$. So $f(r)=f(0)<f(1)\leq f(a)$. 

#### Proof 2

Forward. If $b \in R^*$ then $b | 1$. We have $a = abb^{-1}$ which means $f(ab) \leq f(a) \leq f(ab)$. So $f(a) = f(ab)$. 

To explain, $f(a) \leq f(ab) \leq f((ab)b^{-1}) = f(a)$ so $f(a) = f(ab)$. 


