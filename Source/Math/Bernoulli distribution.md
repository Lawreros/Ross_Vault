name : Bernoulli distribution
tags : 
backlinks : 
source : Intro to Probability

###### Content:
A discrete [[probability distribution]] of a [[random variable]] which takes the value 1 with probability $p$ and the value 0 with probability $q = 1-p$. Less formally, it can be thought as a model for the set of possible outcomes of any single experiment that asks a yes-no question. This is often abbreviated as $X \sim Ber(p)$
*Note: This is a single event, multiple Bernoulli's make a binomial*

**Parameters:** $0 \leq p \leq 1$
**[[probability mass function]]:** $$p_X(0) = 1-p$$ $$p_X(1) = p$$
**[[expectation]]:** $p$
**[[variance]]:** $p(1-p)$

###### Properties:
- A Bernoulli distribution is a special case of the [[binomial distribution]] where a single trial is conducted (so $n$ would be 1 for such a binomial distribution)

###### Additional Thoughts:
