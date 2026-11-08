### Definition
The **mean square error** of an estimator $\hat{\theta}$ of a parameter $\theta$ is defined as 
$$
MSE(\widehat{\theta}) = E\left[(\hat{\theta} - \theta)^{2}\right]
$$
### Property
#### Bias and variance
$$
MSE(\hat{\theta}) = Var(\hat{\theta}) + bias(\hat{\theta})^{2}
$$
##### Proof
- By the definition of MSE
$$
\begin{aligned} 
MSE(\hat{\theta}) &= E\left((\hat{\theta} - \theta)^{2}\right) \\ 
&= E[\hat{\theta}^{2} - 2 \theta \hat{\theta}^{2} + \theta^{2}] \\ &= E(\hat{\theta}^{2}) - 2\theta E(\hat{\theta}) + \theta^{2} 
\end{aligned}
$$
- By the property of [[Population variance|variance]], 
	$$
	\begin{aligned} Var(X) &= E(X^{2}) - \mu^{2} \\ Var(\hat{\theta}) &= E(\hat{\theta}^{2}) - [E(\hat{\theta})]^{2} \end{aligned}
	$$
- By the definition of [[Bias|bias]], 
	$$
	\begin{aligned} bias(\hat{\theta}) &=  E(\hat{\theta}) - \theta \\ [bias(\hat{\theta})]^{2} &=  (E(\hat{\theta}) - \theta)^{2} \\ &= [E(\hat{\theta})]^{2} - 2 \theta E(\hat{\theta}) + \theta^{2} \end{aligned}
	$$
- Hence, 
	$$
	\begin{aligned} Var(\hat{\theta}) + [bias(\hat{\theta})]^{2} &= E(\hat{\theta}^{2}) - [E(\hat{\theta})]^{2}  + [E(\hat{\theta})]^{2} - 2 \theta E(\hat{\theta}) + \theta^{2} \\ &= E(\hat{\theta}^{2}) - 2\theta E(\hat{\theta}) + \theta^{2} \\ &= MSE(\hat{\theta}) \end{aligned}
	$$

##### Interpretation
![[Mean Square Error - Property - Bias and Variance.png|534]]
#### Unbiased estimator
- If $\hat{\theta}$ is unbiased, then 
	$$
	MSE(\hat{\theta}) = Var(\hat{\theta})
	$$