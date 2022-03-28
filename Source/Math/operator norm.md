name : operator norm
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $V, ||\cdot||_V$ and $W, ||\cdot||_W$ be [[normed linear space]]s over [[field]] $\mathcal{K}$, and let $T: V \rightarrow W$ be a [[linear transformation]]. If $T$ is continuous, the operator norm of $T$ is defined:
$$||T||_{V,W}:=\underset{x \in V}{sup}\frac{||Tx||_W}{||x||_V}$$
Where $x$ is a nonzero vector.

**Alternate Definition:**
Let $A \in M_{m,n}$, and consider the [[linear transformation]] $\mathbb{C}^n \rightarrow \mathbb{C}^m$. The operator norm of $A$ can be defined as: $$||A||_{p,q}:= \underset{x \neq 0}{max}\frac{||Ax||_q}{||x||_p} = \underset{||x||_p=1}{max}||Ax||_q$$
###### Properties:
- Let $\mathcal{K}^n,||\cdot||$ be a [[normed linear space]]. For all $A \in M_n(\mathcal{K})$: $$||A||_{||\cdot||,||\cdot||} = ||A^*||_{||\cdot||^D,||\cdot||^D}$$

###### Additional Thoughts:
