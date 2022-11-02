name : p-value
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/P-value

###### Content:
In [[null hypothesis]] testing, the p-value is the probability of obtaining test results as extreme as the result actually observed, under the assumption that the null hypothesis is correct. A very small p-value means that such an extreme observed outcome would be very unlikely under the null hypothesis.

The p-value is widely used in statistical hypothesis testing, specifically in null hypothesis significance testing. In this method, before conducting the study, one first chooses a model (the null hypothesis) and the alpha level $\alpha$ (most commonly .05). After analyzing the data, if the p-value is less than $\alpha$, that is taken to mean that the observed data is sufficiently inconsistent with the null hypothesis for the null hypothesis to be rejected. However, that does not prove that the null hypothesis is false. The p-value does not, in itself, establish probabilities of hypotheses. Rather, it is a tool for deciding whether to reject the null hypothesis.

p-values are often misused, since the precise meaning of a p-value is dependent upon the null hypothesis it is testing. For example if a null hypothesis states that a certain summary statistic $T$ follows the [[standard normal distribution]] $N(0,1)$, then the rejection of this null hypothesis could mean that 
a) the mean of $T$ is not 0, or 
b) the [[variance]] of $T$ is not 1, or 
c) $T$ does not have a [[normal distribution]]
Different tests of the same null hypothesis would be more or less sensitive to different alternatives. However, even if we do manage to reject the null hypothesis for all 3 alternatives, and even if we know the distribution is normal and variance is 1, the null hypothesis test does not tell us which non-zero values of the mean are now most plausible. 

###### Properties:
- The p-value is a function of the chosen test statistic $T$ and is therefore a [[random variable]]. If the [[null hypothesis]] fixes the [[probability distribution]] of $T$ precisely, and if the distribution is continuous, then when the null hypothesis is true, the p-value has [[uniform distribution]] between 0 and 1. Thus, the p-value is not fixed. If the same test is repeated independently with fresh data, one will typically obtain a different p-value in each iteration. If the null-hypothesis is composite, or the distribution of the statistic is discrete, the probability of obtaining a p-value less than or equal to any number between 0 and 1 is less than or equal to that number, if the null-hypothesis is true.

###### Additional Thoughts:
