name : Jordan matrix
tags : 
backlinks : 
source : #MASED 

###### Content:
The Jordan matrix $$\begin{bmatrix} J_{n_1}(\lambda_1) & & \\
& ... & \\
& & J_{n_k}(\lambda_k) \end{bmatrix}, n_1+n_2+...+n_k=n$$ has a definite structure that makes apparent certain basic properties of any matrix that is [[similar]] to it:
1. The number $k$ of [[Jordan block]]s (counting multiple occurrences of the same block) is the maximum number of [[linearly independent]] [[eigenvector]]s of $J$
2. The matrix $J$ is [[diagonalizable]] if and only if $k=n$, that is, if and only if all the Jordan blocks are 1-by-1
3. The number of Jordan blocks corresponding to a given [[eigenvalue]] is the [[geometric multiplicity]] of the eigenvalue, which is the dimension of the associated [[eigenspace]]. The sum of the sizes of all the Jordan blocks corresponding to a given eigenvalue is its [[algebraic multiplicity]]

###### Properties:
- [[geometric multiplicity]]$\leq$[[algebraic multiplicity]] inequality: The geometric multiplicity of an eigenvalue $\lambda$ of a given $A\in M_n$ is the number of [[Jordan block]]s of $A$ corresponding to $\lambda$. This number is less than or equal to the sum of the sizes of all the Jordan blocks corresponding to $\lambda$; this sum is the [[algebraic multiplicity]] of $\lambda$. Thus, the geometric multiplicity of an eigenvalue $\leq$ its algebraic multiplicity
- If [[geometric multiplicity]] = [[algebraic multiplicity]], then the Jordan block corresponding to $\lambda$ is 1-by-1.
- The Jordan canonical form of a direct sum: Let $A_i \in M_{n_i}$ be given for $i =1,...,m$ and suppose that each $A_i = SJ_iS_i^{-1}$, in which each $J_i$ is a Jordan matrix. Then the [[direct sum]] $A = A_1 \bigoplus ... \bigoplus A_m$ is [[similar]] to the direct sum $J = J_1 \bigoplus ... \bigoplus J_m$ via $S = S_1 \bigoplus ... \bigoplus S_m$.

###### Additional Thoughts:
