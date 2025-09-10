## Division Algorithm

Suppose that $a \neq 0$ and $a \in \mathbb{N}$ and $b \in \mathbb{Z}$. Then there are unique integers $q$ and $r$ such that 

$$b = aq + r \space \mathrm{and} \space 0 \leq r < a$$

### Proof of the range of $r$

Let $S = \\{s: s = b-aq \geq 0 \space \mathrm{and} \space q \in \mathbb{Z} \\}$. This is the set of all possible "remainders". 

Firstly $S$ must be nonempty.  

If $b \geq 0$, then choose $q=0$ and we have $s=b \in S$. 

If $b < 0$, then choose $q=b$ so that 

$$\begin{aligned}
s &= b - ab \\
&= b(1-a) \\
&\geq 0
\end{aligned}$$

This is because it is known $a \geq 1$. By the well-ordering principle, there is a least element $r$ in $S$. Let $q \in \mathbb{Z}$ s.t. $r = b-aq$. 

If $r \geq a$, then $r = b-aq \geq a$ so you can subtract another $a$ from $r$ and get a new $r$ that is still in $S$. So then $r-a$ belongs in $S$ and is a smaller element, which contradicts our original assumption. 

Therefore, $r$ must be in between $0 \leq r < a$. 

### Proof of Uniqueness

Suppose $b = aq + r = aq' + r'$, where $0 \leq r, r' < a$. 

We have $aq -aq' = a(q-q')=r - r'$

That means $a|(r-r')$. We also know that $-a < r-r' < a$. The only such $r-r'$ in that range is 0. Therefore, $r=r'$. Since $a \neq 0$, $q=q'$ as well. 

## GCD

The greatest common divisor of a pair of nonzero $a,b \in \mathbb{Z}$ is that largest number $d$ that divides both. In particular, if $d|a$ and $d|b$, and also $e|a$ and $e|b$, then $e \leq d$. 

The Euclidean Algorithm provides a way to find such a gcd of a pair of numbers. 

## Euclidean Algorithm, Method

Start with $a,b \in \mathbb{Z}$ where $a > b$. 

Let $a = q_1b+r_1$ so that 

$$r_1 = a - q_1b$$

$$r_2 = b - q_2r_1$$

$$r_3 = r_1-q_3r_2$$

$$...$$

The last nonzero $r_i$ is the gcd of $a,b$. 

## Formal Euclidean Algorithm

Given $a,b$ are positive integers and $>b$, use the division algorithm to get $r_i$ for all $1 \leq i \leq k+1$ where $r_{k+1}=0$. 

Then we have gcd($a,b$) = $r_k$ and every common divisor of $a$ and $b$ divides this gcd. Also, $\exists s,t \in \mathbb{Z}$ s.t. gcd($a,b$) = $as + bt$. (It can be linearized)

### Proof

Let $r_{-1} = a$ and $r_0 = b$. Define $s_{-1} = 1$, $t_{-1} = 0$, $s_0 = 0$, $t_0=1$. 

Each $r_i = as_i + bt_i$. If $r_i \neq 0$ we get $r_{i-1} = r_iq_{i+1} + r_{i-1}$ where $0 \leq r_{i+1} < r_i$. This means the sequence of $r_i$ is decreasing to 0. 

We then have 

$$\begin{aligned}
r_{i+1} &= r_{i-1} - r_iq_{i+1} \\
&= a(s_{i-1} - s_iq_{i+1}) + b(t_{i-1} - t_iq_{i+1})
\end{aligned}$$

Therefore, $s_{i+1} = s_{i-1} - s_iq_{i+1}$ and $t_{i+1} = t_{i-1} - t_iq_{i+1}$. These are explicit formulae. 

By the principle of strong induction, assume that $r_k$ divides $r_i$ and $r_{i+1}$. Then

$$r_{i-1} = r_iq_{i+1} + r_{i+1}$$ 

is divisible by $r_k$. Hence, since $a,b$ are part of this remainder sequence, then $r_k | a,b$. 

Any divisor $D$ that divides both $a$ and $b$ divides $r_k = as_k +bt_k$. So therefore, $D|r_k$. That indeed means that $r_k$ = gcd($a,b$). 
































