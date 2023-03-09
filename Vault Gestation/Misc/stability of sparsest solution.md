name : stability of [[sparse]]st solution
tags : 
backlinks : 
source : #sparse

###### Content:
Let $x:||x||_0=k \leq \frac{1}{2}(1+\frac{1}{\mu(A)})$, and measurements given by $b=Ax+v$, where $||v||_2 \leq \epsilon$. If the matrix $A$ satisfies the [[Restricted Isometry Property (RIP)]] with constant $\delta_{2k}$, then any solution $\hat x$ to 
$(P_0^\epsilon): \underset{x}{min} ||x||_0$ s.t. $||Ax-b||^2_2 \leq \epsilon^2$
satisfies:
$$||x-\hat x||_2^2 \leq \frac{4\epsilon^2}{1-\delta_{2k}} \leq \frac{4\epsilon^2}{1-(2k-1)\mu(A)}$$

###### Properties:


###### Additional Thoughts:
