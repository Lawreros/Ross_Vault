name : matrix norm
tags : 
backlinks : 
source : Matrix Analysis

###### Content:
A [[norm]] on $M_n(\mathcal{K})$ is a matrix norm if, for all $A,B \in M_n(\mathcal{K})$ the following is true:
- $||A||>0$ if $A \neq 0$  (positivity)
- $||cA|| = |c|||A||$ (homogeneity)
- $||A+B|| \leq ||A||+||B||$ (subadditivity)
- $||AB|| \leq ||A||||B||$ (submultiplicativity)


**Examples:**
- L1 norm on $M_n(\mathcal{K})$: $||A||_1 = max_j \sum_{i}^n |a_{i,j}|$
- L2 norm (or [[Frobenius norm]]) on $M_n(\mathcal{K})$: $||A||_2 = ||A||_F = \sqrt{\sum_{i,j}^n |a_{i,j}|^2}$
- L-infinity norm is NOT a matrix norm as it fails submultiplicativity

###### Properties:
- If a norm fails the follow the submultiplicativity rule, then it is called a "vector norm on matrices"
- If $\mathcal{K}^n,||\cdot||'$ is a [[normed linear space]], matrices $M_n(\mathcal{K})$ are thought of as functions $\mathcal{K}^n,||\cdot||' \rightarrow \mathcal{K}^n,||\cdot||'$, then the [[operator norm]] $||\cdot||_{||\cdot||',||\cdot||'}$ is a matrix norm called an [[induced matrix norm]]
- Let $||\cdot||$ be a matrix norm on $M_n$, and let $S \in M_n$ be [[invertible]]. Then for all $A\in M_n$ the norm defined as $||A||_S:=||S^{-1}AS||$ is a matrix norm.
- Let $A \in M_n$ be given, and let $\epsilon > 0$ be a given scalar. There exists a matrix norm $||\cdot||$ on $M_n$ such that $||A|| \leq \rho (A)+\epsilon$ ([[spectral radius]])
- Let $B \in M_n,||\cdot||$ be a matrix norm on $M_n$ such that $||B|| <1$. Then $I-B$ is [[invertible]] and $(I-B)^{-1} = \sum_{i=1}^\infty B^i$
- If $B \in M_n, \rho(B) <1$ then $I-B$ is [[invertible]] and $(I-B)^{-1} = \sum_{i=0}^\infty B^i$ since there exists a matrix norm $||\cdot||$ such that $||B||<1$
- Let $A \in M_n, ||\cdot||$ be a matrix norm on $M_n$ such that $||I_A||<1$. Then $A$ is invertible and $A^{-1} = \sum_{i=0}^\infty$

###### Additional Thoughts:
