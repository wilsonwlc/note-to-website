### Concept
- *What is it:* a [[Random variable|random variable]]. Its probability distribution is called the [[Sampling distribution]] of the mean
### Definition
Let $X_{1},...,X_{n}$ be [[Independence of random variables|independent]] and identically distributed (i.i.d.) random variables
$$
\overline{X}=\frac{1}{n} \sum\limits_{i=1}^{n}X_{i}
$$
### Property
Assume $E(X_i)=\mu$ and $\text{Var}(X_{i})=\sigma^{2} < \infty$
- [[Population mean|Mean]]: $E(\overline{X})=\mu$
- [[Population variance|Variance]]: $\text{Var}(\overline{X})=\frac{\sigma^{2}}{n}$
- [[Population standard deviation|Standard deviation]] and [[Standard error|Standard error]] of $\overline{X}$: $\frac{\sigma}{\sqrt{n}}$
- [[Moment generating function (mgf)|Moment generating function]]: $$M_{\overline{X}}(t) = \left( M_{X}\left( \frac{t}{n} \right) \right)^{n}$$
	- $M_{X}(t)$ is the common moment generating function of $X_{1},...,X_{n}$
### Interpretation
- Since the mean from a large sample is more likely to be close to [[Population mean|population mean]], $\mu$ than the mean from a small sample, the [[Standard error|standard error]] can be interpreted as a typical distance between the sample mean and the population mean
### Practice
- For [[Standard error|standard error]], the [[Population standard deviation|population standard deviation]] $\sigma$ is unknown. It is estimated by the [[Sample standard deviation|sample standard deviation]], $S$. The estimated standard error can be computed by $$\text{se}(\overline{X}) = \frac{S}{\sqrt{n}}$$