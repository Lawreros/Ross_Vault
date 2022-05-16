name : discrete random variable
tags : 
backlinks : 
source : Intro to Probability

###### Content:
A [[random variable]] $X$ is discrete if there exists a finite or countably infinite set $\{k_1,k_2,k_3,...\}$ of real numbers such that $$\sum_i P(X=k_i) = 1$$ where the sum ranges over the entire set of points $\{k_1,k_2,k_3,...\}$

###### Properties:
- [[probability mass function]]: $p_X(k) = P(X=k)$ for possible values $k$ of $X$
- $P(X \in B) = \sum_{k:k\in B}p_X(k)$
- [[cumulative distribution function]]:
- $F_X(a) = \sum_{k:k \leq a}p_X(k)$ if $F_X$ is a step function
- $$P(X<a) = \underset{t \rightarrow a^-}{lim} F(t) = F(a-)$$ $$P(X=a) = F(a) - \underset{t \rightarrow a^-}{lim} F(t) = F(a)-F(a-)$$
- [[expectation]]: $E(X) = \sum_k k p_X(k)$
- $E(aX+b) = aE[X]+b$
- $E[g(X)]=\sum_{k}g(k)p_X(k)$
- [[variance]]: $Var(X) = E[(X-E[X])^2] = E[X^2]-(E[X])^2$
- $Var(aX+b) = a^2Var(X)$

###### Additional Thoughts:
