### Concept
- *Which:* [[Discrete random variable|Discrete random variable]]
### Definition
If a random variable $X$ has [[Probability mass function (pmf)|pmf]] $$p(x) = P(X = x) = \binom{n}{x} p^{x}(1 - p)^{n-x}$$ where $x = 0, 1,..., n$, then $X$ follows a **Binomial distribution**
It is denoted as $X \sim b(n,p)$
### When
- Given $n$ independent [[Bernoulli trial|Bernoulli trials]], each with success probability $p \in[0,1]$. if a random variable $X$ counts the total number of successes across those trials, then $X\sim b(n,p)$ 
### Assumption
- The $n$ Bernoulli trials have the same success probability $p$
- The trials are independent *i.e.* the success probability of any trial is not affected by the outcomes of other trials
### Property
- [[Cumulative distribution function (cdf)|cdf]]: $F(x) = P(X \le x) = \sum\limits_{i=0}^{x} \binom{n}{i} p^{i} (1-p)^{n-i}$ where $x = 0, 1,..., n$
- [[Moment generating function (mgf)]]: $M_{X}(t)=(e^{t}p+1-p)^{n}$ for all $t$
- [[Population mean|Mean]]: $\mu=np$
	- *Proof:* **Binomial theorem**
- [[Population variance|Variance]]: $\sigma^{2}=np(1-p)$
	- *Proof:* **Binomial theorem**
- When $n$ is equal to 1, $b(1, p)$ is just the [[Bernoulli Distribution|Bernoulli distribution]]
- $X$ can be viewed as a sum of independent Bernoulli random variables $X=\sum\limits_{i=1}^{n}Y_{i}$, where $Y_{i} \overset{iid}{\sim} b(1, p)$
- If $X\sim b(n,p)$, then $$P(X = k+1) = \frac{p}{1-p} \frac{n-k}{k+1} P(X = k)$$
- If $X \sim b(n,p)$, then $P(X =k)$ first increases monotonically and then decreases monotonically, reaching its largest value when $k$ is the largest integer less than or equal to $(n+1)p$