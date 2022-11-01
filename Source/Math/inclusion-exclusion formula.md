name : inclusion-exclusion formula
tags : 
backlinks : [[complement]]
source : Intro to Prob

###### Content:
For events $A$, $B$, $C$:
**Formula for two events:**
$$P(A \cup B) = P(A)+P(B)-P(A \cap B)$$

**Formula for three events:**
$$P(A \cup B\cup C) = P(A)+P(B)+P(C)-P(A\cap B) - P(A\cap C) - P(B \cap C) + P(A \cap B \cap C)$$

**Formula for n events:**
$$P(A_1\cup ... \cup A_n) = \sum_{i=1}^n P(A_i) - \sum_{1 \leq i_1 < i_2 \leq n}P(A_{i_1} \cap A_{i_2}) + \sum_{1 \leq i_1 < i_2 < i_3 \leq n}P(A_{i_1} \cap A_{i_2} \cap A_{i_3}) - \sum_{1 \leq i_1 < i_2 < i_3 <i_4 \leq n}P(A_{i_1} \cap A_{i_2} \cap A_{i_3}\cap A_{i_4}) + ...+(-1)^{n+1}P(A_1 \cap ... \cap A_n)$$
$$= \sum_{k=1}^n(-1)^{k+1}\sum_{1 \leq i_1<...<i_k\leq n}P(A_{i_1}\cap ... \cap A_{i_k})$$
where $k$ denotes the number of events put in each intersection.

###### Properties:


###### Additional Thoughts:
