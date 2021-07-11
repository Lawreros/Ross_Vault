name : inner product
tags : 
backlinks : 
source : #LADR 

###### Content:
An inner product on $V$ is a function that takes each ordered pair $(u,v)$ of elements of $V$ to a number $\langle u, v \rangle \in \textbf{F}$ and has the following properties:

**positivity**
$\langle v,v \rangle \geq 0$ for all $v \in V$

**definiteness**
$\langle v,v \rangle = 0$ if an only if $v = 0$

**additivity in first slot**
$\langle u +v, w\rangle = \langle u,w\rangle +\langle v,w \rangle$ for all $u,v,w \in V$

**homogeneity in first slot**
$\langle \lambda u, v\rangle = \lambda \langle u,v \rangle$ for all $\lambda \in \textbf{F}$ and all $u,v \in V$

**[[complex conjugate]] symmetry**
$\langle u,v \rangle = \overline{\langle v,u\rangle}$ for all $u,v \in V$

###### Properties:
- The [[dot product]] is an inner product
- Suppose V is an [[inner product space]] over $\textbf{F}$: 
		- For each fixed $u \in V$, the function that takes $v$ to $\langle v, u \rangle$ is a [[linear map]] from $V$ to $\textbf{F}$
		- $\langle u, 0 \rangle = 0$ for every $u \in V$
		- $\langle 0,u \rangle = 0$ for every $u \in V$
		- $\langle u, v+w \rangle = \langle u, v \rangle +\langle u, w \rangle$ for all $u,v,w \in V$
		- $\langle u, \lambda v\rangle = \bar \lambda \langle u, v \rangle$ for all $\lambda \in \textbf{F}$ and $u,v, \in V$

###### Additional Thoughts:
