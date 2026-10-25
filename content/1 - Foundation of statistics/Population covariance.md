### Definition
Let $X$ and $Y$ be [[Random variable|random variables]] with [[Population mean|means]] $\mu_{x}$ and $\mu_{y}$ 
The **population covariance** between $X$ and $Y$ is defined as 
$$
\begin{align*} \sigma_{XY} &= \text{Cov}(X,Y) \\ &= E[(X - \mu_{x})(Y - \mu_{y})] \\ &= E(XY) - \mu_{x}\mu_{y} \end{align*}
$$
### Interpretation
- The sign and the magnitude of $\sigma_{XY}$ tells the direction and the strength of the **linear relationship** between $X$ and $Y$ 
	- $\sigma_{XY} > 0$  $\Leftrightarrow$ $X$ $\uparrow$, $Y$ $\uparrow$  $\Leftrightarrow$ $X$ and $Y$ are **positively correlated**
	- $\sigma_{XY} < 0$ $\Leftrightarrow$ $X$ $\uparrow$, $Y$ $\downarrow$ $\Leftrightarrow$ $X$ and $Y$ are **negatively correlated**
### Property
- If $X' = aX + b$, $Y' = cY + d$ , then 
$$
\text{Cov}(X', Y') = ac \; \text{Cov}(X, Y)
$$
- $\text{Cov}(X,X) = \text{Var}(X)$
- $\text{Cov}\left(\sum\limits_{i=1}^{m} a_{i}X_{i}, \sum\limits_{j=1}^{n} b_{j}Y_{j}\right) = \sum\limits_{i=1}^{m} \sum\limits_{j=1}^{n} a_{i}b_{j}\text{Cov}(X_{i},Y_{j})$
- **Variance-Covariance formula** 
$$
\text{Var}\left(\sum_{i=1}^{n} a_{i}X_{i}\right) = \sum_{i=1}^{n} a_{i}^{2}\text{Var}(X_{i}) + 2\sum_{i<j} a_{i}a_{j}\text{Cov}(X_{i}, X_{j})
$$
- $\text{Var}(X+Y) = \text{Var}(X) + \text{Var}(Y) + 2\text{Cov}(X,Y)$
- $\text{Var}(X-Y) = \text{Var}(X) + \text{Var}(Y) - 2\text{Cov}(X,Y)$
