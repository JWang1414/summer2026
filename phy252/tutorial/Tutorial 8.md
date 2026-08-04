# Question 5
---
a.
Generically, the most unbiased probability distribution for a system with fixed energy is:
$$
	p_{i} = \frac{e^{ -\beta E_{i} }}{\mathcal{Z}} \qquad \mathcal{Z}(\beta) = \sum_{i} e^{ -\beta E_{i} }
$$
Where the energies for this system are:
$$
	E(m) = -m\mu B
$$
This results in the total probability function:
$$
	p_{i} = \frac{e^{ -\beta E_{i} }}{e^{ \beta \mu B/2 } + e^{ -\beta \mu B/2 }}
$$
---
b.
$$
	\left< E \right> = -\frac{1}{\mathcal{Z}} \frac{ \partial \mathcal{Z} }{ \partial \beta } = \frac{\mu B}{2} \frac{e^{ \beta \mu B/2 }-e^{ -\beta \mu B/2 }}{e^{ \beta \mu B/2 }+e^{ -\beta \mu B/2 }} = \frac{\mu B}{2} \tanh\left( \frac{\beta \mu B}{2} \right)
$$
Notice that, by the definition of $\beta$ we have:
$$
	\frac{\mu B}{2}\tanh\left( \frac{\mu B}{2k_{B}T} \right)
$$
Below is a graph of $\tanh(1 /x)$
![[Pasted image 20260803163844.png]]
And this is a graph of its derivative
![[Pasted image 20260803163914.png]]

---
c.
$$
	\left< E^{2} \right> = \frac{1}{\mathcal{Z}} \frac{ \partial^{2}\mathcal{Z} }{ \partial \beta^{2} } = \left( \frac{\mu B}{2} \right)^{2} \frac{\mathcal{Z}}{\mathcal{Z}} = \left( \frac{\mu B}{2} \right)^{2}
$$
$$
	\text{var}(E) = \left< E^{2} \right> -\left< E \right> ^{2} = \left( \frac{\mu B}{2} \right)^{2} - \left[ \frac{\mu B}{2} \tanh\left( \frac{\beta \mu B}{2} \right) \right] ^{2} = \left( \frac{\mu B}{2} \right)^{2} \left[ 1- \tanh ^{2}\left( \frac{\mu B}{2k_{B}T} \right) \right]
$$
$$
	\text{var}(E) = \left( \frac{\mu B}{2} \right)^{2} \text{sech}^{2}\left( \frac{\mu B}{2k_{B}T} \right)
$$
---
d.
$$
	\frac{e^{ \beta \mu B/2 }}{e^{ -\beta \mu B/2 }} = e^{ \beta \mu B } = e^{ \mu B/k_{B}T }
$$
---
e.
$$
	e^{ \mu/2k_{B} }
$$
- I have no idea how to determine the magnetic dipole moment $\mu$
# Question 6
---
a.
$$
	\mathcal{Z} = \sum_{n=0}^{\infty} e^{ -n\beta \hbar \omega } = \frac{1}{1-e^{ -\beta \hbar \omega }}
$$
---
b.
$$
	\left< E \right> = \frac{ \partial  }{ \partial \beta } \log \mathcal{Z} = \frac{\hbar \omega}{e^{ \hbar \omega/k_{B}T } -1}
$$
$$
	T = \frac{2\hbar \omega}{k_{B}} \implies \frac{\hbar \omega}{k_{B}T} = \frac{\hbar \omega}{k_{B}} \frac{k_{B}}{2\hbar \omega} = \frac{1}{2}
$$
The average energy is therefore:
$$
	\left< E \right> = \frac{\hbar \omega}{e^{ 1/2 }-1}
$$
---
c.
Recall that the probability for each $n$ is:
$$
	p_{n} = \frac{e^{ -n\beta \hbar \omega }}{\mathcal{Z}}
$$
The ratio between two states is:
$$
	\frac{e^{ -(m+1)\beta \hbar \omega }}{e^{ -m\beta \hbar \omega }} = e^{ -\beta \hbar \omega }
$$
---
d.
$$
	p_{0} = \frac{e^{ 0 }}{\mathcal{Z}} = \mathcal{Z}^{-1} = 1-e^{ -\beta \hbar \omega }
$$
$$
	T = \frac{0.1\hbar \omega}{k_{B}} \implies \frac{\hbar \omega}{k_{B}T} = \frac{\hbar \omega}{k_{B}} \frac{k_{B}}{0.1\hbar \omega} = \frac{1}{0.1} = 10
$$
The probability is therefore,
$$
	p_{0} = 1-e^{ -10 } \approx 0.9999546
$$
---
e.
$$
	\left< E \right>  = \frac{\hbar \omega}{e^{ \hbar \omega/k_{B}T } -1}
$$
As a function of $T$ this could be plotted like:
$$
	\left< E \right> = \frac{1}{e^{ 1/T }-1}
$$
---
f.
Definition of the heat capacity is:
$$
	C = \frac{ \partial \left< E \right>  }{ \partial T } = \frac{\hbar^{2}\omega^{2}}{k_{B}T^{2}} e^{ \hbar \omega/k_{B}T } (e^{ \hbar \omega/k_{B}T }-1)^{-2}
$$
Plotted it looks like:
![[image.png]]
Where the derivative is indicated in red, and the original function in blue.
