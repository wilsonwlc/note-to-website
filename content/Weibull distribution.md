### Definition
#### Shape-scale parameterisation
If a random variable $X$ has [[Probability density function (pdf)|pdf]] 
$$
f(x) = \left\{ \begin{array}{ll} \frac{\alpha}{\beta^{\alpha}}x^{\alpha-1} \exp\{ -(\frac{x}{\beta})^{\alpha} \}, & x \geq 0  \\ 0 & \text{otherwise} \end{array} \right.$$
- $\alpha> 0$: **shape parameter** 
- $\beta > 0$: **scale parameter**
It is denoted as $X \sim \text{Weibull}(\alpha, \beta)$  
#### Shape-rate parameterisation
$$
\begin{align*} f(x) &= \alpha \lambda x^{\alpha-1} \exp(-\lambda x^{\alpha})\end{align*}
$$
- $\alpha> 0$: **shape parameter** 
- $\lambda > 0$: **rate parameter**
It is denoted as $X \sim \text{Weibull}(\alpha, \lambda)$
### Property
- $\lambda=\frac{1}{\beta^{\alpha}}$
- [[Cumulative distribution function (cdf)|cdf]]: 
	- For shape-scale parameterisation, $$F(x) = \left\{ \begin{array}{ll} 1-\exp\{ -(\frac{x}{\beta})^{\alpha} \} & x \geq 0 \\ 0 & \text{otherwise} \end{array} \right.$$
	- For shape-rate parameterisation, $F(x) = 1-\exp(-\lambda x^{\alpha})$
- When $\alpha=1$, $\text{Weibull}(1,\lambda) \equiv \text{Exp}(\lambda)$  where $\lambda$ is the rate parameter