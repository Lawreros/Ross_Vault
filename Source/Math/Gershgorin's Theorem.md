name : Gershgorin's Theorem
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
For any matrix $A\in M_n$, with [[spectrum]] $\sigma(A) \subseteq G(A)$. Furthermore, if there is a connected component of $G(A)$ with, say $k$ [[Gershgorin disc]]s then they contain exactly $k$ [[eigenvalue]]s.

**Proof:** Let $\lambda \in \sigma(A)$ with associated [[eigenvector]] $x$, let $k \in \underset{i}{argmax}|x_i| = ||x||_\infty$.
$Ax = \lambda x \Rightarrow \lambda x_k = \sum_{j=1}^n a_{kj}x_j \Rightarrow (\lambda - a_{kk})x_k = \sum_{j\neq k}^na_{kj}x_j$
Using [[triangle inequality]]: $|\lambda - a_{kk}||x_{kk}| = \sum_{j\neq k}^n |a_{kj}||x_j| \leq \sum_{j\neq k}^n |a_{kj}||x_k|$
if $|x_k|\neq 0 \Rightarrow |\lambda - a_{kk}| \leq \sum_{j\neq k}^n |a_{kj}|$
i.e. $\lambda \in G(A)$

###### Properties:


###### Additional Thoughts:
