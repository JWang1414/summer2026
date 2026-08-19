# Question 1
Maximize $xy$ under the constraint $2x+2y=L$.

$$
	\begin{bmatrix}
	y \\
	x
	\end{bmatrix} = \lambda\begin{bmatrix}
	2 \\
	2
	\end{bmatrix}
$$
$$
	\begin{align}
	x & = 2\lambda \\
	y & = 2\lambda
	\end{align}
$$
This tells us that $x=y$ and therefore:
$$
	2x+2x=L \implies 4x=L \implies x=\frac{L}{4}
$$
The largest possible area of a rectangle with perimeter $L$ is a square with area $L /8$
# Question 3
---
a.
If $\left< E \right> =0$ then the probability of both must be the same. Probability function is 1/2 for both.

---
b.
Probably function must be 1 for $-\mu B /2$ and 0 for the other possibility.

This has 0 surprise, but it is the only possible function.
# Question 4
---
a.
$$
	A \int_{-\infty}^{\infty} e^{ -x/\lambda } \, dx = A \int_{0}^{\infty} e^{ -x/\lambda } \, dx =1
$$
$$
	A(\lambda)=1 \implies A=\frac{1}{\lambda}
$$
---
b.
$$
	\left< x \right> = \frac{1}{\lambda} \int_{0}^{\infty} x e^{ -x/\lambda } \, dx = \frac{1}{\lambda}(\lambda^{2}) = \lambda
$$
$$
	\left< x^{2} \right> = \frac{1}{\lambda} \int_{0}^{\infty} x^{2} e^{ -x/\lambda } \, dx = \frac{1}{\lambda}(2\lambda^{3}) = 2\lambda^{2}
$$
$$
	\text{var}(x) = 2\lambda^{2} - \lambda^{2} = \lambda^{2}
$$
# Question 5
---
a.
$$
	p_{-1 /2} = \frac{e^{ \beta \mu B/2 }}{\mathcal{Z}} \qquad p_{1 /2} = \frac{e^{ -\beta \mu B /2 }}{\mathcal{Z}}
$$
Where:
$$
	\mathcal{Z} = \sum_{i} e^{ -\beta E_{i} } = e^{ \beta \mu B/2 } + e^{ -\beta \mu B/2 } = 2 \cosh\left( \frac{\beta \mu B}{2} \right)
$$
---
b.
$$
	\left< E \right> =- \frac{ \partial \log \mathcal{Z} }{ \partial \beta } = \frac{\mu B}{2} \tanh\left( \frac{\beta \mu B}{2} \right)
$$
---
c.
$$
	\text{var}(E) = \frac{ \partial^2 \log \mathcal{Z} }{ \partial \beta ^2 } = \left( \frac{\mu B}{2} \right)^{2} \left( 1-\tanh ^{2}\left( \frac{\beta \mu B}{2} \right) \right)
$$
---
d.
$$
	e^{ -(\mu B/2 +\mu B/2)/k_{B}T } = e^{ -\mu B/k_{B}T }
$$
---
e.
- Don't know what the magnetic dipole moment is
$$
	\frac{\mu B}{k_{B}T} = \frac{\mu}{k_{B}} \frac{0.5}{1} = \frac{\mu}{2k_{B}}
$$
$$
	e^{ -\mu/2k_{B} }
$$
# Question 6
---
a.
$$
	\mathcal{Z}= \sum_{i}e^{ -\beta(n\hbar \omega) } = \frac{1}{1-e^{ -\beta \hbar \omega }}
$$
- Geometrical series
---
b.
$$
	\left< E \right> =- \frac{ \partial \log \mathcal{Z} }{ \partial \beta } = \frac{ \partial  }{ \partial \beta } \log(1-e^{ -\beta \hbar \omega })
$$
$$
	\left< E \right> = \frac{\hbar \omega}{e^{ \beta \hbar \omega } -1}
$$
$$
	\beta \hbar \omega = \frac{\hbar \omega}{k_{B}T} = \frac{\hbar \omega}{k_{B}(2\hbar \omega /k_{B})} = \frac{1}{2}
$$
$$
	\left< E \right> = \frac{\hbar \omega}{e^{ 1/2 }-1}
$$
---
c.
$$
	(m+1)\hbar \omega - m\hbar \omega = \hbar \omega
$$
Probability should be $e^{ -\hbar \omega/k_{B}T }$

---
d.
$$
	1-e^{ -\hbar \omega/k_{B}T }
$$
$$
	\frac{\hbar \omega}{k_{B}T} = \frac{\hbar \omega}{k_{B}(0.1\hbar \omega /k_{B})} = 10
$$
$$
	1-e^{ -10 } \approx 1
$$

---
e.
$$
	\left< E \right> (T) = \frac{\hbar \omega}{e^{ \hbar \omega/k_{B}T } -1}
$$
