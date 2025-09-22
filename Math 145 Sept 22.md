# Equivalence Relations

The necessary conditions are:

1. Reflexivity
2. Symmetrical
3. Transitivity

For $a \in S$, we say the equivalence class of $a$ is $[a] = \\{b \in S| b \sim a\\}$. We also have:

$$S/\sim = \\{[a] | a \in S \\}$$

## Lemma

Addition and multiplication are well-defined in modular.

### Proof

If $[a_1]=[a_2]$ then $a_1 \equiv a_2 \space \mod{n}$. If $[b_1]=[b_2]$ then $b_1 \equiv b_2 \space \mod{n}$.

For addition, $a_1+b_1 \equiv a_2+b_2 \mod n$ which directly means $[a_1+b_1]=[a_2+b_2]$. 

For multiplication, $a_1b_2 \equiv a_2b_2 \mod n$ which means $[a_1b_1]=[a_2b_2]$. 

## Proposition

The integers mod $n$ is a commutative ring.

### Proof

You will need to prove every axiom for this. In terms of commutativity, we have:

$$[a][b] = [ab] = [ba] = [b][a]$$

The additive identity is $[0]$ and the multiplicative identity is $[1]$. 

## Proposition

The integers mod $n$ are a field only when $n$ is prime. 

### Proof

Suppose $n$ is composite. Then $n=ab$ where $a,b$ are not itself or a unit. We can possibly have $[a][b]=[n]=0$ where neither $[a]$ nor $[b]$ are 0. 

Assume that $[a]$ has a multiplicative inverse. Then we have $[a][b] = 0$ and multiplying the inverse on both sides, $[b]=0$. Because $b < n$ it is impossible for $b$ to be in the equivalence class as $n$. So this statement is false.

## Lemma

If $\gcd(a,n)=1$ then $ax \equiv b \mod n$ has a unique solution mod $n$. 

### Proof

Consider $f: \mathbb{Z}/n \rightarrow \mathbb{Z}/n$ which is $f:[a] \rightarrow [ax]$. Saying that $ax \equiv b \mod n$ has a unique solution mod $n$ is the same as saying $f$ is bijective.

Suppose that $x,y$ are in $\mathbb{Z}/n$ with $[ax]=[ay]$. Then, we have that:

$$\begin{aligned}
ax &\equiv ay \mod n \\
n &| a(x-y) \\
n &| (x-y) \\
x &\equiv y \mod n \\
[x] &= [y] 
\end{aligned}$$

This means that $f$ is injective. Note that the input and output sets have equal numbers of elements. So this also means $f$ is surjective. Therefore, $f$ is bijective.

## Corollary

The units of $\mathbb{Z}/n$ are $\\{[a]|\gcd(a,n)=1\\}$. 

### Proof

If $\gcd(a,n) = 1$ then there exists unique $[x]$ s.t. $[a][x]=1$. 

Suppose that $[a][b]=1$. Then $ab+cn=1$. Therefore, $\gcd(a,n)$ divides both $a$ and $n$ and so it can only divide 1. So because we are working with integers, $\gcd(a,n)=1$. 

# Chinese Remainder Theorem

If $\gcd(n,m)=1$ then,

$$x \equiv a \mod m$$
$$x \equiv b \mod n$$

has a unique solution mod $mn$. 

### Proof

We know $x = a + my = b + nz$ and so $my-nz=b-a$. 

By the proposition, then there are solutions $y_0$ and $z_0$ where 

$$y = y_0 + nk$$
$$z = z_0 + mk$$

Note the sign is changed because $my-nz$ has the negative. 

Therefore, we have $x = a + my_0 + mnk$. Therefore $x = a+my_0$ is the unique solution mod $mn$. 

