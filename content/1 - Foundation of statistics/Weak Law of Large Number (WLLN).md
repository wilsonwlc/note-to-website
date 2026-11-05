### Theorem
Let $X_{1},X_{2},...$   be a sequence of identically independently distributed random variables with finite [[Population mean|mean]] $E(X_{i})=\mu$ and [[Population covariance|variance]] $\text{Var}(X_{i})=\sigma^{2}$ 
If $\overline{X}_{n}=\frac{1}{n}\sum\limits_{i=1}^{n}X_{i}$ is the [[Sample mean|sample mean]] of the [[Random sample|random sample]], then for arbitrary number $\varepsilon>0$, 
$$
\lim_{n \to \infty} P\left( \left| \overline{X}_{n} - \mu \right| \ge \varepsilon \right) = 0
$$
or 
$$
\lim_{n \to \infty} P\left( \left| \overline{X}_{n} - \mu \right| < \varepsilon \right) = 1
$$
### Interpretation
- It states that the sample mean from a large sample would have a very high probability to be arbitrarily close to the population mean. This promise a stable performance of the sample mean
- In large sample theory, it means that the sample mean converges in probability towards the population means. It is denoted as 
$$
\overline{X}_{n} \xrightarrow{P} \mu
$$
### Practice
- *General version of WLLN:* If $E(\left| X_{i} \right|) < \infty$, then $\overline{X}_{n} \xrightarrow{P} \mu$
	- The general version does not require a finite population variance
### Comparison
![[Strong Law of Large Number (SLLN)#WLLN vs SLLN]]