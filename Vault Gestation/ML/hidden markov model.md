name : hidden markov model
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Hidden_Markov_model

###### Content:
A hidden markov model (HMM)  attempts to model a system which is assumed to be a [[markov chain]] $X$ with unobservable ("hidden") states. As part of the definition, HMM requires that there be an observable process $Y$ whose outcomes are "influenced" by the outcomes of $X$ in a known way. Since $X$ cannot be observed directly, the goal is to learn about $X$ by observing $Y$. HMM has an additional requirement that the outcome of $Y$ at time $t=t_0$ must be "influenced" exclusively by the outcome of $X$ at $t=t_0$ and that the outcomes of $X$ and $Y$ at $t < t_0$ must not affect the outcome of $Y$ at $t=t_0$

**Example:**
In a room that is not visible to an observer there is a genie. The room contains urns $X1, X2, X3, ..$. each of which contains a known mix of balls labeled $y1, y2, y3, ...$. The genie chooses an urn in that room and randomly draws a ball from that urn and puts the ball onto a conveyor belt, where the observer can observe the sequence of the balls but not the sequence of urns from which they were drawn. The genie has some procedure to choose urns; the choice of the urn for the _n_-th ball depends only upon a random number and the choice of the urn for the (_n_ − 1)-th ball. The choice of urn does not directly depend on the urns chosen before this single previous urn; therefore, this is called a [[markov chain]]. It can be described by figure below.

The Markov process itself cannot be observed, only the sequence of labeled balls, thus this arrangement is called a "hidden Markov process". Even if the observer knows the composition of the urns and has just observed a sequence of three balls, _e.g._ y1, y2 and y3 on the conveyor belt, the observer still cannot be _sure_ which urn (_i.e._, at which state) the genie has drawn the third ball from. However, the observer can work out other information, such as the likelihood that the third ball came from each of the urns.

![[Pasted image 20220603142702.png]]

**Training:**
The parameter learning task in HMMs is to find, given an output sequence or a set of such sequences, the best set of state transitions ($a_i$ in the model above) and emission probabilities (observable outputs, or the $b_i$ in the model above). This task is usually to derive the [[maximum likelihood estimation]] of the parameters of the HMM given the set of output sequences. This can be done efficiently using the [[Baum-Weich algorithm]].
If the HMMs are used for time series prediction, more sophisticated Bayesian inference methods, like [[Markov chain Monte Carlo]] sampling are proven to be favorable over finding a single maximum likelihood model both in terms of accuracy and stability.

###### Properties:


###### Additional Thoughts:
