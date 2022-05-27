name : independent (mutually independent)
tags : 
backlinks : [[complement]]
source : Intro to Probability

###### Content:
Events $A$ and $B$ are independent if: $$P(AB) = P(A)P(B)$$

Suppose that events $A_1,...,A_n$ are mutually independent. Then for every collection $A_{i_1}...A_{i_k}$, where $2 \leq k \leq n$ and $1 \leq i_1 < i_2<...<i_k\leq n$, we have: 
$$P(A^*_{i_1}A^*_{i_2}...A^*_{i_k}) = P(A^*_{i_1})P(A^*_{i_2})...P(A^*_{i_k})$$ where each $A_i^*$ represents either $A_i$ or $A_i^C$

**Independence of [[random variable]]s:**
Let $X_1, X_2,...,X_n$ be random variables defined on the same [[probability space]]. Then $X_1, X_2,...,X_n$ are independent if: $$P(X_1 \in B_1, X_2 \in B_2, ..., X_n \in B_n) = \prod_{k=1}^n P(X_k \in B_k)$$ for all choices of subsets $B_1,B_2,...,B_n$ of the real line.


###### Properties:
- Suppose that $A$ and $B$ are independent. Then the same is true for each of these pairs: $A^C$ and $B$, $A$ and $B^C$, and $A^C$ and $B^C$
- Independence makes sense only when $A$ and $B$ are events on the same [[sample space]]

###### Additional Thoughts:
