# Variance of a Random Variable
The variance $\text{Var}(X)$ measures the spread of the distribution by quantifying the mean squared distance from the distribution’s centre, the expected value.
$$
	\text{Var}(X) = E[(X-E[X])^{2}] = E[X^{2}] - (E[X])^{2}
$$
For any random variable $X$ and constants $r$ and $s$, the variance under transformation is given by:
$$
	\text{Var}(rX+s) = r^{2}\text{Var}(X)
$$
The standard deviation of a random variable is the square root of its variance.
$$
	\text{sd}(X) = \sqrt{ \text{Var}(X) }
$$
Both measure the spread of a distribution, but the standard deviation is expressed in the same units as $X$.

The variance of a Bernoulli random variable is:
$$
	\text{Var}(X) = (1-p)p \qquad X\sim \text{Ber}(p)
$$
# Moment Generating Function
The Moment Generating Function (MGF) of a random variable $X$, denoted by $M_{X}(t)$ is:
$$
	M_{X}(t) = E[e^{ tX }]
$$
The MGF characterises the distribution if it exists for $t$ near 0, and enables deriving moments (mean, variance, etc.) by differentiation:
$$
	E[X^{n}] = \frac{d^{n}M_{X}(t)}{dt^{n}} \bigg|_{t=0}
$$
---
Example:
The MGF of a Poisson random variable is:
$$
	M_{X}(t) = E[e^{ tX }] = \sum_{k=0}^{\infty} e^{ tk } \frac{\lambda ^{k}e^{ -\lambda }}{k!} = e^{ \lambda(e^{ t }-1) }
$$
Solve for the mean using the MGF:
$$
	\frac{d}{dt} M_{X}(t) \big|_{t=0} = \lambda e^{ t }e^{ \lambda }(e^{ t-1 }) \big|_{t=0} = \lambda
$$
Solve for the variance:
$$
	M_{X}''(t) = \lambda e^{ t } M_{X}(t) (1+\lambda e^{ t })
$$
$$
	\text{Var}(X) = M_{X}''(0) - [M_{X}'(0)]^{2} = \lambda(1+\lambda) - \lambda^{2}=\lambda
$$
---
Example:
The MGF of the normal distribution is:
$$
	M_{X}(t) = e^{ \mu t+\sigma^{2}t^{2}/2 }
$$
Going through the same process, the mean of the normal distribution is:
$$
	M_{X}'(t) \big|_{t=0} = (\mu+\sigma^{2}t) e^{ \mu t+\sigma^{2}t^{2}/2 } \big|_{t=0} = \mu
$$
And the variance is:
$$
	M''_{X}(t) = \sigma^{2}e^{ \mu t+\sigma^{2}t^{2}/2 } + (\mu+\sigma^{2}t)^{2} e^{ \mu t+\sigma^{2}t^{2}/2 }
$$
$$
	\text{Var}(X) = \sigma^{2}
$$
---
# Variable Transformation
The expectation of a function of a random variable allows us to compute the expectation of a transformed random variable without deriving its full distribution.

We, for example, accomplish this during our computation of expectation values:
$$
	E[Y] = E[g(X)] = \sum_{x}g(x)P(X=x)
$$
# Transformation to a Discrete Random Variable
Definition:
> Let $X$ be a discrete random variable with probability mass function $p_{X}$ , and let $Y=g(X)$, where $g:\mathbb{R}\to \mathbb{R}$ is a function. Then $Y$ is also a discrete random variable. Its possible values are
$$
	S_{Y} = \{ g(X):x \in S_{X} \}
$$
> where $S_{X}$ is the support of $X$.

For any possible value $y$ of $Y$
$$
	p_{Y}(y) = P(Y=y) = \sum_{\{ x \in S_{X} : g(x)=y \}} p_{X}(x)
$$
So, if several values of $X$ give the same value of $Y$, their probabilities should be added.
# CDF and PDF
Recall that we can compute the CDF from the PDF like so:
$$
	F_{X}(x) = \int_{-\infty}^{x} f_{X}(t) \, dt
$$
Which tells us that at points where $F_{X}$ is differentiable:
$$
	f_{X}(x) = \frac{d}{dx}F_{X}(x)
$$
This interpretation tells us that while the CDF accumulates probability, the PDF is the rate at which the accumulated probability changes.
## Scaling an Exponential Random Variable
Multiplying an exponential random variable with mean $\mu$ by a positive constant $c$ results in another exponential random variable with mean $c\mu$

That is, if $X\sim\text{Exp}(\lambda)$ then,
$$
	Y = cX \sim \text{Exp}\left( \frac{\lambda}{c} \right)
$$
If $X_{1}$ and $X_{2}$ are independent exponential functions, then,
$$
	Y = X_{1}+X_{2} \sim \text{Gamma}(2, \lambda)
$$
# Transformation to a Continuous Random Variable
> Let $X$ have PDF $f_{X}(x)$ and let $Y=g(X)$, where $g$ is monotonic on the set of all possible values of $X$, so it has an inverse function $X=g^{-1}(Y)=h(Y)$. Then:
$$
	f_{Y}(y) = f_{X}(h(y)) \lvert h'(y) \rvert
$$
> Where we have assumed $h(y)$ is differentiable.

- A number of examples are included in the lecture notes
