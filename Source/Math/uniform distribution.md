name : uniform distribution
tags : 
backlinks : 
source : Intro to Probability

###### Content:
A continuous [[probability distribution]] of a [[random variable]] whose outcome lies between certain bounds. The bounds are defined by the parameters $a$ and $b$, which are maximum and minimum values.

Let $[a,b]$ be a bounded interval on the real line. A random variable $X$ has the uniform distribution on the interval $[a,b]$ if $X$ has [[probability density function]]:
$$f(x) = \begin{cases}
\frac{1}{b-a} & x \in [a,b]\\
0 & x \notin [a,b]
\end{cases}$$
Abbreviate this by $X \sim Unif[a,b]$


**Parameters:**
$$a < b$$
**[[probability density function]]:**
$$f_X(t) = \frac{1}{b-a}$$
$$\text{for  } t \in [a,b]$$
**[[cumulative distribution function]]:** $$0 \text{ for } x<a$$
$$\frac{x-a}{b-a} \text{ for } x\in [a,b]$$
$$1 \text{ for } x<a$$
**[[expectation]]:**
$$\frac{a+b}{2}$$
**[[variance]]:**
$$\frac{1}{12}(b-a)^2$$

###### Properties:


###### Additional Thoughts:
