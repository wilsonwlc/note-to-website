### Normal population
#### Known variance
Suppose we have a [[Random sample|random sample]] from the [[Normal distribution|normal distribution]], $X_{1}, X_{2}, \dots, X_{n} \stackrel{iid}{\sim} N(\mu, \sigma^{2})$ with known variance $\sigma^{2}$
By [[Sampling distributions from normal random sample|Sampling distribution from normal random sample]], $\overline{X} \sim N\left(\mu, \frac{\sigma^{2}}{n}\right)$
1. The [[Confidence interval (CI)|pivot variable]] is $Z = \frac{\overline{X} - \mu}{\frac{\sigma}{\sqrt{n}}} \sim N(0, 1)$
2. For all possible values of $\mu$, $P\left(-z_{\frac{\alpha}{2}} \le \frac{\overline{X} - \mu}{\frac{\sigma}{\sqrt{n}}} \le z_{\frac{\alpha}{2}}\right) = 1 - \alpha$, where $z_{\frac{\alpha}{2}}$ is the upper $\frac{\alpha}{2}$ [[Critical value|critical value]] or $100(1 - \frac{\alpha}{2})$th [[Percentile|percentile]] of the standard normal distribution
3. Solving the inequality gives $P\left(\overline{X} - z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}} \le \mu \le \overline{X} + z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}}\right) = 1 - \alpha$
The $100(1-\alpha)\%$ [[Confidence interval (CI)|CI]] for $\mu$: $$\overline{X} \pm z_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}}$$
#### Unknown variance
- By [[Sampling distributions from normal random sample|Sampling distributions from normal random sample]], $T=\frac{\overline{X}-\mu}{\frac{S}{\sqrt{n}}} \sim t_{n-1}$
- The $100(1-\alpha)\%$ CI for $\mu$: $$\overline{X} \pm t_{\frac{\alpha}{2}, n-1} \frac{S}{\sqrt{n}}$$
### Non-normal population + large sample
 - Approximate CI for the [[Population mean|population mean]] $\mu$ for large sample is $$\begin{cases} \overline{X} \pm z_{\frac{\alpha}{2}}\frac{\sigma}{\sqrt{n}} & \text{if} \; \sigma^{2} \; \text{is known} \\ \overline{X} \pm z_{\frac{\alpha}{2}}\frac{S}{\sqrt{n}} & \text{if} \; \sigma^{2} \; \text{is approximated by} \; S \end{cases}$$
	- $\sigma^{2}$: [[Population variance|Population variance]]
	- $S^{2}$: [[Sample variance|Sample variance]]
	- It is true even if the population distribution is not normal. *Reason:* By [[Central Limit Theorem (CLT)|CLT]], the pivot variable $Z = \frac{\overline{X} - \mu}{\frac{\sigma}{\sqrt{n}}}$ is approximately distributed as normal when the sample size is large
	- *Why we can use sample variance:* $S^{2}$ is a [[Consistency|consistent]] estimator of $\sigma^{2}$
	- *Practice:* Need $n\geq 30$ for a [[Central Limit Theorem (CLT)|good approximation]]
