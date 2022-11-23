name : negative binomial distribution
tags : 
backlinks : [[binomial distribution]]
source : Intro to Probability

###### Content:
A discrete [[probability distribution]] that models the number of failures $(n-k)$ in a sequence of independent and identically distributed trials with [[Bernoulli distribution]] 
$n$ before a specified number of successes $k$ occurs. In other words, what is the probability that in $n$ attempts, $k$ successes occur. 

Let $k$ be a positive integer and $0<p<1$. A [[random variable]] $X$ has the negative binomial distribution with parameters $(k,p)$ if the [[set]] of possible values of $X$ is the set of integers $\{k, k+1,k+2,...\}$ and the [[probability mass function]] is:
$$P(X=n)={n-1 \choose k-1}p^k(1-p)^{n-k}$$ 
for $n \geq k$. This is abbreviated by $X \sim Negbin(k,p)$

**Example:**
Two people are playing a "best-of-7" game series, where the first to get 4 wins wins the entire thing. If person $A$ has a $0.45$ chance to win, what is the probability that they will with the series in $6$ games?
$$P(X=6) = {5 \choose 3}0.45^4 (0.55)^{6-4} \approx 0.12$$


**Parameters:** $$k \geq 1$$ $$0 < p \leq 1$$
**[[probability mass function]]:** $$p_X(n) = {n-1 \choose k-1}p^k(1-p)^{n-k}$$ $$n \geq k$$
**[[cumulative distribution function]]:**
*see wikipedia*
**[[expectation]]:** $$\frac{kp}{1-p}$$
**[[variance]]:** $$k\frac{1-p}{p^2}$$

###### Properties:
- The $Negbin(1,p)$ distribution is the same as the [[geometric distribution]] $Geom(p)$.

###### Additional Thoughts:
