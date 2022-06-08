name : poisson process
tags : 
backlinks : 
source : Intro to Probability, https://www.mygreatlearning.com/blog/gamma-distribution/

###### Content:
The Poisson process with intensity, or rate, $\lambda >0$ is a collection of random points on the positive half-line $[0,\infty)$ with the following properties:
- The points are distinct (that is, there cannot be more than one point at any given position on $[0,\infty)$)
- The number of points in a bounded interval $I \subset [0,\infty)$, which is denoted by $N(I)$, has [[poisson distribution]] with parameter $\lambda \cdot |I|$. For example, if $I = [a,b]$ then $N(I) \sim Poisson(\lambda(b-a))$.
- If $I_1,I_2,...,I_n$ are nonoverlapping intervals in $[0,\infty)$ then the [[random variable]]s $N(I_1), N(I_2),...,N(I_n)$ are mutually [[independent]].

###### Properties:
- The poisson process is a [[stochastic process]]
- The [[gamma distribution]], [[poisson distribution]], and [[exponential distribution]] models are all different aspects of the same process - the Poisson process.
		- Poisson distribution is used to model the number of events in the future
		- Exponential distribution is used to predict the wait time until the very first event occurs
		- The gamma distribution is used to predict the wait time until the $k$-th even occurs


**Spatial Poisson process:**
The Poisson process can be generalized to higher [[dimension]]al Euclidean spaces. Thus Poisson process can be used to model events that happen in multi-dimensional space. The definition is basically the same as before, but instead of measuring the size of a set with length, we use the measure appropriate to the space we work in. Let the integer $d$ be the dimension of the space. For a subset $A \subseteq \mathbb{R}^d$, let $|A|$ denote its **generalized volume**. By this we mean length if $d=1$, area if $d=2$, ordinary volume if $d=3$ and for $d>3$ the natural generalization that gives a $d$-dimensional rectangle $A = [a_1,b_1]\times [a_2,b_2] \times ... \times [a_d,b_d]$ the volume $|A| = \prod_{i=1}^d(b_i-a_i)$

The Poisson process with intensity $\lambda >0$ on $\mathbb{R}^d$ is a collection of random points in $\mathbb{R}^d$ with the following properties:
- The points are all distinct. That is ,there cannot be more than one point at any particular location
- The number of points in a set $A$ is denoted by $N(A)$. This [[random variable]] has [[poisson distribution]] with parameter $\lambda |A|$, for sets $A$ such that the volume $|A|$ is well defined and finite.
- If $A_1,A_2,...,A_n$ are nonoverlapping sets of finite volume then the random variables $N(A_1),N(A_2),...,N(A_n)$ are mutually [[independent]]


###### Additional Thoughts:
