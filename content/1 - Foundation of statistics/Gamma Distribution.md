### Concept
- *Which:* [[Continuous random variable|Continuous random variable]]
### Definition
#### Rate parameterisation
If a random variable $X$ has [[Probability density function (pdf)|pdf]] 
$$
f(x) = \begin{cases} \frac{\lambda^{\alpha}}{\Gamma(\alpha)} x^{\alpha - 1} e^{-\lambda x} & , x > 0 \\ 0 & , x \le 0 \end{cases}
$$
, then $X$ follows a **Gamma distribution**

It is denoted as $X \sim \text{Gamma}(\alpha, \lambda)$ or $X \sim \Gamma(\alpha, \lambda)$.
The parameter $\alpha$ is called the **shape parameter**; $\lambda$ is called the **rate parameter**
A Gamma distribution with an integer-valued $\alpha$ is called an **Erlang distribution**
#### Scale parameterisation
If the density is 
$$
f(x) = \frac{1}{\theta^{\alpha}\Gamma(\alpha)} x^{\alpha-1} e^{-x/\theta}
$$

then $X \sim \Gamma(\alpha,\theta)$
The parameter $\alpha$ is called the **shape parameter**; $\theta$ is called **scale parameter**
### When
- If a random variable $T_{n}$ represents the waiting time until the $n$-th occurrence of an event according to a [[Homogeneous Poisson Process|Poisson process]] with rate $\lambda$, then $X=T_{n}$ follows a **Gamma distribution** with $\alpha=n$ and rate $\lambda$
- Sums of independent [[Exponential Distribution|exponential random variables]]
- Right-skewed positive continuous measurements *e.g.* claim sizes, rainfall, service times. *Reason:* The support of every Gamma distribution is $(0,\infty)$. For every finite shape $\alpha>0$ the density is right-skewed (skewness: $\frac{2}{\sqrt{\alpha}}$); the skewness decreases as $\alpha$ grows and the distribution approaches normality, but it remains positive and continuous.
### Caution
- When $\alpha$ is non-integer, it generally does not have a direct count interpretation like “number of events”. It is the shape parameter of the Gamma distribution.
### Property
- $\theta=\frac{1}{\lambda}$
- **cdf**: $$ F(x) =  \begin{cases} 1 - \sum\limits_{k=0}^{n-1} \frac{(\lambda x)^{k} e^{-\lambda x}}{k!}, \quad x > 0 \text{ and } \alpha = n \\ \int_{0}^{x} \frac{\lambda^{\alpha}}{\Gamma(\alpha)} t^{\alpha - 1} e^{-\lambda t} \, dt, \quad x > 0 \end{cases}$$
	- *Proof:* Case 1: $\alpha$ is an integer 
		$$
		\begin{aligned} F(t) &= P(T_{n} \le t) \\ &= 1 - P(T_{n} > t) \\ &= 1-P(\text{waiting time till n-th occurrence}>t) \\ &= 1-P(\text{n-1 occurrences in [0,t]}) \\ &= 1 - P(N(t) < n) \\ &= 1 - \sum_{k=0}^{n-1} \frac{(\lambda t)^{k} e^{-\lambda t}}{k!}, \quad t > 0 \end{aligned}
		$$
- [[Moment generating function (mgf)|Moment generating function]]: $M_{X}(t) = \left(\frac{\lambda}{\lambda - t}\right)^{\alpha}$, where $t < \lambda$
- [[Population mean|Mean]]: $\mu = \frac{\alpha}{\lambda}$
- [[Population variance|Variance]]: $\sigma^{2} = \frac{\alpha}{\lambda^{2}}$
- *Rescaling:* Let $X \sim \Gamma(\alpha, \lambda)$, $Y=aX$ where $a \in \mathbb{R}^{+}$. Then $Y \sim \Gamma\left(\alpha, \frac{\lambda}{a}\right)$
- If $X_{i} \sim \text{Exp}(\lambda)$ are [[Independence of random variables|independent]], then $X_{1}+X_{2}+...+X_{n} \sim \Gamma(n, \lambda)$
### Comparison
#### Exponential distribution vs Gamma distribution
- The [[Exponential Distribution|exponential distribution]] is a special case of the Gamma distribution with $\alpha = 1$ *i.e.* $\operatorname{Gamma}(1, \lambda) \equiv \operatorname{Exponential}(\lambda)$