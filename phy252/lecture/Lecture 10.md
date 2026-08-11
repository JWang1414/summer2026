So how do we change the energies in the states of each of the systems from last time? (To potentially accomplish work?)

Well, for the particle in the box, the method is to change the length of the box. This will change the energy levels, as they are proportional to $1 /L$.

If you go through the math, you will find that the work from some small change in the length of the box is:
$$
	dW = \frac{ \partial  }{ \partial L } \left( -\frac{1}{\beta}\log \mathcal{Z} \right) \, dL = \left( \frac{ \partial F }{ \partial L }  \right)_{T} \, dL
$$
Where we have defined the free energy $F$.
$$
	F = -\frac{1}{\beta}\log \mathcal{Z} = -k_{B}T \log \mathcal{Z}
$$
So far, while considering our problems, we have implicitly been assuming they are isolated from the rest of the world. Now, we will open up the door for our system to exchange particles with an external reservoir. Because we are at equilibrium with this reservoir, we will say that $\left< N  \right>$ is now a fixed quantity, much like we asserted $\left< E \right>$ was.
$$
	\sum p_{i}N_{i} = \left< N \right>
$$
Though, in reality, because we now need to keep track of both the energy levels and the particle levels, this summation is actually:
$$
	\sum p_{i, j} N_{i, j} = \left< N \right>
$$
The same is extended to the summation over the probabilities and the energies.

In the simplest case we have the outcomes $(i, j)$ which correspond to:
$$
	E(i, j) = jE(i) \qquad N(i, j) =j
$$
Recall that at equilibrium, the surprise of the system is at max. In contact with an energy reservoir, this means:
$$
	\left< \mathcal{S} \right> = \beta \left< E \right> + \log \mathcal{Z}_{e}
$$
Where $\mathcal{Z}_{e}$ is simply the statsum for a system in contact with an energy reservoir. This should be a familiar quantity. Now that we have added on the particle number, this becomes:
$$
	\left< \mathcal{S} \right> = \beta \left< E \right> + \beta \mu \left< N \right> +\log \mathcal{Z}_{en}
$$
Where we have this new quantity $\mu$ to help us quantify the effect of the particles. Unlike $\beta$, this number can be positive or negative.
- $\mu$ is called the chemical potential
