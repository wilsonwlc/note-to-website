### Concept
Let $Y_{i} \overset{iid}{\sim} \operatorname{Poisson}(\theta)$ and $W \sim \text{Poisson}(\lambda)$
Then, as $n \rightarrow \infty$, 
$$
\frac{W-\lambda}{\sqrt{\lambda}} \xrightarrow{L} N(0,1)
$$
#### Proof
- $E(Y_{i}) = \theta$ and $\operatorname{Var}(Y_{i}) = \theta$
- $X = \sum\limits_{i=1}^{n} Y_{i} \sim \text{Poisson}(n\theta)$, $E(X) = n\theta$ and $\operatorname{Var}(X) = n\theta$
- The sample mean of $Y_{i}$'s can be written as $\overline{Y}_{n}=\frac{X}{n}$
- By [[Central Limit Theorem (CLT)|CLT]], as $n\rightarrow \infty$, $\frac{\sqrt{n}\left(\overline{Y}_{n}-\theta\right)}{\sqrt{\theta}} = \frac{X-n\theta}{\sqrt{n\theta}} = \frac{X-E(X)}{\sqrt{\operatorname{Var}(X)}} \xrightarrow{L} N(0,1)$
- As $n\rightarrow \infty$, $\frac{W-\lambda}{\sqrt{\lambda}} \xrightarrow{L} N(0,1)$ if $W \sim \text{Poisson}(\lambda)$
### Practice
- The approximation will be quite well when $n \geq 10$
- Use [[Continuity correction|continuity correction]] to have more accurate result