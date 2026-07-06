![[Pasted image 20260620164553.png]]
Recall the definition of the moment generating function:
$$
	M_{X}(t) = E[e^{ tX }]
$$
Since we also have,
$$
	E[g(X)] = \sum_{x \in S}g(x)P(X=x)
$$
Then,
$$
	M_{X}(t) = \sum_{x \in S}e^{ tx }P(X=x) \equiv  \int_{-\infty}^{\infty} e^{ tx }f(x) \, dx
$$
---
1.
Definition of the exponential distribution:
$$
	f(x) = \lambda e^{ -\lambda x }
$$
Compute the MGF
$$
	\int_{0}^{\infty} e^{ tx }(\lambda e^{ -\lambda x }) \, dx = \lambda \int_{0}^{\infty} e^{ (t-\lambda)x } \, dx
$$
$$
	\frac{\lambda}{t-\lambda} \left[ e^{ (t-\lambda) x } \right] ^{\infty}_{0} = \frac{\lambda}{t-\lambda} \left[ 0-e^{ 0 } \right] =-\frac{\lambda}{t-\lambda}
$$
Where I have assumed $t-\lambda<0$ or $t<\lambda$.

---
2.
Recall that the sum of exponential random variables is a gamma distributed random variable. Therefore,
$$
	S_{n} = \text{Gamma}(n, \lambda)
$$
The gamma distribution is:
$$
	\text{Gamma}(\alpha, \beta) = f(x) = \frac{\beta ^{\alpha}}{\Gamma(\alpha)}x^{\alpha-1} e^{ -\beta x }
$$
For $x>0$. In this case,
$$
	S_{n} = \frac{\lambda ^{n}}{\Gamma(n)} x^{n-1} e^{ -\lambda x }
$$
Compute the MGF
$$
	\int_{0}^{\infty} e^{ tx }\frac{\lambda ^{n}}{\Gamma(n)} x^{n-1}e^{ -\lambda x } \, dx = \frac{\lambda ^{n}}{\Gamma(n)} \int_{0}^{\infty} x^{n-1}e^{ (t-\lambda) x } \, dx
$$
Recall that Gamma distribution integral:
$$
	\int_{0}^{\infty} x^{a-1}e^{ -bx } \, dx = \frac{\Gamma(a)}{b^{a}}
$$
In this case, $a=n$ and $b=\lambda-t$.
$$
	M_{X}(t) = \frac{\lambda ^{n}}{\Gamma(n)} \frac{\Gamma(n)}{(\lambda-t)^{n}} = \frac{\lambda ^{n}}{(\lambda-t)^{n}}
$$
![[Pasted image 20260621183512.png]]
1.
Setup the integral:
$$
	\int_{0}^{\infty} \int_{0}^{x} cye^{ -2x } \, dy  \, dx = c \int_{0}^{\infty} e^{ -2x } \int_{0}^{x} y \, dy  \, dx =1
$$
Split up the integral:
$$
	\int_{0}^{x} y \, dy = \left[ \frac{y^{2}}{2} \right] ^{x}_{0} = \frac{x^{2}}{2} -0
$$
$$
	c \int_{0}^{\infty} e^{ -2x }\left( \frac{x^{2}}{2} \right) \, dx = \frac{c}{2} \int_{0}^{\infty} x^{2}e^{ -2x } \, dx
$$
Gamma integral:
$$
	\int_{0}^{\infty} x^{a-1}e^{ -bx } \, dx =\frac{\Gamma(a)}{b^{a}}
$$
In this case we have
$$
	a-1=2 \implies a=3 \qquad -bx=-2x \implies b=2
$$
Therefore,
$$
	\frac{c}{2} \frac{\Gamma(3)}{2^{3}} = c \times \frac{2!}{2(2^{3})}=1 \implies c = 8
$$
---
2.
Marginal density $f_{X}(x)$ is:
$$
	\int_{0}^{x} cye^{ -2x } \, dy = 8e^{ -2x } \int_{0}^{x} y \, dy =  8e^{ -2x } \left( \frac{x^{2}}{2} \right) = 4x^{2}e^{ -2x }
$$
Marginal density $f_{Y}(y)$ is:
$$
	\int_{y}^{\infty} cye^{ -2x } \, dx = 8y \int_{y}^{\infty} e^{ -2x } \, dx = 8y \left[ e^{ -2x } \frac{1}{-2} \right] ^{\infty}_{y}
$$
$$
	= -4y \left[ e^{ -2x } \right] ^{\infty}_{y} = -4y \left[ 0-e^{ -2y } \right]  = 4ye^{ -2y }
$$
---
3.
By definition:
$$
	p_{Y|X}(y|x) = \frac{p_{X, Y}(x, y)}{p_{X}(x)} = \frac{cye^{ -2x }}{4x^{2}e^{ -2x }} = \frac{2y}{x^{2}}
$$
- The answers claim that the conditional support here is $0<y<x$, however, I'm not sure where that comes from
---
4.
Conditional expectation:
$$
	\int_{0}^{x} y\left( \frac{2y}{x^{2}} \right) \, dy = \frac{2}{x^{2}} \int_{0}^{x} y^{2} \, dy = \frac{2}{x^{2}} \left[ \frac{x^{3}}{3} \right] = \frac{2}{3}x
$$
$$
	E(Y|X=x) = \frac{2x}{3}
$$
Conditional variance:
$$
	\int_{0}^{x} y^{2}\left( \frac{2y}{x^{2}} \right) \, dy = \frac{2}{x^{2}} \int_{0}^{x} y^{3} \, dy = \frac{2}{x^{2}} \left[ \frac{x^{4}}{4} \right] = \frac{1}{2}x^{2}
$$
$$
	\text{Var}(Y|X=x) = \frac{x^{2}}{2} - \left( \frac{2x}{3} \right)^{2} = \frac{x^{2}}{18}
$$
![[Pasted image 20260622162640.png]]
Define a new distribution,
$$
	Y_{i} = X^{2}_{i}
$$
Note that we have,
$$
	\frac{1}{100} \sum_{i=1}^{100} Y_{i} = \bar{Y}_{100}
$$
Where we are taking the sample mean of $Y_{i}$ over 100 samples. The CLT must be applied to $Y_{i}$ instead of $X_{i}$. Begin by solving for the expectation and variance.
$$
	E[Y_{i}] = E[X^{2}_{i}] = \int_{-\infty}^{\infty} x^{2} U(0, 1) \, dx = \int_{0}^{1} x^{2} \, dx = \left[ \frac{x^{3}}{3} \right] ^{1}_{0}
$$
$$
	E[Y_{i}] = \frac{1}{3}
$$
Variance:
$$
	E[Y^{2}_{i}] = E[X^{4}_{i}] = \int_{-\infty}^{\infty} x^{4}U(0, 1) \, dx = \int_{0}^{1} x^{4} \, dx = \left[ \frac{x^{5}}{5} \right] ^{1}_{0}
$$
$$
	E[Y^{2}_{i}] = \frac{1}{5}
$$
$$
	\text{Var}(Y_{i}) = E[Y^{2}_{i}] - E^{2}[Y_{i}] = \frac{1}{5} - \left( \frac{1}{3} \right)^{2} = \frac{4}{45}
$$
According to the CLT, the distribution of $\bar{Y}_{n}$ is approximately,
$$
	\bar{Y}_{n} \approx N\left( \frac{1}{3}, \frac{4}{45n} \right)
$$
Hence,
$$
	\frac{\bar{Y}_{100}-1 /3}{\sqrt{ (4 /45) /100 }} \approx N(0, 1)
$$
$$
	P\left( \bar{Y}_{100} > \frac{2}{5} \right) \approx P\left( Z > \frac{2 /5-1 /3}{\sqrt{ (4 /45) /100 }} \right)= P(Z>\sqrt{ 5 })
$$
