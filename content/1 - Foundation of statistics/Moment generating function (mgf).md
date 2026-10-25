### Definition
Let $X$ be a [[Random variable|random variable]]
The **moment generating function** of $X$ is 
$$
M_{X}(t) = E(e^{tX})
$$
### Property
- The **domain** of $M_{x}(t)$: $t \in \mathbb{R}$ such that $e^{tX}$ has finite [[Expectation|expected value]]
- $M^{(r)}(0) = \left. \frac{d^{r}(M(t))}{dt^{r}} \right|_{t=0} = E(X^{r})$
	- *When:* generating [[Moment|moments]]
- **Uniqueness theorem**: Moment generating function uniquely characterises the distribution *i.e.* If $X$ and $Y$ have the same moment generating function, then they must have the same distribution
	- *When:* find and identify the distribution of random variables
- If $X$ and $Y$ are [[Independence of random variables|independent]], then 
	- $M_{X+Y}(t) = M_{X}(t) + M_Y(t)$
	- $M_{aX+bY}(t) = M_{X}(at) M_{Y}(bt)$
### Example
- $M(0) = 1$
	- *Proof:* $M(t) = E(e^{tX}) = \int_{-\infty}^{\infty} e^{tx} f(x) dx$
- $M'(0) = E(X)$
	- *Proof:* 
	$$
	\begin{align*} M'(t) &= \int_{-\infty}^{\infty} x e^{tx} f(x) dx \\ M'(0) &= \int_{-\infty}^{\infty} x f(x) dx = E(X) \end{align*}
	$$
- $M''(0) = E(X^{2})$
	- *Proof:* 
	$$
	\begin{align*} M''(t) &= \int_{-\infty}^{\infty} x^{2} e^{tx} f(x) dx \\ M''(0) &= \int_{-\infty}^{\infty} x^{2} f(x) dx = E(X^{2}) \end{align*}
	$$