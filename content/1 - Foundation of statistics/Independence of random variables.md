### Definition
Random variable $X$ and $Y$ are **independent** if and only if, for all $x$ and $y$, 
$$
F_{X,Y}(x,y)=F_X(x)F_{Y}(y)
$$
*i.e.* The [[Joint distribution#Property|joint cdf]] can be factorised into the product of the marginal cdfs
### Practice
- Two random variables $X$ and $Y$are said to be **independent** if and only if their **joint pmf** (pdf) is equal to the product of their **marginal pmfs** (pdfs) *i.e.* for all $x$, $y$ 
$$
\begin{aligned} p_{X,Y}(x,y) &= p_X(x)p_Y(y) && \text{if } X, Y \text{ are discrete}\\ f_{X,Y}(x,y) &= f_X(x)f_Y(y) && \text{if } X, Y \text{ are continuous} \end{aligned}
$$
- $X$ and $Y$ are **dependent** if there exists $x$ and $y$ such that $p_{X,Y}(x,y) \neq p_X(x)p_Y(y)$ or $f_{X,Y}(x,y) \neq f_X(x)f_Y(y)$
### Proposition (factorisation)
Let $X$ and $Y$ be random variables with joint pdf (or pmf) $f_{X,Y}(x, y)$. Then $X$ and $Y$ are independent if and only if 
1. The supports of $X$ and $Y$ do not depend on each other *AND*
2. $f_{X,Y}(x, y)$ can be factorised as $g(x)h(y)$ for some functions $g$ and $h$
### Caution
- The above proposition also applies to discrete random variables
### Interpretation
- The first condition means the region of possible values is a rectangle
### Generalisation
$X_{1},X_{2}...,X_{n}$ are **(mutually) independent** if and only if 
$$
\begin{align*} f_{X_{1},...,X_{n}}(x_{1}, x_{2}, \dots, x_{n}) &= f_{X_{1}}(x_{1}) f_{X_{2}}(x_{2}) \cdots f_{X_{n}}(x_{n}) \quad \forall x_{1},x_{2}...,x_{n} \end{align*}
$$
### Proposition
$X_{1},X_{2}, ..., X_{n}$ are independent if and only if $\forall A_{1},A_{2},...,A_{n} \subset (-\infty, \infty)$, 
$$
\begin{aligned}  P(X_{1} \in A_{1}, X_{2} \in A_{2}, \dots, X_{n} \in A_{n}) &= P(X_{1} \in A_{1}) P(X_{2} \in A_{2}) \cdots P(X_{n} \in A_{n}) \end{aligned}
$$
### Generalisation
$X_{1},X_{2}, ..., X_{n}$ are independent if and only if 
$\forall x_{1},x_{2}...,x_{n},$ 
$$
F_{X_{1},...,X_{n}}(x_{1}, x_{2}, \dots, x_{n}) = F_{X_{1}}(x_{1}) F_{X_{2}}(x_{2}) \cdots F_{X_{n}}(x_{n})
$$