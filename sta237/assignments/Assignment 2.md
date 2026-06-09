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

- Fill in the CDF in part 2 of this question
# Question 3
Find $c$.
$$
	\begin{align}
	\sum_{x=0}^{4} c(x+1) & = c(0+1) + c(1+1) + c(2+1) + c(3+1) + c(4+1) \\
	 & = c+2c+3c+4c+5c \\
	 & = 15c
	\end{align}
$$
$$
	15c=1 \implies c=\frac{1}{15}
$$

$$
	\text{Var}(Y) = E[Y^{2}] - E^{2}[Y]
$$
Begin by computing the conditional expectation value.
$$
	E[Y|X] = \sum_{y} yP(Y|X=x) = \sum_{y}y\text{Binomial}(x+2, 0.4)
$$
This is equivalent to the expectation of the binomial function, therefore,
$$
	E[Y|X] = (x+2)(0.4) = 0.4(x+2)
$$
Furthermore,
$$
	E[Y^{2}|X] = \sum_{y}y^{2}P(Y|X=x) = \sum_{y}y^{2} \text{Binomial}(x+2, 0.4)
$$
- Complete this question, it's the hardest one
# Question 4
Given:
$$
	Y = g(X) = \sqrt{ X+1 }
$$
Invert,
$$
	Y=\sqrt{ X+1 } \implies Y^{2}=X+1 \implies X = Y^{2}-1
$$
$$
	X=g^{-1}(Y) = h(Y) = Y^{2}-1
$$
Transformed version:
$$
	f_{Y}(y) = f_{X}(h(y)) \lvert h'(y) \rvert = \frac{2}{9}(y^{2}-1) \left| \frac{d}{dy}(y^{2}-1) \right|
$$
$$
	\frac{d}{dy}(y^{2}-1) = 2y
$$
$$
	f_{Y}(y) = \frac{2}{9}(y^{2}-1)(2y) = \frac{4}{9}y(y^{2}-1)
$$
Compute,
$$
	P(1.5<Y<2) = \int_{1.5}^{2} \frac{4}{9}y(y^{2}-1) \, dy = \frac{4}{9} \int_{1.5}^{2} y^{3}-y \, dy
$$
$$
	\int_{1.5}^{2} y^{3} \, dy = \frac{y^{4}}{4} \bigg|^{2}_{y=1.5} = \frac{175}{64}
$$
$$
	\int_{1.5}^{2} y \, dy = \frac{y^{2}}{2} \bigg|^{2}_{y=1.5} = \frac{7}{8}
$$
$$
	P(1.5<Y<2) = \frac{4}{9}\left( \frac{175}{64} - \frac{7}{8} \right) = \frac{119}{144} \approx 0.83
$$
