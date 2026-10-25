### Proposition
If X is a non-negative random variable i.e. $X(\omega) \geq 0 \quad \forall \omega \in \Omega$ with finite mean, then for any constant $c>0$, 
$$
P(X \ge c) \le \frac{E(X)}{c}
$$
#### Proof
$$
\begin{aligned}
E(X) &= \int_{0}^{\infty} x f(x) dx \\
&= \int_{0}^{c} x f(x) dx + \int_{c}^{\infty} x f(x) dx \\
&\ge \int_{c}^{\infty} x f(x) dx \ge c \int_{c}^{\infty} f(x) dx = c P(X \ge c) \end{aligned}
$$