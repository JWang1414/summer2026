# Simple model systems
We would like to understand the thermal physics of objects from an understanding of quantum mechanics. For this reason we will begin with models that are simple to describe within quantum mechanics.

Notably, beginning from a quantum mechanical understanding, we already have the possible energies the system can take. They are describe by the energy eigenstates.

The first, and simplest system we will consider is the spin-1/2 particle. If the particle has a magnetic moment $\vec{\mu}$, then the interaction of the magnetic moment with a magnetic field $\vec{B}$ is described by the Hamiltonian $H=-\vec{\mu}\cdot \vec{B}$. From quantum mechanics, the expression for the energy is:
$$
	E(n)=-n\mu B
$$
Where $n$ may only be $\pm 1 /2$.

The next system is the harmonic oscillator. It has resonance frequency $\omega=\sqrt{ k /m }$, with spring constant $k$ and mass $m$. The Hamiltonian for this system is $H=\frac{1}{2} \frac{p^{2}_{x}}{m} + \frac{1}{2}kx^{2}$. The energy in each of the levels is:
$$
	E(n)=n\hbar \omega
$$
Where $n$ is an integer from 0 to $\infty$.

The following system is a rotor. A particle with mass $m$ confined to move along a ring with radius $R$. It has Hamiltonian $H=J^{2}_{z} /2I$ where $J_{z}$ is the particle's angular momentum along the axis of the ring, and $I=mR^{2}$ is the moment of inertia. Its energy levels are:
$$
	E(n)=n^{2} \frac{\hbar^{2}}{2I}
$$
Where $n$ is an integer from $-\infty$ to $\infty$.

Finally, we have the particle in a box. This describes a particle of mass $m$ in a 1-D box of length $L$. It has the same Hamiltonian as the free particle $H=\frac{1}{2} \frac{p^{2}_{x}}{m}$. However $x$ is restricted to $[-L /2, L /2]$, to prevent it from leaving the box. The energy levels are:
$$
	E(n) = n^{2} \frac{\hbar^{2}\pi^{2}}{2mL^{2}}
$$
Where $n$ is an integer from 1 to $\infty$.

These equations can be simplified by identifying the characteristic energy $\epsilon$ for each system. In every case, the statsum and average energy are functions of $\epsilon$ and the dimensionless quantity $\beta\epsilon$.
![[Pasted image 20260807220431.png]]

Furthermore, the high and low temperature limits for $\mathcal{Z}$ and $\left< E \right>$ for these models can be seen below.
![[Pasted image 20260807221838.png]]
