### Assumption
- Let $X_{1},X_{2},...,X_{n}$ be a [[Random sample|random sample]] from the [[Normal distribution|normal distribution]] $N(\mu,\sigma^{2})$, where $\sigma$ is a known constant
### Hypothesis testing
- *Aim:* We want to make an inference about $\mu$
- *Case 1:* Two sided test
	- [[Hypothesis|Hypothesis]]: $H_{0} : \mu = \mu_{0}$ VS $H_{1} : \mu \neq \mu_{0}$
	- Reject $H_{0}$ at [[Size and significance level|significance level]] $\alpha$ if $\left| \frac{\overline{X} - \mu_{0}}{\frac{\sigma}{\sqrt{n}}} \right| > z_{\frac{\alpha}{2}}$
- *Case 2:* One sided test
	- Hypothesis: $H_{0} : \mu \le \mu_{0}$ VS $H_{1} : \mu > \mu_{0}$
	- Reject $H_{0}$ at significance level $\alpha$ if $\frac{\overline{X} - \mu_{0}}{\frac{\sigma}{\sqrt{n}}} > z_{\alpha}$
- *Case 3:* One sided test
	- Hypothesis: $H_{0} : \mu \ge \mu_{0}$ VS $H_{1} : \mu < \mu_{0}$
	- Reject $H_{0}$ at significance level $\alpha$ if $\frac{\overline{X} - \mu_{0}}{\frac{\sigma}{\sqrt{n}}} < -z_{\alpha}$
#### Proof
##### Case 1
- Use the [[Sample mean|sample mean]] $\overline{X}$, which is the [[Maximum likelihood estimation (MLE)|MLE]] of $\mu$, as the test statistic
- By the [[Sampling distributions from normal random sample|sampling distributions from normal random sample]], $Z = \frac{\overline{X} - \mu}{\frac{\sigma}{\sqrt{n}}} \sim N(0,1)$. Under $H_{0}$, $$Z = \frac{\overline{X} - \mu_{0}}{\frac{\sigma}{\sqrt{n}}} \sim N(0,1)$$
- Reject $H_{0}$ if $Z$ is too large or too small *i.e.* $|Z|>c$
- Recall $$\begin{align*} \text{size} &= \sup_{\theta \in \Theta_{0}} K(\theta) \\ &= \sup_{\theta \in \Theta_0} P(\text{Reject} \; H_{0} \mid \theta) \\ \alpha &= P(\text{Reject} \; H_{0} \mid \theta=\theta_{0}) \end{align*}$$
- Hence, we have $$\begin{align*} \alpha &=  P(|Z|>c|\mu=\mu_{0}) \\ &= P \left(\left|\frac{\overline{X} - \mu_{0}}{\frac{\sigma}{\sqrt{n}}}\right|>c\right) \\ &= 2[1-\Phi(c)] \\ \Phi(c) &= 1-\frac{\alpha}{2} \\ c &= z_\frac{\alpha}{2}  \end{align*}$$
- Reject $H_{0}$ at significance level $\alpha$ if $\left|\frac{\overline{X} - \mu_{0}}{\frac{\sigma}{\sqrt{n}}}\right| > z_{\frac{\alpha}{2}}$ 