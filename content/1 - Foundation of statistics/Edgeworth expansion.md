### Concept
- Aka **Edgeworth series**
- *What is it:* an asymptotic series
- *What it does:* approximate the distribution (or density) of a standardised sum of independent and identically distributed (i.i.d.) random variables more accurately
- *How:* use higher-order terms involving [[Cumulant|cumulants]] (or [[Moment|moments]])
### Definition
Let $X_{1}, X_{2},...$ be iid random variable with mean $\mu$, variance $\sigma^{2}>0$ 
Define $Z_{n} = \frac{\sqrt{n}\left( \overline{X}_{n} - \mu \right)}{\sigma}$
Under suitable moment and smoothness conditions
$\begin{align*} F_{n}(x) &= P(Z_{n} \le x) \\ &= \Phi(x) + n^{\frac{-1}{2}} p_{1}(x) \phi(x) + n^{-1} p_{2}(x) \phi(x) + \dots + n^{\frac{-j}{2}} p_{j}(x) \phi(x) + \dots\\ &= \Phi(x) + \sum_{k=1}^{m} n^{\frac{-k}{2}} p_{k}(x) \phi(x) + o(n^{\frac{-m}{2}}) \end{align*}$
- $\Phi(x)$: Standard [[Normal distribution|normal]] CDF
- $\phi(x)$: Standard normal density
- $\lambda_{r}=\frac{\kappa_{r}}{\sigma_{r}}$ : Standardised cumulants for $r \geq 3$, where $\kappa_{r}$ is the r-th cumulant of $X_{i}$
- $p_{k}(x)$: polynomials of degree $3k-1$
	- $p_{1}(x) = -\frac{1}{6} \lambda_{3} (x^{2} - 1)$
	- $p_{2}(x) = -x \left\{ \frac{1}{24} \lambda_{4} (x^{2} - 3) + \frac{1}{72} \lambda_{3}^{2} (x^{4} - 10x^{2} + 15) \right\}$