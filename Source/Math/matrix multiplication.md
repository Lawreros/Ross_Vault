name : matrix multiplication
tags : 
backlinks : 
source : #LADR

###### Content:
**Scalar multiplication of a matrix:**
The product of a scalar and a [[matrix]] is the matrix obtained by multiplying each entry in the matrix by the scalar:
$$\lambda \begin{bmatrix}
A_{1,1} & \dots & A_{1,n} \\
\vdots & & \vdots\\
A_{m,1} & \dots & A_{m,n}
\end{bmatrix}
=
\begin{bmatrix}
\lambda A_{1,1} & \dots & \lambda A_{1,n} \\
\vdots & & \vdots\\
\lambda A_{m,1} & \dots & \lambda A_{m,n}
\end{bmatrix}
$$

In other words, $(\lambda A)_{j,k} = \lambda A_{j,k}$

**Matrix multiplication:**
Suppose $A$ is an *m*-by-*n* matrix and $C$ is an *n*-by-*p* matrix. Then $AC$ is defined to be the *m*-by-*p* matrix whose entry in row *j*, column *k*, is given by the following equation:
$$(AC)_{j,k} = \sum^n_{r-1}A_{j,r}C_{r,k}$$

**Preservation of [[spectrum]]/[[eigenvalue]]s:**
Let $A \in M_{m,n}$, $B \in M_{n,m}$
- [[characteristic polynomial]] $P_{BA}(\lambda) = \lambda^{n-m}P_{AB}(\lambda)$ if $m \leq n$
- $P_{AB}(\lambda) = \lambda^{m-n}P_{BA}(\lambda)$ if $n \leq m$

In other words, $AB$ and $BA$ have the same nonzero eigenvalues (with the same [[algebraic multiplicity]]). If $A,B$ are both square ($m=n$) then $\sigma(AB) = \sigma(BA)$


###### Properties:
- matrix multiplication is **not** commutative ([[commutativity]])
- The [[matrix]] of the product of [[linear map]]s:
		- If $T \in \mathcal{L}(U,V)$ and $S \in \mathcal{L}(V,W)$, then $\mathcal{M}(ST) = \mathcal{M}(S)\mathcal{M}(T)$
- Entry of matrix product equals row times column:
		- Suppose $A$ is an *m*-by-*n* matrix and $C$ is an *n*-by-*p* matrix. Then $(AC)_{j,k} = A_{j,\cdot}C_{\cdot,k}$
- Column of matrix product equals matrix times column:
		- Suppose $A$ is an *m*-by-*n* matrix and $C$ is an *n*-by-*p* matrix. Then $(AC)_{\cdot,k} = AC_{\cdot,k}$ for $1 \leq k \leq p$

###### Additional Thoughts:
