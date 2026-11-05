### Definition
Let $X_{1},..., X_{n}$ be [[Independence of random variables|independent]] [[Random variable|random variables]] that have the same [[Marginal distribution|marginal distribution]] with [[Probability mass function (pmf)|pmf]] $p(x)$ or [[Probability density function (pdf)|pdf]] $f(x)$
This set of random variables $\{X_{1},..., X_{n}\}$ is called a **random sample** of size $n$ from the distribution with pmf $p(x)$ and pdf $f(x)$
### Interpretation
- $X_{1},...,X_{n}$ are **independently identically distributed (iid)** with common pmf $p(x)$ and pdf $f(x)$. They share any moments *e.g.* mean $E(X_{i})=\mu$ and variance $\text{Var}(X_{i}) = \sigma^{2}$
### Interpretation
- Assume the histogram of the underlying population resemble the shape of $f(x)$
### Practice
- *Theory:* [[Independence of random variables|Independence among the random variables]] can be justified either (1) the $X$'s are drawn with replacement or (2) there are infinite number of objects in the population. *Reality:* Neither of these two criteria is satisfied. *Solution:* 
	- If the population size $N$ is very large such that the ratio $\frac{n}{N}$ is negligible, then we can assume $X_{1},..., X_{n}$ to be approximately mutually independent
	- If $\frac{n}{N}$ is not small enough, then $X_{1},..., X_{n}$ is called a [[Simple random sample (SRS)|simple random sample (SRS)]] which is not a random sample