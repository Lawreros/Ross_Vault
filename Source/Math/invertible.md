name : invertible
tags : 
backlinks : [[invertible matrix]]
source : #LADR

###### Content:
A linear map $T \in \mathcal{L}(V,W)$ is called invertible if there exists a [[linear map]] $S \in \mathcal{L}(W,V)$ such that $ST$ equals the [[identity map]] on $V$ and $TS$ equals the [[identity map]] on $W$.

A linear map $S \in \mathcal{L}(W,V)$ satisfying $ST = I$ and $TS = I$ is called an **inverse** of $T$ (note that the first $I$ is the identity map on $V$ and the second $I$ is the identity map on $W$).

If $T$ is invertible, the its inverse is denoted by $T^{-1}$.

###### Properties:
- An invertible linear map has a unique inverse
- A linear map is invertible if and only if it is [[injective]] and [[surjective]]
- Suppose $A \in M_n$ is invertible, let $b,x, \Delta b, \Delta x \in \mathbb{C}^n$ be vectors where $b,x \neq 0$, and let the [[matrix norm]] $||\cdot||$ on $M_n$ be [[compatible]] with the [[vector norm]] $||\cdot||$ on $\mathbb{C}^n$. Suppose that $Ax = b$ and $A(x+\Delta x) = b+\Delta b$, then: $$\frac{1}{\mathcal{K}(A)} \frac{||\Delta b||}{||b||} \leq \frac{||\Delta x||}{||x||} \leq \mathcal{K}(A)\frac{||\Delta b||}{||b||}$$(see [[condition number]], and $\Delta$ is just a symbol to distinguish the different matrices)
- Suppose $||\cdot||$ is a matrix norm on $M_n$ and $A, \Delta A \in M_n$ with $A$ being invertible and $||A^{-1}||||\Delta A|| < 1$, then $A+\Delta A$ is invertible. Thus: $$\frac{||A^{-1}-(A+\Delta A)^{-1}||}{||A^{-1}||} \leq \frac{\mathcal{K}(A) \frac{||\Delta A||}{||A||}}{1- \mathcal{K}(A) \frac{||\Delta A||}{||A||}}$$  ($\Delta$ is just a symbol to distinguish the different matrices)

###### Additional Thoughts:
