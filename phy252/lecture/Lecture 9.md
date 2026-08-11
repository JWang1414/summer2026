While we use a thermal reservoir to depict our systems, "boxes" of energies in our system can be represented by a number of things. The spin-1/2 particles derive energy from a magnetic field, a particle in a box has energies according to its momentum.

Lets begin by discussing four systems. The spin-1/2 particle, the harmonic oscillator, a rotor, and a 1D particle in a box. These have the Hamiltonians:
$$
	H = -\vec{\mu}\cdot \vec{B} \qquad H = \frac{1}{2}kx^{2} + \frac{p^{2}_{x}}{2m}
$$
$$
	I = mR^{2} \qquad \text{where } H=\frac{J^{2}_{z}}{2I}
$$
$$
	H = \frac{p^{2}_{x}}{2m} \qquad \text{were } -\frac{L}{2} \leq x \leq \frac{L}{2}
$$
The corresponding energy states in these systems are:
$$
	E_{n} = \pm \frac{1}{2} \mu B
$$
$$
	E_{n} = n\hbar \omega
$$
$$
	E_{n} = \frac{n^{2}\hbar^{2}}{2I}
$$
$$
	E_{n} = \frac{n^{2}\hbar^{2}\pi^{2}}{2mL^{2}}
$$
If you notice, the second and fourth are just the energies for the harmonic oscillator and the infinite square well in quantum physics.
- In this sense, quantum mechanics is doing the "heavy lifting" for us

Recall that $\mathcal{Z}$ is some sum dependent on $\beta E_{i}$. Generally speaking, you can often glean information just by considering the weights on $\mathcal{Z}$. If $\beta\epsilon$ is very small, in the harmonic oscillator system, you might suppose that numerous values are significant. It takes a while to reach small numbers like $e^{ -1 }$ after all. However, if $\beta\epsilon$ is large, then in the spin-1/2 particle case, the positive particle will dominate the negative one. That is, $e^{ e^{ \beta\epsilon/2 } }$ will be substantially larger than $e^{ -\beta\epsilon/2 }$ for $\beta\epsilon\to \infty$.

With our new picture of energies and probabilities, we can restate the first law of thermodynamics in the following manner:
$$
	\left< E \right> = \sum p_{i} E_{i} \implies d\left< E \right> = \sum E_{i} \, dp_{i} + \sum p_{i} \, dE_{i}
$$
This first term, where the probabilities are changing, is heat, and the second term, where the energy levels in the system are changing, is work.
$$
	dQ = \sum E_{i} \, dp_{i} \qquad dW = \sum p_{i} \, dE_{i}
$$

Homework:
- Think about ways to change the energies inside the 4 basic systems described here
