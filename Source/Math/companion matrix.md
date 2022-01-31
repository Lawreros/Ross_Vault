name : companion matrix
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
The companion matrix of the [[monic polynomial]]:
$$p(t) = t^n + c_{n-1}t^{n-1}+...+c_1t+c_0$$
is the square matrix defined as:
$$C(p) = \begin{bmatrix}
0 & 1 & 0 &... & 0\\
0 & 0 & 1 & ... & 0\\
0 & 0 & 0 &...  & 0\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
0 & 0 & 0 & \dots & 1\\
-c_0 & -c_1 & -c_2  & \dots & -c_{n-1}\\
\end{bmatrix}$$

###### Properties:
- The [[eigenvalue]]s  for $C(p)$ correspond with the roots of the monic polynomial $p(t)$ such that $p(\lambda) = 0$.
- The [[geometric multiplicity]] of $\lambda$ is 1, so the companion matrix is [[nonderogatory]]
- The companion matrix of a [[monic polynomial]] is [[nonderogatory]]

###### Additional Thoughts:
