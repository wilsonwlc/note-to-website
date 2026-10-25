### Concept
- *Which:* [[Discrete random variable|Discrete random variable]]
### Definition
If a random variable $X$ has [[Probability mass function (pmf)|pmf]] $$p(x) = p^{x}(1-p)^{1-x}$$where $x=0,1$, then $X$ follows **Bernoulli distribution** 
It is denoted as $X\sim \text{Bernoulli}(p)$
### When
Given a **Bernoulli trial** with 2 possible outcomes - "success" (coded as 1) and "failure" (coded as 0) - and success probability $p \in [0,1]$, if a random variable $X$ represents the outcome of the trial *i.e.* 
$$
\begin{align*} P(X=1) &= p \\ P(X=0) &= 1-p \end{align*}
$$
then $X\sim \text{Bernoulli}(p)$
### Property
- [[Population mean|Mean]]: $\mu=p$
- $E(X^{2})=p$
- [[Population variance|Variance]]: $\sigma^{2}= p(1-p)$