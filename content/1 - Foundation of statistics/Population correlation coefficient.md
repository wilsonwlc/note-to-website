### Motivation
- *Problem:* Since $\sigma_{XY}$ depends on the scales of $X$ and $Y$, it is difficult to determine the strength of the linear relationship between $X$ and $Y$
- *Aim:* have a standardised measure which is invariant under linear transformation of $X$ and $Y$
### Definition
Let $X$ and $Y$ be [[Random variable|random variables]] with [[Population covariance|covariance]] $\sigma_{XY}$ and [[Population standard deviation|standard deviations]] $\sigma_{X}=\sqrt{\text{Var}(X)}$ and $\sigma_{Y}=\sqrt{\text{Var}(Y)}$
The **population correlation coefficient** between $X$ and $Y$ is defined as 
$$
\begin{align*} \rho &= \text{Corr}(X,Y) \\ &= \frac{\sigma_{XY}} {\sigma_{X}\sigma_{Y}} \\  &= \frac{\text{Cov}(X,Y)}{\sqrt{\text{Var}(X)\text{Var}(Y)}} \end{align*}
$$
### Caution
- When $X$ or $Y$ (or both) is a constant, $\rho$ is undefined
- Correlation coefficient measures the strength of the linear relationship only. It may be possible that $X$ and $Y$ are strongly related but that the relation is curvilinear, and $\rho$ would be nearly zero
- An observed correlation may be due to a third unknown casual variable
### Property
- $-1 \leq \rho \leq 1$
	- *Proof:* By [[Cauchy-Schwartz inequality|Cauchy-Schwartz inequality]], 
	$$
	\begin{align*} \sigma_{XY}^{2} &= E[(X - \mu_{X})(Y - \mu_{Y})]^{2} \\ &\le E[(X - \mu_{X})^{2}] E[(Y - \mu_{Y})^{2}] \\ &= \sigma_{X}^{2} \sigma_{Y}^{2} \\ \rho^{2} &= \frac{\sigma_{XY}^{2}}{\sigma_{X}^{2}\sigma_{Y}^{2}} \le 1  \end{align*}
	$$
	- By [[Cauchy-Schwartz inequality|Cauchy-Schwartz inequality]], the equality holds *i.e.* $\rho^{2}=\pm 1$ when $X-\mu_{X}$ and $Y-\mu_{Y}$ are proportional *i.e.* $X$ and $Y$ are perfectly linearly related
- The magnitude of $\rho$ is invariant under linear transformation of $X$ and $Y$
	- *Proof:* Let $X'=aX+b$, $Y'=cY+d$ 
	$$
	\begin{align*} \text{Corr}(X',Y') &= \frac{\text{Cov}(aX + b, cY + d)}{\sqrt{\text{Var}(aX + b)\text{Var}(cY + d)}} \\ &= \frac{ac \; \text{Cov}(X,Y)}{\sqrt{a^{2}\text{Var}(X)c^{2}\text{Var}(Y)}} \\ &= \frac{ac \; \text{Cov}(X,Y)}{|ac|\sqrt{\text{Var}(X)\text{Var}(Y)}} \\ &= sign(ac)\text{Corr}(X,Y)  \end{align*}
	$$
- If $X$ and $Y$ are [[Independence of random variables|independent]], then $\rho=0$
	- *Proof:* Provided that both $X$ and $Y$ are not constant 
	$$
	\begin{align*} \text{Cov}(X,Y) &= E(XY) - E(X)E(Y) \\ &= E(X)E(Y) - E(X)E(Y) \\ &= 0 \end{align*}
	$$
	- *Caution:* $\rho=0$ does not imply $X$ and $Y$ are independent
- If $X$ and $Y$ are [[Independence of random variables|independent]], then 
$$
\text{Var}(X + Y) = \text{Var}(X - Y) = \text{Var}(X) + \text{Var}(Y)
$$