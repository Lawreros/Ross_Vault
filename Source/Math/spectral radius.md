name : spectral radius
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $\lambda_1,...,\lambda_n$ be the eigenvalues of a matrix $A \in M_n$. Then its spectral radius $\rho (A)$ is defined as:
$$\rho (A) = max\{|\lambda_1|,...,|\lambda_n\}$$

###### Properties:
- Let $||\cdot||$ be a [[matrix norm]] on $M_n$, then for all $A\in M_n$: $\rho(A) \leq ||A||$
- For any $A \in M_{m,n}$, $\underset{k \rightarrow \infty}{lim} A^k = 0$ if and only if $\rho(A) <1$
- For any [[matrix norm]] $||\cdot||$ on $M_n$, and any $A \in M_n$: $$\underset{k\rightarrow \infty}{lim}||A^k||^{1/k} = \rho(A)$$
- Let $A \in M_n$ be given, and let $\epsilon > 0$ be a given scalar. There exists a [[matrix norm]] $||\cdot||$ on $M_n$ such that $||A|| \leq \rho (A)+\epsilon$ 
- Let $A,B \in M_n$ such that $|A| \leq B$, then $\rho(A) \leq \rho(|A|) \leq \rho(B)$, where $|A|$ denotes a matrix with entrywise absolute values

###### Additional Thoughts:
