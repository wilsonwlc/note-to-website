### Motivation
- Seldomly estimate "correctly" without error *e.g.* impossible to have a sample mean exactly equal to the population mean
- To justify the estimate, we can specify a "margin of error" for the point estimate from the sample *i.e.* add to and subtracted from the sample result to give a range of values. *e.g.* use the whole range to estimate the population mean
- Justify the range further by considering our confidence that this range contain the true value *e.g.* population mean
### Definition
Let $\{X_{1},X_{2}...,X_{n}\}$ be a [[Random sample|random sample]] from a distribution with unknown parameter $\theta$ 
Let $L(\mathbf{X})$ and $U(\mathbf{X})$ be some functions of the random sample such that for all possible values of $\theta$,  $$P(L(\mathbf{X}) \le \theta \le U(\mathbf{X})) = 1 - \alpha$$
Then, the interval $[L(\mathbf{X}), U(\mathbf{X})]$ is called a $100(1-\alpha)\%$ **confidence interval** for the parameter $\theta$
The quantity $1-\alpha$ is called the **confidence level** associated with the confidence interval
### Step
1. Find a random variable $V(\mathbf{X}, \theta)$ such as its distribution does not depend on $\theta$. $V(\mathbf{X}, \theta)$ is called the **pivot variable**
2. Based on the distribution of $V(\mathbf{X}, \theta)$, find constants $c_{1}$ and $c_{2}$ such that, for all possible values of $\theta$, $$P(c_{1} \le V(\mathbf{X}, \theta) \le c_{2}) = 1 - \alpha$$
3. Solve the inequality inside the probability statement to obtain, for all possible values of $\theta$, $$P(L(\mathbf{X}) \le \theta \le U(\mathbf{X})) = 1 - \alpha$$
4. The interval given by $[L(\mathbf{X}), U(\mathbf{X})]$ is then $100(1-\alpha)\%$ CI for $\theta$

### Interpretation
#### Repeated sampling
- Assume you draw a large number of independent sets of random samples. Each of them has the same size and comes from same population. For each sample, you construct a realised confidence interval (*i.e.* a realisation of a random interval). Approximately $100(1-\alpha)\%$ of these intervals will contain the fixed unknown parameter $\theta$ ![[Confidence interval - Interpretation.jpeg|343]]
- The confidence level $100(1-\alpha)\%$ is the probability describing the behaviour of all possible intervals rather than just the one we obtain. It represents the performance of the entire procedure
- A confidence interval is not a probability statement about the parameter $\theta$ after you have seen the data
#### Random interval vs Realised interval
- $L(\mathbf{X})$ and $U(\mathbf{X})$ are statistics (functions of the random sample $\mathbf{X}$. Hence, the confidence interval $[L(\mathbf{X}), U(\mathbf{X})]$ is a **random interval** before the data is observed *i.e.* its endpoints and the interval itself vary from sample to sample. 
- Once a particular sample is observed (*i.e.* realised), the boundaries and numerical interval become fixed numbers. There is no remaining randomness. The unknown $\theta$ either lies inside that fixed interval or it does not. The probability is then either 1 or 0
- The randomness (and the $1-\alpha$ coverage probability) belongs to the procedure over repeated sampling, not to any single realised interval
#### Length of CI
- There is always a trade-off between the confidence level and the information content
	- A shorter confidence interval is corresponding to a smaller margin of error and thus is more informative
	- Based on the same sample, if we use a lower confidence level, the confidence interval can be made shorter
- With a fixed confidence level, we can reduce the margin of error (hence producing shorter confidence interval) by increasing the sample size
#### Non-uniqueness
- The confidence interval is not unique *i.e.* for any specific confidence level $1-\alpha$, there are infinite pairs of constants $c_{1}$ and $c_{2}$ such that $P(c_{1} \le V(\mathbf{X}, \theta) \le c_{2}) = 1 - \alpha$
### Practice
#### Confidence level
- *Reason:* the non-uniqueness of the confidence interval, 
- *Case 1:* even allocation
	- *Action:* choose $c_{1}$ and $c_{2}$ such as the amount of probability in each of the 2 tails are same *i.e.* $\frac{\alpha}{2}$
		- Probability to the left of $c_{1}$,  $P(V(\mathbf{X}, \theta) < c_{1}) = \frac{\alpha}{2}$
		- Probability to the right of $c_{2}$, $P(V(\mathbf{X}, \theta) > c_{2}) = \frac{\alpha}{2}$
	- *Example:* $\left[ \overline{X} - t_{0.01, 11} \frac{S}{\sqrt{n}}, \overline{X} - t_{0.04, 11} \frac{S}{\sqrt{n}} \right]$
- *Case 2:* one-sided allocation
	- *When:* The possible values of the parameter $\theta$ are restricted by a known finite boundary *e.g.* $\theta \geq 0$, $0 \leq \theta \leq 1$, $\sigma>0$
	- *Action:* put the entire probability $\alpha$ into a single tail and leave the other tail empty *i.e.*
		- Lower confidence bound only: $P(V(\mathbf{X}, \theta) \ge c_{1}) = 1 - \alpha$
		- Upper confidence bound only: $P(V(\mathbf{X}, \theta) \le c_{2}) = 1 - \alpha$
	- *Example:* $\left[ 0, \frac{\chi_{2n, \alpha}^{2}}{2n\overline{X}} \right]$
### Example
- [[CI - 1 population mean|CI - 1 population mean]]
- [[CI - Comparison of 2 population means|CI - Comparison of 2 population means]]
- [[CI - Comparison of 2 population variances|CI - Comparison of 2 population variances]]
- [[CI - 1 population proportion|CI - 1 population proportion]]
- [[CI - Comparison of 2 population proportions|CI - Comparison of 2 population proportions]]
