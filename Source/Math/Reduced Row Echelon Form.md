name : Reduced Row Echelon Form, Hermite normal form
tags : 
backlinks : 
source : #MASED 

###### Content:
To each $A = [a_{ij}] \in M_{m,n}(\textbf{F})$ there corresponds a (unique) canonical form in $M_{m,n}(\textbf{F})$ that can be reached through elementary row and column operations. If a row of $A$ is nonzero, its leading entry is its first nonzero entry. The defining specifications of the RREF are as follows:
- Any zero rows occur at the bottom of the matrix
- The leading entry of any nonzero row is a 1
- All other entries in the column of a leading entry are zero
- The leading entries occur in a stairstep pattern, left to right; that is, if row $i$ is nonzero and $a_{ik}$ is its leading entry, then either $i=m$, or row $i+1$ is zero, or the leading entry in row $i+1$ is $a_{i+1,l}$ in which $l >k$

###### Properties:
- If $R \in M_{m,n}(\textbf{F})$ is the RREF of $A$, then $R=EA$, in which the nonsingular matrix $E\in M_n(\textbf{F})$ is a product of the elementary row operations required to reduce $A$ to RREF
- The [[determinant]] of $A$ is nonzero if an only if its RREF is the identity matrix. The value of $det A$ may be calculated by recording the effects on the determinant of each of the elementary operations that lead to the RREF
- Since the RREF is unique, for given $A_1, A_2 \in M_{m,n}$ and given $b_1,b_2 \in \textbf{F}^m$, consistent systems of linear equations $A_1x = b_1$ and $A_2x = b_2$ have the same set of solutions if and only if $[A_1 b_1]$ and $[A_2 b_2]$ have the same RREF

###### Additional Thoughts:
