name : continuous random variable
tags : 
backlinks : 
source : Intro to Probability

###### Content:
A [[random variable]] whose range of potential events is uncountably infinite.

**[[probability density function]]:** $f_X(x)$
$$P(X \in B) = \int_B f_X(x)dx$$
**[[cumulative distribution function]]:** $F_X(a) = P(X \leq a)$
$F_X(a) = \int_{-\infty}^a f(x)dx$ where $f_X$ is a continuous function
$$P(X<a) = \underset{t \rightarrow a^-}{lim} F(t) = F(a-)$$ $$P(X=a) = F(a) - \underset{t \rightarrow a^-}{lim} F(t) = F(a)-F(a-)$$
**[[expectation]]:** $E(X) = \int_{-\infty}^{\infty}xf(x)dx$
$$E(aX+b) = aE[X]+b$$
$$E[g(X)]=\int_{-\infty}^{\infty}g(x)f(x)dx$$
**[[variance]]:** $Var(X) = E[(X-E[X])^2] = E[X^2]-(E[X])^2$
$$Var(aX+b) = a^2Var(X)$$

###### Properties:
- Suppose that a random variable $X$ has density function $f$ that is continuous at the point $a$. Then for small $\epsilon >0$: $$P(a<X<a+\epsilon) \approx f(a)\cdot \epsilon$$

###### Additional Thoughts:
