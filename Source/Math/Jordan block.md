name : Jordan block
tags : 
backlinks : 
source : #MASED 

###### Content:
A Jordan block $J_k(\lambda)$ is a $k$-by-$k$ [[upper-triangular matrix]] of the form $$J_k(\lambda) = \begin{bmatrix}
\lambda & 1 & 0 & 0 & 0 &0 \\
0& \lambda & 1 &0 &0 & 0\\
0& 0& \ddots & \ddots & 0& 0\\
0& 0& 0& \lambda & 1 \\
0& 0& 0& 0& \lambda
\end{bmatrix} : J_1(\lambda) = [\lambda], J_2(\lambda) = \begin{bmatrix} \lambda & 1 \\ 0 &\lambda \end{bmatrix}$$
The scalar $\lambda$ appears $k$ times on the main diagonal; if $k > 1$, there are $k-1$ entries "+1" in the [[superdiagonal]]; all other entries are zero. A [[Jordan matrix]] $j \in M_n$ is a [[direct sum]] of Jordan blocks $$ J = J_{n_{1}}(\lambda_1) \bigoplus J_{n_{2}}(\lambda_2) \bigoplus J_{n_{3}}(\lambda_3) \bigoplus ... \bigoplus J_{n_{q}}(\lambda_q)$$
where $n_1+n_2+...+n_q=n$. Or, put another way:
$$\begin{bmatrix} J_{n_1}(\lambda_1) & 0 & ... & 0\\
0 & J_{n_2}(\lambda_2) & ... & 0\\
0 & 0 & \ddots & 0 \\
0 & 0 & ... & J_{n_q}(\lambda_q)
\end{bmatrix}$$
where $\lambda_i$ does not have to be distinct.



###### Properties:
- $J_k$ has the [[eigenvalue]] $\lambda$ with [[algebraic multiplicity]] of $k$ and [[geometric multiplicity]] of 1 and a 1 dimensional [[eigenspace]].

###### Additional Thoughts:
