### Concept
- Aka **Gaussian distribution**
- Which: [[Continuous random variable|Continuous random variable]]
### Definition
A random variable $X$ follows a **normal distribution** if its **pdf** is 
$$
f(x) = \frac{1}{\sqrt{2\pi\sigma^{2}}} \exp\left\{-\frac{(x - \mu)^{2}}{2\sigma^{2}}\right\}
$$

- $-\infty< x < \infty$
- $-\infty< \mu < \infty$: **location parameter**
- $\sigma > 0$: **scale parameter**
It is denoted as $X\sim N(\mu,\sigma^{2})$ 
#### Special case
When a random variable $Z$ follows a normal distribution with $\mu=0$ and $\sigma=1$ *i.e.* have **pdf** $\phi(z) = \frac{1}{\sqrt{2\pi}} e^{-\frac{z^{2}}{2}}$ where $-\infty< z < \infty$, then it is said to have a **standard normal distribution**
### Property
- [[Cumulative distribution function (cdf)|cdf]]: 
	- $F(x) = \int_{-\infty}^{x} \frac{1}{\sqrt{2\pi\sigma^{2}}} \exp\left\{-\frac{(t - \mu)^{2}}{2\sigma^{2}}\right\} dt$, where $-\infty< x < \infty$
	- $\Phi(z) = P(Z \le z) = \int_{-\infty}^{z} \frac{1}{\sqrt{2\pi}} e^{-\frac{t^{2}}{2}} dt$ where $-\infty< z < \infty$
- [[Moment generating function (mgf)|Moment generating function]]: $M_{X}(t) = \exp\left(\mu t + \frac{1}{2}\sigma^{2}t^{2}\right)$, where $t\in \mathbb{R}$
- [[Population mean|Mean]]: $E(X) = \mu$
- [[Population variance|Variance]]: $\operatorname{Var}(X) = \sigma^{2}$
- $P(X \le \mu - x) = P(X \ge \mu + x)$
	- *Reason:* Normal distribution is symmetric about its mean 
- $\Phi(x) = 1 - \Phi(-x)$
	- *Reason:* Normal distribution is symmetric about its mean 
- If $X \sim N(\mu, \sigma^{2})$, then $aX + b \sim N\left(a\mu + b, a^{2}\sigma^{2}\right)$
- *Transformation:* $Z=\frac{X-\mu}{\sigma}$
- If $Z \sim N(0,1)$, then $Z^{2} \sim \Gamma(\frac{1}{2}, \frac{1}{2})$
- If $X \sim N(\mu, \sigma^{2})$, then $P(a \le X \le b) = \Phi\left(\frac{b - \mu}{\sigma}\right) - \Phi\left(\frac{a - \mu}{\sigma}\right)$
### Visualisation
- Each bell-shaped **normal curve** is symmetric and centred at its [[Population mean|mean]] $\mu$
- **68–95–99.7 rule** or **empirical rule**
	- *i.e.* (1) About 68% of the area is within one [[Population standard deviation|standard deviation]] of the mean; (2) about 95% of the area is within two standard deviations of the mean; (3) almost all (99.7%) of the area is within three standard deviations of the mean
	- *Caution:* not by [[Chebyshev’s inequality|Chebyshev’s inequality]]
	- *Proof:* 
		- By transforming the standard normal distribution $P(\mu-k\sigma<X<\mu+k\sigma)=2\Phi(k)-1$
		- Since $\Phi(1) \approx 0.841344746$, $P(\mu-\sigma<X<\mu+\sigma)=2\Phi(1)-1\approx 0.6827$
		- $\Phi(2) \approx 0.977249868$, then $P(\mu-2\sigma<X<\mu+2\sigma)=2\Phi(2)-1\approx 0.9545$
		- $\Phi(3) \approx 0.998650102$, then $P(\mu-3\sigma<X<\mu+3\sigma)=2\Phi(3)-1\approx 0.9973$
- The places where the normal curve is steepest are a standard deviation below and above the mean *i.e.* $\mu - \sigma$ and $\mu + \sigma$
### When
- Symmetric measurement around a typical value