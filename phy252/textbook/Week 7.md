# Quantum Particles
For this segment, we will consider a system with a single level whose energy is $\epsilon$. We will further suppose that the particles occupying a level are *indistinguishable*.

For *fermions*, the only allowed occupation numbers for a single level are $j=0,1$. Thus the only energy levels are 0 and $\epsilon$.

The statsum $\mathcal{Z}_{f}$ and probability of finding $j$ fermions in the energy level are therefore:
$$
	\mathcal{Z}_{f} = 1+\lambda e^{ -\beta\epsilon } = 1+e^{ \beta(\mu-\epsilon) } \qquad p(j) = \frac{e^{ -\beta(\epsilon-\mu)j }}{\mathcal{Z}_{f}}
$$
Now, for fermions, when $\epsilon<\mu$, there is a high probability the energy level is filled as opposed to empty, and vice versa. In particular, when $\beta(\epsilon-\mu)\gg 1$, energy levels with $\epsilon<\mu$ are almost certain to be occupied, and when $\epsilon>\mu$, they will likely be empty.

The average number of fermionic particles in a level with energy $\epsilon$ is:
$$
	\left< N(\epsilon) \right> = \lambda \frac{ \partial  }{ \partial \lambda } \log \mathcal{Z} = \frac{1}{e^{ \beta(\epsilon-\mu) }+1}
$$

For *bosons*, multiple particles may occupy the same level. For a single level of energy $\epsilon$ the possible outcomes are 0, $\epsilon$, $2\epsilon$, ...

Owing to this, the statsum is a geometric series, and the probabilities of finding $j$ bosons in the energy level is:
$$
	\mathcal{Z}_{b} = \sum_{j=0}^{\infty} \lambda ^{j}e^{ -j\beta\epsilon } = \frac{1}{1-\lambda e^{ -\beta\epsilon }} \qquad p(j) = \frac{e^{ -\beta(\epsilon-\mu)j }}{\mathcal{Z}_{b}}
$$
The average number of bosonic particles in a level with energy $\epsilon$ is:
$$
	\left< N \right> (\epsilon) = \lambda \frac{ \partial  }{ \partial \lambda } \log \mathcal{Z}_{b} = \frac{1}{e^{ \beta(\epsilon-\mu) }-1}
$$
Now, if you sketch these probabilities, you'll find that it resembles an exponentially decreasing curve when $\epsilon>\mu$. However, when $\mu>\epsilon$, it blows up and goes to infinity.
## Small occupation number limit
In general, for fermions and bosons, the average number of particles over all the energy levels is:
$$
	\left< N \right> = \sum_{i} \left< N(i) \right> = \frac{\lambda e^{ -\beta E(i) }}{1\pm \lambda e^{ -\beta E(i) }}
$$
And the internal energy is:
$$
	\left< E \right> = \sum_{i} \left< N(i) \right> E(i) = \sum_{i} \frac{E(i)}{e^{ \beta[E(i)-\mu] }\pm 1}
$$
The $+$ is for fermions, and $-$ for bosons.

Notice how, for fermions and bosons, when $e^{ \beta(\epsilon-\mu) }\gg 1$, the denominator grows large, and the number of particles in a level becomes $\ll 1$. This condition is equivalent to claiming $\lambda\ll e^{ \beta\epsilon }$ or $\epsilon \gtrsim \mu$.

We call this the small occupation limit, where the average number of particles in a level with energy $\epsilon$ is:
$$
	\left< N(\epsilon) \right> \approx \lambda e^{ -\beta\epsilon }
$$
And, in this limit, $\left< E \right>$ in terms of $\left< N \right>$ conveniently simplifies into:
$$
	\left< E \right> = -\lambda \frac{ \partial  }{ \partial \beta } \frac{\left< N \right> }{\lambda}
$$
## Ideal gas, without the iid assumption
The particles in a box are not iid because they are actually indistinguishable. That is to say, if you swapped the quantum states of any two random particles in the box, there is no physical effect on the system. So, we need to be a little more careful while enumerating through the possible outcomes for the particles in the box.

Consider a 1D box in equilibrium with a particle reservoir with $\mu<0$. Every energy level in the box has energy $E(n)=n^{2} \frac{\hbar^{2}\pi^{2}}{2mL^{2}}>\mu$. According to the small occupation number expression:
$$
	\left< N \right> (n) \approx \lambda e^{ -\beta E(n) }
$$
Sum over all $n$ to find that, in the high temperature limit $k_{B}T\gg \hbar^{2}\pi^{2} /(2mL^{2})$:
$$
	\left< N \right> _\text{1D} \approx \lambda \frac{L\sqrt{ 2\pi mk_{B}T }}{h} \implies \left< N \right> _\text{3D} \approx \lambda \frac{V(2\pi mk_{B}T)^{3/2}}{h^{3}}
$$
Now, the internal energy for particles in a 3D box is:
$$
	\left< E \right> \approx -\lambda \frac{ \partial  }{ \partial \beta } \frac{\left< N \right> }{\lambda} \approx \frac{3}{2} \lambda \frac{V(2\pi mk_{B})^{3/2}}{h^{3}}T^{5/2}
$$
- Notice that this is identical to $\left< E \right> = \frac{3}{2}\left< N \right>k_{B}T$

Now, in terms of the average number density $\left< N \right> /V$ and the temperature of an ideal gas, the absolute activity can now be expressed as:
$$
	\lambda = e^{ \beta \mu } = \frac{\left< N \right> }{V} \left( \frac{h^{2}}{2\pi mk_{B}T} \right)^{3/2}
$$
If you calculate the entropy of a gas of indistinguishable particles, you will discover what is called the *Sackur-Tetrode formula*
$$
	\frac{S}{k_{B}} = \left< N \right> \left[ \log\left( \frac{V\left< E \right> ^{3/2}}{\left< N \right> ^{5/2}} \right) + \frac{3}{2}\log\left( \frac{4\pi m}{3h^{2}} \right) + \frac{5}{2} \right]
$$
# Phases of matter
The simplest definition of a *phase* is a collection of matter with homogeneous macro properties. So the $\left< E \right>$, $S$, and $F$ are spatially uniform everywhere within the phase.

Consider two phases in equilibrium and share a *phase boundary*. So they may exchange energy, volume, and particles. Since they are at equilibrium, they must have the same temperature, pressure, and chemical potential. So, under what conditions is this possible?

Well, the number of unconstrained free parameters is the total free parameters, subtract the number of constraints. It turns out there are $P(C-1)$ free parameters, and $C(P-1)$ constraints. Where $P$ is the number of phases, and $C$ is the number of constituents.

The number of unconstrained free parameters is therefore determined by the *Gibbs phase rule*:
$$
	F-C+P=2
$$
Where $F$ is the number of unconstrained free parameters.

One interesting point is when $F=0$. For example the equilibrium between the three phases of water ($C=1, P=3$). There is no freedom left, and so there is just one choice of pressure and temperature. Notably, this special point where all three phases may co-exist is called the *triple point*.
- For water, this turns out to be 611.66 Pa and 273.16 K.
## Phase transitions
Consider a block of ice at some temperature $T<T_{pt}$, where $T_{pt}$ is the temperature where the solid and liquid phases are in equilibrium.

Ice has a well-defined heat capacity, so, as we transfer heat to it, its internal energy and temperature will increase. However, notice that ice cannot exist above $T_{pt}$, and water cannot exist below $T_{pt}$. At these points there may only be ice, or only water.

So what happens as we increase the temperature of ice to approach $T_{pt}$? Well, at exactly $T=T_{pt}$, heat no longer goes into increasing the internal energy, and instead increases the entropy of the ice at a fixed temperature. That is, until the mass of ice turns into liquid.

The amount of energy required to cross a phase boundary in this way, per unit mass, is called *latent heat*. If you measure the heat capacity of a material by monitoring its temperature vs heat input, you would see a discontinuity at the phase transition, where latent heat is involved.

For a phase transition between 1 and 2 of a single component system, let the latent heat be $L$. Since $\Delta Q=T\Delta S$, and the latent heat is only involved in change entropy, the entropy difference between the two phases at the transition temperature $T_{pt}$ is:
$$
	\frac{\left< S_{2} \right> -\left< S_{1} \right> }{M} = \frac{L}{T_{pt}}
$$
Where $M$ is the mass of the material.
# Chemical reactions
Consider a mixture of $\left< N \right>$ molecules of all types. Define the number fraction be $x_{a}=\left< N_{a} \right> /\left< N \right>$ for particles labelled $a$. Recall from the definition of the absolute activity we have:
$$
	\lambda_{a} = e^{ \beta \mu_{a} }
$$
The ratio of $x_{a}$ and $\lambda_{a}$ is denoted as:
$$
	e^{ -\beta G^0_{a} } = \frac{x_{a}}{\lambda_{a}} = x_{a}e^{ -\beta \mu_{a} }
$$
Where $G^0_{a} = \mu^0_{a}-k_{B}T\log x_{a}$

Consider an example where reactants $a+b+c$ are in equilibrium with products $d+e$. If they are at chemical equilibrium, then:
$$
	\lambda_{a}\lambda_{b}\lambda_{c} = \lambda_{d}\lambda_{e} \implies \mu_{a}+\mu_{b}+\mu_{c} = \mu_{d} + \mu_{e}
$$
At any point where this is not true, a reaction is occurring.

The number fractions of the molecules at equilibrium are:
$$
	\eta = \frac{x_{a}b_{b}x_{c}}{x_{d}x_{e}} = e^{ -\Delta G^{0}/k_{B}T }
$$
Where $\Delta G^0=(G^0_{a}+G^0_{b}+G^0_{c}) - (G^0_{d}+G^0_{e})$ is called the *reaction energy*.

Now, note that for reactive chemicals, $\Delta G^0$ is ~1 eV, the typical energy scale for transferring electrons between atoms to make and break strong bonds. However, $k_{B}T$ at room temperature is just ~25 meV. This means that if $\Delta G^0$ is slightly positive, then $\eta\ll1$ and vice versa. This tells us that equilibrium between reactive chemicals at room temperature often heavily favour side, ideally the side of the products.
