name : binomial distribution
tags : 
backlinks : [[binomial coefficient]]
source : Intro to Probability

###### Content:
A discrete [[probability distribution]], the binomial distribution arises from counting successes.
Let $n$ be a positive integer and $0 \leq p \leq 1$. A [[random variable]] $X$ has the binomial distribution with parameters $n$ and $p$ if the possible values of $X$ are $\{0,1,...,n\}$ and the probabilities are: $$P(X=k) = {n \choose k}p^k(1-p)^{n-k}$$ for $k=0,1,...,n$. This is abbreviated as $X \sim Bin(n,p)$

**Parameters:** $$0 \leq p \leq 1$$ $$n\geq 1$$
**[[probability mass function]]:** $$p_X(k) = {n \choose k}p^k(1-p)^{n-k}$$ $$0 \leq k \leq n$$
**[[cumulative distribution function]]:**
$$F_X(k) = \sum_{i=0}^k {n \choose i}p^i(1-p)^{n-i}$$
**[[expectation]]:** $$np$$
**[[variance]]:** $$np(1-p)$$

###### Properties:
- **[[normal distribution]] approximation of the binomial distribution using [[central limit theorem]]:** Suppose that $S_n \sim Bin(n,p)$, $n$ is large, and $p$ is not too close to 0 or 1. Then:
$$P(a \leq \frac{S_n -np}{\sqrt{np(1-p)}}<b)$$
is close to $\phi(b) - \phi(a)$ (see [[standard normal distribution]]). As a rule of thumb, this approximation is good if $np(1-p)>10$
- **Error bound in the [[normal distribution]]:** Let $S_n \sim Bin(n,p)$. Then for all values of $x$ we have: $$|P(\frac{S_n-np}{\sqrt{np(1-p)}} \leq x)- \phi(x)| \leq \frac{3}{\sqrt{np(1-p)}}$$

###### Additional Thoughts:
