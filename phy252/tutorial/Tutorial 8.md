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
