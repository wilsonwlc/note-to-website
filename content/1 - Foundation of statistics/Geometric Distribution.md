### Concept
- *Which:* [[Discrete random variable|Discrete random variable]]
### Definition
Suppose that we perform a sequence of independent [[Bernoulli trial|Bernoulli trials]] with success probability $p$
#### Version 1
If a random variable $X$ has [[Probability mass function (pmf)|pmf]] 
$$
p(x) = P(X = x) = (1 - p)^{x-1} p
$$
where $x=1,2,...$, then $X$ follows a **Geometric Distribution**
It is denoted as $X\sim \text{Geometric} (p)$ or $X \sim \text{Geo}(p)$
#### Version 2
If a random variable $Y$ has [[Probability mass function (pmf)|pmf]] 
$$
p(y)=(1-p)^{y}p
$$
where $y=0,1,2,...$, then $Y$ follows a **Geometric Distribution**
It is denoted as $Y \sim \text{Geo}(p)$
### When
Suppose that we perform a sequence of independent [[Bernoulli trial|Bernoulli trials]] with success probability $p$
#### Version 1 - number of trials
If $X$ is the number of trials performed until the first success is obtained, then $X \sim \text{Geo}(p)$
#### Version 2 - number of failure
If $Y$ is the number of failures before the first success, then $Y \sim \text{Geo}(p)$
### Property
- $Y=X-1$
- **Memoryless property**: Conditional on no success before a-th trial, the probability of no success in the next b-th trials is equal to the unconditional probability of no success before the first b-th trial
	- *Proof:* $$ \begin{align*} P(X > a + b) &= 1 - \left(1 - (1 - p)^{a+b}\right) \\ &= (1 - p)^{a} (1 - p)^{b} \\ &= P(X > a) \operatorname{Pr}(X > b) \\ P(X > a + b \mid X > a) &= \frac{P(X > a + b, X > a)}{P(X > a)} \\ &= P(X > b) \end{align*} $$
#### Version 1
- [[Cumulative distribution function (cdf)|cdf]]: $F(x)=1-(1-p)^{x}$, where $x=1,2,...$
- [[Moment generating function (mgf)|Moment generating function]]: $M_X(t)=\frac{e^{t} p}{1 - e^{t}(1 - p)}$, where $t < -\log(1 - p)$
- [[Population mean|Mean]]: $\mu=\frac{1}{p}$
- [[Population variance|Variance]]: $\sigma^{2}=\frac{1-p}{p^{2}}$
#### Version 2
- [[Cumulative distribution function (cdf)|cdf]]: $F(y)=1 -(1-p)^{y+1}$, where $y=0,1,2,...$
- [[Moment generating function (mgf)|Moment generating function]]: $M_{Y}(t) = \frac{p}{1 - e^{t}(1 - p)}$ where $t < -\log(1 - p)$
- [[Population mean|Mean]]: $\mu = \frac{1-p}{p}$
- [[Population variance|Variance]]: $\sigma^{2} = \frac{1-p}{p^{2}}$