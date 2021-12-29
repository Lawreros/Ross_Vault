name : Schur Decomposition
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $A \in M_n$ have [[eigenvalue]]s $\lambda_1, \lambda_2,...,\lambda_n$ (in any order). There exists some [[unitary matrix]] $U \in M_n$ and [[upper-triangular matrix]] $T \in M_n$ such that:
$$A = UTU^*$$
$$T = \begin{bmatrix}
\lambda_1 & * &* &\dots&*\\
0 & \lambda_2 & * & \dots & *\\
0 & 0 & \lambda_3 & \dots & *\\
\vdots & \vdots & \dots & \ddots &\vdots\\
0 & 0 & 0 &\dots & \lambda_n
\end{bmatrix}$$

###### Properties:
- If $A$ is a [[real matrix]], and all eigenvalues are real, then $U$ and $T$ must both be a [[real matrix]]
###### Additional Thoughts:
