### Definition
#### Formal
Let $N(t)$ denote the number of occurrences of an event up to time $t \geq 0$. $\{N(t):t \geq 0\}$ is a **Poisson process** with rate $\lambda>0$ if
- *Initial condition:* $N(0) = 0$
- *Independent increments:* The numbers of occurrences in disjoint time intervals are independent *i.e.* For any integer $n \geq 1$ and any times $0 \leq t_{0} \le t_{1} \le ... \le t_{n}$, the increments $N(t_{1}) - N(t_{0}), N(t_{2}) - N(t_{1}), \dots, N(t_{n}) - N(t_{n-1})$ are mutually independent random variables
- *Stationary increments:* The distribution of the number of occurrences in an interval depends only on the length of the interval, not on its location in time *i.e.* For every $t\geq 0$, $h \geq 0$, $k \in \mathbb{N}\cup \{0\}$,  
$$
P(N(t + h) - N(t) = k) = P(N(h) = k)
$$
- *Infinitesimal probabilities*: For a small $h > 0$, 
$$
\begin{align*} P(N(t + h) - N(t) = 1) &= \lambda h + o(h) \\ P(N(t + h) - N(t) \ge 2) &= o(h) \end{align*}
$$
#### Informal
Let an event $E$, occurring at a given time, satisfy the following conditions:
- *Independence*: The number of times that $E$ occurs in disjoint time intervals are independent
- *Lack of clustering*: The probability of two or more occurrences in a sufficiently short time interval is negligible
- *Rate*: The probability of exactly 1 occurrence in a sufficient short time interval of length $h$ is approximately proportional to $h$ *i.e.* approximately $\lambda h$ for some constant $\lambda>0$

If $N(t)$ represents the number of occurrences of $E$ in time interval $[0,t]$, then the counting process $\{N(t):t\geq 0\}$ is a **Poisson process** with $\lambda > 0$
### Application
- [[Poisson Distribution]]
- [[Exponential Distribution]]
- [[Gamma Distribution]]