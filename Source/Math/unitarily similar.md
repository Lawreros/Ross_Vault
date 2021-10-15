name : unitarily similar
tags : 
backlinks : 
source : #MASED 

###### Content:
Let $A, B \in M_n$ be given. We say that $A$ is unitarily similar to $B$ if there is a [[unitary matrix]] $U \in M_n$ such that $A = UBU^*$. If $U$ may be taken to be real (and hence [[real orthogonal]]), then $A$ is said to be real orthogonally [[similar]] to $B$. 

###### Properties:
- We say that $A$ is [[unitarily diagonalizable]] if it is unitarily similar to a diagonal matrix; $A$ is real orthogonally diagonalizable if it is real orthogonally similar to a [[diagonal matrix]].
- Let $U \in M_n$ and $V \in M_m$ be [[unitary]], let $A = [a_{ij}]\in M_{n,m}$ and $B = [b_{ij}] \in M_{n,m}$, and suppose that $A = UBV$. Then $\sum_{i,j=1}^{n,m}|b_{ij}|^2 = \sum_{i,j=1}^{n,m}|a_{ij}|^2$. In particular, this identity is satisfied if $m=n$ and $V = U^*$, that is, if $A$ is unitarily similar to $B$.
- Two matrices $A,B \in M_n$ are unitarily similar if and only if $$trW(A,A^*)=trW(B,B^*)$$ for every word $W(s,t)$ in two noncommuting variables. ([[trace]])


###### Additional Thoughts:
- Unitary similarity, like similarity, corresponds to a change of basis, but of a special type - it corresponds to a change from one [[orthonormal basis]] to another.