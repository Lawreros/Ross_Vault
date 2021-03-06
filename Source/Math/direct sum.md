name : direct sum
tags : 
backlinks : 
source : #LADR, #MASED 

###### Content:
**Definition:**
Suppose $U_1,...,U_m$ are [[subspace]]s of $V$:
- Suppose $U_1+...+U_m$ is called a direct sum if each element of $U_1+...+U_m$ can be written in only one way as a sum $u_1 + ... +u_m$, where each $u_j$ is in $U_j$.
- If $U_1+...+U_m$ is a direct sum, then $U_1\bigoplus ...\bigoplus U_m$ denotes $U_1+...+U_m$, with the $\bigoplus$ notation serving as an indication that this is a direct sum.

**Condition for a direct sum:**
Suppose $U_1,...,U_m$ are [[subspace]]s of $V$. Then $U_1+...+U_m$ is a direct sum if and only if the only way to write 0 as a sum $u_1+...+u_m$, where each $u_j$ is in $U_j$, is by taking each $u_j$ equal to 0.

**Direct sum of two subspaces:**
Suppose $U$ and $W$ are subspaces of $V$. Then $U+W$ is a direct sum if and only if $U \bigcap W = \{0\}$

###### Properties:
- [[sum of subspaces]] are analogous to unions of subsets. Similarly, direct sums of subspaces are analogous to disjoint unions of subsets.
- No two subspaces of a [[vector space]] can be disjoint, because both contain 0
- Let $B_1 \in M_n,..., B_d \in M_{n_d}$ be given and let $B$ be the direct sum $$B = \begin{bmatrix}
B_1 & 0 & ... & 0\\
0 & B_2 & ... & 0\\
0 & 0 & ... & 0\\
0 & 0 & ... & B_d\\
\end{bmatrix} = B_1 \bigoplus ... \bigoplus B_d$$ Then $B$ is [[diagonalizable]] if and only if each of $B_1,...,B_d$ is [[diagonalizable]]


###### Additional Thoughts:
