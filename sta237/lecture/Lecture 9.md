Class notes:

Slide 61:
We have $0<z<x$ because $y=z /x$ and so:
$$
	0<y<1 \implies 0< \frac{z}{x} <1 \implies 0<z<x
$$
Essentially, $x$ is not transformed, and so unchanged. But $y$ is being transformed to $z$, and so the new region is based on $y$.
# Change of Variables for a Joint PMF
> Let $(X, Y)$ be a pair of continuous random variables with joint density function $f_{X, Y}(x, y)$. Suppose $(U, V)$ is a transformation of $(X, Y)$ defined by
$$
	(U, V) = g(X, Y)
$$
> If the transformation is given by $u=g_{1}(x, y)$ and $v=g_{2}(x, y)$, then the joint density function of $(U, V)$ is
$$
	f_{U, V}(u, v) = f_{X, Y}(x, y) \left\lvert  \frac{\partial(x, y)}{\partial(u, v)}  \right\rvert
$$
- This requires $g$ to be one-to-one with inverse function $g^{-1}$.

Recall the definition of the Jacobian determinant
$$
	\lvert J \rvert = \left\lvert  \frac{\partial(x, y)}{\partial(u, v)}  \right\rvert = \begin{vmatrix}
	\frac{ \partial x }{ \partial u }  & \frac{ \partial x }{ \partial v }  \\
	\frac{ \partial y }{ \partial u }  & \frac{ \partial y }{ \partial v } 
	\end{vmatrix}
$$
In our case, $\partial(x, y) /\partial(u, v)$ is the Jacobian matrix of the inverse transformation.
# More Properties of the Expectation
Law of the Unconscious Statistician:
> Let $X$ and $Y$ be jointly distributed random variables with PMF $p(x, y)$ or PDF $f(x, y)$. The expected value of a function $h(X, Y)$, denoted by $E[h(X, Y)]$ or $\mu_{h(X, Y)}$ is given by:
$$
	E[h(X, Y)] = \begin{cases}
	\sum_{x}\sum_{y} h(x, y)p(x, y) \\
	\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} h(x, y)f(x, y) \, dx \, dy 
	\end{cases}
$$

Notably, this generalises to the expected value of a function $h(X_{1}, \dots, X_{n})$ of $n$ random variables. The expectation becomes either an $n$-dimensional sum, or an $n$-dimensional integral.

Linearity:
> Let $X$ and $Y$ be random variables. Then, for any functions $h_{1}, h_{2}$ and constants $a_{1}, a_{2}, b$,
$$
	E[a_{1}h_{1}(X, Y) + a_{2}h_{2}(X, Y) + b] = a_{1} E[h_{1}(X, Y)] + a_{2} E[h_{2}(X, Y)] + b
$$

Independent Random Variables:
> Let $X$ and $Y$ be independent variables. If $h(X, Y)=g_{1}(X)g_{2}(Y)$, then:
$$
	E[h(X, Y)] = E[g_{1}(X)g_{2}(Y)] = E[g_{1}(X)]E[g_{2}(Y)]
$$
# Covariance
> The covariance between two random variables $X$ and $Y$ is given by
$$
	\text{Cov}(X, Y) = E[(X-\mu_{X})(Y-\mu_{Y})] = \sigma_{XY}
$$

Notice that in the discrete and continuous cases we have:
$$
	\text{Cov}(X, Y) = \begin{cases}
	\sum_{x}\sum_{y} (X-\mu_{X})(Y-\mu_{Y})p(x, y) \\
	\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} (X-\mu_{X})(Y-\mu_{Y})f(x, y) \, dx \, dy 
	\end{cases}
$$
The covariance is effectively a measure of how strongly two variables are related to each other.
![[Pasted image 20260609144728.png]]

A few notes:
- The covariance depends on both the set of possible pairs and the probabilities
- Changing probabilities could drastically change the value of the covariance
## Properties of Covariance
$$
	\text{Cov}(X, Y) = E(XY) - E(X)E(Y)
$$
$$
	\text{Cov}(rX+s, tY+u) = rt\text{Cov}(X, Y) \qquad r, t, s, u \in \mathbb{R}
$$
$$
	X\perp Y \implies \text{Cov}(X, Y)=0
$$
$$
	\text{Cov}(X, X) = \text{Var}(X) = \sigma^{2}_{X}
$$

- Although independence implies zero covariance, the opposite is not true
# Properties of Variance
Variance of the Sum of Two Random Variables:
> Let $X$ and $Y$ be two random variables. Then:
$$
	\text{Var}(X+Y) = \text{Var}(X) + \text{Var}(Y) + 2\text{Cov}(X, Y)
$$

Notice that, in the case where $X$ and $Y$ are independent:
$$
	\text{Var}(X+Y) = \text{Var}(X) + \text{Var}(Y)
$$

Variance of the Sum of $n$ Random Variables:
> In general, let $X_{1}, \dots, X_{n}$ be $n$ random variables and $a_{1}, \dots, a_{n}$ be $n$ constants. Then:
$$
	\text{Var}\left( \sum_{i=1}^{n} a_{i}X_{i} \right) = \sum_{i=1}^{n} \sum_{j=1}^{n} a_{i}a_{j} \text{Cov}(X_{i}, X_{j})
$$
> If $X_{1}, \dots, X_{n}$ are all independent of each other, then:
$$
	\text{Var}\left( \sum_{i=1}^{n} a_{i}X_{i} \right) = \sum_{i=1}^{n} a^{2}_{i} \text{Var}(X_{i})
$$
# Correlation
The numerical value of covariance depends on the units and scales of $X$ and $Y$. Changing one variable from dollars to cents will change the covariance, making it difficult to compare across different settings.

The correlation is a unit-less, standardised covariance.

Definition:
> The *correlation coefficient* of $X$ and $Y$ , denoted by $\text{Corr}(X, Y)$, or $\rho_{X, Y}$, or just $\rho$, is defined by
$$
	\rho_{X, Y} = \frac{\text{Cov}(X, Y)}{\sigma_{X}\sigma_{Y}}
$$
> Where,
$$
	\sigma_{X}=\sqrt{ \text{Var}(X) } \qquad \sigma_{Y}=\sqrt{ \text{Var}(Y) }
$$
## Properties of Correlation
$$
	\text{Corr}(X, Y) = \text{Corr}(Y, X)
$$
$$
	\text{Corr}(X, X)=1
$$
$$
	\lvert \text{Corr}(X, Y) \rvert \leq 1
$$
Scale invariance property:
> If $a, b, c, d$ are constants, and $ac>0$,
$$
	\text{Corr}(aX+b, cY+d) = \text{Corr}(X, Y)
$$
