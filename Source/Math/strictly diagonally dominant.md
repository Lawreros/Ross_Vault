name : strictly diagonally dominant
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
A matrix $A \in M_n$ is strictly diagonally dominant if, $\forall i$, $|a_{ii}| > \sum_{j\neq i1}|a_{ij}|$

###### Properties:
- A strictly diagonally dominant matrix is [[invertible]]. By way of contradiction, if $A\in M_n$ is [[singular]], then $0 \in \sigma(A)$, thus by [[Gershgorin's Theorem]] there exists an $i$ such that $|0-a_{ii}| \leq \sum_{i\neq j}|a_{ij}|$
- Suppose $A \in M_n$ is strictly diagonally dominant except in 1 row, where $a_{kk} \neq 0$ and [[diagonally dominant]] in the $k$-th row, then $A$ is [[invertible]].

###### Additional Thoughts:
