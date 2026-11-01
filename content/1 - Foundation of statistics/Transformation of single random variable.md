### Theorem
Let $X$ be a [[Continuous random variable|continuous random variable]] distributed on a space $S$ with pdf $f_{X}(x)$
If $Y=g(X)$ where $g$ is a function such that $g^{-1}$ exists, then the pdf of $Y$ is 
$$
f_Y(y) = f_X(g^{-1}(y)) \left| \frac{d}{dy} g^{-1}(y) \right|
$$

- $y \in g(S)$
#### Proof
- $F_{Y}(y)=P(Y \leq y) = P(g(X) \leq y)$
- *Case 1:* $g$ is strictly increasing function 
	$$
	\begin{aligned} F_{Y}(y) &= P\left(X \leq g^{-1}(y)\right) \\ &= F_{X}\left(g^{-1}(y)\right) \\ \Rightarrow f_{Y}(y) &= \frac{d}{dy} F_{X}\left(g^{-1}(y)\right) \\ &= f_{X}\left(g^{-1}(y)\right) \frac{d}{dy} g^{-1}(y) \end{aligned}
	$$
	
- *Case 2:* $g$ is strictly decreasing function 
	$$
	\begin{aligned} F_{Y}(y) &= P\left(X \geq g^{-1}(y)\right) \\ &= 1 - F_{X}\left(g^{-1}(y)\right) \\ \Rightarrow f_{Y}(y) &= -\frac{d}{dy} F_{X}\left(g^{-1}(y)\right) \\ &= -f_{X}\left(g^{-1}(y)\right) \frac{d}{dy} g^{-1}(y) \end{aligned}
	$$
	
- Since $\frac{d}{dy} g^{-1}(y)$ is positive when $g$ is increasing, and is negative when $g$ is decreasing, the pdf of $Y$ can be written as 
	$$
	f_{Y}(y) = f_{X}(g^{-1}(y)) \left| \frac{d}{dy} g^{-1}(y) \right|
	$$
	where $y \in g(S)$
### When
- Determine the distribution of the transformed random variable. *Alternative methods:*
	- If the transformation is not one-to-one *i.e.* $g^{-1}$ does not exist, need to use start from the [[Cumulative distribution function (cdf)|cumulative distribution function]]
	- [[Moment generating function (mgf)|Moment generating function (mgf)]]