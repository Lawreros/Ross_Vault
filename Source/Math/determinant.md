name : determinant, det $A$
tags : 
backlinks : 
source : #MASED 

###### Content:
The determinant is a scalar value that is a function of the entries of a [[square matrix]], used to summarize the information in a matrix.

$$det[a_{11}]=a_{11}$$
$$det \begin{bmatrix}
a_{11} & a_{12}\\
a_{21} & a_{22}
\end{bmatrix}
=a_{11}a_{22}-a_{12}a_{21}$$
$$det \begin{bmatrix}
a_{11} & a_{12} & a_{13}\\
a_{21} & a_{22} & a_{23}\\
a_{31} & a_{32} & a_{33}
\end{bmatrix}=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}-a_{13}a_{22}a_{31}$$


This can be expanded as an equation through [[Laplace expansion]]

###### Properties:
- If $A$ has a row of zeros, then the determinant is zero
- det $A^T=$ det $A$ if $A \in M_n(\textbf{C})$ ([[transpose]])
- det $A^*= \overline{detA}$ if $A \in M_n(\textbf{C})$ ([[conjugate transpose]])
- det $AB$ = det $A$ det $B$

###### Additional Thoughts:
