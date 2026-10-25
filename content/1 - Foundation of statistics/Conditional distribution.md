### Motivation
- When 2 [[Random variable|random variables]] $(X,Y)$ are observed, their values are related
- *e.g.* $X$ and $Y$ represents a person height and weight respectively. It is more likely that $Y>200$ pounds if $X=182$cm than $X=104$cm
- The knowledge about the value of $X$ gives us some information about the value of $X$ even though it does not reveal the exactly value of $Y$
### Definition
#### PMF & PDF
#### Discrete case
- Let $(X,Y)$ be a discrete bivariate random variable with [[Joint distribution#Discrete case|joint pmf]] $p_{X,Y}(x,y)$ and [[Marginal distribution#Discrete case|marginal pmfs]] $p_{X}(x)$ and $p_{Y}(y)$
- For any $x$ such as $p_{X}(x)=P(X=x)>0$, the **conditional pmf** of $Y$ given that $X=x$ is defined by 
$$
\begin{align*} p_{Y|X}(y|x) &= P(Y = y | X = x) \\ &= \frac{P(Y = y, X = x)}{P(X = x)} \\ &= \frac{p_{X,Y}(x, y)}{p_{X}(x)} \end{align*}
$$
- For any $y$ such that $p_{Y}(y)= P(Y=y)>0$, the **conditional pmf** of $X$ given that $Y=y$ is defined by 
$$
\begin{align*} p_{X|Y}(x|y) &= P(X = x | Y = y) \\ &= \frac{P(X = x, Y = y)}{P(Y = y)} \\ &= \frac{p_{X,Y}(x, y)}{p_{Y}(y)} \end{align*}
$$
#### Continuous case
- Assume $f_X(x)>0$. **Conditional pdf** of $Y$ given $X=x$ is $$f_{Y|X}(y|x) = \frac{f_{X,Y}(x, y)}{f_{X}(x)} $$
- Assume $f_{Y}(y)>0$. **Conditional pdf** of $X$ given that $Y = y$ is $$f_{X|Y}(x|y) = \frac{f_{X,Y}(x, y)}{f_{Y}(y)}$$
#### CDF
$$
\begin{align*} F_{Y|X}(y|x) &= P(Y \le y | X = x) \\ &= \begin{cases} \sum_{i \le y} p_{Y|X}(i|x) & \text{discrete case} \\ \int_{-\infty}^{y} f_{Y|X}(t|x) dt & \text{continuous case} \end{cases} \end{align*}
$$

### Property
- If the discrete random variable $X$ and $Y$ are [[Independence of random variables#Proposition (factorisation)|independent]], then 
	- If $p_{Y}(y)>0$, then for all $y$, $p_{X|Y}(x|y) = \frac{p(x, y)}{p_{Y}(y)} = \frac{p_{X}(x) p_{Y}(y)}{p_{Y}(y)} = p_{X}(x)$
	- If $p_{X}(x)>0$, then for all $x$, $p_{Y|X}(y|x) = \frac{p(x, y)}{p_{X}(x)} = \frac{p_{X}(x) p_{Y}(y)}{p_{X}(x)} = p_{Y}(y)$
- If the continuous random variable $X$ and $Y$ are [[Independence of random variables#Proposition (factorisation)|independent]], then 
	- If $f_{Y}(y)>0$, then for all $y$, $f_{X \mid Y}(x \mid y) = \frac{f_{X,Y}(x,y)}{f_{Y}(y)} = \frac{f_{X}(x) f_{Y}(y)}{f_{Y}(y)} = f_{X}(x)$
	- If $f_X(x)>0$, then for all $x$, $f_{Y \mid X}(y \mid x) = \frac{f_{X,Y}(x,y)}{f_{X}(x)} = \frac{f_{X}(x) f_{Y}(y)}{f_{X}(x)} = f_{Y}(y)$
### Interpretation
- The conditional pmf of $Y$ given $X=x$ is a function of $y$. Similarly, the conditional pmf of $X$ given $Y=y$ is a function of $x$
- If the 2 random variables are independent, the knowledge of the value of one variable do not affect our uncertainty on the value of another variable *i.e.* knowledge of one variable give us no information on the other variable 
### Caution
- The conditional distribution of $Y$ given $X=x$ can be a different probability distribution for each value of $x$. The collection of these distributions is called **a family of conditional distribution** and represented by $Y|X$
