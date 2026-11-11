### Concept
- *What is it:* A **hypothesis test** is a formal rule/procedure that uses the observed sample data to decide whether to reject or not reject the [[Hypothesis|null hypothesis]] $H_{0}$
	- The sample statistics (a function of the data) that is calculated is called the **test statistic**. It will be used to compare against [[Critical value|critical values]] or compute a [[p-value|p-value]]
	- The set of values of the test statistic, for which $H_0$ is rejected, is called the **rejection region** or **critical region**
### Interpretation
#### Intuition
- The basic strategy in hypothesis testing is to measure how far the test statistic (*e.g.* [[Sample mean|sample mean]], $\overline{X}$) is from a hypothesised value of the parameter (*e.g.* [[Population mean|population mean]], $\mu$)
- If the difference between these 2 values is large, we would argue that the hypothesised statement is inconsistent with the data and we would be inclined to reject the hypothesis.
- However, we could be wrong because rare events can happen
- Hence, before jumping to the conclusion, we must take into account the possible variability of the observations as the difference between the values may be just resulted from sampling errors but not the deviation of the null hypothesis from the truth
- We conclude that the null hypothesis is false if the observed difference is sufficiently large relative to the sampling variability
### Caution
#### Interpretation of result
- When we test $H_{0}$ against $H_{1}$, we observe the data to see if there is sufficient evidence to reject $H_{0}$
- we have statistically significant evidence against $H_{0}$ (at the chosen significance level) in favour of $H_{1}$
- If we observe the data and find that $H_0$ is not rejected, it does not mean that we have great confidence in the truth of $H_{0}$. It only means that we have not enough evidence to reject $H_{0}$
- Formally, we should say "do not reject $H_{0}$" instead of "accept $H_{0}$" 
#### Rejection region
- The rejection region, or the decision rule, is decided before we actually observe our data
### Example
- Hypothesis: $H_{0}:\mu=\mu_{0}$ vs $H_{1}:\mu < \mu_{0}$
- Decision rule: Reject $H_0$ and accept $H_{1}$ if $\overline{X}<x_{0}$ for some fixed number $x_{0}$
	- Test statistic: sample statistic $\overline{X}$
	- In fact, $x_0$ is chosen so that the Type I error probability equals the desired significance level