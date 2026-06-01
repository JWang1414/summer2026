# Question 1
Two students from the six receive their own assignments:
$$
	\begin{pmatrix}
	6 \\
	2
	\end{pmatrix}
$$
The total number of permutations is $6!$. So the probability exactly two students receive their own assignment is:
$$
	\frac{1}{6!} \begin{pmatrix}
	6 \\
	2
	\end{pmatrix} = \frac{1}{48}
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
$$
	\frac{36}{12!}
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
