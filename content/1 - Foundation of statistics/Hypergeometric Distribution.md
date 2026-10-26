### Concept
- *Which:* [[Discrete random variable|Discrete random variable]]
### Definition
If a random variable $X$ has [[Probability mass function (pmf)|pmf]] 
$$
p(x) = P(X = x) = \frac{\binom{m}{x} \binom{N - m}{n - x}}{\binom{N}{n}}
$$
where $\max(n - (N - m), 0) \le x \le \min(n, m)$, then $X$ follows a **hypergeometric distribution**
It is denoted as $X \sim \text{Hypergeometric}(N,m, n)$ or $X \sim H(N,m,n)$
### When
Suppose we have a population of $N$ objects with $m$ objects as type I and $(N- m)$ objects as type II. 
A sample of $n$ objects is randomly drawn without replacement from the population. 
If $X$ is the number of type I objects in the sample, then $X \sim H(N,m,n)$
### Property
- [[Population mean|Mean]]: $\mu = np$, where $p=\frac{m}{N}$ represents the proportion of type I objects in the population
- [[Population variance|Variance]]: $\sigma^{2} = \frac{N - n}{N - 1} np(1 - p)$, where $p=\frac{m}{N}$ represents the proportion of type I objects in the population
### Comparison
#### Binomial distribution vs Hypergeometric distribution
##### Replacement
- [[Binomial distribution|Binomial distribution]]: sampling with replacement
- Hypergeometric distribution: sampling without replacement
- Hence, the hypergeometric distribution can be regarded as a finite population counterpart of the binomial distribution
##### Variance
- The binomial distribution has variance $np(1-p)$
- The hypergeometric distribution has variance $\frac{N - n}{N - 1} np(1 - p)$
- $\left(\frac{N - n}{N - 1}\right)$ is called **finite population correction factor**
### Practice
- If the population is very large, then sampling with or without replacement will have negligible difference. Therefore for large $N$, the hypergeometric distribution can be well approximated by the binomial distribution.