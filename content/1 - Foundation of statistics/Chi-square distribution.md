### Definition
Let $r \in \mathbb{N}$.
If $X \sim \Gamma(\frac{r}{2}, \frac{1}{2})$, then it follows **Chi-Square distribution** with degrees of freedom $r$
It is denoted by $X \sim \chi_{r}^{2}$
### Property
- [[Probability density function (pdf)|pdf]]: $$f(x) = \frac{1}{\Gamma(\frac{r}{2})2^{\frac{r}{2}}} x^{\frac{r}{2}-1} e^{\frac{-x}{2}}$$
	- $x>0$
- [[Moment generating function (mgf)|Moment generating function]]: $M_{X}(t) = \frac{1}{(1 - 2t)^{\frac{r}{2}}}$ for $t<\frac{1}{2}$
- [[Population mean|Mean]]: $\mu =r$
- [[Population variance|Variance]]: $\sigma^{2}=2r$
- The sum of independent Chi-square random variables is distributed as Chi-square
	- *Proof:* By the property of normal distribution, $\left(\frac{X_{i}-\mu}{\sigma}\right)^{2} \sim \chi_{1}^{2}$ and $\sum\limits_{i=1}^{n} \left(\frac{X_{i}-\mu}{\sigma}\right)^{2} \sim \chi_{n}^{2}$
- If $X \sim \chi_{n}^{2}$ and $c>0$, then $cX \sim \Gamma(\frac{n}{2},\frac{1}{2c})$