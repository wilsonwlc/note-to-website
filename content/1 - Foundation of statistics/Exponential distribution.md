### Concept
- *Which:* [[Continuous random variable|Continuous random variable]]
### Definition
#### Rate parameterisation
If a random variable $X$ has [[Probability density function (pdf)|pdf]] 
$$
f_X(x)=
\begin{cases}  
\lambda e^{-\lambda x} & \text{if} \quad x \geq 0 \\  
0 & \text{otherwise}
\end{cases}
$$
where $\lambda > 0$ is the **rate parameter**, then $X$ follows an **Exponential distribution**
It is denoted as $X \sim \text{Exponential}(\lambda)$ or $X \sim \text{Exp}(\lambda)$
#### Scale parameterisation
$$
f_{X}(x)=  
\begin{cases}  
\frac{1}{\theta}e^{\frac{-x}{\theta}} & \text{if} \quad x \geq 0 \\  
0 & \text{otherwise}  
\end{cases}
$$
where $\theta > 0$ is the **scale parameter**
It is denoted as $X \sim \text{Exp}(\theta)$
### When
If an random variable $X$ represents the waiting time until the first occurrence in a [[Homogeneous Poisson Process|Poisson process]] with rate $\lambda$, then $X \sim \text{Exp}(\lambda)$
### Property
- *Rate and scale parameter:* $\theta=\frac{1}{\lambda}$
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
- [[Weibull distribution]]: If $X \sim \text{Exp}(\lambda)$ and $Y=X^{\frac{1}{\alpha}}$, then $Y \sim \text{Weibull}(\alpha, \lambda)$ 
- [[Pareto distribution]]: Assume $c>0$. If $X \sim \text{Exp}(\lambda)$, then $Y=ce^{X} \sim \text{Pareto}(c,\lambda)$ 
- [[Sample mean|Sample mean]]: If $X_{i} \stackrel{iid}{\sim} \text{Exp}(\lambda)$, then $\overline{X}= \frac{1}{n} \sum\limits_{i=1}^{n}X_{i} \sim \Gamma(n,n\lambda)$
### Caution
- "An exponential random variable can describe the random time elapsing between unpredictable events e.g. earthquakes". However, it is not accurate. *Reason:*
	- The exponential model can be quite poor for earthquake sequences because earthquakes are not independent events at short timescales. A large earthquake can trigger aftershocks, producing many very short waiting times. This creates clustering, which violates the assumptions of a simple Poisson process
	- "Time between earthquakes" depends enormously on how you define an earthquake catalogue — magnitude threshold, geographical region, time period, whether aftershocks are removed, etc.
### Comparison
#### Exponential distribution vs All distributions
- Among all continuous random variable with support $(0,\infty)$, the exponential distribution is the only distribution that has the memoryless property

![[Gamma distribution#Exponential distribution vs Gamma distribution]]
