# Sept 3: Rings and Fields

## Rings

Definition: A ring is a triple $(R, +, \cdot)$ where $R$ is a set, $+$ is a function, and $\cdot$ is a function where 

$$+:   \space R \times R \rightarrow R$$
$$\cdot:   \space R \times R \rightarrow R$$

This means that the function inputs two elements of $R$ and outputs one element in $R$.


If $a, b \in R$, we write $a+b$ and $ab$ s.t.

1. $+$ is commutative
2. $+$ and $\cdot$ are associative
3. $\exists 0 \in R$ s.t. $\forall a \in R$, $a + 0=a$
4. $\exists 1 \in R$ s.t. $\forall a \in R$, $a \cdot 1 = 1 \cdot a =a$
      - Note that the commutativity of multiplication is not implied, hence needs to be stated such.
5. The distributive law
      - $a(b+c) = ab + ac$
      - $(b+c)a = ba + ca$
      - This allows us to distinguish $+$ and $\cdot$
6. $\forall a \in R$, $\exists -a \in R$ s.t. $a + (-a) = 0$

If for a ring, $\cdot$ is commutative, we say that it is a commutative ring. 

There is a particular zero ring $R = \\{ 0 \\}$ where the "1" is also 0.

Examples: 
- the integers $\mathbb{Z}$
- the rationals $\mathbb{Q}$
- the reals $\mathbb{R}$
- complex numbers $\mathbb{C}$
- If $R$ is a ring, then $R\[x\]$, the polynomials with coefficients in $R$ is also a ring
- Matrices $M_n(\mathbb{Q})$
- $\mathbb{Z\[\sqrt{3}\]} = \\{a+b\sqrt{3} | a,b \in \mathbb{Z} \\}$

Counters: 
- the naturals (fails additive inverse rule)

## Fields

Definition: A field $F$ is a ring s.t. $\forall a \neq 0 \in F$, $\exists a^{-1} \in F$, s.t. $aa^{-1} = a^{-1}a = 1$

Examples:
- the rationals $\mathbb{Q}$
- the reals $\mathbb{R}$
- complex numbers $\mathbb{C}$
- the integers mod $n$

## Homomorphisms

Definition: A homomorphism of rings $\varphi(R \rightarrow S)$ is a function s.t.

1. $\varphi(a+b) = \varphi(a)+\varphi(b)$
2. $\varphi(ab) = \varphi(a)\varphi(b)$
3. $\varphi(0) = 0$
4. $\varphi(1) = 1$

It takes in an input and outputs a result in a new ring. For example: 


$$\begin{aligned}
\mathbb{R} & \rightarrow \mathbb{R}\[x\] \\
a & \rightarrow a
\end{aligned}$$

Definition: A homomorphism is called an isomorphism if it is bijective, which means 

$$\forall s \in S \space \exists \! r \in R \space \mathrm{s.t.} \space \varphi(r) = s$$



