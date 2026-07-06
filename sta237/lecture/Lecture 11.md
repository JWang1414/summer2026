# Sampling Distribution
> The probability distribution of a given statistic based on a random sample. It is, for example, the probability distribution of the mean for all possible random samples from the population.
# Central Limit Theorem
> Let $X_{1}, X_{2}, \dots$ be an i.i.d. sequence of random variables with finite mean $\mu$ and variance $\sigma^{2}$. For $n\in \mathbb{N}$, let $S_{n}=X_{1}+\dots X_{n}$ and $\bar{X}_{n}=S_{n} /n$. Then the distribution of the standardised random variable $\left( \frac{\bar{X}_{n}-\mu}{\sigma /\sqrt{ n }} \right)$ converges to a standard normal distribution in the following sense. For all $t$,
$$
	P\left( \frac{\bar{X}_{n}-\mu}{\sigma /\sqrt{ n }}\leq t \right) \to P(Z\leq t) \qquad \text{as }n\to \infty
$$
> Where $Z\sim\text{Norm}(0, 1)$

The CLT essentially states that the distribution of $\bar{X}_{n}$ will be centred around the population mean $\mu$ even if the population distribution is not. Furthermore, as the sample size $n$ increases, the distribution will become progressively more concentrated around $\mu$.

For symmetrical distributions like the Poisson distribution below, this feels obvious:
![[Pasted image 20260616181903.png]]

However, notably, the CLT still holds for non-symmetrical distributions, like the exponential distribution:
![[Pasted image 20260616182031.png]]
## Sample Size
The CLT only holds for "large $n$", so how large should this $n$ be?

Empirical evidence suggests $n\approx 30$ is typically enough for the CLT to be a relatively good approximation.
- Heavily skewed distributions may require a larger $n$, and vice versa
# Class notes
- I missed a few slides at the start
- 21-28

- The $\bar{X}_{n}$ in the CLT denoting the distribution of the means is the distribution of the possible means. So, the density represents the probability that the mean takes that value
- The CLT essentially states that the distribution of the mean will always tend towards a normal distribution
- This is even true in the exponential population distribution, despite it not being symmetric

- I couldn't go through a number of examples here either
