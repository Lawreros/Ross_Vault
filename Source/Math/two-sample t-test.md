name : two-sample t-test (independent t-test)
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Student%27s_t-test, https://www.investopedia.com/terms/t/t-test.asp

###### Content:
A [[t-test]] is a method used to test whether the unknown population means of two groups are equal or not. For example, suppose we are evaluating the effect of a medical treatment, and we enroll 100 subjects into our study, then randomly assign 50 subjects to the treatment group and 50 subjects to the control group. In this case, we have two independent samples and would use the unpaired form of the _t_-test.

The calculated [[t-value]]s below can be used to carry out either a [[one-tailed t-test]] or [[two-tailed t-test]].

##### Equal Sample Sizes, Equal Variance
Given two groups $(1,2)$, the [[t-value]] is calculated as follows:
$$t = \frac{\bar X_1 - \bar X_2}{s_p \sqrt{2/n}}$$
where 
$$s_p = \sqrt{\frac{s^2_\bar{X_1}+s^2_\bar{X_2}}{2}}$$
Here $s_p$ is the [[pooled standard deviation]] for $n=n_1=n_2$ and $s_{X_1}^2$ $s_{X_2}^2$ are the [[unbiased estimator]]s of the population [[variance]]. The denominator of $t$ is the [[standard error]] of the difference between two means.
For significance testing, the [[degrees of freedom]] for this test is $2n-2$ where $n$ is sample size.

##### Equal or Unequal Sample Sizes, Similar Variances
Given two groups $(1,2)$, where the variances are similar enough $(0.5 < \frac{s_{X_1}}{s_{X_2}}<2)$ the [[t-value]] is calculated as follows:
$$t = \frac{\bar{X_1} - \bar{X_2}}{s_p \cdot \sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}$$
where $$s_p = \sqrt{\frac{(n_1-1)s_{X_1}^2 + (n_2-1)s_{X_2}^2}{n_1+n_2-2}}$$
is the [[pooled standard deviation]] of the two samples: it is defined in this way so that its square is an [[unbiased estimator]] of the common [[variance]] whether or not the population means are the same.
The [[degrees of freedom]] for each group is $n_i -1$ and the total number of degrees of freedom is $n_1+n_2-2$.
##### Equal or Unequal Sample Sizes, Unequal Variances
Also know as Welch's t-test, the t-value is calculated as follows:
$$t = \frac{\bar X_1 - \bar X_2}{s_\bar{\Delta}}$$
where $$s_{\bar \Delta} = \sqrt{\frac{s_1^2}{n_1} + \frac{s^2_2}{n_2}}$$
here $s_i^2$ is an [[unbiased estimator]] of the variance of each of the two samples. In this case $(s_{\bar \Delta})^2$ is not a [[pooled variance]]. For use in significance testing, the distribution of the test statistic is approximated as an ordinary [[Student's t-distribution]] with [[degrees of freedom]]:
$$d.f. = \frac{(\frac{s_1^2}{n_1} + \frac{s^2_2}{n_2})^2}{\frac{(s^2_1/n_1)^2}{n_1-1} + \frac{(s^2_2/n_2)^2}{n_2-1}}$$



###### Properties:
- "Pooled t-tests" are tests where the variance is assumed to be the same between the groups

###### Additional Thoughts:
