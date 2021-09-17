name : conjugate transpose, [[adjoint]], or Hermitian adjoint
tags : 
backlinks : 
source : #MASED 

###### Content:
The conjugate transpose of $A \in M_{m,n}(\textbf{C})$, is denoted by $A^*$ and defined by $A^* = \bar A^T$, in which $\bar A$ is the entrywise [[complex conjugate]]. For example:
$$\begin{bmatrix} 1+i & 2-i \\
-3 & -2i \end{bmatrix}^* = 
\begin{bmatrix} 1-i & -3 \\
2+i & 2i \end{bmatrix}^*$$

**The matrix of $T^*$**
Let $T \mathcal{L}(V,W)$. Suppose $e_1,...,e_n$ is an [[orthonormal basis]] of $V$ and $f_1,...,f_m$ is an orthonormal basis of $W$. Then $$\mathcal{M}(T^*, (f_1,...,f_m),(e_1,...,e_n))$$ is the conjugate transpose of $$\mathcal{M}(T,(e_1,...,e_n), (f_1,...,f_m))$$

###### Properties:
- Both the [[transpose]] and the conjugate transpose obey the *reverse-order law:* $(AB)^T = B^TA^T$ and $(AB)^*=B^*A^*$
- For the complex conjugate of a product, there is no reversing: $\overline AB = \bar A \bar B$

###### Additional Thoughts:
