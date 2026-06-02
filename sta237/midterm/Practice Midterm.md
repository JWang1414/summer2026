# Question 1
The total probability is:
$$
	\begin{pmatrix}
	6 \\
	2
	\end{pmatrix} P(\text{Only the first two get their assignment})
$$
Define $A_{n}$ as the $n$th student receiving their assignment. Then, this is equivalent to,
$$
	\begin{pmatrix}
	6 \\
	2
	\end{pmatrix} P(A_{1} \cap A_{2} \cap A_{3}^{c} \cap A_{4}^{c} \cap A_{5}^{c} \cap A_{6}^{c})
$$
This probability can be split into,
$$
	P(A_{3}^{c} \cap A_{4}^{c} \cap A_{5}^{c} \cap A_{6}^{c} | A_{1}\cap A_{2}) P(A_{1}\cap A_{2})
$$
De Morgan's law tells us,
$$
	P((A_{3}\cup A_{4}\cup A_{5}\cup A_{6})^{c} | A_{1}\cap A_{2}) = 1 - \frac{1}{4!}\left[ 2 \begin{pmatrix}
	4 \\
	1
	\end{pmatrix} + \begin{pmatrix}
	4 \\
	2
	\end{pmatrix} \right] = \frac{5}{12}
$$
Combining everything together,
$$
	\begin{pmatrix}
	6 \\
	2
	\end{pmatrix} \left( \frac{5}{12} \right) \left( \frac{1}{6^{2}} \right) = \frac{25}{144}
$$
# Question 2
---
a.
Contains no green balls:
$$
	\left( \frac{1}{2} \right)^{4} \begin{pmatrix}
	4 \\
	0
	\end{pmatrix}
$$
Contains one green ball:
$$
	\left( \frac{1}{2} \right)^{4} \begin{pmatrix}
	4 \\
	1
	\end{pmatrix}
$$
Contains at least two green balls:
$$
	1 - \frac{1}{2^{4}} - \frac{1}{2^{4}} \begin{pmatrix}
	4 \\
	1
	\end{pmatrix} = \frac{11}{16}
$$
---
b.
The probability of picking 4 balls of different colours is,
$$
	\frac{1}{12} \frac{2}{12} \frac{6}{12} \frac{3}{12}
$$
Multiply by the number of possible permutations:
$$
	\frac{4!(1 \times 2 \times 6 \times 3)}{12^{4}} = \frac{1}{24}
$$
---
c.
Contains no green balls:
$$
	\begin{pmatrix}
	6 \\
	0
	\end{pmatrix} \begin{pmatrix}
	12-6 \\
	4
	\end{pmatrix} = \begin{pmatrix}
	6 \\
	4
	\end{pmatrix}
$$
Contains one green ball:
$$
	\begin{pmatrix}
	6 \\
	1
	\end{pmatrix} \begin{pmatrix}
	12-6 \\
	3
	\end{pmatrix} = 6\begin{pmatrix}
	6 \\
	3
	\end{pmatrix}
$$
Probability of picking at least two green balls:
$$
	1 - \frac{\begin{pmatrix}
	6 \\
	4
	\end{pmatrix}}{\begin{pmatrix}
	12 \\
	4
	\end{pmatrix}} - \frac{6\begin{pmatrix}
	6 \\
	3
	\end{pmatrix}}{\begin{pmatrix}
	12 \\
	4
	\end{pmatrix}} = \frac{8}{11}
$$
The number of ways to pick out a sample such that the balls are all different colours is:
$$
	\begin{pmatrix}
	1 \\
	1
	\end{pmatrix} \begin{pmatrix}
	2 \\
	1
	\end{pmatrix} \begin{pmatrix}
	6 \\
	1
	\end{pmatrix} \begin{pmatrix}
	3 \\
	1
	\end{pmatrix} = 2(6)(3) = 36
$$
So the probability each of the balls is a different colour is:
$$
	\frac{36}{\begin{pmatrix}
	12 \\
	4
	\end{pmatrix}} = \frac{4}{55}
$$
# Question 4
Poisson distribution:
$$
	p_{X}(x) = e^{ -\lambda } \frac{\lambda ^{x}}{x!}
$$
Probability $x$ is an odd number:
$$
	1 - \sum_{k=0}^{\infty} e^{ -\lambda } \frac{\lambda ^{2k}}{(2k)!} = 1-e^{ -\lambda } \sum_{k=0}^{\infty} \frac{\lambda ^{2k}}{(2k)!}
$$
This summation is equal to $\cosh(\lambda)$.
$$
	1 - e^{ -\lambda } \frac{e^{ -\lambda }+e^{ \lambda }}{2} = 1-\frac{e^{ -2\lambda }+1}{2} = \frac{1}{2} - \frac{e^{ -2\lambda }}{2}
$$
Final answer:
$$
	\frac{1}{2} (1-e^{ -2\lambda }) = e^{ -\lambda } \sinh(\lambda)
$$
# Question 5
Gamma distribution:
$$
	f(x) = \frac{\beta ^{\alpha}}{\Gamma(\alpha)} x^{\alpha-1} e^{ -\beta x }
$$
The MGF is given by:
$$
	M_{X}(t) = E[e^{ tX }] = \sum_{k=0}^{\infty} e^{ tk } \frac{\beta ^{\alpha}}{\Gamma(\alpha)} x^{\alpha-1} e^{ -\beta k }
$$
$$
	\frac{\beta ^{\alpha}}{\Gamma(\alpha)} x^{\alpha-1} \sum_{k=0}^{\infty} e^{ tk }e^{ -\beta k } = \frac{\beta ^{\alpha}}{\Gamma(\alpha)} x^{\alpha-1} \sum_{k=0}^{\infty} e^{ (t-\beta)k }
$$
Assume $e^{ t-\beta }$ is small. Apply the geometric sum:
$$
	\sum_{k=0}^{\infty} e^{ (t-\beta)k } = \frac{1}{1-e^{ t-\beta }} = \frac{e^{ \beta }}{e^{ \beta }-e^{ t }}
$$
Therefore,
$$
	M_{X}(t) = \frac{\beta ^{\alpha}}{\Gamma(\alpha)} \frac{e^{ \beta }x^{\alpha-1}}{e^{ \beta }-e^{ t }}
$$
# Question 3
Define $F_{1}$ as the number of coin flips for the first head, and $F_{2}$ as the number of coin flips after getting a head.

In the first case, if you get a tails, the same state resets back to the beginning. If you get a heads, you progress to the game state $F_{2}$. Both of which have a 1/2 chance of happening
$$
	F_{1} = \frac{1}{2}(1+F_{1}) + \frac{1}{2}(1+F_{2})
$$
In the $F_{2}$ state, if you flip heads, you win, and if you flip tails, it resets again.
$$
	F_{2} = \frac{1}{2} + \frac{1}{2}(1+F_{1})
$$
Now solve for $F_{1}$.
# Question 6
$$
	\frac{1-0.84}{1-0.16} = \frac{4}{21}
$$
- This is the first (probably naive) idea I have to approaching this problem
- The >80 percentile is 0.84 and the >64 percentile is 0.16. Then I do a simple division to find $P(>80|>64)$
- Considering this is worth 10 points I'm quite confident this is wrong