name : SVD (Singular Value Decomposition)
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
For any matrix $A \in M_n$ there exists a [[unitary matrix]] $U \in M_m$, and a [[unitary matrix]] $V \in M_n$, and a [[diagonal matrix]] $\Sigma \in M_{m,n}$ consisting of [[singular values]] such that:
$$A = U\Sigma V^*$$

###### Properties:
- If $A$ is a real matrix, then $U,V$ may be found real

Let $U = [u_1,u_2,...,u_m]$, $V = [v_1,v_2,...,v_m]$, and $\Sigma = \begin{bmatrix} \sigma_1 & 0 &... & 0\\ 0 & \sigma_2 &... & 0\\ ... & ... &... & ...\\ 0 & 0 &... & \sigma_n\\\end{bmatrix}$ where $\sigma_1 > ... >\sigma_k > \sigma_k+1 = 0$
such that $A = U\Sigma V^*$, then:
1) $A = U \Sigma V^* = \sum_{i=1}^k\sigma_i u_i v_i^*$
2) [[rank]]$(A) = k$ since $rank(A) = rank(\Sigma)$
3) [[range]]$(A)$ = [[span]]{$u_1,u_2,...u_k$}
4) [[null space]]$(A) = Span\{v_{k+1},v_{k+2},...v_n\}$
5) $range(A^*) = Span\{v_1,v_2,...,v_k\}$
6) $null(A^*) = Span\{u_{k+1},...,u_m\}$
7) ([[Frobenius norm]]) $||A||_F^2 = ||U\Sigma V^*||^2_F = ||\Sigma||^2_F =  \sum_{i=1}^k \sigma_i^2$
8) $||A||_2^2 = \sigma_1^2$

- Say the SVD of $A = U\Sigma V^*$, the [[Moure-Penrose inverse]] of $A$ is $A^\dagger = V \Sigma^\dagger U^*$

###### Additional Thoughts:
