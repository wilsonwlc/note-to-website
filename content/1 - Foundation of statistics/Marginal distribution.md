### Definition
#### Discrete case
Let $X$ and $Y$ be [[Discrete random variable|discrete random variables]] with [[Joint distribution#Discrete case|joint pmf]] $p_{X,Y}(x, y)$. The **marginal pmf** of $X$ and $Y$are respectively defined as 
$$
\begin{align*} p_{X}(x) = P(X = x) = \sum_{y} p(x, y) \\ p_{Y}(y) = P(Y = y) = \sum_{x} p(x, y) \end{align*}
$$
#### Continuous case
Let $X$ and $Y$ be [[Continuous random variable|continuous random variable]] with [[Joint distribution#Continuous case|join pdf]] $f_{X,Y}(x,y)$. The **marginal pdf** of $X$ and $Y$ are respectively defined as
$$
\begin{align*} f_{X}(x) = \int_{-\infty}^{\infty} f(x,y)dy \\ f_{Y}(y) = \int_{-\infty}^{\infty} f(x,y)dx \end{align*}
$$
### Caution
- The **joint distribution** uniquely determines the marginal distributions, but the converse is **not** true in general (unless the variables are [[Independence of random variables|independent]])
### Generalisation
#### Discrete random variable
Marginal pmf of $X_{1}$ 
$$
p_{X_{1}}(x_{1}) = \sum_{x_{2}} \sum_{x_{3}} \cdots \sum_{x_{n}} p(x_{1}, x_{2}, \dots, x_{n})
$$
- $p(x_{1},x_{2} ..., x_{n})$: **joint pmf**
#### Continuous random variable
Marginal pdf $X_{1}$ 
$$
f_{X_{1}}(x_{1}) = \int_{-\infty}^{\infty} \cdots \int_{-\infty}^{\infty} f(x_{1}, x_{2}, \dots, x_{n}) dx_{2} dx_{3} \cdots dx_{n}
$$
- $f(x_{1}, x_{2}, \dots, x_{n})$: **joint pdf**