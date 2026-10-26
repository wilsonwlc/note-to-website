### Concept
- *Which:* [[Discrete random variable|Discrete random variable]]
### Definition
If a random variable $X$ has [[Probability mass function (pmf)|pmf]] $$p(x) = P(X = x) = \frac{e^{-\theta} \theta^{x}}{x!}$$ where $x = 0,1,2,...$, then $X$ follows a **Poisson distribution**
It is denoted by $X \sim \text{Poisson}(\theta)$

### When
If $\{N(t):t\geq 0\}$ be a [[Homogeneous Poisson Process|Poisson process]] with rate $\lambda > 0$, then  $X=N(t)$  for any fixed $t>0$ follows a Poisson distribution with parameter $\theta = \lambda t$ and pmf 
$$
p(x)=P(N(t)=x)= \frac{e^{-\lambda t}(\lambda t)^{x}}{x!}
$$
where $x = 0,1,2,...$  
### Property
- [[Cumulative distribution function (cdf)|cdf]]: $F(x) = \sum_{i=0}^{x} \frac{e^{-\theta} \theta^{i}}{i!}$, where $x = 0,1,2,...$
- [[Moment generating function (mgf)|Moment generating function]]: $M_{X}(t)=e^{-\theta} \exp(\theta(e^{t} - 1))$  for all $t$
- [[Population mean|Mean]]: $\mu = \theta$
- [[Population variance|Variance]]:$\sigma^{2} = \theta$
- If $X\sim \text{Poisson}(\theta)$, then $P(X = i+1) = \frac{\theta}{i+1} P(X = i)$
- [[Approximating Binomial Distribution using Poisson Distribution]]
### Interpretation
- The constant $\lambda$ can be interpreted as the average number of occurrences per unit time interval. 
	- *Reason:* $E(N(t)) = \lambda t \implies E\left(\frac{N(t)}{t}\right) = \lambda$
	- *Caution:* The value of $\lambda$ depends on the time unit used *i.e.* the unit in which time is measured
### Example
- Number of misprints on a page of a book
- Number of people in a community living to 100 years of age
- Number of wrong telephone numbers that are dialled in a day
- Number of packages of dog biscuits sold in a particular store each day
- Number of customers entering a post office on a given day
- Number of vacancies occurring during a year in the Supreme Court
- Number of $\alpha$-particles discharged in a fixed period of time from some radioactive material
- Number of earthquakes occurring during some fixed time span
- Number of wars per year
- Number of electrons emitted from a heated cathode during a fixed time period
- Number of deaths in a given period of time of the policyholders of a life insurance company
- Number of flaws in a certain type of drapery material
- Number of claims on a large group of insurance policies