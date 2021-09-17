name : orthogonal projection, $P_U$
tags : 
backlinks : 
source : #LADR 

###### Content:
Suppose $U$ is a finite-dimensional subspace of [[inner product space]] $V$. The orthogonal projection of $V$ onto $U$ is the [[operator]] $P_U \in \mathcal{L}(V)$ defined as follows:

For $v \in V$, write $v=u+w$, where $u\in U$ and $w \in U^\perp$. Then $P_Uv=u$

###### Properties:
Suppose $U$ is a finite-dimensional subspace of $V$ and $v \in V$. Then:
(a) $P_U \in \mathcal{L}(V)$
(b) $P_Uu = u$ for every $u \in U$
(c) $P_Uw = 0$ for every $w \in U^\perp$
(d) [[range]] $P_U = U$
(e) null $P_U = U^\perp$      ([[null space]])
(f) $v-P_Uv \in U^\perp$
(g) $P_U^2 = P_U$
(h) $||P_Uv|| \leq ||v||$
(i) for every [[orthonormal basis]] $e_1,...,e_m$ of $U$,$$P_Uv = \langle v, e_1 \rangle e_1 +...+\langle v,e_m \rangle e_m$$

###### Additional Thoughts:
