name : exponential distribution
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Exponential_distribution#:~:text=In%20probability%20theory%20and%20statistics,case%20of%20the%20gamma%20distribution.

###### Content:
A continuous [[probability distribution]] which models the "time between events which occur continuously and independently at a constant average rate". In other words, if you observe that an event happens every $t$ units of measurement, you can use this to predict the probability the next event will take $t_2$ units of measurement.

Let $0 < \lambda < \infty$. A random variable $X$ has the exponential distribution with parameter $\lambda$ if $X$ has the [[probability density function]] of:
$$f_X(t) = \lambda e^{-\lambda t}$$
$$\text{for } t \geq 0$$
on the real line. This is abbreviated by $X \sim Exp(\lambda)$. The $Exp(\lambda)$ is also called "the exponential distribution with rate $\lambda$".

**Example:**
Suppose the length of a phone call, in minutes, is well modeled by an exponential random variable with mean 10 minutes. What is the probability that a call takes more than 8 minutes?

Let $X$ be the length of the call. Since the mean is synonymous with the [[expectation]] for a [[continuous random variable]], we know $10 = \frac{1}{\lambda}$. Thus:
$$P(X>8) = 1-P(X<8) = 1-(1-e^{-8/10}) \approx 0.4493$$


**Parameters:**
$$\lambda > 0$$
**[[probability density function]]:**
$$f_X(t) = \begin{cases}
\lambda e^{-\lambda t} & t \geq 0\\
0 & t < 0
\end{cases}$$
**[[cumulative distribution function]]**
$$F_X(t) = 1-e^{-\lambda t}$$
**[[expectation]]:**
$$\frac{1}{\lambda}$$
**[[variance]]:**
$$\frac{1}{\lambda^2}$$

###### Properties:
- The exponential distribution is the continuous analog of the [[geometric distribution]]
- **Memoryless property:** Suppose that $X \sim Exp(\lambda)$. Then for any $s,t >0$ we have: $$P(X>t+s | X >t) = P(X>s)$$

###### Additional Thoughts:
