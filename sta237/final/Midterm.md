![[Pasted image 20260623161953.png]]
Poisson distribution is:
$$
	p_{X}(x) = e^{ -\lambda } \frac{\lambda ^{x}}{x!}
$$
First, consider the probability that $x$ is even:
$$
	\sum_{k=1}^{\infty} p_{X}(2k) = e^{ -\lambda } \sum_{k=1}^{\infty} \frac{\lambda ^{2k}}{(2k)!}
$$
Where the even numbers are modelled by $2k$. Furthermore, this series is the Taylor series representation of $\cosh(\lambda)$.
$$
	= e^{ -\lambda }\cosh(\lambda)
$$
The probability that $X$ is odd is therefore,
$$
	P(X\text{ is odd}) = 1 - e^{ -\lambda }\cosh(\lambda) = e^{ -\lambda }\sinh(\lambda) = \frac{1-e^{ -2\lambda }}{2}
$$
![[Pasted image 20260623163536.png]]
Solve for $c$,
$$
	\int_{-\infty}^{\infty} f_{X}(x) \, dx = \int_{0}^{1} cx \, dx + \int_{1}^{2} c(2-x) \, dx
$$
$$
	c \int_{0}^{1} x \, dx = c \left[ \frac{x^{2}}{2} \right] ^{1}_{0} = \frac{c}{2}
$$
$$
	c\int_{1}^{2} 2-x \, dx = c\left[ \int_{1}^{2} 2 \, dx - \int_{1}^{2} x \, dx  \right] = c\left[ 2(2-1) - \left( \frac{x^{2}}{2} \right)^{2}_{1} \right]
$$
$$
	c \left[ 2 - \left( \frac{4}{2} - \frac{1}{2} \right) \right] = \frac{c}{2}
$$
$$
	\frac{c}{2} + \frac{c}{2} = 1 \implies c=1
$$
Cumulative distribution from $0<x<1$
$$
	\int_{0}^{x'} x \, dx = \left[ \frac{x^{2}}{2} \right] ^{x'}_{0} = \frac{x^{2}}{2}
$$
Cumulative distribution from $1\leq x<2$,
$$
	\int_{0}^{1} x \, dx + \int_{1}^{x'} 2-x \, dx = \frac{1}{2} + \left( 2\int_{1}^{x'}  \, dx - \int_{1}^{x'} x \, dx  \right)
$$
$$
	= \frac{1}{2} + \left[ 2(x'-1) - \left( \frac{x^{2}}{2} \right)^{x'}_{1} \right] = \frac{1}{2} + \left[ 2(x'-1) - \left( \frac{x'^{2}}{2}-\frac{1}{2} \right) \right]
$$
$$
	= 2x-\frac{x^{2}}{2} -1
$$
Naturally, it is 0 when $x\leq0$, and 1 when $x\geq 2$.
$$
	F_{X}(x) = \begin{cases}
	x^{2} /2 & 0<x<1 \\
	2x-x^{2} /2 -1 & 1<x<2
	\end{cases}
$$
![[Pasted image 20260623165910.png]]
$$
	P\left( X< \frac{3}{2} \right) = 2\left( \frac{3}{2} \right) - \frac{(3 /2)^{2}}{2} -1 = \frac{7}{8}
$$
$$
	P\left( X< \frac{1}{2} \right) = \frac{(1 /2)^{2}}{2} = \frac{1}{8}
$$
Therefore,
$$
	P\left( X > \frac{3}{2} \right) = 1- \frac{7}{8} = \frac{1}{8}
$$
$$
	P\left( X> \frac{1}{2} \right) = 1-\frac{1}{8} = \frac{7}{8}
$$
Hence,
$$
	P\left( X > \frac{3}{2} | X > \frac{1}{2} \right) = \frac{P(X > 3 /2)}{P(X>1 /2)} = \frac{1 /8}{7 /8} = \frac{1}{7}
$$
Compute expectation value,
$$
	E[X] = \int_{-\infty}^{\infty} xf_{X}(x) \, dx = \int_{0}^{1} x^{2} \, dx + \int_{1}^{2} x(2-x) \, dx = \int_{0}^{1} x^{2} \, dx + 2 \int_{1}^{2} x \, dx  - \int_{1}^{2} x^{2} \, dx
$$
$$
	\left[ \frac{x^{3}}{3} \right] ^{1}_{0} = \frac{1}{3}
$$
$$
	2 \left[ \frac{x^{2}}{2} \right] ^{2}_{1} = 2 \left( \frac{4}{2} - \frac{1}{2} \right) = 3
$$
$$
	\left[ \frac{x^{3}}{3} \right] ^{2}_{1} = \frac{2^{3}}{3} - \frac{1}{3} = \frac{7}{3}
$$
$$
	E[X] = \frac{1}{3} + 3 - \frac{7}{3} = 1
$$
![[Pasted image 20260623170908.png]]
Using a diagramc
$$
	P(X=0) = \frac{6}{6^{2}} = \frac{1}{6}
$$
$$
	P(X=1) = \frac{10}{36} = \frac{5}{18}
$$
$$
	P(X=2) = \frac{8}{36} = \frac{2}{9}
$$
$$
	P(X=3) = \frac{6}{36} = \frac{1}{6}
$$
$$
	P(X=4) = \frac{4}{36} = \frac{1}{9}
$$
$$
	P(X=5) = \frac{2}{36} = \frac{1}{18}
$$
Compute the expectation value,
$$
	E[X] = \sum_{x=0}^{5} xP(X=x) = \frac{0}{6} + \frac{5}{18} + 2\left( \frac{2}{9} \right) + \frac{3}{6} + \frac{4}{9} + \frac{5}{18}
$$
$$
	E[X] = \frac{35}{18} \approx 1.94
$$
![[Pasted image 20260623175138.png]]
The beta distribution is:
$$
	f(x) = \frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)} x^{a-1} (1-x)^{b-1}
$$
In this case we have,
$$
	f(x) = \frac{\Gamma(\alpha^{2}+\beta^{2})}{\Gamma(\alpha^{2})\Gamma(\beta^{2})} x^{\alpha^{2}-1} (1-x)^{\beta^{2}-1}
$$
The expectation is,
$$
	E[X] = \frac{\Gamma(\alpha^{2}+\beta^{2})}{\Gamma(\alpha^{2})\Gamma(\beta^{2})} \int_{0}^{1} x(x^{\alpha^{2}-1} (1-x)^{\beta^{2}-1}) \, dx
$$
$$
	= \int_{0}^{1} x^{\alpha^{2}}(1-x)^{\beta^{2}-1} \, dx
$$
Beta distribution integral:
$$
	\int_{0}^{1} x^{a-1}(1-x)^{b-1} \, dx = \frac{\Gamma(a)\Gamma(b)}{\Gamma(a+b)}
$$
Define $\alpha^{2}=a-1$ and $\beta^{2}-1=b-1$, so $a=\alpha^{2}+1$ and $b=\beta^{2}$.
$$
	= \int_{0}^{1} x^{\alpha^{2}}(1-x)^{\beta^{2}-1} \, dx = \frac{\Gamma(\alpha^{2}+1)\Gamma(\beta^{2})}{\Gamma(\alpha^{2}+1+\beta^{2})}
$$
According to the hint,
$$
	= \frac{\Gamma(\alpha^{2}+1)\Gamma(\beta^{2})}{\Gamma(\alpha^{2}+1+\beta^{2})} = \frac{\alpha^{2}\Gamma(\alpha^{2})\Gamma(\beta^{2})}{(\alpha^{2}+\beta^{2})(\Gamma(\alpha^{2}+\beta^{2}))}
$$
Combining everything together, the expectation value is,
$$
	E[X] = \frac{\Gamma(\alpha^{2}+\beta^{2})}{\Gamma(\alpha^{2})\Gamma(\beta^{2})} \frac{\alpha^{2}\Gamma(\alpha^{2})\Gamma(\beta^{2})}{(\alpha^{2}+\beta^{2})(\Gamma(\alpha^{2}+\beta^{2}))}= \frac{\alpha^{2}}{\alpha^{2}+\beta^{2}}
$$
![[Pasted image 20260623180421.png]]
Using the R output,
$$
	P(60<X< 78) \approx 0.7475-0.0912 \approx 0.66
$$
The value of 83.54 in the provided R output is the 90th quantile. That is, the score a student would have to get to perform better than 90% of other students.
![[Pasted image 20260623180730.png]]
The distribution of $Y$ is a binomial with 6 samples and probability 0.66.
$$
	Y\sim  \text{Binom}(6, 0.66)
$$
Using the R output,
$$
	P(Y\geq  5) = 0.33
$$
![[Pasted image 20260623180359.png]]
