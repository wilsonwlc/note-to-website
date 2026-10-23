## Probability density function (pdf)
### Definition
If $F$ is differentiable, then $$f(x) = \lim_{t \rightarrow 0} \frac{P(X \le x+t) - P(X \le x)}{t} = \frac{d}{dx} F(x)$$
### Property
- $f(x) \geq 0$ for all $x$
- $\int_{-\infty}^{\infty} f(x) = 1$
- $P(X \in B) = \int_{B}f(x)dx$ where $B$ is any subset of $\mathbb{R}$
- $P(X = a) = \int_{a}^{a} f(x) dx = 0$ for all $a$
- $P(a < X \le b) = \int_{a}^{b} f(x) dx = F(b) - F(a)$
- $P(a \le X \le b) = P(a \le X < b) = P(a < X < b)$
### Caution
- $f(x)$ is NOT a [[Probability|probability]]
### Interpretation
- $f(a)$ is a measure of how likely it is that the random variable will be near $a$. *Reason:* For a small $\epsilon >0$, $$\begin{align*} P\left(a - \frac{\varepsilon}{2} \le X \le a + \frac{\varepsilon}{2}\right) &= \int_{a - \frac{\varepsilon}{2}}^{a + \frac{\varepsilon}{2}} f(x) dx \\ &\approx \varepsilon f(a)\end{align*}$$ 
