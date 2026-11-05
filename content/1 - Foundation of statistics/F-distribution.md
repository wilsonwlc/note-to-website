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

### Visualisation
![[F-distribution - visualisation.png|453]]
- The F-distribution is asymmetric and skewed towards the right

