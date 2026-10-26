### Concept
- *What is it:* A value that divides a probability distribution (or an empirical dataset) into parts of specified relative size
- *Interpretation:* The 0.9-quantile is the value below which 90% of the distribution lies
- *Scale:* 0-1
### Definition
$$
x_{p} = \inf\{x : F(x) \ge p\}
$$

- $x_{p}$: **p-quantile**
- $p \in [0,1]$
- $F(x)$: [[Cumulative distribution function (cdf)|cdf]]
#### Continuous
If $X$ is a [[Continuous random variable|continuous random variable]] and $F$ is strictly increasing, then $F^{-1}$ exists and $x_{p}=F^{-1}(p)$, where $0<p<1$
#### Discrete
Assume $X$ is a [[Discrete random variable|discrete random variable]]
The p-**quantile** of $X$ is defined as the smallest $x$ such $F(x) \geq p$
### Comparison
#### Percentile vs Quantile
- The $p$-th percentile equals the $\frac{p}{100}$-[[Quantile|quantile]]
### Caution
- When $F$ is not strictly increasing, the ordinary inverse may not exist and there may be an interval of quantiles. The general definition using the infimum always selects a unique (lower) percentile / quantile
### Practice
- [[Lower quantile|Lower quantile]]
- [[Median|Median]]
- [[Upper quantile|Upper quantile]]
### Example
#### Percentile and Quantile
| $X$    | 0      | 1      | 2      | 3      | 4      | 5      |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| $p(x)$ | 0.1681 | 0.3602 | 0.3087 | 0.1323 | 0.0284 | 0.0024 |
| $F(x)$ | 0.1681 | 0.5283 | 0.8370 | 0.9693 | 0.9977 | 1      |
- Let $X$ be a binomial random variable with parameters $n = 5$ and $p = 0.3$
- The table shows the pmf and cdf of $X$
- The median of a $b(5,0.3)$ random variable is $x_{0.5}=1$
- The 75th percentile is $x_{0.75}=\min\{x : F(x) \ge 0.75\} = 2$
