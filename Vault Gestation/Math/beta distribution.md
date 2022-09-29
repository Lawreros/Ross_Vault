name : beta distribution
tags : 
backlinks : 
source : Intro to Probability, https://stats.stackexchange.com/questions/47771/what-is-the-intuition-behind-beta-distribution, https://byjus.com/maths/beta-distribution/

###### Content:
A continuous [[probability distribution]] set on the interval $[0,1]$ having two positive shape parameters, expressed by $\alpha$ and $\beta$ ($r,s$ in the equations below). The most common use of this distribution is to model the uncertainty about the probability of success of a random experiment. The Beta distribution is best for representing the a probabilistic distribution of probabilities: the case where we don't know what a probability is in advance, but we have some reasonable guesses. 
In other words, given the number of success and failures in a sample of events, we can calculate the probability distribution of the success rate (*"If 40% of this sample group is successes, what is the probability that the true success rate is between 35% and 45%?"*). 

Let $r,s>0$. A [[random variable]] $X$ has the beta distribution with parameters $(r,s)$ if $0<X<1$ and $X$ has the [[probability density function]]:
$$f(x) = \frac{\Gamma(r+s)}{\Gamma(r) \Gamma(s)}x^{r-1}(1-x)^{s-1}$$ where $0<x<1$. This is abbreviated $X \sim Beta(r,s)$. Where the gamma function: $$\Gamma(z) = \int_0^\infty x^{z-1}e^{-x}dx$$ and for any positive integer $z$: $\Gamma(z) = (z-1)!$

**Example:**
https://stats.stackexchange.com/questions/47771/what-is-the-intuition-behind-beta-distribution
https://byjus.com/maths/beta-distribution/

**Parameters:**
$$r,s > 0$$
**[[probability density function]]:**
$$f_X(x) = \frac{\Gamma (r+s)}{\Gamma (r) \Gamma (s)}x^{r-1}(1-x)^{s-1}$$
$$\text{for } 0 \leq t \leq 1$$
**[[cumulative distribution function]]:**
$$F(x) = \frac{\int_0^x t^{r-1}(1-t)^{s-1}dt}{\int_0^1 t^{r-1}(1-t)^{s-1}dt}$$
$$\text{for } 0 \leq x \leq 1$$
**[[expectation]]:**
$$\frac{r}{r+s}$$
**[[variance]]:**
$$\frac{rs}{(r+s)^2(r+s+1)}$$

###### Properties:
- You can update your beta distribution with each new data point by taking the original distribution $Beta(\alpha, \beta)$ and adding the number of successes and failures to get $Beta(\alpha+success, \beta+failures)$

###### Additional Thoughts:
