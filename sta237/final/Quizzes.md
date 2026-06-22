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
