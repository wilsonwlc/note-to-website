### Theorem
Suppose that $\hat{\theta}_{ML}$ is an [[Maximum likelihood estimation (MLE)|MLE]] of $\theta$. 
Under some **regularity** conditions, $$\sqrt{n} \left( \hat{\theta}_{ML} - \theta \right) \xrightarrow{L} N \left( 0, \frac{1}{I(\theta)} \right) \text{ as } n \to \infty$$
- $I(\theta)$: [[Fisher Information|Fisher information]]
### Interpretation
- The distribution of the MLE $\hat{\theta}_{ML}$ is asymptotically [[Normal distribution|normal]]
### Example
- Given the [[Poisson distribution|Poisson distribution]] with [[Probability mass function (pmf)|pmf]] $f(x;\theta)=\frac{e^{-\theta} \theta^{x}}{x!}$ where $x=0,1,2,...$
- Hence, we have 
$$
\begin{aligned}
\log f(X;\theta) &= -\theta + X \log\theta - \log X! \\
\frac{d}{d\theta} \log f(X;\theta) &= -1 + \frac{X}{\theta} \\ 
\frac{d^{2}}{d\theta^{2}} \log f(X;\theta) &= -\frac{X}{\theta^{2}} \\
I(\theta) &= E\left( -\frac{d^{2}}{d\theta^{2}} \log f(X;\theta) \right) \\ &= E\left( \frac{X}{\theta^{2}} \right) \\ &= \frac{1}{\theta}
\end{aligned}
$$
- Assume we use the **sample mean** $\overline{X}$ as an unbiased estimator for $\theta$
	- Since the $\hat{\theta}_{ML} = \overline{X}$, we have as $n \rightarrow \infty$, 
		$$
		\sqrt{n}(\overline{X}-\theta) \xrightarrow{L} N\left(0, \frac{1}{\frac{1}{\theta}}\right)= N(0, \theta) 
		$$
	- *i.e.* $\overline{X} \xrightarrow{L} N \left(\theta, \frac{\theta}{n} \right)$ as $n \rightarrow \infty$
### Assumption
#### Regularity conditions
- The support of the data distribution cannot depend on the parameter *e.g.*  $U(0, \theta)$ violates this condition
- The MLE cannot lie on boundary of the set of possible parameters. *e.g.* The condition is violated for the normal model $N(\mu, \sigma^{2})$ with $\mu \geq 0$. *Reason:* The MLE of $\mu$ is 
$$
\hat{\mu} = \begin{cases} \overline{X} & \text{if } \overline{X} > 0 \\ 0 & \text{if } \overline{X} \le 0 \end{cases}
$$
- The number of nuisance parameters (*i.e.* parameters other than the one being estimated) cannot increase with the sample size. *e.g.* This condition is violated if we are estimating $\mu$ based on the model $X_{i} \sim N(\mu, \sigma^{2}_{i})$ where $i=1,2,...,n$. *Reason:* The number of variance $\sigma_{i}^{2}$ increases with the sample size
- The amount of information should increases indefinitely with the sample size. *e.g.* If there are too much dependence among the observations, then this condition will be violated
### Practice
- There are some sufficient conditions that guarantee the asymptotic normality of the MLE
	- Both $\frac{\partial}{\partial \theta} \log{f(X;\theta)}$ and $\frac{\partial^{2}}{\partial^{2} \theta} \log{f(X;\theta)}$ exist
	- $I(\theta)$ is continuous
	- The MLE $\hat{\theta}_{ML}$ is a [[Consistency|consistent]] estimator of $\theta$