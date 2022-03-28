name : normed linear space
tags : 
backlinks : 
source : 

###### Content:
A normed linear space is a pair $(V, ||\cdot||)$ where $v$ is a [[vector space]] and $||\cdot||:V \rightarrow[0,\infty)]$ is a norm (either [[vector norm]] or [[matrix norm]]) on $V$.

###### Properties:
- http://mathonline.wikidot.com/normed-linear-spaces
- If $V, ||\cdot||$ is a finite dimensional NLS, then it is complete.
- Let $V, ||\cdot||$ be a NLS. The following are equivalent:
		- $V$ is finite dimensional
		- The unit ball $\{x \in V: ||x|| \leq 1\}$ is compact
		- Unit sphere $\{x \in V: ||x|| = 1\}$ is compact
		- $\forall \mathcal{S} \subseteq V$, $\mathcal{S}$ is compact if and only if $\mathcal{S}$ is closed and bounded
- Let $V$ (over $\mathcal{K}$) be finite dimansional. All norms are "equivalent", i.e. for any norms $||\cdot||$, $||\cdot||'$ in $V$ there exists some $m,M \in \mathbb{R}_{>0}$ such that $\forall x \in V$ $$m ||x||' \leq ||x|| \leq M||x||'$$ $$\frac{1}{m}||x|| \leq ||x||' \leq \frac{1}{m}||x||$$ Thus the two norms "converge" the same and have the same "topologies" (all you need to know is that the rules for any norm is consistent for all norms)

###### Additional Thoughts:
