### Concept
- *Which:* [[Discrete random variable|Discrete random variable]]
### Definition
Suppose we perform a sequence of independent [[Bernoulli trial|Bernoulli trials]] with success probability $p$
#### Version 1
If a random variable $X$ has [[Probability mass function (pmf)|pmf]] $$p(x) = P(X = x) = \binom{x - 1}{r - 1} p^{r} (1 - p)^{x - r}$$where $x=r,r+1,r+2,...$, then $X$ follows a **negative binomial distribution**
It is denoted as $X \sim nb(r,p)$
#### Version 2
If a random variable $Y$ has [[Probability mass function (pmf)|pmf]] $$\begin{align*} p(y) &= \binom{y + r - 1}{r - 1} p^{r} (1 - p)^{y} \\ &= \binom{y + r - 1}{y} p^{r} (1 - p)^{y} \end{align*}$$ where $y=0,1,2,...$, then $Y$ follows a **negative binomial distribution**
It is denoted as $Y \sim nb(r,p)$
### When
Suppose we perform a sequence of independent [[Bernoulli trial|Bernoulli trials]] with success probability $p$
#### Version 1
If $X$ represents the number of trials until a total of $r$ successes are accumulated (*i.e.* there are total $X$ trials to produce $r$ successes, and the $X$-th trial is a success), then $X \sim nb(r,p)$
#### Version 2
If $Y$ represents the number of failures before the $r$-th success, then $Y \sim nb(r,p)$
### Property
- $Y=X-r$
#### Version 1
- [[Cumulative distribution function (cdf)|cdf]]: $F(x) = \sum_{i=r}^{x} \binom{i - 1}{r - 1} p^{r} (1 - p)^{i - r}$, where $x=r,r+1,r+2,...$
- [[Moment generating function (mgf)|Moment generating function]]: $M_{X}(t)= \left[\frac{e^{t} p}{1 - e^{t}(1 - p)}\right]^{r}$, where $t<-\log(1-p)$
- [[Population mean|Mean]]: $\mu = \frac{r}{p}$
- [[Population variance|Variance]]: $\sigma^{2} = \frac{r(1 - p)}{p^{2}}$
- **Geometric distribution**: $nb(1, p) \equiv \operatorname{Geo}(p)$
#### Version 2
- [[Moment generating function (mgf)|Moment generating function]]: $M_{Y}(t) = \left( \frac{p}{1 - e^{t}(1 - p)} \right)^{r}$, where $t < -\ln(1 - p)$
- [[Population mean|Mean]]: $\mu = \frac{r(1 - p)}{p}$
- [[Population variance|Variance]]: $\sigma^{2} = \frac{r(1 - p)}{p^{2}}$
### Application
- [[Inverse binomial sampling]]