name : geometric distribution
tags : 
backlinks : 
source : Intro to Probability

###### Content:
A discrete [[probability distribution]] that represents the probability of a number of consecutive failures before a success is obtained in a [[Bernoulli distribution]] trial.
Let $0 < p \leq 1$. A [[random variable]] $X$ has the geometric distribution with success parameter $p$ if the possible values of $X$ are $\{1,2,3,...\}$ and $X$ satisfies $P(X = k) = (1-p)^{k-1}p$ for positive integers $k$. This is abbreviated by $X \sim Geom(p)$

**Parameters:** $0 < p \leq 1$
**[[probability mass function]]:** $$p_X(k) = p(1-p)^{k-1}$$ $$k=1,2,...$$
**[[cumulative distribution function]]:** $$1-(1-p)^k$$
**[[expectation]]:** $$\frac{1}{p}$$
**[[variance]]:** $$\frac{1-p}{p^2}$$

###### Properties:


###### Additional Thoughts:
