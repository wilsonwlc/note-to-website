### Concept
- Aka **double exponential distribution**
### Definition
If a random variable $X$ has [[Probability density function (pdf)|pdf]] 
$$
f(x) = \frac{1}{2b} \exp\left( -\frac{|x - \mu|}{b} \right)
$$
- $\mu$ is the **location parameter**
- $b>0$ is the **scale parameter**

then it follows **Laplace distribution**. It is denoted as $X \sim \text{Laplace}(\mu, b)$
### Property
- [[Moment generating function (mgf)|Moment generating function]]: $$M_{X}(t)=\frac{\exp(\mu t)}{1 - b^2 t^2}$$ for $|t|<\frac{1}{b}$
