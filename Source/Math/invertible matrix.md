name : invertible matrix
tags : 
backlinks : 
source : #MASED 

###### Content:
A [[linear transformation]] or [[matrix]] is said to be invertible if it has an inverse, is [[nonsingular]] and [[nondegenerate]]

An $A\in M_n(\textbf{F})$ is invertible if there is a matrix $A^{-1} \in M_n(\textbf{F})$ such that $A^{-1}A = I$. 
"A good way to find this is to get it to [[Reduced Row Echelon Form]] and see if it matches the following properties" ( *-Tommy Athey*)

###### Properties:
- If $A \in M_n$ and $A^{-1}A=I$, then $AA^{-1}$; that is, $A^{-1}$ is a left inverse if and only if it is a right inverse; $A^{-1}$ is unique whenever it exists.
- The following are equivalent for a given $A\in M_n(\textbf{F})$
		- $A$ is nonsingular
		- $A^{-1}$ exists
		- [[rank]] $A=n$
		- The rows of $A$ are [[linearly independent]]
		- ([[determinant]]) $det A \neq 0$
		- The [[dimension]] of the [[range]] of $A$ is $n$
		- The dimension of the [[null space]] of $A$ is 0
		- $Ax = b$ is consistent for each $b \in \textbf{F}^n$
		- If $Ax=b$ is consistent, then the solution is unique
		- $Ax=b$ has a unique solution for each $b \in \textbf{F}^n$
		- The only solution to $Ax=0$ is $x=0$
		- 0 is not an [[eigenvalue]] of $A$
- The product of two invertible matrices is invertible. $det(AB)=det(A)*det(B) \neq 0$

###### Additional Thoughts:
