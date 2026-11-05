### Concept
- *What is it:* 
	- The [[Quantile|quantile]] (cut-off point) of a reference distribution that leaves a specified probability $\alpha$ in one tail (or $\frac{\alpha}{2}$ in each tail for a two-sided test)
	- A cut-off point from the reference distribution such that the probability of observing a test statistic at least as extreme as that value, under $H_0$, equals the specified **significance level** $\alpha$
- *When to use it:* Hypothesis testing. If the test statistic falls in the critical region determined by the critical value(s), reject $H_{0}$ 
### Type
- **Upper-tailed** (right-tailed)
- **Lower-tailed** (left-tailed)
- **Two-tailed** (two-sided)
### Notation
- The $100(1 - \alpha)$th [[Percentile|percentile]] of the [[Normal distribution|standard normal distribution]] $Z\sim N(0,1)$ is denoted as $z_{\alpha}$ *e.g.*
	- $z_{0.05}\approx 1.645$ *i.e.* upper 5% point
	- $z_{0.025}\approx 1.96$
- The $100(1 - \alpha)$th percentile of the [[Chi-square distribution|Chi-square distribution]] with degree of freedom $r$, $\chi_{r}^{2}$ is denoted as $\chi_{\alpha, r}^{2}$ *e.g.* 
	- $\chi_{0.05,24}^{2}$ is the 95th percentile of a $\chi_{24}^{2}$ ($\approx 36.42$)
	- $\chi_{0.95, 24}^{2}$ is the 5th percentile of a $\chi_{24}^{2}$ ($\approx 13.85$)
- For one-sided test, the $100(1 - \alpha)$th percentile of the [[t-distribution|t-distribution]] with degree of freedom $r$, $t_{r}$ is denoted as $t_{\alpha,r}$. For two-sided test at level $\alpha$, the critical values are  $\pm t_{\frac{\alpha}{2}, r}$
- The $100(1 - \alpha)$th percentile of the [[F-distribution|F distribution]] with numerator degree of freedom $r_{1}$  and denominator degree of freedom $r_{2}$, $F(r_{1},r_{2})$ is denoted as $F_{\alpha, r_{1}, r_{2}}$  