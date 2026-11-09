### Formula
When the sample size $n$ is large, the $100(1 - a)\%$ [[Confidence interval (CI)|confidence interval (CI)]] for $p$ is 
$$
\hat{p} \pm z_{\frac{\alpha}{2}} \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}
$$
- $\hat{p}$: [[Sample proportion|Sample proportion]]
##### Proof
- When $n$ is large, by [[Central Limit Theorem (CLT)|Central Limit Theorem (CLT)]], the [[Confidence interval (CI)#Step|pivot variable]] 
$$
\frac{X - np}{\sqrt{np(1 - p)}} \sim N(0, 1)
$$
- For all $0<p<1$, 
$$
P\left(-z_{\frac{\alpha}{2}} \le \frac{X - np}{\sqrt{np(1 - p)}} \le z_{\frac{\alpha}{2}}\right) = 1 - \alpha
$$
- An approximate $100(1 - a)\%$ CI for $p$ 
$$
\frac{2\hat{p} + \frac{z_{\frac{\alpha}{2}}^2}{n} \pm \sqrt{\left(2\hat{p} + \frac{z_{\frac{\alpha}{2}}^2}{n}\right)^2 - 4\hat{p}^2\left(1 + \frac{z_{\frac{\alpha}{2}}^2}{n}\right)}}{2\left(1 + \frac{z_{\frac{\alpha}{2}}^2}{n}\right)}
$$
- $\frac{z_{\frac{\alpha}{2}}^2}{n}$ is negligible when $n$ is large
- An approximate $100(1 - a)\%$ CI for $p$ is 
$$
\hat{p} \pm z_{\frac{\alpha}{2}} \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}
$$
### Practice
- To use [[Approximation to Binomial using Normal|normal distribution for the determination of critical value rather than using binomial distribution]], both $np$ and $n(1-p)$ are at least 5. 
	- Some people say 10 instead of 5
	- Because the true $p$ is unknown, we cannot evaluate those expressions directly We replace $p$ by the observed sample proportion $\hat{p}$
### Formula
When the sample size $n$ is small, use the following formulae to construct the one-sided C.I. for $p$
- $[0, \hat{p}_U]$ where $\sum_{j=0}^{X} \binom{n}{j} \hat{p}_U^j (1 - \hat{p}_U)^{n-j} = \alpha$ *or*
- $[\hat{p}_L, 1]$ where $\sum_{j=X}^{n} \binom{n}{j} \hat{p}_L^j (1 - \hat{p}_L)^{n-j} = \alpha$
### Interpretation
- $\hat{p}_{L}$ and $\hat{p}_{U}$ are function of $X$ and therefore are statistics
- $[0, \hat{p}_U]$ and $[\hat{p}_L, 1]$ are called **conservative confidence intervals**. *Reason:* Their confidence level may be larger than $1-\alpha$ *i.e.*
	- $P(0 < p < \hat{p}_U) \ge 1 - \alpha$ for all $p \in (0,1)$
	- $P(\hat{p}_L < p < 1) \ge 1 - \alpha$ for all $p \in (0,1)$