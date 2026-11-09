### Concept
Let $Y_{i} \overset{iid}{\sim} b(1, p)$ and $X = \sum\limits_{i=1}^{n} Y_{i} \sim b(n,p)$
Then, as $n \rightarrow \infty$,  
$$
\frac{X-np}{\sqrt{np(1-p)}} \xrightarrow{L} N(0,1)
$$
#### Proof
- $E(Y_{i}) = p$ and $\operatorname{Var}(Y_{i}) = p(1-p)$
- $E(X) = np$ and $\operatorname{Var}(X) = np(1-p)$ 
- The sample mean of $Y_{i}$ can be written as $\overline{Y}_{n}=\frac{X}{n}$
- By [[Central Limit Theorem (CLT)|CLT]], as $n\rightarrow \infty$, $\frac{\sqrt{n}\left(\overline{Y}_{n}-p\right)}{\sqrt{p(1-p)}} = \frac{X-np}{\sqrt{np(1-p)}} = \frac{X-E(X)}{\sqrt{\operatorname{Var}(X)}} \xrightarrow{L} N(0,1)$
### Practice
- The approximation will be quite good when $n \geq 30$, $np \geq 5$ and $n(1 - p) \geq 5$
- Use [[Continuity correction|continuity correction]] to have more accurate result