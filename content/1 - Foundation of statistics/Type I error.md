### Motivation
- *Problem:* In hypothesis testing we use sample data, which are subject to sampling variability, to decide between $H_0$​ and $H_1$​. Because of this variability, there is always a risk of reaching the wrong conclusion
- *Solution:* Evaluate the reliability of a test by the probabilities of the two kinds of mistaken decision it can produce
### Concept
- Aka **alpha error**
- *What is it:* Type I error rate is the probability of rejecting $H_{0}$ when it is actually true 
- *What it does:* assess the reliability of the hypothesis testing
- *Notation:* $\alpha$
- *Which:* False positive
### Definition
![[Type I and II error - concept 2.png]]
$$
\alpha = P(\text{Reject } H_0 \mid H_0 \text{ true})
$$
### Comparison
#### Type I error and Type II error
- There is a trade-off between [[Type I error|Type I error]] and [[Type II error]]
- Making $\alpha$ smaller will result in a larger $\beta$, and vice versa
### Practice
- Since we can only control either $\alpha$ or $\beta$, so when designing a **test**, the convention is to guarantee $\alpha$ in a desired low level and then try to reduce $\beta$ as much as we could *i.e.* Type I error is considered as more serious than type II error. This also explains why the roles of $H_{0}$ and $H_{1}$ are not interchangeable