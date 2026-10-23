### Motivation
- When an experiment or survey is conducted, two or more [[Random variable|random variables]] are often observed simultaneously. This is because we not only want to study their individual probabilistic behaviours, but also to determine the degree of relationship among the variables as in most of cases
- The probabilistic behaviours of the random variables are described by their joint distribution
### Definition
#### Discrete case
Let $X$ and $Y$ be [[Discrete random variable|discrete random variables]]
$X$ and $Y$ are said to have a **joint discrete distribution** if there exists a function $p(x,y)$ such that, for all $x \in X(\Omega)=\{x_1,\dots,x_r\}$ and $y \in Y(\Omega)=\{y_1,\dots,y_c\}$, $$p(x,y) = P(X=x,Y=y)$$
$p(x, y)$ is called **joint probability mass function (joint pmf)**
#### Continuous case
Let $X$ and $Y$ be [[Continuous random variable|continuous random variables]]
$X$ and $Y$ are said to have a **joint continuous distribution** if there exists a non-negative function $f(x,y)$ such that, for all measurable set $C \subset \mathbb{R}^{2}$, $$\begin{align*}P((X, Y) \in C) &= \iint_{(x, y) \in C} f(x, y) dx dy \end{align*}$$
$f(x,y)$ is called **joint probability density function (joint pdf)** 
### Property
- **Joint cumulative distribution function** $$\begin{align*} F(x,y) &= P(X \le x, Y \le y)\end{align*}$$
#### Discrete random variable
- $F(x,y)=\sum_{x_i\le x}\sum_{y_j\le y}p(x_i,y_j)$
- $0 \leq p(x,y) \leq 1$
- $\sum_{x \in X(\Omega)} \sum_{y \in Y(\Omega)} p(x, y) = 1$
- $P((X, Y) \in A) = \sum_{(x, y) \in A} p(x, y)$ where $A \subset X(\Omega) \times Y(\Omega)$
#### Continuous random variable
- $F(x,y)=\int_{-\infty}^y\int_{-\infty}^x f(s,t)\,ds\,dt$
- $f(x,y) \geq 0$
- $\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(x, y) dx dy = 1$
- $P((X,Y) \in A) = \iint_{A} f(x,y)dxdy$ 
### Generalisation
#### Discrete random variable
- **Joint pmf** $$\begin{align*}  p(x_{1},x_{2} ..., x_{n}) =  P(X_{1} = x_{1}, X_{2} = x_{2}, \dots, X_{n} = x_{n}) \end{align*}$$
#### Continuous random variable
- **Joint pdf** $$P\bigl((X_1,\dots,X_n)\in C\bigr) =\idotsint_C f(x_1,\dots,x_n)\,dx_1\dots dx_n$$