name : Student's t-distribution (t-distribution)
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Student%27s_t-distribution

###### Content:
The Student's t-distribution is any member of a family of [[continuous random variable]] [[probability distribution]]s that arise when estimating the mean of a population with [[normal distribution]] in situations where the sample size is small and the population's [[standard deviation]] is unknown. The [[probability density function]] of the Student's t-distribution depends on the number of [[degrees of freedom]], hence why it is required when running a [[t-test]]

The t-distribution plays a role in a number of widely used statistical analyses, including [[t-test]]s for assessing the [[statistical significance]] of the difference between two sample means, the construction of [[confidence interval]]s for the difference between two population means, and in [[linear regression]] analysis.

###### How Student's distribution arises from sampling:
Let $X_1, ..., X_n$ be [[independent]]ly and identically drawn from the [[normal distribution]] $N(\mu,\sigma^2$). Let:
$$\bar X = \frac{1}{n} \sum_{i=1}^nX_i$$
be the [[sample mean]] and let $$S^2 = \frac{1}{n-1}\sum_{i=1}^n(X_i-\bar{X})^2$$
be the [[sample variance]]. Then the random variable: $$\frac{\bar X - \mu}{\sigma / \sqrt{n}}$$ has a [[standard normal distribution]] and the [[random variable]] $$\frac{\bar X - \mu}{S / \sqrt{n}}$$ has a Student's t-distribution with $n-1$ [[degrees of freedom]]. Since $S$ has replaced $\sigma$, the only unobservable quantity of this expression is $\mu$, so this can be used to derive confidence intervals for $\mu$.

**[[probability density function]]:** See link
**[[cumulative distribution function]]:** See link

###### Properties:
- The _t_-distribution is symmetric and bell-shaped, like the [[normal distribution]]. However, the _t_-distribution has heavier tails, meaning that it is more prone to producing values that fall far from its mean. This makes it useful for understanding the statistical behavior of certain types of ratios of random quantities, in which variation in the denominator is amplified and may produce outlying values when the denominator of the ratio falls close to zero.
- If we take a sample of $n$ observations from a normal distribution, then the t-distribution with $\nu=n-1$ degrees of freedom can be defined as the distribution of the location of the sample mean relative to the true mean, divided by the sample standard deviation, after multiplying by the standardizing term $\sqrt {n}$. In this way, the t-distribution can be used to construct a [[confidence interval]] for the true mean.

###### Additional Thoughts:
