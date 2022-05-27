name : indicator random variable
tags : 
backlinks : 
source : Intro to Probability

###### Content:
An indicator [[random variable]] $I_A$ is defined for $\omega \in \Omega$ ([[sample space]]) by:
$$I_A(\omega) = \begin{cases}
1 & \omega \in A \\
0 & \omega \notin A
\end{cases}$$
In plain English, $I_A$ records whether the event $A$ happens or not. Since the event $\{I_A = 1\}$ is the same as the event $A$, $P(I_A = 1) = P(A)$ and we see that $I_A$ is a random variable with [[Bernoulli distribution]] with parameter $P(A)$.

###### Properties:
- [[expectation]]: $E(I_A) = P(A)$

###### Additional Thoughts:
