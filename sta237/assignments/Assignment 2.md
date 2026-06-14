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
# Question 4
Begin by inverting the provided transformation:
$$
	Y=\sqrt{ X+1 } \implies Y^{2}=X+1 \implies X = Y^{2}-1
$$
Since the transformation is a monotonically increasing function, I will use the transformation of variables function:
$$
	f_{Y}(y) = f_{X}(h(y)) \lvert h'(y) \rvert = \frac{2}{9}(y^{2}-1) \left| \frac{d}{dy}(y^{2}-1) \right|
$$
The PDF of $Y$ is:
$$
	f_{Y}(y) = \frac{4}{9}\lvert y \rvert (y^{2}-1)
$$
Compute the probability of interest:
$$
	P(1.5<Y<2) = \int_{1.5}^{2} f_{Y}(y) \, dy = \frac{4}{9} \int_{1.5}^{2} y^{3}-y \, dy
$$
Separated into two integrals:
$$
	\int_{1.5}^{2} y^{3} \, dy = \frac{y^{4}}{4} \bigg|^{2}_{y=1.5} = \frac{175}{64} \qquad
	\int_{1.5}^{2} y \, dy = \frac{y^{2}}{2} \bigg|^{2}_{y=1.5} = \frac{7}{8}
$$
Hence,
$$
	P(1.5<Y<2) = \frac{4}{9}\left( \frac{175}{64} - \frac{7}{8} \right) = \frac{119}{144} \approx 0.83
$$
# Question 3
Find $c$:
$$
	\begin{align}
	\sum_{x=0}^{4} c(x+1) & = c(0+1) + c(1+1) + c(2+1) + c(3+1) + c(4+1) \\
	 & = c+2c+3c+4c+5c \\
	 & = 15c
	\end{align}
$$
Therefore $c=1 /15$. To compute $\text{Var}(Y)$, use the law of total variance:
$$
	\text{Var}(E(Y|X)) + E(\text{Var}(Y|X)) = \text{Var}(Y)
$$
Since $Y|X=x\sim\text{Binomial}(x+2, 0.4)$,
$$
	E(Y|X) =np= 0.4(x+2)
$$
$$
	\text{Var}(Y|X) =np(1-p)= (x+2)(0.4)(1-0.4) = 0.24(x+2)
$$
Substituting into the law of total variance,
$$
	\text{Var}(0.4(X+2)) + E(0.24(X+2)) = 0.16 \text{Var}(X) + 0.24(E[X] + 2)
$$
Now, compute $\text{Var}(X)$ and $E[X]$.
$$
	E[X] = \sum_{x=0}^{4} xP(X=x) = \frac{1}{15} \sum_{x=0}^{4} x(x+1) = \frac{1}{15} (0+2+6+12+20) = \frac{8}{3}
$$
$$
	E[X^{2}] = \frac{1}{15} \sum_{x=0}^{4} x^{2}(x+1) = \frac{1}{15}(0+2+12+36+80) = \frac{26}{3}
$$
$$
	\text{Var}(X) = E[X^{2}] - E^{2}[X] = \frac{26}{3} - \left( \frac{8}{3} \right)^{2} = \frac{14}{9}
$$
Final answer:
$$
	\text{Var}(Y) = 0.16 \left( \frac{14}{9} \right) + 0.24\left( \frac{8}{3}+2 \right) = \frac{308}{225} \approx 1.37
$$
# Question 2
The numerical value of $a$ is:
```r
qbeta(0.7, 3, 2)
# Output: [1] 0.7276161
```

Written in terms of cumulative distribution functions:
$$
\begin{align}
	P(X>0.6 | X\leq a) & = \frac{P(X>0.6\cap X\leq a)}{P(X\leq a)}
	 = \frac{P(0.6<X\leq a)}{P(X\leq a)} \\
	 & = \frac{P(X\leq a) - P(X\leq 0.6)}{P(X\leq a)}
	 = \frac{F(a) - F(0.6)}{F(a)}
\end{align}
$$
Where $F(x)$ is the CDF of $\text{Beta}(3, 2)$. Solving for the CDF:
$$
	\int_{0}^{x} \text{Beta}(3, 2) \, dx = \frac{\Gamma(5)}{\Gamma(3)\Gamma(2)} \int_{0}^{x} x^{2}(1-x) \, dx = \frac{\Gamma(5)}{\Gamma(3)\Gamma(2)} \frac{x^{3}}{12} (4-3x)
$$
Therefore,
$$
	F(x) = x^{3}(4-3x)
$$
Substituting back, and approximating $a\approx 0.73$ yields:
$$
	P(X>0.6 | X\leq a) = \frac{a^{3}(4-3a) - (0.6)^{3}(4-3(0.6))}{a^{3}(4-3a)} \approx 0.33
$$



Numerical value of the conditional probability obtained using R:
```r
( pbeta(qbeta(0.7, 3, 2), 3, 2) - pbeta(0.6, 3, 2) ) / pbeta(qbeta(0.7, 3, 2), 3, 2)
# Output: [1] 0.3211429
```
