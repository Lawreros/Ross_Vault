name : kernel trick
tags : 
backlinks : 
source : https://towardsdatascience.com/the-kernel-trick-c98cdbcaeb3f

video: https://www.youtube.com/watch?v=Q7vT0--5VII

###### Content:
The kernel trick is used in [[nonlinear SVM]] to provide a solution to the complexities of transforming data to a higher dimensional space. In real application, there might be many features in data and applying transformations that involve many [[polynomial]] combinations of these features will lead to extremely high and impractical computational costs.

The kernel trick provides a solution to this problem by representing the data only through a set of pairwise similarity comparisons between data observations $x$ (with the original coordinates in the lower dimensional space), instead of explicitly applying the transformations $\phi(x)$.

In the kernel methods, the data set $X$ is represented by an $n\times n$ kernel matrix of pairwise similarity comparisons where the entries $(i,j)$ are defined by the kernel function: $$k(x_i,x_j)$$ This kernel function has a special mathematical property, as it acts as a modified dot product.

More formally, if we have data $x,z \in X$ and a map $\phi : X \rightarrow \mathbb{R}^n$ then $$k(x,z) = \langle \phi(x),\phi(z)\rangle$$ is a kernel function.

It can help to understand how the kernel function is equal to the dot product of the transformed vectors by considering that each coordinate of the transformed vector $\phi(x)$ is just some function of the coordinates of the corresponding lower dimensional vector $x$. *See equation 5-9 form towardsdatascience link*

The ultimate benefit of th ekernel trick is that the [[objective function]] we are optimizing to fit the higher dimensional decision boundary only includees the dot product of the transformed feature vectors. Therefore, we can just substitute these [[dot product]] terms witht he kernel function, and we done't even need to know anything about $\phi(x)$. *See towardsdatascience link at the bottom and wikipedia article for SVM*

###### Properties:
- There are a multitude of different nonlinear kernels that can be used with the kernel trick, with the best kernel depending on the input data.

###### Additional Thoughts:
