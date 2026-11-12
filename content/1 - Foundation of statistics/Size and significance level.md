### Concept
- *Which:* a property of [[Hypothesis testing|hypothesis testing]]
### Definition
Let $K(\theta)$ be the [[Power function|power function]]
$$
\text{size} = \sup_{\theta \in \Theta_0} K(\theta)
$$
If the size of a test is less than or equal to pre-chosen threshold $\alpha$, then the test is said to have **significance level** $\alpha$
### Interpretation
- The size is the maximum of the probability of a [[Type I error|Type I error]] over the null parameter space $\Theta_0$. It represents the actual worst scenario of falsely rejecting the null hypothesis. It tells how large the Type I error of this particular test can be
- The significance level is the maximum Type I error rate (false positive) you are willing to tolerate *i.e.* acceptable before looking at the data
- Choosing a smaller $\alpha$ makes the test more conservative
### Caution
- In continuous distributions with [[Hypothesis|simple null hypotheses]], we can often construct a test whose size is exactly $\alpha$. Size and significance level become interchangeable
- However, in many important situations, exact equality is impossible
	- For the [[Discrete random variable|discrete distributions]] *e.g.* [[Binomial distribution|Binomial]], [[Poisson distribution|Poisson]], the attainable [[Type I error|Type I error probabilities]] jump in discrete steps
	- When we have composite null hypotheses, the **power function** $K(\theta)$ varies over $\Theta_0$​, so the supremum need not equal every convenient numerical value of $\alpha$