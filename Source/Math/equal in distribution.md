name : equal in distribution
tags : 
backlinks : 
source : Intro to Prob, https://en.wikipedia.org/wiki/Random_variable#:~:text=Equality%20in%20distribution,-If%20the%20sample&text=To%20be%20equal%20in%20distribution,functions%20have%20the%20same%20distribution.

###### Content:
Random variables $X$ and $Y$ are equal in distribution if $P(X \in B) = P(Y \in B)$ for all [[subset]]s $B$ of $\mathbb{R}$. This is abbreviated by $X \overset{d}{=} Y$.

In other words, multiple [[random variable]]s can be defined on different [[sample space]]s, but still essentially the same in terms of probabilities.

**Example:**
The following random variables from different sample spaces are equal in distribution:
$$X = \begin{cases}
1 & \text{if a fair coin flip is heads} \\
0 & \text{if a fair coin flip is tails}
\end{cases}$$
$$Y = \begin{cases}
1 & \text{if a roll of a fair die is even} \\
0 & \text{if a roll of a fair die is odd}
\end{cases}$$
$$Z = \begin{cases}
1 & \text{if a card dealt from a deck is spades or clubs} \\
0 & \text{if a card dealt from a deck is hearts or diamonds}
\end{cases}$$

###### Properties:
- If two [[discrete random variable]]s $X$ and $Y$ have the same [[probability mass function]], then $X \overset{d}{=} Y$. Similarly if two [[continuous random variable]]s have the same [[probability density function]] then $X \overset{d}{=} Y$

###### Additional Thoughts:
