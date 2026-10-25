### Concept
- *When to use it:* give informative summary on the probabilistic behaviour of the random variable
### Theorem
If the [[Random variable|random variable]] $X$ has a finite [[Population mean|mean]] $\mu$ and finite [[Population variance|variance]] $\sigma^{2}$ , then for any constant $k > 0$, 
$$
\begin{align*} P(|X - \mu| \ge k\sigma) \le \frac{1}{k^{2}} \end{align*}
$$
#### Proof
By [[Markov Inequality|Markov Inequality]], 
$$
\begin{align*} P(|X - \mu| \ge k\sigma) &= \text{Pr}\left( \left| \frac{X - \mu}{\sigma} \right|^{2} \ge k^{2} \right) \\ &\le \frac{E\left((X - \mu)^{2} / \sigma^{2}\right)}{k^{2}} \\ &= \frac{1}{k^{2}} \end{align*}
$$

### Interpretation
- The probability that $X$ deviates from the mean more than 2 standard deviations is at most 0.25 or a general random variable $X$ usually takes a value within two standard deviations from the mean *i.e.* from $\mu-2\sigma$ to $\mu+2\sigma$