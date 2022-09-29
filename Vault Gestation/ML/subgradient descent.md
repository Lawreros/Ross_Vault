name : subgradient descent
tags : 
backlinks : 
source : #sparse

###### Content:
A method for find the minimum when [[gradient descent]] is not applicable (i.e. when the function is not smooth). The subgradient of a [[convex function]] $f: \mathbb{R} \rightarrow R$ at a point $x$ is any vector $g \in \mathbb{R}^m$ such that $$f(y) \geq f(x)+g^T(y-x)$$ for all $x,y \in \mathbb{R}^m$ (*Note that you are concerned with $g$'s that fit*).
Note that this is analogous to the condition satisfied by gardients of differentiable functions, except here $g$ can be *any* vector in $\mathbb{R}^m$ that meets the above inequality. Subgradients always exist for convex functions on the interior of their domains (i.e. all potential inputs of $x$), having a [[subdifferential]] of the function $f$ at each $x$, denoted by $\partial f(x)$.
With these definitions, we can now generalize [[gradient descent]] to subgradient descent, which is given by the iterates: $$x^{k+1}=x^k-\eta^kg^k$$
where $g^k \in \partial f(x^k)$. The only difference between this and [[gradient descent]] is that here $g$ can be any vector in the [[subdifferential]] of $f$ at $x$.
The gradient of a differentiable function has the property that i constitutes a descent direction: the function value is decreased if we move along $\nabla f(x)$ for small enough step-sizes. The property is lost for subgradients, as they don't always constitute descent directions (*Tommy: think of gradients as vectors*). This makes the analysis of this algorithm slightly more involved, and the step-sizes have to be chosen carefully to ensure convergence. Common choices are $\eta^k = \frac{1}{k}$ where each iteration $k$ has a smaller step size $1/k$.

**Example:**
We can use this to minimize the [[LASSO]] problem, where:$$||Ax-b||^2_2+\lambda||x||_1$$ The function $f(x)$ is differentiable, meaning $\nabla f(x) = A^T(Ax-b)$, and $g(x) = ||x||_1$. Because $g(x)=||x||_1 = \sum_{i=1}^m|x_i|$ and $|x_i|$ is differentiable everywhere except zero (it has slope $-1$ if $x<0$ and $1$ if $x>0$) , obtaining the subgradient of $||.||_1$ is now easy. Since the function is seperable, a vector in the [[subdifferential]] will be any vector $g$ withe each coordinate $g_i$ given by the expression above.
Thus, our iterative approach for [[LASSO]] using subgradient descent is: $$x^{k+1} = x-\eta^k(A^T(Ax^k-b)+g^k)$$ for $g^k \in \partial||x^k||_1$

###### Properties:
- The extra difficulties of convergence results in a rate of $\mathcal{O}(1/\sqrt{k})$ for subgradient descent. This can be improved with further assumptions about $f$. For instance, if $f$ is also strongly convex, this rate can be improved to $\mathcal{O}(1/k)$

###### Additional Thoughts:
