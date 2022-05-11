name : Bayes' formula
tags : 
backlinks : [[conditional probability]], [[complement]]
source : Intro to Probability

###### Content:
**Bayes' formula for 2 events:**
For events $A,B$, if $P(A), P(B), P(B^C) >0$ then:
$$P(B|A) = \frac{P(AB)}{P(A)} = \frac{P(A|B)P(B)}{P(A|B)P(B)+P(A|B^C)P(B^C)}$$

**General version of Bayes' formula:**
Let $B_1,...,B_n$ be a [[partition]] of the [[sample space]] $\Omega$ such that each $P(B_i) >0$. Then for any event $A$ with $P(A)>0$, and any $k = 1,...,n$: $$P(B_k|A) = \frac{P(AB_k)}{P(A)} = \frac{P(A|B_k)P(B_k)}{\sum_{i=1}^n P(A|B_i)P(B_i)}$$

###### Properties:


###### Additional Thoughts:
