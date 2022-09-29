name : nonlinear SVM
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Support-vector_machine,
https://towardsdatascience.com/the-kernel-trick-c98cdbcaeb3f

###### Content:
Nonlinear SVM models are used if the data is not [[linearly separable]] in the input space. This is done by applying transformations to the data, which map the data from the original space into a higher [[dimension]]al feature space. The goal is that after the transformation to the higher dimensional space, the class are now linearly separable in this higher dimensional feature space (and is thus found similar to [[linear SVM]]).

For example, in 1-dimension, the data below is not linearly separable, but after applying the transformation $\phi(x) = x^2$ and adding this second dimension to our feature space, the classes become linearly separable.
![[Pasted image 20220602135022.png]]

These transformations of the original data to higher dimensions are just functions, and there are many possible functions that can map the data to any number of higher dimensions. However, **not all of these functions are actually kernels**, the kernel function has a special property that makes it particularly useful in training [[support vector machine]] models, and the use of this property in optimizing nonlinear SVMs is often called the [[kernel trick]].


###### Properties:


###### Additional Thoughts:
