name : gamma distribution
tags : 
backlinks : 
source : https://www.mygreatlearning.com/blog/gamma-distribution/, https://en.wikipedia.org/wiki/Gamma_distribution

###### Content:
A continuous [[probability distribution]] that is widely used to model continuous variables that are always positive and have skewed distributions. It is often used to predict the waiting time until future events occur; the gamma distribution predicts the wait time until the $r$-th event occurs, with the rate of events being $\lambda$. It can be thought of as the waiting time between events with a [[poisson distribution]].

Let $r,\lambda >0$. A [[random variable]] $X$ has the gamma distribution with parameters $(r,\lambda)$ if $X$ nonnegative and has [[probability density function]]: $$f_X(x) = \frac{\lambda^r x^{r-1}}{\Gamma(r)}e^{-\lambda x}$$ for $x\geq 0$, with $f_X(x)=0$ for $x<0$. We abbreviate this $X \sim Gamma(r,\lambda)$

Where the **gamma function** is defined as:
$$\Gamma(r) = \int_0^\infty x^{r-1}e^{-x}dx$$
for $r>0$. The gamma function generalized the factorial function: if $n$ is a positive integer then $\Gamma(n) = (n-1)!$.

**Example:**
Suppose that you are fishing and expect to get a fish every 0.5 hours. Compute the probability that you will have to wait between 2 to 4 hours before you catch 4 fish.
One fish every 0.5 hours means that we would expect $\lambda = 0.5$, and wanting to catch 4 fish means $r=4$. Thus:
$$P(2\leq X \leq 4) = \sum_{x=2}^4 \frac{0.5^4 x^{4-1}}{\Gamma(4)}e^{-0.5 x} = 0.12388$$


**Parameters:**
$$r \geq 1 \text{ "number of events"}$$
$$\lambda >0 \text{ "mean time between events"}$$
**[[probability density function]]:**
$$f_X(t) = \frac{\lambda^r t^{r-1}}{\Gamma(r)}e^{-\lambda t}$$
$$\text{for } t\geq0$$
**[[cumulative distribution function]]:**
$$F(x) = \frac{1}{\Gamma(r)}\int_0^{\lambda x} t^{r-1}e^{-t}dt$$
**[[expectation]]:**
$$\frac{r}{\lambda}$$
**[[variance]]:**
$$\frac{r}{\lambda^2}$$

###### Properties:
- The [[exponential distribution]] is a special case of the gamma distribution: $Exp(\lambda)$ is the same distribution as $Gamma(1,\lambda)$
- Depending on notation, you may see this equation using $\theta$, which represents the mean number of events per time unit. In other words: $\theta = \frac{1}{\lambda}$. It is the same equation, just organized differently.

###### Additional Thoughts:
