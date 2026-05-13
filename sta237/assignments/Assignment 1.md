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
