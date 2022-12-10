name : moment generating function
tags : 
backlinks : 
source : Intro to Prob, https://en.wikipedia.org/wiki/Moment-generating_function

###### Content:
The moment generating function of a real-valued [[random variable]] is an alternative way to characterize the distribution. Thus, it provides the basis of an alternative route to analytical results compared with working directly with [[probability density function]]s or [[cumulative distribution function]]s. As the name suggests, it can be used to compute [[moment]]s of a random variable; the $n$th moment about 0 is the $n$th derivative of the moment generating function, evaluated at 0.

The moment generating function of a [[random variable]] $X$ is defined by $M(t)=E(e^{tX})$. It is a function of the real variable $t$.

When the moment generating function $M(t)$ of a random variable $X$ is finite in an interval around the origin, the moments of $X$ are given by: $$E(X^n)=M^{(n)}(0)$$
*In other words, taking the n-th derivative of $M(t)$ will give you the n-th moment of $X$. For example:*
$$M'(t) = \frac{d}{dt}E[e^{tX}]=E[\frac{d}{dt}e^{tX}] = E[Xe^{tX}]$$

**For a list of the moment generating functions of common distributions, go to the wikipedia link:**
For linking purposes:
- [[Bernoulli distribution]]
- [[geometric distribution]]
- [[binomial distribution]]
- [[negative binomial distribution]]
- [[uniform distribution]]
- [[poisson distribution]]
- [[normal distribution]]
- [[beta distribution]]
- [[gamma distribution]]
- [[exponential distribution]]


###### Properties:
- Not all random variables have moment generating functions
- The moment generating function is not random, but it is a function of the variable $t$. Since $e^0=1$, we have $M(0)=E[e^{0\cdot X}]=E[1]=1$ for all random variables.

###### Additional Thoughts:
