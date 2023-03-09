name : markov chain (markov process)
tags : 
backlinks : [[conditional probability]]
source : Intro to Prob, https://en.wikipedia.org/wiki/Markov_chain

###### Content:
A markov chain (or markov process) is a [[stochastic process]] describing a sequence of possible events in which the probability of each event depends only on the state attained in a previous event.
*Think of the Random Walks problem, where you repeatedly randomly either take a step to the right or the left. Where you end up at the end of each step only depends on where you ended up after the previous step.*

Let $X_0,X_1,X_2,...$ be a [[stochastic process]] of [[discrete random variable]]s. This process is a Markov chain if:
$$P(X_{n+1}=x_{n+1}|X_0=x_0,X_1=x_1,...,X_n=x_n) = P(X_{n+1}=x_{n+1}|X_n=x_n)$$
for all $n \geq 0$ and all $x_0,...,x_n$ such that $P(X_0=x_0,X_1,x_1,...,X_n=x_n)>0$

*"An intuitive explanation for this is the following: in order to compute the conditional distribution for the location of the walk at step $n+1$, it is sufficient to know the location at step $n$ and the rest of the past is irrelevant"*


###### Properties:
- A sequence of [[independent]] [[random variable]]s is an example of a Markov chain because both sides of the above equation reduce to $P(X_{n+1}=x_{n+1})$
- The random walk i also a markov chain

###### Additional Thoughts:
