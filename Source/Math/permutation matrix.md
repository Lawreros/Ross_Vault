name : permutation matrix
tags : 
backlinks : 
source : #MASED 

###### Content:
A [[square matrix]] $P$ is a permutation matrix if exactly one entry in each row and column is equal to 1 and all other entries are $0$. Multiplication by such matrices effects a [[permutation]] of the rows or columns of the matrix multiplied:
$$\begin{bmatrix}
0 & 1 & 0\\
1 & 0 & 0\\
0 & 0 & 1\\
\end{bmatrix}\begin{bmatrix}
1 \\ 2 \\ 3 \end{bmatrix}
=
\begin{bmatrix}
2 \\ 1 \\ 3\\
\end{bmatrix}$$

###### Properties:
- Left multiplication of a matrix $A\in M_{m,n}$ by an $m$-by-$m$ permutation matrix $P$ permutes the rows of $A$, while right multiplication of $A$ by an $n$-by-$n$ permutation matrix $P$ permutes the columns of $A$.
- Since right multiplication by $P^T=P^{-1}$ permutes columns in the same way that left multiplication by $P$ permutates rows, the transformation $A \rightarrow PAP^T$ permutes the rows and columns of $A \in M_n$ in the same way.
- The [[determinant]] of a permutation matrix is  $\pm 1$, so permutation matrices are [[nonsingular]]
- The product of two permutation matrices is a permutation matrix.
- $P^T=P^{-1}$ for every permutation matrix $P$
- The set of $n$-by-$n$ permutation matrices is a subgroup of [[general linear group]] $GL(n,C)$ with cardinality $n!$

###### Additional Thoughts:
