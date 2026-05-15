# Question 1
![[Pasted image 20260513173359.png]]

Number of ways to open at least 1 lock:
$$
	\begin{pmatrix}
	5 \\
	1
	\end{pmatrix} 4!
$$
Number of ways to open at least 2 locks:
$$
	\begin{pmatrix}
	5 \\
	2
	\end{pmatrix} 3!
$$
Total number of key-lock arrangements:
$$
	5!
$$
Therefore the chance to open exactly 1 lock is:
$$
	\frac{1}{5!} \left[ 5(4!) - \begin{pmatrix}
	5 \\
	2
	\end{pmatrix} 3! \right] = \frac{1}{120} \left[ 120 - 60 \right] = \frac{1}{2}
$$
# Question 2
![[Pasted image 20260513174946.png]]

Call the number of $(1, 2)$ steps $a$, and the number of $(2, 1)$ steps $b$. We are interested in the total possible combinations,
$$
	a\begin{bmatrix}
	1 \\
	2
	\end{bmatrix} + b \begin{bmatrix}
	2 \\
	1
	\end{bmatrix} = \begin{bmatrix}
	15 \\
	12
	\end{bmatrix}
$$
This is equivalent to the system of equations:
$$
	\begin{cases}
	a+2b=15 \\
	2a+b=12
	\end{cases}
$$
Using the notation $(a, b)$ the possible values that satisfy the first equation are:
$$
	\{ (15, 0), (13, 1), (11, 2), (9, 3), (7, 4), (5, 5), (3, 6), (1, 7) \}
$$
The possible values that satisfy the second equation are:
$$
	\{ (0, 12), (1, 10), (2, 8), (3, 6), (4, 4), (5, 2), (6, 0) \}
$$
The total number of ways to reach $(15, 12)$ will be the intersection between these two sets.
$$
	\{ (3, 6) \}
$$
So there is just one way to reach $(15, 12)$
- I'm not super confident in this answer. Try checking it later.
# Question 3
![[Pasted image 20260513180514.png]]
Let $D$ represent a person with the disease, and $T$ represent a positive test result.

From the question we have,
$$
	P(T|D) = 0.95 \qquad P(T|D^{c}) = 0.05 \qquad P(D) = 0.01
$$
We are interested in $P(D|T)$. Using Bayes' rule,
$$
	\begin{align}
	P(D|T) & = \frac{P(T|D)P(D)}{P(T|D)P(D) + P(T|D^{c})P(D^{c})} \\
	 & = \frac{0.95(0.01)}{0.95(0.01) + 0.05(0.99)} \\
	 & = \frac{19}{118}
	\end{align}
$$
# Question 4
![[Pasted image 20260515154409.png]]

Calculate the probability person A wins.

Define $p$ as the probability of winning. The chance to win on the first round is 1/6. Furthermore, the chance that both players lose is (5/6)(5/6). The full range of possibilities is therefore,
$$
	p = \frac{1}{6} + \frac{5}{6} \frac{5}{6}p = \frac{1}{6} + \frac{25p}{36} \implies p=\frac{6}{11}
$$
So person A has a 6/11 chance of winning, the higher probability.