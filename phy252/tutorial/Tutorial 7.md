# Question 1
Define the side lengths of the rectangle as $x$ and $y$. Area of the rectangle is $xy$ and the perimeter is $2x+2y$.

We would like to maximize the equation $xy$ under the condition $2x+2y=L$.
$$
	\nabla(xy) = \begin{bmatrix}
	y \\
	x
	\end{bmatrix}
$$
$$
	\nabla(2x+2y) = \begin{bmatrix}
	2 \\
	2
	\end{bmatrix}
$$
Our equations are:
$$
	\begin{bmatrix}
	y \\
	x
	\end{bmatrix} = 2\lambda \begin{bmatrix}
	1 \\
	1
	\end{bmatrix}
$$
$$
	2x+2y=L
$$
$$
	y=2\lambda \qquad x=2\lambda
$$
$$
	2(2\lambda) + 2(2\lambda) = 8\lambda = L \implies \lambda=\frac{L}{8}
$$
Therefore,
$$
	y=2\left( \frac{L}{8} \right) = \frac{L}{4}
$$
$x$ is the same. So the largest possible area is:
$$
	\left( \frac{L}{4} \right)^{2} = \frac{L^{2}}{16}
$$
# Question 3
---
a.
Uniform distribution

---
b.
The energy for $m=-1 /2$ is $\mu B /2$ and the energy for $m=1 /2$ is $-\mu B /2$.

If $\left< E \right>$ then the probability of $m=1 /2$ is 1 and 0 otherwise.
# Question 4
---
a.
$$
	\int_{0}^{\infty} Ae^{ -x /\lambda } \, dx = A(-\lambda) \left[ e^{ -x/\lambda } \right] ^{\infty}_{x=0}
$$
$$
	-\lambda A \left[ 0-1 \right]  = A\lambda=1 \implies A=\frac{1}{\lambda}
$$
---
b.
