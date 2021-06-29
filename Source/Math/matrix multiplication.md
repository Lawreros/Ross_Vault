name : matrix multiplication
tags : 
backlinks : 
source : [[Linear Algebra Done Right]]

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

###### Properties:
- matrix multiplication is **not** commutative
- The [[matrix]] of the product of [[linear map]]s:
		- If $T \in \mathcal{L}(U,V)$ and $S \in \mathcal{L}(V,W)$, then $\mathcal{M}(ST) = \mathcal{M}(S)\mathcal{M}(T)$
- Entry of matrix product equals row times column:
		- Suppose $A$ is an *m*-by-*n* matrix and $C$ is an *n*-by-*p* matrix. Then $(AC)_{j,k} = A_{j,\cdot}C_{\cdot,k}$
- Column of matrix product equals matrix times column:
		- Suppose $A$ is an *m*-by-*n* matrix and $C$ is an *n*-by-*p* matrix. Then $(AC)_{\cdot,k} = AC_{\cdot,k}$ for $1 \leq k \leq p$

###### Additional Thoughts:
