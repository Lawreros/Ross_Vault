name : nilpotent matrix
tags : 
backlinks : 
source : 

###### Content:
A nilpotent matrix is a [[square matrix]] $N \in M_n$ such that $$N^k = 0$$ for some positive integer $k$.

A common example of this is a [[Jordan block]] when you subtract the diagonal eigenvalues. Let $J_4(\lambda) \in M_4(\textbf{C})$, then:
$$J_4(\lambda) - \lambda I = \begin{bmatrix}
0 & 1 & 0 & 0\\
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1\\
0 & 0 & 0 & 0\\
\end{bmatrix}$$

Thus $$(J_4(\lambda) - \lambda I)^2 = \begin{bmatrix}
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0\\
\end{bmatrix}$$

$$(J_4(\lambda) - \lambda I)^3 = \begin{bmatrix}
0 & 0 & 0 & 1\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0\\
\end{bmatrix}$$

$$(J_4(\lambda)- \lambda I)^4 = [0]$$

###### Properties:
- The [[characteristic polynomial]] for $N$ is the [[determinant]] $det(xI - N) = x^n$
- The [[minimal polynomial]] for $N$ is $x^k$ for some positive integer $k \leq n$
- The [[determinant]] and [[trace]] of a nilpotent matrix is always zero, thus a nilpotent matrix cannot be [[invertible]]
- $\forall A \in M_n$ there exists a [[diagonalizable]] matrix $B \in M_n$ and a nilpotent matrix $C \in M_n$ such that $A = B+C$

###### Additional Thoughts:
