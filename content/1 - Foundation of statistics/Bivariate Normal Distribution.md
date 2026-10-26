### Definition
Two [[Random variable|random variables]] $X$ and $Y$are said to follow a **bivariate normal distribution** if their [[Joint distribution|joint pdf]] is 
$$
f(x, y) = \frac{1}{2\pi\sigma_{x}\sigma_{y}\sqrt{1 - \rho^{2}}} \exp\left\{ \frac{-1}{2(1 - \rho^{2})} \left[ \left(\frac{x - \mu_{x}}{\sigma_{x}}\right)^{2} - \frac{2\rho(x - \mu_{x})(y - \mu_{y})}{\sigma_{x}\sigma_{y}} + \left(\frac{y - \mu_{y}}{\sigma_{y}}\right)^{2} \right] \right\}
$$

- $-\infty < x < \infty$
- $-\infty < y < \infty$
- $\mu_{x}, \sigma_{x}^{2}$:  [[Population mean|mean]] and [[Population variance|variance]] of $X$
- $\mu_{y}, \sigma_{y}^{2}$:  mean and variance of $Y$
- $\rho$: the [[Population correlation coefficient|correlation coefficient]] between $X$ and $Y$
It is denoted as $$\begin{pmatrix} X \\ Y \end{pmatrix} \sim N \left[ \begin{pmatrix} \mu_{x} \\ \mu_{y} \end{pmatrix}, \begin{pmatrix} \sigma_{x}^{2} & \rho\sigma_{x}\sigma_{y} \\ \rho\sigma_{x}\sigma_{y} & \sigma_{y}^{2} \end{pmatrix} \right]$$
### Property
- The [[Marginal distribution|marginal distribution]] are [[Normal distribution|normal]]
	- $X \sim N(\mu_{x}, \sigma^{2}_{x})$
	- $Y \sim N(\mu_{y}, \sigma^{2}_{y})$
- The [[Conditional distribution|conditional distribution]] of $Y$ given $X=x$ is [[Normal distribution|normal]] 
	$$
	Y\big|_{X=x} \sim N\left( \mu_{y} + \frac{\rho\sigma_{y}}{\sigma_{x}}(x - \mu_{x}), \, (1 - \rho^{2})\sigma_{y}^{2} \right)
	$$
### Application
- **Linear regression** of $Y$ on $X$ - the best predictor of $Y$ given the value of $X$ is $$E(Y \mid X) = \mu_{y} + \frac{\rho\sigma_{y}}{\sigma_{x}}(X - \mu_{x})$$