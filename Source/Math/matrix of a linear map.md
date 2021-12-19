name : matrix of a [[linear map]] $\mathcal{M}(T)$
tags : 
backlinks : 
source : #LADR

###### Content:
Suppose $T \in \mathcal{L}(V,W)$ and $v_1,...,v_n$ is a [[basis]] of $V$ and $w_1,...,w_m$ is a basis of $W$. The [[matrix]] of $T$ with respect to these bases is the $m$-by-$n$ matrix $\mathcal{M}(T)$ whose entries $A_{j,k}$ are defined by:
$$Tv_k=A_{1,k}w_1+...+A_{m,k}w_m$$
If the bases are not clear from the context, then the notation $\mathcal{M}(T,v_1,...,v_n),(w_1,...,w_m))$ is used.

To remember how $\mathcal{M}(T)$ is constructed from $T$, you might write across the top of the matrix the basis vectors $v_1,...,v_n$ for the domain and along the left the basis vectors $w_1,...,w_m$ for the [[vector space]] into which $T$ maps:

$$
\mathcal{M}(T) = \begin{matrix}
w_1\\
\vdots \\
w_m
\end{matrix}

\begin{matrix}
v_1 \dots v_k \dots v_n\\
\begin{bmatrix}
\dots & A_{1,k}& \dots\\
& \vdots &\\
\dots & A_{m,k} & \dots
\end{bmatrix}
\end{matrix}

$$

###### Properties:

###### Additional Thoughts:
