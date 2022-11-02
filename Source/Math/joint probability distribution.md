name : joint probability distribution
tags : 
backlinks : 
source : Intro to Prob

###### Content:
The [[probability distribution]] of a [[random vector]] is called a joint distribution. A joint probability distribution can be described by a [[joint probability mass function]] in the discrete case, by a [[joint probability density function]] in the continuous case, and in general one can define a [[joint cumulative distribution function]]

**Example:**
Consider the flip of two fair coins; let $A$ and $B$ be [[discrete random variable]]s associated with the outcomes of the first and second coin flips respectively. Each coin flip has a [[Bernoulli distribution]]. If the coin displays "heads" then the associated random variable takes the value $1$ and it takes $0$ otherwise. The probability of each of these outcomes is $0.5$ so the [[joint probability mass function]] of $A$ and $B$ defines the probabilities for each pair of outcomes:
$$(A=0, B=0),(A=0,B=1),(A=1,B=0),(A=1,B=1)$$
Since each outcome is equally likely the joint probability mass function becomes: $$P(A,B) = 1/4 \text{ for } A,B\in \{0,1\}$$
Since the coin flips are independent, the joint probability mass function is the product of the marginals: $$P(A,B) = P(A)P(B)$$

###### Properties:


###### Additional Thoughts:
