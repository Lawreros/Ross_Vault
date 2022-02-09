name : Moure-Penrose inverse (pseudoinverse)
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $A \in M_{m,n}$, there exists a unique {1,2,3,4}-[[generalized inverse]] $A^\dagger \in M_{n,m}$ called the Moure-Penrose (Generalized) inverse.

###### Properties:
- When $A$ has [[linearly independent]] columns (and thus the matrix $AA^*$ is invertible), $A^\dagger$ can be expressed as: $$A^\dagger = (A^*A)^{-1}A^*$$ which is a "left inverse", since $A^\dagger A=I$ When $A$ has linearly independent columns (and thus matrix $A^*A$ is invertible), $A^\dagger$ can be expressed as: $$A^\dagger = A^*(AA^*)^{-1}$$ which is a "right inverse", since $AA^\dagger =I$
- If $A$ is real, then the M-P inverse is real
- (Useful with [[SVD]]) The psuedoinverse of a diagonal matrix $D$ is: $$\begin{bmatrix} 1/d_{11} & 0 & ... & 0\\ 0 & 1/d_{22} & ... & 0\\ 0 & 0 & \ddots & 0\\ 0 & 0 & ... & 1/d_{nn}\end{bmatrix}$$
- Let $A \in M_{m,n}$ and $b\in \mathbb{C}^m$. Among the solutions to $\underset{x \in \mathbb{C}^n}{min} ||Ax - b||_2$, $A^\dagger b$ is a unique solution of least [[L2 norm]]

###### Additional Thoughts:
- This accounts for matrices which may not be [[invertible]], where the pseudoinverse (while not "truly" the inverse) follows all of the properties of a [[generalized inverse]].