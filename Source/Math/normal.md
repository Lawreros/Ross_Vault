name : normal
tags : 
backlinks : [[matrix]]
source : #MASED 

###### Content:
 An [[operator]] on an [[inner product space]] is called normal if it commutes with it's adjoint ([[conjugate transpose]]). $T \in \mathcal{L}(V)$ is said to be normal if $T^*T = TT^*$

###### Properties:
- **Spectral theorem for normal matrices:** Consider $A \in M_n$ with [[eigenvalue]]s $\lambda_1,\lambda_2,...,\lambda_n$. The following are equivalent:
	1) $A$ is [[normal]]
	2) $A$ is [[unitarily diagonalizable]]
	3) $||A||_F^2 = \sum_{i=1}^n |\lambda_i|^2$   ([[Frobenius norm]])

- $T$ is normal if and only if $||Tv|| = ||T^*v||$ for all $v \in V$ and [[vector norm]] $||\cdot||$. An operator $T \in \mathcal{L}(V)$ is normal if and only if $||Tv|| = ||T^*v||$ for all $v \in V$
- For $T$ to be [[normal]], $T$ and $T^*$ have the same [[eigenvector]]s. Suppose $T \in \mathcal{L}(V)$ is normal and $v \in V$ is an eigenvector of $T$ with [[eigenvalue]] $\lambda$. Then $v$ is also an eigenvector of $T^*$ with eigenvalue $\bar \lambda$.
- Let $A,B \in M_n$ be [[unitarily similar]]. $A$ is normal if and only if $B$ is normal.
- [[orthogonal]] eigenvectors for normal operators. Suppose $T \in \mathcal{L}(V)$ is normal. Then eigenvectors of $T$ corresponding to distinct eigenvalues are orthogonal.
- $A^* = AU$ for some normal matrix $A$ and [[unitary matrix]] $U$
- Let $A \in M_n$ be partitioned as $A = \begin{bmatrix}A_{11} & A_{12} \\ 0 & A_{22}\end{bmatrix}$, in which $A_{11}$ and $A_{22}$ are square. Then $A$ is normal if and only if $A_{11}$ and $A_{22}$ are normal and $A_{12} = 0$. A [[block upper-triangular matrix]] is normal if and only if each of its off-diagonal blocks is zero and each of its diagonal blocks is normal' in particular, an [[upper-triangular matrix]] is normal if and only if it is [[diagonal]].

###### Additional Thoughts:
