### Definition
The **Fisher Information** of a [[Random variable|random variable]] $X$ with [[Probability density function (pdf)|pdf]] or [[Probability mass function (pmf)|pmf]] $f(x;\theta)$ is defined as 
$$
\begin{align*} I(\theta) &= \mathbb{E}\left[ \left( \frac{\partial}{\partial \theta} \log f(X; \theta) \right)^{2} \right] \\ &= -\mathbb{E}\left[ \frac{\partial^{2}}{\partial\theta^{2}} \log f(X; \theta) \right] \end{align*}
$$
### Caution
- The second equality requires the following conditions
	- $\log f(x; \theta)$ is twice differentiable with respect to $\theta$
	- Certain additional **regularity** conditions
### Interpretation
- It measures the amount of information that the observed $X$ carried about the unknown parameter $\theta$
### When
- [[Cramér-Rao Inequality]]
- [[Maximum likelihood estimation (MLE)|Maximum likelihood estimator (MLE)]]