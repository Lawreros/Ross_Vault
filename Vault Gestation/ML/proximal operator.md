name : proximal operator
tags : 
backlinks : 
source : #sparse

###### Content:
The proximal operator of a [[convex function]] $f$ at $x$ is defined as the unique solution to: $$prox_f(x) = argmin_y (f(y)+\frac{1}{2}||x-y||^2_2)$$
where $f$ must be a proper, lower-semicontinuous convex function, but it is not required to be smooth nor differentiable.

###### Properties:
- What $f$ is defines what you call the proximal operator. For example, the proximal operator of the $l_1$ norm ([[Lp norm]]) is: $$prox_{\lambda||.||_1}(x) = \underset{x}{argmin} (\frac{1}{2}||b-Ax||^2_2+\lambda||x||_1) $$

###### Additional Thoughts:
