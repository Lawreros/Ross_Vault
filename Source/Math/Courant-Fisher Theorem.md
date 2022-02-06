name : Courant-Fisher Theorem
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $A \in M_n$ be [[Hermitian]] and its [[eigenvalue]]s are ordered $\lambda_n \geq \lambda_{n-1}\geq ... \geq \lambda_1$. For all $k = 1,2,...,n$:
$$\underset{y_1,y_2,...,y_{k-1}}{max} \text{ }\text{ }\underset{x \perp y_1,y_2,...,y_{k-1}}{min} \frac{x^*Ax}{x^*x} = \lambda_k(A)$$ or

$$\underset{y_{k+1},y_{k+2},...,y_{n}}{min} \text{ }\text{ }\underset{x \perp y_{k+1},y_{k+2},...,y_{n}}{max} \frac{x^*Ax}{x^*x} = \lambda_k(A)$$
where $x,y \in \mathbb{C}^n$ are vectors and $x \perp y_1$ denotes that $x$ is orthogonal/perpendicular to $y$.

In other words, say you want to find $\lambda_1(A)$, where $k=1$, using the first equation you will have no vector for $y$ as $y_{k-1} = \{\emptyset\}$, so then you just need to find some nonzero vector $x \perp \{\emptyset\}$ that minimizes the equation (see [[Rayleigh-Ritz  method]]). Now, to find $\lambda_2(A)$, where $k=2$, you set $y_1$ to be equal to the vector you found for $x$ (we'll call $x_{prev}$). Now $y_{k-1} = \{x_{prev}\}$ and you find a value $x \perp x_{prev}$ that minimizes the equation. Repeat this process, continually adding you found $x$ to the set of $y$ vectors until you have found all eigenvalues.

You are essentially finding eigenvector after eigenvector which either maximize or minimize the equation through the use of [[orthogonal]] vectors.

###### Properties:


###### Additional Thoughts:
