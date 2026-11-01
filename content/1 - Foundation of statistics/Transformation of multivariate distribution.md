### When
- Determine the [[Joint distribution|joint pdf]] of the transformed random variables  
	- Let $X_{1},...,X_{n}$ be jointly distributed continuous random variable. Need to obtain the joint distribution of the random variable $Y_{1},..., Y_{n}$  which arise as functions of $X_{i}$'s 
	- *e.g.* $Y_{1}=X_{1}+X_{2}$ and $Y_{2}=X_{1}-X_{2}$
### Concept
- *Which:* [[Transformation of single random variable|generalisation of one-variable transformation]]
### Theorem
Let $X_{1},...,X_{n}$ be jointly distributed continuous random variables with [[Joint distribution|joint pdf]] $f_\mathbf{X}(x_{1},...,x_{n})$, and $Y_{i}= g_{i}(X_{1},...,X_{n})$ where $i=1,...,n$ and $g_{i}$ satisfies the following conditions
- The transformation from $X_{i}$ to $Y_{i}$ is one-to-one *i.e.* the equation $y_{i}=g_{i}(x_{1},...,x_{n})$ can be uniquely solved for $x_{1},...,x_{n}$ in terms of $y_{1},...,y_{n}$ such as  $x_{i}=h_{i}(y_{1},...,y_{n})$ for some functions $h_{i}$
- $g_{i}$'s have continuous partial derivatives at all points $(x_{1},...,x_{n})$ and the $n \times n$ Jacobian determinant is non-zero *i.e.* 
$$
J(x_{1}, x_{2}, \dots, x_{n}) = \begin{vmatrix}
\frac{\partial g_{1}}{\partial x_{1}} & \frac{\partial g_{1}}{\partial x_{2}} & \cdots & \frac{\partial g_{1}}{\partial x_{n}} \\
\frac{\partial g_{2}}{\partial x_{1}} & \frac{\partial g_{2}}{\partial x_{2}} & \cdots & \frac{\partial g_{2}}{\partial x_{n}} \\
\vdots & \vdots & \vdots & \vdots \\
\frac{\partial g_{n}}{\partial x_{1}} & \frac{\partial g_{n}}{\partial x_{2}} & \cdots & \frac{\partial g_{n}}{\partial x_{n}}
\end{vmatrix} \neq 0
$$

Then 
$$
f_{\mathbf{Y}}(y_{1},..., y_{n})=f_\mathbf{X}(x_{1},...,x_{n}) \times |J(x_{1},...,x_{n})|^{-1}
$$
### Practice
If it is complicated to find $J(x_{1},..., x_{n})$, then use the following formula to find it
Assume $h_{i}$'s are the inverse transformation *i.e.* $x_{i}=h_{i}(y_{1},...,y_{n})$
$$
\begin{align*} J(x_{1}, x_{2}, \dots, x_{n})^{-1} &= \begin{vmatrix}
\frac{\partial g_{1}}{\partial x_{1}} & \frac{\partial g_{1}}{\partial x_{2}} & \cdots & \frac{\partial g_{1}}{\partial x_{n}} \\
\frac{\partial g_{2}}{\partial x_{1}} & \frac{\partial g_{2}}{\partial x_{2}} & \cdots & \frac{\partial g_{2}}{\partial x_{n}} \\
\vdots & \vdots & \vdots & \vdots \\
\frac{\partial g_{n}}{\partial x_{1}} & \frac{\partial g_{n}}{\partial x_{2}} & \cdots & \frac{\partial g_{n}}{\partial x_{n}}
\end{vmatrix}^{-1}  \\ \\  &= \begin{vmatrix}
\frac{\partial h_{1}}{\partial y_{1}} & \frac{\partial h_{1}}{\partial y_{2}} & \cdots & \frac{\partial h_{1}}{\partial y_{n}} \\
\frac{\partial h_{2}}{\partial y_{1}} & \frac{\partial h_{2}}{\partial y_{2}} & \cdots & \frac{\partial h_{2}}{\partial y_{n}} \\
\vdots & \vdots & \vdots & \vdots \\
\frac{\partial h_{n}}{\partial y_{1}} & \frac{\partial h_{n}}{\partial y_{2}} & \cdots & \frac{\partial h_{n}}{\partial y_{n}}
\end{vmatrix} \end{align*}
$$