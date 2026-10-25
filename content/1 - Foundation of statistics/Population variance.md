### Definition
The **population variance** of a [[Random variable|random variable]] $X$ is defined as 
$$
\text{Var}(X) = \sigma^{2}=E[(X-\mu)^2]
$$
- $\mu$: [[Population mean|population mean]]

For a finite population of size $N$, 
$$
\begin{aligned} \sigma^{2} &= \frac{1}{N} \sum\limits_{i=1}^{N} (x_{i}-\mu)^{2} \end{aligned}
$$
### Interpretation
- It is a measure of spread
### Property
- 
$$
\begin{align*} \sigma^{2}  &= E\left((X - \mu)^{2}\right) \\ &= E\left(X^{2} - 2\mu X + \mu^{2}\right) \\ &= E\left(X^{2}\right) - 2\mu E(X) + \mu^{2} \\ &= E \left(X^{2}\right) - \mu^{2} \end{align*}
$$
- Let $X$ be a random variable and $a$, $c$ be two constants
$$
Var(aX + c) = a^{2}Var(X)
$$
- [[Conditional expectation|Conditional expectation]] and [[Conditional variance|conditional variance]]: $$Var(X) = E(Var(X \mid Y)) + Var(E(X \mid Y))$$
	- *Proof:* 
	$$
	\begin{align*} E(\operatorname{Var}(X \mid Y)) &= E\left\{ E(X^{2} \mid Y) - \left(E(X \mid Y)\right)^{2} \right\} \\ &= E(X^{2}) - E\left\{ \left(E(X \mid Y)\right)^{2} \right\} \\  \end{align*}
	$$