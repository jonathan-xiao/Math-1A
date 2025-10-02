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





