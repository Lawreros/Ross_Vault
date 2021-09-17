name : Gram-Schmidt Procedure
tags : 
backlinks : [[span]], [[norm]]
source : #LADR 

###### Content:
A method for turning a linearly independent list into an orthonormal list with the same span as the original list.

Suppose $v_1,...,v_m$ is a [[linearly independent]] list of vectors in [[inner product space]] $V$. Let $e_1 = v_1/||v_1||$. For $j = 1,...,m$, define $e_j$ inductively by $$e_j = \frac{v_j - \langle v_j, e_1 \rangle e_1 - ... - \langle v_j, e_{j-1} \rangle e_{j-1}}{||v_j - \langle v_j, e_1 \rangle e_1 - ... - \langle v_j, e_{j-1} \rangle e_{j-1}||}$$
Then $e_1,...,e_m$ is an [[orthonormal]] list of vectors in $V$ such that $$span(v_1,...,v_j) = span(e_1,...,e_j)$$ for $j = 1,...,m$

###### Properties:


###### Additional Thoughts:
