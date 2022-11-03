name : joint probability mass function
tags : 
backlinks : 
source : Intro to Prob

###### Content:
The [[probability distribution]] of a [[random vector]] in the case of a discrete [[joint probability distribution]]:

Let $X_1,X_2,...,X_n$ be [[discrete random variable]]s, all defined on the same [[sample space]]. Their joint probability mass function is defined by:
$$p(k_1,k_2,...,k_n) = P(X_1 = k_1, X_2=k_2,...,X_n=k_n)$$
for all possible values $k_1,k_2,...,k_n$ of $X_1,X_2,...,X_n$.

---
Let $p(k_1,...,k_n)$ be the joint probability mass function of $(X_1,...,X_n)$. Let $1\leq j \leq n$. Then the [[probability mass function]] of $X_j$ is given by $$p_{X_j}(k) = \sum_{l_1,...,l_{j-1}, l_{j+1},...,l_n} p(l_1,...,l_{j-1},k,l_{j+1},...,l_n)$$
where the sum is over the possible values of the other [[random variable]]s. The function $p_{X_j}$ is called the *marginal probability mass function of $X_j$*.

---
Let $1 \leq m < n$. The joint probability mass function of $(X_1,...,X_m)$ is obtained from $$p_{X_1,...,X_m}(k_1,...,k_m) = \sum_{l_{m+1},...,l_n}p(k_1,...,k_m,l_{m+1},...,l_n)$$
where the sum ranges over all possible values $l_{m+1},...,l_n$ of the random variables $X_{m+1},...,X_n$

---
**[[expectation]]:**
Let $g:\mathbb{R}^n \rightarrow \mathbb{R}$ be a real-valued function of an $n$-vector. If $X_1,...,X_n$ are [[discrete random variable]]s with joint probability mass function $p$ then $$E[g(X_1,...,X_n)]=\sum_{k_1,...,k_n}g(k_1,...,k_n)p(k_1,...,k_n)$$
provided the sum is well defined.

###### Properties:


###### Additional Thoughts:
