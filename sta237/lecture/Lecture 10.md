# Conditional Covariance/Correlation
The conditional covariance between random variables $X$, $Y$ given another random variable $Z$ is
$$
	\text{Cov}(X, Y|Z) = E((X-E(X|Z))(Y-E(Y|Z))|Z) = E(XY|Z) - E(X|Z)E(Y|Z)
$$
With the associated conditional correlation:
$$
	\text{Corr}(X, Y|Z) = \frac{\text{Cov}(X, Y|Z)}{\sqrt{ \text{Var}(X|Z)\text{Var}(Y|Z) }}
$$

Law of Total Covariance:
$$
	\text{Cov}(X , Y ) = E (\text{Cov}(X , Y | Z )) + \text{Cov}(E (X | Z ), E (Y | Z ))
$$
# Markov’s Inequality
> Let $X$ be a non-negative random variable with finite expectation. Then for all $\epsilon>0$,
$$
	P(X\geq \epsilon) \leq  \frac{E[X]}{\epsilon}
$$

One common application of Markov's inequality defines $\epsilon=kE[X]=k\mu$, for some positive integer $k$. This tells us that,
$$
	P(X\geq k\mu) \leq \frac{1}{k}
$$
So, for example, the probability of a random variable is twice its mean is at most 1/2.

It follows as a corollary that,
$$
	P(g(X)\geq g(\epsilon)) \leq  \frac{E[g(X)]}{g(\epsilon)}
$$
Chebyshev’s Inequality:
> Let $X$ be a random variable (not necessarily positive) with finite mean $\mu$ and variance $\sigma^{2}$. Then for all $\epsilon>0$,
$$
	P(\lvert X-\mu \rvert \geq \epsilon) \leq  \frac{\sigma^{2}}{\epsilon^{2}} \qquad P(\lvert X-\mu \rvert <\epsilon) \geq  1-\frac{\sigma^{2}}{\epsilon^{2}}
$$

Rearranging Chebyshev's inequality you will also find,
$$
	P(\lvert X-\mu \rvert \geq k\sigma) \leq  \frac{1}{k^{2}}
$$
Similar to the application of Markov's inequality from before.
# Statistic
A *statistic* is any quantity that can be calculated from sample data. It is an example of a random variable.

Uppercase letters are used to denote statistics, and lowercase letters denote the observed values.

The sample mean and variance are both examples of statistics:
$$
	\bar{X} = \frac{1}{m} \sum_{i=1}^{n} X_{i} \qquad S^{2} = \frac{1}{n-1} \sum_{i=1}^{n} (X_{i}-\bar{X})^{2}
$$
## Random Samples
The random variables $X_{1}, \dots, X_{n}$ are said to form a (simple) random sample of size $n$ if
1. The $X_{i}$'s are independent random variables
2. Every $X_{i}$ has the same probability distribution
Such a collection of random variables is also called *independent and identically distributed* (iid).
## Expectation and Variance of an Average
If $\bar{X}_{n}$ is the average of $n$ independent random variables with the same expectation $\mu$ and variance $\sigma^{2}$, then
$$
	E[\bar{X}_{n}] = \mu \qquad \text{Var}(\bar{X}_{n}) = \frac{\sigma^{2}}{n}
$$
# Weak Law of Large Numbers
> Let $X_{1}, X_{2}, \dots$ be an i.i.d. sequence of random variables with $E[X_{i}]=\mu$, and $\text{Var}(X_{i})=\sigma^{2}<\infty$. For
$$
	\bar{X}_{n} = \frac{1}{n}(X_{1}+\dots+X_{n})
$$
> we have, for every $\epsilon>0$,
$$
	P(\lvert \bar{X}_{n}-\mu \rvert \geq \epsilon)\to 0 \qquad \text{as }n\to \infty
$$
> That is, for a large sample size $n$, the average is likely to be close to the population mean $\mu$.

This is denoted as,
$$
	\bar{X}_{n}\xrightarrow{p} \mu
$$
Notes:
- The requirement that we have finite variance $\sigma^{2}<\infty$ is not necessary for the weak law of large numbers to hold. It is there to simplify the proof presented in class
- The type of convergent described by the weak law of large numbers is called *convergence in probability*
# Strong Law of Large Numbers
> Let $X_{1}, X_{2}, \dots$ be an i.i.d. sequence of random variables with $E[X_{i}]=\mu$ and $E\lvert X_{i} \rvert<\infty$. For
$$
	\bar{X}_{n} = \frac{1}{n}(X_{1}+\dots+X_{n})
$$
> we have
$$
	P\left( \lim_{ n \to \infty } \bar{X}_{n}=\mu \right) =1
$$

This essentially states that the sample average $\bar{X}_{n}$ converges to the population mean $\mu$ with probability 1.
$$
	\bar{X}_{n} \xrightarrow{a.s.} \mu
$$
This type of convergence described by the strong law of large numbers is called almost sure convergence.

- The SLLN is about the probability of a limit, whereas the WLLN is about the limit of probabilities.
- Almost sure convergence is stronger than convergence in probability
$$
	Y_{n} \xrightarrow{a.s.}Y \implies Y_{n} \xrightarrow{p}Y
$$
