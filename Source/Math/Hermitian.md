name : Hermitian
tags : 
backlinks : [[matrix]], [[conjugate transpose]]
source : #MASED 

###### Content:
 $A \in M_{n}(\textbf{F})$ is said to be Hermitian if $A^* = A$

###### Properties:
Some observations for $A,B \in M_n$:
- $A+A^*$,$AA^*$, and $A^*A$ are Hermitian
- If $A$ is Hermitian, then $A^k$ is Hermitian for all $k=1,2,3,...$ . If $A$ is [[nonsingular]] as well, then $A^{-1}$ is Hermitian
- If $A$ and $B$ are Hermitian, then $aA+bB$ is Hermitian for all real scalars $a,b$
- $A-A^*$ is [[skew Hermitian]]
- If $A$ and $B$ are [[skew Hermitian]], then $aA+bB$ is skew Hermitian for all scalars $a,b$
- If $A$ is Hermitian, then $iA$ is Hermitian
- $A = \frac{1}{2}(A+A^*)+\frac{1}{2}(A-A^*)=H(A)+iK(A)$, in which $H(A)=\frac{1}{2}(A+A^*)$ is the Hermitian part of $A$, $S(A)=\frac{1}{2}(A-A^*)$ is the [[skew Hermitian]] part of $A$, and $K(A)=\frac{1}{2i}(A-A^*)$
- If $A$ is Hermitian, the main [[diagonal]] entries of $A$ are all real. To specify the $n^2$ elements of $A$, one may choose freely any $n$ real numbers (for the main diagonal entries) and any $\frac{1}{2}n(n-1)$ [[complex numbers]] (for the off-diagonal entries)
- If we write $A = C+iD$ with $C,D \in M_n(R)$ (real and imaginary parts of $A$), then $A$ is Hermitian if and only if $C$ is [[symmetric]] and $D$ is skew symmetric
- A real [[symmetric]] matrix is a complex Hermitian matrix
- Every Hermitian is [[normal]]
- A vector consisting of the [[diagonal]] entries of $A$ [[majorize]]s a vector consisting of the [[eigenvalue]]s of $A$: 
$Diag(A) = \begin{bmatrix} a_{11} \\ a_{22} \\ ... \\ a_{nn}\end{bmatrix}$ majorizes $\lambda(A) = \begin{bmatrix} \lambda_{1} \\ \lambda_{2} \\ ... \\ \lambda_{n}\end{bmatrix}$
- The vector $\lambda(A+B) = \begin{bmatrix} \lambda_1(A+B) \\ \lambda_2(A+B) \\ \vdots \\ \lambda_n(A+B)\end{bmatrix}$ [[majorize]]s the vector $\lambda(A)+\lambda(B) = \begin{bmatrix} \lambda_1(A)+\lambda_1(B) \\ \lambda_2(A)+\lambda_2(B) \\ \vdots \\ \lambda_n(A)+\lambda_n(B)\end{bmatrix}$

- **Spectral Theorem for Hermitian Matrices:** $A \in M_n$ is Hermitian if and only if $A$ is [[unitarily diagonalizable]] and [[eigenvalue]]s of $A$ are all real.


###### Additional Thoughts:
