name : dual norm
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
Let $\mathcal{K}^n,||\cdot||$ be a [[normed linear space]]. The dual norm $||\cdot||^D$ on $\mathcal{K}^n$ is defined as follows. For all $y \in \mathcal{K}^n$:
$$||y||^D:=\underset{||x||=1}{max}|y^*x| = \underset{x \neq 0}{max} \frac{|y^*x|}{||x||}$$
where $x \in \mathcal{K}^n$.

###### Properties:
- This is the [[operator norm]] relative to [[dual space]]
- Let $\mathcal{K}^n,||\cdot||$ be a [[normed linear space]]. For all $x,y \in \mathcal{K}^n$: $$|y^*x|\leq ||x||||y||^D$$
- On $\mathcal{K}^n$:
			$||\cdot||_1^D = ||\cdot||_\infty$
			$||\cdot||_\infty^D = ||\cdot||_1$
			$||\cdot||_2^D = ||\cdot||_2$
- If  $\mathcal{K}^n,||\cdot||$ is a [[normed linear space]], then $||\cdot||^{D^D} = ||\cdot||$

###### Additional Thoughts:
