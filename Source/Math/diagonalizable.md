name : diagonalizable
tags : 
backlinks : 
source : #LADR , #MASED 

###### Content:
An [[operator]] $T \in \mathcal{L}$ is called diagonalizable if the operator has a [[diagonal matrix]] with respect to some [[basis]] of $V$.

If $T \in M_n$ is [[similar]] to a [[diagonal matrix]], then $A$ is said to be diagonalizable.

###### Properties:
- Conditions equivalent to diagonalizability. Suppose $V$ is finite-dimensional and $T \in \mathcal{L}(V)$. Let $\lambda_1,...,\lambda_m$ denote the distinct [[eigenvalue]]s of $T$. Then the following are equivalent:
		- $T$ is diagonalizable
		- $V$ has a [[basis]] consisting of [[eigenvector]]s of $T$ (i.e. $T \in M_n$ is diagonalizable if and only if $T$ has $n$ [[linearly independent]] eigenvectors).
		- There exist 1-dimensional [[subspace]]s $U_1,...,U_n$ of $V$, each [[invariant]] under $T$, such that $V = U_1 \bigoplus ... \bigoplus U_n$
		- ([[eigenspace]]) $V = E(\lambda_1,T) \bigoplus ... \bigoplus E(\lambda_m,T)$
		- $dim V = dim E(\lambda_1,T)+...+dim E(\lambda_m,T)$

- If $A \in M_n$ has all eigenvalues being distinct, then $A$ is diagonalizable.

###### Additional Thoughts:
