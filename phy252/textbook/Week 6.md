# Work and free energy
In the basic systems we have established, we may only transfer heat to and from these systems. However, we would also like to do work with these systems.

The average energy of a system is:
$$
	\left< E \right> =\sum_{n} p_{n}E_{n} \implies d\left< E \right> = \underbrace{\sum_{n} dp_{n} E_{n}}_{dQ} + \underbrace{\sum_{n}p_{n} \, dE_{n}}_{d\left< W \right> }
$$
Which is the simple microscopic picture underlying TD1. When only the probabilities associated with the energy levels changes, this is heat. However, when the energy levels themselves change, this is work.

So, to make a system do work, we need to vary the energies of the levels of a system.

For the magnetic spin-1/2 particle, this may be accomplished by changing the magnetic field. The energy levels in the 1D box change when we vary the length of the box $L$. Changing the spring constant varies the energy levels in the harmonic oscillator. Any parameter in the Hamiltonian of a system provides a way to to work, so long as it can be reliably changed.

Consider a system whose energy levels $E_{n}$ depend on some parameter $b$. The statsum $\mathcal{Z}(\beta, b)$ is in general a function of $\beta$ and $b$. Define the work done on the $n$th energy level by changing $b$ as:
$$
	dW_{n} = \frac{ \partial E_{n} }{ \partial b } \, db
$$
The average work for a system in equilibrium at $T=1 /k_{B}\beta$ is then:
$$
	d\left< W \right> = \sum_{n} p_{n} W_{n} = \sum_{n} \frac{e^{ -\beta E_{n} }}{\mathcal{Z}(\beta, b)} \frac{ \partial E_{n} }{ \partial b } \, db = db \frac{ \partial  }{ \partial b } \left( -\frac{1}{\beta}\log \mathcal{Z} \right)
$$
This final quantity in the brackets is called the *free energy*.
$$
	F \equiv  -\frac{1}{\beta}\log \mathcal{Z}
$$
In terms of this new quantity, the average work done on a system by changing one of its parameters is:
$$
	d\left< W \right> = \left( \frac{ \partial F }{ \partial b }  \right)_{T} \, db
$$
That is, the change in free energy at fixed temperature.