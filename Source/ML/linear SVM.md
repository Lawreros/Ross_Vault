name : linear SVM
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Support-vector_machine

###### Content:
The [[linear classifier]] version of [[support vector machine]]s, the linear SVM is used on [[linearly separable]] (or almost) datasets. For data sets which are not linearly separable, [[nonlinear SVM]] is used.

Let a training dataset of $n$ points take the form of:
$$(x_1, y_1),...,(x_n,y_n)$$
where the $y_i$ are either 1 or -1, each indicating the class to which the point $x_i \in \mathbb{R}^d$ belongs. We want to find the [[hyperplane]] that divides the group of points $x_i$ for which $y_i=1$ from the group where $y_i=-1$. Any hyperplane can be written as a set of points $x$ satisfying $$w^Tx-b=0$$ where $w$ is the [[normal vector]] to the hyperplane. The parameter $\frac{2}{||w||}$ determines the offset of the hyperplane from the origin along the normal vector $w$.

There are two main categories for linear SVMs:

**Hard Margin**
If the training data is [[linearly separable]], two parallel [[hyperplane]]s that separate the two classes of data can be selected which are as far apart as possible. The region bounded by these two hyperplanes is called the "margin", and the optimal hyperplane lies halfway between the two planes (called the **maximum-margin hyperplane**).

![[Pasted image 20220602125045.png]]

Geometrically, the distance between the two hyperplanes is $\frac{2}{||w||}$, so to maximize the distance between the planes Thus, 
$$w^Tx_i -b \geq 1$$ if $y_i = 1$, and $$w^Tx_i -b \leq 1$$ if $y_i = -1$
These constraints state that each data point must lie on the correct side of the margin. This can be rewritten as $$y_i(w^Tx_i-b)\geq 1$$
for all $1\leq i \leq n$. This makes the optimization problem: "Minimize $||w||$ subject to $y_i(w^Tx_i-b)\geq 1$ for all $i=1,...,n$"
The $w$ and $b$ that solve this problem determine our classifier, $y = sgn(w^Tx-b)$. An important consequence of this geometric description is that the two hyperplanes that make the margin are determined by the closest $x_i$, which are called **support vectors**

**Soft Margin**
To extend SVM to cases in which the data is not linearly separable, the hinge loss function is helpful:
$$max(0, 1-y_i(w^Tx_i-b))$$
This function is zero if $x_i$ lies on the correct side of the margin. For data on the wrong side of the margin, the function's value is proportional to the distance from the margin. Thus, the goal of the optimization is to minimize:
$$[\frac{1}{n} \sum_{i=1}^{n}max(0,1-y_i(w^Tx_i-b))]+\lambda ||w||^2$$
Where the parameter $\lambda > 0$ determines the trade-off between increasing the margin size and ensuring that $x_i$ lies on the correct size of the margin.

###### Computing the SVM Classifier
Computing the soft-margin SVM classifier amounts to minimizing the expression:
$$f(w,b) = [\frac{1}{n} \sum_{i=1}^{n}max(0,1-y_i(w^Tx_i-b))]+\lambda ||w||^2$$
Then, because $f$ is a [[convex function]] of $w$ and $b$, [[subgradient descent]] method can be used. *This also applies to hard margin classifiers by just making $\lambda$ sufficiently small.*

###### Properties:


###### Additional Thoughts:
