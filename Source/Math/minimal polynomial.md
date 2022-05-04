name : minimal polynomial
tags : 
backlinks : 
source : #MASED 

###### Content:
Let $A \in M_n$ be given. There exists a unique [[monic polynomial]] $q_A(t)$ of minimum [[degree of a polynomial]] that annihilates $A$. The degree of $q_A(t)$ is at most $n$. If the [[annihilating polynomial]] $p(t)$ exists, then the minimal polynomial $q_A(t)$ divides $p(t)$, that is, $p(t)=h(t)q_A(t)$ for some monic polynomial $h(t)$.



###### Properties:
- [[similar]] matrices have the same minimal polynomial
- Let $A \in M_n$ be a given matrix whose distinct [[eigenvalue]]s are $\lambda_1, ...,\lambda_d$. The minimal polynomial of $A$ is $$q_A(t) = \prod^d_{i=1}(t-\lambda_i)^{r_i}$$ in which $r_i$ is the size of the largest [[Jordan block]] of $A$ corresponding to the eigenvalue $\lambda_i$.
- Let $A\in M_n$ have distinct eigenvalues $\lambda_1,\lambda_2, ...,\lambda_d$ and let $$q(t) = (t-\lambda_1)(t-\lambda_2)...(t-\lambda_d)$$ Then $A$ is [[diagonalizable]] if and only if $q(A)=0$.
- For each $A \in M_n$, the minimal polynomial $q_A(t)$ divides the [[characteristic polynomial]] $p_A(t)$. Moreover, $q_A(\lambda)=0$ if and only if $\lambda$ is an [[eigenvalue]] of $A$, so every root of $p_A(t)=0$ is a root of $q_A(t)=0$. In other words, every eigenvalue of the characteristic polynomial will end up in the minimal polynomial.
- Let $A \in M_n$ and let $q_A(t)$ be its minimal polynomial. The following are equivalent:
		- $q_A(t)$ is a product of distinct linear [[factor]]s
		- Every eigenvalue of $A$ has multiplicity $I$ as a root of $q_A(t)=0$
		- $q'_A(\lambda) \neq 0$ for every eigenvalue $\lambda$ of $A$
		- $A$ is [[diagonalizable]]
- Let $A \in M_n$ have minimal polynomial $q_A(t)$ and characteristic polynomial $p_A(t)$. The following are equivalent:
		- $q_A(t)$ has degree $n$
		- $p_A(t) = q_A(t)$
		- $A$ is [[nonderogatory]]
		- $A$ is [[similar]] to the [[companion matrix]] of $p_A(t)$.

###### Additional Thoughts:
