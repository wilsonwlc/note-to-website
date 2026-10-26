### Concept
- *What is it:* A value below which a given percentage of observations in a dataset (or probability mass in a distribution) fall
- *Interpretation:* The 90th percentile is the value below which 90% of the data lies
- *Scale:* 0-100
### Definition
$$
x_{p} = \inf \left\{ x:F(x) \geq p \right\}
$$

- $x_{p}$: **100p-th percentile**
- $p$ is a probability in $[0,1]$
- $F(x)$: [[Cumulative distribution function (cdf)|cdf]]
#### Continuous
Assume $X$ is a [[Continuous random variable|continuous random variable]], $F^{-1}$ exists
The value $F^{-1}(p)$ is called the 100$p$-th percentile of $X$ , where $0<p<1$
#### Discrete
Assume $X$ is a [[Discrete random variable|discrete random variable]]
The 100p-th percentile of $X$ is defined as the smallest $x$ such $F(x) \geq p$
### Comparison

![[Quantile#Percentile vs Quantile]]

### Caution
- The above definition works for both continuous and discrete distributions and for CDFs that are not strictly increasing
- When $F$ is not strictly increasing, the ordinary inverse may not exist and there may be an interval of quantiles. The general definition using the infimum always selects a unique (lower) percentile / quantile
### Practice
- [[Lower quantile|25th percentile]]
- [[Median|50th percentile]]
- [[Upper quantile|75th percentile]]

### Example

![[Quantile#Percentile and Quantile]]
