name : cumulative distribution function (CDF)
tags : 
backlinks : 
source : 

###### Content:
The cumulative distribution function of a real-valued [[random variable]] $X$, evaluated at point/outcome $x$, is the probability that $X$ will take a value less than or equal to $x$.

The cumulative distribution function of a real-valued random variable $X$ is the function given by: $$F_X(x) = P(X\leq x)$$

###### Properties:
- The probability that $X$ lies in the semi-closed interval $(a,b]$, where $a < b$, is therefore: $$P(a<X \leq b) = F_X(b)-F_X(a)$$
- The CDF of a [[discrete random variable]] $X$ can be expressed as the sum of the discrete values of its [[probability mass function]] $p_X$ as follows: $$F_X(x) = P(X \leq x) = \sum_{x_i \leq x} p(x_i)$$
- The CDF of a [[continuous random variable]] $X$ can be expressed as the integral of its [[probability density function]] $f_X$ as follows: $$F_X(x) = \int_{-\infty}^x f_X(t)dt$$

###### Additional Thoughts:
