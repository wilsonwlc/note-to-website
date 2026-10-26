### Concept
- *Which:* [[Continuous random variable|Continuous random variable]]
### Definition
If a random variable $X$ has [[Probability density function (pdf)|pdf]] 
$$
f(x)=\lambda e^{-\lambda x}
$$
for $x > 0$, then $X$ follows **Exponential distribution**
It is denoted as $X \sim \text{Exponential}(\lambda)$ or $X \sim \text{Exp}(\lambda)$
### When
If an random variable $X$ represents the waiting time until the first occurrence in a [[Homogeneous Poisson Process|Poisson process]] with rate $\lambda$, then $X \sim \text{Exp}(\lambda)$
### Property
- [[Cumulative distribution function (cdf)|cdf]]: $$F(x) = \begin{cases} 1 - e^{-\lambda x} & , x > 0 \\ 0 & , x \le 0 \end{cases}$$
	- *Proof:* 
		- For $x \leq 0$, $F(x)=P(X \leq x)=0$
		- For $x>0$, 
			$$
			\begin{aligned} F(x) &= P(X \le x) \\ &= 1 - P(X > x) \\ &= 1 - P(\text{waiting time > } x) \\ &= 1 - P(\text{no occurrence in} [0, x]) \\ &= 1 - P(N(x) = 0) \\ &= 1 - e^{-\lambda x} \end{aligned}
			$$
- [[Moment generating function (mgf)|Moment generating function]]: $M_{X}(t) = \frac{\lambda}{\lambda - t}$, where $t < \lambda$
- [[Population mean|Mean]]: $\mu=\frac{1}{\lambda}$
- [[Population variance|Variance]]: $\sigma^{2}=\frac{1}{\lambda^{2}}$
- **Memoryless property**: The process starts afresh at any point of observation 
	- *i.e.* An event hasn’t occurred in the past doesn’t alter the distribution of arrival time in the future
	- *Proof:* For any $a, b>0$, 
		$$
		\begin{aligned} P(X > a + b) &= 1 - F(a + b) \\ &= e^{-\lambda(a + b)} \\ &= e^{-\lambda a} e^{-\lambda b} \\ &= (1 - F(a))(1 - F(b)) \\ &= P(X > a)P(X > b) \end{aligned}
		$$
### Caution
- "An exponential random variable can describe the random time elapsing between unpredictable events e.g. earthquakes". However, it is not accurate. *Reason:*
	- The exponential model can be quite poor for earthquake sequences because earthquakes are not independent events at short timescales. A large earthquake can trigger aftershocks, producing many very short waiting times. This creates clustering, which violates the assumptions of a simple Poisson process
	- "Time between earthquakes" depends enormously on how you define an earthquake catalogue — magnitude threshold, geographical region, time period, whether aftershocks are removed, etc.
### Comparison
#### Exponential distribution vs All distributions
- Among all continuous random variable with support $(0,\infty)$, the exponential distribution is the only distribution that has the memoryless property

![[Gamma Distribution#Exponential distribution vs Gamma distribution]]
