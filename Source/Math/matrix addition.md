name : matrix addition
tags : 
backlinks : 
source : #LADR

###### Content:
The sum of two matrices of the same size is the [[matrix]] obtained by adding the corresponding entries in the matrices:
$$\begin{bmatrix}
A_{1,1} & \dots & A_{1,n} \\
\vdots & & \vdots\\
A_{m,1} & \dots & A_{m,n}
\end{bmatrix}
+
\begin{bmatrix}
C_{1,1} & \dots & C_{1,n} \\
\vdots & & \vdots\\
C_{m,1} & \dots & C_{m,n}
\end{bmatrix}
=
\begin{bmatrix}
A_{1,1} +C_{1,1} & \dots & A_{1,n}+C_{1,n} \\
\vdots & & \vdots\\
A_{m,1}+C_{m,1} & \dots & A_{m,n}+C_{m,n}
\end{bmatrix}$$

In other words, $(A+C)_{j,k}=A_{j,k}+C_{j,k}$
###### Properties:
- The matrix of the sum of [[linear map]]s
		- Suppose $S,T \in \mathcal{L}(V,W)$. Then $\mathcal{M}(S+T) = \mathcal{M}(S)+\mathcal{M}(T)$

###### Additional Thoughts:
