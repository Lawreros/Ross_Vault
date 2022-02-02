name : nonnegative matrix
tags : 
backlinks : [[positive matrix]]
source : Matrix Analysis

###### Content:
The matrix $A \in M_{m,n}(\mathbb{R})$ is considered a positive matrix if every entry in the matrix is real and greater than or equal to 0. This is denoted as: $$A \geq 0$$

###### Properties:
- Suppose $A \in M_n$, $A \geq 0$, the scalar $\alpha \geq 0$, and $\forall i$ $\sum_{j=1}^n a_{i,j} = \alpha$, then we know that the [[spectral radius]] $\rho(A) = ||A||_{\infty,\infty} = \alpha$
- Suppose $A \in M_n$ where $A \geq 0$. Then $\underset{i}{min} \sum_{j=1}^n a_{i,j} \leq \rho(A)$
- If $A \in M_n$ is a nonnegative matrix and [[irreducible]], then the [[spectral radius]] $\rho(A) > 0$
- Suppose $A \in M_n$ is a positive matrix, and the vector $x \in \mathbb{C}^n$ is a positive vector (no entries $\leq 0$). If there exists some $\alpha \geq 0$ such that $Ax \geq \alpha x$, then $\rho(A) \geq \alpha$. If there exists some $\alpha \geq 0$ such that $Ax \leq \alpha x$, then $\rho(A) \leq \alpha$.

###### Additional Thoughts:
