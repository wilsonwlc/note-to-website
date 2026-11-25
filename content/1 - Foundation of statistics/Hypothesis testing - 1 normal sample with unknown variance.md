### Concept
- Aka **one-sample t-test**
### Notation
- Let $X_{1},X_{2},...,X_{n}$ be a [[Random sample|random sample]] from the [[Normal distribution|normal distribution]] $N(\mu,\sigma^{2})$, where the value of $\sigma$ is usually unknown. 
- $\sigma$ is estimated by the [[Sample standard deviation|sample standard deviation]] $S$ 
### Hypothesis testing
- *Aim:* We want to make an inference about $\mu$
- *Case 1:* Two sided test
	- [[Hypothesis|Hypothesis]]: $H_{0} : \mu = \mu_{0}$ VS $H_{1} : \mu \neq \mu_{0}$
	- Reject $H_{0}$ at [[Size and significance level|significance level]] $\alpha$ if $\left| \frac{\overline{X} - \mu_{0}}{\frac{S}{\sqrt{n}}} \right| > t_{\frac{\alpha}{2}, n - 1}$
- *Case 2:* One sided test
	- Hypothesis: $H_{0} : \mu \le \mu_{0}$ VS $H_{1} : \mu > \mu_{0}$
	- Reject $H_{0}$ at significance level $\alpha$ if $\frac{\overline{X} - \mu_{0}}{\frac{S}{\sqrt{n}}} > t_{\alpha, n - 1}$
- *Case 3:* One sided test
	- Hypothesis: $H_{0} : \mu \ge \mu_{0}$ VS $H_{1} : \mu < \mu_{0}$
	- Reject $H_{0}$ at significance level $\alpha$ if $\frac{\overline{X} - \mu_{0}}{\frac{S}{\sqrt{n}}} < -t_{\alpha, n - 1}$
