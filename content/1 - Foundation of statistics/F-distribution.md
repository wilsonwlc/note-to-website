### Concept
- Aka **The Snedecor's F-distribution**
- *Which:* continuous distribution
- *When:* compare variances *e.g.* in the analysis of variance ANOVA for analysing experimental data
- *History:* It was developed in its modern form and tabulated by George W. Snedecor, who named it in honour of Sir Ronald A. Fisher

### Definition
Let $W_{1} \sim \chi_{r_{1}}^{2}$ and $W_{2} \sim \chi_{r_{2}}^{2}$
Suppose $W_{1}$ and $W_{2}$ are [[Independence of random variables|independent]]
Then, the ratio $X = \frac{\frac{W_{1}}{r_{1}}}{\frac{W_{2}}{r_{2}}}$ follows an **F-distribution** with numerator degree of freedom $r_{1}$  and denominator degree of freedom $r_{2}$
It is denoted as $X \sim F(r_{1}, r_{2})$ 
### Property
- [[Probability density function (pdf)|pdf]]: 
$$
f(x) = \frac{\Gamma\left(\frac{r_{1} + r_{2}}{2}\right)}{\Gamma\left(\frac{r_{1}}{2}\right) \Gamma\left(\frac{r_{2}}{2}\right)} \left(\frac{r_{1}}{r_{2}}\right)^{\frac{r_{1}}{2}} x^{\frac{r_{1}}{2} - 1} \left(1 + \frac{r_{1}}{r_{2}} x\right)^{-\frac{r_{1} + r_{2}}{2}} \quad \forall x >0
$$
- [[Moment generating function (mgf)|Moment generating function]]: undefined
- [[Population mean|Mean]]: 
$$
\mu = \begin{cases} \frac{r_{2}}{r_{2} - 2} & \text{for } r > 2 \\ \text{undefined} & \text{otherwise} \end{cases}
$$
- [[Population variance|Variance]]: 
$$
\sigma^{2} = \begin{cases} \frac{2 r_{2}^{2} (r_{1} + r_{2} - 2)}{r_{1} (r_{2} - 2)^{2} (r_{2} - 4)} & \text{for } r > 4 \\ \text{undefined} & \text{otherwise} \end{cases}
$$
- [[Critical value|Critical value]]: $F_{1-\alpha, r_{1}, r_{2}} = \frac{1}{F_{\alpha, r_{2}, r_{1}}}$
- *Proof:*
	1. By definition of F-distribution, if $W_{1} \sim \chi_{r_{1}}^{2}$, $W_{2} \sim \chi_{r_{2}}^{2}$ and are independent, then $X = \frac{\frac{W_{1}}{r_{1}}}{\frac{W_{2}}{r_{2}}} \sim F(r_{1}, r_{2})$ . Similarly, $\frac{1}{X} \sim F(r_{2},r_{1})$
	2. Since $X \sim F(r_{1}, r_{2})$, by definition of critical value, 
	$$
	\begin{align*}P(X > F_{1-\alpha, r_{1}, r_{2}}) &= 1-\alpha \\ P\left(\frac{1}{X} < \frac{1}{F_{\alpha, r_{1}, r_{2}}}\right) &= 1-\alpha \end{align*}
	$$ 		
	3. Since $\frac{1}{X} \sim F(r_{2},r_{1})$, by definition of critical value, 
		$$
		\begin{align*} P\left(\frac{1}{X} > F_{\alpha,r_{2}, r_{1}}\right) &= \alpha \\ P\left(\frac{1}{X} < F_{\alpha,r_{2}, r_{1}}\right) &= 1-\alpha \end{align*}
		$$
	4. Hence, $F_{1-\alpha, r_{1}, r_{2}} = \frac{1}{F_{\alpha, r_{2}, r_{1}}}$`

### Visualisation
![[F-distribution - visualisation.png|453]]
- The F-distribution is asymmetric and skewed towards the right

