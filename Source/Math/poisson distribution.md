name : poisson distribution
tags : 
backlinks : 
source : Intro to Probability

###### Content:
A discrete [[probability distribution]] that expresses the probability of a given number of events occurring in a fixed interval of time or space if these events occur with a known constant mean rate and are [[independent]] of the time since the last event. The Poisson distribution can also be used for the number of events in other specified interval types, such as distance, area, or volume.

Let $\lambda >0$. A [[random variable]] $X$ has the Poisson distribution with parameter $\lambda$ if $X$ is a nonnegative integer valued and has the [[probability mass function]]: $$P(X=k) = e^{-\lambda}\frac{\lambda^k}{k!}$$ for $k \in \{0,1,2,...\}$. Abbreviate this by $X \sim Poisson(\lambda)$

**Example:**
On a particular river, overflow floods occur twice every 100 years on average. Calculate the probability of $k=3$ overflow floods in a 100-year interval, assuming the Poisson model is appropriate. Because the average event rate is 2 every 100 years, $\lambda = 2$:
$$P(k = 3) = \frac{2^3}{3!}e^{-2} = 0.18045$$

**Parameters:** $\lambda > 0$
**[[probability mass function]]:** $$p_X(k) = \frac{\lambda^k}{k!}e^{-\lambda}$$ With the number of events: $k = 0,1,2,...$
**[[cumulative distribution function]]:**
**[[expectation]]:** $$\lambda$$
**[[variance]]:** $$\lambda$$

###### Properties:
- It is assumed that the occurrence of one event does not affect the probability that a second event will occur.

###### Additional Thoughts:
