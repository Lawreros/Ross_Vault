name : spark
tags : 
backlinks : 
source : #sparse 

###### Content:
The spark of a matrix $A \in M_n$, denoted by $spark(A)$ is the minimal number of linearly dependent columns in $A$.

**NOTE:** This is minimum number of linearly *dependent* columns. So if there are if there are $m$ [[linearly independent]] columns, then $spark(A) = m+1$.

###### Properties:
- Uniqueness via the spark. If a system $Ax=b$ has a solution $x^*:||x^*||_0 < \frac{1}{2}spark(A)$, then $x^8$ is the sparsest solution possible.
- Upper bound on the spark: For any $A \in M_{n\times m}(\textbf{R})$, $spark(A) \geq 1 + \frac{1}{\mu (A)}$ ([[mutual coherence]])

###### Additional Thoughts:
