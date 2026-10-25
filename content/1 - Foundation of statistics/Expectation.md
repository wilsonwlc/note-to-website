### Concept
- Aka **Expected value**
### Definition
#### Univariate 
Let $X$ be a random variable with [[Probability mass function (pmf)|pmf]] $p(x)$ or [[Probability density function (pdf)|pdf]] $f(x)$
##### Discrete
$$
E(X) = \sum_{x \in X(\Omega)} x p(x)
$$
##### Continuous
$$
E(X) = \int_{-\infty}^{\infty} x f(x) dx
$$
#### Multivariate
- For $X_{1},X_{2},..., X_{n}$ (not necessarily independent) with joint pmf $p(x_{1},..., x_{n})$ or joint pdf $f(x_{1}, ..., x_{n})$
- $u(X_{1}, ..., X_{n})$ is a function of these random variables
##### Discrete
$$
E(u(X_{1}, X_{2}, \dots, X_{n})) = \sum_{x_{1}} \sum_{x_{2}} \dots \sum_{x_{n}} u(x_{1}, x_{2}, \dots, x_{n}) p(x_{1}, x_{2}, \dots, x_{n})
$$
##### Continuous 
$$
E(u(X_{1}, X_{2}, \dots, X_{n})) = \int_{-\infty}^{\infty} \dots \int_{-\infty}^{\infty} u(x_{1}, x_{2}, \dots, x_{n}) f(x_{1}, x_{2}, \dots, x_{n}) dx_{1} dx_{2} \dots dx_{n}
$$
### Property
#### Univariate
- For any function $g$, 
$$
E(g(X)) = \begin{cases} \sum_{x \in X(\Omega)} g(x) p(x) & \text{discrete} \\ \int_{-\infty}^{\infty} g(x) f(x) dx & \text{continuous} \end{cases}
$$
- If $c$ is a constant, then $E(c)=c$
- If $c$ is a constant, then $E(cg(X)) = cE(g(X))$
- If $c_1,c_2...., c_n$ are constants, then $E\left( \sum_{i=1}^{n} c_{i} g_{i}(X) \right) = \sum_{i=1}^{n} c_{i} E(g_{i}(X))$
- $X(\omega) \geq Y(\omega)$ for $\omega \in \Omega$ $\Rightarrow$ $E(X)\geq E(Y)$
- $E(|X|) \ge |E(X)|$
- Let $X$ be a random variable and $a$, $c$ be two constants 
$$
E(aX + c) = aE(X) + c
$$
#### Multivariate
- **Linearity of expectation** 
	- $E(X+Y) = E(X) + E(Y)$, where $X$ and $Y$ need not be [[Independence of random variables|independent]]
	- $E(c_{1} u_{1}(X) + c_{2} u_{2}(Y)) = E(c_{1} u_{1}(X)) + E(c_{2} u_{2}(Y))$, where $X$ and $Y$ need not be independent
- If $X$ and $Y$ are [[Independence of random variables|independent]], then 
	- $E(XY) = E(X) E(Y)$
	- $E(u_{1}(X)u_{2}(Y)) = E(u_{1}(X)) E(u_{2}(Y))$
	- The converse in both cases fails *i.e.* the product formulas alone do not imply the independence
- If $u(X_{1},X_{2},...,X_{n})=g(X_{1})$ *i.e.* $u$ is a function of $X_{1}$ only, then 
$$
\begin{align*} E(g(X_{1})) &= \sum_{x_{1}} \sum_{x_{2}} \dots \sum_{x_{n}} g(x_{1}) p(x_{1}, x_{2}, \dots, x_{n}) \\ &= \sum_{x_{1}} g(x_{1}) \sum_{x_{2}} \sum_{x_{3}} \dots \sum_{x_{n}} p(x_{1}, x_{2}, \dots, x_{n}) \\ &= \sum_{x_{1}} g(x_{1}) p_{X_{1}}(x_{1}) \end{align*}
$$