name : L-smooth (Lipschitz smooth/continuous)
tags : 
backlinks : 
source : #sparse 

###### Content:
A differentiable function $f(x): \mathbb{R}^m \rightarrow \mathbb{R}$ is L-smooth if, for any $x,y \in \mathbb{R}^m$,
$$||\nabla f(x) - \nabla f(y)||_2 \leq L||x-y||_2$$
where $L$ is some constant. Intuitively, $L$ is a measure of how fast the function can change.

###### Properties:
- Due to the Descent Lemma, when $f(x)$ is L-smooth, it is known that for every $x,y$ in its domain, the function value can be upper bounded by a quadratic function: $$f(y) \leq f(x) +\nabla f(x)^T(y-x)+\frac{L}{2}||y-x||^2_2$$

###### Additional Thoughts:
