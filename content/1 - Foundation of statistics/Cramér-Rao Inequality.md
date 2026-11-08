### Concept
- *What it does:* give a lower bound to the [[Population variance|variance]] of all unbiased estimators
### Theorem
For any [[Bias|unbiased]] estimator $\hat{\theta}$ of $\theta$, $$\text{Var}(\hat{\theta}) \geq \frac{1}{nI(\theta)}$$
- $\frac{1}{nI(\theta)}$ is called **Cramér-Rao Lower Bound (CRLB)**
- If the variance of an unbiased estimator $\hat{\theta}$ is equal to the Cramér-Rao Lower Bound, then $\hat{\theta}$ is called an **efficient estimator**
### Property
- An [[Efficiency|efficient]] estimator must be an [[UMVUE]]. The converse is not true
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
- The Cramér-Rao Lower Bound is given by $\frac{1}{nI(\theta)} = \frac{\theta}{n}$
- By Cramér-Rao Inequality, for any **unbiased** estimator $\hat{\theta}$ of $\theta$, we have $Var(\hat{\theta}) \geq \frac{\theta}{n}$
- Assume we use the [[Sample mean|sample mean]] $\overline{X}$ as an unbiased estimator for $\theta$
	- $Var(\overline{X})=\frac{Var(X)}{n}=\frac{\theta}{n}$, so the variance of $\overline{X}$ attains the the Cramér-Rao Lower Bound. *i.e.* 
		- $Var(\hat{\theta}) \geq Var(\overline{X})$ for all unbiased estimator $\hat{\theta}$
		- $\overline{X}$ had the minimum variance among all unbiased estimator
		- $\overline{X}$ is an [[UMVUE]]
	- Since the variance of $\overline{X}$ attains the the Cramér-Rao Lower Bound, $\overline{X}$ is an efficient estimator. An efficient estimator must be an [[UMVUE]]
### Comparison
#### UMVUE vs Efficient Estimator
- [[UMVUE]] refers to an unbiased estimator $\hat{\theta}$ that has the smallest variance among all unbiased estimators, for every value of the parameter $\theta$. It is the “best” unbiased estimator in terms of variance, uniformly over the entire parameter space. It may or may not achieve the theoretical lower bound on variance.
- [[Efficiency|Efficient]] estimator refers to an unbiased estimator that attains the [[Cramér-Rao Inequality|Cramér-Rao Lower Bound (CRLB)]]. It is the unbiased estimator with the absolute lowest possible variance allowed by the information in the data