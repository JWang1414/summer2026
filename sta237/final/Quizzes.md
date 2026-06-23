# Quiz 1
![[Pasted image 20260621205621.png]]
Note that:
$$
	P(\text{3 different and increasing rolls}) \equiv P(\text{3 different rolls})P(\text{3 increasing rolls} | \text{3 different rolls})
$$
According to the multiplication rule.

The probability is therefore,
$$
	\frac{6\times 5\times 4}{6^{3}} \frac{1}{3!} = \frac{5}{54}
$$
![[Pasted image 20260621210533.png]]
The probability that the smallest roll is at least 3 is $(4 /6)^{3}$. The probability that the smallest roll is at least 4 is $(3 /6)^{3}$.

Therefore, the probability that the smallest roll is exactly 3 is,
$$
	\left( \frac{4}{6} \right)^{3} - \left( \frac{3}{6} \right)^{3} = \frac{37}{216}
$$
# Quiz 2
![[Pasted image 20260621213806.png]]
There are four possible colour combinations.
$$
	\text{Blue, blue} \qquad \frac{2}{5} \frac{1}{4} = \frac{1}{10}
$$
$$
	\text{Blue, red} \qquad \frac{2}{5} \frac{3}{4} = \frac{3}{10}
$$
$$
	\text{Red, blue} \qquad \frac{3}{5} \frac{2}{4} = \frac{3}{10}
$$
$$
	\text{Red, red} \qquad \frac{3}{5} \frac{2}{4} = \frac{3}{10}
$$
Therefore,
$$
	P(X=0) = \frac{1}{10} \qquad P(X=1) = \frac{6}{10} \qquad P(X=2) = \frac{3}{10}
$$
PMF is zero otherwise.
![[Pasted image 20260621215102.png]]
Solve for $c$,
$$
	\int_{-1}^{1} c(1-x^{2}) \, dx = c \int_{-1}^{1} 1-x^{2} \, dx = c \left( \int_{-1}^{1}  \, dx - \int_{-1}^{1} x^{2} \, dx  \right) = 1
$$
$$
	\int_{-1}^{1} dx = 1-(-1) = 2
$$
$$
	\int_{-1}^{1} x^{2} \, dx = \left[ \frac{x^{3}}{3} \right] ^{1}_{-1} = \frac{1}{3} - \frac{(-1)^{3}}{3} = \frac{2}{3}
$$
$$
	c \left( 2-\frac{2}{3} \right) = \frac{4}{3}c =1 \implies c = \frac{3}{4}
$$
Compute $P(\lvert X \rvert<1 /2)$.
$$
	\int_{-1/2}^{1 /2} c(1-x^{2}) \, dx = c \left( \int_{-1/2}^{1/2}  \, dx - \int_{-1/2}^{1/2} x^{2} \, dx  \right)
$$
$$
	\int_{-1/2}^{1/2} dx = \frac{1}{2} - \left( -\frac{1}{2} \right) = 1
$$
$$
	\int_{-1/2}^{1/2} x^{2} \, dx = \left[ \frac{x^{3}}{3} \right] ^{1/2}_{-1/2} = \frac{(1 /2)^{3}}{3} - \frac{(-1 /2)^{3}}{3} = \frac{1}{12}
$$
$$
	P\left( \lvert X \rvert  < \frac{1}{2} \right) = \frac{3}{4}\left( 1-\frac{1}{12} \right) = \frac{11}{16}
$$
# Quiz 3
![[Pasted image 20260622204406.png]]
Define $A$ as the probability the part fails between year 3 and year 5, and $B$ as the probability the part as lasted more than 2 years. Then,
$$
	P(A|B) = \frac{P(A\cap B)}{P(B)}
$$
However, notice that $A\subseteq B$, therefore, $P(A\cap B)=P(A)$. Simplifying the above into:
$$
	P(A|B) = \frac{P(A)}{P(B)}
$$
Solve for $P(A)$:
$$
	\int_{3}^{5} \lambda e^{ -\lambda t } \, dt = \lambda \int_{3}^{5} e^{ -\lambda t } \, dt = \lambda \left[ \frac{1}{-\lambda} e^{ -\lambda t } \right] ^{5}_{3}
$$
$$
	-e^{ -5\lambda } + e^{ -3\lambda } = \frac{3}{32}
$$
Solve for $P(B)$:
$$
	\int_{2}^{\infty} \lambda e^{ -\lambda t } \, dt = -\left[ e^{ -\lambda t } \right] ^{\infty}_{2} = -0+e^{ -2\lambda } = \frac{1}{4}
$$
Therefore,
$$
	P(A|B) = \frac{3 /32}{1 /4} = \frac{3}{8}
$$
![[Pasted image 20260622205629.png]]
$$
	E[X(X-1)] = \sum_{k=1}^{n} k(k-1) \begin{pmatrix}
	n \\
	k
	\end{pmatrix} p^{k} (1-p)^{n-k}
$$
Using the hint:
$$
	E[X(X-1)] = \sum_{k=2}^{n} n(n-1)\begin{pmatrix}
	n-2 \\
	k-2
	\end{pmatrix} p^{k}(1-p)^{n-k} = n(n-1) \sum_{k=2}^{n} \begin{pmatrix}
	n-2 \\
	k-2
	\end{pmatrix} p^{k}(1-p)^{n-k}
$$
Substitute, $a=k-2$
$$
	= n(n-1) \sum_{a=0}^{n} \begin{pmatrix}
	n-2 \\
	a
	\end{pmatrix} p^{a+2} (1-p)^{n-(a+2)} = n(n-1)p^{2} \sum_{a=0}^{n} \begin{pmatrix}
	n-2 \\
	a
	\end{pmatrix} p^{a}(1-p)^{(n-2)-a}
$$
Notice that this is equivalent to the binomial variable with $n-2$ as opposed to $n$. The total probability mass of a $\text{Binom}(n-2, p)$ random variable is 1. Therefore,
$$
	E[X(X-1)] = n(n-1)p^{2}
$$
# Quiz 4
![[Pasted image 20260622211422.png]]
Change of variables formula:
$$
	f_{Y}(y) = f_{X}(h(y)) \lvert h'(y) \rvert
$$
Where $Y=g(X)$ and $h(Y)=g^{-1}(Y)$.

Begin by inverting the change of variables function:
$$
	Y=-2\log X \implies -\frac{Y}{2} = \log X \implies e^{ -Y/2 }=X
$$
The derivative of this function is:
$$
	\frac{d}{dy} e^{ -y/2 } = -\frac{1}{2} e^{ -y/2 }
$$
Substitute into change of variables formula:
$$
	f_{Y}(y) = 2e^{ -y/2 } \left\lvert  -\frac{1}{2}e^{ -y/2 }  \right\rvert = e^{ -y/2 }e^{ -y/2 } = e^{ -y } \qquad 0<y<\infty
$$
Compute,
$$
	P(Y<\log 4) = \int_{0}^{\log 4} e^{ -y } \, dy = -\left[ e^{ -y } \right] ^{\log 4}_{0}
$$
$$
	-e^{ -\log 4 } + e^{ -0 } = \frac{3}{4}
$$
![[Pasted image 20260622215018.png]]
Marginal density of $X$ is:
$$
	\int_{-\infty}^{\infty} f_{X, Y}(x, y) \, dy = \int_{0}^{1} \frac{3}{5}x^{2}e^{ -x }y(1+y) \, dy = \frac{3}{5} x^{2}e^{ -x } \int_{0}^{1} y(1+y) \, dy
$$
$$
	\int_{0}^{1} y+y^{2} \, dy = \int_{0}^{1} y \, dy + \int_{0}^{1} y^{2} \, dy
$$
$$
	\left[ \frac{y^{2}}{2} \right] ^{1}_{0} = \frac{1}{2}-0
$$
$$
	\left[ \frac{y^{3}}{3} \right] ^{1}_{0} = \frac{1}{3}-0
$$
$$
	f_{X}(x) = \frac{3}{5} x^{2}e^{ -x }\left( \frac{1}{2}+\frac{1}{3} \right) = \frac{1}{2} x^{2}e^{ -x }
$$
Marginal density of $Y$ is:
$$
	\int_{0}^{\infty} \frac{3}{5}x^{2}e^{ -x }y(1+y) \, dx = \frac{3}{5}y(1+y) \int_{0}^{\infty} x^{2}e^{ -x } \, dx
$$
According to the gamma function:
$$
	\int_{0}^{\infty} x^{2}e^{ -x } \, dx = \Gamma(3)
$$
$$
	f_{Y}(y) = \frac{3}{5}y(1+y) (2!) = \frac{6}{5} y(1+y)
$$
If $X$ and $Y$ are independent, then $f_{X, Y}(x, y)=f_{X}(x)f_{Y}(y)$.
$$
	f_{X}(x)f_{Y}(y) = \frac{1}{2} x^{2}e^{ -x } \times \frac{6}{5} y(1+y) = \frac{3}{5}x^{2}e^{ -x }y(1+y) = f_{X, Y}(x, y)
$$
I conclude $X$ and $Y$ are independent.