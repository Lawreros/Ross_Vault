name : block matrix
tags : 
backlinks : 
source : 

###### Content:
A block matrix or a partition matrix is a matrix that is interpreted as having been broken into sections called **blocks** or **submatrices**.

The matrix $$\textbf{P} = \begin{bmatrix}
1 & 2 & 2 & 7\\
1 & 5 & 6 & 2\\
3 & 3 & 4 & 5\\
3 & 3 & 6 & 7\\
\end{bmatrix}$$
can be partition into four 2x2 blocks
$$\textbf{P}_{11} = \begin{bmatrix}
1 & 2\\
1 & 5\\
\end{bmatrix}, \textbf{P}_{12} = \begin{bmatrix}
2 & 7\\
6 & 2\\
\end{bmatrix}, \textbf{P}_{21} = \begin{bmatrix}
3 & 3\\
3 & 3\\
\end{bmatrix}, \textbf{P}_{22} = \begin{bmatrix}
4 & 5\\
6 & 7\\
\end{bmatrix}$$
The partitioned matrix can then be written as $$P = \begin{bmatrix} P_{11} & P_{12}\\
P_{21} & P_{22} \end{bmatrix}$$

###### Properties:
- Block matrix multiplication: Given an $(m \times p)$ matrix $A$ with $q$ row partitions and $s$ column partitions and a $(p \times n)$ matrix $B$ with $s$ row partitions and $r$ column partitions that are compatible with the partitions of $A$, the matrix product $C = AB$ can be formed blockwise, yielding $C$ as an $(m \times n)$ matrix with $q$ row partitions and $r$ column partitions. The matrices in the resulting matrix $C$ are calculated by multiplying $$C_{qr} = \sum_{i=1}^sA_{qi}B_{ir}$$
- Block matrix [[determinant]]: $$\left( \begin{array}{cc} A & 0 \\ C & D \end{array} \right) = det(A)det(D) = det\left( \begin{array}{cc} A & B \\ 0 & D \end{array} \right)$$

###### Additional Thoughts:
