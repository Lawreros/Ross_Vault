name : gradient descent
tags : 
backlinks : 
source : #sparse

###### Content:
Used when wanting to minimize a convex and differentiable function $f(x): \mathbb{R}^m \rightarrow \mathbb{R}$. One of the most popular optimization strategies, gradient descent is particularly appealing in high-dimensional problems, since it only involves having access to the gradient of the function at a given point, and is given by the updates:
$$x^{k+1}=x^k-\eta \nabla f(x^k)$$

###### Properties:
- Let $f(x):\mathbb{R}^m \rightarrow \mathbb{R}$ be a [[convex function]], differentiable, and [[L-smooth]]. Then the $x^k$ update of a gradient descent from the initialization $x^0$ with $\eta\leq 1/L$ satisfies: $$f(x^k)-f(x^*) \leq \frac{L}{2k}||x^0-x^*||^2_2$$ where $f(x^*)$ is the optimal value.
- Gradient descent converges at a rate of $\mathcal{O}(1/k)$

###### Additional Thoughts:
