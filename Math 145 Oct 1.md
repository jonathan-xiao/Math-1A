## Lemma

Let $a$ be an integer and $p(x) = a_nx^n + a_{n-1}x^{n-1} + ... + a_1x + a_0$ be an integer polynomial. Then $\exists q(x)$ and $r \in \mathbb{Z}$ s.t. $p(x) = (x-a)q(x)+r$ and where $r = p(a)$. 

### Proof

Induction on $n$. If $n=0$ it follows immediately that $q=0$ and $r = a_0$. 

For $n > 0$, then consider $(x-a)a_nx^{n-1}$. This is a multiple of $x-a$, and so is the expanded version $a_nx^n -aa_nx^{n-1}$. Take:

$$p(x)-(x-a)a_nx^{n-1} = (a_{n-1}+aa_n)x^{n-1} + a_{n-2}x^{n-2} + ... + a_1x+a_0$$

By the inductive hypothesis, then there exists $q_1(x)$ that is an integer polynomial and an integer $r$ s.t. $p(x)-(x-a)a_nx^{n-1}$ (which has degree $n-1$ can be expressed as

$$p(x)-(x-a)a_nx^{n-1} = (x-a)q_1(x)+r$$

This means that $p(x) = (x-a)(q_1(x)+a_nx^{n-1})+r$ by rearranging the last equation. Hence, we can express $p(x)$ as some $(x-a)q(x)+r$. 

# Definition

A polynomial is monic if the leading coefficient $a_n$ is 1

## Corollary

If $q(x)$ is an integer polynomial is monic and has degree $d$, and $p$ is prime, then:

$$q(x) \equiv 0 \mod p$$

has at most $d$ solutions mod $p$. 

### Proof 

For $d=1$, this case follows from an earlier lemma.

Assume that the corollary holds for monic polynomials with degree less than $d$. Suppose now $a$ is a solution to $q(x) \equiv 0 \mod p$. Then:

$$q(x) \equiv (x-a)q_q(xq(a) \equiv (x-a)q_1(x) \mod p$$

If $b \not\equiv a \mod p$ is another solution, $0 \equiv q(b) \equiv (b-a)q_1(b) \mod p$.

If $b - a \not\equiv 0 \mod p$ and $\mathbb{Z}/p$ is an integral domain (without zero divisors), then $q_1(b) \equiv 0 \mod p$. 

So any other solution is a root of $q_1$ and $a$ is one more solution. Which means $q(x) \equiv 0 \mod p$ has at most $d$ solutions. 

## Theorem

$$\sum_{d|n} \varphi(d) = n$$

### Proof

Let $S_d = \\{k: 1 \leq k leq n, \gcd(k,n)=d\\}$ where $d|n$. 

We know that $\gcd(k,n)|n$ so this $\gcd(k,n)$ divides all the numbers from 1 ... $n$ into disjoint $S_d$ sets. 

Note if $k \in S_d$ then $\gcd(\frac{k}{d}, \frac{n}{d}) = 1$ and $1 \leq \frac{k}{d} \leq \frac{n}{d}$. 

If $\gcd(j, \frac{n}{d})=1$ and $1 \leq j \leq \frac{n}{d}$ then $k = jd \in S_d$. 

Therefore, $S_d$ to $\mathbb{Z}/\frac{n}{d}^*$ is a bijection so $|S_d| = \varphi(\frac{n}{d})$. 

This means:

$$n = \sum_{d|n}|S_d| = \sum_{d|n} \varphi(\frac{n}{d}) = \sum_{d|n} \varphi(d)$$

Dividing $n$ by all its divisors produces an identical list to the original divisors themselves because they come in pairs (unless it is square, where division produces the same thing). 

# Primitive Roots

If $a$ is a unit in $\mathbb{Z}$ mod $n$, its order $ord_n(a)$ is the smallest positive integer $d$ s.t. $a^d \equiv 1 \mod n$. 

We say $a$ is a primitive root mod $n$ if

$$\mathbb{Z}/n^* = \\{a^k \mod n: 1 \leq k \leq d\\}$$

## Proposition

If $a^b \equiv a^c \equiv 1 \mod n$ then $d = \gcd(b,c)$ satisfies $a^d \equiv 1 \mod n$ as well. 
This means $a^b \equiv 1 \mod n$ iff $ord_n(a)|b$. 

### Proof

By the Euclidean Algorithm, there exists integers $s,t$ s.t. $d = bs+ct$. This means:

$$a^d \equiv (a^b)^s+(a^c)^t \equiv 1 \mod n$$

If $a^b \equiv 1 \mod n$ then since $a^{ord_n(a)} \equiv 1 \mod n$ as well, we have that $e = \gcd(b, ord_n(a))$ satisfies $a^e \equiv 1 \mod n$. 

Then because $e | ord_n(a)$ and $ord_n(a)$ is the smallest value $k$ where $a^k \equiv 1 \mod n$, then $e|b \implies ord_n(a)|b$. 

## Corollary

If $\gcd(a,n) = 1$ then $ord_n(a) | \varphi(n)$. 

### Proof

We know that $a^{\varphi(n)} \equiv 1 \mod n$ so $ord_n(a) | \varphi(n)$. 

## Remarks

Distinct powers of $a^k \mod n$ are the same elements as the set $\\{a^k \mod n: 1 \leq k \leq ord_n(a)\\}$. 

$a$ is a primitive root of $\mathbb{Z}/n$ iff $ord_n(a) = \varphi(n)$. 











