name : expectation (expected value)
tags : 
backlinks : 
source : Intro to Probability

###### Content:
The expected value (also called expectation, expectancy, mean, average, or first moment) of a [[random variable]] is a generalization of the weighted average, where the weights are given by the probabilities. Informally, the expected value is the mean of a large number of [[independent]]ly selected outcomes of a random variable.

**Expectation of a [[discrete random variable]]:**
The expectation of a random variable with a finite number of outcomes is a weighted average of all possible outcomes ([[probability mass function]]). The expectation or mean of a discrete random variable $X$ is defined by: $$E(X) = \sum_k kP(X=k)$$
where the sum ranges over all possible values $k$ of $X$.

**Expectation of a [[continuous random variable]]:**
The expectation of a random variable with a continuum of possible outcomes is defined by an integration where weighting is given by the [[probability density function]]. The expectation or mean of a continuous random variable $X$ with [[probability density function]] $f$ is:
$$E[X]= \int_{-\infty}^{\infty} x f(x)dx$$
and alternative symbol is $\mu = E[X]$.

###### Properties:
- The expectation is also called the "first moment" ([[nth moment]])
- Another conventional symbol for expectation is $E[X] = \mu$
- There exist random variables with infinite expectation values (see St. Petersburg paradox)
- **Expectation of a function of a random variable:** Let $g$ be a real-valued function defined on the range of a random variable $X$. If $X$ is a [[discrete random variable]] then $$E[g(X)] = \sum_k g(k)P(X=k)$$ while if $X$ is a [[continuous random variable]] with density function $f$ then $$E[g(X)] = \int_{-\infty}^{\infty}g(x)f(x)dx$$
- Let $X$ be a random variable and $a$ and $b$ real numbers, then $$E(aX+b) = aE(X)+b$$

###### Additional Thoughts:
