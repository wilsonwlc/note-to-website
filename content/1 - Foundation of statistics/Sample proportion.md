### Motivation
- Many surveys have their objective as the estimation of the proportion of people or objects in a large group that possess a particular attribute *e.g.* support the president, carry a certain virus, have annual salary more than $400,000
- Suppose we draw a sample of size $n$ from a very large population. Assume that a proportion $p$ of the objects in the population have a certain characteristic
- We want to make inference about $p$
### Assumption
- We regard the $n$ drawn samples as $n$ independent Bernoulli trials. $p$ is the success probability. This requires the population is much larger than the sample so that it can be approximately regarded as an infinite population. *Practice:* The population size should be at least 10 times the sample size for adequate approximation
### Definition
Suppose a sample of size $n$ is drawn. The probability that the drawn sample has the characteristic is $p$
Let $X$ be the number of objects in the samples having the characteristic
The **sample proportion** is
$$
\hat{p}=\frac{X}{n}
$$

### Property
- $X \sim b(n,p)$ *i.e.* [[Binomial distribution|Binomial distri]]
- [[Population mean|Mean]]: $\text{E}(\hat{p})=p$
- [[Population variance|Variance]]: $\text{Var}(\hat{p})=\frac{p(1-p)}{n}$
- [[Standard error|Estimated standard error]]: $\widehat{\operatorname{se}}(\hat{p}) = \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}$
- [[Confidence interval (CI)|Confidence interval]]: 
	- [[CI - 1 population proportion]]
	- [[CI - Comparison of 2 population proportions]]
### Practice
- For large $n$, $\hat{p}$ is approximately [[Normal distribution|normal]] $\hat{p} \approx N\left(p, \frac{p(1−p)}{n}\right)$. See [[Approximation to Binomial using Normal]]