name : linear transformation
tags : 
backlinks : [[linear map]]
source : Matrix Analysis

###### Content:
Let $V,W$ be [[vector space]]s over [[field]]$\mathcal{K}$, and let $T: V \rightarrow W$ be a linear transformation if $\forall x,y \in V$ and scalars $\alpha, \beta \in \mathcal{K}$ $$T(\alpha x + \beta y) = \alpha T(x) + \beta T(y)$$

**Example:**
$$A \in M_{m,n} : \mathbb{C}^n \rightarrow \mathbb{C}^m$$

###### Properties:
- If $V$ [[vector space]] over $\mathcal{K}$ is finite dimensional, say $dim(T) = n$, then $V$ is [[isomorphic]] to $\mathcal{K}^n$ over $\mathcal{K}$
- Say $B = \{b^{(1)},b^{(2)},...,b^{(n)}\}$ is a [[basis]] for $V$, then $\forall x \in V$ there exists a unique $\alpha_1,\alpha_2,...,\alpha_n$ such that $x = \sum_{i=1}^n \alpha_1 b^{(i)}$
- If $V,W$ are [[finite-dimensional vector space]]s that have bases $B_v := \{b^{(1)},b^{(2)},...,b^{(n)}\}$, $B_w := \{b^{(1)'},b^{(2)'},...,b^{(n)'}\}$. Then $T : V \rightarrow W$ is a linear transformation if and only if there exists $A \in M_{m,n}(\mathcal{K})$ such that $\forall x \in V, y \in W$ the transformation $T(x) = y$ if and only if $Ax_{B_V} = y_{B_W}$
- Let $V, ||\cdot||_V$ and $W, ||\cdot||_W$ be [[normed linear space]]s over $\mathcal{K}$ such that $T: V \rightarrow W$ is a linear transformation. $T$ is continuous if and only if $\underset{x \in V}{sup} \frac{||Tx||_W}{||x||_V} < \infty$ where $x$ is nonzero.

###### Additional Thoughts:
