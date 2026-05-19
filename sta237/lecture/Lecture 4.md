# Poisson Distribution
The binomial settings requires a fixed number of trials. But what if instead we would like to count the number of events in a fixed time period, with a varying number of trials?

Definition:
> A discrete random variable $X$ has a Poisson distribution with parameter $\lambda$, $\lambda>0$, if its PMF is given by
$$
	p_{X} = e^{ -\lambda } \frac{\lambda ^{x}}{x!}
$$
> Often denoted as $\text{Pois}(\lambda)$.

One may also show that, for some binomial random variable $X_{n}\sim\text{Bin}(n, p_{n})$, if $np_{n}\to \lambda$ as $n\to \infty$ and $p_{n}\to 0$ then $X_{n}\to X\sim\text{Pois}(\lambda)$.
# Hypergeometric Distribution
If,
- The population or set is finite with size $N$
- Each individual can be characterised as a success or failure, and there are $M$ successes in the population
- A sample of $n$ elements are selected without replacement such that each subset of size $n$ is equally likely to be chosen
Then the number of successes in the sample is a hypergeometric random variable denoted $X\sim\text{HyperGeo}(n, M, N)$

Naturally, within this setup there are $M$ successes and $N-M$ failures.

Definition:
> If $X$ is the number of successes, then the probability distribution of $X$ is given by the hypergeometric distribution:
$$
	p_{X}(X=x) = \frac{\begin{pmatrix}
	M \\
	x
	\end{pmatrix} \begin{pmatrix}
	N-M \\
	n-x
	\end{pmatrix}}{\begin{pmatrix}
	N \\
	n
	\end{pmatrix}}
$$
# Negative Binomial Distribution
Given that:
- The experiment consists of a sequence of independent trials
- Each trial results in a success or failure
- The probability of success is constant from trial to trial
- The experiment continues until a total of $r$ successes have been observed, where $r$ is a specified positive integer
Then the number of trials required to achieve the $r$-th success is called a negative binomial random variable denoted by $X\sim\text{NB}(r, p)$.

Definition:
> The PMF of the negative binomial random variable $X$ with parameters $r$ and $p$ is given by:
$$
	p_{X}(X=x) = \begin{pmatrix}
	x-1 \\
	r-1
	\end{pmatrix} p^{r}(1-p)^{x-r}
$$
# Continuous Random Variable and Probability Density
> A random variable $X$ is continuous if there exists a function $f:\mathbb{R}\to \mathbb{R}$ such that for any $a\leq b$, the probability that $X$ falls within the interval $[a, b]$ is given by
$$
	P(a\leq  X\leq  b) = \int_{a}^{b} f(x) \, dx
$$
> Where $f$ is called the *probability density function* of $X$. The value $f(x)$ represents the probability density of $X$ at $x$.

The function $f$ in the PDF must satisfy:
- $f(x)>0$ for all $x$
- $\int_{-\infty}^{\infty} f(x) \, dx=1$

Notes:
- While a PMF represents probability, a PDF does not
- A PDF maps $\mathbb{R}$ to $[0, \infty)$ whereas a PMF maps $\mathbb{R}$ to $[0, 1]$. Therefore, a PDF can result in values that are arbitrarily large
- Probability density is more like a relative measure of likelihood around a given value compared to other values that the corresponding random variable can take
- For continuous random variables, open and closed intervals yield the same results. $P(a\leq X\leq b)= P(a<X<b)$

- The behaviour is basically identical to quantum wavefunctions.
# Cumulative Distribution Function
> The cumulative distribution function $F$ of a random variable $X$ is the function $F:\mathbb{R}\to[0, 1]$, defined by
$$
	F(a)=P(X\leq a)
$$
> for all real numbers $a$

Notice that this definition is identical to the one for discrete random variables. The function $F(a)$ always gives the probability that the random variable $X$ takes on a value less than or equal to $a$.

A random variable is deemed continuous if its CDF $F$ is continuous everywhere.

For a continuous random variable $X$ with PDF $f$ , the CDF $F(a)$ is expressed as:
$$
	F(a)=\int_{-\infty}^{a} f(x) \, dx
$$
# Uniform Distribution
> A continuous random variable has a uniform distribution on the interval $[\alpha, \beta]$ if its probability density function $f$ is given by:
$$
	f(x) = \begin{cases}
	\frac{1}{\beta-\alpha} & \text{when }\alpha\leq x\leq \beta \\
	0 & \text{otherwise}
	\end{cases}
$$

A continuous distribution used for assigning equal likelihoods across a fixed interval.
# Exponential Distribution
> A continuous random variable has an exponential distribution with parameter $\lambda$, $\lambda>0$, if its probability density function $f$ is given by:
$$
	f(x) = \lambda e^{ -\lambda x } \qquad \text{for }x\geq  0
$$
- Often represents the time until the next event in a sequence of events
- $\lambda$ is called the rate parameter, and represents the average number of event occurrences per some interval
# Gamma Distribution
> A continuous random variable $X$ has a gamma distribution with shape parameter $\alpha>0$ and rate parameter $\beta>0$ if its density is
$$
	f(x) = \frac{\beta ^{\alpha}}{\Gamma(\alpha)} x^{\alpha-1} e^{ -\beta x } \qquad x>0
$$
> Where $\alpha$ is the shape parameter, $\beta$ is the rate parameter, and $\Gamma(\alpha)$ is the gamma function. For a positive integer $n$,
$$
	\Gamma(n)=(n-1)!
$$

When $\alpha-1$ the gamma distribution reduces to the exponential distribution,
$$
	\text{Gamma}(1, \beta) = \text{Exp}(\beta)
$$

An alternative representation instead uses the scale parameter $\theta=\beta ^{-1}$. The gamma distribution then becomes,
$$
	f(x) = \frac{1}{\Gamma(\alpha)\theta ^{\alpha}} x^{\alpha-1} e^{ -x/\theta } \qquad x>0
$$
These representations either use the shape and rate parameters, or the shape and scale parameters. Larger $\theta$ stretches the distribution to the right.
## Gamma Function
Extends the idea of factorials to non-integer values. For $\alpha>0$ the gamma function is defined by:
$$
	\Gamma(\alpha) = \int_{0}^{\infty} t^{\alpha-1} e^{ -t } \, dt
$$
This essentially allows the gamma distribution to have any shape parameter $\alpha>0$ as opposed to just positive integers.
# Normal Distribution
> A continuous random variable has a normal distribution with mean $\mu$, variance $\sigma^{2}$, where $\sigma^{2}>0$, if its PDF is given by:
$$
	f(x) = \frac{1}{\sigma \sqrt{ 2\pi }} \exp\left( -\frac{1}{2}\left( \frac{x-\mu}{\sigma} \right)^{2} \right)
$$
> Often denoted as $N(\mu, \sigma^{2})$.
## Standard Normal Distribution
Integrals of the normal distribution often do not have a simple elementary closed-form expression. Typically, normal probabilities are computed by transforming the random variable into a standard normal random variable.

Definition:
> A normal random variable with $\mu=0$ and $\sigma^{2}=1$ is called a standard normal random variable.
$$
	Z\sim N(0, 1)
$$

The probability density function becomes,
$$
	\phi(z) = \frac{1}{\sqrt{ 2\pi }} e^{ -z^{2}/2 }
$$
And the associated cumulative distribution function is:
$$
	\Phi(a) = P(Z\leq a) = \int_{-\infty}^{a} \phi(z) \, dz
$$

Suppose we have some normal variable $X\sim N(\mu_{X}, \sigma^{2}_{X})$. We standardise $X$ by subtracting its mean and dividing by the standard deviation:
$$
	Z = \frac{X-\mu_{X}}{\sigma_{X}}
$$
For any value $x$ we have,
$$
	P(X\leq x) = P\left( Z\leq  \frac{x-\mu_{X}}{\sigma_{X}} \right) = \Phi\left( \frac{x-\mu_{X}}{\sigma_{X}} \right)
$$
# Class Notes
Example: Probability of Major Earthquakes Next Year
- Should be 46 years, because it does not include 2016

Capture-Recapture: Probability Calculations
- Part b on the slides is incorrect
