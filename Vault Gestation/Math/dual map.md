name : dual map, $T'$
tags : 
backlinks : 
source : [[Linear Algebra Done Right]]

###### Content:
If $T \in \mathcal{L}(V,W)$, then the dual map of $T$ is the [[linear map]] $T' \in \mathcal{L}(W',V')$ defined by $T'(\varphi) = \varphi \circ T$ for $\varphi \in W'$.

**Algebraic properties of dual maps**
- $(S+T)' = S' + T'$ for all $S,T \in \mathcal{L}(V,W)$
- $(\lambda T)' = \lambda T'$ for all $\lambda \in \textbf{F}$ and all $T \in \mathcal{L}(V,W)$
- $(ST)' = T'S'$ for all $T \in \mathcal{L}(U,V)$ and all $S \in \mathcal{L}(V,W)$

###### Properties:
- The [[null space]] of $T'$. Suppose $V$ and $W$ are [[finite-dimensional vector space]]s and $T \in \mathcal{L}(V,W)$. Then:
		- $null T' = (range T)^0$
		- dim null $T' =$ dim null $T +$ dim $W -$ dim $V$
- $T$ [[surjective]] is equivalent to $T'$ [[injective]]. Suppose $V$ and $W$ are [[finite-dimensional vector space]]s and $T \in \mathcal{L}(V,W)$. Then $T$ is surjective if and only if $T'$ is injective.
- $T$ injective is equivalent to $T'$ surjective. Suppose $V$ and $W$ are finite-dimensional and $T \in \mathcal{L}(V,W)$ then $T$ is injective if and only if $T'$ is surjective.
- The [[range]] of $T'$. Suppose $V$ and $W$ are finite-[[dimension]]al and $T \in \mathcal{L}(V,W)$. Then:
		- dim range $T'=$ dim range $T$
		- $range T' = (nullT)^0$
- The [[matrix]] of $T'$ is the [[transpose]] of the matrix of $T$. Suppose $T \in \mathcal{L}(V,W)$. Then $\mathcal{M}(T') = (\mathcal{M}(T))^t$

###### Additional Thoughts:
