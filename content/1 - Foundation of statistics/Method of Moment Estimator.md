### Concept
- *Which:* [[Point estimation|Point estimation]]
- *What it does:* equate the moments of the distribution to the sample moments and then solve for the equations in terms of the parameters
### Definition
Let $\mathbf{x} = (x_{1},..., x_{n})$ be iid realisation sample from a distribution where $\theta$ is a vector of parameters
The **method of moments** (MoM) **estimator** $\hat{\theta}_{MoM}$ of $\theta=(\theta_{1},...,\theta_{k})$ is the solution to the $k$ simultaneous equations where the $j$-th [[Moment|true moment]] equals to the $j$-th [[Sample moment|sample moment]] for $j=1,...,k$ *i.e.* 
$$
\begin{align*} \mathbb{E}(X) &= \frac{1}{n} \sum_{i={1}}^{n} x_{i} \\ & \vdots \\ \mathbb{E}(X^{k}) &= \frac{1}{n} \sum_{i={1}}^{n} x_{i}^{k} \end{align*}
$$
### Caution
- $E(X^{k})$ is a function of $\theta$
- Method of moment estimators may be biased even when sample size is large
- Method of moment estimator may not have the least variance even when sample size is large
### Pros
- Although method of moment estimator may not be the best, it is easy to find and therefore it can be used as a first guess on the value of the parameters
### Example
#### One parameter
- Suppose $x_{1}, x_{2},...,x_{n}$ are iid samples from $X \sim \mathrm{Exp}(\theta)$
- *Recall:* If $X \sim \mathrm{Exp}(\theta)$, then $E(X) = \frac{1}{\theta}$
- Set the first true moment to the first sample moment 
$$
\mathbb{E}(X) = \frac{1}{\theta} = \frac{1}{n} \sum_{i = 1}^{n} x_{i}
$$
- Solving for $\theta$, we get 
$$
\hat{\theta}_{MoM} = \frac{1}{\frac{1}{n} \sum_{i = 1}^{n} x_{i}}
$$