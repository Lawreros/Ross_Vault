name : upper-triangular matrix
tags : #important
backlinks : 
source : #LADR

###### Content:
A [[matrix]] is called upper-triangular if all the entries below the [[diagonal]] equal 0.

###### Properties:
- An upper-triangular multiplied by and upper-triangular is upper-triangular
- Conditions for upper-triangular matrix. Suppose $T\in \mathcal{L}(V)$ and $v_1,...,v_n$ is a [[basis]] of $V$. Then the following are equivalent:
		- The matrix of $T$ with respect to $v_1,...,v_n$ is upper-triangular
		- $Tv_j \in span(v_1,...,v_j)$ for each $j = 1,...,n$
		- $span(v_1,...,v_j)$ is [[invariant]] under $T$ for each $j=1,...,n$

- Determination of whether an upper-triangular matrix is [[invertible]]. Suppose $T \in \mathcal{L}(V)$ has an upper-triangular matrix with respect to some basis of $V$. Then $T$ is invertible if and only if all the entries on the diagonal of the upper-triangular matrix are nonzero.
- Determination of [[eigenvalue]]s from upper-triangular matrix. Suppose $T \in \mathcal{L}(V)$ has an upper-triangular matrix with respect to some [[basis]] of $V$. Then the eigenvalues of $T$ are precisely the entries on the [[diagonal]] of the upper-triangular matrix.
- Upper-triangular matrix with respect to [[orthonormal basis]]. Suppose $T \in \mathcal{L}(V)$. If $T$ has an upper-triangular matrix with respect to some basis of $V$, then $T$ has an upper-triangular matrix with respect to some orthonormal basis of $V$.
- An upper-triangular matrix is [[normal]] if and only if it is [[diagonal]]

###### Additional Thoughts:
