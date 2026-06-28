---
layout: single
title:  "Periodic Decimal Expansions"
date:   2026-06-07
categories: math
tags: math
---

When playing with the real numbers a clear difference between rationals and irrationals becomes clear. Irrationals will never exhibit any periodic behavior within their decimal expansions, while rationals will *always* be eventually periodic.

# Proof: Eventually Periodic Decimal Expansions Are Rational
Let $x$ be a real number strictly between $0$ and $1$ with an eventually periodic decimal expansion, that is, $x$ can be represented by a string of digits which will eventually become a repeating pattern, e.g. $\frac{1}{6} = 0.1666\dots$ More formally, this means $x$ can be expanded to the form $A10^{-m} + \sum_{i=1}^\infty B 10^{-(m+in)}$ where $A$ and $B$ are positive integers with the expansions $\sum_{i=0}^ma_i10^i$ and $\sum_{i=0}^nb_i10^i$, with $0 \leq m, 0 < n$ and $a_i, b_i \in \\{0, 1, ..., 9\\}$. Note that this definition includes terminating expansions as well as those which are wholly periodic. 
Then it follows,
  
$$
\begin{align*}
x &= A10^{-m} + \sum_{i=1}^\infty B 10^{-(m+in)} \\\\
10^mx &= A + \sum_{i=1}^\infty B 10^{-in}\\\\
10^mx - A &= \sum_{i=1}^\infty B 10^{-in} \\\\
10^{m+n}x - 10^nA &= \sum_{i=1}^\infty B 10^{n-in} = B + \sum_{i=1}^\infty B 10^{-in}\\\\
(10^{m+n}x - 10^nA) - (10^mx - A) &= B \\\\
10^{m+n}x - 10^mx &= B + 10^nA - A \\\\
\end{align*}
$$
  
and finally,   

$$
x = \frac{B + 10^nA - A}{10^{m+n}-10^m}
$$

therefore $x$ must be rational.   

While the property is proved above for $0 < x < 1$, it is trivial to extend it to all real numbers. Let $x'$ be a real number greater than $1$ with an eventually periodic expansion, then it can be represented by the expansion $10^k(A10^{-m} + \sum_{i=1}^\infty B 10^{-(m+in)})$ where $1 \leq k$. Define $x$ by $A10^{-m} + \sum_{i=1}^\infty B 10^{-(m+in)}$, then we have $x'=10^kx$. Since $x$ is rational from the previous proof $x'$ must be too. Its clear from this the property holds for all any negative number as well.

# Proof: Rationality Implies Eventually Periodic Expansions