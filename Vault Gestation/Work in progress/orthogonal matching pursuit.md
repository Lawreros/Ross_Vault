name : orthogonal matching pursuit
tags : 
backlinks : 
source : 

###### Content:


***Pseudocode***
**Data:** Dictionary $A$, signal $b$ and target cardinality $k$
**Initialization:** set residual $r^0=b$, estimate $\hat x= 0$, and its [[support]] $\mathcal{S}=supp(\hat x^0) = \emptyset$

---
for $i=1,...,k$ do
		a) Find next "best" [[atom]] to approximate the residual: $$j^* = \underset{j}{argmin} \underset{z_j}{min} - r^{i-1}||_2^2 = \underset{j}{argmax} \left| \frac{A_j^Tr^{i-1}}{||A_j||^2_2} \right|$$
		b) Update support: $\mathcal{S} \leftarrow \mathcal{S} \cup \{j^*\}$
		c) Update solution: $\hat x_{\mathcal{S}} = \underset{x_\mathcal{S}}{argmin}||A_\mathcal{S}\hat x_\mathcal{S} - b||_2^2$
		d) Update residual: $r^i = b-A\hat x$
end
---
###### Properties:
Unique relationships/properties

###### Additional Thoughts:
