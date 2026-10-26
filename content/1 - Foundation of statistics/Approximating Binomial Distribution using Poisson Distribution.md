### Theorem
When $n$ is large and $p$ is small such that $np$ is bounded, then the [[Binomial distribution|binomial distribution]] $b(n,p)$ can be approximated by the [[Poisson Distribution]], $\text{Poisson}(p)$ *i.e.* $$p(x) = \binom{n}{x} p^{x} (1 - p)^{n - x} \approx \frac{e^{-np} (np)^{x}}{x!}$$
### Practice
- This approximation should be very successful if $n \geq 100$ and $np \leq 10$