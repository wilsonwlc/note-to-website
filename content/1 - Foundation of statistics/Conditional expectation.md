### Definition
The **conditional expectation** of $g(Y)$ given $X= x$ is defined as
#### Discrete case
$$
E(g(Y) \mid X = x) = \sum\limits_{i} g(i) p_{Y \mid X}(i \mid x)
$$
#### Continuous case
$$
E(g(Y) \mid X = x) = \int_{-\infty}^{\infty} g(t) f_{Y \mid X}(t \mid x) dt
$$