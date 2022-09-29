name : Restricted Isometry Property (RIP)
tags : 
backlinks : 
source : #sparse 

###### Content:
A matrix $A \in M_{n\times m}(\textbf{R})$, with [[norm]]alized columns, satisfies the RIP of order $s\leq n$ with constant $\delta_s$ if this is the minimal value such that: $$(1-\delta_s)||x||_2^2 \leq ||Ax||^2_2 \leq ||x||_2^2(1+\delta_s)$$
for every $x \in R^m:||x|| \leq s$

Just like the [[spark]] of $A$, the RIP constant $\delta$ is not easily computable, as it would require to sweep through all possible combinations of the $s$ columns of $A$. However, it can also be bounded by employing the [[mutual coherence]]. Recall the subgram of $A,G_s=A_S^TA_S$, where $S$ indexes $s$ columns. From the [[Gershgorin Disk Theorem]], we know that: $$|\lambda(G_X)-1| \leq (s-1)\mu(A)$$ since $G_S$ has ones in its diagonal ($A$ is normalized), and each off-diagonal entry can be bounded by the [[mutual coherence]] $\mu(A)$ in absolute value. Therefore:
$$1-(s-1)\mu(A) \leq \lambda(G_X) \leq 1+(s-1)\mu(A)$$Recalling that, for every $s$-[[sparse]] vector $x$, $||Ax||^2_2 \leq \lambda_{max}(A_S^TA_S)||x||^2_2$ for every possible subset $S$, we see that $$\delta_S \leq (s-1)\mu(A)$$

###### Properties:

###### Additional Thoughts:
