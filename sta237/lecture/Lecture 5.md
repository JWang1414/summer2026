# Beta Distribution
> A continuous random variable $X$ has a beta distribution with parameters $a>0$ and $b>0$ if its density is
$$
	f(x) = \frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)} x^{a-1} (1-x)^{b-1}, \qquad 0<x< 1
$$
> Often written as $X\sim\text{Beta}(a, b)$

When $a=b=1$ the beta function is simply the uniform function. The $a$ and $b$ parameters are responsible for changing the shape of the function in various ways.

Furthermore, we have the following identity:
$$
	\int_{0}^{1} x^{a-1}(1-x)^{b-1} \, dx = \frac{\Gamma(a)\Gamma(b)}{\Gamma(a+b)}
$$
For $a, b>0$.

Substituting this identity into the definition of the beta distribution, you will find that the beta distribution integrates to 1.
- That is, it's normalised
# Quantiles and Percentiles
Let $X$ be a random variable with cumulative distribution function $F$, and let $p$ be a number between 0 and 100.

Definition:
> The p% quantile, or the $p$-th percentile, of the distribution of X is the smallest number $q_{p}$ such that
$$
	F(q_{p}) = P(X\leq q_{p}) \geq  \frac{p}{100}
$$
> This is essentially stating that the quantile is the quantity associated with the percentile.

Recall that the median of a distribution is the 50-th percentile.

In some continuous cases, this simplifies into:
$$
	F(q_{p}) = \frac{p}{100}
$$

For continuous random variables, if $F$ is strictly increasing and therefore invertible, the $p$-th percentile is given by:
$$
	q_{p} = F^{-1}\left( \frac{p}{100} \right)
$$
# Normal Distribution Approximations
For a normal distribution, we have:
$$
	P(\mu-\sigma < X < \mu+\sigma) \approx 0.68
$$
$$
	P(\mu-2\sigma < X < \mu+2\sigma) \approx 0.95
$$
$$
	P(\mu-3\sigma < X < \mu+3\sigma) \approx 0.997
$$
Interquartile Range:
> The difference between the 75-th and 25-th quantiles, also called the third and first quartiles. It is essentially the middle 50% values of the distribution.

For the normal distribution, we always have
$$
	\text{IQR} = 1.35\sigma
$$
# Expectation of a Discrete Random Variable
> The expectation of a discrete random variable $X$ taking values $x_{1}, x_{2}, \dots$ and with probability mass function $p$ is
$$
	E[X] = \sum_{i} x_{i}p(x_{i})
$$
- Notice that this is identical to expectation values in quantum mechanics

The expectation value of a discrete uniform distribution is:
$$
	E[X] = \frac{n+1}{2} \qquad X\sim \text{Unif}(1, \dots, n)
$$
For a Bernoulli random variable:
$$
	E[X]=p \qquad X\sim \text{Ber}(p)
$$
For a geometric distribution:
$$
	E[X] = \frac{1}{p} \qquad X\sim \text{Geo}(p)
$$
For a Poisson distribution:
$$
	E[X] = \lambda \qquad X\sim \text{Poisson}(\lambda)
$$
For a binomial distribution:
$$
	E[X] = np \qquad X\sim \text{Binomial}(n, p)
$$
# Expectation of a Continuous Random Variable
> The expectation of a continuous random variable $X$ with probability density function $f$ is
$$
	E[X] = \int_{-\infty}^{\infty} xf(x) \, dx
$$
> This value essentially represents the "centre of mass" for the probability distribution of $X$

The expectation of an exponential random variable is:
$$
	E[Y] = \frac{1}{\lambda} \qquad f(x) = \lambda e^{ -\lambda y }
$$
# Key Properties of Expectation
The expectation value is linear:
$$
	E[rX+s] = rE[X]+s
$$
The mean-centred deviation of $X$ is always 0,
$$
	E[X-E[X]] = E[X] - E[X] =0
$$

Furthermore, note that not all distributions have an expectation. If the integral does not converge, for example, then the expectation may not be possible to establish.

- The expectation of any symmetric distribution is the point of symmetry
- The expectation of a constant is a constant

The expectation of a function of a random variable is:
$$
	E[g(X)] = \sum_{x \in S} g(x)P(X=x) \qquad E[g(X)] = \int_{-\infty}^{\infty} g(x)f(x) \, dx
$$
Where $g(X)$ is the function of the random variable. So we average over the values of $g(X)$ as opposed to $X$.