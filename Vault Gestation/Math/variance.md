name : variance
tags : 
backlinks : [[expectation]], [[standard deviation]]
source : Intro to Probability

###### Content:
The variance of a [[random variable]] (or the realizations of a random variable) measures how much the random variable fluctuates around its mean.

Let $X$ be a [[random variable]] with mean $\mu$. The variance of $X$ is defined by $$Var(X) = E[(X-\mu)^2]$$ An alternative symbol is $\sigma^2 = Var(X)$

**Variance of a [[discrete random variable]]:**
Let $X$ be a random variable with mean $\mu$. Then $$Var(X) = \sum_k (k-\mu)^2P(X=k)$$
*Note: $\mu = E[X]$*

**Expectation of a [[continuous random variable]]:**
Let $X$ be a random variable with mean $\mu$. Then $$Var(X) = \int_{-\infty}^{\infty}(x-\mu)^2 f(x)dx$$
*Note: $\mu = E[X]$*

###### Properties:
- **Alternative formula for variance:** $Var(X) = E(X^2)-E(X)^2$
- Let $X$ be a random variable and $a$ and $b$ real numbers, then $$Var(aX+b) = a^2 Var(X)$$
- For a random variable $X$, $Var(X) = 0$ if and only if $P(X=a)=1$ for some real value $a$

###### Additional Thoughts:
