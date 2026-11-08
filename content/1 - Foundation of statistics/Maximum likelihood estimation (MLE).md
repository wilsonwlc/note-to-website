### Definition
The **maximum likelihood estimator** (MLE) $\hat{\theta}_{ML}$ of $\theta$ is the value of $\theta$ that maximises the [[Likelihood function|likelihood function]]
### Practice
- We can obtain $\hat{\theta}_{ML}$ by maximising the log-likelihood function. *Reason:* The logarithm function is strictly increasing
- Under some **regularity** conditions,
	- Asymptotically [[Efficiency|efficient]]: The MLE $\hat{\theta}_{ML}$ has the smallest variance among all unbiased estimator as $n \rightarrow \infty$. *Proof:* [[MLE - Asymptotic normality|Asymptotic distribution of MLE]], [[Cramér-Rao Inequality|Cramér-Rao Inequality]] and definition of [[Efficiency|efficiency]]
	- [[Consistency]]: The MLE $\hat{\theta}_{ML}$ is a consistent estimator of $\theta$
	- [[MLE - Asymptotic normality|Asymptotic Normality]]: The MLE $\hat{\theta}_{ML}$ is approximately distributed as [[Normal distribution|normal]] when the sample size is large
### Caution
- The MLE may be biased in small sample
