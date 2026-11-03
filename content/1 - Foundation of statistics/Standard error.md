### Concept
- Aka **true** / **theoretical** / **population standard error**
- *Which:* a property of a statistics $\hat{\theta}$
- *What is it:* the [[Population standard deviation|population standard deviation]] of the [[Sampling distribution|sampling distribution]] of a statistic
### Interpretation
- If you could repeatedly draw samples of the same size from the same population and compute the statistic (most commonly the sample mean) each time, the standard error quantifies how much that statistic would typically vary from sample to sample
- The standard error gets smaller as the sample size increases. *Caution:* This statement remains true for all common statistics 
### Example
- For [[Sample mean|sample mean]], its standard error is $\frac{\sigma}{\sqrt{n}}$, where $\sigma$ is the [[Population standard deviation|population standard deviation]] and $n$ is the sample size
### Comparison
#### Standard deviation vs Standard error
- [[Sample standard deviation|Standard deviation]] describes the variability among the raw data points
- [[Standard error|Standard error]] describes the variability of a statistic (*e.g.* [[Sample mean|sample mean]]) across repeated samples of the same size
#### True standard error vs Estimated standard error
- True standard error
	- *How to get it:* almost never known in practice
	- Depend on population parameters
	- Notation: $\text{SE}(\hat{\theta})$
	- *Example:* $\operatorname{SE}(\overline{X}) = \frac{\sigma}{\sqrt{n}}$
- Estimated standard error
	- *How to get it:* replace the unknown population quantities with consistent sample estimates
	- Depend on sample data
	- Notation: $\text{se}(\hat{\theta})$ or $\widehat{\text{SE}}$
	- *Example:* $\widehat{\operatorname{SE}}(\overline{X}) = \frac{s}{\sqrt{n}}$