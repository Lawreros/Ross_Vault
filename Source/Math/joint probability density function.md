name : joint probability density function
tags : 
backlinks : 
source : Intro to Prob

###### Content:
The continuous counterpart to the [[joint probability mass function]]. By definition:
Random variables $X_1,...,X_n$ are **jointly continuous** if there exist a joint density function $f$ on $\mathbb{R}^n$ such that for [[subset]]s $B \subseteq \mathbb{R}^n$: $$P((X_1,...,X_n)\in B) = \underset{B}{\int...\int}f(x_1,...,x_n)dx_1...dx_n$$ 
**[[expectation]]:**
Let $g:\mathbb{R}^n \rightarrow \mathbb{R}$ be a real-valued function of an $n$-vector. If $X_1,...,X_n$ are [[random variable]]s with joint density function $f$ then: $$E[g(X_1,...,X_n)] = \int_{-\infty}^{\infty}...\int_{-\infty}^{\infty}g(x_1,...,x_n)f(x_1,...,x_n)dx_1...dx_n$$
provided the integral is well defined

###### Properties:
- A joint probability density function must be non-negative and its total integral must be 1: $$f(x_1,...,x_n) \geq 0 \text{ and } \int_{-\infty}^{\infty}...\int_{-\infty}^{\infty}f(x_1,...,x_n)dx_1...dx_n = 1$$
- We may write $f_{X_1,...,X_n}(x_1,...,x_n)$ when we wish to emphasize the random variables being considered.

###### Additional Thoughts:
