### Sum of 2 random variables
- When $Z=X+Y$
#### Discrete case
$$
\begin{align*} p_{Z}(z) &= P(X + Y = z) \\ &= \sum_{x} p(x, z - x) \\ &= \sum_{y} p(z - y, y) \end{align*}
$$

#### Continuous case
- cdf 
$$
\begin{align*}
F_{Z}(z) &= P(Z \le z) = P(X + Y \le z) \\
&= P(Y \le z - X) = \int_{-\infty}^{\infty} \int_{-\infty}^{z - x} f(x, y) \, dy \, dx \\
&= P(X \le z - Y) = \int_{-\infty}^{\infty} \int_{-\infty}^{z - y} f(x, y) \, dx \, dy \\
\end{align*}
$$
 - pdf 
 $$
\begin{align*} f_{Z}(z) &= F'(z) \\ &= \int_{-\infty}^{\infty} f(x, z - x) \, dx \\ &= \int_{-\infty}^{\infty} f(z - y, y) \, dy \end{align*}
$$
### Difference between 2 random variables
- When $Z=X-Y$
#### Discrete case
$$
\begin{align*} p_{Z}(z) &= P(X - Y = z) \\ &= \sum_{x} p(x, x - z) = \sum_{y} p(z + y, y) \end{align*} 
$$
#### Continuous case
- cdf 
$$
\begin{aligned}
F_{Z}(z) &= P(Z \le z) = P(X - Y \le z) \\
&= P(Y \ge X - z) = \int_{-\infty}^{\infty} \int_{x-z}^{\infty} f(x, y) \, dy \, dx \\
&= P(X \le z + Y) = \int_{-\infty}^{\infty} \int_{-\infty}^{z+y} f(x, y) \, dx \, dy
\end{aligned}
$$
- pdf 
$$
\begin{align*} f_{Z}(z) &= F'(z) \\ &= \int_{-\infty}^{\infty} f(x, x - z) \, dx \\ &= \int_{-\infty}^{\infty} f(z + y, y) \, dy \end{align*}
$$
### Product of 2 random variables
- When $Z=XY$
#### Discrete case
$$
\begin{align*} p_{Z}(z) &= P(XY = z) \\ &= \sum_{x} p\left(x, \frac{z}{x}\right) \\ &= \sum_{y} p\left(\frac{z}{y}, y\right) \end{align*}
$$
#### Continuous case
- cdf 
$$
\begin{aligned} F_{Z}(z) &= P(Z \le z) = P(XY \le z) \\ &= P(Y \le z/X, X > 0) + P(Y \ge z/X, X < 0) \\ &= \int_{0}^{\infty} \int_{-\infty}^{z/x} f(x, y) \, dy \, dx + \int_{-\infty}^{0} \int_{z/x}^{\infty} f(x, y) \, dy \, dx \end{aligned}
$$
- pdf 
$$
\begin{aligned} f_{Z}(z) &= F'(z) \\ &= \int_{0}^{\infty} f\left(x, \frac{z}{x}\right) \frac{1}{x} \, dx - \int_{-\infty}^{0} f\left(x, \frac{z}{x}\right) \frac{1}{x} \, dx \\ &= \int_{-\infty}^{\infty} f\left(x, \frac{z}{x}\right) \left| \frac{1}{x} \right| dx \\ &= \int_{-\infty}^{\infty} f\left(\frac{z}{y}, y\right) \left| \frac{1}{y} \right| dy \end{aligned}
$$
### Ratio of 2 random variables
- When $Z=\frac{X}{Y}$
#### Discrete case
$$\begin{align*} p_{Z}(z) = P\left(\frac{X}{Y} = z\right) = \sum_{x} p\left(x, \frac{x}{z}\right) = \sum_{y} p(zy, y) \end{align*}$$
#### Continuous case
- cdf 
$$
\begin{align*}
F_{Z}(z) &= P(Z \le z) = P(X/Y \le z) \\
&= P(X \le zY, Y > 0) + P(X \ge zY, Y < 0) \\
&= \int_{0}^{\infty} \int_{-\infty}^{zy} f(x, y) dx dy + \int_{-\infty}^{0} \int_{zy}^{\infty} f(x, y) dx dy
\end{align*}
$$
- pdf 
$$
\begin{align*}
f_{Z}(z) &= F'(z) = \int_{0}^{\infty} f(zy, y) y dy - \int_{-\infty}^{0} f(zy, y) y dy \\
&= \int_{-\infty}^{\infty} f(zy, y) |y| dy = \int_{-\infty}^{\infty} f\left(x, \frac{x}{z}\right) \frac{|x|}{z^{2}} dx
\end{align*}
$$