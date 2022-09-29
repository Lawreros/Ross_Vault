name : mutual coherence
tags : 
backlinks : 
source : #sparse

###### Content:
Given a matrix $A \in M_{n\times m}(\textbf{R})$, with columns given by $a_i$, its mutual coherence is given by $$\mu (A) = \underset{i \neq j}{max} \frac{| \langle a_i, a_j \rangle|}{||a_i||_2||a_j||_2}$$

This equation gives a metric which characterizes the highest possible correlation between two columns in $A$.

###### Properties:
- In general, when $m >n, \mu (A) >0$. If $\mu (A) = 0$, then each column of the vector is [[orthogonal]].
- For [[full rank]] matrices $$\mu (A) \geq \sqrt{\frac{m-n}{n(m-1)}}$$

###### Additional Thoughts:
