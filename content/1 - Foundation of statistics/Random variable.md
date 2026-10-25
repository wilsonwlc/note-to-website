### Definition
- Suppose we conduct an experiment with sample space $\Omega$
- A **random variable** is a numerical function of the outcome $X : \Omega \rightarrow \mathbb{R}$ 
### Notation
- The usual convention is to use capital letters $X$, $Y$, ... to denote random variables and small letters $x$, $y$, ... to denote the possible numerical values (or **realisations**) of these variables *e.g.*
	- $X=x$ represents the event $\{\omega \in \Omega| X(\omega)=x \}$
	- $X \leq x$ represents the event $\{\omega \in \Omega| X(\omega) \leq x \}$
### Type
- [[Discrete random variable|Discrete random variable]]
- [[Continuous random variable|Continuous random variable]]
- **Mixed random variable**
### Caution
- $X$ is a function rather than a number. Hence, The value of $X$ depends on the outcome
- There exists distributions which are neither discrete nor (absolute) continuous *e.g.* The lifetime $T$ of a device may have a continuous distribution on $(0,\infty)$. However, in a test of the device we cannot wait forever and we might terminate the test after a certain time $c$. Then only the truncated lifetime $X$ is recorded and it will be discrete at $c$ as $P(X=c)=P(T\geq c)>0$ and continuous elsewhere. These distributions are called the **mixed distributions**
### Interpretation
- It maps outcomes $\omega \in \Omega$ to numbers *i.e.* $\omega \mapsto X(\omega)$
### Practice
- Functions of random variables are random variables *e.g.* If $Z \sim N(0,1)$, then $Y=Z^{2} \sim \Gamma(\frac{1}{2}, \frac{1}{2})$ and $X=\sigma Z+ \mu \sim N(\mu, \sigma^{2})$