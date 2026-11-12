### Concept
- *What is it:* 
	- The probability of correctly rejecting the $H_{0}$ when it is false 
	- The probability of avoiding [[Type II error|Type II error]]
	- The complement of the Type II error rate
- *Which:* a property of [[Hypothesis testing|hypothesis testing]]
### Definition
$$
\text{power}=1-\beta
$$
- $\beta$: [[Type II error|Type II error]]
### Interpretation
- It is the probability of not committing a Type II error *i.e.* correctly rejecting the [[Hypothesis|null hypothesis]] when the null is false 
- A test has a high power. This means if a true effect or deviation from the null really exists, the test is more likely to detect it *i.e.* produce a statistically significant result. *e.g.* rarely misses a real disease
- A test has a low power. This means even if a real effect is present, the test often fails to find it *i.e.* high chance of a Type II error / “false negative” *e.g.* a test that often misses the disease even when the patient has it 
- For a composite alternative $H_{1}: \theta \in \Theta_{1}$, the power of the test at a particular value $\theta=\theta_{1}$ is the value of the [[Power function|power function]] $\theta_{1}$ *i.e.* $$\text{power at} \; \theta_1 = P(\text{Reject } H_0 \mid \theta = \theta_1) = K(\theta_1)$$
### Practice
- Since we can always construct a test with a desirable [[Size and significance level|size]], the comparison among different test procedures would be based on the power
