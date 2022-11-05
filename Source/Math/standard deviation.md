name : standard deviation
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Standard_deviation

###### Content:
In statistics, the standard deviation is a measure of the amount of variation or dispersion of a set of values. 
Let $\mu$ be the [[expectation]] of the [[random variable]] $X$ with [[probability density function]] $f(x)$:
$$\mu = E[X] = \int_{-\infty}^{\infty}x f(x)dx$$
And the standard deviation $\sigma$ of $X$ is defined as:
$$\sigma = \sqrt{E[(X-\mu)^2]}=\sqrt{\int_{-\infty}^{\infty}(x-\mu)^2 f(x)dx}$$
which can be shown to equal $\sqrt{E[X^2]-(E[X])^2}$, thus the standard deviation is the square root of the [[variance]] of $X$

###### Properties:
- A low standard deviation indicates that the values tend to be close to the mean (or [[expectation]]) of the [[set]]
- The standard deviation of a [[probability distribution]] is the same as that of a random variable having that distribution
- Not all random variables have a standard deviation. If the distribution has fat tails going out to infinity, the standard deviation might not exist, because the integral might not converge. The [[normal distribution]] has tails going out to infinity, but its mean and standard deviation do exist, because the tails diminish quickly enough.

###### Additional Thoughts:
