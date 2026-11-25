### Concept
- Aka Significance Probability
- *What is it:* Probability of the occurrence of the particular observed value or more extreme values under the assumption of $H_0$
### Interpretation
- The smaller the magnitude of p-value, the stronger is the evidence against $H_{0}$
### Comparison 
#### Use p-value vs critical value for hypothesis test
- Given a pre-assigned significance level $\alpha$, there are 2 approaches
	1. Compare the observed value of the test statistic with critical value. It is also called classical approach
	2. Compute the p-value from the observed value of the test statistic and then compare it with $\alpha$
- For the one-sided upper-tail test, the test procedure “Reject $H_0$ if the test statistic is greater than the critical value” is equivalent to “Reject $H_0$ if the p-value is less than or equal to $\alpha$”. The same applies to lower-tail and two-sided tests.
- To use Approach 1, need to specify the significance level and then compute the critical value. However, different people may have different choice of $\alpha$, different critical value will be needed
- To use Approach 2, only need to compute the p-value. p-value is more informative. It not only states whether or not a hypothesis is rejected, but also indicates how unlikely the observed event is under the null hypothesis. The users can make their own decision on what to conclude in face of the evidence.