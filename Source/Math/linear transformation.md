name : linear transformation
tags : 
backlinks : [[linear map]]
source : #MASED 

###### Content:
A linear transformation is a function $T:U \rightarrow V$ such that $T(a_1x_1+a_2x_2)=a_1T(x_1)+a_2T(x_2)$ for any scalers $a_1,a_2$ and vectors $x_1,x_2$.

Let $U$ be an $n$-dimensional [[vector space]] and let $V$ be an $m$-dimensional vector space, both over the same field $\textbf{F}$; let $\mathcal{B}_U$ be a [[basis]] of $U$ and $\mathcal{B}_V$ a basis of $V$. We may use the [[isomorphic]] matrix to do $x \rightarrow [x]_{\mathcal{B}_U}$ and $y \rightarrow [y]_{\mathcal{B}_V}$ to represent vectors in $U$ and $V$ as $n$-vectors and $m$-vectors over $\textbf{F}$, respectively.

A matrix $A \in M_{m,n}(\textbf{F})$ corresponds to the linear transform $T$ in the following way:
$$y = T(x)$$ if and only if $$[y]_{\mathcal{B}_V} = A[x]_{\mathcal{B}_U}$$
The matrix $A$ is said to *represent the linear transformation $T$*, which depends on the bases chosen.

###### Properties:

###### Additional Thoughts:
