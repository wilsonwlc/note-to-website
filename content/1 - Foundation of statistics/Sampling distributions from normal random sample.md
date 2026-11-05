### Concept
- *Why we need it:* It is common to assume the population closely resembles a [[Normal distribution|normal distribution]]. The data analysis would be based on the [[Sampling distribution|sampling distribution]] of [[Sample mean|sample mean]] and [[Sample variance|sample variance]]
### Theorem
Assume $X_{i} \stackrel{iid}{\sim} N(\mu, \sigma^{2})$
1. Sampling distribution of the **sample mean** 
$$
\overline{X} \sim N\left(\mu, \frac{\sigma^{2}}{n}\right)
$$

2. Sampling distribution of the **sample variance** 
$$
\frac{(n-1)S^{2}}{\sigma^{2}} \sim \chi_{n-1}^{2}
$$
3. The sample mean and sample variance are statistically [[Independence of random variables|independent]]
4. Sampling distribution of $T=\frac{\overline{X}-\mu}{\frac{S}{\sqrt{n}}} \sim t_{n-1}$ 

#### Proof
##### Part 1
- The [[Moment generating function (mgf)|moment generating function]] of each individual random variable is 
$$
M_{X}(t) = \exp\left\{\mu t + \frac{\sigma^{2}t^{2}}{2}\right\} \quad \forall \; t
$$
- By its property, the moment generating function for the sample mean is 
$$
\begin{align*} M_{\overline{X}}(t) &= \left\{\exp\left[\mu \frac{t}{n} + \frac{\sigma^{2}(\frac{t}{n})^{2}}{2}\right]\right\}^{n} \\ &= \exp\left\{\mu t + \frac{(\frac{\sigma^{2}}{n})t^{2}}{2}\right\} \end{align*}
$$
- It is the moment generating function of $N\left(\mu, \frac{\sigma^{2}}{n}\right)$
##### Part 3
- Since $X_{i} \stackrel{iid}{\sim} N(\mu, \sigma^{2})$, the [[Joint distribution|joint pdf]] of $X_{1},X_{2},..., X_{n}$ is 
$$
\begin{align*} &\hspace{0.7cm} f_{\mathbf{X}}(x_{1}, x_{2}, \dots, x_{n}) \\ &= \prod_{i=1}^{n} \left\{ \frac{1}{\sqrt{2\pi\sigma^{2}}} \exp\left( -\frac{(x_{i} - \mu)^{2}}{2\sigma^{2}} \right) \right\} \\ &= \left(2\pi\sigma^{2}\right)^{-\frac{n}{2}} \exp\left\{ -\frac{1}{2\sigma^{2}} \sum_{i=1}^{n} (x_{i} - \mu)^{2} \right\} \end{align*}
$$
- Consider the transformation $Y_{1}=\overline{X}$ and $Y_{i}=X_{i}-\overline{X}$ for $i=2,3,...,n$
	- $X_{1} = Y_{1} - \sum\limits_{i=2}^{n} Y_{i}$
		- *Reason:* 
		$$
		\begin{align*} X_{1} &= n\overline{X} - \sum\limits_{i=2}^{n} X_{i} \\ &= \overline{X} + (n-1) \overline{X} - \sum\limits_{i=2}^{n} X_{i} \\ &= \overline{X} - \sum\limits_{i=2}^{n}(X_{i}-\overline{X}) \\ &= Y_{1} - \sum\limits_{i=2}^{n} Y_{i} \end{align*}
		$$
	- $X_{i}=Y_{i}+Y_{1}$ for $i=2,3,...,n$
	- The transformation is 1-1 with inverse transformation
	- Jacobian determinant is 
		$$
		\begin{align*} \left| J(x_{1}, x_{2}, \dots, x_{n}) \right|^{-1} &= \begin{vmatrix} \frac{\partial x_{1}}{\partial y_{1}} & \frac{\partial x_{1}}{\partial y_{2}} & \dots & \frac{\partial x_{1}}{\partial y_{n}} \\ \frac{\partial x_{2}}{\partial y_{1}} & \frac{\partial x_{2}}{\partial y_{2}} & \dots & \frac{\partial x_{2}}{\partial y_{n}} \\ \vdots & \vdots & \vdots & \vdots \\ \frac{\partial x_{n}}{\partial y_{1}} & \frac{\partial x_{n}}{\partial y_{2}} & \dots & \frac{\partial x_{n}}{\partial y_{n}} \end{vmatrix} \\ &= \begin{vmatrix} 1 & -1 & -1 & \dots & -1 \\ 1 & 1 & 0 & \dots & 0 \\ 1 & 0 & 1 & \dots & 0 \\ \vdots & \vdots & \vdots & \vdots & \vdots \\ 1 & 0 & 0 & \dots & 1 \end{vmatrix} \\ &= n  \end{align*}
		$$
- 	$$
	\begin{align*}
	\sum_{i=1}^{n} (x_{i} - \mu)^{2} &= \sum_{i=1}^{n} (x_{i} - \overline{x} + \overline{x} - \mu)^{2} \\
	&= \sum_{i=1}^{n} (x_{i} - \overline{x})^{2} + \sum_{i=1}^{n} (\overline{x} - \mu)^{2} \\ &\hspace{1cm} + 2(\overline{x} - \mu) \sum_{i=1}^{n} (x_{i} - \overline{x}) \\
	&= \sum_{i=1}^{n} (x_{i} - \overline{x})^{2} + n(\overline{x} - \mu)^{2} \\ &= (x_{1} - \overline{x}) + \sum_{i=2}^{n} (x_{i} - \overline{x})^{2} + n(\overline{x} - \mu)^{2} \\
	&= \left(\sum_{i=2}^{n} y_{i}\right)^{2} + \sum_{i=2}^{n} y_{i}^{2} + n(y_{1} - \mu)^{2}
	\end{align*}
	$$
- By [[Transformation of multivariate distribution|transformation of multivariate distribution]], the joint pdf of $Y_{1},..., Y_{n}$ is 
	$$
	\begin{align*} &\hspace{0.7cm} f_{\mathbf{Y}}(y_{1}, \dots, y_{n}) \\ &= \left(2\pi\sigma^{2}\right)^{-\frac{n}{2}} \exp\left\{ -\frac{1}{2\sigma^{2}} \left[ \left(\sum_{i=2}^{n} y_{i}\right)^{2} + \sum_{i=2}^{n} y_{i}^{2} + n(y_{1} - \mu)^{2} \right] \right\} \times |n| \\ &= \left\{ \frac{1}{\sqrt{2\pi(\sigma^{2}/n)}} \exp\left( -\frac{(y_{1} - \mu)^{2}}{2(\sigma^{2}/n)} \right) \right\} \times \left\{ \sqrt{n} \left(2\pi\sigma^{2}\right)^{-\frac{n-1}{2}} \exp\left\{ -\frac{1}{2\sigma^{2}} \left[ \left(\sum_{i=2}^{n} y_{i}\right)^{2} + \sum_{i=2}^{n} y_{i}^{2} \right] \right\} \right\}   \end{align*}
	$$
- $Y_{1}$ and $(Y_{2},...,Y_{n})$ are independent
- Since $\overline{X}=Y_{1}$ and $S^{2} = \frac{1}{n-1} \sum_{i=1}^{n} (X_{i} - \overline{X})^{2} = \frac{1}{n-1} \left[ \left(\sum_{i=2}^{n} Y_{i}\right)^{2} + \sum_{i=2}^{n} Y_{i}^{2} \right]$, $\overline{X}$ and $S^{2}$ are independent
##### Part 2
Consider 
$$
\begin{align*} \sum_{i=1}^{n} (X_{i} - \mu)^{2} &= \sum_{i=1}^{n} (X_{i} - \overline{X} + \overline{X} - \mu)^{2} \\ &= \sum_{i=1}^{n} (X_{i} - \overline{X})^{2} + \sum_{i=1}^{n} (\overline{X} - \mu)^{2} \\ &\hspace{0.9cm} +  2(\overline{X} - \mu) \sum_{i=1}^{n} (X_{i} - \overline{X}) \\ &= \sum_{i=1}^{n} (X_{i} - \overline{X})^{2} + n(\overline{X} - \mu)^{2} \\ \sum_{i=1}^{n} \left(\frac{X_{i} - \mu}{\sigma}\right)^{2} &= \frac{(n-1)S^{2}}{\sigma^{2}} + \left(\frac{\overline{X} - \mu}{\frac{\sigma}{\sqrt{n}}}\right)^{2} \end{align*}
$$
- Let $W = \sum_{i=1}^{n} \left(\frac{X_{i} - \mu}{\sigma}\right)^{2}$, $Y = \frac{(n-1)S^{2}}{\sigma^{2}}$ and $Z = \left(\frac{\overline{X} - \mu}{\frac{\sigma}{\sqrt{n}}}\right)^{2}$
- Then, $W = Y + Z$
	- Since $\frac{X_{i} - \mu}{\sigma} \sim N(0,1)$ *i.e.* [[Normal distribution|normal distribution]], $\left(\frac{X_{i} - \mu}{\sigma}\right)^{2}$ follows $\chi_{1}^{2}$ (*i.e.* [[Chi-square distribution|chi-square distribution]]) and $W \sim \chi_{n}^{2}$ 
	- Since $\overline{X} \sim N\left(\mu, \frac{\sigma^{2}}{n}\right)$, $Z = \left(\frac{\overline{X} - \mu}{\frac{\sigma}{\sqrt{n}}}\right)^{2} \sim \chi_{1}^{2}$
	- By Part 2, $\overline{X}$ and $S^{2}$ are independent, and so are $Y$ and $Z$
- Consider the [[Moment generating function (mgf)|moment generating function]] 
$$
\begin{align*} M_{W}(t) &= M_{Y}(t) M_{Z}(t) \\ \frac{1}{(1 - 2t)^{\frac{n}{2}}} &= M_{Y}(t) \frac{1}{(1 - 2t)^{\frac{1}{2}}} \\ M_{Y}(t) &= \frac{1}{(1 - 2t)^{\frac{n-1}{2}}} \end{align*}
$$
- $Y = \frac{(n-1)S^{2}}{\sigma^{2}} \sim \chi_{n-1}^{2}$

##### Part 4
- $Z=\frac{\overline{X}-\mu}{\frac{\sigma}{\sqrt{n}}} \sim N(0,1)$ is independent of $W=\frac{(n-1)S^{2}}{\sigma^{2}} \sim \chi_{n-1}^{2}$
- By definition of [[t-distribution|t-distribution]], 
$$
T=\frac{Z}{\sqrt{\frac{W}{n-1}}}=\frac{\frac{\overline{X}-\mu}{\frac{\sigma}{\sqrt{n}}}}{\sqrt{\frac{S^{2}}{\sigma^{2}}}}=\frac{\overline{X}-\mu}{\frac{S}{\sqrt{n}}} \sim t_{n-1}
$$
### Corollary
$$S^{2} \sim \Gamma\left(\frac{n-1}{2}, \frac{n-1}{2\sigma^{2}}\right)$$
- [[Population mean|Mean]]: $E(S^{2}) = \frac{\frac{n-1}{2}}{\frac{n-1}{2\sigma^{2}}} = \sigma^{2}$
- [[Population variance|Variance]] $\operatorname{Var}(S^{2}) = \frac{\frac{n-1}{2}}{\frac{(n-1)^{2}}{4\sigma^{4}}} = \frac{2\sigma^{4}}{n-1}$
### Theorem
Assume $X_{i} \stackrel{iid}{\sim} N(\mu_{x}, \sigma^{2}_{x})$ $\forall i\in \{1,2,...,m\}$ and $Y_{j} \stackrel{iid}{\sim} N(\mu_{y}, \sigma^{2}_{y})$ $\forall j \in \{1,2,...,n\}$. 
Suppose the 2 random samples are independent
Let $S_{x}^{2}$ and $S^{2}_{y}$ be the sample variances from the $X_i$'s and $Y_{j}$'s respectively
Then the sampling distribution $$F = \frac{\frac{S_{x}^{2}}{S_{y}^{2}}}{\frac{\sigma_{x}^{2}}{\sigma_{y}^{2}}} \sim F(m-1,n-1)$$
#### Proof
- $W_{1} = \frac{(m-1)S_{x}^{2}}{\sigma_{x}^{2}} \sim \chi_{m-1}^{2}$
- $W_{2} = \frac{(n-1)S_{y}^{2}}{\sigma_{y}^{2}} \sim \chi_{n-1}^{2}$
- $W_{1}$ and $W_{2}$ are independent
- By the definition of F-distribution, $$F=\frac{\frac{W_{1}}{m-1}}{\frac{W_{2}}{n-1}}=\frac{\frac{S_{x}^{2}}{\sigma_{x}^{2}}}{\frac{S_{y}^{2}}{\sigma_{y}^{2}}}=\frac{\frac{S_{x}^{2}}{S_{y}^{2}}}{\frac{\sigma_{x}^{2}}{\sigma_{y}^{2}}} \sim F(m-1,n-1)$$