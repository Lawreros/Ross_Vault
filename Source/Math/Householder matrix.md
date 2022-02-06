name : Householder matrix
tags : 
backlinks : 
source : #MASED , https://handwiki.org/wiki/Householder_transformation

###### Content:
Let $w \in \textbf{C}^n$ be a nonzero vector. The Householder matrix $H_w \in M_n$ is defined by $H_w = I -2(w^*w)^{-1}ww^*$. If $w$ is a unit vector (a vector with length of 1), then $H_w = I - 2ww^*$

Explained another way, the Householder matrix is a linear transformation that describes a reflection about a plane or [[hyperplane]] containing the origin. If you select a vector orthogonal to the plane of interest, you can use it to make a matrix that reflects whatever vector you give it over the plane.

###### Properties:
- The Householder matrix is [[Hermitian]]: $H_w = H_w^*$
- The Householder matrix is [[unitary]]: $H_w^{-1}=H_w^*$
- Has eigenvalues of 1 and -1. (Say $H_w = U_w$) Think of the fact that if $u$ is [[orthogonal]] to the vector $v$ which is used to create the reflector (i.e. is orthogonal to the plane/[[hyperplane]]), then $Pu = u = \lambda u$. Thus 1 is an [[eigenvalue]] of multiplicity $n-1$, since there are $n-1$ independent vectors orthogonal to $v$. Also notice that $Pv = -v$ and so $-1$ is an eigenvalue with multiplicity 1.
- The maximum [[dimension]] of the Householder matrix is $n-1$, assuming the vector $w$ has a dimension of 1 (you have to make a plane orthogonal to the vector, that vector takes up at least one dimension)
- The [[determinant]] of a Householder reflector is $-1$, since the determinant of a matrix is the product of its [[eigenvalue]]s, in this case one of which is $-1$ with the remainder being $1$

###### Additional Thoughts:
