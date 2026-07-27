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
$$
	\left< X \right> = \int_{0}^{\infty } \frac{x}{\lambda}e^{ -x/\lambda } \, dx = \lambda
$$
$$
	\left< X^{2} \right> = \int_{0}^{\infty} \frac{x^{2}}{\lambda}e^{ -x/\lambda } \, dx = 2\lambda^{2}
$$
$$
	\text{var}(X) = \left< X^{2} \right>  - \left< X \right> ^{2} = 2\lambda^{2} - \lambda^{2} = \lambda^{2}
$$
So the average is $\lambda$ and the variance is $\lambda^{2}$.
# Question 2
The heat power generated for a single wire is $I^{2}R$. By law of superposition, the total heat power generated from the two wires is:
$$
	\dot{Q} = I_{1}^{2}R_{1} + I_{2}^{2}R_{2}
$$
From Kirchoff's current law, this becomes:
$$
	= I_{1}^{2}R_{1} + (I-I_{1})^{2}R_{2}
$$
Note that $R_{1}$ and $R_{2}$ are both constant, positive numbers.

Solve for the minimum point:
$$
	\frac{d}{dI_{1}}\left[ I_{1}^{2}R_{1} + (I-I_{1})^{2}R_{2} \right] = 2I_{1}R_{1} - 2(I-I_{1})R_{2} = 2I_{1}R_{1} - 2I_{2}R_{2} =0
$$
Therefore we have:
$$
	I_{1}R_{1} = I_{2}R_{2}
$$
As needed.
