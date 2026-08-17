# Question 1
---
a.
$$
	\mathcal{Z}_\text{3D} = \frac{V}{h^{3}} \left( \frac{2\pi m}{\beta} \right)^{3/2}
$$
$$
	\frac{ \partial  }{ \partial \beta } \log \left[ \frac{V}{h^{3}}\left( \frac{2\pi m}{\beta} \right)^{3/2} \right] = -\frac{3}{2} \frac{ \partial  }{ \partial \beta } \log \beta = -\frac{3}{2} \frac{1}{\beta}
$$
For a single particle:
$$
	\left< E \right> = - \frac{ \partial  }{ \partial \beta } \log \mathcal{Z} = \frac{3}{2} \frac{1}{\beta} = \frac{3}{2} k_{B}T
$$
For $N$ particles:
$$
	\left< E \right> = \frac{3}{2} Nk_{B}T
$$
As needed.

---
b.
From the previous tutorial I have:
$$
	\sigma(E) = \frac{\hbar \omega e^{ \beta \hbar \omega/2 }}{e^{ \beta \hbar \omega }-1}
$$
And from the notes:
$$
	\left< E \right> = \frac{\hbar \omega}{e^{ \beta \hbar \omega }-1}
$$
Therefore we are interested in:
$$
	\frac{\sqrt{ N }}{N} \frac{\sigma(E)}{\left< E \right> }
$$
When $N=3$ and $\sigma(E)$ and $\left< E \right>$ are defined for a single particle. This is:
$$
	\frac{1}{\sqrt{ 3 }} e^{ \beta \hbar \omega/2 }
$$
Where $\beta=1 /k_{B}T$
# Question 2
$$
	\mathcal{Z}_{en}(\beta, \lambda) = \sum_{(i, j)} \lambda ^{j} e^{ -\beta E(i, j) } \qquad \text{where } \lambda=e^{ \beta \mu }
$$
Calculations:
$$
	\lambda = e^{ \beta \mu } = e^{ \mu/k_{B}T } = e^{ \epsilon^{2} }
$$
$$
	\beta E(a, j) = \frac{1}{k_{B}(10 /k_{B}\epsilon)} \times 0 = \frac{\epsilon}{10} \times 0 =0
$$
$$
	\beta E(b, j) = \frac{\epsilon}{10} \times \epsilon = \frac{\epsilon^{2}}{10}
$$
$$
	\beta E(c, j) = \frac{\epsilon}{10} \times 5\epsilon = \frac{\epsilon^{2}}{2}
$$
Assuming the particles are non-interacting then the summation becomes:
$$
	\mathcal{Z}_{en} = \sum_{j} e^{ \epsilon^{2}j }(1 + e^{ -\epsilon^{2}j/10 } + e^{ -e^{2}j/2 })
$$
# Question 3
---
a.
Energy flows from high to low temperature. Therefore energy should flow from B to A.

---
b.
Particles flow from high to low chemical potential. Therefore the particles should flow from B to A.
# Question 5
---
a.
$$
	F-C+P=2
$$
In this case $C=2$. So:
$$
	F-2+P=2 \implies F+P=4
$$
$$
	P=4-F
$$
For the maximum number of phases $F=0$ and therefore the max number of phases that can co-exist at equilibrium is 4.

---
b.
The temperature is roughly 77-78 K

---
c.
$$
	\frac{\left< S_{2} \right> -\left< S_{1} \right> }{M} = \frac{L}{T_{pt}}
$$
We have $M=1$, $L=200$ and $T_{pt}=77.5$.

The change in entropy is therefore:
$$
	\Delta \left< S \right> = \left< S_{2} \right> -\left< S_{1} \right> = \frac{ML}{T_{pt}} \approx 2.58 \text{ kJ/K}
$$
# Question 4
$$
	\Delta S = Nk_{B} \log\left( \frac{V_{f}}{V_{i}} \right)
$$
From the change in volume between the neon and argon:
$$
	\Delta S= Nk_{B} \left[ \log\left( \frac{60}{20} \right) + \log\left( \frac{60}{40} \right) \right]
$$
Using the idea gas law:
$$
	\frac{PV}{T} = Nk_{B}
$$
Therefore:
$$
	\Delta S = \frac{P}{T} \left[ V_\text{neon} \log(3) + V_\text{argon} \log\left( \frac{3}{2} \right) \right] \approx 12.7
$$
So the change in entropy is 12.7 J/K