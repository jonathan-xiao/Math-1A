# Fermat's Little Theorem 

If $p$ is prime and $a$ does not divide $p$, then $a^{p-1} \equiv 1 \mod p$. 

## Corollary

If $a$ is a unit in $\mathbb{Z}/p$, then $[a]^{-1} = [a]^{p-2}$. 

## Wilson's Theorem

If $p$ is prime, then $(p-1)! \equiv -1 \mod p$. 

### Proof

If $p=2$ then $1! \equiv 1 \equiv -1 \mod 2$. 

Otherwise, if $p$ is odd, then $[(p-1)!] = [1][2][3] ... [p-1]$.

Since $p$ is prime, then $\mathbb{Z}/p$ is a field. Then there exists inverses for every element except where $a^2-1 \equiv 0 \mod p$. These would be $a = \pm 1$. 

So we can cancel every element that has an inverse, leaving us with $\pm 1$. 

$[(p-1)!] = [1][-1] = [-1]$.

# Euler's Totient Function

$\varphi(n)$ gives the number of relatively prime natural numbers between $1$ and $n$. 

For example, $\varphi(p) = p-1$ and $\varphi(p^n) = p^n(1-\frac{1}{p})$. 

## Theorem

If $\gcd(a,n) = 1$ then $a^{\varphi(n)} \equiv 1 \mod n$. 

### Proof

Suppose $f: (\mathbb{Z}/n)^* \to (\mathbb{Z}/n)^*$ is a function $f: [x] \to [ax]$. This is a bijection.

This means that the set of all elements in the input is the same as the set of the outputs. So we multiply all the terms. 

$$\begin{aligned}
\prod_{x \in (\mathbb{Z}/n)^{\*}} [x] &= \prod_{x \in (\mathbb{Z}/n)^{\*}} [ax] \\
&= [a^{\varphi(n)}] \prod_{x \in (\mathbb{Z}/n)^{\*}} [x] \\
[1] &= [a^{\varphi(n)}] 
\end{aligned}$$

## Proposition

If $\gcd(n,m) = 1$ then $\varphi(nm) = \varphi(n) \varphi(m)$. 

### Proof

Let $S_k = \\{ 1 \leq a \leq k | \gcd(a,k) = 1\\}$. Then $\gcd(x,nm) = 1$ iff $\gcd(x,m) = 1$ and $\gcd(x,n) = 1$. 

So $\forall a \in S_n, b \in S_m$, Consider $x \equiv a \mod n$ and $x \equiv b \mod n$. 

By the Chinese Remainder solution, there is a unique solution $c \mod mn$, which is in $S_{nm}$. Conversely, for every one element in $S_{mn}$ there is $a \equiv x \mod n$ in $S_n$ and $b \equiv x \mod m$ in $S_m$.

So $\varphi(nm) = |S_{nm}| = |S_n||S_m| = \varphi(n) \varphi(m)$





