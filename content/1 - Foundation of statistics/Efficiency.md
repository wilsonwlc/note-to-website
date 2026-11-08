### Motivation
- If an [[Point estimation|estimator]] $\hat{\theta}_{1}$ is frequently closer to $\theta$ than another estimator $\hat{\theta}_{2}$ in repeated samples of the same size, then $\hat{\theta}_{1}$ should be preferred to $\hat{\theta}_{2}$ even when $\hat{\theta}_{1}$ is [[Bias|biased]]
### Definition
Suppose there are 2 estimators $\hat{\theta}_{1}$ and $\hat{\theta}_{2}$ of a parameter $\theta$. 
The **efficiency** of $\hat{\theta}_{1}$ compared to $\hat{\theta}_{2}$ is defined as 
$$
\mathit{eff}(\hat{\theta}_{1}, \hat{\theta}_{2}) = \frac{\mathit{MSE}(\hat{\theta}_{2})}{\mathit{MSE}(\hat{\theta}_{1})}
$$

- MSE is the [[Mean Squared Error (MSE)|mean squared error]]
### Interpretation
- The estimator $\hat{\theta}_{1}$ is said to be more efficient than the estimator $\hat{\theta}_{2}$ for estimating $\theta$ if $\mathit{eff}(\theta_{1}, \theta_{2}) \geq 1$ for all values of $\theta$ and provided that the strict inequality holds for at least one value of $\theta$ 
	- *i.e.* $\hat{\theta}_{1}$ has smaller or equal variance (or MSE) than $\hat{\theta}_{2}$ for every possible true value of $\theta$ *AND* there exists at least one value of $\theta$ where $\hat{\theta}_{1}$ has strictly smaller MSE. The second condition is to ensure $\hat{\theta}_{1}$ is strictly better somewhere
### Property
- If the variance of an unbiased estimator $\hat{\theta}$ is equal to the [[Cramér-Rao Inequality|Cramér-Rao Lower Bound]], then $\hat{\theta}$ is an [[Efficiency|efficient]] estimator
- Every efficient unbiased estimator is a [[UMVUE|UMVUE]]. However, a UMVUE need not be efficient.
### Example
- Given a random sample $X_{1}, X_{2}, \dots, X_{n} \overset{iid}{\sim} U(0, \theta)$
- We have the following estimators of $\theta$
- $\hat{\theta}_{1} = 2 \overline{X}$ has MSE $\frac{\theta^{2}}{3n}$
- $\hat{\theta}_{2} = \max(X_{1}, X_{2}, \dots, X_{n})$ has MSE $\frac{2\theta^{2}}{(n+1)(n+2)}$
- $\hat{\theta}_{3} = \frac{n+1}{n} \max(X_{1}, X_{2}, \dots, X_{n})$ has MSE $\frac{\theta^{2}}{n(n+2)}$
- $\mathit{eff}(\hat{\theta}_{2}, \hat{\theta}_{1}) = \frac{\mathit{MSE}(\hat{\theta}_{1})}{\mathit{MSE}(\hat{\theta}_{2})} = \frac{(n+1)(n+2)}{6n}$ is greater than 1 for any value of $\theta$ when $n>2$
- $\mathit{eff}(\hat{\theta}_{3}, \hat{\theta}_{2}) = \frac{\mathit{MSE}(\hat{\theta}_{2})}{\mathit{MSE}(\hat{\theta}_{3})} = \frac{2n}{n+1}$ is greater than 1 for any value of $\theta$ when $n>1$
### Comparison
![[Cramér-Rao Inequality#UMVUE vs Efficient Estimator]]