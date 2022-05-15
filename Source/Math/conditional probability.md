name : conditional probability
tags : 
backlinks : 
source : Intro to Probability

###### Content:
Conditional probability is a measure of the probability of an event occurring, given that another event has already occurred. 

Let $B$ be an event in the [[sample space]] $\Omega$ such that $P(B)>0$. Then for all events $A$ the conditional probability of $A$ given $B$ is defined as $$P(A|B) = \frac{P(AB)}{P(B)}$$

###### Properties:
- Suppose that we have an experiment with finitely many equally likely outcomes and $B$ is not the empty set. Then, for any event $A$: $$P(A|B) = \frac{\# AB}{\# B}$$ where $\#$ denotes the number of a given set of events occurring.
- **multiplication rule:** $P(AB) = P(A)P(B|A)$
- **multiplication rule for n events:** $$P(A_1A_2 ...A_n) = P(A_1)P(A_2|A_1)P(A_3|A_1A_2) ... P(A_n|A_1 ...A_{n-1})$$
- **Law of total probability:** Suppose that $B_1,...,B_n$ is a [[partition]] of $\Omega$ with $P(B_i)>0$ for $i = 1,...,n$. Then for any event $A$ we have: $$P(A) = \sum_{i=1}^n P(AB_i) = \sum_{i=1}^n P(A|B_i)P(B_i)$$
- [[conditional independence]]
$$P(A_{i_1}A_{i_2}...A_{i_k}|B) = P(A_{i_1}|B)...P(A_{i_k}|B)$$
- [[Bayes' formula]]

###### Additional Thoughts:
