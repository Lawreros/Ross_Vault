name : unitary matrix
tags : 
backlinks : 
source : #MASED 

###### Content:
A matrix $U \in M_n$ is [[unitary]] if $UU^*=I$.

###### Properties:
- Unitary matrices are also [[real orthogonal]] due to $U^*=U^T$
- Every unitary matrix is [[normal]]
- If $U \in M_n$, the following are equivalent
		- $U$ is [[unitary]]
		- $U$ is [[nonsingular]] and $U^* =U^{-1}$
		- $UU^*=I$
		- $U^*$ is [[unitary]]
		- The columns of $U$ are [[orthonormal]]
		- The rows of $U$ are [[orthonormal]]
		- For all $x \in \textbf{C}^n$, $||x||_2 = ||Ux||_2$, that is, $x$ and $Ux$ have the same Euclidean norm
- Let a unitary $U \in M_n$ be partitioned as $U =\begin{bmatrix} U_{11} & U_{12} \\ U_{21} & U_{22}\\ \end{bmatrix}$, in which $U_{11} \in M_k$. Then [[rank]] $U_{12} =$ [[rank]] $U_{21}$ and rank $U_{22}=$ rank $U_{11}+n-2k$. In particular, $U_{12}=0$ if and only if $U_{21}=0$, in which case $U_{11}$ and $U_{22}$ are [[unitary]]

###### Additional Thoughts:
