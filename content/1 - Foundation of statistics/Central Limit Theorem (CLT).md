### Concept
- *When:* approximate for large sample cases
### Lemma
Let $Z_{1},Z_{2},...$ be a sequence of [[Random variable|random variables]] having [[Moment generating function (mgf)|mgf]] $M_{Z_{n}}(t)$ and let $Z$ be a random variable having mgf $M_{Z}(t)$. 
If $\lim_{n \rightarrow \infty}(t)=M_{Z}(t)$ for all $t$, then $$Z_{n} \xrightarrow{L} Z$$
- A more general proof of the CLT uses the so-called **characteristic function** (which always exists) and does not require the existence of the moment generating function.
### Theorem
Let $\overline{X}_{n}=\frac{1}{n} \sum\limits_{i=1}^{n}X_{i}$ be the [[Sample mean|sample mean]] of a sequence of independent and identically distributed random variables $X_{1},X_{2},..,X_{n}$ from a distribution with finite [[Population mean|mean]] $E(X_{i})=\mu$ and [[Population variance|variance]] $\operatorname{Var}(X_{i}) = \sigma^{2}$. 
Then  
$$
\lim_{n \to \infty} P\left( \frac{\sqrt{n}\left( \overline{X}_{n} - \mu \right)}{\sigma} \le x \right) = \Phi(x)
$$
 - $-\infty < x <\infty$
### Interpretation
- $Z_{n} = \frac{\sqrt{n}\left( \overline{X}_{n} - \mu \right)}{\sigma}$ converges in distribution to the [[Normal distribution|standard normal distribution]]. It is denoted as *i.e.* as $n \rightarrow \infty$,$$Z_{n} = \frac{\sqrt{n}\left( \overline{X}_{n} - \mu \right)}{\sigma} \xrightarrow{L} N(0,1)$$
- The [[Sampling distribution|sampling distribution]] of $\overline{X}_{n}=\frac{1}{n} \sum\limits_{i=1}^{n}X_{i}$ can be approximated by $N(\mu, \frac{\sigma^{2}}{n})$. *Reason:* $Z_{n} = \frac{\overline{X}_{n} - \mu}{\frac{\sigma}{\sqrt{n}}}$ is the **standard score**. This is called **normal approximation**
### Extension
- **Lindeberg-Feller Theorem**
### Application
- [[Approximation to Binomial from Normal|Approximation to Binomial from Normal]]
- [[Approximation to Poisson from Normal|Approximation to Poisson from Normal]]
### Practice
- There is no single magical sample size that guarantees satisfactory normal approximation
	- If a population is fairly symmetrical, small sample sizes usually suffice. *Reason:* Using [[Edgeworth expansion|Edgeworth expansion]] to construct higher order error terms, $$|F_{n}(x) - \Phi(x)| = \phi(x) \left( \frac{\gamma(x^{2} - 1)}{6\sqrt{n}} + \frac{(\tau - 3)(x^{3} - 3x)}{24n} + \frac{\gamma^{2}(x^{5} - 10x^{3} + 15x)}{72n} + \dots \right)$$where $F_{n}(x)$ is [[Cumulative distribution function (cdf)|cdf]] of $\frac{\sqrt{n}(\overline{X} - \mu)}{\sigma}$, $\gamma = \frac{E((X - \mu)^{3})}{\sigma^{3}}$ is the **skewness**, $\tau = \frac{E((X - \mu)^{4})}{\sigma^{4}}$is the **kurtosis**, the first and second order error terms would vanish if $\gamma = 0$ and $\tau =3$. This mean underlying distribution is symmetric and has peakedness close to the normal distribution. The error term have order $O(n^{\frac{-3}{2}})$
	- For strongly skewed populations (e.g. Chi-Square), $n$ may need to be quite large for the sampling distribution to be approximately normal. 
	- For many distributions that arise in practical situations, relatively small sample size such as 30 is sufficiently large for the normal approximation to hold. Do know, however, that there are exceptions