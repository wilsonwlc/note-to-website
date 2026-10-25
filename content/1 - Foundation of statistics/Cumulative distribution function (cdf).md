### Definition

$$
F(x) = P(X \le x)
$$
#### Discrete random variable
The cumulative distribution function of the [[Discrete random variable|discrete random variable]] is defined as 
$$
F(x) = P(X \le x) = \sum_{t \le x} p(t)
$$
- $-\infty < x < \infty$
#### Continuous random variable
$$
F(x) = P(X\leq x) = \int_{-\infty}^{x} f(t) dt
$$
### Property
- $F(x)$ is non-decreasing *i.e.* if $a \leq b$, then $F(a) \leq F(b)$
- $F(-\infty) = \lim_{b\rightarrow -\infty} F(b)=0$
- $F(\infty) = \lim_{b\rightarrow \infty} F(b)=1$
- $F$ is right continuous *i.e*. for any $b$ and any decreasing sequence $\{b_{n}, n\geq 1\}$ that converges to $b$, 
$$
\lim_{n\rightarrow \infty} F(b_{n})=F(b)
$$
- If $X$ is a [[Continuous random variable|continuous random variable]], the distribution function $F$ is continuous everywhere
### Concept
- *When to use it:* describe probability models. The cdf of $X$ completely specifies the random behaviour of $X$
### Interpretation
- $F(x)$ is a step-function if $X$ is a discrete random variable. The step size at the point $x \in X(\Omega)$ is $p(x) = P(X=x)$