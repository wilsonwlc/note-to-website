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
### Step
1. Identify a statistical model
2. Formulate the [[Hypothesis|null hypothesis]] $H_0$ and alternative hypothesis $H_{1}$
3. Specify the [[Size and significance level|significance level]] $\alpha$, which is the maximum probability that we allow to make the type I error
4. Choose a test statistic $T$ with known distribution under $H_{0}$
5. Based on the null distribution of $T$, derive the [[Size and significance level|size]] of the test
6. Find the rejection region by setting the size to be less than or equal to the significance level $\alpha$
7. Compute the value of $T$ based on the observed data
8. If $T$ falls in the rejection region, reject $H_0$ at significance level $\alpha$; otherwise do not reject $H_0$
### Example
- Standard medicine: cure rate $p_0 = 0.6$
- New medicine: believed cure rate $p > 0.6$
- Data: Out of 50 patients taken new medicine, 42 patients are cured
- Is the new medicine better?
- Step
	1. Statistical model: 
		- Let $X$ = number of patients cured out of 50
		- $X \sim b(50,p)$
	2. $H_0 : p \le 0.6$ vs $H_1 : p > 0.6$
	3. Require $\alpha=0.05$ *i.e.* allow no more than 5% chance to falsely rejecting $H_0$
	4. Choose the sample proportion $\hat{p} = \frac{X}{n}$ as the test statistic. Using [[Central Limit Theorem (CLT)|normal approximation]], 
	$$
	\frac{\hat{p} - p}{\sqrt{\frac{p(1 - p)}{50}}} \stackrel{a}{\sim} N(0, 1)
	$$
	5. The size of the test is 
	$$
	\begin{align*} \text{size} &= \sup_{\theta \in \Theta_{0}} K(\theta) \\ &= \sup_{\theta \in \Theta_0} P(\text{Reject} \; H_{0} \mid \theta) \\ &= \sup_{p \le 0.6} P(\hat{p}>c|p) \\ &= \sup_{p \le 0.6} P\left(\frac{\hat{p} - p}{\sqrt{\frac{p(1 - p)}{50}}} > \frac{c - p}{\sqrt{\frac{p(1 - p)}{50}}} \right) \\ &= \sup_{p \le 0.6}\left[ 1 - \Phi \left( \frac{c - p}{\sqrt{\frac{p(1 - p)}{50}}} \right) \right] \\ &= 1 - \Phi\left( \frac{c - 0.6}{\sqrt{\frac{(0.6)(0.4)}{50}}} \right) \\ &= 1 - \Phi\left( \frac{c - 0.6}{0.0693} \right) \end{align*}
	$$
	6. Set the size to the significance level $\alpha=0.05$, we have 
	$$
	\begin{align*} 0.05 &= 1 - \Phi\left(\frac{c - 0.6}{0.0693}\right) \\ \frac{c - 0.6}{0.0693} &= 1.645 \\ c &= 0.7140 \end{align*}
	$$
	7. The rejection region is given by $\hat{p} > 0.7140$ *i.e.* $X > 35.7$. Since $X$ must be integer, we will reject $H_{0}$ if $X \geq 36$. *Caution:* The size of the test would be less than 0.05
	8. The value of the test statistics $X=42>36$
	9. We reject $H_{0}$ at 5% significance level *i.e.* the clinical trial data strongly suggests that the new medicine performs better than the standard medicine
### Application
- Hypothesis testing - 1 normal sample with known variance
- Hypothesis testing - 1 normal sample with unknown variance