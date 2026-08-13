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
# Systems exchanging energy & particles
As of current, we have been limiting ourselves to a setup where the number of particles inside is fixed. However, there are more ways to expand a gas to push a piston. We may either heat it up, or add more particles inside our box. Thus, we are also interested in situations where particles can enter and leave.

In this new state, we expect that, at equilibrium, the internal energy $\left< E \right>$ for the untracked dof is a fixed quantity, and the average number of particles $\left< N \right>$ in the system is at a steady value.

Our task is now to determine the most unbiased probability function given these constraints.

In this new system, we must specify both the energy and the particle number. We will use the tuple $(i, j)$, where $i$ is the energy levels of the system, and $j$ is the number of particles found in an energy level.

$E(i, j)$ means there are $j$ particles in level $i$. If the particles are non-interacting, then $E(i, j)=jE(i)$. However in general the dependence is non-linear. As a note on notation, $N(i, j)$ is $j$, but we'll use this to be clear.

The conditions to maximise $s[p]$ are:
$$
	\begin{align}
	\sum_{(i, j)} p(i, j)-1 & =0 \\
	\sum_{(i, j)} E(i, j) p(i, j)-\epsilon & =0 \\
	\sum_{(i, j)}N(i, j)p(i, j)-\nu & =0
	\end{align}
$$
Where $\left< E \right> =\delta$ and $\left< N \right> =\nu$ are fixed constants.

Associating the Lagrange multipliers $\alpha$, $\beta$, and $\gamma$ with these constraints, we find that:
$$
	p^*_{m} = e^{ -[(1+\alpha)+\beta E_{m}+\gamma N_{m}] }
$$
From which we conclude that the most unbiased probability function for a system with fixed average energy and average particle number is:
$$
	p^*(i, j) = \frac{e^{ -\beta E(i, j)-\gamma N(i, j) }}{\mathcal{Z}_{en}}
$$
With the statsum:
$$
	\mathcal{Z}_{en}(\beta, \gamma) = \sum_{(i, j)} e^{ -\beta E(i, j)-\gamma N(i, j) }
$$
The equilibrium entropy works out to be:
$$
	\left< s \right> _\text{max} = \beta \left< E \right> +\gamma \left< N \right> +\log \mathcal{Z}_{en}(\beta, \gamma)
$$
In this new system, $\beta=1 /k_{B}T$ is unchanged. However, we not define the *chemical potential* $\mu$. Conventionally, $\gamma=-\beta \mu$, and $\lambda=e^{ \beta \mu }$ is called the *absolute activity*.

Rewriting the equilibrium statsum and probability function in terms of these new quantities.
$$
	\mathcal{Z}_{en} = \sum_{(i, j)} \lambda ^{j} e^{ -\beta E(i, j) } \qquad p^*(i, j) = \frac{\lambda ^{j}e^{ -\beta E(i, j) }}{\mathcal{Z}_{en}}
$$
And the equilibrium entropy is:
$$
	\left< s \right> _\text{max} = \beta \left< E \right> - \beta \mu \left< N \right> + \log \mathcal{Z}_{en}(\beta, \mu)
$$
The average energy $\left< E \right> =-\frac{ \partial  }{ \partial \beta }\log \mathcal{Z}_{en}$ is the same, and the average particle number is quite similar:
$$
	\left< N \right> = - \frac{ \partial  }{ \partial \gamma } \log \mathcal{Z}_{en} = \lambda \frac{ \partial  }{ \partial \lambda } \log \mathcal{Z}_{en}
$$
In just the same way as $\left< E \right>$, $\mathcal{Z}$ acts as a sort of moment generating function. For example:
$$
	\left< N^{2} \right> = \frac{1}{\mathcal{Z}_{en}} \lambda^{2} \frac{ \partial^{2} }{ \partial \lambda^{2} } \mathcal{Z}_{en}
$$
Finally, note that:
$$
	d\left< s \right> = \beta d\left< E \right> - \beta \mu d\left< N \right> \implies dS = \frac{1}{T} \, d\left< E \right> - \frac{\mu}{T} \, d\left< N \right>
$$
Telling us a little bit about how the entropy in a system changed according to the changes in the energy and particles inside the system.

For a mixture of particles with numbers $N^{a}$ and $N^b$, each particle system has a corresponding chemical potential $\mu^a$ and $\mu^b$. For such a system, the equilibrium probability of an outcome with $N^a_{i}$ particles of type $a$ and $N^b_{i}$ particles of type $b$ is:
$$
	p^*_{i} = \frac{e^{ -\beta(E_{i}-\mu ^{a}N^a_{i}-\mu^b N^b_{i}) }}{\mathcal{Z}_{en}}
$$
With the equilibrium entropy:
$$
	\left< s \right> _\text{max} = \beta \left< E \right> -\beta \mu^a \left< N^a \right>  - \beta \mu^b \left< N^b \right> +\log \mathcal{Z}_{en}(\beta, \mu^a, \mu^b)
$$
# Flows of energy & particles
