name : probability density function (p.d.f.)
tags : 
backlinks : 
source : Intro to Probability

###### Content:
Let $X$ be a [[random variable]]. If a function $f$ satisfies: $$P(X \leq b) = \int_{\infty}^b f(x)dx$$ for all real values $b$, then $f$ is the probability density function (p.d.f.) of $X$

###### Properties:
- If a random variable $X$ has a density function $f$ then point values have probability zero: $$P(X=c) = \int_c^c f(x)dx = 0$$ for any real $c$
- Suppose that random variable $X$ has density function $f$ that is continuous at the point $a$. Then for small $\epsilon > 0$: $$P(z < X < a+\epsilon) \approx f(a) \cdot \epsilon$$

###### Additional Thoughts:
