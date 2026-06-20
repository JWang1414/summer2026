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
