name : iterative soft thresholding algorithm (ISTA)
tags : 
backlinks : 
source : #sparse , https://blogs.princeton.edu/imabandit/2013/04/11/orf523-ista-and-fista/

###### Content:
One of the most popular choices for optimization of sparse regularized problems. ISTA is a first order method for minimizing an augmented function $Q(x,z)$ so that $Q(x,z) \geq F(x)$ for all $z$ and $Q(x,x)=F(x)$. Let $F(x) = f(x)+g(x)$ where $f(x)=\frac{1}{2}||b-Ax||^2_2$ and $g(x) = \lambda ||x||_1$ ([[Lp norm]]). Consider the choice:
$$Q(x,z) = f(z)+g(x)+\nabla f(z)^T(x-z)+\frac{\eta}{2}||x-z||^2_2$$
It is easy to see that $Q(x,z) \geq F(x)$ because, since $f(x)$ is [[L-smooth]] it can be upper-bounded by a quadratic function:
$$f(x) \leq f(z)+\nabla f(z)^T(x-y)+\frac{L}{2}||x-z||^2_2$$
Thus, by adding $g(x)$ to both sides we can see that $Q(x,z) \geq F(x)$ as long as $\eta \geq L$. In our particular case, recall that $f(x), L= \lambda_{max}(A^TA)$. Now the formulation of $Q(x,z)$ is useful because we are after $min_xQ(x,z)$. Let us expand and simplify this problem:
$$\underset{x}{argmin}Q(x,z) = \underset{x}{argmin} f(z)+\nabla f(z)^T(x-z) + \frac{\eta}{2}||x-z||^2_2+g(x)$$
$$= \underset{x}{argmin} f(z)+\nabla f(z)^Tx-\nabla f(z)^Tz + \frac{\eta}{2}||x-z||^2_2+g(x)$$
Because $f(z)$ is a constant and does not change with respect to $x$, it is redundant to the minimization and can be removed:
$$= \underset{x}{argmin} \frac{\eta}{2}(||x-z||^2_2+\frac{2}{\eta} \nabla f(z)^Tx)+g(x)$$
We can then expand the L-2 norm using the [[FOIL method]], we find
$$ = \underset{x}{argmin} \frac{\eta}{2}(||x||^2_2-2(z)^Tx+||z||^2_2+\frac{2}{\eta}\nabla f(z)^Tx)+g(x)$$
Noticing how $2z^T(x)x+\frac{2}{\eta}\nabla f(z)^Tx = 2(z-\eta^{-1}\nabla f(z))x$, which results in a form similar to that needed when [[completing the square]], we can capitalize by adding $+||z-\eta \nabla^{-1} f(z)||_2^2-||z-\eta \nabla^{-1} f(z)||_2^2$ to complete the square:
$$= \underset{x}{argmin} \frac{\eta}{2}(||x||^2_2-2(z-\eta^{-1} \nabla f(z))x)+||z-\eta^{-1} \nabla f(z)||_2^2-||z-\eta^{-1} \nabla f(z)||_2^2)+g(x)$$
Because $||z-\eta \nabla^{-1} f(z)||_2^2$ does not change with $x$,  the second occurrence can be can be ignored to give us a form we can use the [[completing the square]] method to get back to an L-2 norm:
$$=\underset{x }{argmin} \frac{\eta}{2}||x-(x^k-\eta \nabla f(x^k))||^2_2+g(x)$$
Recalling that $\nabla f(z) = A^T(Az-b)$ and defining $g=z-\eta^{-1}A^T(Az-b)$, we get: $$\underset{x}{min}||x-g||^2_2+\frac{\lambda}{\eta}||x||_1$$

Whose solution is given by the [[soft-thresholding operator]] $\mathcal{S}_\lambda(g)$. Putting everything together and recalling the min-max approach consists on iteratively performing the updates $$x^{i+1} = \mathcal{S}_{\lambda/n}(x^i- \eta^{-1}A^T(Ax^i-b))$$

###### Properties:
- You can also write the iterative equation as $$x^{i+1}=prox_{\frac{\lambda}{\eta}||.||_1}(x^i-\eta^{-1}\nabla f(x^i))$$ since the [[soft-thresholding operator]] is nothing else that the[[proximal operator]] of the L-1 norm.

###### Additional Thoughts:
