- Most of this lecture was composed of examples for the transformation of variables. Refer to the previous lecture for more detailed coverage of that topic
# Indicator Function
> Given a set $A\subseteq \Omega$, the indicator function $1_{A}$ is defined as:
$$
	1_{A}(x) = \begin{cases}
	1 & x \in A \\
	0 & \text{otherwise}
	\end{cases}
$$

Notably, it is defined such that:
$$
	E(1_{A}(X)) = \sum_{x \in A}P(X=x) = P(A)
$$
$$
	E(1_{A}(X)) = \int_{A} f_{X}(x) \, dx = P(A)
$$
In the discrete and continuous cases, respectively.

# Inverse Transform Method
> Suppose $X$ is a continuous random variable with CDF $F$, where $F$ is invertible with inverse function $F^{-1}$. Let $U \sim U(0, 1)$. Then the distribution of $F^{-1}(U)$ is equal to the distribution of $X$. Similarly, $F(X) \sim U(0, 1)$.

The inverse transform method is typically used to generate a random variable with a desired continuous distribution from $U(0, 1)$.

---
Example:
Generating samples from $\text{Exp}(1)$.

We would like to have $X\sim\text{Exp}(1)$. The CDF of this function is:
$$
	F(x) = 1-e^{ -x }
$$
By the inverse transform method:
$$
	U=F(X) \implies U=1-e^{ -X } \implies X=-\ln(1-U)
$$
Therefore, in order to transform some uniform sample from $U(0, 1)$ to the exponential distribution, we would send it through this transform:
$$
	-\ln(1-U) \equiv  -\ln U
$$
# Jensen’s Inequality
For some transformed random variable $Y=g(X)$ we would often like to compute:
$$
	E[Y] = E[g(X)]
$$
For linear functions,
$$
	E[g(X)] = g(E[X])
$$
However, more generally, for convex functions:
$$
	g(E[X]) \leq  E[g(X)]
$$
- This is Jensen's inequality

Notably, since $x^{2}$ is a convex function, this tells us,
$$
	(E[X])^{2} \leq  E[X^{2}]
$$
And so the variance is always positive.
# Class notes
Lecture 6 slides

21.
While it's possible to do this segment manually, it might be useful to remember the result:
$$
	f_{Y}(y) = \frac{1}{\lvert a \rvert } f_{X}\left( \frac{y-b}{a} \right)
$$
Where $Y=aX+b$ and $f_{X}\sim \text{Exp}(\lambda)$.

25.
$$
	f_{U}(u) = f_{Z}(u) + f_{Z}(-u)
$$
The above is true because our definition of $U=\lvert Z \rvert$ essentially splits the function of $Z$ into two segments. Each of the $f_{Z}$ functions here represent one half of the full function. Specifically, $f_{Z}(u)$ represents the case when $z\geq 0$ and $f_{Z}(-u)$ represents the case when $z< 0$.

The rest of this portion is pretty straight-forward

- When we encounter non-monotonic functions, we can try to split them up into exclusively the monotonic sections

27.
I believe the reason we use the segment $-1\leq X\leq \sqrt{ y }$ here is because we are holding the lower bound static as we vary $\sqrt{ y }$. Why we do this, I do not know

- Review textbook material afterwards

31.
Not sure what a convex function is, but it seems to include most common single variable functions
