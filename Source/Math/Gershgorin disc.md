name : Gershgorin disc
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $A \in M_n$. For all $i = 1,2,...,n$ the Gershgorin discs $$G_i := \{z \in \mathbb{C}:|z-a_{ii}| \leq \sum_{i \neq j}^n |a_{ij}|\}$$

With the collection of discs being: $G(A) := \bigcup_{i=1}^n G_i(A)$

###### Properties:
- G-discs of [[strictly diagonally dominant]] matrix $A$ can never contain the origin, because the center of the disk is greater than the radius. Thus $0 \notin \sigma(A)$, thus [[invertible]]
- For all $A \in M_n$: $$\sigma(A) \subseteq G(A^T) $$ For all [[invertible]] $S\in M_n$ $$ \sigma(A) \subseteq G(SAS^{-1})$$ $$\sigma(A) = \bigcap_{S\in M_n} G(S^{-1}AS) $$

###### Additional Thoughts:
