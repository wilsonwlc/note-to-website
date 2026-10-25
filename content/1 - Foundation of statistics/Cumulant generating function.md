### Definition
$$
R(t) = \log{M(t)}
$$
- $M(t)$: [[Moment|moment]]
### Property
- $R'(0) = \mu$
	- *Proof:* $R'(t) = \frac{M'(t)}{M(t)} \Rightarrow R'(0) = \frac{M'(0)}{M(0)} = \mu$
- $R''(0) = \sigma^{2}$
	- *Proof:* 
	$$
	\begin{align*} R''(t) &= \frac{M(t)M''(t) - M'(t)M'(t)}{[M(t)]^{2}} \\ R''(0) &= \frac{M(0)M''(0) - [M'(0)]^{2}}{[M(0)]^{2}} = \sigma^{2} \end{align*}
	$$
- $R'''(0) = E[(X-\mu)^{3}]$
### Caution
- $R^{(4)}(0) \neq E\left((X - \mu)^{4}\right)$
- $R^{(5)}(0) \neq E\left((X - \mu)^{5}\right)$