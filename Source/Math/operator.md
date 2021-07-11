name : operator
tags : 
backlinks : 
source : #LADR

###### Content:
A [[linear map]] from a [[vector space]] to itself is called an operator. The notation $\mathcal{L}(V)$ denotes the set of all operators on $V$. In other words, $\mathcal{L}(V)=\mathcal{L}(V,V)$.

###### Properties:
- Suppose $V$ is a [[finite-dimensional vector space]] and $T \in \mathcal{L}(V)$. Then the following are equivalent:
		- $T$ is [[invertible]]
		- $T$ is [[injective]]
		- $T$ is [[surjective]]

- Operators on [[complex vector space]]s have an [[eigenvalue]]. Every operator on a finite-dimensional, nonzero, complex vector space has an eigenvalue. (This may not be true for non-complex vector spaces, think rotation)

- Over $\textbf{C}$, every operator has an [[upper-triangular matrix]]. Suppose $V$ is a finite-dimensional complex vector space and $T \in \mathcal{L}(V)$. Then $T$ has an [[upper-triangular matrix]] with respect to some [[basis]] of $V$

- Suppose $T \in \mathcal{L}(V)$ and *m* is a positive integer
		- $T^m = T*...*T$ (m times)
		- $T^mT^n = T^{m+n}$ and $(T^m)^n = T^{mn}$
		- $T^0$ is defined to be the [[identity operator]] $I$ on $V$
		- If $T$ is [[invertible]] with inverse $T^{-1}$, then $T^{-m}$ is defined by $T^{-m} = (T^{-1})^m$

- Suppose $T \in \mathcal{L}(V)$ and $p \in \mathcal{P}(\textbf(F))$ is a [[polynomial]] given by $p(z) = a_0+a_1z+a_2z^2+...+a_mz^m$ for $z \in \textbf{F}$. Then $p(T)$ is the operator defined by $p(T) = a_0I+a_1T + a_2T^2+...+a_mT^m$

###### Additional Thoughts:
