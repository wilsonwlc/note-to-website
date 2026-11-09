### Theorem
For 2 independent normal samples $X_{1}, X_{2}, \dots, X_{m} \stackrel{iid}{\sim} N(\mu_{x}, \sigma_{x}^{2})$, $Y_{1}, Y_{2}, \dots, Y_{n} \stackrel{iid}{\sim} N(\mu_{y}, \sigma_{y}^{2})$
Then, the pivot variable $$T = \frac{(\overline{X} - \overline{Y}) - (\mu_{x} - \mu_{y})}{\sqrt{\frac{S_{x}^{2}}{m} + \frac{S_{y}^{2}}{n}}}$$ is approximately distributed as $t_{\nu}$ ([[t-distribution|t-distribution]]) where the degree of freedom $\nu$ is $$\nu = \frac{\left(\frac{S_{x}^{2}}{m} + \frac{S_{y}^{2}}{n}\right)^2}{\frac{S_x^4}{m^2(m - 1)} + \frac{S_y^4}{n^2(n - 1)}}$$


