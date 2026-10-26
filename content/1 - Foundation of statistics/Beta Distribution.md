### Concept
- *Which:* [[Continuous random variable|Continuous random variable]]
### Definition
If $X$ is a positive [[Random variable|random variable]] with **pdf** with 
$$
f(x) = \begin{cases} \dfrac{\Gamma(\alpha + \beta)}{\Gamma(\alpha)\Gamma(\beta)} x^{\alpha - 1}(1 - x)^{\beta - 1} & , \, 0 < x < 1 \\ 0 & , \, \text{otherwise} \end{cases}
$$

where $\alpha$ and $\beta$ are positive numbers, then $X$ follows a **Beta distribution** 
It is denoted as $X \sim \text{Beta}(\alpha, \beta)$
### When
- A random quantity distributed within a finite interval
### Property
- [[Probability density function (pdf)|pdf]] in term of [[Beta function]]: 
	$$
	f(x) = \begin{cases} \dfrac{1}{B(\alpha, \beta)} x^{\alpha - 1}(1 - x)^{\beta - 1} & , \, 0 < x < 1 \\ 0 & , \, \text{otherwise} \end{cases}
	$$
- [[Population mean|Mean]]: $E(X) = \frac{\alpha}{\alpha + \beta}$
- [[Population variance|Variance]]: $\operatorname{Var}(X) = \frac{\alpha\beta}{(\alpha + \beta)^{2}(\alpha + \beta + 1)}$
- When $\alpha = \beta = 1$, the beta distribution becomes the [[Uniform Distribution|uniform distribution]], $U(0,1)$