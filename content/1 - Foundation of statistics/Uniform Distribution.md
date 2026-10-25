### Concept
- *Which:* [[Continuous random variable|Continuous random variable]]
### Definition
If $X \sim U(a,b)$, then the [[Probability density function (pdf)|pdf]] of $X$ is a constant function on $(a,b)$
$$
f(x) = \left\{ \begin{array}{ll} \frac{1}{{b-a}} & \text{if } a<x<b \\ 0 & \text{otherwise} \end{array} \right.
$$
### Visualisation
![[Uniform distribution.png|310]]

### Interpretation
- $X$ can be thought as a point randomly drawn from the interval $(a,b)$
- It has no preference to be located near any particular region
### Property
- [[Cumulative distribution function (cdf)|cdf]]
$$
F(x) = \left\{ \begin{array}{ll} 0 & \text{if } x \leq a \\
\frac{x-a}{b-a} & \text{if } a < x < b \\ 1 & \text{if } x \geq b  \end{array} \right.
$$
- [[Population mean|Mean]]: $\mu= E(X) = \frac{a+b}{2}$ *i.e.* midpoint of interval
- [[Population variance|Variance]]: $\sigma^{2} = E(X^{2})-\mu^{2} = \frac{(b-a)^{2}}{12}$
- If $X \sim U(0,1), Y=cX+d$, then 
$$
\begin{array}{ll} Y \sim U(d,c+d) & \text{if } c \text{ is positive} \\ Y \sim U(c+d, d) & \text{if } c \text{ is negative}  \end{array}
$$
