# Question 1
The total number of requests received within one hour is,
$$
	X = X_{1}+X_{2}+X_{3}+X_{4}+X_{5}+X_{6}
$$
Where each $X_{n}$ represents the number of requests received for each 10 minutes period within the hour.

It is given that $X_{n}\sim\text{Pois}(2.5)$. Assuming that the requests are mutually independent from each other, I will apply the additive property of the Poisson distribution such that:
$$
	\text{Pois}(\lambda_{1}) + \text{Pois}(\lambda_{2}) + \dots + \text{Pois}(\lambda_{n}) = \text{Pois}(\lambda_{1}+\lambda_{2}+\dots+\lambda_{n})
$$
The final distribution is therefore:
$$
	X = \text{Pois}(6 \times 2.5) = \text{Pois}(15)
$$
The probability of receiving at least 12 but no more than 20 requests is equivalent to:
$$
	P(12\leq X\leq 20) = P(X\leq 20) - P(X\leq 11)
$$
In R this is:
```r
ppois(20, lambda = 15) - ppois(11, lambda = 15)
# Output: [1] 0.7322773
```
# Question 2
The numerical value of $a$ is:
```r
qbeta(0.7, 3, 2)
# Output: [1] 0.7276161
```

Written in terms of cumulative distribution functions:
$$
	P(X>0.6 | X\leq a) = \frac{P(X>0.6\cap X\leq a)}{P(X\leq a)} = \frac{P(0.6<X\leq a)}{P(X\leq a)}
$$
$$
	 P(X>0.6 | X\leq a) = \frac{P(X\leq a) - P(X\leq 0.6)}{P(X\leq a)} = \frac{F(a) - F(0.6)}{F(a)}
$$
Where $F(x)$ is the CDF of $\text{Beta}(3, 2)$.

Numerical value of the conditional probability obtained using R:
```r
( pbeta(qbeta(0.7, 3, 2), 3, 2) - pbeta(0.6, 3, 2) ) / pbeta(qbeta(0.7, 3, 2), 3, 2)
# Output: [1] 0.3211429
```
