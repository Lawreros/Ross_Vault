name : strongly connected
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $A \in M_n$ be a matrix with [[entry directed graph]] $\Gamma (A)$ is strongly connected if $\forall i,j \in \{1,2,...,n\}$ there exists a directed path from $i$ to $j$.

**Example**
$$A = \begin{bmatrix} 0 & 1 & 0\\
0 & 0 & 1\\
i & 0 & 0\\
\end{bmatrix}$$
path from vertex 1 to 2 has edge weight 1, vertex 2 to 3 has edge weight 1, and vertex 3 to 1 has edge weight $i$. Thus you can get from any node to any other node by following the edges.

**Exception**
- The zero matrix is not strongly connected

###### Properties:
- A matrix $A \in M_1$ that is not the zero matrix is strongly connected.
- Strongly connected matrices are [[irreducible]]

###### Additional Thoughts:
