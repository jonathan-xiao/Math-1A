## Euclidean Domains

### Definition

$R$ is a Euclidean Domain (ED) if $\exists f: R \rightarrow \mathbb{N}$ s.t. 

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

Backward. Suppose that $f(a)=f(ab)$. Then, by the division property, we know that $a = ab(q)+r$ where $f(r) < f(ab) = f(a)$. 

Rearranging, we have $r = a(1-bq)$ so that $a|r$. Then $r=ac$ so that $f(a) \leq f(ac) = f(r)$. So, $f(a) \leq f(r)<f(a)$. This is a contradiction. 

Well then the only solution is when we said $r=ac$, $c=0$. Then we have $r=a(1-bq)=0$ and since $a \neq 0$ then $1 = bq$. So $b$ is a unit and $b \in R^*$. 

#### Proof 3

Take $a=1$ in the previous statement. Then statement 3 immediately follows. 

### Euclidean Algorithm

Let $(R, f)$ be ED and let $a,b \in R$ with $b \neq 0$. Then, using the division algorithm repeatedly gives us:

$$a = bq_1 + r_1, \space f(b)>f(r)$$
$$b=r_1q_2 + r_2, \space f(r_1)>f(r_2)$$
$$...$$
$$r_{k-2} = r_{k-1}q_k + r_k, \space f(r_{k-1})>f(r_k)$$
$$r_{k-1} = r_kq_{k+1}+0, \space f(r_k)>f(0)$$

We know this algorithm must terminate because each $f(r_i)$ is strictly decreasing. It also must obey the following properties:

1. $r_k | a,b$
2. $\exists s,t \in R$ s.t. $as+bt=r_k$
3. $\forall e \in R$ if $e|a$ and $e|b$ then $e|r_k$

#### Proof 1

Since $r_{k+1}=0$ then we know that $r_{k-1}=r_kq_{k+1}$. Therefore, $r_k | r_{k-1}$. Each $r_{i} | r_{i-1}$. So we can apply this logic using induction until we reach $a$ and $b$. 

#### Proof 2

We prove by induction. For the base case, we have $a = r_{-1} \cdot 1 + r_0 \cdot 0$ and $b = r_{-1} \cdot 0 + r_0 \cdot 1$. So we have $s_{-1} = 1$, $s_0 = 0$, $t_{-1}=0$, $t_0 = 1$.

Assume there exists some $s_{i−1},t_{i−1},s_i,t_i \in R$ so that:

$$as_{i−1} +bt_{i−1} = r_{i−1} \space \mathrm{and} \space as_i +bt_i = r_i$$

Then, we just have:

$$r_{i+1} = r_{i−1}−r_iq_i = (as_{i−1} +bt_{i−1})−(as_i +bt_i)q_i$$

and we rearrange to factor out $a$ and $b$ to get explicit formulae for $s_{i+1}$ and $t_{i+1}$. 

#### Proof 3

From statement 2, we know that any common divisor of $a$ and $b$ must also divide $r_k$ since $as+bt=r_k$. 

### Definition

We say that $a,b \in R$, an integral domain, are relatively prime if for every $e \in R$, $e|a$ and $e|b \implies e \in R^*$.  

### Corollary

Let $(R, f)$ be ED. Then $a,b \in R$ are relatively prime iff $\exists s,t \in R$ s.t. $as+bt=1$. 

#### Proof

Backward. Suppose that $as+bt=1$. If $d|a$ and $d|b$ then $d|1$ so $d \in R^*$. 

Forward. We know $\exists s,t, r_k \in R$ s.t. $as+bt = r_k$ and $r_k|a$ and $r_k|b$. Since $a,b$ are relatively prime, then $r_k \in R^*$. Hence, by multiplying both sides with the inverse of $r_k$, we have:

$$a(sr^{−1}_k )+b(tr^{−1}_k) = 1$$

### Proposition

If $R$ is ED and $a \in R$ where $a$ is nonzero and not a unit, then $a$ is the product of finitely many irreducibles. 

#### Proof

Induct on $f(a)$ because it has an ordering on the natural numbers. We know $f(a)>f(1)$ when $a \neq 0$. The base case is where $f(a)=f(1)$. By a lemma, $a \in R^*$ so $a$ is itself irreducible. Choose $n>1$ and assume that the statement is true for all $b$ where $f(1) \leq f(b) < n$. We will prove the statement for $f(a)=n$. 

If $a$ is irreducible, the result holds. If it is not, then $a=bc$ where $b$ and $c$ are not units. We know that $f(b)$ and $f(c)$ are less than $f(a)$ since $a=bc$. Each of $b$ and $c$ are products of finitely many irreducibles, so so is $a$. 

### Proposition

Let $R$ be ED and suppose $p \in R$ is irreducible. If $p|a_1a_2a_3 ... a_k$ then $p$ divides one of the individual $a$ values. 

#### Proof

Proceed with induction. $k=1$ is trivial. For $k=2$, suppose that $p$ does not divide $a_1$. We know then that $p$ and $a_1$ are relatively prime, so there exists $s$ and $t$ s.t.

$$ps+a_1t = 1$$

So $a_2 = psa_2 + a_1ta_2$. Since $p|a_1a_2$ then $p|a_2$. 

Now suppose they are not relatively prime then. Then there is a $d$ which is not a unit that divides both. Then $up=d$ because $p$ is irreducible. Well then $up=d|a_1$ so $p|a_1$. So the $k=2$ case is fine.

Now we do the rest. We have $p|a_1a_2a_3 ... a_k$. If $p|a_k$ then this is proved. Else $p$ divides the product of all $a$ with index less than $k$. By the inductive hypothesis, $p$ divides one of the $a$ values. So this result is proved.

### Unique Factorization

The proof follows nearly identical to the proof for integers. 

















