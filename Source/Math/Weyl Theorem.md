name : Weyl Theorem
tags : 
backlinks : 
source : Matrix Analysis 

###### Content:
Let $A,B \in M_n$ be [[Hermitian]] matrices, for all $k = 1,2,...,n$ and [[eigenvalue]]s ordered as $\lambda_n \geq \lambda_{n-1} \geq ... \geq \lambda_1$:
$$\lambda_k(A) + \lambda_1(B) \leq \lambda_k(A+B) \leq \lambda_k(A) + \lambda_n(B)$$

This can be proven using [[Courant-Fisher Theorem]]:
$$\lambda_k(A+B) = \underset{y_{k+1},y_{k+2},...,y_{n}}{min} \text{ }\text{ }\underset{x \perp y_{k+1},y_{k+2},...,y_{n}}{max} \frac{x^*(A+B)x}{x^*x} = \underset{}{min} \text{ } \underset{}{max}(\frac{x^*Ax}{x^*x} +\frac{x^*Bx}{x^*x})$$
$$\leq \underset{}{min} \text{ } \underset{}{max}(\frac{x^*Ax}{x^*x} + \lambda_n(B)) = \underset{}{min} \text{ } \underset{}{max} \frac{x^*Ax}{x^*x} + \lambda_n(B)= \lambda_k(A)+\lambda_n(B)$$

###### Properties:
- For Hermitian $A \in M_n$ and [[positive semidefinite]] $B\in M_n$, for all $k$ $\lambda_k(A) \leq \lambda_k(A+B)$

###### Additional Thoughts:
