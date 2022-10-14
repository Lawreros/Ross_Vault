name : t-test
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Student%27s_t-test, https://www.investopedia.com/terms/t/t-test.asp, https://www.scribbr.com/statistics/t-test/#:~:text=A%20t%2Dtest%20is%20a%20statistical%20test%20that%20compares%20the,means%20is%20different%20from%20zero.

###### Content:
A t-test is an inferential statistic used to determine if there is a significant difference between the means of ***two*** groups and how they are related. T-tests are used when the data sets follow a [[normal distribution]] and have unknown [[variance]]s. The t-test questions whether the difference between the groups represents a true difference in the study or merely a random difference. The [[null hypothesis]] for the t-test is that the true difference between the group means is zero, with the [[alternate hypothesis]] is that the true difference is not zero.

Calculating a t-test requires three fundamental data values. They include the difference between the mean values from each data set, or the mean difference, the [[standard deviation]] of each group, and the number of data values of each group.

Four assumptions are made while using a t-test:
1. The data collected must follow a continuous or ordinal scale, such as the scores for an IQ test
2. The data is collected from a randomly selected portion of the total population
3. The data will result in a [[normal distribution]] of a bell-shaped curve
4. Equal or homogeneous [[variance]] exists when the [[standard deviation]]s are equal

The t-test produces two values as its output: the [[t-value]] and [[degrees of freedom]]. In the context of the t-test, the degrees of freedom refer to the values in a study that have the freedom to vary and are essential for assessing the importance and validity of the null hypothesis. Computation of these values usually depends on the number of data records available in the sample set.

The [[t-value]] and [[degrees of freedom]] are used in conjunction with a table of values from the [[Student's t-distribution]] to get a [[p-value]] (which depends on whether you are performing [[one-tailed t-test]] or [[two-tailed t-test]]) for [[statistical significance]].

##### Conceptual Explanation?
In order to understand what the results of a t-test are actually telling you, here is a general explanation:
- Imagine two samples of values, $X$ and $Y$, each having a [[normal distribution]]. $\bar X - \bar Y = r$
- $Q = (X-Y)$ also results in a normal distribution
- Because $Q$ is normally distributed, it can be used to calculated the percentile of the value $r$. If you standardize $Q$ in some way, this relation ship gives you the probability that the null hypothesis ($\bar X_0- \bar Y_0 = 0$, where $X_0$ is the population $X$ is a sample of, same for $Y_0$) is correct given the observed value $r$
- The t-value equations unique to each type to t-test and the degrees of freedom are effectively the parameters fed into the student's t-distribution to do this probability calculation
- Confidence intervals come from $Q$. For example, the 95% confidence interval determines that there is a 95% chance the $(\bar X_0-\bar Y_0)$ falls somewhere in range $[a,b]$

##### **What type of t-test should I use?**
When choosing a t-test, you will need to consider two things: whether the groups being compared come from a single population or two different populations, and whether you want to test the difference in a specific direction.
**One-sample, two-sample, or paired t-test?:**
- If the groups come from a single population (e.g. measuring before and after an experimental treatment), perform a [[paired t-test]]
- If the groups come from two different populations (e.g. two different species, or people from two separate cities), perform a [[two-sample t-test]] (a.k.a. independent t-test)
	- What type of t-sample t-test depends on whether the two groups have equal variance (see note)
- If there is one group being compared against a standard value (e.g. comparing the acidity of a liquid to a neutral pH of 7), perform a [[one-sample t-test]]

**One-tailed or two-tailed t-test?:**
- If you only care whether the two populations are different from one another, perform a [[two-tailed t-test]]
- If you want to know whether one population mean is greater than or less than the other, perform a [[one-tailed t-test]]

![[Pasted image 20220919105607.png]]



###### Properties:


###### Additional Thoughts:
