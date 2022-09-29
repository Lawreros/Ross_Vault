name : trilinear interpolation
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Trilinear_interpolation

###### Content:
A method for interpolating the value of a point between known points in 3D space.
![[Pasted image 20210921114013.png]]

To find the value of point $C$, first we interpolate along $x$, giving:
$$c_{00} = c_{000}(1-x_d)+c_{100}x_d$$
$$c_{01} = c_{001}(1-x_d)+c_{101}x_d$$
$$c_{10} = c_{010}(1-x_d)+c_{110}x_d$$
$$c_{11} = c_{011}(1-x_d)+c_{111}x_d$$
Where $c_{000}$ means the function value of $(x_0,y_0,z_0)$. Then we interpolate these values along $y$, giving:
$$c_{0} = c_{00}(1-y_d)+c_{10}y_d$$
$$c_{1} = c_{01}(1-y_d)+c_{11}y_d$$
Finally we interpolate these values along $z$
$$c = c_0(1-z_d)+c_1z_d$$

###### Properties:
- The order of axes you interpolate across doesn't matter
- An alternative way to write the solution to the interpolation problem is: $$f(x,y,z) \approx a_0+a_1x+a_2y+a_3z+a_4xy+a_5xz+a_6yz+a_7xyz$$ where the coefficients are found by solving the following linear system: $$\begin{bmatrix}
1 & x_0 & y_0 & z_0 & x_0y_0 & x_0z_0 & y_0z_0 & x_0y_0z_0 \\
1 & x_1 & y_0 & z_0 & x_1y_0 & x_1z_0 & y_0z_0 & x_1y_0z_0 \\
1 & x_0 & y_1 & z_0 & x_0y_1 & x_0z_0 & y_1z_0 & x_0y_1z_0 \\
1 & x_1 & y_1 & z_0 & x_1y_1 & x_1z_0 & y_1z_0 & x_1y_1z_0 \\
1 & x_0 & y_0 & z_1 & x_0y_0 & x_0z_1 & y_0z_1 & x_0y_0z_1 \\
1 & x_1 & y_0 & z_1 & x_1y_0 & x_1z_1 & y_0z_1 & x_1y_0z_1 \\
1 & x_0 & y_1 & z_1 & x_0y_1 & x_0z_1 & y_1z_1 & x_0y_1z_1 \\
1 & x_1 & y_1 & z_1 & x_1y_1 & x_1z_1 & y_1z_1 & x_1y_1z_1 \\
 \end{bmatrix}\begin{bmatrix}
 a_0 \\ a_1\\ a_2 \\ a_3\\ a_4 \\ a_5\\ a_6 \\ a_7\\
 \end{bmatrix} = \begin{bmatrix}
 c_{000} \\ c_{100} \\ c_{010} \\c_{110} \\c_{001} \\c_{101} \\c_{011} \\ c_{111} \\
 \end{bmatrix}$$

###### Additional Thoughts:
