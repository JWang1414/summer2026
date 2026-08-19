# Question 1
---
a.
For a single particle we have:
$$
	\mathcal{Z} = \frac{1}{2} \sqrt{ \frac{\pi}{\beta\epsilon} } \implies \left< E \right> = \frac{1}{2\beta}
$$
For $N$ particles this becomes:
$$
	\frac{N}{2\beta} = \frac{1}{2}Nk_{B}T
$$
And in 3 dimensions this is
$$
	\left< E \right> = \frac{3}{2}Nk_{B}T
$$
Compute the variance in the energy:
$$
	\text{var}(E) = \frac{ \partial^2 \log \mathcal{Z} }{ \partial^2 \beta } = \frac{ \partial^2  }{ \partial^2 \beta } \log \left[ \frac{1}{2}\sqrt{ \frac{\pi}{\beta\epsilon} } \right] = \frac{1}{2\beta^{2}}
$$
The standard deviation is therefore:
$$
	\sigma(E) = \frac{1}{\sqrt{ 2 }\beta} \to \frac{3}{\beta}\sqrt{ \frac{N}{2} }
$$
Since $\sigma(E)\propto \sqrt{ N }$ and $\left< E \right>\propto N$, $\sigma(E)\ll \left< E \right>$ as $N$ becomes large. As needed.

---
b.
For a classical oscillator we instead have:
$$
	\mathcal{Z} = \frac{1}{\beta\epsilon} \qquad \left< E \right> = \frac{1}{\beta}
$$
Compute the variance:
$$
	\frac{ \partial^2 \log \mathcal{Z} }{ \partial^2 \beta } = \frac{ \partial^2  }{ \partial^2 \beta } \log\left( \frac{1}{\beta\epsilon} \right) =- \frac{ \partial^2  }{ \partial^2 \beta } \log(\beta\epsilon) = \frac{1}{\beta^{2}}
$$
The standard deviation is therefore:
$$
	\sigma(E) = \frac{1}{\beta} \to \frac{3\sqrt{ N }}{\beta}
$$
The average energy is:
$$
	\left< E \right> =\frac{1}{\beta} \to \frac{3N}{\beta}
$$
The ratio between the two is:
$$
	\frac{\sigma(E)}{\left< E \right> }= \frac{1}{\sqrt{ N }}
$$
# Question 2
$$
	\mathcal{Z}(\beta, \lambda) = \sum_{(i, j)} \lambda ^{j} e^{ -\beta E(i, j) } \qquad p^*(i, j) = \frac{\lambda ^{j}e^{ -\beta E(i, j) }}{\mathcal{Z}}
$$
$$
	\beta \mu = \frac{\mu}{k_{B}T} = \frac{10\epsilon}{k_{B}(10 /k_{B}\epsilon)} = \epsilon^{2} \implies \lambda = e^{ \epsilon^{2} }
$$
$$
	\beta E(a) = \frac{1}{k_{B}(10 /k_{B}\epsilon)} \times 0 = \frac{\epsilon}{10} \times 0 =0
$$
$$
	\beta E(b) = \frac{\epsilon}{10} (\epsilon) = \frac{\epsilon^{2}}{10}
$$
$$
	\beta E(c) = \frac{\epsilon}{10} (5\epsilon) = \frac{\epsilon^{2}}{2}
$$
Therefore:
$$
	\mathcal{Z} = \sum_{j} e^{ \epsilon^{2}j } \left( 1 + e^{ -\epsilon^{2}j/10 } + e^{ -\epsilon^{2}j/2 } \right)
$$
- And then you can approximate this with a calculator of sorts. Which I do not have time to do
# Question 3
---
a.
Energy flows from high to lower temperature. So $B\to A$

---
b.
Particles flow from higher to lower chemical potential. Compute this in combination with the energy.
$$
	\frac{\mu_{A}}{T_{A}} = \frac{0.5}{300} = \frac{1}{600}
$$
$$
	\frac{\mu_{B}}{T_{B}} = \frac{2}{500} = \frac{1}{250}
$$
Therefore $B\to A$
