Recall from last time that we found the definition of temperature:
$$
	T=\frac{2}{3k_{B}}\left< E_{k} \right>
$$
Where $\left< E_{k} \right>$ is the average kinetic energy per particle.

Furthermore, the force exerted onto the walls (if particles are inside of a box) is:
$$
	\left< F_{x} \right> = \frac{2}{3} \frac{\left< E_{k} \right> }{L_{x}}
$$
Where $L_{x}$ is the length of the box. From which, we derive something similar to the ideal gas law:
$$
	\left< P \right> V = Nk_{B}T = \frac{2N}{3} \left< E_{k} \right>
$$
$\left< P \right>$ is the pressure in the box, and $V$ is the volume of the box.
# When does the ideal gas law work?
Well, when we derived the law, we setup a simple system where point particles were bouncing around in a box.
- Point particles have 3 momentum dof
	- $V$ doesn't depend on $N$. We don't really care about how much empty space is in the box, even if there are a lot of particles filling it up
- Very short range interactions (at most they're bouncing on each other)
	- Small compared to the size of the particles
- Particles have no potential energy

If there aren't many particles, in comparison to the volume of the box
$$
	\frac{N}{V}=n \ll \frac{1}{(4 /3)\pi b^{2}}
$$
Where $b$ is the "range" of the interactions. Then we have something closer to an ideal gas

We assume that the particles aren't interacting with anything. However, they do interact with the walls of the box. So, when the box gets quite small, our assumptions fail.

If a particle is moving slowly enough, and it collides with the wall, it will stick to the wall because it is within the binding energy,
$$
	T\ll T_\text{binding} \propto  \frac{E_\text{binding}}{k_{B}}
$$
This is another example of a non-ideal gas. In the case of a liquid, for example, the particles are binding to each other. Another non-ideal gas.
# Internal Energy
Recall that the internal energy is the energy from the untracked degrees of freedom. For example, for a bunch of particles in a box, it is just the sum of the energy of all the particles,
$$
	\left< E \right> = N\left< E_{k} \right>
$$
Lets begin with an example. Lets say you drop a stone into a lake. The stone would splash, and then slowly drop to the bottom of the lake before stopping. Where did the energy go? Well, it went into the water (and perhaps the floor), the untracked degrees of freedom.
- This approach is called the *mechanical way*

The thermal way, on the other hand, supposes that you would put one cold substance in contact with a warmer substance. Like heating up a soup. In this case, energy is being transferred between two regions with untracked dof.

The first case is a transfer from a tracked dof to untracked. This is called *work*. The second case, from untracked to untracked, is called *heat*.
- Another way of thinking about the second, is that it is the transfer of internal energy
## First Law of Thermodynamics
$$
	d\left< E \right> =dW+dQ
$$
This is essentially saying that work and heat result in small changes in the total energy in a system.
- One main takeaway is that work and heat can be treated effectively the same.

Imagine we have a piston again. Particles in a box with one movable wall. The force applied to this wall, in terms of the pressure is,
$$
	F=P_\text{ext}A
$$
If you are pushing against the wall, for example, then you might be changing the energy inside the box,
$$
	d\left< E \right> =-P_\text{ext}A \, dx = -P_\text{ext} \, dV
$$
So a force closing up the box would increase the energy inside.

What about the other version? What if we place a box next to another one? Well the transfer of energy looks like,
$$
	dQ = d\left< E \right>
$$
Resulting from just the heat. Presumably, we would have the energy conducting from one box to the other (*diathermal*), and the energy would be insulated inside the receiving box (*adiabatic*).

Recall from the definition of temperature we have,
$$
	\left< E \right> =\frac{3}{2}Nk_{B}T \implies d\left< E \right> = \frac{3}{2} Nk_{B} \, dT
$$
Which ultimately tells us that,
$$
	dQ = \frac{3}{2} Nk_{B} \, dT
$$
This also introduces us to the concept of the heat capacity, or heat capacitance:
$$
	C=\frac{dQ}{dT}
$$
- I think the heat capacitance is the one that is per volume. Capacity changing depending on the volume

In this case, when the volume is static,
$$
	C_{V} = \frac{3}{2}Nk_{B}
$$
- There was a derivation for the capacitance when there is a constant pressure here, but I was behind, so here is the result
$$
	C_{P} = \frac{dQ}{dT} \bigg|_{P} = \frac{3}{2} Nk_{B} \, dT + Nk_{B} \, dt = C_{V} + Nk_{B}
$$
# Particles in a Box
However, this time we would like to use a diatonic gas. The particles are little bars with two atoms on the ends this time. (Before it was monotonic.)

Now we have 9 dof, adding in the 3 new rotational dof. However, because it's a bar, there is no $z$ axis rotation. The energy is:
$$
	E=\frac{p^{2}_{x}}{2m}+\frac{p^{2}_{y}}{2m}+\frac{p^{2}_{z}}{2m} + \frac{L^{2}_{x}}{2I_{x}}+\frac{L^{2}_{y}}{2I_{y}}
$$
So there are 5 energetic dof.

- It is worth noting that the bars can also stretch. However, for this case, we will ignore that stretching for now.