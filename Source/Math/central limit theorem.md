name : central limit theorem
tags : 
backlinks : 
source : Intro to Probability, https://en.wikipedia.org/wiki/Central_limit_theorem

###### Content:
The central limit theorem states that when the realizations of [[independent]] [[random variable]]s are summed, their properly normalized sum tends toward a [[normal distribution]] even if the original variables themselves are not normally distributed. This theorem is a key concept in probability because it implies that methods that work for normal distributions can be applicable to many problems involving other types of distributions, assuming a large enough sample size.

*Note: For easy calculation, the resulting normal distribution can be normalized to a [[standard normal distribution]]*

**Central limit theorem for random variables with [[binomial distribution]]:**
Let $0<p<1$ be fixed and suppose that $S_n \sim Bin(n,p)$. Then for any fixed $-\infty \leq a \leq b \leq \infty$ we have the limit:
$$\underset{n \rightarrow \infty}{lim} P(a \leq \frac{S_n -np}{\sqrt{np(1-p)}}<b) = \int_a^b \frac{1}{\sqrt{2\pi}}e^{-x^2/2}dx$$
If $n$ is large and $p$ is not too close to 0 or 1. Then:
$$P(a \leq \frac{S_n -np}{\sqrt{np(1-p)}}<b)$$
is close to $\phi(b) - \phi(a)$ (see [[standard normal distribution]]). As a rule of thumb, this approximation is good if $np(1-p)>10$

###### Properties:


###### Additional Thoughts:
