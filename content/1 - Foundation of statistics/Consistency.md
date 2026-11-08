### Motivation
- A good estimator should have the property that when we observe a very large sample, the observed value of the estimator $\hat{\theta}_{n}$ would be close or almost equal to the true value $\theta$
### Definition
Let the [[Random sample|random sample]] be size of $n$
The [[Point estimation|estimator]] $\hat{\theta}_{n}$ is said to be a **consistent** estimator of $\theta$ if 
$$
\forall \varepsilon>0 \text{,} \quad \lim_{n \rightarrow \infty} P(\left| \hat{\theta}_{n} - \theta  \right| < \varepsilon) = 1
$$
### Properties
#### [[Mean Squared Error (MSE)|MSE]]
- If $\hat{\theta}_{n}$ be an estimator of $\theta$  with $\lim_{n \rightarrow \infty} MSE(\hat{\theta}_{n})=0$, then $\hat{\theta}_{n}$ is a consistent estimator of $\theta$ 
- *Caution:* The converse is not necessarily true
- *Proof:*
	- By [[Markov Inequality|Markov inequality]], for all $\varepsilon>0$, 
		$$
		\begin{align*} P \left( \left| \hat{\theta}_{n} - \theta \right| < \varepsilon \right) &= P \left( \left| \hat{\theta}_{n} - \theta \right|^{2} < \varepsilon^{2} \right) \\ &\geq 1 - \frac{E \left( \left( \hat{\theta}_{n} - \theta \right)^{2} \right)}{\varepsilon^{2}} \\ &\to 1 \quad \text{as} \quad n \to \infty \end{align*}
		$$
#### Unbiased and small variance
- If $\hat{\theta}_{n}$ is an [[Bias|unbiased]] estimator of $\theta$ with $\lim_{n \rightarrow \infty} Var(\hat{\theta}_{n}) = 0$, then $\hat{\theta}_{n}$ is a consistent estimator of $\theta$ 
#### Small bias and small variance
- If $\hat{\theta}_{n}$ is an estimator of $\theta$ with $\lim_{n \rightarrow \infty} bias(\hat{\theta}_{n}) = 0$ and $\lim_{n \rightarrow \infty} Var(\hat{\theta}_{n}) = 0$, then $\hat{\theta}_{n}$ is a consistent estimator of $\theta$ 
### Example
#### Sample mean
- Suppose we have a [[Random sample|random sample]] from [[Normal distribution|normal distribution]] $X_{i} \stackrel{iid}{\sim} N(\mu, \sigma^{2})$ for $i=1,2,...,n$ 
- $\overline{X}_{n}=\frac{1}{n} \sum\limits_{i=1}^{n}X_{i}$
- *Method 1:*
	- $E(\overline{X}_{n})=\mu$ *i.e.* unbiased
	- $Var(\overline{X}_{n})=\frac{\sigma^{2}}{n} \rightarrow 0$ as $n \rightarrow \infty$
	- Hence, the [[Sample mean|sample mean]] is a consistent estimator of the [[Population mean|population mean]]
- *Method 2:* 
	- By [[Weak Law of Large Number (WLLN)|Weak Law of Large Number]] and the definition of consistency
#### Sample variance
- $S^{2}_{n} = \frac{1}{n-1} \sum_{i=1}^{n} (X_{i} - \overline{X})^{2}$
- $E(S^{2}_{n}) = \sigma^{2}$ *i.e.* unbiased
- $\operatorname{Var}\left(S^{2}_{n}\right) = \frac{2 \sigma^{4}}{n - 1}\rightarrow 0$ as $n \rightarrow \infty$
- Therefore the [[Sample variance|sample variance]] is a consistent estimator of the [[Population variance|population variance]]