name : direct sum
tags : 
backlinks : 
source : [[Linear Algebra Done Right]]

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
- No two subspaces of a vector space can be disjoint, because both contain 0

###### Additional Thoughts:
