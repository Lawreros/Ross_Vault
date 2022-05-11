name : binomial distribution
tags : 
backlinks : [[binomial coefficient]]
source : Intro to Probability

###### Content:
A discrete [[probability distribution]], the binomial distribution arises from counting successes.
Let $n$ be a possitive integer and $0 \leq p \leq 1$. A [[random variable]] $X$ has the binomial distribution with parameters $n$ and $p$ if the possible values of $X$ are $\{0,1,...,n\}$ and the probabilities are: $$P(X=k) = {n \choose k}p^k(1-p)^{n-k}$$ for $k=0,1,...,n$. This is abbreviated as $X \sim Bin(n,p)$

**Parameters:** $$0 \leq p \leq 1$$ $$n\geq 1$$
**[[probability mass function]]:** $$p_X(k) = {n \choose k}p^k(1-p)^{n-k}$$ $$0 \leq k \leq n$$
**[[expectation]]:** $$np$$
**[[variance]]:** $$np(1-p)$$

###### Properties:


###### Additional Thoughts:
