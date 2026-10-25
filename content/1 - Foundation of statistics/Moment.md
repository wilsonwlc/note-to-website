### Definition
Let $X$ be a [[Random variable|random variable]], $r \in \mathbb{N}$, $b \in \mathbb{R}$
- The r-th **moment** of $X$ / **raw moment** is 
$$
\mu'_{r} = E[X^{r}]
$$
- The r-th **moment** of $X$ about $b$ is 
$$
\mu_{r}(b) = E[(X-b)^{r}]
$$
- The r-th moment of $X$ about $\mu$ is called **r-th central moment** and denoted by $\mu_{r}$
- The r-th **standardised central moment** is 
$$
\gamma_{r} = E\left[\left(\frac{X - \mu_{X}}{\sigma_{X}}\right)^{r}\right]
$$
### Special case
- The [[Population mean|mean]] $E(x)$ is the 1st moment of $X$
- The [[Population variance|variance]] $\sigma^{2}$ is the 2nd central moment of $X$
### Comparison
#### Central moment vs Raw moment
- $\mu_{1} = 0$
- $\mu_{2} = -{\mu'_{1}}^{2} + \mu'_{2}$
- $\mu_{3} = 2 {\mu'_{1}}^{3} - 3 \mu'_{1} \mu'_{2} + \mu'_{3}$
- $\mu_{4} = -3 {\mu'_{1}}^{4} + 6 {\mu'_{1}}^{2} \mu'_{2} - 4 \mu'_{1} \mu'_{3} + \mu'_{4}$
- $\mu_{5} = 4 {\mu'_{1}}^{5} - 10 {\mu'_{1}}^{3} \mu'_{2} + 10 {\mu'_{1}}^{2} \mu'_{3} - 5 \mu'_{1} \mu'_{4} + \mu'_{5}$
#### Central moment vs Cumulant
- $\mu_{2} = \kappa_{2}$
- $\mu_{3} = \kappa_{3}$
- $\mu_{4} = 3 \kappa_{2}^{2} + \kappa_{4}$
- $\mu_{5} = 10 \kappa_{2} \kappa_{3} + \kappa_{5}$
#### Raw moment vs Cumulant
- $\mu'_{1} = \kappa_{1}$
- $\mu'_{2} = \kappa_{1}^{2} + \kappa_{2}$
- $\mu'_{3} = \kappa_{1}^{3} + 3 \kappa_{1} \kappa_{2} + \kappa_{3}$
- $\mu'_{4} = \kappa_{1}^{4} + 6 \kappa_{1}^{2} \kappa_{2} + 3 \kappa_{2}^{2} + 4 \kappa_{1} \kappa_{3} + \kappa_{4}$
- $\mu'_{5} = \kappa_{1}^{5} + 10 \kappa_{1}^{3} \kappa_{2} + 15 \kappa_{1} \kappa_{2}^{2} + 10 \kappa_{1}^{2} \kappa_{3} + 10 \kappa_{2} \kappa_{3} + 5 \kappa_{1} \kappa_{4} + \kappa_{5}$

