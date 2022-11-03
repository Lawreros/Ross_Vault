name : joint cumulative distribution function
tags : 
backlinks : 
source : Intro to Prob

###### Content:
The joint cumulative distribution function of [[random variable]]s $X_1,X_2,...,X_n$ is a function of $n$ variables defined as $$F(s_1,...,s_n) = P(X_1 \leq s_1,...,X_n\leq s_n)$$ for all $s_1,...,s_n \in \mathbb{R}$.

###### Properties:
- If $X$ and $Y$ have [[joint probability density function]] $f$ then their joint cumulative distribution function is: $$F(x,y) = P(X\leq x, Y \leq y) = \int_{-\infty}^{x}\int_{-\infty}^{y}f(s,t)dtds$$
- If $X$ and $Y$ have [[joint probability mass function]] $p$ then their joint cumulative distribution function is : $$F(x,y) = P(X\leq x, Y\leq y) = \sum_{x_i < x}\sum_{y_j < y}p(x_i,y_j)$$

###### Additional Thoughts:
