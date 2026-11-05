### Concept
- Aka Student's t-distribution
- *Which:* [[Continuous random variable|continuous]] distribution
- *History:* In 1908, William Sealy Gosset published the t-distribution under the pseudonym "Student" because his employer, the Gunness Brewery restricted staff from publishing scientific papers under their real names to protect trade secrets
### Definition
Let $Z \sim N(0,1)$ and $W \sim \chi_{r}^{2}$. Suppose $Z$ and $W$ are [[Independence of random variables|independent]]
Then $X=\frac{Z}{\sqrt{\frac{W}{r}}}$ follows **t-distribution** with $r$ degrees of freedom
It is denoted as $X \sim t_{r}$
### Property
- [[Probability density function (pdf)|pdf]]: 
$$
f(x)=\frac{\Gamma(\frac{r+1}{2})}{\Gamma(\frac{r}{2})\Gamma(\frac{1}{2})}r^{\frac{-1}{2}}\left(1+\frac{x^{2}}{r}\right)^{-\frac{r+1}{2}}
$$
- [[Moment generating function (mgf)|Moment generating function]]: undefined
- [[Population mean|Mean]]: $$\mu = \begin{cases} 0 & \text{for } r > 1 \\ \text{undefined} & \text{otherwise} \end{cases}$$
- [[Population variance|Variance]]: $$\sigma^{2} = \begin{cases} \frac{r}{r-2} & \text{for } r > 2 \\ \text{undefined} & \text{otherwise} \end{cases}$$
### Comparison
#### t-distribution vs normal distribution 
- *Similarity:* The [[t-distribution|t-distributions]] look like the [[Normal distribution|standard normal distribution]]: symmetric and bell shaped
- *Difference:* the t-distributions are flatter than standard normal distribution in the middle part and have wider and thicker tails