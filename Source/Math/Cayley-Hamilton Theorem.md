name : Cayley-Hamilton Theorem
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $A \in M_n$ be a matrix, and the [[characteristic polynomial]] of $A$ be $p_A(t)$. Then by the Cayley-Hamilton Theorem, every [[square matrix]] over a real of complex [[field]] satisfies its own charasteric polynomial:
$$p_A(A) = 0$$

###### Properties:
- If $A \in M_n$ is an [[invertible matrix]] with [[characteristic polynomial]] $$p_A(t) = t^n+a_{n-1}t^{n-1}+...+a_0$$ then $$A^{-1} = \frac{(-1)^{n-1}}{det(A)}(A^{n-1}+a_{n-1}A^{n-2}+a_{n-2}A^{n-3}+...+a_1I) = q(A)$$ Where $q(t)$ is a polynomial with [[degree of a polynomial]] less than $n$. Thus the inverse is always expressible as a polynomial.

###### Additional Thoughts:
