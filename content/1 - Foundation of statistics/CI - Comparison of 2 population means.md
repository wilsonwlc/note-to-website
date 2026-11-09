### Assumption
- Suppose we have two populations, each with measurements that follow a [[Normal distribution|normal distribution]]. We draw [[Random sample|random samples]] from these two populations independently to make inferences
### Notation
- Assume the 2 [[Independence of random variables#Corollary|independent samples]] are $X_{1}, X_{2}, \dots, X_{m} \stackrel{iid}{\sim} N(\mu_{x}, \sigma_{x}^{2})$ and $Y_{1}, Y_{2}, \dots, Y_{n} \stackrel{iid}{\sim} N(\mu_{y}, \sigma_{y}^{2})$ where $\mu_{x}$, $\mu_{y}$, $\sigma_{x}^{2}$, $\sigma_{y}^{2}$ are unknown parameters
### When
- Compare the 2 [[Population mean|population means]] by constructing a [[Confidence interval (CI)|CI]] for $\mu_{x}-\mu_{y}$
### Formula
#### Case 1: Both population variance are known
- The MLE for $\mu_{x}-\mu_{y}$ is $\overline{X}-\overline{Y}$
- By [[Sampling distributions from normal random sample|Sampling distributions from normal random sample]], we have $\overline{X} \sim N\left(\mu_{x}, \frac{\sigma_{x}^{2}}{m}\right)$ and $\overline{Y} \sim N\left(\mu_{y}, \frac{\sigma_{y}^{2}}{n}\right)$
- Since $\overline{X}$ and $\overline{Y}$ are [[Independence of random variables|independent]], by the property of [[Normal distribution|normal distribution]], we have $(\overline{X} - \overline{Y}) \sim N\left(\mu_{x} - \mu_{y}, \frac{\sigma_{x}^{2}}{m} + \frac{\sigma_{y}^{2}}{n}\right)$ 
- The [[Confidence interval (CI)#Step|pivot variable]] is $Z = \frac{(\overline{X} - \overline{Y}) - (\mu_{x} - \mu_{y})}{\sqrt{\frac{\sigma_{x}^{2}}{m} + \frac{\sigma_{y}^{2}}{n}}} \sim N(0, 1)$
- The $100(1-\alpha)\%$ CI for $\mu_{x}-\mu_{y}$ is $(\overline{X} - \overline{Y}) \pm z_{\alpha/2} \sqrt{\frac{\sigma_{x}^{2}}{m} + \frac{\sigma_{y}^{2}}{n}}$
#### Case 2: Both population variance are unknown
- Since $\sigma^{2}_{x}$ and $\sigma^{2}_{y}$ are unknown, estimate them by [[Sample variance|sample variance]]
- The pivot variable is $T = \frac{(\overline{X} - \overline{Y}) - (\mu_{x} - \mu_{y})}{\sqrt{\frac{S_{x}^{2}}{m} + \frac{S_{y}^{2}}{n}}} \sim t_{\nu}$
	- Degree of freedom $\nu = \frac{\left(\frac{S_{x}^{2}}{m} + \frac{S_{y}^{2}}{n}\right)^{2}}{\frac{S_{x}^{4}}{m^{2}(m-1)} + \frac{S_{y}^{4}}{n^{2}(n-1)}}$
	- *Caution:* 
		- The [[Sampling distribution|sampling distribution]] is not exact
		- $\nu$ is not an integer, and $t_{\frac{\alpha}{2},\nu}$ cannot be obtained from the [[t-distribution table|t-table]]
		- *Proof:* 
			- Require [[Cochran-Satterthwaite approximation for the linear combination of mean squares|Cochran-Satterthwaite approximation for the linear combination of mean squares]] and [[Sampling distributions from normal random sample|Sampling distributions from normal random sample]]
			- See [[Satterthwaite approximation for two sample comparison|Satterthwaite approximation for two sample comparison]]
- The $100(1-\alpha)\%$ CI for $\mu_{x}-\mu_{y}$ is $(\overline{X} - \overline{Y}) \pm t_{\alpha/2, \nu} \sqrt{\frac{S_{x}^{2}}{m} + \frac{S_{y}^{2}}{n}}$
- This test is called **Welch's t-test**, **unequal variances t-test**, **Satterthwaite test**, **Welch-Satterthwaite test**
#### Case 3: Both population variance are unknown, but equal
- Assume $\sigma^{2}_{x}=\sigma^{2}_{y}=\sigma^{2}$
- The pooled sample variance (a weighted mean of the two sample variances) is $S_{pool}^{2} = \frac{(m-1)S_{x}^{2} + (n-1)S_{y}^{2}}{m + n - 2}$
- The sampling distribution $W = \frac{(m+n-2)S_{pool}^{2}}{\sigma^{2}} = \frac{(m-1)S_{x}^{2}}{\sigma^{2}} + \frac{(n-1)S_{y}^{2}}{\sigma^{2}} \sim \chi_{m+n-2}^{2}$
	- *Reason:* (1) [[Sampling distributions from normal random sample|Sampling distribution of the sample variance]] is a [[Chi-square distribution|chi-square distribution]]; (2) The sum of independent **Chi-square** random variables is distributed as Chi-square
- $Z = \frac{(\overline{X} - \overline{Y}) - (\mu_{x} - \mu_{y})}{\sqrt{\frac{\sigma^{2}}{m} + \frac{\sigma^{2}}{n}}} = \frac{(\overline{X} - \overline{Y}) - (\mu_{x} - \mu_{y})}{\sigma \sqrt{\frac{1}{m} + \frac{1}{n}}} \sim N(0,1)$
	- *Reason:* By the property of normal distribution and the [[Sampling distributions from normal random sample|sampling distributions from normal random sample]], we have $\overline{X} - \overline{Y} \sim N\left(\mu_x - \mu_y, \sigma^2 \left(\frac{1}{m} + \frac{1}{n}\right)\right)$ 
- The pivot variable is $T = \frac{Z}{\sqrt{\frac{W}{m+n-2}}} = \frac{(\overline{X} - \overline{Y}) - (\mu_{x} - \mu_{y})}{S_{pool} \sqrt{\frac{1}{m} + \frac{1}{n}}} \sim t_{m+n-2}$
	- *Reason:* By definition of [[t-distribution|t-distribution]]
- The $100(1-\alpha)\%$ CI for $\mu_{x}-\mu_{y}$ is $(\overline{X} - \overline{Y}) \pm t_{\frac{\alpha}{2}, m+n-2} S_{pool} \sqrt{\frac{1}{m} + \frac{1}{n}}$
### Caution
- The assumption about equal population variances must be satisfied. *How to verify it:*
	- Domain knowledge *e.g.* If it is believed that a certain treatment will be more or less the same on all experimental objects, then it can be regarded as a shifting of the distribution without altering the variation. In such case, it would be reasonable to assume equal population variances on treatment and control groups
	- Comparison of 2 population variances
- *When to use them:*
	- [[Normal distribution|Normal]] population → confidence-interval procedures are valid, even with small samples
	- Non-normal population + large sample → procedures are still valid, mainly because of the **Central Limit Theorem**
	-  Non-normal population + small sample → use **non-parametric methods** instead
- *How to satisfy the assumption about independence:* 
	- Usually it can be guaranteed by proper design on the sampling or experimental procedures
	- In some typical experiments (e.g. **before-and-after studies**, **matched-pairs studies**, and **repeated-measures studies**), data are measured on same objects. The result cannot be regarded as independence samples although the data looks like obtaining from two samples