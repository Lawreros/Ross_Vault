name : induced matrix norm
tags : 
backlinks : 
source : https://www.cs.utexas.edu/users/flame/laff/alaff/chapter01-induced-matrix-norms.html

###### Content:
Let $||\cdot||_\mu: \mathcal{K}^m \rightarrow \mathbb{R}$ and $||\cdot||_v: \mathcal{K}^n \rightarrow \mathbb{R}$ be [[vector norm]]s. Define the induced [[matrix norm]] $||\cdot||_{\mu , v}: \mathcal{K}^{m\times n} \rightarrow \mathcal{K}$ as:
$$||A||_{\mu ,v} = \underset{x \in \mathbb{C}^n}{sup}\frac{||Ax||_\mu}{||x||_v}$$
where $x$ is a nonzero vector.

###### Properties:
- Some [[matrix norm]]s which are induced by [[vector norm]]s:
		$||\cdot||_{1,1}$ is induced by the L1 norm
		$||\cdot||_{\infty,\infty}$ is induced by the L-infinity norm
		$||\cdot||_{2,2}$ is induced by the [[L2 norm]]

- Not all matrix norms are induced:
		L1 norm on $M_n(\mathcal{K})$: $||A||_1 = \sum_{i,j}^n |a_{i,j}|$
		L2 norm (or [[Frobenius norm]]) on $M_n(\mathcal{K})$: $||A||_2 = ||A||_F = \sqrt{\sum_{i,j}^n |a_{i,j}|^2}$

###### Additional Thoughts:
