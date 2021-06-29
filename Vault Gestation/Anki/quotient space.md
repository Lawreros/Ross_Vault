name : quotient space, $V/U$
tags : 
backlinks : 
source : [[Linear Algebra Done Right]]

###### Content:
Suppose $v \in V$ and $U$ is a subspace of $V$. Then $v+U$ is a subset of $V$ defined by $v+U = \{v+u: u\in U\}$. Then the quotient space $V/U$ is the set of all [[affine subset]]s of $V$ parallel to $U$. In other words, $$V/U = \{v+U:v \in V\}$$

**Addition and scalar multiplication** are defined on $V/U$ by $$(v+U)+(w+U) = (v+w)+U$$$$\lambda(v+U) = (\lambda v) + U$$ for $v,w \in V$ and $\lambda \in \textbf{F}$

###### Properties:
- Quotient space is a [[vector space]]. Suppose $U$ is a subspace of $V$. Then $V/U$, with the operations of addition and scalar multiplication as defined above, is a vector space.
- Suppose $V$ is [[finite-dimensional vector space]] and $U$ is a [[subspace]] of $V$. Then the [[dimension]] of the quotient space is: $$dim (V/U) = dim V - dim U$$

###### Additional Thoughts:
