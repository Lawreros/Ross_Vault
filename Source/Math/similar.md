name : similar
tags : 
backlinks : 
source : #MASED 

###### Content:
Let $A, B \in M_n$ be given. We say that $B$ is similar to $A$ if there exists a [[nonsingular]] $S \in M_n$ such that $$B = S^{-1}AS$$ The transformation $A \rightarrow S^{-1}AS$ is called a similarity transformation by the [[similarity matrix]] $S$.

###### Properties:
- $B$ is [[permutation similar]] to $A$ if there is a [[permutation matrix]] $P$ such that $B = P^TAP$
- Similarity is an equivalence relation on $M_n$: that is, similarity is [[reflexive]], [[symmetric]], and [[transitive]]
- Let $A,B \in M_n$. If $B$ is similar to $A$, then $A$ and $B$ have the same [[characteristic polynomial]]
- Let $A, B \in M_n$ and suppose that $A$ is similar to $B$. Then
		- $A$ and $B$ have the same [[eigenvalue]]s (and by extension the same [[determinant]])
		- If $B$ is a [[diagonal matrix]], its main diagonal entries are the eigenvalues of $A$
		- $A$ and $B$ have the same [[trace]], as they have the same eigenvalues
		- $B=0$ (a diagonal matrix) if and only if $A=0$
		- $B=I$ (a diagonal matrix) if and only if $A=I$
- Let $A \in M_n$ be given. Then $A$ is similar to a [[block matrix]] of the form 
$$\begin{bmatrix}
\Lambda & C \\
0 & D
\end{bmatrix}$$
Where  $\Lambda = diag(\lambda_1,...,\lambda_k)$, $D \in M_{n-k}$, and $1 \leq k < n$ if an only if there are $k$ [[linearly independent]] vectors in $\textbf{C}^n$, each of which is an [[eigenvector]] of $A$. The matrix $A$ is [[diagonalizable]] if an only if there are $n$ linearly independent vectors, each of which is an eigenvector of $A$. If $x^{(1)},...,x^{(k)}$ are linearly independent eigenvectors of $A$ and if $S = [x^{(1)},...,x^{(k)}]$, then $S^{-1}AS$ is a [[diagonal matrix]]. If A is similar to a matrix of the form above, then the diagonal entries of $\Lambda$ are [[eigenvalue]]s of $A$; if $A$ is similar to a diagonal matrix $\Lambda$, then the diagonal entries of $\Lambda$ are all of the eigenvalues of $A$.

###### Additional Thoughts:
