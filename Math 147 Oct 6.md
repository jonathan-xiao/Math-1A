## Theorem

Let $a_n$ be a sequence of nonzero real numbers. Then:

$$\lim \inf \left|\frac{a_{n+1}}{a_n}\right| \leq \lim \inf |a_n|^{\frac{1}{n}} \leq \lim \sup |a_n|^{\frac{1}{n}} \leq \lim \sup \left|\frac{a_{n+1}}{a_n}\right|$$

### Proof

Let $\alpha = \lim \sup |a_n|^{\frac{1}{n}}$ and $L = \lim \sup \left|\frac{a_{n+1}}{a_n}\right|$. If $L$ is infinite then the theorem is trivially true. 

Suppose that $L$ is finite. Fix $\epsilon > 0$. Let $L_1 = L + \epsilon$. Then we know that $L < L_1$. Therefore, $\exists N$ s.t. 

$$\sup\\{\left|\frac{a_{n+1}}{a_n}\right|: n \geq N\\} \leq L < L_1$$

AKA there exists one term within distance $\epsilon$ of $L$, which means it is closer to $L$ than $L_1$ is. This means $\left|\frac{a_{n+1}}{a_n}\right| < L_1$ for all $n \geq N$. Now, for all $n \geq N$, 

$$|a_n| = \left|\frac{a_{n}}{a_{n-1}}\right| \cdot \left|\frac{a_{n-1}}{a_{n-2}}\right| \cdot ... \cdot \left|\frac{a_{N+1}}{a_N}\right| \cdot |a_N|$$

The number of fraction terms on the right is $n-N$, each of which are less than $L_1$, which means $|a_n| < L_1^{n-N} \cdot |a_N|$.

Therefore:

$$\begin{aligned}
|a_n| &\leq L_1^n \cdot L_1^{-N} \cdot |a_N| \\
|a_n|^{\frac{1}{n}} &\leq L_1(L_1^{-N} \cdot |a_N|)^{\frac{1}{n}}
\end{aligned}$$

Because we are raising that second term on the right to the $-n$-th power, we get the bracket tending to 1. Therefore, $L_1(L_1^{-N} \cdot |a_N|)^{\frac{1}{n}} \to L_1$. This means that:

$$\lim \sup |a_n|^{\frac{1}{n}} \leq L_1$$

Which means that, because $L < L_1$ was arbitrary, 

$$\lim \sup |a_n|^{\frac{1}{n}} \leq L$$

The other inequalities follow by symmetry and the definition of inf and sup.

# Ratio Test

Let $\sum a_n$ be a series of nonzero terms. Then $\sum a_n$

1. Converges absolutely if $\lim \sup \left|\frac{a_{n+1}}{a_n}\right| < 1$
2. Diverges if $\lim \inf \left|\frac{a_{n+1}}{a_n}\right| > 1$
3. Otherwise, the test gives no information.

## Proof

Let $\alpha = \lim \sup |a_n|^{\frac{1}{n}}$. We then have:

$$\lim \inf \left|\frac{a_{n+1}}{a_n}\right| \leq \alpha \leq \lim \sup \left|\frac{a_{n+1}}{a_n}\right|$$

If $\lim \sup \left|\frac{a_{n+1}}{a_n}\right| < 1$ then $\alpha < 1$ so by the Root Test, the series converges.
If $\lim \inf \left|\frac{a_{n+1}}{a_n}\right| > 1$ then $\alpha > 1$ so by the Root Test, the series diverges.

Otherwise, see $\sum \frac{1}{n}$ and $\sum \frac{1}{n^2}$.

## Corollary

If $\lim \left|\frac{a_{n+1}}{a_n}\right| = L$ then $\lim |a_n|^{\frac{1}{n}} = L$. 

## Remark

The Ratio Test is weaker than the Root Test. You may have a sequence that has no information in the Ratio Test but is convergent or divergent by the Root Test.

Use the Ratio Test when you have cancellations, like factorials. Use the Root Test if terms are raised to the $n$-th power.

## Recall

$\sum a_n$ converges if $a_n \to 0$, but the reverse does not have to be true. 

# Alternating Series Test

Suppose that $a_n$ is a decreasing series of non-negative terms and $\lim a_n \to 0$. Then $\sum (-1)^n a_n \to L$. 

## Proof

Let $s_n$ denote the partial sums of $\sum a_n$. You can see than even terms of $s_n$ are negative and odd terms are positive. 

Note that the even terms of $s_n$ are increasing since we know that $s_{2n+2} - s_{2n} = -a_{2n+2}+a_{2n+1} \geq 0$. 
Note that the odd terms of $s_n$ are decreasing since we know that $s_{2n+1} - s_{2n-1} = a_{2n+1}-a_{2n} \leq 0$. 

So now $s_{2n+1}-s_{2n} = a_{2n+1} \geq 0$. This means that if $m \leq n$ then $s_{2m} \leq s_{2n} \leq s_{2n+1}$ and if $m \geq n$ then $s_{2n+1} \geq 2_{2m+1} \geq s_{2m}$. 

Let $s_{2n} \to L$ and $s_{2n+1} \to L'$. Observe that:

$$L'-L = \lim s_{2n+1} - \lim s_{2n} = \lim (s_{2n+1] - s_{2n}) = \lim a_{2n+1} = 0$$.

Therefore, $L = L'$. 

# Conditionally Convergent

If $\sum a_n$ converges but $\sum |a_n|$ does not, then the series $\sum a_n$ is conditionally convergent. 

## Theorem

Let $\sum a_n$ be an absolutely convergent series of nonzero real numbers, and let $\sum b_n$ be a rearrangement of $\sum a_n$. Then $\sum b_n$ is also absolutely convergent and both series converge to the same limit. 

## Theorem

Let $a_n$ be a sequence of real numbers. Let $k \in \mathbb{R}$. Suppose that $\sum a_n$ converges conditionally. Then there exists a rearrangement $\sum b_n$ of $\sum a_n$ that converges to $k$.

## Rearrangement

Let $a_n$ is a sequence indexed by $I$. Let $\pi(n): I \to I$ be a bijection. Then $a_{\pi(n)}$ is a rearrangement of $a_n$. 








