name : normal distribution (Gaussian distribution)
tags : 
backlinks : 
source : Intro to Probability

###### Content:
A continuous [[probability distribution]] for a real valued [[random variable]]. The normal distribution is important in statistics and is often used in the natural and social sciences to represent real-valued random variables whose distributions are not known. Their importance is partly due to the [[central limit theorem]], which states that, under some conditions, the average of many samples of a random variable with finite mean and [[variance]] is itself a random variable whose distribution converges to a normal distribution as the number of samples increases. Therefore, physical quantities that are expected to be the sum of many [[independent]] processes often have nearly normal distribution.

Let $\mu$ be real and $\sigma >0$. A [[random variable]] $X$ has the normal distribution with mean $\mu$ and [[variance]] $\sigma^2$ if $X$ has [[probability density function]]: $$f(x) = \frac{1}{\sqrt{2\pi \sigma^2}}e^{\frac{-(x-\mu)^2}{2\sigma^2}}$$
on the real line. Abbreviate this by $X \sim \mathcal{N}(\mu,\sigma^2)$.

**Parameters:**
$$\mu \in \mathbb{R}$$ $$ \sigma^2 > 0$$
**[[probability density function]]:**
$$f_X(t) = \frac{1}{\sqrt{2\pi \sigma^2}}e^{-\frac{(t-\mu)^2}{2\sigma^2}}$$
**[[cumulative distribution function]]:** *See below*
**[[expectation]]:**
$$\mu$$
**[[variance]]:**
$$\sigma^2$$

###### Properties:
- The sum/difference of two normal distributions is also a normal distribution
- You can easily estimate probabilities of different normal distributions by linear transformations of $Z$ and using the [[standard normal distribution]]. $$X = \sigma Z+\mu$$ Let $\mu$ be real, $\sigma >0$, and suppose $X \sim \mathcal{N}(\mu, \sigma^2)$. Let $a \neq 0$, $b$ real, and $Y = aX+b$. Then $Y\sim \mathcal{N}(a\mu+b, a^2\sigma^2)$, that is, $Y$ is normal distributed with mean $a\mu+b$ and variance $a^2\sigma^2$. In particular, $Z= \frac{X-\mu}{\sigma}$ is a standard normal random variable.
**Example:** Suppose $X \sim \mathcal{N}(-3,4)$. Find the probability $P(X\leq -1.7)$.
Since $Z = \frac{X-(-3)}{2} \sim \mathcal{N}(0,1)$ we have:
$$P(X\leq -1.7) = P(\frac{X-(-3)}{2} \leq \frac{-1.7-(-3)}{2}) = P(Z\leq 0.65)$$ $$= \phi(0.65) \approx 0.7422$$

###### Additional Thoughts:
