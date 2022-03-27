name : interlacing
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
There are two different interlacing properties covered in the Matrix Analysis class:

**Interlacing "I"**
For any $A \in M_n$ [[Hermitian]] matrix, vector $y \in \mathbb{C}^n$, scalar $a \in \mathbb{R}$:
$$\lambda_k(A+ayy^*) \leq \lambda_{k+1}(A)$$
$\forall k = 1,...,n-1$, where $yy^*$ is a [[rank]]-1 matrix.

- Let $A,B \in M_n$ be [[Hermitian]], with $rank(B)=r$. Then $\forall k$ $\lambda_k(A+B)\leq \lambda_{k+r}(A)$
- Suppose $A,B \in M_n$ are [[Hermitian]], with $rank(B) = r$. Then $\forall k$: $$\lambda_{k-r}(A) \leq \lambda_k(A+B) \leq \lambda_{k+r}(A)$$ $$\lambda_{k-r}(A+B) \leq \lambda_k(A) \leq \lambda_{k+r}(A+B)$$ This is shown by using the previous bullet point but let $\hat{A} = A+B$ and $\hat{B} = -B$


**Interlacing "II"**
Let $A \in M_n$ be [[Hermitian]], $B$ be an $r$-by-$r$ [[principle submatrix]] (say $i,i_2,...,i_{n-r}$ are the rows/columns deleted from $A$). Then $\forall k = 1,2,...,n$ $$\lambda_k(A) \leq \lambda_k(B) \leq \lambda_{k+n-r}(A)$$

- Suppose $A \in M_n$ is [[Hermitian]], then $\forall i$ $\lambda_1(A) \leq a_{ii} \leq \lambda_n(A)$

###### Properties:


###### Additional Thoughts:
