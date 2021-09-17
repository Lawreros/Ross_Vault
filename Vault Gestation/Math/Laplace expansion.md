name : Laplace expansion
tags : 
backlinks : 
source : #MASED, https://en.wikipedia.org/wiki/Laplace_expansion

###### Content:
An expression of the [[determinant]] of an $n\times n$ matrix as a weighted sum of "minors", which are the [[determinant]]s of some $(n-1) \times (n-1)$ submatrices of $A$.

Suppose $A = [a_{ij}] \in M_n(\textbf{F})$. Assume that the determinant is defined over $M_{n-1}(\textbf{F})$ and let $A_{ij} \in M_{n-1}(\textbf{F})$ denote the submatrix of $A\in M_n(\textbf{F})$ obtained by deleting row $i$ and column $j$ of $A$. Then, for any $i,j \in \{1,...,n\}$, we have: $$detA = \sum_{k=1}^n(-1)^{i+k}a_{ik} det A_{ik} = \sum_{k=1}^n(-1)^{k+j}a_{kj}detA_{kj}$$
The first sum is the *Laplace expansion by minors along row i*; the second sum is the *Laplace expansion by minors along column j*.

----
Another way to describe this is: $$det A=\sum_{k=1}^n(-1)^{i+k}a_{ik}\Omega_{ik} = \sum_{k=1}^n(-1)^{k+j}a_{kj}\Omega_{kj}$$ where $\Omega_{s,t}=detA$ after deleting the s'th row and the t'th column.

----
Or, to help visualize this, consider the matrix:
$$B = \begin{bmatrix}
1 & 2 & 3\\
4 & 5 & 6\\
7 & 8 & 9
\end{bmatrix}$$
The determinant of this matrix can be computed by using the Laplace expansion along any one of its rows or columns. For instance, and expansion along the first row yields:
$$detB = 1*det\begin{bmatrix}
5 & 6\\
8 & 9
\end{bmatrix} - 2*det\begin{bmatrix}
4 & 6\\
7 & 9
\end{bmatrix} + 3*det\begin{bmatrix}
4 & 5\\
7 & 8
\end{bmatrix}$$
$$=1*(-3)-2*(-6)-3*(-3)=0$$
Laplace expansion along the second column yields the same result:
$$detB = -2*det\begin{bmatrix}
4 & 6\\
7 & 9
\end{bmatrix} +5*det\begin{bmatrix}
1 & 3\\
7 & 9
\end{bmatrix} -8*det\begin{bmatrix}
1 & 3\\
4 & 6
\end{bmatrix}$$
$$=-2*(-6)+5*(-12)-8*(-6)=0$$

###### Properties:


###### Additional Thoughts:
