name : adjoint, $T^*$
tags : 
backlinks : 
source : #LADR 

###### Content:
Suppose the [[linear map]] $T \in \mathcal{L}(V,W)$. The adjoint of $T$ is the function $T^*:W \rightarrow V$ such that $$\langle Tv, w \rangle = \langle v, T^*w\rangle$$
for every $v \in V$ and every $w \in W$.

**Properties of the adjoint**
(a) $(S+T)^* = S^*+T^*$ for all $S,T \in \mathcal{L}(V,W)$
(b) $(\lambda T)^*= \bar \lambda T^*$ for all $\lambda \in \textbf{F}$ and $T \in \mathcal{L}(V,W)$
(c) $(T^*)* = T$ for all $T \in \mathcal{L}(V,W)$
(d) $I^* = I$, where $I$ is the identity [[operator]] on $V$
(e) $(ST)^* = T^*S^*$ for all $T \in \mathcal{L}(V,W)$ and $S \in \mathcal{L}(W,U)$ (here $U$ is an [[inner product space]] over $\textbf{F}$)

###### Properties:
- The adjoint is the linear map. If $T \in \mathcal{L}(V,W)$, then $T^* \in \mathcal{L}(W,V)$.
- [[null space]] and [[range]] of $T^*$. Suppose $T \in \mathcal{L}(V,W)$. Then
		(a) $\text{null } T^* = (\text{range }T)^\perp$
		(b) $\text{range } T^* = (\text{null } T)^\perp$
		(c) $\text{null } T = (\text{range } T^*)^\perp$
		(d) $\text{range }T = (\text{null }T^*)^\perp$

###### Additional Thoughts:
