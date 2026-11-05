### Concept
- *What is it:* the coefficients that appear when [[Cumulant generating function (CGF)|cumulant generating function (CGF)]] is expanded in a **Taylor series** about the origin *i.e.* **Maclaurin series**
### Definition
$$\kappa_n = K^{(n)}(0) = \left.\frac{d^n}{dt^n} K(t)\right|_{t=0}$$
### Comparison
#### Cumulant vs Raw moment
- $\kappa_{1} = \mu'_{1}$
- $\kappa_{2} = \mu'_{2} - {\mu'_{1}}^{2}$
- $\kappa_{3} = 2 {\mu'_{1}}^{3} - 3 \mu'_{1} \mu'_{2} + \mu'_{3}$
- $\kappa_{4} = -6 {\mu'_{1}}^{4} + 12 {\mu'_{1}}^{2} \mu'_{2} - 3 {\mu'_{2}}^{2} - 4 \mu'_{1} \mu'_{3} + \mu'_{4}$
- $\kappa_{5} = 24 {\mu'_{1}}^{5} - 60 {\mu'_{1}}^{3} \mu'_{2} + 20 {\mu'_{1}}^{2} \mu'_{3} - 10 \mu'_{2} \mu'_{3} + 5 \mu'_{1} \left(6 {\mu'_{2}}^{2} - \mu'_{4}\right) + \mu'_{5}$
#### Cumulant vs Central moment
- $\kappa_{1} = \mu$
- $\kappa_{2} = \mu_{2} = \operatorname{Var}(X)$
- $\kappa_{3} = \mu_{3}$
- $\kappa_{4} = \mu_{4} - 3 \mu_{2}^{2}$
- $\kappa_{5} = \mu_{5} - 10 \mu_{2} \mu_{3}$