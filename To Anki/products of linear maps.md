name : products of [[linear map]]s
tags : 
backlinks : 
source : [[Linear Algebra Done Right]]

###### Content:
If $T \in \mathcal{L}(U,V)$ and $S \in \mathcal{L}(V,W)$, then the product $ST \in \mathcal{L}(U,W)$ is defined by: $$(ST)(u)=S(Tu)$$ for $u \in U$.

###### Properties:
- [[associativity]] $$(T_1T_2)T_3 = T_1(T_2T_3)$$ whenever $T_1,T_2,T_3$ are linear maps such that the products make sense ($T_3$ maps into the domain of $T_2$ and $T_2$ maps into the domain of $T_1$)
- **identity** $$TI = IT=T$$ whenever $T \in \mathcal{L}(U,V)$ (the first $I$ is the [[identity map]] on $V$, and the second $I$ is the identity map on $W$).
- [[distributive property]] $$(S_1 +S_2)T = S_1T+S_2T$$ and $$S(T_1+T_2)=ST_1+ST_2$$ whenever $T,T_1,T_2\in \mathcal{L}(U,V)$ and $S,S_1,S_2 \in \mathcal{L}(V,W)$.
- Multiplicative of linear maps is not commutative ($ST$ doesn't always equal $TS$,[[commutativity]])

###### Additional Thoughts:
