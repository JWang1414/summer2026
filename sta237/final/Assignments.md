# Assignment 2
![[Pasted image 20260623192229.png]]
Define $X_{i}$ as the number of requests received in one 10 minute period. Then, the number of requests in an hour is,
$$
	X = X_{1}+X_{2}+X_{3}+X_{4}+X_{5}+X_{6}
$$
Each $X_{i}$ is a Poisson distribution $X_{i}\sim\text{Pois}(2.5)$. By the properties of the Poisson distribution,
$$
	X\sim \text{Pois}(6 \times 2.5) = \text{Pois}(15)
$$
![[Pasted image 20260623193158.png]]
```r
qbeta(0.7, 3, 2)
```
$$
	P(X>0.6 | X\leq a) = \frac{P(X>0.6\cap X\leq a)}{P(X\leq a)} = \frac{P(X\leq a) - P(X<0.6)}{P(X\leq a)}
$$
![[Pasted image 20260623213914.png]]
Change of variables function:
$$
	f_{Y}(y) = f_{X}(h(y)) \lvert h'(y) \rvert
$$
Invert the change of variables function,
$$
	Y^{2}=X+1 \implies X=Y^{2}-1
$$
Therefore,
$$
	f_{Y}(y) = \frac{2}{9}(y^{2}-1) \left\lvert  \frac{d}{dy}y^{2}-1  \right\rvert = \frac{4}{9}y(y^{2}-1) \qquad 1<y< 2
$$
Compute,
$$
	P(1.5<Y<2) = \int_{1.5}^{2} \frac{4}{9}y(y^{2}-1) \, dy =\frac{119}{144}
$$
![[Pasted image 20260623215630.png]]
Use the law of total variance.
$$
	\text{Var}(Y) = \text{Var}(E(Y|X)) + E(\text{Var}(Y|X))
$$
The expectation and variance of the binomial distribution is:
$$
	E[X]=np \qquad \text{Var}(X) = np(1-p)
$$
In the form $\text{Binom}(n, p)$.

Therefore,
$$
	E(Y|X) = 0.4(x+2) \qquad \text{Var}(X) = 0.24(x+2)
$$
By linearity,
$$
	E(\text{Var}(Y|X)) = 0.24(E[X]+2)
$$
And,
$$
	\text{Var}(E(Y|X)) = (0.4)^{2}\text{Var(X)}
$$
Solve for $c$,
$$
	\sum_{x=0}^{4} c(x+1) = (1+2+3+4+5)c = 15c=1 \implies c=\frac{1}{15}
$$
Compute the expectation of $X$,
$$
	E[X] = \sum_{x=0}^{4} xc(x+1) = \frac{1}{15} \sum_{x=0}^{4} x(x+1) = \frac{1}{15}(0+2+6+12+20) = \frac{8}{3}
$$
Compute the variance of $X$
$$
	E[X^{2}] = \frac{1}{15} \sum_{x=0}^{4} x^{2}(x+1) = \frac{1}{15} (0+2+12+36+80) = \frac{26}{3}
$$
$$
	\text{Var}(X) = E[X^{2}] - E^{2}[X] = \frac{26}{3} - \left( \frac{8}{3} \right)^{2} = \frac{14}{9}
$$
Substituting back into the law of total variance,
$$
	\text{Var}(Y) = 0.4^{2}\left( \frac{14}{9} \right) + 0.24\left( \frac{8}{3}+2 \right) = \frac{308}{225} \approx 1.37
$$
